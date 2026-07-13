![](images/cover.jpg)

![Cover Page](images/cover.jpg)

# A Common-Sense Guide to Data Structures and Algorithms in JavaScript, Volume 1

### Level Up Your Core Programming Skills

### by Jay Wengrow

Version: P1.0 (August 2024)

Copyright © 2024 The Pragmatic Programmers, LLC. This book is licensed to the individual who purchased it. We don't copy-protect it because that would limit your ability to use it for your own purposes. Please don't break this trust—you can use this across all of your devices but please do not share this copy with other members of your team, with friends, or via file sharing services. Thanks.

Many of the designations used by manufacturers and sellers to distinguish their products are claimed as trademarks. Where those designations appear in this book, and The Pragmatic Programmers, LLC was aware of a trademark claim, the designations have been printed in initial capital letters or in all capitals. The Pragmatic Starter Kit, The Pragmatic Programmer, ...

# Early Praise for *A Common-Sense Guide to Data Structures and Algorithms in JavaScript, Volume 1*

This book is the best I’ve encountered on data structures and algorithms. It comprehensively explains key concepts in a manner that is both accessible and detailed, ideal for beginners as well as experienced programmers looking to enhance their skills. All these aspects make A Common-Sense Guide to Data Structures and Algorithms an essential reference in this domain. I highly recommend it!

| → | Boris Pietrzak |
|  | GIS developer, ChapsVision |

The author balances detail with brevity and a healthy sense of humor, making complex concepts more accessible and even fun to consider!

| → | Ann Clawson |
|  | Software Engineer |

Jay Wengrow places the reader in the driver’s seat from page one with real-world examples and explanations that actually make sense. This updated version takes an already great approach to data structures and algorithms and tailors it to developers interested in expanding their developer’s tool belt without having to learn yet another programming language. It’s got all the right stuff without any of the fluff.

| → | Jose Oseguera |
|  | Front-end Developer |

# Acknowledgments

While the task of writing a book may seem like a solitary one, this book simply could not have happened without the many people who have supported me in my journey writing it. I’d like to personally thank all of you.

To my wonderful wife, Rena—thank you for the time and emotional support you’ve given to me. You took care of everything while I hunkered down like a recluse and wrote. To my adorable kids, Tuvi, Leah, Shaya, Rami, and Yechiel—thank you for your patience as I wrote my book on “algorizms.” And yes—it’s finally done.

To my parents, Mr. and Mrs. Howard and Debbie Wengrow—thank you for initially sparking my interest in computer programming and helping me pursue it. Little did you know that getting me a computer tutor for ...

# 
Preface

Data structures and algorithms are more than abstract concepts. Mastering them enables you to write code that is efficient, leading to software that runs faster and consumes less memory. This is a big deal for today’s software applications, which exist on increasingly mobile platforms and handle increasingly greater amounts of data.

The problem with most resources on these subjects, though, is that they are...well...obtuse. Most texts go heavy on the math jargon, and if you’re not a mathematician, it can be difficult to grasp what on earth is going on. Even books that claim to make algorithms “easy” seem to assume that the reader has an advanced math degree. Because of this, too many people shy away from these concepts feeling that they’re not “smart” enough to understand them.

The truth, though, is that everything about data structures and algorithms boils down to common sense. Mathematical notation itself is simply a particular language, and everything in math can also be explained with common-sense terminology. In this book, I use that common-sense language (plus a lot of diagrams!) to explain these concepts in simple and, dare I say, enjoyable ways.

Once you understand these concepts, you’ll be equipped to write code that is efficient, fast, and elegant. You’ll be able to weigh the pros and cons of various code alternatives and be able to make educated decisions as to which code is best for the given situation.

In this book, I go out of my way to make these concepts real and practical with ideas that you can make use of today. Sure, you’ll learn some really cool computer science along the way. But this book is about taking that seemingly abstract stuff and making it directly practical. You’ll be writing better code and faster software by the time you’re done reading this book.

## Who Is This Book For?

This book is ideal for several audiences:

*   You’re a computer science student who wants a text that explains data structures and algorithms in plain English. This book can serve as a supplement to whatever “classic” textbook you happen to be using.

*   You’re a beginning developer who knows basic programming but wants to learn the fundamentals of computer science to write better code and increase your programming knowledge and skills.

*   You’re a self-taught developer who has never studied formal computer science (or a developer who did but forgot everything!) and wants to leverage the power of data structures and algorithms to write more scalable and elegant code.

Whoever you may be, I tried to write this book so that it can be ...

## The JavaScript Edition

All the code in this book is written in JavaScript. The original edition of this book, A Common-Sense Guide to Data Structures and Algorithms (the second edition of which was published in 2020), was language-agnostic; it was written using multiple programming languages. The idea behind this was that we didn’t want to imply that the book would only be helpful for one language, given that data structures and algorithms are concepts that apply across all of computing in general.

Over the years, I received feedback from readers who expressed that they would love to see language-specific editions of the book. After all, if you’re working with one particular programming language, wouldn’t it be nice to have a book in which all of the code is in that language?

Accordingly, I set out to create new single-language versions of A Common-Sense Guide to Data Structures and Algorithms. The first of these was the Python version, published in 2023\. The second version is the JavaScript edition and is what you’re reading now!

And because there’s so much to say about data structures and algorithms, this is the first volume in a progression of books. In this volume, I lay the foundation for these concepts and cover the most common data structures and algorithms. In the next volume, I’ll build upon this knowledge to level up further with more advanced ideas and techniques.

## A Note About the Code

The code in this book has been updated to follow ECMAScript 6+ standards. Where possible, I also strived to follow a modern JavaScript style inspired by the Airbnb JavaScript Style Guide.^([[1]](#f_0012.xhtml_FOOTNOTE-1)) That being said, I deviated from certain rules in cases where I thought that doing so would help keep the code easier to understand.

One such example is that JavaScript is blessed (or cursed, depending on your viewpoint) with many different types of loop syntax. Even though the modern forEach loop could be used in many of the code snippets, there are plenty of cases where it would not be the optimal choice. And I felt that having too many different types of loops across all the code snippets would be a little jarring. And so, to use ...

## What’s in This Book?

As you may have guessed, this book talks quite a bit about data structures and algorithms. More specifically, the book is laid out as follows:

In Chapter 1, [​*Why Data Structures Matter*​](#f_0013.xhtml_chp.understanding_data_structures) and Chapter 2, [​*Why Algorithms Matter*​](#f_0024.xhtml_chp.binary_search), I explain what data structures and algorithms are and explore the concept of time complexity—which is used to determine how fast an algorithm is. In the process, I also talk a great deal about arrays, sets, and binary search.

In Chapter 3, [​*O Yes! Big O Notation*​](#f_0031.xhtml_chp.big_o_notation), I unveil Big O notation and explain it in terms that are easy to understand. We use this notation throughout the book, so this chapter is pretty important.

In Chapter 4, [​*Speeding Up Your Code with Big O*​](#f_0040.xhtml_chp.speeding_up), Chapter 5, [​*Optimizing Code With and ...*](#f_0048.xhtml_chp.optimizing_big_o)

## How to Read This Book

You’ve got to read this book in order. In some books out there you can read each chapter independently and skip around a bit, but this isn’t one of them. Each chapter assumes you’ve read the previous ones, and the book is carefully constructed so you can ramp up your understanding as you proceed.

That being said, there are certain chapters in the latter half of the book that don’t depend entirely on each other. The diagram below depicts which chapters are prerequisites for other chapters.

![images/preface/chapters.png](images/preface/chapters.png)

For example, you could technically skip from Chapter 10 to Chapter 13 if you wanted to. (Oh! And this diagram is based on a data structure called a tree. You’re going to learn about it in Chapter 15.)

Another important note: to make this book easy to understand, I don’t always reveal everything about a particular concept when I first introduce it. Sometimes, the best way to break down a complex concept is to reveal a small piece of it and only reveal the next piece once the first piece has sunk in. If I define a particular term as such-and-such, don’t take that to be the textbook definition until you’ve completed the entire section on that topic.

It’s a trade-off: to make the book digestible, I’ve chosen to oversimplify certain concepts at first and clarify them over time rather than ensure that every sentence is completely, academically, accurate. But don’t worry too much, because by the end, you’ll see the entire accurate picture.

## Online Resources

This book has its own web page^([[3]](#f_0012.xhtml_FOOTNOTE-3)) on pragprog.com where you can find more information about the book, download the source code for the code examples, and help improve the book by reporting errata, typos, and content suggestions.

Additionally, I post updates about my writing at my website.^([[4]](#f_0012.xhtml_FOOTNOTE-4)) There you can find more information about my books as well as video tutorials made by my colleagues and me in which we use the “common-sense” approach to explaining all sorts of technologies and concepts. In particular, you might enjoy my “Jay Vs. Leetcode”^([[5]](#f_0012.xhtml_FOOTNOTE-5)) video series where I solve programming puzzles using many of the techniques discussed in this book.

## Connecting

I enjoy connecting with my readers and invite you to find me on LinkedIn.^([[6]](#f_0012.xhtml_FOOTNOTE-6)) I’d gladly accept your connection request—just send a message that you’re a reader of this book. I look forward to hearing from you!

Jay WengrowJune 2024

#### Footnotes

[[1]](#f_0008.xhtml_FNPTR-1)

[https://github.com/airbnb/javascript](https://github.com/airbnb/javascript)

[[2]](#f_0008.xhtml_FNPTR-2)

[https://pragprog.com/titles/jwjavascript](https://pragprog.com/titles/jwjavascript)

[[3]](#f_0011.xhtml_FNPTR-3)

[https://pragprog.com/titles/jwjavascript](https://pragprog.com/titles/jwjavascript)

[[4]](#f_0011.xhtml_FNPTR-4)

[https://commonsensedev.com](https://commonsensedev.com)

[[5]](#f_0011.xhtml_FNPTR-5)

[https://www.commonsensedev.com/jay-vs-leetcode](https://www.commonsensedev.com/jay-vs-leetcode)

[[6]](#f_0012.xhtml_FNPTR-6)

[https://www.linkedin.com/in/jaywengrow](https://www.linkedin.com/in/jaywengrow)

Copyright © 2024, The Pragmatic Bookshelf.

# Chapter 1Why Data Structures Matter

When people first learn to code, their focus is—and should be—on getting their code to run properly. Their code is measured using one simple metric: does the code actually work?

As software engineers gain more experience, though, they begin to learn about additional layers and nuances regarding the quality of their code. They learn that there can be two snippets of code that both accomplish the same task, but that one snippet is better than the other.

There are numerous measures of code quality. One important measure is code maintainability. Maintainability of code involves aspects such as the readability, organization, and modularity of one’s code.

However, another aspect of high-quality code is code

## Data Structures

Let’s talk about data.

Data is a broad term that refers to all types of information, down to the most basic numbers and strings. In the simple but classic “Hello World!” program, the string ’Hello World!’ is a piece of data. In fact, even the most complex pieces of data usually break down into a bunch of numbers and strings.

Data structures refer to how data is organized. You’re going to learn how the same data can be organized in a variety of ways.

Let’s look at the following code:

| ​  | x = 'Hello! ' |
| ​  | y = 'How are you ' |
| ​  | z = 'today?' |
| ​  |  |
| ​  | console.log(x + y + z) |

This simple program deals with three pieces of data, outputting three strings to make one coherent message. If we were to describe how the data is organized in this program, ...

## The Array: The Foundational Data Structure

The array is one of the most basic data structures in computer science. I assume you’ve worked with arrays before, so you’re aware that an array is a list of data elements. The array is versatile and can serve as a useful tool in many situations, but let’s take a look at one quick example.

If you’re looking at the source code for an application that allows users to create and use shopping lists for the grocery store, you might find code like this:

| ​  | array = ["apples", "bananas", "cucumbers", "dates", "elderberries"] |

This array happens to contain five strings, each representing something that I might buy at the supermarket. (You’ve got to try elderberries.)

Arrays come with their own technical jargon. ...

## Measuring Speed

So how do we measure the speed of an operation?

If you take away just one thing from this book, let it be this: when we measure how “fast” an operation is, we do not refer to how fast the operation takes in terms of pure time but instead in how many steps it takes.

We’ve actually seen this earlier in the context of printing the even numbers from 2 to 100\. The second version of that function was faster because it took half as many steps as the first version did.

Why do we measure code’s speed in terms of steps?

We do this because we can never say definitively that any operation takes, say, five seconds. While a piece of code may take five seconds on a particular computer, that same piece of code may take longer on an older piece ...

## Reading

The first operation we’ll look at is reading, which looks up what value is contained at a particular index inside the array.

A computer can read from an array in just one step. This is because the computer has the ability to immediately access any particular index in the array and peer inside. In our example of ["apples", "bananas", "cucumbers", "dates", "elderberries"], if we looked up index 2, the computer would jump right to index 2 and report that it contains the value "cucumbers".

How is the computer able to look up an array’s index in just one step? Let’s see how.

A computer’s memory can be viewed as a giant collection of cells. In the following diagram, you can see a grid of cells in which some are empty and some contain bits ...

## Searching

As I stated previously, searching an array means looking to see whether a particular value exists within an array and if so, at which index it’s located.

In a sense, it’s the inverse of reading. Reading means providing the computer an index and asking it to return the value contained there. Searching, on the other hand, means providing the computer a value and asking it to return the index of that value’s location.

While these two operations sound similar, there’s a world of difference between them when it comes to efficiency. Reading from an index is fast, since a computer can jump immediately to any index and discover the value contained there. Searching, though, is tedious since the computer has no way to immediately locate a particular ...

## Insertion

The efficiency of inserting a new piece of data into an array depends on where within the array you’re inserting it.

Let’s say we want to add "figs" to the end of our shopping list. Such an insertion takes just one step.

This is true due to another fact about computers: when allocating an array, the computer always keeps track of the array’s length.

When we couple this with the fact that the computer also knows at which memory address the array begins, computing the memory address of the last item of the array is a cinch: if the array begins at memory address 1010 and is of length 5, that means its final memory address is 1014\. So to insert an item beyond that would mean adding it to the next memory address, which is 1015.

Once the ...

## Deletion

Deletion from an array is the process of eliminating the value at a particular index.

Let’s return to our original example array and delete the value at index 2\. In our example, this value is "cucumbers".

Step 1: We delete "cucumbers" from the array:

![images/understanding_arrays/array_16.png](images/understanding_arrays/array_16.png)

While the actual deletion of "cucumbers" technically took just one step, we now have a problem: we have an empty cell sitting smack in the middle of our array. An array isn’t effective when there are gaps in the middle of it, so to resolve this issue, we need to shift "dates" and "elderberries" to the left. This means our deletion process requires additional steps.

Step 2: We shift "dates" ...

## Sets: How a Single Rule Can Affect Efficiency

Let’s explore this other data structure: the set. A set is a data structure that does not allow duplicate values to be contained within it.

Sets are of different types, but for this discussion, I’ll talk about an array-based set. This set is just like an array—it’s a simple list of values. The only difference between this set and a classic array is that the set never allows duplicate values to be inserted into it.

For example, if you had the set [’a’, ’b’, ’c’] and tried to add another ’b’, the computer just wouldn’t allow it, since a ’b’ already exists within the set.

Sets are useful when you need to ensure that you don’t have duplicate data.

For instance, if you’re creating an online phone book, ...

## Wrapping Up

Analyzing the number of steps an operation takes is the heart of understanding the performance of data structures. Choosing the right data structure for your program can spell the difference between bearing a heavy load versus collapsing under it. In this chapter, you’ve learned to use this analysis to weigh whether an array or a set might be the appropriate choice for a given application.

Now that you’ve begun to learn how to think about the time complexity of data structures, we can use the same analysis to compare competing algorithms (even within the same data structure) to ensure the ultimate speed and performance of our code. And that’s exactly what the next chapter is about.

## Exercises

The following exercises provide you with the opportunity to practice with arrays. The solutions to these exercises are found in the section [​*Chapter 1*​](#f_0206.xhtml_why.data.structures.matter.solutions).

1.  For an array containing 100 elements, provide the number of steps the following operations would take:
    1.  Reading
    2.  Searching for a value not contained within the array
    3.  Insertion at the beginning of the array
    4.  Insertion at the end of the array
    5.  Deletion at the beginning of the array
    6.  Deletion at the end of the array
2.  For an array-based set containing 100 elements, provide the number of steps the following operations would take:
    1.  Reading
    2.  Searching for a value not contained within the set
    3.  Insertion of a new value at the beginning of the set
    4.  Insertion of a new value at the end of the set
    5.  Deletion at the beginning of the set
    6.  Deletion at the end of the set
3.  Normally the search operation in an array looks for the first instance of a given value. But sometimes we may want to look for every instance of a given value. For example, say we want to count how many times the value "apple" is found inside an array. How many steps would it take to find all the "apple"s? Give your answer in terms of N.

Copyright © 2024, The Pragmatic Bookshelf.

# Chapter 2Why Algorithms Matter

In the previous chapter, we took a look at our first data structures and saw how choosing the right data structure can affect the performance of our code. Even two data structures that seem so similar, such as the array and the set, can have very different levels of efficiency.

In this chapter, we’re going to discover that even if we decide on a particular data structure, another major factor can affect the efficiency of our code: the proper selection of which algorithm to use.

Although the word algorithm sounds like something complex, it really isn’t. An algorithm is simply a set of instructions for completing a specific task.

Even a process as simple as preparing a bowl of cereal is technically an algorithm, ...

## Ordered Arrays

The ordered array is almost identical to the classic array we saw in the previous chapter. The only difference is that ordered arrays require that the values are always kept—you guessed it—in order; that is, every time a value is added, it gets placed in the proper cell so that the values in the array remain sorted.

For example, let’s take the array [3, 17, 80, 202]:

![images/binary_search/binary_search_1.png](images/binary_search/binary_search_1.png)

Assume we want to insert the value 75 into the array. If this array were a classic array, we could insert the 75 at the end, as follows:

![images/binary_search/binary_search_2.png](images/binary_search/binary_search_2.png)

As we saw in the previous chapter, ...

## Searching an Ordered Array

In the previous chapter, I described the process for searching for a particular value within a classic array: we check each cell one at a time—from left to right—until we find the value we’re looking for. I noted that this process is referred to as linear search.

Let’s see how linear search differs between a classic and an ordered array.

Say we have a regular array of [17, 3, 75, 202, 80]. If we were to search for the value 22—which happens to be nonexistent in this array—we would need to search each and every element because the 22 could potentially be anywhere in the array. The only time we could stop our search before we reach the array’s end is if we happen to find the value we’re looking for before we reach the ...

## Binary Search

You’ve probably played this guessing game as a child: I’m thinking of a number between 1 and 100\. Keep guessing which number I’m thinking of, and I’ll let you know whether you need to guess higher or lower.

You may know intuitively how to play this game. You wouldn’t begin by guessing number 1\. Instead, you’d probably start with 50, which is smack in the middle. Why? Because by selecting 50, no matter whether I tell you to guess higher or lower, you’ve automatically eliminated half the possible numbers!

If you guess 50 and I tell you to guess higher, you’d then pick 75, to eliminate half of the remaining numbers. If after guessing 75, I told you to guess lower, you’d pick 62 or 63\. You’d keep on choosing the halfway mark to keep ...

## Binary Search vs. Linear Search

With ordered arrays of a small size, the algorithm of binary search doesn’t have much of an advantage over linear search. But let’s see what happens with larger arrays.

With an array containing 100 values, here are the maximum number of steps each type of search would take:

*   Linear search: 100 steps
*   Binary search: 7 steps

With linear search, if the value we’re searching for is in the final cell or is greater than the value in the final cell, we have to inspect each and every element. For an array of size 100, this would take 100 steps.

When we use binary search, however, each guess we make eliminates half of the possible cells we’d have to search. In our very first guess, we get to eliminate a whopping fifty cells. ...

## Wrapping Up

Often there’s more than one way to achieve a particular computing goal, and the algorithm you choose can seriously affect the speed of your code.

It’s also important to realize that there usually isn’t a single data structure or algorithm that is perfect for every situation. For example, just because ordered arrays allow for binary search doesn’t mean you should always use ordered arrays. In situations where you don’t anticipate the need to search the data much but, instead, to add data, standard arrays may be a better choice because their insertion is faster.

As we’ve seen, the way to analyze competing algorithms is to count the number of steps each one takes. In the next chapter, we’re going to look at a formalized way of expressing the time complexity of competing data structures and algorithms. Having this common language will give us clearer information that will allow us to make better decisions about which algorithms we choose.

## Exercises

The following exercises provide you with the opportunity to practice with binary search. The solutions to these exercises are found in the section [​*Chapter 2*​](#f_0207.xhtml_why.algorithms.matter.solutions).

1.  How many steps would it take to perform a linear search for the number 8 in the ordered array [2, 4, 6, 8, 10, 12, 13]?

2.  How many steps would binary search take for the previous example?

3.  What is the maximum number of steps it would take to perform a binary search on an array of size 100,000?

Copyright © 2024, The Pragmatic Bookshelf.

# Chapter 3O Yes! Big O Notation

We’ve seen in the preceding chapters that the primary factor in determining an algorithm’s efficiency is the number of steps it takes.

However, we can’t simply label one algorithm a “22-step algorithm” and another a “400-step algorithm.” This is because the number of steps an algorithm takes cannot be pinned down to a single number. Let’s take linear search, for example. The number of steps linear search takes varies, as it takes as many steps as there are elements in the array. If the array contains 22 elements, linear search takes 22 steps. If the array contains 400 elements, however, linear search takes 400 steps.

The more effective way, then, to quantify the efficiency of linear search is to say that linear ...

## Big O: How Many Steps Relative to N Elements?

Big O achieves consistency by focusing on the number of steps an algorithm takes, but in a specific way. Let’s start off by applying Big O to the algorithm of linear search.

In a worst-case scenario, linear search will take as many steps as there are elements in the array. As we’ve previously phrased it: for N elements in the array, linear search can take up to N steps. The appropriate way to express this in Big O notation is:

O(N)

Some pronounce this as “Big Oh of N.” Others call it “Order of N.” My personal preference, however, is “Oh of N.”

Here’s what the notation means. It expresses the answer to what we’ll call the key question. The key question is this: if there are N data elements, how many ...

## The Soul of Big O

Now that we’ve encountered O(N) and O(1), we begin to see that Big O notation does more than simply describe the number of steps an algorithm takes, such as with a hard number like 22 or 400\. Rather, it’s an answer to that key question on your forehead: if there are N data elements, how many steps will the algorithm take?

While that key question is indeed the strict definition of Big O, there’s actually more to Big O than meets the eye.

Let’s say we have an algorithm that always takes three steps no matter how much data there is. That is, for N elements, the algorithm always takes three steps. How would you express that in terms of Big O?

Based on everything you’ve learned up to this point, you’d probably say that it’s O(3). ...

## An Algorithm of the Third Kind

In the previous chapter, you learned that binary search on an ordered array is much faster than linear search on the same array. Let’s now look at how to describe binary search in terms of Big O notation.

We can’t describe binary search as being O(1), because the number of steps increases as the data increases. It also doesn’t fit into the category of O(N), since the number of steps is much fewer than the N data elements. As we have seen, binary search takes only seven steps for an array containing 100 elements.

Binary search, then, seems to fall somewhere in between O(1) and O(N). So what is it?

In Big O terms, we describe binary search as having a time complexity of

O(log N).

I pronounce this as “Oh of log N.” ...

## Logarithms

Let’s examine why algorithms such as binary search are described as O(log N). What is a log, anyway?

Log is shorthand for logarithm. The first thing to note is that word logarithm has nothing to do with algorithm, even though the two words look and sound so similar.

Logarithms are the inverse of exponents. Here’s a quick refresher on what exponents are:

2³ is the equivalent of

2 * 2 * 2.

This just happens to be 8.

Now, log[2] 8 is the converse. It means: how many times do you have to multiply 2 by itself to get a result of 8?

Because you have to multiply 2 by itself three times to get 8, log[2] 8 = 3.

Here’s another example:

2⁶ translates to

2 * 2 * 2 * 2 * 2 * 2 = 64.

Because we had to multiply 2 by itself six times to get 64, we have, ...

## O(log N) Explained

Let’s bring this all back to Big O notation. In this book, whenever we say O(log N), imagine that we’re saying O(log[2] N). In [​*Ignoring Constants*​](#f_0052.xhtml_ignoring.constants), we’ll discuss why we’re dropping the base of 2 in our notation. But for now, when you see O(log N), treat it in your mind as O(log[2] N).

With this in mind, we can now explain precisely what O(log N) means.

Recall that Big O notation resolves the key question: if there are N data elements, how many steps will the algorithm take?

O(log N) means that for N data elements, the algorithm would take log[2] N steps. If there are 8 elements, the algorithm would take three steps, since log[2] 8 = 3.

Said another way, if we keep dividing the 8 elements in half, it would take us three steps until ...

## Practical Examples

Here’s some typical JavaScript code that prints all the items from a list:

| ​  | ​**let**​ things = [​*'apples'*​, ​*'baboons'*​, ​*'cribs'*​, ​*'dulcimers'*​]; |
| ​  |  |
| ​  | ​**for**​ (​**const**​ thing ​**of**​ things) { |
| ​  | console.log(​*`Here's a thing:* ​${thing}​*`*​); |
| ​  | } |

How would we describe the efficiency of this algorithm in Big O notation?

The first thing to realize is that this is an example of an algorithm. While it may not be fancy, any code that does anything at all is technically an algorithm—it’s a particular process for solving a problem. In this case, the problem is that we want to print all the items from a list. The algorithm we use to solve this problem is a for loop containing a console.log statement.

To break this down, we need to analyze how many ...

## Wrapping Up

With Big O notation, we have a consistent system that allows us to compare any two algorithms. With it, we’ll be able to examine real-life scenarios and choose between competing data structures and algorithms to make our code faster and able to handle heavier loads.

In the next chapter, we’ll encounter a real-life example in which we use Big O notation to speed up our code significantly.

## Exercises

The following exercises provide you with the opportunity to practice with Big O notation. The solutions to these exercises are found in the section [​*Chapter 3*​](#f_0208.xhtml_big.o.notation.solutions).

1.  Use Big O notation to describe the time complexity of the following function that determines whether a given year is a leap year:

    | ​  | ​**function**​ isLeapYear(year) { |
    | ​  | ​**if**​ (year % 100 === 0) { |
    | ​  | ​**if**​ (year % 400 === 0) { |
    | ​  | ​**return**​ ​**true**​; |
    | ​  | } ​**else**​ { |
    | ​  | ​**return**​ ​**false**​; |
    | ​  | } |
    | ​  | } |
    | ​  | ​**return**​ year % 4 === 0; |
    | ​  | } |

2.  Use Big O notation to describe the time complexity of the following function that sums up all the numbers from a given array:

    | ​  | ​**function**​ arraySum(array) { |
    | ​  | ​**let**​ sum = 0; |
    | ​  |  |
    | ​  | ​**for**​ (​**const**​ number ​**of**​ array) { |
    | ​  | sum += number; |
    | ​  | }; |
    | ​  |  |
    | ​  | ​**return**​ sum; |
    | ​  | } |

3.  The following function ...

# Chapter 4Speeding Up Your Code with Big O

Big O notation is a great tool for expressing the efficiency of an algorithm. We’ve already been able to use it to quantify the difference between binary search vs. linear search, as binary search is O(log N)—a much faster algorithm than linear search, which is O(N).

With Big O, you also have the opportunity to compare your algorithm to general algorithms out there in the world, and you can say to yourself, “Is this a fast or slow algorithm as far as algorithms generally go?”

If you find that Big O labels your algorithm as a slow one, you can now take a step back and try to figure out if there’s a way to optimize it by trying to get it to fall under a faster category of Big O. This may not always be ...

## Bubble Sort

Before jumping into our practical problem, though, we need to first look at a new category of algorithmic efficiency in the world of Big O. To demonstrate it, we’ll get to use one of the classic algorithms of computer-science lore.

Sorting algorithms have been the subject of extensive research in computer science, and tens of such algorithms have been developed over the years. They all solve the following problem:

Given an array of unsorted values, how can we sort them so that they end up in ascending order?

In this chapter and those following, we’re going to encounter a number of these sorting algorithms. Some of the first ones you’ll learn about are known as simple sorts, in that they are easy to understand but are not as efficient ...

## Bubble Sort in Action

Let’s walk through a complete example of Bubble Sort.

Assume we want to sort the array [4, 2, 7, 1, 3]. It’s currently out of order, and we want to produce an array that contains the same values in ascending order.

Let’s begin the first pass-through. This is our starting array:

![images/speeding_up_your_code_with_big_o/bubble_sort_5.png](images/speeding_up_your_code_with_big_o/bubble_sort_5.png)

Step 1: First, we compare the 4 and the 2:

![images/speeding_up_your_code_with_big_o/bubble_sort_6.png](images/speeding_up_your_code_with_big_o/bubble_sort_6.png)

Step 2: They’re out of order, so we swap them:

![images/speeding_up_your_code_with_big_o/bubble_sort_7.png](images/speeding_up_your_code_with_big_o/bubble_sort_7.png)

Step 3: Next, we compare the 4 and the 7:

They’re in the correct ...

## The Efficiency of Bubble Sort

The Bubble Sort algorithm contains two significant kinds of steps:

*   Comparisons: Two numbers are compared with one another to determine which is greater.

*   Swaps: Two numbers are swapped with one another to sort them.

Let’s start by determining how many comparisons take place in Bubble Sort.

Our example array has five elements. Looking back, you can see that in our first pass-through, we had to make four comparisons between sets of two numbers.

In our second pass-through, we only had to make three comparisons. This is because we didn’t have to compare the final two numbers, since we knew that the final number was in the correct spot due to the first pass-through.

In our third pass-through, we made two comparisons, ...

## A Quadratic Problem

Here’s a practical example of where we can replace a slow O(N²) algorithm with a speedy O(N) one.

Let’s say you’re working on a JavaScript application that analyzes the ratings people give to products, where users leave ratings from 0 to 10\. Specifically, you’re writing a function that checks whether an array of ratings contains any duplicate numbers. This will be used in more complex calculations in other parts of the software.

For example, the array [1, 5, 3, 9, 1, 4] has two instances of the number 1, so we’d return true to indicate that the array has a case of duplicate numbers.

One of the first approaches that may come to mind is the use of nested loops, as follows:

| ​  | ​**function**​ hasDuplicateValue(array) { |
| ​  | ​**for**​ (​ ... |

## A Linear Solution

What follows is another implementation of the hasDuplicateValue function that doesn’t rely on nested loops. It’s a bit clever, so let’s first look at how it works and then we’ll see if it’s any more efficient than our first implementation.

| ​  | ​**function**​ hasDuplicateValue(array) { |
| ​  | ​**const**​ existingNumbers = []; |
| ​  |  |
| ​  | ​**for**​ (​**let**​ i = 0; i < array.length; i += 1) { |
| ​  | ​**if**​ (existingNumbers[array[i]] === 1) { |
| ​  | ​**return**​ ​**true**​; |
| ​  | } ​**else**​ { |
| ​  | existingNumbers[array[i]] = 1; |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | ​**return**​ ​**false**​; |
| ​  | } |

Here’s what this function does. It creates an array called existingNumbers, which starts out empty.

Then we use a loop to check each number in the input array. As it encounters each number, it places an arbitrary value (we’ve chosen to use a 1) into existingNumbers at the index that is equal to the number we’re encountering.

For example, let’s say our input array is [3, 5, 8]. When we encounter the 3, we place a 1 at index 3 of existingNumbers. So the existingNumbers array will now be the rough equivalent of this:

| ​  | [0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0] |

There’s now a 1 at index 3 of existingNumbers, to indicate and remember for the future that we’ve already encountered a 3 in our given array.

When our loop then encounters the 5 from the given array, it adds a 1 to index 5 of existingNumbers:

| ​  | [0, 0, 0, 1, 0, 1, 0, 0, 0, 0, 0] |

Finally, when we reach the 8, existingNumbers will now look like this:

| ​  | [0, 0, 0, 1, 0, 1, 0, 0, 1, 0, 0] |

Essentially, we’re using the indexes of existingNumbers to remember which numbers from the array we’ve seen so far.

Now, here’s the real trick. Before the code stores a 1 in the appropriate index, it first checks to see whether that index already has a 1 as its value. If it does, this means we’ve already encountered that number, meaning we found a duplicate. If this is the case, we simply return true and cut the function short. If we get to the end of the loop without having returned true, it means there are no duplicates and we return false.

To determine the efficiency of this new algorithm in terms of Big O, we once again need to determine the number of steps the algorithm takes in a worst-case scenario.

Here, the significant type of step is looking at each number and checking whether the value of its index in existingNumbers is a 1:

| ​  | ​**if**​ (existingNumbers[array[i]] === 1) { |

(In addition to the comparisons, we also make insertions into the existingNumbers array, but we’re considering that kind of step trivial in this analysis. More on this in the next chapter.)

In terms of the worst-case scenario, such a scenario would occur when the array contains no duplicates, in which case our function must complete the entire loop.

This new algorithm appears to make N comparisons for N data elements. This is because there’s only one loop, and it simply iterates for as many numbers as there are in the array. We can test out this theory by tracking the steps in the JavaScript console:

| ​  | ​**function**​ hasDuplicateValue(array) { |
| ​  | ​**let**​ steps = 0; |
| ​  | ​**const**​ existingNumbers = []; |
| ​  |  |
| ​  | ​**for**​ (​**let**​ i = 0; i < array.length; i += 1) { |
| ​  | steps += 1; |
| ​  | ​**if**​ (existingNumbers[array[i]] === 1) { |
| ​  | ​**return**​ ​**true**​; |
| ​  | } ​**else**​ { |
| ​  | existingNumbers[array[i]] = 1; |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | console.log(steps); |
| ​  | ​**return**​ ​**false**​; |
| ​  | } |

If we run hasDuplicateValue([1, 4, 5, 2, 9]) now, we’ll see that the output in the JavaScript console is 5, which is the same as the size of our array. We’d find this to be true across arrays of all sizes. This algorithm, then, is O(N).

We know that O(N) is much faster than O(N²), so by using this second approach, we’ve optimized our hasDuplicateValue function significantly. This is a huge speed boost.

(One disadvantage with this new implementation is that this approach will consume more memory than the first approach. Don’t worry about this for now; we’ll discuss this at length in Chapter 19, [​*Dealing with Space Constraints*​](#f_0189.xhtml_chp.dealing_with_space_constraints).)

## Wrapping Up

It’s clear that having a solid understanding of Big O notation can enable you to identify slow code and select the faster of two competing algorithms.

However, in some situations Big O notation will have us believe that two algorithms have the same speed, while one is actually faster. In the next chapter, you’re going to learn how to evaluate the efficiencies of various algorithms even when Big O isn’t nuanced enough to do so.

## Exercises

The following exercises provide you with the opportunity to practice with speeding up your code. The solutions to these exercises are found in the section [​*Chapter 4*​](#f_0209.xhtml_speeding.up.your.code.with.big.o.solutions).

1.  Replace the question marks in the following table to describe how many steps occur for a given number of data elements across various types of Big O:

    | N Elements | O(N) | O(log N) | O(N²) |
    | --- | --- | --- | --- |
    | 100 | 100 | ? | ? |
    | 2,000 | ? | ? | ? |

2.  If we have an O(N²) algorithm that processes an array and find that it takes 256 steps, what is the size of the array?

3.  Use Big O notation to describe the time complexity of the following function. It finds the greatest product of any pair of two numbers within a given array:

    | ​  | ​**function**​ greatestProduct(array) { |
    | ​  | ​**if**​ (array.length < 2) { ​**return**​ ​**null**​; } |
    | ​  |  |
    | ​  | ​**let**​ greatestProductSoFar ... |

# Chapter 5
Optimizing Code With and Without Big O

We’ve seen that Big O notation is a great tool for comparing algorithms and determining which algorithm should be used for a given situation. However, it’s certainly not the only tool. In fact, there may be times when two competing algorithms are described in the same way using Big O, yet one algorithm is faster than the other.

In this chapter, you’re going to learn how to discern between two algorithms that seem to have the same efficiency and how to select the faster of the two.

## Selection Sort

In the previous chapter, we explored a sorting algorithm known as Bubble Sort, which had an efficiency of O(N²). We’re now going to dig into another sorting algorithm called Selection Sort and see how it measures up to Bubble Sort.

The steps of Selection Sort are as follows:

1.  We check each cell of the array from left to right to determine which value is least. As we move from cell to cell, we keep track of the lowest value we’ve encountered so far. (We’ll do this by storing its index in a variable.) If we encounter a cell that contains a value that is even lower than the one in our variable, we replace it so that the variable now points to the new index. See the following diagram:

2.  Once we’ve determined which index contains the ...

## Selection Sort in Action

Let’s walk through the steps of Selection Sort using the example array [4, 2, 7, 1, 3].

We begin our first pass-through:

We set things up by inspecting the value at index 0\. By definition, it’s the lowest value in the array we’ve encountered so far (as it’s the only value we’ve encountered so far), so we keep track of its index in a variable:

![images/optimizing_code_with_and_without_big_o/selection_sort_1.png](images/optimizing_code_with_and_without_big_o/selection_sort_1.png)

Step 1: We compare the 2 with the lowest value so far (which happens to be 4):

![images/optimizing_code_with_and_without_big_o/selection_sort_2.png](images/optimizing_code_with_and_without_big_o/selection_sort_2.png)

The 2 is even less than the 4, so it becomes the lowest value so far:

![images/optimizing_code_with_and_without_big_o/selection_sort_3.png](images/optimizing_code_with_and_without_big_o/selection_sort_3.png)

Step 2: We compare the next value—the 7—with the lowest value so far. The 7 is greater than the 2, so 2 remains our lowest value:

![images/optimizing_code_with_and_without_big_o/selection_sort_4.png](images/optimizing_code_with_and_without_big_o/selection_sort_4.png)

Step 3: We compare the 1 with the lowest value so far:

![images/optimizing_code_with_and_without_big_o/selection_sort_5.png](images/optimizing_code_with_and_without_big_o/selection_sort_5.png)

Because the 1 is even less than the 2, 1 becomes our new lowest value:

![images/optimizing_code_with_and_without_big_o/selection_sort_6.png](images/optimizing_code_with_and_without_big_o/selection_sort_6.png)

Step 4: We compare the 3 to the lowest value so far, which is the 1. We’ve reached the end of the array, and we’ve determined that 1 is the lowest value out of the entire array:

![images/optimizing_code_with_and_without_big_o/selection_sort_7.png](images/optimizing_code_with_and_without_big_o/selection_sort_7.png)

Step 5: Because 1 is the lowest value, we swap it with whatever value is at index 0—the index we began this pass-through with:

![images/optimizing_code_with_and_without_big_o/selection_sort_8.png](images/optimizing_code_with_and_without_big_o/selection_sort_8.png)

Since we’ve moved the lowest value to the beginning of the array, that means the lowest value is now in its correct spot:

![images/optimizing_code_with_and_without_big_o/selection_sort_9.png](images/optimizing_code_with_and_without_big_o/selection_sort_9.png)

We’re now ready to begin our second pass-through.

Setup: The first cell—index 0—is already sorted, so this pass-through begins at the next cell, which is index 1\. The value at index 1 is the number 2, and it’s the lowest value we’ve encountered in this pass-through so far:

![images/optimizing_code_with_and_without_big_o/selection_sort_10.png](images/optimizing_code_with_and_without_big_o/selection_sort_10.png)

Step 6: We compare the 7 with the lowest value so far. The 2 is less than the 7, so 2 remains our lowest value:

![images/optimizing_code_with_and_without_big_o/selection_sort_11.png](images/optimizing_code_with_and_without_big_o/selection_sort_11.png)

Step 7: We compare the 4 with the lowest value so far. The 2 is less than the 4, so 2 remains our lowest value:

![images/optimizing_code_with_and_without_big_o/selection_sort_12.png](images/optimizing_code_with_and_without_big_o/selection_sort_12.png)

Step 8: We compare the 3 with the lowest value so far. The 2 is less than the 3, so 2 remains our lowest value:

![images/optimizing_code_with_and_without_big_o/selection_sort_13.png](images/optimizing_code_with_and_without_big_o/selection_sort_13.png)

We’ve reached the end of the array. Since the lowest value from this pass-through was already in its correct spot, we don’t need to perform a swap. This ends our second pass-through, leaving us with this:

![images/optimizing_code_with_and_without_big_o/selection_sort_14.png](images/optimizing_code_with_and_without_big_o/selection_sort_14.png)

We now begin the third pass-through.

Setup: We begin at index 2, which contains the value 7\. The 7 is the lowest value we’ve encountered so far in this pass-through:

![images/optimizing_code_with_and_without_big_o/selection_sort_15.png](images/optimizing_code_with_and_without_big_o/selection_sort_15.png)

Step 9: We compare the 4 with the 7:

![images/optimizing_code_with_and_without_big_o/selection_sort_16.png](images/optimizing_code_with_and_without_big_o/selection_sort_16.png)

We note that 4 is our new lowest value:

![images/optimizing_code_with_and_without_big_o/selection_sort_17.png](images/optimizing_code_with_and_without_big_o/selection_sort_17.png)

Step 10: We encounter the 3, which is even lower than the 4:

![images/optimizing_code_with_and_without_big_o/selection_sort_18.png](images/optimizing_code_with_and_without_big_o/selection_sort_18.png)

The 3 becomes our new lowest value:

![images/optimizing_code_with_and_without_big_o/selection_sort_19.png](images/optimizing_code_with_and_without_big_o/selection_sort_19.png)

Step 11: We’ve reached the end of the array, so we swap the 3 with the value we started our pass-through with, which is the 7:

![images/optimizing_code_with_and_without_big_o/selection_sort_20.png](images/optimizing_code_with_and_without_big_o/selection_sort_20.png)

We now know that the 3 is in the correct place within the array:

![images/optimizing_code_with_and_without_big_o/selection_sort_21.png](images/optimizing_code_with_and_without_big_o/selection_sort_21.png)

While you and I can both see that the entire array is correctly sorted at this point, the computer doesn’t know this yet, so it must begin a fourth pass-through.

Setup: We begin the pass-through with index 3\. The 4 is the lowest value so far:

![images/optimizing_code_with_and_without_big_o/selection_sort_22.png](images/optimizing_code_with_and_without_big_o/selection_sort_22.png)

Step 12: We compare the 7 with the 4:

![images/optimizing_code_with_and_without_big_o/selection_sort_23.png](images/optimizing_code_with_and_without_big_o/selection_sort_23.png)

The 4 remains the lowest value we’ve encountered in this pass-through so far, so we don’t need to swap it, since it’s already in the correct place.

Because all the cells besides the last one are correctly sorted, that must mean the last cell is also in the correct order, and our entire array is properly sorted:

![images/optimizing_code_with_and_without_big_o/selection_sort_24.png](images/optimizing_code_with_and_without_big_o/selection_sort_24.png)

### Code Implementation: Selection Sort

Here’s an implementation of Selection Sort in JavaScript:

| ​  | ​**function**​ selectionSort(array) { |
| ​  | ​**for**​ (​**let**​ i = 0; i < array.length - 1; i += 1) { |
| ​  | ​**let**​ lowestNumberIndex = i; |
| ​  |  |
| ​  | ​**for**​ (​**let**​ j = i + 1; j < array.length; j += 1) { |
| ​  | ​**if**​ (array[j] < array[lowestNumberIndex]) { |
| ​  | lowestNumberIndex = j; |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | ​**if**​ (lowestNumberIndex !== i) { |
| ​  | [array[i], array[lowestNumberIndex]] = |
| ​  | [array[lowestNumberIndex], array[i]]; |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | ​**return**​ array; |
| ​  | } |

Let’s break this down line by line.

We begin a loop that represents each pass-through. It uses the variable i to point to each index of the array and goes up through the second-to-last value:

| ​  | ​**for**​ (​**let**​ i = 0; i < array.length - 1; i += 1) { |

It doesn’t need to run for the last value itself, since the array will be fully sorted by that point.

Next, begin keeping track of the index containing the lowest value we encounter so far:

| ​  | ​**let**​ lowestNumberIndex = i; |

This lowestNumberIndex will be 0 at the beginning of the first pass-through, 1 at the beginning of the second, and so on.

The reason we specifically keep track of the index is because we’ll need access to both the lowest value and its index in the rest of our code, and we can use the index to reference both. (We can check the lowest value by calling array[lowestNumberIndex]).

Within each pass-through, we check the remaining values of the array to see if there might be a lower value than the current lowest value:

| ​  | ​**for**​ (​**let**​ j = i + 1; j < array.length; j += 1) { |

Indeed, if we find a lower value, we store this new value’s index in lowestNumberIndex:

| ​  | ​**if**​ (array[j] < array[lowestNumberIndex]) { |
| ​  | lowestNumberIndex = j; |
| ​  | } |

By the end of the inner loop, we’ll have found the index of the lowest number from this pass-through.

If the lowest value from this pass-through is already in its correct place (which would happen when the lowest value is the first value we encounter in the pass-through), we don’t need to do anything. But if the lowest value is not in its correct place, we need to perform a swap. Specifically, we swap the lowest value with the value at i, which was the index we started the pass-through with:

| ​  | ​**if**​ (lowestNumberIndex !== i) { |
| ​  | [array[i], array[lowestNumberIndex]] = [array[lowestNumberIndex], array[i]]; |
| ​  | } |

Finally, we return the sorted array:

| ​  | ​**return**​ array; |

## The Efficiency of Selection Sort

Selection Sort contains two types of steps: comparisons and swaps. We compare each value with the lowest number we’ve encountered in each pass-through, and we swap the lowest number into its correct position.

Looking back at our example array that contains five elements, we had to make a total of 10 comparisons. Let’s break it down in the following table:

| Pass-Through # | # of Comparisons |
| --- | --- |
| 1 | 4 comparisons |
| 2 | 3 comparisons |
| 3 | 2 comparisons |
| 4 | 1 comparison |

That’s a grand total of 4 + 3 + 2 + 1 = 10 comparisons.

To put it in a way that works for arrays of all sizes, we’d say that for N elements, we make (N - 1) + (N - 2) + (N - 3) … + 1 comparisons.

As for swaps, though, we only need to make a maximum of one swap per pass-through. ...

## Ignoring Constants

But here’s the funny thing: in the world of Big O notation, Selection Sort and Bubble Sort are described in exactly the same way.

Again, Big O notation answers the key question: if there are N data elements, how many steps will the algorithm take? Because Selection Sort takes roughly half of N² steps, it would seem reasonable that we’d describe the efficiency of Selection Sort as being O(N² / 2). That is, for N data elements, there are N² / 2 steps. The following table bears this out:

| N Elements | N² / 2 | Max # of Steps in Selection Sort |
| --- | --- | --- |
| 5 | 5² / 2 = 12.5 | 14 |
| 10 | 10² / 2 = 50 | 54 |
| 20 | 20² / 2 = 200 | 209 |
| 40 | 40² / 2 = 800 | 819 |
| 80 | 80² / 2 = 3200 | 3239 |

In reality, however, Selection Sort is described in Big O as O(N²), just like Bubble Sort. This is because ...

## Big O Categories

This leads us to the next concept within Big O: Big O notation only concerns itself with general categories of algorithm speeds.

As an analogy, let’s talk about physical buildings. There are, of course, many different types of buildings. There are one-floor single-family homes, and two-floor single-family homes, and three-floor single-family homes. There are high-rise apartment buildings with varying numbers of floors. And there are skyscrapers with various heights and shapes.

If we were to compare two buildings, one of which is a single-family home and one of which is a skyscraper, it becomes almost moot to mention how many floors each one has. Because the two buildings are so incredibly different in their sizes and functions, we don’t need to say, “This one is a two-story home, while the other is a one-hundred-floor skyscraper.” We may as well just call one a house and the other a skyscraper. Calling them by their general categories is enough to signify their vast differences.

The same applies to algorithm efficiencies. If we compare, say, an O(N) algorithm with an O(N²) algorithm, the two efficiencies are so different that it doesn’t really matter whether the O(N) algorithm is actually O(2N), or O(N / 2) or even O(100N).

Now, here’s why O(N) and O(N²) are considered two separate categories, while O(N) and O(100N) are part of the same category.

Remember [​*The Soul of Big O*​](#f_0033.xhtml_sect.soul-of-big-o). Big O notation doesn’t care merely about the number of steps an algorithm takes. It cares about the long-term trajectory of the algorithm’s steps as the data increases. O(N) tells a story of straight growth—that the steps increase in a straight line according to some proportion of the data. This is true even when the steps are 100N. O(N²) tells a different story—one of exponential growth.

Exponential growth is a completely different category compared to any form of O(N). This point is really driven home when we consider that O(N²) will, at some point in data growth, become slower than O(N) multiplied by any factor.

In the following graph, you can see how O(N²) becomes slower than various factors of N:

![images/optimizing_code_with_and_without_big_o/o_n_2_vs_o_n_graph.png](images/optimizing_code_with_and_without_big_o/o_n_2_vs_o_n_graph.png)

Therefore, when comparing two efficiencies that belong to two different categories of Big O, it’s enough to identify them by their general category. Talking about O(2N) when compared to O(N²) is like talking about a two-story house compared to a skyscraper. We may as well just say that O(2N) is part of the general category of O(N).

All the types of Big O we’ve encountered, whether it’s O(1), O(log N), O(N), O(N²), or the types we’ll encounter later in this book, are general categories of Big O that are widely different from each other. Multiplying or dividing the number of steps by a regular number doesn’t make them change to another category.

However, when two algorithms fall under the same classification of Big O, it doesn’t necessarily mean that both algorithms have the same speed. After all, Bubble Sort is twice as slow as Selection Sort even though both are O(N²). So while Big O is perfect for contrasting algorithms that fall under different classifications of Big O, when two algorithms fall under the same classification, further analysis is required to determine which algorithm is faster.

### A Practical Example

Let’s return to the first code example from Chapter 1, with minor changes:

| ​  | ​**function**​ printNumbersVersionOne(upperLimit) { |
| ​  | ​**let**​ number = 2; |
| ​  |  |
| ​  | ​**while**​ (number <= upperLimit) { |
| ​  | ​**if**​ (number % 2 === 0) { |
| ​  | console.log(number); |
| ​  | } |
| ​  |  |
| ​  | number += 1; |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | ​**function**​ printNumbersVersionTwo(upperLimit) { |
| ​  | ​**let**​ number = 2; |
| ​  |  |
| ​  | ​**while**​ (number <= upperLimit) { |
| ​  | console.log(number); |
| ​  |  |
| ​  | number += 2; |
| ​  | } |
| ​  | } |

Here we have two algorithms for accomplishing the same task, namely printing all even numbers starting from 2 to some upperLimit. (In Chapter 1, the upper limit was fixed at 100, while here we let the user pass in a number as the upperLimit.)

I noted in Chapter 1 that the first version takes twice as many steps as the second version, but now let’s see how this plays out in terms of Big O.

Again, Big O expresses the answer to the key question: if there are N data elements, how many steps will the algorithm take? In this case, though, N isn’t the size of an array, but simply the number we pass into the function to serve as the upperLimit.

The first version takes about N steps. That is, if the upperLimit is 100, the function takes about 100 steps. (It really takes 99 steps since it starts the count at 2.) So we can safely say that the first algorithm has a time complexity of O(N).

The second version takes N / 2 steps. When the upperLimit is 100, the function takes just 50 steps. While it would be tempting to call this O(N / 2), you’ve now learned that we drop the constants and reduce the expression to O(N).

Now, the second version is twice as fast as the first one and would naturally be the better choice. This is another great example of where two algorithms can be expressed the same way using Big O notation but further analysis is needed to figure out which algorithm is faster.

### Significant Steps

Let’s apply one more level of analysis to the previous example. If we look again at the first version, printNumbersVersionOne, we said that it takes N steps. This is because the loop runs N times, with N being the upperLimit.

But does the function really take just N steps?

If we really break things down, we can see that multiple steps occur in each round of the loop.

First, we have the comparison step (if number % 2 == 0), which checks whether the number is divisible by 2\. This comparison happens in each round of the loop.

Second, we have the print step (console.log(number)), which happens just for the even numbers. This, then, occurs in every other round of the loop.

And third, we have number += 1, which runs in each round of the loop.

In the previous chapters, I alluded to the fact that you’d learn how to determine which steps are significant enough to be counted when expressing the Big O of an algorithm. In our case, then, which of these steps are considered significant? Do we care about the comparisons, the printing, or the incrementing of number?

The answer is that all steps are significant. It’s just that when we express the steps in Big O terms, we drop the constants and thereby simplify the expression.

Let’s apply this here. If we count all the steps, we have N comparisons, N incrementings, and N / 2 printings. This adds up to 2.5N steps. However, because we eliminate the constant of 2.5, we express this as O(N). So which step was significant? They all were, but by dropping the constant, we effectively focus more on the number of times the loop runs rather than the exact details of what happens within the loop.

## Wrapping Up

We now have some powerful analysis tools at our disposal. We can use Big O to broadly determine the efficiency of an algorithm, and we can also compare two algorithms that fall within one classification of Big O.

However, another important factor must be taken into account when comparing the efficiencies of two algorithms. Until now, we’ve focused on how fast an algorithm is in a worst-case scenario. Now, worst-case scenarios, by definition, don’t happen all the time. On average, most scenarios that occur are…well…average-case scenarios. In the next chapter, you’ll learn how to take all scenarios into account.

## Exercises

The following exercises provide you with the opportunity to practice analyzing algorithms. The solutions to these exercises are found in the section [​*Chapter 5*​](#f_0210.xhtml_optimizing.code.with.and.without.big.o.solutions).

1.  Use Big O notation to describe the time complexity of an algorithm that takes 4N + 16 steps.

2.  Use Big O notation to describe the time complexity of an algorithm that takes 2N².

3.  Use Big O notation to describe the time complexity of the following function, which returns the sum of all numbers of an array after the numbers have been doubled:

    | ​  | ​**function**​ doubleThenSum(array) { |
    | ​  | ​**const**​ doubledArray = []; |
    | ​  |  |
    | ​  | ​**for**​ (​**const**​ number ​**of**​ array) { |
    | ​  | doubledArray.push(number * 2); |
    | ​  | } |
    | ​  |  |
    | ​  | ​**let**​ sum = 0; |
    | ​  |  |
    | ​  | ​**for**​ (​**const**​ number ​**of**​ doubledArray) { |
    | ​  | sum += number; |
    | ​  | } |
    | ​  |  |
    | ​  | ​**return ...** |

# Chapter 6
Optimizing for Optimistic Scenarios

Until this point, we’ve focused primarily on how many steps an algorithm would take in a worst-case scenario. The rationale behind this is simple: if you’re prepared for the worst, things will turn out okay.

However, you’ll discover in this chapter that the worst-case scenario isn’t the only situation worth considering. Being able to consider all scenarios is an important skill that can help you choose the appropriate algorithm for every situation.

## Insertion Sort

We’ve previously encountered two different sorting algorithms: Bubble Sort and Selection Sort. Both have efficiencies of O(N²), but Selection Sort is actually twice as fast. Now you’ll learn about a third sorting algorithm called Insertion Sort that will reveal the power of analyzing scenarios beyond the worst case.

Insertion Sort consists of the following steps:

1.  In the first pass-through, we temporarily remove the value at index 1 (the second cell) and store it in a temporary variable. This will leave a gap at that index, since it contains no value:

    ![images/optimizing_for_optimistic_scenarios/insertion_sort_1.png](images/optimizing_for_optimistic_scenarios/insertion_sort_1.png)

    In subsequent pass-throughs, we remove the values at the subsequent indexes.

## Insertion Sort in Action

Let’s apply Insertion Sort to the array [4, 2, 7, 1, 3].

We begin the first pass-through by inspecting the value at index 1. This happens to contain the value 2:

![images/optimizing_for_optimistic_scenarios/insertion_sort_6.png](images/optimizing_for_optimistic_scenarios/insertion_sort_6.png)

Step 1: We temporarily remove the 2 and keep it inside a variable called tempValue. We represent this value by shifting it above the rest of the array:

![images/optimizing_for_optimistic_scenarios/insertion_sort_7.png](images/optimizing_for_optimistic_scenarios/insertion_sort_7.png)

Step 2: We compare the 4 to the tempValue, which is 2:

![images/optimizing_for_optimistic_scenarios/insertion_sort_8.png](images/optimizing_for_optimistic_scenarios/insertion_sort_8.png)

Step 3: Because 4 is greater than 2, we shift the 4 to the ...

## The Efficiency of Insertion Sort

Four types of steps occur in Insertion Sort: removals, comparisons, shifts, and insertions. To analyze the efficiency of Insertion Sort, we need to tally up each of these steps.

First, let’s dig into comparisons. A comparison takes place each time we compare a value to the left of the gap with the tempValue. In a worst-case scenario, where the array is sorted in reverse order, we have to compare every number to the left of tempValue with tempValue in each pass-through. This is because each value to the left of tempValue will always be greater than tempValue, so the pass-through will only end when the gap reaches the left end of the array.

During the first pass-through, in which tempValue is the value at index ...

## The Average Case

Indeed, in a worst-case scenario, Selection Sort is faster than Insertion Sort. However, it’s critical we also take into account the average-case scenario.

Why?

By definition, the cases that occur most frequently are average scenarios. Take a look at the [bell curve](#f_0060.xhtml_fig.ch6.bell_curve).

![images/optimizing_for_optimistic_scenarios/bell_curve.png](images/optimizing_for_optimistic_scenarios/bell_curve.png)

Best- and worst-case scenarios happen relatively infrequently. In the real world, average scenarios are what occur most of the time.

Take a randomly sorted array, for example. What are the odds that the values will occur in perfect ascending or descending order? It’s much more likely that the values will be all over the place.

Let’s examine Insertion Sort, then, in ...

## A Practical Example

Suppose you’re writing a JavaScript application, and somewhere in your code you find that you need to get the intersection between two arrays. The intersection is a list of all the values that occur in both of the arrays. For example, if you have the arrays [3, 1, 4, 2] and [4, 5, 3, 6], the intersection would be a third array [3, 4] since both of those values are common to the two arrays.

Here’s one possible implementation:

| ​  | ​**function**​ intersection(firstArray, secondArray) { |
| ​  | ​**const**​ result = []; |
| ​  |  |
| ​  | ​**for**​ (​**const**​ i ​**of**​ firstArray) { |
| ​  | ​**for**​ (​**const**​ j ​**of**​ secondArray) { |
| ​  | ​**if**​ (i === j) { |
| ​  | result.push(i); |
| ​  | } |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | ​**return**​ result; |
| ​  | } |

Here, we’re running nested loops. In the outer loop, we iterate over each value ...

## Wrapping Up

Being able to discern between best-, average-, and worst-case scenarios is a key skill in choosing the best algorithm for your needs, as well as taking existing algorithms and optimizing them further to make them significantly faster. Remember, while it’s good to be prepared for the worst case, average cases are what happen most of the time.

Now that we’ve covered the important concepts related to Big O notation, let’s apply our knowledge to practical algorithms. In the next chapter, we’re going to take a look at various everyday algorithms that may appear in real codebases and identify the time complexity of each one in terms of Big O.

## Exercises

The following exercises provide you with the opportunity to practice with optimizing for best- and worst-case scenarios. The solutions to these exercises are found in the section [​*Chapter 6*​](#f_0211.xhtml_optimizing.for.optimistic.scenarios.solutions).

1.  Use Big O notation to describe the efficiency of an algorithm that takes 3N² + 2N + 1 steps.

2.  Use Big O notation to describe the efficiency of an algorithm that takes N + log N steps.

3.  The following function checks whether an array of numbers contains a pair of two numbers that add up to 10.

    | ​  | ​**function**​ twoSum(array) { |
    | ​  | ​**for**​ (​**const**​ [indexI, i] ​**of**​ array.entries()) { |
    | ​  | ​**for**​ (​**const**​ [indexJ, j] ​**of**​ array.entries()) { |
    | ​  | ​**if**​ ((indexI !== indexJ) && (i + j === 10)) { |
    | ​  | ​**return**​ ​**true**​; |
    | ​  | } |
    | ​  | } |
    | ​  | } |
    | ​  |  |
    | ​  | ​**return**​ ​**false**​; |
    | ​  | } |

    What are the best-, ...

# Chapter 7Big O in Everyday Code

In the previous chapters, you learned how to use Big O notation to express the time complexity of code. As you’ve seen, quite a few details go into Big O analysis. In this chapter, we’ll use everything you’ve learned so far to analyze the efficiency of practical code samples that might be found in real-world codebases.

Determining the efficiency of our code is the first step in optimizing it. After all, if we don’t know how fast our code is, how would we know if our modifications would make it faster?

Additionally, once we know how our code is categorized in terms of Big O notation, we can make a judgment call as to whether it may need optimization in the first place. For example, an algorithm that is O(N²) is ...

## Mean Average of Even Numbers

The following method accepts an array of numbers and returns the mean average of all its even numbers. How would we express its efficiency in terms of Big O?

| ​  | ​**function**​ averageOfEvenNumbers(array) { |
| ​  | ​**let**​ sum = 0; |
| ​  | ​**let**​ countOfEvenNumbers = 0; |
| ​  |  |
| ​  | ​**for**​ (​**const**​ number ​**of**​ array) { |
| ​  | ​**if**​ (number % 2 === 0) { |
| ​  | sum += number; |
| ​  | countOfEvenNumbers += 1; |
| ​  | } |
| ​  | }; |
| ​  |  |
| ​  | ​**if**​ (countOfEvenNumbers === 0) { ​**return**​ ​**null**​; } |
| ​  |  |
| ​  | ​**return**​ Math.floor(sum / countOfEvenNumbers); |
| ​  | } |

Here’s how to break the code down to determine its efficiency.

Remember that Big O is all about answering the key question: if there are N data elements, how many steps will the algorithm take? Therefore, the first thing we want to do is determine what the N data elements are.

In this case, the algorithm is processing the array of numbers passed into this method. These, then, would be the N data elements, with N being the size of the array.

Next, we have to determine how many steps the algorithm takes to process these N values.

We can see the guts of the algorithm is the loop that iterates over each number inside the array, so we’ll want to analyze that first. Since the loop iterates over each of the N elements, we know the algorithm takes at least N steps.

Looking inside the loop, though, we can see that a varying number of steps occur within each round of the loop. For each and every number, we check whether the number is even. Then, if the number is even, we perform two more steps: we modify the sum variable, and we modify the countOfEvenNumbers variable. So we execute two more steps for even numbers than we do for odd numbers.

As you’ve learned, Big O focuses primarily on worst-case scenarios. In our case, the worst case is when all the numbers are even, in which case we perform three steps during each round of the loop. Because of this, we can say that for N data elements, our algorithm takes 3N steps. That is, for each of the N numbers, our algorithm executes three steps.

Now, our method performs a few other steps outside of the loop as well. Before the loop, we initialize the two variables and set them to 0\. Technically, these are two steps. After the loop, we perform another step: the division of sum / countOfEvenNumbers. Technically, then, our algorithm takes three extra steps in addition to the 3N steps, so the total number of steps is 3N + 3.

However, you also learned that Big O notation ignores constant numbers, so instead of calling our algorithm O(3N + 3), we simply call it O(N).

## Word Builder

The next example is an algorithm that collects every combination of two-character strings built from an array of single characters. For example, given the array ["a", "b", "c", "d"], we’d return a new array containing the following string combinations:

| ​  | [ |
| ​  | ​*'ab'*​, ​*'ac'*​, ​*'ad'*​, ​*'ba'*​, ​*'bc'*​, ​*'bd'*​, |
| ​  | ​*'ca'*​, ​*'cb'*​, ​*'cd'*​, ​*'da'*​, ​*'db'*​, ​*'dc'*​ |
| ​  | ] |

Following is an implementation of this algorithm. Let’s see if we can figure out its Big O efficiency:

| ​  | ​**function**​ wordBuilder(array) { |
| ​  | ​**const**​ collection = []; |
| ​  |  |
| ​  | ​**for**​ (​**const**​ [indexI, valueI] ​**of**​ array.entries()) { |
| ​  | ​**for**​ (​**const**​ [indexJ, valueJ] ​**of**​ array.entries()) { |
| ​  | ​**if**​ (indexI !== indexJ) { |
| ​  | collection.push(valueI + valueJ); |
| ​  | } |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | ​**return**​ collection; |
| ​  | } |

Here we’re running one loop nested inside another. The outer loop iterates over each character in the array, keeping track of the index of valueI. For each indexI, we run an inner loop that iterates again over each character in the same array using the index indexJ. Within this inner loop, we concatenate the characters at indexI and indexJ, with the exception of when indexI and indexJ are pointing to the same index.

To determine the efficiency of our algorithm, we once again need to determine what the N data elements are. In our case, as in the previous example, N is the number of items inside the array passed to the function.

The next step is to determine the number of steps our algorithm takes relative to the N data elements. In our case, the outer loop iterates over all N elements, and for each element, the inner loop iterates again over all N elements, which amounts to N steps multiplied by N steps. This is the classic case of O(N²) and is often what nested-loop algorithms turn out to be.

Now, what would happen if we modified our algorithm to compute each combination of three-character strings? For our example array of ["a", "b", "c", "d"], our function would return the following array:

| ​  | [ |
| ​  | ​*'abc'*​, ​*'abd'*​, ​*'acb'*​, |
| ​  | ​*'acd'*​, ​*'adb'*​, ​*'adc'*​, |
| ​  | ​*'bac'*​, ​*'bad'*​, ​*'bca'*​, |
| ​  | ​*'bcd'*​, ​*'bda'*​, ​*'bdc'*​, |
| ​  | ​*'cab'*​, ​*'cad'*​, ​*'cba'*​, |
| ​  | ​*'cbd'*​, ​*'cda'*​, ​*'cdb'*​, |
| ​  | ​*'dab'*​, ​*'dac'*​, ​*'dba'*​, |
| ​  | ​*'dbc'*​, ​*'dca'*​, ​*'dcb'*​ |
| ​  | ] |

Here’s an implementation that uses three nested loops. What is its time complexity?

| ​  | ​**function**​ wordBuilder(array) { |
| ​  | ​**const**​ collection = []; |
| ​  |  |
| ​  | ​**for**​ (​**const**​ [indexI, valueI] ​**of**​ array.entries()) { |
| ​  | ​**for**​ (​**const**​ [indexJ, valueJ] ​**of**​ array.entries()) { |
| ​  | ​**for**​ (​**const**​ [indexK, valueK] ​**of**​ array.entries()) { |
| ​  | ​**if**​ (indexI !== indexJ && indexJ !== indexK && indexI !== indexK) { |
| ​  | collection.push(valueI + valueJ + valueK); |
| ​  | } |
| ​  | } |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | ​**return**​ collection; |
| ​  | } |

In this algorithm, for N data elements, we have N steps of the “i” loop multiplied by the N steps of the “j” loop multiplied by the N steps of the “k” loop. This is N * N * N, which is N³ steps, which is described as O(N³).

If we had four or five nested loops, we’d have algorithms that are O(N⁴) and O(N⁵), respectively. Let’s take a look at how these all appear on a graph as [shown](#f_0066.xhtml_fig.ch7.big_o_graph_with_arrows).

![images/big_o_in_everyday_code/big_o_graph_with_arrows.png](images/big_o_in_everyday_code/big_o_graph_with_arrows.png)

Optimizing any code from a speed of O(N³) to O(N²) would be a big win since the code becomes exponentially faster. However, the algorithm above remains stuck at O(N³).

## Array Sample

In the next example, we create a function that takes a small sample of an array. We expect to have very large arrays, so our sample is just the first, middlemost, and last value from the array.

Here’s an implementation of this function. See if you can identify its efficiency in Big O:

| ​  | ​**function**​ sample(array) { |
| ​  | ​**if**​ (array.length === 0) { ​**return**​ ​**null**​; } |
| ​  |  |
| ​  | ​**const**​ first = array[0]; |
| ​  | ​**const**​ middle = array[Math.floor(array.length / 2)]; |
| ​  | ​**const**​ last = array[array.length - 1]; |
| ​  |  |
| ​  | ​**return**​ [first, middle, last]; |
| ​  | } |

In this case again, the array passed into this function is the primary data, so we can say that N is the number of elements in this array.

However, our function ends up taking the same number of steps no matter ...

## Average Celsius Reading

Here’s another example that involves mean averages. Let’s say we’re building weather-forecasting software. To determine the temperature of a city, we take temperature readings from many thermometers across the city, and we calculate the mean average of those temperatures.

We’d also like to display the temperatures in both Fahrenheit and Celsius, but our readings are initially only provided to us in Fahrenheit.

To get the average Celsius temperature, our algorithm does two things: first, it converts all the readings from Fahrenheit to Celsius. Then it calculates the mean average of all the Celsius numbers.

Below is some code that accomplishes this. What is its Big O?

| ​  | ​**function**​ averageCelsius(fahrenheitReadings) { |
| ​  |  |

## Clothing Labels

Suppose we’re writing software for a clothing manufacturer. Our code accepts an array of newly produced clothing items (stored as strings) and creates text for every possible label we’ll need.

Specifically, our labels should contain the item name plus its size, ranging from 1 to 5\. For example, if we have the array, ["Purple Shirt", "Green Shirt"], we want to produce label text for those shirts like this:

| ​  | [ |
| ​  | "Purple Shirt Size: 1", |
| ​  | "Purple Shirt Size: 2", |
| ​  | "Purple Shirt Size: 3", |
| ​  | "Purple Shirt Size: 4", |
| ​  | "Purple Shirt Size: 5", |

| ​  | "Green Shirt Size: 1", |
| ​  | "Green Shirt Size: 2", |
| ​  | "Green Shirt Size: 3", |
| ​  | "Green Shirt Size: 4", |
| ​  | "Green Shirt Size: 5" |
| ​  | ] |

Here’s code that will create this text for an entire array of clothing items: ...

## Count the Ones

Here’s another algorithm where the Big O is different from what it seems at first glance. This function accepts an array of arrays, where the inner arrays contain 1s and 0s. The function then returns how many 1s there are.

So take a look at this example input:

| ​  | [ |
| ​  | [0, 1, 1, 1, 0], |
| ​  | [0, 1, 0, 1, 0, 1], |
| ​  | [1, 0] |
| ​  | ] |

Our function will return 7 since there are seven 1s.

Here’s the function:

| ​  | ​**function**​ countOnes(outerArray) { |
| ​  | ​**let**​ count = 0; |
| ​  |  |
| ​  | ​**for**​ (​**const**​ innerArray ​**of**​ outerArray) { |
| ​  | ​**for**​ (​**const**​ number ​**of**​ innerArray) { |
| ​  | ​**if**​ (number === 1) { |
| ​  | count += 1; |
| ​  | } |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | ​**return**​ count; |
| ​  | } |

What’s the Big O of this algorithm?

Again, it’s easy to notice the nested loops and jump to the conclusion that it’s O(N²). However, ...

## Palindrome Checker

A palindrome is a word or phrase that reads the same both forward and backward. Some examples include racecar, kayak, and deified.

Here’s a function that determines whether a string is a palindrome:

| ​  | ​**function**​ isPalindrome(string) { |
| ​  | ​**let**​ leftIndex = 0; |
| ​  | ​**let**​ rightIndex = string.length - 1; |
| ​  |  |
| ​  | ​*// Iterate until leftIndex reaches the middle of the array:*​ |
| ​  | ​**while**​ (leftIndex < Math.floor(string.length / 2)) { |
| ​  | ​*// If the character on the left doesn't equal the character*​ |
| ​  | ​*// on the right, the string is not a palindrome:*​ |
| ​  | ​**if**​ (string[leftIndex] !== string[rightIndex]) { |
| ​  | ​**return**​ ​**false**​; |
| ​  | } |
| ​  |  |
| ​  | leftIndex += 1; |
| ​  | rightIndex -= 1; |
| ​  | } |
| ​  |  |
| ​  | ​*// If we got through the entire loop without finding any*​ |
| ​  | ​*// mismatches, ...* |

## Get All the Products

Our next example is an algorithm that accepts an array of numbers and returns the product of every combination of two numbers.

For example, if we passed in the array [1, 2, 3, 4, 5], the function returns:

| ​  | [2, 3, 4, 5, 6, 8, 10, 12, 15, 20] |

This is because we first multiply the 1 by the 2, 3, 4, and 5\. Then we multiply the 2 by the 3, 4, and 5\. Next, we multiply the 3 by the 4 and the 5\. And finally, we multiply the 4 by the 5.

Note something interesting: when we multiply, say, the 2 by the other numbers, we only have to multiply it by the numbers that are to the right of it. We don’t have to go back and multiply 2 by the 1, because that was already covered back when we multiplied the 1 by the 2\. So each number only needs ...

## Password Cracker

You’re a hacker (an ethical one, of course) who’s trying to figure out someone’s password. You decide on a brute-force approach and write some code that produces every possible string of a given length. Here’s the code you whipped up:

| ​  | ​**function**​ everyPassword(length) { |
| ​  | ​**let**​ string = ​*'a'*​.repeat(length); |
| ​  | console.log(string); |
| ​  |  |
| ​  | ​**while**​ (string !== ​*'z'*​.repeat(length)) { |
| ​  | ​**let**​ stringToBase36 = parseInt(string, 36); |
| ​  | stringToBase36 += 1; |
| ​  | string = (stringToBase36.toString(36)).replace(​*/0/g*​, ​*'a'*​); |
| ​  | console.log(string); |
| ​  | } |
| ​  | } |

There’s a bit of complicated magic in this code, which thankfully, we don’t need to understand at this time. That’s because we’re not going to focus on how this code works, but rather what ...

## Wrapping Up

Congratulations! You’re now a Big O pro. You can analyze all sorts of algorithms and categorize their time complexities. Armed with this knowledge, you’ll be able to methodically optimize your code for speed.

Speaking of which, in the next chapter, we’ll discover a new data structure that is one of the most useful and common tools for speeding up algorithms. And I’m talking about some serious speed.

## Exercises

The following exercises provide you with the opportunity to practice with algorithms in practical situations. The solutions to these exercises are found in the section [​*Chapter 7*​](#f_0212.xhtml_big.o.in.everyday.code.solutions).

1.  Use Big O notation to describe the time complexity of the following function. The function returns true if the array is a 100-sum array, and false if it is not.

    A 100-sum array meets the following criteria:

    *   Its first and last numbers add up to 100.
    *   Its second and second-to-last numbers add up to 100.
    *   Its third and third-to-last numbers add up to 100, and so on.

      Here’s the function:

    | ​  | ​**function**​ oneHundredSum(array) { |
    | ​  | ​**if**​ (array.length % 2 !== 0 &#124;&#124; array.length === 0) { |
    | ​  | ​**return**​ ​**false**​; |
    | ​  | } |
    | ​  |  |
    | ​  | ​**let**​ leftIndex = 0; |
    | ​  | ​**let**​ rightIndex = array.length - ... |

# Chapter 8
Blazing Fast Lookup with Hash Tables

Imagine you’re writing a program that allows customers to order fast food from a restaurant, and you’re implementing a menu of foods with their respective prices. You could, technically, use an array:

| ​  | menu = [ |
| ​  | [​*"french fries"*​, 0.75], |
| ​  | [​*"hamburger"*​, 2.5], |
| ​  | [​*"hot dog"*​, 1.5], |
| ​  | [​*"soda"*​, 0.6] |
| ​  | ] |

This array contains several subarrays, and each subarray contains two elements. The first element is a string representing the food on the menu, and the second element represents the price of that food.

As you learned in Chapter 2, [​*Why Algorithms Matter*​](#f_0024.xhtml_chp.binary_search), if this array were unordered, searching for the price of a given food would take O(N) steps since the computer would have to perform a linear search. If it’s an ordered array, the computer could do a binary search, which would take O(log N).

While O(log N) isn’t bad, we can do better. In fact, we can do much better. By the end of this chapter, you’ll learn how to use a special data structure called a hash table, which can be used to look up data in just O(1) time. By knowing how hash tables work under the hood and the right places to use them, you can leverage their tremendous lookup speeds in many situations.

## Hash Tables

Most programming languages include a data structure called a hash table, and it has an amazing superpower: fast reading. Note that hash tables are called by different names in various programming languages. In JavaScript they’re called objects, and other languages call them hashes, maps, hash maps, dictionaries, or associative arrays. We’ll refer to them as hash tables since that’s a common universal way to refer to this data structure.

Here’s an example of the menu as implemented with a hash table:

| ​  | ​**const**​ menu = { ​*"french fries"*​: 0.75, ​*"hamburger"*​: 2.5, |
| ​  | ​*"hot dog"*​: 1.5, ​*"soda"*​: 0.6 }; |

A hash table is a list of paired values. The first item in each pair is called the key, and the second item is called the value. In a hash table, the key and value have some significant association with one another. In this example, the string "french fries" is the key, and 0.75 is the value. They are paired together to indicate that french fries cost 75 cents.

In JavaScript, you can look up a key’s value using this syntax:

| ​  | menu[​*"french fries"*​]; |

This would return the value 0.75\. If we tried to look up a value that doesn’t exist with the hash table, we’d get back undefined.

Looking up a value in a hash table has an efficiency of O(1) on average, as it usually takes just one step. Let’s see why.

## Hashing with Hash Functions

Do you remember those secret codes you used as a kid to create and decipher messages? For example, here’s a simple way to map letters to numbers:

A = 1 B = 2 C = 3 D = 4 E = 5

and so on. According to this code,

ACE converts to 135, CAB converts to 312, DAB converts to 412,

and

BAD converts to 214.

This process of taking characters and converting them to numbers is known as hashing. And the code that is used to convert those letters into particular numbers is called a hash function.

Many other hash functions exist besides this one. Another example of a hash function may be to take each letter’s corresponding number and return the sum of all the numbers. If we did that, BAD would become the number 7, following a two-step ...

## Building a Thesaurus for Fun and Profit, but Mainly Profit

On nights and weekends, you’re single-handedly working on a stealth startup that will take over the world. It’s…a thesaurus app. But this isn’t any old thesaurus app—this is Quickasaurus. And you know that it will totally disrupt the billion-dollar thesaurus market. When a user looks up a word in Quickasaurus, it returns just one synonym, instead of every possible synonym, as old-fashioned thesaurus apps do.

Since every word has an associated synonym, this is a great use case for a hash table. After all, a hash table is a list of paired items. Let’s get started.

We can represent our thesaurus using a hash table:

| ​  | thesaurus = {}; |

Under the hood, a hash table stores its data in a bunch ...

## Hash Table Lookups

When we look up items from a hash table, we use a key to find its associated value. Let’s see how this works with our Quickasaurus example hash table.

Suppose we want to look up the value associated with the key "bad". In our code, we’d say this:

| ​  | thesaurus[​*"bad"*​] |

To find the value associated with "bad", the computer executes two simple steps:

1.  The computer hashes the key we’re looking up: BAD = 2 * 1 * 4 = 8.
2.  Since the result is 8, the computer looks inside cell 8 and returns the value stored there. In this case, that is the string "evil".

Let’s take a step back and look at the big picture here. In a hash table, the placement of each value is determined by its key; that is, by hashing the key itself, we compute the index number ...

## Dealing with Collisions

Hash tables are awesome but are not without complications.

Continuing our thesaurus example: what happens if we want to add the following entry into our thesaurus?

| ​  | thesaurus[​*"dab"*​] = ​*"pat"*​; |

First, the computer would hash the key:

DAB = 4 * 1 * 2 = 8

Then, it would try to add "pat" to our hash table’s cell 8:

![images/blazing_fast_lookup_with_hashes/hash_4.png](images/blazing_fast_lookup_with_hashes/hash_4.png)

Uh-oh. Cell 8 is already filled with "evil"—literally!

Trying to add data to a cell that is already filled is known as a collision. Fortunately, there are ways around it.

One classic approach for handling collisions is known as separate chaining. When a collision occurs, instead of placing a single value in the ...

## Making an Efficient Hash Table

Ultimately, a hash table’s efficiency depends on three factors:

*   How much data we’re storing in the hash table
*   How many cells are available in the hash table
*   Which hash function we’re using

It makes sense why the first two factors are important. If you have a lot of data and only a few cells, there will be many collisions and the hash table will lose its efficiency. Let’s explore, however, why the hash function itself is important for efficiency.

Let’s say we’re using a hash function that always produces a value that falls in the range from 1 to 9\. An example of this is a hash function that converts letters into their corresponding numbers and keeps adding the resulting digits together until it ends up with a single ...

## Hash Tables for Organization

Because hash tables keep data in pairs, they’re useful in many scenarios for organizing data.

Some data exists naturally in paired form. The fast-food menu and thesaurus scenarios from this chapter are classic examples. The menu contains each food item paired with its price. The thesaurus contains each word paired with its synonym. In fact, this is why JavaScript refers to hash tables as dictionaries. A dictionary is a common form of paired data; it’s a list of words with their respective definitions.

Other examples of naturally paired data can include tallies, such as political candidates and the number of votes each received:

| ​  | {​*"Candidate A"*​: 1402021, ​*"Candidate B"*​: 2321443, ​*"Candidate C"*​: 432} |

An inventory ...

## Hash Tables for Speed

While hash tables are a perfect fit for paired data, they can also be used to make your code faster—even if your data doesn’t exist as pairs. And this is where things get exciting.

Here’s a simple array:

| ​  | const array = [61, 30, 91, 11, 54, 38, 72]; |

If you want to search for a number in this array, how many steps would it take?

Because the array is unordered, you’d have to perform a linear search, which would take N steps—you learned this back at the beginning of the book.

However, what would happen if we ran some code that would convert these numbers into a hash table that looked like this?

| ​  | ​**const**​ hashTable = {61: ​**true**​, 30: ​**true**​, 91: ​**true**​, |
| ​  | 11: ​**true**​, 54: ​**true**​, 38: ​**true**​, 72: ​**true**​} |

Here, we’ve stored each ...

## Wrapping Up

Hash tables are indispensable when it comes to building efficient software. With their O(1) reads and insertions, it’s a difficult data structure to beat.

Until now, our analysis of various data structures revolved around their efficiency and speed. But did you know that some data structures provide advantages other than speed? In the next lesson, we’re going to explore two data structures that can help improve code elegance and maintainability.

## Exercises

The following exercises provide you with the opportunity to practice with hash tables. The solutions to these exercises are found in the section [​*Chapter 8*​](#f_0213.xhtml_blazing.fast.lookup.with.hashes.solutions).

1.  Write a function that returns the intersection of two arrays. The intersection is a third array that contains all values contained within the first two arrays. For example, the intersection of [1, 2, 3, 4, 5] and [0, 2, 4, 6, 8] is [2, 4]. Your function should have a complexity of O(N). (If your programming language has a built-in way of doing this, don’t use it. The idea is to build the algorithm yourself.)

2.  Write a function that accepts an array of strings and returns the first duplicate value it finds. For example, if the array is ["a", "b", "c", "d", "c", "e", "f"], the function ...

# Chapter 9
Crafting Elegant Code with Stacks and Queues

Until now, our discussion around data structures has focused primarily on how they affect the performance of various operations. However, having a variety of data structures in your programming arsenal also allows you to create code that is simpler and easier to read.

In this chapter, you’re going to discover two new data structures: stacks and queues. The truth is that these two structures are not entirely new. They’re simply arrays with restrictions. Yet these restrictions are exactly what make them so elegant.

More specifically, stacks and queues are elegant tools for handling temporary data. From operating system architecture to printing jobs to traversing data, stacks and queues serve as temporary containers that can be used to form beautiful algorithms.

Think of temporary data like the food orders in a diner. What each customer orders is important until the meal is made and delivered; then you throw the order slip away. You don’t need to keep that information around. Temporary data is information that doesn’t have any meaning after it’s processed, so you can throw it away once you’re done with it.

Stacks and queues handle this kind of temporary data but have a special focus on the order in which the data is handled, as you’ll now learn.

## Stacks

A stack stores data in the same way arrays do—it’s simply a list of elements. The one catch is that stacks have the following three constraints:

*   Data can be inserted only at the end of a stack.
*   Data can be deleted only from the end of a stack.
*   Only the last element of a stack can be read.

You can think of a stack as an actual stack of dishes; you can’t look at the face of any dish other than the one at the top. Similarly, you can’t add any dish except to the top of the stack, nor can you remove any dish besides the one at the top. (At least, you shouldn’t.) In fact, most computer science literature refers to the end of the stack as its top and the beginning of the stack as its bottom.

Our diagrams will reflect this terminology by viewing ...

## Abstract Data Types

Most programming languages don’t come with the stack as a built-in data type or class. Instead, it’s up to you to implement it yourself. This is a stark contrast with arrays, which are available in most languages.

To create a stack, then, you generally have to use one of the built-in data structures to hold the data. Here’s one way to implement a stack using JavaScript, which uses an array under the hood:

| ​  | ​**class**​ Stack { |
| ​  | ​**constructor**​() { |
| ​  | ​**this**​.data = []; |
| ​  | } |
| ​  |  |
| ​  | push(element) { |
| ​  | ​**this**​.data.push(element); |
| ​  | } |
| ​  |  |
| ​  | pop() { |
| ​  | ​**if**​ (​**this**​.data.length > 0) { |
| ​  | ​**return**​ ​**this**​.data.pop(); |
| ​  | } ​**else**​ { |
| ​  | ​**return**​ ​**null**​; |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | read() { |
| ​  | ​**if**​ (​**this**​.data.length > 0) { |
| ​  | ​**return**​ ​**this**​.data[​**this**​.data.length - 1]; ... |

## Stacks in Action

Although a stack isn’t typically used to store data on a long-term basis, it can be a great tool to handle temporary data as part of various algorithms. Let’s look at an example.

Let’s create the beginnings of a JavaScript linter—that is, a program that inspects a programmer’s JavaScript code and ensures that each line is syntactically correct. JavaScript is notorious for having an abundance of parentheses in its code, so that’s the aspect of syntax we’ll be focusing on. This includes parentheses, square brackets, and curly braces—all common causes of frustrating syntax errors.

To solve this problem, let’s first analyze what type of syntax is incorrect when it comes to braces. If we break it down, we’ll find three situations of erroneous syntax.

The first is when there’s an opening brace that doesn’t have a corresponding closing brace, such as this:

| ​  | (​**let**​ x = 2; |

We’ll call this Syntax Error Type #1.

The second is when there is a closing brace that was never preceded by a corresponding opening brace:

| ​  | ​**let**​ x = 2;) |

We’ll call that Syntax Error Type #2.

The third, which we’ll refer to as Syntax Error Type #3, is when a closing brace is not the same type of brace as the immediately preceding opening brace:

| ​  | (​**let**​ x = [1, 2, 3)]; |

In the preceding example, there’s a matching set of parentheses and a matching pair of square brackets, but the closing parenthesis is in the wrong place, as it doesn’t match the immediately preceding opening brace, which is a square bracket.

How can we implement an algorithm that inspects a line of JavaScript code and ensures that there are no brace-related syntax errors? This is where a stack allows us to implement a beautiful linting algorithm, which works as follows.

We first prepare an empty stack, and then we read each character from left to right following these rules:

1.  If we find any character that isn’t a type of brace (parenthesis, square bracket, or curly brace), we ignore it and move on.

2.  If we find an opening brace, we push it onto the stack. Having it on the stack means we’re waiting to close that particular brace.

3.  If we find a closing brace, we pop the top element in the stack and inspect it. We then analyze:

    *   If the item we popped (which is always an opening brace) does not match the current closing brace, it means we’ve encountered Syntax Error Type #3.

    *   If we couldn’t pop an element because the stack was empty, that means the current closing brace doesn’t have a corresponding opening brace beforehand. This is Syntax Error Type #2.

    *   If the item we popped is a corresponding match for the current closing brace, it means we’ve successfully closed that opening brace, and we can continue parsing the line of JavaScript code.

4.  If we make it to the end of the line and there’s still something left on the stack, that means there’s an opening brace without a corresponding closing brace, which is Syntax Error Type #1.

Let’s see this in action using the following example:

![images/stacks_and_queues/parens_1_new.png](images/stacks_and_queues/parens_1_new.png)

After we prepare an empty stack, we begin reading each character from left to right.

Step 1: We begin with the first character, which happens to be an opening parenthesis:

![images/stacks_and_queues/parens_2_new.png](images/stacks_and_queues/parens_2_new.png)

Step 2: Since it’s a type of opening brace, we push it onto the stack:

![images/stacks_and_queues/push_open_parens.png](images/stacks_and_queues/push_open_parens.png)

We then ignore all the characters let x = since they aren’t brace characters.

Step 3: We encounter our next opening brace:

![images/stacks_and_queues/parens_3_new.png](images/stacks_and_queues/parens_3_new.png)

Step 4: We push it onto the stack:

![images/stacks_and_queues/push_open_curly_brace.png](images/stacks_and_queues/push_open_curly_brace.png)

We then ignore the y:.

Step 5: We encounter the opening square bracket:

![images/stacks_and_queues/parens_4_new.png](images/stacks_and_queues/parens_4_new.png)

Step 6: We add that to the stack as well:

![images/stacks_and_queues/push_open_square_bracket.png](images/stacks_and_queues/push_open_square_bracket.png)

We then ignore the 1, 2, 3.

Step 7: We encounter our first closing brace—a closing square bracket:

![images/stacks_and_queues/first_closing_brace_new.png](images/stacks_and_queues/first_closing_brace_new.png)

Step 8: We pop the element at the top of the stack, which happens to be an opening square bracket:

![images/stacks_and_queues/pop_square_bracket.png](images/stacks_and_queues/pop_square_bracket.png)

Since our closing square bracket is a corresponding match to this top element of the stack, it means we can continue with our algorithm without throwing any errors.

Step 9: We move on, encountering a closing curly brace:

![images/stacks_and_queues/parens_6_new.png](images/stacks_and_queues/parens_6_new.png)

Step 10: We pop the top item from stack:

![images/stacks_and_queues/pop_curly_brace.png](images/stacks_and_queues/pop_curly_brace.png)

It’s an opening curly brace, so we’ve found a match with the current closing brace.

Step 11: We encounter a closing parenthesis:

![images/stacks_and_queues/parens_7_new.png](images/stacks_and_queues/parens_7_new.png)

Step 12: We pop the last element in the stack. It’s a corresponding match, so there are no errors so far.

Because we’ve made it through the entire line of code and our stack is empty, our linter can conclude that there are no syntactical errors on this line (relating to opening and closing braces).

### Code Implementation: Stack-Based Code Linter

Here’s an implementation of the preceding algorithm. Note that we’re using our earlier implementation of the Stack class:

| ​  | ​**import**​ Stack ​**from**​ ​*'./stack.js'*​; |
| ​  |  |
| ​  | ​**class**​ Linter { |
| ​  | ​**constructor**​() { |
| ​  | ​**this**​.stack = ​**new**​ Stack(); |
| ​  | } |
| ​  |  |
| ​  | lint(text) { |
| ​  | ​**while**​ (​**this**​.stack.read()) { |
| ​  | ​**this**​.stack.pop(); |
| ​  | } |
| ​  |  |
| ​  | ​**const**​ matchingBraces = { ​*'('*​: ​*')'*​, ​*'['*​: ​*']'*​, ​*'{'*​: ​*'}'*​ }; |
| ​  |  |
| ​  | ​**for**​ (​**const**​ ​**char**​ ​**of**​ text) { |
| ​  | ​**if**​ (matchingBraces[​**char**​]) { |
| ​  | ​**this**​.stack.push(​**char**​); |
| ​  | } ​**else**​ ​**if**​ (Object.values(matchingBraces).includes(​**char**​)) { |
| ​  | ​**if**​ (!​**this**​.stack.read()) { |
| ​  | ​**return**​ ​*`*​${​**char**​}​ *does not have opening brace`*​; |
| ​  | } ​**else**​ { |
| ​  | ​**const**​ poppedOpeningBrace = ​**this**​.stack.pop(); |
| ​  |  |
| ​  | ​**if**​ (​**char**​ !== matchingBraces[poppedOpeningBrace]) { |
| ​  | ​**return**​ ​*`*​${​**char**​}​ *has mismatched opening brace`*​; |
| ​  | } |
| ​  | } |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | ​*// If we get to the end of line, and the stack isn't empty:*​ |
| ​  | ​**if**​ (​**this**​.stack.read()) { |
| ​  | ​**return**​ ​*`*​${​**this**​.stack.read()}​ *does not have closing brace`*​; |
| ​  | } |
| ​  |  |
| ​  | ​*// Return true if line has no errors:*​ |
| ​  | ​**return**​ ​**true**​; |
| ​  | } |
| ​  | } |

The import Stack from ’./stack.js’ allows our code to use our own stack implementation from above, as we saved it in a file called stack.js.

As soon as we create an instance of the Linter class, we create a stack that our algorithm can use. This is accomplished with the following code:

| ​  | ​**constructor**​() { |
| ​  | ​**this**​.stack = ​**new**​ Stack(); |
| ​  | } |

The main linting algorithm takes place within the lint method, which accepts a string of JavaScript code and assigns it to a variable called text.

The very first thing we do is ensure that the stack is empty, as it still may have data in it from a previous linting. We accomplish this by popping data from the stack until there’s no data left:

| ​  | ​**while**​ (​**this**​.stack.read()) { |
| ​  | ​**this**​.stack.pop(); |
| ​  | } |

We then define what we consider to be sets of matching brackets:

| ​  | ​**const**​ matchingBraces = { ​*'('*​: ​*')'*​, ​*'['*​: ​*']'*​, ​*'{'*​: ​*'}'*​ }; |

We’re now up to the main part of the algorithm, which runs using a loop that analyzes each character of text, one at a time:

| ​  | ​**for**​ (​**const**​ ​**char**​ ​**of**​ text) { |

If the character we’re up to is an opening brace, we push it onto the stack:

| ​  | ​**if**​ (matchingBraces[​**char**​]) { |
| ​  | ​**this**​.stack.push(​**char**​); |
| ​  | } |

If the current character is not an opening brace, we then check to see if it’s perhaps a closing brace:

| ​  | ​**else**​ ​**if**​ (Object.values(matchingBraces).includes(​**char**​)) { |

The Object.values method gives us an array of all the values of the matchingBraces object (that is, a hash table) without the keys. In our case, these values are all the closing braces.

If the current character is a closing brace, we then consider a couple of possibilities. We first check to see if there’s anything on the stack. If there isn’t, we trigger Syntax Error #2:

| ​  | ​**if**​ (!​**this**​.stack.read()) { |
| ​  | ​**return**​ ​*`*​${​**char**​}​ *does not have opening brace`*​; |
| ​  | } |

If there is something on the stack, we pop it off and check to see if it’s a matching opening brace. If it isn’t, we trigger Syntax Error #3:

| ​  | ​**else**​ { |
| ​  | ​**const**​ poppedOpeningBrace = ​**this**​.stack.pop(); |
| ​  |  |
| ​  | ​**if**​ (​**char**​ !== matchingBraces[poppedOpeningBrace]) { |
| ​  | ​**return**​ ​*`*​${​**char**​}​ *has mismatched opening brace`*​; |
| ​  | } |
| ​  | } |

The loop continues this way until it processes the entire text.

However, we’re not quite done. We still have to check whether the stack contains anything, because if it does, it means we have a stray opening brace that was never closed. This, again, is Syntax Error #1:

| ​  | ​**if**​ (​**this**​.stack.read()) { |
| ​  | ​**return**​ ​*`*​${​**this**​.stack.read()}​ *does not have closing brace`*​; |
| ​  | } |

At the end of our method we return true if we process the entire text and don’t encounter any errors.

Here’s some sample code to run our linter:

| ​  | ​**const**​ linter = ​**new**​ Linter(); |
| ​  | linter.lint(​*'(let x = 2;'*​) |

This example will trigger Syntax Error #1 since the opening parenthesis has no closing parenthesis.

In this example, we used a stack to implement our linter with a neat algorithm. But if a stack actually uses an array under the hood, why bother with a stack? Couldn’t we have accomplished the same task using an array?

## The Importance of Constrained Data Structures

By definition, if a stack is just a constrained version of an array, that means an array can do anything a stack can do. If so, what advantage does a stack provide?

Constrained data structures like the stack (and the queue, which we’ll encounter shortly) are important for several reasons.

First, when we work with a constrained data structure, we can prevent potential bugs. The linting algorithm, for example, only works if we exclusively remove items from the top of the stack. If a programmer inadvertently writes code that removes items from the middle of the array, the algorithm will break down. By using a stack, we’re forced into only removing items from the top, as it’s impossible to get the stack ...

## Queues

A queue is another data structure designed to process temporary data. It’s like a stack in many ways, except that it processes data in a different order. Like a stack, a queue is also an abstract data type.

You can think of a queue as a line of people at the movie theater. The first one in the line is the first one to leave the line and enter the theater. With queues, the first item added to the queue is the first item to be removed. That’s why computer scientists apply the acronym FIFO to queues: first in, first out.

As with a line of people, a queue is usually depicted horizontally. It’s also common to refer to the beginning of the queue as its front and the end of the queue as its back.

Like stacks, queues are arrays with three ...

## Queues in Action

Queues are common in many applications, ranging from printing jobs to background workers in web applications.

Let’s say we’re programming a simple JavaScript interface for a printer that can accept printing jobs from various computers across a network. We want to make sure we print each document in the order in which it was received.

This code uses our implementation of the Queue class from earlier:

| ​  | ​**import**​ Queue ​**from**​ ​*'./queue.js'*​; |
| ​  |  |
| ​  | ​**class**​ PrintManager { |
| ​  | ​**constructor**​() { |
| ​  | ​**this**​.queue = ​**new**​ Queue(); |
| ​  | } |
| ​  |  |
| ​  | queuePrintJob(document) { |
| ​  | ​**this**​.queue.enqueue(document); |
| ​  | } |
| ​  |  |
| ​  | run() { |
| ​  | ​**while**​ (​**this**​.queue.read()) { |
| ​  | ​**this**​.printDocument(​**this**​.queue.dequeue()); |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | printDocument(document) { |
| ​  | ​*// Code ...* |

## Wrapping Up

As you’ve seen, stacks and queues are programmers’ tools for elegantly handling all sorts of practical algorithms.

Now that you’ve learned about stacks and queues, you’ve unlocked a new achievement: you can learn about recursion, which depends upon a stack. Recursion also serves as the foundation for many of the more advanced and super-efficient algorithms that I’ll cover in the rest of this book.

## Exercises

The following exercises provide you with the opportunity to practice with stacks and queues. The solutions to these exercises are found in the section [​*Chapter 9*​](#f_0214.xhtml_stacks.and.queues.solutions).

1.  If you were writing software for a call center that places callers on hold and then assigns them to “the next available representative,” would you use a stack or a queue?

2.  If you pushed numbers onto a stack in the following order: 1, 2, 3, 4, 5, 6, and then popped two items, which number would you be able to read from the stack?

3.  If you inserted numbers into a queue in the following order: 1, 2, 3, 4, 5, 6, and then dequeued two items, which number would you be able to read from the queue?

4.  Write a function that uses a stack to reverse a string. (For example, "abcde" would ...

# Chapter 10Recursively Recurse with Recursion

Recursion is a key concept in computer science that will unlock the more advanced algorithms we’re going to encounter in this book. When used correctly, recursion can be used to solve certain types of tricky problems in surprisingly simple ways. Sometimes, it even seems like magic.

But before we dive in, a pop quiz!

What happens when the blah() function defined here is called?

| ​  | ​**function**​ blah() { |
| ​  | blah(); |
| ​  | } |

As you may have guessed, it will call itself infinitely, since blah() calls itself, which in turn calls itself, and so on.

Recursion is the term for a function calling itself. Indeed, infinite recursion, as in the above example, is utterly useless. When harnessed correctly, though, recursion ...

## Recurse Instead of Loop

Let’s say you work at NASA and need to program a countdown function for launching spacecraft. The particular function that you’re asked to write should accept a number—such as 10—and display the numbers from 10 down to 0.

Take a moment and implement this function yourself. When you’re done, read on.

Odds are that you wrote a simple loop, along the lines of this implementation:

| ​  | ​**function**​ countdown(number) { |
| ​  | ​**while**​ (number >= 0) { |
| ​  | console.log(number); |
| ​  | number -= 1; |
| ​  | } |
| ​  | } |

Nothing is wrong with this implementation, but it may have never occurred to you that you don’t have to use a loop.

How?

Let’s try recursion instead. Here’s a first attempt at using recursion to implement our countdown function:

| ​  | ​**function**​ countdown(number) ... |

## The Base Case

Let’s continue our walk-through of the countdown function. We’ll skip a few steps for brevity…

Step 21: We call countdown(0).

Step 22: We print number (that is, 0) to the console.

Step 23: We call countdown(-1).

Step 24: We print number (that is, -1) to the console.

Uh-oh. As you can see, our solution isn’t perfect, as we’ll end up infinitely printing negative numbers.

To perfect our solution, we need a way to end our countdown at 0 and prevent the recursion from continuing on forever.

We can solve this problem by adding a conditional statement that ensures that if number is currently 0, we don’t call countdown() again:

| ​  | ​**function**​ countdown(number) { |
| ​  | console.log(number); |
| ​  |  |
| ​  | ​**if**​ (number === 0) { |
| ​  | ​**return**​; |
| ​  | } ​**else**​ { |
| ​  |  |

## Reading Recursive Code

It takes time and practice to get used to recursion, and you’ll ultimately learn two sets of skills: reading recursive code and writing recursive code. Reading recursive code is somewhat easier, so let’s get some practice with that first.

We’ll do this by looking at another example: calculating factorials.

A factorial is best illustrated with some examples.

This is the factorial of 3:

3 * 2 * 1 = 6

This is the factorial of 5:

5 * 4 * 3 * 2 * 1 = 120

And so on and so forth.

Here’s a recursive implementation that returns a number’s factorial:

| ​  | ​**function**​ factorial(number) { |
| ​  | ​**if**​ (number <= 1) { |
| ​  | ​**return**​ 1; |
| ​  | } ​**else**​ { |
| ​  | ​**return**​ number * factorial(number - 1); |
| ​  | } |
| ​  | } |

This code can look somewhat confusing at first ...

## Recursion in the Eyes of the Computer

To complete your understanding of recursion, we need to see how the computer itself processes a recursive function. It’s one thing for humans to reason about recursion using the earlier “napkin” method. However, the computer has to do the tricky work of calling a function from within the function itself. So let’s break down the process of how the computer executes a recursive function.

Say that we call factorial(3). Since 3 isn’t the base case, the computer reaches this line:

| ​  | ​**return**​ number * factorial(number - 1); |

This then launches the function factorial(2).

But there’s a catch. When the computer begins to run factorial(2), did the computer yet complete running factorial(3)?

This is what makes recursion ...

## Filesystem Traversal

Now that you’ve seen how recursion works, we can use it to solve certain problems that would otherwise be uncrackable.

One type of problem in which recursion is a natural fit is when we need to delve into multiple layers of a problem without knowing how many layers there are.

Take the example of traversing through a filesystem. Let’s say you have a script that does something with all the contents inside a directory, such as printing all the subdirectory names. However, you don’t want the script to only handle the immediate subdirectories—you want it to act on all the subdirectories within the subdirectories of the directory and all of their subdirectories, and so on.

Let’s create a simple script that prints the names of all subdirectories within a given directory:

| ​  | ​**import**​ { readdirSync, lstatSync } ​**from**​ ​*'fs'*​; |
| ​  | ​**import**​ { join } ​**from**​ ​*'path'*​; |
| ​  |  |
| ​  | ​**function**​ printSubdirectories(directoryName) { |
| ​  | ​**for**​ (​**const**​ fileName ​**of**​ readdirSync(directoryName)) { |
| ​  | ​**if**​ (lstatSync(fileName).isDirectory()) { |
| ​  | ​**const**​ pathName = join(directoryName, fileName); |
| ​  | console.log(pathName); |
| ​  | } |
| ​  | } |
| ​  | } |

We can call this function by passing in a directory name. If we want to call it on the current directory, we could write the following:

| ​  | printSubdirectories(​*'.'*​); |

In this script, we look through each file within the given directory. If the file is itself a subdirectory, we print the subdirectory name.

While this works well, it only prints the names of the subdirectories immediately within the current directory. It doesn’t print the names of the subdirectories within those subdirectories.

Let’s update our script so that it can search one level deeper:

| ​  | ​**import**​ { readdirSync, lstatSync } ​**from**​ ​*'fs'*​; |
| ​  | ​**import**​ { join } ​**from**​ ​*'path'*​; |
| ​  |  |
| ​  | ​**function**​ printSubdirectories(directoryName) { |
| ​  | ​**for**​ (​**const**​ fileName ​**of**​ readdirSync(directoryName)) { |
| ​  | ​**if**​ (lstatSync(fileName).isDirectory()) { |
| ​  | ​**const**​ pathName = join(directoryName, fileName); |
| ​  | console.log(pathName); |
| ​  |  |
| ​  | ​**for**​ (​**const**​ fileName2 ​**of**​ readdirSync(pathName)) { |
| ​  | ​**const**​ pathName2 = join(pathName, fileName2); |
| ​  | console.log(pathName2); |
| ​  | } |
| ​  | } |
| ​  | } |
| ​  | } |

Now, every time our script discovers a directory, it then conducts an identical loop through the subdirectories of that directory and prints the names of the subdirectories. But this script also has its limitations because it’s only searching two levels deep. What if we want to search three, four, or five levels deep? We would need five levels of nested loops.

And what if we want to search as deep as our subdirectories go? That would seem to be impossible, as we don’t even know how many levels there are.

And this is where recursion really shines. With recursion, we can write a script that goes arbitrarily deep—and with a lot less code!

| ​  | ​**import**​ { readdirSync, lstatSync } ​**from**​ ​*'fs'*​; |
| ​  | ​**import**​ { join } ​**from**​ ​*'path'*​; |
| ​  |  |
| ​  | ​**function**​ printSubdirectories(directoryName) { |
| ​  | ​**for**​ (​**const**​ fileName ​**of**​ readdirSync(directoryName)) { |
| ​  | ​**const**​ pathName = join(directoryName, fileName); |
| ​  | ​**if**​ (lstatSync(pathName).isDirectory()) { |
| ​  | console.log(pathName); |
| ​  | printSubdirectories(pathName); |
| ​  | } |
| ​  | } |
| ​  | } |

As this script encounters files that are themselves subdirectories, it calls the printSubdirectories method upon that very subdirectory. The script can therefore dig as deep as it needs to, leaving no subdirectory unturned.

To visualize how this algorithm acts on an example filesystem, examine the following diagram, which specifies the order in which the script traverses the subdirectories:

![images/recursively_recurse_with_recursion/filesystem.png](images/recursively_recurse_with_recursion/filesystem.png)

## Wrapping Up

As you’ve seen with the filesystem example, recursion is often a great choice for an algorithm in which the algorithm needs to dig an arbitrary number of levels deep into something.

You’ve now seen how recursion works and how incredibly useful it can be. You’ve also learned how to walk through and read recursive code. However, most people have a difficult time writing their own recursive functions when they’re first starting out. In the next chapter, we’ll explore techniques to help you learn to write recursively. Along the way, you’ll also discover other important use cases where recursion can be an incredible tool.

## Exercises

The following exercises provide you with the opportunity to practice with recursion. The solutions to these exercises are found in the section [​*Chapter 10*​](#f_0215.xhtml_recursively.recurse.with.recursion.solutions).

1.  The following function prints every other number from a low number to a high number. For example, if low is 0 and high is 10, it would print:

    | ​  | 0 |
    | ​  | 2 |
    | ​  | 4 |
    | ​  | 6 |
    | ​  | 8 |
    | ​  | 10 |

    Identify the base case in the function:

    | ​  | ​**function**​ printEveryOther(low, high) { |
    | ​  | ​**if**​ (low > high) { ​**return**​; } |
    | ​  |  |
    | ​  | console.log(low); |
    | ​  | printEveryOther(low + 2, high); |
    | ​  | } |

2.  My kid was playing with my computer and changed my factorial function so that it computes factorial based on (number - 2) instead of (number - 1). He also changed number <= 1 to number === 1. Predict what will happen when we run factorial(10) using ...

# Chapter 11
Learning to Write in Recursive

In the previous chapter, you learned what recursion is and how it works. I found on my own learning journey that even once I understood how recursion works, I still struggled to write my own recursive functions.

Through deliberate practice and taking note of various recursive patterns, I discovered some techniques that helped me to learn to “write in recursive” more easily, and I’d like to share them with you. Along the way, you’ll discover additional areas where recursion shines.

Note that we won’t be discussing the efficiency of recursion in this chapter. Recursion can actually have a terribly negative impact on the time complexity of an algorithm, but this is the subject of the next chapter. For now, we’re just going to focus on developing the recursive mindset.

## Recursive Category: Repeatedly Execute

Over the course of tackling various recursive problems, I began to find that there are various categories of problems. Once I learned an effective technique for a certain category, when I found another problem that belonged to the same category, I was able to apply the same technique to solve it.

The category that I found to be the easiest was one in which the goal of the algorithm was to repeatedly execute a task.

The NASA spacecraft countdown algorithm from the previous chapter is a great example. The code prints a number such as 10, and then 9, then 8, all the way down to 0\. While the number the function prints is different each time, we boil down the code’s essence to the fact that it is repeatedly ...

## Recursive Category: Calculations

In the previous section, we discussed the first category of recursive functions—those whose job it is to repeatedly execute a task. For the remainder of this chapter, I’ll elaborate on a second general category: performing a calculation based on a subproblem.

The goal of many functions is to perform a calculation. A function that returns the sum of two numbers, or a function that finds the greatest value within an array, are examples. These functions receive some sort of input and return the result of calculations involving that input.

In Chapter 10, [​*Recursively Recurse with Recursion*​](#f_0096.xhtml_chp.recursion), we found that one area in which recursion shines is where we need to act on a problem that has an arbitrary number of levels ...

## Top-Down Recursion: A New Way of Thinking

This brings us to the central point of this chapter: recursion shines when implementing a top-down approach because going top-down offers a new mental strategy for tackling a problem. That is, a recursive top-down approach allows one to think about a problem in a completely different way.

Specifically, when we go top-down, we get to mentally “kick the problem down the road.” We can free our mind from some of the nitty-gritty details we normally have to think about when going bottom-up.

To see what I mean, let’s take another look at the key line from our top-down factorial implementation:

| ​  | ​**return**​ number * factorial(number - 1); |

This line of code makes its calculation based on factorial(number - 1). When ...

## The Staircase Problem

You’ve now learned to use a new mental strategy for solving certain computational problems using top-down recursion. However, you may still be skeptical and ask, “Why do we need this new mental strategy anyway? I’ve been able to solve these problems with loops just fine until now.”

Indeed, you may not need a new mental strategy for simpler computations. But when it comes to more complex functions, you may find that the recursive mindset makes the writing of code much easier. It certainly does for me!

Here’s one of my favorite examples. A famous question—known as the staircase problem—goes like this:

Let’s say we have a staircase of N steps, and a person has the ability to climb one, two, or three steps at a time. How many ...

## Anagram Generation

To top off our conversation, let’s tackle our most complex recursive problem yet. We’re going to use everything we’ve got in our recursion toolbox to make this work.

We’re going to write a function that returns an array of all anagrams of a given string. An anagram is a reordering of all the characters within a string. For example, these are the anagrams of "abc":

| ​  | ["abc", |
| ​  | "acb", |
| ​  | "bac", |
| ​  | "bca", |
| ​  | "cab", |
| ​  | "cba"] |

Now, let’s say we were to collect all the anagrams of the string "abcd". Let’s apply our top-down mindset to this problem.

Presumably, we could say that the subproblem of "abcd" is "abc". The question then is this: if we had a working anagrams function that returned all the anagrams of "abc", how can we use them to ...

## Wrapping Up

Learning to write functions that use recursion certainly takes practice. But you’re now armed with tricks and techniques that will make the learning process easier for you.

We’re not done with our journey through recursion just yet, though. While recursion is a great tool for solving a variety of problems, it can actually slow your code down a lot if you’re not careful. In the next chapter, you’ll learn how to wield recursion while still keeping your code nice and speedy.

## Exercises

The following exercises provide you with the opportunity to practice with recursion. The solutions to these exercises are found in the section [​*Chapter 11*​](#f_0216.xhtml_learning.to.write.in.recursive.solutions).

1.  Use recursion to write a function that accepts an array of strings and returns the total number of characters across all the strings. For example, if the input array is ["ab", "c", "def", "ghij"], the output should be 10 since there are ten characters in total.

2.  Use recursion to write a function that accepts an array of numbers and returns a new array containing just the even numbers.

3.  A particular numerical sequence is known as triangular numbers. The pattern begins as 1, 3, 6, 10, 15, 21, and continues onward. To calculate the next number in the sequence, we add the previous number ...

# Chapter 12Dynamic Programming

In the previous chapter, you learned how to write recursively and how to use recursion to solve some rather complex problems.

While recursion can certainly solve some problems, it can also create new ones if not used properly. In fact, recursion is often the culprit behind some of the slowest categories of Big O, such as O(2^N).

The good news, though, is that many of these problems can be avoided. In this chapter, you’ll learn how to identify some of the most common speed traps found in recursive code and how to express such algorithms in terms of Big O. More important, you’ll learn the techniques to fix these problems.

Here’s some more good news: the techniques found in this chapter are pretty simple. Let’s take ...

## Unnecessary Recursive Calls

Here’s a recursive function that finds the greatest number from an array:

| ​  | ​**function**​ max(array) { |
| ​  | ​**if**​ (array.length === 0) { ​**return**​ ​**null**​; } |
| ​  |  |
| ​  | ​**if**​ (array.length === 1) { ​**return**​ array[0]; } |
| ​  |  |
| ​  | ​**if**​ (array[0] > max(array.slice(1))) { |
| ​  | ​**return**​ array[0]; |
| ​  | } ​**else**​ { |
| ​  | ​**return**​ max(array.slice(1)); |
| ​  | } |
| ​  | } |

The essence of each recursive call is the comparison of a single number (array[0]) to the maximum number from the remainder of the array. (To calculate the maximum number from the remainder of the array, we call the very max function we’re in, which is what makes the function recursive.)

We achieve the comparison with a conditional statement. The first half of the conditional statement is as follows:

## The Little Fix for Big O

Thankfully, there’s an easy way to eliminate all these extra recursive calls. We’ll call max only once within our code, and save the result to a variable:

| ​  | ​**function**​ max(array) { |
| ​  | ​**if**​ (array.length === 0) { ​**return**​ ​**null**​; } |
| ​  |  |
| ​  | ​**if**​ (array.length === 1) { ​**return**​ array[0]; } |
| ​  |  |
| ​  | ​*// Calculate the max of the remainder of the array*​ |
| ​  | ​*// and store it inside a variable:*​ |
| ​  | ​**const**​ maxOfRemainder = max(array.slice(1)); |
| ​  |  |
| ​  | ​*// Comparison of first number against this variable:*​ |
| ​  | ​**if**​ (array[0] > maxOfRemainder) { |
| ​  | ​**return**​ array[0]; |
| ​  | } ​**else**​ { |
| ​  | ​**return**​ maxOfRemainder; |
| ​  | } |
| ​  | } |

By implementing this simple modification, we end up calling max a mere four times. Try it out yourself by adding the console.log(’RECURSION’) ...

## The Efficiency of Recursion

In our second, improved version of the max function, the function recursively calls itself as many times as there are values in the array. We’d call this O(N).

Up until this point, the cases of O(N) we’ve seen involved loops, with a loop running N times. However, we can apply the same principles of Big O to recursion as well.

As you’ll recall, Big O answers the key question: if there are N data elements, how many steps will the algorithm take?

Since the improved max function runs N times for N values in the array, it has a time complexity of O(N). Even if the function itself contains multiple steps, such as five, its time complexity would be O(5N), which is reduced to O(N).

In the first version, though, the function called itself twice during each run (save for the base case). Let’s see how this plays out for different array sizes.

The following table shows how many times max gets called on arrays of various sizes:

| N Elements | Number of Calls |
| --- | --- |
| 1 | 1 |
| 2 | 3 |
| 3 | 7 |
| 4 | 15 |
| 5 | 31 |

Can you see the pattern? When we increase the data by one, we roughly double the number of steps the algorithm takes. As you learned by our discussion of the [​*Password Cracker*​](#f_0073.xhtml_sect.password-cracker), this is the pattern of O(2^N). We already know that this is an extremely slow algorithm.

The improved version of the max function, however, only calls max for as many elements as there are inside the array. This means that our second max function has an efficiency of O(N).

This is a powerful lesson: avoiding extra recursive calls is key to keeping recursion fast. What at first glance was a very small change to our code—the mere storing of a computation in a variable—ended up changing the speed of our function from O(2^N) to O(N).

## Overlapping Subproblems

The Fibonacci sequence is a mathematical sequence of numbers that goes like this until infinity:

0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55…

This sequence begins with the numbers 0 and 1, and each subsequent number is the sum of the previous two numbers of the sequence. For example, the number 55 was computed because it is the sum of the previous two numbers, which are 21 and 34.

The following JavaScript function returns the Nth number in the Fibonacci sequence. For example, if we pass the number 10 to the function, it will return 55, as 55 is the tenth number in the series. (The 0 is considered the 0th number in the series.)

| ​  | ​**function**​ fib(n) { |
| ​  | ​**if**​ (n === 0 &#124;&#124; n === 1) { |
| ​  | ​**return**​ n; |
| ​  | } |
| ​  |  |
| ​  | ​**return**​ fib(n - 2) + fib(n - 1); |
| ​  | } |

The key line in this function is the following:

| ​  | ​**return**​ fib(n - 2) + fib(n - 1); |

This line sums the previous two numbers in the Fibonacci series. It’s a beautiful recursive function.

However, alarm bells should be going off in your head right now because our function calls itself twice.

Let’s take the computation of the sixth Fibonacci number, for example. The function fib(6) makes a call to both fib(4) and fib(5), as shown in the following diagram:

![images/dynamic_programming/simple_fib_6.png](images/dynamic_programming/simple_fib_6.png)

As we’ve seen, a function calling itself twice can easily lead us down the road to O(2^N). Indeed, all the recursive calls made by fib(6) are shown in the [diagram](#f_0116.xhtml_fig.ch12.complete_fib_6).

![images/dynamic_programming/complete_fib_6.png](images/dynamic_programming/complete_fib_6.png)

You’ve got to admit, O(2^N) can look pretty scary.

While one simple change worked to optimize the first example in this chapter, optimizing our Fibonacci sequence isn’t as simple.

And that’s because there isn’t just one single piece of data we can save in a variable. We need to calculate both fib(n - 2) and fib(n - 1) (as each Fibonacci number is the sum of those two numbers), and storing the result of one won’t alone give us the result for the other.

This is a case of what computer scientists call overlapping subproblems. Let’s unpack that term.

When a problem is solved by solving smaller versions of the same problem, the smaller problem is called a subproblem. This concept isn’t new—we’ve been dealing with it frequently throughout our discussion of recursion. In the case of the Fibonacci sequence, we compute each number by first computing the smaller numbers in the sequence. The computations of these smaller numbers are the subproblems.

What makes these subproblems overlapping, though, is the fact that fib(n - 2) and fib(n - 1) end up calling many of the same functions as each other. Specifically, fib(n - 1) ends up making some of the very same calculations already made by fib(n - 2). For example, you can see in the previous diagram that fib(5) calls fib(3) even though fib(4) has itself already done so. Many other calls are duplicated too.

Well, it seems that we’re at a dead end. Our Fibonacci example requires us to make many overlapping function calls, and our algorithm oozes along at a pace of O(2^N). There’s just nothing we can do.

Or is there?

## Dynamic Programming Through Memoization

Luckily, we do have options, and that is through something called dynamic programming. Dynamic programming is the process of optimizing recursive problems that have overlapping subproblems.

(Don’t pay too much attention to the word dynamic. There’s some debate as to how the term came about, and there’s nothing obviously dynamic about the techniques I’m about to demonstrate.)

Optimizing an algorithm with dynamic programming is typically accomplished with one of two techniques.

The first technique is something called memoization. And no, that’s not a typo. Pronounced meh-moe-ih-ZAY-shun, memoization is a simple, but brilliant, technique for reducing recursive calls in cases of overlapping subproblems.

Essentially, memoization reduces recursive calls by remembering previously computed functions. (In this respect, memoization really is like its similar-sounding word memorization.)

In our Fibonacci example, the first time fib(3) is called, the function does its computation and returns the number 2\. However, before moving on, the function stores this result inside a hash table. The hash table will look something like this:

| ​  | {3: 2} |

This indicates that the result of fib(3) is the number 2.

Similarly, our code will memoize the results of all new computations it encounters. After encountering fib(4), fib(5), and fib(6), for example, our hash table will look like this:

| ​  | { |
| ​  | 3: 2, |
| ​  | 4: 3, |
| ​  | 5: 5, |
| ​  | 6: 8 |
| ​  | } |

Now that we have this hash table, we can use it to prevent future recursive calls. Here’s the way this works:

Without memoization, fib(4) would normally call fib(3) and fib(2), which in turn make their own recursive calls. Now that we have this hash table, we can approach things differently. Instead of fib(4) just blithely calling fib(3), for example, it first checks the hash table to see if the result of fib(3) has already been computed. Only if the 3 key is not in the hash table does the function proceed to call fib(3).

Memoization goes for the jugular of overlapping subproblems. The whole issue with overlapping subproblems is that we end up computing the same recursive calls over and over again. With memoization, though, each time we make a new calculation, we store it in the hash table for future use. This way, we only make a calculation if it hasn’t ever been made before.

Okay, this all sounds good, but there’s one glaring problem. How does each recursive function get access to this hash table?

The answer is this: we pass the hash table as a second parameter to the function.

Because the hash table is a specific object in memory, we’re able to pass it from one recursive call to the next, even though we’re modifying it as we go. This is true even as we unwind the call stack. Even though the hash table may have been empty when the original call was made, that same hash table can be full of data by the time the original call has finished executing.

### Implementing Memoization

To pass the hash table along, we modify our function to accept two arguments, with the hash table as the second. We call this hash table, memo, as in memoization:

| ​  | ​**function**​ fib(n, memo={}) { |

Note that we’re setting memo up as a default argument; this way we don’t have to pass in an empty hash table the first time we call it. As such, we can simply call the function using this:

| ​  | fib(6); |

Each time fib calls itself, it also passes along the hash table, which gets filled up along the way.

Here’s the rest of the function:

| ​  | ​**function**​ fib(n, memo={}) { |
| ​  | ​**if**​ (n === 0 &#124;&#124; n === 1) { |
| ​  | ​**return**​ n; |
| ​  | } |
| ​  |  |
| ​  | ​**if**​ (!memo[n]) { |
| ​  | memo[n] = fib(n - 2, memo) + fib(n - 1, memo); |
| ​  | } |
| ​  |  |
| ​  | ​**return**​ memo[n]; |
| ​  | } |

Let’s analyze this line by line.

Again, our function now accepts two parameters, namely n and the memo hash table:

| ​  | ​**function**​ fib(n, memo={}) { |

First off, the base cases of 0 and 1 both automatically return n and are unaffected by memoization.

Before making any recursive calls, our code first checks to see whether fib(n) has already been calculated for the given n:

| ​  | ​**if**​ (!memo[n]) { |

(If the calculation for n is already in the hash table, we simply return the result with return memo[n].)

Only if the calculation for n has not yet been made do we proceed with the calculation:

| ​  | memo[n] = fib(n - 2, memo) + fib(n - 1, memo); |

Here, we store the result of the calculation in the memo hash table so we never have to calculate it again.

Also note how we pass memo along as an argument to the fib function each time we call it. This is the key to sharing the memo hash table across all the calls to the fib function.

As you can see, the guts of the algorithm remain the same. We’re still using recursion to solve our problem, as the computation of fib is still essentially fib(n - 2) + fib(n - 1). However, if the number we’re computing is new, we store the result in a hash table, and if the number we’re computing was already computed once before, we simply grab the result from the hash table instead of computing it again.

When we map out the recursive calls in our memoized version, we get this:

![images/dynamic_programming/memoized_fib.png](images/dynamic_programming/memoized_fib.png)

In this diagram, each call that is surrounded by a box is one in which the result was retrieved from the hash table.

So what is the Big O of our function now? Let’s look at how many recursive calls we make for different types of N:

| N Elements | Number of Calls |
| --- | --- |
| 1 | 1 |
| 2 | 3 |
| 3 | 5 |
| 4 | 7 |
| 5 | 9 |
| 6 | 11 |

We can see that for N, we make (2N) - 1 calls. Since in Big O we drop the constants, this is an O(N) algorithm.

This is an incredible improvement over O(2^N). Go memoization!

## Dynamic Programming Through Going Bottom-Up

I mentioned earlier that dynamic programming can be achieved through one of two techniques. We looked at one technique, memoization, which is quite nifty.

The second technique, known as going bottom-up, is a lot less fancy and may not even seem like a technique at all. All going bottom-up means is to ditch recursion and use some other approach (like a loop) to solve the same problem.

The reason that going bottom-up is considered part of dynamic programming is because dynamic programming means taking a problem that could be solved recursively and ensuring that it doesn’t make duplicate calls for overlapping subproblems. Using iteration (that is, loops) instead of recursion is, technically, a way to achieve this.

Going bottom-up becomes more of a “technique” when the problem is more naturally solved with recursion. Generating Fibonacci numbers is one example where recursion is a neat, elegant solution. Having to solve the same problem with iteration may take more brainpower, as an iterative approach may be less intuitive. (Imagine solving the staircase problem from the previous chapter with a loop. Ugh.)

Let’s see how we might implement a bottom-up approach for our Fibonacci function.

### Bottom-Up Fibonacci

In the following bottom-up approach, we start with the first two Fibonacci numbers: 0 and 1\. We then use good ol’ iteration to build up the sequence:

| ​  | ​**function**​ fib(n) { |
| ​  | ​**if**​ (n === 0) { ​**return**​ 0; } |
| ​  |  |
| ​  | ​**let**​ a = 0; |
| ​  | ​**let**​ b = 1; |
| ​  |  |
| ​  | ​**for**​ (​**let**​ i = 1; i < n; i += 1) { |
| ​  | [a, b] = [b, a + b]; |
| ​  | } |
| ​  |  |
| ​  | ​**return**​ b; |
| ​  | } |

The very first thing we do is return 0 if the input n is 0\. Officially, fib(0) should return 0, so we easily dispense with that with a simple conditional statement.

Now, we get to the meat of the code. We initialize variables a and b as 0 and 1 respectively, as those are the first two numbers of the Fibonacci sequence.

We then start a loop so we can calculate each number of the sequence until we reach n:

| ​  | ​**for**​ (​**let**​ i = 1; i < n; i += 1) { |

To calculate the next number in the sequence, we need to add the two previous numbers together, namely a + b. We’ll update b to be this new number, since b always is supposed to point to the last number in the sequence. We also update a to what b was, so that a continues to point to the second-to-last number. We do this all with one convenient swap:

| ​  | [a, b] = [b, a + b]; |

Because our code is a simple loop from 1 to N, our code takes N steps. Like the memoization approach, it’s O(N).

### Memoization vs. Bottom-Up

You’ve now seen the two primary techniques of dynamic programming: memoization and going bottom-up. Is one technique better than the other?

Usually, it depends on the problem and why you’re using recursion in the first place. If recursion presents an elegant and intuitive solution to a given problem, you may want to stick with it and use memoization to deal with any overlapping subproblems. However, if the iterative approach is equally intuitive, you may want to go with that.

It’s important to point out that even with memoization, recursion does carry some extra overhead versus iteration. Specifically, with any recursion, the computer needs to keep track of all the calls in a call stack, which consumes memory. The memoization itself also requires the use of a hash table, which will take up additional space on your computer as well. (More on this in Chapter 19, [​*Dealing with Space Constraints*​](#f_0189.xhtml_chp.dealing_with_space_constraints).)

Generally speaking, going bottom-up is often the better choice, unless the recursive solution is more intuitive. Where recursion is more intuitive, you can keep the recursion and keep it fast by using memoization.

## Wrapping Up

Now that you’re able to write efficient recursive code, you’ve also unlocked a superpower. You’re about to encounter some really efficient—yet advanced—algorithms, and many of them rely on the principles of recursion.

## Exercises

The following exercises provide you with the opportunity to practice with dynamic programming. The solutions to these exercises are found in the section [​*Chapter 12*​](#f_0217.xhtml_dynamic.programming.solutions).

1.  The following function accepts an array of numbers and returns the sum, as long as a particular number doesn’t bring the sum above 100. If adding a particular number will make the sum higher than 100, that number is ignored. However, this function makes unnecessary recursive calls. Fix the code to eliminate the unnecessary recursion:

    | ​  | ​**function**​ addUntil100(array) { |
    | ​  | ​**if**​ (array.length === 0) { ​**return**​ 0; } |
    | ​  |  |
    | ​  | ​**if**​ (array[0] + addUntil100(array.slice(1)) > 100) { |
    | ​  | ​**return**​ addUntil100(array.slice(1)); |
    | ​  | } ​**else**​ { |
    | ​  | ​**return**​ array[0] + addUntil100(array.slice(1)); |
    | ​  | } |
    | ​  | } |

2.  The following function uses recursion to calculate the Nth number from a mathematical sequence known as the Golomb sequence. It’s terribly inefficient, though! Use memoization to optimize it. (You don’t have to understand how the Golomb sequence works to do this exercise.)

    | ​  | ​**function**​ golomb(n) { |
    | ​  | ​**if**​ (n === 1) { ​**return**​ 1; } |
    | ​  |  |
    | ​  | ​**return**​ 1 + golomb(n - golomb(golomb(n - 1))); |
    | ​  | } |

3.  Here is a solution to the unique paths problem from an exercise in the previous chapter. (Sorry, it’s a bit of a spoiler if you haven’t tried doing that exercise yet.) Use memoization to improve its efficiency:

    | ​  | ​**function**​ uniquePaths(rows, columns) { |
    | ​  | ​**if**​ (rows === 1 &#124;&#124; columns === 1) { |
    | ​  | ​**return**​ 1; |
    | ​  | } |
    | ​  |  |
    | ​  | ​**return**​ uniquePaths(rows - 1, columns) + uniquePaths(rows, columns - 1); |
    | ​  | } |

Copyright © 2024, The Pragmatic Bookshelf.

# Chapter 13Recursive Algorithms for Speed

We’ve seen that understanding recursion unlocks all sorts of new algorithms, such as traversing a filesystem or producing anagrams. In this chapter, you’re going to learn that recursion is also the key to algorithms that can make our code run much, much faster.

In previous chapters, we’ve encountered a number of sorting algorithms, including Bubble Sort, Selection Sort, and Insertion Sort. In real life, however, none of these methods are actually used to sort arrays. Most computer languages have built-in sorting functions for arrays that save us the time and effort of implementing our own. And in many of these languages, the sorting algorithm that is employed under the hood is Quicksort.

The reason we’re ...

## Partitioning

To partition an array is to take a random value from the array—which is then called the pivot—and make sure every number that is less than the pivot ends up to the left of the pivot and every number greater than the pivot ends up to the right of the pivot. We accomplish partitioning through a simple algorithm that will be described in the following example.

Let’s say we have the following array:

![images/divide_and_conquer_code_in_turbo_mode/quicksort_1.png](images/divide_and_conquer_code_in_turbo_mode/quicksort_1.png)

For consistency’s sake, we’ll always select the rightmost value to be our pivot (although we can technically choose other values). In this case, the number 3 is our pivot. We indicate this by circling it:

![images/divide_and_conquer_code_in_turbo_mode/quicksort_2.png](images/divide_and_conquer_code_in_turbo_mode/quicksort_2.png)

We then assign pointers—one to the leftmost value of the array, and one to the rightmost value of the array, excluding the pivot itself:

![images/divide_and_conquer_code_in_turbo_mode/quicksort_3.png](images/divide_and_conquer_code_in_turbo_mode/quicksort_3.png)

We’re now ready to begin the actual partition, which follows these steps. Don’t worry—the steps will become clearer shortly, when we walk through our example.

1.  The left pointer continuously moves one cell to the right until it reaches a value that is greater than or equal to the pivot and then stops.

2.  Then the right pointer continuously moves one cell to the left until it reaches a value that is less than or equal to the pivot and then stops. The right pointer will also stop if it reaches the beginning of the array.

3.  Once the right pointer has stopped, we reach a crossroads. If the left pointer has reached (or gone beyond) the right pointer, we move on to Step 4\. Otherwise, we swap the values that the left and right pointers are pointing to, and then we go back to repeat Steps 1, 2, and 3 again.

4.  Finally, we swap the pivot with the value that the left pointer is currently pointing to.

When we’re done with a partition, we are now assured that all values to the left of the pivot are less than the pivot, and all values to the right of the pivot are greater than it. And that means the pivot itself is now in its correct place within the array, although the other values are not yet necessarily completely sorted.

Let’s apply this to our example:

Step 1: Compare the left pointer (now pointing to 0) to our pivot (the value 3):

![images/divide_and_conquer_code_in_turbo_mode/quicksort_3.png](images/divide_and_conquer_code_in_turbo_mode/quicksort_3.png)

Since 0 is less than the pivot, the left pointer moves on in the next step.

Step 2: The left pointer moves on:

![images/divide_and_conquer_code_in_turbo_mode/quicksort_4.png](images/divide_and_conquer_code_in_turbo_mode/quicksort_4.png)

We compare the left pointer (the 5) to our pivot. Is the 5 lower than the pivot? It’s not, so the left pointer stops, and we activate the right pointer in our next step.

Step 3: Compare the right pointer (6) to our pivot. Is the value greater than the pivot? It is, so our pointer will move on in the next step.

Step 4: The right pointer moves on:

![images/divide_and_conquer_code_in_turbo_mode/quicksort_5.png](images/divide_and_conquer_code_in_turbo_mode/quicksort_5.png)

We compare the right pointer (1) to our pivot. Is the value greater than the pivot? It’s not, so our right pointer stops.

Step 5: Since both pointers have stopped, we swap the values of the two pointers:

![images/divide_and_conquer_code_in_turbo_mode/quicksort_6.png](images/divide_and_conquer_code_in_turbo_mode/quicksort_6.png)![images/divide_and_conquer_code_in_turbo_mode/quicksort_7.png](images/divide_and_conquer_code_in_turbo_mode/quicksort_7.png)

We then activate our left pointer again in the next step.

Step 6: The left pointer moves on:

![images/divide_and_conquer_code_in_turbo_mode/quicksort_8.png](images/divide_and_conquer_code_in_turbo_mode/quicksort_8.png)

We compare the left pointer (2) to our pivot. Is the value less than the pivot? It is, so the left pointer moves on.

Step 7: The left pointer moves on to the next cell. Note that at this point, both the left and right pointers are pointing to the same value:

![images/divide_and_conquer_code_in_turbo_mode/quicksort_9.png](images/divide_and_conquer_code_in_turbo_mode/quicksort_9.png)

We compare the left pointer to our pivot. Because our left pointer is pointing to a value that is greater than our pivot, it stops. At this point, since our left pointer has reached our right pointer, we’re done with moving pointers.

Step 8: For our final step of the partition, we swap the value that the left pointer is pointing to with the pivot:

![images/divide_and_conquer_code_in_turbo_mode/quicksort_10.png](images/divide_and_conquer_code_in_turbo_mode/quicksort_10.png)![images/divide_and_conquer_code_in_turbo_mode/quicksort_11.png](images/divide_and_conquer_code_in_turbo_mode/quicksort_11.png)

Although our array isn’t completely sorted, we’ve successfully completed a partition; that is, since our pivot was the number 3, all numbers that are less than 3 are to its left, while all numbers greater than 3 are to its right. This also means, by definition, that the 3 is now in its correct place within the array.

### Code Implementation: Partitioning

Following is an implementation of a SortableArray class in JavaScript that includes a partition method that partitions the array as we’ve described:

| ​  | ​**class**​ SortableArray { |
| ​  | ​**constructor**​(array) { |
| ​  | ​**this**​.array = array; |
| ​  | } |
| ​  |  |
| ​  | partition(leftPointer, rightPointer) { |
| ​  | ​**const**​ pivotIndex = rightPointer; |
| ​  | ​**const**​ pivot = ​**this**​.array[pivotIndex]; |
| ​  |  |
| ​  | rightPointer -= 1; |
| ​  |  |
| ​  | ​**while**​ (​**true**​) { |
| ​  | ​**while**​ (​**this**​.array[leftPointer] < pivot) { |
| ​  | leftPointer += 1; |
| ​  | } |
| ​  |  |
| ​  | ​**while**​ (​**this**​.array[rightPointer] > pivot) { |
| ​  | rightPointer -= 1; |
| ​  | } |
| ​  |  |
| ​  | ​**if**​ (leftPointer >= rightPointer) { |
| ​  | ​**break**​; |
| ​  | } ​**else**​ { |
| ​  | [​**this**​.array[leftPointer], ​**this**​.array[rightPointer]] = |
| ​  | [​**this**​.array[rightPointer], ​**this**​.array[leftPointer]]; |
| ​  | leftPointer += 1; |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | [​**this**​.array[leftPointer], ​**this**​.array[pivotIndex]] = |
| ​  | [​**this**​.array[pivotIndex], ​**this**​.array[leftPointer]]; |
| ​  |  |
| ​  | ​**return**​ leftPointer; |
| ​  | } |

| ​  | } |

Let’s break this code down a bit.

The partition method accepts the starting points of the left and right pointers as parameters:

| ​  | partition(leftPointer, rightPointer) { |

When this method is first called on an array, these pointers will point to the left and right ends of the array, respectively. However, we’ll see that Quicksort will call this method on subsections of the array as well. Because of this, we can’t always assume the left and right pointers are always the two extremities of the array, so they need to become method arguments. This point will be clearer when I explain the complete Quicksort algorithm.

Next, we select our pivot, which is always the rightmost element in the range we’re dealing with:

| ​  | ​**const**​ pivotIndex = rightPointer; |
| ​  | ​**const**​ pivot = ​**this**​.array[pivotIndex]; |

Once our pivot has been identified, we move the rightPointer to the item immediately left of the pivot:

| ​  | rightPointer -= 1; |

We then begin a loop (while (true)) that will seem to run indefinitely. However, later within the loop is a break statement that will terminate the loop as soon as the leftPointer and rightPointer cross paths. Within this loop, we use another loop to keep moving the leftPointer to the right until it reaches an item that is greater than or equal to the pivot:

| ​  | ​**while**​ (​**this**​.array[leftPointer] < pivot) { |
| ​  | leftPointer += 1; |
| ​  | } |

Similarly, we move the rightPointer to the left until it hits an item that is less than or equal to the pivot:

| ​  | ​**while**​ (​**this**​.array[rightPointer] > pivot) { |
| ​  | rightPointer -= 1; |
| ​  | } |

Once the leftPointer and rightPointer have stopped moving, we check whether the two pointers have met:

| ​  | ​**if**​ (leftPointer >= rightPointer) { |
| ​  | ​**break**​; |
| ​  | } |

If they have, we exit the loop and get ready to swap out the pivot, which we’ll get to momentarily. However, if the two pointers have stopped but not yet met each other, we swap the values at the two pointers:

| ​  | [​**this**​.array[leftPointer], ​**this**​.array[rightPointer]] = |
| ​  | [​**this**​.array[rightPointer], ​**this**​.array[leftPointer]]; |

We then move the leftPointer to get ready for the next round of left- and right-pointer movements:

| ​  | leftPointer += 1; |

Finally, once the two pointers have met, we swap the pivot with the value at the leftPointer:

| ​  | [​**this**​.array[leftPointer], ​**this**​.array[pivotIndex]] = |
| ​  | [​**this**​.array[pivotIndex], ​**this**​.array[leftPointer]]; |

The method concludes by returning the leftPointer, as this will be needed by the Quicksort algorithm (which I’ll explain shortly).

## Quicksort

The Quicksort algorithm is a combination of partitions and recursion. It works as follows:

1.  Partition the array. The pivot is now in its proper place.

2.  Treat the subarrays to the left and right of the pivot as their own arrays, and recursively repeat Steps 1 and 2\. That means we’ll partition each subarray and end up with even smaller sub-subarrays to the left and right of each subarray’s pivot. We then partition those sub-subarrays, and so on and so forth.

3.  When we have a subarray that has zero or one elements, that’s our base case and we do nothing.

Let’s return to our example. We began with the array of [0, 5, 2, 1, 6, 3] and ran a single partition on the entire array. Since Quicksort begins with such a partition, that means we’re already ...

## The Efficiency of Quicksort

To figure out the efficiency of Quicksort, let’s first determine the efficiency of a single partition.

When we break down the steps of a partition, we’ll note that a partition involves two primary types of steps:

*   Comparisons: We compare each of the values at hand to the pivot.
*   Swaps: When appropriate, we swap the values being pointed to by the left and right pointers.

Each partition has at least N comparisons—that is, we compare each element of the array with the pivot. This is true because a partition always has the left and right pointers move through each cell until the left and right pointers reach each other.

The number of swaps, however, will depend upon how the data is sorted. A single partition can have, at most, N / 2 swaps, as even if we’d swap values at every opportunity, each swap takes care of two values. As you can see in the following diagram, we partition six elements in just three swaps:

![images/divide_and_conquer_code_in_turbo_mode/three_swaps.png](images/divide_and_conquer_code_in_turbo_mode/three_swaps.png)

Now, in most cases, we’re not making a swap every step of the way. For randomly sorted data, we generally swap about half of the values. On average, then, we’re making about N / 4 swaps.

So on average, we make about N comparisons and N / 4 swaps. We can say, then, that there are about 1.25N steps for N data elements. In Big O notation, we ignore constants, so we’d say that a partition runs in O(N) time.

Now, that’s the efficiency of a single partition. But Quicksort involves many partitions, so we need to conduct further analysis to determine the efficiency of Quicksort.

### Quicksort from a Bird’s-Eye View

To visualize this more easily, see the [diagram](#f_0124.xhtml_fig.ch13.partition_numbers), depicting a typical Quicksort on an array of eight elements from a bird’s-eye view. In particular, the diagram shows how many elements each partition acts upon. We have left out the actual numbers from the array since the exact values don’t matter. Note that in the diagram, the active subarray is the group of cells that’s not grayed out.

![images/divide_and_conquer_code_in_turbo_mode/partition_numbers.png](images/divide_and_conquer_code_in_turbo_mode/partition_numbers.png)

We can see that we have eight partitions, but each partition takes place on subarrays of various sizes. We perform a partition on the original array of eight elements but also perform partitions on subarrays of sizes 4, 3, and 2, and another four partitions on arrays of size 1.

Since Quicksort is essentially comprised of this series of partitions, and each partition takes about N steps for N elements of each subarray, if we add the sizes of all the subarrays together, we’ll get the total number of steps Quicksort takes:

| ​  | 8 elements |
| ​  |  |
| ​  | 3 elements |
| ​  |  |
| ​  | 1 element |
| ​  |  |
| ​  | 1 element |
| ​  |  |
| ​  | 4 elements |
| ​  |  |
| ​  | 2 elements |
| ​  |  |
| ​  | 1 element |
| ​  |  |
| ​  | + 1 element |
| ​  | __________ |
| ​  |  |
| ​  | Total = About 21 steps |

We see that where the original array has 8 elements, Quicksort takes about 21 steps. This assumes a best- or average-case scenario, where the pivot ends up roughly in the middle of the subarray after each partition.

For an array of 16 elements, Quicksort takes about 64 steps, and for an array of 32 elements, Quicksort takes about 160 steps. Take a look at this table:

| N | Quicksort Steps (approx.) |
| --- | --- |
| 4 | 8 |
| 8 | 24 |
| 16 | 64 |
| 32 | 160 |

(While in our example earlier, the number of Quicksort steps for an array of size 8 was 21, I put 24 in this table. The exact number can vary from case to case, and 24 is also a reasonable approximation. I specifically made it 24 to make the following explanation a little clearer.)

### The Big O of Quicksort

How do we categorize Quicksort in terms of Big O notation?

If we look at the pattern shown earlier, we’ll note that the number of Quicksort steps for N elements in the array is about N multiplied by log N, as shown in the following table:

| N | log N | N * log N | Quicksort Steps (approx.) |
| --- | --- | --- | --- |
| 4 | 2 | 8 | 8 |
| 8 | 3 | 24 | 24 |
| 16 | 4 | 64 | 64 |
| 32 | 5 | 160 | 160 |

In fact, this is exactly how to express the efficiency of Quicksort. It’s an algorithm of O(N log N). We’ve discovered a new category of Big O!

The [graph](#f_0124.xhtml_fig.ch13.big_o_graph) shows how O(N log N) looks beside other categories of Big O.

![images/divide_and_conquer_code_in_turbo_mode/big_o_graph.png](images/divide_and_conquer_code_in_turbo_mode/big_o_graph.png)

Now, it’s not a coincidence that the number of steps in Quicksort just happens to align with N * log N. If we think about Quicksort more broadly, we can see why it’s this way.

Each time we partition the array, we end up breaking it down into two subarrays. Assuming the pivot ends up somewhere in the middle of the array—which is what happens in the average case—these two subarrays are of roughly equal sizes.

How many times can we break an array into halves until we’ve broken it completely down to the point where each subarray is of size 1? For an array of size N, this will take us log N times. Take a look at the following diagram:

![images/divide_and_conquer_code_in_turbo_mode/halvings.png](images/divide_and_conquer_code_in_turbo_mode/halvings.png)

As you can see, for an array of size 8, it takes us three halvings until we’ve reduced the array into eight individual elements. This is log N, and fits with our definition of log N as being the number of times it takes to halve something until we reach 1.

So this is why Quicksort takes N * log N steps. We have log N halvings, and for each halving, we perform a partition on all the subarrays whose elements add up to N. (They add up to N because all the subarrays are simply pieces of the original array of N elements.)

This is illustrated in the previous diagram. At the top of the diagram, for example, we partition the original array of eight elements, creating two subarrays of size 4\. We then partition both subarrays of size 4, which means that we’re again partitioning eight elements.

Bear in mind that O(N * log N) is just an approximation. In reality, we first perform an extra O(N) partition on the original array as well. Additionally, an array doesn’t cleanly break into two even halves, since the pivot is not part of the halving.

Here’s what a more realistic example looks like, where we ignore the pivot after each partition:

![images/divide_and_conquer_code_in_turbo_mode/realistic.png](images/divide_and_conquer_code_in_turbo_mode/realistic.png)

## Quicksort in the Worst-Case Scenario

For many other algorithms we’ve encountered, the best case was one where the array was already sorted. When it comes to Quicksort, however, the best-case scenario is one in which the pivot always ends up smack in the middle of the subarray after the partition. Interestingly, this generally occurs when the values in the array are mixed up pretty well.

The worst-case scenario for Quicksort is one in which the pivot always ends up on one side of the subarray instead of in the middle. This can happen where the array is in perfect ascending or descending order. The visualization for this process is shown here:

![images/divide_and_conquer_code_in_turbo_mode/visualization.png](images/divide_and_conquer_code_in_turbo_mode/visualization.png)

In this diagram you can see that the pivot always ends up on the left end of each subarray.

While in this case each partition still involves only one swap, we lose out because of the increased number of comparisons. In the first example, when the pivot always ended up toward the middle, each partition after the first one was conducted on relatively small subarrays (the largest subarray had a size of 4). In this example, however, the first five partitions take place on subarrays of size 4 or greater. And each of these partitions has as many comparisons as there are elements in the subarray.

So in this worst-case scenario, we have partitions of 8 + 7 + 6 + 5 + 4 + 3 + 2 + 1 elements, which yields a total of 36 comparisons.

To put this a little more formulaically, we’d say that for N elements, there are N + (N - 1) + (N - 2) + (N - 3) … + 1 steps. We saw in our discussion of [​*Get All the Products*​](#f_0072.xhtml_sect.get-all-the-products), that this computes to N² / 2 steps, which for the purposes of Big O is O(N²).

So in a worst-case scenario, Quicksort has an efficiency of O(N²).

### Quicksort vs. Insertion Sort

Now that we’ve got Quicksort down, let’s compare it with one of the simpler sorting algorithms, such as Insertion Sort:

|  | Best Case | Average Case | Worst Case |
| --- | --- | --- | --- |
| Insertion Sort | O(N) | O(N²) | O(N²) |
| Quicksort | O(N log N) | O(N log N) | O(N²) |

We can see they have identical worst-case scenarios and that Insertion Sort is faster than Quicksort in a best-case scenario. However, the reason Quicksort is superior to Insertion Sort is because of the average scenario—which, again, is what happens most of the time. For average cases, Insertion Sort takes a whopping O(N²), while Quicksort is much faster at O(N log N).

Because of Quicksort’s superiority in average circumstances, many programming languages use Quicksort under the hood of their built-in sorting functions. So it’s unlikely you’ll be implementing Quicksort yourself. However, a very similar algorithm can come in handy for practical cases—and it’s called Quickselect.

## Quickselect

Let’s say you have an array in random order, and you don’t need to sort it, but you do want to know the tenth-lowest value in the array, or the fifth-highest. This can be useful if we have a lot of test grades and want to know what the 25th percentile is, or if we want to find the median grade.

One way to solve this would be to sort the entire array and then jump to the appropriate index.

However, even were we to use a fast sorting algorithm like Quicksort, this algorithm would take at least O(N log N) for average cases. And while that isn’t bad, we can do even better with a brilliant little algorithm known as Quickselect. Like Quicksort, Quickselect relies on partitioning and can be thought of as a hybrid of Quicksort and binary search.

As you’ve seen earlier in this chapter, after a partition, the pivot value ends up in the appropriate spot in the array. Quickselect takes advantage of this in the following way:

Let’s say we have an array of eight values, and we want to find the second-to-lowest value within the array.

First, we partition the entire array:

![images/divide_and_conquer_code_in_turbo_mode/partition_entire_array.png](images/divide_and_conquer_code_in_turbo_mode/partition_entire_array.png)

After the partition, the pivot will hopefully end up somewhere toward the middle of the array:

![images/divide_and_conquer_code_in_turbo_mode/pivot_in_middle.png](images/divide_and_conquer_code_in_turbo_mode/pivot_in_middle.png)

This pivot is now in its correct spot, and since it’s in the fifth cell, we now know which value is the fifth-lowest value within the array.

Now, we’re looking for the second-lowest value, not the fifth-lowest. But we do know that the second-lowest value is somewhere to the left of the pivot. We can now ignore everything to the right of the pivot and focus on the left subarray. It’s in this respect that Quickselect is similar to binary search: we keep dividing the array in half and focus on the half in which we know the value we’re seeking will be found.

Next, we partition the subarray to the left of the pivot:

![images/divide_and_conquer_code_in_turbo_mode/subarray_left_of_pivot.png](images/divide_and_conquer_code_in_turbo_mode/subarray_left_of_pivot.png)

Let’s say the new pivot of this subarray ends up the third cell:

![images/divide_and_conquer_code_in_turbo_mode/pivot_third_cell.png](images/divide_and_conquer_code_in_turbo_mode/pivot_third_cell.png)

We now know that the value in the third cell is in its correct spot, meaning it’s the third-to-lowest value in the array. By definition, then, the second-to-lowest value will be somewhere to its left. We can now partition the subarray to the left of the third cell:

![images/divide_and_conquer_code_in_turbo_mode/partition_left_of_third_cell.png](images/divide_and_conquer_code_in_turbo_mode/partition_left_of_third_cell.png)

After this next partition, the lowest and second-lowest values will end up in their correct spots within the array:

![images/divide_and_conquer_code_in_turbo_mode/second_lowest_value.png](images/divide_and_conquer_code_in_turbo_mode/second_lowest_value.png)

We can then grab the value from the second cell and know with confidence that it’s the second-lowest value in the entire array. One of the beautiful things about Quickselect is that we can find the correct value without having to sort the entire array.

With Quicksort, each time we halved the array, we needed to re-partition every single element again (in their subarray form), giving us O(N log N). With Quickselect, on the other hand, each time we cut the array in half, we only had to partition the one half we cared about—the half in which we know our value is to be found.

### The Efficiency of Quickselect

When analyzing the efficiency of Quickselect, we’ll see that it’s O(N) for average scenarios. Why is this?

In our earlier example of an array of eight elements, we executed three partitions: one on an array of eight elements, one on a subarray of four elements, and one on a subarray of two elements.

Recall that each partition takes about N steps for the subarray it’s run upon. The total steps, then, for the three partitions is 8 + 4 + 2 = 14 steps. So an array of eight elements yields roughly 14 steps.

For an array of 64 elements, we run about 64 + 32 + 16 + 8 + 4 + 2 = 126 steps. For 128 elements, we would need about 254 steps. And for 256 elements, we would end up with 510 steps.

We can see that we need about 2N steps for N elements in the array.

(Another way to formulate this is to say that for N elements, we would need N + (N/2) + (N/4) + (N/8) + … 2 steps. This always turns out to be roughly 2N steps.)

Since Big O ignores constants, we drop the 2 from the 2N and say that Quickselect has an efficiency of O(N).

### Code Implementation: Quickselect

Following is an implementation of a quickselect method that can be dropped into the SortableArray class described earlier. You’ll note that it’s very similar to the quicksort method:

| ​  | quickselect(kthLowestValue, leftIndex, rightIndex) { |
| ​  | ​**if**​ (rightIndex - leftIndex <= 0) { |
| ​  | ​**return**​ ​**this**​.array[leftIndex]; |
| ​  | } |
| ​  |  |
| ​  | ​**const**​ pivotIndex = ​**this**​.partition(leftIndex, rightIndex); |
| ​  |  |
| ​  | ​**if**​ (kthLowestValue < pivotIndex) { |
| ​  | ​**return**​ ​**this**​.quickselect(kthLowestValue, leftIndex, pivotIndex - 1); |
| ​  | } ​**else**​ ​**if**​ (kthLowestValue > pivotIndex) { |
| ​  | ​**return**​ ​**this**​.quickselect(kthLowestValue, pivotIndex + 1, rightIndex); |
| ​  | } ​**else**​ { |
| ​  | ​**return**​ ​**this**​.array[pivotIndex]; |
| ​  | } |
| ​  | } |

The variable kthLowestValue allows us to choose which value we’re searching for. We can search for the second-to-lowest value, the fifth-to-lowest value, or any other value we’d like.

If you want to find the second-to-lowest value of an unsorted array, you’d run the following code:

| ​  | ​**const**​ array = [0, 50, 20, 10, 60, 30]; |
| ​  | ​**const**​ sortableArray = ​**new**​ SortableArray(array); |
| ​  | console.log(sortableArray.quickselect(1, 0, array.length - 1)); |

The first argument of the quickselect method accepts the position you’re looking for, starting at index 0. We’ve put in a 1 to represent the second-to-lowest value. The second and third values are the left and right indexes of the array, respectively.

## Sorting as a Key to Other Algorithms

As of this writing, the fastest sorting algorithms we know of have speeds of O(N log N). While Quicksort is one of the most popular among them, there are many others as well. Mergesort is another well-known O(N log N) sorting algorithm and will be covered in Volume 2 of this book.

The fact that the fastest sorting algorithms are O(N log N) is important, as this has implications for other algorithms as well. This is because there are algorithms that use sorting as a component of a larger process.

For example, if you’ll recall from Chapter 4, [​*Speeding Up Your Code with Big O*​](#f_0040.xhtml_chp.speeding_up), we dealt with the problem of checking whether there are duplicate values within an array.

The first solution we looked at involved nested loops and had an efficiency of O(N²). While we found a solution that took O(N), I parenthetically hinted at a disadvantage with that approach having to do with extra memory consumption. (I’ll eventually discuss this at length in Chapter 19, [​*Dealing with Space Constraints*​](#f_0189.xhtml_chp.dealing_with_space_constraints).) So let’s assume that the O(N) approach is out. Are there any other ways we can improve upon the quadratic O(N²) solution? Hint: the solution has something to do with sorting!

We can build a beautiful algorithm if we presort the array.

Let’s say the original array was [5, 9, 3, 2, 4, 5, 6]. This array has two instances of 5, so we do have a case of duplicates.

Now, if we first sorted this array, it would become [2, 3, 4, 5, 5, 6, 9].

Next, we can use a single loop to iterate over each number. As we inspect each number, we’d check whether it’s identical to the next number. If it is, we’ve found a duplicate. If we get to the end of the loop without finding a duplicate, then we know that we have no duplicates.

The trick here is that by presorting the numbers, we end up bunching duplicate numbers together.

In our example, we’d start by looking at the first number, which is the 2. We’d check whether it’s identical to the next number. The next number is 3, so they’re not duplicates.

We’d then check the 3 against the following number, which happens to be a 4, allowing us to move on. We’d check the 4 against the 5, and we’d move on again.

At this point, we’d inspect the first 5 and check it against the following number, which is the second 5. Aha! We found a pair of duplicate numbers, and we can return true.

Here’s a JavaScript implementation of this:

| ​  | ​**function**​ hasDuplicateValue(array) { |
| ​  | array.sort((a, b) => a - b); |
| ​  |  |
| ​  | ​**for**​ (​**let**​ index = 0; index < array.length - 1; index += 1) { |
| ​  | ​**if**​ (array[index] === array[index + 1]) { |
| ​  | ​**return**​ ​**true**​; |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | ​**return**​ ​**false**​; |
| ​  | } |

Here we use JavaScript’s built-in sort function. The argument (a, b) => a - b is necessary to ensure that JavaScript sorts integers correctly, and doesn’t sort them as if they were strings.

Now, this is an algorithm that used sorting as one of its components. What’s the Big O of this algorithm?

We start out by sorting the array. We can assume that JavaScript’s sort function uses something like Quicksort under the hood and has an efficiency of O(N log N). Next, we spend up to N steps iterating through the array. Our algorithm, then, takes (N log N) + N steps.

You learned that when we have multiple orders added together, Big O notation keeps only the highest order of N because the lower orders are trivial beside the higher orders. Here as well, N is trivial beside N log N, so we reduce the expression to O(N log N).

So, that’s it! We’ve used sorting to develop an algorithm that is O(N log N), which is a significant improvement over the original O(N²) algorithm.

Plenty of algorithms employ sorting as part of a larger process. We now know that any time we do so, we have an algorithm that is at least O(N log N). Of course, the algorithm may be slower than this if it has other things going on, but we know that O(N log N) will always be the baseline.

## Wrapping Up

The Quicksort and Quickselect algorithms are recursive algorithms that present beautiful and efficient solutions to thorny problems. They’re great examples of how a non-obvious but well-thought-out algorithm can boost performance.

Now that we’ve seen some more advanced algorithms, we’re now going to head in a new direction and explore a trove of additional data structures. Some of these data structures have operations that involve recursion, so we’ll be fully prepared to tackle those now. Besides their being really interesting, we’ll see that each data structure has a special power that can bring significant advantages to a variety of applications.

## Exercises

The following exercises provide you with the opportunity to practice with fast sorting. The solutions to these exercises are found in the section [​*Chapter 13*​](#f_0218.xhtml_divide.and.conquer.in.turbo.mode.solutions).

1.  Given an array of positive numbers, write a function that returns the greatest product of any three numbers. The approach of using three nested loops would clock in at O(N³), which is very slow. Use sorting to implement the function in a way that it computes at O(N log N) speed. (Some other implementations are even faster, but we’re focusing on using sorting as a technique to make code faster.)

2.  The following function finds the missing number from an array of integers; that is, the array is expected to have all integers from 0 up to the array’s length, but one is missing. As examples, the array [5, 2, 4, 1, 0] is missing the number 3, and the array [9, 3, 2, 5, 6, 7, 1, 0, 4] is missing the number 8.

    Here’s an implementation that is O(N²) (the clause if (!array.includes(number)) is itself already O(N), since the computer needs to search the entire array to find number):

    | ​  | ​**function**​ findMissingNumber(array) { |
    | ​  | ​**for**​ (​**let**​ number = 0; number <= array.length; number += 1) { |
    | ​  | ​**if**​ (!array.includes(number)) { |
    | ​  | ​**return**​ number; |
    | ​  | } |
    | ​  | } |
    | ​  |  |
    | ​  | ​**return**​ ​**null**​; |
    | ​  | } |

    Use sorting to write a new implementation of this function that only takes O(N log N). (Some other implementations are even faster, but we’re focusing on using sorting as a technique to make code faster.)

3.  Write three different implementations of a function that finds the greatest number within an array. Write one function that is O(N²), one that is O(N log N), and one that is O(N).

Copyright © 2024, The Pragmatic Bookshelf.

# Chapter 14
Node-Based Data Structures

For the next several chapters, we’re going to explore a variety of data structures that all build upon a single concept—the node. As you’ll see shortly, nodes are pieces of data that may be dispersed throughout the computer’s memory. Node-based data structures offer new ways to organize and access data that provide a number of major performance advantages.

In this chapter we’ll explore the linked list, which is the simplest node-based data structure and the foundation for future chapters. You’ll discover that linked lists seem almost identical to arrays but come with their own set of trade-offs in efficiency that can give us a performance boost for certain situations.

## Linked Lists

Like an array, a linked list is a data structure that represents a list of items. While on the surface arrays and linked lists look and act quite similarly, under the hood there are big differences.

As mentioned in Chapter 1, [​*Why Data Structures Matter*​](#f_0013.xhtml_chp.understanding_data_structures), memory inside a computer can be visualized as a giant set of cells in which bits of data are stored. You learned that when creating an array, your code finds a contiguous group of empty cells in memory and designates them to store data for your application, as [shown](#f_0131.xhtml_fig.ch14.array_3).

![images/understanding_arrays/array_3.png](images/understanding_arrays/array_3.png)

You also saw that the computer has the ability to access any memory address in one step and can use that power to also immediately access any index within the array. If you wrote code that said, “Look up the value at index 4,” your computer could locate that cell in a single step. Again, this is because your program knows which memory address the array starts at—say, memory address 1000—and therefore knows that if it wants to look up index 4, it should simply jump to memory address 1004.

Linked lists, on the other hand, work differently. Instead of being a contiguous block of memory, the data from linked lists can be scattered across different cells throughout the computer’s memory.

Connected data that are dispersed throughout memory are known as nodes. In a linked list, each node represents one item in the list. The big question, then, is this: if the nodes are not next to each other in memory, how does the computer know which nodes are part of the same linked list?

This is the key to the linked list: each node also comes with a little extra information—namely, the memory address of the next node in the list.

This extra piece of data—this pointer to the next node’s memory address—is known as a link. Here’s a visual depiction of a linked list:

![images/pitting_linked_lists_against_arrays/linked_list_1.png](images/pitting_linked_lists_against_arrays/linked_list_1.png)

In this example, we have a linked list that contains four pieces of data: "a", "b", "c", and "d". However, it uses eight cells of memory to store this data, because each node consists of two memory cells. The first cell holds the actual data, while the second cell serves as a link that indicates where in memory the next node begins. The final node’s link contains null since the linked list ends there.

A linked list’s first node is also referred to as its head, and its last node its tail. We may use the terms head and first node interchangeably.

If the computer knows at which memory address the linked list begins, it has all it needs to begin working with the list! Since each node contains a link to the next node, all the computer needs to do is follow each link to string together the entire list.

The fact that a linked list’s data can be spread throughout the computer’s memory is a potential advantage it has over the array. An array, by contrast, needs to find an entire block of contiguous cells to store its data, which can get increasingly difficult as the array size grows. These details are managed by your programming language under the hood, so you may not have to worry about them. However, you’ll see shortly that there are more tangible differences between linked lists and arrays that we can sink our teeth into.

## Implementing a Linked List

Some programming languages, such as Java, come with linked lists built into the language. Many languages don’t, but it’s fairly simple to implement them on our own.

Let’s create our own linked list using JavaScript. We’ll use two classes to implement this: Node and LinkedList. Let’s create the Node class first:

| ​  | ​**class**​ Node { |
| ​  | ​**constructor**​(data) { |
| ​  | ​**this**​.data = data; |
| ​  | ​**this**​.nextNode = ​**null**​; |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | ​**export**​ ​**default**​ Node; |

The Node class has two attributes: data contains the node’s primary value (for example, the string "a"), while nextNode contains the link to the next node in the list. We can use this class as follows:

| ​  | ​**const**​ node1 = ​**new**​ Node(​*'once'*​); |
| ​  | ​**const**​ node2 = ​**new**​ Node(​*'upon'*​); |
| ​  | ​**const**​ node3 = ​**new**​ Node(​*'a'*​); |
| ​  | ​**const**​ node4 = ​**new**​ Node(​*'time'*​); |
| ​  |  |
| ​  | node1.nextNode = node2; |
| ​  | node2.nextNode = node3; |
| ​  | node3.nextNode = node4; |

With this code, we’ve created a list of four nodes that serve as a list containing the strings ’once’, ’upon’, ’a’, and ’time’.

Note that in our implementation, the nextNode refers to another Node instance rather than an actual memory address number. The effect, however, is the same—the nodes are likely dispersed throughout the computer’s memory, and yet we can use the nodes’ links to string the list together.

Going forward, then, we’re simply going to discuss each link as pointing to another node rather than to a specific memory address. Accordingly, we’re going to use simplified diagrams to depict linked lists, such as this one:

![images/pitting_linked_lists_against_arrays/once_upon_a_time.png](images/pitting_linked_lists_against_arrays/once_upon_a_time.png)

Each node in this diagram consists of two cells. The first cell contains the node’s data, and the second cell points to the next node.

This reflects our implementation of the Node class. In it, the data method returns the node’s data, while the nextNode method returns the next node in the list. In this context, the nextNode method serves as the node’s link.

While we’ve been able to create this linked list with the Node class alone, we still need an easy way to tell our program where the linked list begins. To do this, we’ll create a LinkedList class in addition to our previous Node class. Here’s the LinkedList class in its basic form:

| ​  | ​**import**​ Node ​**from**​ ​*'./node.js'*​; |
| ​  |  |
| ​  | ​**class**​ LinkedList { |
| ​  | ​**constructor**​(firstNode=​**null**​) { |
| ​  | ​**this**​.firstNode = firstNode; |
| ​  | } |

| ​  | } |

Note that we import node at the beginning of our code, since we placed the Node class in a separate file from this LinkedList class.

At this point, all a LinkedList instance does is keep track of the first node of the list.

Previously we created a chain of nodes containing node1, node2, node3, and node4. We can now use our LinkedList class to reference this list by writing the following code:

| ​  | ​**const**​ list = ​**new**​ LinkedList(node1); |

This list variable now acts as a handle on the linked list, as it’s an instance of LinkedList that has access to the list’s first node.

An important point emerges: when dealing with a linked list, we have immediate access only to its head. This is going to have serious ramifications, as we’ll see shortly.

At first glance, though, linked lists and arrays are similar—they’re both just lists of stuff. When we dig into the analysis, though, we’ll see some dramatic differences in these two data structures’ performances! Let’s jump into the four classic operations: reading, searching, insertion, and deletion.

## Reading

As you know, a computer can read from an array in O(1) time. But now let’s figure out the efficiency of reading from a linked list.

If you want to read, say, the value of the third item of a linked list, the computer cannot look it up in one step, because it wouldn’t immediately know where to find it in the computer’s memory. After all, each node of a linked list could be anywhere in memory! All our program knows immediately is the memory address of the first node of the linked list; it doesn’t know offhand where any of the other nodes are.

To read from the third node, then, the computer must go through a process. First, it accesses the first node. It then follows the first node’s link to the second node and then the second node’s link to the third node.

To get to any node, then, we always need to start with the first node (the only node we initially have access to), and follow the chain of nodes until we reach the node we want.

It turns out, then, that if we were to read from the last node in the list, it would take N steps for N nodes in the list. Linked lists having a worst-case read of O(N) is a major disadvantage when compared with arrays that can read any element in just O(1). But don’t fret, as linked lists will have their moment to shine, as we’ll see soon.

### Code Implementation: Linked List Reading

Let’s go ahead and add a read method to our LinkedList class:

| ​  | read(index) { |
| ​  | ​**let**​ currentNode = ​**this**​.firstNode; |
| ​  | ​**let**​ currentIndex = 0; |

| ​  | ​**while**​ (currentIndex < index) { |
| ​  | currentNode = currentNode.nextNode; |
| ​  | currentIndex += 1; |
| ​  |  |
| ​  | ​**if**​ (!currentNode) { |
| ​  | ​**return**​ ​**null**​; |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | ​**return**​ currentNode.data; |
| ​  | } |

If we want to read the fourth node from a list, for example, we’d call our method by passing in the node’s index as follows:

| ​  | list.read(3); |

Let’s walk through how this method works.

First, we create a variable called currentNode that refers to the node we’re currently accessing. Since we’re going to start by accessing the head, we say this:

| ​  | ​**let**​ currentNode = ​**this**​.firstNode; |

Recall that firstNode is an instance variable of the LinkedList class.

We also track the index of currentNode so that we can know when we reach the desired index. We start at 0 since the first node’s index is 0:

| ​  | ​**let**​ currentIndex = 0; |

We then launch a loop that runs while currentIndex is less than the index we’re attempting to read:

| ​  | ​**while**​ (currentIndex < index) { |

In each pass-through of the loop, we access the next node in the list and make it the new currentNode:

| ​  | currentNode = currentNode.nextNode; |

We also bump up the currentIndex by 1:

| ​  | currentIndex += 1; |

At the end of each pass-through, we check whether we’ve reached the end of the list, and we return null if the index we’re trying to read isn’t in our list:

| ​  | ​**if**​ (!currentNode) { |
| ​  | ​**return**​ ​**null**​; |
| ​  | } |

This works because the final node of the list will actually have a nextNode that is null since the last node was never assigned a nextNode of its own. This being the case, when currentNode refers to the final node and we then execute current =currentNode.nextNode, the currentNode becomes null.

Finally, if we do break out of the loop, it’s because we reached the desired index. We can then return the node’s value with the following:

| ​  | ​**return**​ currentNode.data; |

## Searching

As you know, searching means looking for a value within the list and returning its index. We’ve seen that linear search on an array has a speed of O(N), since the computer needs to inspect each value one at a time.

Linked lists also have a search speed of O(N). To search for a value, we need to go through a similar process to the one we did with reading; that is, we begin with the head and follow the links of each node to the next one. Along the way, we inspect each value until we find what we’re looking for.

### Code Implementation: Linked List Search

Here’s how we can implement the search operation in JavaScript. We’ll call this method search and pass in the value we’re searching for:

| ​  | search(value) { |
| ​  | ​**let**​ currentNode = ​**this**​.firstNode; |
| ​  | ​**let**​ currentIndex = 0; |
| ​  |  |
| ​  | ​**while**​ (​**true**​) { |
| ​  | ​**if**​ (currentNode.data === value) { |
| ​  | ​**return**​ currentIndex; |
| ​  | } |
| ​  |  |
| ​  | currentNode = currentNode.nextNode; |
| ​  |  |
| ​  | ​**if**​ (!currentNode) { |
| ​  | ​**break**​; |
| ​  | } |
| ​  |  |
| ​  | currentIndex += 1; |
| ​  | } |
| ​  |  |
| ​  | ​**return**​ ​**null**​; |
| ​  | } |

We can then search for any value within the list, like so:

| ​  | list.search(​*'time'*​); |

Using this, we would get back the index of where ’time’ is located within the list. In our example above, this would be 3.

As you can see, the mechanics of searching are similar to reading. The main difference is that the loop doesn’t stop at a particular index but runs until we either find the value or reach the end of the list.

## Insertion

Admittedly, linked lists have yet to impress us from a performance standpoint. They’re no better than arrays at search, and much worse at reading. But not to worry—linked lists will have their moment. In fact, that moment is now.

Insertion is one operation in which linked lists have a distinct advantage over arrays in certain situations.

Recall that the worst-case scenario for insertion into an array is when the program inserts data into index 0, because it first has to shift the rest of the data one cell to the right, which ends up yielding an efficiency of O(N). With linked lists, however, insertion at the beginning of the list takes just one step—which is O(1). Let’s see why.

Say we have the following linked list:

If we want to ...

## Deletion

Linked lists also shine when it comes to deletion, especially when deleting from the beginning of the list.

To delete a node from the beginning of a linked list, all we need to do is perform one step: we change the firstNode of the linked list to now point to the second node.

Let’s return to our example of the linked list containing the values "once", "upon", "a", and "time". If we want to delete the value "once", we could simply change the linked list to begin at "upon":

| ​  | list.firstNode = node2; |

Contrast this with an array, in which deleting the first element means shifting all remaining data one cell to the left, which takes O(N) time.

When it comes to deleting the final node of a linked list, the actual deletion takes one step—we just take the second-to-last node and make its link null. However, it takes N steps to even access the second-to-last node in the first place, since we need to start at the beginning of the list and follow the links until we reach it.

The following table contrasts the various scenarios of deletion for both arrays and linked lists. Note how it’s identical to insertion:

| Situation | Array | Linked List |
| --- | --- | --- |
| Delete at beginning | Worst case | Best case |
| Delete at middle | Average case | Average case |
| Delete at end | Best case | Worst case |

While deleting from the beginning or end of a linked list is straightforward, deleting from anywhere in the middle is slightly more involved.

Say we want to delete the value at index 2 ("purple") from our example linked list of colors, as shown in the following diagram:

![images/pitting_linked_lists_against_arrays/list_of_colors.png](images/pitting_linked_lists_against_arrays/list_of_colors.png)

To accomplish this, we need to first access the node immediately preceding the one we’re deleting ("blue”). Then we change its link to point to the node that is immediately after the node we’re deleting ("green").

The following visualization demonstrates us changing the link of the "blue" node from "purple" to "green":

![images/pitting_linked_lists_against_arrays/linked_list_6.png](images/pitting_linked_lists_against_arrays/linked_list_6.png)

It’s interesting to note that whenever we delete a node from our linked list, the node still exists in memory somewhere. We’re just removing the node from our list by ensuring that no other node from the list links to it. This has the effect of deleting the node from our list, even if the node still exists in memory.

(Different programming languages handle these deleted nodes in various ways. Some will automatically detect that they’re not being used and will “garbage collect” them, freeing up memory.)

### Code Implementation: Linked List Deletion

Here’s what the delete operation might look like in our LinkedList class. It’s called delete, and we pass in the index we’re going to delete:

| ​  | ​**delete**​(index) { |
| ​  | ​**if**​ (index === 0) { |
| ​  | ​**this**​.firstNode = ​**this**​.firstNode.nextNode; |
| ​  | ​**return**​; |
| ​  | } |
| ​  |  |
| ​  | ​**let**​ currentNode = ​**this**​.firstNode; |
| ​  | ​**let**​ currentIndex = 0; |
| ​  |  |
| ​  | ​**while**​ (currentIndex < (index - 1)) { |
| ​  | currentNode = currentNode.nextNode; |
| ​  | currentIndex += 1; |
| ​  | } |
| ​  |  |
| ​  | ​**const**​ nodeAfterDeletedNode = currentNode.nextNode.nextNode; |
| ​  | currentNode.nextNode = nodeAfterDeletedNode; |
| ​  | } |

This method is pretty similar to the insert method we saw earlier. Let’s highlight some of the novel points.

The method first deals with a case in which index is 0, meaning we intend to delete the first node of the list. The code for this is ridiculously simple:

| ​  | ​**if**​ (index === 0) { |
| ​  | ​**this**​.firstNode = ​**this**​.firstNode.nextNode; |
| ​  | ​**return**​; |
| ​  | } |

All we do is change our list’s firstNode to point to what is currently the second node, and we’re done!

The rest of the method handles deletions anywhere else from the list. To do this, we use a while loop to access the node immediately preceding the one we want to delete. This becomes our currentNode.

We then grab the node that comes immediately after the node we’re going to delete and store it in a variable called nodeAfterDeletedNode:

| ​  | ​**const**​ nodeAfterDeletedNode = currentNode.nextNode.nextNode; |

Notice our little trick in accessing that node. It’s simply the node that comes two nodes after the currentNode!

Then we modify the link of the currentNode to point to the nodeAfterDeletedNode:

| ​  | currentNode.nextNode = nodeAfterDeletedNode; |

## Efficiency of Linked List Operations

After our analysis, it emerges that the comparison of linked lists and arrays breaks down as follows:

| Operation | Array | Linked list |
| --- | --- | --- |
| Reading | O(1) | O(N) |
| Search | O(N) | O(N) |
| Insertion | O(N) (O(1) at end) | O(N) (O(1) at beginning) |
| Deletion | O(N) (O(1) at end) | O(N) (O(1) at beginning) |

In the grand scheme of things, linked lists seem to be lackluster when it comes to time complexity. They perform similarly to arrays for search, insertion, and deletion, and are much slower when it comes to reading. If so, why would one ever want to use a linked list?

The key to unlocking the linked list’s power is in the fact that the actual insertion and deletion steps are just O(1).

But isn’t that only relevant when inserting or deleting at the beginning ...

## Linked Lists in Action

One case where linked lists shine is when we examine a single list and delete many elements from it. Let’s say, for example, we’re building an application that combs through existing lists of email addresses and removes any email address that has an invalid format.

No matter whether the list is an array or a linked list, we need to comb through the entire list one element at a time to inspect each email address. This, naturally, takes N steps. However, let’s examine what happens when we actually delete each email address.

With an array, each time we delete an email address, we need another O(N) steps to shift the remaining data to the left to close the gap. All this shifting will happen before we can even inspect the next email address.

Let’s assume that 1 in 10 email addresses are invalid. If we had a list of 1,000 email addresses, we’d have about 100 invalid ones. Our algorithm, then, would take 1,000 steps to read all 1,000 email addresses. On top of that, though, it might take up to an additional 100,000 steps for deletion, as for each of the 100 deleted addresses, we might shift up to 1,000 other elements.

With a linked list, however, as we comb through the list, each deletion takes just one step, as we can simply change a node’s link to point to the appropriate node and move on. For our 1,000 emails, then, our algorithm would take just 1,100 steps, as there are 1,000 reading steps and 100 deletion steps.

It turns out, then, that linked lists are an amazing data structure for moving through an entire list while making insertions or deletions, as we never have to worry about shifting other data as we make an insertion or deletion.

## Doubly Linked Lists

Linked lists come in a number of different flavors. The linked list we’ve discussed until this point is the classic linked list, but with some slight modifications we can grant linked lists additional superpowers.

One variant form of the linked list is the doubly linked list.

A doubly linked list is like a linked list except that each node has two links—one that points to the next node and another that points to the previous node. In addition, the doubly linked list always keeps track of both the head and tail nodes, instead of just the head.

Here’s what a doubly linked list looks like:

![images/pitting_linked_lists_against_arrays/doubly_linked_list.png](images/pitting_linked_lists_against_arrays/doubly_linked_list.png)

We can implement the core of a doubly ...

## Queues as Doubly Linked Lists

Because doubly linked lists have immediate access to both the front and end of the list, they can insert data on either side at O(1) as well as delete data on either side at O(1).

Because doubly linked lists can insert data at the end in O(1) time and delete data from the front in O(1) time, they make the perfect underlying data structure for a queue.

We looked at [​*Queues*​](#f_0092.xhtml_sect.queues), and you’ll recall that they are lists of items in which data can only be inserted at the end and removed from the beginning. You learned there that queues are an example of an abstract data type and that we were able to use an array to implement them under the hood.

Now, since queues insert at the end and delete from the beginning, arrays are only so good as the underlying data structure. While arrays are O(1) for insertions at the end, they’re O(N) for deleting from the beginning.

A doubly linked list, on the other hand, is O(1) for both inserting at the end and for deleting from the beginning. That’s what makes it a perfect fit for serving as the queue’s underlying data structure.

### Code Implementation: Queue Built upon a Doubly Linked List

Before implementing the queue itself, we’ll first add one more method to our DoublyLinkedList class. This popHead method removes the head from the list and returns it:

| ​  | popHead() { |
| ​  | ​**const**​ poppedNode = ​**this**​.firstNode; |
| ​  | ​**this**​.firstNode = ​**this**​.firstNode.nextNode; |
| ​  | ​**this**​.firstNode.previousNode = ​**null**​; |
| ​  | ​**return**​ poppedNode; |
| ​  | } |

As you can see, we effectively delete the first node by changing the list’s this.firstNode to be what is currently the second node. We also make sure that the new head doesn’t link to any previous node. Finally, we return the node we just deleted.

With this in place, we can now create a queue implementation that is built upon a doubly linked list:

| ​  | ​**import**​ DoublyLinkedList ​**from**​ ​*'./doubly_linked_list.js'*​; |
| ​  |  |
| ​  | ​**class**​ Queue { |
| ​  | ​**constructor**​() { |
| ​  | ​**this**​.data = ​**new**​ DoublyLinkedList(); |
| ​  | } |
| ​  |  |
| ​  | enqueue(element) { |
| ​  | ​**this**​.data.append(element); |
| ​  | } |
| ​  |  |
| ​  | dequeue() { |
| ​  | ​**const**​ dequeuedNode = ​**this**​.data.popHead(); |
| ​  | ​**return**​ dequeuedNode.data; |
| ​  | } |
| ​  |  |
| ​  | read() { |
| ​  | ​**if**​ (!​**this**​.data.firstNode) { ​**return**​ ​**null**​; } |
| ​  |  |
| ​  | ​**return**​ ​**this**​.data.firstNode.data; |
| ​  | } |
| ​  | } |

The Queue class implements its methods on top of our DoublyLinkedList. The enqueue method relies on the append method of our DoublyLinkedList:

| ​  | enqueue(element) { |
| ​  | ​**this**​.data.append(element); |
| ​  | } |

Similarly, the dequeue method takes advantage of the linked list’s ability to delete from the front of the list:

| ​  | dequeue() { |
| ​  | ​**const**​ dequeuedNode = ​**this**​.data.popHead(); |
| ​  | ​**return**​ dequeuedNode.data; |
| ​  | } |

By implementing our queue with a doubly linked list, we can now both insert and delete from the queue at a speedy O(1). And that’s doubly awesome.

## Wrapping Up

As we’ve seen, the subtle differences between arrays and linked lists unlock new ways to make our code faster than ever.

By looking at linked lists, you’ve also learned the concept of nodes. However, the linked list is only the simplest of node-based data structures. In the coming chapters, you’ll learn about node-based structures that are both more complex and more interesting—and that will reveal new worlds about how nodes can yield tremendous power and efficiency.

## Exercises

The following exercises provide you with the opportunity to practice with linked lists. The solutions to these exercises are found in the section [​*Chapter 14*​](#f_0219.xhtml_pitting.linked.lists.against.arrays.solutions).

1.  Add a method to the classic LinkedList class that prints all the values of the list.

2.  Add a method to the DoublyLinkedList class that prints all the values of the list in reverse order.

3.  Add a method to the classic LinkedList class that returns the last value from the list. Assume you don’t know how many elements are in the list.

4.  Here’s a tricky one. Add a method to the classic LinkedList class that reverses the list; that is, if the original list is A -> B -> C, all of the list’s links should change so that C -> B -> A.

5.  Here’s a brilliant little linked list puzzle for you. Let’s say you have access to a node from somewhere in the middle of a classic linked list but not to the linked list itself; that is, you have a variable that points to an instance of Node, but you don’t have access to the LinkedList instance. In this situation, if you follow this node’s link, you can find all the values from this middle node until the end, but you have no way to find the nodes that precede this node in the list.

    Write code that will effectively delete this node from the list. The entire remaining list should remain complete, with only this node removed.

Copyright © 2024, The Pragmatic Bookshelf.

# Chapter 15Speeding Up All the Things with Binary Search Trees

Sometimes, we may want to arrange our data in a specific order. For example, we may want an alphabetized list of names or a list of products in order of lowest price to highest.

While we can use a sorting algorithm such as Quicksort to arrange our data into perfect ascending order, it comes at a cost. As we’ve seen, even the fastest algorithms take O(N log N) time. So if we’re going to want our data sorted often, it would be sensible to always keep our data in sorted order in the first place so that we never need to re-sort it.

An ordered array is a simple but effective tool for keeping data in order. It’s also fast for certain operations, as it has O(1) reads and O(log N) search ...

## Trees

You were introduced to node-based data structures in the previous chapter with linked lists. In a classic linked list, each node contains a link that connects the node to a single other node. A tree is also a node-based data structure, but within a tree each node can have links to multiple nodes.

Here is a visualization of a simple tree:

![images/binary_trees/bst_1.png](images/binary_trees/bst_1.png)

In this example, each node has links that lead to two other nodes. For the sake of simplicity, we can represent this tree visually without showing all the memory addresses:

![images/binary_trees/bst_2.png](images/binary_trees/bst_2.png)

Trees come with their own unique nomenclature:

*   The uppermost node (in our example, “j”) is called the root. Yes, in our picture the root is at the top of the tree; it’s how trees are typically depicted.

*   In our example, we’d say that “j” is a parent to “m” and “b”. Conversely, “m” and “b” are children of “j”. Similarly, the “m” is a parent of “q” and “z”, and “q” and “z” are children of “m”.

*   As in a family tree, a node can have descendants and ancestors. A node’s descendants are all the nodes that stem from a node, while a node’s ancestors are all the nodes that it stems from. In our example, “j” is the ancestor of all the other nodes in the tree, and all the other nodes are, therefore, descendants of “j”.

*   Trees are said to have levels. Each level is a row within the tree. Our example tree has three levels:

![images/binary_trees/bst_3.png](images/binary_trees/bst_3.png)

*   One property of a tree is how balanced it is. A tree is balanced when its nodes’ subtrees have the same number of nodes in it.

For instance, the preceding tree is said to be perfectly balanced. If you look at each node, its two subtrees have the same number of nodes. The root node (“j”) has two subtrees, which each contain three nodes. You’ll see that the same is also true for every node in the tree. For example, the “m” node also has two subtrees where the two subtrees each contain one node.

The following tree, on the other hand, is imbalanced:

![images/binary_trees/imbalanced_tree.png](images/binary_trees/imbalanced_tree.png)

As you can see, the root’s right subtree contains more nodes than its left subtree, causing an imbalance.

## Binary Search Trees

Many different kinds of tree-based data structures exist, but in this chapter, we’ll focus on a particular tree known as a binary search tree.

Note that there are two adjectives here: binary and search.

A binary tree is a tree in which each node has zero, one, or two children.

A binary search tree is a binary tree that also abides by the following rules:

*   Each node can have at most one left child and one right child.
*   A node’s left descendants can only contain values that are less than the node itself. Likewise, a node’s right descendants can only contain values that are greater than the node itself.

Here’s an example of a binary search tree, in which the values are numbers:

![images/binary_trees/bst_4.png](images/binary_trees/bst_4.png)

Note that each node has one child with a lesser value than itself, which is depicted using a left arrow, and one child with a greater value than itself, which is depicted using a right arrow.

Additionally, notice that all of the 50’s left descendants are less than it. At the same time, all of the 50’s right descendants are greater than it. The same pattern goes for each and every node.

While the following example is a binary tree, it’s not a binary search tree:

![images/binary_trees/bst_5.png](images/binary_trees/bst_5.png)

It’s a binary tree because each node has zero, one, or two children. But it’s not a binary search tree, because the root node has two left children; that is, it has two children than are less than it. For a binary search tree to be valid, it can have at most one left (lesser) child and one right (greater) child.

The implementation of a tree node in JavaScript might look something like this:

| ​  | ​**class**​ TreeNode { |
| ​  | ​**constructor**​(value, left=​**null**​, right=​**null**​) { |
| ​  | ​**this**​.value = value; |
| ​  | ​**this**​.leftChild = left; |
| ​  | ​**this**​.rightChild = right; |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | ​**export**​ ​**default**​ TreeNode; |

We can then build a simple tree like this:

| ​  | ​**const**​ node1 = ​**new**​ TreeNode(25); |
| ​  | ​**const**​ node2 = ​**new**​ TreeNode(75); |
| ​  | ​**let**​ root = ​**new**​ TreeNode(50, node1, node2); |

Because of the unique structure of a binary search tree, we can search for any value within it very quickly, as we’ll now see.

## Searching

Here, again, is a binary search tree:

![images/binary_trees/bst_4.png](images/binary_trees/bst_4.png)

The algorithm for searching within a binary search tree is as follows:

1.  Designate a node to be the current node. (At the beginning of the algorithm, the root node is the first current node.)

2.  Inspect the value at the current node.

3.  If we’ve found the value we’re looking for, great!

4.  If the value we’re looking for is less than the current node, search for it in its left subtree.

5.  If the value we’re looking for is greater than the current node, search for it in its right subtree.

6.  Repeat Steps 1 through 5 until we find the value we’re searching for, or until we hit the bottom of the tree, in which case our ...

## Insertion

As I mentioned earlier, binary search trees are at their best when it comes to insertion. Now we’ll see why.

Say we want to insert the number 45 into our example tree. The first thing we’d have to do is find the correct node to attach the 45 to. To begin our search, we start at the root, as shown in the following illustration:

![images/binary_trees/bst_6.png](images/binary_trees/bst_6.png)

Since 45 is less than 50, we drill down to the left child:

![images/binary_trees/bst_10.png](images/binary_trees/bst_10.png)

Since 45 is greater than 25, we must inspect the right child:

Since 45 is greater than 33, we check the 33’s right child:

At this point, we’ve reached a ...

## Deletion

Deletion is the least straightforward operation within a binary search tree and requires some careful maneuvering.

Let’s say we want to delete the 4 from this binary search tree:

![images/binary_trees/bst_4.png](images/binary_trees/bst_4.png)

First, we perform a search to find the 4\. We won’t visualize this search again, since you’ve already got that down.

Once we find the 4, we can delete it in one step:

![images/binary_trees/bst_16.png](images/binary_trees/bst_16.png)

Well, that was simple. But let’s see what happens when we try to delete the 10:

![images/binary_trees/bst_17.png](images/binary_trees/bst_17.png)

We end up with an 11 that isn’t connected to the tree anymore. And we can’t have that, because we’d lose the 11 forever.

However, to solve this problem, we can plug the 11 into where the 10 used to be:

![images/binary_trees/bst_18.png](images/binary_trees/bst_18.png)

So far, our deletion algorithm follows these rules:

*   If the node being deleted has no children, simply delete it.
*   If the node being deleted has one child, delete the node and plug the child into the spot where the deleted node was.

### Deleting a Node with Two Children

Deleting a node that has two children is the most complex scenario. Let’s say we want to delete the 56 in this tree:

![images/binary_trees/bst_19.png](images/binary_trees/bst_19.png)

What are we going to do with its former children, 52 and 61? We can’t move both of them to where the 56 was. This is where the next rule of the deletion algorithm comes into play:

*   When deleting a node with two children, replace the deleted node with the successor node. The successor node is the child node whose value is the least of all values that are greater than the deleted node.

That was a tricky sentence. To put it in other words: if we were to put the deleted node and all of its descendants in ascending order, the successor node would be the next number after the one we just deleted.

In this case, it’s easy to figure out which node is the successor since the deleted node had only two descendants. If we put the numbers 52-56-61 in ascending order, the next number after 56 is 61.

Once we find the successor node, we plug it into where the deleted node was. So we replace the 56 with the 61:

![images/binary_trees/bst_20.png](images/binary_trees/bst_20.png)

### Finding the Successor Node

How does the computer find the successor node? This can be tricky when we delete a node high up in the tree.

Here’s the algorithm for finding the successor node:

*   Visit the right child of the deleted value, and then keep on visiting the left child of each subsequent child until there are no more left children. The bottom value is the successor node.

Let’s see this again in action in a more complex example. Let’s delete the root node:

![images/binary_trees/delete_root_node.png](images/binary_trees/delete_root_node.png)

We now need to plug the successor node into where the 50 was and turn it into the root node. So let’s find the successor node.

To do this, we first visit the right child of the deleted node, and then keep descending leftward until we reach a node that doesn’t have a left child:

![images/binary_trees/bst_21.png](images/binary_trees/bst_21.png)

It turns out that the 52 is the successor node.

Now that we’ve found the successor node, we plug it into the node we deleted:

![images/binary_trees/bst_22.png](images/binary_trees/bst_22.png)

And we’re done!

### Successor Node with a Right Child

We haven’t accounted for one case yet, though, and that’s where the successor node has a right child of its own. Let’s re-create the preceding tree but add a right child to the 52:

![images/binary_trees/bst_23.png](images/binary_trees/bst_23.png)

In this case, we can’t simply plug the successor node—the 52—into the root, since we’d leave its child of 55 hanging. This leads us to one more rule for our deletion algorithm:

*   If the successor node has a right child, after plugging the successor node into the spot of the deleted node, take the former right child of the successor node and place it where the successor node used to be.

That was another tricky sentence, so let’s walk through the steps.

First, we plug the successor node (52) into the root. This leaves the 55 dangling without a parent:

![images/binary_trees/bst_24.png](images/binary_trees/bst_24.png)

Next, we place the 55 in the spot where the successor node used to be, which is the left child of the 61:

![images/binary_trees/bst_25.png](images/binary_trees/bst_25.png)

### Successor Node is a Right Child

It can sometimes happen that the successor node is itself a right child. And sometimes this successor node can have a right child of its own. For example, in the following tree, if we delete the 3, the 4 becomes the successor node, since the 4 has no left children:

![images/binary_trees/bst_15.png](images/binary_trees/bst_15.png)

Here, when we plug the successor node into the spot where the deleted 3 was, we don’t make the 5 dangling and reattach it elsewhere. Instead, we simply keep the 5 as the 4’s right child.

And now we’re really done.

### The Complete Deletion Algorithm

Putting all the steps together, here is the algorithm for deletion from a binary search tree:

*   If the node being deleted has no children, simply delete it.

*   If the node being deleted has one child, delete the node and plug the child into the spot where the deleted node was.

*   When deleting a node with two children, replace the deleted node with the successor node. The successor node is the child node whose value is the least of all values that are greater than the deleted node.

*   To find the successor node: visit the right child of the deleted node, and then keep on visiting the left child of each subsequent child until there are no more left children. The bottom node is the successor node. If the deleted node’s right child has no left children, the deleted node’s right child itself becomes the successor node.

*   If the successor node has a right child (and the successor node was itself a left child of its parent), after plugging the successor node into the spot of the deleted node, take the former right child of the successor node and turn it into the left child of the former parent of the successor node.

### Code Implementation: Binary Search Tree Deletion

Here’s a JavaScript implementation of deletion from a binary search tree. The primary method here is delete, which in turn relies on a helper method called replaceWithSuccessorNode:

| ​  | ​**function**​ deleteNode(valueToDelete, node) { |
| ​  | ​**let**​ currentNode = node; |
| ​  | ​**let**​ parentOfCurrentNode; |
| ​  | ​**let**​ childOfDeletedNode; |
| ​  | ​**let**​ nodeToDelete; |
| ​  |  |
| ​  | ​**while**​ (currentNode) { |
| ​  | ​**if**​ (currentNode.value === valueToDelete) { |
| ​  | nodeToDelete = currentNode; |
| ​  | ​**break**​; |
| ​  | } |
| ​  |  |
| ​  | parentOfCurrentNode = currentNode; |
| ​  | ​**if**​ (valueToDelete < currentNode.value) { |
| ​  | currentNode = currentNode.leftChild; |
| ​  | } ​**else**​ ​**if**​ (valueToDelete > currentNode.value) { |
| ​  | currentNode = currentNode.rightChild; |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | ​**if**​ (!nodeToDelete) { ​**return**​ ​**null**​; } |
| ​  |  |
| ​  | ​**if**​ (nodeToDelete.leftChild && nodeToDelete.rightChild) { |
| ​  | replaceWithSuccessorNode(nodeToDelete); |
| ​  | } ​**else**​ { ​*// deleted node has 0 or 1 children*​ |
| ​  | childOfDeletedNode = (nodeToDelete.leftChild &#124;&#124; nodeToDelete.rightChild); |
| ​  |  |
| ​  | ​**if**​ (!parentOfCurrentNode) { |
| ​  | nodeToDelete.value = childOfDeletedNode.value; |
| ​  | nodeToDelete.leftChild = childOfDeletedNode.leftChild; |
| ​  | nodeToDelete.rightChild = childOfDeletedNode.rightChild; |
| ​  | } ​**else**​ ​**if**​ (nodeToDelete === parentOfCurrentNode.leftChild) { |
| ​  | parentOfCurrentNode.leftChild = childOfDeletedNode; |
| ​  | } ​**else**​ ​**if**​ (nodeToDelete === parentOfCurrentNode.rightChild) { |
| ​  | parentOfCurrentNode.rightChild = childOfDeletedNode; |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | ​**return**​ nodeToDelete; |
| ​  | } |
| ​  |  |
| ​  | ​**function**​ replaceWithSuccessorNode(node) { |
| ​  | ​**let**​ successorNode = node.rightChild; |
| ​  | ​**let**​ parentOfSuccessorNode; |
| ​  |  |
| ​  | ​**if**​ (!successorNode.leftChild) { |
| ​  | node.value = successorNode.value; |
| ​  | node.rightChild = successorNode.rightChild; |
| ​  | ​**return**​; |
| ​  | } |
| ​  |  |
| ​  | ​**while**​ (successorNode.leftChild) { |
| ​  | parentOfSuccessorNode = successorNode; |
| ​  | successorNode = successorNode.leftChild; |
| ​  | } |
| ​  |  |
| ​  | ​**if**​ (successorNode.rightChild) { |
| ​  | parentOfSuccessorNode.leftChild = successorNode.rightChild; |
| ​  | } ​**else**​ { |
| ​  | parentOfSuccessorNode.leftChild = ​**null**​; |
| ​  | } |
| ​  |  |
| ​  | node.value = successorNode.value; |
| ​  | ​**return**​ successorNode; |
| ​  | } |

That’s a decent amount of code, but we’ll walk through it step by step.

In contrast with search and insertion, we wrote the deletion code without recursion. While we could have written the deletion method recursively, I find that the recursive code for deletion is considerably more difficult to grasp. Instead, we use a loop to move about the tree.

Let’s begin by walking through the delete method.

When we call this method, we pass in the value we’d like to delete (valueToDelete) as well as the root node of the tree (node).

At first, we create a few variables:

| ​  | ​**let**​ currentNode = node; |
| ​  | ​**let**​ parentOfCurrentNode; |
| ​  | ​**let**​ childOfDeletedNode; |
| ​  | ​**let**​ nodeToDelete; |

The currentNode initially points to the root but will be updated as we move down the tree looking for the value we are to delete. The parentOfCurrentNode, as the name implies, will track the parent of the currentNode. The same goes for the variable childOfDeletedNode. The reason we need to track these will become apparent later on. Finally, the nodeToDelete will eventually point to the node we’ll be deleting.

We then begin a loop that searches for the valueToDelete within the tree. This is essentially a search operation, but again, this time we use iteration instead of recursion:

| ​  | ​**while**​ (currentNode) { |
| ​  | ​**if**​ (currentNode.value === valueToDelete) { |
| ​  | nodeToDelete = currentNode; |
| ​  | ​**break**​; |
| ​  | } |
| ​  |  |
| ​  | parentOfCurrentNode = currentNode; |
| ​  | ​**if**​ (valueToDelete < currentNode.value) { |
| ​  | currentNode = currentNode.leftChild; |
| ​  | } ​**else**​ ​**if**​ (valueToDelete > currentNode.value) { |
| ​  | currentNode = currentNode.rightChild; |
| ​  | } |
| ​  | } |

This snippet moves down through the tree, updating currentNode as we go, searching for the valueToDelete. If we don’t find it, which will be the case if the value is not present in the tree, the loop will terminate on its own because currentNode will be null.

If, however, we do find the valueToDelete, we declare the currentNode to be the nodeToDelete and break out of the loop. Note that we also keep track of the parentOfCurrentNode, which is now the parent of the node we’ll be deleting.

Next, we have this snippet:

| ​  | ​**if**​ (!nodeToDelete) { ​**return**​ ​**null**​; } |

This returns null if the value we’d like to delete isn’t even in our tree to begin with.

The remainder of this method performs the actual deletion. We first handle the most complex case, where the node we’re deleting has two children:

| ​  | ​**if**​ (nodeToDelete.leftChild && nodeToDelete.rightChild) { |
| ​  | replaceWithSuccessorNode(nodeToDelete); |
| ​  | } |

Here, we outsource the heavy lifting to the replaceWithSuccessorNode helper method, which we’ll analyze soon. In the meantime, though, let’s move on.

Next, we handle the case in which the deleted node has 0 or 1 children:

| ​  | ​**else**​ { |
| ​  | childOfDeletedNode = (nodeToDelete.leftChild &#124;&#124; nodeToDelete.rightChild); |
| ​  |  |
| ​  | ​**if**​ (!parentOfCurrentNode) { |
| ​  | nodeToDelete.value = childOfDeletedNode.value; |
| ​  | nodeToDelete.leftChild = childOfDeletedNode.leftChild; |
| ​  | nodeToDelete.rightChild = childOfDeletedNode.rightChild; |
| ​  | } ​**else**​ ​**if**​ (nodeToDelete === parentOfCurrentNode.leftChild) { |
| ​  | parentOfCurrentNode.leftChild = childOfDeletedNode; |
| ​  | } ​**else**​ ​**if**​ (nodeToDelete === parentOfCurrentNode.rightChild) { |
| ​  | parentOfCurrentNode.rightChild = childOfDeletedNode; |
| ​  | } |
| ​  | } |

Here, we first set a new variable called childOfDeletedNode, which will represent the deleted node’s child. In a case where the deleted node has no children, this variable will be set to null. This variable is crucial, for when we delete our nodeToDelete, we need to place its child in the spot where the deleted node used to be.

And that’s exactly what the code above does in the two else if clauses. It determines whether the deleted node was a left or right child of its parent, and attaches the childOfDeletedNode to the deleted node’s parent accordingly.

The first clause in the if statement handles the case where we’re deleting the root node. To ensure that we mark the deleted root’s child as the new root, we overwrite the root with its child.

This brings us to the final line of our method, which simply returns the deleted node in case we may want to use it for some other purpose:

| ​  | ​**return**​ nodeToDelete; |

Let’s now return to the case where the deleted node had two children. Our previous code called the helper method replaceWithSuccessorNode, so let’s walk through that now.

When calling this method, we pass in the node that we’ll be deleting, which will be called node.

Next, we identify the successor node using the following code:

| ​  | ​**let**​ successorNode = node.rightChild; |
| ​  | ​**let**​ parentOfSuccessorNode; |
| ​  |  |
| ​  | ​**if**​ (!successorNode.leftChild) { |
| ​  | node.value = successorNode.value; |
| ​  | node.rightChild = successorNode.rightChild; |
| ​  | ​**return**​; |
| ​  | } |
| ​  |  |
| ​  | ​**while**​ (successorNode.leftChild) { |
| ​  | parentOfSuccessorNode = successorNode; |
| ​  | successorNode = successorNode.leftChild; |
| ​  | } |

Here, we begin at the deleted node’s right child, and then move down the tree following left children until we can’t go any further. That bottom node is our successor node. We also keep track of the successor node’s parent.

However, in the case that the successor node happens to be the deleted node’s right child (which occurs when the deleted node’s right child has no left children), we simply plug the successor node into the spot where the deleted node was. If this is the case, this is all we need to do. But if the successor node is a left child of its parent, we move on.

Next, we remove the successor node from its spot:

| ​  | ​**if**​ (successorNode.rightChild) { |
| ​  | parentOfSuccessorNode.leftChild = successorNode.rightChild; |
| ​  | } ​**else**​ { |
| ​  | parentOfSuccessorNode.leftChild = ​**null**​; |
| ​  | } |

Our code deals with two possible cases. The second case (in the else clause) is the simpler case, which is when the successor node has no children. In that case, we wipe away the successor node by replacing it with null.

In the more complex case, where the successor node has a right child, we place that right child in the spot where the successor node used to be.

We’ve successfully removed the successor node from the tree, but there’s one more critical step. Remember we didn’t initially set out to delete the successor node. Our entire goal was to delete the node from higher up in the tree.

To do that, we plug the successor node into the spot of the node we’re deleting:

| ​  | node.value = successorNode.value; |

Note that we don’t plug in the actual successor node; instead, we simply use its value to overwrite the value of node, effectively deleting node.

And that’s it! It was a journey, but we did it.

### The Efficiency of Binary Search Tree Deletion

Like search and insertion, deleting from trees is also typically O(log N). This is because deletion requires a search plus a few extra steps to deal with any hanging children. Contrast this with deleting a value from an ordered array, which is O(N) due to shifting elements to the left to close the gap of the deleted value.

## Binary Search Trees in Action

We’ve seen that binary search trees boast efficiencies of O(log N) for search, insertion, and deletion, making it an efficient choice for scenarios in which we need to store and manipulate ordered data. This is particularly true if we’ll be modifying the data often, because while ordered arrays are just as fast as binary search trees when searching data, binary search trees are significantly faster when it comes to inserting and deleting data.

For example, let’s say we’re creating an application that maintains a list of book titles. We’d want our application to have the following functionality:

*   Our program should be able to print the list of book titles in alphabetical order.

*   Our program should allow for constant ...

## Binary Search Tree Traversal

Now, we’ve already seen how to search, insert, and delete data from a binary search tree. I mentioned, though, that we also want to be able to print the entire list of book titles in alphabetical order. How can we do that?

First, we need the ability to visit every single node in the tree. Visiting nodes is another term for accessing them. The process of visiting every node in a data structure is known as traversing the data structure.

Second, we need to make sure we traverse the tree in alphabetically ascending order so that we can print the list in that order. You can traverse a tree in multiple ways, but for this application, we’ll perform what is known as inorder traversal, so that we can print each title in alphabetical order.

Recursion is a great tool for performing traversal. We’ll create a recursive function called traverse that can be called on a particular node. The function then performs the following steps:

1.  Call itself (traverse) recursively on the node’s left child. The function will keep getting called until we hit a node that does not have a left child.

2.  Visit the node. (For our book title app, we print the value of the node at this step.)

3.  Call itself (traverse) recursively on the node’s right child. The function will keep getting called until we hit a node that does not have a right child.

For this recursive algorithm, the base case is when we call traverse on a child that does not exist, in which case we return without doing anything further.

Here’s a JavaScript traverseAndPrint function that works for our list of book titles. Note how concise it is:

| ​  | ​**function**​ traverseAndPrint(node) { |
| ​  | ​**if**​ (!node) { ​**return**​; } |
| ​  |  |
| ​  | traverseAndPrint(node.leftChild); |
| ​  | console.log(node.value); |
| ​  | traverseAndPrint(node.rightChild); |
| ​  | } |

Let’s walk through the inorder traversal step by step.

We first call traverseAndPrint on “Moby Dick”. This, in turn, calls traverseAndPrint on the left child of “Moby Dick”, which is “Great Expectations”:

| ​  | traverseAndPrint(node.leftChild); |

Before we move on to that, though, we’re going to add to the call stack the fact that we’re in the middle of the function in “Moby Dick” and the fact that we’re in the middle of traversing its left child:

![images/binary_trees/call_stack_1.png](images/binary_trees/call_stack_1.png)

We then proceed with traverseAndPrint("Great Expectations"), which calls traverse_and_print on the left child of “Great Expectations”, which is “Alice in Wonderland”.

Let’s add traverseAndPrint("Great Expectations") to the call stack before moving on:

![images/binary_trees/call_stack_2.png](images/binary_trees/call_stack_2.png)

The traverseAndPrint("Alice in Wonderland") calls traverseAndPrint on the left child of “Alice in Wonderland”. However, there isn’t any left child (the base case), so nothing happens. The next line of traverseAndPrint is the following:

| ​  | console.log(node.value); |

This line prints "Alice in Wonderland".

Next, the function attempts to traverseAndPrint the right child of “Alice in Wonderland”:

| ​  | traverseAndPrint(node.rightChild); |

However, there’s no right child (the base case), so the function returns without doing anything further.

Since we’ve completed the function traverseAndPrint("Alice in Wonderland"), we check the call stack to see where we’re up to in this recursive soup:

![images/binary_trees/call_stack_3.png](images/binary_trees/call_stack_3.png)

Ah, that’s right. We were in the middle of traverseAndPrint("Great Expectations"), and we had just completed calling traverseAndPrint on its left child. Let’s pop this from the call stack:

![images/binary_trees/call_stack_4.png](images/binary_trees/call_stack_4.png)

And let’s continue. The function next prints "Great Expectations" and then calls traverseAndPrint on the right child, which is “Lord of the Flies”. Before moving on to that, though, let’s hold our place within this function in the call stack:

![images/binary_trees/call_stack_5.png](images/binary_trees/call_stack_5.png)

We now execute traverseAndPrint("Lord of the Flies"). First, we call traverseAndPrint on its left child, but it doesn’t have one. Next, we print “Lord of the Flies”. Finally, we call traverseAndPrint on its right child, but that doesn’t exist either, so the function is now done.

We look at our call stack and see that we were in the process of executing traverseAndPrint on the right child of “Great Expectations”. We can pop that from the stack and continue, as shown in the [diagram](#f_0150.xhtml_fig.ch15.call_stack_6).

![images/binary_trees/call_stack_6.png](images/binary_trees/call_stack_6.png)

Now, it just so happens that we’ve also now completed everything we have to do in traverseAndPrint("Great Expectations"), so we can go back to the call stack to see what to do next:

![images/binary_trees/call_stack_7.png](images/binary_trees/call_stack_7.png)

We can see that we were in the middle of traverseAndPrint of the left child of “Moby Dick”. We can pop that from the call stack (which leaves the stack empty for now) and continue with the next step within traverseAndPrint("Moby Dick"), which is to print “Moby Dick”.

Then, we call traverseAndPrint on the right child of “Moby Dick”. We’ll add this to the call stack:

![images/binary_trees/call_stack_8.png](images/binary_trees/call_stack_8.png)

For the sake of brevity (although it’s probably too late for that), I’ll let you walk through the rest of the traverseAndPrint function from here.

By the time our function has finished executing, we’ll have printed the nodes in this order:

![images/binary_trees/bst_27.png](images/binary_trees/bst_27.png)

And that’s how we achieve our goal of printing the book titles in alphabetical order. Note that tree traversal is O(N), since by definition, traversal visits all N nodes of the tree.

## Wrapping Up

The binary search tree is a powerful node-based data structure that provides order maintenance, while also offering fast search, insertion, and deletion. It’s more complex than its linked list cousin, but it offers tremendous value.

However, the binary search tree is just one type of tree. Trees are of many different kinds, and each type brings unique advantages to specialized situations. In the next chapter, we’re going to discover another tree that will bring unique speed advantages to a specific, but common, scenario.

## Exercises

The following exercises provide you with the opportunity to practice with binary search trees. The solutions to these exercises are found in the section [​*Chapter 15*​](#f_0220.xhtml_binary.trees.solutions).

1.  Imagine you were to take an empty binary search tree and insert the following sequence of numbers in this order: [1, 5, 9, 2, 4, 10, 6, 3, 8].

    Draw a diagram showing what the binary search tree would look like. Remember, the numbers are being inserted in the order presented here.

2.  If a well-balanced binary search tree contains 1,000 values, what is the maximum number of steps it would take to search for a value within it?

3.  Write an algorithm that finds the greatest value within a binary search tree.

4.  In the text, I demonstrated how to use inorder traversal to print a list of all the book titles. Another way to traverse a tree is known as preorder traversal. Here’s the code for it as applied to our book app:

    | ​  | ​**function**​ traverseAndPrint(node) { |
    | ​  | ​**if**​ (!node) { ​**return**​; } |
    | ​  |  |
    | ​  | console.log(node.value); |
    | ​  | traverseAndPrint(node.leftChild); |
    | ​  | traverseAndPrint(node.rightChild); |
    | ​  | } |

    For the example tree in the text (the one with “Moby Dick” and the other book titles), write out the order in which the book titles are printed with preorder traversal. As a reminder, here’s the example tree:

    ![images/binary_trees/bst_26.png](images/binary_trees/bst_26.png)
5.  Yet another form of traversal is called postorder traversal. Here’s the code as applied to our book app:

    | ​  | ​**function**​ traverseAndPrint(node) { |
    | ​  | ​**if**​ (!node) { ​**return**​; } |
    | ​  |  |
    | ​  | traverseAndPrint(node.leftChild); |
    | ​  | traverseAndPrint(node.rightChild); |
    | ​  | console.log(node.value); |
    | ​  | } |

    For the example tree in the text (which also appears in the previous exercise), write out the order in which the book titles are printed with postorder traversal.

Copyright © 2024, The Pragmatic Bookshelf.

# Chapter 16Keeping Your Priorities Straight with Heaps

Now that we’ve discovered the tree, we’ve unlocked many new data structures. In the previous chapter, we focused specifically on the binary search tree, but there are many other types of trees as well. Like all data structures, each type of tree comes with its own benefits and drawbacks, and the trick is knowing which one to harness in a specific situation.

In this chapter we’ll explore the heap, a type of tree data structure that has special powers that can be leveraged for specific scenarios, in particular when we want to constantly keep tabs on the greatest or least data element in a dataset.

To appreciate what a heap can do, let’s take a look at a completely different data structure: ...

## Priority Queues

You learned about [​*Queues*​](#f_0092.xhtml_sect.queues), and discovered that the queue is a list in which items are processed first in, first out (FIFO). Essentially, this means that data is inserted only at the end of the queue, and data is accessed and removed only from the front of the queue. In accessing the queue’s data, we give precedence to the order in which the data was inserted.

A priority queue is a list whose deletions and access are just like a classic queue but whose insertions are like an ordered array. So we only delete and access data from the front of the priority queue, but when we insert data, we always make sure the data remains sorted in a specific order.

One classic example of where a priority queue is helpful is an application that manages the triage system for a hospital emergency room. In the ER, we don’t treat people strictly in the order in which they arrived. Instead, we treat people in the order of the severity of their symptoms. If someone suddenly arrives with a life-threatening injury, that patient will be placed at the front of the queue, even if the person with the flu had arrived hours earlier.

Let’s say our triage system ranked the severity of a patient’s condition on a scale of 1 to 10, with 10 being the most critical. Our priority queue may look like this:

![images/heaps/initial_priority_queue.png](images/heaps/initial_priority_queue.png)

In determining the next patient to treat, we’ll always select the patient at the front of the priority queue since that person’s need is the most urgent. In this case, the next patient we’d treat is Patient C.

If a new patient now arrives with a condition severity of 3, we’ll initially place this patient at the appropriate spot within the priority queue. We’ll call this person Patient E:

![images/heaps/add_e_to_priority_queue.png](images/heaps/add_e_to_priority_queue.png)

The priority queue is an example of an abstract data type—one that can be implemented using other, more fundamental, data structures. One straightforward way we can implement a priority queue is by using an ordered array; that is, we use an array and apply the following constraints:

*   When we insert data, we ensure we always maintain proper order.
*   Data can only be removed from the end of the array. (This will represent the front of the priority queue.)

This approach is straightforward, but now let’s analyze its efficiency.

The priority queue has two primary operations: deletions and insertions.

We saw in Chapter 1, [​*Why Data Structures Matter*​](#f_0013.xhtml_chp.understanding_data_structures), that deleting from the front of an array is O(N) since we have to shift all the data over to fill the gap created at index 0\. However, we’ve cleverly tweaked our implementation so that we consider the end of the array to be the front of the priority queue. This way, we’re always deleting from the end of the array, which is O(1).

With O(1) deletions, our priority queue is in good shape so far. But what about insertions?

You learned that inserting into an ordered array is O(N) since we have to inspect up to all N elements of the array to determine where our new data should go. (And even if we find the correct spot early, we need to then shift all the remaining data over to the right.)

Our array-based priority queue, then, has deletions that are O(1) and insertions that are O(N). If we expect there to be many items in our priority queue, the O(N) insertions may cause some real unwanted drag in our application.

Because of this, computer scientists discovered another data structure that serves as a more efficient foundation for the priority queue. This data structure is the heap.

## Heaps

Heaps are of several different types, but we’re going to focus on the binary heap.

The binary heap is a specific kind of binary tree. As a reminder, a binary tree is a tree where each node has a maximum of two child nodes. (The binary search tree from the last chapter was one specific type of binary tree.)

Now, even binary heaps come in two flavors: the max-heap and the min-heap. We’re going to work with the max-heap for now, but as you’ll see later, the difference between the two is trivial.

Going forward, I’m going to refer to this data structure simply as a heap, even though we’re specifically working with a binary max-heap.

The heap is a binary tree that maintains the following conditions:

*   The value of each node must be greater than each of its descendant nodes. This rule is known as the heap condition.

*   The tree must be complete. (I’ll explain the meaning of this shortly.)

Let’s break down both of these conditions, starting with the heap condition.

### The Heap Condition

The heap condition says that each node’s value must be greater than each and every one of its descendants.

For example, the following tree meets the heap condition since each node is greater than any of its descendants, as shown in the [diagram](#f_0155.xhtml_fig.ch16.basic_heap).

![images/heaps/basic_heap.png](images/heaps/basic_heap.png)

In this example, the root node of 100 has no descendant that is greater than it. Similarly, the 88 is greater than both of its children, and so is the 25.

The following tree isn’t a valid heap, because it doesn’t meet the heap condition:

![images/heaps/invalid_heap.png](images/heaps/invalid_heap.png)

As you can see, the 92 is greater than its parent of 88\. This violates the heap condition.

Note how the heap is structured very differently than the binary search tree. In a binary search tree, each node’s right child is greater than it. In a heap, however, a node never has any descendant that is greater than it. As they say, “A binary search tree doth not a heap make.” (Or something like that.)

We can also construct a heap that has the opposite heap condition, which is each node must contain a smaller value than any of its descendants. Such a heap is known as the min-heap, which I mentioned earlier. We’re going to continue to focus on the max-heap, where each node must be greater than all of its descendants. Ultimately, whether a heap is a max-heap or a min-heap is trivial, as everything else about both heaps is identical; they only have reversed heap conditions. Otherwise, the fundamental idea is the same.

### Complete Trees

Now, let’s get to the second rule of heaps—that the tree needs to be complete.

A complete tree is a tree that is completely filled with nodes; no nodes are missing. So if you read each level of the tree from left to right, all of the nodes are there. However, the bottom row can have empty positions, as long as there aren’t any nodes to the right of these empty positions. This is best demonstrated with examples.

The following tree is complete since each level (meaning, each row) of the tree is completely filled in with nodes:

![images/heaps/complete_tree.png](images/heaps/complete_tree.png)

The following tree is not complete, since there’s an empty position on the third level (and other nodes exist on the third level to the right of that empty position):

![images/heaps/incomplete_tree.png](images/heaps/incomplete_tree.png)

Now, the next tree is actually considered complete since its empty positions are limited to the bottom row and there aren’t any nodes found to the right of the empty positions:

![images/heaps/also_complete_tree.png](images/heaps/also_complete_tree.png)

A heap, then, is a tree that meets the heap condition and is also complete. Here’s one more example of a heap:

![images/heaps/foundational_heap.png](images/heaps/foundational_heap.png)

This is a valid heap since each node is greater than any of its descendants and the tree is also complete. While it does have some gaps in the bottom row, these gaps are limited to the very right of the tree.

## Heap Properties

Now that you know what a heap is, let’s examine some of its interesting properties.

While the heap condition dictates that the heap be ordered a certain way, this ordering is still useless when it comes to searching for a value within the heap.

For example, let’s say that in the above heap, we want to search for the value 3\. If we start at the root node of 100, should we search among its left or right descendants? In a binary search tree, we’d know that the 3 must be among the 100’s left descendants. In a heap, however, all we know is that the 3 has to be a descendant of the 100 and can’t be its ancestor. But we’d have no idea as to which child node to search next. Indeed, the 3 happens to be among the 100’s right descendants, but it could have also easily been among its left descendants.

Because of this, heaps are said to be weakly ordered as compared to binary search trees. While heaps have some order, as descendants cannot be greater than their ancestors, this isn’t enough order to make heaps worth searching through.

Another property of heaps, that may be obvious by now but is worth calling attention to, is in a heap, the root node will always have the greatest value. (In a min-heap, the root will contain the smallest value.) This will be the key as to why the heap is a great tool for implementing priority queues. In the priority queue, we always want to access the value with the greatest priority. With a heap, we always know that we can find this in the root node. Thus, the root node will represent the item with the highest priority.

The heap has two primary operations: inserting and deleting. As we noted, searching within a heap would require us to inspect each node, so search isn’t an operation usually implemented in the context of heaps. (A heap can also have an optional read operation, which would simply look at the value of the root node.)

Before we move on to how the heap’s primary operations work, let me define one more term, since it’ll be used heavily in the upcoming algorithms.

The heap has something called a last node. A heap’s last node is the rightmost node in its bottom level.

Take a look at the [heap](#f_0156.xhtml_fig.ch16.lastNode).

![images/heaps/last_node.png](images/heaps/last_node.png)

In this heap, the 3 is the last node since it’s the rightmost node in the bottom row.

Next, let’s get into the heap’s primary operations.

## Heap Insertion

To insert a new value into the heap, we perform the following algorithm:

1.  We create a node containing the new value and insert it at the next available rightmost spot in the bottom level. Thus, this value becomes the heap’s last node.

2.  Next, we compare this new node with its parent node.

3.  If the new node is greater than its parent node, we swap the new node with the parent node.

4.  We repeat Step 3, effectively moving the new node up through the heap, until the new node has a parent whose value is greater than it.

Let’s see this algorithm in action. Here’s what would happen if we were to insert a 40 into the heap.

Step 1: We add the 40 as the heap’s last node:

Note that doing the following would have been incorrect:

Placing the 40 as ...

## Looking for the Last Node

While the insertion algorithm seems straightforward, there’s one little snag. The first step has us place the new value as the heap’s last node. But this begs the question: how do we find the spot that will be the last node?

Let’s take a look again at the heap before we inserted the 40:

![images/heaps/foundational_heap.png](images/heaps/foundational_heap.png)

We know by looking at the diagram that to make the 40 into the last node, we’d make it the right child of the 8, as that’s the next available spot in the bottom row.

But a computer doesn’t have eyeballs and doesn’t see the heap as a bunch of rows. All it sees is the root node, and it can follow links to child nodes. So how do we create an algorithm for the computer to find the spot for the new value?

Take our example heap. When we start at the root node of 100, do we tell the computer to look among the 100’s right descendants to find the next available spot for the new last node?

While it’s true that in our example heap the next available spot is among the 100’s right descendants, take a look at the following alternative heap:

![images/heaps/last_node_on_left_side.png](images/heaps/last_node_on_left_side.png)

In this heap, the next available spot for the new last node would be the 88’s right child, which is among the 100’s left descendants.

Essentially, then, just as it’s impossible to search through a heap, it’s impossible to efficiently find the heap’s last node (or next available spot to hold a new last node) without having to inspect each and every node.

So how do we find the next available node? I’ll explain this later on, but for now, let’s call this issue the problem of the last node. I promise we’ll come back to it.

In the meantime, let’s explore the heap’s other primary operation, which is deletion.

## Heap Deletion

The first thing to know about deleting a value from a heap is that we only ever delete the root node. This is right in line with the way a priority queue works, in that we only access and remove the highest-priority item.

The algorithm for deleting the root node of a heap is as follows:

1.  Move the last node into where the root node was, effectively removing the original root node.

2.  Trickle the root node down into its proper place. I’ll explain how trickling down works shortly.

Let’s say we’re going to remove the root node from the [heap](#f_0159.xhtml_fig.ch16.foundational_heap).

![images/heaps/foundational_heap.png](images/heaps/foundational_heap.png)

In this example, the root node is the 100\. To delete it, we overwrite the root by placing the last node there instead. In this case, the last node is the 3\. So we move the 3 and place it where the 100 was:

![images/heaps/move_3_to_root.png](images/heaps/move_3_to_root.png)

Now, we can’t leave the heap as is, because the heap condition has been violated since the 3 is currently less than some (actually, most) of its descendants. To make things right again, we need to trickle the 3 down until its heap condition has been restored.

Trickling down is a tad more complex than trickling up since each time we trickle a node down, we have two possible directions as to where we’ll trickle it down; that is, we can either swap it with its left child or its right child. (When trickling up, on the other hand, each node has only one parent to swap with.)

Here’s the algorithm for trickling down. For the sake of clarity, we’re going to call the node we’re trickling the “trickle node.” (Sounds gross, I know.)

1.  We check both children of the trickle node and see which one is larger.

2.  If the trickle node is smaller than the larger of the two child nodes, we swap the trickle node with that larger child.

3.  We repeat Steps 1 and 2 until the trickle node has no children who are greater than it.

Let’s see this in action.

Step 1: The 3, which is the trickle node, currently has two children, the 88 and the 25\. The 88 is larger of the two, and since the 3 is smaller than the 88, we swap the trickle node with the 88:

![images/heaps/swap_3_with_88.png](images/heaps/swap_3_with_88.png)

Step 2: The trickle node now has two new children, the 87 and the 16. The 87 is the larger one, and it’s greater than the trickle node. So we swap the trickle node with the 87:

![images/heaps/swap_3_with_87.png](images/heaps/swap_3_with_87.png)

Step 3: The trickle node’s children are currently the 86 and the 50. The 86 is the larger of the two, and it’s also greater than the trickle node, so we swap the 86 with the trickle node:

![images/heaps/swap_3_with_86.png](images/heaps/swap_3_with_86.png)

At this point, the trickle node has no children that are greater than it. (In fact, it has no children at all.) So we’re done, as the heap condition has been restored.

The reason why we always swap the trickle node with the greater of its two children is because if we swap it the with the smaller one, we’d end up violating the heap condition immediately. Watch what happens when we try to swap the trickle node with a smaller child.

Let’s start again with the trickle node of 3 as our root:

![images/heaps/move_3_to_root.png](images/heaps/move_3_to_root.png)

Let’s swap the 3 with the 25, which is the smaller of the children:

![images/heaps/swap_3_with_25.png](images/heaps/swap_3_with_25.png)

We’ve now placed the 25 in a situation where it is a parent of the 88\. Since the 88 is greater than its parent, the heap condition has been broken.

Like insertion, the time complexity of deletion from a heap is O(log N), as we have to trickle a node from the root down through all log(N) levels of the heap.

## Heaps vs. Ordered Arrays

Now that you know the efficiency of heaps, let’s see why it’s a great choice for implementing priority queues.

Here’s a side-by-side comparison of ordered arrays versus heaps:

|  | Ordered Array | Heap |
| --- | --- | --- |
| Insertion | O(N) | O(log N) |
| Deletion | O(1) | O(log N) |

At first glance, it seems that it’s a wash. Ordered arrays are slower than heaps when it comes to insertion but faster than heaps for deletion.

However, heaps are considered to be the better choice, and here’s why.

While O(1) is extremely fast, O(log N) is still very fast. And O(N), by comparison, is slow. With this in mind, we can rewrite the earlier table this way:

|  | Ordered Array | Heap |
| --- | --- | --- |
| Insertion | Slow | Very fast |
| Deletion | Extremely fast | Very fast |

In this light, it becomes clearer as to why the heap is considered the better choice. We’d rather use a data structure that is consistently very fast than a data structure that is sometimes extremely fast and sometimes slow.

It’s worth pointing out that priority queues generally perform insertions and deletions in about equal proportion. Think about the emergency room example, where we expect to treat everyone who comes in. So we want both our insertions and deletions to be fast. If either operation is slow, our priority queue will be inefficient.

With a heap, then, we ensure that both of the priority queue’s primary operations—insertion and deletion—perform at a very fast clip.

## The Problem of the Last Node…Again

While the heap deletion algorithm seems straightforward, it once again raises the problem of the last node.

I explained that the first step of deletion requires us to move the last node and turn it into the root node. But how do we find the last node in the first place?

Before we solve the problem of the last node, let’s first explore why insertion and deletion are so dependent on the last node anyway. Why couldn’t we insert new values elsewhere in the heap? And why, when deleting, can’t we replace the root node with some other node other than the last node?

Now, if you think about it, you’ll realize that if we were to use other nodes, the heap would become incomplete. But this begs the next question: why is completeness important for the heap?

The reason why completeness is important is because we want to ensure our heap remains well balanced.

To see this clearly, let’s take another look at insertion. Let’s say we have the following heap:

![images/heaps/small_heap.png](images/heaps/small_heap.png)

If we want to insert a 5 into this heap, the only way to keep the heap well balanced is by making the 5 the last node—in this case, making it a child of the 10:

![images/heaps/make_5_last_node.png](images/heaps/make_5_last_node.png)

Any alternative to this algorithm would cause imbalance. Say, in an alternative universe, the algorithm was to insert the new node into the bottom leftmost node, which we could easily find by traversing the left children until we hit the bottom. This would make the 5 a child of the 15:

![images/heaps/make_5_child_of_15.png](images/heaps/make_5_child_of_15.png)

Our heap is now somewhat imbalanced, and it’s easy to see how much more imbalanced it would become if we kept inserting new nodes at the bottom leftmost spot.

Similarly, when deleting from a heap, we always turn the last node into the root because, otherwise, the heap can become imbalanced. Take again our example heap:

![images/heaps/small_heap.png](images/heaps/small_heap.png)

If, in our alternative universe, we always moved the bottom rightmost node into the root position, the 10 would become the root node, and we’d end up with an imbalanced heap with a bunch of left descendants and zero right descendants.

Now, the reason why this balance is so important is because it’s what allows us to achieve O(log N) operations. In a severely imbalanced tree like the following one, traversing it could take O(N) steps instead:

![images/heaps/imbalanced_heap.png](images/heaps/imbalanced_heap.png)

But this brings us back to the problem of the last node. What algorithm would allow us to consistently find the last node of any heap? (Again, without having to traverse all N nodes.)

And this is where our plot takes a sudden twist.

## Arrays as Heaps

Because finding the last node is so critical to the heap’s operations, and because we want to make sure that finding the last node is efficient, heaps are usually implemented using arrays.

While until now we always assumed that every tree consists of independent nodes connected to each other with links (just like a linked list), you’ll now see that we can also use an array to implement a heap. The heap itself can be an abstract data type that really uses an array under the hood.

The [diagram](#f_0162.xhtml_fig.ch16.heap_as_array) shows how an array is used to store the values of a heap.

The way this works is that we assign each node to an index within the array. In this diagram, the index of each node is found in a square below the node. If you look carefully, you’ll see that we assign the index of each node according to a specific pattern.

![images/heaps/heap_as_array.png](images/heaps/heap_as_array.png)

The root node is always stored at index 0\. We then move down a level and go from left to right, assigning each node to the next available index in the array. So on the second level, the left node (88) becomes index 1, and the right node (25) becomes index 2\. When we reach the end of a level, we move down to the next level and repeat this pattern.

Now, the reason why we’re using an array to implement the heap is because it solves the problem of the last node. How?

When we implement the heap in this fashion, the last node will always be the final element of the array. Since we move top-down and left to right when assigning each value to the array, the last node will always be the final value in the array. In the previous example, you can see that the 3, which is the last node, is the last value in the array.

Because the last node will always be found at the end of the array, it becomes trivial to find the last node: we just need to access the final element. Additionally, when we insert a new node into the heap, we do so at the end of the array to make it the last node.

Before we get into the other details of how an array-based heap works, we can already begin to code its basic structure. Here’s the beginning of our heap implementation in JavaScript:

| ​  | ​**class**​ Heap { |
| ​  | ​**constructor**​() { |
| ​  | ​**this**​.data = []; |
| ​  | } |
| ​  |  |
| ​  | rootNode() { |
| ​  | ​**return**​ ​**this**​.data[0]; |
| ​  | } |
| ​  |  |
| ​  | lastNode() { |
| ​  | ​**return**​ ​**this**​.data[​**this**​.data.length - 1]; |
| ​  | } |

| ​  | } |

As you can see, we initialize the heap as an empty array. We have a rootNode method, which returns the first item of this array, and we also have a lastNode method that returns the last value of this array.

### Traversing an Array-Based Heap

As you’ve seen, the heap’s insertion and deletion algorithms require us to be able to trickle our way through the heap. Trickling, in turn, requires us to be able to traverse the heap by accessing a node’s parent or children. But how do we move from node to node when all the values are merely stored in an array? Traversing a heap would have been straightforward if we could have simply followed each node’s links. But now that the heap is an array under the hood, how do we know which nodes are connected to each other?

This has an interesting solution. It turns out that when we assign the indexes of the heap’s nodes according to the pattern described earlier, the following traits of a heap are always true:

*   To find the left child of any node, we can use the formula (index * 2) + 1.
*   To find the right child of any node, we can use the formula (index * 2) + 2.

Take another look at the previous diagram and focus on the 16, which is at index 4\. To find its left child, we multiply its index (4) by 2 and add 1, which yields 9\. This means that index 9 is the left child of the node at index 4.

Similarly, to find the right child of index 4, we multiply the 4 by 2 and add 2, which yields 10\. This means that index 10 is the right child of index 4.

Because these formulas always work, we’re able to treat our array as a tree.

Let’s add these two methods to our Heap class:

| ​  | leftChildIndex(index) { |
| ​  | ​**return**​ (index * 2) + 1; |
| ​  | } |
| ​  |  |
| ​  | rightChildIndex(index) { |
| ​  | ​**return**​ (index * 2) + 2; |
| ​  | } |

Each of these methods accepts an index within the array and returns the left or right child index, respectively.

Here’s another important trait of array-based heaps:

*   To find a node’s parent, we can use the formula Math.floor((index - 1) / 2).

Note that this formula uses floor division, meaning we throw away any numbers beyond the decimal point. For example, Math.floor(3 / 2) returns 1, rather than the more accurate 1.5.

Again, in our example heap, focus on index 4\. If we take that index, subtract 1, and then divide by 2, we get 1\. And as you can see in the diagram, the parent of the node at index 4 is found at index 1.

So now we can add another method to our Heap class:

| ​  | parentIndex(index) { |
| ​  | ​**return**​ Math.floor((index - 1) / 2); |
| ​  | } |

This method accepts an index and calculates the index of its parent node.

### Code Implementation: Heap Insertion

Now that we have the essential elements of our Heap in place, let’s implement the insertion algorithm:

| ​  | insert(value) { |
| ​  | ​**this**​.data.push(value); |
| ​  | ​**let**​ newNodeIndex = ​**this**​.data.length - 1; |
| ​  |  |
| ​  | ​**while**​ (newNodeIndex > 0 |
| ​  | && (​**this**​.data[newNodeIndex] > ​**this**​.data[​**this**​.parentIndex(newNodeIndex)])) { |
| ​  | ​**const**​ parentIndex = ​**this**​.parentIndex(newNodeIndex); |
| ​  | [​**this**​.data[parentIndex], ​**this**​.data[newNodeIndex]] = |
| ​  | [​**this**​.data[newNodeIndex], ​**this**​.data[parentIndex]]; |
| ​  |  |
| ​  | newNodeIndex = parentIndex; |
| ​  | } |
| ​  | } |

As usual, let’s break this thing down.

Our insert method accepts the value we’re inserting into our heap. The first thing we do is make this new value the last node by adding it to the very end of the array:

| ​  | ​**this**​.data.push(value); |

Next, we keep track of the index of the new node, as we’ll need it later. Right now, the index is the last index in the array:

| ​  | ​**let**​ newNodeIndex = ​**this**​.data.length - 1; |

Next, we trickle up the new node to its proper place using a while loop:

| ​  | ​**while**​ (newNodeIndex > 0 |
| ​  | && (​**this**​.data[newNodeIndex] > ​**this**​.data[​**this**​.parentIndex(newNodeIndex)])) { |

This loop runs as long as two conditions are met. The main condition is that the new node is greater than its parent node. We also make a condition that the new node must have an index greater than 0, as funny things can happen if we try to compare the root node with its nonexistent parent.

Each time this loop runs, we swap the new node with its parent node since the new node is currently greater than the parent:

| ​  | ​**const**​ parentIndex = ​**this**​.parentIndex(newNodeIndex); |
| ​  | [​**this**​.data[parentIndex], ​**this**​.data[newNodeIndex]] = |
| ​  | [​**this**​.data[newNodeIndex], ​**this**​.data[parentIndex]]; |

We also then update the index of the new node appropriately:

| ​  | newNodeIndex = parentIndex; |

Since this loop only runs while the new node is greater than its parent, the loop ends once the new node is in its proper place.

### Code Implementation: Heap Deletion

We’ll next look at an implementation of deleting an item from a heap. We named the method pop since the term pop implies a focus on returning the deleted value to be used by other code, such as in a priority queue (as we’ll see soon). We’re not merely trying to eliminate the root value; we also want to pass that value along to other code to be processed.

The main method is the pop method, but to make the code simpler, we’ve created two helper methods, hasGreaterChild and findLargerChildIndex.

Here goes:

| ​  | pop() { |
| ​  | ​**if**​ (​**this**​.data.length === 1) { |
| ​  | ​**const**​ valueToDelete = ​**this**​.rootNode(); |
| ​  | ​**this**​.data = []; |
| ​  | ​**return**​ valueToDelete; |
| ​  | } |
| ​  |  |
| ​  | ​**const**​ valueToDelete = ​**this**​.rootNode(); |
| ​  | ​**this**​.data[0] = ​**this**​.data.pop(); |
| ​  | ​**let**​ trickleNodeIndex = 0; |
| ​  |  |
| ​  | ​**while**​ (​**this**​.hasGreaterChild(trickleNodeIndex)) { |
| ​  | ​**const**​ largerChildIndex = ​**this**​.findLargerChildIndex(trickleNodeIndex); |
| ​  |  |
| ​  | [​**this**​.data[trickleNodeIndex], ​**this**​.data[largerChildIndex]] = |
| ​  | [​**this**​.data[largerChildIndex], ​**this**​.data[trickleNodeIndex]]; |
| ​  |  |
| ​  | trickleNodeIndex = largerChildIndex; |
| ​  | } |
| ​  |  |
| ​  | ​**return**​ valueToDelete; |
| ​  | } |
| ​  |  |
| ​  | hasGreaterChild(index) { |
| ​  | ​**return**​ ((​**this**​.leftChildIndex(index) < ​**this**​.data.length |
| ​  | && ​**this**​.data[​**this**​.leftChildIndex(index)] > ​**this**​.data[index]) |
| ​  | &#124;&#124; (​**this**​.rightChildIndex(index) < ​**this**​.data.length |
| ​  | && ​**this**​.data[​**this**​.rightChildIndex(index)] > ​**this**​.data[index])); |
| ​  | } |
| ​  |  |
| ​  | findLargerChildIndex(index) { |
| ​  | ​**if**​ (!​**this**​.data[​**this**​.rightChildIndex(index)]) { |
| ​  | ​**return**​ ​**this**​.leftChildIndex(index); |
| ​  | } |
| ​  |  |
| ​  | ​**if**​ (​**this**​.data[​**this**​.rightChildIndex(index)] > |
| ​  | ​**this**​.data[​**this**​.leftChildIndex(index)]) { |
| ​  | ​**return**​ ​**this**​.rightChildIndex(index); |
| ​  | } ​**else**​ { |
| ​  | ​**return**​ ​**this**​.leftChildIndex(index); |
| ​  | } |
| ​  | } |

Let’s first dive into the pop method.

The pop method doesn’t accept any arguments, since the only node we ever delete is the root node. Here’s how the method works.

First, we handle the case where the heap only contains one element:

| ​  | ​**if**​ (​**this**​.data.length === 1) { |
| ​  | ​**const**​ valueToDelete = ​**this**​.rootNode(); |
| ​  | ​**this**​.data = []; |
| ​  | ​**return**​ valueToDelete; |
| ​  | } |

Since there only is a root node, that becomes the value we’ll be deleting, which we store in a variable appropriately named valueToDelete. We wipe this.data clean by making it point to an empty array, and we return the valueToDelete.

The rest of the pop method handles cases where the heap contains more than one element.

First, we save the value we’re going to delete so we can return it at the end of the method:

| ​  | ​**const**​ valueToDelete = ​**this**​.rootNode(); |

Next, we remove the last value from the array and make it the first value:

| ​  | ​**this**​.data[0] = ​**this**​.data.pop(); |

This simple line effectively deletes the original root node, as we’re overwriting the root node’s value with the last node’s value.

Next, we need to trickle the new root node down to its proper place. We called this the trickle node earlier, and our code reflects this.

Before we start the actual trickling, we keep track of the trickle node’s index, as we’ll need it later. Currently, the trickle node is at index 0:

| ​  | ​**let**​ trickleNodeIndex = 0; |

We then use a while loop to execute the trickle-down algorithm. The loop runs as long as the trickle node has any children that are greater than it:

| ​  | ​**while**​ (​**this**​.hasGreaterChild(trickleNodeIndex)) { |

This line uses the hasGreaterChild method, which returns whether a given node has any children who are greater than that node.

Within this loop, we first find the index of the greater of the trickle node’s children:

| ​  | ​**const**​ largerChildIndex = ​**this**​.findLargerChildIndex(trickleNodeIndex); |

This line uses the method findLargerChildIndex, which returns the index of the trickle node’s greater child. We store this index in a variable called largerChildIndex.

Next, we swap the trickle node with its greater child:

| ​  | [​**this**​.data[trickleNodeIndex], ​**this**​.data[largerChildIndex]] = |
| ​  | [​**this**​.data[largerChildIndex], ​**this**​.data[trickleNodeIndex]]; |

We update the index of the trickle node, which will be the index it was just swapped with:

| ​  | trickleNodeIndex = largerChildIndex; |

Finally, we return the value of the node we deleted from the heap:

| ​  | ​**return**​ valueToDelete; |

### Alternate Heap Implementations

Our heap implementation is now complete. It’s worth noting that while we did use an array to implement the heap under the hood, it is possible to implement a heap using linked nodes as well. (This alternative implementation uses a different trick to solve the problem of the last node, one that involves binary numbers.)

However, the array implementation is the more common approach, so that’s what I presented here. It’s also interesting to see how an array can be used to implement a tree.

Indeed, it’s possible to use an array to implement any sort of binary tree, such as the binary search tree from the previous chapter. However, the heap is the first case of a binary tree where an array implementation provides an advantage, as it helps us find the last node easily.

## Heaps as Priority Queues

Now that you understand how heaps work, we can circle back to our old friend, the priority queue.

Again, the primary function of a priority queue is to allow us immediate access to the highest-priority item in the queue. In our emergency room example, we want to first address the person with the most serious problem.

It’s for this reason that a heap is a natural fit for priority queue implementations. The heap gives us immediate access to the highest-priority item, which can always be found at the root node. Each time we take care of the highest-priority item (and then remove it from the heap), the next-highest item floats to the top of the heap and is on deck to be addressed next. And the heap accomplishes this while ...

## Wrapping Up

So far, we’ve seen how different types of trees can optimize different types of problems. Binary search trees kept search fast while minimizing the cost of insertions, and heaps were the perfect tool for building priority queues.

In the next chapter, we’ll explore another tree that’s used to power some of the most common text-based operations you use on a day-to-day basis.

## Exercises

The following exercises provide you with the opportunity to practice with heaps. The solutions to these exercises are found in the section [​*Chapter 16*​](#f_0221.xhtml_heaps.solutions).

1.  Draw what the following heap would look like after we insert the value 11 into it:

    ![images/heaps/exercise_1.png](images/heaps/exercise_1.png)
2.  Draw what the previous heap would look like after we delete the root node.

3.  Imagine you’ve built a brand-new heap by inserting the following numbers into the heap in this particular order: 55, 22, 34, 10, 2, 99, 68\. If you then pop them from the heap one at a time and insert the numbers into a new array, in what order would the numbers now appear?

Copyright © 2024, The Pragmatic Bookshelf.

# Chapter 17It Doesn’t Hurt to Trie

Did you ever wonder how your smartphone’s autocomplete feature works? Autocomplete is the feature you see when you start typing “catn” and your phone suggests that the word you’re about to type is either “catnip” or “catnap”. (Yes, I text my friends about catnip all the time.)

For this to work, your phone has access to an entire dictionary of words. But what data structure are these words stored in?

Let’s imagine, for a moment, that all the words in the English language are stored within an array. If the array were unsorted, we’d have to search every word in the dictionary to find all words that start with “catn”. This is O(N), and a very slow operation considering that N is a pretty large number in this case, ...

## Tries

The trie is a kind of tree that’s ideal for text-based features such as autocomplete. Before we get into how the trie works, though, let’s first address its pronunciation.

In my (unasked for) opinion, the trie is one of the most unfortunately named data structures out there. The word trie is derived from the word retrieval. So technically, it should be pronounced “tree.” But since that would be confused with the word tree, which is the general term for all tree-based data structures, most people pronounce trie as “try.” Some resources refer to this same data structure as the prefix tree or the digital tree, but trie, amazingly, remains the most popular name. So there you have it.

Here’s one last comment before we dive into the details. The trie is not as well documented as the other data structures in this book, and many different resources implement the trie in slightly different ways. I’ve chosen a particular implementation that I find to be the most straightforward and understandable, but you’ll find other implementations out there. In any case, the general ideas behind most of the implementations remain the same.

### The Trie Node

Like most other trees, the trie is a collection of nodes that point to other nodes. However, the trie is not a binary tree. Whereas a binary tree doesn’t allow any node to have more than two child nodes, a trie node can have any number of child nodes.

In our implementation, each trie node contains a hash table, where the keys are English characters and the values are other nodes of the trie. Take a look at the following diagram:

![images/tries/abc_trie.png](images/tries/abc_trie.png)

Here, the root node contains a hash table with the keys "a", "b", and "c". The values are other trie nodes, which are the children of this node. These children also contain hash tables, which will in turn point to their children. (For now, we left the children’s hash tables empty, but they’ll contain data in future diagrams.)

The implementation of the actual trie node itself is very simple. Here is our JavaScript version of the TrieNode class:

| ​  | ​**class**​ TrieNode { |
| ​  | ​**constructor**​() { |
| ​  | ​**this**​.children = {}; |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | ​**export**​ ​**default**​ TrieNode; |

As you can see, the TrieNode just contains a hash table.

If we print (to the console) the data from our root node in the previous example, we’ll get something along these lines:

| ​  | { |
| ​  | a: TrieNode { }, |
| ​  | b: TrieNode { }, |
| ​  | c: TrieNode { } |
| ​  | } |

Again, in this hash table, the keys are individual character strings, and the values are instances of other TrieNodes.

### The Trie Class

To fully create our trie, we’ll also need a separate Trie class, which will keep track of the root node:

| ​  | ​**import**​ TrieNode ​**from**​ ​*'./trie_node.js'*​; |
| ​  |  |
| ​  | ​**class**​ Trie { |
| ​  | ​**constructor**​() { |
| ​  | ​**this**​.root = ​**new**​ TrieNode(); |
| ​  | } |

| ​  | } |

This class keeps track of a this.root variable that points to the root node. In this implementation, when we create a new Trie, it begins with an empty TrieNode as its root.

As we progress through this chapter, we’re going to add our trie operation methods to this Trie class as well.

## Storing Words

Now, the point of our trie is to store words. Let’s see how the following trie stores the words, “ace”, “bad”, and “cat”, as shown in the [diagram](#f_0168.xhtml_fig.ch17.ace_bad_cat).

![images/tries/ace_bad_cat.png](images/tries/ace_bad_cat.png)

This trie stores the three words by turning each character of each word into its own trie node. If you start with the root node and follow its "a" key, for example, it points to a child node containing a key of "c". The "c" key, in turn, points to a node that contains a key of "e". When we string these three characters together, we get the word "ace".

With this pattern, you can see how the trie also stores the words "bad" and "cat".

You’ll note that the final characters in these words have children nodes of their own. If you look at the "e" node from the word "ace", for example, you can see that the "e" points to a child node that contains a hash table with a key of "*", an asterisk. (The value doesn’t actually matter, so it can simply be null.) This indicates we’ve reached the end of a word, and that "ace", therefore, is a complete word. The need for this "*" key will become more apparent shortly.

Now, here’s where tries become even more interesting. Let’s say we want to also store the word “act”. To do this, we keep the existing "a" and "c" keys, but we add one new node containing the key of "t". Look at the following diagram:

![images/tries/add_act.png](images/tries/add_act.png)

As you can see, the bolded node’s hash table now contains two children nodes, an "e" and a "t". By doing this, we indicate that both "ace" and "act" are valid dictionary words.

To make things easier to visualize going forward, we’re going to represent our tries using a simpler diagram. Here’s the same trie using this new format:

![images/tries/no_hash.png](images/tries/no_hash.png)

In this diagram style, we place each hash table key next to an arrow pointing to its child node.

### The Need for the Asterisk

Let’s say we want to store the words “bat” and “batter” in a trie. This is an interesting case since the word “batter” actually contains the word “bat”. Here’s how we handle this:

![images/tries/bat_and_batter.png](images/tries/bat_and_batter.png)

The first "t" points to a node that has two keys. One key is an "*" key (with a null value), while the other is a "t" whose value points to another node. This indicates that "bat" is itself a word even though it’s also a prefix of the longer word "batter".

Note that in this diagram, we’re not using classic hash table syntax anymore but instead using a condensed syntax to save space. We’ve used curly braces to indicate that the node contains a hash table. However, the {*, "t"} is not a key-value pair but simply two keys. The "*" key has a null value, and the "t" key has the next node as its value.

This is why those "*"s are critical. We need them to indicate when parts of a word are also words themselves.

Let’s bring this all together with a more complex example. Here’s a trie that contains the words “ace”, “act”, “bad”, “bake”, “bat”, “batter”, “cab”, “cat”, “catnap”, and “catnip”:

![images/tries/foundational_trie.png](images/tries/foundational_trie.png)

Tries used in real applications may contain thousands of words. If they don’t contain the entire English language, they at least contain the most common words.

To build our autocomplete feature, let’s first analyze the basic trie operations.

## Trie Search

The most classic trie operation is search—namely, determining whether a string is found in the trie. Search has two flavors: we can search to see whether the string is a complete word, or we can search to see whether the string is at least a word prefix (that is, the beginning of a word). These two versions are similar, but we’ll implement the latter one, where our search will look for prefixes. This search will end up finding complete words as well since a complete word is at least as good as a prefix.

The algorithm for prefix search performs the following steps (they’ll become clearer when we walk though an example that follows):

1.  We establish a variable called currentNode. At the beginning of our algorithm, this points to the root ...

## The Efficiency of Trie Search

The great thing about trie search is that it’s incredibly efficient.

Let’s analyze the number of steps it takes.

In our algorithm, we focus on each character of our search string one at a time. As we do so, we use each node’s hash table to find the appropriate child node in one step. As you know, a hash table lookup takes just O(1) time. It turns out, then, that our algorithm takes as many steps as there are characters in our search string.

This can be much faster than using binary search on an ordered array. Binary search is O(log N), with N being the number of words in our dictionary. Trie search, on the other hand, takes only as many steps as the number of characters in our search term. For a word like “cat”, ...

## Trie Insertion

Inserting a new word into a trie is similar to searching for an existing word. We first search to see if the word already exists in the trie. If it doesn’t, we insert the new word.

Here’s how the algorithm goes:

1.  We establish a variable called currentNode. At the beginning of our algorithm, this points to the root node.

2.  We iterate over each character of our search string. Here, our search string represents the new word we’re inserting. We call it a search string since we’re also searching whether the string already exists in the trie.

3.  As we point to each character of our search string, we look to see if the currentNode has a child with that character as a key.

4.  If it does, we update the currentNode to become that child node, and ...

## Building Autocomplete

We’re just about ready to build a real autocomplete feature. To make this a tad easier, let’s first build a slightly simpler function that we’ll use to help us with this feature.

### Collecting All the Words

The next method we’re going to add to our Trie class is a method that returns an array of all the words in the trie. Now, it’s rare that we’d actually want to list the entire dictionary. However, we’re going to allow this method to accept any node of the trie as an argument so that it can list all the words that start from that node.

The following method, called collectAllWords, collects a list of all the trie’s words starting from a particular node:

| ​  | collectAllWords(words, node=​**null**​, word=​*''*​) { |
| ​  | ​**const**​ currentNode ... |

## Completing Autocomplete

We’re finally ready to implement our autocomplete feature. In fact, we’ve pretty much done all the legwork already. All we need to do is put the pieces together.

Here’s a basic autocomplete method that we can drop into our Trie class:

| ​  | autocomplete(prefix) { |
| ​  | ​**const**​ currentNode = ​**this**​.search(prefix); |
| ​  |  |
| ​  | ​**if**​ (!currentNode) { ​**return**​ ​**null**​; } |
| ​  |  |
| ​  | ​**return**​ ​**this**​.collectAllWords([], currentNode); |
| ​  | } |

Yes, that’s it. By using our search method and collectAllWords method together, we can autocomplete any prefix. Here’s how this works.

The autocomplete method accepts the prefix parameter, which is the string of characters the user begins typing in.

First, we search the trie for the existence of the prefix. If the search method doesn’t find the prefix in the trie, the search method returns null, and so our method does as well.

However, if the prefix is found in the trie, the search method returns the node in the trie that represents the final character in the prefix. We noted earlier that we could have simply had the search method return true once it finds the word. The reason why we had it return the final node was so that we could use the search method to help us with the autocomplete feature.

Our autocomplete method continues by calling the collectAllWords method on the node returned by the search method. This finds and collects all words that stem from that final node, which represents all the complete words that can be appended to the original prefix to form a word.

Our method finally returns an array of all possible endings to the user’s prefix, which we could then display to the user as possible autocomplete options.

## Tries with Values: A Better Autocomplete

If we think about it, a good autocomplete feature isn’t necessarily going to display every possible word the user might be intending to type. Showing, say, sixteen options would be overwhelming to the user, so we’d rather show just the most popular words from the available list.

For example, if the user starts typing “bal”, the user might be intending to type “ball”, “bald”, or “balance”. Now, it’s also possible that the user is typing the obscure word “balter” (which means to dance clumsily, if you wanted to know). However, odds are that “balter” is not the intended word, since it’s not a common word.

To display the most popular word options, we somehow need to store the word popularity data in our trie ...

## Wrapping Up

We’ve now covered three types of trees: binary search trees, heaps, and tries. There are many other types of trees as well, such as AVL trees, red black trees (covered in Volume 2 of this book), 2-3-4 trees, and plenty of others. Each tree has unique traits and behaviors that can be leveraged for specific situations. I encourage you to learn more about these various trees, but for now you have a taste for how different trees can solve different problems.

It’s now time for the final data structure of the book. Everything you’ve learned about trees will help you understand graphs. Graphs are helpful in so many different situations, and that’s why they’re so popular. So let’s dive in.

## Exercises

The following exercises provide you with the opportunity to practice with tries. The solutions to these exercises are found in the section [​*Chapter 17*​](#f_0222.xhtml_tries.solutions).

1.  List all the words stored in the following trie:

    ![images/tries/exercise_1.png](images/tries/exercise_1.png)
2.  Draw a trie that stores the following words: “get”, “go”, “got”, “gotten”, “hall”, “ham”, “hammer”, “hill”, and “zebra”.

3.  Write a function that traverses each node of a trie and prints each key, including all "*" keys.

4.  Write an autocorrect function that attempts to replace a user’s typo with a correct word. The function should accept a string that represents text a user typed in. If the user’s string is not in the trie, the function should ...

# Chapter 18
Connecting Everything with Graphs

Let’s say we’re building a social network that allows people to be friends with one another. These friendships are mutual, so if Alice is friends with Bob, then Bob is also friends with Alice.

How can we best organize this data?

One basic approach might be to use a two-dimensional array that stores the list of friendships:

| ​  | friendships = [ |
| ​  | [​*"Alice"*​, ​*"Bob"*​], |
| ​  | [​*"Bob"*​, ​*"Cynthia"*​], |
| ​  | [​*"Alice"*​, ​*"Diana"*​], |
| ​  | [​*"Bob"*​, ​*"Diana"*​], |
| ​  | [​*"Elise"*​, ​*"Fred"*​], |
| ​  | [​*"Diana"*​, ​*"Fred"*​], |
| ​  | [​*"Fred"*​, ​*"Alice"*​] |
| ​  | ] |

Here, each subarray containing a pair of names represents a friendship between two people.

Unfortunately, with this approach, there’s no quick way to see who Alice’s friends are. If we look carefully, we can see that Alice is friends with Bob, Diana, and Fred. But for the computer to determine this, it would have to comb through all the relationships in the list since Alice can be present in any of them. This is O(N), which is very slow.

Thankfully, we can do much, much better than this. With a data structure known as a graph, we can find Alice’s friends in just O(1) time.

## Graphs

A graph is a data structure that specializes in relationships, as it easily conveys how data is connected.

Here’s a visualization of our social network, displayed as a graph:

![images/graphs/graph_1.png](images/graphs/graph_1.png)

Each person is represented by a node, and each line indicates a friendship with another person. If you look at Alice, for example, you can see that she is friends with Bob, Diana, and Fred since her node has lines that connect to their nodes.

### Graphs vs. Trees

You might have noticed that graphs look similar to trees, which we’ve dealt with in the past few chapters. Indeed, trees are a type of graph. Both data structures consist of nodes connected to each other.

So what’s the difference between a graph and a tree?

Here’s the deal: while all trees are graphs, not all graphs are trees.

Specifically, for a graph to be considered a tree, it cannot have cycles, and all nodes must be connected. Let’s see what that means.

A graph may have nodes that form what is known as a cycle—that is, nodes that reference each other circularly. In the previous example, Alice is friends with Diana, and Diana is connected to Bob, and Bob is connected…to Alice. These three nodes form a cycle.

Trees, on the other hand, are not “allowed” to have cycles. If a graph has a cycle, then it’s not a tree.

Another characteristic specific to trees is that every node is somehow connected to every other node, even if the connections are indirect. However, it’s possible for a graph to not be fully connected.

See the following graph:

![images/graphs/disconnected_graph.png](images/graphs/disconnected_graph.png)

In this social network, we have two pairs of friends. However, no one from either pair is friends with anyone from the other pair. Additionally, we can see that Vicky has no friends yet, as perhaps she signed up for this social network just minutes ago. With trees, however, there’s never a node that’s disconnected from the rest of the tree.

### Graph Jargon

Graphs have a bit of their own technical jargon. We’re used to calling each piece of data a node, but in “graph-speak,” each node is called a vertex. The lines between nodes, um—vertices, have their own name as well and are called edges. And vertices that are connected by an edge are said to be adjacent to each other. Some computer scientists also refer to adjacent vertices as neighbors.

In our first graph, then, the vertices of Alice and Bob are adjacent to each other since they share an edge.

I mentioned earlier that it’s possible for a graph to have a vertex that isn’t connected at all to other vertices. However, a graph where all the vertices are connected in some way is said to be a connected graph.

### The Bare-Bones Graph Implementation

For the sake of code organization, we’re going to use object-oriented classes to represent our graphs, but it’s worth noting that we can also use a basic hash table (see Chapter 8, [​*Blazing Fast Lookup with Hash Tables*​](#f_0076.xhtml_chp.hashes) ) to represent a rudimentary graph. Here’s a bare-bones implementation of our social network using a hash table:

| ​  | friends = { |
| ​  | ​*"Alice"*​: [​*"Bob"*​, ​*"Diana"*​, ​*"Fred"*​], |
| ​  | ​*"Bob"*​: [​*"Alice"*​, ​*"Cynthia"*​, ​*"Diana"*​], |
| ​  | ​*"Cynthia"*​: [​*"Bob"*​], |
| ​  | ​*"Diana"*​: [​*"Alice"*​, ​*"Bob"*​, ​*"Fred"*​], |
| ​  | ​*"Elise"*​: [​*"Fred"*​], |
| ​  | ​*"Fred"*​: [​*"Alice"*​, ​*"Diana"*​, ​*"Elise"*​] |
| ​  | } |

With a graph, we can look up Alice’s friends in O(1) because we can look up the value of any key in the hash table with one step:

| ​  | friends[​*"Alice"*​] |

This immediately returns the array containing all of Alice’s friends.

## Directed Graphs

In some social networks, relationships are not mutual. For example, a social network may allow Alice to follow Bob, but Bob doesn’t have to follow Alice back. Let’s construct a new graph that demonstrates who follows whom:

![images/graphs/graph_2.png](images/graphs/graph_2.png)

This is known as a directed graph. In this example, the arrows indicate the direction of the relationship. Alice follows both Bob and Cynthia, but no one follows Alice. We can also see that Bob and Cynthia follow each other.

We can still use our simple hash-table implementation to store this data:

| ​  | followees = { |
| ​  | ​*"Alice"*​: [​*"Bob"*​, ​*"Cynthia"*​], |
| ​  | ​*"Bob"*​: [​*"Cynthia"*​], |
| ​  | ​*"Cynthia"*​: [​*"Bob"*​] |
| ​  | } |

The only ...

## Object-Oriented Graph Implementation

I demonstrated how a hash table can be used to implement a graph, but going forward, we’ll work with an object-oriented approach.

Here’s the beginning of an object-oriented graph implementation, using JavaScript:

| ​  | ​**class**​ Vertex { |
| ​  | ​**constructor**​(value) { |
| ​  | ​**this**​.value = value; |
| ​  | ​**this**​.adjacentVertices = []; |
| ​  | } |
| ​  |  |
| ​  | addAdjacentVertex(vertex) { |
| ​  | ​**this**​.adjacentVertices.push(vertex); |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | ​**export**​ ​**default**​ Vertex; |

The Vertex class has two primary attributes, the value and an array of adjacentVertices. In our social network example, each vertex represents a person, and the value might be a string containing the person’s name. With a more complex application, we’d probably want to store multiple pieces of data inside a vertex, such as the person’s additional profile information.

The adjacentVertices array contains all the vertices this vertex connects to. We can add a new adjacent vertex to a given vertex using the addAdjacentVertex method.

Here’s how we can use this class to build a directed graph representing who follows whom in this image:

![images/graphs/graph_2.png](images/graphs/graph_2.png)

| ​  | ​**let**​ alice = ​**new**​ Vertex(​*'alice'*​); |
| ​  | ​**let**​ bob = ​**new**​ Vertex(​*'bob'*​); |
| ​  | ​**let**​ cynthia = ​**new**​ Vertex(​*'cynthia'*​); |
| ​  |  |
| ​  | alice.addAdjacentVertex(bob); |
| ​  | alice.addAdjacentVertex(cynthia); |
| ​  | bob.addAdjacentVertex(cynthia); |
| ​  | cynthia.addAdjacentVertex(bob); |

Now, if we were building an undirected graph for the social network (where all friendships are mutual), it would make sense if we add Bob to Alice’s list of friends, we should automatically add Alice to Bob’s list of friends as well.

To do this, we can modify our addAdjacentVertex method as follows:

| ​  | addAdjacentVertex(vertex) { |
| ​  | ​**this**​.adjacentVertices.push(vertex); |
| ​  | vertex.adjacentVertices.push(​**this**​); |
| ​  | } |

Let’s say we’re calling this method on Alice and adding Bob to her list of friends. As with the previous version, we use this.adjacentVertices.push(vertex) to add Bob to Alice’s list of adjacentVertices. However, we also call this very method on Bob’s vertex, with vertex.adjacentVertices.push(this). This adds Alice to Bob’s list of friends as well.

To keep things simple going forward, we’re going to work with graphs that are connected (again, meaning all vertices are connected to each other in some way). With such graphs, we can use this one Vertex class to achieve all the algorithms going forward. The general idea is if we have access to just one vertex, we can find all other vertices from there since all the vertices are connected.

However, it’s important to point out that if we’re dealing with a disconnected graph, it may be impossible to discover all the vertices just from one vertex. In this case, we may need to store all the graph vertices in some additional data structure, such as an array, so that we have access to all of them. (It’s common to see graph implementations use a separate Graph class to contain this array.)

Adjacency List vs. Adjacency Matrix

Our implementation of the graph uses a simple list (in the form of an array) to store a vertex’s adjacent vertices. This approach is known as the adjacency list implementation.

However, it’s good to know that there’s another implementation that uses two-dimensional arrays instead of lists. This alternative approach is known as the adjacency matrix, and it can provide advantages in specific situations.

Both approaches are popular, and I’ve decided to stick with the adjacency list because I find it to be more intuitive. But I recommend you research the adjacency matrix as well, as it can be useful and is particularly interesting.

## Graph Search

One of the most common graph operations is searching for a particular vertex.

When dealing with graphs, the term search can have several connotations. In the simplest sense, to search a graph means to find a particular vertex somewhere within the graph. This would be similar to searching for a value within an array or a key-value pair inside a hash table.

However, when applied to graphs, the term search usually has a more specific connotation, and that is if we have access to one vertex in the graph, we must find another particular vertex that is somehow connected to this vertex.

For example, take a look at this example social network:

![images/graphs/social_network.png](images/graphs/social_network.png)

Let’s say we currently have access to Alice’s vertex. If we said that we’ll search for Irena, it would mean that we’re trying to find our way from Alice to Irena.

Interestingly, you can see that there are two different paths we can take to get from Alice to Irena.

The shorter path is obvious:

![images/graphs/shorter_path.png](images/graphs/shorter_path.png)

We can get from Alice to Irena in this sequence:

Alice -> Derek -> Gina -> Irena

However, we can take a slightly longer path to get to Irena as well:

![images/graphs/slightly_longer_path.png](images/graphs/slightly_longer_path.png)

This is the longer path:

Alice -> Elaine -> Derek -> Gina -> Irena

The term path is an official graph term, and it means the specific sequence of edges to get from one vertex to another.

Now, searching a graph (which you now know means getting from one vertex to another) can be useful for a variety of use cases.

Perhaps the most obvious application for graph search is searching for a particular vertex within a connected graph. When this is the case, search can be used to find any vertex within the entire graph even if we have access to just one random vertex.

Another use for graph search is to discover whether two vertices are connected. For example, we may want to know whether Alice and Irena are somehow connected to each other in this network. A search would give us the answer.

Search can also be used even if we aren’t looking for one particular vertex; that is, we can use graph search to merely traverse a graph, which can be useful if we want to perform an operation on every vertex in the graph. You’ll see shortly how this works.

## Depth-First Search

The two well-known approaches for graph search are depth-first search and breadth-first search. Both approaches can get the job done, but each provides unique advantages in particular situations. We’re going to start with depth-first search, also referred to as DFS, because it’s actually quite similar to the algorithm for binary tree traversal that we discussed back in [​*Binary Search Tree Traversal*​](#f_0150.xhtml_sect.binary-tree-traversal). In fact, it’s also the same essential algorithm that we saw in [​*Filesystem Traversal*​](#f_0101.xhtml_sect.filesystem-traversal).

As mentioned earlier, graph search can be used either to find a particular vertex or to simply traverse the graph. We’re going to begin by using depth-first search to traverse the graph since that algorithm is slightly simpler.

The key to any graph search algorithm is keeping track of which vertices we’ve visited so far. If we don’t do this, we can end up in an infinite cycle. Take the following graph, for example:

![images/graphs/cycle_graph.png](images/graphs/cycle_graph.png)

Here, Mohammad is friends with Felicia. And Felicia also happens to be friends with Zeina. But Zeina is friends with Mohammad. So our code would end up going in circles unless we keep track of which vertices we’ve already traversed.

This problem didn’t occur when we dealt with trees (or filesystem traversal), since trees can’t have cycles. But since a graph can have a cycle, we need to address this issue now.

One way to keep track of our visited vertices is by using a hash table. As we visit each vertex, we add the vertex (or its value) as a key in the hash table and assign it an arbitrary value, such as the Boolean true. If a vertex is present in the hash table, it means we’ve already visited it.

With this in mind, the depth-first search algorithm works as follows.

1.  Start at any random vertex within the graph.

2.  Add the current vertex to the hash table to mark it as having been visited.

3.  Iterate through the current vertex’s adjacent vertices.

4.  For each adjacent vertex, if the adjacent vertex has already been visited, ignore it.

5.  If the adjacent vertex has not yet been visited, recursively perform depth-first search on that vertex.

### Depth-First Search Walk-Through

Let’s see this in action.

In this walk-through, we’re going to start with Alice. In the following diagrams, the vertex with lines around it is the current vertex. A check mark means we’ve officially marked the vertex as having been visited (and added to the hash table).

Step 1: We start with Alice and give her a check mark to indicate that we’ve officially visited her vertex:

![images/graphs/visited_alice.png](images/graphs/visited_alice.png)

Next up, we’ll iterate over Alice’s neighbors using a loop. These will be Bob, Candy, Derek, and Elaine.

The order of which neighbor to visit first doesn’t matter, so let’s just start with Bob. He seems nice.

Step 2: We now perform depth-first search on Bob. Note that this is making a recursive call, as we’re already in the middle of a depth-first search of Alice.

As with all recursion, the computer needs to remember which function calls it’s still in the middle of, so it first adds Alice to the call stack:

![images/graphs/alice_call_stack.png](images/graphs/alice_call_stack.png)

We can now begin the depth-first search on Bob, which makes Bob the current vertex. We mark him as visited, as shown in the [graph](#f_0182.xhtml_fig.ch18.visit_bob).

![images/graphs/visit_bob.png](images/graphs/visit_bob.png)

We then iterate over Bob’s adjacent vertices. These are Alice and Fred.

Step 3: Alice has already been visited, so we can ignore her.

Step 4: The only other neighbor, then, is Fred. We call the depth-first search function on Fred’s vertex. The computer first adds Bob to the call stack to remember that it’s still in the middle of searching Bob:

![images/graphs/bob_call_stack.png](images/graphs/bob_call_stack.png)

We now perform depth-first search on Fred. He’s now the current vertex, so we mark him as visited:

![images/graphs/visit_fred.png](images/graphs/visit_fred.png)

Next, we iterate over Fred’s adjacent vertices, which are Bob and Helen.

Step 5: Bob has already been visited, so we ignore him.

Step 6: The only remaining adjacent vertex is Helen. We recursively perform depth-search first on Helen, so the computer first adds Fred to the call stack:

![images/graphs/fred_call_stack.png](images/graphs/fred_call_stack.png)

We now begin depth-first search on Helen. She’s the current vertex, so we mark her as visited:

![images/graphs/visit_helen.png](images/graphs/visit_helen.png)

Helen has two adjacent vertices: Fred and Candy.

Step 7: We’ve already visited Fred, so we can ignore him.

Step 8: Candy has not yet been visited, so we recursively perform depth-search on Candy. First, though, Helen gets added to the call stack:

![images/graphs/helen_call_stack.png](images/graphs/helen_call_stack.png)

We perform depth-first search on Candy. She’s now the current vertex, and we mark her as visited:

![images/graphs/visit_candy.png](images/graphs/visit_candy.png)

Candy has two adjacent vertices: Alice and Helen.

Step 9: We’ve already visited Alice, so we can ignore her.

Step 10: We’ve already visited Helen, so we can ignore her as well.

Since Candy has no other neighbors, we’re done performing depth-first search on Candy. At this point, then, the computer begins to unwind the call stack.

First, it pops off Helen from the call stack. We’ve already iterated over all her neighbors, so the depth-first search on Helen is complete.

The computer pops off Fred. We’ve iterated over all his neighbors too, so we’re done searching him as well.

The computer pops off Bob, but we’re done with him as well.

The computer then pops Alice off the call stack. Within our search of Alice, we were in the middle of looping through all of Alice’s neighbors. Now, this loop already iterated over Bob. (This was Step 2.) This leaves Candy, Derek, and Elaine.

Step 11: Candy has already been visited, so there’s no need to perform search on her.

However, we’ve not yet visited Derek or Elaine.

Step 12: Let’s proceed by recursively performing depth-first search on Derek. The computer adds Alice to the call stack once again:

![images/graphs/alice_call_stack.png](images/graphs/alice_call_stack.png)

The depth-first search of Derek now begins. Derek is the current vertex, so we mark him as visited:

![images/graphs/visit_derek.png](images/graphs/visit_derek.png)

Derek has three adjacent vertices: Alice, Elaine, and Gina.

Step 13: Alice has already been visited, so we don’t need to perform another search on her.

Step 14: Let’s visit Elaine next, by recursively performing depth-first search on her vertex. Before we do, the computer adds Derek to the call stack:

![images/graphs/derek_call_stack.png](images/graphs/derek_call_stack.png)

We now perform depth-first search on Elaine. We mark Elaine as visited, as shown in the [graph](#f_0182.xhtml_fig.ch18.visit_elaine).

![images/graphs/visit_elaine.png](images/graphs/visit_elaine.png)

Elaine has two adjacent vertices: Alice and Derek.

Step 15: Alice has already been visited, so there’s no need to perform another search on her.

Step 16: Derek, too, has already been visited.

Since we iterated over all Elaine’s neighbors, we’re done searching Elaine. The computer now pops Derek from the call stack and loops over his remaining adjacent vertices. In this case, Gina is the final neighbor to visit.

Step 17: We’ve never visited Gina before, so we recursively perform depth-first search on her vertex. First, though, the computer adds Derek to the call stack again:

![images/graphs/derek_call_stack.png](images/graphs/derek_call_stack.png)

We begin our depth-first search of Gina, and mark her as visited, as shown in the [graph](#f_0182.xhtml_fig.ch18.visit_gina).

![images/graphs/visit_gina.png](images/graphs/visit_gina.png)

Gina has two neighbors: Derek and Irena.

Step 18: Derek has already been visited.

Step 19: Gina has one unvisited adjacent vertex—namely, Irena. Gina gets added to the call stack so that we can recursively perform depth-first search on Irena:

![images/graphs/gina_call_stack.png](images/graphs/gina_call_stack.png)

We begin search on Irena and mark her as visited:

![images/graphs/visit_irena.png](images/graphs/visit_irena.png)

We iterate over Irena’s neighbors. Irena has only one neighbor: Gina.

Step 20: Gina has already been visited.

The computer then unwinds the call stack, popping off each vertex one by one. However, since each vertex on the call stack has already iterated over all of its neighbors, there’s nothing more for the computer to do with each vertex.

This means we’re done!

### Code Implementation: Depth-First Search

Here is an implementation of depth-first traversal:

| ​  | ​**function**​ dfsTraverse(vertex, visitedVertices={}) { |
| ​  | visitedVertices[vertex.value] = ​**true**​; |
| ​  |  |
| ​  | console.log(vertex.value); |
| ​  |  |
| ​  | ​**for**​ (​**const**​ adjacentVertex ​**of**​ vertex.adjacentVertices) { |
| ​  | ​**if**​ (!visitedVertices[adjacentVertex.value]) { |
| ​  | dfsTraverse(adjacentVertex, visitedVertices); |
| ​  | } |
| ​  | } |
| ​  | } |

Our dfsTraverse method accepts a single vertex and a visitedVertices hash table. The first time we call this function, visitedVertices defaults to an empty hash table. For the above example, we’d perform a depth-first traversal starting with the alice vertex, with the following:

| ​  | dfsTraverse(alice); |

As we visit vertices, though, we populate this hash table with the vertices we’ve visited and pass along the same hash table with each recursive call.

The first thing we do within the function is mark the current vertex as visited. We do this by adding the vertex’s value to the hash:

| ​  | visitedVertices[vertex.value] = ​**true**​; |

We then optionally print the vertex’s value just to get feedback that we’ve truly traversed it:

| ​  | console.log(vertex.value); |

Next, we iterate over all the adjacent vertices of the current vertex:

| ​  | ​**for**​ (​**const**​ adjacentVertex ​**of**​ vertex.adjacentVertices) { |

We check each adjacent vertex to see whether it has already been visited. If it has, we do nothing, but if it has never been visited, we recursively call dfsTraverse on that adjacent vertex:

| ​  | ​**if**​ (!visitedVertices[adjacentVertex.value]) { |
| ​  | dfsTraverse(adjacentVertex, visitedVertices); |
| ​  | } |

Again, we also pass in the visitedVertices hash table so the ensuing call has access to it.

If we want to use depth-first search to search for a particular vertex, we can use a modified version of the previous function:

| ​  | ​**function**​ dfs(vertex, searchValue, visitedVertices={}) { |
| ​  | visitedVertices[vertex.value] = ​**true**​; |
| ​  |  |
| ​  | ​**if**​ (vertex.value === searchValue) { ​**return**​ vertex; } |
| ​  |  |
| ​  | ​**for**​ (​**const**​ adjacentVertex ​**of**​ vertex.adjacentVertices) { |
| ​  | ​**if**​ (adjacentVertex.value === searchValue) { |
| ​  | ​**return**​ adjacentVertex; |
| ​  | } |
| ​  |  |
| ​  | ​**if**​ (!visitedVertices[adjacentVertex.value]) { |
| ​  | ​**const**​ vertexWeAreSearchingFor = |
| ​  | dfs(adjacentVertex, searchValue, visitedVertices); |
| ​  |  |
| ​  | ​**if**​ (vertexWeAreSearchingFor) { |
| ​  | ​**return**​ vertexWeAreSearchingFor; |
| ​  | } |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | ​**return**​ ​**null**​; |
| ​  | } |

This implementation also recursively calls itself for each vertex but returns the vertexWeAreSearchingFor if it finds the correct vertex.

## Breadth-First Search

Breadth-first search, often abbreviated BFS, is another way to search a graph. Unlike depth-first search, breadth-first search does not use recursion. Instead, the algorithm revolves around our old friend, the queue. As you’ll recall, the queue is a FIFO data structure, and whatever goes in first, comes out first.

Let’s look at the algorithm for breadth-first search. As with our walk-through of depth-first search, we’re going to focus on graph traversal using breadth-first search; that is, we’re going to visit each vertex from our example social network.

Here’s the BFS traversal algorithm:

1.  Start at any vertex within the graph. We’ll call this the starting vertex.

2.  Add the starting vertex to the hash table to mark it as having ...

## The Efficiency of Graph Search

Let’s analyze the time complexity of graph search using Big O notation.

In both depth-first search and breadth-first search, we traverse all the vertices in a worst-case scenario. The worst-case scenario may be that we’re intending to do a full-graph traversal, or we may be searching for a vertex that doesn’t exist in the graph. Or, the vertex we’re searching for may just happen to be the last vertex in the graph that we check.

In any case, we touch all vertices in the graph. At first glance, this would seem to be O(N), with N being the number of vertices.

However, in both search algorithms, for each vertex we traverse, we also iterate over all of its adjacent vertices. We may ignore an adjacent vertex if it has already been visited, but we still spend a step checking that vertex to see whether we’ve visited it.

So for each vertex we visit, we also spend steps checking each of the vertex’s adjacent neighbors. This would seem tough to peg down using Big O notation since each vertex may have a different number of adjacent vertices.

Let’s analyze a simple graph to make this clear:

![images/graphs/abcde_graph.png](images/graphs/abcde_graph.png)

Here, Vertex A has four neighbors. By contrast, B, C, D, and E each have three neighbors. Let’s count the number of steps it takes to search this graph.

At the very least, we have to visit each of the five vertices. This alone takes five steps.

Then, for each vertex, we iterate over each of its neighbors.

This would add the following steps:

A: 4 steps to iterate over 4 neighbors
B: 3 steps to iterate over 3 neighbors
C: 3 steps to iterate over 3 neighbors
D: 3 steps to iterate over 3 neighbors
E: 3 steps to iterate over 3 neighbors

This yields sixteen iterations.

So we have the visiting of the five vertices, plus sixteen iterations over adjacent neighbors. That’s a total of twenty-one steps.

But here’s another graph with five vertices:

![images/graphs/vwxyz_graph.png](images/graphs/vwxyz_graph.png)

This graph has five vertices, but the count of iterations over adjacent neighbors is as follows:

V: 4 steps to iterate over 4 neighbors
W: 1 step to iterate over 1 neighbor
X: 1 step to iterate over 1 neighbor
Y: 1 step to iterate over 1 neighbor
Z: 1 step to iterate over 1 neighbor

This is a total of eight iterations.

We have the five vertices, plus eight iterations over adjacent neighbors. This is a total of thirteen steps.

So, we have two graphs, each containing five vertices. However, searching one takes twenty-one steps, while searching the other takes thirteen steps.

It emerges that we can’t just count how many vertices are in the graph. Instead, we also need to consider how many adjacent neighbors each vertex has.

To effectively describe the efficiency of graph search, then, we’re going to need to use two variables. We need one to represent the number of vertices in the graph and another to be the total number of adjacent neighbors each vertex has.

### O(V + E)

Interestingly enough, Big O notation doesn’t use the variable N to describe either of these things. Instead, it uses the variables V and E.

The V is the easier one. V stands for vertex and represents the number of vertices in the graph.

E, interestingly, stands for edge, meaning the number of edges in the graph.

Now, computer scientists describe the efficiency of graph search as O(V + E). This means that the number of steps is the number of vertices in the graph plus the number of edges in the graph. Let’s see why this is the efficiency of graph search, as it’s not immediately intuitive.

Specifically, if you look at our two earlier examples, you’ll notice that V + E doesn’t seem to be accurate.

In the A-B-C-D-E graph, there are five vertices and eight edges. This would be a total of thirteen steps. However, we noted that there’s actually a total of twenty-one steps.

And in the V-W-X-Y-Z graph, there are five vertices and four edges. O(V + E) says that graph search would have nine steps. But we saw that there are actually thirteen.

The reason for this discrepancy is that while O(V + E) only counts the number of edges once, in reality graph search touches each edge more than once.

In the V-W-X-Y-Z graph, for example, there are only four edges. However, the edge between V and W is used twice; that is, when V is the current vertex, we find its adjacent neighbor W using that edge. But when W is the current vertex, we find its adjacent vertex V using that same edge.

With this in mind, the most accurate way to describe the efficiency of graph search in the V-W-X-Y-Z graph would be to count the five vertices plus the following:

2 * edge between V and W
2 * edge between V and X
2 * edge between V and Y
2 * edge between V and Z

So this comes out to be V + 2E since we visit all the vertices once (that’s the V) and use each edge twice (that’s the 2E).

In this example, V is 5, as we visit 5 vertices. And since we use each of the four edges twice, 2E comes out to be 8\. This is how V + 2E gives us a total of thirteen steps.

The answer, though, to why we just call this O(V + E), is because Big O drops the constants. While in reality the number of steps is V + 2E, we reduce this to O(V + E).

So while O(V + E) is ultimately just an approximation, it’s good enough, as are all expressions of Big O.

What is definitely clear, though, is that increasing the number of edges will increase the number of steps. After all, both the A-B-C-D-E and V-W-X-Y-Z graphs have five vertices, but because the A-B-C-D-E graph has more edges, it takes considerably more steps.

At the end of the day, graph search is O(V + E) in a worst-case scenario, where the vertex we’re searching for is the last one we find (or isn’t present in the graph at all). And this is true for both breadth-first search and depth-first search.

However, we saw earlier that depending on the shape of the graph and the data we’re searching for, our choice of breadth-first versus depth-first can optimize our search where we’d hope to find our vertex at some point before having to traverse the entire graph. The right method of search can help us increase the odds that we won’t end up in a worst-case scenario and that we’ll find the vertex early.

In the next section, you’re going to learn about a specific type of graph that comes with its own set of search methods that can be used to solve some complex but useful problems.

Graph Databases

Because graphs are so efficient at working with data involving relationships (such as friends in a social network), special graph databases are often used to store this kind of data in real-world software applications. These databases use the concepts you’re learning about in this chapter, as well as other elements of graph theory, to optimize efficiency of operations around this kind of data. Indeed, many social networking applications are powered by graph databases under the hood.

Some examples of graph databases include Neo4j^([[7]](#f_0188.xhtml_FOOTNOTE-7)) and ArangoDB.^([[8]](#f_0188.xhtml_FOOTNOTE-8)) These websites are a good place to start if you’re interested in learning more about how graph databases work.

## Weighted Graphs

We’ve already seen that graphs can come in a number of different flavors. Another useful type of graph, known as a weighted graph, adds additional information to the edges of the graph.

Here’s a weighted graph that represents a basic map of several major cities in the United States:

![images/graphs/weighted_graph_1.png](images/graphs/weighted_graph_1.png)

In this graph, each edge is accompanied by a number that represents the distance in miles between the cities the edge connects—for example, 714 miles between Chicago and New York City.

It’s also possible to have weighted graphs that are also directional. In the following example, we can see that although a flight from Dallas to Toronto is $138, a flight from Toronto back to Dallas is $216:

![images/graphs/weighted_graph_2.png](images/graphs/weighted_graph_2.png)

### Weighted Graphs in Code

We need to make a slight modification to our code if we want to add weights to our graph. One way to do this is to use a hash table to represent the adjacent vertices rather than using an array:

| ​  | ​**class**​ WeightedGraphVertex { |
| ​  | ​**constructor**​(value) { |
| ​  | ​**this**​.value = value; |
| ​  | ​**this**​.adjacentVertices = ​**new**​ Map(); |
| ​  | } |
| ​  |  |
| ​  | addAdjacentVertex(vertex, weight) { |
| ​  | ​**this**​.adjacentVertices.​**set**​(vertex, weight); |
| ​  | } |
| ​  | } |

As you can see, this.adjacentVertices is now a hash table instead of an array. The hash table will contain key-value pairs, where in each pair the adjacent vertex is the key and the weight (of the edge from this vertex to the adjacent vertex) is the value.

When we use the addAdjacentVertex method to add an adjacent vertex, we now pass in both the adjacent vertex as well as the weight.

Since we’ll continue to deal with the example of a graph that depicts flight fares to and from various cities, we’ll create a special class called City. This is the same implementation as the preceding WeightedGraphVertex but uses class and variable names appropriate to our use case:

| ​  | ​**class**​ City { |
| ​  | ​**constructor**​(name) { |
| ​  | ​**this**​.name = name; |
| ​  | ​**this**​.routes = ​**new**​ Map(); |
| ​  | } |
| ​  |  |
| ​  | addRoute(city, price) { |
| ​  | ​**this**​.routes.​**set**​(city, price); |
| ​  | } |
| ​  | } |

So if we want to create the Dallas–Toronto flight price graph from earlier, we can run the following code:

| ​  | ​**let**​ dallas = ​**new**​ City(​*'Dallas'*​); |
| ​  | ​**let**​ toronto = ​**new**​ City(​*'Toronto'*​); |
| ​  |  |
| ​  | dallas.addRoute(toronto, 138); |
| ​  | toronto.addRoute(dallas, 216); |

### The Shortest Path Problem

Weighted graphs can be very useful in modeling all sorts of datasets, and they also come with some powerful algorithms that help us make the most out of that data.

Let’s harness one of these algorithms to save us a bit of money.

Here’s a graph that demonstrates the costs of available flights between five different cities:

![images/graphs/weighted_graph_3.png](images/graphs/weighted_graph_3.png)

Now, say I’m in Atlanta and want to fly to El Paso. Unfortunately, we can see in this graph that there’s no direct route from Atlanta to El Paso at this time. However, I can get there if I’m willing to stop over in other cities along the way. For example, I can fly from Atlanta to Denver and then from Denver to El Paso. But there are other paths as well, and each path has a different price. The Atlanta–Denver–El Paso path will set me back $300, but the Atlanta–Denver–Chicago–El Paso path only costs $280.

The puzzle, now, is this: how do we create an algorithm that finds the cheapest price I’d have to shell out to get to my destination? Let’s assume we don’t care about how many stops we have to make; we’re just out to get the cheapest fare.

This kind of puzzle is known as the shortest path problem. This problem can take other forms as well. For example, if the graph showed us distances between cities, we might want to find the path that has the shortest distance. But here, the shortest path we’re looking for is the cheapest one since the weights represent flight prices.

## Dijkstra’s Algorithm

Numerous algorithms can solve the shortest path problem, and one of the most famous is one discovered by Edsger Dijkstra (pronounced “dike’ struh”) in 1959\. Unsurprisingly, this algorithm is known as Dijkstra’s algorithm.

In this section, we’re going to use Dijkstra’s algorithm to find the cheapest path in our city flights example.

### Dijkstra’s Algorithm Setup

The first thing to note is that Dijkstra’s algorithm comes with a free bonus. By the time we’re done, we’re not just going to find the cheapest price from Atlanta to El Paso, but also we’re going to find the cheapest prices from Atlanta to all known cities. As you’ll see, the algorithm simply works this way; we end up gathering all of this data. So we’ll know the cheapest ...

## Wrapping Up

We’re almost at the end of our journey, as this chapter represents the last significant data structure you’ll encounter in this book. You’ve seen that graphs are extremely powerful tools for dealing with data involving relationships, and in addition to making our code fast, they can also help solve tricky problems.

In truth, I could fill a book just discussing graphs. So many interesting and useful algorithms surround this data structure, such as the minimum spanning tree, topological sort, bidirectional search, the Floyd--Warshall algorithm, the Bellman–Ford algorithm, and graph coloring, just to name a few. But this chapter should serve as the foundation for you to explore these additional topics.

Along our travels, our primary ...

## Exercises

The following exercises provide you with the opportunity to practice with graphs. The solutions to these exercises are found in the section [​*Chapter 18*​](#f_0223.xhtml_graphs.solutions).

1.  The first [graph](#f_0188.xhtml_fig.ch18.recommendation_graph) powers an e-commerce store’s recommendation engine. Each vertex represents a product available on the store’s website. The edges connect each product to other “similar” products the site will recommend to the user when browsing a particular item.

    If the user is browsing “nails”, what other products will be recommended to the user?

2.  If we perform depth-first search on the second [graph](#f_0188.xhtml_fig.ch18.exercise_2_graph), starting with the A vertex, what is the order in which we’ll traverse all the vertices? Assume that when given the choice to visit multiple adjacent vertices, we’ll first visit the node that is earliest in the alphabet.

    ![images/graphs/recommendation_graph.png](images/graphs/recommendation_graph.png)![images/graphs/exercise_2_graph.png](images/graphs/exercise_2_graph.png)
3.  If we perform breadth-first search on the previous graph starting with the A vertex, what is the order in which we’ll traverse all the vertices? Assume that when given the choice to visit multiple adjacent vertices, we’ll first visit the node that is earliest in the alphabet.

4.  In this chapter, I only provided the code for breadth-first traversal, as discussed in [​*Breadth-First Search*​](#f_0183.xhtml_sect.breadth-first-search); that is, the code simply printed the value of each vertex. Modify the code so that it performs an actual search for a vertex value provided to the function. (We did this for depth-first search.) In other words, if the function finds the vertex it’s searching for, it should return that vertex’s value. Otherwise, it should return null.

5.  In [​*Dijkstra’s Algorithm*​](#f_0186.xhtml_sect.dijkstras-algorithm), we saw how Dijkstra’s algorithm helped us find the shortest path within a weighted graph. However, the concept of a shortest path exists within an unweighted graph as well. How?

    The shortest path in a classic (unweighted) graph is the path that takes the fewest number of vertices to get from one vertex to another.

    This can be especially useful in social networking applications. Take the example network that follows:

    ![images/graphs/exercise_5_graph.png](images/graphs/exercise_5_graph.png)

    If we want to know how Idris is connected to Lina, we’d see that she’s connected to her from two different directions; that is, Idris is a second-degree connection to Lina through Kamil, but she’s also a fifth-degree connection through Talia. Now, we’re probably interested in how closely Idris is connected to Lina, so the fact that she’s a fifth-degree connection is unimportant given that they’re also second-degree connections.

    Write a function that accepts two vertices from a graph and returns the shortest path between them. The function should return an array containing the precise path, such as ["Idris", "Kamil", "Lina"].

    Hint: The algorithm may contain elements of both breadth-first search and Dijkstra’s algorithm.

#### Footnotes

[[7]](#f_0184.xhtml_FNPTR-7)

http://neo4j.com

[[8]](#f_0184.xhtml_FNPTR-8)

https://www.arangodb.com

Copyright © 2024, The Pragmatic Bookshelf.

# Chapter 19Dealing with Space Constraints

When analyzing the efficiency of various algorithms throughout this book, we’ve focused exclusively on how fast they run—that is, their time complexity. However, another measure of efficiency can be useful as well, which is how much memory an algorithm consumes. This measure is known as space complexity.

Space complexity becomes an important factor when memory is limited. If you have an enormous amount of data, or are programming for a small device with limited memory, space complexity can matter a lot.

In a perfect world, we’d always use algorithms that are both fast and memory-efficient. However, sometimes we can’t have both and we need to choose between the two. Each situation requires a careful analysis ...

## Big O of Space Complexity

Interestingly, computer scientists use Big O notation to describe space complexity just as they do for time complexity.

Back when I introduced Big O notation in Chapter 3, [​*O Yes! Big O Notation*​](#f_0031.xhtml_chp.big_o_notation), I described Big O in terms of what I called the “key question.” For time complexity, the key question was this: if there are N data elements, how many steps will the algorithm take?

To use Big O for space complexity, we just need to reframe the key question. When it comes to memory consumption, the key question becomes if there are N data elements, how many units of memory will the algorithm consume?

Here’s a simple example.

Let’s say we’re writing a function that accepts an array of strings and returns an array of those ...

## Trade-Offs Between Time and Space

Here’s a function that accepts an array and returns whether it contains any duplicate values (you may recognize this function from Chapter 4, [​*Speeding Up Your Code with Big O*​](#f_0040.xhtml_chp.speeding_up):

| ​  | ​**function**​ hasDuplicateValue(array) { |
| ​  | ​**for**​ (​**let**​ i = 0; i < array.length; i += 1) { |
| ​  | ​**for**​ (​**let**​ j = 0; j < array.length; j += 1) { |
| ​  | ​**if**​ (i !== j && array[i] === array[j]) { |
| ​  | ​**return**​ ​**true**​; |
| ​  | } |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | ​**return**​ ​**false**​; |
| ​  | } |

This algorithm uses nested loops and has a time complexity of O(N²). We’ll call this implementation Version #1.

Here’s a second implementation, Version #2, which employs a hash table and just a single loop:

| ​  | ​**function**​ hasDuplicateValue(array) { |
| ​  | ​**const**​ existingValues = {}; |
| ​  |  |
| ​  | ​**for**​ (​**const**​ value ... |

## The Hidden Cost of Recursion

We’ve dealt quite a bit with recursive algorithms in this book. Let’s look at a simple recursive function:

| ​  | ​**function**​ recurse(n) { |
| ​  | ​**if**​ (n < 0) { ​**return**​; } |
| ​  |  |
| ​  | console.log(n); |
| ​  | recurse(n - 1); |
| ​  | } |

This function accepts a number n and counts down to 0, printing each decrementing number along the way.

It’s a straightforward bit of recursion and seems harmless. Its speed is O(N), as the function will run as many times as the argument n. And it doesn’t create any new data structures, so it doesn’t seem to take up any additional space.

Or does it?

I explained how recursion works under the hood back in Chapter 10, [​*Recursively Recurse with Recursion*​](#f_0096.xhtml_chp.recursion). You learned that each time a function recursively calls itself, an item is added to the call stack so that the computer can come back to the outer function once the inner function is complete.

If we pass the number 100 into our recurse function, it would add recurse(100) before proceeding to execute recurse(99). And it would then add recurse(99) to the call stack before executing recurse(98).

The call stack would be at its peak when recurse(-1) is called, and there would be 101 items in the call stack, from recurse(100) down to recurse(0).

Now, even though the call stack will eventually get unwound, we do need enough memory to store these 101 items for at least some period of time. It emerges, then, that our recursive function takes up O(N) space. In this case, N is the number passed into the function; if we pass in the number 100, we need to temporarily store about 100 function calls in the call stack.

An important principle emerges from all of this: a recursive function takes up a unit of space for each recursive call it makes. This is the sneaky way recursion can gobble up memory; even if our function doesn’t explicitly create new data, the recursion itself adds data to the call stack.

To properly calculate how much space a recursive function takes, we always need to figure out how big the call stack would be at its peak.

For our recurse function, the call stack will be about as large as whatever number n is.

At first, this may seem a bit trivial. After all, our modern computers can handle a few items on the call stack, right? Well, let’s see.

When I pass in the number 20,000 into the recurse function on my sleek, up-to-date laptop, my computer cannot process it. Now, 20,000 doesn’t seem like a very large number. But this is what happens when I run recurse(20000):

My computer prints the numbers from 20000 until 9120 and then terminates with this message:

| ​  | RangeError: Maximum call stack size exceeded |

Because the recursion lasted from 20000 until about 9000 (I’m rounding 9120 down), we can figure out that the call stack reached a size of about 11,000 when the computer ran out of memory. It turns out my computer will not tolerate a call stack that contains more than 11,000 items.

This is a huge limitation on recursion, as I can’t use my beautiful recurse function on a number greater than 11,000!

Let’s contrast this to a simple loop approach:

| ​  | ​**function**​ loop(n) { |
| ​  | ​**while**​ (n >= 0) { |
| ​  | console.log(n); |
| ​  | n -= 1; |
| ​  | } |
| ​  | } |

This function accomplishes the same goal using a basic loop instead of recursion.

Because this function doesn’t use recursion, and doesn’t take up any additional memory, it can process a huge number without ever causing the computer to run out of space. The function may take some time on huge numbers, but it’ll get the job done without giving up prematurely as the recursive function did.

With this in mind, we can now understand why Quicksort is said to take up O(log N) space. Quicksort makes O(log N) recursive calls, so at its peak has a call stack that is the size of log(N).

When we can implement a function using recursion, then, we need to weigh recursion’s benefits against its drawbacks. Recursion allows us to use the “magical” top-down mindset, as you looked at in Chapter 11, [​*Learning to Write in Recursive*​](#f_0104.xhtml_chp.learning_to_write_in_recursive), but we also need our function to get the job done. And if we’re processing a lot of data, or even just a number like 11,000, recursion may not cut it.

Again, this isn’t to discredit recursion. It just means we need to weigh all the pros and cons of each algorithm in every situation.

## Wrapping Up

We’ve now covered how to measure the efficiency of our algorithms from all angles, including time and space. You’re now armed with the analytical abilities to weigh each algorithm against the next and make informed decisions on which approach to use for your own applications.

As you’re now able to make your own decisions, it’s time to move on to the final chapter of our journey. In it, I’m going to provide a few last pieces of advice on how to optimize your own code, while taking you through some realistic scenarios that we’ll optimize together.

## Exercises

The following exercises provide you with the opportunity to practice with space constraints. The solutions to these exercises are found in the section [​*Chapter 19*​](#f_0224.xhtml_dealing.with.space.constraints.solutions).

1.  Following is the word builder algorithm we encountered in [​*Word Builder*​](#f_0066.xhtml_sect.word-builder). Describe its space complexity in terms of Big O:

    | ​  | ​**function**​ wordBuilder(array) { |
    | ​  | ​**const**​ collection = []; |
    | ​  |  |
    | ​  | ​**for**​ (​**const**​ [indexI, valueI] ​**of**​ array.entries()) { |
    | ​  | ​**for**​ (​**const**​ [indexJ, valueJ] ​**of**​ array.entries()) { |
    | ​  | ​**if**​ (indexI !== indexJ) { |
    | ​  | collection.push(valueI + valueJ); |
    | ​  | } |
    | ​  | } |
    | ​  | } |
    | ​  |  |
    | ​  | ​**return**​ collection; |
    | ​  | } |

2.  Following is a function that reverses an array. Describe its space complexity in terms of Big O:

    | ​  | ​**function**​ reverse(array) { |
    | ​  | ​**const**​ newArray = []; |
    | ​  |  |
    | ​  | ​**for**​ (​**const**​ value ​**of**​ array) { |
    | ​  | newArray.unshift(value); |
    | ​  | } |
    | ​  |  |
    | ​  | ​**return**​ newArray; |
    | ​  | } |

3.  Create a new function to reverse an array that takes up just O(1) extra space.

4.  Following are three different implementations of a function that accepts an array of numbers and returns an array containing those numbers multiplied by 2\. For example, if the input is [5, 4, 3, 2, 1], the output will be [10, 8, 6, 4, 2].

    | ​  | ​**function**​ doubleArray1(array) { |
    | ​  | ​**const**​ newArray = []; |
    | ​  |  |
    | ​  | ​**for**​ (​**const**​ value ​**of**​ array) { |
    | ​  | newArray.push(value * 2); |
    | ​  | } |
    | ​  |  |
    | ​  | ​**return**​ newArray; |
    | ​  | } |
    | ​  |  |
    | ​  | ​**function**​ doubleArray2(array) { |
    | ​  | ​**for**​ (​**let**​ i = 0; i < array.length; i += 1) { |
    | ​  | array[i] *= 2; |
    | ​  | } |
    | ​  |  |
    | ​  | ​**return**​ array; |
    | ​  | } |
    | ​  |  |
    | ​  | ​**function**​ doubleArray3(array, index = 0) { |
    | ​  | ​**if**​ (index >= array.length) { ​**return**​; } |
    | ​  |  |
    | ​  | array[index] *= 2; |
    | ​  | doubleArray3(array, index + 1); |
    | ​  |  |
    | ​  | ​**return**​ array; |
    | ​  | } |

    Fill in the table that follows to describe the efficiency of these three versions in terms of both time and space:

    | Version | Time Complexity | Space Complexity |
    | --- | --- | --- |
    | Version #1 | ? | ? |
    | Version #2 | ? | ? |
    | Version #3 | ? | ? |

Copyright © 2024, The Pragmatic Bookshelf.

# Chapter 20Techniques for Code Optimization

We’ve come a long way. You now have the tools to analyze the time and space complexity of algorithms across a wide variety of data structures. With these concepts, you’re now able to write code that is fast, memory-efficient, and beautiful.

In this final chapter of our journey, I’d like to leave you with some additional techniques for optimizing code. Sometimes it’s difficult to see how an algorithm can be improved. Over the years, I’ve found the following mental strategies help me see how I can make my code more efficient. I hope they’ll be helpful to you as well.

## Prerequisite: Determine Your Current Big O

Before we get into the optimization techniques, though, it’s important to stress that there’s something you need to do before you start optimizing your algorithm.

The prerequisite to optimization is determining the efficiency of your current code. After all, it’s impossible to make an algorithm faster if you don’t know how fast it is now.

By now, you have a thorough understanding of Big O notation and the various categories of Big O. Once you know what category of Big O your algorithm belongs to, you can begin optimizing.

Throughout the rest of this chapter, I’ll refer to this step of determining your current algorithm’s Big O as the “prereq.”

## Start Here: The Best-Imaginable Big O

While all the techniques in this chapter are useful, you’ll find that some come in handy for certain scenarios, while others are effective for other scenarios.

This first technique, however, applies to all algorithms and should be the first step of your optimization process.

And here it is.

Once you’ve determined the efficiency of your current algorithm (the prereq), come up with what you believe to be what I call the “best-imaginable Big O.” (I’ve seen others refer to this as the “best-conceivable runtime” when applied to speed.)

Essentially, the best-imaginable Big O is the absolute best Big O you could dream of for the problem at hand. This is the Big O you know is absolutely impossible to beat.

For example, if we were to write a function that prints every item from an array, we’d probably say that the best-imaginable Big O for this task is O(N). Given that we have to print each of the N items in the array, we have no choice but to process each of the N items. There’s no way around this fact, as we need to “touch” each item to print it. Because of this, O(N) is the best-imaginable Big O we could imagine for this scenario.

When optimizing an algorithm, then, we need to determine two Big Os. We need to know the Big O our algorithm currently takes (the prereq), and we need to come up with the best-imaginable Big O the task could possibly take.

If these two Big Os are not the same, it means we have something to optimize. If, say, my current algorithm has a runtime of O(N²) but the best-imaginable Big O is O(N), we now have an improvement to strive for. The gap between the two Big Os shows us the potential gains we can make through optimization.

Let’s summarize these steps:

1.  Determine the Big O category of your current algorithm. (This is the prereq.)

2.  Determine the best-imaginable Big O you could dream of for the problem at hand.

3.  If the best-imaginable Big O is faster than your current Big O, you can now try to optimize your code, with the goal of bringing your algorithm as close to the best-imaginable Big O as possible.

It’s important to stress that it’s not always possible to achieve the best-imaginable Big O. After all, just because you can dream of something doesn’t mean it can become reality.

In fact, it might turn out that your current implementation cannot be optimized further. However, the best-imaginable Big O is still a tool for giving us a goal to shoot for with our optimization.

Often, I find that I can successfully optimize an algorithm to a speed that is in between my current Big O and the best-imaginable Big O.

For example, if my current implementation is O(N²) and my best-imaginable Big O is O(log N), I’ll aim to optimize my algorithm to become O(log N). If, in the end, my optimizations speed up my code to “just” O(N), that’s still a great success, and the best-imaginable Big O will have served a useful purpose.

### Stretching the Imagination

As you’ve seen, the benefit of coming up with the best-imaginable Big O is that it gives us an optimization goal to shoot for. To really make the most of this, it’s worth stretching the imagination a bit to come up with a best-imaginable Big O that is amazing. In fact, I recommend making your best-imaginable Big O the fastest Big O you can think of that isn’t outright impossible.

Here’s another mental trick I use for stoking my imagination. I pick a really fast Big O for the problem at hand—let’s call it “Amazing Big O.” I then ask myself, “If someone told me that they know how to pull off the Amazing Big O for this problem, would I believe them?” If I’d believe someone who said that they figured out how to solve this problem with the efficiency of Amazing Big O, I then make the Amazing Big O my best-imaginable Big O.

Once we know the Big O of our current algorithm and the best-imaginable Big O that we’re aiming for, we’re primed for optimization.

In the remainder of this chapter, we’re going to explore additional optimization techniques and mental strategies that can help us boost the efficiency of our code.

## Magical Lookups

One of my favorite go-to optimization techniques is to ask myself, “If I could magically find a desired piece of information in O(1) time, can I make my algorithm faster?” If the answer to this is yes, I then use a data structure (often a hash table) to make that magic happen. I call this technique “magical lookups.”

Let me clarify this technique with an example.

### Magically Looking Up Authors

Let’s say we’re writing library software and we have data about books and their authors contained in two separate arrays.

Specifically, the array of authors looks like this:

| ​  | ​**const**​ authors = [ |
| ​  | { authorId: 1, name: ​*'Virginia Woolf'*​ }, |
| ​  | { authorId: 2, name: ​*'Leo Tolstoy'*​ }, |
| ​  | { authorId: 3, name: ​*'Dr. Seuss'*​ }, |
| ​  | { authorId: 4, name: ... |

## Recognizing Patterns

One of the most helpful strategies for both code optimization and algorithm development in general is to find patterns within the problem at hand. Often, the discovery of a pattern can help you cut through all the complexity of a problem and develop an algorithm that is simple.

### The Coin Game

Here’s a great example. A game I call “the coin game” has two players who compete in the following way: they start with a pile of coins, and each player has the choice of removing either one or two coins from the pile. The player who removes the last coin loses. Fun, right?

It turns out that this isn’t a game of random chance, and with the right strategy, you can force your opponent to take the last coin and lose the game. To make this ...

## Greedy Algorithms

This next tactic can speed up some of the most stubborn algorithms. It doesn’t work in every situation, but when it does, it can be a game changer.

Let’s talk about writing greedy algorithms.

This may sound like a strange term, but here’s what it means. A greedy algorithm is one that, in each step, chooses what appears to be the best option at that moment in time. This will make sense with a basic example.

### Array Max

Let’s write an algorithm that finds the greatest number in an array. One way we can do this is to use nested loops and check each number against every other number in the array. When we find the number that is greater than every other number, it means we’ve found the greatest number in the array.

As is typical for ...

## Change the Data Structure

Another helpful optimization technique is to imagine what would happen if we stored our given data in an alternative data structure.

For example, we may be working on a problem where the data is given to us in the form of an array. However, reimagining that same data stored as a hash table, tree, or other data structure can sometimes reveal clever optimization opportunities.

Our use of a hash table for the magical lookup technique earlier is a specific example of this. And we’re about to see that changing the data structure can be useful for other scenarios as well.

### The Anagram Checker

Here’s one example. Let’s say we’re writing a function that determines whether two given strings are anagrams of one another. We encountered ...

## Wrapping Up

The techniques presented here can be useful in optimizing your code. Again, you’ll always want to start by determining your current Big O and the best-imaginable Big O. After that, you have all the other techniques at your disposal.

You’ll find that some techniques work better than others in certain situations, but they’re all worth thinking about in a given situation to see if they may be the right tool for the job.

With experience, you’ll hone your optimization sense and probably develop additional techniques of your own!

## Parting Thoughts

You’ve learned a lot in this journey, but your journey is only just beginning. (Cue dramatic music.)

You’ve learned that the right choices in algorithm design and data structures can dramatically affect the performance of your code.

You’ve learned how to determine the efficiency of your code.

You’ve learned how to optimize your code to make it faster, more memory-efficient, and more elegant.

What you can take away from this book is a framework for making educated technology decisions. Creating great software involves evaluating the trade-offs of the available options, and you’re now armed with the ability to see the pros and cons of each option and make the best choice for the task at hand. And you also have the ability to think ...

## Exercises

The following exercises provide you with the opportunity to practice with optimizing your code. The solutions to these exercises are found in the section [​*Chapter 20*​](#f_0225.xhtml_tips.for.code.optimization.solutions).

1.  You’re working on software that analyzes sports players. Following are two arrays of players of different sports:

    | ​  | const basketballPlayers = [ |
    | ​  | { firstName: 'Jill', lastName: 'Huang', team: 'Gators' }, |
    | ​  | { firstName: 'Janko', lastName: 'Barton', team: 'Sharks' }, |
    | ​  | { firstName: 'Wanda', lastName: 'Vakulskas', team: 'Sharks' }, |
    | ​  | { firstName: 'Jill', lastName: 'Moloney', team: 'Gators' }, |
    | ​  | { firstName: 'Luuk', lastName: 'Watkins', team: 'Gators' }, |
    | ​  | ]; |
    | ​  |  |
    | ​  | const footballPlayers = [ |
    | ​  | { firstName: 'Hanzla', lastName: 'Radosti', team: '32ers' }, |
    | ​  | { firstName: 'Tina', ... |

# Appendix 1Exercise Solutions

## Chapter 1

These are the solutions to the exercises found in the section [​*Exercises*​](#f_0023.xhtml_why.data.structures.matter.exercises).

1.  Let’s break down each of the cases:

    1.  Reading from an array always takes just one step.

    2.  Searching for a nonexistent element within an array of size 100 will take 100 steps, as the computer needs to inspect each element of the array before determining the element cannot be found.

    3.  The insertion will take 101 steps: 100 shifts of each element to the right, and one step to insert the new element at the front of the array.

    4.  Insertion at the end of an array always takes one step.

    5.  The deletion will take 100 steps: first the computer deletes the first element and then shifts the remaining 99 elements to the left, one at a time.

    6.  Deletion at the end of an array always takes one step.

2.  Let’s break down each of the cases:

    1.  Like the array, reading from the array-based set will take just one step.

    2.  Like the array, searching the array-based set will take 100 steps, as we inspect each element before concluding that the element isn’t there.

    3.  To insert into the set, we first need to conduct a full search to make sure the value doesn’t already exist within the set. This search will take 100 steps. Then we need to shift all 100 elements to the right to make room for the new value. Finally, we drop the new value at the beginning of the set. This is a total of 201 steps.

    4.  This insertion takes 101 steps. Again, we need to conduct a full search before inserting, which takes 100 steps. We then conclude with the final step of inserting the new value at the end of the set.

    5.  The deletion will take 100 steps, just like a classic array.

    6.  The deletion will take one step, just like a classic array.

3.  If the array contains N elements, searching for all instances of the string "apple" in an array will take N steps. When searching for just one instance, we can cut our search short as soon as we find it. But if we need to find all instances, we have no choice but to inspect each element of the entire array.

## Chapter 2

These are the solutions to the exercises found in the section [​*Exercises*​](#f_0030.xhtml_why.algorithms.matter.exercises).

1.  Linear search on this array would take four steps. We start at the beginning of the array and check each element from left to right. Because the 8 is the fourth number, we’ll find it in four steps.

2.  Binary search would take just one step in this case. We start the binary search at the middlemost element, and the 8 just happens to be the middlemost element!

3.  To solve this, we need to count how many times we halve 100,000 until we get down to 1\. If we keep dividing 100,000 by 2, we see that it takes us sixteen times until we get down to about 1.53\. If we halve this a seventeenth time, we get roughly 0.76, which is already below 1\. This suggests that in a worst-case scenario, it takes either sixteen or seventeen steps to perform binary search on 100,000 elements. If your answer is either sixteen or seventeen, it means you understand this concept well. Nice job!

    In practice, binary search takes sixteen steps. We can see this if we (tediously) walk through each step.

    Let’s start with 100,000 elements. When dealing with an even number of elements, there isn’t an exact item in the center. Instead, there are two central elements, and we arbitrarily search one of them. By searching this element, we’ve essentially taken it out of the picture, leaving behind 50,000 elements on one side of it and 49,999 on the other side. In the worst-case scenario, the value we’re searching for is among the 50,000 elements.

    Let’s perform a few more searches. Our second search leaves us with 25,000 elements. Our third search leaves 12,500 elements remaining. Our fourth search whittles down the elements to 6,250\. The fifth search leaves us with 3,125 elements.

    Now, this is the first time we’re encountering an odd number of elements. Here, there’s a single central element, and when we search it, each side will have 1,562 elements. Therefore, when doing the math for our next search, we can subtract 1 from 3,125 (since we’ve removed the central element from the picture) and divide 3,124 by 2\. This, as we noted, gives us 1,562.

    When we continue this pattern, it emerges that it takes sixteen steps to halve 100,000 until we find the value we’re searching for.

## Chapter 3

These are the solutions to the exercises found in the section [​*Exercises*​](#f_0039.xhtml_big.o.notation.exercises).

1.  This is O(1). We can consider N to be the year passed into the function. But no matter what the year is, the algorithm doesn’t vary in how many steps it takes.

2.  This is O(N). For N elements in the array, the loop will run N times.

3.  This is O(log N). In this case, N is the number numberOfGrains, which is passed into the function. The loop runs as long as placedGrains < numberOfGrains, but placedGrains starts at 1 and doubles each time the loop runs. If, for example, numberOfGrains was 256, we’d keep doubling the placedGrains nine times until we reach 256, meaning that our loop would run eight times for an N of 256\. If numberOfGrains was 512, our loop would run nine ...

## Chapter 4

These are the solutions to the exercises found in the section [​*Exercises*​](#f_0047.xhtml_speeding.up.your.code.with.big.o.exercises).

1.  Here is the completed table:

    | N Elements | O(N) | O(log N) | O(N²) |
    | --- | --- | --- | --- |
    | 100 | 100 | About 7 | 10,000 |
    | 2,000 | 2,000 | About 11 | 4,000,000 |

2.  The array would have sixteen elements since 16² is 256\. (Another way of saying this is that the square root of 256 is 16.)

3.  The algorithm has a time complexity of O(N²). N, in this case, is the size of the array. We have an outer loop that iterates over the array N times, and for each of those times, an inner loop iterates over the same array N times. This results in N² steps.

4.  The following version is O(N), as we only iterate through the array once:

    | ​  | ​**function**​ greatestNumber(array) { |
    | ​  | ​**if**​ (array.length === 0) { ​**return**​ ​**null**​; } |
    | ​  |  |
    | ​  | ​**let**​ greatestNumberSoFar ... |

## Chapter 5

These are the solutions to the exercises found in the section [​*Exercises*​](#f_0055.xhtml_optimizing.code.with.and.without.big.o.exercises).

1.  After dropping the constants, we can reduce the expression to O(N).

2.  After dropping the constant, we can reduce the expression to O(N²).

3.  This algorithm is one of O(N), with N being the size of the array. While there are two distinct loops that process the N elements, this is simply 2N, which is reduced to O(N) after dropping the constants.

1.  This algorithm is one of O(N), with N being the size of the array. Within the loop, we run three steps, which means our algorithm takes 3N steps. However, this is reduced to O(N) when we eliminate the constants.

2.  This algorithm is one of O(N²), with N being the size of the array. While we only run the inner loop half of the time, ...

## Chapter 6

These are the solutions to the exercises found in the section [​*Exercises*​](#f_0063.xhtml_optimizing.for.optimistic.scenarios.exercises).

1.  In Big O notation, 2N² + 2N + 1 gets reduced to O(N²). After getting rid of all the constants, we’re left with N² + N, but we also drop the N since it’s a lower order than N².

2.  Since log N is a lower order than N, it’s simply reduced to O(N).

3.  The important thing to note here is that the function ends as soon as we find a pair that sums to 10\. The best-case scenario, then, is when the first two numbers add up to 10, since we can end the function before the loops even get underway. An average-case scenario may be when the two numbers are somewhere in the middle of the array. The worst-case scenarios are when there aren’t any two numbers that add up to 10, in which case we must exhaust both loops completely. This worst-case scenario is O(N²), where N is the size of the array.

4.  This algorithm has an efficiency of O(N), as the size of the array is N, and the loop iterates through all N elements.

    This algorithm continues the loop even if it finds an “X” before the end of the array. We can make the code more efficient if we return true as soon as we find an “X”:

    | ​  | ​**function**​ containsX(string) { |
    | ​  | ​**for**​ (​**const**​ ​**char**​ ​**of**​ string) { |
    | ​  | ​**if**​ (​**char**​ === ​*'X'*​) { ​**return**​ ​**true**​; } |
    | ​  | } |
    | ​  |  |
    | ​  | ​**return**​ ​**false**​; |
    | ​  | } |

## Chapter 7

These are the solutions to the exercises found in the section [​*Exercises*​](#f_0075.xhtml_big.o.in.everyday.code.exercises).

1.  Here, N is the size of the array. Our loop runs for N / 2 times, as it processes two values each round of the loop. However, this is expressed as O(N) because we drop the constant.

2.  It’s slightly tricky to define N in this case since we’re dealing with two distinct arrays. The algorithm only processes each value once, so we could decide to call N the total number of values between both arrays, and the time complexity would be O(N). If we want to be more literal and call one array N and the other M, we could alternatively express the efficiency as O(N + M). However, because we’re simply adding N and M together, it’s simpler to just use N to refer to the total number ...

## Chapter 8

These are the solutions to the exercises found in the section [​*Exercises*​](#f_0086.xhtml_blazing.fast.lookup.with.hashes.exercises).

1.  The following implementation first stores the values of the first array in a hash table and then checks each value of the second array against that hash table:

    | ​  | ​**function**​ getIntersection(array1, array2) { |
    | ​  | ​**const**​ intersection = []; |
    | ​  | ​**const**​ hashTable = {}; |
    | ​  |  |
    | ​  | array1.forEach((value) => { |
    | ​  | hashTable[value] = ​**true**​; |
    | ​  | }); |
    | ​  |  |
    | ​  | array2.forEach((value) => { |
    | ​  | ​**if**​ (hashTable[value]) { |
    | ​  | intersection.push(value); |
    | ​  | } |
    | ​  | }); |
    | ​  |  |
    | ​  | ​**return**​ intersection; |
    | ​  | } |

    This algorithm has an efficiency of O(N).

2.  The following implementation checks each string in the array. If the string isn’t yet in the hash table, the string gets added. If the string is in the hash table, that ...

## Chapter 9

These are the solutions to the exercises found in the section [​*Exercises*​](#f_0095.xhtml_stacks.and.queues.exercises).

1.  Presumably, we’d want to be nice to the callers and answer their phone calls in the order in which they were received. For this we’d use a queue, which processes data FIFO (first in, first out).

2.  We’d be able to read the 4, which is now the top element in the stack. This is because we’ll have popped the 6 and the 5, which were previously sitting on top of the 4.

3.  We’d be able to read the 3, which is now at the front of the queue, after having dequeued the 1 and the 2.

4.  We can take advantage of the stack because of the fact that we pop each item in the reverse order of which they were pushed onto the stack. So we’ll first push each character of the string onto the stack. Then we’ll pop each one off while adding them to the end of a new string:

    | ​  | ​**import**​ Stack ​**from**​ ​*'./stack.js'*​; |
    | ​  |  |
    | ​  | ​**function**​ reverse(string) { |
    | ​  | ​**const**​ stack = ​**new**​ Stack(); |
    | ​  | ​**let**​ newString = ​*''*​; |
    | ​  |  |
    | ​  | ​**for**​ (​**const**​ ​**char**​ ​**of**​ string) { |
    | ​  | stack.push(​**char**​); |
    | ​  | } |
    | ​  |  |
    | ​  | ​**while**​ (stack.read()) { |
    | ​  | newString += stack.pop(); |
    | ​  | } |
    | ​  |  |
    | ​  | ​**return**​ newString; |
    | ​  | } |

    The Stack class imported at the beginning of our code is our homegrown Stack implementation from Chapter 9, which we’ve saved in a file called stack.js.

## Chapter 10

These are the solutions to the exercises found in the section [​*Exercises*​](#f_0103.xhtml_recursively.recurse.with.recursion.exercises).

1.  The base case is if (low > high)—that is, we want to stop the recursion once low has exceeded high. Otherwise, we’d end up printing numbers even greater than the high number, and onto infinity.

2.  We’d have infinite recursion! factorial(10) calls factorial(8), which calls factorial(6), which calls factorial(4), which calls factorial(2), which calls factorial(0). Since our base case is if (number === 1), we never end up with number ever being 1, so the recursion continues. factorial(0) calls factorial(-2), and so on.

3.  Let’s say low is 1 and high is 10\. When we call sum(1, 10), that in turn returns 10 + sum(1, 9). That is, we return the sum of 10 plus whatever the ...

## Chapter 11

These are the solutions to the exercises found in the section [​*Exercises*​](#f_0111.xhtml_learning.to.write.in.recursive.exercises).

1.  Let’s call our function characterCount. The first step is to pretend that the characterCount function has already been implemented.

    Next, we need to identify the subproblem. If our problem is the array ["ab", "c", "def", "ghij"], then our subproblem can be the same array missing one string. Let’s specifically say that our subproblem is the array minus the first string, which would be ["c", "def", "ghij"].

    Now, let’s see what happens when we apply the “already-implemented” function on the subproblem. If we were to call characterCount(["c", "def", "ghij"]), we’d get a return value of 8 since there are eight characters in total.

    So to solve our original problem, ...

## Chapter 12

These are the solutions to the exercises found in the section [​*Exercises*​](#f_0120.xhtml_dynamic.programming.exercises).

1.  The problem here is the function recursively calls itself twice each time it runs. Let’s make it so that it only calls itself once each time:

    | ​  | ​**function**​ addUntil100(array) { |
    | ​  | ​**if**​ (array.length === 0) { ​**return**​ 0; } |
    | ​  |  |
    | ​  | ​**const**​ sumOfRemainingNumbers = addUntil100(array.slice(1)); |
    | ​  |  |
    | ​  | ​**if**​ (array[0] + sumOfRemainingNumbers > 100) { |
    | ​  | ​**return**​ sumOfRemainingNumbers; |
    | ​  | } ​**else**​ { |
    | ​  | ​**return**​ array[0] + sumOfRemainingNumbers; |
    | ​  | } |
    | ​  | } |

2.  Here is the memoized version:

    | ​  | ​**function**​ golomb(n, memo = {}) { |
    | ​  | ​**if**​ (n === 1) { ​**return**​ 1; } |
    | ​  |  |
    | ​  | ​**if**​ (!memo[n]) { |
    | ​  | memo[n] = 1 + golomb(n - golomb(golomb(n - 1, memo), memo), memo); |
    | ​  | } |
    | ​  |  |
    | ​  | ​**return**​ memo[n]; |
    | ​  | } |

3.  To accomplish memoization here, we need to make a key that takes into account both the number of rows and the number of columns. To this end, we can make our key be based on the row and column together.

| ​  | ​**function**​ uniquePaths(rows, columns, memo = {}) { |
| ​  | ​**if**​ (rows === 1 &#124;&#124; columns === 1) { |
| ​  | ​**return**​ 1; |
| ​  | } |
| ​  |  |
| ​  | ​**if**​ (!memo[[rows, columns]]) { |
| ​  | memo[[rows, columns]] = (uniquePaths(rows - 1, columns, memo) |
| ​  | + uniquePaths(rows, columns - 1, memo)); |
| ​  | } |
| ​  |  |
| ​  | ​**return**​ memo[[rows, columns]]; |
| ​  | } |

## Chapter 13

These are the solutions to the exercises found in the section [​*Exercises*​](#f_0129.xhtml_divide.and.conquer.in.turbo.mode.exercises).

1.  If we sort the numbers, we know that the three greatest numbers will be at the end of the array, and we can just multiply them together. The sorting will take O(N log N):

    | ​  | ​**function**​ greatestProductOf3(array) { |
    | ​  | array.sort((a, b) => a - b); |
    | ​  |  |
    | ​  | ​**return**​ array[array.length - 1] * |
    | ​  | array[array.length - 2] * |
    | ​  | array[array.length - 3]; |
    | ​  | } |

    (This code takes for granted that there are at least three values in the array. You can add code to handle arrays where this is not the case.)

2.  If we presort the array, we can then expect each number to be at its own index. That is, the 0 should be at index 0, the 1 should be at index 1, and so on. We can then iterate through ...

## Chapter 14

These are the solutions to the exercises found in the section [​*Exercises*​](#f_0142.xhtml_pitting.linked.lists.against.arrays.exercises).

1.  One way we can do this is with a simple while loop:

    | ​  | printList() { |
    | ​  | ​**let**​ currentNode = ​**this**​.firstNode; |
    | ​  |  |
    | ​  | ​**while**​ (currentNode) { |
    | ​  | console.log(currentNode.data); |
    | ​  | currentNode = currentNode.nextNode; |
    | ​  | } |
    | ​  | } |

2.  With a doubly linked list, we have immediate access to the last nodes and can follow their “previous node” links to access the previous nodes. This code is basically the inverse of the previous exercise:

    | ​  | reversePrint() { |
    | ​  | ​**let**​ currentNode = ​**this**​.lastNode; |
    | ​  |  |
    | ​  | ​**while**​ (currentNode) { |
    | ​  | console.log(currentNode.data); |
    | ​  | currentNode = currentNode.previousNode; |
    | ​  | } |
    | ​  | } |

3.  Here, we use a while loop to move through each node. However, before we move forward, ...

## Chapter 15

These are the solutions to the exercises found in the section [​*Exercises*​](#f_0152.xhtml_binary.trees.exercises).

1.  The tree should look like this. Note that it’s not well balanced, as the root node only has a right subtree and no left one:

    ![images/binary_trees/solution_1.png](images/binary_trees/solution_1.png)
2.  Search within a balanced binary search tree takes a maximum of about log(N) steps. So, if N is 1,000, search should take a maximum of about 10 steps.

3.  The greatest value within a binary search tree will always be the bottom rightmost node. We can find it by recursively following each node’s right child until we hit the bottom:

    | ​  | ​**function**​ max(node) { |
    | ​  | ​**if**​ (node.rightChild) { |
    | ​  | ​**return**​ max(node.rightChild); |
    | ​  | } ​**else**​ { |
    | ​  | ​**return**​ node.value; ... |

## Chapter 16

These are the solutions to the exercises found in the section [​*Exercises*​](#f_0165.xhtml_heaps.exercises).

1.  After inserting an 11, the heap would look like this:

    ![images/heaps/solution_1.png](images/heaps/solution_1.png)
2.  After deleting the root node, the heap would look like this:

    ![images/heaps/solution_2.png](images/heaps/solution_2.png)
3.  The numbers would be in perfect descending order. (This is for a max-heap. For a min-heap, they’d be in ascending order.)

    Do you realize what this means? It means you’ve just discovered another sorting algorithm!

    Heapsort is a sorting algorithm that inserts all the values into a heap and then pops each one. As you can see from this exercise, the values ...

## Chapter 17

These are the solutions to the exercises found in the section [​*Exercises*​](#f_0176.xhtml_tries.exercises).

1.  This trie stores the words: “tag”, “tan”, “tank”, “tap”, “today”, “total”, “we”, “well”, and “went”.

2.  Here is a trie that stores the words “get”, “go”, “got”, “gotten”, “hall”, “ham”, “hammer”, “hill”, and “zebra”:

    ![images/tries/solution_2.png](images/tries/solution_2.png)
3.  The following code starts at the trie’s node and iterates over each of its children. For each child, it prints the key and then recursively calls itself on the child node:

    | ​  | traverse(node = ​**null**​) { |
    | ​  | ​**const**​ currentNode = node &#124;&#124; ​**this**​.root; |
    | ​  |  |
    | ​  | ​**for**​ (​**const**​ [key, childNode] ​**of**​ Object.entries(currentNode.children)) { |
    | ​  | console.log(key); |
    | ​  |  |
    | ​  | ​**if**​ (key !== ​*'*'*​) { |
    | ​  | ​**this**​.traverse(childNode); |
    | ​  | } |
    | ​  | } |
    | ​  | } |

4.  Our autocorrect implementation is a combination of the search and collectAllWords functions:

    | ​  | autocorrect(word) { |
    | ​  | ​**let**​ currentNode = ​**this**​.root; |
    | ​  | ​**let**​ wordFoundSoFar = ​*''*​; |
    | ​  |  |
    | ​  | ​**for**​ (​**const**​ ​**char**​ ​**of**​ word) { |
    | ​  | ​**if**​ (currentNode.children[​**char**​]) { |
    | ​  | wordFoundSoFar += ​**char**​; |
    | ​  | currentNode = currentNode.children[​**char**​]; |
    | ​  | } ​**else**​ { |
    | ​  | ​**return**​ wordFoundSoFar + ​**this**​.collectAllWords([], currentNode)[0]; |
    | ​  | } |
    | ​  | } |
    | ​  |  |
    | ​  | ​**return**​ word; |
    | ​  | } |

    The basic approach is that we first search the trie to find as much of the prefix as we can. When we hit a dead end, instead of just returning null (as the search function does), we call collectAllWords on the current node to collect all the suffixes that stem from that node. We then use the first suffix of the array and concatenate it with the prefix to suggest a new word to the user.

## Chapter 18

These are the solutions to the exercises found in the section [​*Exercises*​](#f_0188.xhtml_graphs.exercises).

1.  If a user is browsing “nails”, the website will recommend “nail polish”, “needles”, “pins”, and “hammer”.

2.  The order of depth-first search would be A-B-E-J-F-O-C-G-K-D-H-L-M-I-N-P, as seen in the following image:

    ![images/graphs/solution_2_graph.png](images/graphs/solution_2_graph.png)
3.  The order of breadth-first search would be A-B-C-D-E-F-G-H-I-J-K-L-M-N-O-P, as seen in the following image:

    ![images/graphs/solution_3_graph.png](images/graphs/solution_3_graph.png)
4.  Following is an implementation of breadth-first search:

    | ​  | ​**import**​ Queue ​**from**​ ​*'./queue_implementation.js'*​; |
    | ​  |  |
    | ​  | ​**function**​ bfs(startingVertex, searchValue) { |
    | ​  | ​**const**​ queue = ​**new**​ Queue(); |
    | ​  | ​**const**​ visitedVertices = {}; |
    | ​  | visitedVertices[startingVertex.value] = ​**true**​; |
    | ​  | queue.enqueue(startingVertex); |
    | ​  |  |
    | ​  | ​**while**​ (queue.read()) { |
    | ​  | ​**const**​ currentVertex = queue.dequeue(); |
    | ​  | ​**if**​ (currentVertex.value === searchValue) { |
    | ​  | ​**return**​ currentVertex; |
    | ​  | } |
    | ​  |  |
    | ​  | ​**for**​ (​**const**​ adjacentVertex ​**of**​ currentVertex.adjacentVertices) { |
    | ​  | ​**if**​ (!visitedVertices[adjacentVertex.value]) { |
    | ​  | visitedVertices[adjacentVertex.value] = ​**true**​; |
    | ​  | queue.enqueue(adjacentVertex); |
    | ​  | } |
    | ​  | } |
    | ​  | } |
    | ​  |  |
    | ​  | ​**return**​ ​**null**​; |
    | ​  | } |

5.  To find the shortest path in an unweighted graph, we’re going to use breadth-first search. The main feature of breadth-first search is that it stays close to the starting vertex as long as possible. This feature will serve as the key to finding the shortest path.

    Let’s apply this to our social-networking example. Because breadth-first search stays close to Idris as long as possible, we’ll end up finding Lina first through the shortest possible path. Only later on in the search would we end up finding Lina through longer paths. In fact, we can even stop the search as soon we as find Lina. (Our implementation that follows doesn’t end early, but you can modify it to do so.)

    As we visit each vertex for the first time, then, we know that the current vertex is always part of the shortest path from the starting vertex to the vertex we’re visiting. (Remember, with BFS, the current vertex and the vertex we’re visiting aren’t necessarily the same.)

    For example, when we visit Lina for the first time, Kamil will be the current vertex. This is because in BFS, we’ll get to Lisa first through Kamil before we get to her through Sasha. When we do visit Lina (through Kamil), we can store in a table that the shortest path from Idris to Lina will be through Kamil. This table is similar to the cheapestPreviousStopoverCityTable from Dijkstra’s algorithm.

    In fact, whenever we visit any vertex, the shortest path from Idris to that vertex will be through the current vertex. We’ll store all of this data in a table called previousVertexTable.

    Finally, we can then use this data to work backward from Lina to Idris to build the precise shortest path between the two of them.

Here’s our implementation:

| ​  | ​**import**​ Queue ​**from**​ ​*'./queue_implementation.js'*​; |
| ​  |  |
| ​  | ​**function**​ findShortestPath(firstVertex, secondVertex, visitedVertices) { |
| ​  | ​**const**​ queue = ​**new**​ Queue(); |
| ​  | ​**const**​ previousVertexTable = {}; |
| ​  |  |
| ​  | visitedVertices[firstVertex.value] = ​**true**​; |
| ​  | queue.enqueue(firstVertex); |
| ​  |  |
| ​  | ​**while**​ (queue.read()) { |
| ​  | ​**const**​ currentVertex = queue.dequeue(); |
| ​  |  |
| ​  | ​**for**​ (​**const**​ adjacentVertex ​**of**​ currentVertex.adjacentVertices) { |
| ​  | ​**if**​ (!visitedVertices[adjacentVertex.value]) { |
| ​  | visitedVertices[adjacentVertex.value] = ​**true**​; |
| ​  | queue.enqueue(adjacentVertex); |
| ​  | previousVertexTable[adjacentVertex.value] = currentVertex.value; |
| ​  | } |
| ​  | } |
| ​  | } |
| ​  |  |
| ​  | ​**const**​ shortestPath = []; |
| ​  | ​**let**​ currentVertexValue = secondVertex.value; |
| ​  |  |
| ​  | ​**while**​ (currentVertexValue !== firstVertex.value) { |
| ​  | shortestPath.unshift(currentVertexValue); |
| ​  | currentVertexValue = previousVertexTable[currentVertexValue]; |
| ​  | } |
| ​  |  |
| ​  | shortestPath.unshift(firstVertex.value); |
| ​  |  |
| ​  | ​**return**​ shortestPath; |
| ​  | } |

## Chapter 19

These are the solutions to the exercises found in the section [​*Exercises*​](#f_0194.xhtml_dealing.with.space.constraints.exercises).

1.  The space complexity is O(N²). This is because the function creates the array called collection, which will end up holding N² strings.

2.  This implementation takes up O(N) space, as we create a newArray containing N items.

3.  The following implementation uses this algorithm: we swap the first item with the last item in place. Then we swap the second item with the second-to-last item in place. We then proceed to swap the third item with the third-to-last item in place, and so on. Since everything is done in place and we don’t create any new data, this has a space complexity of O(1).

| ​  | ​**function**​ reverse(array) { |
| ​  | ​**let**​ i = 0; |
| ​  |  |
| ​  | ​**while**​ (i < Math.floor(array.length / 2)) { |
| ​  | ​**const**​ mirrorOfI = array.length - 1 - i; |
| ​  | [array[i], array[mirrorOfI]] = [array[mirrorOfI], array[i]]; |
| ​  |  |
| ​  | i += 1; |
| ​  | } |
| ​  |  |
| ​  | ​**return**​ array; |
| ​  | } |

(While JavaScript may, under the hood, be creating a temporary variable to accomplish each swap, we never have more than that one piece of data stored at any time during the algorithm’s execution.)

1.  Here’s the completed table:

    | Version | Time Complexity | Space Complexity |
    | --- | --- | --- |
    | Version #1 | O(N) | O(N) |
    | Version #2 | O(N) | O(1) |
    | Version #3 | O(N) | O(N) |

    All three versions run for as many steps as there are numbers in the array, so the time complexity is O(N) for all of them.

    Version #1 creates a brand-new array to store the doubled numbers. This array will have the same length as the original array, so takes up O(N) space.

    Version #2 modifies the original array in place, so takes up zero extra space. This is expressed as O(1).

    Version #3 also modifies the original array in place. However, since the function is recursive, the call stack at its peak will have N calls on it, taking up O(N) space.

## Chapter 20

These are the solutions to the exercises found in the section [​*Exercises*​](#f_0204.xhtml_tips.for.code.optimization.exercises).

1.  We can optimize this algorithm if we ask ourselves, “If I could magically find a desired piece of information in O(1) time, can I make my algorithm faster?”

    Specifically, as we iterate over one array, we’d want to “magically” look up that athlete from the other array in O(1) time. To accomplish this, we can first transform one of the arrays into a hash table. We’ll use the full name (that is, the first and last name) as the key, and true (or any arbitrary item) as the value.

    Once we’ve turned one array into this hash table, we then iterate over the other array. As we encounter each athlete, we do an O(1) lookup in the hash table to see if that athlete already ...

## You May Be Interested In…

*Select a cover for more information*

### A Common-Sense Guide to Data Structures and Algorithms, Second Edition

[![](images/_covers/jwdsal2.jpg)](http://pragmaticprogrammer.com/titles/jwdsal2)

If you thought that data structures and algorithms were all just theory, you’re missing out on what they can do for your code. Learn to use Big O notation to make your code run faster by orders of magnitude. Choose from data structures such as hash tables, trees, and graphs to increase your code’s efficiency exponentially. With simple language and clear diagrams, this book makes this complex topic accessible, no matter your background. This new edition features practice exercises in every chapter, and new chapters on topics such as dynamic programming and heaps and tries. Get the hands-on info you need to master data structures and algorithms for your day-to-day work.

Jay Wengrow

(506 pages) ISBN: 9781680507225 $45.95

### JavaScript Brain Teasers

[![](images/_covers/fkjsbrain.jpg)](http://pragmaticprogrammer.com/titles/fkjsbrain)

If you’ve ever felt the exhilaration of cracking a thorny problem or the joy of witnessing elegant code that challenges your mind, then this book is tailor-made for you. Prepare yourself to dive into a diverse array of mind-bending JavaScript brain teasers. Each puzzle is more than just a code exercise; it’s a gateway to unlocking new insights and honing your abilities. As you work through the challenges, you’ll learn to think pragmatically, optimize your code for efficiency, and avoid hidden pitfalls that can catch you off guard. What’s more—the puzzle format will help you remember what you’ve learned!

Faraz K. Kelhini

(128 pages) ISBN: 9798888650523 $32.95

### Text Processing with JavaScript

[![](images/_covers/fkjavascript.jpg)](http://pragmaticprogrammer.com/titles/fkjavascript)

You might think of regular expressions as the holy grail of text processing, but are you sure you aren’t just shoehorning them in where standard built-in solutions already exist and would work better? JavaScript itself provides programmers with excellent methods for text manipulation, and knowing how and when to use them will help you write more efficient and performant code. From extracting data from APIs to calculating word counts and everything in between, discover how to pick the right tool for the job and make the absolute most of it every single time.

Faraz K. Kelhini

(240 pages) ISBN: 9798888650332 $51.95

### Programming WebRTC

[![](images/_covers/ksrtc.jpg)](http://pragmaticprogrammer.com/titles/ksrtc)

Build your own video chat application—but that’s just the beginning. With WebRTC, you’ll create real-time applications to stream any kind of user media and data directly from one browser to another, all built on familiar HTML, CSS, and JavaScript. Power real-time activities like text-based chats, secure peer-to-peer file transfers, collaborative brainstorming sessions—even multiplayer gaming. And you’re not limited to two connected users: an entire chapter of the book is devoted to engineering multipeer WebRTC apps that let groups of people communicate in real time. You’ll create your own video conferencing app. It’s all here.

Karl Stolley

(266 pages) ISBN: 9781680509038 $45.95

### Small, Sharp Software Tools

[![](images/_covers/bhcldev.jpg)](http://pragmaticprogrammer.com/titles/bhcldev)

The command-line interface is making a comeback. That’s because developers know that all the best features of your operating system are hidden behind a user interface designed to help average people use the computer. But you’re not the average user, and the CLI is the most efficient way to get work done fast. Turn tedious chores into quick tasks: read and write files, manage complex directory hierarchies, perform network diagnostics, download files, work with APIs, and combine individual programs to create your own workflows. Put down that mouse, open the CLI, and take control of your software development environment.

Brian P. Hogan

(326 pages) ISBN: 9781680502961 $38.95

### Programming Kotlin

[![](images/_covers/vskotlin.jpg)](http://pragmaticprogrammer.com/titles/vskotlin)

Programmers don’t just use Kotlin, they love it. Even Google has adopted it as a first-class language for Android development. With Kotlin, you can intermix imperative, functional, and object-oriented styles of programming and benefit from the approach that’s most suitable for the problem at hand. Learn to use the many features of this highly concise, fluent, elegant, and expressive statically typed language with easy-to-understand examples. Learn to write maintainable, high-performing JVM and Android applications, create DSLs, program asynchronously, and much more.

Venkat Subramaniam

(460 pages) ISBN: 9781680506358 $51.95

### Modern Front-End Development for Rails, Second Edition

[![](images/_covers/nrclient2.jpg)](http://pragmaticprogrammer.com/titles/nrclient2)

Improve the user experience for your Rails app with rich, engaging client-side interactions. Learn to use the Rails 7 tools and simplify the complex JavaScript ecosystem. It’s easier than ever to build user interactions with Hotwire, Turbo, and Stimulus. You can add great front-end flair without much extra complication. Use React to build a more complex set of client-side features. Structure your code for different levels of client-side needs with these powerful options. Add to your toolkit today!

Noel Rappin

(408 pages) ISBN: 9781680509618 $55.95

### Agile Web Development with Rails 7

[![](images/_covers/rails7.jpg)](http://pragmaticprogrammer.com/titles/rails7)

Rails 7 completely redefines what it means to produce fantastic user experiences and provides a way to achieve all the benefits of single-page applications – at a fraction of the complexity. Rails 7 integrates the Hotwire frameworks of Stimulus and Turbo directly as the new defaults, together with that hot newness of import maps. The result is a toolkit so powerful that it allows a single individual to create modern applications upon which they can build a competitive business. The way it used to be.

Sam Ruby

(474 pages) ISBN: 9781680509298 $59.95

### Docker for Rails Developers

[![](images/_covers/ridocker.jpg)](http://pragmaticprogrammer.com/titles/ridocker)

Docker does for DevOps what Rails did for web development—it gives you a new set of superpowers. Gone are “works on my machine” woes and lengthy setup tasks, replaced instead by a simple, consistent, Docker-based development environment that will have your team up and running in seconds. Gain hands-on, real-world experience with a tool that’s rapidly becoming fundamental to software development. Go from zero all the way to production as Docker transforms the massive leap of deploying your app in the cloud into a baby step.

Rob Isenberg

(238 pages) ISBN: 9781680502732 $35.95

### Rediscovering JavaScript

[![](images/_covers/ves6.jpg)](http://pragmaticprogrammer.com/titles/ves6)

JavaScript is no longer to be feared or loathed—the world’s most popular and ubiquitous language has evolved into a respectable language. Whether you’re writing front-end applications or server-side code, the phenomenal features from ES6 and beyond—like the rest operator, generators, destructuring, object literals, arrow functions, modern classes, promises, async, and metaprogramming capabilities—will get you excited and eager to program with JavaScript. You’ve found the right book to get started quickly and dive deep into the essence of modern JavaScript. Learn practical tips to apply the elegant parts of the language and the gotchas to avoid.

Venkat Subramaniam

(286 pages) ISBN: 9781680505467 $45.95

* * *
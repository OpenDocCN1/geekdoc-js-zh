![](cover.jpeg)

![](images/00001.jpeg)

Programming for Beginners

2 Books in 1:

Arduino Programming for Beginners

Javascript for Beginners

Text Copyright © [Matthew Python]
All rights reserved. No part of this guide may be reproduced in any form without permission in writing from the publisher except in the case of brief quotations embodied in critical articles or reviews.

Legal & Disclaimer

The information contained in this book and its contents is not designed to replace or take the place of any form of medical or professional advice; and is not meant to replace the need for independent medical, financial, legal or other professional advice or services, as may be required. The content and information in this book has been provided for educational and entertainment purposes only.

The content and information contained in this book has been compiled from sources deemed reliable, and it is accurate to the best of the Author's knowledge, information and belief. However, the Author cannot guarantee its accuracy and validity and cannot be held liable for any errors and/or omissions. Further, changes are periodically made to this book as and when needed. Where appropriate and/or necessary, you must consult a professional (including but not limited to your doctor, attorney, financial advisor or such other professional advisor) before using any of the suggested remedies, techniques, or information in this book.

Upon using the contents and information contained in this book, you agree to hold harmless the Author from and against any damages, costs, and expenses, including any legal fees potentially resulting from the application of any of the information provided by this book. This disclaimer applies to any loss, damages or injury caused by the use and application, whether directly or indirectly, of any advice or information presented, whether for breach of contract, tort, negligence, personal injury, criminal intent, or under any other cause of action.

You agree to accept all risks of using the information presented inside this book.

You agree that by continuing to read this book, where appropriate and/or necessary, you shall consult a professional (including but not limited to your doctor, attorney, or financial advisor or such other advisor as needed) before using any of the suggested remedies, techniques, or information in this book.

Table of Contents

Arduino Programming for Beginners

[INTRODUCTION](#part0000_split_004.html__Toc29578491)

[Chapter 1:What is Arduino?](#part0000_split_005.html__Toc29578492)

[History of Arduino](#part0000_split_005.html__Toc29578493)

[But what is Arduino?](#part0000_split_005.html__Toc29578494)

[Who Uses Arduino?](#part0000_split_005.html__Toc29578495)

[Chapter 2:Understanding of Arduino](#part0000_split_006.html__Toc29578496)

[Key terms related to Arduino](#part0000_split_006.html__Toc29578497)

[Chapter 3: Anatomy of Arduino Board](#part0000_split_007.html__Toc29578498)

[Chapter 4: Arduino Family](#part0000_split_008.html__Toc29578499)

[Chapter 5: Explanation of Arduino Components](#part0000_split_009.html__Toc29578500)

[Chapter 6: Getting started with Arduino](#part0000_split_010.html__Toc29578501)

[Installing the Arduino IDE](#part0000_split_010.html__Toc29578502)

[Digital Input/Output](#part0000_split_010.html__Toc29578503)

[Chapter 7: Basic digital Arduino programs](#part0000_split_011.html__Toc29578504)

[LED Blink](#part0000_split_011.html__Toc29578505)

[LED Blink without Delay](#part0000_split_011.html__Toc29578506)

[Fading an LED](#part0000_split_011.html__Toc29578507)

[Arduino Button](#part0000_split_011.html__Toc29578508)

[Arduino Pushbutton as a Debounce](#part0000_split_011.html__Toc29578509)

[Creating a Loop](#part0000_split_011.html__Toc29578510)

[Chapter 8:Basic analog Arduino programs](#part0000_split_012.html__Toc29578511)

[Analog Input](#part0000_split_012.html__Toc29578512)

[Knock Sensor](#part0000_split_012.html__Toc29578513)

[Arduino Smoothing](#part0000_split_012.html__Toc29578514)

[Printing Analog Input (Graphing)](#part0000_split_012.html__Toc29578515)

[Chapter 9: Arduino programming tools](#part0000_split_013.html__Toc29578516)

[Arduino Control Statements](#part0000_split_013.html__Toc29578517)

[Arduino Programming Loops](#part0000_split_013.html__Toc29578518)

[Chapter 10: Input, Outputs, and Sensor](#part0000_split_014.html__Toc29578519)

[Advanced Strategies for Arduino](#part0000_split_014.html__Toc29578520)

[Chapter 11: Arduino function libraries](#part0000_split_015.html__Toc29578521)

[I/O Function; advanced I/O function; etc.](#part0000_split_015.html__Toc29578522)

[Functions in Arduino](#part0000_split_015.html__Toc29578523)

[INPUT Pins](#part0000_split_015.html__Toc29578524)

[Output Pins](#part0000_split_015.html__Toc29578525)

[The digitalWrite() Function](#part0000_split_015.html__Toc29578526)

[The analogRead() Function](#part0000_split_015.html__Toc29578527)

[The analogReference() Function](#part0000_split_015.html__Toc29578528)

[Character Functions](#part0000_split_015.html__Toc29578529)

[Conditional Operator](#part0000_split_015.html__Toc29578530)

[Chapter 12: Computer interfacing with an Arduino](#part0000_split_016.html__Toc29578531)

[The FTDI Chips; Example of Temperature sensors with serial interface](#part0000_split_016.html__Toc29578532)

[Chapter 13: C language Basics](#part0000_split_017.html__Toc29578533)

[The Memory Maps](#part0000_split_017.html__Toc29578534)

[Chapter 14: Arduino clones and similar boards](#part0000_split_018.html__Toc29578535)

[Chapter 15: Troubleshooting](#part0000_split_019.html__Toc29578536)

[Arduino Board Testing](#part0000_split_019.html__Toc29578537)

[Breadboard Circuit Testing](#part0000_split_019.html__Toc29578538)

[Problem Identification](#part0000_split_019.html__Toc29578539)

[Problem Isolation and Solving](#part0000_split_019.html__Toc29578540)

[Online Help](#part0000_split_019.html__Toc29578541)

[CONCLUSION](#part0000_split_020.html__Toc29578542)

JavaScript for Beginners

[INTRODUCTION](#part0000_split_021.html__Toc29452702)

[Chapter 1:What is Javascript?](#part0000_split_022.html__Toc29452703)

[What is JavaScript?](#part0000_split_022.html__Toc29452704)

[Why to learn JavaScript](#part0000_split_022.html__Toc29452705)

[What is HTML?](#part0000_split_022.html__Toc29452706)

[How to include JavaScript in XHTML](#part0000_split_022.html__Toc29452707)

[JavaScript and Browsers](#part0000_split_022.html__Toc29452708)

[Basic Glossary](#part0000_split_022.html__Toc29452709)

[Chapter 2:Why JavaScript?](#part0000_split_023.html__Toc29452710)

[Python Vs Javascript: Which One Is Better For Web](#part0000_split_023.html__Toc29452711)

[characteristics of JavaScript](#part0000_split_023.html__Toc29452712)

[Advantages of JavaScript](#part0000_split_023.html__Toc29452713)

[Limitations of JavaScript](#part0000_split_023.html__Toc29452714)

[The two Types of JavaScript Execution](#part0000_split_023.html__Toc29452715)

[Parameters And Ideal Test Environment](#part0000_split_023.html__Toc29452716)

[Syntax](#part0000_split_023.html__Toc29452717)

[The Code Syntax Rules](#part0000_split_023.html__Toc29452718)

[Creating A Personal Library Of Javascript](#part0000_split_023.html__Toc29452719)

[JavaScript examples](#part0000_split_023.html__Toc29452720)

[Chapter 3: Basic Programming structure](#part0000_split_024.html__Toc29452721)

[VariableS](#part0000_split_024.html__Toc29452722)

[Global and Local Variables](#part0000_split_024.html__Toc29452723)

[Types of variables](#part0000_split_024.html__Toc29452724)

[One Statement, Several Variables](#part0000_split_024.html__Toc29452725)

[JavaScript Booleans](#part0000_split_024.html__Toc29452726)

[operators](#part0000_split_024.html__Toc29452727)

[String Operators](#part0000_split_024.html__Toc29452728)

[Adding Strings and Numbers](#part0000_split_024.html__Toc29452729)

[Comparison Operators](#part0000_split_024.html__Toc29452730)

[If/else statement](#part0000_split_024.html__Toc29452731)

[Booleans Can be Objects](#part0000_split_024.html__Toc29452732)

[Flow control structure](#part0000_split_024.html__Toc29452733)

[Function and basic properties of JavaScript](#part0000_split_024.html__Toc29452734)

[Chapter 4: Advanced Programing structure](#part0000_split_025.html__Toc29452735)

[Functions and scope of the variables](#part0000_split_025.html__Toc29452736)

[The “break” Statement](#part0000_split_025.html__Toc29452737)

[The “for… of” Statement](#part0000_split_025.html__Toc29452738)

[The “for… in” Statement](#part0000_split_025.html__Toc29452739)

[The “continue” Statement](#part0000_split_025.html__Toc29452740)

[ Other Control Structures](#part0000_split_025.html__Toc29452741)

[Chapter 5: Data Structures: Objects & Arrays](#part0000_split_026.html__Toc29452742)

[Introduction to Objects](#part0000_split_026.html__Toc29452743)

[Introduction to Object Oriented Programming: Classes](#part0000_split_026.html__Toc29452744)

[Overloading Operators](#part0000_split_026.html__Toc29452745)

[Inheritance between Classes](#part0000_split_026.html__Toc29452746)

[Implementing Polymorphism](#part0000_split_026.html__Toc29452747)

[Custom Constructors](#part0000_split_026.html__Toc29452748)

[Using Object Literal](#part0000_split_026.html__Toc29452749)

[Node tree](#part0000_split_026.html__Toc29452750)

[Arrays](#part0000_split_026.html__Toc29452751)

[Prototypal inheritance](#part0000_split_026.html__Toc29452752)

[Prototype](#part0000_split_026.html__Toc29452753)

[Chapter 6: Higher-order Functions](#part0000_split_027.html__Toc29452754)

[Transforming with map; strings and character codes.](#part0000_split_027.html__Toc29452755)

[Transforming with map](#part0000_split_027.html__Toc29452756)

[Strings and character codes](#part0000_split_027.html__Toc29452757)

[Chapter 7: What is JavaScript cookies](#part0000_split_028.html__Toc29452758)

[Explain how to create, read and delete cookies.](#part0000_split_028.html__Toc29452759)

[CONCLUSION](#part0000_split_029.html__Toc29452760)

Arduino Programming For Beginners

How to learn and understand Arduino hardware and software as well as the fundamental electronic concepts with this beginner’s guide. Getting started Arduino sketches

[Matthew Python]

Text Copyright © [Matthew Python]
All rights reserved. No part of this guide may be reproduced in any form without permission in writing from the publisher except in the case of brief quotations embodied in critical articles or reviews.

Legal & Disclaimer

The information contained in this book and its contents is not designed to replace or take the place of any form of medical or professional advice; and is not meant to replace the need for independent medical, financial, legal or other professional advice or services, as may be required. The content and information in this book has been provided for educational and entertainment purposes only.

The content and information contained in this book has been compiled from sources deemed reliable, and it is accurate to the best of the Author's knowledge, information and belief. However, the Author cannot guarantee its accuracy and validity and cannot be held liable for any errors and/or omissions. Further, changes are periodically made to this book as and when needed. Where appropriate and/or necessary, you must consult a professional (including but not limited to your doctor, attorney, financial advisor or such other professional advisor) before using any of the suggested remedies, techniques, or information in this book.

Upon using the contents and information contained in this book, you agree to hold harmless the Author from and against any damages, costs, and expenses, including any legal fees potentially resulting from the application of any of the information provided by this book. This disclaimer applies to any loss, damages or injury caused by the use and application, whether directly or indirectly, of any advice or information presented, whether for breach of contract, tort, negligence, personal injury, criminal intent, or under any other cause of action.

You agree to accept all risks of using the information presented inside this book.

You agree that by continuing to read this book, where appropriate and/or necessary, you shall consult a professional (including but not limited to your doctor, attorney, or financial advisor or such other advisor as needed) before using any of the suggested remedies, techniques, or information in this book.

Table of Contents

[INTRODUCTION](#part0000_split_004.html__Toc29578491)

[Chapter 1:What is Arduino?](#part0000_split_005.html__Toc29578492)

[History of Arduino](#part0000_split_005.html__Toc29578493)

[But what is Arduino?](#part0000_split_005.html__Toc29578494)

[Who Uses Arduino?](#part0000_split_005.html__Toc29578495)

[Chapter 2:Understanding of Arduino](#part0000_split_006.html__Toc29578496)

[Key terms related to Arduino](#part0000_split_006.html__Toc29578497)

[Chapter 3: Anatomy of Arduino Board](#part0000_split_007.html__Toc29578498)

[Chapter 4: Arduino Family](#part0000_split_008.html__Toc29578499)

[Chapter 5: Explanation of Arduino Components](#part0000_split_009.html__Toc29578500)

[Chapter 6: Getting started with Arduino](#part0000_split_010.html__Toc29578501)

[Installing the Arduino IDE](#part0000_split_010.html__Toc29578502)

[Digital Input/Output](#part0000_split_010.html__Toc29578503)

[Chapter 7: Basic digital Arduino programs](#part0000_split_011.html__Toc29578504)

[LED Blink](#part0000_split_011.html__Toc29578505)

[LED Blink without Delay](#part0000_split_011.html__Toc29578506)

[Fading an LED](#part0000_split_011.html__Toc29578507)

[Arduino Button](#part0000_split_011.html__Toc29578508)

[Arduino Pushbutton as a Debounce](#part0000_split_011.html__Toc29578509)

[Creating a Loop](#part0000_split_011.html__Toc29578510)

[Chapter 8:Basic analog Arduino programs](#part0000_split_012.html__Toc29578511)

[Analog Input](#part0000_split_012.html__Toc29578512)

[Knock Sensor](#part0000_split_012.html__Toc29578513)

[Arduino Smoothing](#part0000_split_012.html__Toc29578514)

[Printing Analog Input (Graphing)](#part0000_split_012.html__Toc29578515)

[Chapter 9: Arduino programming tools](#part0000_split_013.html__Toc29578516)

[Arduino Control Statements](#part0000_split_013.html__Toc29578517)

[Arduino Programming Loops](#part0000_split_013.html__Toc29578518)

[Chapter 10: Input, Outputs, and Sensor](#part0000_split_014.html__Toc29578519)

[Advanced Strategies for Arduino](#part0000_split_014.html__Toc29578520)

[Chapter 11: Arduino function libraries](#part0000_split_015.html__Toc29578521)

[I/O Function; advanced I/O function; etc.](#part0000_split_015.html__Toc29578522)

[Functions in Arduino](#part0000_split_015.html__Toc29578523)

[INPUT Pins](#part0000_split_015.html__Toc29578524)

[Output Pins](#part0000_split_015.html__Toc29578525)

[The digitalWrite() Function](#part0000_split_015.html__Toc29578526)

[The analogRead() Function](#part0000_split_015.html__Toc29578527)

[The analogReference() Function](#part0000_split_015.html__Toc29578528)

[Character Functions](#part0000_split_015.html__Toc29578529)

[Conditional Operator](#part0000_split_015.html__Toc29578530)

[Chapter 12: Computer interfacing with an Arduino](#part0000_split_016.html__Toc29578531)

[The FTDI Chips; Example of Temperature sensors with serial interface](#part0000_split_016.html__Toc29578532)

[Chapter 13: C language Basics](#part0000_split_017.html__Toc29578533)

[The Memory Maps](#part0000_split_017.html__Toc29578534)

[Chapter 14: Arduino clones and similar boards](#part0000_split_018.html__Toc29578535)

[Chapter 15: Troubleshooting](#part0000_split_019.html__Toc29578536)

[Arduino Board Testing](#part0000_split_019.html__Toc29578537)

[Breadboard Circuit Testing](#part0000_split_019.html__Toc29578538)

[Problem Identification](#part0000_split_019.html__Toc29578539)

[Problem Isolation and Solving](#part0000_split_019.html__Toc29578540)

[Online Help](#part0000_split_019.html__Toc29578541)

[CONCLUSION](#part0000_split_020.html__Toc29578542)

JavaScript for Beginners [INTRODUCTION](#part0000_split_021.html__Toc29452702)

[Chapter 1:What is Javascript?](#part0000_split_022.html__Toc29452703)

[What is JavaScript?](#part0000_split_022.html__Toc29452704)

[Why to learn JavaScript](#part0000_split_022.html__Toc29452705)

[What is HTML?](#part0000_split_022.html__Toc29452706)

[How to include JavaScript in XHTML](#part0000_split_022.html__Toc29452707)

[JavaScript and Browsers](#part0000_split_022.html__Toc29452708)

[Basic Glossary](#part0000_split_022.html__Toc29452709)

[Chapter 2:Why JavaScript?](#part0000_split_023.html__Toc29452710)

[Python Vs Javascript: Which One Is Better For Web](#part0000_split_023.html__Toc29452711)

[characteristics of JavaScript](#part0000_split_023.html__Toc29452712)

[Advantages of JavaScript](#part0000_split_023.html__Toc29452713)

[Limitations of JavaScript](#part0000_split_023.html__Toc29452714)

[The two Types of JavaScript Execution](#part0000_split_023.html__Toc29452715)

[Parameters And Ideal Test Environment](#part0000_split_023.html__Toc29452716)

[Syntax](#part0000_split_023.html__Toc29452717)

[The Code Syntax Rules](#part0000_split_023.html__Toc29452718)

[Creating A Personal Library Of Javascript](#part0000_split_023.html__Toc29452719)

[JavaScript examples](#part0000_split_023.html__Toc29452720)

[Chapter 3: Basic Programming structure](#part0000_split_024.html__Toc29452721)

[VariableS](#part0000_split_024.html__Toc29452722)

[Global and Local Variables](#part0000_split_024.html__Toc29452723)

[Types of variables](#part0000_split_024.html__Toc29452724)

[One Statement, Several Variables](#part0000_split_024.html__Toc29452725)

[JavaScript Booleans](#part0000_split_024.html__Toc29452726)

[operators](#part0000_split_024.html__Toc29452727)

[String Operators](#part0000_split_024.html__Toc29452728)

[Adding Strings and Numbers](#part0000_split_024.html__Toc29452729)

[Comparison Operators](#part0000_split_024.html__Toc29452730)

[If/else statement](#part0000_split_024.html__Toc29452731)

[Booleans Can be Objects](#part0000_split_024.html__Toc29452732)

[Flow control structure](#part0000_split_024.html__Toc29452733)

[Function and basic properties of JavaScript](#part0000_split_024.html__Toc29452734)

[Chapter 4: Advanced Programing structure](#part0000_split_025.html__Toc29452735)

[Functions and scope of the variables](#part0000_split_025.html__Toc29452736)

[The “break” Statement](#part0000_split_025.html__Toc29452737)

[The “for… of” Statement](#part0000_split_025.html__Toc29452738)

[The “for… in” Statement](#part0000_split_025.html__Toc29452739)

[The “continue” Statement](#part0000_split_025.html__Toc29452740)

[ Other Control Structures](#part0000_split_025.html__Toc29452741)

[Chapter 5: Data Structures: Objects & Arrays](#part0000_split_026.html__Toc29452742)

[Introduction to Objects](#part0000_split_026.html__Toc29452743)

[Introduction to Object Oriented Programming: Classes](#part0000_split_026.html__Toc29452744)

[Overloading Operators](#part0000_split_026.html__Toc29452745)

[Inheritance between Classes](#part0000_split_026.html__Toc29452746)

[Implementing Polymorphism](#part0000_split_026.html__Toc29452747)

[Custom Constructors](#part0000_split_026.html__Toc29452748)

[Using Object Literal](#part0000_split_026.html__Toc29452749)

[Node tree](#part0000_split_026.html__Toc29452750)

[Arrays](#part0000_split_026.html__Toc29452751)

[Prototypal inheritance](#part0000_split_026.html__Toc29452752)

[Prototype](#part0000_split_026.html__Toc29452753)

[Chapter 6: Higher-order Functions](#part0000_split_027.html__Toc29452754)

[Transforming with map; strings and character codes.](#part0000_split_027.html__Toc29452755)

[Transforming with map](#part0000_split_027.html__Toc29452756)

[Strings and character codes](#part0000_split_027.html__Toc29452757)

[Chapter 7: What is JavaScript cookies](#part0000_split_028.html__Toc29452758)

[Explain how to create, read and delete cookies.](#part0000_split_028.html__Toc29452759)

[CONCLUSION](#part0000_split_029.html__Toc29452760)

INTRODUCTION

When it comes to creating some of your own robotics products, there are many things that you can consider. You will need to decide what kind of project you want to work on as well as the type of code that will help you to get the work done. One of the best options that you can use is the Arduino platform. When we are talking about Arduino, we are talking about a software and microcontroller that is programmable, open sourced, and will use the ATMega chip. It is designed to be more of a prototyping platform, there is a huge fan base for this software when it comes to building an electronic project. When it comes to working with an electronic project, you will find that the Arduino platform is good for using either as a temporary addition while you work on the project or you can even embed it as a permanent part of the robotic project when it is done.

The Arduino board is also programmable with the Arduino software, which is pretty easy to use, even for those who are just getting started and have no idea how to work with this kind of software. If you have happened to use the C + + or Java programming languages, you will see that the Arduino coding language is going to be fairly similar. The idea behind using this software is meant to be really simple, but there is a lot of power there to, making it perfect for those who have some experience and for those who are just getting started out. Arduino is also an open sourced platform, which means that anyone is able to use it, for free, as well as make adjustments to the code to fit their needs. This is a really cool addition for those who are just starting to use the Arduino system because they will be able to access thousands of codes from other programmers, or even make some changes to their own codes, in order to make the program work perfectly. In addition to finding that many of the codes that you would like to use are already available and developed, beginners are going to enjoy that the Arduino community is pretty large. You will be able to go online and look through forums and communities to ask your personal questions related to your own project, to find out new information, and even watch tutorials to make working with Arduino easier than ever. The Arduino platform may be pretty powerful to use, but it is also pretty basic. You will find that this platform only comes with two main components for you to use including: The hardware: this is going to include the microcontroller, which is also known as the circuit board. You are able to physically program this part. You will find that there are a number of Arduino boards for you to choose from and the choice will vary depending on the type of project that you are putting together.

The software: this would be the environment that you use with the board, or the IDE, that is going to run right on your own computer. You will use the IDE to help you to upload and write the programming codes that you would like to be relayed over to the board. Once you write your programs on the board and transfer them over, the Arduino board should act in the manner that you requested.

These parts are able to come together to help you to get the project to work well. You need to make sure that you have some hardware in place, such as one of the Arduino board types, and then it needs to respond to what you are able to send through with the software. We will spend some time talking about the various things that you are able to do with the software in order to get your project to work later on, but both of these will need to be set up to ensure that the messages from the IDE are getting over to the board and working properly. With Arduino, you need to have the IDE in place before writing out any code. The IDE for this program is free since it is open sourced, which makes it easier to get ahold of a copy. When writing codes, you will use the Arduino programming language, which will be easy to learn and works well with all of the operating systems on your computer. One thing to note with the IDE and the coding language with Arduino, if you are working on a Windows 7 operating system or earlier, you will have a few steps that you will need to take, in addition to the regular steps, to make sure that the Arduino board will work with the operating system. It does work with the older versions of Windows, you just need to take some extra time to introduce the board to this system to get it to work. Whether you are just getting started out with programming or want to use some of your skills to make a great electronic or robotic project, the Arduino platform will be able to help you get this done. It has all the power that you need with a simplistic background that helps even the beginner understand and accomplish what they want.

What can I do when using Arduino?

One of the first questions that you may have when you see the Arduino programming language is what you are able to do with it all? There are many programming languages out there and you are able to choose them to accomplish different things, but Arduino is going to work a bit differently compared to some of the others. There are many great projects that you are able to do with the Arduino platform. Basically, the coding that goes with Arduino is going to travel from the IDE on your computer over to the hardware that you purchase to go with your project. You can use just the board or attach it to some electronic project to make it do some amazing things. There are a lot of things that you can do with your robotics with the help of Arduino and if you are just getting started with your own electronic learning process or you want to try something new, this is the best platform to do so with. You are able to work with the board making sounds, blinking lights, sending out signals to control what is on the screen ahead of it, and so many other things. We will spend some time looking at the different projects that you are able to do with Arduino so you get a better idea of what you are able to do with this great language.

Chapter 1:What is Arduino?

History of Arduino 

A microcontroller is a small computer board that can be programmed to perform certain functions. At the time, BASIC stamp microcontrollers cost $100 and upward, and, as we will see later, Arduino certainly reduced the costs while maintaining the ability to perform various functions and the ease of programming such functions. 

Supervised by Massimo Banzi and Casey Reas, Barragán worked in the computer language called Processing to create the environment, IDE (Arduino’s official coding environment and program). He fiddled with the Wiring platform technology to come up with the hardware called ATmega168, the first Arduino microcontroller. 

Later in 2003, Massimo Banzi, David Mellis, and David Cuartielles added support for Wiring to their microcontroller board, named ATmega8, and they reworked the Wiring source code, naming it Arduino. Together, the three along with Tom Igoe and Gianluca Martino continued to develop Arduino technologies, and by the year 2013, 700,000 microcontroller boards were sold from the New York City supplier, Adafruit Industries, alone. 

After some issues with establishing the trademark for Arduino, which resulted in a split in the company for a few years, Arduino is now a single company that is committed to the development of hardware and software usable by the average person or hobbyist, but also flexible enough to be of interest to the professional engineer. 

But what is Arduino? 

This history of Arduino might sound as convoluted as the technology itself seems to you. Full of many puzzling and confusing elements, you might feel overwhelmed by the language of “microcontrollers,” “environments,” and “languages.” We will start here, beginning with the definition of Arduino. 

How it works is as follows: one purchases the hardware that is appropriate to his or her purposes and then, on a more powerful Windows, Macintosh OSX, or Linux computer, and codes or write instructions for the board and uploads the instructions via a cable. The code is then stored on the microcontroller, and it functions according to the instructions, such as activating a beeping sound when light filters in through an opening door. The light activates a sensor connected to the microcontroller, like an alarm. 

In a nutshell, Arduino is an electronic project development platform (or electronic prototyping, as it is also commonly said), consisting of both hardware and software, and which is available under the Creative Commons Attribution-Share-Alike license. 

This means that all Arduino project design files are freely available on the internet and that their software is open source. Also, the platform may be used for both personal and business purposes, provided that credits are attributed to the Arduino brand, and project files are also made available under the same license.

The project emerged in Italy in 2015 from a group of developers led by Massimo Banzi. The initial purpose was to create a low-cost, easy-to-work platform that could be used by students to develop their prototypes efficiently and cheaply. It was also thought to assist in the teaching of electronics to art and design students, particularly to create interactive environments, something very much in vogue within contemporary design and arts.

Who Uses Arduino? 

A wide array of people uses Arduino for various projects and hobbies, as well as for professional uses. It is known for being simple and straightforward enough for beginners, deep and rich enough for the beginner to grow, and with enough potential for a more advanced user to utilize. 

Teachers and students use Arduino, and indeed are the intended consumer base for the products, as Arduino offers a low-cost way to build scientific instruments. This allows teachers and students to practice and demonstrate chemistry and physics principles, as well as get started with programming and building robots. 

Designers and architects might use Arduino technologies to build interactive models and prototypes of what they hope to develop on a full-scale. Musicians and artists also use Arduino microcontrollers to experiment with new instruments or techniques in their art. 

Just about anyone can use Arduino, including children, that want to start tinkering with coding and computer hardware, as well as hobbyists who simply want to learn a bit about software and microcomputers.  

The main reasons for using the Arduino platform in your projects are as follows:

*   Low-cost prototyping
*   Free simulation software available
*   Easy to program
*   A large number of tutorials, articles, and projects ready on the internet
*   Extensive community of developers and hobbyists
*   No experience or extensive prior knowledge of electronics/programming required (however, it is advisable to know the basics at least)

Arduino is not the only electronic prototyping platform on the market. There are other projects and development kits, the most common being Raspberry Pi and BeagleBone. Each uses a different microcontroller and has hardware design with its own characteristics. Prices also vary widely, and some other platforms are not as popular.

The choice of which prototyping kit to use depends on the demands and needs your project imposes. Certainly, given the reasons cited above, Arduino is a strong candidate for most of its projects.

Chapter 2:Understanding of Arduino

Key terms related to Arduino

It will then close a circuit lighting up a bulb as output: a nightlight for your child. On most boards, there will be a Pin LED, associated with a specific pin, like Pin 13 on the Arduino Uno. This Pin LED is the only output possibility built into the board, and it will help you with your first project of a “blink sketch,” which will be explained later. The Pin LED is also used for debugging or fixing the code you have written so that it has no mistakes in it. The Power LED is what its name implies: it lights up when the board is receiving power or is “turned on.” This can also be helpful in debugging your code. There exists on every board the microcontroller itself, called the ATmega microcontroller, which is the brain of the entire board. It receives your instructions and acts accordingly. Without this, the entire board would have no functionality.

Analog in pins exist on the opposite edge of the board from the digital pins on the Arduino Uno. It is an input into the Arduino system. Analog means that the signal which is input is not constant but instead varies with time, such as audio input. In the example of audio input, the auditory input in a room varies with the people in the room talking and with the noises filtering in from outside the room. GND and 5V pins are used to create additional power of 5V to the circuit and microcontroller. The power connector is most often on the edge of the Arduino board, and it is used to provide power to the microcontroller when it is not plugged into the USB. The USB port can be used as a power source as well, but its main function is to upload, or transfer, your sketch, or set of instructions that you have coded, from your computer to the Arduino. TX and RX LED’s are used to indicate that there is a transfer of information occurring. This indication of communication will happen when you upload your sketches from your computer to the Arduino so that they will blink rapidly during the exchange.

Chapter 3: Anatomy of Arduino Board

Now that we know some basics in understanding the Arduino microcontroller boards let us look at the various options you have when purchasing an Arduino board. We will look at price, functionality, amount of memory, and other features to help make your decision as easy and straightforward as possible.

Uno

This is the board in which most people start their Arduino journey. It is on the smaller side in terms of memory but is very flexible in functionality and a great tool for beginners and those wanting to try their hand and mind at Arduino. This model has a mini-USB port which allows you to upload directly to the board without using a breakout board or other extra hardware.

Price: $24.95

Flash Memory: 32kB

SRAM: 2kB

EEPROM: 1kB

Processing Speed: 16MHz

Digital Pins: 14 pins

PWM Pins: 6 pins

Analog In: 6 pins

Operating Power: 5V

Input Power: 7-12V

Leonardo

The Leonardo microcontroller board is functional out-of-the-box: all you need is a micro-USB cable and a computer to get started. In addition, the computer can recognize the Leonardo as a mouse or a keyboard due to its ATmega32U4 processor.

Price: $19.80

Flash Memory: 32kB

SRAM: 2.5kB

EEPROM: 1kB

Processing Speed: 16MHz

Digital Pins: 20 pins

PWM Pins: 7 pins

Analog In: 12 pins

Operating Power: 5V

Input Power: 7-12V

101

This microcontroller contains a lot of features that are not available in other beginner models. For example, you can connect to the board through Bluetooth Low Energy connectivity from your phone. In addition, it comes with an accelerometer and a gyroscope built in to recognize motion in all directions with its six-axis sensitivity. It can recognize gestures as well.

Put together, these features allow you to have motion of or around the device be the input to which the microcontroller will respond with an output.

Price: $30.00

Flash Memory: 196kB

SRAM: 24kB

EEPROM: 0kB

Processing Speed: 32MHz

Digital Pins: 14 pins

PWM Pins: 4 pins

Analog In: 6 pins

Operating Power: 3.3V

Input Power: 7-12V

Esplora

This board is based on the Leonardo but comes with even more technology built into it so that you do not have to learn as much electronics to get up and running. Instead, you can learn as you see the processes work themselves out.

The input sensors that are built in include a joystick, a slider, a temperature sensor, a microphone, an accelerometer, and a light sensor. It also includes some sound and light outputs. It can expand its capabilities by attaching to other technology called a TFT LCD screen through two Tinker kit input/output connections.

Price: $43.89

Flash Memory:32kB

SRAM: 2.5kB

EEPROM: 1kB

Processing Speed: 16MHz

Digital Pins: n/a

PWM Pins: n/a

Analog In: n/a

Operating Power: 5V

Input Power: 7-12V

Mega 256O

This microcontroller is designed for larger projects like robotics and 3D printers. It has many times the number of digital pins and analog in pins, as well as almost three times the number of PWM pins. This, along with the many times multiplied flash storage, SRAM, and EEPROM allows for projects that require more instructions. There is space for greater complexity and specificity in this Arduino board.

Price: $45.95

Flash Memory: 256kB

SRAM: 8kB

EEPROM: 4kB

Processing Speed: 16MHz

Digital Pins: 54 pins

PWM Pins: 15 pins

Analog In: 16 pins

Operating Power: 5V

Input Power: 7-12V

UART: 4 lines

Zero

This is an extension of the Arduino Uno technologies that were developed. It is a 32-bit extension of Uno, and it increases performance with a vastly increased processing speed, 16 times the amount of SRAM and a many times multiplied flash memory. You will pay for the extensions, at almost twice the price of the Uno, but you much more than double your capabilities with this hardware.

One other advantage of the Zero is that it has a built-in feature called Atmel’s Embedded Debugger, abbreviated as EDBG, which helps you debug your code without using extra hardware and thereby increases your efficiency in the software coding.

Price: $42.90

Flash Memory: 256kB

SRAM: 32kB

EEPROM: n/a

Processing Speed: 48MHz

Digital Pins: 14 pins

PWM Pins: 10 pins

Analog In: 6 pins

Analog Out: 1 pin

Operating Power: 3.3V

Input Power: 7-12V

UART: 2 lines

USB port: 2 micro-USB ports

Due

This is a novelty in the microcontroller board world because it is built on a 32-bit ARM core microcontroller, giving it a great deal of power and functionality. It has an extremely quick processor and 4 UART’s, giving it a lot of flexibility and availability to perform multiple functions. It is used for larger scale Arduino projects, and while it might not be your first board, you would do well to consider it for any bigger projects you have down the line.

Price: $37.40

Flash Memory: 512kB

SRAM: 96kB

EEPROM: n/a

Processing Speed: 84MHz

Digital Pins: 54 pins

PWM Pins: 12 pins

Analog In: 12 pins

Analog Out: 2 pins

Operating Power: 3.3V

Input Power: 7-12V

UART: 4 lines

USB ports: 2 micro-USB ports

Mega ADK

This is based on the Mega256O Arduino board, with incredible memory capacity and a lot of availability for input and output. The difference between the Mega256O and the Mega ADK is that the Mega ADK is compatible specifically with Android technologies, such as Samsung phones and tablets, Asus technologies, and other non-iOS, non-Windows, mobile devices that use Android. It comes at a hefty almost $50 price tag, but if you are looking to incorporate Android into your project, this would be the board with which you would want to do so.

Price: $47.30

Flash Memory: 256kB

SRAM: 8kB

EEPROM: 4kB

Processing Speed: 16MHz

Digital Pins: 54 pins

PWM Pins: 15 pins

Analog In: 16 pins

Operating Power: 5V

Input Power: 7-12V

UART: 4 lines

Arduino Pro (8 MHz)

This is the SparkFun company’s take on the ATmega328 board. It is basically the Uno for professionals and is meant to be semi-permanent in installation of an object or technology. The 8MHz version is less powerful than the Uno by half, but it is also a good deal cheaper. It requires more knowledge of hardware to get this one working, as it does not have a USB port or a way to power the board by USB, and thus must have a connection to an FTDI cable or breakout board to communicate with the board and upload sketches. Once you get through the technicalities of getting this board hooked up to your computer, however, it functions like a half-power Uno. Unlike the 16MHz Arduino Pro, this 8MHz Pro can be powered by a lithium battery.

Price: $14.95

Flash Memory: 16kB

SRAM: 1kB

EEPROM: 0.512kB

Processing Speed: 8MHz

Digital Pins: 14 pins

PWM Pins: 6 pins

Analog In: 6 pins

Operating Power: 3.3V

Input Power: 3.35-12V

UART: 1 line

Arduino Pro (16 MHz)

This is the 16MHz version of the Arduino Pro by SparkFun. It is the same amount of power as the Uno but has the same drawbacks as the 8MHz Pro: you will need to find an FTDI cable or purchase a breakout board from SparkFun in order to make the board compatible with your computer to upload sketches. This means learning a bit more about the technology than if you were to start with the Uno, but after getting things set up, this will function the same as the Uno.

Price: $14.95

Flash Memory: 32kB

SRAM: 2kB

EEPROM: 1kB

Processing Speed: 16MHz

Digital Pins: 14 pins

PWM Pins: 6 pins

Analog In: 6 pins

Operating Power: 5V

Input Power: 5-12V

UART: 1 line

Arduino M0

This board is an extension of Arduino Uno, giving the Uno the 32-bit power of an ARM Cortex M0 core. This will not be your first board, but it might be your most exciting project. It will allow a creative mind to develop wearable technology, make objects with high tech automation, create yet-unseen robotics, come up with new ideas for the Internet of Things, or many other fantastic projects. This is a powerful extension of the straightforward technology of the Uno, and thus it has the flexibility to become almost anything you could imagine.

Price: $22.00

Flash Memory: 256 kB

SRAM: 32kB

Processing Speed: 48MHz

Digital Pins: 20 pins

PWM Pins: 12 pins

Analog In: 6 pins

Operating Power: 3.3V

Input Power: 5-15V

Arduino M0 Pro

This is the same extended technology of the Uno as the Arduino M0, but it has the added functionality and capability of debugging its own software with the Atmel's Embedded Debugger (EDBG) integrated into the board itself. This creates an interface with the board in which you can debug, or, in other words, a way to interact with the board where you can find the problems in the code you have provided and fix the issues.

Price: $42.90

Flash Memory: 256 kB

SRAM: 32kB

Processing Speed: 48MHz

Digital Pins: 20 pins

PWM Pins: 12 pins

Analog In: 6 pins

Operating Power: 3.3V

Input Power: 5-15V

Arduino YÚN (based on ATmega32U4)

The Arduino YÚN is a great board to use when connecting to the Internet of Things. It is perfect for if you want to design a device connected to a network, like the Internet or a data network. It has built-in ethernet support, which would give you a wired connection to a network, and Wi-Fi capabilities, allowing you to connect cordlessly to the Internet. The YÚN has a processor that supports Linux code in the operating system, or code language, of Linino OS. This gives it extra power and capabilities but retains the ease of use of Arduino.

Price: $68.20

Flash Memory: 32kB

SRAM: 2.5kB

EEPROM: 1kB

Processing Speed: 16MHz

Digital Pins: 20 pins

PWM Pins: 7 pins

Analog In: 12 pins

Operating Power: 5V

UART: 1 line

Chapter 4: Arduino Family

There are three types of memory in an Arduino system. Memory is the space where information is stored. Flash memory is where the code for the program that you have written is stored. It is also called the “program space,” because it is used for the program automatically when you upload it to the Arduino.

This type of memory remains intact when the power is cut off, or when the Arduino is turned off.

SRAM (static random-access memory) is the space used by the sketch or program you have created to create, store, and work with information from the input sources to create an output. This type of storage disappears once the power is turned off. EEPROM is like a tiny a hard-drive that allows the programmer to store information other than the program itself when the Arduino is turned off. There are separate instructions for the EEPROM, for reading,writing, and erasing, as well as other functions. Certain digital pins will be designated as PWM pins, meaning that they can create analog using digital means. Analog, as we remember, means that input (or output) is varied and not constant. Normally, digital pins can only create a constant flow of energy. However, PWM pins can vary the "pulse" of energy between 0 and 5 Volts. Certain tasks that you program can only be carried out by PWM pins.

In addition, in comparing microcontroller boards, you will want to look at clock speed, which is the speed at which the microcontroller operates. The faster the speed, the more responsive it the board will be, but the more battery or energy it will consume as well. UART measures the number of serial communication lines the device can handle. Serial communication lines are lines that transfer data serially, that is, in a line rather than in parallel or simultaneously. It requires much less hardware to process things serially than in parallel.

Some projects will have you connecting devices to the Internet of Things, which essentially describes the interconnectedness of devices, other than desktop and laptop computers, to various networks in order to share information. Everything from smart refrigerators, to smartphones, to smart TV’s are connected to the Internet of Things.

Chapter 5: Explanation of Arduino Components

An Arduino can very easily be built using a solderless bread board and just a few minutes of your time (once you are familiar with the process). Once you have built the board, the microcontroller can be programmed with the Arduino programming language. Then, you will be ready to use the board in your next do-it-yourself project.

What You Will Need

You only need a few inexpensive pieces to turn your solderless breadboard into an Arduino, including:

*   440 or 840 Tie Point Breadboard
*   TTL-232R-3V3 USB to Serial Converter Cable
*   Small Momentary Tact Switch
*   16 MHz Clock Crystal
*   1 Row Male Header Pins
*   22 AWG Wire (selection of colors)
*   1 Brown, Black, Red 10k Ohm Resistor
*   2 Red, Red, Brown 220 Ohm Resistors
*   2 22pF Capacitors
*   2 10 uF Capacitors

Step 1

Once you have gathered all of the necessary parts, you are ready to start building your Arduino breadboard. The first step is to set up power. For this particular model, a constant +5Volts of power will be provided. You will also set up a 7805 voltage regulator. 

When looking at your breadboard, you will see squares with red and black + and – symbols on them. Begin by placing one 10uF capacitor here. Then you will need to add the 7805 voltage regulator to the breadboard. Be sure you are lining up the left leg of the 7805 with the power in, and the middle power up with the ground.  Now you will need the second 10uF capacitor. Place this on the power rail. Finally, if you choose, include an LED status indicator on your breadboard. This is a good idea for troubleshooting. Connect the right and left power rails with a 220 resistor. 

Step 2

For the second step, you will be preparing your chip. Each pin should align with a specific slot on the board. This will ensure your Arduino functions the way that you need it to. 

| Number on the Board | Corresponding Pin |
| 1 | Reset |
| 2 | Digital Pin 0 (RX) |
| 3 | Digital Pin 1 (TX) |
| 4 | Digital Pin 2 |
| 5 | Digital Pin 3 |
| 6 | Digital Pin 4 |
| 7 | VCC |
| 8 | GND |
| 9 | XTAL 1 |
| 10 | XTAL 2 |
| 11 | Digital Pin 5 |
| 12 | Digital Pin 6 |
| 13 | Digital Pin 7 |
| 14 | Digital Pin 8 |
| 15 | Digital Pin 9 (PWM) |
| 16 | Digital Pin 10 (PWM) |
| 17 | Digital Pin 11 (PWM) |
| 18 | Digital Pin 12 |
| 19 | Digital Pin 13 (LED) |
| 20 | AVCC |
| 21 | AREF |
| 22 | GND |
| 23 | Analog Input 0 |
| 24 | Analog Input 1 |
| 25 | Analog Input 2 |
| 26 | Analog Input 3 |
| 27 | Analog Input 4 |
| 28 | Analog Input 5 |

Step 3

Once your pins are in place, add the tact switch near pin 1\. This will reset your Arduino breadboard when necessary. Then, connect a small jumper wire between the bottom leg of the switch and pin 1\. The next step is to connect the 10K resistor between pin row 1 and the power switch. The final thing you will need to do in this area is connect a GND wire to the top leg.

Next, connect power and GND jumpers between VCC (pin 7) and GND (pin 8). The 16 MHz clock crystal should then be added to pins 9 and 1-. Next, add the .22pF capacitors from these pins to GND. You can stop here if you choose, and add a programming chip. If you are interested in setting the breadboard up for programming, however, continue reading.

Step 4

The connections you will need for programming include the pins GND, NC, 5V, TX, RX, and NC. Connect the GND wire from the power rail to the GND pin. Add a power wire to the 5V pin. Finally, connect a wire between the TX pin and the RX pin. Your Arduino breadboard is now ready to be programmed. You can do this by using the USB – Serial Converter Cable from the list of necessary items. 

How to Build a Swimming Electronic Snake

When built correctly, this snake is waterproof and can be controlled using a remote controller. If this is your first attempt at an Arduino project, you may want to choose a simpler option from one of the later chapters to start with. While this section will be fun to read, you may want to attempt building the light-up, rain-sensing umbrella from Chapter 8, the biking jacket with blinking turn signals from Chapter 9, or the Arduino gas sensor from Chapter 10 first.

Electronic Items

You will need:

*   Arduino Uno
*   Seeeduino Mega
*   10 Servo Motors (Remember that you get what you pay for. The nylon gears in these motors may wear out quickly if you choose lower quality motors.)
*   Servo Extension Wire
*   Servo Motor Shield
*   2 Xbee Series 1
*   Xbee Explorer
*   Xbee Breakout (with 2 rows Xbee 2mm female headers and 2 rows of 10 male header pins)
*   3 6V NiMh Battery packs

Mechanical Hardware

*   Urethane Sealant
*   Marine Epoxy Sealant
*   Marine Grease
*   Nylon String
*   Green Loctite
*   2” x 10” of 1/8” Thick Rubber
*   3 Strips Each of Carbon Fiber – 1/32”, 1” x 12”
*   2 2.5 to 1.25” Shop Vac Vacuum Reducer
*   O Rings
*   5/16” Hose Clamp
*   Convoluted Hose Clamp
*   5/16” Tubing
*   5 Servo Brackets
*   5 Injection Molded Servo Hinge
*   5’ x 2.5” Urethane Dust Collection Tube
*   5 Lynxmotion C-Brackets
*   5 Lynxmotion Servo Brackets

Tools

*   Solder Iron + Solder
*   Drill
*   3mm Drill Bit
*   Small Screwdriver
*   Needlenose Pliers
*   Wire Strippers
*   Wires
*   Angle Snips
*   Hack saw
*   2-56 nuts, bolts, and screws, either lock or toothed
*   4-40 nuts, bolts, and screws, either lock or toothed

Step 1

Once you have gathered all of the various tools, electronic items, and hardware, it is time to begin your project. You will start by waterproofing the 10 Servo motors. Begin by applying the silicon marine sealant around the plastic seams of the motor. You should also apply it to the bottom of the motor (where the screws are located) and around the wire insertion area. You should let this dry for a minimum of 24 hours. 

Next, unscrew the round plastic that makes up the top of the motor. Slip an O-ring around the shaft after using a thin layer of marine grease on it. Then, replace the plastic top. This is also known as the servo horn. 

Step 2

For this step, you will be preparing the carbon fiber for use. Cut the 12” x 1” strips into 3 separate pieces. This will result in 4” strips. If you have a dremel handy, you can round the corners so they are not jagged from cutting. Then, place the servo brackets 3 inches apart on the strips. Make markings where the bracket holes line up. Take a 3mm drill bit and drill into the carbon fiber, making holes where the markings are. You will need to do this with 7 of your 4” strips of carbon fiber.

Step 3

In this step, you will be building the frame of your robotic snake. Begin by using the screws that come with the brackets to attach the carbon fiber. Be sure you use the bolt that came with the bracket as well. Then, take the rubber and line it up with the middle section of the c-bracket. Use these as your guideline to cut 5 pieces of rubber that are approximately 1” x 2.” Draw a dot where the holes of the bracket align with the rubber. Then, poke a hole through the rubber so you can more easily insert the 2-56 screws. These should go through the black clamp, through the rubber, and through the red bracket.

Step 4

In this step, you will be mounting the Servos motors. Your Servos should come with several parts. Begin with the rectangular cube and insert it into the four holes of the motor. The flat side should face outward. Adhere the injection molded joint on five of the motors and place them in the bracket. Use the 4x40 screws and a lock nut to screw the servo into the black servo bracket.

Step 5

In this step, you will be mounting the servos bracket to the c-bracket pairs. For the red brackets, the c-bracket should be put into place underneath of the servo bracket, but above the servo horn. A screw and bearing should be used to secure it. For the black brackets, the c-bracket should be slipped over the motor. This will cover most of its body. Once you secure these, you should have s snake-like structure that makes up the body of your robotic snake. 

Step 6

To complete the body of your snake, line up the servo horns with the holes of the bracket. Ensure your horn is centered before screwing them together. If the brackets and motors do not rotate freely after being secured, apply grease between the brackets. For additional security, apply Loctite to the screws once you are sure they are in the correct position.

Step 7

In this step, you will be making the circuit board for your snake. Begin by soldering the male and female headers onto the Xbee Breakout board. Insert the Xbee. Then, take the Servo motor shield and solder it into the screw terminals. Once it has been soldered together, take your wires and connect the Xbee to the Arduino. Connect the 3.3Vin pin on the Xbee to the Arduino 3.3V pin. Jump the TX pin on the Xbee to the Arduino RX pin. Connect the Xbee ground to the Arduino ground pin. Finally, jump the power cord between the Arduino VIN pin and the 6V battery input.

Next, solder the wires from digital output pins for the number of servo motors you are using. You should take the dOUT wires from your Arduino, and then plug them into the servo cables. Screw the wires into the screw terminals. This will attach the 6V and ground from the batteries.

Step 8

Next you will need the code to make your snake swim. You can find this in the software library on the Servo Arduino library. You will need a code to generate wave locomotion using oscillation. This will create a sine wave that travels down the servos motors. 

Step 9

In this step, you will create a free standing joystick controller for the snake. Begin by plugging the Xbee into the Xbee shield. Set them atop the Arduino and make 6 button inputs. These buttons should be connected to digital pins 2-7 on the Arduino. You will now upload a code from the Arduino library to take the button inputs and output them as movement in the snake.

Step 10

This is the step where you will add all of the wires to the snake. Use the wire extenders from the servo motors and extend the wires down the body of the snake. They should end just a few inches after the last bracket. If you want to, you can tape the wires to the carbon fiber so it is easier to put the carbon fiber on. 

Step 11

In this step, you will attach the batteries using the 6V/GND wires so that your snake can operate. Attach one battery to each segment of carbon fiber, using two zip ties. You should also take the wire extensions from the Servo motor so that he battery power reaches the ground and Arduino at the front of the snake. 

Step 12

This is the step where you add the on/off buttons. You may want to use one for the Arduino/Servos connection and one for the water pump. Be sure you turn on the snake before the pump, because running the water pump without water will cause it to dry out and burn up. Then, cut two pieces of rubber 1.75” in diameter. This should fit inside of the vacuum reducer. You should also cut two 2’ long pieces of cord to help position the snake’s body inside the vacuum reducer. You will need to cut a small slit for the wires in the rubber before placing it in the vacuum reducer. You will also attach the string here. You will have power and ground wires from the water pump, power and ground wires from the on/off switches, and one string running thorough both the rubber pad and the vacuum reducer. At the tail, you will only need the string on the outside to tether the snake. Next, take the 6V wire on the screw terminal and solder the on/off button to it.

Step 13

In this step, you will elongate the snake body and prepare the battery so the water pump can operate properly. Attach carbon fiber pieces that are 4” long at the head and tail ends of the snake. Solder a battery junction and the water pump together. Next, locate the wire that extends between the battery and pump. This is where you will need to solder the switch to turn your snake on and off. Use the zip ties to attach the battery to the carbon fiber next to the Arduino.

Step 14

In this step, you will be sealing the body of the snake and putting on the skin. Use caulk on either end of the vacuum reducer to cover the wires completely. Wait at least 24 hours for the caulk to dry before finishing the project. You can use hot glue to secure the wires and silica packs to absorb moisture if you choose. You should also take this opportunity to ensure the joints are moving freely. Add additional grease if necessary. Now, slip the skin over the body of the snake. Cut the tube length if necessary so that the carbon fiber fits into the end of the tube when positioned with the string. Tie the string in a knot once you have finished to prevent slippage. Finally, you need to put caps on the head and tail end of the snake using marine grease to keep water out. 

Step 15

Now that the snake is fully assembled, you are ready to mount the water pump. Once mounted, the water pump should be located close to the head of the snake, but on the bottom side. It will be submerged during operation. Cut 5/16” plastic tubing to slip over the output nozzle of the pump. Then secure a hose-clamp at the joint of the tube. Use this plastic tubing to mount the pump. You can use a zip tie to secure it. If you are interested, you can even mount a GoPro on the snake.

Step 16

Now you are ready to test out your robotic water snake! Be sure to apply grease around the plastic buttons before taking it outside. Turn the snake on and place it in the water. Once you have placed the robotic snake in the water, you will be able to turn the pump on without drying it up. Use your remote controller to direct the motion of the snake.

Chapter 6: Getting started with Arduino

The first step in setting up your Arduino microcontroller will be to choose an Arduino board with which you want to work.

Choosing a Board

When looking at the options for Arduino Boards, there are a few factors you will want to consider before making a choice. Before deciding on a board, ask yourself the following questions:

How much power do I need to run the application I have in mind?

You might not know the exact measure of flash memory and processing power that you require for your project, but there is a clear difference between the functioning of a simple nightlight that changes colors and a robotic hand with many moving parts. The latter would require a more robust Arduino microcontroller board, with faster processing,more flash memory, and more SRAM than the more straightforward night light idea.

How many digital and analog pins will I require to have the functionality that I desire?

Again, you don’t need to have an extremely specific idea in mind but knowing whether you need more pins or less will have a great effect on which board you choose. If you are going for a simple first project, you could get away with having less digital, PWM, and analog pins, while if you are looking to do something more complex, you will want to consider the boards with a great number of pins in general. Do I want this to be a wearable device?

There are a few options for wearable devices so, of course, this question will not entirely make the decision for you. It will, however, help narrow down the choices and steer you in a direction, with Lilypads and the Gemma or other comparable technologies being your best options. Do I want to connect to the Internet of Things? If so, how?

If you want connectivity to the Internet of Things, your work will be made much easier by the YÚN, the Tian, the Ethernet, the Leonardo ETH, or the Industrial 101\. These have the capabilities of Ethernet connection as well as Wi-Fi capability so you will be able to connect to a network like the Internet and share data or interact with and control other devices on the Internet of Things. Getting Started on Arduino IDE The Arduino Software runs in an environment called IDE. This means that you will either need to download the desktop IDE to code in or code online on the online IDE. The first way that you might access IDE, downloading the desktop application, has a few options to suit the various devices that you might be using. First, there is the Windows desktop application. You can also access it from a Windows tablet or Windows phone with the Windows application. Next, there is the Macintosh OSX version, which allows IDE to run on Apple laptops and desktops, but not on Apple mobile devices like iPhones and iPads. Finally, there are three options for running Arduino IDE on Linux: the 32-bit, the 64-bit, and the Linux ARM version. If you prefer this option to the web browser option, you will simply need to visit the Arduino IDE site by heading to https:// www.arduino.cc/ en/ Main/ Software There, you can download the appropriate version of desktop IDE. Next, you will run the installation application, click through the options presented, and you should have a running Arduino IDE environment in just a few minutes.

This allows you to access the IDE software from Android devices and Apple mobile devices as well since it is based in a web browser that runs on its own platform rather than on the Android or iOS platforms. You can also run the web browser on various computer types, including Linux, Microsoft Windows, and Apple Macintosh. This will allow you to upload your sketches to the Cloud, that is, to store the information you have coded in a secure location that you can then re-access from another device by connection to the Internet. Coding a Program for Your Arduino Next you will write code for a program that you want the Arduino board to run. This allows you to see the entire code at once, allowing for easier debugging, or removing of errors.

Once you write the code, you will want to run it and troubleshoot or debug any errors that you find. You will best be able to do this by applying the coded program to the Arduino board and seeing if it runs. To do this, you will need to proceed to the next step of uploading your sketch. Connecting to the Arduino Board

Some of the boards come with built-in USB, mini-USB, or micro-USB ports. Examples would be the Uno and the Leonardo, for the more beginning stages of your Arduino career. Simply insert the appropriate end of the USB cord into your computer and the other end into the particular USB port that is present on the board you possess, and the Arduino IDE software should recognize the type of board it is. If it does not, you can always choose the correct board from a dropdown menu.

Sometimes you will need to use a TKDI cable or a breakout board in order to make the Arduino compatible with your computer. This means you will insert the TKDI into the TKDI port on the Arduino microcontroller board and then connect it either to your computer or to another board. If you connect the TKDI cable to a breakout board, you will do as you did with the USB-compatible boards: insert the appropriate end of the cord to the breakout board and the other end to the computer. Again, the computer’s Arduino IDE software program should recognize your Arduino board, but you can always choose from a dropdown menu should it fail to recognize it. Uploading to the Arduino Board

To upload your sketch, the program you just created in code, you will need to select the correct board and port to which you would like to upload. It should be easy enough to select the correct board, as you simply look for the board title that matches the name of the type of board you are using.

To select the correct serial port, the options you might choose are as follows:

Mac

Use /dev/ tty.usbmodem241 for the Uno, Mega256O or Leonardo.

Use /dev/ tty.usbserial-1B1 for Duemilanove or earlier Arduino boards.

Use /dev/ tty.USA19QW1b1P1.1 for anything else connected by a USB-to-serial adapter.

Windows

Use COM1 or COM2 for a serial board.

Use COM4, COM5, or COM7 or higher for a USB-connected board.

Look in Windows Device Manager to determine which port the device you are using is utilizing.

Linux

Use /dev/ ttyACMx for a serial

port.

Use /dev/ ttyUSBx or something like it for a USB port. Once you have selected the correct board and port, click Upload and choose which Sketch to upload from the menu that appears. If you have a newer Arduino board, you will be able to upload the new sketch simply, but with the older boards, you must reset the board before uploading a new sketch, else you will have two, possibly conflicting sketches present in the board’s memory, causing it to crash. Running the Arduino with Your Program

There are a few ways to power your Arduino once you have uploaded the program that you have coded to it. First, you can power it by the USB connection to another powered device, such as your computer. Second, you can power by Ethernet on boards with that capability. This means that by connecting to the network, you will be connected to a power source through the Ethernet. Finally, you can power most Arduino’s by lithium polymer battery. Once power is connected, and the specified input is put into the microcontroller, it will perform the function for which it is intended.

Installing the Arduino IDE

Now that you know the different parts of the Arduino board, we can learn how to prepare the Arduino IDE. After learning this, we will be ready to upload out the first program to the board. You will learn how to setup the board and set it ready to receive the program through a USB cable. 

Ensure that you have the Arduino board and a USB cable. After assembling these, the next step is to download the Arduino IDE. You can download this from the following URL:

[https://www.arduino.cc/en/Main/Software](https://www.arduino.cc/en/Main/Software)

Download the right version of Arduino based on the operating system that you are using. Once the download completes, unzip the downloaded file. 

You can now power your board. The board can draw power from a USB connection to your computer or from an external power supply. Just connect your Arduino board to your computer via a USB cable. You should see the green power LED glow. 

It is now time to launch the Arduino IDE. Open the folder where you unzipped the Arduino IDE. Double the .exe file to start the IDE. 

The software will be opened and you will be able to create a new project or open an existing one. To create a new project, click File then chooses New. To open an existing project, click File, choose Example, Basics and then Blink. 

You need to select the type of board that you are using. To avoid any errors when you are loading programs from the IDE to the board, ensure that you select the correct board, that is, the type of board you select in the IDE must match the type of board that is connected to your computer via the USB cable. 

To select the board, click Tools then choose Board. 

Next, you should select the serial port of your Arduino board. Click Tools then choose Serial Port. If you find it hard to know the serial port, just disconnect the Arduino board from the computer then look for the entry that disappears. This should be the Arduino board. You can then reconnect the board and choose that port. 

Anytime you need to load a program to the Arduino board, just click the Upload button on the IDE. Note that an Arduino program is referred to as a sketch.

Digital Input/Output

Digital signals are discrete values that either exists as 1 or 0\. This is to mean 1 (High) implies presence of a signal while 0 (Low) represents the absence of a signal. Digital signal is therefore transmitted as binary codes represented by either presence or absence of current, 5v or ground, or presence or absence of a pulse.

Human beings are used to analog signals while robots, computers and most electronic circuits perceive digital signals. As stated earlier, a digital signal only has two states, that is, ON and OFF just like a two-way light switch on your wall.

Digital signals are used everywhere in Arduino programming except for the analog input that is meant specifically to tolerate analog signals. The ON or HIGH state of the digital signal will always equal the board voltage as either 3.3 volts or 5.0 volts. On the other hand, the LOW or OFF state is always represented by 0 volts.

In order to receive or send digital signals on the Arduino board, use only pins labeled 0-13\. Again as explained earlier it is possible to set up the analog pins to act as digital pins. This is achievable through the use of the command: pinMode (pin label, value). The pin number here stands for an analog pin ranging from A0-A5, the value in the function is always either input or output.

You can use the same command to set up digital pins. First of all reference the digital pin for pinNumber instead of analog. It is also important to note that digital pins by default used as input pins so it is only required of you to set them to OUTPUT mode. To achieve this, use the command: digitalRead (pin label) where the digital component will be connected to the pin label. digitalRead (pin number) returns either HIGH or LOW as results. 

When you want to send a digital signal to a digital pin from the IDE platform, you are supposed to use the code: digitalWrite(pin label, value) where pin label stands for the pin number from which the signal is coming from and the value can either be HIGH or LOW.

Arduino also uses the technique of Pulse Width Modulation to send Digital signal that is in the form of analog. The pin numbers responsible for this are: 3, 5, 6, 9, 10 and 11\. And the command used here looks like this: analogWrite(pin label, value). The pin numbers are already provided up there and the value is an integer ranging from 0 (0%) and 100% (255).

Examples of digital signals

ON/OFF, Men’s table/Women’s table, pregnancy, death, consciousness and the list continues.

Sensors and interfaces used here may include: Relays, Circuit breakers, Switches, Buttons and many others.

Chapter 7: Basic digital Arduino programs

LED Blink

This is the most basic program in Arduino programming just like printing the word “hello world” in any other programming language. Since in Arduino programming there is no screen to print “hello world”, we therefore blink an LED as our first test program. This is indeed a very simple program that is meant to give you a strong foundation as you invest into the world of circuit building through prototyping.

The Required Components

*   One breadboard
*   An Arduino Uno
*   One LED
*   Resistor (330 ohms)
*   Two jumper wires

Circuit

The circuit is quite simple due to the small number of components, therefore just follow the simple circuit diagram below:

![Description: 00024.jpeg](images/00002.jpeg)

Finding the polarity of the LED

An LED has polarity, that is, negative and positive terminals. To determine this, hold the LED with the flat side facing you. The shorter leg on your left side is the negative terminal while the longer leg on your right is the positive terminal.

![Description: 00025.jpeg](images/00003.jpeg)

Sketch

Quickly open the Arduino IDE on your computer, then a new sketch file on the New tab then begin writing your codes as shown below:

*/ Blink an LED, the codes below are meant to turn a Light Emitting Diode connected to a digital pin periodically. Pin number 13 is used since it has a resistor in its circuit to limit current through the LED */

int ledPin = 13; // LED has been connected to digital pin number 13
void setup()
{
  ledPin(pinMode, OUTPUT); // the digital pin is set as the output
}
void loop()
{
  digitalWrite(pinMode, HIGH); // the code is used to set LED ON
  delay(1000); // delay time is a second
  digitalWrite(ledPin, LOW); // the code is used to set LED OFF
  delay(1000); // delay time is a second
}

LED Blink without Delay

Sometimes you may wish to let the LED light without stopping and this calls for the use of another function other than delay ( ). The function for LED blinking without delay keep track of the time when the LED was turned ON and OFF. The using a loop ( ), it checks if sufficient time interval has passed so as to turn the LED ON if it was OFF and vice versa. The other components are the same as for the example above.

Here are the codes:

int ledPin = 13; // an LED has been connected to a digital pin number 13

int num = LOW; // int num has been declared and assigned LOW representing LED //previous value 

long previousMillis = 0; // stores the value for when the LED was last updated

long delay = 1000; // delay time is set to one second (milliseconds)

void setup()

{

   pinMode(ledPin, OUTPUT); // the digital pin is set to be the OUTPUT

}

void loop()

{

// the codes are the ones to control the lighting of the LED.

if (millis() - previousMillis > delay) 

   {

    previousMillis = millis(); // recalls the previous time the LED blinked

// the codes below turns the LED ON in case it was OFF and vice-versa.

if (num == LOW)

    num = HIGH;

else

   num = LOW;

   digitalWrite(ledPin, num);

  }

}

Fading an LED   

For this case we will be using the analogWrite ( ) function to initiate the fading process an LED connected to the Arduino board. This is possible because analogWrite ( ) function uses Pulse Width Modulation technique which is able to turn on and off a digital pin quickly in different ratios thereby creating the fading effect. The components are still the same with the first example including the circuit. The only difference is noticed in the codes as shown below:

/*
Fade 

This example illustrates the use of the function analogWrite ( ) to control the fading of an LED*/

int ledPin = 6;     // LED is attached to the PMW pin number 6

int brightness = 0; // current brightness of the LED 

int fadeStep = 6; // the number of steps to fade the LED through

void loop()

 {

     //code used to set the brightness of the LED on pin 6:

 analogWrite(ledPin, brightness);

     //code meant to change LED brightness for the next step through the 

      //loop:

 brightness = brightness + fadeStep;

   //codes used to reverse the fading direction at the ends of each previous 

 //fade:

 if (brightness == 0 || brightness == 255)

  {

      fadeStep = -fadeStep ;

  }

  // our delat time is 30 milliseconds so as to realize the dimming effect

delay(300);

}  

Arduino Button

This is typically a button that connects two points in a circuit. When pressed, the button completes the circuit between these two points as in lighting an LED.

Components

*   A pushbutton
*   One Arduino Uno
*   One Light Emitting Diode
*   Three connecting wires.
*   2.2 kilo ohms

Procedure

Your circuit should look like the one below:

![Description: 00026.jpeg](images/00004.jpeg)

The codes for this project are written below:

int outPin = 14; // the LED has been connected to pin number 14

int inPin = 3; // our input pin for a pushbutton will be pin number 3 

int num = 0; // variable declaration; used to read the pin status

void setup() {

  pinMode(outPin, OUTPUT); // LED will be used as the OUTPUT

  pinMode(inPin, INPUT); // pushbutton shall be our INPUT for this case

}

void loop()

  {

      num = digitalRead(inPin); // the code is used to read value of the input 

    if (num == HIGH) { // checks whether the button is released (HIGH input)

    digitalWrite(outPin, LOW); // turns OFF the LED

 } 

else 

  {

   digitalWrite(outPin, HIGH); // turns the LED ON

  }

}

Arduino Pushbutton as a Debounce

This example is similar to the above exercise apart from the function of the pushbutton. The pushbutton debounces the input that is to mean without pressing the button represents a code similar to multiple presses.

The components and the circuit board is the same as the above example. So we will go direct to the codes as that we highlight the difference. 

Code

int inPin = 6;      // the input has been assigned to pin number 6 

int outPin = 11;   // the output has been assigned to pin number 11

int position = HIGH; // shows the current state of the output pin number 11

int display; //indicates the current reading of the input pin number 6

int previous = LOW; // the previous reading the input pin assigned LOW

long time = 0; // the variable time represents the period when the output was //toggled

long debounce =100; // the debounce time has been assigned 

void setup()

{

    pinMode(inPin, INPUT);

    pinMode(outPin, OUTPUT);

}

void loop()

 {

  display = digitalRead(inPin);

if (display == HIGH && previous == LOW && millis() - time > debounce) {

  // ... the function returns an inverted output

if (position == HIGH)

     position = LOW;

  else

     position = HIGH;

// ... function recalls the time when button was pressed

time = millis();

  }

digitalWrite(outPin, position);

previous = display;

}

Creating a Loop

Components required

*   Six Light Emitting Diodes
*   Six 220 Ohm resistors
*   Seven jumper wires
*   One Arduino Uno

In this example we shall six LEDs to demonstrate sequential blinking using the function digitalWrite(pin label, LOW/HIGH) together with delay ( ).

Circuit

![Description: 00027.jpeg](images/00005.jpeg)

Code

int timer = 120; // timing reduces with an increase in the time number.

int pins[] = { 2,3, 4, 5, 6, 7, 8 }; // pin numbers as an array of

int value_pins = 6; // array length represented by the number of pins

void setup()

{

  int j;

for (j = 0; j< value pins; j++) // the array elements as numbered from 0 //to value_pins – 1

pinMode(pins[j], OUTPUT); // each pin has been set as an output

}

void loop()

{

int j;

for (j = 0; j < num_pins; j++) 

   { 

// a loop is set through each output pin...

digitalWrite(pins[j], HIGH); // function to turn the output pin   ON,

delay(timer);                // delay function,

digitalWrite(pins[j], LOW); // function to turn the output pin OFF 

         }

for (j = value_pins - 1; j >= 0; j--) 

   {

digitalWrite(pins[j], HIGH);

delay(timer);

digitalWrite(pins[j], LOW);

       }

}

Chapter 8:Basic analog Arduino programs

Analog Input

In this project we shall use a potentiometer as the source of analog input signal to the Arduino board. Ideally, the potentiometer is able to vary resistance (variable resistance) which can then be read by the Arduino board as analog input. We are going to use the already fixed LED pin 11 on the Arduino board as part of our project.

Components required

 A potentiometer

 An Arduino project for LED lighting

 Three jumper wires

![Description: 00028.jpeg](images/00006.jpeg)

Sketch

/* potentiometer project under AnalogInput

This project aims to turn ON and OFF a light Emitting Diode periodically. The amount of light of the LED depends on the value of resistance of the potentiometer used. Increasing resistance reduces the amount of light and vice versa.

*/

int num = 0; //this variable stores the input value from the sensor output, //initially assigned 0

void setup() 

{

pinMode(ledPin, OUTPUT); // function declares the LED as an OUTPUT

}

void loop() 

{

num = analogRead(inPin);    // function to read the value of sensor //output

digitalWrite(ledPin, HIGH);  // function to turn the LED ON

delay(num);           // delay function to stop the program for a while

digitalWrite(ledPin, LOW);    // function to turn OFF the LED

delay(num);                  // function stops the program for a while

}

Knock Sensor

For this kind of a project, we shall employ the use of a piezo element and trap its sound as the analog input into the Arduino board. The processor of the board is able to read analog signals with the aid of its ADC (analog to digital Converter). The Piezo element (knock sensor) is just but an electronic device that is capable of playing tones and detect tones at the same. The Arduino board detects the sound levels as voltage levels, transform the voltage level to a corresponding value ranging from 0 to 1024 for voltages of 0 to 5.0 volts.

Remember that the Piezo element has polarity, black wire representing the negative terminal while the red wire represents the positive terminal.

In the sketch, we will try to capture the sound level (knock ) of the Piezo element and confirm that it is above a certain threshold then send a “Knock” string a signal to the Arduino IDE platform.

Circuit

![Description: 00029.jpeg](images/00007.jpeg)

Sketch

/* Knock Sensor

In this project we are using the Piezo element as a knock sensor. We therefore have to listen to the sound level, if the signal goes beyond a specified threshold.

void setup() 

{

  pinMode(ledPin, OUTPUT); // function declares the ledPin as the OUTPUT

  Serial.begin(9600); // indicate the use of serial port

}

void loop() 

{

num = analogRead(knockSensor); // function is used to read the value of the  //sensor and store it in the variable num

if (num >= THRESHOLD) 

   {

statePin = !statePin; // function that is used to toggle the status of the ledPin though it does not use time cycle

digitalWrite(ledPin, statePin); // function to turn LED ON or OFF

Serial.println("Knock!"); // function sends the string "Knock!" through //the serial port to the computer then a newline

delay(100); // a very short delay in order to prevent serial port from //overloading

   }

}

Arduino Smoothing

Involves the use of arrays where the sketch is supposed to read analog input repeatedly, calculate the running average and finally print the result.

Sketch

int readings[VALUES];   // array declaration to represent readings from the //analog input

int index = 0;   // variable declaration and initialization

int total = 0;  // variable declaration and initialization

int average = 0; // variable declaration and initialization

int inputPin = 0; // variable declaration and initialization

void setup()

{

 Serial.begin(9600); // function used to create a serial communication with the //computer

for (int j = 0; j < VALUES; j++)

readings[j] = 0; //setting all the initial readings to 0

}

void loop()

Printing Analog Input (Graphing)

This project demonstrate the how to read analog data, convert the signal into voltage levels and finally print t.

Components Required

 One breadboard

 One Arduino Uno

 One Potentiometer 5 kilo ohms

 Two jumper wires

 Eight LEDs

Circuit

The circuit diagram and the components on the diagram are shown below:

![Description: 00030.jpeg](images/00008.jpeg)

Sketch

*/

// the constants used below are to remain the same all through:

const int analogPin = A0; // the potentiometer has been attached to this pin

const int ledCount = 8; // representing the number of pins that will produce //the graphing effect

int ledPins[] = {3, 4, 5, 6, 7, 8, 9, 10}; // pin numbers where the LEDs will //be attached forming an array of pins

void setup()

{

   // a loop over the pin array thereby setting them as the OUPUT:

for (int firstLed = 0; firstLed < ledCount; firstLed++)

    {

       pinMode(ledPins[firstLed], OUTPUT);

    }

}

void loop()

{

 // the code below reads the potentiometer output to use as the system input:

int sensorOutput = analogRead(analogPin);

// copy the result to a range of LEDs from 0 to 7:

int ledLevel = map(sensoroutput, 0, 1023, 0, ledCount);

// a loop over the pin array:

for (int firstLed = 0; firstLed < ledCount; firstLed++)

{

// when the array element has an index which is less than ledLevel then

// turn ON the pin for this particular element:

if (firstLed < ledLevel)

          {

      digitalWrite(ledPins[firstLed], HIGH);

          }

// function to turn OFF all other pins whose array element have indices higher      //than the ledLevel:

     else

          {

            digitalWrite(ledPins[firstLed], LOW);

        }

    }

}

It is equally important to NOTE the results of this project: The eight LEDs will turn ON one after another with an increase in the value of the analog reading and they will be again turning OFF one by one on decreasing the value of analog reading.

Chapter 9: Arduino programming tools

Arduino Control Statements

Control structures involved in decision making demand that the person doing the actual programming (programmer) clarifies and specifies certain conditions that will be tested and evaluated by the program itself. These condition should be written along with some statements that will be executed if the condition is to return a value. Otherwise, other statements will be executed so as to return a false response or outcome for the condition.

Most of the programming languages have a general format for decision making structures as illustrated below: ![Description: 00014.jpeg](images/00009.jpeg)

The statements within the control structure (condition) as mean to coordinate the flow of program execution and are therefore referred to as Source Code Control Statements.

These are statements include:

If statement

If….else statement

If…else if…else statement

Switch case statement

Conditional operator?

Again just to emphasize, these statements are very important in navigating through various loops and sections in a program. Executing one part at a time and using the results to instruct the processor on the next block of codes to be executed.

If statement

This particular structure uses expressions in parenthesis together with statements or block of statements in the next line of codes. When the expression is true, then the processor is instructed to execute the block of statements or statements that were included in this condition. And if the expression is false, the processor skips the block of statements or statements and gets to the next line of codes. If statement takes two kinds of forms as explained below:

First form

{

if (expression)
block of statements;

}

Second form

if (expression)

{

statements;

}

Execution Sequence of If Statement

The order of execution for if statement is summarized below by the diagram:

![Description: 00015.jpeg](images/00010.jpeg)

Example in a program:

/* definition of Global variables */
int X = 5 ;
int Y= 9 ;
Void setup ()
{ 

}
Void loop ()
{
/* this section is used to check the boolean condition */
    if (X > Y) /* when the condition is true then the processor is to execute the

    statement below*/
    Y++;
/* this part is use to check the boolean condition */
   If ( ( X>Y ) && ( Y!=0 )) /* when this condition is true then the processor executes the statement below*/

    { 

          X+=Y;
      Y--;
    }
}

The If…else statement

This structure provides an alternative statement to be executed in case the condition is false, that is to mean when if statement is false, then there is an optional way out since there is a provision of an optional else statement to be executed.

Syntax

if (expression)
{
     statements;  //these statements are executed only when the condition is true
}
else
{
    statements; // optional statements to be executed in case the expression is false.
}

Summary of the execution sequence

![Description: 00016.jpeg](images/00011.jpeg)

Example in a program

/* definition of Global variables */
int X = 6 ;
int Y= 8 ;
Void setup ()
{ 

}
Void loop ()
{
/* this section is used to check the boolean condition */
    if (X > Y) /* when the condition is true then the processor is to execute the

    statement below*/
{   

         X++;
       }

   else

       {

    Y-=X

        }

}

If…else if…else statement

This is a special control structure where an if statement is followed by an optional else..if…else control structure. Such an expression is quite important in navigating through conditions to test whether they are true or false.

NOTE: Always remember the following points while using If…else if…else statement:

It is possible for an if statement to have none or just one else statement, and the if statement must always come after any else if’s.

It is lawful for an if statement to have none or many else if statements that must always come before the else statement.

All else if or else statements succeeded by an else if will never be executed since the processor goes by a mode of priority.

Syntax

if (first expression)
  {
    statements or block of statements;
  }
else if(second expression)
  {
     statements or block of statements;
}

.                 //other else if statements

.

.

.
else
   {
statements or block of statements;
   }

Example in a program

/* definition of Global variables */
int X = 5 ;
int Y= 9 ;
int Z=15;
Void setup ()
{ 

}
Void loop ()
{
   /* checks if the boolean condition below is true or false */
   if (X > Y) /* when the condition is true the processor is instructed to execute the statements below*/

{
       X++;
    }
  /* checks if the boolean condition below is true or false */
else if ((X==Y )||( Y < Z) ) /* when the condition is true the processor is instructed to execute the statements below */
    {
      Z=Y* X;
  }
else
    Z++;
}

Switch Case Statement

This kind of control structure works in a similar manner with if statements where the programmer is able to specify the different levels of codes that will be executed for different conditions.

A switch statement is instructed to compare the value of some variables against the specified values written within the case statement hence the name switch case. So the processor looks for a case statement with similar value to that of the switch statement then executes the codes in that particular case statement.

A break statement is used at the end of each case statement to enable the execution to exit at the end of each case. Without a break, execution will go through a state called falling-through where the switch statement will go on running the following until that point when there will a break or typically at the end of the switch statement.

Syntax

switch (variable)
{
      name of the case:
      // statements or block of statements
            break;
    }
      name of case:
    {
     // statements or block of statements
           break;
    }
  default case:
   {
    // statements or block of statements
          break;

   }
}

Example in a program:

We will use a very simple example where we will assume a variable with only three states, that is, high, low and mid representing logic levels of 0, 1 and 2\. The program is supposed to switch the code according to the right routine. The codes would therefore look like this:

switch (variable state)
{

    case 0: Low();

       break;

    case 1: Mid();

       break;

    case 2: High();

       break;

   default case: 

   Display ("Invalid state!");

}

Conditional Operator?

Conditional operator remains to be the only ternary operator in Arduino programming as well as in C programming language.

Syntax

First expression? second expression: third expression

Explanation: The first expression is executed first then depending on the outcome of this first execution, the subsequent expressions are either processed or skipped. That is to mean, when the outcome of expression is true, then the second one is executed and the sequence continues. When the first expression gives a false result then the execution skips expression two and processes expression three. Expression should give a result of either true or false depending on the condition to be satisfied.

Example in a program:

/* Find min(x, y): */
min = ( x > y ) ? x : y;
/* this portion is supposed to Convert a small letter to a capital: */
/* (parentheses may not necessarily be required in this case) */
z = ( z >= 'x' && x <= 'c' ) ? ( z - 45 ) : z;

Some of the rules to take care of while working with condition operator:              

 Always ensure that the first expression is of a scalar type.

 For the subsequent expressions, keep in mind the following: 

*   If they are two, then both must be of arithmetic type
*   If they are two, then both should be evaluated by simple arithmetic conversions which     eventually will determine the resulting type.
*   If they are two, they should both use the void set up giving a result which is void in nature.

Arduino Programming Loops

Programming loops are more or less like control structures that provide for more complicated paths for execution.

Therefore a loop statement makes a provision for the execution to process statements or a block of statements in a multiple of times. The general schematic diagram is shown below:

![Description: 00017.jpeg](images/00012.jpeg)

Arduino programming together with C language provides the following types of loops:

*   While loop
*   Do…while loop
*   For loop
*   Nested loop
*   Infinite loop

While Loop

This loop continues to execute or process infinitely until that point in time when the expression inside the parenthesis gives a false result. Actually while loop will never exit unless something changes with the nested variables.

Syntax

while(expression)
  {
statements or block of statements;
  }

Do…while loop

Do…while loop is similar to while loop only that in while loop execution, the condition for loop-continuation is tested right at the commencement of loop before execution gets to the body of the loop. While in do…while loop, execution tests the body of the loop before checking the condition for loop-continuation. 

After execution of a do…while loop execution (after termination), execution actually goes on to process those statements after the while statement.

Syntax

Do

{
     Statements or block of statements;
} 

 while (expression);

For loop

For this kind of a loop, the statements are executed for a predetermined number of successions. Within the for loop expression, the control expression is initialized, tested and changed during execution.

This presents a very easy to debug arrangement where the structure has a looping behavior which is entirely independent of the activities happening inside the loop.

For loop has three expressions inside the parenthesis which controls its operation. The expressions are separated by with semicolons.

Syntax

for ( expression initialization; control part; increment or decrement portion)
  {
         // statements or block of statements
  }

Example in a program:

for(counter=3;counter >=10;counter++)
  {
     //statements or block of statements will be executed 10 times
  }

Nested Loop

This is a technique where you can use a loop inside another loop as illustrated below by the syntax.

Syntax

for (expression initialization ;control part; increment or decrement portion)
    {
         // statements or a block of statements
for (expression initialization ;control part; increment or decrement portion)
         {
              // statements or a block of statements
         }
   }

Example in a program:

for(counter=0;counter<=10;counter++)
{
   //statements or a block of statements will be executed 10 times
   for(j=0;j<=100;j++)
    {
         //statements or a block of statements will be executed 101 times
     }
}

Infinite Loop

As the name suggests, this is a loop without a point of termination therefore executes infinite number of times.

Syntax

1\. When using for loop

for (;;)
  {
    // statements or a block of statements
  }

2\. Using while loop

while(expression)
  {
      // statements or a block of statements
  }

3\. Using do…while loop

Do

  {
   Statements or a Block of statements;
  } 

while(expression);

Arduino Functions

These are statements per see that allow programmers to structure their programs in parts or segments that are meant to perform particular tasks at a time. For example, a function would be helpful when one wants to perform a particular task a multiple times in a program.

Advantages of code segmentation into standardized fragments:

 Segmented codes presents a more organized work enhancing easier conceptualization such codes.

 During modification, code fragments are least liable to error since any mistake is easily noticeable.

 Codes stay compact and there is reduced space since most of the codes are reused several times.

 Functions presents a modular set up of codes that is easy to read and can be reused in other sections.

Arduino programming provides for two compulsory functions, that is, set up ( ) and loop ( ). Other functions must be created right outside of the brackets of the above functions.

Common syntax defining a function:

Return type function name (first argument, second argument, …..) 

      {

               Statements or a block of statements

      }

Explanation:

Return type: the type of value that is returned by the function, for example, any data type.

Function name: Identifier or title by which this function can be recalled. 

First argument, second argument…: These are parameters that are used to define the data type. 

Statements or a block of statements: Incorporates the statements or the body of the function itself.

Function Declaration

Any function is supposed to be declared outside other functions, that is, below or above loop ( ) function.

Function declaration can take two forms namely:

 Just writing the function prototype just above the loop ( ) function and this form consists of: Return type, name, and argument type. Function prototype is always followed by a semi-colon.

Example in a program:

int aver_func (int a, int b) // declaration of the efunction
{
  int c=0;
      c= a+b ;
     return z; // return the result’s value
}
void setup ()

{
    Statements // block of statements
}
Void loop ()
{
  int result =0 ;
     result = Aver_func (8,7) ; // part of the program referred to as a function call
}

 The function declaration part or function definition is declared below the loop ( ) function and consists of: Return type, name and argument type.

Example in a program:

int aver_func (int , int ) ; // part of the program called a function prototype
void setup ()
{
   Statements //    block of statements
}
Void loop ()
{
  int result =0 ;
      result = Aver_func (9,10) ; // part of the program called a function call
}
int Aver_func (int a, int b) // declaration of this function
{
     int b=0;
     b= a+c ;
     return b; // return the resultant value of b
}

Arduino Programming- Strings

The two types of strings used in Arduino programming are:

Character arrays which are equivalent to strings in C programming language

Arduino String that enables programmers to use a string object as part the sketch.

So in this chapter we will be able to identify strings, objects and which types of strings to use in Arduino programming (sketches).

String of Character Arrays

This is typically a series of characters of the data type char also called an array consisting char variables. An array therefore would mean a collection texts of the same data type and stored in a memory.

However a string is a special type of array with an extra element always zero at the end of it.

Example in a program:

void setup()
{
   char go_str[7]; // an array which can accommodate string made up of six characters
   Serial.begin(10000);
   go_str[0] = 'G'; // this string is made up of six characters
   go_str[1] = 'o';
   go_str[2] = 'o';
   go_str[3] = 'd';
   go_str[4] = 'i';

    go_str[5] = 'e';
    go_str[6] = 0; // the 7th array element called a null terminator
   Serial.println(go_str);
}
void loop()
{ 

}

This same example can be rewritten in a more convenient way as shown below:

void setup()
{
    char go_str[] = "Goddie";
    Serial.begin(10000);
    Serial.println(go_str);
}
void loop()
{ 

}

Before this string is executed, the compiler is supposed to calculate its size and automatically terminate it using the null terminator.

Manipulation of a String Array:

We will consider the sketch below to explain how to manipulate a string array.

void setup()
{
char take[] = "I do not take mangoes and tea"; // creating a string array
    Serial.begin(10000);
          // the codes below are used to print the string
    Serial.println(take);
          // the codes below are used to delete part of the string
    take[13] = 0;
  Serial.println(take);
         // the codes below explain how to substitute a text into an existing string
    take[13] = ' '; // the null terminator replaced with a space
    take[18] = 'e'; // point to insert the next new word
    take[19] = 'g';
    take[20] = 'g';

    take[21] = 0; // null terminator used to terminate the string
    Serial.println(take);
}
void loop()
{
}

Result

 I do not take mangoes and tea

 I do not take mangoes

 I do not take mangoes and egg

Explanation

First you need to create and print a string. For the sketch above, a new string was created and displayed on the Serial Monitor window.

The second process is to shorten the string using a null terminator. That means when printing the new string, characters are displayed up to that point where there is the null terminator.

The next procedure is to change a word in a string. Firstly you have to replace the new null terminator with a space so that the string is restored to its original format. The next step is to replace the individual characters in the word to be replaced, that is, t-e-a with e-g-g.

Arrays and strings have specified bounds that restrict programmers to always work within those restrictions. In the above example, we created an array of 38 characters long and therefore trying to copy and array which is longer that this may be difficult. The copied longer array will be copied over the end of the created array.

Arduino Programming- Time

Arduino programming has a total of four time manipulation functions as listed below:

 Delay ( ) function

 Delaymicroseconds ( ) function

 Millis ( ) function

 Micros ( ) function

We will discuss each of these time functions and highlight their importance in Arduino programming.

Delay ( ) function

This presents the simplest time manipulation function among the four functions. Only a single integer is used as its input or argument. This integer represents a waiting time in milliseconds that instructs the program to wait until it moves on to the next group of codes where it will encounter the delay ( ) function.

Usually this function is not recommended to instruct your code to wait as it is associated with a phenomenon called “blocking”.

DelayMicroseconds ( ) function

Just lie the delay ( ) function, delayMicroseconds ( ) also accepts only a single integer as its argument or input. The integer here represents time in microseconds which is equivalent to a thousandth of a millisecond or a millionth of a second in this case.

Record time that has been tested and proved to be able to produce an accurate delay is 16383 which is subject to change depending on future inventions in Arduino boards’ production. However, for delays less than thousand microseconds, it is advisable to use the delay ( ) function.

Millis ( ) function

The time delay used here is milliseconds, which is to mean, immediately the Arduino board runs a program, it returns a number of milliseconds. This delay time at times goes back to zero a phenomenon called “overflowing” after around 50 or so days.

Syntax

millis () ; // this function returns milliseconds from when the program begins.

Example in a program:

unsigned double delay time;
void setup(){
   Serial.begin(9600);
}
   void loop()
{
  Serial.print("delay time:");
  delay time = millis();
       //the codes below will print time since the program begun
  Serial.println(delay time);
      //this code dictate that you will have to wait for a second to prevent sending //massive amounts of data
delay time(1000);
}

Micros ( ) function

This function also returns the amount of time from the beginning of the program, the time is expressed in microseconds. Overflowing phenomenon also happens here after a period of about 70 minutes.

Syntax

micros () ; // the function is supposed to return a time period in microseconds after the program ahs begun.

Example in a program

unsigned double delay time;
void setup(){
   Serial.begin(9600);
}
void loop(){
   Serial.print("delay Time:");
delay time = micros();
          //the codes below prints time period  since program begun

  Serial.println(delay time);
        // this code dictate that you will have to wait for a second to prevent //sending massive amounts of data
delay time(1000);

}

Arduino programming- Arrays

An array is a consecutive collection of elements of the same data type located in consecutive memory locations.

In locating a particular element in array, we must specify its name and the name of its storage location. Therefore an array has two important features, that is, name and location. Identifying an array is done by giving that particular element a name then by the element’s position in a square bracket [ ]. The first element (called zero element) has a subscript zero and the subsequent elements can be represented by C[1], C[2], C[3] and the rest as shown in the figure below:

![Description: 00018.jpeg](images/00013.jpeg)

The above array is called C with 11 elements. Each element has a value for example C[10] has a value of 78.

We can therefore write programs to manipulate these values, for example, to print the sum of the values of the first three elements in the array we can write:

Serial.print (C[ 0 ] + C[ 1 ] + C[ 2 ] );

Again we can write another program to multiply the value of C[8] by 6 and assign the result to a variable called y: 

x = C[ 8 ] * 6;

Arrays Declaration

Arrays declaration helps to specify the type of element and the total number of elements in that array as illustrated below:

type arrayName [ arraySize ] ;

This instructs the compiler to reserve enough memory for the array. That is why the array size must be an integer. For example:

int D[32]; // array name is D with an array size of 32 integers

Examples of programs using Arrays

Array declaration and then using a loop in the initialization of the array elements:

int b[ 12 ] ; // array name is b with 12 integers as array size
void setup ()

{ }
void loop ()
{
  for ( int j = 0; j < 10; ++j ) // array initialization with elements
{
     b[ j ] = 0; // this codes sets element at location j to be 0
    Serial.print (j) ;
    Serial.print (‘\r’) ;
}
   for ( int i = 0; j=i < 10; ++i ) // specifies the output of each array element's //value
{
   Serial.print (n[i]) ;
   Serial.print (‘\r’) ;
} 

}

Array declaration and initialization using an initializer list:

// b is an array made up of 12 integers
int b[ 10 ] = { 23, 20, 48, 12, 16, 28, 87, 79, 69, 37, 58,17 } ;
void setup ()

{ 

}
void loop ()
{
  for ( int j = 0; j < 10; ++j ) // the codes are used for initialization of elements //in the array from n to 0
{
  Serial.print (j) ;
  Serial.print (‘\r’) ;
}
  for ( int i = 0; i < 10; ++i ) //codes that specify the output of each array //element's value
{
  Serial.print (n[i]) ;
  Serial.print (‘\r’) ;
} 

}

Multidimensional Arrays

An array of two dimensions mostly represent a table of elements consisting of rows and columns.

Some of the outstanding features of a multidimensional array:

 Has two subscripts representing the columns and rows of a table.

 The first subscript represent the elements’ rows and the second subscript represents the elements’ columns.

 Multidimensional arrays have two and more dimensions.

An example by declaration is shown below:

int c[ 3 ][ 3 ] = { { 3, 8 }, { 3, 7 } };

or int c[ 3 ][ 3 ] = { { 3 }, { 3, 9 } };

Summing all the Array elements

Those elements in an array normally represent values that are as a result of a calculation or those yet to be used in a particular math work. For example a professor may decide to enter the marks of students in a table forming an array then using the total to calculate the average marks of the class. The example below explains how this can be achieved using array functions.

const int arraySize = 5; // array size indicated by a variable called const and data type used is int

int c[ arraySize ] = { 80, 60, 50, 100, 70,};
int total = 0;
  void setup ()
{ 

}
  void loop ()
{
// the code below is used to get the sum of the contents of array c
for ( int j = 0; j < arraySize; ++j )
   total += c[ j ];
Serial.print (“ sum Total of elements of array c : ”) ;
Serial.print(total) ;
}

Chapter 10: Input, Outputs, and Sensor

One conductor is going to be used to receive data, another will be used to send information, one is going to synchronize, and the other will choose which device it will communicate with. For this to function, it will mean it is set up as the connections full duplex. This means the data can be simultaneously received and sent. The largest baud rate can be far greater than the communication system housing the i2c. 

Panel SPI Pin

The SPI is going to use four wires.

1.  SS: this will be the slave selection wire 
2.  SCK: this will be the serial clock driven by the master 
3.  MISO: the master input and the slave result. which is going to be powered by the mater 
4.  MOSI: the mast output and slave input driven by the master. 

Some of the functions that you are going to use will have to include the SPI. H 

SPI set clock divider (divider): this will set up the SPI clock divider which means that it is going to be relative to the system clock. With the AVR base panels, the divider is going to be available with two, four, eight, sixteen, thirty-two, sixty-four, and one hundred and twenty-eight. Your default setting will be SPI CLOCK DIV 4 which is going to set up the SPI clock to a quarter of the frequencies of the system’s clock. 

1.  Divider: this is going to be (SPI CLOCK DIV 2, SPI CLOCK DIV 4, etc.) 
2.  SPI transfer (Val): the SPI is going to be assigned based on the sending and receiving that will occur at the same time. The data that is obtained will be returned in a standard Val form. 
3.  SPI begin transaction (SPI setting (speed maximum, data order, data mode)) the top speed is going to be clocked with data order (MSBFIRST or LSBFIRST) 

There are going to be four modes of operation that the SPI is going to follow

1.  Mode 0 (default): the clock is naturally going to be low, and the data that is obtained from the transition can be visualized when the data itself goes from the bottom end of the spectrum to higher levels. This will be what is known as the leading edge. 
2.  Mode 1: this is going to be considered the trailing edge whenever the data is going from high to low
3.  Mode 2: this is also going to be the leading edge when your data goes from high to low. 
4.  Mode 3: the data here also goes from the low end of the spectrum to the high. In this instance, it is known in the industry as the trailing edge. 
5.  SPI attach interrupt (handler): the function is going to be summoned as the slave device gets its data from the master.

At this point in time, you are going to connect two Uno panels together with one being the slave and the other being the master. 

Pin ten will be SS

Pin eleven will be MOSI

Pin twelve will be MISO

Pin thirteen will be SCK

The ground is going to be common, and in the following image, you are going to see the connection that is going to occur between both panels. 

![Description: Connection of Boards](images/00014.jpeg)

Advanced Strategies for Arduino

Speeding Up the Input and Output Access

On each AVR Arduino panel, the clock speed is going to be sixteen MHz. Every instruction that is located on the controller is going to be completed in under four cycles; therefore, you are going to be able to do four million instructions in a single second. But, the input-output speed is going to be a lot slower. This happens due to the digital write and digital read functions. Each time that a function is executed, there is going to be extra code that has to be executed as well. The additional code is going to end up being responsible for detecting and mapping out the digital pins to the output port. On every microcontroller, the input-output device will be allocated in a group of eight pins to a port which is going to be specially registered to the controller. 

Therefore, the next question is going to be, how slow is it? You will figure this out by using this code. 

You will be able to improve the program by wrapping the loop code into an infinite loop. This is going to speed up the execution since the CPU is going to be doing less of a function call. This should speed up your input and output so that it is up to ten percent faster. If you want to top the output speed, you are going to have to use a low-level access port and to do that, you are going to have to learn how to use the microcontroller; however, it is going to take away from the beauty of the Arduino machine. However, there is going to be a library that you can use to increase the input and output access. 

Keep in mind that there are going to be limitations because it is mainly going to support the Leonardo, Mega, Uno, Nana, and Attiny models. 

This is going to provide an inline function for faster input-output access.   

Analog Readings

Analog readings on a USB powered Arduino model is going to give you some unexpected results. This happens because the analog reference voltage will be tied to the logic voltage which is typically going to be five volts, however, if you are powering your panel from a switch power supply or from the USB you are going to be dealing with commotion and voltage drops because of the USB cable. This is possible as long as your controller is running at four point five instead of five volts. 

It is not going to be ideal when it comes to precision measurements. To do the proper measurements, you are going to have to use an external precision voltage reference. On the other hand, you can use the voltage reference that is built into the chip to measure the current VCC and do the calculations that have to be done.   

Getting Free RAM

In this section, you are going to learn how to get the free RAM returned in bytes. 

Using the Const, Program and Global Variables

In the event that you are having to store a large amount of data in the code that you are using, then you are going to need to make a global const and include the program statement. This is going to tell the program's compiler to store the data in the program memory instead of on the RAM 

Forgetting the Default IDE

While the IDE that comes with Arduino is great, it is not going to be suitable for use with professional software development. If you are using it, you are going to realize that it is going to become a pain to use once you have written a program that has more than a few hundred lines. 

So, to bypass this, you will use the Atmel Studio or the Visual Studio that comes with the Visual Micro plugin. This plugin is going to have a debugger, but it is vital that you know that it is not free, it is going to cost you seventeen dollars. 

You can also use a text editor so that you can write out your programs. However, with Arduino one point five, the IDE is going to support the building and uploading of your program through the command line. 

Syntax 

Arduino --panel (panel type description) --port (serial port) --upload (sketch path)

Arduino --panel (panel type description) --port (serial port) --verify (sketch path)

You will need to have a panel type description as well. 

Syntax 

package:arch:panel[:parameters]

You are going to be able to find out more about the command line through the manual documents for Arduino IDE. 

Inlining Small Functions

There is a manual that says that the inline function is as fast as a macro. But, there is a catch. If you make an inline function, it is going to make your code size larger; especially if you call the function in several places. 

Chapter 11: Arduino function libraries

I/O Function; advanced I/O function; etc.

Functions in Arduino

The Arduino board comes with a number of pins. These pins can be configured to act as either inputs or outputs. It will be good for you to note that most of the Arduino analog pins can be programmed and used in the same way as the digital pins. 

INPUT Pins

Pull-up Resistors

Pull-up resistors are used to steer up an input pin to a particular state if no input is available. We can do this by adding a pull-up resistor (to +5V) or a pull-down resistor on the input. You can use a 10K resistor for a pull-up or pull-down resistor. 

The Atmega chip has 20,000 pull-up resistors and all can be accessed from the software. To access these built-in pull-up resistors, we set the pinMode() to INPUT_PULLUP. This will invert the behavior of the input mode. A value of HIGH will mean that the sensor is ON while a value of LOW will mean that the sensor is OFF. The value of the pull-up will depend on the type of microcontroller that has been used. This value ranges between 20kΩ and 50kΩ on most AVR-based boards. This value ranges between 50kΩ and 150kΩ on Arduino Due. The exact value is shown ion the datasheet on the microcontroller of the board.

When you connect a sensor to a pin that has been configured with INPUT_PULLUP, you should connect the other end to the ground. If the pin is simple, this will cause the pin to read HIGH when the switch is open and LOW when the pin is pressed. Pull-up resistors can provide enough current to light an LED dimly that has been connected to a pin that has been configured as an input. If you see working LEDs, but lighting dimly, this could be the reason. 

The following example demonstrates this:

pinMode(3,INPUT)  ;  //set the pin to input mode without using a built-in pull up resistor

pinMode(5,INPUT_PULLUP)  ;  //set the pin to input using a built-in pull up resistor

Output Pins

A pin that has been configured as OUTPUT using the pinMode() function is said to be in the low-impedance state. Such a pin is able to provide a significant amount of current to other circuits.

When you attempt to run high current devices from output pins, you can damage the output transistors in the pin, or destroy the entire Atmega chip. In most cases, this results in a dead pin on the microcontroller but the rest of the chips will function normally.

The pinMode() Function

We use this function to configure a particular pin as either an input or an output pin. If you need to enable the internal pull-up resistors, you can use this function with the IINPUT_PULLUP mode. When you use the INPUT mode, it will disable the internal pull-ups. 

The pinMode() function takes the syntax given below:

Void setup ()  {

pinMode (pin, mode);

}

The function takes two parameters as shown in the above syntax. The first parameter is a pin, which is the number of the pin whose mode you need to set or modify. The mode is the state you want to set the pin to, and it can be INPUT, OUTPUT, or INPUT_PULLUP.

Consider the example given below:

int btn =  5  ;  // The button connected to pin 5

int LED =  6;  // The LED connected to pin 6

void setup ()  {

   pinMode(btn , INPUT_PULLUP); 

 // set the digital pin as input with a pull-up resistor

   pinMode(btn , OUTPUT);  // set the digital pin as output

}

void loop ()  {

 if  (digitalRead(btn )  == LOW){  // if the button is pressed

      digitalWrite(LED,HIGH); // turn the led on

      delay(500);  // delay for 500 ms

      digitalWrite(LED,LOW); // turn the led off

      delay(500);  // a delay of 500 ms

}

}

We created two variables, btn and LED. These denote the button connected to pin 5 and the LED connected to pin 6 respectively. Inside the setup() function, the digital pin was set as input with a pull-up resistor. The digital pin was also set as output.

The logic for the sketch has then been implemented in the loop() function. When the button is pressed, the LED will be turned on and delay in the stated for 500 milliseconds. The LED will then turn off and delay in that state for 500 milliseconds.

The digitalWrite() Function

We use this function when we need to write a value of HIGH or LOW to a digital pin. If the pin had been configured to be OUTPUT using the pinMode() function, it will be assigned a corresponding value of voltage (which is 5V or 3.3V on 3.3V boards) for HIGH, oV (which is ground) for LOW.

If the pinMode() function is not set to OUTPUT, then a LED is connected to a pin, a call to digitalWrite(HIGH) may make the LED appear dim. If you don’t set pinMode() explicitly, the digitalWrite() function will enable the internal pull-up resistor, which will act like a large resistor resisting the flow of current.

The digitalWrite() function takes the following syntax:

Void loop()  {

digitalWrite (pin ,value);

}

The function takes two arguments, pin and value as shown in the above syntax. The pin denotes the number of the pin whose mode you need to set. The value argument can take a value of either HIGH or LOW. 

Consider the following example that demonstrates how to use the digitalWrite() function:

int LED =  6;  // A LED connected to pin 6

void setup ()  {

   pinMode(LED, OUTPUT);  // set the digital pin as output

}

void loop ()  { 

   digitalWrite(LED,HIGH);  // turn the led on

   delay(500);  // delay for 500 ms

   digitalWrite(LED,LOW);  // turn the led off

   delay(500);  // a delay of 500 ms

} 

We created a variable named LED to denote the LED that has been connected to pin 6\. In the setup() function, this pin was set to act as an output pin. In the loop() function, we have used the digitalWrite() function to turn the pin on and off. A delay of 500 milliseconds has been added.

The analogRead() Function

Arduino whether a voltage has been applied to any of its pins then reports this using the analogRead() function. A difference exists between an on/off sensor and an analog sensor. The on/off sensor detects the presence of an object while the value an analogue sensor changes continuously. For us to read an analog sensor, a different type of pin is required.

The lower part of the Arduino board has six pins that have been marked Analog In. These pins are able to tell whether a voltage has been applied to them as well as the value of this voltage. The analogRead() function can help us read the amount of voltage that has been applied to any of these pins.

The function will always return a value ranging between 0 and 1023, which is a representation of voltage between 0 and 5 volts. For example, if a voltage of 2.5V has been applied to the pin number 0, the analogRead(0) will read a value of 512\. The 0 passed to the function is the number of the pin. This means that the function takes the number of the pin as the argument as shown in the following syntax:

analogRead(pin);

The pin parameter is the number of analog pins whose value is to be read. Here is an example that demonstrates how to use the analogRead() function in Arduino:

int analogPin =  3;// a potentiometer wiper

 // connected to the analog pin 3

int x =  0;  // variable to store the read value

void setup()  {

   Serial.begin(9600);  // setup serial

} 

void loop()  {

x = analogRead(analogPin);  // to read the input pin

   Serial.println(x);  // print the value

}

We began by creating a variable named analogRead and assigning it a value of 3\. This variable denotes a potentiometer wiper that has been connected to the analog pin number 3. We have also created a second variable, x, and assigned it a value of 0\. We will use this variable to store the value that has been read from the pin, which is the voltage applied to the pin. In the loop() function, we have called the analogRead() function and passed the value analogPin to it as the parameter. This will read the value of the voltage on the analog pin number 3 and store the read value in the variable x. We have then printed out this value. 

The analogReference() Function

This function configures the reference voltage that is used for analog input, that is, the value that has been used as the top of the input range. The function can take any of the following options:

DEFAULT – This is the default analog reference of 5 volts on the 5V Arduino boards or 3.3 volts on the 3.3V Arduino boards. 

INTERNAL – This is a built-in reference, which is equal to 1.1 volts on ATmega168 or the ATmega328 and 2.56 volts on ATmega8\. It is not available on the Arduino Mega. 

INTERNAL1V1 – This is a built-in 1.1V reference. It is available on Arduino Mega only. 

INTERNAL2V56 – This is a built-in 2.56V reference.  It is available on Arduino Mega only. 

EXTERNAL – This is the voltage applied to the AREF pin, that is, 0 to 5V only, and it is used as the reference. 

The function takes the following syntax:

analogReference (type);

The parameter type can be any of the options discussed above.

Avoid using anything that is less than 0V or above 5V for external reference voltage on the AREF pin. In case you are using an external reference on the AREF pin, you should set the analog reference to EXTERNAL before you can call the analogRead() function. If you don’t do this, you will short the active reference voltage, which is generated internally, and the AREF pin, which may damage the microcontroller on your Arduino board.

You can also connect the external reference voltage to the AREF pin via a 5K resistor, which will allow you to switch between the internal and external reference voltages. The resistor will change the voltage that has been used as the reference since the AREF pin has an internal 32K resistor. The two will act as a voltage divider.

The following example demonstrates how to use the analogReference() function:

int analogPin =  3;// a potentiometer wiper connected to analog pin 3

int x =  0;  // a variable for storing the read value

void setup()  {

   Serial.begin(9600);  // to setup serial

   analogReference(EXTERNAL);  // voltage applied to AREF pin

 // is used as the reference.

}

void loop()  {

x = analogRead(analogPin);  // to read the input pin

   Serial.println(x);  // to print the value

}

We began by creating a variable named analogRead and assigning it a value of 3\. This variable denotes a potentiometer wiper that has been connected to the analog pin number 3. We have also created a second variable, x, and assigned it a value of 0\. We will use this variable to store the value that has been read from the pin, which is the voltage applied to the pin. 

Consider the following line extracted from the code:

analogReference(EXTERNAL);

This line simply means that the voltage that is applied to the AREF pin, which ranges between 0 and 5V, will be used as the reference. 

In the loop() function, we have called the analogRead() function and passed the value analogPin to it as the parameter. This will read the value of the voltage on the analog pin number 3 and store the read value in the variable x. We have then printed out this value. 

Character Functions

We enter data into a computer in the form of characters. The characters can be letters, digits and other special symbols.

The library for handling characters comes with a number of functions that we can use to test and manipulate characters of data. Every function receives data in the form of int, or EOF as an argument. This means that the characters are manipulated as integers. 

The EOF usually has a value of -1 and some hardware architectures don’t allow for the storage of negative values as char variables. This means that the functions for handling characters manipulate them as strings. 

Anytime we need to use the functions for handling characters, we should add the <cctype> header to the program. The following the different functions provided by the character-handling library:

The isdigit function checks whether its argument is a digit or not. The isalpha function determines whether the argument passed to it is an uppercase letter, that is, A-Z, or lowercase letter, that is, a-z. The isalnum function checks whether the argument passed to it is an uppercase letter, a lowercase letter or a digit. The isxdigit function checks whether the argument passed to it is a hexadecimal digit, that is, A-F, a-f or 0-9. 

The conditional operator (?:) can be used with every function to determine whether the string “ is a” or “ is not a” should be printed in the output of every character that has been tested. 

We now need to create an example that demonstrates how to use the isupper and the islower functions. We use the isupper function to check whether the argument passed to it is uppercase, that is, A-Z. We use the islower function to check whether the argument passed to it is lower, that is, a-z.

The code will return the following when executed:

The islower function returns:

m is a lowercase letter

M is not a lowercase letter

6 is not a lowercase letter

! is not a lowercase letter

The isupper function returns:

D is an uppercase letter

d is not an uppercase letter

9 is not an uppercase letter

$ is not an uppercase letter

We now need to create an example that demonstrates the use of isdigit, isalpha, isalnum andisxdigit functions. The isdigit function helps us check whether the argument passed to it is a digit, that is, 0-9\. The isalph function helps us check whether the argument passed to it is an uppercase letter, that is, A-Z, or a lowercase letter, that is, a-z. The isalnum function determines whether the argument passed to it is a lowercase, uppercase letter or a digit. The isxdigit function checks whether the argument passed to it is a hexadecimal digit, that is, a-f, A-F, or 0-9\.

Conditional Operator

The conditional operator (?:) is used with every function to determine whether the string “is a” or “is not a” should be printed in the output of every character that is tested. 

We now need to create an example that demonstrates how to use the islower and the isupper functions. The islower function checks whether the argument passed to it is a lowercase letter, that is, a-z. The isupper function checks whether the argument passed to it is uppercase, that is, A-Z.

Chapter 12: Computer interfacing with an Arduino

The FTDI Chips; Example of Temperature sensors with serial interface

Before you begin to program your Arduino, you will need to understand the basic sketch of a microcontroller. A sketch is the term used to describe an Arduino program. It is the code uploaded to an Arduino board, where it then runs to allow the microcontroller to perform specific functions. Now that you know what a sketch is, you should be able to comprehend how they work with Arduino commands. The most basic commands of Arduino involve the digital and analog pins. We will discuss these in this chapter. However, remember that these are only a small amount of the commands that you can complete using the Arduino board. These commands are used in conjunction with input and output values to write codes. Arduino codes can be long and complex. Many of them are found in the Arduino library. The flexibility of the program even allows you to write your own coding in the event that you cannot find coding to make your project perform the function that you want it to.

Basic Commands

The basic Arduino commands include BareMinimum, Fade, Blink, ReadAnalogVoltage, AnalogReadSerial, and DigitalReadSerial.

BareMinimum: The least amount of coding needed to run an Arduino sketch. Two command lines are used with this. Void setup( ) and void loop ( ). The setup function runs once each time the board is started and once when the board is reset. The loop function is used to allow your program to respond and change to your commands. 

Fade: This command is used with an analog output to fade an LED light on your Arduino board.

Blink: The blink command will make an LED turn on and off.

ReadAnalogVoltage: This command will allow the microcontroller to read an analog input, before printing the voltage onto the serial monitor of the Arduino.

AnalogReadSerial: This command is responsible for reading a potentiometer. It can then print the state of the potentiometer to a serial monitor.

DigitalReadSerial: This command lets the Arduino read a switch. Then, the Arduino will make this visible by printing the state to a serial monitor.

Analog

The analog commands are designed to work specifically with the analog inputs and outputs on the Arduino board. These include Analog Input, AnalogInOutSerial, Calabration, AnalogWriteMega, Smoothing, and Fading.

Analog Input: This command is used with a potentiometer to cause an LED to blink on and off as needed.

AnalogInOutSerial: This command works by first reading an analog input pin. Then, AnalogInOutSerial maps the result of the input pin and uses those results to cause an LED light to either brighten or dim.

Calibration: This command is used to define expected values for an analog sensor using a minimum and maximum value.

AnalogWriteMega: This command is designed to work with the Arduino Mega microcontroller. It sequentially fades 12 separate LEDs on and off.

Smoothing: The smoothing command is used to smooth analog input readings if there are several of them.

Fading: As the command name suggests, the fading command is responsible for causing an LED to fade. It does this using a PWM pin.

Digital

The digital functions can play musical tones, control the function of LEDs, and read pushbuttons. These functions include Simple Keyboard, Tone, Tone4, Pitch Follower, Debounce, Button State Change, Button, and Blink Without Delay.

Simple Keyboard: This turns your Arduino into a musical keyboard with three keys by using a pizo speaker and force sensors.

Tone: This command is to be used in conjunction with a Piezo speaker to play a melody.

Tone4: This uses the tone command with multiple speakers to play sequential tones.

Pitch Follower: This uses an analog input and a Piezo speaker to play a certain pitch.

Debounce: This command is used to filter noise by reading a pushbutton that has been linked to your Arduino.

Button State Change: This command allows your Arduino to count the number of times a button has been pressed.

Button: The button command allows your Arduino to control an LED when an attached pushbutton is pressed.

Blink Without Delay: This command allows an LED on your board to blink without the delay function, meaning it can blink faster or remain constantly lit.

Chapter 13: C language Basics

The Memory Maps

When you create an Arduino program, it is essential to have some knowledge about the working of computer systems. Even though C programming is the language that is close to the machines, how certain things are done when the program runs will become clear.

A primary system consists of the control device referred to as the CPU or microcontroller. There are a few differences when it comes to some of these. We shall dig deep into this later. Just to mention, microcontrollers may not be that powerful compared to the standard microprocessor. However, it still contains input, output ports, as well as hardware functions.

Microprocessors are connected to the external Memory. Generally, microcontrollers contain a sufficient amount of onboard memory. However, it should be noted that we are not referring to the large sizes; it is possible for a microcontroller to have only a few hundred bytes or so of memory for the simple applications. Don’t forget that a memory byte has 8 bits, and each bit can either be true or false, high or low and I/ O.

When it comes to the relation between the processor and the functional data stored in the memory, data must be kept in the processor’s register. The register is the only place where we can have logical mathematical operations carried out. For example, if you would like to carry out an addition of two variables, the value of the variables has to be moved over to the register.

Memory Maps

Each memory byte in the computer system has a connected address. Now, if we do not have the address, the processor will not have a means to identify a particular memory. In general, the memory address begins from 0 as it increases. Even though we have specific addresses with a private or unique system, a particular address may not point to the input and output port of external communication.

Most of the time, you will find it necessary to map-out the memory. This is merely a massive array of memory slots. We have people who develop a memory map and have the address with the least value positioned at the top while others who draw a memory map and assign the least address at the bottom. Each address points to a place where it can have the byte stored. However, the C compiler will complete this. For instance, if we declare the char variable as –X. It can be located at address 2, so if we print the value, there would be no need to select the value at the address 2\. We will instead write, “select the X value” where the compiler produces code to ensure that it works correctly to the right address. Using this level of abstraction simplifies the whole process. However, since most variables carry a specific amount that is higher than one byte, we might have to collect these addresses to hold only a single value. For example, if we pick a short int, then it will require us to have two bytes. Now, if the following address starts at four, there is a need to use the address 5. When we choose to access this particular variable, the compiler will automatically build the code and make use of all the addresses since it is aware of the presence of the short int.

Stacks

Most programmers prefer to use temporary storages for the variables. What this means is that there are variables that are used for a short period then they are discarded. Therefore, it will not be right if we move on and allocate a permanent space for this particular variable. Ordinarily, an application is made up of two parts: the code and the data. The data part is permanent since these two parts cannot consume the whole memory; the remaining memory is used temporarily for storage via the stack. It starts at the opposite end of the memory map; the stack increases towards the data part as well as the code. It is similar to the stack of trays. The first tray on the stack will be the last to be pulled off. Any time temporary variables are needed, this part of the memory is used. Given that many items are required, most of the memory will be used up. When the code ends, the temporary variables declared are no longer useful, and therefore the stack shrinks.

The Basics of C-language

C language is designed for professional developers who want to accomplish many things with less code. C is a compiler language. This shows that once we have written the program, we must transfer it into the compiler that will begin to change the C language instructions into a machine code that the microcontroller can manage.

As you can see, this is an additional step to take, but it will result in a better program compared to the interpreter. After this, the interpreter will convert the code from the machine language.

It is crucial for the machine to have an interpreter. You can look at it as a compiler that translates it once instead of line-by-line.

However, C is not the same as in other languages. It is a free-flow language. We have the statements, functions, and variables. Variables, as we have already seen, are objects that can store things. It can be a floating-point number or other types of variables. Statements have assignments, operations and so on.

Functions have statements and can call other functions.

How to name variables, and declare

The naming of variables in C is quite easy. Names of variables carry with them numerals, underscores, and letters. You can as well combine the upper and lower case. However, the length cannot go past the 31 characters. However, the actual limit depends on the C compiler. In addition, variables cannot contain reserved keywords or unique characters like a semicolon, comma, and other special characters. Therefore, valid names can be names such as resistor8, volt5, and we_are_variables. C language has different variable types. Some of them consist of floating-point numbers and real numbers in two forms. First, there is the 32-bit float, and then the double. We also have a few types of integers that consist of char, 16 bits, short int, and 32 bits long int. Though char is only an 8 bit, still has a 2 to the 8th combinations – or even 256 separate values that you will find it perfect for a single ASCII character. Similar to other languages, the C language has arrays and compound data types. When it comes to variables in the C language, it is vital for the variables to be declared before they are used. Variables cannot just be created instantly like the way it happens in the Python language. Variable declarations are made up of the variable type and variable name. You can also include an initial value for the variable during the declaration, but that is optional. Multiple variable declarations are still allowed in C language. For instance:

Float c = 1.2;

Char c;

Unsigned char x;

You should underline that every type of variable declaration ends with a semi-colon. Like many other programming languages such as Java, the semi-colon indicates the end of that statement.

Functions

Functions have a similar naming rule like variables. All functions have a similar syntax that resembles: Return_value function_name (function argument list) { Statement( s) } You can borrow the concept of mathematical functions where you assign it some value( s) as well as allocate back some values. An example is a calculator that contains the cosine function. It is possible to assign an angle to it, and this will return a specific value. Functions may contain separate arguments in the C language. Furthermore, it is possible for a C function to return values. A void function is one that does not require a value or return a value. A void function will look like this:

void function_name (void)

{

// necessary statements come here

}

This might look like a lot of work, but the data types in the C language make sense. What this means is that if you choose to use a wrong kind of variable in a function, or even an incorrect number of variables, you will receive a warning.

Therefore, if you have a float function and attempt to send it an integer variable, the compiler will send you a warning. Every program must have a start and an end. In the C language, all programs begin at the main function. You can look at the program below:

void main (void) 

{

float y = 3.0;

float f = 2.0;

float t;

t = y* t

}

There exists one main() function. It accepts no variables and returns nothing.

Libraries

The previous example is limited because it is hard to see the result. Therefore, you will need some methods when you want to display the results on your computer screen. To achieve this, it will depend on the libraries and systems functions. Countless libraries have the most advanced C systems. In essence, somebody has just tested, compiled and wrote a collection of functions. What you need to do is to link the functions into the program. Linking helps integrate the code and any existing library into an entire program. To display the general data and the input data, we use the standard IO and the stdio.

The stdio library has a function called printf().

The program will display the words “Hello World” on the computer screen. It will further insert a new line after the backslash-n combo. The \n refers to the addition of a new line. If we failed to include the #include directive, the compiler will not understand anything concerning the printf(), and it would show up an error when we attempt to use it. Well,what about the header file? The header file has a lot of different function prototypes. These prototypes can be seen as templates but if you want, you can build your own. To make use of it, you are required to have the correct include statement written into the code, and it will be better set if you remember to include the linker library code. This will not only save time but also allow you to reuse the code.

Simple Math

C has certain basic math operators just like other languages. Some of them include the -, +, / and the multiple. Parentheses help divide the elements and power hierarchy operations. The C language has the % operator that represents modulo. The modulo is an operation which carries the remainders of a division. For example, 8 modulo 18 would, of course, be 2\. The division will behave separately both to integers and floats which have no remainder. In other words, integer 5 divided by 2 is 2, and not 2.5\. Within the C language, there is a sequence of bit manipulators useful for situations such as this. For complex math operators, you will have to go deep into the math library. Some of the examples are log (10), tan(), cos() and sin().

However, you should not attempt to use the ^ operator because it has a separate meaning in the C language. Well, do you still remember what we said earlier about the use of libraries? Placing certain functions such as sin() into your code forces the compiler to define the prototypes along with other related information. Therefore, during the start of the program, it will be necessary to include the following line:

#include < math.h >

C Language Input and Output

We know that the prinf() function displays the information on the screen. The printf() is an extensive and complex function which has a lot of variants and format specifiers. The format specifiers comprise of the % stuff applied as the placeholders for the values.

Take for instance, if we want to show the value of a variable in the decimal form. We could have done it this way: printf (“ The value is %d, in hex %x, and in octal is &o.\ n”, value1, value1, value1); You should see the way we have labeled the variables. This is critical because if you make a mistake and display a value that has no label, it will be impossible to tell whether it is a hex or decimal. For instance, if you see a number like 22, how will you tell that the number is a decimal or hex for that matter? It is impossible to know.

Besides indicating the label, you can print it with a field width. For instance, %6d is equivalent to writing the integer in the decimal with a minimum space of 6\. Similarly, %6.2f implies that you print the floating-point value with a minimum of 6 spaces. The .2 part is an exact specifier, and in the following example, it shows two digits after the decimal point. You can then see how powerful and flexible this function looks. The input function for the C language is the scanf(). This resembles the Python’s input statement. Even though it is possible to request different values at once, it is the best.

It comes with similar specifiers like the printf(). So, there is a point which needs to be understood, and the scanf() function will require you to specify the location where the value is kept in the computer memory. This shows that just writing the name of the variable is not enough. You need to describe it in detail. C has the & operator which means the address of. For example, when you want to select a specific integer variable from a user and store it snugly inside the voltage variable. Here is the code fragment for you to look at:

printf (“ Kindly type in the voltage”); scanf (“% d,” &voltage);

There are hundreds of communication procedures that are defined by Arduino and will be used to achieve the data exchange. Every procedure is going to will be placed into one of two categories, serial or parallel. 

Parallel

A parallel connection between the peripherals and Arduino will be established through input and output ports so that there is a shorter distance of several meters. But, in some cases, it is going to be required that communication is established between two pieces of equipment over a longer distance, and you are not going to be able to use parallel connections. Parallel interfaces will move a group of bits at the same time. They will typically require a bus of data that are going to transmit through the wires labeled eight and sixteen. The data transfer is going to be massive. 

![Description: Parallel Communication](images/00015.jpeg)

Pros and Cons

While parallel communication is going to have its advantages, such as it is faster and more straightforward as well as easier to implement. However, it is going to require a lot of input and output lines and ports. If you find that you need to move a project from an Uno panel to a Mega board, you are going to have to know the input-output lines on the microprocessor, and you will be aware that there are not going to be many. So, you are going to discover you like to use serial communication which means that you are going to be sacrificing the potential speed for pin real estate. 

Serial Communication

In most panels that you are going to use today, there are several systems that are built in for serial communication. 

The system that is used will be determined by the following factors: 

1. Do you need to be able to send and receive data simultaneously? 

2. How many pieces of equipment is the microcontroller exchanging data with? 

3. What is the space between the pieces of equipment? 

4. How fast does the data transfer need to be?

It is of vital importance to establish procedure whenever you are working with serial communication. The procedure is going to have to be strictly observed. This set of rules is going to be applied so that the device knows how to interpret the data that is being exchanged. Thankfully, Arduino is going to automatically take care of this so that the user is dealing with clear data. 

Types of Serial Communication

1.  Asynchronous: a device that is asynchronous is going to have its own clock that will be triggered by an output of the previous state. 
2.  Synchronous: for a device that is synchronized with another, it is going to be using the same clock, and the timing is going to be synchronized with each other. 

It is going to be easy to discover if the device you are using is synchronous or not. Should the same clock be given to all the pieces of equipment that are connected, then they are going synchronous. However, if there is no clock line, it is going to be asynchronous. 

An example would be the UART – universal asynchronous receiver transmitter – module will be asynchronous. 

The asynchronous procedure is going to have several rules built in. these rules are not going to be anymore more than mechanisms that are going to help to ensure data transfers are robust and error-free. The mechanisms are going to be: 

1.  Baud rate 
2.  Synchronization bits 
3.  Parity bits
4.  Data Bits 

Synchronized Bits

Synchronized bits are two or three bits that are special and will be transferred with every packet of data. They are going to be bits designated for starting and stopping the sending of data packets. Just like their name suggests, these bits will mark the beginning and the end of a packet. 

There is always going to be a single start bit, but there can be multiple stop bits that can be configured to each other. 

Your start bit will always be indicated by an idle data line that is going to go from one to zero while the stop bits are going to transition to idle holding the line at one. 

![Description: Synchronization Bits](images/00016.jpeg)

Data Bits

The magnitude of data that is in each package will have the option of being set five to nine bits. The standard size is going to be eight bits; however, the other bit sizes are going to have their uses. Like a seven-bit packet is going to be more efficient than an eight bit if you are transferring seven-bit ASCII characters. 

Parity bits

You are going to have the option of picking whether there should be a parity bit or not and if they decide there should be, then the parity bit is going to be odd or even. The parity bit will be zero in the event that the digital representation of ones inside the data bit is even, then the odd parity will be labeled as the opposite. 

Baud rate

This function is going to be used to denote the digital representation of bits that are being transferred per second. Keep in mind that this is going to refer to bits and not bytes. The baud rate will typically be required by the procedure that each byte is transferred along with several control bits. That means that for every one byte there will be eleven bits. 

Uart

Once the sketch has been uploaded to Arduino, you are going to have to open serial monitor which is located at the top right of the IDE. 

You can type in whatever you want in the top box of the serial monitor and press send. This is going to send a series of bytes to the Arduino panel that you are using. 

The code will return whatever is received as an input.

Chapter 14: Arduino clones and similar boards

The Microcontroller/ Main Chip

This is the brain of the Arduino board. This is the part which is programmed. It is the one responsible for running the code, hence it can be seen as the CPU (Central Processing Board) of the board. 

This chip has some legs, which are usually plugged into the socket. These can be seen once it is taken out of the socket. However, they are not referred to as “legs” but “pins”. 

Power Jack and Supply 

There are two ways on how you can supply power to your Arduino board. You may choose to use a USB connector to establish a connection to a computer or some portable power jack, or you may choose to plug it to the wall adapter. The USB can be used for powering and programming. The DC is only used for powering the board, and it is the best if you are in need of connecting the board and leaving it for some long-term project. 

USB Jack and Interface 

The USB Jack is the cable that helps you connect your board to the computer. You can use any computer, provided it has a USB port. 

Some processor chips will fail when you are using a USB cable for connection to a computer. In such a case, you will have to use the serial interface. You must have a USB to the serial interface translator chip. 

The LEDs

The Arduino comes with some lights from which you can draw ideas regarding what it is up to. The lights are referred to as LEDs. The Arduino board comes with 4 LEDs which are L, RX, TX, and ON. On the UNO board, you will find three of these at the center and one on the right side.   

The ON LED will turn to green once you have powered the Arduino board. In case you find it off or flickering, then just check on your power connection. 

The RX and TX boards will blink whenever data is being sent from the board or being received on the board. The TX LED will light yellow once you send data from Arduino to the computer USB port. The RX LED will light yellow whenever data is sent to Arduino from the computer’s USB port. 

The LED is the one that you are able to control. The other 3 LEDS usually light automatically. The L LED has been connected to the main chip of the Arduino. This can be turned on and off once you begin to write the code. 

Headers

This is the main part of the Arduino board. These are the two lines of sockets that line up with edges of the circuit board. The thin sockets will allow you to plugin some wires into them. The wires can, in turn, be connected to any types of electronic parts including sensors, LEDs, displays, motors etc. 

USB Fuse

The little USB fuse protects the computer and the Arduino. There are high chances that all types of wires will be connected to the Arduino, which may cause an accidental short on the wires. The importance of this fuse comes during this time. It is resettable, and in such occurrence, it will just open up in the same way a fuse or circuit breaker works. This will protect your board from damage. 

Reset Button

This button is located next to the USB jack. However, on some other boards, you may find it on the right side. It is the button that can be used for restarting the Arduino. Restarting the board will only take a second, and it is done if it gets stuck or if you need to re-run some program. 

Power up Test

We are now ready to power on our Arduino board. You can simply do this by connecting one end of your USB cable to the Arduino board and the other one to your computer. The computer will act as the source of power for the Arduino.

If you are using Arduino UNO, then the USB cable should have its end as square B-type. The USB cable should be plugged directly to the computer port. After you are sure that you are able to power the Arduino then upload the sketches, you will be set. You can then plug it to the other ports. For you to know whether the power source is working correctly, just check on whether the ON LED is lit green. The L or yellow LED may also blink or light up, which the same case with the RX and TX LEDs. 

Chapter 15: Troubleshooting

Arduino Board Testing

In the process of circuit building, there will come a time when nothing will be working. This moment will call for a process of troubleshooting and debugging in order to identify and solve the problems with your experiment.

Key points to a successful troubleshooting:

Understanding: Always ensure that you properly understand all the components used in your experiment. Clearly mark out the power flow all these components are connected with one another.

Simplification and Segmentation: This is more like divide and rule tactic where you break down the project and figure out the problem with each and every component

Exclusion and Certainty: This involves investing each part separately and being sure of their functionality. Through this you will be able ascertain the problem with each component.

Board testing therefore involves “Blinking an LED”, if it does not work, check on the USB connection and other more options explored below.

Breadboard Circuit Testing

Run a short circuit test by connecting your Arduino board to the breadboard. If the PWR LED turns OFF then there is a serious short circuit connection on your board. Quickly begin segmentation and simplification to find the wrong connection.

Problem Identification

Some of the common problems with Arduino programming are listed below:

 Arduino IDE not launching: Use the run.bat files as alternative option.

 Windows Operating System assigning a COM port which is greater to Arduino: Solve this by convincing windows to assign a lower COM port. For other versions of Windows, follow the procedures described earlier in this book about Port Identification.

Problem Isolation and Solving

This option provides for you to reproduce a problem. When your circuit exhibits some problems, find out the exact place and place (component) associated with that particular problem. This will help you to correctly describe a problem and possibly suggest a solution.

Online Help

In case the above suggestions do no work, you are welcomed to seek online help on the Arduino website: www. Arduino.cc/en/Guide. While seeking online help, be sure to specify the following parameters:

 The type of Arduino board you are using.

 The Operating System you are using to run Arduino IDE.

 Give a general description of your problem.

 Of course use CAPITALS to specify all these.

CONCLUSION

This marks the end of this book. You can program the Arduino board so as to come up with complex systems. An example of such a system is one that controls access to a facility.  You can use Arduino to program the door that grants access to the facility. Arduino is good for hardware programming. If you are familiar with the C programming language, then it is easy for you to program the Arduino boards. The code is written in the Arduino software, which is an open source software. You can download and use this software on your system or free. The codes written in the Arduino software are known as sketches. There are a number of libraries that you need to include in your programs when programming the Arduino board. These libraries are included by the use of the “#include” keyword used in the C programming language. You can write programs that can control the Arduino LED light. Note that you can power the Arduino board from your computer or directly into the power socket, and the effect will be the same in all of these cases. Data can be sent from the computer to the Arduino board, and from the Arduino board to the computer. The RX and TX LEDs usually light to show the direction in which the data is flowing. 

When programming the Arduino board, you can take advantage of the various features provided by the language including decision making statements, loops, functions, variables and others. The language also supports various data types that you can use when declaring variables. The math.h library comes with a number of functions that you can to perform various mathematical operations. An example of such a function is the sqrt() function that can help you calculate the square root of a number.

JavaScript for beginners

The simplified for absolute beginner’s guide to learn and understand computer programming coding with JavaScript step by step.

Basics concepts and practice examples inside.

[Matthew Python]

INTRODUCTION

This book is going to tackle a couple of hefty questions and also assume that you’ve got little to no practical programming experience. The reason for this is that, for a lot of people, JavaScript is their first language. Many people start out with something like web development or perhaps with a recommendation from a friend and find that JavaScript is one of the “easiest” languages to learn.

This is a bit of a misnomer of course; I’ve helped a lot of people learn to program. Some benefit more from a language that is more abstract and easier to understand, such as JavaScript. Others still benefit more from languages where everything is a concept and put right in front of them to toy with, because the verbosity helps them to understand what they’re working within a better sense, such as Java or C++.

Regardless of these, I’m going to assume, since you’re here, that you’re in the first camp, as well as explain things with enough rigor so that you’ll still understand the language well if you’re already in the second camp. JavaScript is not a difficult first language. Actually, it’s far from it. It’s easy to understand, abstract, and master. However, there is a definite degree of challenge that comes with, such as getting out of your comfort zone and learning all of the little concepts related to programming itself.

Therefore, let’s think for a second. What is JavaScript? JavaScript is a programming language. A programming language is basically something that allows you to talk to computers and instruct them on what to do. We know for a fact that computers don’t understand English. In fact, they don’t even understand programming languages. When you break it down, you’ll find that computers only really understand things in terms of binary codes - a sequence of ones and zeroes. This is where the name of the computer comes from a computer.

The computer makes millions of tiny computations that you can’t see every single second. All of these computations are performed using these ones and zeroes that are present at the very smallest level of the computer that you can’t see. Knowing this, we’ve figured out over the years that these ones and zeroes could be controlled and manipulated, first, through the development of languages that work with the processor of the computer itself (assembly) and, second, through the development of languages that serve as the connection between the complex zeroes and ones and the programmer.

As computers have gotten more popular and stronger these days, people who are interested in programming want to learn languages that aren’t absurdly difficult to use and understand. As a result, over time, programming languages too have become much simpler as more people started programming as a hobby. The increased processing power of computers over the years and the standardization of an object-oriented paradigm have led to the development of far simpler languages.

In order to understand JavaScript itself, we have to first learn it’s history. In the 1970s, there was a place called Bell Labs, a research lab owned and managed by AT&T. A lot of important technological advances originated from Bell Labs. One of the most important ones that you’ve probably heard before is the Unix system.

Unix was a landmark. It was an open-source and simple operating system that was intuitive enough that it could easily be marketed to businesses, developers, and universities all in tandem with one another without encroaching on each other’s markets. This was spurred by the development of the C programming language.

The C programming language itself has it’s long line of history, but essentially it was the first simple and intuitive language that almost anybody can figure out. It offers a layer of abstraction from the system itself and also offers the programmer the ability to scrutinize the system buildup and therefore understand the computer much better. This allows the programmer to directly manage things, such as memory allocation, or the amount of memory being used by the program in order to perform certain processes. In short, C allows programmers to better understand the system. However, they are expected to handle a great amount of difficult information and are prone to manipulate, for example, the computer’s processing capabilities.

Unix would eventually be rewritten in C instead of the standard Assembly code. This is part of the reason why C became so famous. This was a huge deal because it means that any processor that can run a C compiler, that is, the program which converts human-readable programming code to Assembly code that the computer can understand can run Unix as well. Now, this program can be compiled in any system that has a C compiler. This made the program extremely popular worldwide.

Moreover, since C is open source, universities often teach their students the language so that even if they cannot immediately compile Unix for their computers, they can at least modify the code so that they can run Unix on them. In addition, Unix is beneficial to C and vice versa because, first, C is being taught in universities to allow students to gain experience first before handling their Unix courses and, second, because Unix comes with a C compiler which makes it even easier for people to write and run codes on Unix systems.

This may seem like an irrelevant detail, but it’s a pretty important factor in the overall development of JavaScript and is a key part in the development of modern programming languages in general. This is because these languages can inspire a ton of different languages. For example, the extremely popular languages Java, Python, and C++ all have been – to one extent or another – inspired by C.

JavaScript is no exception. However, with that context, let’s think back what the computing landscape was like in the late 80s and early 90s. The general population was slowly being introduced with computers because of the popularity of both C and Unix. The combined popularity and accessibility of these mean that a lot of applications are being built for a lot of computers, approximately exponentially more every year.

However, the Internet was still in its infancy in many ways. Web browsers, for example, were unpopular and nowhere near their technological peak. Web browsers were, in many ways, much more simple and unsophisticated as were web pages themselves.

Currently, web pages primarily consist of just basic text markup rendered through HTML. This book isn’t going to tackle HTML except when it’s necessary. Therefore, a working knowledge about it is assumed. JavaScript is, after all, one of the three core web development languages alongside HTML and CSS. So, it’s worthwhile to learn HTML and CSS as well.

Anyhow, early web browsers were known as static web pages. Static web pages are the opposite of dynamic web pages, which are web pages that are designed to reflect and render text and images only. Basically, once a static web page is loaded, it cannot be changed from within the page without changing and the reloading the web file.

Dynamic web pages – or pages that can be changed in real-time without altering the web file itself – are implemented through what is called client-side scripting. Client-side scripting is about allowing changes to happen on a web page exclusively on the browser side. That is, client-side scripting allows sophisticated logic and dynamic changes to run within the context of the user’s web browser. Any changes are made their machine and within their browser and don’t necessarily indicate the transfer of information to a server.

Essentially, JavaScript and all related languages are about giving life to web pages. It’s about taking web pages and making them able to do things instead of just be still. This functionality was, for a long time, just a glimmer in the eye of people who were looking forward to web development. However, this doesn’t mean that scripting didn’t exist way before. There was early support for technologies designed to allow web pages to interact more. However, these were very rudimentary. The early graphical web browsers were capable of scripting even during its infancy.

This resulted in the creation of another browser, Mozilla which inspired the development of Firefox. Currently, however, Firefox was far from being a factor. Officially, the browser was released as Netscape, which was known by many as being among the most popular browsers in the 90s, and if you used a computer in the 90s, then you probably were using Netscape.

In the mid-90s, the idea of embedded codes in web pages – that is, codes written in other programming languages that can be inserted directly into and run from a web page – started becoming even more popular. However, there still wasn’t enough information regarding the process of practical embedded languages. Java did somewhat serve the purpose, but it wasn’t simple. In fact, it died out because it entails a great amount of raw computing power for it to be used. A better alternative was needed, something that can be directly embedded into and alter the web page. Such a thing didn’t exist.

Netscape decided to create a scripting language that can run within HTML documents and be easily embedded and interpreted within the browser itself. The language was supposed to display a similar syntax to Java and C++. This was to differentiate it from other popular scripting languages at that time, such as Perl, Python, and Lisp. Believe it or not, a C-inspired scripting language was relatively nouveau at the time.

The language was first released as LiveScript and then later was changed to JavaScript. JavaScript became the final name of the language from that on, most likely as an attempt by Netscape to capitalize the success of the Java programming language that was extremely popular at the time, even though JavaScript wasn’t particularly related to Java except in its syntactic in some places.

JavaScript was initially only implemented for client-side scripting or the creation of dynamic web pages (as we’ve already discussed). The first server-side implementation of JavaScript appeared a year or so after the initial release of JavaScript. Today, the server-side JavaScript is still being implemented even though its implementations are far less common than those of the client-side.

The mid-90s showed the development of many now-important web technologies and also browser wars. JavaScript plays an important part in the browser wars, which gained popularity pretty quickly and was implemented by Netscape in their browser. However, Netscape’s primary opponent during that time, Internet Explorer, didn’t have a support for JavaScript.

This started to change in late 1996\. It was clear that some kind of business-wide standard for JavaScript was needed in order for the World Wide Web to be accessed by all browsers. In order to do this, Netscape sent their language into a standards board in order for the language to be reviewed and standardized. The language standard was called ECMAScript, which was published in 1997\. This standardization became the starting point for many different languages and is a language in its own right. It’s the standard of a language, upon which other languages are derived from. All of these different derivations are referred to as implementations of the standard. JavaScript is the most popular one, but there were a few others that transpired, such as ActionScript designed for Flash coding.

With the standardization of ECMAScript, JavaScript was finally being used by other browsers and not just Netscape. JavaScript was an ambition in the mid-2000s. During this time, JavaScript and the things for which it could be used were becoming popular to the public (especially the developers) after the development of a white paper wherein Ajax was defined, basically promising the development of extremely dynamic web pages as opposed to the static pages prior. This resulted in the development of many more technologies that can be used alongside JavaScript, such as jQuery, which remained until 2015 or 2016\.

A little later in the Oughts, there was at last cohesive work done in order to push the status of the JavaScript language forward and force new standards fit for new technologies. Since then, newer implementations and constant unified updates have been created to develop a unified version of ECMAScript. Therefore, all implementations of ECMA, including JavaScript, resulted in the development of more technical possibilities.

For the last few years, new standards of ECMAScript have been released every year.

The major breakthrough of JavaScript must have been Ajax when developers began to take interest and supported the language. Today, there is an even greater need for an extensive browser support, and JavaScript began to push for that spotlight. Since then, it has become the most widely used web scripting language.

The history of JavaScript shows that it has undergone challenges to become what it is today. I hope that you appreciated the path that it has taken. In the following chapter, we’re going to discuss exactly where we are at today and all of the different things that JavaScript can be used for.

Chapter 1:What is Javascript?

What is JavaScript?

JavaScript, abbreviated JS, is a high-level programming language introduced to add specific programs to web pages, and it has been adopted by all major web browsers. JavaScript can be used to build interactive web applications to function appropriately without reloading every page per-action. JavaScript is used to create different forms of activities within web pages and is one of the essential components of the World Wide Web (www), which are HTML (Hypertext Markup Language) and CSS (Cascading Style Sheets). JavaScript and HTML are used to develop web pages. JavaScript brings a page to life by adding special effects such as sliders, pop-ups, form validations, etc. CSS determines the color intensity, image size, background colors, typeface, font size, etc.

why to learn JavaScript

JavaScript ranks as the top most used language of programming as is utilized by every browser version available today. It is therefore important to know what JavaScript does.

Below are a few details of what it does

JavaScript is designed in a way that its users are always able to be in charge of their browsers.

JavaScript is able to identify the specific browser being used by the user plus the Operating system as well. This enables it to function as per the functions being performed.

JavaScript is equipped with a calculator that enables users to work out some problems.

JavaScript is able to warn a user when an invalid input has been made immediately and be able to correct it as needed.

A JavaScript user can always be able to come up with new functions that are contained in scripts.

JavaScript also possess some limitations and they are as follows: For one JavaScript lacks multithreading capabilities which means it cannot be able to execute a number of multithreads at the same time

JavaScript is not designed in a way that it can be able to gain access to pages that are on other domains. There are some databases that JavaScript is not able to access without there being a server side script. However it is worth noting that there are some client side ones that a user can obtain.

A user of JavaScript is not permitted to write a file that is on the server side without use of an Ajax request which will in turn do this.

There is a limitation on how many devices a user is able to use with JavaScript. Different browsers interpret JavaScript differently which results in very different outputs.

Why is it called JavaScript?

When JavaScript was created, it originally had a different name: "LiveScript". But Java was very popular at the time, so it was decided that setting up a new language as Java's younger brother would be helpful.
But JavaScript, as it evolved, became a completely independent language with its own definition, called ECMAScript, and currently has no relation to Java.

What is HTML?

HTML basically allows you to present your site’s content in a structured manner. Think of it as a blueprint for building a house; it tells you where the living room, bathroom, kitchen, and other rooms will be placed and how they harmoniously interconnect.

Learning the structure of an HTML file is quite simple; it’s structured almost like an essay - you provide a title, a skeletal structure, and content that flows coherently within the structure. Whenever you read an article, the title tells you what the article talks about, and the content is structured in a particular way, oftentimes with a sentence that piques your interest, followed by anecdotes, facts and figures, arguments, and a conclusion. When you start coding in HTML, you’ll see how similarly structured it is to articles you read or write.

Creating an HTML file, then, is as simple as saving your file with a .html file extension. When you create documents in a word processor like Microsoft Word, you’ll notice that when you save your file it has either an .odt, .doc, .docx, or something similar at the end of the filename. This tells the computer to read and format the contents of the file in a very specific way. This is because whenever you save something you’ve created using a word processor you’re not just saving a bunch of words you’ve typed; you’re also saving the font size, font styles, and other formatting styles you’ve used so that when you open your file, your computer will check the file extension, read the contents according to the file extension specified, and then present you the file you’ve created, making sure that it looks exactly the same way when you’ve saved it. 

HTML basically acts the same way, but this time you use tags in order to tell the computer what to do with the data enclosed by the tags; this allows you to easily change the font styles and other aspects of your web page. Think of HTML as a more precise version of a Word Document. For example, take a look at the text below:

| This is a sentence. |

 If you save this as a Word Document, it will save not only the text, but also its font style, size, and structure. The attributes of the document you've just saved is tucked neatly inside the file and accessible only through the word processor menus. However, if you want to display the same sentence in HTML form, the HTML file would look like this:

| <html>    <head>    </head>    <body>        <p>This is a sentence.</p>    </body></html> |

By saving this file with a .html extension, you get a basic webpage that displays "This is a sentence." Notice how it has the same string of text as the previous text box, but it contains additional tags you may or may not be familiar with. When your browser opens this file, it understands the tags and displays only the content on the previous text box; it doesn’t actually show the tags to the user. The most basic tags are shown in the code example:

*   The <html> tag - contains everything in your web page. It’s the alpha and the omega, literally; never forget the <html> tag or else your site won’t work properly!
*   The <head> tag - keeps the title and other preliminary scripts that the body might use. For instance, if you want to use a set of design protocols (typically in the form of CSS) that dictate what type of fonts to use, their colors, etc., you can place the code or its reference here.
*   The <body> tag - this is where your content goes. From text, to sound, to images, to videos, this is where everything happens.

Don’t worry too much if you don’t yet fully understand how these tags work; you’ll learn better how they work by trying them out in future sample codes and exercises. 

How to include JavaScript in XHTML

Now that you have a general overview of how HTML works, we’re going to have a quick run through the basics, just enough to help you learn how to integrate JavaScript seamlessly into it. 

We’ve discussed how HTML files are like Word Documents with additional tags, so let’s start with a simple line of text. Type this into your text editor:

| Hi There! |

Now create a folder in your computer where you can store all the html files are created and save what you’ve just typed with a .html extension (e.g., "My First Website.html"). A standard practice for programmers is to create a folder called 'Developer' -- this is where all your files that pertain to programming are stored. You can place this in your home folder. Inside the Developer folder, create a folder called 'Web Development' and for now, place all your html files here. If you’re using TextEdit or other text editors that aren’t built specifically for html files, remember to check the settings and make sure that “Plain text” format is selected.

Now that you’ve created your first html file, open it using any web browser you have and see a simple string of text appear before your very eyes! Notice, however, that what you’ve typed into the text editor (referred to as “source code”) looks just like what the browser displayed; it didn’t have the <html> tags and other stuff. What gives?

Now, try changing your html file by adding a few tags. It should then look like this:

| <!DOCTYPE html><html>   <body>      Hi There!   </body></html> |

Now reload your browser and see what happens.

Your browser isn’t malfunctioning; the web page looks pretty much the same despite the addition of tags in the source code. At this point you may not fully understand why tags are used, but don’t worry; you’ll see what they're for when you start programming in HTML more.

JavaScript conveniently fits into HTML quite readily using the script tag. The script tag can either contain a JavaScript code or a reference to a .js file that contains the JavaScript code. The latter is advised when creating long JavaScript code to avoid mixing up different programming languages in one file - that’d be like writing an essay with some paragraphs in English and some paragraphs in Latin! Internal JavaScript is, however, good to use when  you’re testing out small fragments of JavaScript code. 

JavaScript and Browsers

Modern JavaScript is considered to be one of the safest programming languages because it doesn’t provide any access, low-level or otherwise, to the CPU or memory. The reason for this is that JavaScript was originally created for use in browsers and these do not require that kind of access level.

The environment that JavaScript is running in will dictate the capabilities. For example, Node.JS will support those functions that let JavaScript and read and write arbitrary files, carry out network requests, and so on. The in-browser JavaScript can do anything that is related to manipulation of web pages, user interaction, and the web server. For example, in-browser JavaScript can:

*   React to actions from a user
*   Change content on a page
*   Add new HTML
*   Modify the styles
*   Send network requests
*   Upload and download files
*   Get cookies and set cookies
*   As the user questions
*   Show the user messages
*   Remember browser data

It can’t do everything though. In-browser JavaScript is limited to protect the safety of the user, i.e. to stop a malicious web page from accessing their private and confidential date. Restrictions of the in-browser capabilities include:

*   Not being able to read or write arbitrary files to a hard drive
*   Not being able to copy the files or execute programs
*   Not having any access directly to the functions of the operating system
*   Although it can work with a file in a modern browser, it only has limited access and that is only if a user does specific things, like selecting a file through an <input> tag or dropping files into the browser window.
*   Limited in access to the cameras and/or microphone on a device and that access is only allowed if the user gives express permission. This means that any page run on JavaScript may not enable your webcam or microphone

The different windows and tabs you use are not aware of one another unless JavaScript is used to open a window or tab from another one. Even so, JavaScript that is in one window or a tab cannot access the JavaScript on another if they are from different ports, protocols or domains

This is known as “Same Origin Policy” and the only way around it is for both of the JavaScript pages to have a special code that can handle the exchange of data. Again, this is for the safety of the user, stopping one page from accessing personal details on another.

JavaScript is more than able to communicate with the current page server over the network but it cannot receive data from any other domain or site. It is possible but it must have express permission, through the HTTP headers on the web page and that must be granted from the remote side. Again, user safety is paramount.

However, if JavaScript is out of the browser, such as on a server, there are no limits. Modern browsers also let you install extensions and plugins which can have extended permissions. These should be considered carefully before being installed though as some can cause problems for the safety of the user.

Basic Glossary

Script: each of the programs, applications or pieces of code created with the JavaScript programming language. A few lines of code form a script and a file of thousands of lines of JavaScript is also considered a script. Sometimes it is translated into Spanish directly as "escribir", although script is a more appropriate and commonly accepted word. Sentence: each of the instructions that form a script.

Chapter 2:Why JavaScript?

It is the programming language of web browsers (all the most important ones support it and have it activated by default: Firefox, Chrome, IE, Opera, Safari ...), which make it the most popular language on the Internet. There are other options, but they require installation and activation through plugins or only work in specific browsers.

There is a real competition between browsers to optimize their engines and provide better support for JavaScript and for your code to run faster. JavaScript is therefore increasingly stable and has better performance.

It is fully integrated with HTML and CSS. Each plays a definite role in a web page: HTML is the markup language to create the structure, CSS the language of styles to configure the presentation and JavaScript provides interactive and dynamic behavior.

It will play an important role, enhancing its performance, with the arrival of HTML5 / CSS3

It is very powerful and expressive, with syntax that keeps similarities with other very popular languages, but with particular characteristics. Is easy to learn. They have a fast learning curve and require little time investment to start using it. It is very easy to work with him. You do not need a web server or a special development environment. It is interpreted so we don't have to compile code. We do not need to acquire licenses. A text editor (or a code editor that facilitates the task) and a browser is all you need. To that, we can add an add-on such as Firebug to debug and we are fully equipped with free and free tools.

It is the basis for using AJAX on our pages, a programming technique that well used allows us to build 'new generation' websites greatly improving the user experience (we will see it in a next post). Once we know the basics of JavaScript, we have open and free frameworks available (work environments / libraries) such as JQuery, Prototype, Dojo,…. which make our work even easier and allow us to develop very advanced elements with extraordinary simplicity.

It allows us to work in an open and standardized environment without being tied to the criteria of any software manufacturer. In addition, it can interact with other popular technologies such as Flash or Java.

It is true that some of these reasons have also been used to criticize JavaScript, as it is so simple that it is used without knowing it. The label of 'language for amateurs' for its use to overload visual effects web pages, has changed radically. Opinions like those of Douglas Crockford helped to understand it better and generate a great interest in knowing and applying its possibilities also among advanced programmers.

For those who start and have an interest in programming (web) is a language that makes it easy for them to take the first steps. In fact, the low complexity to work with him has encouraged its use as a reference language to teach programming concepts. Like any tool, it has its flaws and can be misused, but knowing where its limitations are is one of the first learning options that anyone who wants to start in web programming should consider.

Python Vs Javascript: Which One Is Better For Web

Development? It is difficult to find a person, company or brand that currently lacks a website. Many of these sites are programmed “to measure”, and in most cases they fulfill functions superior to the demonstrative and informative ones, with which the –even less static– corporate sites were born.

Then it is there where questions appear that although they are simple to answer, they can be somewhat disturbing at some time for those of us who are in one way or another involved in the IT sector. How to develop a different website? What is better? What language should I use for the web development of a site to make it look more professional? Will Python suit me better or do I focus on learning JavaScript?

It is good to start any comparison (and particularly this one) indicating that both are languages of different syntaxes, but the paradigms are the same and the pre conclusion is that similar results are obtained.

But although these similarities can be discussed, in terms of code and when it comes to web development they are totally different. For this reason, here we will know a little about each one of them, what are their advantages and which one you should choose.

What is Python?

Python is a minimalist programming language, which contains a syntax that makes it quite simple. It is an interpreted language, that is to say, not compiled, in addition this serves for all types of development especially to give dynamics to objects in different programs and / or paradigms.

Undoubtedly Python is one of the best options to develop a website, especially when you know the basic elements of language. Let's see Python what offers us.

Python Features

Before continuing, we will point out some important Python features and why you should learn it.

Minimalist Dode

Yes, the code and the simple syntax are perfect for developing websites, facilitating the work and writing of it. Well Paid That's right, if you are going to develop a Python website, prepare your bank account, since the benefit you will receive from developing a Python website will be very profitable, as you can see in Medium. Multiplatform

Python can not only run it in an operating system, so you can take it anywhere, from free operating systems such as Linux and through the already known Windows or Mac, in addition to other devices that have systems based on the aforementioned distributions.

Extensive Libraries

An advantage that comes very well from Python is the amount of libraries or libraries you can find to develop. There is a wide variety of reusable code, from game creation to large websites and quality.

What Is Javascript?

Javascript is a very simple language, which can hardly be interpreted with a browser. This means that it does not need to be compiled for execution. Javascript is highly recommended for the realization ofpages websince it allows the development of the user in it. How? Javascript It allows the website to be as static as possible, and comes hand in hand with other compulsory learning languages, such as HTML and CSS. What gives interactivity to the web with animations, which allows the user to feel more at ease, since he will not observe a flat website, all this is included in JavaScript. Normally with JavaScript, programs or applications are created and then inserted into the website to be used. Likewise, they are used to develop mobile applications and complex programs, from the Backend and Front End point of view.

characteristics of JavaScript

Many new programmers often get a little bit disappointed when they hear people call JavaScript a language for kids. Well, let me clear this up for you. First, JavaScript is hands down, one of the strongest programming languages out there. It’s a popular skill required for web development.

The beauty of JavaScript lies in its simple yet complex presentation. It has been used for many years now by numerous developers. It can add a fresh spin on their web pages, ranging from very subtle but important features such as automatic image changers, to more intricate designs that enhance their beauty. 

The following are just a few of the features that help JavaScript to stand out on its own in the crowd.

Integrated Browser Support

Right off the bat, the user friendly nature of JavaScript is very intriguing and it attracts many new programmers and experts. Many web development languages out there require installing a supplementary flash plugin in order to be allowed to access flash content and work on the browser. The users of JavaScript are mostly spared from this hassle as almost all the browsers have invariably accepted JavaScript as their core scripting language. This allows them to deliver integrated support for the language. In the most critical cases, the users will only need to handle some particular tasks that rely on DOM with care, but other than that, JavaScript is fully accessible and free to be used.

A Functional and Flexible Programming Language

For programmers who prefer a lot of functions in their programs, JavaScript isa joy. This is because of the versatile manipulation techniques incorporated within the language that allows the programmers to determine the execution of a function. Two of the more prominent features of Java that put it at the frontend offunctional programming is that it gives programmers the freedom to assign a function to any variable, and make a function accept another function using the arguments parameters. Such in-depth ability for customization makes it so much more fun for ![Description: 00007.gif](images/00017.gif)programmers who like to have more freedom in programming. 

The ability to use JavaScript on both Client and Server Side  Since JavaScript has been officially recognized by the web-browsers as being the prime development language for them, JavaScript has been given the administrative privileges to have access to the document model objects of any browser. What this does is that it gives the programmer another level of freedom. It allows programmers to change the structure of the web pages on the fly. Not only that, the language can also be used to add various interesting effects to the web pages. And if you are working with Alfresco, then you are in luck! Because JavaScript also allows web scripts to be created in Alfresco. This allows programmers to add custom tasks to any Alfresco server very easily. 

When you combine all of these together, JavaScript is truly a magnificent programming language that is powerful yet easy to use.

Self-Conscious ability to detect browser and OS

![Description: 00008.gif](images/00018.gif)

Sometimes when you are programming, you might face some issues and need to write code that is dependent on the operating system and web browser that you are using.

JavaScript has been intelligently designed to allow itself to be self-aware of the browser and OS which you are using. This allows you to easily adjust the language in accordance with your requirements to perform all the OS dependent actions with ease.

The Diverse Support for Object Oriented Programming

Object oriented programming is perhaps the keystone of programming languages these days. Programmers often like to choose their language depending on the accessibility to the handling mechanism of these objects. When brought in to comparison, JavaScript has a very different and unique structural system that determines how to handle the objects. It offers a huge amount of support, while at the same time it remains relatively easy to learn and use. This encourages the users to write more complex object oriented code smoothly and efficiently with very little complication.

This is one of the many reasons why JavaScript always remains on the top of the list for programmers and also in the industry.

If you are interested in object oriented programming, then you can’t go wrong with JavaScript.

Advantages of JavaScript

With JavaScript, users can organize input before getting the page sent to the server, which automatically reduces loads on the server. JavaScript enables swift response to page visitors. Whenever you read an article, the title tells you what the article talks about, and the content is structured in a particular way, oftentimes with a sentence that piques your interest, followed by anecdotes, facts and figures, arguments, and a conclusion. When you start coding in HTML, you’ll see how similarly structured it is to articles you read or write.

The page does not have to reload before visitors can see if there was an error in typing.

JavaScript is used to build a reactive interface that gives a reaction when the mouse hovers over them.

Limitations of JavaScript

JavaScript programming language lacks the following essential features. They are:

· For security reasons, client-side JavaScript does not read or write files

· JavaScript for networking applications

· JavaScript does not contain multiprocessor capabilities

JavaScript Development Tools

You do not need an expensive development tool to write JavaScript codes. You can write with a simple text editor such as Microsoft FrontPage, Macromedia Dreamweaver MX, Macromedia HomeSite 5, etc.

The two Types of JavaScript Execution

The first types of programming languages are called ‘Compiled’ languages. The popular languages in this category are: C++, Java, C Fortran and COBOL. 

A compiled programming language has to be coded (written) by the person doing the programming, and then this code has to be run through a particular program called a compiler. This ‘complier’ program then ‘translates’ the code into machine language, which the computer can understand, and then perform the given orders.

The second type of programming languages are called Interpreted languages. For example: JavaScript, PHP, Ruby, Haskell and Perl. With the Interpreted language, the code is still written in human form, but it is not necessary for the code to be run through compilers. Instead, the compiling (translation) process takes place in the actual browser, the moment the program is being run.

The benefits of these are that the process is shorter. Also, the programmer has the ability to update and make changes to the program at any time. On the contrary, because the program is being compiled and being run simultaneously, it can slow down the overall performance of the programs.

However, upgraded computer processers that operate faster, combined with JIT (Just-In-Time) compilers, have given a huge boost to the performance. 

Parameters And Ideal Test Environment

It is necessary to keep in mind that to start working with JavaScript, you need a minimum of HTML knowledge, especially the notion of tags that allow you to place yourself on the page. To refresh the memory, we will simply remember that an HTML page is divided into two main parts: The head where the data corresponding to the description of the content are located; The body where the code that makes possible the construction of objects on the page (form fields, text areas, images, etc.) appears. A JavaScript script can be located, as desired, in one or the other of these two parts. However, in principle, scripts are generally found in the head part of the page. Its execution can be immediate (when the page is loaded) or deferred (click on a button, for example). In this case, it will be necessary to use event-based programming and functions for the code to execute. These points are discussed in the Functions and Events chapter of this book. However, placing the scripts in the head part does not mean that they will be indexed by the search engines. In fact, until now, search engines such as Yahoo or Google do not propose any content from these elements of the code, but with the development of Web 2.0 they will do so sooner or later. At the moment, in the case...

Syntax

The syntax of a programming language is defined as the set of rules that must be followed when writing the source code of the programs to be considered correct for that programming language. The basic rules that define JavaScript syntax are as follows:

▪ Blank spaces and new lines are not taken into account: as is the case with XHTML, the JavaScript interpreter ignores any remaining blank space, so the code can be properly sorted to better understand it (tabulating the lines, adding spaces, creating new lines, etc.)

▪ The case is case sensitive: as is the case with the syntax of the XHTML tags and elements. However, if an XHTML page is used interchangeably, the page is displayed correctly, the only problem being the non-validation of the page. On the other hand, if JavaScript is exchanging upper and lower case letters, the script does not work.

▪ The type of the variables is not defined: when creating a variable, it is not necessary to indicate the type of data that will be stored. In this way, the same variable can store different types of data during script execution.

▪ It is not necessary to end each sentence with the semicolon character (;): in most programming languages, it is mandatory to finish each sentence with the character; Although JavaScript does not require you to do so, it is convenient to follow the tradition of ending each sentence with the semicolon character (;).

▪ Comments can be included: comments are used to add information in the source code of the program. Although the content of the comments is not displayed on the screen, it is necessary to take precautions on the information included in the comments. JavaScript defines two types of comments: those of a single line and those that occupy several lines.

Example of a single line comment:

// below is an alert message (" test message"); Single line comments are defined by adding two slashes (//) at the beginning of the line. Example of multi-line comment:

/ * Multi-line comments are very useful when you need to include enough information in comments * / alert (" test message"); Multiline comments are defined by enclosing the text of the comment between the symbols / * and * /.

Creating The Test Page

To write effectively in the HTML pages, it is best to create a model page where you must include the labels that indicate the beginning and end of the script .

Being the head part of the page where the JavaScript code is usually inserted, look at this example of the HTML code of the model page that will be used for writing all your scripts.

The first two lines determine the type of document, its presence is essential for the proper functioning of DHTML instructions, as we will see in the chapter Improve interactivity with JavaScript and CSS. The fourth line indicates the beginning of the head tag that interests us in a particular way. The fifth line allows you to add a meta tag that indicates the characters used, the sixth gives a title to the page.

The Code Syntax Rules

In view of the fact that JavaScript is a non-flexible language that does not authorize errors, as we can see in the following lines, respecting these rules is essential to start on JavaScript.

1.  Upper and lower case

One of the main difficulties of JavaScript is to be a programming language that distinguishes the use of upper and lower case. It is a rule that becomes very important when working with variables and objects.

Specifically, in JavaScript Myobject is not the same as myobject. This applies to all keywords (properties, methods, JavaScript functions) and the use of design tools such as Aptana or the Dreamweaver editor facilitates the identification of this syntax since they are almost instantly identified with colors. Another syntactic rule refers to the insertion of comments. Whenever you read an article, the title tells you what the article talks about, and the content is structured in a particular way, oftentimes with a sentence that piques your interest, followed by anecdotes, facts and figures, arguments, and a conclusion. When you start coding in HTML, you’ll see how similarly structured it is to articles you read or write.

2.  Inserting comments

As in most programming languages, inserting comments into your scripts can be extremely useful. In fact, apart from being able to more easily find the instruction blocks that you have created, the comments can be of immense help the day you have to retake the code. The readability of the code is even one of the main criteria determining the quality of a JavaScript code. Because, after all, how about...

Creating A Personal Library Of Javascript

Scripts Over time, you will have to develop numerous scripts that can be reused later. To facilitate this reuse, identify your pages with names that clearly indicate the purpose of your JavaScript script.

Beware of confusing personal library scripts and common libraries, abundant in the network, and that enrich the classic JavaScript operation. The installation of new JavaScript libraries will be discussed in the chapter Improving interactivity with JavaScript and CSS.

JavaScript examples

< script > tags are usually used to contain our JavaScript statements. The script tag can be placed anywhere on your webpage as required. It is important to remember to always maintain it inside the < head > so as to achieve the right outcome. An example that can be used to first illustrate this is one that can help print out “Hello World”. So as to ensure our code remains even when using a browser that isn’t able to use JavaScript, it is important to feed a JavaScript code inside of an HTML code. Observe the code below

<html>

<body>

<Script language= “JavaScript” type= “text /java script”>

<!—

Document. Write (“Hello World!”)

//-->

</body>

</html>

The result that will be achieved from the above code is: Hello World! Here ‘//’ is symbolic of a phrase that is found in JavaScript that is added to block any browser from translating the last HTML phrase like a JavaScript code portion.

Chapter 3: Basic Programming structure

VariableS

The variable is the "named storage" of the data. We can use variables to store specialties, visitors, and other information.
Use the keyword to create a variable in the JavaScript application.
The sentence below creates (in other words: declares) a variable called "message":

![Description: 00027.jpeg](images/00019.jpeg)Now we can put information there using the task operator =:
![Description: 00028.jpeg](images/00020.jpeg)The string is now stored in the memory associated with the variable. We can use it as a variable name:
![Description: 00029.jpeg](images/00021.jpeg)In summary, we can combine a statement and the address of a variable on one line:
![Description: 00030.jpeg](images/00022.jpeg)We can also declare several variables on a single line:
![Description: 00031.jpeg](images/00023.jpeg)It may sound shorter, but we don't recommend it. Use one line of the variable for better readability.
The multi-line variant is a little longer but easier to read:
![Description: 00032.jpeg](images/00024.jpeg)Some people also define several variables in this multi-line style:
![Description: 00033.jpeg](images/00025.jpeg)... Or even a "comma first" style:
![Description: 00034.jpeg](images/00026.jpeg)Technically, all of these variants do the same thing. It is, therefore, a question of personal taste and aesthetics.
var instead of LET

![Description: 00035.jpeg](images/00027.jpeg) 

The var keyword is almost identical to enter. He also declares a variable, but in a slightly different way, in the "old school" way.

Global and Local Variables

Variables not being accessible anywhere else in your code except within the functions they were created in. These are called local variables. Global variables are the ones declared outside functions and can be accessible anywhere within your code. For example:

| var x = 10; // this is a global variable because it isn’t declared inside the functionvar turnToZero = function(number) {    number = 0;    console.log("The value of x is now: " + x);}; turnToZero(x);console.log("Outside the function the value of x is: " + x); |

Notice how the variable 'x' can still be accessed inside the turnToZero() function. Here’s where a lot of beginners get confused: when you pass a variable to a function, just like what we did when we invoked:

| turnToZero(x); |

You’re just copying the value of x into the function, and placing it into the temporary variable named 'number'. This means that when you do stuff to the variable 'number', you’re not really doing anything to x. This is why the turnToZero function is useless; when you pass a variable into it, only the value of the temporary variable is changed, not the actual variable.

That being said, you don’t have to pass a global variable to a function in order to modify its value. We can simply do the following:

| var x = 10; // this is a global variable because it isn’t declared inside the functionvar turnToZero = function() {    x = 0;    console.log("The value of x is now: " + x);}; console.log("Before calling the function, the value of x is: " + x);turnToZero();console.log("After calling the function, the value of x is now: " + x); |

In a nutshell, the var keyword, apart from telling the computer that you’re declaring a variable, also tells the interpreter to create a new variable in the current scope, which is why if it’s created inside a function, it’ll only exist inside a function, and if it’s created outside a function, it’ll exist throughout the whole code. With this in mind, you might be wondering why one would even need local variables if global variables are much easier to use. The reason for this is that global variables can make it harder to read and debug programs. You’ll notice this when you start creating more complex JavaScript codes, but for now, it’s best not to try modifying global variables inside a function unless you know exactly why you’re doing it.

Types of variables

Be aware that a variable is able to hold values that are of number type and text type. A text value is called a text string and while JavaScript is capable of handling several different data types, for now, we will concentrate on the numbers and the strings.

A text string is enclosed in single or double quotes while a number has no quotes. If you were to enclose a number inside a set of quote marks, it would be seen as a string. For example:

var pi = 3.14;
var person = "Jane Deer";
var answer = 'Yes I can!';

One Statement, Several Variables

You are not limited to one variable per statement; you can use several. Just make sure you begin the statement with the var keyword and then ensure that each variable name is separated by a comma:

var person = "Jane Deer", carName = "Ford", price = 300;

Each declaration can go over more than one line:

var person = "Jane Deer",
carName = "Ford",
price = 300;

Undefined Value

In a computer program, it wouldn’t be unusual to find a declared variable that has no value. In these cases, the value may be the result of a calculation that has to be done or perhaps something that may be input later, such as something from a user. These variables, although they have no specific value, actually have a value of undefined. After the next statement is executed, the variable called carName will have a value of undefined:

var carName;

Re-Declaring a Variable

Variables that are re-declared do not lose their initial value. For example, if we re-declared carName, it would retain its vale of “Ford” after the statements are executed:

var carName = "Ford";
var carName;

Arithmetic

With a JavaScript variable, you can use certain operators that allow you to do arithmetic, such as, + and =. For example:

var x = 3 + 4 + 5;
You are also able to add strings together but these will be concatenated, i.e. joined together. For example:

var x = "Jane" + " " + "Deer";

You could also do this:

var x = "3" + 4 + 5;
If you place a number inside quote marks, the remaining numbers will be seen as strings and they will be concatenated or joined together. Have a go at this:

var x = 1 + 4 + "5";
Data Types

A variable is able to hold several data types, such as strings, numbers, objects, etc.

var length = 15;                               // Number
var lastName = "Parker";                      // String
var x = {firstName:"Jane", lastName:"Deer"};    // Object

Data types are a very important concept for you to remember in computer programming. If you are going to perform an operation on a variable, you must have some knowledge about the type. Take the following example; without a type, the computer could not solve this safely:

var x = 15 + "Ford";

Does this make any sense? Adding Ford to 15? Would it come up with a result or an error? JavaScript will see this example as”

var x = "15" + "Ford";

When you add a string and a number, JavaScript will see the number as a string. Try this example yourself:

var x = 15 + "Ford";

And this one:

var x = "Ford" + 15;

The first example shows JavaScript seeing the numbers 15 and 6 as numbers until it gets to “Ford”. The second example shows everything being treated as a string because the first one is a string.

Dynamic Types

Dynamic types are a big part of JavaScript. What this means is that one variable can hold several different data types. For example:

var x;               // x is undefined
var x = 6;           // x is a Number
var x = "Jane";      // x is a String

Strings

Strings are series of characters, such as “Jane Deer”. All strings are enclosed in double or single quotes – please note, you cannot mix these and use, for example, a single quote to open a string and a double quote to close it.

var carName = "Ford XS80”;  // with double quotes
var carName = 'Ford XS80;   // with single quotes

You should also remember that quotes can be used in a string provided they are not the same as those around the string:

var answer = "It's ok";             // A single quote used within double quotes
var answer = "He is called 'Billy'";    // Single quotes used within double quotes
var answer = 'He is called "Billy"';    // Double quotes used within single quotes

We will talk more about strings later in the book.

The next few points are just an overview of what we will cover more of later in the book but, for now, they are included here because they are related to data types.

Numbers

JavaScript contains just one number type and the numbers may or may not have decimal places, for example:

var x1 = 56.00;     // with a decimal place
var x2 = 56;       // without a decimal place

To write very large or very small numbers, you must use an exponential or scientific notation:

var y = 234e5;      // 23400000
var z = 234e-5;     // 0.00234

JavaScript Booleans

Booleans have just two values – True or False

var x = true;
var y = false;

Arrays

In JavaScript, an array is enclosed in square brackets and each item is separated by a comma. Look at the next example which is declaring an array with the name of cars and with three items in it, the names of the cars:

var cars = ["Volvo", "Ford", "Mercedes"];

The indexes in an array are what we call zero-based and this means that the first item will start at 0, the second one is 1 and so on. So, for 10 items in one array, you will go from 0 to 9\.

Objects

Objects are contained within curly braces and the properties of the objects are written as pairs of name: value, each pair separated by a comma:

var person = {firstName:"Jane", lastName:"Deer", age:45, eyeColor:"green"};
The object in the example is a person with four properties:

*   firstName
*   lastName
*   age
*   eyeColor

typeof Operator

The typeof operator is used to find a variable type. Look at these examples:

typeof ""                  // Returns "string"
typeof "Jane"              // Returns "string"
typeof "Jane Deer"          // Returns "string"

Example

typeof 1                                 // Returns "number"
typeof 253                               // Returns "number"
typeof 2.53 // Returns "number"
typeof (1)                          // Returns "number"
typeof (5 + 8)             // Returns "number"

Primitive Data

Primitive data values are simple single values that have no extra properties or methods. The following primitive types can be returned by the typeof operator:

*   boolean
*   null
*   number
*   string
*   undefined

For example:

typeof "Jane"              // Returns "string" 
typeof 2.53                // Returns "number"
typeof true                // Returns "boolean"
typeof false               // Returns "boolean"

Complex Data

It can also return one of the following complex data types:

*   function
*   object

For example:

typeof [3, 4, 5, 6]             // Returns "object” and not an array – see below
typeof {name:jane, age:45} // Returns "object"
typeof function myFunc(){}   // Returns "function"

The typeof operator will return “object” because arrays are objects in JavaScript.

Undefined

As we said earlier, a variable that has no value is given the value of undefined. The typeof operator is undefined too:

You can empty a variable of its assigned value by setting it to undefined value; the type is also undefined:

person = undefined;        // the value is undefined, the type is undefined

Empty Values

Empty values are not to be confused with undefined values. Empty string variables have both value and type, for example:

var car = "";              // The value is "", the typeof is "string"

Null

Objects can be emptied by setting them to null, like this:

var person = null;         // the value is null, but the type remains an object
You can also empty objects by setting them to undefined:

var person = undefined;   // the value is undefined, the type is undefined

operators

The basic operators in JavaScript are created with signs and symbols. We have already familiarized ourselves with a few operators, such as the equal sign operator which is used to assign value to a variable.

Ex-

var a = 8;

var b = 9;

The meaning of the above two lines is that the variables a and b are being declared and a value is assigned to them. In this case, the value of a is 8 and the value of b is 9\.

Similarly, JavaScript has a number of other basic mathematical operators built inside its core script. Let’s look at the following four operators:

- The addition operator ( + )

- The multiplication operator ( * )

- The division operator ( / )

- The Subtraction Operator ( - )

Each of these operators works the same as how they would work in a calculator.

Ex-

var a = 10; 

var b = 5 ;

a/b

This is a simple division, which divides 10 by 5 giving 2\.

a + b

This operation performs an addition, 10 + 5 gives 15\.

a – b

This operation does a subtraction, 10-5 gives 5. 

a *b

This is a basic multiplication, 10 * 5 = 50.

Aside from the basic operators, here are some more:

Different types of assignment operators (Usage: Assigning values to variables)

![Description: 00004.gif](images/00028.jpeg)

The examples in the chart are all numbers, but operators are not only for numbers.

Concatenation allows you to combine two individual strings together and turn them into one string using + operator or += assignment operator.

Ex-

var Spray = “Hello” ;

var Body = “World” ;

console.log(Spray + “ “ + Body); 

This will give an output of “Hello World”

Ex2-

var a=”I am ”

var b +=”Legend”

The result will be: I am Legend

Also, you can add a string and a number together:

X=”3”+1      (Result will be 31, not 4)

X=”Jessica”+1   (Result will be Jessica1)

The result will be a String.

Unlike other programming languages, the behavior of the operators that deal with Strings and those that deal with numbers vary to a great extent. Having a deep understanding of the core differences between the two is important in order to make sure that both of them are used properly.

For example, one of the prime differences you will notice while using these two types of operators can be found during the usage of the Addition Operator.

See the following example:

Consider a scenario where we are trying to add a number and a string.

Example 1.

var Bar = 5;

var Legal = “6”

console.log (Bar + Legal)

The output here will be 56. 

If you want to force the strings to act as simple numbers, you can add a Number keyword in front of the string variable.

Example 2.

X=1+Number(“6”)

The result will be 7 in this case.

Example 3.

var Bar = 5;

var Legal = “6”;

console.log (Bar + Number(Legal))

The output of this statement is 11.

These are examples of how JavaScript allows you to do type conversion manually from numbers to Strings, Strings to numbers, or Boolean values to numbers or Strings.

We’ve already shown you how to convert Strings to numbers using the global Number() method. A similar method exists to convert numbers to Strings. This uses the global String() method. See the following Examples.

Example 4.

String (3.14) will convert the number 3.14 to a String. 

String(x + y) converts the expression of x + y into a String.

You may wonder why you would ever want to convert a number to a String. There are times when you will want to preserve the accuracy of a number out to a certain number of decimals. Because of how computers deal with numbers by converting them to binary and back, you can lose accuracy when working with just the number type. In this case, preserving the value as a string ensures that you won’t lose any accuracy in your values.

You can also convert Boolean values into numbers or Strings. 

Number(TRUE) will return a value of 1

Number(FALSE) will return a value of 0

String(TRUE) returns a String, “true”

String(FALSE) returns a String, “false”

In the example 1 + 2 equals to 3, the numbers 1 and 2 are called operands and the ‘+’ sign is the operator.

JavaScript supports the following types of operators:

Arithmetic Operators

Logical Operators

Assignment Operators

Conditional Operators

Let’s discuss each type of operator.

Arithmetic Operators

| Operator | Description | ExampleA=5, B=10 |
| + | Addition (works for numeric and strings) | X = A + B: X=15Y = “z” + B: Y = z10 |
| - | Subtraction | X = A – B: X = -5 |
| * | Multiplication | X = A * B: X = 50 |
| / | Division | X = B/A: X =2 |
| % | Modulus (outputs the remainder of an integer division) | X = B % A: X = 0 |
| ++ | Increment by 1 | X=A++: X = 6 |
| -- | Decrement by 1 | X=A--: X = 4 |

Exercise: Here’s a sample code using arithmetic operators:

<!DOCTYPE html>

<html>

<body>

<script type="text/javascript">

<!--

var x = 15;

var y = 12;

var z = "Strings";

var enter = "<br />":

document.write("x + y = ");

answer = x + y:

document.write(answer);

document.write(enter);

document.write("x - y = ");

answer = x - y:

document.write(answer);

document.write(enter);

document.write("x * y = ");

answer = x * y:

document.write(answer);

document.write(enter);

document.write("x / y = ");

answer = x / y:

document.write(answer);

document.write(enter);

document.write("x % y = ");

answer = x % y:

document.write(answer);

document.write(enter);

document.write("x + y + z = ");

answer = x + y + z:

document.write(answer);

document.write(enter);

document.write("x++ = ");

answer = x++:

document.write(answer);

document.write(enter);

document.write("y-- = ");

answer = x--:

document.write(answer);

document.write(enter);

</script>

<p> Practice using other variables </p>

</body>

</html>

Here’s the output:

x + y = 27
x - y = 3
x * y = 180
x / y = 1.25
x % y = 3
x + y + z = 27Strings
x++ = 15
y-- = 16

Practice using other variables

Experiment with the values and change the variables.

Let’s now move on to the next type of operators.

Logical Operators

Logical operators validate the truthfulness or falseness of the expression. The result of the expression evaluation will depend if one of them is true, both are true, or if a logical negation should be performed.

| Operator | Description | ExampleX=true, Y=false |
| && | Logical AND | X && Y // false |
| &#124;&#124; | Logical OR | X &#124;&#124; Y // true |
| ! | NOT | !( X && Y) // true |

Exercise: Using our simple code, let’s see how these operators work:

<!DOCTYPE html>

<html>

<body>

<script type="text/javascript">

<!--

var x = true;

var y = false;

var enter = "<br />";

document.write("(x && y) => ");

answer = (x && y);

document.write(answer);

document.write(enter);

document.write("(x || y) => ");

answer = (x || y);

document.write(answer);

document.write(enter);

document.write("!(x && y) => ");

answer = !(x && y);

document.write(answer);

document.write(enter);

document.write("!(x || y) => ");

answer = !(x || y);

document.write(answer);

document.write(enter);

</script>

<p> Practice using other variables </p>

</body>

</html>

Here’s the output of the logical statements:

(x && y) => false
(x || y) => true
!(x && y) => true
!(x || y) => false

Practice using other variables

Bitwise Operators

These are not commonly used in JavaScript. Not nearly as much as we use the other types of operators. We will discuss these operators in order, to have a complete understanding of what JavaScript can do.

When bitwise operators are used, the operands are transformed into their 32-bit binary representation, perform the operation, and convert the results back to decimal. 

Let’s take the value 12 for example. 

This is 12 represented in binary:

00000000000000000000000000001100

Starting from the rightmost bit, each bit represents a value from 20-231.  To represent 12, the 3rd and 4th bit are set to 1. This signifies a value of 23+22 = 12\.

The example above expresses a positive integer. To express a negative number in binary, we make use of the two’s complement rule.

Let’s convert -12 to binary.

The first step is to flip all the values. 

00000000000000000000000000001100

11111111111111111111111111110011  // Flip all values 0 to 1 and vice-versa

Next, add 1 to the result. 

11111111111111111111111111110100  // Add one to the rightmost bit

The above is the binary equivalent of -12.

Now let’s have a look at what JavaScript can do with binary.

| Operator | Description | ExampleA=3 Binary: 0011B=2 Binary: 0010 |
| & | Bitwise AND (Do Boolean AND on each bit) | C = A & B; C=2 |
| &#124; | Bitwise OR (Do Boolean OR on each bit) | C = A &#124; B; C=3 |
| ~ | Bitwise NOT (Reverses all the bits in the operand) | ~A is equal to -4 |
| >> | Right shift (In the first operand, all the bits are moved to the right by the number of places stated in the second operand.) | B >> 1 is equal to 1 |
| >>> | Right shift with zero (Bit are shifted to the right, removing the bits that shifted off, and zeros are added from the left)  | B >>> 1 is equal to 1 |

Exercise: Use the code below to demonstrate how to use bitwise operators. Manually solve the statements and check if you got the correct answer.

<!DOCTYPE html>

<html>

<body>

<script type="text/javascript">

<!--

var x = 2; // Bit 0010  

var y = 3; // Bit 0011

var enter = "<br />";

document.write("(x & y) => ");

answer = (x & y);

document.write(answer);

document.write(enter);

document.write("(x | y) => ");

answer = (x | y);

document.write(answer);

document.write(enter);

document.write("(x ^ y) => ");

answer = (x ^ y);

document.write(answer);

document.write(enter);

document.write("(~y) => ");

answer = (~y);

document.write(answer);

document.write(enter);

document.write("(x << y) => ");

answer = (x << y);

document.write(answer);

document.write(enter);

document.write("(x >> y) => ");

answer = (x >> y);

document.write(answer);

document.write(enter);

document.write("(x >>> y) => ");

answer = (x >> y);

document.write(answer);

document.write(enter);

</script>

<p> Practice using other variables! </p>

</body>

</html>

Did you get it right? Here’s the output:

(x & y) => 2
(x | y) => 3
(x ^ y) => 1
(~y) => -4
(x << y) => 16
(x >> y) => 0
(x >>> y) => 0

Practice using other variables!

Assignment Operators

Notice the parameter result in all of the sample codes above. The use of this parameter is an example of an assignment operator. Assignment operator assigns the value of the operand on the right to the operand on the left.

From our previous example, we assigned the value of x && y to the parameter result.

answer = (x && y);

Here are other assignment operators:

| Operator | Description | ExampleA=10, B=5 |
| = | Simple Assignment | C = A + B; C = 15 |
| += | Add and Assignment | C += A (similar to C = C + A) |
| -= | Subtract and Assignment | C -= A (similar to C = C - A) |
| *= | Multiply and Assignment | C *=A (similar to C = C *A) |
| /= | Divide and Assignment | C /=A (similar to C = C /A) |
| %= | Modulus and Assignment | C %=A (similar to C = C %A) |

Exercise: Do the exercise below to understand how assignment operators work.

<!DOCTYPE html>

<html>

<body>

<script type="text/javascript">

<!--

var x = 22;

var y = 10;

var enter = "<br />";

document.write("Value of x =>(x = y) => ");

answer = (x = y);

document.write(answer);

document.write(enter);

document.write("Value of x =>(x += y) => ");

answer = (x += y);

document.write(answer);

document.write(enter);

document.write("Value of x =>(x -= y) => ");

answer = (x -= y);

document.write(answer);

document.write(enter);

document.write("Value of x =>(x *= y) => ");

answer = (x *= y);

document.write(answer);

document.write(enter);

document.write("Value of x =>(x /= y) => ");

answer = (x /= y);

document.write(answer);

document.write(enter);

document.write("Value of x =>(x %= y) => ");

answer = (x %= y);

document.write(answer);

document.write(enter);

</script>

<p> Practice using other variables! </p>

</body>

</html>

Did you get the output right?

Value of x =>(x = y) => 10
Value of x =>(x += y) => 20
Value of x =>(x -= y) => 10
Value of x =>(x *= y) => 100
Value of x =>(x /= y) => 10
Value of x =>(x %= y) => 0

Practice using other variables!

Special Operators

There are other operators in JavaScript that don’t fall under the categories mentioned above but are equally important to know if you want to learn how to code.

| Operator | Description | ExampleA=10, B=5 |
| ?: | Conditional Operator ( if condition is true? Then value X : Otherwise value Y | C= (A > B) ? less than value : greater than valueC= greater than value |
| typeof | Typeof (evaluates the data type of the operand) | C= typeof A == ‘string’ ? this is string: this is numericC= this is numeric |

Exercise: Demonstrate the use of special operators.

<!DOCTYPE html>

<html>

<body>

<script type="text/javascript">

<!--

var x = 10;

var y = 20;

var z = 'Z';

var enter = "<br />";

document.write("((x>y) ? 100:200) => ");

answer = (x > y)? 100 :200;

document.write(answer);

document.write(enter);

document.write("((x<y ? 100:200) => ");

answer = (x < y)? 100 :200;

document.write(answer);

document.write(enter);

answer = (typeof z=="string" ? "z is string":"z is numeric")

document.write(answer);

document.write(enter);

answer = (typeof x=="string" ? "x is string":"x is numeric")

document.write(answer);

document.write(enter);

</script>

<p> Practice using other variables!</p>

</body>

</html>

Here’s the output:

((x>y) ? 100:200) => 200
((x<y) ? 100:200) => 100
z is string
x is numeric

Practice using other variables!

***  

String Operators

String operators are used to perform operations on strings:

We can use the + operator to concatenate or add two strings together. For example:

txt1 = "Jane";
txt2 = "Deer";
txt3 = txt1 + " " + txt2;

txt3 will output a result of:

Jane Deer

We can use the += operator to add strings together as well:

txt1 = "What a wonderful ";
txt1 += "sunny day";

txt1 will output a result of:

What a wonderful sunny day

Although this is called the addition assignment operator, when we use the + operator on a string it is named a concatenation operator.

Adding Strings and Numbers

If you add two numbers together, the output is the sum of those numbers but, if you add a string and a number, the output is a string:

x = 5 + 10;
y = "5" + 10;
z = "Hello" + 10;
The output will be:

15

510

Hello10

Comparison and Logical Operators

We use these operators to test to see if a condition or statement is true or false, i.e. to see if there is any equality or any difference between values or variables. 

Comparison Operators

Supposing that x = 5, the list below explains the comparison operators:

OperatorDescriptionComparing       Returns  

==equal tox == 8       false              

x == 5true 

x == "5"true 

===equal value and equal typex === 5       true              

x === "5"false 

!=not equalx != 8       true              

!==not equal value or not equal typex !== 5       false              

x !== "5"true 

x !== 8true 

>greater thanx > 8       false              

<less thanx < 8       true              

>=greater than or equal tox >= 8                      false              

<=less than or equal tox <= 8                      true             

If/else statement

Right now, your programming is sequential, which means that the code is being executed from the top down. It is what we call linear code, with every code line being read by Java, starting with the first line and working down to the last line that you wrote. 

We don’t always require our programs to work like this, though. Sometimes, you want your code to execute only when and if specific conditions are met. For example, you might want a specific message to be displayed if a user is under 18, while a different one would display for those over 18\. What you want is to control how your code flows yourself, and we do this by using conditional logic.

When we talk about conditional logic, we are mostly talking about the IF word. For example, IF user is younger than 18 then display this message; IF user is older than 18, display this message. Luckily, you will find that using conditional logic in Java is easy so let’s begin by looking at IF statements. 

IF Statements

One of the most common things in computer programming is to execute code when one thing happens instead of something else.

Run the program and check it – Note that NetBeans tends to run the program in bold text in the window for Projects, not the code that you displayed. If you want the code run in your coding window, right-click on the code, anywhere and then click on Run File in the menu that appears. The output will now appear in the Output window.

Next, we change the user variable value from 17 to 18; now run the program again.

You should see that the program runs fine, no errors but nothing will be printed. The reason for this is because the message is in between the curly brackets in the IF statement and that statement is looking for values of lower than 18\. If the condition isn’t met, Java will ignore the curly brackets and anything in between them, moving on to the rest of the code.

Nested ifs

We have previously looked at nested scopes; now we want to look at nested ifs. You will interact most of the time with a nested if. The greatest lesson to learn is nested ifs point to the block of code with the else.

Read the following example:

![Description: 00027.jpeg](images/00029.jpeg)

You should be able to note that the last else has not been associated with if(j<20), but associated with the if(i==10).

IF … ELSE

If you don’t want to use two IF statements, there is another way -and IF … ELSE statement.

So, we have two choices in this code – the user is either 18 or younger, or older than 18\. Change your code so it matches what is above and try it. You should now see that the first message is printed out. Change the user variable value to 20 and then run the code again. You should see the message that is between the curly brackets for ELSE displayed in the Output window.

IF … ELSE IF

The first IF statement will test for the first condition, then we have the ELSE IF, followed by parentheses, in between which goes condition two. If there is anything that the first two conditions do not catch, it will be caught by the last ELSE. Again, we have sectioned the code using curly brackets and each IF, Else IF or ELSE has its own set. If you miss out any of these curly brackets, you will get an error message.

Before you try out any more code, you must first learn about a few more conditional operators. So far, you have used these ones:

< - Greater Than

< - Less Than

>= - Greater Than or Equal To

<= - Less Than or Equal To

Here's four more you can use:

&& - AND

|| -  OR

== - HAS A VALUE OF

!  - NOT

The first one, a pair of ampersand symbols, is used for testing two or more conditions at once.

We are checking to see if a user is older than the age of 18 but younger than the age of 40 – remember, we are checking what is in the variable called user. The first condition, “greater than 18”; the second condition, “less than 40”. Between those two conditions, we have the AND operator so the entire line is saying else if user is greater than 18 AND user is less than 40\.

Now run the program and test it again; before it runs you should already be able to guess what is going to print. The user variable has a value of 21 so the message that is between the else if curly brackets will show in the output window.

Nested IF Statements

Look at where the curly brackets are – get one set in the wrong place or miss one out and the code will not run. Nested IF statements might be a little tricky but, really, all you are doing is narrowing the choices down.

Boolean Values

Instead of using int, double or string, you would simply type in boolean (lower case b) and, after the variable name, you assign a TRUE or FALSE value. Notice that we use a single equal sign as the assignment operator.  If you wanted to see if a variable “has a value of”, you would need to use a pair of equals signs.

This time, we have used the NOT operator in front of the variable called user. The NOT operator is indicated by the use of an exclamation mark, just one, and it will be placed in front of the variable that you are trying to test. This operator tests for negation, which means that it is testing for the opposite of the actual value. 

Switch Statements 

Another way of controlling flow is to use a switch statement. This provides you with the option of testing for a range of values for the variables and can be used in place of complicated, long IF … ELSE statements.

Start with the word “switch” and then a set of parentheses. The variable you are checking is placed between the switch parentheses and is followed by a set of curly brackets.  The rest of the switch statement goes in between the curly brackets. 

Booleans Can be Objects

Usually, a Boolean is a primitive value that has been created from a literal:

var x = false;

but a Boolean may also be defined as an object by using the keyword new, for example:

new: var y = new Boolean (False)

The Switch Statement

Switch statements are used when we want to carry out differing actions depending on differing conditions, i.e. to choose from one of several code blocks to execute.

This is how the switch statement works:

*   The expression value is compared against each case value
*   If a match occurs, the block of code associated with the match will be executed.

Flow control structure

If you wanted to create a user registration form that asks for the user’s name, email address, age, and password, you’d first declare the variables as:

| var name;var email;var age;var password; |

Now we’d need to store the user’s input. For now, we use the prompt function:

| name = prompt('What’s your name?');email = prompt('What’s your email?');age = prompt('What’s your age?');password = prompt('Please enter your desired password: '); |

Assuming you’ve entered the right kind of information in the data fields, the name, email, age, and password variables now have the right type of data to process and store. What if, however, the user leaves the email field blank, or the age field with a letter? We can’t just let the program continue if some of the vital fields of information don’t have the right kind of data, therefore we use flow control statements. The first one we shall discuss is the if statement. 
if...structure

Sometimes we have to take different function depending on different circumstances. We can use it with an if statement and a conditional operator ? also called a "question mark operator."
2.10.1 "If" statement
If statement(...) evaluates the condition in parentheses and if the result is true, execute the block of code.
For example:

![Description: 00120.jpeg](images/00030.jpeg)

this example above, the condition is equality check (year == 2015), but it can always be more complex.
We want to execute more than one statement; we need to wrap your block of code inside the braces:

![Description: 00121.jpeg](images/00031.jpeg)We recommend that you wrap the code block with {} loopholes each time you use the if statement, even if there is only one statement to execute. This will improve readability.

Function and basic properties of JavaScript

In general, functions serve as “subprograms” that you can invoke using internal/external codes. Similar to a complete program, a function has a group of statements known as its “body.” JavaScript allows you to pass values to a function. Additionally, a function can return a value.

JavaScript considers functions as first-class objects, since they possess methods and properties found in other programming objects. The main difference between functions and other JavaScript objects is that you can invoke a function whenever you need to.

What is a Function?

In JavaScript, each function is treated as a unique object. Also, functions are different from procedures. Functions return a value 100% of the time, while some procedures don’t.

You must add a “return” statement in your functions if you want them to return a value. The “return” statement specifies the value/s that must be returned. Functions that don’t have a return statement give a default value. In most cases, the default value of a function is “undefined.”

The arguments of a function are the parameters used in calling it. JavaScript uses values to pass arguments to a function. If a function modifies an argument’s value, the modification won’t appear globally or inside the function itself. However, an object reference is a value too (and a special one at that) – if a function alters the properties of a referred object, the alteration/s will appear globally.

How to Define a Function

In JavaScript, you can define functions in different ways. Let’s discuss each approach in detail:

*   Using the function statement – JavaScript offers a special syntax that you can use to declare a function. The syntax is:

![Description: 00032.jpeg](images/00032.jpeg)

That syntax has three different parts, which are:

*   name – This is the name of the function. You may replace this with any valid identifier.
*   param – This is the  argument/parameter that you want to pass to the function. JavaScript allows you to include up to 255 parameters in each function.
*   statements – This section holds the statements (i.e. the body) of a function.

*   Through the function expression – This approach is similar to the previous one. In fact, it uses the syntax (see below):

![Description: 00033.jpeg](images/00033.jpeg)

*   Using JavaScript’s “Function Constructor” – JavaScript allows you to generate functions using “new” (i.e. a JavaScript operator). Here is the syntax that you must use:

![Description: 00034.jpeg](images/00034.jpeg)

The syntax given above has the following parts:

*   arg1, arg2, … argN – This part holds the name/s you want to use as the formal parameter/s.
*   functionBody – This is a string that holds JavaScript statements (i.e. the body of the function).

How to Call a Function

When defining a function, you are just naming that function and assigning what to be done once the function is invoked/called. Call a function if you want it to perform the assigned actions. For instance, if you have defined the “square” function, you may call it using the following code:

square(2);

The code given above calls the “square” function and assigns 2 as the argument. The function runs its statements and gives 4 as the resulting value.

Your functions must be within the proper scope when you call them. However, you can hoist (i.e. lift to the top) your function declarations. Here’s an example:

![Description: 00035.jpeg](images/00035.jpeg)

A function’s arguments may hold different programming elements (i.e. not just numbers and strings). JavaScript allows you to assign entire objects to your functions. For example, show_props() (i.e. a built-in JavaScript function) accepts objects as arguments.

The Scope of a Function

If you defined a variable within a function, you won’t be able to access that variable from outside the function. That’s because you defined the variable within the function’s scope only. A function, however, can access all of the variables and other functions created within the scope in which it was defined. Simply put, global functions can access global variables. A nested function (i.e. a function placed inside another function) can access the variables created inside its “mother function.”

The Arguments of a Function

JavaScript treats arguments as array objects. Inside a function, you may access the arguments it contains using the following syntax:

arguments[n]

In this syntax, “n” represents the argument’s ordinal number, beginning at zero. That means the initial argument of a function is arguments[0].

If you’ll use the JavaScript object called “arguments,” you may invoke functions that hold more arguments than what was declared in the code. This object can be extremely useful, especially if you have no idea about the number of arguments that you must assign to a function. To determine the quantity of objects inside a function, you may use arguments.length. Then, you may use the “arguments” object to access the function’s arguments.

Chapter 4: Advanced Programing structure

Functions and scope of the variables

Let’s see now, normally when we are talking about a ‘function’ what’s the first thing that comes to your mind? Obviously an activity right? 

The functions in JavaScript also work in a similar manner. Functions are blocks of codes which are required to be executed over and over again by the program. A Function is used to perform a particular task. A Function can contain any number of arguments and statements; they can even have none. Depending on how the structure is coded, it may or may not return any value to the user.

A Function is declared in the following manner:

Function name(                 ) { /*code blocks to be executed*/}

To start the Function, we start with the function keyword, and then we add the name, and parentheses. To finish the function, we place the code blocks to be executed in a curvy brackets. 

You can also put the function in a named variable-

var jam = function() {/* code blocks to be executed*/}

Below are few examples of how you can execute a function-

i) This is the example of the most basic function

varsayHello = function(person, greeting) {

var text = greeting + ‘ , ‘+ person;

console.log(text);

};

Say Hello (‘ Jessica’ , ‘ Hello’);

ii) This is the example of a function that returns a value

var greet = function (person, greeting) 

{

var writing = greeting + ‘ , ‘ + person ;

return function () {console.log(text); };

}

console.log(greet(‘Richard’ ,’ Hello”));

iii) Sometimes, you might want to use a nested function. (Note: A nested function is a function within another function.)

varsayHi = function( person, greeting) {

var text = greeting + ‘,’ + person;

return function() {console.log (text);}

};

var greeting = greet( ‘ Richard’ , ‘Hello’);

greeting();

Self-Executing Anonymous Function

Programmers have always been looking for the most advanced and clever methods available to improve their programming experience and ways to make it more accessible and easier for them. This resulted in the creation of theSelf-Executing Anonymous function.

The core purpose of the self-executing anonymous function is to create a JavaScript function and then immediately execute it upon its conception. 

This makes it much easier for a programmer who isworking on large scale programs. Likewise, it will help you to code without creating a messy global namespace. 

A basic Self-Executing Anonymous Function Would be-

![Description: 00006.jpeg](images/00036.jpeg)

It is very important that you understand how to use this type of function if you plan on programming complex code in JavaScript. Using the Self-Executing Anonymous Function can produce some great code that is easy to use. As an example, the JQuery library is designed to make using JavaScript on websites much easier. It does this by wrapping the entire library in one large self-executing function. 

Typeof Operator

You might run into a situation where you need to determine the type of variable that you are working in JavaScript. You won’t have call Sherlock Holmes to find that! Instead, you can simply use the ‘typeof’ operator to determine the type of any specific value. In other words, the typeof operator is used to evaluate the type of the operand. 

EX-

Varmyvar=0

alert(typeofmyvar) //alerts “number”

Number isn’t the only type of operand that can be detected. It can also be: string, Boolean, object, null, and not defined.

Scope

Scope is the accessibility of a variable.

A good understanding of Scope is necessary when it comes to debugging because it allow you to know what variable from which code block is causing the problem.

The simple rule here is that whenever you declare a variable inside a scope, it will only be recognized by the statements that are inside that scope; the statements that are outside the scope will not acknowledge its existence and so that variable will not work.

Another way to look at this is to imagine your entire code as a hotel with specific functions and sections of code as hotel rooms. The hotel rooms represent the private scopes of the code, while the common areas represent the global scope. A person in one hotel room cannot see or use what is in another hotel room. Staff who work in the hotel (and the global scope) also don’t have access to private hotel rooms unless they have specific permission. Meanwhile, guests can go through the common areas and make use of any object there. 

Thus, you can see how scope can affect how your code runs. If you need two different functions to access the same variable, you need to ensure that they both have access to it. One key way to ensure that the necessary variables have access to is to make your variables globally accessible.

There are two possible alternatives if you want your variables to become globally accessible. 

The first thing you can do is to declare the variable outside the scope of your given piece of code, this will allow any functions in your program to be able to call it and recognize it.

The other thing you can do is to declare the variables inside your scope without using the word var. If the same variable was not defined at the beginning of the code outside the scope of the piece of code in question, then the variable will act similarly to a global one.

Ex-

var foo = ‘hello’;

var talkHello = function() {

console.log(foo);

};

talkHello(); // logs ‘hello’

console.log(foo); // also logs ‘hello’

As you can see, the variable foo is declared outside of the function talkHello. That means that foo is a global variable and any function will be able to access it, so when the function talkHello calls it, it is accessible.

The following example is contradictory to the first example. This shows that a code block that was written outside the scope is not being able to recognize the variable.

var talkHello = function() {

var doo = ‘hello’;

console.log(doo);

};

talkHello(); // logs ‘hello’

console.log(doo); // gives an empty log.

In this example, the variable doo is called inside the function talkHello. This creates a private variable that is only accessible to the function, hence when the command console.log(doo) attempts to access it, it returns a null value.

The “break” Statement

Programmers use this statement to end loop or switch statements. When using a “break” statement, you must remember the following rules:

*   If your break statement doesn’t have a label, it will terminate the innermost loop/switch and pass the control flow to the next statement.
*   If your break statement has a label, it will terminate the labeled statement.

The syntax of a break statement is:

![Description: 00028.jpeg](images/00037.jpeg)

Use the first variant of the syntax if you don’t need to specify a label. This will terminate the innermost loop/switch. Use the second variant if you want to terminate a certain loop/switch. Just enter the label of that particular loop or switch. When using the second variant, only the specified loop/switch will be terminated.

The “for… of” Statement

This statement is a recent addition to the JavaScript language. It creates a loop that can repeat “iterable objects” (e.g. maps, sets, arrays, arguments, etc.). It also invokes an iteration hook that will run for each distinct property of an object. JavaScript allows you to customize the iteration hook of any “for… of” statement. Here is the syntax that you must use:

![Description: 00029.jpeg](images/00038.jpeg)

The “for… in” Statement

A “for… in” statement repeats the assigned statement/s over the properties of any object. JavaScript will execute the assigned statement/s for every property. The syntax of a “for… in” statement is:![Description: 00030.jpeg](images/00039.jpeg)

The “continue” Statement

You may use this statement to restart other statements (e.g. for, while, do… while, and label). Here are the two rules that you must remember when using a “continue” statement:

*   If you won’t include a label in your continue statement, it will terminate the current process of the innermost loop and continue the next one. Unlike a break statement, a continue statement cannot terminate an entire loop. If used on “while” loops, the control flow will return to the assigned condition. If used on a “for” loop, on the other hand, the control flow will go back to the increment expression.
*   If you’ll include a label in your continue statement, it will only affect the statement linked to that label.

The syntax of a continue statement has two forms, which are:

![Description: 00031.jpeg](images/00040.jpeg) Other Control Structures

The flow control structures that have been seen (if, else, for) and the sentences that modify their behavior (break, continue) are not sufficient to perform some complex tasks and other types of repetitions. For this reason, JavaScript provides other flow control structures that are different and in some cases more efficient. While Structure The while structure allows you to create loops that run no more or more times, depending on the condition indicated. Its formal definition is: while (condition) {... }

The operation of the while loop is summarized in: "While the indicated condition is fulfilled, repeat the instructions included within the loop indefinitely". If the condition is not met even the first time, the loop is not executed. If the condition is met, the instructions are executed once and the condition is checked again. If the condition is still fulfilled, the loop is executed again and so it continues until the condition is not met. Obviously, the variables that control the condition must be modified within the loop itself, since otherwise, the condition would always be met and the while loop would be repeated indefinately

Structure do ... while

The loop of type do ... while is very similar to the while loop, except that in this case the instructions of the loop are always executed at least the first time. Its formal definition is: do { ... } while (condition); In this way, as the condition is checked after each repetition, the loop instructions are always executed the first time. It is important not to forget that after the while () the character must be added; (contrary to what happens with the simple while loop). Using this loop you can easily calculate the factorial of a number: var result = 1; var number = 5; do { result * = number; // result = result * number number--; } while (number > 0); alert (result); In the previous code, the result is multiplied in each repetition by the value of the variable number. In addition, in each repetition, the value of this variable number is decremented. The condition of the do ... while loop is that the number value is greater than 0 since the factorial of a number multiplies all numbers less than or equal to itself, but up to number 1 (the factorial of 5, for example, is 5 x 4 x 3 x 2 x 1 = 120). As in each repetition, the value of the variable number is decremented and the condition is that number is greater than zero, in the repetition in which number is worth 0, the condition is no longer fulfilled and the program leaves the do loop ... while. Switch Structure The if ... else structure can be used to perform multiple checks and make complex decisions. However, if all conditions always depend on the same variable, the resulting JavaScript code is too redundant: if (number = = 5) {...} else if (number = = 8) {...} else if ( number = = 20) {... } else {... }

In these cases, the switch structure is the most efficient, since it is specially designed to easily handle multiple conditions on the same variable. Its formal definition may seem complex, although its use is very simple. The switch structure is defined by the reserved keyword switch followed, in parentheses, by the name of the variable to be used in the comparisons. As usual, the instructions that are part of the switch are enclosed in quotes {and}. Within the switch, all the comparisons that you want to make on the value of the variable are defined. Each comparison is indicated by the reserved word case followed by the value with which the comparison is made.

What happens if no value of the switch variable matches the values  defined in the cases? In this case, the default value is used to indicate the instructions that are executed in the case where no case is met for the indicated variable. Although default is optional, switch structures usually include it to define at least one default value for some variable or to display a message on the screen

Chapter 5: Data Structures: Objects & Arrays

Introduction to Objects

Procedural programming required programmers to spell out almost every command to the computer. This can quickly lead to messy code, so people thought about keeping certain commands and information inside what one can call an "object." For instance, if you wanted to create a database of pets, you’d have to do something like:

| //First, we create arrays with the information we wish to savevar petName = ["Cat", "Spot", "Fluffy"];var petSpecies = ["Dog", "Fish", "Parrot"];var petAge = [5, 2, 6];var petGender = ["Male", "Female", "Male"];var petDetails = [petName, petSpecies, petAge, petGender]; //Then we create a function that displays themvar displayInformation = function(details){    for(var counter = 0; counter < petSpecies.length; counter++)    {    console.log("Name: "+ details[0][counter]);    console.log("Species: "+ details[1][counter]);    console.log("Age: "+ details[2][counter]);    console.log("Gender: "+ details[3][counter]);    }};displayInformation(petDetails); |

While the code does work and provides us with a relatively neat list of information, the code is rather messy and can get pretty hard to debug when new functions and details are added. That being said, here’s a code snippet that turns the first entry into an object:

| var pet = {};pet.name = "Cat";pet.species = "Dog"; pet.age = 5;pet.gender = "Male";pet.showDetails = function(){    console.log("Name: "+ this.name);    console.log("Species: "+ this.species);    console.log("Age: "+ this.age);    console.log("Gender: "+ this.gender);}pet.showDetails(); |

This line:

| var pet = {}; |

Is what creates an object with the name "pet." There are actually two ways to create an object, and this is the first, called the literal notation. We’ve started with an empty object and added attributes after the declaration, but we can actually start with a filled object:

| var pet = {    name: "Cat",    species: "Dog",    age: 5,    gender: "Male",};pet.showDetails = function(){    console.log("Name: "+ this.name);    console.log("Species: "+ this.species);    console.log("Age: "+ this.age);    console.log("Gender: "+ this.gender);}pet.showDetails(); |

Take note of the differences, subtle as they may be! (e.g., using a colon (:) instead of an equal sign (=))

You can also use a constructor, turning the code snippet into:

| var pet = new Object();pet.name = "Cat";pet.species = "Dog"; pet.age = 5;pet.gender = "Male";pet.showDetails = function(){    console.log("Name: "+ this.name);    console.log("Species: "+ this.species);    console.log("Age: "+ this.age);    console.log("Gender: "+ this.gender);}pet.showDetails(); |

Both ways of creating objects are correct, so it really is all up to preference.

Now notice how the object is a little bit different from the other data types we’ve used so far. This is because objects are modern concepts that serve to represent real world stuff by keeping all the relevant details and information in one place. For instance, if one is to create a "phone" object, then it’d most likely contain attributes like screen size, pixel density, number and speed of processors, RAM, etc. If we want to create different phones, we’d just simply have to do something like:

| var smartPhone1 = {    screenSize: 5,    pixelDensity: 200,    processorNumber: 2,    processorSpeed: 500,};var smartPhone2 = {    screenSize: 6,    pixelDensity: 400,    processorNumber: 8,    processorSpeed: 2000,}; |

This makes organizing data much more efficient and easy.

As an exercise, print out the details of each phone into the console by accessing the properties using the dot notation. To start you off, here’s the code for the screenSize of smartPhone1 printed to the console:

| console.log(smartPhone1.screenSize); |

So far, we can access either information or functions of an object using the dot notation. The variables we access using the dot notation are called properties, while the functions we access using the dot notation are called methods. 

The concept of methods and properties arose from the need to turn real life concepts into code. Going back to our phone example, for instance, without objects there’s no simple way to tell which screen size belongs to a specific phone, unless one keeps the phone names and screen sizes in two different arrays. This quickly becomes more complicated when more attributes are added. 

Going back to our explanations about functions, functions are able to keep a large number of instructions without messing up the whole source code by being invokable with a function name. Going back to our phone example, phones differ in terms of what functionalities are available, as well as the internal implementation of those functionalities. For instance, let’s add a texting function to the two phones from our example earlier, as well as the capability to swap sim cards:

| var smartPhone1 = {    screenSize: 5,    pixelDensity: 200,    processorNumber: 2,    processorSpeed: 500,    simCardNumber: 123456,    textNumber: function(number, text)    {        console.log("Message, '" + text + "' has been sent to " + number);        console.log("Processing time: " + text.length/this.processorNumber);    },    setSimCardNumber: function(newSimCardNumber)    {        this.simCardNumber = newSimCardNumber;    }, };var smartPhone2 = {    screenSize: 6,    pixelDensity: 400,    processorNumber: 8,    processorSpeed: 2000,    simCardNumber: 654321,    textNumber: function(number, text)    {        console.log("'" + text + "' sent to " + number);        console.log("Processing time: " + text.length/this.processorNumber);    },    setSimCardNumber: function(newSimCardNumber)    {        this.simCardNumber = newSimCardNumber;    }, }; |

Notice how both phones have the same set of functions, but with a slightly different implementation, just as in real life, when you tell somebody to text someone, you only need to specify the message and the number you need to send it to regardless of the type of phone used. As for the setSimCardNumber function, this is actually common practice in object-oriented programming; instead of setting the properties of an object manually, like:

| smartPhone1.simCardNumber = 55555; |

Since the setter at least can have an extra set of instructions, like checking for any possible errors in the process. 

Another thing you might have noticed is that we’re using the keyword, "this" when we’re creating methods for our objects. The keyword, "this" acts as a placeholder and will point to the object that called the method. For example, if you type:

| smartPhone2.textNumber(0000, "Hi!"); |

Then we call the function:

|     textNumber: function(number, text)    {        console.log("'" + text + "' sent to " + number);        console.log("Processing time: " + text.length/this.processorNumber);    }, |

This makes references to a processorNumber variable. Because of the "this" keyword, the function finds a variable called "processorNumber" in the object that called it, which is "smartPhone2." 

Introduction to Object Oriented Programming: Classes

A class is an extended idea of an information structure, as opposed to holding just information. It can hold both functions and data. An object, on the other hand, is an instantiation of a class. Regarding variables, a class would be the type, and an object would be the variable.

Classes are by and large declared utilizing the keyword class, with the accompanying syntax:

class <className> {

accessSpecifier_1:

memberData;

memberFunction;

access_specifier_2:

memberData;

memberFunction;

} <objectName>;

Where className is an identifier for the class, objectName is a non obligatory identifier of names for objects of this class. The assortment of the presentation can contain parts, which could be either data members or function statements, and alternatively get to specifiers.

Example:

int a;

Here, ‘a’ is an object of the int class.

Access Specifiers

All is fundamentally the same to the statement on information structures, aside from that we can now incorporate additionally functions and data parts, and this new thing called access specifier. A right to gain access or access specifier includes one of the accompanying three keywords: private, public or protected. These specifiers alter the right to gain entrance access to the members that fall under its scope.

● Private:

Such members of a class are available just from inside different members of the same class or from their companions.

● Protected

Such members are available from members of their same class and from their companions, additionally from parts of their inferred classes.

● Public

Such members are available from anyplace where the item is noticeable.

By default, all members of a class are private to access for all its members. 

Example:

class myRectangle {

double a, b;

public:

void setValues (double, double);

double func (void);

} myRect;

In this example, a and b are private while functions setValues() and func() are public.

Constructors and Destructors

You, for the most part, need to introduce variables or allocate dynamic memory during the methodology of creation to clear up memory and to abstain from returning startling values during the execution of the program.

If you consider the previous example, had you sent ‘a’ and ‘b’ as parameters to a function without initializing them, the values taken by the function will be garbage. Your code will most likely give wrong results or crash abruptly.

Keeping in mind the end goal to keep away from that, a class can incorporate a unique function called constructor, which is naturally called at whatever point another object of this class is made. This constructor function must have the same name as the class, and can't have any return data type.

The first statement in the main() instantiates the class myRectangle. The parameters passed with the creation of the object called the constructor function and initialize the dimensions of the rectangle to 1 and 2\. Therefore, when the areaRect() is called, the function returns the correct value of area, 2\.

Constructors can't be called unequivocally as though they were normal functions. They are just executed when another object of that class is made. You can likewise perceive how not one or the other, the constructor function (inside the class) nor the last constructor definition incorporate a return value, not even void.

The destructor satisfies the inverse usefulness. It is consequently called when an item needs to be demolished, either on the grounds that its extent of presence has completed (for instance, on the off chance that it was characterized as a nearby protest inside a function and the function closes) or in light of the fact that it is an article alertly appointed and it is discharged utilizing the operator delete.

The destructor must have the same name as the class. However, a tilde sign (~) is placed before the name and it should likewise give back no return value. The utilization of destructors is particularly suitable when an object uses dynamic memory amid its lifetime and right now of being annihilated, we need to discharge the memory that the item was designated.

Overloading Constructors

Like other functions, a constructor can likewise be overloaded with more than one function definitions that have the same name yet distinctive sorts or number of parameters. Keep in mind that for overloading to work, the compiler will call the one whose parameters match the values utilized as a part of the function call. On account of constructors, which are consequently called when an object is made, the one executed is the particular case that matches the values passed on the item assertion.

Default Constructor

In the event that you don't declare any constructors in a class definition, the compiler accepts the class to have a default constructor with no parameters. The compiler not just makes a default constructor for you on the off chance that you don't create your own.

It gives three extraordinary functions altogether that are certainly declared in the event that you don't declare your own. These are the copy constructor, the default destructor and the copy assignment operator.

The copy constructor and the copy assignment operator duplicate all the information contained in an alternate object to the members of the current object.

Pointers to Classes

It is flawlessly legitimate to make pointers that indicate classes. We essentially need to consider that once declared, a class turns into a substantial data type, so we can utilize the class name as the data type for the pointer.

Example:

myRectangle * pointerRect;

The pointerRect is a pointer to an object of class myRectangle.

As it happened with information structures, so as to allude specifically to a specific member of an object pointed by a pointer, we can utilize the arrow operator (->) of indirection.

Overloading Operators

C++ consolidates the alternative to utilize standard operators to perform operations with classes notwithstanding with major data types. C++ has a functionality that allows you to overload operators by planning classes ready to perform operations utilizing standard administrators.

To overburden an operator with a specific end goal to utilize it with classes we proclaim operator functions, which are consistent functions whose names are the function keywords emulated by the operator sign that we need to overload. The arrangement is:

<data type> <operator> <operator sign> (<parameters>)

{

              //Code

}

Here you have an illustration that overloads the addition operator (+). We are going to make a class to store 2-D vectors and afterward, we are going to include two of them: a (2,4) and b (3,4). The addition of two 2D vectors is an operation as basic as adding the two x directions to get the ensuing x direction. The result of this operation on the points ‘a’ and ‘a’ should be (2+3, 4+4), which is equal to (5, 8).

#include <iostream>

using namespace std;

class myVector {

  public:

    int a, b;

    myVector () {};

    myVector (int, int);

    myVector operator + (myVector);

};

myVector :: myVector (int x, int y) {

  a = x;

b = y;

}

myVector myVector :: operator+ (myVector myParam) { myVector tempo;

tempo.a = a + myParam.a;

tempo.b = b + param.b;

return (tempo);

}

int main () {

  myVector x (2, 4);

  myVector y (3, 4);

  myVector z;

  z = x + y;

  cout << z.a << "," << z.b;

  return 0;

}

Keyword this

The word this speaks of a pointer to the object whose member function is continuously executed. It is a pointer to the object itself.

It is additionally regularly utilized as a part of operator= function that returns objects by reference (keeping away from the utilization of impermanent objects). Taking after with the vector's illustrations seen before we could have composed an operator= capacity like this one.

Actually this capacity is very much alike to the code that the compiler creates verifiably for this class on the off chance that we do exclude an operator= part function to duplicate objects of this class.

Static Members

A class can contain static parts, either data or functions. Static data of a class are otherwise called "class variables", on the grounds that there is stand out novel values for all the objects of that same class. Their substance is not the same as one object of this class to an alternate.

Friend Functions

On a fundamental level, private members of a class can't be gotten to from outside the same class in which they are pronounced. Then again, this standard does not influence friend functions.

On the off chance that we need to proclaim an outside function as friend of a class, in this manner permitting this capacity to have admittance to the private and secured members of this class, we do it by proclaiming a model of this outer capacity inside the class, and placing the keyword friend before it.

Example:

#include <iostream>

using namespace std;

class myRectangle {

int x, y;

public:

void setValues (int, int);

int func () {return (x * y);} friend myRectangle copy (myRectangle);

};

void myRectangle :: setValues (int a, int b) {

x = a;

y = b;

}

myRectangle copy (myRectangle rectParam) {

myRectangle rects;

rects.x = rectParam.x*2;

rects.y = rectParam.y*2;

return (rects);

}

int main () {

myRectangle rectx, recty;

rectx.setValues (2,3);

recty = copy (rectx);

cout << recty.func();

return 0;

}

The copy function is a friend function of myRectangle. From inside that function, we have possessed the capacity to get to the private members of the class, ‘x’ and ‘y’. Recognize that not one or the other in the statement of copy() nor in its later use in principle() have we considered copy a part of class myRectangle. It isn't! It essentially has entry to its private and secured members without being a part of the class.

The friend function can serve, for instance, to direct operations between two separate classes. For the most part, the utilization of friend function is out of an item arranged programming technique, so at whatever point conceivable it is better to utilize parts of the same class to perform operations with them.

Friend Classes

Generally as we have the likelihood to declare a friend function capacity, we can likewise declare a class as friend of another, allowing that top of the line access to the ensured and private members of the second one.

Example

#include <iostream>

using namespace std;

class mySquare;

class myRectangle {

int x, y;

public:

int myArea () {return (x * y);}

void convert (mySquare a);

};

class mySquare {

private:

int x;

public:

void setSide (int a)

{side=a;}

friend class myRectangle;

};

void myRectangle::convert (mySquare a) {

x = a.x;

y = a.x;

}

int main () {

mySquare sqr;

myRectangle rect;

sqr.setSide(4);

rect.convert(sqr);

cout << rect.myArea();

return 0;

}

In this illustration, we have declared myRectangle as a companion of mySquare so that myRectangle functions could have entry to the ensured and private members of mySquare, all the more solidly to Csquare::x, which portrays the side of the square.

Inheritance between Classes

A key feature of C++ classes is inheritance, which permits you to make classes that are inferred from different classes. So, they naturally incorporate some of its "parent's" members, in addition to its own.

Classes that are inferred from others inherit all the available parts of the base class. That implies that if a base class incorporates a part A and we determine it to an alternate class with an alternate part called B, the determined class will contain both parts A and B.

To determine a class from an alternate, we utilize a colon (:) as a part of the revelation of the inferred class utilizing the accompanying arrangement:

class <derived class name>: public <base_class_name>

{

              //Code

};

Where derived_class_name is the name of the inferred class and base_class_name is the name of the class on which it is based. The public specifier may be supplanted by any of alternate access specifiers protected and private. This access specifier portrays the base access level for the parts that are inherited from the base class.

#include <iostream>

using namespace std;

class myPol {

protected:

double x, y;

public:

void setValues (double a, double b)

{ x = a; y = b;}

};

class myRect: public myPol {

public:

double myArea ()

{

return (x * y);

}

};

class myTri: public myPol {

public:

int myArea ()

{

return (x * y/ 2);

}

};

int main () {

myRect rect;

myTri trgl;

rect.setValues (4,5);

trgl.setValues (4,5);

cout << rect.myArea() << endl;

cout << trgl.myArea() << endl;

return 0;

}

The objects of the classes, myRectangle and myTriangle, each one contain members inherited from myPolygon. These are: x, y and setValues().

The protected access specifier is like private. Its contrast happens actually with inheritance. At the point when a class inherits from another, the parts of the inherited class can get access to the protected members inherited from the base class, however not its private members.

Since we needed x and y to be public from parts of the inferred classes myRectangle and myTriangle and not just by parts of myPolygon, we have utilized protected rather than private.

What Is Inherited From The Base Class

On a basic level, an inherited class inherits each member of a base class with the exception of:

● Constructor

● Destructor

● Operator=() members

● Friends

Although, the destructors and constructors of the base class are not inherited themselves, the destructor and default constructor are constantly called when another object of an inherited class is made or destroyed. In the event that the base class has no default constructor or you need that an overload constructor is called when another inherited object is made, you can detail it in every constructor meaning of the determined class:

<derived constructor name> (<parameters>) : <base constructor name> (<parameters>) {

              //Code

}

Multiple Inheritance

There is a provision for a class to inherit from multiple classes in C++. This can be carried out, by separating the base classes, with commas in the class declaration. Case in point, in the event that we had a particular class to print on screen (myOutput) and we needed our classes myRectangle and myTriangle to likewise inherit its members notwithstanding those of myPolygon we could compose them accordingly. 

Implementing Polymorphism

Before getting into this segment, it is prescribed that you have a legitimate understanding of pointers and class inheritance. In the event that any of the accompanying explanations appear unusual to you, you ought to audit the showed segments:

Pointers to base class

One of the key peculiarities of inherited classes is that a pointer to an inferred class is sort good with a pointer to its base class. Polymorphism is the craft of exploiting this straightforward however compelling and flexible peculiarity that brings Object Oriented Methodologies to its maximum capacity.

Virtual Members

A part of a class that could be reclassified in its inferred classes is known as a virtual member. With a specific end goal to declare a part of a class as virtual, we must place before its statement the keyword virtual.

What the virtual keyword does is that it permits a part of a determined class with the same name as one in the base class to be properly called from a pointer, and all the more accurately when the kind of the pointer is a pointer to the base class yet is indicating an object of the inferred class.

Abstract Base Class

The fundamental distinction between a theoretical base class and a customary polymorphic class is that in light of the fact that in conceptual base classes no less than one of its parts needs usage, we can't make cases (items) of it. Be that as it may a class that can't instantiate objects is not completely futile. We can make pointers to it and exploit all its polymorphic capabilities.

Virtual members and dynamic classes stipend C++ the polymorphic qualities that make item situated programming such a helpful instrument in huge activities. Obviously, we have seen exceptionally basic employments of these features, however these peculiarities could be connected to exhibits of items or progressively apportioned objects.

Custom Constructors

As you may have noticed, having to create and assign properties every time for similar objects is quite a hassle. Since smartPhone1 and smartPhone2 are both classified as phones, then they’re bound to have similar methods and properties. With that in mind, we can do something like this to make our code cleaner:

| function Phone(screenSize, pixelDensity, processorNumber, processorSpeed, simCardNumber){    this.screenSize = screenSize;    this.pixelDensity = pixelDensity;    this.processorNumber = processorNumber;    this.processorSpeed = processorSpeed;    this.simCardNumber = simCardNumber;    this.textNumber =  function(number, text)    {        console.log("'" + text + "' sent to " + number);        console.log("Processing time: " + text.length/this.processorNumber);    };    this.setSimCardNumber = function(newSimCardNumber)    {        this.simCardNumber = newSimCardNumber;    };}//Now we can create our two smart phones using the constructor we’ve just made!var smartPhone1 = new Phone(5, 200, 2, 500, 123456);var smartPhone2 = new Phone(6, 400, 8, 2000, 654321);//let’s add a new phone!var simplePhone1 = new Phone(2.5, 100, 1, 80, 111111); |

See how it makes our code much shorter? In real life, this would be the equivalent of creating a factory - you systemize the creation of objects while allowing a certain number of customizations to be made after the basics are taken care of. 

Using Object Literal

The object literal method uses the var keyword similar to defining a variable.

var dog = {name: “Abby”, eyeColor: "brown", age: 7};

Also, similar to defining variables, you can define the object first and add the properties at a later time.

var dog = {};

dog.name= “Abby”;

dog.eyeColor= "brown";

dog.age= 7;

Node tree

All HTML elements and attributes are nodes in the Document Object Model (DOM). Take a look at the following HTML code as a starting point: < html >

< head >

< title > The title </ title >

</ head >

< body > The body

</ body >

</ html >

Arrays

What is an array?

A parameter can have a list of values. Take, for example, the variable color. The values for these are red, blue, and yellow. Instead of defining a variable for each (eg. color1=red, color2=blue, color3=yellow), we use arrays to simplify the way we store multiple values or lists of values in a variable.

An array can also contain arrays inside. This is called multidimensional arrays.

Creating An Array

One Dimension Array

Let’s take a look on how we can use arrays in our code.  Arrays are created in a similar way to how we create a regular variable.

Syntax:

There are two ways to create an array:

var colors = new Array (“red”, “blue”, “yellow”);

Or you may directly define it like this:

var colors = [red”, “blue”, “yellow”];

To assign and access the values inside an array, we refer to them by their element and index number. The numbers [0-2] in the sample below are the index numbers. The colors red, blue, and yellow are the corresponding array elements.

colors[0] = red

colors[1] = blue

colors[2] = yellow

You may also define an array name first and add values at a later time:

var colors = [];

colors[0]= “red”;

colors[1]= “blue”;

colors[2]= “yellow”;

colors[55]= “green”;

Note that in the above example, we have added the array element green to array index 55\. Defining array indices sequentially is not required. However, this will automatically create blank elements from all the indices from 3 to 54\. When you check on the array length, this will return 56 even if you only have 4 elements defined.

While you may create a long list of color names for your array, keep in mind that the maximum number of values an array can store is up to 4,294,967,295 elements.

Multidimensional Array

An array can contain an array containing an array. This can go on to several levels depending on how you want to group your data.

Continuing with our color variable, follow the example below. Suppose that we want to store primary colors and secondary colors in this array.

Syntax:

To define multidimensional arrays, we use additional brackets to denote array and index number. Think of multidimensional arrays as outlines.

var color = [["red","blue","yellow"],["green","purple","orange"]]

Using Arrays within the code

Retrieving array values

Use the code below to retrieve values from the sample above:

color[0][0]; //red

color[1][1]; //purple

color[0]; //["red", "blue", "yellow"]

Note in the last command that when you do not specify the specific index number when retrieving values for a multidimensional array, all of the array elements will be returned.

Array Properties

The array object comes with different properties.

| Property | Description |
| prototype | Allows you to add properties and methods to an Array object |
| constructor | Ouputs a reference to the function that created the Array object |
| index | Zero-based index of the match in the string |
| input | Present only in arrays created by regular expression matches |
| length | Ouputs or sets the number of elements in an array |

Here we demonstrate the different properties. Use the codes below to demonstrate the array properties.

Constructor

Syntax:

array.constructor

Output:

samplearr.constructor is:function Array() { [native code] }

Length

Syntax:

array.length

Output:

samplearr.length is:3

Prototype

Syntax:

object.prototype.name = value   

Output:

Book title is: GOT
Book author is: Martin
Book price is: 100

Array Methods

The following are the methods of the array object, including their description.

In the following exercises, we will explore how some of the array methods can be used:

concat()

Outputs a new array consisting of this array joined more arrays

Syntax:

array.concat(value1, value2, ..., valueX);

Argument Details:

valueX : Arrays and/or values to concatenate to the resulting array.

Return Value:

Returns the array elements

Output:

new str : X,Y,Z

new str : X, Y, Z

new str : X + Y + Z

push()

Adds the given element in the last of the array and outputs the length of the new array

Syntax:

array.push();

Argument Details:

element1, ..., elementX: The elements to add to the end of the array.

Return Value:

Outputs the length of the new array.

Output:

new numbers are : 2,4,6,8

new numbers are : 2,4,6,8,10

reverse()

Reverses the element of an array

Syntax:

array.reverse();

Return Value:

Ouputs the length of the new array

Output:

Reversed array is : 10, 9, 8, 7

shift()

Deletes the first element from an array and outputs that element.

Syntax:

array.shift();

Return Value:

Outputs the deleted single value of the array.

Output:

Removed number is : 123

***

If you wanted to, say, record ten names, without using arrays, you’d have to do something like:

| var name1, name2, name3, name4, name5, name6, name7, name8, name9, name10; |

And this is only for declaring the variables! Here’s how messy it would be if you actually have to store user input using this method:

| for (var counter = 1; counter <= 10; counter++){    if(counter == 1)    {        name1 = prompt('Please enter name 1: ');    }    if(counter == 2)    {        name2 = prompt('Please enter name 2: ');    }    if(counter == 3)    {        name3 = prompt('Please enter name 3: ');    }    if(counter == 4)    {        name4 = prompt('Please enter name 4: ');    }    if(counter == 5)    {        name5 = prompt('Please enter name 5: ');    }    if(counter == 6)    {        name6 = prompt('Please enter name 6: ');    }    if(counter == 7)    {        name7 = prompt('Please enter name 7: ');    }    if(counter == 8)    {        name8 = prompt('Please enter name 8: ');    }    if(counter == 9)    {        name9 = prompt('Please enter name 9: ');    }    if(counter == 10)    {        name10 = prompt('Please enter name 10: ');    }} |

Now imagine if social media sites used this method to register the users; programmers would have to keep recoding the site in order to accommodate more users! Fortunately, we have arrays to help us.

Arrays, in a nutshell, can store lists of data that could even have different data types. The data stored have fixed positions, so you’re sure of where each data is placed and can therefore retrieve them reliably. Here are examples of array declarations:

| var strings = ["apple","grapes","tomatoes"];var numbers = [1, 2, 3, 4, 5];var stringsAndNumbers = ["Oceans", 11]; |

As you may have noticed, the declaration statements for arrays are pretty similar to the declaration statements for regular variables; the only difference is that the data are enclosed in braces and separated by commas. If you want to create an empty array, you can leave the braces blank and add a couple of items later using the push() function, for instance:

| var numbers = [];for (var counter = 1; counter <= 10; counter++){    numbers.push(counter);} |

Now we can go back to our previous attempt at getting ten names! Let’s see how using arrays drastically improves our code:

| var names = [];for (var counter = 1; counter <= 10; counter++){    names.push(prompt('Please enter name ' + counter + ':'));    console.log('Obtained name ' + counter);} |

Our code just became much more efficient and much better to look at! Congratulations! 

So far, you’ve learned how to declare arrays and put stuff in them, but how exactly can we access what’s inside them? Well, the position of the items we place inside the array stay in the same spot, so we only need to know what the name of the array is and the numerical position of the item we’ve stored.

One small caveat though: in programming, we always start counting from 0, so if you have 10 items in an array, your first item will be in the 0th place while your last item will be in the 9th place. That being said, if you want to access the names you’ve just collected, simply do something like:

| console.log(names[0]); //for the 1st nameconsole.log(names[9]); //for the 10th name |

Sometimes, when you just keep adding stuff to an array, you may lose track of how big it is. Fortunately we can just use the '.length' keyword we normally add to strings in order to count the number of characters. For instance, if we were to count the number of names stored in our variable 'names', we’d need to just append .length to 'names:

| names.length |

Great job! You’ve now learned how to create arrays and how to put stuff inside them. As an exercise, create a for-loop that prints out every name from the 'names' array into the console. Hint: the 'counter' variable comes in handy when keeping track of the index of the array.

Prototypal inheritance
In programming, we mostly want to take something and extend it.
For example, we have a user object with its functionality and methods, and we want to make the administrator and the foreigner slightly modified. We want to reuse what our users have, not copy / complete its methods, just build a new object on it.
The inheritance of prototypes is a characteristic of the language that contributes to it.

Prototype
Objects in JavaScript have a special hidden property [[Prototype]] (as defined in the definition) which is either null or refers to another object.

Chapter 6: Higher-order Functions

Transforming with map; strings and character codes.

A large program takes time to develop and produces a lot of space for bugs to hide, which in turn makes them hard to find. Here are examples of two large programs:

The first is self-contained, and the statement is six lines long.

let total = 0, count = 1;

while (count <= 10) {

total += count;

count += 1;

}

console.log(total);

The second depends on two external functions, and the statement is one line long.

console.log(sum(range(1, 10)));

Abstraction

When it comes to JavaScript programming language, vocabulary’s use the term abstraction. Abstraction is used to hide details and gives the user the capability to talk about problems on a higher level. Let us differentiate two recipes for pea soup. First:

Per person, place 1 cup of dried peas within a container. Put enough water to cover the peas, let it soak for about 12 hours. Remove it from the water and place it in a pot used for cooking with the addition of water four cups of water (4 cups). Let it boil for about two hours, per-person hold half of an onion, slice it using a knife, and pour it into the peas, let it prepare for 10 minutes.

Then the second recipe

Per person:  Half an onion, a stalk of celery, 1 cup dried split peas, and a carrot.

Dip the peas into the water for about 12 hours. Boil it for about 2 hours in water (4 cups), attach and slice vegetables. Cook it for 10 minutes.

The computer performs tasks one by one, from blind to high-level concepts.

Abstracting repetition

Plain functions are used to create abstractions. It is habitual for a program to repeat a particular function a specified amount of time. you can achieve that with a loop like this:

83

for (let i = 0; i < 10; i++) {

console.log(i);

}

function repeat(n, action) {

for (let I = 0; I < n; I++) {

action(i);

}

}

repeat(3, console.log);

// → 0

// → 1

// → 2

Sometimes you do not need to roll in a predefined function to repeat in a loop, create a function value as an alternative:

let labels = [];

repeat(5, i => {

labels.push(`Unit ${i + 1}`);

});

console.log(labels);

// → ["Unit 1", "Unit 2", "Unit 3", "Unit 4", "Unit 5"]

This method layout looks similar to a loop; it defines the type of loop and then produce a body. Although the body is written in function enclosed in parentheses of the call to repeat.

Higher-order functions

Higher-order functions are functions that work on other functions whether by arguments or by sending them back. This type of function enables user to abstract over actions. For instance, you have a function that can produce functions

function greaterThan(n) {

return m => m > n;

}

let greaterThan10 = greaterThan(10);

console.log(greaterThan10(11));

// → true

Transforming with map

The map method changes an array by setting a function to each and every of its elements and creating a new array from the returned values. The new array consists of the same length with the input array but will map out its content to a renewed for by the function.

Summarizing with reduce

When you add up numbers, begin with zero and add the foreach element to the sum. The parameter to reduce are map function combination and begin a value. This function is much easier to understand than the filter and map.

You can use the high-order functions when you want to compose operations. For instance, here is a line of code that searches for the average year for living and dead in humans’ scripts in the data set.

The block of code displays that the death script is older than the living ones.

Let’s begin with the entire script, filter out the dead (or living), eradicate their years, average them and complete the result. You can as well write these calculations as a big loop:

Our two examples are not identical, the first creates new arrays when administering the map and filter while the second calculate numbers only.

Strings and character codes

One of the significant use of data set is to find out what script a block of text is using. Below is a program that performs that task.

Another high-order function is the same method. This method gets a test function and determine if that function sends back true for any component in the array.

There are some operations on JavaScript strings like securing their length using the length property and evaluating their contents through the square brackets.

JavaScript’s charCodeAt method offers a full Unicode character. This method is used to take characters from a string. Although the argument sent to codePointAt remains an index into the succession of code units. If you use the codePointAt to loop across a string, it produces real characters and not code units.

Recognizing text

You have the character Script function and a way to loop across characters correctly, now calculate the characters each script owns.

The countBy function anticipates a collection (a group of numbers, element or anything that you can loop over with for/of) and a function that calculates a group name for a specified element. It sends back a list of objects. Each of the objects names a group and determines the number of elements contained in the group.

The method findIndex is similar to indexOf. This method is used to search for the first value for which the stated function sends back true and returns -1 when zero elements is found.

The function calculates the characters by name through the use of characterScript to attach a name and returning back to the string "none" for characters without any script. If you want to calculate percentages, you need to determine the total amount of characters belonging to a script that the reduce method can reduce. If it finds zero characters, the function sends back the "none" string.

Summary

Having the ability to send function values to several functions is an essential aspect of JavaScript. It enables writing functions that imitate computations with “gaps” between them. The code that declares these functions can contain the gaps by giving function values. Arrays provide several important higher-order methods. Use forEach to loop across elements within an array. Use the filter method to send back a new array that has elements that convey the predicate function. Changing an array by setting each item through a function using the map. Use reduce to merge every component of an array to an individual value.

Exercises

Illustrate a JavaScript function that takes an array of numbers saved and search for the second-lowest and second highest numbers.

Solution

![Description: 00009.jpeg](images/00041.jpeg)![Description: 00010.jpeg](images/00042.jpeg)

Chapter 7: What is JavaScript cookies

Explain how to create, read and delete cookies.

What is a Cookie?

Web servers and browsers utilize HTTP to communicate. However, the HTTP protocol is stateless (i.e. it treats requests as independent transactions). That means that the system won’t remember any of the previous transactions. This can be a huge problem for commercial sites, since they need to share the user’s information across various webpages.

In most cases, cookies help websites in tracking and remembering transactions; thus, cookies can help you improve the user-friendliness and overall traffic of your website.

How Does a Cookie Work?

The web server sends information to the user’s internet browser as a cookie. If the browser accepts the cookie, the information will be converted to plaintext inside the user’s hard drive. Once the user visits another webpage on your site, his browser will send the same cookie to the web server for data retrieval. Once data has been retrieved, your web server will know what has occurred before.

Basically, a cookie is a plaintext data record that has 5 fields (which are variable-length). These fields are:

*   Domain – This is your website’s domain name.
*   Secure – If this field is tagged as “secure,” only a secure webserver can retrieve the cookie. If it is blank, however, any webserver can access the cookie.
*   Expires – This field specifies the date at which the cookie will expire. If this field is blank, the cookie will expire as soon the user closes the web browser.
*   Path – This is the path to the webpage or directory that created the cookie. If you want to retrieve cookies from any page or directory, you may leave this field empty.
*   Name=Value – Each cookie is set and retrieved as key-value pairs.

Cookies were created for CGI (i.e. Common Gateway Interface) programming. The information stored in a cookie is transmitted automatically between the webserver and the user’s web browser. That means CGI scripts written on the webserver can read and edit cookie information stored on the user’s hard drive.

JavaScript allows you to manage cookies using the Document object’s cookie property. The JavaScript language can create, read, alter, and delete cookies that are applied on the active webpage.

How to Create a Cookie?

The easiest way to generate a cookie is to place a string value to the object named document.cookie. The syntax that you should use is:

![Description: 00039.jpeg](images/00043.jpeg)

In this syntax, expires is completely optional. If you’ll enter a valid time or date on this field, the cookie will expire on that particular time or date. You won’t be able to access the values stored in an expired cookie.

Important Note: You can’t save whitespaces, commas, or semicolons into a cookie. Thus, you have to encode those characters using the escape() function before saving them onto a cookie. If you’ll encode characters this way, you should also use unescape() to allow the system to read the value you stored.

How to Read a Cookie

You can read cookies easily. This is because the cookie is the value stored on the object named “document.cookie”. That means you can use that string to access the cookie whenever you want. Basically, document.cookie contains a set of name=value pairs that are separated by semicolons. Here, name is the cookie’s name and value is the cookie’s string value.

How to Set a Cookie’s Expiry Date

In some cases, you have to extend the cookie’s life beyond the current browsing session. By doing so, you can complete long processes without having to reenter any piece of information. JavaScript allows you to set your preferred expiration date and save that information inside the cookie itself. You can accomplish this by customizing the cookie’s “expires” attribute.

The image below shows you how to set a cookie’s expiration date. It extends the current expiry date by one month.

![Description: 00040.jpeg](images/00044.jpeg)

How to Delete a Cookie

In most cases, you must delete cookies after using them. This ensures that the webserver won’t get any information from the unnecessary cookie. Deleting a cookie is easy and simple. You just have to set the expiration date to a time in the past.

CONCLUSION

Thank you for making it through the end of JavaScript. Let’s hope that it was informative and able to provide you with all of the tools you need to achieve your goals whatever they may be.

The next step is to use this knowledge. Get out there and start working with some JavaScript frameworks. The way to reinforce all that you’ve learned is by doing it. You won’t be familiar with all of them, and sometimes you’re even going to be left really confused, but if you keep pushing through, then I guarantee that it will be worth it and you’ll come out the other end as a fantastic web developer.

A lot of people believe that the only way to learn proper programming is by going back to school or other education centers. But l doesn’t believe it’s true. Thanks to the tremendous advancements in online communication, you can easily learn and master any new skill through internet tutorials and videos. The information available out there for you to grasp is endless.

JavaScript is not a program that is only for geniuses and geeks. This is a very standardized language and it can easily be picked up by anyone. Just like languages in real life, this language will also help you to open unlimited possibilities and opportunities.

At this point, you might be wondering, what exactly is the future of JavaScript? What can I expect to gain from learning all these?

Since the whitepaper that brought Ajax to the forefront, JavaScript has only been gaining steam constantly. There are a huge number of new JavaScript frameworks that are being introduced every year that are fantastic for their various different purposes, and more frameworks will be expected.

The future of JavaScript is more about the future of you. JavaScript is only going to become more popular if further features are added into the future ECMA standardizations, if the web in general is used by more people, and if web platforms mature. Likewise, JavaScript matures alongside PHP and CSS. It is expected that JavaScript will continue to develop in the future.

If you want to be a web developer, you must learn JavaScript and be aware of its frameworks, because those will allow you to keep up with the trends.

As technology grows more and more advanced, JavaScript programmers will also be more in demand. There are a number of things right now that are currently relegated to other common scripting languages, like Python, that can be ported to JavaScript. Natural language processing and machine translation are just two examples that will inevitably be ported to JavaScript which therefore increases demand.

JavaScript isn’t just for creating pretty web pages; the actual utility of web pages is expanding. With this in mind, JavaScript will advance to this because web pages are now able to perform very complicated actions. The advent of browser-based HTML/CSS/JavaScript games only goes to support this.

As a JavaScript programmer, expect that more programmers will be needed in the industry. Therefore, one of the best things that you can do for yourself is to learn JavaScript and advance your learning.
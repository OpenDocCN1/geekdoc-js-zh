![](images/cover.jpg)

![image](images/cover.jpg)

# Modern Web
Development with
Deno

![](images/line.jpg)

# *Develop Modern JavaScript and TypeScript
Code with Svelte, React, and GraphQL*

![](images/line.jpg)

# Mayur Borse

![](images/logo.jpg)

[www.bpbonline.com](http://www.bpbonline.com)

Copyright © 2023 BPB Online

*All rights reserved.* No part of this book may be reproduced, stored in a retrieval system, or transmitted in any form or by any means, without the prior written permission of the publisher, except in the case of brief quotations embedded in critical articles or reviews.

Every effort has been made in the preparation of this book to ensure the accuracy of the information presented. However, the information contained in this book is sold without warranty, either express or implied. Neither the author, nor BPB Online or its dealers and distributors, will be held liable for any damages caused or alleged to have been caused directly or indirectly by this book.

BPB Online has endeavored to provide trademark information about all of the companies and products mentioned in this book by the appropriate use of capitals. However, BPB Online cannot guarantee the accuracy of this information.

**Group Product Manager:** Marianne Conor

**Publishing Product Manager:** Eva Brawn

**Senior Editor:** Connell

**Content Development Editor:** Melissa Monroe

**Technical Editor:** Anne Stokes

**Copy Editor:** Joe Austin

**Language Support Editor:** Justin Baldwin

**Project Coordinator:** Tyler Horan

**Proofreader:** Khloe Styles

**Indexer:** V. Krishnamurthy

**Production Designer:** Malcolm D'Souza

**Marketing Coordinator:** Kristen Kramer

**First published:** 2023

Published by BPB Online

WeWork, 119 Marylebone Road

London NW1 5PU

**UK | UAE | INDIA | SINGAPORE**

ISBN 978-93-55510-969

**[www.bpbonline.com](http://www.bpbonline.com)**

# Dedicated to

*"To all the Developers in the world"*

# About the Author

**Mayur** is a Dynamic and Result Oriented professional with a passion for Software Engineering and Perfection. Currently, working as a Full Stack Software Engineer on various projects utilising Gatsby.js, Nikola, HTML,CSS, Bootstrap, Javascript and so on. Mayur has also used various design patterns such as CRUD, SearchBar, CSVDownloader, Loader for UI creation of a network device and written blogs on each of them. He has done Bachelors of Electronic Engineering from University of Pune, along with a Diploma in Electronics and Telecommunications. Apart from this, he posseses 60+ certifications on Pluralsight, which includes course subjects such as React, React Native, GraphQL, Python, Django, Javascript, etc. He is also passionate about philosophy and spirituality.

# About the Reviewer

**Chad Elofson** is a Software Analyst using Node and Deno-based technologies. He works at Thompson Rivers University as a Software Analyst. He started his IT career 19 years ago as Network Administrator. For the past eight years, he has moved to Software Engineering focused on JavaScript runtime-based technologies.

# Acknowledgement

I’m grateful to the team at BPB Publications for giving me the opportunity to write the book.

# Preface

This book introduces developers to the new JavaScript runtime named Deno. It also shows how to create web applications on the front-end and the back-end with TypeScript using Deno.js.

This book takes a practical approach for web developers or JavaScript. It covers a few realtime examples as well.

This book is divided into **9 chapters**. They will cover Introduction to Deno, Introduction to TypeScript, Create Web Applications with React, Introduction to GraphQL, Creating GraphQL API server, Creating Svelte Application etc. The details are listed below.

**[Chapter 1](#c01.xhtml)** will cover what Deno is, why Deno was introduced by the creator of Node.js (popular JavaScript runtime), what are the differences between Deno and Node etc. Will list features of Deno. Will explain different technologies used in creating Deno. It will also provide information about What is JavaScript runtime and What is JavaScript engine.

**[Chapter 2](#c02.xhtml)** will cover What is TypeScript, benefits of TypeScript, features of TypeScript etc. It will also explain the basics of TypeScript for the JavaScript developers. It will also provide details about how to set up TypeScript.

**[Chapter 3](#c03.xhtml)** will provide details on how to install Deno. It will also list some of the widely used developer tools like VS Code, Terminal etc. necessary for development.

**[Chapter 4](#c04.xhtml)** will cover details about the Deno Ecosystem. Deno ecosystem includes Deno CLI details like Environment variables, subcommands, how to pass arguments, File watcher, Permission flags, Permission allow-list etc. It will also list Deno runtime APIs like Web APIs, Global APIs etc. Deno modules which are an essential part of the ecosystem are listed as two categories Standard library and Third-party modules. Also, Module registries like Deno’s own site deno.land/x and nest.land will also be listed.

**[Chapter 5](#c05.xhtml)** will introduce Aleph.js, A Full-stack React framework for Deno. It will list the concepts like pages, routing etc. in brief. It will create a Todos App API using provided API like GET, POST, DELETE etc. This will be helpful for the developer to get familiar with the concepts utilized in the next chapter.

**[Chapter 6](#c06.xhtml)** will continue the Todos app development and will cover UI implementation. It will provide details on how to use the Styled component library to create React components with CSS styling. It will provide code to create basic components like Button, Input etc. and will utilize them in the app along with TodoList and TodoDetails components.

**[Chapter 7](#c07.xhtml)** will introduce GraphQL and will provide details about features like precise fetching, Single API Endpoint etc. It will also list some of the core concepts like Type, Input, Mutation, Resolver etc. It will then introduce oak module along with oak-graphql which will be used to implement GraphQL Server in the next chapter.

**[Chapter 8](#c08.xhtml)** will cover implementation of GraphQL server using oak, oak-graphql for creating Phonebook app. It will provide details on how to create a git repo, will use trex as package manager and velociraptor as script runner. It will also provide the code for server setup, Schema, Resolvers. Database setup using ORM and authentication etc.

**[Chapter 9](#c09.xhtml)** will introduce the promising JavaScript framework or compiler Svelte. Snel is a module for creating Svelte applications using Deno. It will cover the setup process for Snel and snel-carbon (UI component module). It will then provide code for setting up public private routes for the app along with Svelte components.

# Coloured Images

Please follow the link to download the
***Coloured Images*** of the book:

# [https://rebrand.ly/nbyzlk9](https://rebrand.ly/nbyzlk9)

We have code bundles from our rich catalogue of books and videos available at **[https://github.com/bpbpublications](https://github.com/bpbpublications)**. Check them out!

# Errata

We take immense pride in our work at BPB Publications and follow best practices to ensure the accuracy of our content to provide with an indulging reading experience to our subscribers. Our readers are our mirrors, and we use their inputs to reflect and improve upon human errors, if any, that may have occurred during the publishing processes involved. To let us maintain the quality and help us reach out to any readers who might be having difficulties due to any unforeseen errors, please write to us at :

**[errata@bpbonline.com](mailto:errata@bpbonline.com)**

Your support, suggestions and feedbacks are highly appreciated by the BPB Publications’ Family.

Did you know that BPB offers eBook versions of every book published, with PDF and ePub files available? You can upgrade to the eBook version at **[www.bpbonline.com](http://www.bpbonline.com)** and as a print book customer, you are entitled to a discount on the eBook copy. Get in touch with us at: **[business@bpbonline.com](mailto:business@bpbonline.com)** for more details.

At **[www.bpbonline.com](http://www.bpbonline.com)**, you can also read a collection of free technical articles, sign up for a range of free newsletters, and receive exclusive discounts and offers on BPB books and eBooks.

# Piracy

If you come across any illegal copies of our works in any form on the internet, we would be grateful if you would provide us with the location address or website name. Please contact us at [**business@bpbonline.com**](mailto:business@bpbonline.com) with a link to the material.

# If you are interested in becoming an author

If there is a topic that you have expertise in, and you are interested in either writing or contributing to a book, please visit [**www.bpbonline.com**.](http://www.bpbonline.com/) We have worked with thousands of developers and tech professionals, just like you, to help them share their insights with the global tech community. You can make a general application, apply for a specific hot topic that we are recruiting an author for, or submit your own idea.

# Reviews

Please leave a review. Once you have read and used this book, why not leave a review on the site that you purchased it from? Potential readers can then see and use your unbiased opinion to make purchase decisions. We at BPB can understand what you think about our products, and our authors can see your feedback on their book. Thank you!

For more information about BPB, please visit [**www.bpbonline.com**.](http://www.bpbonline.com/)

# [CHAPTER 1](#toc.xhtml_c01)

# [The Deno Land](#toc.xhtml_c01)

# [Introduction](#toc.xhtml_s1a)

After a decade of success of **Node** runtime, its creator *Ryan Dahl* has come up with another exciting technology called **Deno**, which is also a runtime like Node but is more secure and provides many improvements and modern features in comparison to Node. Dahl stormed the development world by announcing **Deno** during a *JSCONF EU* talk in 2018 named *10 things I Regret about Node.js* (**https://www.youtube.com/watch?v=M3BM9TB-8yA**). Since then, Deno has been a topic of excitement in the software industry.

# [Structure](#toc.xhtml_s2a)

In this chapter, we will cover the following topics:

*   Introducing Deno
    *   The Node revolution
*   Comparison of Deno and Node
*   Deno features
*   Deno foundation stack
*   What is a JavaScript engine?
*   What is a JavaScript runtime?

# [Objectives](#toc.xhtml_s3a)

After studying this chapter, you will be familiar with the main features of Deno and its internal architecture. You will also be able to understand the reasons for the creation of Deno, the role of Node in the creation of Deno, the similarities and differences between Deno and Node, and the stack used for creating Deno, that is, Chrome V8 Engine by Google, Rust by Mozilla, and Tokio.

You will also be familiar with how the JavaScript engine works and how the JavaScript runtime works.

# [Introducing Deno](#toc.xhtml_s4a)

Deno is a secure and modern JavaScript runtime that uses the V8 engine for JavaScript code conversion, Tokio (written in Rust) for async event handling and the API backend written in Rust. It provides features as follows:

*   Integrated security. Access to the network, file, and environment is provided only through flags.
*   Built-in tools such as formatter, test-runner, debugger, linter, and so on.
*   Typescript support out of the box.
*   Top-level await (without async).
*   ES Modules import (default).
*   No package manager is required as module imports are done using URLs.

Deno is the creation of *Ryan Dahl*. Interestingly, Dahl is also the creator of Node, which is also a runtime. In fact, Deno was created to overcome the limitations of Node and provide modern features out of the box, which is not part of Node runtime. Hence, the journey of Deno begins with Node, which changed the way JavaScript was perceived and used in the industry. It is a fact that JavaScript has become a widely used and revered language after the entry of Node. Many developers are using only JavaScript for their entire stack, thanks to Node. Therefore, to understand “*The Deno Evolution*”, one must begin with “*The Node Revolution*”.

# [The Node Revolution](#toc.xhtml_s5a)

A decade ago, JavaScript was mocked as a funny and peculiar language useful mostly for front-end Web development. The scope of JavaScript was very limited compared to mainstream languages like C++ or Java, as it was mainly useful for browser-based applications only.

In 2009, *Ryan Dahl* introduced Node.js to the world. **Node** is a JavaScript runtime written in C++ which uses V8 Engine by Google (launched in 2008) and **libuv** event loop to perform asynchronous operations in the background. Since its release, Node.js has revolutionized JavaScript usability and is being used by several tech giants such as PayPal, LinkedIn, Netflix, and Uber to name a few. Let us see the features that led to the rise of Node.

# JavaScript everywhere

Node has been the reason that made JavaScript available outside the browser. Nowadays, JavaScript is used for development across many domains. **Electron.js** is used for cross-platform desktop apps, **React.js** for Web development, and **React Native** for mobile development. Many companies and developers use JavaScript alone for their entire stack as the code logic can be moved from client to server because both are using the same language.

# Asynchronous and event-driven architecture

Node is single-threaded, meaning it contains only one call stack that executes only one program at a time. It has event-driven architecture. This means executions in Node are done according to some event occurrence. Node uses an event loop **libuv** to handle executions asynchronously, i.e., in a non-blocking way.

# Open-source and cross-platform

Node is open source which is one of the major factors for its popularity and acceptance amongst the developers.

Cross-platform support is also an amazing feature node offers to developers. It works on OSX, Linux and Windows very well. Using this benefit, a developer can write node code on OSX and can use Linux to deploy.

# Very performant

Node uses V8 JavaScript Engine under the hood. The V8 engine is very fast, and this makes the Node a very high-performing runtime. Performance is one of the major feature node offers.

# A node package manager (npm) for handling dependencies

Node package manager **`npm`** is used to install packages and manage package dependencies. It is also a centralized registry where users can publish their node packages.

# [Event loop](#toc.xhtml_s6a)

Node uses **libuv** event loop for performing async i/o operations. The event loop uses workers and a thread pool for performing operations in the background. It also checks if the call stack is empty and the main programme has been executed so it can push the code from the callback queue to the empty call stack. The JavaScript runtime process is available in visualization here (**[http://latentflip.com/loupe/](http://latentflip.com/loupe/)**). We will check the JavaScript runtime architecture in detail later in this chapter.

Along with such great features, Node has several shortcomings, which led its creator *Ryan Dahl* to start a new project (Deno). In the next section, we will compare Deno with Node and see how Deno overcomes Node’s shortcomings.

# [Deno comparison with Node](#toc.xhtml_s7a)

Deno was created to address the shortcomings of Node. So, it would be evident that both of them will have many similarities and differences. Let us check each of these.

| **Feature** | **Node** | **Deno** |
| Built using | C++ | Rust |
| JavaScript Engine | V8 (C++ bindings and backend) | V8 (Rust bindings and backend) |
| Event loop | libuv | tokio |
| TypeScript support | Need to be installed | Out of the box |
| Package manager | Npm (centralized) | no package manager (decentralized) |
| Import system | CommonJS (require()) | ES modules (import) |
| Security | Full access by default | No access by default |
| package.json | Used | Not used |

# [Deno features](#toc.xhtml_s8a)

Deno has excellent support for modern features and includes many features not available in Node out of the box (TypeScript support). Let us have a look at some of its main features.

*   External dependencies are loaded using URLs
*   Code execution in Sandbox
    *   Runtime has no access to network file systems and environments
    *   Access needs to be granted explicitly
*   Typescript support out of the box
*   Top-level await
*   Standard modules library
*   Built-in tools provided like:
    *   **Bundler**: Builds scripts and dependencies into a single file
    *   **Dependency inspector**: Inspects ES modules and lists all their dependencies
    *   **Documents generator:** Parses JSDoc
    *   **Formatter**: For auto-formatting JS and TS Files
    *   **Test-runner**: For testing using the assertions module from the standard library
    *   **Linter**: To catch code issues

# [Deno foundation stack](#toc.xhtml_s9a)

Deno has been created using some solid technologies, which increase its chances of becoming highly successful. Once we have gone through the stack used for creating Deno, we can be assured about Deno’s future (a very bright one). Let us check the tech stack used by Deno.

*   Uses Google’s V8 Engine
*   Written in Rust
*   Tokio (async runtime written in Rust) used for event thread management

# [The V8 Engine by Google](#toc.xhtml_s10a)

An open-source JavaScript engine built using C++ by Google. It converts JavaScript code (passed by Deno) into bytecode/machine code. Deno supports Typescript out of the box, so we can also provide Typescript code which gets compiled to JavaScript by Deno. It executes the JavaScript code and passes Deno API-related code (Rust code) to the Rust backend via “*rusty_v8*” bindings written in Rust for the V8 engine by the Deno team.

The combination of an interpreter (Ignition) and compiler (TurboFan) makes V8 produce optimized machine code which runs really fast.

# [Rust](#toc.xhtml_s11a)

Rust has been the “*most loved*” language in every StackOverflow survey since 2016 (five years in a row). It is a systems programming language that enables control over low-level details. It provides memory-safety, thread-safety, and type systems. For these and many other features, Rust remains the most loved and wanted language for the last five years in StackOverflow surveys.

*   Memory safe by default
*   Ownership and borrowing support
*   Performance is very close to other low-level languages (C, C++)
*   Either one mutable or many immutable references
*   No NULL pointers, only options

Used by:

*   Amazon—firecracker
*   Google—Fuchsia
*   Facebook—Mononoke
*   Microsoft—IoT Edge

The Deno backend contains a file system, network and environment access and is written in Rust. The asynchronous i/o bindings are handled by tokio library.

# [Tokio I/O library](#toc.xhtml_s12a)

It is used to write asynchronous applications with Rust. It is an event-driven, non-blocking i/o platform. It uses thread pools and workers to perform the operations in the background.

Whenever a code related to i/o, network, and so on is passed to the V8 engine, it forwards it to Rust backend using “*rusty_v8*” bindings. The execution of the received code is done by tokio using workers.

*   Asynchronous I/O ops using non-blocking event
*   Uses Mio as an event queue
*   The event loop mechanism is used to monitor the call stack and callback queue
*   Thread pool and workers are used to perform the tasks in the background

# [What is a JavaScript engine](#toc.xhtml_s13a)

JavaScript engine is used to convert JavaScript/Typescript code into bytecode (interpreter) or optimized machine code (compiler) so the computer can execute it.

There are many JavaScript engines released since release.

*   V8 Engine by Google
*   SpiderMonkey by Mozilla
*   Chakra by Microsoft

In the JavaScript engine, the code is parsed into tokens, which are used to generate the Abstract Syntax Tree. The interpreter uses this tree to generate Byte Code. A profiler monitors the byte code and passes it to the compiler if there is a scope for optimization. Compiler outputs optimized machine code which performs faster than the byte code.

**Interpreter:**

An interpreter translates the code one line at a time. It provides a ByteCode as output. The interpreter is very fast to get started coding but does not provide any optimizations.

**Compiler:**

The compiler translates the entire code at once. The compiler has a scope to analyze the entire program and optimize it. It outputs optimized machine code. The compiler takes longer to analyze and optimize the code as it goes through the entire program.

JavaScript engine combines the functionality of interpreter and compiler. This way, we get an optimized code that runs faster. Such a compiler is called the “*JIT Compiler*”. A Profiler is used to monitor the byte code and pass it to the compiler (TurboFan) if there is any scope for optimization.

![](images/Figure-1.1.jpg)

**Figure 1.1:** V8 JavaScript engine

# [What is a JavaScript runtime](#toc.xhtml_s14a)

JavaScript runtime is an environment that combines the JavaScript Engine (V8 in Deno runtime), The API backend written in some low-level language (Rust in Deno runtime), a callback queue and an event loop that continuously monitors the call stack and the callback queue.

![](images/Figure-1.2.jpg)

**Figure 1.2:** Deno architecture

**Memory heap:**

JavaScript code is passed to the V8 engine that stores the variables and functions from the code in the Memory Heap.

**Call Stack:**

It stores the functions invoked within the code. It operates on the **Last In First Out** (**LIFO**) principle. It always points to the currently running function. Once the function returns or is passed to Deno API, it pops the function out and executes the earlier one on the stack.

**Deno API**

Whenever Deno detects code related to i/o, network, environment, and so on, it passes the code to the API backend, which is written in Rust. It uses “*rusty_v8*” bindings to pass the code to the backend.

**Tokio:**

It is an event-driven, asynchronous i/o platform. Deno API passes the code to tokio.

This uses thread pool and workers to execute the operations in the background and passes them on the callback queue.

**Callback Queue:**

It operates on the **First In First Out** (**FIFO**) principle. It stores all the completed functions passed by Tokio. It “*waits*” till the call stack is empty.

**Event loop:**

It monitors the call stack and the callback queue continuously. If the call stack is empty and the callback queue has a function in the queue, it passes the function on the call stack where it gets executed.

# [Conclusion](#toc.xhtml_s15a)

Our journey in the Deno land has begun with this chapter. We learnt the history of Deno and Node, compared Deno with Node and listed Deno features. We also covered the stack Deno is built from, i.e., *V8* JavaScript engine, *Tokio* event-loop, and Deno API backend written in Rust. Finally, we covered the JavaScript engine and the JavaScript runtime architectures, which are not mandatory but give us a solid foundation to understand what is Deno and how it performs the operations in the background.

While this chapter covered the Major Deno features, TypeScript is one important section in Deno land that needs to be covered. TypeScript support out of the box is a major Deno feature, and learning TypeScript requires an entire dedicated chapter to cover the basics. Hence, we will learn *TypeScript* in the upcoming chapter, as we will be using *TypeScript* for programming throughout this book.

As you have reached this point, it is evident that you are interested and excited to learn Deno. Deno has many exciting and modern features, which we will learn throughout this book.

# [CHAPTER 2](#toc.xhtml_c02)

# [Introduction to TypeScript](#toc.xhtml_c02)

# [Introduction](#toc.xhtml_s16a)

TypeScript support out of the box is an exciting feature offered by Deno runtime. TypeScript has been a popular choice for large-scale applications and is being adopted rapidly in the industry. It ranked second in the Most Loved Languages (**[https://insights.stackoverflow.com/survey/2020#most-loved-dreaded-and-wanted](https://insights.stackoverflow.com/survey/2020#most-loved-dreaded-and-wanted)**) section of the Stack Overflow Developer Survey 2020 (**[https://insights.stackoverflow.com/survey/2020](https://insights.stackoverflow.com/survey/2020)**).

# [Structure](#toc.xhtml_s17a)

In this chapter, we will cover the following topics:

*   Introducing TypeScript
*   TypeScript benefits
*   TypeScript features
*   TypeScript basics
    *   Basic types
    *   Interfaces
    *   Type aliases
    *   Interfaces versus Type aliases
    *   Type inferences
    *   Type assertions
    *   Unions
    *   Intersections
    *   Classes
*   Dynamic versus static typing
*   Strongly versus weakly typing
*   TypeScript setup

# [Objectives](#toc.xhtml_s18a)

This chapter should help you become familiar with TypeScript fundamentals and the use of TypeScript for programming Deno applications. This chapter should also help you understand the pros and cons of static type checking and the benefits provided by TypeScript.

# [Introducing TypeScript](#toc.xhtml_s19a)

Announced publicly by *Anders Hejlsberg* in 2012, TypeScript is a very popular and open-source superset of JavaScript. It adds static type definitions to JavaScript code. It was developed and maintained by Microsoft. TypeScript provides type safety, type inference, type assertions, and many more features, including ES Next features to JavaScript. Please take a look at the following screenshot:

![](images/Figure-2.1.jpg)

**Figure 2.1:** TypeScript

# [TypeScript benefits](#toc.xhtml_s20a)

JavaScript is very popular and widely used in our industry. But while using JavaScript for large-scale applications, its dynamic nature lets many type-related errors and bugs pass through in the development phase and are caught only during runtime. Runtime debugging is more awful compared to compile-time debugging.

Statically typed languages caught errors and bugs during compilation, even before running the code. TypeScript helps us write and maintain large-scale applications by providing type safety during the development cycle. TypeScript catches type-related or other errors during compile time, saving a lot of our precious time.

TypeScript was introduced to add types to JavaScript. TypeScript code gets transformed into Javascript by TypeScript compiler or babel transpiler. TypeScript enables *static type checking*, which detects errors in the code without running it, that is, in compile time. It preserves the runtime behavior of JavaScript, meaning the code will run the same way. Keeping the same runtime behavior is one of the core features of TypeScript.

# [TypeScript features](#toc.xhtml_s21a)

TypeScript provides many es-next features out of the box, along with features helpful for developing large-scale applications. We will list some of the major features of TypeScript.

*   Detects errors in compile-time, without running the code
*   IDE can use type definitions for auto-completion
*   Static type system support for JavaScript code
*   Less prone to errors due to static type checking
*   ES-Next Features support out of the box
*   Tooling
*   Type safety
*   Type inference
*   Type assertions
*   Generics
*   Interfaces and type aliases
*   Language services
*   Same runtime behavior as that of JavaScript

# [Basics of TypeScript](#toc.xhtml_s22a)

Being a superset of JavaScript, TypeScript is easy to grasp for a JavaScript developer. Assuming you are familiar with JavaScript, we will learn the additional types included in TypeScript.

# [Basic types](#toc.xhtml_s23a)

We are covering the commonly used data types in this section. We will be using them for the majority of the time during Deno’s development.

*   **Boolean**: Accepts either *true* or *false* value.
*   **Number**: Accepts either floating point values (for example, 10.34) or integer values (for example, 39).
*   **String:** Accepts texts and characters, including *template string.*
*   **Array:** Array of mentioned element type declared in two ways:
    *   [] symbol:
        1.  **`const shoppingList: string[] = [“milk”, “vegetables”];`**
    *   Generics:
        1.  **`const shoppingList: Array<string> = [“milk”, “vegetables”];`**
*   **Tuple**: An array with a fixed number of elements of either similar or different types. Tuple can be defined as:
    1.  **`const deviceStage: [number, string] = [0, “OFF”];`**
*   **Enum:** Maps string values to a set of numeric values.
    1.  **`enum State {`**
    2.  **`OFF,`**
    3.  **`ON,`**
    4.  **`}`**
    5.  **`console.log(State.OFF, State[0]); // 0, OFF`**
*   **Unknown:** Accepts all types. This type of value is only assignable to either **unknown** or **any** type.
*   **Any:** It also accepts all types of values like unknown, but it is more permissible than an unknown type. It lets us skip type checking for the variable.
*   **Null:** Accepts null value.
*   **Undefined:** Accepts undefined value.
*   **Never:** Used as a return type of function that never returns.
*   **Void:** Used as a return type of function that does not return any value.
*   **Object:** Represents non-primitive types.

# [Interfaces](#toc.xhtml_s24a)

Interfaces are used to define the shape of an entity or an object. It describes the properties an object should have.

1.  `interface IPerson {`
2.  `  firstName: string;`
3.  `  lastName: string;`
4.  `}`

6.  `const person: IPerson = {`
7.  `  firstName: “first”,`
8.  `  lastName: “last”`
9.  `};`

In the preceding example, **`IPerson`** is an interface (notice the capital I for interface) that defines a shape that the object **`person`** must have. Hence, the property **`place`** will cause a compiler error as it does not exist in the interface **`IPerson`**.

# [Optional properties](#toc.xhtml_s25a)

In many cases, we need to provide a field that can be optional. In an interface, “?” symbol can be used to make the field optional.

1.  `interface IPerson {`
2.  `  name: string;`
3.  `  age?: number; // age is optional`
4.  `}`

6.  `let printProfile = (person: IPerson): void => {`
7.  `  console.log(person.name);`
8.  `};`

10.  `const person = { name: “name1” };`
11.  `printProfile(person);`

# [Read only properties](#toc.xhtml_s26a)

A **`readonly`** keyword before the property indicates we want a property to be immutable after creation.

1.  `interface IPerson {`
2.  `  name: string;`
3.  `  readonly age: number; // age is read-only`
4.  `}`

6.  `const person: IPerson = {`
7.  `  name: “me”,`
8.  `  age: 29,`
9.  `};`

11.  `person.name = “you”;`
12.  `// person.age = 25; // Cannot assign to age because it is a read-only property`

# [Type aliases](#toc.xhtml_s27a)

Type aliases work in a similar way to that of interfaces. While interfaces are used to define the shape of an object, type aliases can be used to provide names for primitive types. They can also be used for union types.

1.  `type myInt = number; // type provides new name myInt for primitive type number`
2.  `let myId: myInt = 11; // Here myInt represents number type`
3.  `let id: number = 11;`

5.  `// Unions`
6.  `type unionId = number | string; // union types`
7.  `let myUnionId: unionId = 25; // number`
8.  `myUnionId = “1a2b”; // string`

10.  `// Similar functioning to interfaces`
11.  `type PersonType = {`
12.  `  firstName: string;`
13.  `  lastName: string;`
14.  `};`

16.  `const person: PersonType = {`
17.  `  firstName: “first”,`
18.  `  lastName: “last”,`
19.  `  // place: “unknown”, // Compiler error: place does not exist in the type IPerson`
20.  `};`

# [Interfaces versus type aliases](#toc.xhtml_s28a)

Interface merging is allowed in TypeScript, whereas type aliases merging will give a compile error.

1.  `interface IPerson {`
2.  `  name: string;`
3.  `}`

5.  `interface Iperson {`
6.  `  // Merges place into existing Iperson`
7.  `  place: string;`
8.  `}`

10.  `const person: Iperson = { name: “Name1”, place: “space” };`

12.  `type PersonType = {`
13.  `  name: string;`
14.  `};`

16.  `// type PersonType = {`
17.  `//   // Compiler error: Duplicate identifier ‘PersonType’`
18.  `//   place: string;`
19.  `// };`

21.  `// const person1: PersonType = { name: “name2”, place: “time” }; // place does not exist`

# [Type inference](#toc.xhtml_s29a)

There are two ways to handle type inference in TypeScript. When we provide the type *explicitly*, it is called **Explicit typing**, and when TypeScript infers the type *implicitly* using the assigned value, it is called **Implicit typing**.

*   **Explicit typing**

    Whenever we provide the type to a variable explicitly, it is called explicit typing.

    1.  `let myId: number = 25;   // Explicitly typed as number`
*   **Implicit typing**

    TypeScript infers the data type of a variable even if the type is not specified explicitly either by the initially assigned value or function parameter default value, or function return type. This is called implicit typing or type inference.

    If **`false`** is assigned to **`isAllowed`** variable without explicit annotation, TypeScript concludes the data type to be **`boolean`** using the **`false`** value.

    1.  `let isAllowed = false; // Implicitly typed`
    2.  `// TypeScript infers type boolean as the value is false`
    3.  `// let isAllowed: boolean = false;`

    5.  `// Compiler error`
    6.  `// isAllowed = 25; // TS2322 [ERROR]: Type ‘number’ is not assignable to type ‘boolean’.`

If no value is provided during the declaration, **`any`** type is inferred. This behavior can be disabled by setting **`“noImplicitAny”: true;`** flag in **`tsconfig.json`**.

1.  `let anyVar; // ‘any’ type inferred`
2.  `anyVar = 2.3;`
3.  `anyVar = false;`
4.  `anyVar = “I’m any”;`

# [Type assertions](#toc.xhtml_s30a)

Type assertions are used to override types inferred by the compiler. Type assertions can be defined in two ways:

*   **`as`** syntax
    1.  `const word: unknown = “abcdefg”;`
    2.  `// const charCount: number = word.length; // error: TS2571 [ERROR]: Object is of type ‘unknown’.`
    3.  `const charCount: number = (word as string).length;`
*   Angle bracket <> syntax
    1.  `const word: unknown = “abcdefg”;`
    2.  `// const charCount: number = word.length; // error: TS2571 [ERROR]: Object is of type ‘unknown’.`
    3.  `const charCount: number = (<string>word).length;`

# [Unions](#toc.xhtml_s31a)

In union types, a variable can hold values of two or more types. Union is denoted by the vertical bar or pipe “|” symbol.

1.  `let myNum: number = 24;`
2.  `// myNum = “id2234”; // error: TS2322 [ERROR]: Type ‘string’ is not assignable to type ‘number’.`
3.  `let myId: string | number = 25; // myId will accept either string or number.`
4.  `myId = “id2234”; // string is accepted`

6.  `// Using type`
7.  `type myIdType = string | number;`
8.  `let myId1: myIdType = 53;`
9.  `myId1 = “id1234”;`

# [Intersections](#toc.xhtml_s32a)

Intersection types are created by combining all the properties and methods of two different types. Ampersand is used to create intersection types.

1.  `interface IPerson {`
2.  `  name: string;`
3.  `  age: number;`
4.  `}`

6.  `interface IEmployee {`
7.  `  employeeId: number;`
8.  `}`

10.  `// PersonType will have all the props of IPerson & IEmployee`
11.  `type PersonType = IPerson & IEmployee;`

13.  `const printMe = (person: PersonType): PersonType => {`
14.  `  return person;`
15.  `};`

17.  `const user: PersonType = {`
18.  `  name: “name1”,`
19.  `  age: 25,`
20.  `  employeeId: 555,`
21.  `};`

23.  `const result = printMe(user);`
24.  `console.log(result);`

# [Classes](#toc.xhtml_s33a)

TypeScript allows an object-oriented programming approach with the help of classes. In **OOP** terms, class is a blueprint used to create an instance or object. In general, a class can have the following entities:

*   **`constructor()`**: Invoked whenever an instance of the class is to be created.
*   **fields:** A variable or property.
*   **method:** A function

# [Modifiers](#toc.xhtml_s34a)

Modifiers are access controllers for the fields of the class. There are three modifiers named **`public`**, **`private`**, and **`protected`**, used for fields and methods.

# public

This is the default modifier which allows access to the field/method outside class.

1.  `class Person {`
2.  `  name: string; // public`
3.  `  age: number; // public`

5.  `  // Called during instance creation`
6.  `  constructor(name: string, age: number) {`
7.  `    this.name = name;`
8.  `    this.age = age;`
9.  `  }`

11.  `  printMe() {`
12.  `    console.log(this.name, this.age); // this refers to ‘person’ instance`
13.  `  }`
14.  `}`

16.  `const person = new Person(“me”, 99); // Calls contructor,with name=”me” and age=99`
17.  `person.printMe();`
18.  `console.log(person.age); // public property is accessible outside class`

# private

It does not allow access to the field/method outside class. Even the subclasses do not have access to private properties. It is defined by either a private keyword or ECMAScript’s hash(#) modifier.

1.  `class Person {`
2.  `  name: string;`
3.  `  private _age: number;`
4.  `  #isActive: boolean; // private identifier`

6.  `  constructor(name: string, age: number, isActive: boolean = true) {`
7.  `    this.name = name;`
8.  `    this.age = age;`
9.  `    this.#isActive = isActive;`
10.  `  }`

12.  `  printMe() {`
13.  `    console.log(this.name, this.age, this.#isActive);`
14.  `  }`
15.  `}`

17.  `const person = new Person(“me”, 99);`
18.  `person.printMe();`
19.  `console.log(person.name);`

21.  `/**`
22.  `* error: TS2341 [ERROR]: Property ‘age’ is private and only accessible within class ‘Person’.`
23.  `*/`
24.  `// console.log(person.age);`

26.  `/**`
27.  `* TS18013 [ERROR]: Property ‘#isActive’ is not accessible`
28.  `* outside class ‘Person’ because it has a private identifier.`
29.  `*/`
30.  `// console.log(person.#isActive);`

# protected

It does not allow access to the field/method outside class, but the subclasses do have access to its fields.

1.  `class Person {`
2.  `  name: string;`
3.  `  protected age: number; // protected field`

5.  `  constructor(name: string = “unnamed”, age: number = 0) {`
6.  `    this.name = name;`
7.  `    this.age = age;`
8.  `  }`

10.  `  printMe() {`
11.  `    console.log(this.name, this.age);`
12.  `  }`
13.  `}`

15.  `class User extends Person {`
16.  `  userId: number;`

18.  `  constructor(userId: number, name: string, age: number) {`
19.  `    super(name, age);`
20.  `    this.userId = userId;`
21.  `  }`

23.  `  printMe() {`
24.  `    console.log(this.name);`
25.  `    console.log(this.age); // protected field age of Person class is accessible to subclasses`
26.  `  }`
27.  `}`

29.  `const user = new User(1, “me”, 99);`
30.  `user.printMe();`

32.  `/**`
33.  `* error: TS2445 [ERROR]: Property ‘age’ is protected and only accessible within`
34.  `* class ‘Person’ and its subclasses.`
35.  `*/`
36.  `// console.log(user.age);`

# [Getter and Setter](#toc.xhtml_s35a)

As we saw in the modifier section, **`private`** and **`protected`**, fields/methods are not accessible outside the class. We will need to access them in some situations. *Getters* and *Setters* will be helpful in such cases.

1.  `class Person {`
2.  `  name: string;`
3.  `  private _age: number;`
4.  `  #isActive: boolean;`

6.  `  constructor(name: string, age: number, isActive: boolean = true) {`
7.  `    this.name = name;`
8.  `    this.age = age;`
9.  `    this.#isActive = isActive;`
10.  `  }`

12.  `  printMe() {`
13.  `    console.log(this.name, this.age, this.#isActive);`
14.  `  }`

16.  `  get _age() {`
17.  `    return this.age;`
18.  `  }`

20.  `  set _age(value: number) {`
21.  `    this.age = value;`
22.  `  }`

24.  `  get Is_active() {`
25.  `    return this.#isActive;`
26.  `  }`
27.  `  set Is_active(value: boolean) {`
28.  `    this.#isActive = value;`
29.  `  }`
30.  `}`

32.  `const person = new Person(“me”, 99);`
33.  `person.printMe();`
34.  `console.log(person.name);`

36.  `/**`
37.  `* error: TS2341 [ERROR]: Property ‘age’ is private and only accessible within class ‘Person’.`
38.  `*/`
39.  `// console.log(person.age);`

41.  `console.log(person._age);`
42.  `person._age = 11;`
43.  `console.log(person._age);`

45.  `/**`
46.  `* TS18013 [ERROR]: Property ‘#isActive’ is not accessible`
47.  `* outside class ‘Person’ because it has a private identifier.`
48.  `*/`
49.  `// console.log(person.#isActive);`

51.  `console.log(person.Is_active);`
52.  `person.Is_active = false;`
53.  `console.log(person.Is_active);`

# [Static](#toc.xhtml_s36a)

It is used to define a property that belongs to the class and not its instance. This means that the static field remains the same for all class instances. It is useful in scenarios where we want a single copy of a field shared across all the instances. In the following example, we are using **`static instanceCount`** to count the number of instances of the **`Person`** object.

1.  `class Person {`
2.  `  name: string; // public`
3.  `  age: number; // public`

5.  `  // static property shared across instances`
6.  `  static instanceCount: number = 0;`

8.  `  constructor(name: string, age: number) {`
9.  `    this.name = name;`
10.  `    this.age = age;`

12.  `    // TS2576 [ERROR]: Property ‘instanceCount’ is a static member of type ‘Person’.`
13.  `    // this.instanceCount += 1;`

15.  `    // Class property`
16.  `    Person.instanceCount += 1;`
17.  `  }`

19.  `  printMe() {`
20.  `    console.log(this.name, this.age);`
21.  `  }`
22.  `  printTotalPersons() {`
23.  `    console.log(“Total persons: “, Person.instanceCount);`
24.  `  }`
25.  `}`

27.  `const person = new Person(“me”, 99);`
28.  `person.printMe();`
29.  `person.printTotalPersons(); // instanceCount = 1;`

31.  `const person2 = new Person(“you”, 29);`
32.  `person2.printMe();`
33.  `person2.printTotalPersons(); // instanceCount = 2;`

# [Abstract](#toc.xhtml_s37a)

Abstract class is a common base class (for example, **`Person`**) with a basic structure that can be inherited by other classes (for example, **`Employee`**, **`Employer`**).

1.  `abstract class Person {`
2.  `  name: string; // public`
3.  `  age: number; // public`

5.  `  constructor(name: string, age: number) {`
6.  `    this.name = name;`
7.  `    this.age = age;`
8.  `  }`

10.  `  printMe() {`
11.  `    console.log(this.name, this.age);`
12.  `  }`
13.  `}`

15.  `/**`
16.  `* error: TS2511 [ERROR]: Cannot create an instance of an abstract class.`
17.  `*/`
18.  `// const person = new Person(“employee”, 39);`
19.  `// person.printMe();`

21.  `class Employee extends Person {}`
22.  `class Employer extends Person {}`

24.  `const employee = new Employee(“employee”, 39);`
25.  `employee.printMe();`

27.  `const employer = new Employer(“employer”, 99);`
28.  `employer.printMe();`

# [Static versus dynamic typing](#toc.xhtml_s38a)

While writing applications, we come across programming languages which fall into either static or dynamic type systems. Static typing provides type safety during compile time but takes more time in the development process, whereas dynamic typing allows us to write code faster but may have errors and bugs which get caught only during run time.

1.  `// Static typing (TypeScript)`
2.  `let id: number = 235; // Type is determined in compile-time`
3.  `// id = “332w”; // Error. Type change not allowed`
4.  `// Type inferred by TypeScript`
5.  `let myId = 235; // number type inferred by value`
6.  `// myId = “332w”; // Error. Type change not allowed`

8.  `// Dynamic typing (JavaScript)`
9.  `let id1 = 10; // Type is determined in the runtime`
10.  `id1 = “132w”; // Type change allowed`

|  | **Static typing** | **Dynamic typing** |
| **Data type** | Needs to be specified explicitly | No need to specify data type explicitly |
| **Type checking** | At compile-time | At runtime |
| **Type change** | Not allowed | Allowed |
| **Languages** | C, C++, Java, C# | Python, JavaScript, Ruby |

# [Strong versus weak typing](#toc.xhtml_s39a)

Strong typing means type conversions are not allowed implicitly, whereas weak typing means type conversions can be done implicitly.

`# Strong typing (Python)`

1.  `id = 34 + “sfs” // Error: unsupported operand type(s) for +: ‘int’ and ‘str’`

`// Weak typing (JavaScript)`

1.  `let id = 34 + “abc”; // results “34abc” because of type casting`

|  | **Strong typing** | **Weak typing** |
| **Languages** | Python | JavaScript |
| **Type conversion** | Only manual | Automatic and manual |
| **Example** | 1 + “2”  // gives error in Python | 1 + “2” // results “12” in JavaScript |

# [TypeScript setup](#toc.xhtml_s40a)

Before Deno, TypeScript had to be installed via “**`npm`**”. But, as Deno ships with TypeScript, we can start writing TypeScript code directly. But, if you intend to use TypeScript outside the Deno environment, you will have to install it using npm globally.

**Note: Make sure you have installed node & npm.**

**`npm install -g typescript`**

Once done, check if typescript is installed by running:

**`tsc --version`**

**`tsc --help`**

# [tsconfig.json](#toc.xhtml_s41a)

It is a TypeScript configuration/settings file that indicates the root of the TypeScript project and also specifies root files and compiler options. Deno provides a default **`tsconfig.json`**, which can be checked here. (**[https://deno.land/manual/getting_started/typescript#custom-typescript-compiler-options](https://deno.land/manual/getting_started/typescript#custom-typescript-compiler-options)**)

# [Conclusion](#toc.xhtml_s42a)

TypeScript is a widely revered and accepted superset of JavaScript providing type safety. Its popularity in the industry is one of the reasons Deno made it the primary language in its setup.

We have covered the TypeScript basics in this chapter, and there is much more we can learn in the entire journey, as TypeScript will be our language of choice for Deno programming. We will get hands-on practice with TypeScript in upcoming chapters.

Meanwhile, you can always try different TypeScript features directly in the TS Playground (**[https://www.typescriptlang.org/play/](https://www.typescriptlang.org/play/)**).

With this chapter, our foundation section (Deno, TypeScript) is completed, and we will get started with hands-on programming with Deno in the upcoming chapter, where we will setup Deno and get to know basic Deno commands.

# [CHAPTER 3](#toc.xhtml_c03)

# [Setting Up Deno](#toc.xhtml_c03)

# [Introduction](#toc.xhtml_s43a)

We are now ready to get our hands-on experience running Deno in this section. Before getting started, we need to set up the development environment for Deno. Coding or programming is only one of the major aspects of software engineering. There are other major factors involved that allow us to engineer and ship well-crafted software applications in an estimated timeframe.

# [Structure](#toc.xhtml_s44a)

In this chapter, we will cover the following points:

*   Installing Deno
*   Development tools
    *   Terminal
    *   zsh + Oh my zsh
    *   Vim
    *   VS Code (with extensions)
    *   Git and GitHub
    *   Postman
    *   Docker
    *   Silver searcher
    *   Database
        *   MongoDB + MongoDB Atlas
        *   Postgres
        *   Redis
    *   Heroku CLI
    *   Pomodoro Technique
    *   Tmux

# [Objectives](#toc.xhtml_s45a)

We will be installing Deno via terminal, and we will also have a brief overview of some major development tools and technologies required during Deno development. We will be using them while working on the projects later on. Though optional, these tools will provide a better developer experience and organization. We will also learn to set up some of the popular development tools useful for developers to be productive and organized.

# [Installing Deno](#toc.xhtml_s46a)

Installing Deno is quite easy and can be done using a single terminal command. There are various ways to install Deno on your machine as follows:

`# Shell (MacOS, Linux):`

`curl -fsSL https://deno.land/x/install/install.sh | sh`

`Install specific version:`

`curl -fsSL https://deno.land/x/install/install.sh | sh -s v1.5.4`

`# PowerShell (Windows):`

`iwr https://deno.land/x/install/install.ps1 -useb | iex`

`Install specific version:`

`$v=”1.5.4”; iwr https://deno.land/x/install/install.ps1 -useb | iex`

`# Homebrew (MacOS):`

`brew install deno`

Check if Deno is installed by running:

**`deno --version`**

Deno can be upgraded by running:

**`deno upgrade`**

Deno can be upgraded to a specific version by running:

**`deno upgrade --version 1.5.3`**

# [Development tools](#toc.xhtml_s47a)

Productivity, focus, and organization are critical aspects of a developer’s day-to-day life. They allow us to manage and organize our workflow so we can create more value with a systematic and organized approach.

Development tools are one important aspect of software engineering that is often ignored or sidelined. These tools are very helpful for increased productivity and better organization. They let us focus on the prime part, that is, software development, whereas they manage other factors efficiently for us. Let us have an overview of some of the major tools used by developers worldwide.

# [Terminal](#toc.xhtml_s48a)

This is where we live in the programming world for most of our time. Getting familiar with it gives us an upper edge while planning and executing daily tasks or scripts as they are known in the software world. This is the place where we will execute Deno commands (from installing Deno to running Deno applications). You could use UNIX terminal for Linux/mac or PowerShell for windows OS.

# [zsh + oh my zsh](#toc.xhtml_s49a)

While using the terminal, **`zsh`** (Z shell) and **`oh my zsh`** (zsh framework) can level up your overall development experience and productivity. Check out the GitHub page for installation guides. Oh my zsh comes with some great plugins, as shown in *[figure 3.1](#c03.xhtml_fig3_1)*.

**`Install zsh`**

**[https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)**

**`Install oh my zsh`**

**[https://github.com/ohmyzsh/ohmyzsh](https://github.com/ohmyzsh/ohmyzsh)**

![](images/Figure-3.1.jpg)

**Figure 3.1:** Terminal with zsh + oh my zsh setup

**Theme**: powerlevel10k

**Plugins**: Git, zsh-syntax-highlighting, and zsh-autosuggestions

# [Vim](#toc.xhtml_s50a)

Vim (also known as vi) is a legendary text editor used for fast and efficient text operations. Vim has been in the industry for decades and has maintained its ranking in the topmost editors for all these years. It is a keyboard-centric application that focuses on keyboard commands to perform complex text operations. Vim has its own keybinding, which needs some time to get used to, resulting in better control over text manipulation and cursor movements.

There are many legends associated with vim, and editor war is perhaps the most famous of all. There is a famous legend about the rivalry between vim and emacs back in the 90s. Vim can be used via VS Code Extension or directly from the terminal.

**`Install vim`**

**[https://www.vim.org/download.php](https://www.vim.org/download.php)**

# [VS Code](#toc.xhtml_s51a)

VS Code is an open-source IDE developed by Microsoft. It is available on all platforms (Windows, Linux, and macOS) and is one of the most popular and widely used IDE at the moment.

It is built with Electron—A JavaScript framework for the development of cross-platform desktop applications. We will be using it for coding Deno applications. Installing VS Code on any platform is very easy. Open **[https://code.visualstudio.com/download](https://code.visualstudio.com/download)** and download and run the executable file for your OS.

# [VS Code extensions](#toc.xhtml_s52a)

We will list a few useful extensions while developing Deno programs in VS Code. These extensions can be searched and installed from VS Code.

*   **Deno**: Enables Deno support for VS Code
*   **Prettier**: A code formatter to prettify your Deno code
*   **ESLint**: A linter that analyses your ES code for issues
*   **Vim**: Enable vim support in VS Code
*   **GitLens**: Visualized git experience in VS Code

# [Git and GitHub](#toc.xhtml_s53a)

*Git* is a distributed version control system developed by *Linus Torvalds* (Creator of the Linux kernel). It is widely used in the Software Industry for code versioning and management. Head over to **[https://git-scm.com/downloads](https://git-scm.com/downloads)** to install it on your OS.

*GitHub* is a source code hosting site owned by *Microsoft*. It uses Git for version control and source code management. Head over to **[https://github.com/](https://github.com/)** and sign up if you have not yet. We will use it for hosting our Deno code.

# [Postman](#toc.xhtml_s54a)

A platform for API development and testing, it helps us manage the API collections and test our APIs with GUI. We will be using it to test our APIs. Head over to **[https://www.postman.com/downloads/](https://www.postman.com/downloads/)** to download and install Postman on your OS platform.

# [Docker](#toc.xhtml_s55a)

Docker is a container-based software development platform that runs the entire application as an isolated process. It is a very useful tool in containerization and microservices. Docker has brought the container revolution that changed the way an application is developed and deployed.

Docker was ranked #1 most wanted, #2 most loved, and #3 most popular platforms in Stack Overflow survey 2020.

**`Install docker`**

**[https://docs.docker.com/engine/install/](https://docs.docker.com/engine/install/)**

# [Docker Compose](#toc.xhtml_s56a)

Docker Compose is a tool developed by the Docker team to compose and run multiple docker containers as a single service. We will be using it to define multiple services/containers in the **`docker-compose.yml`** file. We can then run all the defined services with the YAML configurations using a single command.

**`Install docker-compose`**

**[https://docs.docker.com/compose/install/](https://docs.docker.com/compose/install/)**

# [Silver Searcher](#toc.xhtml_s57a)

A free and open-source command-line tool for searching code fast from the terminal. Check out **[https://github.com/ggreer/the_silver_searcher](https://github.com/ggreer/the_silver_searcher)** for installation instructions. This tool will be helpful for quick code searches from the terminal during Deno development.

# [Databases](#toc.xhtml_s58a)

There are two types of databases widely used in the industry, *relational* databases (SQL and PostgreSQL) storing data in tables as columns and rows and *non-relational* databases (MongoDB, Redis, and ElasticSearch) storing the data in collections. Postgres (RDBMS) and MongoDB (NoSQL) databases are the most popular amongst databases.

# [PostgreSQL](#toc.xhtml_s59a)

PostgreSQL (also known as **postgres**) is a free and open-source **relational database management system** (**RDBMS**). It is a SQL-based database that uses SQL for data management and stores the data in table format.

**`Install postgres`**

**[https://www.postgresql.org/download/](https://www.postgresql.org/download/)**

# [MongoDB and MongoDB Atlas](#toc.xhtml_s60a)

MongoDB is an open-source NoSQL database system that uses JSON-like documents to store the data. There are two ways to use MongoDB in Deno projects as follows:

1.  **Install MongoDB locally**

    This will install MongoDB on your machine, which can be used as a database.

    During the local development of Deno applications.

    **[https://docs.mongodb.com/manual/installation/](https://docs.mongodb.com/manual/installation/)**

2.  **MongoDB Atlas**

    It is a cloud-based database service that lets us use MongoDB services without installing them locally. It has a free-tier plan that we will be using as a database for Deno projects. You can register yourself to get started with MongoDB Atlas.

    **[https://www.mongodb.com/cloud/atlas](https://www.mongodb.com/cloud/atlas)**

# [Redis](#toc.xhtml_s61a)

**Remote Dictionary Server** (**Redis**) is an open-source, in-memory database that stores data in key-value format. We can always try it locally by following instructions on **[https://redis.io/topics/quickstart](https://redis.io/topics/quickstart)**

Redis docker image

**[https://hub.docker.com/_/redis](https://hub.docker.com/_/redis)**

# [Heroku](#toc.xhtml_s62a)

It is a **platform as a service** (**PAAS**) used to deploy applications written using different programming languages for free.

**Signup on Heroku**

**[https://www.heroku.com/home](https://www.heroku.com/home)**

**Heroku CLI**

**[https://devcenter.heroku.com/articles/heroku-cli#download-and-install](https://devcenter.heroku.com/articles/heroku-cli#download-and-install)**

# [Tmux](#toc.xhtml_s63a)

It is an open-source terminal multiplexer program that lets you create multiple terminals from a single screen. It will be a very useful utility while using the terminal. Please take a look at the following screenshot:

![](images/Figure-3.2.jpg)

**Figure 3.2:** Tmux

# [Pomodoro Technique](#toc.xhtml_s64a)

It is a time management technique used to break down work into time intervals known as **Pomodoro** (the Italian word for “*tomato*”), followed by a short/long break. It helps us break our work into smaller tasks and work on each task for certain Pomodoros/Pomodori. It has been beneficial to many developers (including myself), and hence, it has made its way into this chapter. You can learn more about it from the official website:

**[https://francescocirillo.com/pages/pomodoro-technique](https://francescocirillo.com/pages/pomodoro-technique)**

| **Term** | **Length** |
| Pomodoro | 25 minutes |
| Short break | 5 minutes |
| **Long break** | **15 or 25 minutes** |

**Table 3.1:** Pomodoro technique terms

# [Conclusion](#toc.xhtml_s65a)

We have explored some of the major tools useful during software development. We will be using many of the mentioned tools while creating Deno applications. Though many of these tools are optional for Deno development, we still recommend using them to have a better development experience. We will learn about the Deno Ecosystem, including CLI, Standard modules, and the nest.land (Deno package registry that uses blockchain), and other stuff in the upcoming chapter.

# [CHAPTER 4](#toc.xhtml_c04)

# [Deno Ecosystem](#toc.xhtml_c04)

# [Introduction](#toc.xhtml_s66a)

Before getting hands-on experience in Deno applications development, we need to learn the runtime APIs, CLI commands, and other functions. These APIs will provide input/output and network-related functionality. We will explore the Deno CLI, Deno runtime APIs (Web APIs + Deno global APIs), standard modules library, third-party modules, and module registries that together form the Deno ecosystem.

# [Structure](#toc.xhtml_s67a)

In this chapter, we will cover the following points:

*   Deno CLI
    *   Environment variables
    *   Subcommands
    *   Passing arguments
    *   File watcher
    *   Permission flags
    *   Permissions allow-list
*   Deno runtime APIs
    *   Web APIs
    *   Deno global APIs
    *   Variables
    *   Classes
*   Deno modules
    *   Standard library
    *   Third-party modules
*   Module registries
    *   deno.land/x
    *   nest.land
    *   Skypack CDN
    *   esm.sh
    *   jspm
    *   Web
*   Dependency management

# [Objectives](#toc.xhtml_s68a)

We will be exploring the various sections of the Deno ecosystem in this chapter. The ecosystem includes **command line interface** (**CLI**) commands such as run, install, and so on. The runtime APIs (Web + Deno global) and standard modules (inspired by Go’s standard library) such as uuid, http, fs, and so on. Apart from the standard modules, there are thousands of third-party Deno modules available for various applications such as *http server (oak, opine), graphql (oak-graphql), script runner (velociraptor), orm (denodb), module managers (trex), file watcher (denon),* and so on.

We will be using some of them in the upcoming Deno projects section. These modules are hosted on Deno’s official registry at **[https://deno.land/x](https://deno.land/x)** and also at **[https://nest.land](https://nest.land)**, which uses Permaweb where modules can never be deleted. As Deno can import modules from URL, modules hosted on, esm.sh, and skypack can also be used for Deno application development.

# [Deno CLI](#toc.xhtml_s69a)

Deno **command-line interface** (**CLI**) provides some standard environment variables, subcommands, and options out of the box. We will check some major ones in this section.

# [Environment variables](#toc.xhtml_s70a)

Environment variables are stored outside the code program and can be modified without any changes to the code itself. These are very useful for setting values in different execution environments (development, staging, production, and so on). They are also used to store private/secret keys that should not be exposed as part of the code. Deno offers several environment variables, and we are listing a few major ones as follows:

*   **`DENO_DIR`**: The directory used to cache downloaded imports. Imports are downloaded only on the first execution. The cached imports from DENO_DIR are then used for subsequent runs
*   **`DENO_INSTALL_ROOT`**: The directory used to save modules installed via Deno install command.

# [Subcommands](#toc.xhtml_s71a)

Deno subcommands are used to perform a variety of operations, such as running the program, formatting the code, installing scripts, and so on. We will be using the **`run`** command most frequently along with the **`help`** to get help about specific subcommands. We will check most of the subcommands with a brief overview and code example in the following section:

*   **help**: Useful to print general help information or of the specified subcommand.
    1.  `deno help # Lists subcommands, options, environment variables`
    2.  `deno help run # Prints help info for the run command`
*   **run**: It executes Deno program provided in any of the following ways:
    *   filename:
        1.  `deno run welcome.ts # executes local welcome.ts file`
    *   url:
        1.  `deno run https://deno.land/std@0.79.0/examples/welcome.ts`
    *   stdin:
        1.  `cat welcome.ts | deno run -`
*   **install:** Installs a Deno script as an executable in the directory specified as **`DENO_INSTALL_ROOT`**.
    1.  `# Install denon (file watcher) as an executable`
    2.  `deno install -qAf https://deno.land/x/denon@2.4.5/denon.ts`
*   **fmt:** Formatter for TypeScript/Javascript code.
    1.  `deno fmt # Formats all the files in the current directory recursively`
*   **doc**: Prints documentation for provided source file (module)
*   **eval**: Evaluate Javascript code from the terminal
    1.  `deno eval “console.log(Deno.args)” deno land`
    2.  `# Output: [“deno”, “land”]`
*   **test**: Runs tests using a built-in test runner. Files with **`{*_,*.,}test.{js,mjs,ts,jsx,tsx}`** patterns are considered for testing. Supports filter, coverage, fail-fast, and other options.
*   **cache**: Downloads and compiles a module and saves all its dependencies in the local cache without running the code.
    1.  `deno cache https://deno.land/std/http/file_server.ts`
*   **bundle**: Bundles a single JavaScript file with all dependencies.
*   **completions**: Outputs Deno shell completion script to the provided source file.
    1.  `# Install Deno completions as a plugin in oh-my-zsh`
    2.  `mkdir ~/.oh-my-zsh/custom/plugins/deno`
    3.  `deno completions zsh > ~/.oh-my-zsh/custom/plugins/deno/_deno`
    4.  `# Add deno in ~/.zshrc plugin`
    5.  `plugins=(… deno) // … represents other plugins`
*   **compile**: Compiles provided script into self-contained executable.

# [Passing arguments](#toc.xhtml_s72a)

Arguments are useful whenever a dynamic value needs to be provided to the code. Arguments can be passed to the script by specifying them after the script name in the following format:

1.  `deno run [FLAGS] [SCRIPT] [ARGUMENTS]`

The preceding format starts with **`deno`** executable command followed by **`run`** subcommand, which executes the provided script followed by optional security flags such as **`--allow-net`**, **`--allow-read`**, and so on. The path for the script to be executed is then provided, followed by optional arguments. All the entries (separated by space) provided after the script are considered as arguments and are made available via **`Deno.args`** variable.

We can use the preceding format for running Deno scripts with arguments. Create a file named **`args.ts`** in the projects folder (like **`home/my/work/deno/passing-arguments`**) with the following code:

1.  `// args.ts`
2.  `console.log(Deno.args);`

The preceding code simply logs Deno runtime variable **`Deno.args`**, which is an array of provided arguments. An empty array [] is logged if no arguments are provided, as shown in *[figure 4.1](#c04.xhtml_fig4_1)*:

![](images/Figure-4.1.jpg)

**Figure 4.1:** Passing arguments

We will now pass two arguments **`deno`** and **`land`**, to the **`args.ts`** file. As shown in *[figure 4.1](#c04.xhtml_fig4_1)*, the console should log **`[“deno”, “land”]`** after running the following code:

1.  `deno run args.ts deno land`
2.  `# Output: [“deno”, “land”]`

The preceding code runs the **`args.ts`** file with two additional parameters **`deno`** and **`land`**. As Deno considers all the entries passed after the file name separated with space as arguments, the entries are made available to the **`args.ts`** file in **`Deno.args`** variable.

**Note: Flags should not be passed after the script name as they will be considered as arguments.**

The **`--allow-net`** flag passed before **`args.ts`** script is considered as a **`flag`**, as shown in the following code:

1.  `deno run --allow-net args.ts deno land # Args [“deno”, “land”]. allow-net is a flag.`

The **`--allow-net`** flag passed after **`args.ts`** script is considered as an **argument**, as shown in the following code:

1.  `deno run args.ts name --allow-net # Args[“name”, “--allow-net”]. Allow-net is not a flag`

# [File watcher](#toc.xhtml_s73a)

Deno will run the script in watch mode if **`--watch`** option is provided. It will rerun the script whenever a change is detected in the script. Watch mode watches for changes in the script and all its imports. This feature is still in unstable mode, which means it is not suitable for production use and will likely have breaking changes. For such features, we will have to use the **`--unstable`** flag along with **`--watch`** flag:

1.  `# Watch welcome.ts and rerun if changes detected`
2.  `deno run --watch --unstable welcome.ts`

# [Permission flags](#toc.xhtml_s74a)

Unlike Node, Deno does not provide access by default to the network, input/output, unless asked explicitly via permission flags. This functionality makes Deno very secure compared to Node. The following table includes all the major permission flags:

| **Permission** | **Description** | **Command** |
| **`--allow-net`** | Allows network access | **`deno run --allow-net example.ts`** |
| **`--allow-read`** | Allows read operation | **`deno run --allow-read example.ts`** |
| **`--allow-write`** | Allows write operation | **`deno run --allow-write example.ts`** |
| **`--allow-run`** | Allows running subprocesses | **`deno run --allow-run example.ts`** |
| **`--allow-env`** | Allows environment access | **`deno run --allow-env example.ts`** |
| **`--allow-plugin`** | Allows use of plugins | **`deno run --allow-plugin example.ts`** |
| **`--allow-all`** | Allows all permissions | **`deno run -A example.ts # -A = --allow-all`** |

**Table 4.1:** Permission flags

# [Permissions allow-list](#toc.xhtml_s75a)

By default, flags such as allow-write and allow-net provide access to any path or domain. To limit access to a specific domain/path, we use a permissions allow-list. Only mentioned paths in the list are allowed access to the resource.

Create a file named **`permission_list.ts`** and add code that uses the fetch API to fetch resources from sites *deno.land*, *github.com*, and *google.com*, respectively, as shown in the following code:

1.  `// permission_list.ts`
2.  `fetch(“https://deno.land”);`
3.  `fetch(“https://github.com”);`
4.  `fetch(“https://google.com”); // Throws error if not added in permission_list`

We would not get any network access error as all domains are allowed when we run the **`permission_list.ts`** script with **`--allow-net`** flag without permission list, as shown as follows:

1.  `# All domains are allowed to access the network`
2.  `$ deno run --allow-net permission_list.ts`

If we run the **`permission_list.ts`** script with the permission list allowing network access *deno.land* and *github.com* only, network access to all other domains will not be allowed, as shown in the following code:

1.  `# Only ‘deno.land’ and ‘github.com’ domains are allowed network access`
2.  `$ deno run --allow-net=deno.land,github.com allow-net_example.ts`

We used the domain for the **`allow-net`** permission list. Similarly, we can provide allowed paths for **`allow-read`** and **`allow-write`** flags. The following code reads previously created file **`args.ts`** and requires an **`allow-read`** flag. It uses **`readTextFile`** function from Deno API to read the **`args.ts`** file contents as utf8 encoded string.

1.  `// allow-read-list_example.ts`
2.  `const argsContent = await Deno.readTextFile(“./args.ts”);`
3.  `console.log(argsContent);`

If we run the preceding code with the following command, it would log the contents of **`args.ts`** to console:

1.  `# Only ‘args.ts’ file is allowed to be read`
2.  `$ deno run --allow-read=args.ts allow-read-list_example.ts`

The following command would throw **`PermissionDenied`** error as **`args.ts`** is not added in the permission list:

1.  `# Only ‘args1.ts’, ‘args2.ts’ files are allowed to be read`
2.  `$ deno run --allow-read=args1.ts,args2.ts allow-read-list_example.ts`

# [Deno runtime APIs](#toc.xhtml_s76a)

Deno provides several number of runtime API functions that are useful during application development. All these runtime functions are documented at doc.deno.land (**[https://doc.deno.land/https/github.com/denoland/deno/releases/latest/download/lib.deno.d.ts](https://doc.deno.land/https/github.com/denoland/deno/releases/latest/download/lib.deno.d.ts)**). These functions can be categorized into two sections, namely, Web (browser) APIs and Deno global APIs.

# [Web APIs](#toc.xhtml_s77a)

Deno focuses on using existing Web standard APIs instead of creating new ones. Browser APIs such as **`fetch`**, **`setTimeout`**, and many other Web APIs are available in Deno. This gives an advantage that the developer familiar with web APIs can use them directly. We will list these APIs in the following table:

| **Web API** | **Description** |
| **`Fetch`** | Used to make HTTP requests and fetch a resource from the network. It returns a promise. |
| **`addEventListener`** | Adds an event listener in the global scope. |
| **`removeEventListener`** | Removes **`eventListener`** added by the **`addEventListener`** function from the global scope |
| **`Alert`** | A standard alert function that shows an alert message and waits until Enter key is pressed |
| **`setInterval`** | Calls provided function repeatedly after provided interval until it is cleared using **`clearInterval`** function |
| **`clearInterval`** | Cancels an action initiated by **`setInterval`** |
| **`setTimeout`** | Invokes function after the specified time period |
| **`clearTimeout`** | Cancels delayed action initiated by **`setTimeout`** |
| **`Btoa`** | Creates base-64 ASCII encoded string from the provided string |
| **`Atob`** | Decodes string of data encoded by base-64 encoder like **btoa** |
| **`Confirm`** | Shows provided message and wait for user input. Returns user input in **boolean** (only **y** and **Y** are true) |
| **`Prompt`** | Shows provided message and wait for user input. Returns user input in **string** format |
| **`dispatchEvent`** | Dispatches event in the global scope and invokes registered listeners. Returns **false** for a cancelable event or if a listener called **`Event.preventDefault()`** |

**Table 4.2:** Web APIs

# [Deno global APIs](#toc.xhtml_s78a)

All non-Web standard APIs are made available via Deno global namespace. APIs for i/o (**`Deno.readFile`**, **`Deno.writeFile`**) and networking (**`Deno.listen`**, **`Deno.connect`**) are available in this namespace.

Note that many of the functions have synchronous versions available.

For example, **`create`** function has a synchronous method **`createSync`.**

We will list the Web APIs and their synchronous versions (if available) in the following table:

| **Deno API** | **Sync** | **Description** |
| **`listen`** | **`–`** | Used to create a listener with options for hostname, port, and transport |
| **`close`** | **`–`** | Closes previously opened resource ID (**`rid`**) |
| **`connect`** | **`–`** | Connects to the provided hostname, port |
| **`copy`** | **`–`** | Copies from source to destination |
| **`cwd`** | **`–`** | Returns current working directory (**`cwd`**) as a string |
| **`run`** | **`–`** | Spawns a new subprocess. The subprocess command must be defined as an array to the cmd key |
| **`exit`** | **`–`** | Exits the Deno process. An optional error code can be provided as an argument(default=0) |
| **`open`** | **`openSync`** | Open a file to perform read, write, and create operations |
| **`copyFile`** | **`copyFileSync`** | Copies contents and permissions of one file to another file |
| **`create`** | **`createSync`** | Creates a file if none exists or truncates the existing one |
| **`mkdir`** | **`mkdirSync`** | Creates a new directory with a provided string path |
| **`readDir`** | **`readDirSync`** | Reads directory at the provided path and returns **`Deno.dirEntry`** iterable. Error is thrown if the path is not a directory |
| **`readFile`** | **`readFileSync`** | Reads file as an array of bytes. The bytes can be converted to a string using TextDecoder. Returns an empty array if the path contains a directory |
| **`readTextFile`** | **`readTextFileSync`** | Reads file as an utf8 encoded string. Throws an error if the path contains a directory |
| **`remove`** | **`removeSync`** | Removes file or directory at the provided path. Throws error for a non-empty directory(with recursive option is not set to true), the path not found, permission denied |
| **`rename`** | **`renameSync`** | Renames/Moves resource (file or directory) from old path to new path. Overwrites a new path if it already exists |
| **`chmod`** | **`chmodSync`** | Changes permissions of provided file or directory using the three octal sequence called mode |
| **`chown`** | **`chownSync`** | Changes owner of file or directory (not available on Windows OS) |
| **`writeFile`** | **`writeFileSync`** | Writes data (Array of bytes encoded by TextEncoder) at the provided path by either creating a new file or overwriting the existing one |
| **`writeTextFile`** | **`writeTextFileSync`** | Writes data (string) at the provided path by either creating a new file or overwriting the existing one |

**Table 4.3:** Deno APIs

# [Variables](#toc.xhtml_s79a)

Deno provides variables for various applications. It includes variables for CLI arguments, build-related info, environment variables, and so on. The following table lists major variables in the Deno runtime.

| **Variable** | **Description** |
| **`args`** | Returns array of arguments in string. Arguments are provided via CLI |
| **`build`** | Provides system-related info such as **`os`**, **`target`**, **`arch`**, **`vendor`**, and **`env`** |
| **`env`** | Provides functions to **`set`**, **`get`**, and **`delete`** environment variables. **`toObject`** function lists all the available environment variables |
| **`mainModule`** | Returns URL of the entrypoint module in a string |
| **`pid`** | Returns the current process id of the runtime |
| **`stdin`** | A handle for **`stdin`** (Standard Input) |
| **`stdout`** | A handle for **`stdout`** (Standard Output) |
| **`stderr`** | A handle for **`stderr`** (Standard Error) |
| **`version`** | Provides version-related info for Deno, Typescript, and v8 |

**Table 4.4:** Deno variables

# [Classes](#toc.xhtml_s80a)

There are several classes in Deno runtime for different purposes. We will be using **`Request`** and **`Response`** classes in our upcoming projects. The following list contains the major classes with the description:

| **Class** | **Description** |
| **`Blob`** | A file-like object containing raw, immutable data. |
| **`Event`** | Class representing **DOM Event**. Contains target attribute, **`PreventDefault()`** method, and so on. |
| **`File`** | Provides file-related info like **`lastModified`**, **`name`**, **`type`**, **`size`**, and so on. It is inherited from the **`Blob`** class. |
| **`FormData`** | Represents form fields in key-value pair format. Provides methods such as **`get`**, **`set`**, **`keys`**, **`values`**, **`entries`**, and so on. |
| **`Headers`** | Represents header-related data in object format. |
| **`Location`** | Provides location/URL of the linked object via **`globalThis.location`** |
| **`Request`** | Represents a request related info |
| **`Response`** | Represents a response to the request |
| **`TextEncoder`** | Provides utf8 encoding functionality useful to encode a string to an array of bytes |
| **`TextDecoder`** | Provides decoding function to decode an array of bytes to string |
| **`URL`** | Provides object with static methods required to create object URLs |
| **`WebSocket`** | Provides APIs to create and manage WebSocket connections and send and receive data |

**Table 4.5:** Deno classes

# [Deno modules](#toc.xhtml_s81a)

The runtime ecosystem cannot be completed without the modules (standard and third-party). In fact, the popularity of Node is owed to a large number of third-party modules available via npm. There are two types of modules available in Deno: Standard Library and Third-Party modules. We will check both types of modules in the following sections.

# [Standard library](#toc.xhtml_s82a)

Deno standard library is a collection of standard modules and is inspired by the standard library of the Go language. All the standard modules are reviewed by Deno Core Team and do not have external dependencies. These modules are available at **[https://deno.land/std](https://deno.land/std)**. We have listed them in the following table:

| **Module** | **Description** |
| **`archive`** | Module providing **Tar**, **Untar** functionality. |
| **`Async`** | Asynchronous task utility with **deferred** (Promise with reject, resolve functions)**, delay** (delay promise resolve) functionality. |
| **`Bytes`** | Provides helper functions to manipulate bytes. |
| **`Datetime`** | Datetime module with **parse** (string to date), **format** (date to string), **difference** (the difference between 2 dates), and some additional functions. |
| **`Encoding`** | Ported from Go’s **encoding** module, this module is useful for dealing with external data structures such as csv, yaml, toml, and so on |
| **`flags`** | A command-line argument parser based on **`minimist`** npm module. It is useful for CLI tool development. |
| **`Fmt`** | Provides i/o formatting functions like **`printf`.** |
| **`Fs`** | Provides helper functions for file system manipulation. Provides **`emptyDir`**, `ensureDir`**,** **`exists`,** **`move`,** **`copy`,** **`walk`,** and other functions. This module is unstable as of now, and hence, will need to use **`–unstable`** flag during usage. |
| **`Hash`** | Used to create a hash with a large number of supported algorithms. |
| **`http`** | Useful for creating HTTP Web servers. It also includes a file server function to serve local files over HTTP. |
| **`Io`** | Provides functions like **`Reader`,** **`Writer`,** **`Streams`,** and so on. |
| **`Log`** | A logger module with log levels. |
| **`Mime`** | Used to deal with multipart form data. |
| **`Node`** | The Compatibility module for Node’s Standard Library. Enables use of Node modules like lodash in Deno. |
| **`Path`** | Provides path related functions. |
| **`Permissions`** | Provides Permissions to the scripts. |
| **`Signal`** | Provides APIs to capture and monitor OS signals like SIGINT. |
| **`Testing`** | Provides test-related utilities such as **assert, equal,** and so on. |
| **`Textproto`** | Inspired by Go’s **`textproto`** module. |
| **`Uuid`** | Provides functions to **generate** and **validate** **Universal unique identifier** (**UUID**) with support for versions 1, 4, and 5. |
| **`Wasi`** | Provides the implementation for **WebAssembly System Interface** (**WASI**) |
| **`ws`** | Useful to create WebSocket servers. |

**Table 4.6:** Deno standard library

# [Third-party modules](#toc.xhtml_s83a)

Deno 1.0 was released in May 2020\. Since then, there have been a lot of modules already available for different purposes, such as Web servers (**`oak`**), authentication (**`onyx`**), databases (**`mongo`**), ORMs (**`denodb`**), JWT (**`djwt`**), and so on. We are going to have a brief overview of many of such modules in the following table:

| **Third-Party Module** | **Description** |
| **oak** | An extremely popular web middleware framework, including middlewares like routing. It is inspired by **koa** framework. |
| **Aleph** | A react framework inspired by **Next.js** that supports **Server-Side Rendering (SSR)**, **Static Site Generator** (**SSG**)**,** and so on. |
| **Pagic** | A React framework for Static Site Generation |
| **drash** | A lightweight REST MicroFramework that supports API Development and **Single Page Applications** (**SPA**) development using React and Vue. |
| **Servest** | A web server compatible with **std/http**, it supports WebSocket and JSX out of the box. |
| **Denon** | A Deno alternative to Node’s **nodemon** that restarts the app or server automatically whenever changes are detected. It also serves as a replacement wrapper for **`deno`** command. |
| **Webview** | A cross-platform module for creating desktop GUI apps. |
| **Denodb** | ORM supports MySQL, PostgreSQL, MongoDB, MariaDB, and SQLite databases. |
| **Trex** | An NPM-like module manager that aligns with Deno’s philosophy. It uses **`import_map.json`** as a module import controller. |
| **Velociraptor** | An alternative to npm scripts, it supports scripts written in **yaml**, **json,** and **ts** format. |
| **Postgres** | A driver module for the PostgreSQL database. |
| **Redis** | A Redis client module for Deno. |
| **Dvm** | A Deno version manager is similar to **`nvm`**. |
| **Mongo** | A Mongo driver module for MongoDB database. |
| **Vno** | A compiler and bundler module for Vue components. |
| **Obsidian** | A GraphQL client and server module with caching support. |
| **Eta** | A lightweight JavaScript Template Engine is written in TypeScript. |
| **Mysql** | Driver module for MySQL database. |
| **Sqlite** | Driver module for SQLite database. |
| **Ssgo** | **Static Site Generator** (**SSG**) module built with Deno. |
| **Onyx** | Authentication module inspired by passport.js, which is compatible with **oak**. |
| **Otpauth** | OTP authentication module. |
| **Aqua** | A web framework module that is fast and minimal. |
| **Denox** | A cross-platform script runner module. |
| **Dejs** | EJS Template Engine module. |
| **Dotenv** | A module to handle environment variables. |
| **Udd** | A module to update Deno dependencies to the latest versions. |
| **Djwt** | A module to use **JSON Web Token** (**JWT**) in Deno. |
| **Cotton** | A SQL Database Toolkit module. |
| **Denomander** | A **command-line interface** (**CLI**) tool module. |
| **Lume** | A Static Site Generator module for Deno inspired by Jekyll. |
| **Oak_graphql** | A GraphQL middleware module for **oak** framework. |
| **Drake** | A Task Runner module inspired by **make, rake,** and **jake.** |
| **rhum** | A Testing framework module for Deno which is lightweight from the creators of **drash.** |
| **websocket** | A WebSocket module for Deno. |
| **dext.js** | A Preact framework module inspired by **`next.js`**. |
| **denoliver** | A static file server module with live reload support. |
| **wocket** | A WebSocket module from the creators of **drash**. |
| **dem** | A module version manager for Deno. |
| **bundler** | A bundler module to transpile TypeScript code for the web. |
| **dmm** | A Deno module manager from the creators of **drash**. |
| **opencv** | A pre-compiled OpenCV to JavaScript + WebAssembly module. |
| **garn_validator** | A validator module with many validation functions. |
| **watch** | A file watcher module for Deno. |
| **smtp** | A **Simple Mail Transfer Protocol** (**SMTP**) module for sending and receiving mails. |
| **nanoid** | A NanoID implementation module for Deno. |
| **superoak** | HTTP Assertions module for **oak** framework. |
| **dpx** | NPX like module runner (runs module without installing) for Deno. |
| **drash_middleware** | A middleware module for **drash** framework from the creators of **drash**. |
| **cors** | A **Cross-Origin Resource Sharing** (**CORS**) module for Deno. |
| **postcss** | A Postcss module for Deno. |
| **oak_middleware** | A middleware collection module for **oak** framework from the creators of **oak**. |

**Table 4.7:** Deno third-party modules

# [Module registries](#toc.xhtml_s84a)

Module registries are places where the Deno modules are hosted. Just like **`npm`** in Node, Deno has several module registries built using modern features like blockchain.

After listing the standard and third-party modules for Deno, we will be checking the major module registries available for Deno:

| **Module Registry** | **Description** |
| **`deno.land/x`** | An official module registry hosting large numbers of third-party modules (1651 modules at the time of writing) |
| **`nest.land`** | A modern Deno module registry built using **blockweave,** a derivative of **blockchain**. The published modules are immutable, decentralized, and permanent, meaning they can never be deleted. |
| **`Skypack CDN`** | A CDN to host pre-optimized ES modules offered by **Pika**. It provides minification, caching, polyfilling, and converts npm packages to ES modules. Whenever **?dts** is appended to the module URL, it automatically fetches type declarations using the **X-TypeScript-Types** header. |
| **`esm.sh`** | A CDN for ES modules from the creator of the **aleph** framework that bundles all dependencies (except peer dependencies) for every module. Node packages are transformed to ES modules using **esbuild** to run on Deno via polyfill. It provides type declarations via the **X-TypeScript-Types** header by default. |
| **`jspm`** | A module CDN that converts npm packages to ES modules. |
| **`Web`** | Any ECMAScript module hosted on the internet (e.g., GitHub) can be used via ESM import supported by Deno. |

**Table 4.8:** Deno module registries

# [Central dependencies in deps.ts](#toc.xhtml_s85a)

There is one convention in Deno land to import all the dependencies in the **`deps.ts`** file. These dependencies are re-exported and used throughout the project. This helps us maintain all the dependencies in a single place. Similarly, development dependencies are kept in a single file named **`dev_deps.ts`**.

In the following code, we are importing all the dependency URLs in the **`deps.ts`** file and exporting them to use across the project. We are importing the **`titleCase`** function from a third-party module case that returns each word in the title case. We are also importing **`assertEquals`** function from the testing module from Deno’s standard library.

`// deps.ts`

1.  `import titleCase from “https://deno.land/x/case@v2.1.0/titleCase.ts”;`
2.  `import { assertEquals } from “https://deno.land/std@0.97.0/testing/asserts.ts”;`

4.  `export { titleCase, assertEquals };`

We will now import the modules from **`deps.ts`** file in **`hello.ts`** file, as shown in the following code:

`// hello.ts`

1.  `import { titleCase, assertEquals } from “./deps.ts”;`

3.  `console.log(titleCase(“hello world”));`
4.  `assertEquals(“hello”, “helloz”);`

The preceding code logs **`“hello world“`** string in title case **`“Hello World“`** and the **`assertEquals`** function throws **`AssertionError`** as actual (**`“hello”`**) and expected (**`“helloz”`**) values are not equal, as shown in the following figure:

![](images/Figure-4.2.jpg)

**Figure 4.2:** deps.ts example

# [Conclusion](#toc.xhtml_s86a)

We are now concluding this chapter on the Deno Ecosystem. It outlined various sections of the Deno Ecosystem, such as runtime API, CLI, standard and third-party modules, module registries, and so on. Being a new technology in the industry, the Deno Ecosystem is evolving at a rapid pace. We would likely see the Deno community come up with new and exciting ideas and implementations in the coming time, as they have done until now.

With the end of this chapter, we are now ready to move to the most exciting part of the book—writing code. We will start with writing a Deno application from scratch in the upcoming chapters. Till then, keep exploring the Deno ecosystem.

# [CHAPTER 5](#toc.xhtml_c05)

# [Todos App—API](#toc.xhtml_c05)

# [Introduction](#toc.xhtml_s87a)

We are now ready to enter the Deno coding battlefield or playground (it depends on how you see it). We will create a **CREATE, RETRIEVE, UPDATE**, and **DELETE** (**CRUD**) application in this chapter. A Todos app. It will be a great way to begin our Deno coding journey. We will learn, tweak, and play around with the Todos app created using a Full Stack React framework called **`Aleph.js`** (aleph), listed in *[Table 4.7](#c04.xhtml_tab4_7)* of *[Chapter 4, Deno Ecosystem](#c04.xhtml)*. The API will be implemented in this chapter, whereas the UI will be implemented in the next one.

# [Structure](#toc.xhtml_s88a)

In this chapter, we will cover the following topics:

*   Introduction to Aleph.js
    *   Features
    *   Concepts
        *   Pages
        *   Routing
        *   APIs
*   Todos app API implementation
    *   Routes
        *   GET (list)
        *   POST
        *   PATCH
        *   GET (object)
        *   DELETE

# [Objective](#toc.xhtml_s89a)

We will be able to create a server-side API using the *Aleph.js* framework after studying this chapter. The aim of this chapter is to get familiar with Aleph.js and use its concepts to create API. Aleph.js is a Full Stack React framework used to create API and UI as well. We will start the chapter by introducing Aleph.js features and concepts. The API for the Todos app will then be developed using Aleph.js.

We will also learn to implement different **Representational State Transfer** (**REST**) API actions like **`POST`** (CREATE), **`GET`** (RETRIEVE), **`PATCH`** (UPDATE), and **`DELETE`** (DELETE) after studying this chapter.

# [Introducing Aleph.js](#toc.xhtml_s90a)

Aleph.js is a Full Stack React framework inspired by Next.js. It uses the ES module import syntax without the need for Webpack or other bundlers. It does not re-bundle every change but only the changed module and updates instantly in the browser by **Hot Module Replacement** (**HMR**) with React Fast Refresh.

Aleph.js can be installed using the following command:

1.  `deno install -A -f -n aleph https://deno.land/x/aleph/cli.ts`

# [Features](#toc.xhtml_s91a)

Aleph.js is a feature-rich framework that provides server-side rendering, static site generation, API development, and many other features. Some of the major features are as follows:

*   File-system-based pages and API routing
*   API development
*   Server-side rendering
*   Static site generation
*   Zero config
*   Use of import maps
*   HMR with Fast Refresh
*   Access to Deno runtime within component via **`useDeno`** hook

# [Command Line Interface](#toc.xhtml_s92a)

Aleph.js **Command Line Interface** (**CLI**) provides commands for static site generation, creating a new app with boilerplate code, upgrading Aleph.js, and so on. All major commands are listed in the following table:

| **Command** | **Description** |
| **`aleph init`** | Create new app with boilerplate code |
| **`aleph upgrade`** | Upgrade aleph.js |
| **`aleph`** | Prints all cli commands |
| **`aleph -h / aleph --help`** | Prints help message |
| **`aleph -v / aleph --version`** | Prints aleph.js version |
| **`aleph dev`** | Starts server in development mode |
| **`aleph start`** | Starts server in production mode |
| **`aleph build`** | Builds the app to static site |
| **`aleph analyze`** | Analyzes app dependencies |

**Table 5.1:** Aleph.js CLI

**`aleph init`** command provides an example app with boilerplate code. We will be using it to initialize the demo app as follows:

1.  `aleph init hello-aleph // Creates hello-aleph folder with boilerplate code`
2.  `cd hello-aleph`
3.  `aleph dev // Runs app in development mode`

You can visit **http://localhost:8080** to view the demo app, as shown in the following figure:

![](images/Figure-5.1.jpg)

**Figure 5.1:** Aleph.js Demo App

# [Concepts](#toc.xhtml_s93a)

There are three basic concepts we need to learn to develop a full stack app using aleph. We will use these concepts for creating pages, routing based on filenames, and API.

# [Pages](#toc.xhtml_s94a)

Any file with extension **`*.js`**, **`*.jsx`**, **`*.ts`**, **`*tsx`**, and **`*.mjs`** in /pages folder having a default exported React component is considered as a page. As aleph.js supports filename-based routing, each page will then be associated with a route based on the filename.

**Example**:

If we create **`pages/hello.tsx`** with the default exported React component as shown in the following code, then we can access that page at **http://localhost:8080/hello**, as shown in *[figure 5.2](#c05.xhtml_fig5_2).*

1.  `// pages/hello.tsx`
2.  `import React from “react”;`

4.  `export default function Hello() {`
5.  `return “Hello Deno!”;`
6.  `}`

![](images/Figure-5.2.jpg)

**Figure 5.2:** Hello Deno! Page

Every page is **pre-rendered**, meaning HTML for the page is generated in advance, resulting in better performance and SEO. Aleph.js also supports a **hydration** process, where associated JavaScript code for the HTML is run when the page is loaded by the browser, making it fully interactive.

# [Routing](#toc.xhtml_s95a)

Aleph.js supports file-system-based routing. It automatically routes files named **`index`** to the root of the directory. **Dynamic Routes** are also supported via **bracket** syntax ([]) or **$** sign prefix.

`// Index routing`

`pages/index.tsx => localhost:8080/`

`pages/hello/index.tsx => localhost:8080/hello`

`// Dynamic routing`

`// $ prefix`

`pages/hello/$name.tsx => pages/hello/buddy`

The following code uses a **`params`** object of **`useRouter()`** hook to obtain the passed parameter value. The property key of **`params`** is determined by the filename ($name).

1.  `// pages/hello/$name.tsx`
2.  `import React from “react”;`
3.  `import { useRouter } from “https://deno.land/x/aleph/framework/react/mod.ts”;`

6.  `export default function Hello() {`
7.  `const { params } = useRouter();`
8.  ``return `Hello ${params.name}!`;``
9.  `}`

If we enter **`route /hello/buddy`** in the browser, where **`buddy`** is the value of the **`name`** parameter, we shall see the response shown in *[figure 5.3](#c05.xhtml_fig5_3)*.

![](images/Figure-5.3.jpg)

**Figure 5.3:** Dynamic routes ($ Syntax)

`// Bracket syntax []`

`pages/places/[place].ts => pages/places/munich`

Similar to $ sign syntax, a bracket syntax [] does serve the same purpose as shown as follows. Here, the parameter key is the place (derived from the filename **`[place].ts`**). If we enter **`/places/munich`** in the browser, where Munich is the value of the place parameter, we shall see the response as shown in *[figure 5.4](#c05.xhtml_fig5_4)*.

1.  `// pages/places/[place].tsx`
2.  `import React from “react”;`
3.  `import { useRouter } from “https://deno.land/x/aleph/framework/react/mod.ts”;`

5.  `export default function Places() {`
6.  `const { params } = useRouter();`

8.  ``return <h1>{`${params.place} is a wonderful place!`}</h1>;``
9.  `}`

![](images/Figure-5.4.jpg)

**Figure 5.4:** Dynamic routes (bracket syntax)

**Nested Routes** are supported and can be achieved as shown in the following code:

`pages/users/[username]/account.tsx => pages/users/user1/account`

1.  `// pages/users/[username]/account.tsx`
2.  `import React from “react”;`
3.  `import { useRouter } from “https://deno.land/x/aleph/framework/react/mod.ts”;`

5.  `export default function UserAccount() {`
6.  `const { params } = useRouter();`

8.  ``return <h1>{`${params.username}’s account.`}</h1>;``
9.  `}`

![](images/Figure-5.5.jpg)

**Figure 5.5:** Nested routes

# [Application Programming Interface (API)](#toc.xhtml_s96a)

Similar to pages, any file with **`*.ts`**, **`*.js`**, **`*.mjs`** extension having default exported function inside **`api/`** folder is mapped to **`/api/*`** and is treated as an API endpoint. The exported function will be of type **`APIHandler`**.

1.  `// api/users/index.ts`
2.  `import type { APIHandler} from “aleph/types.d.ts”;`

4.  `const users = [`
5.  `{ id: 1, name: “abc”, place: “Munich” },`
6.  `{ id: 2, name: “name2”, place: “wonderland” },`
7.  `];`

9.  `export const handler: APIHandler = ({response}) => {`
10.  `response.status = 200;`
11.  `response.json(users);`
12.  `}`

![](images/Figure-5.6.jpg)

**Figure 5.6:** API routing

**Dynamic API routes** are also supported. We can create a file like **`api/users/[id].ts`** with the default export function. The **`id`** can then be passed as a parameter like **`api/users/1234`** and will be obtained from the **`router.params`** object.

1.  `// api/users/[id].ts`
2.  `import type { APIHandler } from “aleph/types.d.ts”;`

4.  `export const handler: APIHandler = async ({response, router}) => {`
5.  `response.json(router.params);`
6.  `}`

![](images/Figure-5.7.jpg)

**Figure 5.7:** Dynamic API route

# [Initializing Todos App](#toc.xhtml_s97a)

We have checked the major Aleph.js concepts required for full-stack application development. We will now initialize our todos app using the **`aleph init`** command. Head over to the terminal and type the following commands. Make sure you have installed Deno, Aleph, and VS code before running the commands.

1.  `aleph init todos-app`
2.  `cd todos-app`
3.  `code . // Make sure VS code is installed`
4.  `aleph dev // Server running on http://localhost:8080`

# [Project structure](#toc.xhtml_s98a)

The project structure shown in *[figure 5.8](#c05.xhtml_fig5_8)* is familiar to us. We have already seen API and page concepts. The **`app.tsx`** file is the entry point for our app. **`styles`** folder contains styling-related files, the components folder contains React Component files, the public folder contains all the static files, and **`lib`** folder contains custom hooks and other utility functions.

![](images/Figure-5.8.jpg)

**Figure 5.8:** Aleph project structure

Our development approach will be creating API endpoints first and then creating UI that consumes the API.

# [Todos API](#toc.xhtml_s99a)

Before creating the UI for Todos App, we will need to create the API endpoints for CRUD actions. Create an **`index.ts`** file in a folder called **`todos`** in the **`api`** folder. It should have a path like **`api/todos/index.ts`**.

1.  `// api/todos/index.ts`
2.  `import type { APIHandler} from “aleph/types.d.ts”;`

4.  `export const handler: APIHandler = ({response}) => {`
5.  `response.json({ message: “Hello Aleph!” });`
6.  `}`

Preceding code exports a function of type **`APIHandler`**. If you hit **http://localhost:8080/api/todos** using Postman, curl, or browser, the function will be called with the context argument containing request, response, and router objects. The **`response.json`** function is then used to reply with JSON content, as shown in *[figure 5.9](#c05.xhtml_fig5_9)*.

![](images/Figure-5.9.jpg)

**Figure 5.9:** **`api/todos`** endpoint

# [GET (list)](#toc.xhtml_s100a)

Now, we should modify the file to GET all existing todos instead of the message. We will create a Todos array with dummy todos, as shown here:

1.  `// api/todos/index.ts`
2.  `import type { APIHandler} from “aleph/types.d.ts”;`

4.  `const todos = [`
5.  `{ id: 1, title: “todo1” },`
6.  `{ id: 2, title: “todo2” },`
7.  `];`

9.  `export const handler: APIHandler = ({request, response}) => {`
10.  `switch (request.method) {`
11.  `case “GET”:`
12.  `   response.json(todos);`
13.  `   break;`

15.  `  default:`
16.  `   response.status = 405;`
17.  `   response.json({ message: “Action not allowed” });`
18.  `   break;`
19.  `}`
20.  `}`

Here, we are using a **`switch`** statement with the request **`method (GET, POST)`** as a case.

![](images/Figure-5.10.jpg)

**Figure 5.10:** GET/api/todos endpoint

It will respond with all the existing todos for the **`GET`** method (*[figure 5.10](#c05.xhtml_fig5_10)*), and if the requested action is not defined in the switch statement, it will reply with the **`405`** Method Not Allowed code (*[figure 5.11](#c05.xhtml_fig5_11)*). The break skips the following cases and ensures that only matched case code is executed.

![](images/Figure-5.11.jpg)

**Figure 5.11:** 405 code for undefined actions

# [POST](#toc.xhtml_s101a)

We will now implement **`CREATE (POST)`** action for adding todo.

1.  `…`
2.  `export const handler: APIHandler = async ({request, response}) => {`
3.  `switch (request.method) {`
4.  `  case “GET”:`
5.  `   response.json(todos);`
6.  `   break;`

8.  `  case “POST”:`
9.  `   let body;`

11.  `   try {`
12.  `    body = await request.json();`
13.  `   } catch (error) {`
14.  `    response.status = 400;`
15.  `    response.json({ error: error.message });`
16.  `    break;`
17.  `   }`

19.  `   const title = body.title ? body.title.toLowerCase() : null;`
20.  `   if (!title) {`
21.  `    response.status = 400;`
22.  `    response.json({`
23.  `     message: “title not provided”,`
24.  `    });`
25.  `    break;`
26.  `   }`

28.  `   let todo = todos.find((_todo) => _todo.title === title);`

30.  `   if (!todo) {`
31.  `    todo = {`
32.  `     id: todos[todos.length - 1].id + 1,`
33.  `     title, // Shorthand for title: title`
34.  `    };`

36.  `    todos.push(todo);`
37.  `   }`
38.  `   response.json(todo);`
39.  `   break;`

41.  `  default:`
42.  `…`

We are decoding the request body using the **`request.json()`** method that parses the request body as JSON. **`400`** code is responded with an error message for invalid or no JSON and also if the title is not provided. We are using the **`toLowerCase()`** function to get todo titles in lowercase. This will help us find existing Todo with the same title using the find method. If an existing todo is not found, a new todo will be created and added to the Todos list. The **`id`** property set uses the id of the last todo item (last Todo id + 1). The Todo (existing or created) will then be returned using the **`response.json`** function. Now, try adding a todo, as shown in *[figure 5.12](#c05.xhtml_fig5_12)*.

![](images/Figure-5.12.jpg)

**Figure 5.12:** POST **`api/todos`** API endpoint

The **`GET api/todos`** endpoint should contain the newly created Todo, as shown in *[figure 5.13](#c05.xhtml_fig5_13)*.

![](images/Figure-5.13.jpg)

**Figure 5.13:** Newly created Todo in GET api/todos

Now, close the server by hitting *Ctrl* + *c* and start again using the **`aleph dev`** command. You will not see the newly created Todo. This is because we are not saving the data to a file or database. To persist the data, we will create a **`todos.json`** file with the following JSON data in **`db`** folder.

`// db/todos.json`

1.  `[`
2.  `{ “id”: 1, “title”: “todo1” },`
3.  `{ “id”: 2, “title”: “todo2” }`
4.  `]`

The saved todos can then be retrieved using **`readTodos`** utility function created in **`lib/read_todos.ts`** file. We are using **`Deno.readTextFileSync`** function to read the text synchronously and then parse the JSON using **`JSON.parse`**.

1.  `lib/read_todos.ts`
2.  `const readTodos = () => JSON.parse(Deno.readTextFileSync(“db/todos.json”));`

4.  `export default readTodos;`

Now, we will obtain all saved todos using **`readTodos`** in the **`index.ts`** file. Replace the existing todos code with the following code:

1.  `// api/todos/index.ts`
2.  `import type { APIHandler} from “aleph/types.d.ts”;`
3.  `import readTodos from “../../lib/read_todos.ts”;`

5.  `export const handler: APIHandler = async ({request, response}) => {`
6.  `const todos = readTodos();`
7.  `…`

We will create another utility function named **`writeTodo`** in the **`lib/write_todo.ts`** file to persist the added Todo by writing it to the **`todos.json`** file.

1.  `// lib/write_todos.ts`
2.  `const writeTodos = (todos) =>`
3.  `Deno.writeTextFileSync(“db/todos.json”, JSON.stringify(todos));`

5.  `export default writeTodos;`

The typescript compiler shows a message for implicit any type for todos parameter as shown in the following figure:

![](images/Figure-5.14.jpg)

**Figure 5.14:** TypeScript warning for implicit any type

Let us fix this by adding an **`ITodo`** interface in the **`interfaces/ITodo.ts`** file.

1.  `// interfaces/ITodo.ts`
2.  `export default interface ITodo {`
3.  `id: number;`
4.  `title: string;`
5.  `}`

We will provide **`ITodo`** as a type for the Todos parameter in **`write_todos.ts`**. The bracket [] after ITodo indicates an ITodo array. The TypeScript warning should be gone now.

1.  **`/`**`/ utils/write_todos.ts`
2.  `import ITodo from “../interfaces/ITodo.ts”;`

4.  `const writeTodos = (todos: ITodo[]) =>`
5.  `…`

We will use the **`writeTodo`** function and **`ITodo`** interface in the **`index.ts`** file.

1.  `// api/todos/index.ts`
2.  `…`
3.  `   let todo = todos.find((_todo: ITodo) => _todo.title === title); // Modified code`
4.  `…`
5.  `    todos.push(todo);`
6.  `    writeTodos(todos); // New code`
7.  `…`

If you restart the server after adding a Todo, you should see the created Todo persists in the **`todos.json`** file and is included in the **`GET api/todos`** response.

# [GET (object), PATCH, and DELETE](#toc.xhtml_s102a)

We will now implement the remaining actions (**`GET`**,**`PUT`**, and**`DELETE`**). All these actions will be performed on the existing Todo. Hence, we will require a unique identifier like the id of the Todo to be passed as a parameter. We will achieve this with the use of the **Dynamic API Route**, which we learned previously in the API section.

As we learned in the **Routing** section, the bracket syntax is used to create a **Dynamic Route**. We will create the file **`api/todos/[id].ts`** with the following code:

1.  `// api/todos/[id].ts`
2.  `import type { APIHandler } from “aleph/types.d.ts”;`

4.  `export const handler:APIHandler = async ({request, response, router}) => {`
5.  `const id = parseInt(router.params.id);`
6.  `response.json({ id: id });`
7.  `}`

The function looks for id **`param`** (derived from **`[id].ts`** filename) in the **`router.params`** object. We are using the **`parseInt`** function to convert the id from string to integer. The parsed integer is then returned as a response.

If we hit the endpoint **`api/todos/3`**, we will get a response as shown in *[figure 5.15](#c05.xhtml_fig5_15)*.

![](images/Figure-5.15.jpg)

**Figure 5.15:** Dynamic API route

1.  `…`
2.  `import ITodo from “../interfaces/ITodo.ts”;`
3.  `import readTodos from “../../lib/read_todos.ts”;`

5.  `…`
6.  `const todos = readTodos();`
7.  `const id = parseInt(router.params.id);`
8.  `const todo = todos.find((_todo: ITodo) => _todo.id === id);`

10.  `if (todo) {`
11.  `  response.json(todo);`
12.  `} else {`
13.  `  response.status = 400;`
14.  `  response.json({ error: “Todo not found” });`
15.  `}`
16.  `…`

We will use the **`find`** function to get the existing Todo with provided id. If the Todo exists, we will return it, or else we will reply with **`404`** code, and a **`“Todo not found”`** error message.

Just like **`index.ts`**, we will use a switch statement to match **`request.method GET, PATCH, and DELETE`**. The modified code is shown as follows:

1.  `…`

3.  `import writeTodos from “../../lib/write_todos.ts”;`

5.  `…`
6.  `if (todo) {`
7.  `  switch (request.method) {`
8.  `   case “GET”:`
9.  `    response.json(todo);`
10.  `    break;`

12.  `   case “PATCH”:`
13.  `    let body;`
14.  `    try {`
15.  `     body = await request.json();`
16.  `    } catch (error) {`
17.  `     response.status = 400;`
18.  `     response.json({ error: error.message });`
19.  `     break;`
20.  `    }`

22.  `    const title = body.title ? lowerCase(body.title) : null;`
23.  `    if (!title) {`
24.  `     response.status = 400`
25.  `     response.json({`
26.  `      error: “title not provided”,`
27.  `     });`
28.  `     break;`
29.  `    }`

31.  `    todos.forEach((_todo: ITodo) => {`
32.  `     if (_todo.id === todo.id) {`
33.  `      _todo.title = title;`
34.  `     }`
35.  `    });`
36.  `    writeTodos(todos);`
37.  `    response.json(todo);`
38.  `    break;`

40.  `   case “DELETE”:`
41.  `    const _todos = todos.filter((_todo: ITodo) => _todo.id !== id);`
42.  `    writeTodos(_todos);`
43.  `    response.json({ message: “Deleted” });`
44.  `    break;`

46.  `   default:`
47.  `    response.status = 405;`
48.  `    response.json({ message: “Action not allowed” });`
49.  `    break;`
50.  `  }`
51.  `} else {`
52.  `…`

For **`GET`** method, we are simply returning the matched Todo. This **`GET`** method differs from the one in the **`index.ts`** file. It provides only a single todo (derived using provided id), whereas the **`GET`** in **`index.ts`** provides a list/array of all the todos.

For **`DELETE`**, we are filtering out the matched Todo from todos and then writing the updated todos to the **`todos.json`** file using the **`writeTodos`** function.

For **`PATCH`**, the initial code is similar to that of the **`POST`** method from **`index.ts`** file. We obtain an updated title from the JSON provided by **`readBody(“json”)`**. Then using **`forEach`**, we are updating only the matched Todo of todos data. The updated Todos is then saved to the file using the **`writeTodos`** function, and the updated Todo is replied.

# [Conclusion](#toc.xhtml_s103a)

The Todos App API endpoints have been implemented in this chapter. We can now use Postman, or curl to test them. We have also learned the features and basic concepts of Aleph.js.

The next phase will be to implement the UI for Todos App. We will check the unique features offered by Aleph.js for React Development and implement the UI in the upcoming chapter.

# [CHAPTER 6](#toc.xhtml_c06)

# [Todos App—UI Implementation](#toc.xhtml_c06)

# [Introduction](#toc.xhtml_s104a)

We have implemented REST APIs for Todos App in the previous chapter. We will implement UI for the same in this chapter. We will be using a Full Stack React framework named **aleph.js** for this purpose. We will also be using the **styled components** library to create UI components and the **axiod** to make network requests.

# [Structure](#toc.xhtml_s105a)

In this chapter, we will cover the following topics:

*   Styled components
    *   Card
    *   Text
    *   Button
    *   Input
    *   Checkbox
*   Todos components
    *   TodoList
    *   TodoDetails

# [Objective](#toc.xhtml_s106a)

After completion of this chapter, you will be able to create UI for react application using the aleph module. You should also be able to create custom components using styled components and integrate them into the app. You should also be able to make network requests using **`axiod`** module.

# [Styled components](#toc.xhtml_s107a)

Styled components is a React library that allows us to create components with css styles having a component-level scope. We will use this library to create components such as **`Button`**, **`Text`**, **`Card`**, and so on. Switch over to the **`todos-app`** folder from a terminal that was initialized in the previous chapter. To install styled-components, we will use the following **`trex`** command:

`trex -c styled=”https://esm.sh/styled-components@5.3.1”`

Once installed, we will create various components in **`StyledComponents.tsx`** file. The code for each component will be as follows:

1.  `import styled, { css } from “styled”`

3.  `` export const Card = styled.div` ``
4.  `    display: flex;`
5.  `    flex-direction: row;`
6.  `    background: #ddd;`
7.  `    border-radius: 5px;`
8.  `    margin: 10px;`
9.  `    justify-content: space-between;`
10.  `    align-items: center;`
11.  `    max-width: 600px;`
12.  `    margin: “auto”;`
13.  `` ` ``

15.  `` export const Text = styled.span` ``
16.  `    font-size: 20px;`
17.  `    font-weight: bold;`
18.  `    flex: 1;`
19.  `    margin-left: 10px;`
20.  ``      ${props => props.completed && css` ``
21.  `        text-decoration: line-through;`
22.  `        color: grey`
23.  ``     `}``
24.  `` ` ``
25.  `` export const Button = styled.button` ``
26.  `  /* Adapt the colors based on primary prop */`
27.  `  background: ${props => props.primary ? “palevioletred” : “white”};`
28.  `  color: ${props => props.primary ? “white” : “palevioletred”};`

30.  `  font-size: 1em;`
31.  `  margin: 1em;`
32.  `  padding: 0.25em 1em;`
33.  `  border: 2px solid palevioletred;`
34.  `  border-radius: 3px;`
35.  `  cursor: pointer;`
36.  ``   ${props => props.disabled && css` ``
37.  `      background: lightgrey;`
38.  `      cursor: not-allowed;`
39.  `      border: 2px solid lightgrey;`
40.  ``     ` ``
41.  `    }`
42.  `` `; ``

44.  `` export const Input = styled.input` ``
45.  `    flex:1;`
46.  `    padding: 10px;`
47.  `    margin: 10px;`
48.  `    border: none;`
49.  `    background: #ddd;`
50.  `    font-size: 20px;`
51.  `    font-weight: bold;`
52.  ``      ${props => props.completed && css` ``
53.  `        text-decoration: line-through;`
54.  `        color: grey`
55.  ``     `}``
56.  `` ` ``

58.  `` export const Checkbox = styled.input` ``
59.  `    type: “checkbox”;`
60.  `    color: red;`
61.  `    margin-left: 10px;`
62.  `` ` ``

64.  `` export const Header1 = styled.h1` ``

66.  `` ` ``

In the preceding code, we are styling various components such as **`Card`**, **`Button`**, **`Text`**, and so on using styled and css from **`styled`** components. Each component is then exported and used across the project. We are creating our own UI library using this approach.

We are passing a function to some components. These functions are used to set values based on props. We are using the **`completed`** prop in **`Text`** and **`Input`** components to adapt color and text decoration accordingly. We are using the **`primary`** flag in the **`Button`** component to adapt the color as per the prop.

# [Creating Todos components](#toc.xhtml_s108a)

We will now use the custom-styled components in **`TodoDetails`** and **`TodoList`** components. We will start by adding the **`TodoList`** component in **`pages/index.tsx`** file, which is the entry point of our project as follows:

1.  `import React from ‘react’`
2.  `import TodoList from “../components/TodoList.tsx”`

4.  `export default function Home() {`
5.  `  return <TodoList />`
6.  `}`

We will check the details of the **`TodoList`** component in the next section.

# [TodoList](#toc.xhtml_s109a)

This component will be used to add new Todo and list existing Todos. We will be using custom components from **`StyledComponents.tsx`** file for this purpose. The API calls will be made using **`axiod`** module. The code for this file is as follows:

1.  `// components/TodoList.tsx`

3.  `import React from ‘react’`
4.  `import { useDeno } from “https://deno.land/x/aleph/framework/react/mod.ts”;`
5.  `import axiod from “axiod”;`

7.  `import TodoDetails from “./TodoDetails.tsx”;`
8.  `import { Button, Card, Input, Header1 } from “./StyledComponents.tsx”;`

10.  `import readTodos from “../lib/read_todos.ts”;`

12.  `export default function Page() {`
13.  `  const _todos = useDeno(async () => {`
14.  `    return await readTodos();`
15.  `  }, { revalidate: 1 });`
16.  `  const [todos, setTodos] = React.useState(_todos);`
17.  `  const [todoInput, setTodoInput] = React.    useState(“”);`

19.  `  const getTodos = () => {`
20.  `    axiod.get(“/api/todos”).then((res) => {`
21.  `      console.log(res);`
22.  `      setTodos(res.data);`
23.  `    }).catch((err) => {`
24.  `      console.log(err);`
25.  `    });`
26.  `  };`

28.  `  const addTodo = () => {`
29.  `    if (!todoInput) {`
30.  `      alert(“Please enter a todo text”);`
31.  `      return;`
32.  `    }`
33.  `    axiod.post(“/api/todos”, { title: todoInput         }).then((res) => {`
34.  `      console.log(res);`
35.  `      getTodos();`
36.  `      alert(“Todo added successfully”);`
37.  `    }).catch((err) => {`
38.  `      console.log(err);`
39.  `      alert(“Error adding todo”);`
40.  `    });`
41.  `  };`
42.  `  return (`
43.  `    <>`
44.  `      <Header1>Todos</Header1>`
45.  `      <Card>`
46.  `        <Input`
47.  `          placeholder=”Add Todo”`
48.  `          value={todoInput}`
49.  `          onChange={(e) => setTodoInput(e.target.             value)}`
50.  `        />`
51.  `        <Button primary onClick={addTodo}>+</Button>`
52.  `      </Card>`
53.  `      {todos.map((todo: any) => <TodoDetails key={todo.id} getTodos={getTodos} todo={todo} />)}`
54.  `    </>`
55.  `  );`
56.  `}`

In the preceding code, we are importing the custom components, **`axiod`** module and **`readTodos`** function. We are also importing the **`useDeno`** function that allows Deno runtime usage in the component. We are fetching the Todos from JSON file in it. The state **`todos`** is used to store the list of Todos, whereas **`todoInput`** is used to store add Todo text box input.

We are using **`getTodos`** function to fetch Todos by making an API call using **`axiod`** module. The fetched Todos are then stored in **`todos`** state. Similarly, the **`addTodo`** function is used to make **`POST`** requests to add new Todo in the JSON file. We are passing **`todoInput`** as **`title`** in the request body. If the Todo is added successfully, we fetch the Todos using **`getTodos`** function.

The styled-components **`Header1`**, **Card**, **`Input`**, and **`Button`** are used for UI creation. **`TodoDetails`** component is used to render each Todo detail. We will check its details in the next section.

*[Figure 6.1](#c06.xhtml_fig6_1)* shows the **`TodoList`** component with Add Todo Input.

![](images/Figure-6.1.jpg)

**Figure 6.1:** TodoList component

# [TodoDetails](#toc.xhtml_s110a)

We will be using this component to render each added **`todo`** element. We will provide two actions, namely, **`Save`** and **`Delete`**. We will also use a **`checkbox`** element to mark the Todo as completed. The code for this component is written in **`TodoDetails.tsx`** file as follows:

1.  `// components/TodoDetails.tsx`

3.  `import React from “react”;`
4.  `import { Button, Card, Checkbox, Input, Text } from “./StyledComponents.tsx”;`
5.  `import axiod from “axiod”;`

7.  `interface ITodo {`
8.  `  id: number;`
9.  `  title: string;`
10.  `  completed: boolean;`
11.  `}`

13.  `interface IProps {`
14.  `  todo: ITodo;`
15.  `  getTodos: () => void;`
16.  `}`

18.  `function TodoDetails(props: IProps) {`
19.  `  const { todo, getTodos } = props;`
20.  `  const [isCompleted, setIsCompleted] = React.useState(todo.completed);`
21.  `  const [todoText, setTodoText] = React.useState(todo.title);`

23.  `  const editTodo = () => {`
24.  `    if (!todoText) {`
25.  `      alert(“Please enter a todo text”);`
26.  `      return;`
27.  `    }`
28.  ``    axiod.patch(`/api/todos/${todo.id}`, {``
29.  `      title: todoText,`
30.  `      completed: isCompleted,`
31.  `    }).then((res) => {`
32.  `      console.log(res);`
33.  `      alert(“Todo updated successfully”);`
34.  `    }).catch((err) => {`
35.  `      console.log(err);`
36.  `      alert(“Error updating todo”);`
37.  `      setTodoText(todo.title);`
38.  `    });`
39.  `  };`

41.  `  const deleteTodo = () => {`
42.  ``    axiod.delete(`/api/todos/${todo.id}`, { title: todoText }).then((res) => {``
43.  `      console.log(res);`
44.  `      alert(“Todo deleted successfully”);`
45.  `      getTodos();`
46.  `    }).catch((err) => {`
47.  `      console.log(err);`
48.  `      alert(“Error deleting todo”);`
49.  `    });`
50.  `  };`

52.  `  return (`
53.  `    <Card>`
54.  `      <Checkbox`
55.  `        type=”checkbox”`
56.  `        defaultChecked={isCompleted}`
57.  `        onChange={() => setIsCompleted(!isCompleted)}`
58.  `      />`
59.  `      <Input`
60.  `        completed={isCompleted}`
61.  `        value={todoText}`
62.  `        onChange={(e) => setTodoText(e.target.value)}`
63.  `        disabled={isCompleted}`
64.  `      />`
65.  `      <Button primary onClick={editTodo}>Save</Button>`
66.  `      <Button onClick={deleteTodo}>Delete</Button>`
67.  `    </Card>`
68.  `  );`
69.  `}`

71.  `export default TodoDetails;`

In the preceding code, we are importing custom-styled components **`Button`,** **`Card`,** **`Checkbox`,** **`Input`,** **`Text`,** and **`axiod`**. We then defined two interfaces **`ITodo`** (Todo details) with **`id`,** **`title`,** and **`completed`** fields and **`IProps`** (props passed by parent component) with **`todo`** and **`getTodos`** fields. We have also defined two states **`isCompleted`** (to mark Todo as completed) with **`todo.completed`** as the initial value and **`todoText`** (to store user input) with **`todo.title`** as the initial value.

We have defined two actions **`editTodo`** and **`deleteTodo`**, for updating the Todo and deleting the Todo, respectively. In **`editTodo`,** we check if the edited **`todoText`** is empty or not. We show the message if it is empty; else, we make a **`PATCH`** request using **`axiod`** passing **`todoText`** as **`title`** and **`isCompleted`** as **`completed`** flag. In **`deleteTodo`** action, we are passing **`todo.id`** as a param and fetching the Todos list if the delete request is successful.

*[Figure 6.2](#c06.xhtml_fig6_2)* shows the **`TodoDetails`** component with Save and Delete actions along with a checkbox.

![](images/Figure-6.2.jpg)

**Figure 6.2:** TodoDetails component

For the JSX part, we are using the **`Card`** element as a container. The **`Checkbox`** element has **`isCompleted`** as default value and the **`onChange`** function will invoke **`setIsCompleted`** function with negated **`isCompleted (!isCompleted)`**. The **`Input`** element has **`completed`** prop set to **`isCompleted`** value. This is done to change the styling of the element according to the flag as shown in the **`StyledComponents.tsx`** file. The element is bound with **`todoText`** using **`value`** and **`onChange`** attributes. The **`disabled`** flag is also set to **`isCompleted`** similar to **`completed`** flag. In the end, we are **`Button`** element with **`onClick`** attribute to **Edit** or **Delete** the Todo by invoking the respective function.

*[Figure 6.3](#c06.xhtml_fig6_3)* shows the **`TodoDetails`** component with completed status.

![](images/Figure-6.3.jpg)

**Figure 6.3:** TodoDetails component with completed status

# [Conclusion](#toc.xhtml_s111a)

We have created a UI for the Full Stack React application in this chapter. We used the Aleph framework for this purpose. We also used the Styled components module to create custom components. Axiod was used to make API calls.

This knowledge will be useful for creating a Full Stack App having API endpoints and UI using aleph. Our Todos App is completed, and we will create a different project in the upcoming chapters. We will create a GraphQL API server using **`oak`** and **`oak-graphql`** modules in the next chapter, and then we will create UI for a svelte app using snel module in the subsequent chapter.

# [CHAPTER 7](#toc.xhtml_c07)

# [Introduction to GraphQL, Oak, and Oak-GraphQL](#toc.xhtml_c07)

# [Introduction](#toc.xhtml_s112a)

We are going to learn the core **Graph Query Language** (**GraphQL**) concepts along with its features in this chapter. Once we cover the basics, we shall create an API server (GraphQL) for the *Phonebook* App using these concepts in the upcoming chapter. We will also introduce the *Oak Web* framework and *Oak GraphQL*. Both will be used for GraphQL API server implementation in the upcoming chapter.

# [Structure](#toc.xhtml_s113a)

In this chapter, we will cover the following topics:

*   GraphQL intro
    *   Features
        *   Precise fetching
        *   Single API endpoint
        *   Validation and type checking
        *   Fragments
        *   Auto-generated API docs
    *   Core concepts
        *   Schema
            *   Type
            *   Input
            *   Query
            *   Mutation
            *   Relationship
        *   Resolver
*   Introducing Oak framework
*   Introducing Oak-GraphQL

# [Objective](#toc.xhtml_s114a)

After completion of this chapter, you will be able to understand and apply GraphQL core concepts such as query, mutation, resolvers, type definitions, and so on. You should also be able to use the Oak framework to create Deno Web servers and the Oak-GraphQL module to create GraphQL servers.

# [Introducing GraphQL](#toc.xhtml_s115a)

GraphQL is an open-source query language for APIs developed by Facebook and released in 2015\. It allows the client to control the resolved data structure as opposed to a fixed data structure in REST. This way, the client can **query** only for the exact necessary data. It also allows **mutations (**writing or changing data) and **subscriptions** (subscribing to data updates). It is used by many large organizations, such as Facebook, GitHub, Coursera, and Pinterest, to name a few.

# [Features](#toc.xhtml_s116a)

GraphQL allows clients to *query or mutate* data across multiple resources in a single request. It creates a single entry point or API endpoint POST **/graphql** to query or mutate the data. GraphQL also provides resolved data in the same format as that of the requested query. Other GraphQL features are explained in detail as follows.

# [Precise fetching](#toc.xhtml_s117a)

By allowing the client to fetch only required data, GraphQL solves the data-related issues where the client gets more than required data (*over fetching***)** or less than required data (*under fetching***)**.

# [Single API endpoint](#toc.xhtml_s118a)

Unlike REST, GraphQL will always have a single Endpoint **/graphql (POST)**, which can be used by the client to fetch any data defined in the schema as GraphQL resolves the request using the *query* passed in the request body.

*[Figure 7.1](#c07.xhtml_fig7_1)* fetches **`users`** data using **/graphql** endpoint by providing the **`users`** query in the body as follows:

![](images/Figure-7.1.jpg)

**Figure 7.1:** Fetch users

*[Figure 7.2](#c07.xhtml_fig7_2)* fetches *Todos data* using the same endpoint **/graphql** by providing **`todos`** query in the body as follows:

![](images/Figure-7.2.jpg)

**Figure 7.2:** Fetch Todos

As shown in *[figures 7.1](#c07.xhtml_fig7_1)* and *[7.2](#c07.xhtml_fig7_2),* GraphQL allows fetching **`users`** and **`todos`** from a single API endpoint using **query** operation**.**

We can even fetch **users** and **todos** in a single request. This is a very powerful feature of GraphQL that lets the client get all the required data in a single request, which is extremely useful for devices with slower networks.

*[Figure 7.3](#c07.xhtml_fig7_3)* fetches both **`users`** and **`todos`** in a single request as follows:

![](images/Figure-7.3.jpg)

**Figure 7.3:** Fetch Users and Todos

# [Validation and type checking](#toc.xhtml_s119a)

GraphQL uses **a** **type system** to validate the query. The client can check which fields are available (with field type) and whether the query is valid or not before making the request.

*[Figure 7.4](#c07.xhtml_fig7_4)* demonstrates validation and type-checking concepts for **`todos`** where **`someField`** field is not defined in the schema as follows:

![](images/Figure-7.4.jpg)

**Figure 7.4:** Validation

# [Fragments](#toc.xhtml_s120a)

GraphQL allows writing a reusable code *fragment* that can be used across multiple queries. We can create a fragment that replaces the repeated code unit and makes the queries less cluttered and more readable.

*[Figure 7.5](#c07.xhtml_fig7_5)* shows code units repeated for **`todos`** (fetch all Todos) and **`todo`** (fetch single Todo by id) queries as follows:

![](images/Figure-7.5.jpg)

**Figure 7.5:** Repeated code unit

We will move the repeated code unit in the **`todoData`** fragment and use it with the *spread operator* (**`…`**) in both queries.

*[Figure 7.6](#c07.xhtml_fig7_6)* demonstrates the use of **`fragment`** for fetching **`todoData`** and **`userData`** as follows:

![](images/Figure-7.6.jpg)

**Figure 7.6:** Fragments

Fragments are very useful in complex queries used in multiple places with many fields.

# [Autogenerated API documentation](#toc.xhtml_s121a)

GraphQL generates API documentation using the schema for *queries* and *mutations*.

*[Figure 7.7](#c07.xhtml_fig7_7)* shows autogenerated API documentation for **`todo`** using schema.

![](images/Figure-7.7.jpg)

**Figure 7.7:** API docs

As the documentation is generated according to the schema, every change in the schema is synced and reflected in the docs.

If we change the **`user`** type from **`User`** to **`Int`**, docs will reflect it, as shown in *[figure 7.8](#c07.xhtml_fig7_8)*.

![](images/Figure-7.8.jpg)

**Figure 7.8:** Synced docs

# [Core concepts](#toc.xhtml_s122a)

GraphQL provides a *Schema* for defining the data model, *a Resolver* that *resolves* the *request*, along with actions like *query* for reading data, *mutations* for writing data, and *subscription* for subscribing to real-time data. We will cover these concepts in the following section.

# [Schema](#toc.xhtml_s123a)

A Schema (*a type system*) is a contract between client and server that defines the shape of the data. The schema defines *types* that describe an entity or field and the relationship between types. It lets the client discover available *data fields*, *queries***,** and *mutations*. The client uses this schema to define the structure of resolved data.

GraphQL uses **Schema Definition Language** (**SDL**) to define the schema. A schema for a sample Todos app can be defined as follows:

1.  `  type User {`
2.  `    userId: String!`
3.  `    name: String! # Scalar Type`
4.  `    todos: [Todo!]! # Object Type`
5.  `  }`

7.  `  type Todo {`
8.  `    todoId: String!`
9.  `    title: String!`
10.  `    user: User!`
11.  `  }`

13.  `  input UserInput {`
14.  `    name: String!`
15.  `  }`

17.  `  input TodoInput {`
18.  `    title: String!`
19.  `    userId: String!`
20.  `  }`

22.  `  type Query {`
23.  `    todos: [Todo!]!`
24.  `    todo(todoId: String!): Todo!`
25.  `    users: [User!]!`
26.  `    user(userId: String!): User!`
27.  `  }`

29.  `  type Mutation {`
30.  `    addTodo(todo: TodoInput!): Todo`
31.  `    addUser(user: UserInput!): User`
32.  `  }`

This schema can also be viewed via *GraphQL playground,* as shown in *[figure 7.9](#c07.xhtml_fig7_9)*.

![](images/Figure-7.9.jpg)

**Figure 7.9:** GraphQL schema

Let us explain various keywords (**`type`** and **`input`**) used in the preceding schema:

# [Type](#toc.xhtml_s124a)

Type is used to define the shape of the resolved query. The schema shown in *[figure 7.9](#c07.xhtml_fig7_9)* defines two Object types **`User`** and **`Todo`.** **`User`** type defines fields **`userId`,** **`name`**, and **`todos`** (an array of **`Todo`** object type). **`Todo`** type defines fields **`todoId`**, **`title`**, and **`user`** (of type **`User`**). Both object types are used by the **`Query`** type while returning the corresponding data.

# [Input](#toc.xhtml_s125a)

Input is used to define the shape of client input during *mutation*. It defines two *input types*, **`UserInput`** and **`TodoInput`**. **`UserInput`** accepts a **`name`** argument, and **`TodoInput`** accepts **`title`** and **`userId`** arguments. Both Input types are used for creating or updating the corresponding entity by the *mutation* type.

# [Query](#toc.xhtml_s126a)

Defines entry points for **`read`** operations to be executed by the client. Four fields **`todos`**, **`todo`**, **`users`**, and **`user`** are defined in the query. **`todos`** and **`users`** fields accept no arguments and return array corresponding types. **`todo`** and **`user`** fields accept the **`id`** of the entity and return the entity of corresponding types.

# [Mutation](#toc.xhtml_s127a)

Defines entry points for **write** operations to be executed by the client. **`addTodo`** and **`addUser`** fields are defined in this type. **`addTodo`** accepts arguments of type **`TodoInput`** and returns data of type **`Todo`,** whereas **`addUser`** accepts arguments of type **`UserInput`** and returns data of type **`User`**.

# [Relationship](#toc.xhtml_s128a)

The Todos schema defines the relationship of type *one-to-many* between **`User`** and **`Todo`** types. It means every *Todo* has *one* user, and every *user* has *many* Todos**.**

As shown in *[figure 7.10](#c07.xhtml_fig7_10)*, GraphQL gives flexibility to the client to fetch all user-related Todos in a single query.

![](images/Figure-7.10.jpg)

**Figure 7.10:** Relationships

# [Resolver](#toc.xhtml_s129a)

A resolver is a function used to *resolve* a *query* or *mutation* by populating data for a single field in a schema. The following code demonstrates the use of *resolvers* for a previously defined schema**:**

1.  `export const resolvers = {`
2.  `  Query: {`
3.  `    todos: (parent: any, args: any, context: any, info: any) => {`
4.  `      if (args.userId) return getTodosByUserId(args.userId);`
5.  `      return getTodos();`
6.  `    },`
7.  `    todo: async (parent: any, args: any, context: any, info: any) => {`
8.  `      return getTodo(args._id);`
9.  `    },`
10.  `    users: (parent: any, args: any, context: any, info: any) => {`
11.  `      return getUsers();`
12.  `    },`
13.  `    user: async (parent: any, args: any, context: any, info: any) => {`
14.  `      return getUser(args._id);`
15.  `    },`
16.  `  },`
17.  `  Mutation: {`
18.  `    addTodo: async (parent: any, args: any, context: any, info: any) => {`
19.  `      const { title, userId } = args.todo;`
20.  `      return createTodo(title, userId);`
21.  `    },`
22.  `    addUser: async (parent: any, args: any, context: any, info: any) => {`
23.  `      const { name } = args.user;`
24.  `      const user = createUser(name);`
25.  `      return user;`
26.  `    },`
27.  `  },`
28.  `  Todo: {`
29.  `    title: (parent: any, args: any, context: any, info: any) => {`
30.  `      return parent.title;`
31.  `    },`
32.  `    user: async (parent: any, args: any, context: any, info: any) => {`
33.  `      const user = await info.rootValue.Query.user(`
34.  `        parent,`
35.  `        { _id: parent.userId },`
36.  `        context,`
37.  `        info`
38.  `      );`
39.  `      return user;`
40.  `    },`
41.  `  },`
42.  `  User: {`
43.  `    name: (parent: any, args: any, context: any, info: any) => {`
44.  `      return parent.name;`
45.  `    },`
46.  `    todos: async (parent: any, args: any, context: any, info: any) => {`
47.  `      const todos = await resolvers.Query.todos(`
48.  `        parent,`
49.  `        { userId: parent._id },`
50.  `        context,`
51.  `        info`
52.  `      );`
53.  `      return todos;`
54.  `    },`
55.  `  },`
56.  `};`

Let us see what is happening in the preceding code. We define **`Query`**, **`Mutation`**, **`Todo`**, and **`User`** objects. **`Query`** object contains **`todos`** (list), **`todo`**, **`users`**, and **`user`** objects. Similarly, **`Mutation`** contains **`addTodo`** and **`addUser`** objects, each with the same signature. The other objects **`User`** and **`Todo`** are required for resolving internal fields (title and so on) of the respective type. The data can then be fetched from various sources. Each object mentioned previously accepts optional parameters: parent**,** **`args`,** **`context`**, and **`info`**.

The **`parent`** is the return value for the field’s parent, and **`args`** contains all the provided GraphQL arguments, a **`context`** is an object whose content is available across all resolvers, and **info** contains information such as field name, path, and so on.

# [Introducing Oak framework](#toc.xhtml_s130a)

Oak is a Web framework for Deno, inspired by the *koa* framework of node.js. It provides middleware functions that are invoked in between the request and the response. Oak provides the **`use()`** method to use the middleware function. The following code demonstrates the **`Hello World`** server in oak**:**

1.  `import { Application } from “https://deno.land/x/oak@v7.7.0/mod.ts”;`

3.  `const app = new Application();`

5.  `app.use((ctx) => {`
6.  `  ctx.response.body = “Hello World!”;`
7.  `});`

9.  `await app.listen({ port: 8000 });`

In the preceding code, the **`Application`** instance **`app`** invokes each middleware with *context*, which contains necessary info such as **`app`**, **`cookies`**, **`request`**, **`response`**, **`state`**, **`assert()`**, and **`throw()`**. Finally, the server starts listening on port **`8000`** for incoming requests using **`listen()`** method.

# [Introducing Oak-GraphQL middleware](#toc.xhtml_s131a)

Oak-GraphQL module allows us to create a GraphQL API on top of the oak server. We will be using Oak-GraphQL middleware for GraphQL API implementation. A simple Hello World GraphQL API can be set up as follows:

1.  `// oak_graphql_server.ts`

3.  `import {`
4.  `  Application,`
5.  `  Router,`
6.  `  RouterContext,`
7.  `} from “https://deno.land/x/oak@v9.0.0/mod.ts”;`
8.  `import {`
9.  `  applyGraphQL,`
10.  `  gql,`
11.  `  GQLError,`
12.  `} from “https://deno.land/x/oak_graphql/mod.ts”;`

14.  `const app = new Application();`
15.  `` const types = gql` ``
16.  `  type Query {`
17.  `    hello(name: String): String`
18.  `  }`
19.  `` `; ``

21.  `const resolvers = {`
22.  `  Query: {`
23.  `    hello: (parent: any, { name }: any, context: any, info: any) => {`
24.  `      if (!name) throw new GQLError(“Name not provided”);`
25.  ``      return `Hello ${name}`;``
26.  `    },`
27.  `  },`
28.  `};`

30.  `const GraphQLService = await applyGraphQL<Router>({`
31.  `  Router,  // Same as Router: Router,`
32.  `  typeDefs: types,`
33.  `  resolvers: resolvers,`
34.  `});`

36.  `app.use(GraphQLService.routes(), GraphQLService.allowedMethods());`

38.  `console.log(“Server listening on http://localhost:8080/graphql”);`
39.  `await app.listen({ port: 8080 });`

Preceding code imports required methods and classes from **`oak`** (Application, Router, and RouterContext) and **`oak-graphql`** (applyGraphQL, gql, and GQLError). After creating an **`Application`** instance, type definitions are defined using **`gql`** along with **resolvers** for the type definitions.

A **`GraphQLService`** is then created using the **`applyGraphQL`** function that accepts an object with a **`Router`**, **`typeDefs`**, and **`resolvers`**. Middlewares **`GraphQLService.routes()`**, **`GraphQLService.allowedMethods()`** are then added to the **`app`** using the **`use()`** method. Finally, the server starts and listens to incoming requests using the **`listen()`** method on port 8080.

If we run the preceding code with the command **`deno run --allow-net oak_graphql_server.ts`** and open URL **http://localhost:8080/graphql** with query **`{ hello(name: “ABC”) }`** we should see the results shown in *[figure 7.11](#c07.xhtml_fig7_11)* as follows:

![](images/Figure-7.11.jpg)

**Figure 7.11:** GraphQL API Hello World

# [Conclusion](#toc.xhtml_s132a)

We have covered the basic features and concepts of GraphQL, such as schema, resolver along with type, query, and mutation. We also introduced the oak framework used to create a Web server along with the Oak-GraphQL module used to create a GraphQL server.

We will use the preceding GraphQL concepts to create a GraphQL API server for the PhoneBook App using Oak and Oak-GraphQL modules in the upcoming chapter.

# [CHAPTER 8](#toc.xhtml_c08)

# [PhoneBook App—API Implementation](#toc.xhtml_c08)

# [Introduction](#toc.xhtml_s133a)

We will implement **Graph Query Language** (**GraphQL**) **Application Programming Interface** (**API**) server in this chapter. The basics of GraphQL we learnt previously will be applied in this chapter for API implementation. We will use **`oak`** and **`oak-graphql`** modules (introduced previously) to implement the API server.

# [Structure](#toc.xhtml_s134a)

In this chapter, we will cover the following topics:

*   Initial setup
    *   Version control using git
    *   Trex as the package manager
    *   Velociraptor as script runner
*   Oak GraphQL Server setup
*   Schema
*   Resolvers
*   DenoDB setup
    *   DB
        *   ElephantSQL PostgreSQL setup
    *   Models
        *   User
        *   Contact
    *   Controllers
*   Authentication

# [Objective](#toc.xhtml_s135a)

After completion of this chapter, you will be able to create GraphQL API server using **`Oak`** and **`Oak-GraphQL`** modules. You will learn the use of **Object–relational mapping** (**ORM**) using the **`denodb`** module to connect to different databases such as MySQL, PostgreSQL, NoSQL, and so on. You will also learn the use of **JSON Web Token** (**JWT**) to authenticate users using **`djwt`** module. You will also learn to setup a Deno server project using **`trex`** and **`velociraptor`** modules.

# [Initial setup](#toc.xhtml_s136a)

We will start coding by initiating a git repository. Then we shall install the **`oak`** and **`oak-graphql`** modules for creating Web server. We will use **`trex`** package management module for installing these modules.

# [Version control using git](#toc.xhtml_s137a)

*[Figure 8.1](#c08.xhtml_fig8_1)* shows git repo initialization, installation of **`trex`** module, and installation of **`oak`** and **`oak-graphql`** using **`trex`** module.

![](images/Figure-8.1.jpg)

**Figure 8.1:** Initial setup

# [Trex as the package manager](#toc.xhtml_s138a)

Trex caches installed packages and add them to the **`import_map.json`** file. *[Figure 8.2](#c08.xhtml_fig8_2)* shows the list of installed modules (**`oak`**, **`oak-graphql`**) in the **`import_map.json`** file.

![](images/Figure-8.2.jpg)

**Figure 8.2:** Installed modules in import_map.json

The installed modules can then be accessed as follows:

1.  `import { Application } from “oak”;`

# [Velociraptor as script runner](#toc.xhtml_s139a)

Create a file named **`mod.ts`** in **`src`** folder with the following code:

1.  `console.log(“Hello Velociraptor!”);`

What is velociraptor, you would ask. It is a script runner module for Deno. We will install velociraptor and run the **`mod.ts`** file using it. Velociraptor can be installed using **[https://nest.land/](https://nest.land/)** package registry as follows:

1.  `deno install -qAn vr https://x.nest.land/velociraptor@1.1.0/cli.ts`

We will now create **`scripts.yaml`** file to add the script to run the **`mod.ts`** file. Velociraptor detects files named **`scripts`** or **`velociraptor`** with extension **`yml`**, **`yaml`**, **`json`**, and **`ts`** as script files.

*[Figure 8.3](#c08.xhtml_fig8_3)* shows **`scripts.yaml`** file with **`dev`** script that executes **`src/mod.ts`** file.

![](images/Figure-8.3.jpg)

**Figure 8.3:** scripts.yaml file

If we run **`vr`** command in the terminal, we will see a list of available scripts. We can then run the available script as follows:

1.  `vr dev`

*[Figure 8.4](#c08.xhtml_fig8_4)* shows commands to list available scripts and run a script.

![](images/Figure-8.4.jpg)

**Figure 8.4:** Velociraptor CLI

We have setup a Deno server project using trex and velociraptor. Now, we will set up a Web server in the next section.

# [Oak GraphQL server setup](#toc.xhtml_s140a)

We will setup a simple GraphQL server using **`oak`** and **`oak-graphql`** modules. We will use **`oak-graphql`** code from previous *[Chapter 7, Introduction to GraphQL, Oak, and Oak-GraphQL](#c07.xhtml)* to setup the server with few changes. We no longer need to mention the module URL. Instead, we can mention the module name mentioned in the **`import_map.json`** file.

1.  `import { Application, Router } from “oak”;`
2.  `import { applyGraphQL, gql, GQLError } from “oak_graphql”;`

We will structure the project by having **`mod.ts`** (main file), **`middlewares.ts`** (GraphQL Middleware), **`schema.ts`** (GraphQL schema/type definitions), and **`resolvers.ts`** (GraphQL Resolver) files.

*[Figure 8.5](#c08.xhtml_fig8_5)* shows the project structure with the preceding files:

![](images/Figure-8.5.jpg)

**Figure 8.5:** Project structure

We will write code for each file one by one, starting from the **`mod.ts`** file as follows:

1.  `// src/mod.ts`
2.  `import { Application} from “oak”;`
3.  `import {GraphQLService} from “./middlewares.ts”`

5.  `const app = new Application();`

7.  `app.use(GraphQLService.routes(), GraphQLService.allowedMethods());`

9.  `console.log(“Server listening on http://localhost:8080/graphql”);`
10.  `await app.listen({ port: 8080 });`

In the preceding code, we are creating oak server with GraphQL Middleware called **`GraphQLService`** that can be accessed at **`/graphql`** route.

1.  `// src/schema.ts`
2.  `import { gql } from “oak_graphql”;`

4.  `` export const types = gql` ``
5.  `  type Query {`
6.  `    hello(name: String): String`
7.  `  }`
8.  `` `; ``

In the **`schema.ts`** file, we have defined a **`hello`** query that accepts **`name`** argument. GraphQL validates incoming requests according to data models defined in **`types`**. The incoming request will then be resolved by **`resolvers`**.

1.  `// src/resolvers.ts`
2.  `import { GQLError } from “oak_graphql”;`

4.  `export const resolvers = {`
5.  `  Query: {`
6.  `    hello: (parent: any, { name }: any, context: any, info: any) => {`
7.  `      if (!name) throw new GQLError(“Name not provided”);`
8.  ``      return `Hello ${name}`;``
9.  `    },`
10.  `  },`
11.  `};`

We need to update **`scripts.yaml`** file for **`import_map`** file path and permissions. The file after the update will have the following code:

1.  `# scripts.yaml`
2.  `imap: import_map.json`
3.  `unstable: true`
4.  `allow:`
5.  `  - net`
6.  `scripts:`
7.  `  dev:`
8.  `    cmd: src/mod.ts`
9.  `    desc: “run graphql server in dev mode”`
10.  `    watch: true`

In the preceding code, **`imap`** points to **`import_map`** file path, **`unstable`** flag allows unstable Deno features to be executed, and **`allow`** includes **`net`** for allowing network access. We have also added **`cmd`** (execution command)**,** **`desc`** (description), and **`watch`** (file watcher) fields to **`dev`** command.

# [Schema](#toc.xhtml_s141a)

Schema is a type of system that defines the shape of data. It provides available data fields, queries, and mutations to clients. We have already learned schema-related concepts in the following chapter with code. We will add **types**, **queries**, and **mutations** for **`User`** and **`Contact`** entities as shown in the following code:

1.  `// src/schema.ts`
2.  `import { gql } from “oak_graphql”;`

4.  `` export const types = gql` ``
5.  `  type User {`
6.  `    userId: String!`
7.  `    name: String!`
8.  `    contacts: [Contact!]!`
9.  `    email: String!`
10.  `  }`

12.  `  type Contact {`
13.  `    contactId: String!`
14.  `    name: String!`
15.  `    phone: String`
16.  `    email: String`
17.  `    address: String`
18.  `    user: User!`
19.  `  }`

21.  `  type Login {`
22.  `    token: String!`
23.  `  }`

25.  `  input RegisterUserInput {`
26.  `    name: String!`
27.  `    email: String!`
28.  `    password: String!`
29.  `  }`

31.  `  input LoginUserInput {`
32.  `    email: String!`
33.  `    password: String!`
34.  `  }`

36.  `  input UpdateUserInput {`
37.  `    name: String`
38.  `  }`

40.  `  input CreateContactInput {`
41.  `    name: String!`
42.  `    phone: String`
43.  `    email: String`
44.  `    address: String`
45.  `  }`

47.  `  input UpdateContactInput {`
48.  `    contactId: String!`
49.  `    name: String`
50.  `    phone: String`
51.  `    email: String`
52.  `    address: String`
53.  `  }`

55.  `  type Query {`
56.  `    user: User`

58.  `    contacts: [Contact]`
59.  `    contact(contactId: String!): Contact`

61.  `    login(user: LoginUserInput): Login`
62.  `  }`

64.  `  type Mutation {`
65.  `    registerUser(user: RegisterUserInput!): User`
66.  `    deleteUser: Boolean`
67.  `    updateUser(user: UpdateUserInput!): Boolean`

69.  `    addContact(contact: CreateContactInput!): Contact`
70.  `    deleteContact(contactId: String!): Boolean`
71.  `    updateContact(contact: UpdateContactInput!): Boolean`
72.  `  }`
73.  `` `; ``

We have defined various **types** and **inputs** in the preceding code. Let us explain them one by one.

# User type

We are defining fields **`userId`**, **`name`**, **`contacts`**, and **`email`** for this type. The client receives user-related data as per this type. Let us explain each one of the fields. An exclamation mark “!” after the field type denotes a non-nullable type.

*   **`userId`**: identifier or primary key
*   **`name`**: user’s name
*   **`contacts`**: user’s contacts in array
*   **`email`**: user’s email

# Contact type

We are defining fields **`userId`**, **`name`**, **`contacts`**, and **`email`** for this type. The client receives user-related data as per this type. Let us explain each one of the fields. An exclamation mark “!” after the field type denotes a non-nullable type.

*   **`contactId`**: Identifier or primary key
*   **`name`**: Name of the contact
*   **`phone`**: Phone number of the contact
*   **`email`**: Email of the contact
*   **`address`**: Address of the contact
*   **`user`**: userId of the creator of the contact

# Login type

We are defining a **`token`** field in this type.

*   **token:** Access token used to access protected API endpoints and identify requesting users.

# RegisterUser Input

We are defining **`name`**, **`email`**, and **`password`** in this input type. It will be used as a **`mutation`** to create a user.

*   **`name`**: Name of the user
*   **`Email`**: Email of the user.
*   **`Password`**: Password of the user.

# LoginUser Input

We are defining **`email`** and **`password`** in this input type. Email and password created during registration will be used to authenticate the user and return the token.

*   **`Email`**: Email of the user.
*   **`Password`**: Password of the user.

# UpdateUser Input

We are defining a single field **`name`** for this input. It will be used to update user information.

# CreateContact and UpdateContact Input

Here, we are defining **`name`**, **`email`**, **`phone`**, and **`address`** fields for these types. Both types have identical fields, whereas **`UpdateContact`** has an extra field **`contactId`,** which is used to identify the contact to be updated.

# Query Type

We have defined **`login`**, **`user`**, **`contacts`**, and **`contact`** queries for reading operations. **`Login`** query accepts input **user** of type **`LoginUserInput`** and returns data of **`Login`** type. **`user`** query returns details of the currently authenticated user.

**`contacts`** query returns an array of contacts added by the current user. It returns an array of **`Contact`** type. **`Contact`** query returns single **Contact** data using contactId.

# Mutation Type

We have defined **`registerUser`,** **`deleteUser`,** **`updateUser`,** **`addContact`,** **`deleteContact`**, and **`updateContact`** queries for write operations. These queries perform create, update, and delete operations on User and Contact entities.

# Resolvers

Queries and mutations defined in the schema previously will be *resolved* by the resolver for the respective query/mutation. Each resolver will perform database operations and return data for the query/mutation. The code for each resolver is as follows:

1.  `import {`
2.  `  getUser,`
3.  `  getUserByEmail,`
4.  `  createUser,`
5.  `  deleteUser,`
6.  `  updateUser,`
7.  `  getContactsByUserId,`
8.  `  getContact,`
9.  `  createContact,`
10.  `  deleteContact,`
11.  `  updateContact,`
12.  `  userLoader,`
13.  `} from “./controllers.ts”;`
14.  `import { authenticate } from “./auth.ts”;`
15.  `import { GQLError } from “oak_graphql”;`

17.  `export const resolvers = {`
18.  `  Query: {`
19.  `    user: async (parent: any, args: any, context: any, info: any) => {`
20.  `      if (!context?.userId) throw new GQLError(“Authentication error”);`
21.  `      return getUser(context.userId);`
22.  `    },`
23.  `    contacts: (parent: any, args: any, context: any, info: any) => {`
24.  `      if (!context?.userId) throw new GQLError(“Authentication error”);`
25.  `      return getContactsByUserId(context.userId);`
26.  `    },`
27.  `    contact: async (parent: any, args: any, context: any, info: any) => {`
28.  `      if (!context?.userId) throw new GQLError(“Authentication error”);`
29.  `      return getContact(args.contactId);`
30.  `    },`
31.  `    login: async (parent: any, args: any, context: any, info: any) => {`
32.  `      const { email, password } = args.user;`
33.  `const user = await getUserByEmail(email);`
34.  ``      if (!user) throw new GQLError(`Invalid email or password`);``
35.  `      const authToken = await authenticate(user, password);`
36.  ``      if (!authToken) throw new GQLError(`Invalid email or password`);``
37.  `      return { token: authToken };`
38.  `    },`
39.  `  },`
40.  `  Mutation: {`
41.  `    registerUser: async (parent: any, args: any, context: any, info: any) => {`
42.  `      const { name, email, password } = args.user;`
43.  `      const user = await createUser(name, email, password);`
44.  `      console.log(“created user :>> “, user);`
45.  `      return user;`
46.  `    },`
47.  `    deleteUser: async (parent: any, args: any, context: any, info: any) => {`
48.  `      if (!context?.userId) throw new GQLError(“Authentication error”);`
49.  `      return deleteUser(context.userId);`
50.  `    },`
51.  `    updateUser: async (parent: any, args: any, context: any, info: any) => {`
52.  `      if (!context?.userId) throw new GQLError(“Authentication error”);`
53.  `      const { name, isActive } = args.user;`
54.  `      return updateUser(context.userId, { name, isActive });`
55.  `    },`

57.  `    addContact: async (parent: any, args: any, context: any, info: any) => {`
58.  `      if (!context?.userId) throw new GQLError(“Authentication error”);`
59.  `      const contact = await createContact(args.contact, context.userId);`
60.  `      console.log(“created user :>> “, contact);`
61.  `      return contact;`
62.  `    },`
63.  `    deleteContact: async (parent: any, args: any, context: any, info: any) => {`
64.  `      if (!context?.userId) throw new GQLError(“Authentication error”);`
65.  `      return deleteContact(args.contactId);`
66.  `    },`
67.  `    updateContact: async (parent: any, args: any, context: any, info: any) => {`
68.  `      if (!context?.userId) throw new GQLError(“Authentication error”);`
69.  ``      console.log(`args`, args);``
70.  `      const { contactId, …contactData } = args.contact;`
71.  `      if (contactId) return updateContact(contactId, contactData);`
72.  `    },`
73.  `  },`
74.  `  User: {`
75.  `    name: (parent: any, args: any, context: any, info: any) => {`
76.  `      return parent.name;`
77.  `    },`
78.  `    contacts: async (parent: any, args: any, context: any, info: any) => {`
79.  `      const contacts = await resolvers.Query.contacts(`
80.  `        parent,`
81.  `        {},`
82.  `        context,`
83.  `        info`
84.  `      );`
85.  `      return contacts;`
86.  `    },`
87.  `  },`
88.  `  Contact: {`
89.  `    name: (parent: any, args: any, context: any, info: any) => {`
90.  `      return parent.name;`
91.  `    },`
92.  `    user: async (parent: any, args: any, context: any, info: any) => {`
93.  `      return await userLoader.load(parent.userId);`
94.  `    },`
95.  `  },`
96.  `};`

Our code for resolvers is based on the resolver code from the previous chapter. We have defined **`Query`**,**`Mutation`**,**`User`**, and**`Contact`** objects, each containing resolvers. **`Query`** object contains **`user`,** **`contacts`**,**`contact`**, and**`login`** resolvers**.** **`Mutation`** contains **`registerUser`**,**`updateUser`**,**`deleteUser`**,**`addContact`**,**`updateContact`**, and**`deleteContact`** resolvers. The other objects, **`User`** and**`Contact`**, are useful for resolving internal fields (name, and so on) of the respective type. The data can then be fetched from various sources. Each resolver function accepts optional parameters **`parent`,** **`args`**,**`context`**, and**`info`**, which are already explained in the previous chapter.

*[Figure 8.6](#c08.xhtml_fig8_6)* shows a list of all the resolvers from the **`resolvers.ts`** file

![](images/Figure-8.6.jpg)

**Figure 8.6:** Resolvers

While resolving a query, we need to perform operations such as read/write database, authentication, and so on. We are handling database operations in the **`controllers.ts`** file and authentication in the **`auth.ts`** file.

We will perform, create, update, and delete operations on database models **`User`** and **`Contact`** defined in the **`models.ts`** file. We need to set up a database and link it with the models in order to use the models in controllers. Let us set up a database and create models using the Deno module named **`denodb`**.

# [Database setup](#toc.xhtml_s142a)

We will set up a PostgreSQL database using **`ElephantSQL`**. Head over to **[https://www.elephantsql.com/](https://www.elephantsql.com/)** and login/signup with your account. Once done, we need to create an instance named **`phonebook`** with a **tiny turtle (**free) plan. Open the created instance and copy the **`URL`** mentioned in the **`Details`** section. We will set an environment variable named **`DATABASE_URL`** in the **`.env`** file as follows:

1.  `//  .env`
2.  `// Replace following url with elephantsql url`
3.  `DATABASE_URL=postgres://deno_admin:deno_admin@localhost:5432/deno_db`

Now, to access **`DATABASE_URL`** in the code, we will add **`envFile`** flag with **`.env`** file in **`scripts.yaml`** file as follows:

1.  `# scripts.yaml`
2.  `…`
3.  `allow:`
4.  `  - net`
5.  `  - env`
6.  `envFile:`
7.  `  - .env`
8.  `…`

Install **`denodb`** using **`trex i -c https://deno.land/x/denodb/mod.ts`** command and use **`PostgresConnector`** to connect with the database URL in the **`db.ts`** file as follows:

1.  `import { Database, PostgresConnector } from “denodb”;`

3.  `const DATABASE_URL = Deno.env.get(“DATABASE_URL”) as string;`

5.  `const connector = new PostgresConnector({`
6.  `  uri: DATABASE_URL,`
7.  `});`

9.  `export const db = new Database(connector);`

The preceding database will be used and linked with database models **`User`** and **`Contact`** in the next section.

# [Models](#toc.xhtml_s143a)

We will define two models, **`User`** and **`Contact`**, using **Model, DataTypes,** and **Relationships** from **`denodb`** module. The code for both models is as follows:

1.  `// src/models.ts`

3.  `import { Model, DataTypes, Relationships } from “denodb”;`
4.  `import { db } from “./db.ts”;`
5.  `import { v4 } from “uuid”;`

7.  `export class User extends Model {`
8.  `  static table = “users”;`
9.  `  static timestamps = true;`

11.  `  static fields = {`
12.  `    userId: {`
13.  `      type: DataTypes.STRING,`
14.  `      primaryKey: true,`
15.  `    },`
16.  `    name: { type: DataTypes.STRING, length: 50 },`
17.  `    isActive: { type: DataTypes.BOOLEAN },`
18.  `    email: { type: DataTypes.STRING },`
19.  `    password: { type: DataTypes.STRING },`
20.  `  };`

22.  `  static defaults = {`
23.  `    userId: v4.generate,`
24.  `    name: “ABC”,`
25.  `    isActive: true,`
26.  `  };`

28.  `  static contacts() {`
29.  `    return this.hasMany(Contact);`
30.  `  }`
31.  `}`

33.  `export class Contact extends Model {`
34.  `  static table = “contacts”;`
35.  `  static timestamps = true;`

37.  `  static fields = {`
38.  `    contactId: {`
39.  `      type: DataTypes.STRING,`
40.  `      primaryKey: true,`
41.  `    },`
42.  `    name: { type: DataTypes.STRING, length: 100 },`
43.  `    phone: { type: DataTypes.STRING, length: 50, allowNull: true },`
44.  `    email: { type: DataTypes.STRING, length: 100, allowNull: true },`
45.  `    address: { type: DataTypes.STRING, length: 200, allowNull: true },`
46.  `  };`

48.  `  static defaults = {`
49.  `    contactId: v4.generate,`
50.  `    name: “Learn Deno”,`
51.  `    isCompleted: false,`
52.  `  };`

54.  `  static user() {`
55.  `    return this.hasOne(User);`
56.  `  }`
57.  `}`

59.  `Relationships.belongsTo(Contact, User);`

61.  `db.link([User, Contact]);`
62.  `await db.sync({ drop: true });`

For both models, we have defined **`table`**,**`timestamps`**,**`fields`**,**`defaults`,** and **`relationship`** static properties**.** The **`table`** will be the name of the database table for the model, e.g., **`users`** from **`User`** model and **`contacts`** for **`Contact`** model. We will set **`timestamps`** to true in order to add **`created_at`** **and** **`updated_at`** fields to the model.

The **`fields`** property will contain all the model fields defined with the **`type (INTEGER, STRING,`** and so on**`)`**, **`length (max length)`**, **`allowNull (nullable)`**, and **`primaryKey`**. We can also provide default values to the fields using the **`defaults`** property. Here, we are using the **`v4.generate`** function provided by **uuid** (standard Deno module) to generate **`UUID`** for **`userId`** **and** **`contactId`** fields. Make sure you have installed **uuid** module using the following command:

1.  `trex -c uuid=https://deno.land/std@0.132.0/uuid/mod.ts`

Then, we added query methods to query relationship value **`contacts`** for User and **`user`** for contact**.**

*   **`this.hasMany(Contact)`** will return **`Contact`** instances where **`Contact.userId`** matches **`User.userId`**.
*   **`this.hasOne(User)`** will return **`User`** instance where **`User.userId`** matches **`Contact.userId`**.

We will then add a foreign key using the **`Relationships.belongsTo`** method. The database link is done afterward using the **`link`** method. Finally, models are synchronized using the **`sync`** method with a **`drop`** flag to remove existing records.

# [Controllers](#toc.xhtml_s144a)

We need to map resolvers with models via controllers. Each controller will perform database operations on models to get, create, update, and delete an entity. All the controller functions are added in the **`controllers.ts`** file as follows:

1.  `import { User, Contact } from “./models.ts”;`
2.  `import { GQLError } from “oak_graphql”;`
3.  `import DataLoader from “dataloader”;`
4.  `import { hash } from “scrypt”;`

6.  `interface IContact {`
7.  `  name: string;`
8.  `  phone: string;`
9.  `  email: string;`
10.  `  address: string;`
11.  `}`

13.  `export const getUser = async (userId: string) => {`
14.  `  return await User.find(userId);`
15.  `};`

17.  `export const getUserByEmail = async (email: string) => {`
18.  `  const existingUser = await User.where(“email”, email).first();`
19.  `  return existingUser;`
20.  `};`

22.  `export const createUser = async (`
23.  `  name: string,`
24.  `  email: string,`
25.  `  password: string`
26.  `) => {`
27.  `  const existingUser = await getUserByEmail(email);`
28.  `  if (existingUser) throw new GQLError(“User already exists”);`
29.  `  const hashedPassword = await hash(password);`
30.  `  const user = await User.create({ name, email, password: hashedPassword });`
31.  `  return user;`
32.  `};`

34.  `export const deleteUser = async (userId: string) => {`
35.  `  await Contact.where(“userId”, userId).delete();`
36.  `  await User.deleteById(userId);`
37.  `  return null;`
38.  `};`

40.  `export const updateUser = async (userId: string, userData: any) => {`
41.  `  await User.where(“userId”, userId).update(userData);`
42.  `  return null;`
43.  `};`

45.  `export const getContactsByUserId = async (userId: string) => {`
46.  `  return await User.where(“userId”, userId).contacts();`
47.  `};`

49.  `export const getContact = async (contactId: string) => {`
50.  `  return await Contact.find(contactId);`
51.  `};`

53.  `export const createContact = async (contactData: IContact, userId: string) => {`
54.  `  const existingUser = await User.where(“userId”, userId).get();`
55.  `  if (!existingUser.length) throw new GQLError(“User does not exist”);`
56.  `  const contact = await Contact.create({ …contactData, userId });`
57.  `  return contact;`
58.  `};`

60.  `export const deleteContact = async (userId: string) => {`
61.  `  await Contact.deleteById(userId);`
62.  `  return null;`
63.  `};`

65.  `export const updateContact = async (contactId: string, contactData: any) => {`
66.  `  await Contact.where(“contactId”, contactId).update(contactData);`
67.  `  return null;`
68.  `};`

70.  `const batchGetUsersByIds = (ids: any) => {`
71.  `  const userPromises = ids.map(getUser);`
72.  `  const usersPromise = Promise.resolve(userPromises);`
73.  `  return usersPromise;`
74.  `};`

76.  `export const userLoader = new DataLoader(batchGetUsersByIds);`

In the preceding code, we have defined **`getUser`**,**`getUserByEmail`**,**`createUser`**,**`deleteUser`,** and **`updateUser`** functions for **`User`** model related queries and **`getContactByUserId`**, **`getContact`**, **`updateContact`**, and **`deleteContact`** functions for Contact model related queries. We are using **`find`**, **`where`**,**`create`**,**`deleteById`**,**`update`**, and**`delete`** model methods to perform the operations.

We have also defined **`batchGetUsersByIds`** function that works as **`dataloader`** function. It collects all the user’s ids and all the users in a single database call. It then returns a promise that resolves the array. We need to install **`dataloader`** using the following command to enable this functionality.

1.  `trex -c dataloader=https://esm.sh/dataloader@2.0.0/index.js`

Also, we are hashing the password (transforming the password into another string) in **`createUser`** function using the **`hash`** function provided by **`scrypt`** module. We will install scrypt module using the following command:

1.  `trex i -c https://deno.land/x/denOBodb/mod.ts`

# [Authentication](#toc.xhtml_s145a)

In order to identify requesting users, we will use **`djwt`** module to create and verify **JSON Web Token (JWT).** We need to set a **`SECRET_KEY (random string)`** in **`.env`** file, which will be used during JWT creation and verification. All the authentication-related code is written in the **`auth.ts`** file as follows:

1.  `// src/auth.ts`

3.  `import { create, verify } from “djwt”;`
4.  `import { RouterContext } from “oak”;`
5.  `import { verify as hashVerify } from “scrypt”;`

7.  `const SECRET_KEY = Deno.env.get(“SECRET_KEY”);`
8.  `const ALGORITHM = “HS512”;`

11.  `export const authenticate = async (user: any, password: string) => {`
12.  `  if (await verifyPassword(password, user.password)) {`
13.  `    return createToken(user);`
14.  `  }`
15.  `};`

17.  `const verifyPassword = async (password: string, hashedPassword: string) => {`
18.  `  const isValidPassword = await hashVerify(password, hashedPassword as string);`
19.  `  return isValidPassword;`
20.  `};`

22.  `const createToken = async (user: any) => {`
23.  `  if (!SECRET_KEY)`
24.  `    throw new Error(“SECRET_KEY not set as environment variable”);`
25.  `  const jwt = await create(`
26.  `    { alg: ALGORITHM, typ: “JWT” },`
27.  `    { userId: user.userId },`
28.  `    SECRET_KEY`
29.  `  );`
30.  `  return jwt;`
31.  `};`

33.  `export const setContextUser = async (ctx: RouterContext) => {`
34.  `const token = await parseToken(ctx);`
35.  `  if (!token) return null;`
36.  `  const user = await verifyToken(token);`
37.  `  return user;`
38.  `};`
39.  `const parseToken = async (ctx: RouterContext) => {`
40.  `  const authorizationHeader = ctx.request.headers.get(“authorization”);`
41.  `  const parts = authorizationHeader ? authorizationHeader.split(“ “) : [];`
42.  `  const token =`
43.  `    parts.length === 2 && parts[0].toLowerCase() === “bearer”`
44.  `      ? parts[1]`
45.  `      : undefined;`
46.  `  return token;`
47.  `};`

49.  `const verifyToken = async (token: string | undefined) => {`
50.  `  if (token) {`
51.  `    if (!SECRET_KEY)`
52.  `      throw new Error(“SECRET_KEY not set as environment variable”);`
53.  `    const payload = await verify(token, SECRET_KEY, ALGORITHM);`
54.  `    return payload;`
55.  `  }`
56.  `  return;`
57.  `};`

In the **`authenticate`** function, we are accepting **`user`** and **`password`** as arguments. We are using **`verifyPassword`** function to verify the password by checking it against the hashed password. If the password is valid, we then create a *JWT token* using **`SECRET_KE`** and **`ALGORITHM`** with payload **`userId`**.

In the **`setContextUser`** function, we are accepting **`ctx`** of type **`RouterContext`** as an argument. We then pass the ctx to **`parseToken`** function that returns a **`token`** provided in the **authorization** header. The parsed token is then passed to **`verifyToken`** function that verifies the token using **`SECRET_KEY`** and **`ALGORITHM`** and returns the **payload** after successful verification. The payload will then be available for all the resolvers to identify the requesting user. We need to install **`djwt`** module using the following command:

1.  `trex i -m djwt@v2.2`

We will now use **`setContextUser`** as a context handler for GraphQL middleware in the **`middlewares.ts`** file as follows:

1.  `// src/middlewares.ts`

3.  `import { Router } from “oak”;`
4.  `import { applyGraphQL } from “oak_graphql”;`
5.  `import { types } from “./schema.ts”;`
6.  `import { resolvers } from “./resolvers.ts”;`
7.  `import { setContextUser } from “./auth.ts”;`

9.  `export const GraphQLService = await applyGraphQL<Router>({`
10.  `  Router,`
11.  `  typeDefs: types,`
12.  `  resolvers: resolvers,`
13.  `  context: setContextUser,`
14.  `});`

In the **`src/middlewares.ts`** file, we are importing GraphQL schema/type definitions from the **`types.ts`** file. We are also importing resolvers from the **`resolvers.ts`** file. They are passed along with **Router** to **`applyGraphQL`** service to create **`GraphQL`** service. The **`setContextUser`** function uses **JSON Web Token (JWT)** provided in the authorization header to retrieve userId and set it in the context so every resolver will have access to it.

Finally, we will add **`oakcors`** middleware in our app to enable **cross-origin resource sharing (CORS)** to allow other domains to access the resources on this server. We will also use the **PORT** environment variable to set the server port. Our **`mod.ts`** file will have the following code after changes:

1.  `import { Application } from “oak”;`
2.  `import { GraphQLService } from “./middlewares.ts”;`
3.  `import { oakCors } from “cors”;`

5.  `const app = new Application();`

7.  `const _PORT = Deno.env.get(«PORT»);`
8.  `const PORT = parseInt(_PORT as string);`
9.  `const port = isNaN(PORT) ? 8080 : PORT;`

11.  `app.use(`
12.  `  oakCors()`
13.  `);`

15.  `app.use(GraphQLService.routes(), GraphQLService.allowedMethods());`

17.  ``console.log(`GraphQL Server listening on ${port}/graphql`);``

19.  `await app.listen({ port });`

We will install **`cors`** module using the following command:

1.  `trex i -m cors@v1.2.2`

# [Conclusion](#toc.xhtml_s146a)

We have implemented a GraphQL API in this chapter using various Deno modules such as **`oak-graphql`**,**`djwt`**,**`scrypt`**, and**`cors`**. Oak-GraphQL is useful for the creation of a GraphQL API server along with the Oak framework. Djwt is useful to create and verify JSON Web Tokens. Scrypt is useful for hashing passwords. CORS is useful for allowing server access via different domains. We learnt how to configure settings (env variables, scripts, and permissions) using *velociraptor***.** We used **`trex`** module to install Deno modules and add them to **`import_map.json`** file.

This knowledge will be helpful in setting up a new Deno project. We can test the implementation in the playground for now. We will create a Svelte front end using **`Snel`** module and integrate the GraphQL API in the upcoming chapter.

# [CHAPTER 9](#toc.xhtml_c09)

# [PhoneBook App - UI Implementation](#toc.xhtml_c09)

# [Introduction](#toc.xhtml_s147a)

We implemented the GraphQL API server in the previous chapter for the PhoneBook App. The **User Interface** (**UI**) for the application will be implemented in this chapter using that API. We will be using **`snel`** module to create **`svelte`** applications in deno along with **`snel-carbon`** module which provides carbon components and icons based on carbon design system by IBM. We will also use axiod module to make network requests to the server.

# [Structure](#toc.xhtml_s148a)

In this chapter, we will cover the following topics:

*   Initial setup
    *   Snel setup
    *   Snel-carbon installation
*   Routes
    *   Public routes
        *   Login
        *   Register
    *   Private routes
        *   Home
        *   Contacts
            *   ContactTable
            *   ContactForm
*   Layout
    *   Header
    *   Sidebar

# [Objective](#toc.xhtml_s149a)

After completion of this chapter, you should be able to create svelte UI applications using **`snel`** and **`snel-carbon`** modules. You should be able to create public and private routes for svelte applications afterwards. You will also learn the use of **`axiod`** module to make network requests.

# [Initial setup](#toc.xhtml_s150a)

In this section, we will install **`snel`** and initialize a snel project and then use **`trex`** to run the scripts. Once a snel project is created, we will install **`snel-carbon`** components, icons module and **`axiod`** module for network requests. Let’s start with snel installation.

# [Snel setup](#toc.xhtml_s151a)

Snel is “*A Cybernetical framework for svelte applications in deno*” that compiles Svelte components to javascript files. We will install snel using following command:

1.  `deno run --allow-run --allow-read https://deno.land/x/snel/install.ts`

Above command will install **`snel`**, **`trex`**, **`bundler`** modules to provide good developer experience. Once the command is successfully executed, we will create new snel app using following command:

1.  `snel create [project name]`

*[Figure 9.1](#c09.xhtml_fig9_1)* shows creation of new snel project with default settings.

![](images/Figure-9.1.jpg)

**Figure 9.1:** Snel Project Creation

Once the project is created, we can use several commands to run the project in various modes like **`development`,** **`watch`,** **`build`**, and so on.

*[Figure 9.2](#c09.xhtml_fig9_2)* lists several commands available to run the snel project.

![](images/Figure-9.2.jpg)

**Figure 9.2:** Trex Commands for Snel Project

We will start the project by running **`trex run start`** command as suggested in the message. This will run the server on port **`3000`**.

*[Figure 9.3](#c09.xhtml_fig9_3)* shows a sample snel project running on port 3000.

![](images/Figure-9.3.jpg)

**Figure 9.3:** Snel sample project running on port 3000

# [Snel Carbon installation](#toc.xhtml_s152a)

Snel-Carbon is a deno module providing UI components for svelte. It would help us to build a UI based on the Carbon Design System. Let’s start by adding css in the **`index.html`** file. This will add stylings required for the components.

1.  `<link rel=”stylesheet” href=”https://cdn.jsdelivr.net/npm/carbon-components-svelte@0.44.2/css/all.min.css” />`

Snel provides **`snel.config.js`** file to configure snel settings. It provides **`extendsImportMap`** field to link external import map to the project. We will add import maps for components and icons provided by **`snel-carbon`** library in this field as follows:

1.  `// snel.config.js`

3.  `export default {`
4.  `  port: 3000,`
5.  `  mode: “dom”,`
6.  `  plugins: [],`
7.  `  extendsImportMap: [`
8.  `    “https://denopkg.com/crewdevio/Snel-carbon@main/components.map.json”,`
9.  `    “https://denopkg.com/crewdevio/Snel-carbon@main/icons.map.json”,`
10.  `  ],`
11.  `};`

We will now install **`axiod`** module using familiar **`trex`** command as follows:

1.  `trex i -m axiod@0.20.0-0`

Above command will add **`axiod`** in **`import_map.json`** file in the project. We have installed all the required modules in this section. We will now create routes for different pages in the next section.

# [Routes](#toc.xhtml_s153a)

Snel module includes **Svelte Routing** library to create routes. We will use it to create two types of routes named public and private routes for our project. Public routes will be available to all the users while private routes will be available only to authenticated users.

Let’s start by adding **`Route`** component from **`routes/index.svelte`** file in **`App.svelte`** file as follows:

1.  `// App.svelte`

3.  `<script>`
4.  `  import Routes from “routes/index.svelte”;`
5.  `  import { fade } from “svelte/transition”;`
6.  `</script>`

8.  `<main transition:fade>`
9.  `  <Routes />`
10.  `</main>`

12.  `<style>`
13.  `  main {`
14.  `    max-width: 240px;`
15.  `  }`

17.  `  @media (min-width: 640px) {`
18.  `    main {`
19.  `      max-width: none;`
20.  `    }`
21.  `  }`
22.  `</style>`

In the preceding code, we are replacing code within the main element (HTML element that represents the dominant content of the body) by **`Route`** component. This way our app will always render each page as per the route address. Let’s implement the routes in the **`routes/index.svelte`** file as follows:

1.  `<script>`
2.  `  // Modules`
3.  `  import Router from “svelte-routing/Router.svelte”;`
4.  `  import Route from “svelte-routing/Route.svelte”;`

6.  `  // Routes`
7.  `  import Contacts from “./Contacts.svelte”;`
8.  `  import Login from “./Login.svelte”;`
9.  `  import Register from “./Register.svelte”;`
10.  `  import Home from “./Home.svelte”;`
11.  `  import NotFound from “./NotFound.svelte”;`
12.  `  import PrivateRoute from “./PrivateRoute.svelte”;`

14.  `  import Content from “snel-carbon/components/UIShell/Content.svelte”;`
15.  `  import Grid from “snel-carbon/components/Grid/Grid.svelte”;`
16.  `  import Row from “snel-carbon/components/Grid/Row.svelte”;`
17.  `  import Column from “snel-carbon/components/Grid/Column.svelte”;`

19.  `  // Components`
20.  `  import Layout from “@/components/Layout.svelte”;`
21.  `</script>`

23.  `<Router>`
24.  `  <Layout />`
25.  `  <Content>`
26.  `    <Grid>`
27.  `      <Row>`
28.  `        <Column>`
29.  `          <Route path=”login” component={Login} />`
30.  `          <Route path=”register” component={Register} />`
31.  `          <Route path=”*” component={NotFound} />`

33.  `          <PrivateRoute path=”/”>`
34.  `            <Home />`
35.  `          </PrivateRoute>`
36.  `          <PrivateRoute path=”contacts” let:location>`
37.  `            <Contacts />`
38.  `          </PrivateRoute>`

40.  `        </Column>`
41.  `      </Row>`
42.  `    </Grid>`
43.  `  </Content>`
44.  `</Router>`

In the preceding code, we are using **`Router`**, **`Route`** components from **`svelte-routing`** module. **`Router`** provides route information via context to **`Route`**, **`Link`** components and renders best matched **`Route`**.

In the **`Routes`** import section, we are importing **`Contacts`**, **`Login`**, **`Home`**, and **`Register`**. Each route will be assigned a path. Apart from these routes, we are also importing two special routes named **`NotFound`**, **`PrivateRoute`**. **`NotFound`** renders when no other route is matched. **`PrivateRoute`** is used to restrict access to routes like **`Contacts`** for authenticated users only.

We are importing Carbon components such as **`Content`**, **`Row`**, **`Grid`,** **`Column`** from **`snel-carbon`** module to create a responsive UI along with **Layout** custom component having header and sidebar implementation.

Let’s implement each route code one by one.

# [Login](#toc.xhtml_s154a)

Login will be the default page shown to every unauthenticated user. We will use **`Form`** to handle validations for **`email`**, **`password`**. The implementation for **`Login.svelte`** is as follows:

1.  `// Login.svelte`

3.  `<script>`
4.  `  import { navigate } from “svelte-routing”;`

6.  `  import Form from “snel-carbon/components/Form”;`
7.  `  import Tile from “snel-carbon/components/Tile”;`
8.  `  import TextInput from “snel-carbon/components/TextInput/TextInput.svelte”;`
9.  `  import PasswordInput from “snel-carbon/components/TextInput/PasswordInput.svelte”;`
10.  `  import Button from “snel-carbon/components/Button”;`
11.  `  import InlineLoading from “snel-carbon/components/InlineLoading”;`
12.  `  import InlineNotification from “snel-carbon/components/Notification/InlineNotification.svelte”;`

14.  `  import axiod from “https://deno.land/x/axiod/mod.ts”;`

16.  `  import { accessToken } from “../utils/stores.ts”;`

18.  `  let email = “”;`
19.  `  let password = “”;`
20.  `  let loading = false;`
21.  `  let errors = [];`

23.  `  const handleSubmit = (e) => {`
24.  `    loading = true;`
25.  ``     const query = ` ``
26.  `      {`
27.  `        login(user:{email:”${email}”, password:”${password}”}){`
28.  `          token`
29.  `        }`
30.  `      }`
31.  `` `; ``
32.  `    axiod`
33.  `      .post(“http://localhost:8080/graphql”, { query })`
34.  `      .then((res) => {`
35.  `        if (res.data.errors) {`
36.  `          errors = res.data.errors;`
37.  `        }`
38.  `        if (res.data.data?.login?.token) {`
39.  `          localStorage.setItem(“accessToken”, res.data.data?.login?.token);`
40.  `          $accessToken = res.data.data?.login?.token;`
41.  `          navigate(“/contacts”, {`
42.  `            replace: false,`
43.  `          });`
44.  `        }`
45.  `      })`
46.  `      .catch((err) => {`
47.  ``        console.log(`err`, err);``
48.  `      })`
49.  `      .finally(() => {`
50.  `        loading = false;`
51.  `      });`
52.  `  };`
53.  `</script>`

55.  `{#each errors as error (error.message)}`
56.  `  <InlineNotification timeout={5000} type=”error” title={error.message} />`
57.  `{/each}`

59.  `<Tile>`
60.  `  <Form on:submit={handleSubmit}>`
61.  `    <TextInput`
62.  `      bind:value={email}`
63.  `      required`
64.  `      type=”email”`
65.  `      labelText=”Email”`
66.  `      placeholder=”Enter Email”`
67.  `      size=”sm”`
68.  `    />`
69.  `    <PasswordInput`
70.  `      bind:value={password}`
71.  `      required`
72.  `      type=”password”`
73.  `      labelText=”Password”`
74.  `      placeholder=”Enter Password”`
75.  `      size=”sm”`
76.  `    />`
77.  `    {#if loading}`
78.  `      <InlineLoading />`
79.  `    {:else}`
80.  `      <Button type=”submit” size=”small”>Login</Button>`
81.  `    {/if}`
82.  `  </Form>`
83.  `</Tile>`

In the above code, we are using various **`snel-carbon`** components like **`Form`**,**`Tile`**,**`TextInput`**,**`PasswordInput`**,**`Button`**,**`InlineLoading`**,**`InlineNotifications`** to create the UI. We are using **`navigate`** function to redirect to **`contacts`** route on successful login. We are also importing **`accessToken`** which is stored in **`stores.ts`** file to check if the user is authenticated or not and **`axiod`** will be used to make network requests to GraphQL API Server.

We are using four states, **`email`**, **`password`**, **`errors`**, **`loading`** for this component where email, password will be used to store user input via **`TextInput`**, **`PasswordInput`**, loading will be used to render loader during network request using **`InlineLoading`** and errors will be used to store errors from the response.

In the UI part, the **`TextInput`** and **`PasswordInput`** are bound to **`email`**, **`password`** states respectively. The **`Form`** component will invoke **`handleSubmit`** function on **`submit`** event. The **`handleSubmit`** function makes network request using **`axiod`** with **`login`** query. If the response contains errors then those errors will be stored as **`errors`** and will be rendered using **`InlineNotification`** component. If the response provides **`token`** in the **`data`,** it will be stored into localStorage as well as **stores** as **`accessToken`** and the user will be redirected to **contacts** route.

*[Figure 9.4](#c09.xhtml_fig9_4)* shows login route with email, password input fields.

![](images/Figure-9.4.jpg)

**Figure 9.4:** Login Route

# [Register](#toc.xhtml_s155a)

This route is similar to **`login`** route with few changes. It will have additional states and few changes in the query and the network response handling**.** The implementation for **`Register.svelte`** route is as follows:

1.  `<script>`
2.  `  import { navigate } from “svelte-routing”;`

4.  `  import Form from “snel-carbon/components/Form”;`
5.  `  import Tile from “snel-carbon/components/Tile”;`
6.  `  import TextInput from “snel-carbon/components/TextInput/TextInput.svelte”;`
7.  `  import PasswordInput from “snel-carbon/components/TextInput/PasswordInput.svelte”;`
8.  `  import Button from “snel-carbon/components/Button”;`
9.  `  import InlineNotification from “snel-carbon/components/Notification/InlineNotification.svelte”;`
10.  `  import InlineLoading from “snel-carbon/components/InlineLoading”;`

12.  `  import axiod from “https://deno.land/x/axiod/mod.ts”;`

14.  `  let name = “”;`
15.  `  let email = “”;`
16.  `  let password = “”;`
17.  `  let confirmPassword = “”;`
18.  `  let loading = false;`
19.  `  let errors = [];`

21.  `  const handleSubmit = (e) => {`
22.  `    if (password === confirmPassword) {`
23.  `      loading = true;`
24.  ``       const query = ` ``
25.  `      mutation{`
26.  `        registerUser(user:{email:”${email}”, password:”${password}”, name:”${name}”}){`
27.  `          name`
28.  `        }`
29.  `      }`
30.  `` `; ``
31.  `      axiod`
32.  `        .post(“http://localhost:8080/graphql”, { query })`
33.  `        .then((res) => {`
34.  ``          console.log(`res`, res);``
35.  `          if (res.data.errors) {`
36.  `            errors = res.data.errors;`
37.  `          }`
38.  `          if (res.data.data.registerUser?.name) {`
39.  ``            alert(`user ${res.data.data.registerUser.name} registered`);``
40.  `            navigate(“/contacts”, {`
41.  `              replace: false,`
42.  `              state: { accessToken: res.data.data.login },`
43.  `            });`
44.  `          }`
45.  `        })`
46.  `        .catch((err) => {`
47.  ``          console.log(`err`, err);``
48.  `        });`
49.  `    } else {`
50.  `      alert(“Passwords do not match”);`
51.  `    }`
52.  `  };`
53.  `</script>`

55.  `{#each errors as error}`
56.  `  <InlineNotification type=”error” title={error.message} />`
57.  `{/each}`

59.  `<Tile>`
60.  `  <Form on:submit={handleSubmit}>`
61.  `    <TextInput`
62.  `      bind:value={name}`
63.  `      required`
64.  `      labelText=”Name”`
65.  `      placeholder=”Enter Name”`
66.  `      size=”sm”`
67.  `    />`
68.  `    <TextInput`
69.  `      bind:value={email}`
70.  `      required`
71.  `      type=”email”`
72.  `      labelText=”Email”`
73.  `      placeholder=”Enter Email”`
74.  `      size=”sm”`
75.  `    />`
76.  `    <PasswordInput`
77.  `      bind:value={password}`
78.  `      required`
79.  `      type=”password”`
80.  `      labelText=”Password”`
81.  `      placeholder=”Enter Password”`
82.  `      size=”sm”`
83.  `    />`
84.  `    <PasswordInput`
85.  `      bind:value={confirmPassword}`
86.  `      required`
87.  `      type=”password”`
88.  `      labelText=”Confirm Password”`
89.  `      placeholder=”Enter Confirm Password”`
90.  `      size=”sm”`
91.  `    />`
92.  `    {#if loading}`
93.  `      <InlineLoading />`
94.  `    {:else}`
95.  `<Button type=”submit” size=”small”>Register</Button>`
96.  `    {/if}`
97.  `  </Form>`
98.  `</Tile>`

As we can see, the above code has many similarities with **`Login.svelte`** code. We have added two additional states **`name`** and **`confirmPassword`** each bound to an input component (**`TextInput`,** **`PasswordInput`)**. In the **`handleSubmit`** function, we are using **`mutation`** instead of query as we are creating a new user instance on the backend.

*[Figure 9.5](#c09.xhtml_fig9_5)* shows Register route with name, email, password, confirm password fields.

![](images/Figure-9.5.jpg)

**Figure 9.5:** Register Route

# [Home](#toc.xhtml_s156a)

This will be the home page for authenticated users. It will be containing **`Link`** component that navigates to **`contacts`** path. The code for this route is as follows:

1.  `<script>`
2.  `  import Link from “svelte-routing/Link.svelte”;`
3.  `</script>`

5.  `<h1>Home</h1>`
6.  `<Link to=”contacts”>Contacts</Link>`

*[Figure 9.6](#c09.xhtml_fig9_6)* shows Home route with **`Link`** component for **`Contacts`** route.

![](images/Figure-9.6.jpg)

**Figure 9.6:** Home Route

# [NotFound](#toc.xhtml_s157a)

Whenever a user opens a non-existing path address, this route will get rendered. We have used Asterisk (*) for that purpose. The code for the route is as follows:

1.  `<script>`
2.  `  import Link from “svelte-routing/Link.svelte”;`
3.  `</script>`

5.  `<h2>Page Not Found</h2>`
6.  `Go back to <Link to=”/”>Home</Link>`

8.  `<style>`
9.  `  h2 {`
10.  `    color: red;`
11.  `  }`
12.  `</style>`

Above code is a simple page with **`Page Not Found`** message and **`Link`** to Home page.

*[Figure 9.7](#c09.xhtml_fig9_7)* shows **`NotFound`** component rendered for undefined path.

![](images/Figure-9.7.jpg)

**Figure 9.7:** NotFound Route

# [Private route](#toc.xhtml_s158a)

While Login, Register are public routes (no authentication required), Home, Contacts are private routes and should only be accessible to authenticated users. We will protect these pages by using PrivateRoute (a custom route) instead of normal Route. The code for private route is as follows:

1.  `<script>`
2.  `  import Route from “svelte-routing/Route.svelte”;`
3.  `  import PrivateRouteGuard from “./PrivateRouteGuard.svelte”;`

5.  `  export let path;`
6.  `</script>`

8.  `<Route {path}>`
9.  `  <PrivateRouteGuard>`
10.  `    <slot />`
11.  `  </PrivateRouteGuard>`
12.  `</Route>`

In the above code we are using the **`Route`** component as wrapper. We are passing the **`path`** prop to it which is an route address. The **`slot`** element is nothing but the component to be rendered. We are wrapping it using **`PrivateRouteGuard`** component. The code for **`PrivateRouteGuard`** is as follows:

1.  `<script>`
2.  `  import { onMount } from “svelte”;`
3.  `  import { navigate } from “svelte-routing”;`
4.  `  import { accessToken } from “../utils/stores.ts”;`

6.  `  onMount(() => {`
7.  `    console.log(“Mounting…”);`
8.  `    if (!$accessToken) {`
9.  `      navigate(“/login”, {`
10.  `        replace: false,`
11.  `      });`
12.  `    }`
13.  `  });`
14.  `</script>`

16.  `{#if $accessToken}`
17.  `  <slot />`
18.  `{/if}`

**`PrivateRouteGuard`** uses **`onMount`** function that gets called on component mount. It checks the **`accessToken`** value in it. If **`accessToken`** is null then it will navigate to **`login`** route else it will render the child component.

# [Contacts](#toc.xhtml_s159a)

This route will be accessible to all the authenticated users and it lists all the contacts of the user. The code for contacts route is as follows:

1.  `<script>`
2.  `  import { onMount } from “svelte”;`

4.  `  import Modal from “snel-carbon/components/ComposedModal”;`

6.  `  import axiod from “https://deno.land/x/axiod/mod.ts”;`

8.  `  import ContactForm from “../components/ContactForm.svelte”;`
9.  `  import ContactTable from “../components/ContactTable.svelte”;`

11.  `  let showForm = false;`
12.  `  let contacts = [];`
13.  `  const accessToken = localStorage.getItem(“accessToken”);`
14.  `  let editContact = null;`

16.  `  const getContacts = () => {`
17.  `    console.log(“fetching contacts…”);`
18.  ``     const query = ` ``
19.  `        {`
20.  `          contacts {`
21.  `            contactId`
22.  `            name`
23.  `            email`
24.  `            phone`
25.  `            address`
26.  `          }`
27.  `        }`
28.  ``      `;``
29.  `    axiod`
30.  `      .post(`
31.  `        “http://localhost:8080/graphql”,`
32.  `        { query },`
33.  `        {`
34.  ``          headers: { Authorization: `Bearer ${accessToken}` },``
35.  `        }`
36.  `      )`
37.  `      .then((res) => {`
38.  ``        console.log(`res`, res);``
39.  `        if (res.data.errors) {`
40.  `          for (let error of res.data.errors) {`
41.  `            alert(error.message);`
42.  `          }`
43.  `        }`
44.  ``        // console.log(`res.data.data.login`, res.data.data.login);``
45.  `        if (res.data.data?.contacts) {`
46.  `          contacts = res.data.data.contacts;`
47.  `        }`
48.  `      })`
49.  `      .catch((err) => {`
50.  ``        console.log(`err`, err);``
51.  `      });`
52.  `    console.log(“fetched contacts…”);`
53.  `  };`

55.  `  const deleteContact = (contactId) => {`
56.  ``     const query = ` ``
57.  `    mutation {`
58.  `      deleteContact(contactId: “${contactId}”)`
59.  `    }`
60.  ``    `;``
61.  `    axiod`
62.  `      .post(`
63.  `        “http://localhost:8080/graphql”,`
64.  `        { query },`
65.  `        {`
66.  ``          headers: { Authorization: `Bearer ${accessToken}` },``
67.  `        }`
68.  `      )`
69.  `      .then((res) => {`
70.  ``        console.log(`res`, res);``
71.  `        if (res.data.errors) {`
72.  `          for (let error of res.data.errors) {`
73.  `            alert(error.message);`
74.  `          }`
75.  `        } else {`
76.  `          getContacts();`
77.  `        }`
78.  `        if (res.data.data?.contacts) {`
79.  `          contacts = res.data.data.contacts;`
80.  `        }`
81.  `      })`
82.  `      .catch((err) => {`
83.  ``        console.log(`err`, err);``
84.  `      });`
85.  `  };`

87.  `  onMount(async () => {`
88.  `    console.log(“Mounting…”);`
89.  `    await getContacts();`
90.  `  });`

92.  `  const resetForm = () => {`
93.  `    showForm = !showForm;`
94.  `    editContact = null;`
95.  `  };`

97.  `  const handleEdit = (event) => {`
98.  `    showForm = true;`
99.  `    editContact = event.detail.contact;`
100.  `  };`
101.  `</script>`

103.  `{#if showForm}`
104.  `  <Modal`
105.  `    bind:open={showForm}`
106.  `    preventCloseOnClickOutside`
107.  ``    modalHeading={`${editContact ? “Edit” : “Add”} Contact`}``
108.  `  >`
109.  `    <ContactForm`
110.  `      on:resetForm={resetForm}`
111.  `      on:contactSaved={(event) => {`
112.  ``        console.log(`event`, event);``
113.  `        showForm = event.detail.showForm;`
114.  `        getContacts();`
115.  `        editContact = event.detail.editContact;`
116.  `      }}`
117.  `      {editContact}`
118.  `    />`
119.  `  </Modal>`
120.  `{/if}`
121.  `<ContactTable`
122.  `  {contacts}`
123.  `  on:deleteContact={(event) => deleteContact(event.detail.contactId)}`
124.  `  on:edit={handleEdit}`
125.  `  on:openForm={resetForm}`
126.  `/>`

Above code renders two components namely **`ContactForm`** and **`ContactTable`**. Modal component from snel-carbon is used to show **`ContactForm`** in modal view. It defines three states **`showContact`**, **`contacts`** and **`editContact`**. **`showContact`** is a boolean flag to show or hide the **`ContactForm`** modal. contacts is an array of contacts. These contacts are fetched using **`getContacts`** function that makes network request using axiod to the GraphQL API server. It gets called once component is mounted using **`onMount`** function. We have also defined **`deleteContact`** function that make contact delete request to the server. We have set **`Authorization`** header with **`accessToken`** for each request for user authentication purpose. **`resetForm`** function is used to reset the form fields on form close or submission. **`handleEdit`** function is used to set selected entity as **`editContact`**. The **`editContact`** data will then be passed to the form to be edited. Let’s check **`ContactForm`** and **`ContactTable`** components in detail.

# [ContactTable](#toc.xhtml_s160a)

We will show all the contacts in the table format using snel-carbon components in **`ContactTable.svelte`** file. We will also provide actions for **`create`,** **`delete`,** **`edit`** in the table. The code for the component is as follows:

1.  `<script>`
2.  `  import { createEventDispatcher } from “svelte”;`

4.  `  import DataTable from “snel-carbon/components/DataTable”;`

6.  `  import Toolbar from “snel-carbon/components/DataTable/Toolbar.svelte”;`
7.  `  import ToolbarContent from “snel-carbon/components/DataTable/ToolbarContent.svelte”;`

9.  `  import OverflowMenu from “snel-carbon/components/OverflowMenu/OverflowMenu.svelte”;`
10.  `  import OverflowMenuItem from “snel-carbon/components/OverflowMenu/OverflowMenuItem.svelte”;`

12.  `  import Button from “snel-carbon/components/Button”;`

14.  `  import AddAlt16 from “snel-carbon/icons/AddAlt16”;`
15.  `  import Edit16 from “snel-carbon/icons/Edit16”;`
16.  `  import Delete16 from “snel-carbon/icons/Delete16”;`

18.  `  const dispatch = createEventDispatcher();`

20.  `  export let contacts;`
21.  `  $: {`
22.  `    contacts = contacts.map((contact, index) => {`
23.  `      contact.id = index + 1;`
24.  `      return contact;`
25.  `    });`
26.  `  }`
27.  `</script>`

29.  `<DataTable`
30.  `  title=”Contacts”`
31.  `  sortable`
32.  `  headers={[`
33.  `    { key: “id”, value: “ID” },`
34.  `    { key: “name”, value: “Name” },`
35.  `    { key: “email”, value: “Email” },`
36.  `    { key: “phone”, value: “Phone” },`
37.  `    { key: “address”, value: “Address” },`
38.  `    { key: “overflow”, empty: true },`
39.  `  ]}`
40.  `  rows={contacts}`
41.  `>`
42.  `  <Toolbar>`
43.  `    <ToolbarContent>`
44.  `      <Button`
45.  `        on:click={() => {`
46.  `          dispatch(“openForm”);`
47.  `        }}`
48.  `        icon={AddAlt16}`
49.  `      />`
50.  `    </ToolbarContent>`
51.  `  </Toolbar>`

53.  `  <span slot=”cell” let:cell let:row>`
54.  `    {#if cell.key === “overflow”}`
55.  `      <OverflowMenu flipped>`
56.  `        <OverflowMenuItem`
57.  `          on:click={() => {`
58.  `            dispatch(“edit”, { contact: row });`
59.  `          }}`
60.  `          ><Edit16 />`
61.  `        </OverflowMenuItem>`
62.  `        <OverflowMenuItem`
63.  `          danger`
64.  `          on:click={() => {`
65.  `            dispatch(“deleteContact”, { contactId: row.contactId });`
66.  `          }}`
67.  `        >`
68.  `          <Delete16 />`
69.  `        </OverflowMenuItem>`
70.  `      </OverflowMenu>`
71.  `    {:else}{cell.value}{/if}`
72.  `  </span>`
73.  `</DataTable>`

In the preceding code, we are importing various components from snel-carbon like **`DataTable`,** **`Toolbar`**, **`Overflow`**, **`Button`**, and so on. We are also importing icons like **`AddAlt16`**, **`Edit16`**,**`Delete16`** from snel-carbon.

We are importing **`createEventDispatcher`** from svelte which will be used to dispatch events to the parent component. The **`contacts`** is passed as **`prop`** by parent components.

We are using **$:** (labeled statement) syntax for **reactive declarations** meaning run the code on reference value change. We are using it to add an **id** field to each contact. We are doing this because the **`DataTable`** component requires each row to have an id field. We are passing an object with **key, value** keys as **headers** to the DataTable. These will be used as header for each column. The **`contacts`** (each with **`id`**) are passed as **`rows`**. In the **`DataTable`,** we are using **`Toolbar`** with **`Add`** button that allows to add new contact.

*[Figure 9.8](#c09.xhtml_fig9_8)* shows ContactTable with Toolbar and headers:

![](images/Figure-9.8.jpg)

**Figure 9.8:** ContactTable with toolbar

**OverflowMenu** is used to to provide actions such as **`edit`**, **`delete`** the contact. We need to add { key: “overflow”, empty: true } in the **headers** to enable the overflow menu. We are using slot prop **cell to** identify the overflow cell and render it or else render the normal value for the cell. The **row** prop is passed to edit, delete actions to perform API requests using the contact data. We are dispatching these actions using **dispatch.** This means we will pass events **`edit`**, **`deleteContact`** along with state to the parent. The parent will then handle the events accordingly.

*[Figure 9.9](#c09.xhtml_fig9_9)* shows **`OverflowMenu`** with edit, and delete actions.

![](images/Figure-9.9.jpg)

**Figure 9.9:** OverflowMenu with Edit, Delete actions

We will now check the form details used to create, edit contact on click on the **`Add`** button in next section.

# [ContactForm](#toc.xhtml_s161a)

Whenever the user clicks on the **`Add`** button, we show a modal with contact form for create or update purpose as explained in **`Contacts`** section. We will implement this component using snel-carbon components and axiod for API calls. The code for **`ContactForm.svelte`** component is as follows:

1.  `<script>`
2.  `  import Form from “snel-carbon/components/Form”;`
3.  `  import Tile from “snel-carbon/components/Tile”;`
4.  `  import TextInput from “snel-carbon/components/TextInput/TextInput.svelte”;`
5.  `  import TextArea from “snel-carbon/components/TextArea”;`

7.  `  import Button from “snel-carbon/components/Button”;`
8.  `  import InlineLoading from “snel-carbon/components/InlineLoading”;`

10.  `  import axiod from “https://deno.land/x/axiod/mod.ts”;`
11.  `  import { accessToken } from “../utils/stores.ts”;`
12.  `  import { createEventDispatcher } from “svelte”;`

14.  `  const initialContact = {`
15.  `    name: “”,`
16.  `    email: “”,`
17.  `    phone: “”,`
18.  `    address: “”,`
19.  `  };`

21.  `  const dispatch = createEventDispatcher();`

23.  `  export let editContact;`

25.  `  $: contact = editContact || initialContact;`

27.  `  let loading = false;`

29.  `  const handleSubmit = () => {`
30.  `    loading = true;`
31.  ``     const addQuery = ` ``
32.  `    mutation {`
33.  `      addContact(contact: {name: “${contact.name}”, email: “${contact.email}”, phone: “${contact.phone}”, address: “${contact.address}”}){`
34.  `        name`
35.  `      }`
36.  `    }`
37.  ``        `;``
38.  ``     const updateQuery = ` ``
39.  `    mutation {`
40.  `      updateContact(contact: {contactId: “${contact?.contactId}”, name: “${contact.name}”, email: “${contact.email}”, phone: “${contact.phone}”, address: “${contact.address}”})`
41.  `    }`
42.  ``    `;``
43.  `    const query = editContact ? updateQuery : addQuery;`

45.  `    axiod`
46.  `      .post(`
47.  `        “http://localhost:8080/graphql”,`
48.  `        { query },`
49.  `        {`
50.  ``          headers: { Authorization: `Bearer ${$accessToken}` },``
51.  `        }`
52.  `      )`
53.  `      .then((res) => {`
54.  ``        console.log(`res`, res);``
55.  `        if (res.data.errors) {`
56.  `          for (let error of res.data.errors) {`
57.  `            alert(error.message);`
58.  `          }`
59.  `        } else {`
60.  `          contact = initialContact;`
61.  `          dispatch(“contactSaved”, {`
62.  `            showForm: false,`
63.  `            editContact: null,`
64.  `          });`
65.  `        }`
66.  `      })`
67.  `      .catch((err) => {`
68.  ``        console.log(`err`, err);``
69.  `      })`
70.  `      .finally(() => {`
71.  `        loading = false;`
72.  `      });`
73.  `  };`
74.  `</script>`

76.  `<Tile>`
77.  `  <Form on:submit={handleSubmit}>`
78.  `    <TextInput`
79.  `      bind:value={contact.name}`
80.  `      required`
81.  `      labelText=”Name”`
82.  `      placeholder=”Enter Name”`
83.  `      size=”sm”`
84.  `    />`
85.  `    <TextInput`
86.  `      bind:value={contact.email}`
87.  `      required`
88.  `      type=”email”`
89.  `      labelText=”Email”`
90.  `      placeholder=”Enter Email”`
91.  `      size=”sm”`
92.  `    />`
93.  `    <TextInput`
94.  `      bind:value={contact.phone}`
95.  `      required`
96.  `      type=”number”`
97.  `      labelText=”Phone”`
98.  `      placeholder=”Enter Phone Number”`
99.  `      size=”sm”`
100.  `    />`
101.  `    <TextArea`
102.  `      bind:value={contact.address}`
103.  `      required`
104.  `      labelText=”Address”`
105.  `      placeholder=”Enter Address”`
106.  `      size=”sm”`
107.  `    />`
108.  `    {#if loading}`
109.  `      <InlineLoading />`
110.  `    {:else}`
111.  `      <Button type=”submit” size=”small”>Save</Button>`
112.  `      <Button`
113.  `        on:click={() => {`
114.  `          dispatch(“resetForm”);`
115.  `        }}`
116.  `        size=”small”`
117.  `        kind=”danger”>Cancel</Button`
118.  `      >`
119.  `    {/if}`
120.  `  </Form>`
121.  `</Tile>`

In the above code, we are importing **`Tile`**, **`Form`**, **`TextInput`**, **`PasswordInput`**, **`Button`** components from snel-carbon. **`Tile`** is used as card layout for the form. **`Form`** is used to handle validations like email, number etc. and submission. **`TextInput`** is as input field for name, email (type=”email”), phone (type=”number”). **`Button`** is used to close the form and set field values to empty or with type=”submit” that validates all fields and invokes on:submit function **`handleSubmit`**.

*[Figure 9.10](#c09.xhtml_fig9_10)* shows **`ContactForm`** while creating new contact:

![](images/Figure-9.10.jpg)

**Figure 9.10:** ContactForm for new contact

In the **script** section, we are using **`initialContact`** object to set all fields to empty on new form creation or on form close. **`editContact`** prop is used to identify whether form values should be empty for new contact using **`initialContact`** or existing form values to be used using **`editContact`**. The reactive variable **`contact`** is set according to **`editContact`** value.

The **`handleSubmit`** function contains two queries **`addQuery`** **(**create contact) and **`updateQuery`** (update contact)**.** Again, we are using **`editContact`** to select the query accordingly. Then, we are making network request for the selected query with **`Authorization`** header.

*[Figure 9.11](#c09.xhtml_fig9_11)* shows **`ContactForm`** with **`editContact`** to update the existing contact:

![](images/Figure-9.11.jpg)

**Figure 9.11:** ContactForm for existing contact

# [Layout](#toc.xhtml_s162a)

We will create a layout using **`Header`** and **`Sidebar`** **`snel-carbon`** components in this section. This will allow us to provide App title in **`Header`** and add login/logout buttons in the Sidebar. We will write all the layout related code in file **`Layout.svelte`** as follows:

1.  `<script>`
2.  `  import Header from “snel-carbon/components/UIShell/GlobalHeader/Header.svelte”;`
3.  `  import SideNav from “snel-carbon/components/UIShell/SideNav/SideNav.svelte”;`
4.  `  import SideNavItems from “snel-carbon/components/UIShell/SideNav/SideNavItems.svelte”;`

6.  `  import Authentication from “./Authentication.svelte”;`

8.  `  let theme = “g10”;`
9.  `  $: document.documentElement.setAttribute(“theme”, theme);`

11.  `  let isSideNavOpen = false;`
12.  `</script>`

14.  `<Header`
15.  `  company=”Phonebook”`
16.  `  platformName=”App”`
17.  `  bind:isSideNavOpen`
18.  `  persistentHamburgerMenu={true}`
19.  `/>`
20.  `<SideNav bind:isOpen={isSideNavOpen}>`
21.  `  <SideNavItems>`
22.  `    <Authentication />`
23.  `  </SideNavItems>`
24.  `</SideNav>`

In the preceding code, we are importing **`Header`**, **`SideNav`**, **`SideNavItems`** from snel carbon. The **`Header`** will be placed at top of the app while **`SideNav`** will be used to create a sidebar where **`SideNavItems`** contains actions like **`login`**, **`register`**, and so on. We have set theme to **`g10`** that is a grey colored theme. There are other themes available in the documentation.

# [Header](#toc.xhtml_s163a)

We are providing few props to the component. The **`company`** prop is used to set Title (Phonebook) for the App. The **`platformName`** (App) is a subtitle. We are the using a state **`isSideNavOpen`** to show hide the sidebar. The **`persistentHamburgerMenu`** prop is used to show hamburger button to open close the sidebar.

# [SideNav](#toc.xhtml_s164a)

We are using it along with **`SideNavItems`** to show **`Login`**, **`Register`** and **`Logout`** buttons. Our logic will be to show **`Login`** and **`Register`** buttons for unauthorized user and show **`Logout`** button to authorized user. This logic is written in **`Authentication.svelte`** file as follows:

1.  `<script>`
2.  `  import Button from “snel-carbon/components/Button”;`
3.  `  import ButtonSet from “snel-carbon/components/Button/ButtonSet.svelte”;`
4.  `  import Link from “svelte-routing/Link.svelte”;`
5.  `  import { accessToken } from “../utils/stores.ts”;`
6.  `  import Login16 from “snel-carbon/icons/Login16”;`
7.  `  import Logout16 from «snel-carbon/icons/Logout16»;`
8.  `</script>`

10.  `<div class=”auth-container”>`
11.  `  <ButtonSet stacked>`
12.  `    {#if !$accessToken}`
13.  `      <Link to=”/login”>`
14.  `        <Button kind=”ghost” icon={Login16}>Login</Button>`
15.  `      </Link>`
16.  `      <Link to=”/register”>`
17.  `        <Button kind=”ghost”>Register</Button>`
18.  `      </Link>`
19.  `    {:else}`
20.  `      <Link to=”/”>`
21.  `        <Button`
22.  `          kind=”ghost”`
23.  `          icon={Logout16}`
24.  `          on:click={() => {`
25.  `            localStorage.removeItem(“accessToken”);`
26.  `            $accessToken = “”;`
27.  `          }}`
28.  `        >`
29.  `          Logout`
30.  `        </Button>`
31.  `      </Link>`
32.  `    {/if}`
33.  `  </ButtonSet>`
34.  `</div>`

36.  `<style>`
37.  `  .auth-container {`
38.  `    margin: 10px;`
39.  `    display: flex;`
40.  `    flex-direction: column;`
41.  `    justify-content: space-between;`
42.  `  }`
43.  `</style>`

In the preceding code, we are using carbon components **`Button`**, **`ButtonSet`** along with carbon icons **`Login16`**, **`Logout16`**. We are also importing **`Link`** component from svelte-routing and accessToken from store. The **`Link`** component is used to set url address to login, register etc. We are using **`accessToken`** to show either Login, Register buttons or Logout button. If the **`accessToken`** is valid, then we will show Logout button or else Login and Register buttons.

The **`ButtonSet`** is used to show group of buttons (Login, Register). We are passing few props to each Button component. The **`kind`** defines type of button (here, ghost). The **`icon`** prop is used to show icon in the button. We are using Login16 and Logout16 icons from snel-carbon for Login and Logout buttons respectively.

# [Conclusion](#toc.xhtml_s165a)

We have implemented a svelte application UI in this chapter using various deno modules like **`snel`**, **`snel-carbon`**, **`axiod`**, and so on. Snel module is useful for creation of Svelte applications using deno runtime. **Snel-carbon** provides components, icons based on carbon design system. We used these components, icons to create our UI. **Axiod** is used to make network requests to the server. **Svelte Routing** module is used to define various routes (public and private) for the app. We used **trex** provided by snel by default to run the scripts.

This knowledge will be helpful to set up a new deno project for Svelte UI Application. We can test the implementation by running it along with the API server from previous chapter. With this, our *Phonebook* App is completed and can be used locally or can be deployed to cloud using various platforms.

# [Index](#toc.xhtml_ind)

A

Aleph.js [66](#c05.xhtml_page66)

Application Programming Interface (API) [71](#c05.xhtml_page71), [72](#c05.xhtml_page72)

Command Line Interface (CLI) [67](#c05.xhtml_page67)

features [66](#c05.xhtml_page66), [67](#c05.xhtml_page67)

pages [68](#c05.xhtml_page68), [69](#c05.xhtml_page69)

routing [69](#c05.xhtml_page69)-[71](#c05.xhtml_page71)

arguments [47](#c04.xhtml_page47), [48](#c04.xhtml_page48)

B

basic types, TypeScript [14](#c02.xhtml_page14)

abstract [29](#c02.xhtml_page29)

classes [22](#c02.xhtml_page22)

Getter and Setter [26](#c02.xhtml_page26)

interfaces [15](#c02.xhtml_page15), [16](#c02.xhtml_page16)

interfaces, versus type aliases [18](#c02.xhtml_page18)

intersections [21](#c02.xhtml_page21)

modifiers [22](#c02.xhtml_page22)

optional properties [16](#c02.xhtml_page16)

read only properties [16](#c02.xhtml_page16)

static [28](#c02.xhtml_page28)

type aliases [17](#c02.xhtml_page17)

type assertions [20](#c02.xhtml_page20)

type inference [19](#c02.xhtml_page19)

unions [20](#c02.xhtml_page20)

bundle command [46](#c04.xhtml_page46)

C

cache command [46](#c04.xhtml_page46)

class [22](#c02.xhtml_page22)

entities [22](#c02.xhtml_page22)

classes [55](#c04.xhtml_page55), [56](#c04.xhtml_page56)

command line interface (CLI) [44](#c04.xhtml_page44)

compile command [47](#c04.xhtml_page47)

compiler [8](#c01.xhtml_page8)

completions command [47](#c04.xhtml_page47)

ContactForm [169](#c09.xhtml_page169), [173](#c09.xhtml_page173), [174](#c09.xhtml_page174)

ContactTable with Toolbar [168](#c09.xhtml_page168)

cross-origin resource sharing (CORS) [141](#c08.xhtml_page141)

D

databases

MongoDB [39](#c03.xhtml_page39)

MongoDB Atlas [39](#c03.xhtml_page39)

PostgreSQL [39](#c03.xhtml_page39)

data types, in TypeScript

any [15](#c02.xhtml_page15)

array [15](#c02.xhtml_page15)

Boolean [14](#c02.xhtml_page14)

enum [15](#c02.xhtml_page15)

never [15](#c02.xhtml_page15)

null [15](#c02.xhtml_page15)

number [14](#c02.xhtml_page14)

object [15](#c02.xhtml_page15)

string [14](#c02.xhtml_page14)

tuple [15](#c02.xhtml_page15)

undefined [15](#c02.xhtml_page15)

unknown [15](#c02.xhtml_page15)

void [15](#c02.xhtml_page15)

Deno [1](#c01.xhtml_page1), [2](#c01.xhtml_page2)

features [2](#c01.xhtml_page2)-[5](#c01.xhtml_page5)

installing [34](#c03.xhtml_page34), [35](#c03.xhtml_page35)

versus, Node [4](#c01.xhtml_page4)

Deno CLI [45](#c04.xhtml_page45)

environment variables [45](#c04.xhtml_page45)

file watcher [49](#c04.xhtml_page49)

passing arguments [47](#c04.xhtml_page47), [48](#c04.xhtml_page48)

permission flags [49](#c04.xhtml_page49)

permissions allow-list [50](#c04.xhtml_page50), [51](#c04.xhtml_page51)

DENO_DIR [45](#c04.xhtml_page45)

Deno ecosystem [43](#c04.xhtml_page43)

Deno foundation stack [6](#c01.xhtml_page6)

Rust [6](#c01.xhtml_page6), [7](#c01.xhtml_page7)

tokio I/O library [7](#c01.xhtml_page7)

V8 engine by Google [6](#c01.xhtml_page6)

Deno global APIs [52](#c04.xhtml_page52)-[54](#c04.xhtml_page54)

DENO_INSTALL_ROOT [45](#c04.xhtml_page45)

Deno modules [56](#c04.xhtml_page56)

registries [61](#c04.xhtml_page61)

standard library [56](#c04.xhtml_page56)-[58](#c04.xhtml_page58)

third-party modules [58](#c04.xhtml_page58)-[61](#c04.xhtml_page61)

Deno runtime APIs [51](#c04.xhtml_page51)

classes [55](#c04.xhtml_page55), [56](#c04.xhtml_page56)

Deno global APIs [52](#c04.xhtml_page52)-[54](#c04.xhtml_page54)

variables [54](#c04.xhtml_page54), [55](#c04.xhtml_page55)

Web APIs [51](#c04.xhtml_page51), [52](#c04.xhtml_page52)

deps.ts

central dependencies [62](#c04.xhtml_page62), [63](#c04.xhtml_page63)

development tools [35](#c03.xhtml_page35)

databases [39](#c03.xhtml_page39)

Docker [38](#c03.xhtml_page38)

Docker Compose [38](#c03.xhtml_page38)

Git [37](#c03.xhtml_page37)

GitHub [37](#c03.xhtml_page37)

Postman [38](#c03.xhtml_page38)

Redis [40](#c03.xhtml_page40)

Silver Searcher [38](#c03.xhtml_page38)

terminal [35](#c03.xhtml_page35)

Vim [36](#c03.xhtml_page36), [37](#c03.xhtml_page37)

VS Code [37](#c03.xhtml_page37)

VS Code extensions [37](#c03.xhtml_page37)

zsh + oh my zsh [36](#c03.xhtml_page36)

doc command [46](#c04.xhtml_page46)

Docker [38](#c03.xhtml_page38)

Docker Compose [38](#c03.xhtml_page38)

Dynamic API routes [72](#c05.xhtml_page72)

Dynamic Routes [69](#c05.xhtml_page69)

dynamic typing

versus, static typing [30](#c02.xhtml_page30)

E

Electron.js [3](#c01.xhtml_page3)

environment variables [45](#c04.xhtml_page45)

eval command [46](#c04.xhtml_page46)

event loop [4](#c01.xhtml_page4)

Explicit typing [19](#c02.xhtml_page19)

F

file watcher [49](#c04.xhtml_page49)

First In First Out (FIFO) principle [10](#c01.xhtml_page10)

fmt command [46](#c04.xhtml_page46)

G

Git [37](#c03.xhtml_page37)

GitHub [37](#c03.xhtml_page37)

GraphQL [100](#c07.xhtml_page100)

autogenerated API documentation [104](#c07.xhtml_page104), [105](#c07.xhtml_page105)

core concepts [105](#c07.xhtml_page105)

features [100](#c07.xhtml_page100)

fragments [103](#c07.xhtml_page103), [104](#c07.xhtml_page104)

precise fetching [101](#c07.xhtml_page101)

Schema [105](#c07.xhtml_page105), [106](#c07.xhtml_page106)

single API endpoint [101](#c07.xhtml_page101), [102](#c07.xhtml_page102)

validation and type checking [102](#c07.xhtml_page102)

H

help command [45](#c04.xhtml_page45)

Heroku [40](#c03.xhtml_page40)

Hot Module Replacement (HMR) [66](#c05.xhtml_page66)

hydration process [69](#c05.xhtml_page69)

I

Implicit typing [19](#c02.xhtml_page19)

install command [46](#c04.xhtml_page46)

interpreter [8](#c01.xhtml_page8)

J

JavaScript engine [7](#c01.xhtml_page7)

compiler [8](#c01.xhtml_page8)

interpreter [8](#c01.xhtml_page8)

JavaScript runtime [9](#c01.xhtml_page9)

call back [9](#c01.xhtml_page9)

callback queue [10](#c01.xhtml_page10)

Deno API [9](#c01.xhtml_page9)

event loop [10](#c01.xhtml_page10)

memory heap [9](#c01.xhtml_page9)

reference link [4](#c01.xhtml_page4)

tokio [9](#c01.xhtml_page9)

JSON Web Token (JWT) [137](#c08.xhtml_page137)

L

Last In First Out (LIFO) principle [9](#c01.xhtml_page9)

layout, PhoneBook App [174](#c09.xhtml_page174), [175](#c09.xhtml_page175)

header [175](#c09.xhtml_page175)

SideNav [175](#c09.xhtml_page175), [177](#c09.xhtml_page177)

libuv event loop [3](#c01.xhtml_page3), [4](#c01.xhtml_page4)

M

modifiers [22](#c02.xhtml_page22)

private [23](#c02.xhtml_page23)

protected [24](#c02.xhtml_page24)

public [22](#c02.xhtml_page22)

module registries [61](#c04.xhtml_page61), [62](#c04.xhtml_page62)

MongoDB [39](#c03.xhtml_page39)

URL [39](#c03.xhtml_page39)

MongoDB Atlas [39](#c03.xhtml_page39)

URL [39](#c03.xhtml_page39)

mutations [100](#c07.xhtml_page100)

N

Nested Routes [71](#c05.xhtml_page71)

Node [3](#c01.xhtml_page3)

asynchronous and event-driven architecture [3](#c01.xhtml_page3)

node package manager (npm) [4](#c01.xhtml_page4)

performance [4](#c01.xhtml_page4)

versus, Deno [4](#c01.xhtml_page4)

O

Oak [111](#c07.xhtml_page111)

Oak-GraphQL middleware [112](#c07.xhtml_page112)-[114](#c07.xhtml_page114)

Oak GraphQL server setup [118](#c08.xhtml_page118)-[121](#c08.xhtml_page121)

Object–relational mapping (ORM) [116](#c08.xhtml_page116)

open-source [3](#c01.xhtml_page3), [4](#c01.xhtml_page4)

OverflowMenu [168](#c09.xhtml_page168)

P

pages, Aleph.js [68](#c05.xhtml_page68), [69](#c05.xhtml_page69)

permission flags [49](#c04.xhtml_page49)

permissions allow-list [50](#c04.xhtml_page50)

persistentHamburgerMenu prop [175](#c09.xhtml_page175)

PhoneBook App, API implementation [115](#c08.xhtml_page115)

authentication [137](#c08.xhtml_page137)-[141](#c08.xhtml_page141)

controllers [134](#c08.xhtml_page134)-[137](#c08.xhtml_page137)

database setup [130](#c08.xhtml_page130), [131](#c08.xhtml_page131)

initial setup [116](#c08.xhtml_page116)

models [131](#c08.xhtml_page131)-[134](#c08.xhtml_page134)

Schema [121](#c08.xhtml_page121)-[123](#c08.xhtml_page123)

Trex, as package manager [117](#c08.xhtml_page117)

velociraptor, as script runner [117](#c08.xhtml_page117), [118](#c08.xhtml_page118)

version control, with git [116](#c08.xhtml_page116)

PhoneBook App, UI implementation [143](#c09.xhtml_page143)

initial setup [144](#c09.xhtml_page144)

layout [174](#c09.xhtml_page174), [175](#c09.xhtml_page175)

routes [147](#c09.xhtml_page147)-[149](#c09.xhtml_page149)

Snel Carbon installation [146](#c09.xhtml_page146), [147](#c09.xhtml_page147)

snel setup [144](#c09.xhtml_page144)-[146](#c09.xhtml_page146)

platform as a service (PAAS) [40](#c03.xhtml_page40)

Pomodoro [41](#c03.xhtml_page41)

PostgreSQL [39](#c03.xhtml_page39)

Postman [38](#c03.xhtml_page38)

pre-rendered [69](#c05.xhtml_page69)

Profiler [8](#c01.xhtml_page8)

Q

query [100](#c07.xhtml_page100)

R

React.js [3](#c01.xhtml_page3)

React Native [3](#c01.xhtml_page3)

relational database management system (RDBMS) [39](#c03.xhtml_page39)

Remote Dictionary Server (Redis) [40](#c03.xhtml_page40)

Representational State Transfer (REST) API [66](#c05.xhtml_page66)

resolver [108](#c07.xhtml_page108)-[111](#c07.xhtml_page111)

Route component [147](#c09.xhtml_page147)

routes [147](#c09.xhtml_page147)-[149](#c09.xhtml_page149)

ContactForm [169](#c09.xhtml_page169)-[174](#c09.xhtml_page174)

contacts [160](#c09.xhtml_page160)-[165](#c09.xhtml_page165)

ContactTable [165](#c09.xhtml_page165)-[168](#c09.xhtml_page168)

home [157](#c09.xhtml_page157), [158](#c09.xhtml_page158)

login [150](#c09.xhtml_page150)-[153](#c09.xhtml_page153)

NotFound [158](#c09.xhtml_page158), [159](#c09.xhtml_page159)

private [159](#c09.xhtml_page159), [160](#c09.xhtml_page160)

register [153](#c09.xhtml_page153)-[157](#c09.xhtml_page157)

routing [69](#c05.xhtml_page69)

run command [46](#c04.xhtml_page46)

Rust [6](#c01.xhtml_page6), [7](#c01.xhtml_page7)

S

Schema Definition Language (SDL) [105](#c07.xhtml_page105)

Schema, PhoneBook App [121](#c08.xhtml_page121), [123](#c08.xhtml_page123)

contact type [124](#c08.xhtml_page124)

CreateContact input [125](#c08.xhtml_page125)

login type [124](#c08.xhtml_page124)

LoginUser Input [124](#c08.xhtml_page124)

Mutation type [125](#c08.xhtml_page125)

Query type [125](#c08.xhtml_page125)

RegisterUser Input [124](#c08.xhtml_page124)

resolvers [125](#c08.xhtml_page125), [129](#c08.xhtml_page129), [130](#c08.xhtml_page130)

UpdateContact input [125](#c08.xhtml_page125)

UpdateUser Input [124](#c08.xhtml_page124)

user type [123](#c08.xhtml_page123)

Schema, Todos App [105](#c07.xhtml_page105), [106](#c07.xhtml_page106)

inputs [107](#c07.xhtml_page107)

mutation [108](#c07.xhtml_page108)

query [107](#c07.xhtml_page107), [108](#c07.xhtml_page108)

relationship [108](#c07.xhtml_page108)

resolver [108](#c07.xhtml_page108)-[111](#c07.xhtml_page111)

type [107](#c07.xhtml_page107)

SideNavItems [175](#c09.xhtml_page175)

Silver Searcher [38](#c03.xhtml_page38)

Snel-Carbon [146](#c09.xhtml_page146)

standard library [56](#c04.xhtml_page56)-[58](#c04.xhtml_page58)

static typing

versus, dynamic typing [30](#c02.xhtml_page30)

styled components [88](#c06.xhtml_page88)-[90](#c06.xhtml_page90)

subcommands [45](#c04.xhtml_page45)

bundle [46](#c04.xhtml_page46)

cache [46](#c04.xhtml_page46)

compile [47](#c04.xhtml_page47)

completions [47](#c04.xhtml_page47)

doc [46](#c04.xhtml_page46)

eval [46](#c04.xhtml_page46)

fmt [46](#c04.xhtml_page46)

help [45](#c04.xhtml_page45)

install [46](#c04.xhtml_page46)

run [46](#c04.xhtml_page46)

test [46](#c04.xhtml_page46)

subscriptions [100](#c07.xhtml_page100)

Svelte Routing library [147](#c09.xhtml_page147)

T

test command [46](#c04.xhtml_page46)

third-party modules [58](#c04.xhtml_page58)-[61](#c04.xhtml_page61)

Tmux [40](#c03.xhtml_page40)

Todos API [74](#c05.xhtml_page74)

DELETE [82](#c05.xhtml_page82)-[86](#c05.xhtml_page86)

GET (list) [75](#c05.xhtml_page75), [76](#c05.xhtml_page76)

GET (object) [82](#c05.xhtml_page82)-[86](#c05.xhtml_page86)

PATCH [82](#c05.xhtml_page82)-[86](#c05.xhtml_page86)

POST [76](#c05.xhtml_page76)-[81](#c05.xhtml_page81)

Todos App [66](#c05.xhtml_page66)

initializing [73](#c05.xhtml_page73)

project structure [73](#c05.xhtml_page73), [74](#c05.xhtml_page74)

UI implementation [87](#c06.xhtml_page87)

Todos components

creating [91](#c06.xhtml_page91)

TodoDetails [94](#c06.xhtml_page94)-[97](#c06.xhtml_page97)

TodoList [91](#c06.xhtml_page91)-[94](#c06.xhtml_page94)

tokio I/O library [7](#c01.xhtml_page7)

tsconfig.json [32](#c02.xhtml_page32)

TypeScript [11](#c02.xhtml_page11), [12](#c02.xhtml_page12)

basic types [14](#c02.xhtml_page14)

benefits [13](#c02.xhtml_page13)

features [13](#c02.xhtml_page13)

setup [31](#c02.xhtml_page31)

static, versus dynamic typing [30](#c02.xhtml_page30)

strong, versus weak typing [31](#c02.xhtml_page31)

tsconfig.json [32](#c02.xhtml_page32)

type system [102](#c07.xhtml_page102)

U

UI implementation

Todos App [87](#c06.xhtml_page87)

PhoneBook App [143](#c09.xhtml_page143)

V

V8 engine, by Google [6](#c01.xhtml_page6)

V8 JavaScript engine [8](#c01.xhtml_page8)

variables [54](#c04.xhtml_page54), [55](#c04.xhtml_page55)

Vim [36](#c03.xhtml_page36), [37](#c03.xhtml_page37)

VS Code [37](#c03.xhtml_page37)

extensions [37](#c03.xhtml_page37)

W

Web APIs [51](#c04.xhtml_page51), [52](#c04.xhtml_page52)

Z

zsh + oh my zsh [36](#c03.xhtml_page36)
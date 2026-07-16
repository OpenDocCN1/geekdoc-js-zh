![](images/cover.jpg)

![Cover](images/cover.jpg)

Copyright © 2024 BPB Online

*All rights reserved.* No part of this book may be reproduced, stored in a retrieval system, or transmitted in any form or by any means, without the prior written permission of the publisher, except in the case of brief quotations embedded in critical articles or reviews.

Every effort has been made in the preparation of this book to ensure the accuracy of the information presented. However, the information contained in this book is sold without warranty, either express or implied. Neither the author, nor BPB Online or its dealers and distributors, will be held liable for any damages caused or alleged to have been caused directly or indirectly by this book.

BPB Online has endeavored to provide trademark information about all of the companies and products mentioned in this book by the appropriate use of capitals. However, BPB Online cannot guarantee the accuracy of this information.

First published: 2024

Published by BPB Online

WeWork

119 Marylebone Road

London NW1 5PU

**UK | UAE | INDIA | SINGAPORE**

ISBN 978-93-55518-750

[www.bpbonline.com](https://www.bpbonline.com)

**Dedicated to**

*For **Cathy***

Love of my Life, Wife, Best Friend,
Inspiration and Anchor,
Without whom this would not have been possible

# About the Author

**Clive Harber** has been programming computers since he was 13\. He holds a Master's degree in Chemical Engineering from the University of Wales, Swansea and diplomas in Marine Biology and Art History. Having written code in a number of programming languages and different paradigms over the years for the sports and betting industries, telecommunications, health care, retail and entertainment sectors, he is now at a point where he feels he can be useful to the programming community as a whole.

Clive has previously co-written two other books – Getting MEAN with MongoDB, Express, Angular and Node 2nd ed and Implementing Cloud Design Patterns for AWS 2nd ed, and has been a reviewer and technical reviewer on more than 10 other widely available books on a variety of technical subjects (Frontend frameworks – Vue.js/React/Web Components, testing, Elixir, UI/UX, Microservices, desktop applications). He has been using Vue.js for several years on multiple projects.

Currently, Clive runs his own consultancy providing expertise in building web and mobile applications using Node, Vue.js, Quasar, NativeScript, Elm, Elixir and PhoenixFramework.

# About the Reviewer

Ivan Almaši is a full-time Frontend Developer. He has been working as a contractor/freelancer for the past 6 years and the last 5 years almost exclusively in the Vue.js ecosystem during which he worked on different projects, most notably a SaaS enterprise solution for quality assurance. His experience also includes converting designs to pixel-perfect UIs utilizing Tailwind CSS.

# Acknowledgements

I want to express my deepest gratitude to my family and friends for their unwavering support and encouragement throughout this book's writing, especially my wife Cathy and my children, Jacob and Rebecca.

I am also grateful to BPB Publications for their guidance and expertise in bringing this book to fruition. It was a long journey of building this book, with valuable participation and collaboration of reviewers, technical experts, and editors.

I would also like to acknowledge the valuable contributions of my colleagues and co-workers during many years working in the tech industry, who have taught me so much and provided valuable feedback on my work.

Thank you to all the readers who have taken the time to read this book. I hope that this will help you in your future endeavours.

Lastly, burn out, depression, anxiety and imposter syndrome are real things that we can all suffer from. If you are effected by any of these, speak up and ask for help, the world is a better place for you in it.

# Preface

Knowing where to start with any element of building software is usually half the battle. There are a plethora of options, myriad of opinions and multiple ways of doing things, so finding the best way can prove to be very daunting. This book is a good place to begin getting acquainted with frontend development using Vue.js.

This book is designed to give insight into not only the framework, but also how the industry works, some questions you might face at interview, plus some handy pointers of the wider Vue.js ecosystem that you might need to understand, or use as a springboard for your own projects.

This is not a total beginners manual, you will need to know the basics of HTML, CSS and some JavaScript already. You might have completed some self- or college study, already have a year or two of industry experience or transitioning from a different framework. You will be covering some of the more advanced topics that you might not have come across before, that you will need in order to create maintainable code and advance your career.

We will be bringing you Vue.js from the ground up, so do not have to worry about that. Once we have the basics of Vue.js under our collective belts, we will forge ahead through standard uses such as front-side routing and state management before you finally cover some advanced, more modern, topics, such as server-side rendering and building for mobile which are not ordinarily covered in books like this.

With this book, you will gain knowledge and experience of the Vue.js framework and its ecosystem, learn how to use the framework to solve problems and build easy to maintain user interfaces that can be used across many different display devices. We hope that you find this book interesting, helpful and informative, regardless of which stage your career is at.

[Chapter 1: Introducing Front-End Development with Vue.js](#ch01.xhtml) – this is the start of your journey. This chapter covers web development as a paradigm, where it came from, and where it is going. You will then get a 10,000 ft view of the framework, where it fits in and how it can improve your working life.

[Chapter 2: Working in Vue.js Roles](#ch02.xhtml) – this chapter gives you an overview of the job roles that might be on offer and the kinds of work that you can expect to do and how you might progress in your career. We will also cover different types of company and how developers fit into these organizations, and how you might progress your learning.

[Chapter 3: HTML, CSS, and JS/TS for Extra Credit](#ch03.xhtml) – presents more advanced topics that underpin the use of Vue.js. We will cover virtual DOM, CSS rules and specificity, before digging into JavaScript's many different capabilities and covering the basics of TypeScript. This chapter gives you many tools that you might not have in order to become a successful developer. You will also go over various API's that JavaScript enables you to access so that you have an understanding of what capabilities the browser provides.

[Chapter 4: Understanding the Vue.js Instance](#ch04.xhtml) - you will start your Vue.js journey by understanding the base technology and how to structure your components. In this chapter you will get exposed to the Options API variant of Vue.js components as a basic starting point. You will also gain understanding of the life cycle and how to hook into it to get better control of your component state.

[Chapter 5: Designing Component-Based UIs and Single Page Applications](#ch05.xhtml) – throughout this chapter you will gain an understanding of how UIs can be constructed. This is not a chapter on design tools, but provides you, the developer, the tools and knowledge required to break apart a design and determine the interactions that you might need to build. Here you will be starting a prototype project from a given design.

[Chapter 6: Using the Composition API to Manage Component Logic](#ch06.xhtml) – gives attention to the modern way of building Vue.js components. You will understand how to segment your components in order to reuse functionality across many different components. This way of building components was an optional add-on in Vue2 and baked into Vue3\. It is fast becoming the default way of constructing user interfaces with the Vue framework.

[Chapter 7: Creating and Setting Up a Vue.js Application with Vue CLI and Vite](#ch07.xhtml) – so far we have seen how to build components in different ways and how to make them fit together. This chapter looks, in detail, at how to bootstrap Vue.js projects quickly in order to get the most out of the framework. Of the various ways that are available for starting Vue.js projects, we will discuss using the Vue CLI, the old way, and Vite, the new way, in detail. You will start building the prototype project in this chapter.

[Chapter 8: Adding a CSS Framework to the Mix – TailwindCSS, Bootstrap or Foundation](#ch08.xhtml) – when working at a professional level, it is unlikely that you will be creating your own CSS for standard display elements. It is more likely that you will be using a CSS framework , hence, you will need to know how to integrate these frameworks into your application stack. This chapter covers integrating the three most widely used CSS frameworks. This chapter will equip you to expand the prototype project with TailwindCSS.

[Chapter 9: Building User Interfaces with Components](#ch09.xhtml) – expands the readers' knowledge of building components through building the prototype project. We will be pulling together all the knowledge we have gained and putting it into practise. After working through setting up a working directory structure that suits our needs, we will set up the basic component templates and construct the various layouts that the project needs.

[Chapter 10: Routing Between Pages with VueRouter](#ch10.xhtml) – single page applications are very limited without being able to navigate between the various “pages”. After the last chapter, we'll be expanding the prototype with more pages using VueRouter. We'll also discuss how VueRouter helps you direct and manage navigation based on state – authentication we're looking at you…

[Chapter 11: Interacting with the UI Using Events](#ch11.xhtml) – at the moment, the UI is fairly boring. You can't have an event driven UI without events and in this chapter you'll understand the Vue.js events system, from standard DOM events to custom events and basic component to component state management. Events are one of the cornerstones of building effective UIs, and interacting with your user, but also having components interact with each other. With this understanding, we'll expand the prototype application to respond to users.

[Chapter 12: Building Forms and Handling User Input](#ch12.xhtml) – the next vital element that we need to learn is how to obtain information from your users and manage this data effectively so that it doesn't pollute your database, or expose your application to attack. Not only will you learn how to effectively build forms and manage the data within them, you will also get necessary experience in validating this data to ensure that it conforms to expected inputs, informing the user if it does not. The prototype application will also not be forgotten, we'll add forms to collect user data

[Chapter 13: Managing State with Pinia and API Communication](#ch13.xhtml) – when building component based applications, as the application grows, it becomes necesssary to bring all the available state together into a store. This is where Pinia comes into play – the standard state management tool for the Vue.js ecosystem. Once we have understood how to utilise Pinia, we will cover the various ways we can get data into the application from a remote server. For this we will integrate data obtained via JSON ReST APIs and GraphQL.

[Chapter 14: Testing Vue.js Applications](#ch14.xhtml) – understanding testing and how to test your application is vitally important. In a professional context, you will most likely end up writing more code in test files than you will for your actual application. This is normal, but many juniors (or those that are self-taught) do not understand the importance of testing. By the end of this chapter, you will understand this and more. We will go over component and unit tests, integration tests and end-to-end testing and show that it does not need to be complicated.

[Chapter 15: Server-Side Rendering with Nuxt.js](#ch15.xhtml) – with the core functionality now covered, it is time to strike out and look at some parts of the wider ecosystem. One of the biggest trends at the moment is server-side rendering, where for the Vue.js
ecosystem, Nuxt.js is one of the bigger players. This chapter covers the basics of building a site with Nuxt.js, which combines much of what we have already covered, but in new and interesting ways.

[Chapter 16: Building Multi-tenanted Apps with Quasar](#ch16.xhtml) – in this final content-rich chapter, we will explore Quasar, one of the many ways of getting your web application available across many different platforms using Vue.js and not having to learn a mobile-native language. Quasar allows you to build different types of applications that have the same UI implementation in common, reducing time to market and engineering overhead. This chapter aims to add this one size fits all framework to your toolbox.

[Chapter 17: Interview Questions](#ch17.xhtml) – what good is learning all of this, if when you get to interview, and cannot answer any questions. This last chapter of the book goes some way to preparing you for technical questions that might be asked, plus provides pointers to other areas that you might need knowledge of.

# Code Bundle and Coloured Images

Please follow the link to download the

***Code Bundle*** and the ***Coloured Images*** of the book:

[https://rebrand.ly/93x9jcr](https://rebrand.ly/93x9jcr)

The code bundle for the book is also hosted on GitHub at **[https://github.com/bpbpublications/Vue.js-for-Jobseekers](https://github.com/bpbpublications/Vue.js-for-Jobseekers)**. In case there’s an update to the code, it will be updated on the existing GitHub repository.

We have code bundles from our rich catalogue of books and videos available at [**https://github.com/bpbpublications**](https://github.com/bpbpublications). Check them out!

Errata

We take immense pride in our work at BPB Publications and follow best practices to ensure the accuracy of our content to provide with an indulging reading experience to our subscribers. Our readers are our mirrors, and we use their inputs to reflect and improve upon human errors, if any, that may have occurred during the publishing processes involved. To let us maintain the quality and help us reach out to any readers who might be having difficulties due to any unforeseen errors, please write to us at :

**[errata@bpbonline.com](mailto:errata@bpbonline.com)**

Your support, suggestions and feedbacks are highly appreciated by the BPB Publications’ Family.

**Join our book’s Discord space**

Join the book’s Discord Workspace for Latest updates, Offers, Tech happenings around the world, New Release and Sessions with the Authors:

**[https://discord.bpbonline.com](https://discord.bpbonline.com)**

![](images/fm1.png)

# [CHAPTER 1Introducing Front-End Development with Vue.js](#contents.xhtml_ch01a)

[Introduction](#contents.xhtml_sc2_1a)

Vue.js is the front-end framework of choice for numerous large companies and many small ones. These companies have chosen this framework over its many competitors due to its small footprint, easy-to-use semantics, predictable behavior and simple way to provide extensions. As a front-end framework, Vue.js helps you build user-friendly, functionality-rich and data-rich UI's that are easy to maintain and deploy.

In this chapter, we will be exploring where and how Vue.js fits into front-end development, how Vue.js compares with its contemporaries and finally, how to use the framework at the 10,000ft view.

[Structure](#contents.xhtml_sc2_2a)

We will be covering the following topics in this chapter:

*   A brief history of web development
*   The rise of Vue.js
*   Comparing Vue.js with the competition
*   Using Vue.js to solve problems – Case studies

[Objectives](#contents.xhtml_sc2_3a)

This chapter explores where Vue.js comes from and how it is used.

In this chapter, you will be introduced to Vue.js as a technology, learn the basics of Vue.js single file components, and understand where Vue.js fits in the development ecosystem.

You don't need to know anything special to go through this chapter; everything will be explained over the course of the book.

[A brief history of web development](#contents.xhtml_sc2_4a)

Over the years, front-end development has changed significantly from building complete pages using the humble triad of HTML, CSS and JavaScript. As applications became more complicated, and companies and consumers wanted more, jQuery (and similar) filled this functionality gap. There were, however, significant issue with the libraries in that the functionality created to manipulate the HTML document object model (DOM) with JavaScript was intermingled with the data that was being used to power that manipulation. This, in turn, made it more difficult to extract and maintain this functionality; large applications started taking significant effort to build and maintain, increasing development time and application development cost.

In this landscape, web development frameworks based on the Model-View-Controller (MVC) pattern were being created, initial attempts gaining small pockets of traction. The MVC pattern is a standard pattern that dictates how to manage data flow between different parts of an application.

As a brief explanation, the Controller receives a message/request and processes it. The Controller then passes on a request for data from the Model. The Model returns the data that then gets passed on to the View to create the UI, as shown in [Figure 1.1](#ch01.xhtml_fig1-1):

![Diagram Description automatically generated](images/figure1.1.png)

Figure 1.1: Model-View-Controller Pattern

For those who have been around a while, we're talking about the frameworks Knockout.js, Backbone.js, Dojo.js and MooTools.

Then, Google released Angular and at roughly the same time, Node.js, a JavaScript engine that runs on a server rather than a browser, gained prominence in web development circles. Overnight, everything changed – the MongoDB, Express, Angular and Node (MEAN) stack was born, and an explosion of frameworks, tooling and concepts occurred, with companies wanting to utilize this change in technology. As with everything, faster ways of building web UIs came about, and Google went back to the drawing board with Angular.

While this was happening, Facebook dropped React.js on the world. With its quicker “conception to deployment” time and shallower learning curve, React.js had been set to take over the world. However, the learning curve for React isn't shallow enough for some, and it has various idiosyncrasies that are unpalatable for others.

In order to smooth out some of the perceived issues in both Angular and React, Angular core team member Evan You created Vue.js. In many ways, Vue.js and React.js are similar, but they are very different in terms of execution.

With its leaner implementation, faster execution time, and reliance on standard technologies, Vue.js has become one of the top three front-end JavaScript frameworks in use by companies today.

[The rise of Vue.js](#contents.xhtml_sc2_5a)

Since its creation in 2014, Vue.js has had a steady rise in uptake. While many companies tended to take the decision to use React due to its association with Facebook, developers tended to like the simpler learning curve and cleaner interface provided by Vue.js.

Slowly, over time and with the backing of large companies like Alibaba, Font Awesome, Gitlab, and Apple, Vue.js has gained traction in the development community. And over recent years, Vue has joined React and Angular as one of the three most used JS front-end frameworks in use by corporations and enterprise-sized organizations today.

The short bootstrapping time and ease of development also makes Vue.js ideal for SME's and start-ups.

There's plenty of scope for jobseekers of all kinds.

[Comparing Vue.js with the competition](#contents.xhtml_sc2_6a)

If you take the time to look at the “Best frameworks to learn in…” or the “React vs Angular vs Vue” blog posts, more often than not you'll end up reading some contrived half-formed, badly articulated opinion of why framework X is the best as per the authors' limited experience, not that all these types of articles should be seen as equal, some are well thought out and balanced.

As a reader, you've probably already decided that there is something behind the hype of Vue.js, but I'll try to be balanced. Let's take a look:

Do you need to have specialist knowledge beyond the framework?

Well, no; not unless you want to; the core technologies used in Vue.js are HTML, CSS and JavaScript. If you want to use SCSS, Less, JSX, TypeScript or something else, then you can, but it's not essential, unlike the other frameworks. When working with React, you need to learn and understand JSX, you also need to understand some of the more advanced JS idioms. React does however give the choice of using ReasonML if you're feeling more adventurous. Angular requires TypeScript. While TypeScript is not very different from JavaScript, it does add overhead to the learning curve.

Does everything need to be rebuilt to make the project fit the framework?

Again, the answer is no. Vue.js is not overly opinionated and therefore, tends to not get in the way. You can just drop Vue.js into your project and use your existing dependencies. While this is also mostly possible with React or Elm, it's not possible with Angular or Svelte.

Is the framework large? Does it load quickly?

The speed at which the JS is made available to the browser is dependent on file size; the smaller the file, the quicker it downloads – stands to reason, doesn't it? The core framework at version 2 has been found to weigh around 24kB when it has been minified and gzipped for production deployments, and version 3 has been pinned to about 33kB. This makes it small in terms of memory footprint and therefore, quick to download. Compare this to React, which weighs 99kB (split between the core at ~6.5kB and react-dom at ~92.5kB) and Angular at a hefty ~563kB. Frameworks like Elm or Svelte have a varying package size because of the way they are built and deployed.

Does the rendering speed matter?

Quicker, snappier rendering gives your users a better experience. The better the experience, the more likely they are to return or convert. Vue.js uses a virtual DOM, similar to React with a similar rendering and page update speed.

Can you use the framework to bootstrap an application quickly to get user feedback?

Vue.js can be injected straight into a web page. Additionally, with the CLI and UI, bootstrapping and managing dependencies is quick and easy. Single file components can be built, tested, integrated, and iterated over quickly. Reduced development time of prototypes and new features has benefits of getting these out to users quicker, which, in turn, gives compressed feedback cycles and faster iterations.

[Using Vue.js to solve problems – Case studies](#contents.xhtml_sc2_7a)

Vue.js lends itself to many use cases to cater for different situations, so you can dip your toe in or go whole hog – Vue.js has your back.

These case studies are just to give you an idea of what is possible, without going into too much detail.

[Case Study 1: Adding Vue.js into an already created site – client-side rendering](#contents.xhtml_sc3_8a)

The Scenario: There is a website that has already been built, but you've been tasked to add a new feature that Vue.js has been deemed perfect for.

Your Goal: Build out the expected feature using client-side rendered Vue.js.

The Implementation: To make this work, you will be pulling Vue.js directly into the web page and building your JavaScript as you normally would.

As a demonstration, a simple hello world example is as follows:

1.  <!DOCTYPE html>
2.  <html lang="en">
3.  <head>
4.  <title>My first Vue app</title>
5.  <script src=”https://unpkg.com/vue"></script>
6.  </head>
7.  <body>
8.  <div id="app">
9.  {{ message }}
10.  </div>

12.  <script>
13.  const app = new Vue({
14.  el: '#app',
15.  data: {
16.  message: "Hi there, you're using Vue!"
17.  }
18.  })
19.  </script>
20.  </body>
21.  </html> 

This code can be found in chapter-1/case-study-1-hello-world/index.html of the source files. The preceding code is the simplest of Hello world Vue.js applications. There are four major steps:

*   Line 5: Import the Vue framework into the page
*   Line 9: Use double mustache syntax to print out the required data
*   Line 13: Create a new Vue instance and attach it to the #app element in the page body
*   Line 16: Set the data in the message variable to “Hi there, you're using Vue!

What is happening here will be explained in depth in [Chapter 4](#ch04.xhtml), Understanding the Vue.js Instance.

So, the next question is, “How does that example help me integrate Vue.js in my page?”

Let's assume that you have a page as follows:

![](images/figure1.2.png)

Figure 1.2: Wireframe showing where Vue.js component is to be placed

In the marked section, you are looking to put in the following solution:

![](images/figure1.3.png)

Figure 1.3: Wireframe showing component to integrate

So, to start this, as in the previous example, we'll import the Vue.js library file in the head of the document:

1.  <head>
2.  …
3.  <script src="https://unpkg.com/vue"></script>
4.  …
5.  </head>

The preceding code shows how to import Vue.js into a page and can be found in the code repo at chapter-1/case-study-1-site-integration/01-index.html.

Then, add the mark-up that we need to place the Vue.js application in the page (chapter-1/case-study-1-site-integration/02-index.html):

1.  <div class="…">
2.  <div id="app"></div>
3.  </div>

Into this wrapper, we will add the required mark-up to provide the skeleton for our application:

1.  <body>
2.  <!-- The rest of the site -->

4.  <div class="w-1/4">
5.  <div id="app">
6.  <!-- Adding the application markup -->

8.  <img :src="imageUrl" class="..." />
9.  <div class="...">
10.  <div class="...">
11.  <div>
12.  <i class="fas fa-heart" />
13.  {{ likeNumber }}
14.  </div>
15.  <div>
16.  <i class="fas fa-minus-square" />
17.  {{ dislikeNumber }}
18.  </div>
19.  </div>
20.  <div>
21.  <a :href="shareUrl">SHARE</a>
22.  </div>
23.  </div>
24.  <div class="...">
25.  <label for="email" class="...">
26.  <input type="email" class="..." v-model ="email"         
27.  placeholder="..." />
28.  </label>
29.  <textarea type="email" class="…" v-model="comment" @blur="postComment"></textarea>
30.  </div>
31.  </div>
32.  </div>

34.  <!-- The rest of the site -->
35.  </body>

In the code for chapter-1/case-study-1-site-integration/03-index.html, we add in the required mark-up:

*   Line 8: Uses the v-bind directive to inject the imageUrl variable
*   Line 13: To print the likeNumber data point
*   Line 17: To printing the dislikeNumber data point
*   Line 21: Uses v-bind to inject the shareUrl
*   Line 26: Pulling the v-model for email
*   Line 28: The element has both a v-model comment to hold the textarea data and the blur event handler to handle posting the data

Simple, isn't it? It's just HTML; the only extra bit is the v-model attribute. This attribute is called a directive in Vue.js parlance; it starts with a v-; it's an instruction to the core framework to provide supplementary functionality against that marked DOM element. We'll cover directives in detail when we discuss binding data to the UI and handling events, etc.

With the HTML in place, we'll add our script tag that adds our JS functionality, and we'll set up the Vue.js instance and apply it to the #app hook that we have in the mark-up:

1.  <script>
2.  const app = new Vue({
3.  el: "#app",
4.  ...
5.  })
6.  </script>

In chapter-1/case-study-1-site-integration/04-index.html, see the code above, we create a new Vue.js instance (line 2) and then attach that instance to the HTML element #app on line 3.

With the instance skeleton in place, we can start building out the desired functionality:

1.  <script>
2.  const app = new Vue({
3.  el: "#app",
4.  data: {},
5.  methods: {}
6.  })
7.  </script>

In this code snippet, chapter-1/case-study-1-site-integration/05-index.html, we've introduced the Vue.js data attribute and the methods attribute on lines 4 and 5.

From the mark-up (chapter-1/case-study-1-site-integration/06-index.html), you can see that you need to have the following data points: imageUrl, likeNumber, dislikeNumber, shareUrl, email, and comment; so we'll add those into the data object:

1.  const app = new Vue({
2.  el: "#app",
3.  data: {
4.  imageUrl: "remote-image-url.png",
5.  likeNumber: 609,
6.  dislikeNumber: 120,
7.  shareUrl: "share-url.html",
8.  email: "",
9.  comment: ""
10.  },
11.  methods: {}
12.  })

If you look back at the HTML, you should also notice the v-on directive that is waiting for a blur event. This is how to mark that you're looking to handle an event. Events are handled in the methods section of your Vue.js instance:

1.  const app = new Vue({
2.  el: "#app",
3.  data: {...},
4.  methods: {
5.  postComment () {
6.  fetch("post-endpoint-url",
7.  {
8.  method: "POST", 
9.  mode: "same-origin",
10.  headers: [{"Content-Type": "application/json"}],
11.  body: JSON.stringify({
12.  email: this.email,
13.  comment: this.comment
14.  })
15.  }
16.  ).then(() => {
17.  // handle post response here
18.  })
19.  }
20.  }
21.  })

In the preceding code for chapter-1/case-study-1-site-integration/07-index.html, we're adding the code to build the event handler starting on line 5 with the postComment() event handler.

On line 6, we use the Fetch API to POST data to an API endpoint  and then  create a simple POST-able object with local data.

Adding in the postComment() function is the event handler that we added to the HTML v-on directive handler; we are using the Fetch API to send data to a make-believe endpoint as JSON. The important part here is the accessing of the object data using the this variable.

Results: As you can see, integrating Vue.js into an existing project is simple and non-intrusive. You can use as much or as little of the framework as you need to complete your solution.

[Case study 2: Building a Vue.js-based website](#contents.xhtml_sc3_9a)

The scenario: You are building a green-field site from the ground up.

Your goal: To have a web application built completely using Vue.js. The application is to have four main sections: a header; a side menu; a main content area and a footer.

The Implementation: As with all software projects, building a project of a significant size requires significant time and effort, so this is somewhat of a contrived example in order to fit. This will not be an explanation of the complete solution; the complete details will be presented later in the book.

Starting a new Vue.js application with the CLI gives you a basic idea to build your application against. When we use the CLI, the preferred way of constructing the application is to use single file components – a component that is built in a file with the extension of .vue that conforms to a set of simple-to-remember rules. [Chapter 5](#ch05.xhtml), Designing component-based UIs and Single Page Applications covers this.

With component-based builds, you can start with the smallest component and compose to build larger and larger components; start at the page level and break the build down into smaller components, or you can use a hybrid approach. The way to construct depends on the project, the situation you find yourself in, and on personal preference.

For this simple build, we've decided to split the page up in the main App.vue file instead of building out a layout. You might also notice that we're using TailwindCSS ([https://tailwindcss.com](https://tailwindcss.com)).

1.  <template>
2.  <div class="container mx-auto">
3.  <header class="w-full">
4.  <PageHeader />
5.  </header>
6.  <div class="flex space-x-4">
7.  <div class="w-1/6">
8.  <SideMenu />
9.  </div>
10.  <div class="w-5/6">
11.  <PageContent />
12.  </div>
13.  </div>
14.  <footer class="w-full">
15.  <PageFooter />
16.  </footer>
17.  </div>
18.  </template>

In this initial application from chapter-1/case-study-2-basic-build/basic-app/src/App.vue, we set up the template and place the PageHeader, SideMenu and PageContent and PageFooter components.

In order to get the components into the HTML, we need to import the .vue files and inject via the components attribute, as shown below:

1.  <script>
2.  import PageHeader from './components/PageHeader.vue'
3.  import PageFooter from './components/PageFooter.vue'
4.  import SideMenu from './components/SideMenu.vue'
5.  import PageContent from './components/PageContent.vue'

7.  export default {
8.  name: 'App',
9.  components: {
10.  PageHeader,
11.  PageFooter,
12.  SideMenu,
13.  PageContent
14.  }
15.  }
16.  </script>

In the previous code example, we have used the standard JS import syntax to import the required components.

From here, of the components that constitute the application, the simplest are the PageHeader and PageFooter, see below:

1.  <template>
2.  <div class="flex justify-between bg-purple-200 px-6 py-4">
3.  <div class="text-xl font-semibold">Sites'R'Us</div>
4.  <HorizontalMenu />
5.  </div>
6.  </template>

8.  <script>
9.  import HorizontalMenu from './HorizontalMenu.vue'

11.  export default {
12.  name: 'PageHeader',
13.  components: {
14.  HorizontalMenu
15.  }
16.  }
17.  </script>

The code listing (chapter-1/case-study-2-basic-build/basic-app/src/components/PageHeader.vue) imports the HorizontalMenu component. The HorizontalMenu component is re-used in the PageFooter as shown in chapter-1/case-study-2-basic-build/basic-app/src/components/PageFooter.vue. This code is shown below:

1.  <template>
2.  <div class="flex bg-gray-300 justify-center py-3">
3.  <HorizontalMenu />
4.  </div>
5.  </template>

7.  <script>
8.  import HorizontalMenu from './HorizontalMenu.vue'

10.  export default {
11.  name: 'PageFooter',
12.  components: {
13.  HorizontalMenu
14.  }
15.  }
16.  </script>

Simple, isn't it?

The HorizontalMenu  component just provides the content navigation:

1.  <template>
2.  <nav class="...">
3.  <li v-for="i in items" :key="i">{{ i }}</li>
4.  </nav>
5.  </template>

7.  <script>
8.  export default {
9.  name: 'HorizontalMenu',
10.  data () {
11.  return {
12.  items: [
13.  'Item 1',
14.  'Item 2',
15.  'Item 3',
16.  'Item 4'
17.  ]
18.  }
19.  }
20.  }
21.  </script>

The HorizontalMenu.vue in chapter-1/case-study-2-basic-build/basic-app/src/components/HorizontalMenu.vue: Here, in line 3, we're using the v-for directive to loop over the items array, using the key prop and printing out the data item. In line 12, and we add in the data definition section, and line 12 defines the items array data.

Next, we will take a quick look at SideMenu:

22.  <template>
23.  <div class="py-8 px-4 border-r border-gray-200">
24.  <nav class="...">
25.  <li v-for="i in items" :key="i">{{ i }}</li>
26.  </nav>
27.  </div>
28.  </template>

30.  <script>
31.  export default {
32.  name: "SideMenu",
33.  data () {
34.  return {
35.  items: [
36.  'Main 1',
37.  'Main 2',
38.  'Main 3',
39.  'Main 4'
40.  ]
41.  }
42.  }
43.  }
44.  </script>

The code here is similar to HorizontalMenu. A natural question is, ‘Can this be split further so that the navigation elements can be pulled in by the menu components?' Sure, but in this case, we're going simple and don't have an API yet.

If we look at the final App.vue included component, PageContent, we notice a couple of differences:

1.  <template>
2.  <div class="h-5/6 py-8 px-4">
3.  <ContentComponent>
4.  <div>Slot Content</div>
5.  </ContentComponent>
6.  <ContentComponent>
7.  <div>Slot Content</div>
8.  </ContentComponent>
9.  <FormComponent :name="formData.name" 
10.  :email="formData.email" />
11.  </div>
12.  </template>

14.  <script>
15.  import ContentComponent from './ContentComponent.vue'
16.  import FormComponent from './FormComponent.vue'

18.  export default {
19.  components: { 
20.  ContentComponent,
21.  FormComponent
22.  },
23.  name: 'PageContent',
24.  data () {
25.  return {
26.  formData: {
27.  name: 'name',
28.  email: 'name@email.test'
29.  }
30.  }
31.  }
32.  }
33.  </script>

The PageContent component shows how to inject content using the default slot on lines 4 and 7 and data being passed from the parent to the child component on line 9.

Here, the PageContent component is passing data forward into the child components in various ways: by slot and by prop. Props are discussed in [Chapter 5](#ch05.xhtml), Designing component-based UIs and Single Page Applications, and slots are discussed in detail in [Chapter 9](#ch09.xhtml), Building User Interface Components.

How does this data end up in the child component? For the ContentComponent (via a slot):

1.  <template>
2.  <div class="mb-8 py-8 border-b border-gray-200">
3.  <slot></slot>
4.  </div>
5.  </template>

7.  <script>
8.  export default {
9.  name: 'ContentComponent'
10.  }
11.  </script>

The ContentComponent.vue: line 3: The slot - HTML from the parent gets injected here.

FormComponent is the most complicated component in this example:

1.  <template>
2.  <div>
3.  <div class="mb-4">
4.  <p class="...">Data Collection Form</p>
5.  <label>
6.  <span class="font-semibold mr-2">Name</span>
7.  <input :value="name" name="name" class="..."  />
8.  </label>
9.  </div>
10.  <div>
11.  <label>
12.  <span class="font-semibold mr-2">Email</span>
13.  <input type="email" :value="email" name="email"
14.  </label>
15.  </div>
16.  <div class="flex pl-24">
17.  <button class="..." @click.prevent="submitChange">Update</button>
18.  </div>
19.  </div>
20.  </template>

22.  <script>
23.  export default {
24.  name: 'FormComponent',
25.  props: {
26.  name: {
27.  type: String,
28.  required: true
29.  },
30.  email: {
31.  type: String,
32.  required: true
33.  }
34.  },
35.  methods: {
36.  submitChange () {
37.  alert(`You're updating ${this.name} and ${this.email}`)
38.  }
39.  }
40.  }
41.  </script>

FormComponent.vue: Line 7 use the shortcut syntax : to bind the variables; it's just so much easier to type. Line 17 injects an event handler with the @ shortcut and uses the .prevent event modifier to ensure that the event doesn't bubble.

Line 25 defines the props data for the injected data.

There's a lot more going on here with props data being injected into FormComponent and some simple event handling.

Results: This is a contrived, simple and really basic design. It was built from the outside in, from the large components to the smaller ones with a limited specification. What it shows, though, is the way the UI is composed of smaller components assembled to make a whole.

[Conclusion](#contents.xhtml_sc2_10a)

This chapter is a whistle stop tour of front-end development using Vue.js. We explored some of the history of the languages of the web, where Vue.js came from and which companies are using it. Then we took a quick look at how to integrate Vue.js into a web page and how to use single file components to build a UI.

In the next chapter, we will discuss the kinds of roles and the type of work you can expect to be doing as a developer who specializes in web development.

[Points to remember](#contents.xhtml_sc2_11a)

*   Vue.js is a versatile front-end web development framework that can be used in any number of scenarios
*   The framework uses standard HTML, CSS, and JS

[Multiple choice questions](#contents.xhtml_sc2_12a)

1.  What is Vue.js?

    1.  A versatile front-end web framework
    2.  A cinema chain
    3.  A design pattern component
    4.  A jQuery plugin
2.  How can Vue.js be used to build your UI?

    1.  Embedded alongside the rest of the UI code
    2.  As a full single page application using single file components
    3.  Both of the above
3.  Name some of the current frameworks in the UI space.

    1.  React
    2.  Angular
    3.  Svelte
    4.  Knockout.js
    5.  jQuery
    6.  Elm

[Answers](#contents.xhtml_sc2_13a)

1.  A

2.  A and B, or just C

3.  A, B, C, F

[Questions](#contents.xhtml_sc2_14a)

1.  Which contemporary frameworks are competitors to Vue.js?

2.  What are the different sections of a Vue.js component?

3.  Name some of the companies that use Vue.js in production.

[Key terms](#contents.xhtml_sc2_15a)

*   HTML
*   CSS
*   JS
*   DOM
*   MVC
*   Web development
*   UI
*   Template
*   Component
*   Angular
*   React
*   MongoDB
*   Express
*   Node.js
*   jQuery

Join our book’s Discord space

Join the book's Discord Workspace for Latest updates, Offers, Tech happenings around the world, New Release and Sessions with the Authors:

**[https://discord.bpbonline.com](https://discord.bpbonline.com)**

![](images/fm1.png)

# [CHAPTER 2Working in Vue.js Roles](#contents.xhtml_ch02a)

[Introduction](#contents.xhtml_sc2_16a)

In the previous chapter, we discussed some of where Vue.js comes from and how it can be used. In this chapter, we'll talk about using Vue.js in a day-to-day setting.

We'll start by looking at the framework in the context of where it fits in the workplace and what you as a user of this framework can expect to be doing. We'll then move on to typical roles and explore what sort of career path might be out there.

As we're looking at the types of roles you can expect to find as a web developer specializing in when it comes to Vue.js, this chapter will not be presenting any detail on the framework itself; rather, we'll be getting a taste of what the workplace is like.

We'll cover a number of working practices and organizational structures, and while we cannot hope to cover every single variation, we can generalize to cover most bases.

[Structure](#contents.xhtml_sc2_17a)

We will be discussing the following topics in this chapter:

*   Working with Vue.js
*   Jobs/Roles that use Vue.js
*   Expected future demand

[Objectives](#contents.xhtml_sc2_18a)

After going through this chapter, you will learn how the framework fits into various types of company and your career path. This chapter will also help you explore various opportunities that are open for Vue.js developers.

[Working with Vue.js](#contents.xhtml_sc2_19a)

There are a myriad of ways in which the framework can be used or integrated into a company's product architecture and even between front-end and full-stack roles, between teams and across departments. To cover them all is a tall order. We'll look at the most likely cases.

[Freelancer/Consultant](#contents.xhtml_sc3_20a)

As a consultant, freelancer, or freelancing company of only 1 or 2 people, you might have the luxury to dictate to your client which framework you will use to complete their project, or maybe the client came to you because of your expertise in a particular technology. Whichever category or service provision type you fall into, as a freelancer, you will most likely have a freer hand in the choice of technology that you can use, which you would not have in other business types.

In this part of the software industry, you will most likely also have to consult, design and/or hand over a completed product, interface with a client's in-house team, if they have one, and provide documentation and training. This means you need to be comfortable with the technology that you're proposing/using, comfortable enough to defend your choice and provide relevant and comprehensive documentation and training.

Starting with this section, we'll use the following depiction to give you an idea of who pays and covers training time for each sector. They are generalizations. [Figure 2.1](#ch02.xhtml_fig2-1) shows this for freelancers and consultants:

![](images/figure_2.1.png)

Figure 2.1: Freelancer training funding and time

As a freelancer, you are most likely to be funding your own training and will be completing this in your own time, so you will be looking for technologies that are easy and quick to learn and simple to put into practice.

[Design Studio](#contents.xhtml_sc3_21a)

In a design studio, you will probably have to contend with a company favorite framework. This framework might be Vue.js but might also be React or Angular, should the company be modern and progressive. If you're really (un)lucky, the company favorite could be something from the dim and distant past, like jQuery or Dojo. Alternatively, you might be working on a home-grown framework, or something dictated by the client, or have to move between different frameworks, depending on client project rotation. The point is that design studio work can be varied but not necessarily up to date.

Design studios tend to work by building lots of things (usually brochureware) quickly; the higher the turnover of projects, the more profitable they seem to be. This puts a great amount of pressure on the development team to produce work rapidly and then move on, but the teams do not necessarily put in a great deal of thought, accuracy or code cleanliness, especially if the projects have moving targets/requirements or are running close to the end of, or are even over-budget.

[Figure 2.2](#ch02.xhtml_fig2-2) shows where funding and time to learn might come from:

![A picture containing chart Description automatically generated](images/figure_2.2.png)

Figure 2.2: Design Studio training funding and time

In this type of setting, you might get a small training budget and limited time to learn, but most likely you'll need to fund your training yourself and complete the training in your own time.

[Small business](#contents.xhtml_sc3_22a)

Small businesses generally have between 3 and 50 people. Design studios might also fall into the small business category. The main difference between design studios and other types of small business are that design studios target clients wanting to work in the digital space and provide products and services that help their clients navigate that space; small businesses target different sectors – retail, supply chain, services, finance, the list goes on.

Small businesses tend to go with what they know, and unless the main aim of the business is to create/service software, your role will be one supporting the main product and therefore, secondary to the main business concern; this might entail supporting third-party software and various integrations. Sometimes you might be lucky and the business owner will take advice or alternate practices onboard, but some (most probably most) will not.

If the business doesn't already use Vue.js in its software stack, bringing a new technology like Vue.js into the small business environment can be a shock, can create a large amount of mess, or can bring massive reward, but this is the case for bringing any new tech into a small environment.

[Figure 2.3](#ch02.xhtml_fig2-3) shows how employees working in small businesses fund and find time for training:

![A picture containing logo Description automatically generated](images/figure_2.3.png)

Figure 2.3: Small business training funding and time

Any training costs will usually be funded by you, and the training completed in your own time. Small businesses tend to put all their money into other things, and training is not usually a priority unless it's directly related to the aims of the business.

[Small/Medium Enterprises](#contents.xhtml_sc3_23a)

Small and medium enterprises (SME's), usually sized between 50 and 500 people, tend to have a small number of dedicated, targeted products, which are not software related. The job of any inhouse software team in this type of environment is to support the sales, marketing and maintenance of the core product range.

While it might be a step up from small family run businesses, getting the relevant decision maker(s) to bring in a new technology can prove to be an uphill struggle, especially if the management team doesn't understand how to build or manage software or development teams.

[Figure 2.4](#ch02.xhtml_fig2-4) depicts the funding of training opportunities for SMEs:

![A picture containing chart Description automatically generated](images/figure_2.4.png)

Figure 2.4: SMEs' training funding and time

SMEs might have a small training budget; obviously, the larger the company, the more likely they can have a budget. In general though, training will be completed in your own time, outside of work hours.

[Large business/Enterprise](#contents.xhtml_sc3_24a)

In a large or enterprise business, you could be talking about a large and varied software ecosystem with multiple products serviced by multiple teams. The teams might (or might not) be specialized as purely front and back end or a mixture of specialty.

These teams may have autonomy over the development platforms they can use (microservice type architectures), or they might have a limited ecosystem and directed, allowable software list (usually monolithic applications); as with everything, each company's philosophy, ethos and development layout are different.

In an organization like this, you will most likely be a team member completing work as directed in a formalized software development cycle. Unless you're an architect, lead developer or employed in some other decision-making capacity, your ability to influence the usage of different frameworks, if not already established, will be limited. However, it's not unheard of for prototypes to be generated and presented to decision-makers who fire the corporate imagination. Sometimes it pays off, sometimes it doesn't. Usually, companies that reserve some working time for personal study and projects are more receptive to this type of thing.

[Figure 2.5](#ch02.xhtml_fig2-5) gives an idea of how larger organizations cater for employee training needs:

![A picture containing chart Description automatically generated](images/figure_2.5.png)

Figure 2.5: Large business training funding and time

Large companies usually have a training budget for employees, and provided you can argue that training is relevant, you could get your employer to pay for it. There's usually a policy that covers what will and won't be paid for and some expectations placed on you by the company. Oftentimes, it's at your line manager's discretion. There might also be company-wide subscriptions for online training services that you can tap into.

[Job/Roles that use Vue.js](#contents.xhtml_sc2_25a)

As you look for roles that use the skills covered in the rest of this book, you will come across the following broad categories of role types. Each subsection covers what you should typically expect to be looking for/doing.

[Front-end/Web Developer](#contents.xhtml_sc3_26a)

It will be your job, as a front-end developer, to create and maintain the application front-end code. This means building out the HTML, CSS, and JS for the codebase that you're responsible for. There might also be a design component and a UX component. So along with code, there could also be an understanding of tools like Photoshop, Sketch, XD, and Illustrator; this list is not exhaustive.

In larger organizations, while not maybe directly contributing to the design or UX elements, you will be responsible for working within the companies formalized development structure and policies. This includes submitting code to software repositories, checking, and reviewing other team members' code to ensure that relevant style guides and coding standards are adhered to, bug fixing, writing UI tests to check that user interactions receive the expected responses, etc.; the list goes on. As you gain more experience, you can probably add systems design, mentoring and team leadership to this list.

That said, your main focus will be using the web developers standard tool kit (HTML, CSS and JS) to complete these tasks.

[Full-stack developer](#contents.xhtml_sc3_27a)

As a full-stack developer, on top of everything discussed in the previous section, you could be building databases and creating interactions with data, building server-based software including APIs, plus creating, and maintaining the server infrastructure, at least in smaller organizations.

Larger organizations might have DBAs, server administrators, DevOps, and other teams to support you, but part of your job will be to help feed into those teams with your knowledge and experience to provide application support and suitable deployment environments.

A full-stack developer is a jack of most trades and a master of some.

[JAMStack Developer](#contents.xhtml_sc3_28a)

The JAMStack is a relatively new phenomenon, at least in the current incarnations and hype centered on frameworks like NuxtJS, GatsbyJS, and Hugo, among others. JAM stands for JavaScript, API, and Markup, and it covers technology that is used to create a website offline using a transpiler and have it generated based on various data sources like markdown content files, public APIs, blog and CRM-based data endpoints, sharepoint, etc.; the list goes on. The point of these technologies is that there are no moving parts for malicious users to exploit, but more importantly, the end user gets a better and faster experience using a JAMStack product than other DB-driven services, as the heavy lifting (that is data consumption and UI generation) has already happened and the user is just getting optimized HTML, CSS, and JS to render.

What this means is that a JAMStack developer is not very different from a front-end developer the only addition is that of building out the data interface to assemble the pages dynamically using technologies like GraphQL or the fetch API.

Using NuxtJS will be the focus of [Chapter 15](#ch15.xhtml), Server-Side Rendering With Nuxt.js.

[Mobile developer](#contents.xhtml_sc3_29a)

Building mobile applications using Vue.js is a very niche discipline. There are very few frameworks that support a variation of Vue.js to build out mobile: NativeScript and Quasar.

NativeScript is a framework that uses JS and markup to target both Android and iOS platforms. It has various flavors: JS/XML, Angular, Vue.js and Svelte. React has React Native. Quasar only uses Vue.js as its view layer, but has different build engines that allow it to target a number of different output platforms.

Building mobile applications with Quasar is the focus of [Chapter 16](#ch16.xhtml), Building Mulit-tenanted Apps with Quasar.

[Expected future demand](#contents.xhtml_sc2_30a)

There is not going to be a decrease in the demand for people who can use HTML, CSS, or JavaScript effectively. Building web applications based on components is also here to stay. Framework take up and usage, however, does change. Right now, it's React, Angular and Vue.

Better, and more usable and capable frameworks will come about over time, and these three will be consigned to the annuls of history. Realistically, it can be expected that Vue.js (and React/Angular) will be a framework of choice for web development for between 5 and 10 years. The skills that you learn with these frameworks, however, are transferable.

What this means is that projects requiring some sort of web interface will most probably require the skills that you learn when you use this framework and can help you plan and implement whatever comes next for the industry.

Career progression in Vue.js is the same as in any other branch of web/software development, as you're just a developer using a framework to complete the tasks set. This is not unusual. You might be having to work across multiple projects using multiple frameworks, all in the same organization or across multiple client code bases. This is also not unusual.

As is standard, you can expect all the grades of development to be available to you, from junior developer and developer to senior developer, lead developer, and sometimes architect and sometimes management. Architects from purely front-end developers are rare, but if you're a full-stack developer, then being an architect is a realistic proposition. If at some point you get bored of being at the code-face, then management might be an option for you.

The following image maps out a typical career path for a web developer. It's fairly linear to start off with, but once you reach a certain point in your path, it can diverge depending on your interest or ambition.

![](images/figure_2.6.png)

Figure 2.6: Career roadmap

[Junior Web Developer](#contents.xhtml_sc3_31a)

A junior web developer is usually the entry position. You can expect to be a junior for a couple of years. You'll be fixing long standing bugs, creating small amounts of functionality, and generally learning the craft under the mentorship of more experienced team members.

[Web Developer](#contents.xhtml_sc3_32a)

As a mid-level developer, you'll be building on the experience you gained as a junior. Your daily tasks will be building out the main site functionality as parceled out by the application designers/architects, so you will be left, mostly, to your own devices to design and build out that functionality, but you can expect to be bought into smaller application design decisions as well.

By this time, you should have a good understanding of the parts of the application for which your team is responsible. You might also have a passable or good understanding of other parts of the application as you might have shifted teams in your tenure.

Depending on your ability, environment, and ambition, you could expect to be a mid-tier developer for between 5 and 10 years.

[Senior Web Developer](#contents.xhtml_sc3_33a)

As a senior developer, your typical day will probably look not that different from that of a mid-tier, with added responsibilities around training junior staff and guiding application development. You'll be spending roughly 90% of your time coding. You will be working more closely with the application designers, tech leads and architects, helping make application design-level decisions. In this position, you're likely to be the “go-to person” for the team.

At a senior level, you will have an overall understanding of your application area, plus many others. As you'll be working with the application architecture team, you'll have a good overview of the entire application and deployment environment.

If you don't want to progress any further, you can just leave it here; otherwise, you can progress into team leadership, architecture and management roles.

[Tech Lead/Lead Developer](#contents.xhtml_sc3_34a)

As a Tech Lead, you probably still be spending around 50%–60% of your time coding, the balance centering around team management and meetings, where the focus will be on leading the team, making resource decisions, and generally shielding the team from other parts of the decision-making apparatus in the business.

Tech Leads tend to move into management positions, if you're any good and want to progress in that direction, it'll happen after a year or two.

[Architect](#contents.xhtml_sc3_35a)

As an architect or a member of the architecture team, you'll be responsible for creating or amending application design and guiding the application build against business requirements. As part of this team, you'll be interfacing with other parts of the business, most likely through business analysts and project managers, and you'll be working alongside the development teams, guiding them through the design decisions. As a team, you will have total overview of the system.

It will be your job to introduce new technologies, tools and development paradigms to the business and verify that they suit the needs of the business. You will do this by building prototypes to flesh out ideas and writing documentation describing how and when to use the new technology, why it is being considered and introduced, and what to use the new technology for. This means you'll be looking at around roughly 25%–50% coding time.

It will be up to the architecture team to mitigate the effect of introducing new technologies, ensuring that ramp up time is minimized and code quality is maintained.

[Management](#contents.xhtml_sc3_36a)

Managers are supposed to, well, manage. They oversee people, resources, time, and business requirements.

On a daily basis, you will probably spend most time in meetings as manager. This is not an activity that some enjoy. The amount of coding that you can expect to be doing will approach zero when at this position.

[Conclusion](#contents.xhtml_sc2_37a)

There are several types of companies where Vue.js skills, and web development skills in general, can be utilized. In this chapter, we covered the various types of companies that might employ you and the titles that you can look for in your job search.

This chapter covered only the tip of the iceberg on companies, and the same goes for the various roles that you might be doing or are available to you as a web developer.

In the next chapter, we will cover some of the more advanced concepts that you might need when working with Vue.js.

[Points to remember](#contents.xhtml_sc2_38a)

*   Generally, career progression is from Junior Web Developer to Web Developer, then Senior Web Developer, Tech Lead and then Architect and/or Management.
*   Most jobs sit with large businesses and corporations, but there's plenty of opportunity with companies of all sizes.

[Multiple choice questions](#contents.xhtml_sc2_39a)

1.  As a Tech Lead, what is the next career step?

    1.  Architect
    2.  Senior Developer
    3.  Manager
    4.  Junior
2.  As an Architect, how much time can you expect to use coding?

    1.  10%
    2.  25%
    3.  75%
    4.  100%

[Answers](#contents.xhtml_sc2_40a)

1.  A and C

2.  B

[Questions](#contents.xhtml_sc2_41a)

1.  What is the JAMStack?

2.  What is the expected career progression for a web developer?

3.  If not already, do you expect to progress into Architecture or Management?

[Key terms](#contents.xhtml_sc2_42a)

*   Junior
*   Mid-tier
*   Senior
*   Architect
*   Management
*   Enterprise
*   SMEs
*   Small Business

Join our book’s Discord space

Join the book's Discord Workspace for Latest updates, Offers, Tech happenings around the world, New Release and Sessions with the Authors:

**[https://discord.bpbonline.com](https://discord.bpbonline.com)**

![](images/fm1.png)

# [CHAPTER 3HTML, CSS, and JS/TS for Extra Credit](#contents.xhtml_ch03a)

[Introduction](#contents.xhtml_sc2_43a)

This chapter covers some of the more advanced elements of these tools of the trade. This will not a be tutorial on the basics; you're expected to already understand those; if you don't, then there are some excellent tutorials online – we'll wait. This chapter might stretch you a little.

We'll start off by discussing the more modern alternatives to traditional DOM rendering – virtual DOM, before briefly covering some CSS and looking at some advanced uses of JavaScript. We'll finish off with a primer on TypeScript.

With this extra knowledge under our collective belts, we'll be well placed to start designing and building applications with Vue.js.

[Structure](#contents.xhtml_sc2_44a)

In this chapter, we will go over the following parts of the craft:

*   Working with a Virtual DOM
*   CSS rule application and CSS frameworks
*   Modern JavaScript (JS) practices
*   Using TypeScript (TS)

[Objectives](#contents.xhtml_sc2_45a)

As a reader of this book, you are expected to already know HTML basics, i.e., what tags are, what the different parts of a web page are, and building pages using semantic markup. You're also expected to know how and where to apply CSS, what the selectors are, and the basics of constructing style rules. As far as JS goes, you should already know the basics, i.e., variables, flow of logic, basic operators, and some basic types and structures. We'll cover some of the more advanced elements in this chapter.

[Working with a Virtual DOM](#contents.xhtml_sc2_46a)

Before we cover what a Virtual DOM is and what problem it solves for us, we'll quickly remind ourselves of how a HTML DOM, i.e., the pages HTML node tree, is rendered by a web browser.

You might recall that HTML is a tree when seen at a browser level, with the HTML tag as its root, followed by HEAD and BODY branches, and so on.

Because of this tree-like structure, to make changes, i.e., manipulate the DOM, you need to walk it. Walking the DOM can be inefficient, depending on where you join the tree, how deep traverse it and how much it gets manipulated. Joining the DOM can be done by targeting an element, or via a class or id attribute. The DOM can then be manipulated through JS. Large or frequent changes can cause multiple reflows or repaints.

To understand why this might be the case, you need to understand the following process that a browser uses to render a page:

![Shape Description automatically generated](images/Figure_3.1.png)

Figure 3.1: Browser rendering flow

Depending on what and how much you are doing, the re-rendering or repainting of the page can take a significant amount of time. This is what you need to avoid for creating a good user experience, as users expect a fluid, snappy response to their interactions with your page.

To circumvent this issue, some front-end frameworks, including Vue.js, use the concept of a virtual DOM, a separate, lightweight, in-memory JS representation of the DOM that the framework can use to baseline changes against.

The virtual DOM, a concept popularized by React, is used in declarative frameworks (where you declare what you want to happen, rather than program everything explicitly) like Vue.js and Elm to improve the rendering speed of changes made to the DOM.

As stated earlier, a virtual DOM is a lightweight in-memory JS representation of the current DOM. But what you might be asking yourself is, ‘How does having two versions of the DOM increase the responsivity of DOM during re-renders and repaints'?

If changes are made, then the whole DOM might be repainted across every frame, which is not a workable solution for building a responsive UI.

![A picture containing antenna Description automatically generated](images/Figure_3.2.png)

Figure 3.2: Repainting of example DOM

The answer lies in diffing.

The framework makes changes to the virtual DOM, and when complete, the framework creates a diff between the virtual DOM and the current DOM, as shown in the following figure:

![Diagram Description automatically generated](images/Figure_3.3.png)

Figure 3.3: Applying a diff to the DOM

The diff is a list of changes that is a determination of how to minimize the number of touches to the DOM. The framework then schedules and applies only those changes to the actual DOM, causing as little disruption as possible, minimizing re-renders and repaints.

If the difference between the rendered DOM and the virtual DOM results in no differences, then no work is done.

The scheduling algorithm of the difference varies between frameworks, but ultimately, the algorithm is optimized for efficiency of both renders and reflows.

With this understanding of the basis of the Vue.js renderer, we'll segue into some CSS.

[CSS rule application and CSS frameworks](#contents.xhtml_sc2_47a)

CSS has a specific set of rules to determine which rule is applied to an element, and whether multiple rules need to be applied to an element. This is called specificity.

Specificity in CSS can be put simply as the most specific style rule wins. Sometimes, however, it can be difficult to determine which style rule that is.

To this end, there is a standard set of rules followed to determine the specificity of a style rule, and it's calculated as follows:

For each rule, start at 0, then sum as follows:

 Style attribute = 1000

 Id (#) = 100

 Each attribute, class, or pseudo-class = 10

 Each element name or pseudo-element = 1

Tip: The highest value wins.

We'll use the following examples to see how this is applied:

1.  <section class="classSelector">
2.  <header id="idSelector">
3.  <h1>This is an example title</h1>
4.  <h4 style="font-weight: bold">Title tag line</h4>
5.  </header>
6.  </section>

In this example, suppose we were targeting the h4 element with the following rules:

1.  Style attribute       # specificity = 1000
2.  .classSelector h4     # specificity = 11
3.  #idSelector h4        # specificity = 101
4.  header h4             # specificity = 2
5.  h4                    # specificity = 1 

As you can see, the style attribute has the highest value and is applied. After we've determined the specificity, we apply the following rules in order:

If specificity of two rules is equal, the last defined rule is applied.

Your style sheet has the following rules defined:

1.  .classSelector h1 {
2.  color: purple;
3.  }

5.  .classSelector h1 {
6.  color: red;
7.  }

Even though the rules have the same specificity (11), the last rule is deemed closer to the selected element as it's defined last and therefore, the h1 element in the code example will be red.

ID selectors are more specific than attribute selectors, as follows:

1.  section#idSelector { border: gray; }        # => 101
2.  #idSelector { border: green; }     # => 10
3.  section[id=idSelector] { border: blue; }    # => 11

Here, the rules all target the same element, but rule 1 wins with higher specificity.

Contextual selectors are more specific than single element selectors.

This refers to the style rule location discussed earlier:

Style attribute > internal style sheet > external style sheet

Class selectors are more specific than element selectors.

This is where .class > element, as discussed earlier.

Inherited values have specificity = 0

Properties that are inherited have a specificity of 0.

* selector has specificity = 0

The universal (*) selector has a specificity of 0.

!important

Rules marked with !important override any previously specified rules, regardless of specificity. If you find that you're using this a lot, then it might be that your CSS rules need to be rearranged to a better order.

[CSS Frameworks](#contents.xhtml_sc3_48a)

It is becoming increasingly unusual to build a project's CSS from scratch. In the main, a CSS framework is selected to provide a baseline from which to work. The reasons for this vary, but in the main, CSS frameworks have done a lot of the hard work in handling various compatibility issues between browsers and browser versions; they provide a set of standard classes that behave in a predictable manner, and they reduce the amount of time required to build the visual elements of your project. In short, they save you a great deal of time.

There are many different types of CSS framework. Some just provide a simple grid, some are designed for responsive design, some just provide styling for components, and some do everything.

Currently used popular frameworks include Bootstrap, Foundation, Bulma, Milligram, Material Design, and TailwindCSS.

This book will concentrate on using TailwindCSS as this CSS framework is becoming increasingly popular, and it doesn't require us to build our templates in a certain way. We'll cover the integration and usage of TailwindCSS in [Chapter 8](#ch08.xhtml), Adding a CSS Framework to the Mix.

We will also briefly cover Twitter Bootstrap integration as this seems to be the framework with the greatest penetration, but as Twitter requires you to build your visuals a certain way, as presented in the documentation, you end up building more HTML in the templates, or worse, having to split the required HTML across several components that cause maintenance headaches.

Other frameworks can be integrated the same way as these, so there's nothing more to gain by covering more than these two.

[Modern JavaScript practices](#contents.xhtml_sc2_49a)

To build anything with Vue.js, you need to know how to use JavaScript (JS); as already stated, you should at least know the basics. Most software developers will have come across JS in one form or another, and it is the most pervasive software development platform in the world; everyone who has access to a computer with a web browser has access to JS.

Note: ES2015 or ES6?

Officially, all versions of JS since the updated release in 2015 are given a year name. Before that, they were given a version number, i.e., ES5\. Because it took a while for the language working group to make naming official, many branded ES2015 as ES6, ES2016 as ES7, and so on. However, we feel about it, the name ES6 is here to stay, and many companies and recruiters refer to ES6 incorrectly when they mean ES2015.

However, there are several tools that are seen as industry standard. The most widely used is Microsoft Visual Studio Code (VS Code), a free, simple-to-use text editor with an extensible plugin system that allows you to tailor it to any number of programming languages and styles. Other tools include but are not limited to JetBrains IntelliJ, Sublime Text, Notepad++, BBEdit, WebStorm, Visual Studio, Eclipse, NetBeans, Vim, and Emacs. The point is that you need to find an editor or integrated development environment (IDE) that you are comfortable with because as a developer, you will be spending a lot of time using it.

If you don't already know some JavaScript basics, this chapter might be a stretch as we're going to cover some edges and dark corners.

[Objects and Prototypes](#contents.xhtml_sc3_50a)

Objects are used to create collections of key-value pairs and more complex entities. The Object type is also the base type (prototype) of a majority of the objects provided by JavaScript. Typically, an Object inherits the properties and methods provided by Object.prototype.

Objects are constructed using either the Object() constructor function or the Object literal ({}), as follows:

1.  const obj1 = Object()           // {}
2.  const obj2 = Object(null)       // {}
3.  const obj3 = {}                 // {}
4.  const obj4 = { answer: 42 }     // {answer: 42}
5.  const obj5 = Object(42)         // [Number: 42]
6.  const obj6 = Object("Twelve")   // [String: 'Twelve']

This is all well and good, but where do prototypes come in, and what are prototypes anyway?

Prototypal inheritance is the inheritance mechanism employed by JavaScript in lieu of a proper subclassing mechanism.

Class-based OOP languages like Java use a blueprint, called a class, which defines what a class looks like, how it should behave, and how it should be communicated with its API and encapsulated data. To use a class, you create an instance that is an instantiation of that class and has the exact same data and API as the parent. Think cookie cutters.

In JavaScript, there is no distinction; it just has objects. A prototype is a template that provides the initial properties, after which an object can specify its own property set. An object (object1) can even set its own prototype to the prototype of a different object (object2). This allows object1 to share, or inherit, the properties of object2.

Every JavaScript object has a prototype. It is accessible using the prototype property, which points to a property in the object called __proto__. Although both properties are visible, use the prototype property to manipulate an object's prototype as it's more explicit.

To create classes in ES2015+, it is advisable to use the class declaration syntax explained later in this chapter, but the following example is still valid and hopefully explains the concept:

1.  function Vehicle (wheels = 0, totalPassengers = 0) {
2.  this.wheels = wheels
3.  this.totalPassengers = totalPassengers
4.  this.currentPassengers = 0
5.  }
6.  Vehicle.prototype.getMaxOccupancy = function () {
7.  return this.totalPassengers
8.  }
9.  Vehicle.prototype.setPassengers = function (numberOfPassengers) {
10.  this.currentPassengers = numberOfPassengers
11.  return this
12.  }
13.  Vehicle.prototype.getPassengers = function () {
14.  return this.currentPassengers
15.  }

17.  function Car (totalPassengers) {
18.  Vehicle.call(this, 4, totalPassengers)
19.  }
20.  Car.prototype = Object.create(Vehicle.prototype)

22.  const car = new Car(4)
23.  const peopleCarrier = new Car(7)
24.  peopleCarrier.setPassengers(5)

26.  console.log(car.getMaxOccupancy()) // 4
27.  console.log(peopleCarrier.getMaxOccupancy()) // 7
28.  console.log(`People Carrier currently has ${peopleCarrier.getPassengers()} passengers`)

30.  console.log(car)
31.  // Vehicle { wheels: 4, totalPassengers: 4, 
32.  currentPassengers: 0 

34.  console.log(car.__proto__)
35.  // Vehicle {}

37.  console.log(car.__proto__.__proto__)
38.  // {
39.  // getMaxOccupancy: [Function (anonymous)],
40.  // setPassengers: [Function (anonymous)],
41.  // getPassengers: [Function (anonymous)]
42.  //

We'll revisit this example with class declaration syntax to demonstrate how much clearer the code will be if you use it. This example demonstrates the way that the prototype chain is queried to obtain access to the provided functions.

[Functions](#contents.xhtml_sc3_51a)

Functions are a separate type, and in line with that, functions can be assigned to and passed around in the same way as variables.

In JavaScript, functions come in three flavors: named, anonymous and arrow.

You should already be familiar with how to create and use named functions. What you might not be aware of is that named functions have two special values: this and arguments.

The arguments value is an object of the data or arguments that have been passed to the function, and the keys are the values position in the provided arguments and values are the provided data points.

The this value behaves slightly differently from other OOP languages and can become a source of confusion. this provides the current execution context rather than the written function context. There is a subtle distinction; the former is dictated by the context (the conditions) provided by the execution rather than the context of the flow of logic. This means that the this value of a function might change depending on the context in which it is executed. It is also changeable through either the call(), bind(), or apply() functions. The this value is more useful when used in the context of a class or class-like structure (such as an IIFE – Immediately Invoked Function Expression), but these are just different facets of the function type. We'll cover classes and IIFEs further on in this chapter.

Named functions are scoped to the nearest context, which is either the global context or a module/namespace context.

Anonymous functions are functions without a name. They are primarily used in places where small functions of limited execution are needed.

An anonymous function needs to be either used directly (say in a callback; callbacks are discussed later in this chapter) or assigned to a variable before it can be used, as follows:

1.  const func = function (args) {
2.  // function body
3.  }

5.  // called by
6.  func(1)

8.  // or as a callback
9.  setTimeout(function (i) {
10.  // callback body
11.  }, 100)

Anonymous functions defined like this have access to the previously mentioned arguments and this special variables too.

Lastly, arrow functions are a specialized form of anonymous functions. They are defined slightly differently than the other functions, and they don't have access to arguments or this in the same way. In an arrow function, the value of this is derived from the surrounding context, and it forms a closure around the data that it receives from that context. In some circumstances, having the this context leak through is useful, but usage of this within an arrow function is discouraged, especially in Vue.js single file components.

Tip: Closure

A closure is the combination of a function and the lexical environment, or context, within which that function was declared (as given on MDN). This means that a function has access to any local variables that were in scope when the function was created and carries that information with it so that it can be used when the function is executed. Understanding context in JavaScript is important; creation context and execution context are different. Closures ensure that data available to the function in creation context is available in execution context.

The following set of examples show how the arrow function can be used:

1.  // full arrow function, uses explicit return
2.  const arrow = (arg1, arg2) => {
3.  // function body
4.  return value
5.  }

7.  // single line arrow, implicit return
8.  const arrow2 = (arg1, arg2) => arg1 + arg2

10.  // single argument arrow function,
11.  // parens can be dropped
12.  const arrow3 = arg1 => arg1

14.  // arrow function without arguments requires
15.  // parens to denote function
16.  const arrow4 = () => doSomethingHere()

As you can see, arrow function definitions can be very versatile; the form used should make the code easier to read.

We'll cover these things in much more detail when we start using them to build out components.

[JSON](#contents.xhtml_sc3_52a)

JSON, or JavaScript Object Notation, is a way for representing serialized JavaScript objects containing key-value pairs of primitive data, objects, and arrays. It is a data representation; not all JavaScript can be defined in terms of JSON.

JSON uses a specialized syntax; it is based on JavaScript but is distinct and has the following requirements:

*   Objects and Arrays: Keys are double-quoted strings and trailing commas are not allowed.
*   Numbers with leading zeros are not to be used.
*   Floating point representations must have at least one digit following the decimal point.
*   Undefined, NaN and Infinity are not supported.
*   Strings should only be doubled-quoted.
*   There are no comments.

This means that a JavaScript object literal can represent any kind of JavaScript data, as follows:

1.  const objectLiteral = {
2.  name: 'Clive',
3.  languages: [],
4.  age: 43,
5.  married: true,
6.  "has-beard": null,
7.  addLanguage: function (language) {
8.  this.languages.push(language)
9.  },
10.  languagesKnown: () => this.languages.join(', '),
11.  otherInfo: {
12.  otherBooks: [],
13.  papers: undefined,
14.  qualifications: {}
15.  }
16.  }

As you can see, this is a mix of value types, including functions, other objects, and arrays. This is perfectly acceptable for an object literal.

Suppose you take this literal and convert it into JSON, as follows:

1.  JSON.stringify(objectLiteral)

3.  '{"name":"Clive","languages":[],"age":43,"married"true,"has-beard":null,"otherInfo":{"otherBooks":[],
    "qualifications":{}}}'

If you look closely, all the keys are converted to double-quoted strings, and the functions have been removed from the data and any properties with undefined values have been dropped.

As JSON and JavaScript are so interrelated, JSON makes an ideal data packaging mechanism; if you're using Vue.js with a Node.js back end and MongoDB datastore, the JSON essentially becomes transparent across the various layers.

[Promises](#contents.xhtml_sc3_53a)

Promises are a way of representing a completion value or failure of an asynchronous operation. It states that at this point in the execution, the enclosed function will return a value (or error) that will be available at a later point in time.

A Promise has three states:

*   Pending: This is the initial state, plus waiting for a response from the async operation.
*   Fulfilled: The async operation completed successfully.
*   Rejected: The operation failed, and an error was received.

The Promise then defines handlers to manage the data response: then() and catch().

In the simplest of cases, then() handles a non-error response, fulfilling or rather resolving the Promise, and catch() is used to handle any errors returned: rejecting. These two functions also return Promises, which means they are chainable.

Should a specific call to then() require immediate error handling, this can be achieved using the rejection handler, which is the second argument to the then() function.

Promises and the async/await mechanism are discussed in further detail as we move on, as this is a large topic with plenty of gotchas.

[Generators](#contents.xhtml_sc3_54a)

Generators are iterable objects returned by generator functions; iterable objects conform to both the iterable and iterator protocols (they define how an object can be iterated over and what values the iteration yields).

Defining a generator function is like defining other function, but it has a few extra rules:

A generator function is denoted by function* and not by function.

A generator function needs to be able to yield a value and have a way of determining the next value to yield.

An explicit return terminates the generator.

An example generator (as given on MDN) is as follows:

1.  function* generator(i) {
2.  yield i
3.  yield i + 10
4.  }

6.  const gen = generator(10)

8.  console.log(gen.next().value)
9.  // expected output: 10

11.  console.log(gen.next().value)
12.  // expected output: 20

Generators are a very powerful and advanced technique, especially when combined with Promises. However, for working with Vue.js, they provide very little value when compared to async/await.

[Scopes](#contents.xhtml_sc3_55a)

To keep things simple, JS has three types of scope, global, function, and block (or lexical), plus a form of scope inheritance.

While understanding global scope is beneficial to your growth as a developer, is should be of lesser concern to users of Vue.js, so we're not going to concern ourselves with it here too much. We'll cover function and block scope though.

Tip: the var keyword

Modern code aimed at modern browsers should not be written using the var keyword; it's viewed as a bad practice. Additionally, the var keyword is scheduled for deprecation in a future release of JavaScript. The baggage that var comes with when it comes to scoping and hoisting can cause issues to the inexperienced.

ES2015 introduces lexical scoped let and const keywords that have clearer semantics along the lines of other languages developers might be familiar with. We'll discuss these in detail further in the text.

Prior to the release of ES2015, JavaScript did not have lexical scope. All variables were either scoped globally or to the function definition in which they were defined. Variables defined outside of a function are automatically scoped globally; variables defined within a function using var are scoped to the function. Variables defined without the var keyword are scoped globally; this is called global scope. Defining variables in this way is a bad practice as it causes function-defined variables to leak into the surrounding scope, causing confusion and making your code brittle by being subject to mutation by global side effect.

The following code example shows different types of scoping:

1.  // globally defined variable
2.  var var1 = 'defined'

4.  function myFunction() {

6.  var var2 = 'defined'    // function scoped variable
7.  // defined without var
8.  // leaky variable definition
9.  var3 = 'bad'
10.  }

Variables defined in a scope are ‘hoisted' to the top of the surrounding scope by the JavaScript compiler in its first pass through the code; it also moves a few other things in this first pass before code execution on the second pass.

Variable hoisting can lead to some unexpected results if not properly understood. What happens is that the compiler checks the code for variable definition or rather, variable assignment, and pulls the variable declaration to the top of the scope. If the location of the assignment is not toward the top of the surrounding scope, the variable is declared and assigned the value of undefined, as follows:

1.  // defining a variable globally
2.  const firstname = 'Clive'

4.  const addLastname = function () {
5.  const lastname = 'Harber'
6.  // expectation might be 'Clive Harber'
7.  const fullname = `${firstname} ${lastname}`
8.  const firstname = 'Max'
9.  // displays 'undefined Harber'
10.  console.log(fullname)
11.  }

13.  addLastname()

The expectation here might be that the code on line 7 pulls the firstname from the globally defined one on line 2 (due to scope inheritance) so that it can be used in console.log() on line 10\. This view is wrong but understandable.

What the execution engine sees after the compiler first pass is as follows:

1.  // defining a variable globally
2.  const firstname = 'Clive'

4.  const addLastname = function () {
5.  // declared at the top of scope, but unassigned
6.  // therefore at this point they are undefined
7.  const firstname, lastname, fullname

9.  // assignment
10.  lastname = 'Harber'
11.  // assignment, but firstname is still undefined
12.  fullname = `${firstname} ${lastname}`
13.  firstname = 'Max'
14.  // displays 'undefined Harber'
15.  console.log(fullname)
16.  }

18.  addLastname()

Hoisting can be the cause of hard-to-spot bugs, but if you write your code in the way that JavaScript executes it, then these types of issues can be minimized.

With the inclusion of lexical scope in ES2015, issues around hoisting are somewhat mitigated; scopes are more clearly defined as matching braces denoting blocks rather than at the function level. These keywords also differ from var in that they are not hoisted in their surrounding scope; the compiler first pass leaves them in place. This is an important distinction.

This is achieved with the let and const keywords. Semantically, these two keywords are different and so is their designed usage.

let

The let keyword behaves, at least superficially, like var. It creates the desired variable in the current scope and allows you to manipulate it as required. let allows you to create mutable variables. As stated earlier, let is scoped to the enclosing braces; this might be a function, but this also applies to looping and branching constructs; so for, while, if and similar. This allows variable visibility to be managed more easily. As variables defined with let are not hoisted, trying to access them ahead of the point of definition causes a ReferenceError and halts execution rather than continuing with undefined data.

The following code example shows how let can be used:

1.  // simple definition
2.  let var1 = 'a'
3.  let var2 = 'b'

5.  var1 = var2 // var1 is now 'b'

7.  // ReferenceError
8.  console.log(var3)
9.  let var3 = false // not hoisted

let is designed to explicitly mark data that you expect to change. let should be used infrequently to ensure that only the state that is expected to change is changed. Everything else should be defined using const.

const

const is similar to let in many ways. Where let allows you to alter the state, const does not. It does not allow reassignment, redeclaration, or shadowing, irrespective of whether the initial creation or the redefinition is through let or var. Trying to change a const defined variable will cause the compiler to throw an Error type.

Note: const and object types

In general, const should be used to declare both primitive and object types. The reason is that for object types, const holds the reference to the object rather than the object itself. Unless you explicitly need to recreate the reference to an object, you don't need to use let to hold it. As const holds just the reference, you can still manipulate the object type as necessary.

The following code shows how const is different from let:

1.  // simple definition
2.  const var1 = 'a'
3.  const var2 = 'b'

5.  var1 = var2 // redefinition throws Error

7.  // ReferenceError
8.  console.log(var3)
9.  const var3 = false // not hoisted

As const does not allow mutation of the state (if that state is primitive data), it should be used by preference to ensure that you have control over the state and that it is in the expected form when you want to use it. It helps to minimise side effects, bearing in mind the note provided earlier.

[Classes, IIFEs and Modules](#contents.xhtml_sc3_56a)

One of JavaScript's strengths is that it can be used for both object-orientated programming, discussed here, and functional programming, discussed later.

The class syntax that JavaScript uses is a wrapper around the prototypal inheritance model that is central to how JS behaves. Classes, however, do work as expected if you have OOP experience.

Vue.js components written using JavaScript doesn't use classes. That doesn't mean understanding classes is not useful; classes can be used to provide supporting functionality.

The properties and methods (both instance and static) of a class are public by default. Privately scoped class properties and methods are due to be available in ES2022; however, these are immediately available if code is compiled using Babel version 7.3 or greater.

Inheritance is facilitated through the extends keyword. Class initialization uses the constructor() function, with the super() function providing access to the parent constructor. Access to properties can be controlled through the get and set property accessors.

We will not discuss the specifics of OOP here, but we will cover the syntax with a brief example:

1.  class Vehicle { 
2.  // define private properties
3.  #wheels
4.  #totalPassengers
5.  #currentPassengers

7.  // constructor function
8.  constructor (wheels, totalPassengers) {
9.  this.#totalPassengers = totalPassengers
10.  this.#wheels = wheels
11.  this.#currentPassengers = 0
12.  }

14.  // public getter
15.  get maxOccupancy () {
16.  return this.#totalPassengers
17.  }

19.  // public accessors
20.  set passengers (numberOfPassengers) {
21.  this.#currentPassengers = numberOfPassengers
22.  return this
23.  }

25.  get passengers () {
26.  return this.#currentPassengers
27.  }
28.  }

30.  // Child class
31.  class Car extends Vehicle {
32.  constructor (totalPassengers) {
33.  super(4, totalPassengers)
34.  }
35.  }

37.  const car = new Car(4)
38.  const peopleCarrier = new Car(7)
39.  peopleCarrier.passengers = 5

41.  console.log(car.maxOccupancy) // 4
42.  console.log(peopleCarrier.maxOccupancy) // 7
43.  console.log(`People Carrier currently has ${peopleCarrier.passengers} passengers`)

Immediately invoked function expressions of IIFEs were a way of encapsulating state in lieu of having formalized classes. They effectively used closures to hide properties and managed a public interface.

An IIFE is a function that is immediately invoked, which has a return value that provides the public interface; so using the vehicle example from earlier and rewriting it as an IIFE, you get the following:

1.  const vehicle = (function () {
2.  let _wheels, _totalPassengers, _currentPassengers

4.  const create = function (wheels, totalPassengers) {
5.  _wheels = wheels
6.  _totalPassengers = totalPassengers
7.  _currentPassengers = 0
8.  }

10.  const maxOccupancy = function () {
11.  return _totalPassengers
12.  }

14.  const setPassengers = function (numOfPassengers) {
15.  _currentPassengers = numOfPassengers
16.  }

18.  const getPassengers = function () {
19.  return _currentPassengers
20.  }

22.  return {
23.  create, maxOccupancy, setPassengers, getPassengers
24.  }
25.  })()

27.  const car = vehicle.create(4, 4)
28.  car.setPassengers(4)
29.  console.log(car.getPassengers())    // 4

What you will notice is that the function declaration is wrapped in () and then immediately invoked with () and the return object is assigned to the variable. Access to the object functions is then provided through the dot (.) operator, as it would be for any other object property. This allows you to encapsulate the data of the ‘object' into a private space. Everything that is not in the returned object is scoped privately.

IIFEs, although an older technique, is still useful in some cases but will become less relevant with ES2022.

Understanding IIFEs meant that you could build in a modular fashion. However, in modern JS code, a module is simply any file that uses the import and export keywords. As we'll be using those keywords a lot while building Vue.js components, we'll discuss them as we build out the example application.

There's an excellent article on MDN that covers modern module practices at [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules).

[Callbacks](#contents.xhtml_sc3_57a)

Callbacks are functions, often anonymous, that are executed in response to an event or trigger. They are passed into the calling function as a parameter; if you remember, functions are first-class citizens in JS and can be used as data.

Executing a callback is achieved the same way as calling any other function, as the following code example demonstrates:

1.  // Callback function
2.  const waitForMe = () => {
3.  console.log("I'm from the callback")
4.  }

6.  // Passing in the callback
7.  const mainFunction = (callback, name) => {
8.  console.log(`Hi, ${name}`)
9.  // callback execution
10.  callback()
11.  }

13.  // calling the main function
14.  mainFunction(waitForMe, 'Clive')

There's nothing magical going on here; we're just passing the callback function into the required flow and calling it when we need it.

Callbacks are used to handle responses from all sorts of event types: User events and UI interactions like clicks and form changes; asynchronous server responses (AJAX) and promises; file, filesystem and database interactions; in other words, anything that might block the processing thread probably has a callback.

One thing to bear in mind when using callbacks is scope. If you're using an arrow function to define your callback (as demonstrated in the previous code), the scope that the function executes in is the scope in which it was defined, not the scope in which it was called. This can trip you up if your function relies on data from the calling function scope.

If you need data from the execution context scope, then you need to pass that data into the callback:

1.  // Callback function
2.  const processData = data => 
3.  console.log(`I'm from the callback. I have this data: ${data}`)
4.  // Passing in the callback
5.  const mainFunction = async (callback, processData) => {
6.  // execution context data
7.  const val = await longAsyncProcess(processData)
8.  // callback execution with data
9.  callback(val)
10.  }

12.  // calling the main function
13.  mainFunction(processData, 20)

In general, however, you should write your functions to only rely on the data that has been passed in. This reduces issues around scoping and worries about what shape the data is in when the function is being executed.

The previous examples used named callbacks for readability in the book, but they could have been as follows:

1.  const mainFunction = async (callback, processData) => {
2.  const val = await longAsyncProcess(processData)
3.  callback(val)
4.  }

6.  mainFunction(data => {
7.  console.log(`I'm from the callback. I have this data: ${data}`)
8.  }, 20)

Sometimes it makes sense to write the anonymous function directly in the function call, but not so much the other times. Sometimes it's a matter of personal preference or house-style. Neither way is more correct than the other.

One thing to watch out for is something called “callback hell”. Imagine that you're constructing some code that requires a callback to process the data response, but then that code requires a callback to process something else, and then that callback needs another callback, and so on. In code like this, it's very easy to lose track of what is happening.

In code like this, it makes sense to use named callbacks so that those functions can be extracted to reduce the amount of line noise for the reader. The computer doesn't care, but maintaining code like that is a nightmare, hence the term.

One cause of this type of code is the use of Promises and the Promise API. Understanding how to use the Promise API and how to avoid falling into callback hell when using promises is covered next.

[Async/Await and Promises](#contents.xhtml_sc3_58a)

Promises, and in some Functional Programming (FP) libraries, Futures, are essentially placeholders of values that haven't been derived yet. They're a promise that a value will be delivered to that point in the code at some indeterminate point in the future. Promises allow asynchronicity, which means operations that would take a long time to resolve don't block the processing thread while they are resolved.

As a reminder, a Promise can be in one of three given states:

1.  Pending: Where the promise has been set up and is waiting for a result
2.  Fulfilled: Where the result of the async operation has been successfully received and the promise is resolved
3.  Rejected: Where the result the of the async operation has resulted in an error

Once a promise has been resolved or rejected, the value returned cannot be altered; the returned value is immutable.

Setting up a promise involves creating a function that accepts two callbacks: one to handle the fulfilled or resolved case, and one to handle the rejected or error case. However, the error case can be deferred to a catch-all function at the end of the processing chain.

Promises fall into a category of objects called Thenables, which means that they provide a then prototype function to handle the subsequent processing operations. Thenables can usually be chained together, as demonstrated in the following listing:

1.  const myPromise = new Promise((resolve, reject) => {
2.  /* set up and execute long running or async operation */

4.  if (successful) {
5.  resolve(result)
6.  } else {
7.  reject()
8.  }
9.  })

11.  myPromise()
12.  .then(data => { /* process successful result */ })
13.  .then(data => { /* next process in chain, etc */ })
14.  .catch(err => { /* handle any errors here */ })

The Promise API provides several functions that are helpful in managing promises. The most commonly used ones are all(), any() and race().

Promise.all() takes a list of promises that need to be resolved at the same time and returns a collection of successfully resolved promises when all the return values are in. If any of the provided Promises fail, the Promise.all() function calls the rejects function immediately, discarding all received good results. It's an all or nothing operation. Let's look at an example:

1.  // These resolve
2.  const firstPromise = new Promise((res, rej) => res())
3.  const secondPromise = new Promise((res, rej) => res())
4.  const thirdPromise = new Promise((res, rej) => res())
5.  // This rejects
6.  const lastPromise = new Promise((res, rej) => rej())

8.  Promise.all([
9.  firstPromise,
10.  secondPromise,
11.  thirdPromise,
12.  lastPromise
13.  ])
14.  .then(data => { /* process success */ })
15.  .catch(err => { /* as the last promise rejects, result ends up here */ })

Promise.any(), like Promise.all(), accepts a list of Promises and immediately returns the first result obtained. Only if none of the Promises resolve does Promise.any() call the reject function . Consider the following example:

1.  // These resolve
2.  const firstPromise = new Promise((res, rej) => res())
3.  const secondPromise = new Promise((res, rej) => res())
4.  const thirdPromise = new Promise((res, rej) => res())
5.  // This rejects
6.  const lastPromise = new Promise((res, rej) => rej())

8.  Promise.any([
9.  firstPromise,
10.  secondPromise,
11.  thirdPromise,
12.  lastPromise
13.  ])
14.  .then(data => {/* even though there's a rejection, code ends up here */})
15.  .catch(err => {  })

Promise.race() is like Promise.any(); however, race() returns when the Promise is settled, whether that is fulfilled or rejected, and any() returns the first fulfilled Promise. There is a difference (refer to the following code):

1.  // This resolves in ~400ms
2.  const firstPromise = new Promise((res, rej) => res())

4.  // This rejects in ~ 200ms
5.  const secondPromise = new Promise((res, rej) => rej())

7.  Promise.race([
8.  firstPromise,
9.  secondPromise
10.  ])
11.  .then(data => { /* rejection happens first */ })
12.  .catch(err => { /* error is received */ })

Promises rely on callbacks, so it pays to make sure you avoid callback hell, as described earlier.

One of the best ways to mitigate callback hell when using Promises is to use the async/await syntax. These are convenience wrappers to make async code look and read like synchronous code. Functions marked with async are automatically, implicitly, wrapped in a Promise, which then uses the await keyword to mark the long operation. await causes the code to operate in a synchronous fashion, pausing program execution. The await keyword can only be used in functions marked as async. Without it, the code will throw a SyntaxError. The following example shows this in action:

1.  // define async function
2.  const asyncFunction = async data => {
3.  // long running operation
4.  const result1 = await longAsyncFunc1()
5.  const result2 = await longAsyncFunc2(data)
6.  return [result1, result2]
7.  }

9.  // call the function and handle the result and error
10.  asyncFunction().then(data => { }).catch(err => { })

Both the Promise API and async/await have their place in building Vue.js applications, which we'll look at while we work through the rest of the chapters.

[AJAX](#contents.xhtml_sc3_59a)

AJAX can happen in many forms. It once stood for Asynchronous JavaScript and XML, it is now an umbrella term for all remote HTTP-based communication, regardless of what the data package contains. Modern data packages most likely comprise of JSON because its leaner than XML and maps more easily to JS data structures and concepts.

There's plenty of material online about how to use AJAX, and we'll look at it in detail in [Chapter 13](#ch13.xhtml), Managing State With Pinia and API Communication.

[Building structures](#contents.xhtml_sc3_60a)

Here, we're going to talk about destructing JS objects and arrays into primitives and other objects.

Destructuring is a simple form of pattern matching where array values and object properties are ‘matched' into variables. This way, only the data that you need can be extracted in assignments and function calls.

In some of the functional languages, the pattern match can happen on either side of the = operator, but in JS, it can only happen on the LHS.

Pulling apart an array is simply a case of providing the required number of placeholder variables to capture the expected data; the rest of the contents of the array can be safely ignored or pushed into a variable marked with the rest operator:

1.  const animals = ['dog', 'cat', 'hamster', 'mouse', 'otter', 'beaver']

3.  // need all the array contents here
4.  const [ dog, cat, ...otherMammals ] = animals

6.  // don't care about dogs or other animals
7.  const [ , myCat ] = animals

Similarly, objects are easy to deconstruct, but you use the property keys to identify the data required, rather than place order:

8.  const obj = { a: 1, b: 2, c: 3 }

10.  // Just pull out a and c
11.  const { a, c } = obj

13.  // Reassign values a and c
14.  const { a: one, c: three } = obj

16.  // Assign default values in match, if not provided
17.  const { a, d = 4 } = obj

Objects can also be matched as part of a function definition structure. This ensures that functions only take the data out of a passed object that it needs:

1.  const shape = { type: 'circle', radius: 4, centre: { x: 4, y: 4 } }

3.  const areaOfCircle = ({ radius }) => Math.PI * radius * radius

5.  const distanceFromOrigin = ({ centre: { x, y } }) => Math.sqrt(( x * x ) + ( y * y ))

7.  const area = areaOfCircle(shape)
8.  const distance = distanceFromOrigin(shape)

We'll be using destructuring a lot in working through this book, so you'll get plenty of practice.

[Basic functional programming concepts](#contents.xhtml_sc3_61a)

Many modern languages have started integrating concepts espoused by the functional programming (FP) paradigm; this is in addition to the object-orientation foundations that most of them were built on. There are several reasons for this: it's the “new cool” thing, and everyone else is doing it. OOP, while a decent enough practice is not the only way to write software and it's not necessarily the best way in all cases, i.e., use the right tool for the job. FP allows you to make some guarantees about your program state that OOP doesn't. Composing functions to operate over immutable state is often easier to read/follow, reducing time to understand what is happening for maintenance or debugging purposes. Whatever the reason, understanding FP principles never hurts.

Of the many concepts that exist in FP, the following can be applied either directly or with a little discipline to your JS code: immutability, purity, and declaration of intent and function composition. We'll discuss each of these in turn.

To support FP in JS, there are several libraries that have grown to help you manage data types and data flow. Some conform to the Fantasyland specification ([https://github.com/fantasyland/fantasy-land](https://github.com/fantasyland/fantasy-land)) that describes algebraic structures and their use in JS. Libraries that conform to this specification include Sanctuary.js, Folktale.js, and Ramda.js. Other libraries, like lodash.js, underscore.js, and immutable.js are less strict in their application of the principles but are easier to work with.

[Immutable data](#contents.xhtml_sc3_62a)

Immutability can be enforced in your code in a couple of ways; immutable.js is a library that supplies types that resemble the standard types in JS but are designed to be immutable. If you dislike the idea of using a third-party dependency, immutability can be implemented using a little forethought and some rigor to enforce the rules in a simple and effective manner.

The concept of immutability refers to the state of a variable. Once a variable has been defined, it is not changed. The state of your application, that is, the data that your application operates on, is not mutated directly but altered in a controlled way by copying, transforming, and assigning to an alternative variable.

Dealing with primitive data this way is simple in JS by using const as described earlier. If all your primitive data is created this way, if you try to overwrite the data created this way, your application will complain.

Examples of this have already been covered in the section on const.

Types that assign references when created (so Arrays, Objects, Maps, Sets), require a little more care. To maintain immutability in these types, instead of using language constructs that allow you to directly mutate the data contained, use the prototype methods supplied by that type (i.e., map(), filter(), reduce(), entries(), values(), assign(), etc.) and assign the result to a new const. This way, the original variables' integrity is maintained, and the required transformation is performed.

Libraries like those already mentioned provide supplementary functionality that can be invaluable to this effort.

[Purity](#contents.xhtml_sc3_63a)

The concept of purity is that functions do not, under any circumstances, have side effects or operate on data that they haven't been supplied with. In JS, purity is an ideal, rather than an absolute. Some side effects are required and necessary, like writing text to a screen or printing a document, but some are detrimental and need to be avoided, like using or changing global variable data, and altering the state in the enclosing context. Writing code that causes global state change, unless in a controlled and understandable manner, is a code smell and should strictly be avoided. Relying on global state is deemed as poor practice.

If a function is designed with purity in mind, it needs to only operate on the data that it is supplied with and return values that are predictable and consistent with the supplied data. Pure functions should be idempotent: with a given set of inputs, the expected output should not vary, regardless of external conditions. You wouldn't expect 99 + 1 to not equal 100 ever, so why should you expect the output of a function to give you a different answer if you're giving it the same data? The answer is that you shouldn't; you should try to code, at least the applications business logic, without side effects.

The purest of pure functions is a simple function that performs addition:

1.  const addNumbers = (a, b) => a + b

3.  console.log(addNumbers(1, 2))         // 3

What we would not expect is that this function relies on something external, as we cannot predict what value that external thing might have. It might be a benign, expected value, or it might be something completely different:

1.  var someGlobalValue = {}

3.  const addNumbers = (a, b) => a + b + someGlobalValue

5.  console.log(addNumbers(1, 2))        // 3[object Object]

When we try and use pure functions in JS, we need to be mindful of only using the data supplied or in context and not relying on global data.

[Declaration of intent](#contents.xhtml_sc3_64a)

Most code written in languages that use the C-style of syntax, which includes JS, is of an imperative style. Usually, this is regardless of whether this is procedural or object-orientated; it's a set of instructions that detail, line by line, what you expect the computer to do, in essence, a recipe. Writing code like this is fine; millions of lines are written this way every day, and most of it works fine.

Writing code declaratively means you state what you want to achieve but leave the details up to the execution engine, i.e., how best to achieve it.

To support this, the code written should favour the following:

*   Iterators over loops, or recursion
*   Partial application and composition
*   Use of ternary operators over language constructs where they exist
*   Avoiding state mutation and side effects

We're advocating “should” here as some of these concepts are not native in JS, tail call optimization, for example. Other concepts like partial application and composability are ideas on how to build code with JS rather than have native support.

[Partial Function Application and Composability](#contents.xhtml_sc3_65a)

Partial function application, called currying after Haskell Curry, means to provide fewer arguments to a function to return an intermediary function that performs the expected operation only when all expected arguments have been applied.

If functions are written to be pure, then they have predictable outcomes. With predictable outcomes, functions can be combined in innovative and novel ways. Small functions can be built up into larger functions without having to be concerned with intermediary results. Understanding partial function application helps understand function composition.

JS does not support partial application, currying, natively. It does, however, provide support for emulating this through the use of syntax and the first-class nature of functions, as follows:

1.  // Function taking 3 arguments
2.  const threeArgFunction = (a, b, c) => `${a} ${b} ${c}`
3.  console.log(threeArgFunction('hi', 'de', 'hi')) // hi de hi

5.  // Function that applies args by partial application
6.  const partialArgFunction = a => b => c => `${a} ${b} ${c}`
7.  console.log(partialArgFunction('hi')('de')('ho'))

9.  // OR
10.  const applyHi = partialArgFunction('hi')
11.  const applyDe = applyHi('de')
12.  const str = applyDe('ho')
13.  console.log(str) // hi de ho

When building functions like this in JS, currying in itself is not all that special, just turning a multi-argument function into many single argument functions, which return intermediary functions that can be called as required.

Using this knowledge, and taking one step further, we get to composition. Composition is the combination of a multitude of functions to create flows of increasing complexity, avoiding streams of instructions, such as you would get from imperative programming. You can avoid imperative style looping and creating recipe like instructions by abstracting away the various complexities of the processing into operations based on simple and/or pure functions:

1.  // simple, pure functions
2.  const simpleAdd = x => y => x + y
3.  const product = x => y => x * y

5.  // partial application of 10
6.  const multiplyBy10 = product(10)

8.  //construct the result
9.  const result = multiplyBy10(simpleAdd(5)(5))

Having composition work properly in JavaScript relies on having side-effect free code. Functions used in composition need to have outputs that match the inputs of the next function in the chain. In JavaScript, because of implicit typecasting, this is not strictly necessary but can be a source of subtle and hard to diagnose bugs.

Some of the previously mentioned libraries have a compose function that allows composition in an elegant way, but it's not all that difficult to build one from first principles. All that needs to be understood is the mathematical application of the formula g(f(x)). Let's see the following example:

1.  // g(f(x))
2.  const compose = (f, g) => x => g(f(x))

4.  // composing functions
5.  const compute = compose(
6.  simpleAdd(5),
7.  multiplyBy10
8.  )

10.  // obtaining result
11.  const result = compute(5)  // 100

13.  // Variable length compose
14.  const vcompose = (...funcs) => x => funcs.reduce((acc, f) => f(acc), x)

16.  // composing functions
17.  const vcompute = vcompose(
18.  simpleAdd (5),
19.  multiplyBy10,
20.  multiplyBy10
21.  )

23.  // obtaining result
24.  const result = vcompute(5)  // 1000

The vcompose function in the previous listing is a little more complex as it now accepts many functions in the form of a list and applies them in the order provided. This demonstrates the power of compose as a technique: assemble all the parts that you need upfront, and then apply the required data and collect the results, no need to worry about what's happening in between.

Building code this way, i.e., using composition, can be a tool to make the code cleaner and easier to maintain and understand.

[Client-side APIs](#contents.xhtml_sc2_66a)

The HTML5 specification contains several useful standard API's that can be used to build feature-rich and engaging interfaces. Introducing these APIs somewhat removes the reliance on third-party functionality, especially jQuery.

[Fetch API](#contents.xhtml_sc3_67a)

The Fetch API is designed to obtain resources that the website needs, utilising a flexible interface. It is functionally similar to XMLHttpRequest.

As fetch() is asynchronous, it returns a Promise, which then makes it easy to handle the Response object that is returned. At a basic level, you supply a URI string to the fetch() function, which is the only mandatory argument, and it responds with a Response object. Depending on the body of the Response, you can then extract using one of the Body object functions, as follows:

1.  fetch('https://targetUrl.com/test.json')
2.  .then(response => response.json())
3.  .then(json => doSomethingUsefulWithThisData(json))
4.  .catch(err => handleError(error))

Here, we're using .json() function as we're expecting JSON back from the URI provided.

As fetch returns a Promise, we can combine it with async/await:

1.  function async doFetch(url) {
2.  const response = await fetch(url)

4.  if (!response.ok) {
5.  throw new Error('ErrorMessage')
6.  }

8.  return await response.json()
9.  }

11.  doFetch('https://targetUrl.com/test.json')
12.  .then(json => doSomethingUsefulWithThisData(json))
13.  .catch(err => handleError(error));

Using async/await is a little more verbose (in this example), but it is clearer and gives you the opportunity to handle errors more explicitly.

The fetch() function takes a second optional argument that allows you to refine how the request is sent. This configuration object provides the following properties:

1.  {
2.  method: HTTP_VERB, // i.e. GET, POST, PUT, DELETE, etc.
3.  mode: REQUEST_MODE, // cors, no-cors, same-origin
4.  cache: CACHE_TYPE, // default, no-cache, reload, force-cache, only-if-cached
5.  credentials: CREDS_HANDLING_TYPE, // include, same-origin, omit
6.  headers: {
7.  WHAT_HEADERS_TO_USE
8.  // 'Content-Type': 'application/json'
9.  // 'Content-Type': 'application/x-www-form-urlencoded',
10.  },
11.  redirect: HANDLE_REDIRECT, // manual, follow, error
12.  body: POST_BODY // body data type must match "Content-Type" header
13.  }

There are a few more, but these are the most you'll use on a regular basis.

As you can see, the Fetch API allows you to make requests for remote data in an easy and manageable way, without relying on third-party libraries like jQuery or Axios.js. This removes project dependencies, maintenance, and versioning headaches and provides a standard interface.

[Canvas API](#contents.xhtml_sc3_68a)

The Canvas API is designed to allow developers to create graphics using JavaScript within an HTML <canvas> element. The <canvas> element can be used to build animations, graphics for games, visualisations, and photo editing. Primarily, the Canvas API is used for 2D graphics. If you need 3D graphics, then using the WebGL API is more appropriate as it has access to hardware acceleration.

To use the API, you firstly need access to the element's context:

1.  // HTML
2.  <canvas id="canvas" width="100" height="100"></canvas>

4.  // JavaScript
5.  const canvas = document.getElementById("canvas")
6.  const ctx = canvas.getContext("2d")

With access to the context, we can now use the canvas grid and functions provided by the context prototype to create shapes, import images, and apply transformations:

1.  // create a rectangle
2.  const rect = new Path2D()
3.  rect.rect(20, 20, 60, 60)

5.  // change colour to blue
6.  ctx.fillColor('blue')
7.  // add rect to canvas context
8.  ctx.fill(rect)

10.  // push context onto canvas stack
11.  ctx.save()
12.  // perform transformations
13.  ctx.rotate((Math.PI / 180) * 30)
14.  ctx.scale(3, 3)
15.  // restore canvas
16.  ctx.restore()

This is only a taste of the capability of the Canvas API, but this is all that we've got space for.

[Drag and Drop API](#contents.xhtml_sc3_69a)

Historically, the drag-and-drop capability was provided by third-party libraries like jQuery. HTML5 Drag and Drop API defines several events and handlers and attributes.

It all starts with the draggable attribute. This designates the element draggable. To show that an element will accept a draggable, i.e., make it a drop zone, the receiving element needs to handle both the drop and dragover events, either by adding event listeners or by passing functions directly to the event handlers.

To move information (HTML nodes, images, text, files, etc.) using the Drag and Drop API, the dataTransfer property enclosed in the provided event object is used. See the following example:

1.  // HTML
2.  <div class="w-full">
3.  <div class="w-1/2">
4.  // Drag list
5.  <ul ondragstart="dragStart(evt)">
6.  <li draggable="true" id="one">One</li>
7.  <li draggable="true" id="two">Two</li>
8.  <li draggable="true" id="three">Three</li>
9.  </ul>
10.  </div>

12.  <div class="w-1/2">
13.  // Drop list
14.  <ul ondragover="dragOver(evt)" ondrop="drop(event)">
15.  </ul>
16.  </div>
17.  </div>

19.  // Script
20.  <script>
21.  const dragStart = (evt) => {
22.  evt.dataTransfer.setData('text/html', ev.target.id)
23.  }

25.  const dragOver = (evt) => {
26.  evt.preventDefault()
27.  }

29.  const drop = (evt) => {
30.  const data = evt.dataTransfer.getData('text/html')
31.  evt.dataTransfer.dropEffect = 'move'
32.  evt.target.appendChild(document.getElementById(data))
33.  }
34.  </script>

[History API](#contents.xhtml_sc3_70a)

The History API allows you to interact with the browser session history so that you can programmatically navigate the user.

To simulate pressing the browser back button:

1.  window.history.back()

Moving the user forward, i.e., pressing the forward button:

2.  window.history.forward()

To navigate directly to a particular step, pass an integer into the go() function:

3.  // move forward in 2 pages
4.  window.history.go(2)

6.  // move backwards 3 pages
7.  window.history.go(-3)

9.  // refresh the current page
10.  window.history.go(0)

[Web Storage API](#contents.xhtml_sc3_71a)

Web storage is a simple key-value store available in the browser. It provides two different mechanisms: sessionStorage for storing data required only for the current session, and localStorage, which persists data for an indefinite period.

Both mechanisms use the same set of functions:

*   <storageType>.setItem("key", value) for putting a value into storage
*   <storageType>.getItem("key") get a stored value back out of storage
*   <storageType>.removeItem("key") delete the selected value from storage
*   <strorageType>.clear() clear all the stored data

The following examples demonstrate how to use the Web Storage API:

1.  // LocalStorage

3.  // Setting a item
4.  localStorage.setItem('key', value)

6.  // Getting a item
7.  const value = localStorage('key')

9.  // Remove an item
10.  localStorage.remove('key')

12.  // SessionStorage

14.  // Setting a item
15.  sessionStorage.setItem('key', value)

17.  // Getting a item
18.  const value = sessionStorage('key')

20.  // Remove an item
21.  sessionStorage.remove('key')

Even though you can directly manipulate the storage object, the recommended way is to use the API functions to manage this data to avoid several pitfalls, including bypassing inheritance, preventing method overriding, and avoiding issues around the __proto__ property.

[Web workers](#contents.xhtml_sc3_72a)

Web workers allow you to create long running operations and run them on a background thread, away from the main web processing thread.

These are important in modern web applications because they provide additional non-blocking process routes and form the basis of building progressive web apps (PWAs) using Vue.js.

Web workers themselves have access to many of the standard APIs detailed here, plus they can spawn new workers themselves. As web workers are removed from the main web thread, they cannot manipulate the DOM. Of the three types of workers available via the API (dedicated, shared and service), a Vue.js PWA uses the Service Worker type by default (generated by the CLI into src/registerServiceWorker):

1.  /* eslint-disable no-console */

3.  import { register } from 'register-service-worker'

5.  if (process.env.NODE_ENV === 'production') {
6.  register(`${process.env.BASE_URL}service-worker.js`, {
7.  ready () {
8.  console.log(
9.  'App is being served from cache by a service worker.\n' +
10.  'For more details, visit https://goo.gl/AFskqB'
11.  )
12.  },
13.  registered () {
14.  console.log('Service worker has been registered.')
15.  },
16.  cached () {
17.  console.log('Content has been cached for offline use.')
18.  },
19.  updatefound () {
20.  console.log(‘New content is downloading.')
21.  },
22.  updated () {
23.  console.log(‘New content is available; please refresh.')
24.  },
25.  offline () {
26.  console.log('No internet connection found. App is running in offline mode.')
27.  },
28.  error (error) {
29.  console.error('Error during service worker registration:', error)
30.  }
31.  })
32.  }

This file provides the standard hooks that could be used by the registered service worker; each callback will accept an argument that represents the service worker that can be used to send messages to the worker when the callbacks are used. To have your application use a service worker, you need to provide a src/service-worker.js file that contains the handlers for the messages that you are expecting to send. When working in a service worker file, the service worker itself is referred to as self.

So, suppose we update the preceding code sample with the following change to the update handler:

1.  ...
2.  updated (registration) {
3.  registration.waiting.postMessage({msg: 'test'})
4.  }
5.  ...

Then we would set up the service worker to receive the message as follows:

1.  self.onmessage = (msg) => {
2.  if (msg.data.msg) {
3.  console.log(msg.data.msg)
4.  }
5.  }

Primarily, service workers are used to cache or retrieve information for offline usage or to support a PWA if it is used in offline mode.

[Web Sockets API](#contents.xhtml_sc3_73a)

Web sockets are a two-way communication channel between the server and the web application. In most cases, normal stateless HTTP communication between server and client is sufficient, but sometimes, in the case of messaging applications, you need to establish a dedicated two-way route to send messages. This is what web sockets are for.

To build a web socket-enabled application, you will need to build a client application that establishes the connection and a server app that accepts the connection and processes the requests.

As an example, at the simplest level, establishing a socket connection can be achieved as follows:

1.  const socket = new WebSocket('wss://127.0.0.1:8000') // server endpoint URI

3.  // sending a message to the server
4.  socket.send('Message goes here')

6.  // receiving a message from the server
7.  socket.onmessage = (event) => {
8.  // process message
9.  }

11.  // close the connection
12.  socket.close()

At the server level, you need to create a server that accepts the connection and handles the requests, something like (created in Node.js) the following:

1.  import { server as wsServer } from 'websocket'
2.  import { createServer } from 'http'

4.  const wsPort = 8000

6.  // Create the http server and the websocket server.
7.  const httpServer = createServer()
8.  server.listen(wsPort)
9.  const ws = new wsServer({ httpServer })

11.  ws.on('request', request => {  // process request })

The important parts here are as follows:

*   The server and client communicate over the same port, which in this case, is 8000.
*   The client establishes the connection using the wss protocol (wss is like https for web sockets).
*   Messages sent by either side are identified and handled as required. Messages of types that are unknown are ignored.

There are server packages available that take the uncertainty of web sockets away from both the server and client sides; the most widely used are ws and socket.io. Documentation and examples for using these can be found on NPM and/or GitHub.

With this short introduction to JS under our belt, we're set to look at the parts of TypeScript that are useful to us.

[Using TypeScript](#contents.xhtml_sc2_74a)

TypeScript (TS) is a “superset” of the JavaScript language. That means it takes what JavaScript is and adds a bunch of extra stuff to the language – in this case, TypeScript adds formal types and type definitions.

Defining a variable with a type follows the same rules as in JS, but with the addition of the type:

1.  const var1: string = 'string'
2.  const var2: number = 1
3.  const var3: boolean = false
4.  const var4: string[] = ['string1', 'string2']
5.  const var5: any = 'anything'

Function parameters and return types can be also defined with the same syntax:

1.  const func = function (para1: type): returnType { }

TypeScript also rewards you if you code to interfaces and use classes.

As a Vue.js developer, you'll probably end up using the interface or type keywords a lot. Interfaces and type aliases are used to define expected prop types and data types, with classes (via the class keyword) being used to create supplementary functionality as required.

As we'll be using interfaces and type aliases quite a lot in the book, we'll just briefly cover these here.

To define an interface, you use the interface keyword and define all the public property and method signatures (if using a class inheritance hierarchy) that you need to describe the interface contract that is required to model the data. Consider the following example:

1.  interface Vehicle {
2.  wheels: number
3.  totalPassengers: number
4.  currentPassengers: number
5.  }

Interfaces are all well and good if you're sticking to OOP type code. Type aliases are more intuitive if you've got an FP leaning, although they fulfil mostly the same job as interfaces. The only real differences are that interfaces can be extended and can be used for class implementations, whereas type aliases cannot. The following example shows how to create a type alias:

1.  type Vehicle = {
2.  wheels: number
3.  totalPassengers: number
4.  currentPassengers: number
5.  }

Interfaces and type aliases are used to make code more readable and maintainable by ensuring that the data supplied is of the expected type, or that it adheres to the provided contract, and gives the reader a name to hook concepts against.

Classes are not any different between TypeScript and JavaScript, except for the typing of the properties and method arguments. Some things that we should really cover here, though, are the extends (along with abstract and super) and implements keywords.

extends is used to build class hierarchies, where a child class extends a parent class and therefore, inherits all the capabilities, responsibilities, and publicly shared data of the parent; this includes any classes that the parent extends. Even though class hierarchies can be arbitrarily deep, having them too deep can be a sign of bad object design and of a large amount of unpaid technical debt.

extends is used in the following manner:

1.  class Vehicle {
2.  // define private properties
3.  private wheels: number
4.  private totalPassengers: number
5.  private currentPassengers: number

7.  // constructor function
8.  constructor(wheels: number, totalPassengers: number) {
9.  this.totalPassengers = totalPassengers
10.  this.wheels = wheels
11.  this.currentPassengers = 0
12.  }

14.  // public getter
15.  get maxOccupancy(): number {
16.  return this.totalPassengers
17.  }

19.  // public accessors
20.  set passengers(numberOfPassengers: number) {
21.  this.currentPassengers = numberOfPassengers
22.  }

24.  get passengers(): number {
25.  return this.currentPassengers
26.  }
27.  }

29.  // Child class
30.  class Car extends Vehicle {
31.  constructor(totalPassengers: number) {
32.  super(4, totalPassengers)
33.  }
34.  }

As you can see, this is very similar to the same example given in JavaScript earlier. Sometimes, when working in a class hierarchy, you need to override a parent method to supplement the provided functionality, but you also need to call the method in the parent class; this is where the super keyword comes into play. Often, you'll call super() from a child class constructor to ensure that the parent's data is initialised correctly. When you need to call an overridden parent method, you'll use super and call the required method in the parent, as presented in the following code:

1.  class Parent {
2.  sayHi() {
3.  console.log('Hi, there!')
4.  }
5.  }

7.  class Child extends Parent {
8.  sayHi(name?: string) {
9.  // Calling super if there's no name defined
10.  name === undefined ? super.sayHi() : console.log(`Hi, ${name}!`)
11.  }
12.  }

14.  const child = new Child()
15.  child.sayHi()              // Hi, there!
16.  child.sayHi('everyone')    // Hi, everyone!

The abstract keyword allows you to build parents that should not be created directly. This is useful for creating base classes for holding the required functionality for their child classes but otherwise should not be instantiated themselves.

A basic, contrived example of this is as follows:

1.  abstract class Person {
2.  protected name: string
3.  protected age: number

5.  construct(name: string, age: number) {
6.  this.name = name
7.  this.age = age
8.  }

10.  abstract speak(msg: string): void

12.  get name(): string {
13.  return this.name
14.  }
15.  set name(name: string) {
16.  this.name = name
17.  }

19.  hasBirthday(): number {
20.  ++this.age
21.  return this.age
22.  }
23.  }

25.  class Employee extends Person {
26.  private salary: number

28.  constructor(name: string, age: number, salary: number) {
29.  super(name, age)
30.  this.salary = salary
31.  }

33.  speak(msg: string) {
34.  console.log(`My name is ${this.name} and I earn £${this.salary}. I want to say ${msg}`)
35.  }
36.  }

Here, not only is the Person class abstract, but it also has an abstract method that needs to be overridden in child classes that extend the Person class. If a class extends an abstract class but does not override all the abstract methods, it also needs to be marked as abstract, otherwise the code will generate an error. In instances like this, the compiler is your friend.

Abstract classes have limited application in Vue.js applications; they're of more use when building server-based applications with Node.js.

implements is used with interfaces. A class can extend another class, but it implements an interface. This means that all properties and methods given in the interface need to be provided by the implementing class. Otherwise, it does not conform to the expected contract, and it will not compile:

1.  interface IPerson {
2.  speak(msg: string): void
3.  hasBirthday(): number
4.  }

6.  class Person implements IPerson {
7.  protected name: string
8.  protected age: number

10.  constructor(name: string, age: number) {
11.  this.name = name
12.  this.age = age
13.  }

15.  get name() {
16.  return this.name
17.  }

19.  set name(val: string) {
20.  this.name = val
21.  }

23.  // Other accessors

25.  speak(msg: string): void {
26.  console.log(msg)
27.  }

29.  hasBirthday(): number {
30.  return  ++this.age
31.  }
32.  }

We'll leave understanding the merits and the how and when to use interfaces, type aliases and/or class hierarchies as an exercise for you. Throughout this book though, we'll use these methods aplenty so if you're not familiar now, you will be when you work through the example code.

There is a lot more to TypeScript than is presented in this chapter; this is just a primer to get your feet wet. We've not touched upon Generics, Partial Types, Decorators, Enum or Mixins, or a bunch of other stuff. Not that these things aren't important; they're just not important enough right now to present here.

[Conclusion](#contents.xhtml_sc2_75a)

This chapter has covered a lot and sets us up in good stead to start moving forward.

As a brief review, we have covered HTML and CSS in some detail; we have also seen how to use JS and TS in modern code. You've also seen some of the most used APIs that are available as a JavaScript programmer and how to use them.

There is a lot to remember from here. Don't worry if you don't get it all the first time; you won't be alone.

[Points to remember](#contents.xhtml_sc2_76a)

Visualize the web page structure as you would a person, but in the following manner:

HTML = Skeleton = Structure

CSS = Skin/Clothing = Display

JS = Behaviours = Actions

For HTML, remember to close tags and indent to keep things readable.

For CSS, keep CSS together in an external file. This way, changes can be made without impacting the page structure. If you keep the specificity of your rules low, they're easier to override when you need to.

For JS, keep your functions short and to the point. Build them with a view of having them work together without outside influence.

[Key terms](#contents.xhtml_sc2_77a)

*   HTML: Hyper Text Markup Language: the bones of your web page/site/application
*   CSS: Cascading Style Sheets: the display layers – skin and clothes of your application
*   JavaScript/TypeScript: Programming languages used to build your applications' behaviors and abilities
*   Object Orientated Programming (OOP): A programming style where elements are modelled as “objects” and programs are different objects working in concert with each other to achieve the programs outcomes; OOP generally uses mutable state
*   Functional Programming (FP): A programming style where the state (data) of a program is passed through a series of functions that apply transformations to achieve the programs aims as state is generally immutable

Join our book’s Discord space

Join the book's Discord Workspace for Latest updates, Offers, Tech happenings around the world, New Release and Sessions with the Authors:

**[https://discord.bpbonline.com](https://discord.bpbonline.com)**

![](images/fm1.png)

# [CHAPTER 4Understanding the Vue.js Instance](#contents.xhtml_ch04a)

[Introduction](#contents.xhtml_sc2_78a)

So far, we have only covered the basics of web development and haven't even started looking at Vue.js yet, but that will change in this chapter.

We're going to delve deeply into what Vue.js is and how it works. Then, we'll look at some of the common patterns that are used to construct applications and then move on to working on how to add various additional supporting cast members that you'll likely need or come across.

After this important foundation, you'll be well on your way to understanding the core ideas used in the framework.

[Structure](#contents.xhtml_sc2_79a)

In this chapter, we will discuss the following topics:

*   The Vue.js instance
*   The Options API
*   Understanding the Vue.js life cycle
*   Reactivity
*   Building an application
*   Mixins, filters, and directives
*   Including TypeScript support in Vue.js applications

[Objectives](#contents.xhtml_sc2_80a)

The objective of this chapter is to get you started on understanding how Vue.js works and how to start building projects using this framework.

This is a foundational chapter; all projects that you create using Vue.js will require the knowledge you will gain from this chapter.

[The Vue.js instance](#contents.xhtml_sc3_81a)

The Vue instance is the main engine of your web application. It forms the foundation of everything that you'll be doing. However, the instance will mostly be transparent to you as components (where you'll usually be working) are essentially just configuration objects. This configuration is called the Options API; you will pass these configuration objects to the instance, which then performs its magic to render the completed elements to the web browser and therefore, to your end user.

There are only a few places where you'll be exposed directly to the instance, and the first is at initialization. If we examine the main.js file from the initial scaffold, which we'll cover later this is chapter, we can see the following:

1.  // import the createApp function
2.  import { createApp } from 'vue'
3.  // import the root component
4.  import App from './App.vue'

6.  // mount web app to the DOM
7.  createApp(App).mount('app')

This initialization code kicks off the application and mounts it to the specified DOM node. The createApp() function takes the specified root component, creates a root instance, and then goes about rendering all the child nodes.

Now that we have an instance, what does that mean? The next section explores the various parts of the Options API and how they are used to construct a component.

[The Options API](#contents.xhtml_sc2_82a)

A component based on the Options API is a JavaScript object that conforms to a defined structure. This structure consists of various key-value pairs and life cycle functions.

The most common options available to you are presented in the following code sample:

1.  <script>
2.  export default {
3.  /* Lifecycle hooks */
4.  beforeCreate() {},
5.  created() {},
6.  beforeMount() {},
7.  mounted() {},
8.  beforeUpdate() {},
9.  updated() {},
10.  beforeUnmount() {},
11.  unmounted() {},

13.  /* Data options */
14.  data() {},
15.  props: {},
16.  computed: {},
17.  methods: {},
18.  watch: {},
19.  emits: {},

21.  /* DOM options */
22.  template: "",
23.  render() {},

25.  /* Asset options */
26.  components: {},
27.  directives: {},

29.  /* Miscellaneous options */
30.  name: ""
31.  }
32.  </script>

As with other parts of a component's setup, these elements are all optional; if your component is purely presentational, then it will only have a template and none or a very small options object definition.

Now that we understand this, we can take a quick look at the various elements of the Vue life cycle.

[Understanding the Vue life cycle](#contents.xhtml_sc2_83a)

Vue.js has two separate life cycles, depending on whether you are using the Options API (as you would in a traditional Vue2 application) or the newer Composition API (introduced in Vue v2.6 and v3).

In this chapter, we're going to cover the Options API and its life cycle in depth, and [Chapter 7](#ch07.xhtml), Creating and setting up a Vue.js application with Vue CLI and Vite will walk you through the Composition API. We are covering the Options API first because any older code that you will come across, especially if ported from v2, will be of the Options API type.

Tip: Options API

The Options API allows you to build components with an object that conforms to a standard set of keys. This allows you to create functionality in packages that can be composed together to build the application. This is great for one-off and simple components, however, the Options API is known for making it difficult to created shared functionality that needs to cross component hierarchies.

Tip: Composition API

The Composition API allows you to create functionality that you can share across component hierarchies. This is especially important if you have a large number of components (say several hundred) and need to be able to easily share code across the estate.

The Options API life cycle is illustrated in the following figure:

![Diagram Description automatically generated](images/figure_4.1.png)

Figure 4.1: The Vue.js Options API life cycle

All the hooks in the Options API are called synchronously. This means any code executed by a hook needs to be short or non-blocking, or ideally, both. While these hooks are useful in managing the state of a component throughout its life cycle, using them to perform heavyweight operations will negatively impact user experience.

[Arrow functions and life cycle hooks](#contents.xhtml_sc3_84a)

When a life cycle hook is encountered, the hooks this context is automatically bound to the instance so that the hook has access to the data, methods, and computed properties of the instance.

Due to the special nature of arrow functions; we're talking about how they don't have a 'this' value and how they are scoped to the parent or surrounding context; they should not be used to build life cycle hook functions. They shouldn't be used for other Options API  properties either, like methods or computed properties. This is demonstrated in the following listing:

1.  export default {
2.  methods: {
3.  someMethod () {
4.  return 'something'
5.  }
6.  },
7.  mounted: () => {
8.  this.someMethod() // the context of this is scoped globally, this call will fail with a TypeError
9.  }

Having no access to this means you will have no access to the component instance, so you'll not be able to work with the component state at all. Also, you'll probably end up with various TypeErrors that can be difficult to trace.

[beforeCreate() life cycle hook](#contents.xhtml_sc3_85a)

As can be seen from the diagram, beforeCreate() is fired right after a component is initialized, but not yet created. At this point in the life cycle, there is no access to the component instance, its data, or any observers; this stuff has not been created yet.

You might be wondering about how this can be useful then. Even though beforeCreate() is seldom called, it can be used to initiate asynchronous events, such as fetching data from a remote resource to put into an application store, Pinia for example, or to interrogate local browser storage, or to ensure that a user has authenticated and is authorized to see the information provided by that component.

The following code sample demonstrates one such use case:

1.  import { createNamespacedHelpers } from 'vuex'

3.  const { mapGetters } = createNamespacedHelpers('myGetters')

5.  export default {
6.  beforeCreate () {
7.  this.getSomethingFromAPI()
8.  },
9.  computed: {
10.  ...mapGetters(['getSomethingFromAPI'])
11.  }
12.  }

Once this hook has competed, the component continues with its initialization and creation. Once the component has been created, the created() hook is fired.

[created() life cycle hook](#contents.xhtml_sc3_86a)

The next life cycle hook in the sequence is the created() hook. At this point, the component has been created, so there is access to the component data, any observers/watchers, computed properties, and methods. The component hasn't been made available to the DOM yet, in other words, it hasn't been mounted yet, so there is no access the $el property; there's no $el because there's no element.

The created() hook is used for manipulating the component data prior to rendering or for performing operations that require the component data to be available, but where it's not necessary to have access to the DOM.

The following code sample illustrates its use:

1.  export default {
2.  created () {
3.  this.myData = 'someValue'
4.  },
5.  data () {
6.  return {
7.  myData: null
8.  }
9.  }
10.  }

After this, the template is compiled into a render function and made ready for mounting.

[beforeMount() life cycle hook](#contents.xhtml_sc3_87a)

Once a component has been created, it needs to be mounted for it to be available for the browser to display. The first of these mounting hook functions, beforeMount(), is called just before the execution of the created render function. This means you will still not have access to the $el property.

Using beforeMount() is the same as any of the other hooks that we've covered; an example is provided here:

1.  export default {
2.  beforeMount () {
3.  this.internalMethod('someValue')
4.  },
5.  methods: {
6.  internalMethod: function (value) { console.log(value) }
7.  }
8.  }

This hook is there to handle value initializations that shouldn't be spread throughout the component and to ensure that expected values are present.

[mounted() life cycle hook](#contents.xhtml_sc3_88a)

As the name implies, this hook is called once the component is mounted. If this is a parent component, its children are not guaranteed to have also completed mounting. Using this hook is the same as all the others; an example is provided as follows:

1.  export default {
2.  mounted () {
3.  this.$el.css('someCssKey', 'someCssValue')
4.  }
5.  }

At this point though, access to this.$el, the $el property, is now available so that the UI can be accessed if necessary.

If for whatever reason you need to ensure that all the child components have been rendered, you need to use the $nextTick callback in this hook as follows:

1.  export default {
2.  mounted () {
3.  this.$nextTick(function () {
4.  this.executeSomethingOverChildComps()
5.  })
6.  }
7.  }

The code here should really be restricted to interacting with, or changing, the DOM, especially if you're integrating non-Vue libraries into the component; mounted() is the last hook before entering the observe/compute/render cycle of the update hooks.

The update hooks are called when data is changed while the component is rendered. There are two hooks: one for before the DOM patching occurs and one for after.

[beforeUpdate() life cycle hook](#contents.xhtml_sc3_89a)

Whenever data in the component changes, this hook is called before the DOM is patched (updated with new data). This provides you access to the new state of any reactive data or allows to perform any required clean-up operations before the new DOM is rendered.

There should be no surprises with the following code example:

1.  export default {
2.  ...
3.  beforeUpdate () {
4.  this.$el.removeEventListener(this.listener)
5.  },
6.  data () {
7.  return {
8.  listener: ...
9.  }
10.  }
11.  }

[updated() life cycle hook](#contents.xhtml_sc3_90a)

The updated hook is used in a similar way to the mounted hook, but for DOM changes that need to be made after the DOM have been re-rendered.

Component state should not be mutated in the updated() hook; this has potential to create an infinite update loop, so much so that it has been noted in the hook documentation.

This hook, like mounted(), does not guarantee that any child components have rendered, so the $nextTick callback should be used if this is a requirement. See the following as an example:

1.  export default {
2.  updated () {
3.  this.$nextTick(function () {
4.  this.executeSomethingOverChildComps()
5.  })
6.  }
7.  }

Tip: The update hooks should not be used if you need to respond to a reactive property change; this is what computed properties and watchers are for. Use the hooks for working with the DOM around the changes.

[beforeUnmount() life cycle hook](#contents.xhtml_sc3_91a)

Eventually, the component will need to be removed from the DOM as the user navigates away, or the component is swapped for something else; if you need to clean up event handlers and/or other reactive properties, this should be done in beforeUnmount(). This helps prevent memory leaks, unnecessary event handlers, and random reactive properties from hanging around.

beforeUnmount() should be relatively simple and can be used as follows:

1.  export default {
2.  ...
3.  beforeUnmount () {
4.  this.leakyValue = null
5.  },
6.  data () {
7.  return {
8.  leakyValue: {}
9.  }
10.  }
11.  }

[unmounted() life cycle hook](#contents.xhtml_sc3_92a)

At this point, the component no longer exists, nor do any bound directives, event listeners, and child components. There is very little that you can do here apart from some last second cleanups, final web service communications, or final profiler messages.

This hook looks the same as all the others:

1.  export default {
2.  ...
3.  unmounted () {
4.  this.$store.dispatch('finalCleanUp')
5.  }
6.  }

[Other hooks](#contents.xhtml_sc3_93a)

There are a few other hooks, but they're not used commonly, and there is little value in covering them here.

[Reactivity](#contents.xhtml_sc3_94a)

In terms of building web applications, and programming in general, reactivity is defined as automatically responding to a change of data or event, usually in a declarative manner.

We can all understand that JavaScript and TypeScript usually do not work in this fashion, but Vue.js does respond to value changes and events; Vue.js is reactive.

Internally, Vue uses a set of proxies, that wrap the original objects which manage this reactivity. In many cases, the proxied object is created transparently for you by Vue, but there are functions provided by the framework that can be used to mark data as reactive for use with the Composition API. We will cover those in depth in [Chapter 6](#ch06.xhtml), Using the Composition API to Manage Component Logic.

[Building an application](#contents.xhtml_sc3_95a)

There are several ways to use Vue.js in your project:

*   As a single component within a page
*   As a small stand-alone component in a wider application
*   As a single page application built up of components working together

However you want to use Vue, you'll be using the createApp() function as detailed earlier in this chapter.

In the main, you would either import the required library file using a script tag (for smaller integrations), or through NPM/CLI (or Vite) for single page apps.

[Using Vue.js as part of a wider app (script tag)](#contents.xhtml_sc3_96a)

There are two ways to integrate Vue through a script tag.

The first and most convenient way is to use the CDN hosted version, at least for prototyping and learning.

The second one is to download and host your own copy of the library files.

The following code listing shows how this is done using the CDN hosted version of the Vue library:

1.  <!DOCTYPE html>
2.  <html lang="en">
3.  <head>
4.  <meta charset="UTF-8">
5.  <meta http-equiv="X-UA-Compatible" content="IE=edge">
6.  <meta name="viewport" content="width=device-
    width, initial-scale=1.0">
7.  <title>Document</title>

9.  <script src="https://unpkg.com/vue"></script>
10.  </head>
11.  <body>
12.  <div id="app"></div>
13.  </body>
14.  <script>
15.  const App = {
16.  template: '<span>{{ text }}</span>',
17.  data () {
18.  return {
19.  text: 'Hello World'
20.  }
21.  }
22.  }
23.  Vue.createApp(App).mount('#app')
24.  </script>
25.  </html>

[Creating Vue.js as a stand-alone application (NPM/CLI)](#contents.xhtml_sc3_97a)

The easiest way to get started with building an SPA is by using the Vue-CLI. The CLI creates a scaffolded application quickly with “batteries included”, so hot reload, file linting, test integration, and modern workflow.

The downside to this is that you need to have Node.js installed on your computer and understand how to use some of the build tools available in this environment.

As this is how we'll be building the example application throughout the remainder of the book, it is recommended that you install the latest version of Node.js (https://.nodejs.org). Any tools and commands that you need will be explained when we come to use them.

With Node.js installed, type the following using your command line:

1.  npm i -g @vue/cli

NPM is the node package manager; it is automatically installed when you install Node. There is an alternative, called Yarn, but we'll be using NPM here. This command installs the Vue CLI globally.

With the CLI in place, you can now create your application, as follows:

1.  vue create my-first-application

You then need to answer a few simple questions, as displayed in [Figure 4.2](#ch04.xhtml_fig4-2), after which your application will be scaffolded out:

![Text Description automatically generated](images/figure_4.2.png)

Figure 4.2: Initial Vue CLI scaffold preset menu

Select the last option: Manually select features. This option opens a list of the following selections (see [Figure 4.3](#ch04.xhtml_fig4-3)):

![Graphical user interface, text, website Description automatically generated](images/figure_4.3.png)

Figure 4.3: Manual configuration menu of Vue.js scaffold

The minimum required selections are as follows:

*   Choose Vue version
*   Babel
*   TypeScript
*   Router
*   CSS Pre-processors
*   Linter/Formatter

With this done, you'll get to select the version of Vue that you want to use, as shown in [Figure 4.4](#ch04.xhtml_fig4-4); here, select 3.x:

![](images/figure_4.4.png)

Figure 4.4: Vue.js scaffold version selection

After this, you'll be presented with several options based on the features selected; choose the most appropriate options for your project. Refer to [Figure 4.5](#ch04.xhtml_fig4-5):

![Text Description automatically generated](images/figure_4.5.png)

Figure 4.5: Final scaffold options menu

The scaffolder will then start pulling in the required dependencies, and once done, you get to what's shown in [Figure 4.6](#ch04.xhtml_fig4-6):

![A picture containing text Description automatically generated](images/figure_4.6.png)

Figure 4.6: Scaffold complete message

From here, just follow the instructions to start the application.

[Creating Vue.js as a standalone application (NPM/Vite)](#contents.xhtml_sc3_98a)

Vite is the newest, cleanest way of generating a Vue.js application. It still relies on NPM to create the build, but the instruction is as follows:

1.  npm init vite@latest my-first-application ----template vue

This sets up your application with minimal fuss; take a look at [Figure 4.7](#ch04.xhtml_fig4-7):

![Text Description automatically generated](images/figure_4.7.png)

Figure 4.7: Vite scaffolding output

With a web app generated, we'll take a quick look at how to add some CSS and custom fonts to the mix so that these assets are managed and built as part of the application.

[Mixins, filters, and custom directives](#contents.xhtml_sc3_99a)

If you are coming from Vue2, then these terms will mean something to you. If, however, you're not familiar with these and are purely interested in Vue3, then you may wish to skip ahead to custom directives.

[Mixins](#contents.xhtml_sc3_100a)

Mixins are reusable parts of the Options API that can be distributed among components. For Vue2, they were essential for code reuse.

In the simplest sense, a mixin is an object that holds component options allowable by the Options API that get mixed into a component definition.

The following code examples show how a mixin is created; let's just call it mixin.js:

1.  export default {
2.  beforeCreate () {
3.  this.runOperation()
4.  },
5.  methods: {
6.  runOperation () {
7.  ...
8.  },
9.  overrideMethod () {
10.  console.log('mixin')
11.  }
12.  },
13.  data () {
14.  return {
15.  conflictData: 'conflict'
16.  }
17.  }
18.  }

Here, we've defined a mixin that provides a life cycle hook, a few methods, and some potentially conflicting data. As you can see, it's just a simple Options API object definition.

Using it is equally simple:

1.  import myMixin from '@/mixins/mixin.js'

3.  export default {
4.  // import the mixin into the component
5.  mixins: [myMixin],
6.  beforeCreate () {
7.  this.runLocalOperation()
8.  },
9.  methods: {
10.  runLocalOperation () {
11.  ...
12.  },
13.  overrideMethod () {
14.  console.log('local')
15.  }
16.  },
17.  data () {
18.  return {
19.  conflictData: 'localData'
20.  }
21.  }
22.  }

In essence, when a mixin is applied to a component, the options are merged using a defined strategy:

*   The properties of each mixin will be applied in turn, with the components' own data taking priority in case of conflict.
*   Life cycle hooks are merged into an array and executed in turn, with the components' own hooks the last to be called.
*   Properties that expect object values, like methods or components, will be merged into a single object; in case of a key conflict, the components own options will be used as resolution.

This means that after merge, the preceding component has the following definition:

1.  export default {
2.  beforeCreate: [
3.  (function () { this.runOperation() })(),
4.  (function () { this.runLocalOperation() })()
5.  ]},
6.  methods: {
7.  runLocalOperation () {
8.  ...
9.  },
10.  runOperation () {
11.  ...
12.  },
13.  overrideMethod () {
14.  console.log('local')
15.  }
16.  },
17.  data () {
18.  return {
19.  conflictData: 'localData'
20.  }
21.  }
22.  }

The order of resolution can give rise to some unexpected behaviors if many mixins are used in the same component. What this means in practice is that mixins have the following features:

*   Prone to conflicts: You need to know the properties of each mixin that you're using and understand the merge order to get the expected result. Also, if creating your own, you need to have an insight into the internals of each mixin that you're using to avoid property name conflicts.
*   Magic properties: Because of the nature of mixins, properties defined outside your component are available inside it, seemingly by magic. Again, knowledge of the mixins' internals is required in order to prevent conflicts.
*   Limited reusability: As mixins are plain JS objects, parameters cannot be passed into them to abstract out reusable logic. This means they are an inherently less flexible solution for abstraction.

Because of these limitations, in Vue3, it is recommended that the Composition API is in preference to mixins for the task of abstracting out reusable functionality.

[Filters](#contents.xhtml_sc3_101a)

Filters have been removed from Vue3 altogether. To provide custom formatting for values, which is what filters were originally intended for, it is now recommended that either a component method or computed value is used instead.

[Custom Directives](#contents.xhtml_sc3_102a)

Custom directives are not really used, but they can be a powerful tool in your toolbox. The main reason why they are rarely used is that the basic unit of reuse in Vue is the component, but there may be occasions where lower-level DOM access to the plain elements is required.

Creating a custom directive can happen at either the application level or the component level, and there is comprehensive information on the Vue.js website on how to create these. However, we will not need to use this type of functionality in this book, so finding out more is an exercise left to you.

[Including TypeScript support in Vue.js applications](#contents.xhtml_sc2_103a)

If you followed the CLI-based instructions and selected the TypeScript option, then your project is already TS enabled, and the files that have been pre-generated for you are already in TS.

If you're using Vite to build your application, then you'll need to use the following command to create one that uses TypeScript, otherwise you'll get a JavaScript-based one:

1.  npm init vite@latest my-first-application --template vue-ts

With modern build systems, integrating TypeScript is quite simple.

[Conclusion](#contents.xhtml_sc2_104a)

In this chapter, we covered the basics of what a Vue.js instance is, how to construct one, and the various ways to create a project. We also saw how to hook into the life cycle of a Vue.js instance.

Additionally, we looked at some of the supporting features that the framework provides. Lastly, we found out how easy it is to add TypeScript to a Vue.js project with modern build tools.

In the next chapter, we'll discuss how to design UIs and single-page applications based on hierarchies and composition; we will frame that discussion in the context of the example application that we are going to be building throughout the remainder of the book.

[Points to remember](#contents.xhtml_sc2_105a)

A Vue.js application consists of a Vue.js instance and a set of components constructed using the Options API or Composition API.

*   Many elements in a components construction are optional.
*   Use the Vue component life cycle to perform any actions required to support the user experience.
*   Don't use arrow functions for life cycle hooks or functionality that relies on the this context of component as you will not get the object context that you think you're getting.
*   Vue.js components are reactive, and several mechanisms are supplied by Vue.js to support this out of the box.
*   There are multiple ways to use Vue.js in a project; select the most appropriate way for your particular use case.
*   Project scaffolding is moving to Vite, but there are plenty of uses that the Vue CLI covers that Vite does not.
*   Adding TypeScript to a Vue.js project can be as simple as selecting that option in the project builder.

[Questions](#contents.xhtml_sc2_106a)

1.  Practice constructing applications using the Vue CLI and Vite to become more familiar with the various options that they provide; do this for JS and TS projects.

2.  Find the API documentation for Vue3 and become familiar with it.

3.  What are the three ways that Vue.js can be used to either enhance or create a web project?

4.  What is the preferred method of building reusable functionality in Vue3?

[Key terms](#contents.xhtml_sc2_107a)

*   Instance
*   Options API
*   Composition API
*   Reactivity
*   Mixins
*   Directives
*   NPM
*   Vite
*   Vue CLI
*   Lifecycle hook

Join our book’s Discord space

Join the book's Discord Workspace for Latest updates, Offers, Tech happenings around the world, New Release and Sessions with the Authors:

**[https://discord.bpbonline.com](https://discord.bpbonline.com)**

![](images/fm1.png)

# [CHAPTER 5Designing Component-Based UIs and Single Page Applications](#contents.xhtml_ch05a)

[Introduction](#contents.xhtml_sc2_108a)

In the last few chapters, we've been coming up to speed on the basics of the technologies that lie at the heart of working with Vue.js.

In this chapter, we're going to cover what components actually are, how they can be composed, how to design UIs based on the Vue.js component model, and how data moves between components.

To aid our discussion, we're going to be designing the application that we're going to be building throughout the rest of the book.

[Structure](#contents.xhtml_sc2_109a)

In this chapter, we're going to go over the following things:

*   Understanding Vue.js components
*   Understanding component UI composition
*   Understanding data flow
*   Designing components
*   Functional components
*   The sample application as a set of components

[Objectives](#contents.xhtml_sc2_110a)

This chapter covers how to design and compose user UIs using components and how to manage data between components.

You'll explore the basics of building components through assembling hierarchies of components and understanding how to communicate between them. We'll finally work through the sample application that we'll use to cement the concepts described.

[Understanding Vue.js Components](#contents.xhtml_sc2_111a)

A Vue.js component is a JavaScript or TypeScript object that uses certain keys that the Vue.js instance understands and knows how to render, plus the template markup that accompanies that object and any styling information.

In the main, unless you're building a small set of components, each component will live in its own file; in the Vue documentation, these are called Single File Components or SFCs.

SFC files have a .vue extension rather than .js or .ts. Either JavaScript or TypeScript can be used to create the code for a component, and different components can be built using one or the other language. The builder deals with that; it's all JavaScript in the end.

A single file component consists of a template section, a script section, and a style section, with the style section being optional and the template and script sections being optional under some circumstances. See the following listing as a demonstration:

1.  <template>
2.  <!--
3.  This section can contain HTML and 
4.  references to other components
5.  -->
6.  </template>

8.  <script>
9.  /**
10.  This section contains all the code relevant to make 
11.  this component work
12.  */
13.  </script>

15.  <style>
16.  /**
17.  This section contains general styles
18.  */
19.  </style>

21.  <style scoped>
22.  /**
23.  This section contains styles scoped to this component
24.  */
25.  </style>

A component usually has one script section, although there can also be two, i.e., a normal <script> section and a <script setup> section; at most one template section; and up to two style sections.

The script section is optional if your component only contains markup and doesn't need to receive data.

The template section is optional if your script section contains a render function.

The style sections are completely optional, as oftentimes, you'll be using a CSS framework, like TailwindCSS, Twitter Bootstrap, or Zurb Foundation, and so, a style section should be unnecessary. If you need to have styles bundled with your component, i.e., for local overrides, you can have a general <style></style> section that contains globally affecting styles, or a <style scoped></style> section that holds styles scoped to the holding component only.

[Template Section](#contents.xhtml_sc3_112a)

The template section holds the HTML that comprises the display of the component and only the component.

The HTML can be standard HTML mixed with embedded components and Vue directives, as shown below:

1.  <template>
2.  <main>
3.  <header>
4.  <h1>Sample Template Example</h1>
5.  </header>
6.  <section>
7.  <p>This is just some sample paragraph text</p>
8.  <ul>
9.  <li v-for="item in list"
10.  :key="item"
11.  :item="item"
12.  >
13.  {{ item }}
14.  </li>
15.  </ul>
16.  <custom-component>
17.  This is some slot text
18.  </custom-component>
19.  </section>
20.  </main>
21.  </template>

We'll cover the standard directives later, but they provide the templates with basic looping and decision logic, and you can also create your own if necessary.

[Script Section](#contents.xhtml_sc3_113a)

The script section is where the component definition is put. If you think about it, it's logical; we are dealing with JavaScript components after all.

It is here that we put all the parts that we need to compose a component. In line with building standard JavaScript code, the script section holds all the relevant imports necessary to support the component. It also needs to export the component definition using the default export.

1.  <script>
2.  import CustomComponent from '@/components/CustomComponent.vue'

4.  export default {
5.  name: 'sample-component',
6.  components: { CustomComponent },
7.  data: () => ({
8.  list: ['item 1', 'item 2', 'item 3']
9.  })
10.  }
11.  </script>

[Render function](#contents.xhtml_sc3_114a)

Even though it is recommended that the component uses templates to build the HTML, there can be occasion when you will be able to control the HTML generation more closely; this is where the render function comes in, which is a closer to the compiler alternative.

This is most useful when you have an abstract component to output context-specific HTML that is verbose and/or repetitive to create in a template.

Let's just pull together a quick example to illustrate this.

Our objective here is to build a simple card component. This is an everyday type of component, which, truth be told, is better as a templated component, but it will suffice for this.

This component consists of the following HTML:

1.  <div class="...">
2.  <img src="..." class="..." alt="...">
3.  <div class="...">
4.  <h5 class="...">Title Text</h5>
5.  <p class="...">Just a quick sentence that gives some basic body text for this component.</p>
6.  <a href="#" class="...">Call to action link</a>
7.  </div>
8.  </div>

It's a relatively simple DOM tree that has a couple of levels of child nodes. We'll construct this as a render function-based component. The component consists of the following code:

1.  const { createApp, h } = Vue

3.  const app = createApp()

5.  app.component('card-component', {
6.  render () {
7.  return h('div', { class: '...' }, [
8.  h('img', { src: '#', class: '...', alt: '...' }),
9.  h('div', { class: '...' }, [
10.  h('h5', { class: '...' }, this.title),
11.  h('p', { class: '...' }, this.$slots.default()),
12.  h('a', {
13.  href: this.url,
14.  class: '...',
15.  onClick: $event => { 
16.  console.log('clicked', $event.target)
17.  }
18.  }, this.link_text)
19.  ])
20.  ])
21.  },
22.  props: {
23.  title: {
24.  type: String,
25.  required: true
26.  },
27.  url: {
28.  type: String,
29.  required: true,
30.  default: '#'
31.  },
32.  link_test: {
33.  type: String,
34.  required: true
35.  }
36.  }
37.  })

In general, the format of the component is the same as that of any other component. The big difference here is the render function instead of the <template/> tag.

The basis of any render function is the h() function. h() is a virtual node factory function; it generates virtual nodes with the provided data and has the following signature:

1.  // @returns {VNode}
2.  h('div', {}, [])

4.  h(
5.  // Required
6.  // {String | Object | Function} tag
7.  // An HTML tag name, a component, an async component,
8.  // or a functional component
9.  tag,

11.  // Optional
12.  // {Object} props | null
13.  // An object corresponding to the attributes, props and events
14.  // we would use in a template.
15.  {},
16.  // Optional
17.  // {String | Array | Object} children
18.  // Children VNodes, built using 'h()',
19.  // or using strings to get 'text VNodes' or
20.  // an object with slots.
21.  []
22.  )

If you have any familiarity with Elm, this signature is reminiscent of the functions supplied by the Html module. There is no magic going on here; the h() function is the basis of all rendering in Vue, and it's how the template tag is processed when components are compiled.

As you can see in the example, props are accessed in the render() function the same way as you would in a standard template; see lines 10 and 18 in the example code. The same is the case with accessing instance-specific things like slots (this.$slots) on line 11.

Where render functions differ from standard templates is how events are written and how repeated items are generated.

At place events, where you would use v-on (or  @), you need to use the HTML DOM equivalent; so @click is onClick (as on lines 15 – 17 in the example), @change is onChange, and so on.

When you would like to repeatedly render some elements (v-for) or conditionally render something (v-if), you need to look to the Array.map() prototype function and the if(){} language construct.

As there are no examples of these constructs in the example code, we will look at these in the following examples, first v-if and then its equivalent:

1.  // template
2.  <template>
3.  <p v-if='show'>Show this if true</p>
4.  <p v-else>Show this if false</p>
5.  </template>

1.  // render function
2.  render () {
3.  if (this.show) {
4.  h('p', null, 'Show this if true')
5.  } else {
6.  h('p', null, 'Show this if false')
7.  }
8.  },
9.  props: {
10.  show: Boolean
11.  }

And v-for:

1.  // template
2.  <template>
3.  <ul>
4.  <li v-for="(ele, idx) in list" :key="idx">ele</li>
5.  </ul>
6.  </template>

1.  // render function
2.  render() {
3.  return h('ul', this.list.map(ele => {
4.  return h('li', ele)
5.  }))
6.  },
7.  props: ['list']

There are a few other things that we need to discuss with regard to where render functions differ from templates, but we haven't discussed v-models or dynamic components yet.

[Style Section](#contents.xhtml_sc3_115a)

The style section holds the component-specific style overrides. This section doesn't necessarily need to be CSS, which is the default; any of the available style languages understood by babel, i.e., Sass, SCSS, Less, or Stylus, works, so long as it's marked by the relevant lang attribute.

This section can also be marked as scoped so that the provided styles only apply to this component rather than to the global scope.

Look at the following listing to understand how this might be achieved:

1.  <style>

3.  </style>

5.  <style scoped>

7.  </style>

9.  <style lang="stylus">

11.  </style>

13.  <style lang="scss" scoped>

15.  </style>

17.  <style lang="less" module>

19.  </style>

21.  <style module="myModule">

23.  </style>

What we see here are various ways to define a components style rule:

Line 1: Use standard, globally available CSS

Line 5: Use standard CSS, but scoped locally to component

Line 9: Use Stylus to format the style rules and make them globally available

Line 13: Use SCSS to format style rules and scope locally

Line 17: Set the used CSS language to Less and have this as a plain CSS module that can be referred to in the HTML as $style

Line 21: Use normal CSS style as a named CSS module where the class rules are referred in the HTML as prefixed with the myModule  name

When the styles are marked as scoped, the compiler prefixes all the styles with a random string, which it then injects into the generated HTML to isolate the component styles.

Defining a scoped style is achieved as follows:

1.  <style scoped>
2.  .example {
3.  font-weight: bold;
4.  font-size: 3.5em;
5.  }
6.  </style>

8.  <template>
9.  <div class="example">Scoping styles to here only</div>
10.  </template>

Here, the engine employs PostCSS to transform the preceding into the following:

1.  <style>
2.  .example[data-v-a6d78g2] {
3.  font-weight: bold;
4.  font-size: 3.5em;
5.  }
6.  </style>

8.  <template>
9.  <div class="example" data-v-a6d78g2>
10.  Scoping styles to here only
11.  </div>
12.  </template>

[Understanding component UI composition](#contents.xhtml_sc2_116a)

Building a UI out of components is usually a case of determining what components will be required and constructing each part in turn. Components can be built straight out of HTML, out of other components, or a mix of the two.

The fact that components can be constructed from other components as building blocks is a fundamental property of component-based UIs, particularly of Vue.js, and is called composition.

This abstraction allows for the creation of small, self-contained, reusable components that can be leveraged to build up large-scale web applications. Just like the HTML DOM can be represented by a tree of elements, you can use the same model to think how to build an interface with Vue components. As an example, let us consider the following figure, which shows a wireframe for a simple interface:

![Graphical user interface, text, application Description automatically generated](images/figure_5.1.png)

Figure 5.1: Wireframe for component composition

From this wireframe, we might consider building the interface in the manner demonstrated in the following code snippet:

1.  <template>
2.  <layout-component>
3.  <header-component :title="title" />
4.  <hero-component
5.  :image="image"
6.  :call-to-action-text="ctaText"
7.  />
8.  <description-component>
9.  <p>This is some description text</p>
10.  </description-component>
11.  </layout-component>
12.  </template>

14.  <script>
15.  import LayoutComponent from '@/components/layout/LayoutComponent.vue'
16.  import {HeaderComponent, HeroComponent} from '@/components/layout/GeneralComponents.vue'
17.  import DescriptionComponent from '@/components/text/DescriptionComponent.vue'

19.  export default {
20.  components: {
21.  HeaderComponent,
22.  HeroComponent,
23.  LayoutComponent, 
24.  DescriptionComponent
25.  },
26.  data() {
27.  return {
28.  title: 'Some title',
29.  image: 'image.png',
30.  ctaText: 'Some action text'
31.  }
32.  }
33.  }
34.  </script>

As you can see, the components define attributes and have child elements, just like normal HTML. This is what makes templating in Vue so flexible and powerful; it's just an extension of what you're already used to.

[Understanding data flow](#contents.xhtml_sc2_117a)

Most components you build will require data to be supplied so that they can render effectively. There are obviously exceptions, but oftentimes, a component that just renders static HTML has little use.

This means pretty much everything will need some sort of data or state. While each component usually maintains its own internal state, it is more common to have a parent component pass the state required by each of its children down to them. This ‘one-way' data flow allows for a simple, reactive system of components to be constructed; if the data in the parent changes, it gets cascaded down to all the children that need it, creating smaller diffs as discussed in the previous chapter. Take a look at the following figure:

![Diagram Description automatically generated](images/figure_5.2.png)

Figure 5.2: Flow of data from parent to child

[Figure 5.2](#ch05.xhtml_fig5-2) shows a simple flow of data from parent to child, but it can get tedious and error-prone if the child component that needs the data supplied by a parent is deeply nested. In this case, Vue has a provide/inject mechanism, which is part of the Composition API.

When using Providers and Injectors, the parent is marked with the data that it is allowed to provide, and the child is marked with the data it is allowed to accept.

The following figure demonstrates this functionality:

![Diagram Description automatically generated](images/figure_5.3.png)

Figure 5.3: Provide and Inject, the parent defines what is provided and the child defines what it will accept

There is one small caveat with using provide/inject. The mechanism is not reactive by default, which means when the data in the parent changes, it is not used to automatically update any of the children that rely on that changed data.

In order to make the provide/inject properties reactive, if that's a requirement, the data that is being provided needs to be placed in a reactive wrapper using ref(), reactive(), computed() or similar; refer to the following code sample:

1.  <template>
2.  <parent-component>
3.  ...
4.  </parent-component>
5.  </template>

7.  <script>
8.  export default {
9.  data () {
10.  return {
11.  item1: 'data_point'
12.  }
13.  },
14.  provide () {
15.  return {
16.  data_point: ref(this.item1)
17.  }
18.  }
19.  }
20.  </script>

The one-way data flow pattern doesn't mean children can't influence the state of a parent component, but the mechanism is different: it involves events that are used to pass the data back up the tree.

In this mechanism, the parent defines an event handler that responds to an event emitted by the child. If the child is nested deeply, then the event can use the browser default bubbling mechanism to allow the parent to intercept the event.

The events API provides a number of standard modifiers that can be used to influence how the event is handled, which corresponds to the typical things that you might want to do to an event: prevent propagation (.stop()), fire only once (.once()), or prevent default behavior (.prevent()). There are several others, but these three are the most used modifiers. Other event and key modifiers can be found at [https://v3.vuejs.org/guide/events.html#event-modifiers](https://v3.vuejs.org/guide/events.html%23event-modifiers).

The following image shows how components emit and handle events as a way of communicating between child and parent:

![](images/figure_5.4.png)

Figure 5.4: A child component emitting an event that is handled by its parent

We'll discuss events in depth in [Chapter 11](#ch11.xhtml), Interacting With the UI Using Events.

[Designing components](#contents.xhtml_sc2_118a)

The definition of what constitutes a component is a little flexible. A component can be as little or as large as it needs to be to accomplish the task for which it has been designed. In general, a component handles only one element or a related set of interactions in an interface.

By one element, we're talking about either managing small amounts of related data, a single user action or small set of related actions, or some part of the UI. Most components are small – they handle interactions with buttons or obtaining some user input – and some are large but only handle presentation and passing data down to children and handling general events.

The total scope and therefore, size of a component is for you to decide as the designer/architect. Part of this design process is ensuring that your components are small, flexible, reusable, and testable enough with a well-defined, easy-to-use interfaces and not unwieldy, too large or have too much scope/functionality.

Vue has two main types of components: the normal/classical type that we've been using throughout this discussion so far, and functional components. We'll cover functional components next.

[Functional components](#contents.xhtml_sc2_119a)

Functional components (FCs) are to components as arrow functions are to ordinary functions in JavaScript; they're stripped-down, lightweight versions with limits on their functionality.

What makes FCs different from normal components is that they primarily don't hold or maintain their own state – they don't have a component instance and side-step the component life cycle, akin to arrow functions, which don't have a this instance or their own scope (among other things).

Creating a functional component is relatively simple, instead of an options object (Options API or Composition API), you use a simple plain function that has two arguments: props and context; this is illustrated as follows. The context object provides three properties that also get injected: attrs, emit and slots; these are equivalent to their normal component counterparts $attrs, $emit and $slots.

1.  // simple type
2.  // render function body
3.  const functionalComponent = (props, ctx) => {
4.  }

6.  // using destructing
7.  const functionalComponent = (props, {attrs, emit, slots}) => {
8.  // render function body
9.  }

In this case, you are creating a component that has only a render() function.

If you want to define the props that the FC will accept or the events that the FC will emit, then you do that by adding them as properties, as follows:

1.  // simple type
2.  const functionalComponent = (props, {emits}) => {
3.  // render function body
4.  }

6.  functionalComponent.props = {
7.  prop1: String,
8.  prop2: {
9.  type: Boolean,
10.  default: false
11.  }
12.  }

14.  functionalComponent.emits = ['customEvent']

If you don't define your props, then your FC will receive identical props and attrs objects that aren't validated and the prop names that are not normalized to camel-case, as would be expected in a normal component.

FCs can be used wherever a normal component can be used in the same way, but it requires all data and events to be passed in from the holding parent component:

1.  <template>
2.  <functional-component prop1="String" :prop2="false" />
3.  </template>

5.  <script>
6.  import FunctionalComponent from '@/compontents/functional/FunctionalComponent.js'

8.  export default {
9.  name: 'StandardComponent',
10.  components: { FunctionalComponent }
11.  }
12.  </script>

With this information under our belts, we're ready to start looking at a design and work out how we can break it down using components and then determine the best way to compose the components together to build a functional web application. Let's do that next.

[The sample application as a set of components](#contents.xhtml_sc2_120a)

To design a web application, we're going to need a project – the web agency that you work for has been approached by the growing pizza delivery company Speedy Pizza^([1](#ch05.xhtml_footnote-000)) to prototype for them a new sales portal, as their current one is old and creaking. They want something better and have furnished the agency with a design to build out.

[1](#ch05.xhtml_footnote-000-backlink) this is a purely fictitious name and any association with any company of this name, real or otherwise is purely coincidental.

As you will see from the images, it's a fairly simple design with a few pages.

[Landing page](#contents.xhtml_sc3_121a)

This is a simple landing page with a top menu, a hero section, some “top deals” and access to the menu and accounts sections.

[Design](#contents.xhtml_sc3_122a)

There are four major sections to this page: the top menu and footer, both of which should really be part of the site layout (we'll extract these out later); the hero section; and the offers section, which holds multiple offers.

This is presented in the following figure:

![A picture containing text, food, dish Description automatically generated](images/figure_5.5.png)

Figure 5.5: The clients prototype design for the sample site

[Wireframe](#contents.xhtml_sc3_123a)

From a component point of view, this wire frame can be broken down into a small set of simple components, as shown in the following figure:

![Graphical user interface, application Description automatically generated](images/figure_5.6.png)

Figure 5.6: Showing how to break a design into a wireframe

The hierarchy here is fairly flat: the only parent-child relationship is the OfferComponent and OffersComponent, and even that isn't very complicated.

[Proposed components](#contents.xhtml_sc3_124a)

As it makes sense to use semantic naming for components, we'll match the component names to the terms that we've already been using. So we'll need the following for the landing page:

*   MenuBarComponent to hold the top menu elements and child components.
*   HeroComponent to handle the hero component.
*   OffersComponent to present the offers/deals that Speedy Pizza want to highlight to their visitors on the landing page. As OffersComponent is the parent to all the OfferComponents, it will hold the data needed to display all the offers and only pass the data required to each child.
*   OfferComponent is a component holding the details of a single offer, including a call-to-action button.
*   FooterComponent to hold the information suitable for a footer.

[Listing/Menu Page](#contents.xhtml_sc3_125a)

This is the first of the internal pages that we'll work through; it's a simple list of all the types of pizza that are available. Initially, you'll work with a static list, but we'll look to switch that out later in the book when we look at fetching data from a server.

Working on this page will give us the opportunity to extract the parts of the page that are consistent across the site in terms of layout. At this point, adding in a router is also a good idea.

[Design](#contents.xhtml_sc3_126a)

This page will simply list all the items that are available. Parts of this design, in terms of functionality, will be left until later. This is so that they can be integrated with the data structures that constitute a shopping cart.

[Wireframe](#contents.xhtml_sc3_127a)

As already mentioned, the page is really a list; the wireframe shown in the following figure highlights this:

![](images/figure_5.7.png)

Figure 5.7: Listing Page wireframe

[Proposed Components](#contents.xhtml_sc3_128a)

The bulk of the page consists of a single component, ItemListingComponent, which holds all the ItemComponents, so we'll also be building the site layout files and components. Arguably, that could have been done for the first page, but it makes more sense here. Plus, we will add some basic routing.

The list of components that we're going to be working with on this page include the following:

*   MainLayoutComponent: This component will hold the HeaderComponent and FooterComponents that we've already built to handle the page layout in a consistent and easy-to-manage manner. The layout file will also hold the SideBarComponent.
*   SideBarComponent: This holds current order and other secondary information.
*   SmallCartListComponent: This is a high-level list of all the items in the cart, plus the ability to increase/decrease/delete items held there.
*   SmallCartPriceComponent: As the cart will hold pricing information, it makes sense to inform the user how much it's going to cost, but this can just be a functional component.
*   NavigateToCheckoutComponent: This component handles two operations: the first is to totally clear the cart of the order (the cancel link), and the other is to navigate to the cart, identify whether the user is logged in, and route to the relevant checkout entry point.
*   ItemListingComponent: This is a parent to the ItemComponents and therefore, will hold all the data expected to display an item.
*   ItemComponent: Each individual list component, each of which is going to be a parent to an ImageComponent and an AddCartComponent.
*   ImageComponent: This is a functional component to hold an image.
*   AddCartComponent: This is to manage making changes to the cart.

This is a long but typical list of components for this sort of page design – we're using components to encapsulate functionality and its associated data where appropriate, but you should also be able to start recognizing some of the expected behaviors that will be excellent candidates for Composition API, particularly the cart editing behaviors. There are also a few functional components because they just need to display the provided data.

[Item Display Page](#contents.xhtml_sc3_129a)

This will be the single item display page, in line with similar pages from other e-commerce sites. There'll be a picture, some details and pricing information of the selected pizza, plus the option to add to the cart. The client also wants to include a set of recommendations and available offers.

[Design](#contents.xhtml_sc3_130a)

We'll look to compose several components together here for the actual item that has been selected, some of which will be functional components: specifically for the images and tab body elements. We'll also reuse the pricing and order components.

[Wireframe](#contents.xhtml_sc3_131a)

The wireframe here reuses many components that have already been built; some are coming in from the layout and others are from other pages. This is part of the power and attraction of building UIs using components; we now have a toolkit of reusable parts that we can integrate in new and interesting ways. See the following figure:

![](images/figure_5.8.png)

Figure 5.8: Single Item wireframe

There are some new components here, but they're simple compared to others that we've built.

[Proposed Components](#contents.xhtml_sc3_132a)

Apart from the components already discussed, this page needs ProductDescriptionComponent, a component that consists of a tab bar and several tab contents. We'll build this out as a small set of functional components, with the parent being responsible for keeping track of which tab should be displayed.

[Checkout pages](#contents.xhtml_sc3_133a)

This will be a standard checkout page, listing all items in the current cart. There is also a modal to collect delivery information and whether the user is a guest to the application or wants to deliver their order to an alternative address from their account.

[Design](#contents.xhtml_sc3_134a)

The design intends to clearly display the items placed into the order cart, including any requested special orders/changes, the current price of each item, and the full total of the order. The user also has the capability to add extra information and edit quantities or delete items. All these things are expected accepted functionality.

[Wireframe](#contents.xhtml_sc3_135a)

The components on this page are largely new. There are a few that are reused, that is, ImageComponent and SmallCartPriceComponent, and there are a couple that are quite similar to others that we have already built, but as they need to encapsulate different functionality, it makes more sense to have separate components to handle this.

The following figure does not mark layout elements that we've already discussed:

![Graphical user interface Description automatically generated](images/figure_5.9.png)

Figure 5.9: The checkout page wireframe

When the order button is pushed in the PlaceOrderComponent, the response will be one of two things:

1.  The user is either new or hasn't logged in yet, so we show a modal to get them to log in, create an account or give them the choice to place the order as a guest user. Once this information has been collected, the user can be moved on to payment. The modal wireframe is given in the following figure:

    ![](images/figure_5.10.png)

    Figure 5.10: Checkout with login modal

2.  The user is already logged into the account, so the default delivery data is already available, and the user can move directly to payment, which we've elected to use Stripe for. Refer to [Figure 5.11](#ch05.xhtml_fig5-11):

    ![](images/figure_5.11.png)

    Figure 5.11: Stripe payment modal wireframe

[Proposed components](#contents.xhtml_sc3_136a)

The following is a list of components required for the above design:

*   OrderItemListComponent: This is the parent for OrderItemComponents.
*   OrderItemComponent: These child components are amalgams of an ImageComponent, a ManageOrderComponent, and the relevant textual data contained in each row of the order.
*   ManageOrderComponent: This is similar to AddCartComponent but allows for deleting the item and displays the row price.
*   PlaceOrderComponent: This either clears out the cart entirely or moves the user on to the next step, depending on the logged in status of the user. See the next two figures.
*   CartAddressComponent: This component will hold the delivery address details if available or allow editing if not.
*   ApplyVoucherToCartComponent: This component accepts data relating to a possible voucher code. It is to dynamically check that the code is valid (in both format and content), and then apply it to the cart and update the display accordingly.
*   ModalComponent: This isa standard modal component that accepts multiple internal contents via a slot.
*   LoginComponent: This collects and manages user login data or collects guest checkout data.
*   StripePaymentComponent: This is a wrapper component for working with the Stripe Payment Gateway.

[Login and Registration Pages](#contents.xhtml_sc2_137a)

These are standard login and registration pages. There's nothing controversial here.

[Design](#contents.xhtml_sc3_138a)

The wireframe shows how simple these pages are. Due to the component-based nature, the elements that comprise the forms are extracted out into separate components so that the core functionality can be reused elsewhere.

[Wireframe](#contents.xhtml_sc3_139a)

As mentioned previously, these pages are constructed out of very few components. See [Figure 5.12](#ch05.xhtml_fig5-12):

![](images/figure_5.13.png)

Figure 5.12: Login page wireframe

Structurally, both the log in and create account pages are similar. Apart from MainLayoutComponent, there is a wrapper component and then the required functionality component.

The following figure shows the create account wireframe, which is equally minimalistic in its presentation:

![Graphical user interface Description automatically generated](images/figure_5.131.png)

Figure 5.13: Create account wireframe

[Proposed components](#contents.xhtml_sc3_140a)

The following is a list of components required for the above design:

*   UserWrapperComponent: This is a simple wrapper component that accepts information and component references to create identical layouts for both pages.
*   LoginComponent: The login component has been previously discussed and is being reused here.
*   RegisterComponent: This is similar to LoginComponent but forms the messages to the server to enable the user to register an account.

[Orders page](#contents.xhtml_sc2_141a)

This page is a simple summary of all the orders placed by the user with the option to reorder the exact set of selections.

[Design](#contents.xhtml_sc3_142a)

This will be a simple grid, as demonstrated in the wireframe in [Figure 5.14](#ch05.xhtml_fig5-14), showing previous orders against the account; this is a simple convenience design function that takes that data directly to the checkout page for the user.

[Wireframe](#contents.xhtml_sc3_143a)

The wire is a list of cards that hold the data describing previous orders.

![Graphical user interface Description automatically generated](images/figure_5.14.png)

Figure 5.14: Previous orders summary page wireframe

[Proposed components](#contents.xhtml_sc3_144a)

The following is a list of components required for the above design:

*   OrderGridComponent: This is just a parent component that supplies the relevant data; it is a pattern that you should now be familiar with.
*   OrderCardComponent: These are individual display components for each database entry. The button in the card is there to tell the application to build a new cart out of the data and direct the user directly to checkout.

[Final thoughts](#contents.xhtml_sc2_145a)

This is an ambitious example to build out, but it handles a real-world piece of work. There are always different ways of carving this UI and handling all the events the differently to how we're doing it here; some may be better for different use cases, but this is a logical way of building this particular sample application.

[Conclusion](#contents.xhtml_sc2_146a)

In this chapter, we went through the different parts of a Vue.js component and understood how they relate to each other within the component and across component hierarchies.

We also delved into how to get components to communicate with each other, at least at a very basic level, and how to handle user events.

Finally, we explored how to compose components together to form complex components and worked through a sample application, where we applied this knowledge to help break a design into its constituent parts to provide a simple frame on which to build the desired views.

This chapter was mainly focused on building components using the Options API; the next chapter will describe how to work with the Composition API. Both APIs are valid forms of building components and need to be explored together.

[Points to remember](#contents.xhtml_sc2_147a)

*   An Options API component consists of three sections: Script, Template and Style. These sections are all optional.
*   A render function can be used if tight control over the rendering of a components template is required. This is done by wrapping the h() function.
*   The h() function is the basis of all Vue.js template rendering; there's no magic here.
*   Functional components can and should be used when a component that doesn't need to manage its internal state is required.
*   Components can be composed of other components, and although rare, can also be recursive.
*   Breaking up a design into components doesn't need to be complicated. Components should manage a single concern or be the scaffolding over multiple concerns, but never both.
*   Only events can handle user input or actions. Events can be HTML DOM events like onClick or onChange. Events can also be custom; these types of events are used to pass data between child and parent.
*   Deep hierarchies of components should use the provide/inject mechanism to help a component's parent supply data to its children.

[Key terms](#contents.xhtml_sc2_148a)

*   Template section
*   Script section
*   Style section
*   Props
*   Render function
*   Functional component
*   Events

Join our book’s Discord space

Join the book's Discord Workspace for Latest updates, Offers, Tech happenings around the world, New Release and Sessions with the Authors:

**[https://discord.bpbonline.com](https://discord.bpbonline.com)**

![](images/fm1.png)

# [CHAPTER 6Using the Composition API to Manage Component Logic](#contents.xhtml_ch06a)

[Introduction](#contents.xhtml_sc2_149a)

In this chapter, we're going to be exploring the Composition API; if you think back to [Chapter 4](#ch04.xhtml), Understanding the Vue.js Instance, where we explored the Options API in detail, we said that we would return to the topic. If you're coming from React, this idea is like the one explored in the Hooks API.

[Structure](#contents.xhtml_sc2_150a)

In this chapter we'll cover the following topics:

*   The Composition API
*   The problems solved by the API
*   Composition API Life cycle and Reactive properties
*   Creating Composable utilities
*   Handling Dependency Injection - Provide and Inject
*   Using Teleport and Suspense
*   The VueUse utilities library

[Objectives](#contents.xhtml_sc2_151a)

After studying this chapter, you will understand how the Vue.js Composition API is used and how it is different from the Options API. You'll also understand how to build composable utilities, how to manage user expectation with Suspense, and how to manipulate the HTML DOM with Teleport. Lastly, we'll look at how to import utilities from the VueUse library to make your code more flexible and maintainable.

[The Composition API](#contents.xhtml_sc2_152a)

The Composition API allows components to be built with functions that are imported, rather than creating an options object for the Vue instance to ingest. The documentation for Vue.js states that this is an umbrella term that covers three APIs:

*   Reactivity API
*   Life cycle Hooks
*   Dependency Injection

Each of these APIs is covered in detail later in this chapter.

If you're working on an older project using Vue2, you can still benefit from the Composition API, but you'll need to use the @vue/composition-api plugin, otherwise it's already baked in.

[Problems solved by the Composition API](#contents.xhtml_sc2_153a)

As flexible as the Options API is, it comes with a few downsides when it comes to the reuse of logic across your application, primarily that of mixins. If you may recall, we covered mixins in [Chapter 4](#ch04.xhtml), Understanding the Vue.js Instance.

An application using Composition API no longer uses mixins, and it is no longer restricted by the Options API when a component's size or complexity reaches a certain point, so the organization of the code becomes more flexible. This means that it's easier to manage the code that deals with a particular concern; all the code is grouped together rather than being spread over many lines and across different parts in an Options API-based component. The fact that all the code that manages a particular concern is held together means it can (and should) be extracted into a reusable utility; this is difficult to do with an Options API component; it leads us back to mixins.

While it doesn't affect components built in JavaScript, with the growing adoption of TypeScript, using type inference can be quite difficult with the Options API. The documentation uses absurdly complex type gymnastics; to get this is work with mixins and dependency injection can be extremely difficult or time consuming, to a point where it becomes impractical to implement. As most Composition API functionalities can be implemented using plain JS/TS values and functions that are inherently type friendly, writing manual type signatures often becomes largely redundant, saving time and cycles.

The flexibility now afforded to Vue.js developers is such that you can build applications:

*   Purely in Options API,
*   Purely in Composition API, or
*   With a hybrid approach using both APIs where appropriate.

Which approach to use for an individual component or for your entire application is largely a matter of preference and experience. At the time of this book being written, industry preference is to build components using Composition API, but this can be viewed as a move to embrace the latest changes rather than design for best of breed; our advice is that you design for the requirements of the components rather that what is cool right now.

[Composition API Life cycle and Reactive properties](#contents.xhtml_sc2_154a)

If you recall our discussion of the Options API life cycle, we demonstrated how a component life cycle can be hooked into using the various available options in the component definition: created(), mounted(), updated(), etc. To achieve this, the Composition API provides a setup() method where you specify all the startup hooks and the state references that your component operates over. The changes to the life cycle made by the Composition API are demonstrated in [Figure 6.1](#ch06.xhtml_fig6-1):

![](images/Figure_6.1.png)

Figure 6.1: Composition API life cycle diagram, including the setup hook

This change is expressed in code as follows:

1.  // As an option
2.  <script>
3.  import { reactive } from 'vue'
4.  export default {
5.  setup () {
6.  const state = reactive({state: 0})
7.  const func = () => { console.log('this functions output') }
8.  return {
9.  state,
10.  func
11.  }
12.  },
13.  created(() => {
14.  // code to execute on created hook
15.  })
16.  }
17.  </script>

How the setup method is accessed depends on how the component is being constructed, but when building SFCs, the framework provides a convenience setup attribute for the script tag. All code required to set up a component is placed in the <script setup> section of the component definition; you treat this as a normal script tag, but you do have the option of adding a further un-annotated script tag to handle third-party libraries or non-Composition API based code as can be seen in the code below:

1.  // In <script setup> block
2.  <script setup>
3.  import { reactive, onCreated } from 'vue'
4.  const state = reactive({state: 0})
5.  const func = () => { console.log('this functions output') }
6.  onCreated(() => {
7.  // code to execute on created hook
8.  })
9.  </script>

11.  <script>
12.  // code to execute outside of the Composition API
13.  </script>

Comparing these examples, you should have noticed that when using the setup() hook, you need to return an object that contains or rather exposes some or all the properties and functions needed to power the component template. When using <script setup>, this is handled transparently for you; this is due to the additional build step required in transpiling an SFC into the underlying object structure.

All the life cycle hooks that are available to you as part of the Options API are still available, but in a slightly different form; they all need to be specified in the setup() function or <script setup> as callbacks. The callbacks themselves will be outlined a little later as a reminder, but they are, by and large, semantically the same as Options API life cycle hooks as shown in the following listing:

1.  <script setup lang="ts">
2.  import { ref, onCreated, onMounted, onUpdated } from 'vue'

4.  const state = ref(0)

6.  onCreated(() => {
7.  // code to execute on created hook
8.  })

10.  onMounted(() => {
11.  // code to execute on mounted hook
12.  })

14.  onUpdated(() => {
15.  // code to execute on updated hook
16.  })
17.  </script>

Additionally, because the setup() step is run synchronously ahead of the beforeCreate() hook, there is no access to the this variable. To make the component state (component internal data) available to the template compiler, the Composition API (via the exposed Reactivity API) provides two functions: reactive() and ref().

[reactive()](#contents.xhtml_sc3_155a)

The reactive() function allows us to create a JS proxy around an object, which, in turn, allows Vue to track the internals of the wrapped object. reactive() only operates over object types, not primitives. The listing below demonstrates this:

1.  <script setup>
2.  import { reactive } from 'vue'

4.  const value = reactive({ key: 'value' })

6.  function mutateValue (newValue) {
7.  value.key = newValue
8.  }
9.  </script>

When the reactive state is mutated, the DOM is automatically updated. As with other DOM updates, Vue buffers the changes instead of applying them synchronously (i.e., at the time of the change in question). The buffer is cleared at the next tick event to ensure that the components are only updated once, irrespective of the number of state changes buffered.

State in Vue is deeply reactive, meaning that mutations are tracked even if they occur in a nested object (including arrays), as below:

1.  <script setup>
2.  import { reactive } from 'vue'

4.  const obj = reactive({
5.  parent: { child: { count: 0 } },
6.  greekLetterNames: ['alpha', 'beta']
7.  })

9.  function deepMutation() {
10.  // these will work as expected.
11.  obj.parent.child.count++
12.  obj. greekLetterNames.push('gamma')
13.  }
14.  </script>

However, any attempt to assign or destructure the reactive object into local variables results in breaking the connection to the reactivity in the original declared state object.

If you find yourself requiring to manage state of primitives or to address the issues with reactive(), Vue provides a ref() function, which will be discussed next.

[ref()](#contents.xhtml_sc3_156a)

ref() also creates reactive state, but in slightly different way. ref() wraps the value provided in an object that has a value property. These are reactive references to the underlying value as shown below:

1.  <script setup>
2.  import { ref } from 'vue'

4.  // primitive value wrapping
5.  // myValue = { value: 0 }
6.  const myValue = ref(0)

8.  // object value wrapping
9.  // myObject = { value: { obj: 0 } }
10.  const myObject = ref({ obj: 0 })
11.  </script>

Wrapping and unwrapping the data is handled automatically, but only if the property being accessed is a top-level property – i.e., within a template, as below:

1.  // this doesn't work as expected
2.  <script setup lang="ts">
3.  import { ref } from 'vue'

5.  const myObject = { prop1: ref(1) }
6.  </script>
7.  <template>
8.  <div>{{ myObject.prop1++ }}</div>
9.  </template>

11.  // this is correct
12.  <script setup lang="ts">
13.  import { ref } from 'vue'

15.  const myObject = { prop1: ref(1) }
16.  const { prop1 } = myObject
17.  </script>
18.  <template>
19.  <div>{{ prop1++ }}</div>
20.  </template>

Values in objects wrapped with ref() remain reactive when destructured or passed into function calls, see below:

21.  <script setup lang="ts">
22.  const myObject = {
23.  prop1: ref(1),
24.  prop2: ref(2)
25.  }

27.  // the function still needs to access the value by .value
28.  // because its a ref(), but it will retain the 
29.  //reactivity connection
30.  callFunction(myObject.prop1)

32.  // still reactive
33.  const { prop2 } = myObject
34.  </script>

When unwrapping a ref() in a template, there is no need to access the .value directly; it happens automatically. See the template section in the following listing:

1.  <script setup lang="ts">
2.  import { ref } from 'vue'
3.  const counter = ref(0)

5.  function incrementCounter() {
6.  counter.value++
7.  }
8.  </script>

10.  <template>
11.  <button @click="incrementCounter">
12.  {{ counter }}
13.  </button>
14.  </template>

As mentioned earlier, when using <script setup>, as in the previous code samples, functions and reactive data are automatically exposed to the template and are actively tracked for changes via a Proxy object.

[Composition API Life cycle Hooks](#contents.xhtml_sc3_157a)

The following is a brief reminder of the available life cycle hooks.

The setup() hook (or <script setup> block) will be the most commonly used hook when using Composition API; it will do all the setup work that you would have put into different life cycle hooks: create references to state, functions, event listeners and life cycle callbacks.

We've already covered reactive and ref.

The following is a small example of using setup(). We've seen this earlier and will be using it throughout the sample application build, so you'll get plenty of practice:

1.  <script setup lang="ts">
2.  import {
3.  ref,
4.  onCreated,
5.  onMounted,
6.  onUpdated,
7.  onBeforeCreate,
8.  onBeforeMount,
9.  onBeforeUpdate,
10.  onBeforeUnmount,
11.  onUnmounted,
12.  } from 'vue'
13.  const state = ref(0)

15.  onBeforeCreate(() => {})
16.  onCreated(() => {})
17.  onBeforeMount(() => {})
18.  onMounted(() => {})
19.  onBeforeUpdate(() => {})
20.  onUpdated(() => {})
21.  onBeforeUnmount(() => {})
22.  onUnmounted(() => {})
23.  </script>

Each of the Options API life cycle methods has a Composition API counterpart, which is presented in the following table:

| Composition API life cycle callback | Options API counterpart |
| --- | --- |
| onBeforeCreate(callback: () => void): void | beforeCreate |
| onCreated(callback: () => void): void | created |
| onBeforeMount(callback: () => void): void | beforeMount |
| onMounted(callback: () => void): void | mounted |
| onBeforeUpdate(callback: () => void): void | beforeUpdate |
| onUpdated(callback: () => void): void | updated |
| onBeforeUnmount(callback: () => void): void | beforeUnmount |
| onUnmounted(callback: () => void): void | unmounted |

Table 6.1: Comparing Composition API to Options API life cycle methods

As we already know how use the Options API life cycle methods, the Composition API callbacks are not really all that different.

[Data Flow between Composition API components](#contents.xhtml_sc3_158a)

So far, we haven't explored how to pass data between components built with the Composition API. In most cases, what we've discussed for the Options API holds true, but as we are not working with an options object but <script setup> in most cases, setting up the data flow elements between components is a little different.

We'll start by looking at how to set up (declare) props as they require explicit declaration.

[Props](#contents.xhtml_sc3_159a)

When declaring props with <script setup>, the defineProps() macro is used. The value passed into the macro is the same as you would provide the props option with.

1.  // simple props setup
2.  <script setup lang="ts">
3.  defineProps(['prop1', 'prop2'])
4.  </script>

6.  // props set up with validation
7.  <script setup lang="ts">
8.  defineProps({
9.  // Basic type check
10.  prop1: Number,

12.  // Multiple possible types
13.  prop2: [String, Number],

15.  // Required string
16.  prop3: {
17.  type: String,
18.  required: true
19.  },

21.  // Number with a default value
22.  prop4: {
23.  type: Number,
24.  default: 100
25.  },

27.  // Object with a default value
28.  prop5: {
29.  type: Object,
30.  // Object/array defaults need to be 
    returned from a factory function
31.  default() {
32.  return { message: 'hello' }
33.  }
34.  },

36.  // Custom type based on class
37.  prop6: {
38.  type: CustomClassType
39.  }
40.  })
41.  </script>

The rules governing the declaration of props with defineProps() is the same as if they were declared in the Options API props option.

When using TS, we can also define props in terms of TS types; the syntax for doing so is slightly different, as demonstrated here using defineProps<{}>():

1.  <script setup lang="ts">
2.  defineProps<{
3.  // validate as a number
4.  prop1: number,
5.  // validate as maybe a string
6.  prop2?: string
7.  }>()
8.  </script>

When using TS, defineProp() can take either an object literal, as shown earlier, or a reference to an interface or object literal given in the same file:

1.  <script setup lang="ts">
2.  interface Props {
3.  // validate as a number
4.  prop1: number,
5.  // validate as maybe a string
6.  prop2?: string
7.  }

9.  defineProps<Props>()
10.  </script>

Unfortunately, this does not mean that you can import interfaces or object literals from other files due to the way that components are compiled – the compiler does not currently check imported files for source types, and the component itself is compiled in isolation.

There is one caveat when using the type-only defineProp with TS is that you lose the ability to provide default values when creating props. Vue supplies a withDefaults macro to help with this issue; using it is detailed in the following example:

1.  <script setup lang="ts">
2.  interface Props {
3.  prop1: number
4.  prop2?: string
5.  }

7.  const props = withDefaults(defineProps<{Props}>(), {
8.  prop1: 0,
9.  prop2: 'A string'
10.  })
11.  </script>

Passing data to the template remains the same. Props are automatically made available to the template renderer.

[Data](#contents.xhtml_sc3_160a)

It is not directly part of the data flow between components, but it is important to note that while the option is available to Composition API components in the same way as for Options API with the data() function, it's better to use reactive state through the <script setup> and reactive()/ref() functions.

[Events](#contents.xhtml_sc3_161a)

Adding events to the HTML DOM is the same, regardless of whether it's an Options API or Composition API; this is the template after all.

Defining the event handlers in Composition API components uses the defineEvents() macro. Like defineProps(), defineEvents() can take a list of strings or an object.

1.  // defining event handers as functions
2.  <script setup lang="ts">
3.  defineEvents(['event_1', 'event_2'])

5.  function event_1 (evt) { ... }

7.  function event_2 (evt) { ... }
8.  </script>

10.  // defining event handlers as objects
11.  <script setup lang="ts">
12.  defineEvents({
13.  event_1 (evt) { ... },

15.  event_2 (evt) { ... }
16.  })
17.  </script>

19.  // defining event handlers as type-based
20.  <script setup lang="ts">
21.  defineEvents<{
22.  (e: 'event_1', value: number): void
23.  (e: 'event_2', value: string): void
24.  }>()
25.  </script>

Even though it is possible to just create the event handlers, they are just plain functions after all, it's best to define them through defineEvents() to prevent an attribute fall through issue.

[Computed properties](#contents.xhtml_sc3_162a)

Computed properties are created using the computed() function, which takes a callback to perform the computation. Usually computed properties are read-only, but you'll need to create getters and setters to make a computed property mutable:

1.  // computing a simple value
2.  <script setup lang="ts">
3.  import { computed, ref } from 'vue'
4.  const price = ref(29.99)
5.  const asPrice = computed(() => {
6.  return `£ ${price.value.toFixed(2)}`
7.  })
8.  </script>

10.  // making computed value writeable
11.  <script setup lang="ts">
12.  import { computed, ref } from 'vue'
13.  const price = ref(0)

15.  const asPrice = computed({
16.  get() {
17.  return `£ ${price.value.toFixed(2)}`
18.  },
19.  set(newPrice) {
20.  price.value = newPrice
21.  }
22.  })
23.  </script>

When working in TS, the return type is inferred. If you need to specify a return type, it can be achieved with a generic argument; in the following example, the return value is marked as a string:

1.  // setting return type
2.  <script setup lang="ts">
3.  import { computed, ref } from 'vue'
4.  const price = ref(29.99)
5.  const asPrice = computed<string>(() => {
6.  return `£ ${price.value.toFixed(2)}`
7.  })
8.  </script>

[Watchers](#contents.xhtml_sc3_163a)

Working with watchers in Composition API is as simple as working with computed properties.

With a watcher, you need to define to arguments, the value you want to watch, and what you want to happen when the value changes.

The function supplied to the watcher can be used to perform side effects, as given below:

1.  <script setup lang="ts">
2.  import { ref, watch } from 'vue'

4.  const data: Ref<T> = ref({} as T);
5.  const { watchedValue } = <remote data fetch>

7.  watch(watchedValue, value => {
8.  data.value = value?.getValue();
9.  });

11.  </script>

[Template Refs](#contents.xhtml_sc3_164a)

Creating references to template elements takes a little bit of thought.

Firstly, we'll use the special ref attribute in the template to mark which element to track:

1.  <template>
2.  <div ref="templateRef">Div Content</div>
3.  </template>

The next part is to create the reference in <script setup> so that we can access the template element. To do this, we use the ref() function from Vue and give it the same name as that given to the element ref in the template. This can only be done in life cycle hooks that operate after the component has been mounted, otherwise it will return null:

1.  <script setup lang="ts">
2.  import { ref, onMounted } from 'vue'

4.  // this is the same name as that given in the template
5.  const templateRef = ref(null)

7.  onMounted(() => {
8.  templateRef.value.innerHTML = '<p>New content</p>'
9.  })
10.  </script>

[Fall-through attributes](#contents.xhtml_sc3_165a)

Fall-through attributes are those that are passed to a child component but are not explicitly declared as a prop or emit; common ones are class, style, id attributes and event listeners. These attributes are passed into the child components rendered DOM.

When class and style attributes fall through, they are automatically merged in the output DOM:

1.  <!--  SubmitComponent template -->
2.  <input type="submit" class="btn-lg">Save</input>

4.  <!-- Using the component in parent -->
5.  <SubmitComponent class="bg-blue-400 text-white" />
6.  <!-- rendered output DOM -->
7.  <input type="submit" class="btn-lg bg-blue-400 text-white">Save</input>

There are some caveats when looking to bind fall-through attributes to a template that has multiple root nodes, the main one being that they need explicitly binding with v-bind.

Accessing the component attributes in JavaScript is facilitated by the useAttrs() function in the following manner:

1.  <script setup>
2.  import { useAttrs } from 'vue'

4.  const attrs = useAttrs()
5.  </script>

[Creating Composable utilities](#contents.xhtml_sc2_166a)

The biggest issue with using setup() is that it holds pretty much all the code that controls the components functionality, so when it comes to components that need to manage more than a few types of state, this function can become very large.

The whole point of moving toward this type of API is to put all the functionality that manages a particular concern into a single place and be able to reuse it across the application. This can't happen if all the code is placed into the setup() function.

Due to the nature of the Composition API (as it uses standard JS plain functions) it becomes possible to compose component functionality by abstracting this functionality into “utilities”. By convention, the names for these utilities are prefixed with use, i.e., useRef(), useCallback(), etc.

Extracting code such as this allows us to create what is called a Composable – a set of functionalities that relates to a particular concern that can be imported into a component and used as though it was part of the component.

The following code listings demonstrate how to extract some simple functionality into a Composable and import it ready for use.

Suppose we're building a component that needs to fetch its own data; for this, we'll use the Fetch API. For this simple example, we have the following component:

1.  <script setup lang="ts">
2.  import { ref } from 'vue'

4.  const resp = ref(null)
5.  const err = ref(null)

7.  fetch('http://www.example.com')
8.  .then( res => res.json() )
9.  .then( json => { data.value = json } )
10.  .catch( e => { err.value = e } )
11.  </script>
12.  <template>
13.  <div v-if="error">{{ err.message }} Encountered</div>
14.  <div v-else-if="data">
15.  Response received: <pre>{{ resp }}</pre>
16.  </div>
17.  <div v-else>Awaiting Response</div>
18.  </template>

This type of boilerplate is not code that we want to write into each component that needs to pull its own data; what we're after is something we can call, which we provide some data for and then it performs the operation; the whole point is that we are creating something that we can reuse across the codebase, or even better, from project to project.

The way to work with this is to extract the functional parts into a use* function; in this case, it makes sense to call it  useFetch(). We create a file with an exported named function:

1.  // useFetch.js
2.  import { ref } from 'vue'

4.  export function useFetch(url) {
5.  const resp = ref(null)
6.  const err = ref(null)

8.  fetch(url)
9.  .then( res => res.json() )
10.  .then( json => { data.value = json } )
11.  .catch( e => { err.value = e } )

13.  return { resp, err }
14.  }

Making this change means we can reduce the code in the component to the following:

1.  <script setup lang="ts">
2.  import { useFetch } from './useFetch.js'

4.  const { resp, err } = useFetch('http://www.example.com')
5.  </script>

This is a simple example, which can be expanded; the obvious is that this particular Composable example only fetches on setup and doesn't watch for changes in the URL to perform the request again.

Not only are Composables useful for extracting and reusing functionality, they are also useful for organizing code. The possibilities afforded to Composition API components mean that all the functionality can be extracted into smaller functions or Composables. Composables are formed along lines of logical concern and imported, as needed, to aid readability, navigability, and the ability to reason about the code.

Because the concept of being able to share and reuse dedicated functionality is pervasive in the industry (why reinvent the wheel when you can borrow one that's already been made) a growing library of utilities, VueUse, is available as a central repository or distribution hub to handle different concerns encountered by the community. We will look at this next.

[VueUse – Composition API utilities library](#contents.xhtml_sc2_167a)

VueUse documentation can be found at [https://github.com/vueuse/vueuse](https://github.com/vueuse/vueuse).

Introducing Vue Use into a project is the same as any other NPM package:

1.  $ npm i @vueuse/core

With this added, any of the utilities can be imported through the usual channel of setup(). Consider this example:

1.  <script setup lang="ts">
2.  import { useStorage } from '@vueuse/core'

4.  const state = useStorage('storageKey', {})
5.  </script>

It is recommended that you take a good look at the 200+ utilities provided by VueUse; there's most likely something in there that can make your life easier in any project.

[Handling Dependency Injection - Provide and Inject](#contents.xhtml_sc2_168a)

We've already seen how to use Provide and Inject in an Options API setting in [Chapter 5](#ch05.xhtml), Designing Component-Based UIs and Single Page Applications, even though it's a Composition API addition to the framework.

The problem of “props drilling”, i.e., having to pass props down a component hierarchy so that a deeply nest child has access to data from a root parent, is extremely brittle. It means we must maintain the data being passed throughout the hierarchy, even if the intermediary components have no use for it, essentially widening the scope of all the intermediaries, making them aware of data they don't need.

Using provide/inject with Composition API is simpler than with the Options API; you use the provide() and inject() functions in the setup() function.

We'll go over this with a brief example – first off, let's set up a root parent component that provides some data:

1.  <script setup lang="ts">
2.  import { provide, ref } from 'vue'
3.  // providing some ref data from parent root
4.  const value = ref('value')
5.  provide('key', value)
6.  </script>

This is setting up a value that can be pulled in any of the child components using the ‘key' value, regardless of how deeply nested it is.

A deeply nested child, say great-grandchild of the about root parent, needs the data provided by that parent; this requires inject():

1.  <script setup lang="ts">
2.  import { inject } from 'vue'

4.  // injecting the ref data from parent root
5.  const value = inject('key', 'default value')
6.  </script>

The optional default value in the inject() function can be any type, including a factory function over an expensive operation (in case the operation is not needed).

If you're ever in a position where you need to mutate a provided value, it's best to provide a mutating function from the parent root component. This way, the data and the mutating operation are kept together, which improves maintenance experience and removes the requirement to create duplicate code across the component code bases. There are great examples in the Vue.js documentation, which you can find at [https://vuejs.org/guide/components/provide-inject.html](https://vuejs.org/guide/components/provide-inject.html).

What we didn't discuss so far is that the provide key can either be a string or a Symbol. It makes sense to use Symbols as provide keys when your project relies on large numbers of providers or if you're supplying components to other developers; you want to make sure the keys don't collide.

The best way to accomplish this is to create a dedicated file that exports all the Symbol keys and import them where required. Since Symbols are unique values across the project, collisions are avoided.

Having a dedicated file also allows maintainers of components to easily see which keys are available across a project, without having to be aware of all the components that require them.

Using a dedicated Symbols file for providers and injectors works as shown in the following examples:

1.  // keys.ts
2.  export const mySymbolKey1 = Symbol()
3.  export const mySymbolKey2 = Symbol()

The required keys are then imported into the provider component for setting the data and the injector component file retrieval, like below:

1.  // provider component
2.  <script setup lang="ts">
3.  import { provide, ref } from 'vue'
4.  import { mySymbolKey1, mySymbolKey2 } from './keys.ts'

6.  provide(mySymbolKey1, 'value')
7.  provide(mySymbolKey2, ref({}))
8.  </script>

10.  // first injector component
11.  <script setup lang="ts">
12.  import { inject } from 'vue'
13.  import { mySymbolKey1 } from './keys.ts'

15.  const providedValue = inject(mySymbolKey1)
16.  </script>

18.  // second injector component
19.  <script setup lang="ts">
20.  import { inject } from 'vue'
21.  import { mySymbolKey2 } from './keys.ts'

23.  const providedValue = inject(mySymbolKey2)
24.  </script>

As with all things, be judicious in your usage of this technique. Being overly reliant on providers can be seen as an anti-pattern, especially if your component tree is very shallow.

[Using Teleport and Suspense](#contents.xhtml_sc2_169a)

There are occasions in any project where you will find that logically, a particular component in your hierarchy should handle some concern/data/display. However, that component is deeply nested in the HTML tree, but the HTML output of this component needs to be attached to a different part of the HTML to display correctly.

This is where Teleport comes in. In short, Teleport allows us to attach a part of a components template to a DOM node that is present outside that components DOM tree.

Suspense handles a different issue but is still related to operating over a section of the HTML DOM tree. With Suspense, you can orchestrate several async dependencies in the HTML hierarchy without each of these components handling their own loading/error states. With Suspense, you can avoid having multiple spinners on the page and have the content delivered to the user at different intervals as it arrives. Suspense allows this to be managed from a top-level component; this built-in component will be discussed further in the chapter.

[Teleport](#contents.xhtml_sc3_170a)

Teleport is a built-in component that is used to wrap any part of a component's HTML tree that needs to be attached elsewhere in the page DOM.

This description seems a little vague, so an example will probably help.

To start off, we'll set up the component tag in a parent:

1.  <div class="...">
2.  <div><!-- component inner content --></div>
3.  <div>
4.  <FullScreenModal />
5.  </div>
6.  </div>
7.  From here, the internals look as follows:
8.  <template>
9.  <div v-if="isOpen" class="...">
10.  <div><!-- modal content area --></div>
11.  <div><button @click="toggleModal">Close</button></div>
12.  </div>

14.  <button @click="toggleModal">Open</button>
15.  </template>

17.  <script setup lang="ts">
18.  import { ref } from 'vue'

20.  const _isOpen = ref(false)

22.  const toggleModal = () => {
23.  _isOpen.value = !_isOpen.value
24.  }
25.  </script>

27.  <style scoped>
28.  /* style rules omitted for space */
29.  </style>

Some of the issues here, although not obvious, are CSS related. For this component to render correctly from its deeply nested position takes some CSS gymnastics. To avoid several potential issues, we can use Teleport to attach the HTML to another part of the DOM at render time.

To alter the <FullScreenModal> component to use <Teleport>, we just wrap the parts we need with the <Teleport> tags, as follows:

1.  <template>
2.  <Teleport to="body">
3.  <div v-if="isOpen" class="...">
4.  <div><!-- modal content area --></div>
5.  <div>
6.  <button @click="toggleModal">Close</button>
7.  </div>
8.  </div>
9.  </Teleport>

11.  <button @click="toggleModal">Open</button>
12.  </template>

Everything else remains the same. The to attribute is used to target real DOM elements or CSS selectors. Combining <Teleport> with <Transition> allows you to make impressive, animated modals with very little work.

[Suspense](#contents.xhtml_sc3_171a)

The Suspense component has been built to wait upon two types of async child components: those with an asynchronous setup() hook and async components.

Async setup() hooks can be defined in two ways.

The first way is with an async setup() function:

1.  <script>
2.  export default {
3.  async setup() {
4.  const resp = await fetch(<remote URL>)
5.  const data = await resp.json()

7.  return { data }
8.  }
9.  }
10.  </script>

The second is with a top-level await expression in a <script setup>, which hoists the component automatically to an async dependency, as follows:

1.  <script setup>
2.  const resp = await fetch(<remote URL>)
3.  const data = await resp.json()
4.  </script>

When using Suspense, you have a component that provides two slots: #default (the default slot) and #fallback (to handle the loading state).

Each of these slots will only allow a single direct child node, either a component (which is directly async or has one or more children that are async) or a wrapper node that contains one or more async components.

The Suspense component attempts to display the content in the default slot if possible; the component will render the content in the fallback slot if not.

Either way, the Suspense component will render the default content in memory and enter a pending state if any async dependencies are encountered. While in a pending state, any async calls will be resolved and the fallback content displayed.

When all async dependencies are resolved, the Suspense component enters a resolved state and the content in the default slot is displayed. This is also the case if there are no async dependencies in the component hierarchy.

Should the root node in the default slot be replaced, then the Suspense component will re-enter a pending state. This is the only case when this will happen. After entering pending state, the async dependencies will perform their respective concerns to obtain new content. The previous default content will continue to be displayed until new content is available. When the new content is received it is rendered out to the user. If an error state or timeout is encountered, the fallback content is displayed.

If an error is encountered by one of the async dependencies, you will need to use either the errorCaptured option (Options API) or the onErrorCaptured() hook (Composition API) to handle any errors returned in the parent of the Suspense component.

Each of the named states, i.e., pending, resolve and fallback, can be used to show loading indicators (spinners, progress bars, etc.) or other user experience enhancing feedback.

Using the Suspense component is the same as using any other:

1.  <template>
2.  <Suspense>
3.  <!-- this is the default slot -->
4.  <DefaultComponent />

6.  <!-- fallback template slot -->
7.  <template #fallback>
8.  <FallbackComponent />
9.  </template>
10.  </Suspense>
11.  </template>

When working with Suspense, you'll use <Transition> frequently, which we have not covered yet, and the <KeepAlive> and <RouterView> components. However, the nesting order of these components is important otherwise these components would not work together properly. If you follow the given pattern, the components should work as expected:

1.  <RouterView v-slot="{ Component }">
2.  <template v-if="Component">
3.  <Transition mode="mode">
4.  <KeepAlive>
5.  <Suspense>
6.  <!-- inject the Component dynamically -->
7.  <!-- this is the default slot -->
8.  <component :is="Component"></component>

10.  <!-- fallback template slot -->
11.  <template #fallback>
12.  <FallbackComponent />
13.  </template>
14.  </Suspense>
15.  </KeepAlive>
16.  </Transition>
17.  </template>
18.  </RouterView>

The Vue Router has support for lazy loading components; we'll cover Vue Router in [Chapter 10](#ch10.xhtml), Routing Between Pages Using Vue Router.

[Conclusion](#contents.xhtml_sc2_172a)

In this chapter, we explored the Composition API. We saw how and why it can be used to simplify our code around concerns and how this makes code around these concerns more maintainable.

We also covered how to create composable functionalities that aid reuse, i.e., small fragments of code that can be reused in multiple projects, which leads into being able to use and contribute to the VueUse library.

[Key terms](#contents.xhtml_sc2_173a)

*   Composition API
*   <script setup>
*   Reactivity
*   Dependency Injection
*   Flexibility
*   Composing
*   VueUse Library
*   Teleport
*   Suspense

Join our book’s Discord space

Join the book's Discord Workspace for Latest updates, Offers, Tech happenings around the world, New Release and Sessions with the Authors:

**[https://discord.bpbonline.com](https://discord.bpbonline.com)**

![](images/fm1.png)

# [CHAPTER 7Creating and Setting Up a Vue.js Application with Vue CLI and Vite](#contents.xhtml_ch07a)

[Introduction](#contents.xhtml_sc2_174a)

Starting with this chapter, you are going to be working through building the prototype application as discussed in [Chapter 5](#ch05.xhtml), Designing Component-Based UIs and Single Page Applications. Some of you might not be familiar with some of the tools required to make this or any successful project. This chapter is foundational to any project using Vue.js; in fact, some of the skills you will learn here will be foundational to many other projects, JavaScript-based or otherwise.

We'll firstly cover the Node Package Manager or NPM, and for those who haven't come across version management at all or using Git, we'll cover that too.

Lastly, we'll cover starting the project using the three available tools that are used across the industry for Vue.js projects.

So, let's start by covering the tools that you'll use for any JavaScript project: Git and NPM.

[Structure](#contents.xhtml_sc2_175a)

We'll be covering the following topics in this chapter:

*   Git
*   NPM
*   Vue CLI
*   Vue UI
*   Vite

[Objectives](#contents.xhtml_sc2_176a)

The objective of this chapter is to get you up to speed with standard tools that you'll come across in the industry.

If you are familiar with Git and/or NPM, you can safely skim those parts of this chapter.

Familiarity with setting up Vue.js projects is important. Even if you're aware of some of these methods, it's always worthwhile reminding yourself of them.

[Git and NPM primer](#contents.xhtml_sc2_177a)

In this section, we will cover the foundational tools of Git and NPM. Git is one of the few ubiquitous tools that the industry uses, and you will use it in many projects regardless of technology. NPM is one of a handful of package managers you might come across. Others are Yarn and pnpm. We will be using NPM as it is a standard tool that is installed when you install Node, so it's already available rather than being an extra third-party tool that you need to install on top of Node.

[Git Primer](#contents.xhtml_sc3_178a)

Git is the most widely available and popular tool of a set of tools called Distributed Version Control Systems or DVCS.

These tools allow a team to manage a central repository to store the application code and associated materials in an easy to access way, where each team member can obtain a copy of the code to make changes and then share these changes across the team.

With DVCS, teams can monitor changes and perform quality and sanity checks before the integration of the changes into the main codebase.

Git is easily installed using your operating systems package manager or using an OS-specific binary as can be found on [https://git-scm.com/downloads](https://git-scm.com/downloads).

There are many visual tools available that can help you work with Git: GitKraken, SourceTree, TortiseGit, git-gui, and gitk; you can find a comprehensive list at [https://git-scm.com/downloads/guis](https://git-scm.com/downloads/guis). We'll, however, be using the CLI through your local, friendly terminal – using the GUIs might seem like an easier way of working with Git, but without understanding what the tools are doing under the hood, you'll find it difficult to rectify issues.

In order to follow along, you can check out the code from <code repo>, which we'll use as the core repository for the code that you'll be following with. The code that accompanies this book will have a before and after so that you can build the application using the listings given in the book, or just jump ahead to the final code listings and read along. To learn how to work with Vue.js properly, it is recommended that you use the starter branch and code along.

Bear in mind that this is just a primer; there is a full set of documentation at [https://git-scm.com/docs](https://git-scm.com/docs) that provides a lot more detail than there is room for here.

[Basic terminology](#contents.xhtml_sc3_179a)

In this section, we'll cover basic terms that you'll use when using Git, with examples of how to use them on the command line:

SHA

SHA is a reference to a point in the branch history. Each SHA is unique in the repo and is 32-bit long.

Branch

A branch is the thing that holds what your project is; it's the code files, documentation, assets, whatever else you need. A branch is the basic unit in Git. Branches exist either remotely or locally, and each is a copy of the branch that was used as a basis, plus the changes that were made. Branches can be created, checked out, committed to, pulled, pushed, and merged. Apart from the code contained on a branch, each branch holds a record of all the changes that were made; this is called the branch history and is fundamental to how Git works. Branches have names, which you assign when you create the branch. Usually, the primary/first branch is called master or main. Depending on which branching strategy your company/team uses, you may also have secondary branches with names like development, feature, integration, release, bug, and hot fix. Examples of which are given in the following listing:

1.  # create a branch from the current branch
2.  # git branch <source-branch> <new-branch>
3.  $ git branch master new-branch 

5.  # Change to new branch
6.  $ git switch new-branch

8.  # delete a branch - after merge
9.  $ git branch -d new-branch 

11.  # force delete a branch
12.  $ git branch -D new-branch

Listing the branches is done using the --list switch, as follows:

13.  # list local branches
14.  $ git branch --list

16.  #list remote branches
17.  $ git branch --list --remote

Sometimes a branch needs to be renamed, and this is done with the -m option:

1.  # rename local branch
2.  $ git branch -m renamed-branch

Repository

A repository (repo) is where branches and therefore, the project files, reside. Repos are usually, but not necessarily, held in a remote location; this can be at a repository host like GitHub or BitBucket, a private hosted server at your company network (on prem), or locally on your machine. Because of the distributed nature of Git, using a remote host is best, and the remote is, usually, viewed as the absolute source of truth.

Setting up a local repository is relatively simple:

1.  # initialise the repo
2.  $ git init

4.  # If you want to add the existing code
5.  # in the current directory
6.  $ git add .
7.  $ git commit

Setting up a remote one is more involved. Most companies tend to use a remote hosting service like GitHub or BitBucket to hold their code.

Remote (Origin)

The remote is (usually but not required to be) called origin. It is just a name that is an alias of a web address to make it easier to remember. The origin is the place where you cloned or pulled your code from and a location that is the default push target. However, with all things, it can be repointed; Git allows you to do this quite easily. You can also have multiple remote endpoints for code distribution, but in general you only need or use the one called origin.

1.  # listing
2.  $ git list --remote

4.  # adding a remote
5.  $ git remote add branch-name

7.  # changing the remote URL
8.  $ git remote set-url new-url

All these commands change the settings in your local git config file:

1.  # edit config file
2.  $ git config -e

4.  # open editor
5.  [core]
6.  repositoryformatversion = 0
7.  filemode = true
8.  bare = false
9.  logallrefupdates = true
10.  ignorecase = true
11.  precomposeunicode = true
12.  [remote "origin"]
13.  url = git@remote-url/branch.git
14.  fetch = +refs/heads/*:refs/remotes/origin/*
15.  [branch "master"]
16.  remote = origin
17.  merge = refs/heads/master
18.  [pull]
19.  rebase = false
20.  [remote "heroku"]
21.  url = https://git.heroku.com/branch.git
22.  fetch = +refs/heads/*:refs/remotes/heroku/*
23.  [branch "new-branch"]
24.  remote = origin
25.  merge = refs/heads/new-branch

You can change these by hand but be warned that if you don't know what you're doing here, you could end up breaking your access to the remote, which is not something that is recommended.

Local

Your local is exactly that, where you are locally editing code. Usually, this is your local development environment, but it could be a remote development service, like Eclipse Che.

Clone

Cloning refers to creating a reference to a remote repository and branch, making a copy of all the code in that remote branch, and downloading it to the locally specified location, i.e., your local. Once the repository has been cloned, you can checkout or create a working branch.

To clone, you issue a command as follows:

1.  # cloning a remote branch
2.  $ git clone http://repo.com/path/to/repo branch-name

Checkout/Switch

When you check out, you're primarily switching between branches, but the checkout command can also be used to create a new local branch and then switch to it.

To just change branches, you issue the following:

1.  # switching to a branch (new - experimental)
2.  $ git switch branch-name

4.  # checkout a branch
5.  $ git checkout branch-name

To create a new branch from your currently checked out branch and switch to it, issue the following:

1.  # create and switch to new branch (new -experimental)
2.  $ git switch -c branch-name

4.  # Or
5.  $ git checkout -b branch-name

7.  # Checkout previous branch
8.  $ git checkout -

The main difference between switch and checkout (apart from switch being experimental and therefore, its possibility of changing behavior) is that switch does not require a clean index and working tree, but it will abort if switching leads to loss of local changes.

Fetch

When you fetch, what you're doing is pulling a copy of the branch history rather than the branch change so that you can tell if there are changes that need to be pulled or pushed, as shown in the following:

1.  # fetch all histories from the origin
2.  $ git fetch

4.  # Or a specific branch
5.  $ git fetch git://path/to/repo/branch.git

Pull

When you pull code from the remote, you get a copy of the branch history, if not up to date, and a patch of all the code changes that need to be applied locally in order to bring the branch up to date with the remote changes, see below:

1.  # pull changes from remote branch
2.  $ git pull origin branch-name

When you're in a team with multiple people all wanting to apply code to the same remote branch, you will often need to pull before you can push.

Commit

Committing means to apply your locally made, uncommitted changes, to the local branch, see the following examples:

1.  # add all local changes to working branch history
2.  $ git add .

4.  # commit the code and open an
5.  # editor window to add a commit comment
6.  $ git commit 

8.  # commit only add changes to tracked files
9.  # opens an editor window
10.  $ git commit -a

12.  # commit with message from command line
13.  $ git commit -m 'Message here'

15.  # add, commit and include a message
16.  $ git commit -am 'Message here'

This command updates the local branch history. This is a precursor to pushing your code changes to the remote branch for checking and distribution.

Merge

When you merge, you apply the code changes from one branch to another locally, merging the branch histories:

1.  # merge code from a named branch
2.  $ git merge prev-branch

4.  # merge code from previously checked out branch
5.  $ git merge -

Sometimes, if there's multiple changes in the same code file location, merging can cause conflicts – code conflicts on a branch need to be resolved before being able to continue either with a merge, if there are many files in the merge, or before a push to a remote.

Push

Pushing moves the remote branch history in line with your local history and sends a patch file up to the remote with your local code changes; it merges your local code into the remote branch of the same name., as below:

1.  # push code to remote - origin
2.  $ git push origin branch-name

Branch histories on the remote can then be managed independently so that code quality checks, remote testing, building and integrations can happen, if your company does such things.

Conflict

A conflict arises when there are differing histories for the same lines of code from different localities. Conflicts need to be resolved, which can be done in one of three ways:

*   Accepting the remote changes, overwriting your local ones
*   Ignoring the remote changes and using your local changes
*   Combine the remote and local changes into a hybrid change

Working through conflicts can be challenging if the amount or scope of the change is large. It's always best to try to limit the size/scope of changes required and commit/push/pull often. Companies will often have internal strategies to minimise conflicts. From experience, some work well and some don't.

Find a merge tool that you are comfortable with; the author favors VIM for this task, others Nano or Emacs, but there are tools built into most IDEs and code editors to help with this task.

Stash

When you stash your code changes, you temporarily wind back the local change history to when the branch was created and hold it separately, as in the code below:

1.  # stash the code and rewind the working branch
2.  $ git stash

4.  # list the elements in the stash
5.  $ git stash list

7.  # pull the last stashed code
8.  $ git stash pop

Stashing is most useful when you need to pull code from remote, but you're aware that there might be a resulting conflict and need to protect your changes that you can apply in a controlled manner after the pull/merge.

Diff

Diffs allow you to compare code changes between branches, both locally and remote, or different states of a branch. Various ways of using diff given in the listing:

1.  # diff the changes made against HEAD on current branch
2.  $ git diff

4.  # diff current branch against a different branch
5.  $ git diff branch-1 branch-2

Being able to view the diffs allows you to see if/where a code change might cause a conflict, or if there's a breaking change and you need to pin it down.

When reading a diff or any description of a change, a + symbol (usually on a green line) shows an addition on that line and a – symbol (usually on a red line) shows a deletion on that line. A line without a change is usually shown in grey.

Patch

A patch exports a diff into a file. The file can then be sent around as required. Creating patches isn't usually required. Pushing/pulling and merging is the most effective and easily manageable way of moving code about.

Rebase

Sometimes you need to rewrite the branch history, merging multiple commits into a single one, or you need to selectively manipulate/reorder the commits; for this, you need rebase.

Rebase is a power tool that takes a bit of practice to learn to use properly. With great power comes great responsibility; as you are rewriting history, it's easy to lose changes if care is not taken.

Cherry-pick

As the name suggests, cherry-picking means you select the commits from the branch you need them from and merge their respective histories into the current branch. This is, again, a power tool that should not be used lightly.

[NPM Primer](#contents.xhtml_sc2_180a)

The Node Package Manager is just that, a package manager. Mostly, your interaction with it will be to add packages to your project or to update them. Sometimes, you'll use it to start a project. Unless you're a package maintainer, that's pretty much all you'll use it for.

Initialising a project

There are many ways of starting a JavaScript/TypeScript project. Even with Vue.js, there are at least three ways of doing the same thing. Different front-end ecosystems have their own ways of doing just that. Each of these though, at the very basic level, are just wrappers around package.json.

The package.json file is the core of any JS project as it defines the project dependencies, project meta data, scripts for running the project, and a start point.

Even without the ecosystem tools, creating a JS project is simple:

1.  npm init

Once this file has been created, you can start adding dependencies, metadata, and other elements to your project. The package.json file will be discussed as we move on.

Installing a new package

The simplest way to install a new package into your project is via npm i <package-name>. The i is the shortcut option for install. You can, by all means, write npm install <package-name>, but i is shorter.

This simple command updates the package.json file, adding a line that references the latest version of the named package, fetches that package and places it into the project local node_modules folder. It then reads that package.json file and does the same to all the dependencies named in that file, all the way down until all the dependencies are collated together under the node_modules directory. It also checks that the versions named in all the required packages are compatible; it gives warnings if not, and lets you know if you need to add anything else that your named package might require as a “peer dependency”. Lastly, it creates a package-lock.json file that holds all the same information but locks down the versions for when the project is deployed in other contexts. If there is a lock file in place, this will be preferred to ensure that the versions across deployments are as similar as possible within the confines of the versions provided. That's a lot of work saved by using such a small command. Its simplicity hides all these details.

If you find yourself in a situation where you need a version of a package that is different from the latest version, then the install command can be changed to include a specific version, like so: npm i <package-name>@<version>.

The npm i command also takes several different options. Not all packages that you will want to use are necessary or appropriate for production deployment; these include packages that you'll need for testing your code, or tools for building css from js and compiling. For these packages, you'll need to use the following:

1.  npm i --save-dev <package-name>

This performs the same install sequence as described earlier, but only in your local development. The reference to the package is also placed in a slightly different section of the package.json file to keep the production packages separate from packages that are only required in the development environment.

If you run the npm i command without any package names, it will check the local package.json file and install all the dependencies named in there. This allows you to make manual adjustments to the package.json file references and then run the command to reinstall all the packages. It's also not unknown to have to delete the node_modules directory and reinstall the dependencies.

One last thing to mention: Some packages might need to be installed globally, that is, outside of the projects' node_modules directory. This is because if it's a local build tool, testing package, formatter or executable, the list goes on, then it needs to be available system wide. To do this, you need to include the -g, for global, in the command. This switch installs the package (and its dependencies) in a system available location, on the system path, so that its accessible from the command terminal.

Updating an installed package

The NPM ecosystem has several tools to help manage package updates, but NPM itself uses npm outdated to pinpoint packages that need updating and provide information on how to do that.

One thing to bear in mind is that even though npm outdated flags a package for updating, that doesn't mean it should be updated. Many things come into play when updating, as the latest version might introduce incompatibilities or instabilities into your project. Some of this can be handled by manual or automated testing, but you will also need to build and run your project to test for instabilities and issues caused by the updated packages.

Again, with experience, you can manually update the package.json file to the package versions that you want to use and then run npm -i to install the updates.

Performing a package safety audit

As a professional developer, your primary concern, aside from building a functional product, should be to build a secure one.

Your Vue.js project is going to be delivered to users all over the world, some of whom might not have the intended functionality in mind. All the code, even if transpiled and sitting in node_modules, will be available to the browser and therefore, to the browser internal development tools. So, anybody can see what the code does or what data the web app might store locally in the browser. You should assume that all dependencies and any code written that communicates with external server resources (third-party or otherwise) is inherently insecure. This is just the nature of the beast.

The NPM provides a service that queries an online resource to determine whether any of the project dependencies have been flagged as insecure, dangerous, or incompatible in some way, and it provides suggestions on to how the issues can be resolved. In most cases, the fix is to update the package to the latest version, but in some cases, you need to be more diligent in how the insecure package is dealt with. Sometimes, Google is your friend.

To run a package safety audit issue the following command in your terminal:

1.  npm audit

This will return a list of any packages that have been flagged as having an issue.

In some cases, packages can be updated automatically; to do this, the following command can be used:

1.  npm audit --fix

Any packages that can't be updated like this will be flagged following the execution of this command and pointers to possible resolution will be provided.

Remember, don't trust your project dependencies or any third-party systems, your code, your production environment, or your users. All these are attack vectors can put your users or application data at risk.

The package.json file

The package.json file is the backbone of any JS/TS project. It is the place where all the project metadata is defined: project and development dependencies; execution and test scripts; keywords, NPM and project settings; and project entry point.

As it's a JSON file, it needs to be valid according to JSON validation rules.

There are plenty of details on all the options available to you at [https://docs.npmjs.com/cli/v8/configuring-npm/package-json](https://docs.npmjs.com/cli/v8/configuring-npm/package-json).

The main options where you will be doing the bulk of your changes to this file will be in the following sections:

*   scripts
*   config
*   dependencies
*   devDependencies
*   peerDependencies
*   engines

Other tools might also want to have data stored in the package.json file; typical ones are babel, typescript, postcss, prettier, and eslint.

There is plenty of detail on how to specify the dependency versioning in the above link, but it will be discussed in further detail later, when we need to make changes to the package.json file directly.

Now that we have all this information under our collective belts, we're ready to start creating the project as discussed in [Chapter 5](#ch05.xhtml), Designing Component-Based UIs and Single Page Applications. The first step will remind us how to create a project using each of the three main ways available to us. This will be a short reprise so that we might get on to more interesting work in [Chapter 8](#ch08.xhtml), Adding a CSS Framework to the Mix – TailwindCSS, Bootstrap or Foundation.

[Using the Vue CLI to create a project](#contents.xhtml_sc2_181a)

In this and the following two sections, we will create the basis of the project that we're going to build in the subsequent chapters, each one reprising a different method but still forming the required basis of the project.

It is up to you or your team to select the one that's more appropriate to use in your situation as each one produces slightly different results.

We will call the project speedy-pizza-e-commerce-prototype, which is self-explanatory. At this time, we will also set up the git tracking and remote hosting for the code.

At this point, we'll assume that you have installed the prerequisites to run the CLI.

Issue this command on your command line:

1.  $ vue create speedy-pizza-e-commerce-prototype

This will start the CLI wizard and show you the following:

1.  Vue CLI v5.0.1
2.  ? Please pick a preset: 
3.  standard-setup ([Vue 2] router, vuex, sass, babel, pwa, eslint, unit-jest, e2e-nightwatch) 
4.  clives-setup ([Vue 2] router, vuex, babel, pwa, eslint) 
5.  Default ([Vue 3] babel, eslint) 
6.  Default ([Vue 2] babel, eslint) 
7.  ❯ Manually select features 

We're going to be manually selecting features – the last option.

This opens a selection menu, where the Babel and Linter functions are already selected. We are going to add TypeScript, PWA Support, Router and Unit Testing:

1.  Vue CLI v5.0.1
2.  ? Please pick a preset: Manually select features
3.  ? Check the features needed for your project: (Press <space> to select, <a> to toggle all, <i> to invert selection, and <enter> to proceed)
4.  ◉ Babel
5.  ◉ TypeScript
6.  ◉ Progressive Web App (PWA) Support
7.  ◉ Router
8.  ◯ Vuex
9.  ◯ CSS Pre-processors
10.  ◉ Linter / Formatter
11.  ◉ Unit Testing
12.  ◯ E2E Testing

From here, we move on to select the version of Vue that we're looking to use; the CLI selects version 3.x by default:

1.  ? Choose a version of Vue.js that you want to start the project with (Use arrow keys)
2.  ❯ 3.x 
3.  2.x 

Next, we'll force the application to use class-style components:

1.  ? Choose a version of Vue.js that you want to start the project with 3.x
2.  ? Use class-style component syntax? (y/N) y

The next presented option is a yes:

1.  ? Use class-style component syntax? Yes
2.  ? Use Babel alongside TypeScript (required for modern mode, auto-detected polyfills, transpiling JSX)? (Y/n) y

We're going to use the Router in history mode:

1.  ? Use class-style component syntax? Yes
2.  ? Use Babel alongside TypeScript (required for modern mode, auto-detected polyfills, transpiling JSX)? Yes
3.  ? Use history mode for router? (Requires proper server setup for index fallback in production) (Y/n) y

Finally, we're adding ESLint and Prettier:

1.  ? Use Babel alongside TypeScript (required for modern mode, auto-detected polyfills, transpiling JSX)? Yes
2.  ? Use history mode for router? (Requires proper server setup for index fallback in production) Yes
3.  ? Pick a linter / formatter config: 
4.  ESLint with error prevention only 
5.  ESLint + Airbnb config 
6.  ESLint + Standard config 
7.  ❯ ESLint + Prettier 

The next option we're faced with is to tell ESLint to lint on save; this enforces conformity of style. The wizard then moves on to test framework selection:

1.  ? Pick a unit testing solution: (Use arrow keys)
2.  ❯ Jest 

Lastly, we'll get the scaffolder to put the config into separate files, which makes maintenance easier in the long run:

1.  ? Where do you prefer placing config for Babel, ESLint, etc.? (Use arrow keys)
2.  ❯ In dedicated config files

The last question it asks is whether you would like to save these options as a preset for future projects. For this section, we're going to answer “no”, but once you have a set of options that you're happy with, it makes sense to say yes to this and use the saved configuration at the first question:

1.  ? Save this as a preset for future projects? (y/N)

Once this is done, the project will start building:

1.  Vue CLI v5.0.1
2.  ✨ Creating project in /speedy-pizza-e-commerce-prototype.
3.  🗃 Initializing git repository...
4.  ⚙️ Installing CLI plugins. This might take a while...

6.  ...

8.  added 1338 packages from 639 contributors and audited 1338 packages in 33.51s

10.  found 2 moderate severity vulnerabilities
11.  run 'npm audit fix' to fix them, or 'npm audit' for details
12.  🚀 Invoking generators...
13.  📦 Installing additional dependencies...

15.  added 132 packages from 97 contributors and audited 1473 packages in 15.892s

17.  ⚓ Running completion hooks...

19.  📄 Generating README.md...

21.  🎉 Successfully created project speedy-pizza-e-commerce-prototype.
22.  👉 Get started with the following commands:

24.  $ cd speedy-pizza-e-commerce-prototype
25.  $ npm run serve

If you follow the last two lines of instructions, the project will serve the project default page.

[Using the Vue UI to create and manage a project](#contents.xhtml_sc2_182a)

Even though the Vue UI is a visual tool, it also starts on the command line:

1.  $ vue ui
2.  🚀  Starting GUI...
3.  🌠  Ready on http://localhost:8000
4.  Auto cleaned 4 projects (folder not found).

This opens a web browser, and you end up on a page that looks like this:

![Graphical user interface, text, application Description automatically generated](images/figure_7.1.png)

Figure 7.1: Vue UI Landing Page

To create a new project, we press the create button, as shown in [Figure 7.2](#ch07.xhtml_fig7-2):

![Graphical user interface Description automatically generated with medium confidence](images/figure_7.2.png)

Figure 7.2: Vue UI Header with Create Button

This surfaces the following:

![A picture containing graphical user interface Description automatically generated](images/figure_7.3.png)

Figure 7.3: Project Create Button

Pressing this button surfaces a new screen so that you can start entering the data you need to create the project:

![Graphical user interface, application, Teams Description automatically generated](images/figure_7.4.png)

Figure 7.4: Set up the project basics

Copy the information from here and press Next.

This takes you to the pre-sets screen, as shown below; again, select manual and then next:

![Graphical user interface, text, application, email Description automatically generated](images/figure_7.5.png)

Figure 7.5: Pre-sets Page

From here, we move on to the configuration screen:

![Graphical user interface, text, application Description automatically generated](images/figure_7.6.png)

Figure 7.6: Feature Configuration Screen

From there, we move on to configuring the version of Vue and the other stuff as per the following figure:

![Graphical user interface, text, application Description automatically generated](images/figure_7.7.png)

Figure 7.7: Configuration Screen

When you create the project from here, you're faced with an option to save the configuration as a pre-set:

![Graphical user interface, text, application Description automatically generated](images/figure_7.8.png)

Figure 7.8: Save Preset Screen

Complete this form or continue with saving the pre-set; the UI wizard starts building your project, after which you end up here:

![Graphical user interface, application, website Description automatically generated](images/figure_7.9.png)

Figure 7.9: Project dashboard shown after completing the wizard

When you get here, the project is set up in the same way as the previous section, but here you can explore extra plugins, dependencies, configurations, and tasks. We'll not be installing anything more from here now but take the time to become familiar with it. There's a lot of helpful stuff on those screens.

[Using Vite to create a project](#contents.xhtml_sc2_183a)

Setting up a project with Vite is even simpler and is fast becoming the standard way of scaffolding out a project.

The following code creates the basis of the app, and it's very quick:

1.  $ npm create vite@latest speedy-pizza-e-commerce-prototype -- --template vue-ts

3.  npx: installed 6 in 1.247s

5.  Scaffolding project in /speedy-pizza-e-commerce-prototype...

7.  Done. Now run:

9.  cd speedy-pizza-e-commerce-prototype
10.  npm install
11.  npm run dev

The last three lines are instructions to follow to pull down all the required dependencies and start the project off in development mode.

[Conclusion](#contents.xhtml_sc2_184a)

This chapter covered the basics of setting up and managing your project and its dependencies. These basics include using NPM and Git, and setting up Vue.js projects.

The tools presented here are all industry standard; you'll be using these all the time for your web projects. However, tools like ,Git which are language agnostic, are used in many other types of projects; this is a really important tool to get to know and add to your skill set.

[Points to remember](#contents.xhtml_sc2_185a)

Git

Git is a distributed code management system. Usually, the remote is used as the single source of truth.

Usually, after the repository is cloned, the codebase is managed by branching, making the required changes, adding (or staging) the code changes into a commit, performing the commit, and then pushing those changes to the remote. Your local copy is kept up to date by fetching and pulling code from the remote.

Code commits might also be rebased (to manage histories) or cherry-picked into the source branch.

How source code is managed is largely specified or controlled by the documentation or process in your organisation.

NPM

JavaScript project dependencies are managed using a package management tool; the one we've opted for in this book is the standard NPM. This means that beyond installing node, we don't need to worry about installing anything to help manage our dependencies. Other tools are available, namely Yarn, but once you understand how to use NPM, learning Yarn is a piece of cake.

NPM is used to install, update, and remove packages from your project. It is a standard tool used in both web and server (Node.js) applications. Many server-side tools from other ecosystems might also use NPM to manage client-side dependencies.

Everything that the project requires is usually held and managed in the package.json file. In many cases, this is the code of your application.

Vue.js CLI

The CLI was predominantly the tool used for creating and managing Vue2 applications. For Vue3, it has been mostly superseded by Vite.

Creating applications with the CLI is well documented and relatively trivial.

Vue.js UI

The UI is a visual wrapper around the CLI. All functionality that is available to you via the CLI is available in the UI. The UI makes management a little easier as it presents the information in a clearer format.

Vite

Vite is the brand new scaffolding tool for Vue.js. It is simple and fast to use. This is the preferred tool for working with Vue3 applications.

[Key terms](#contents.xhtml_sc2_186a)

*   Checkout
*   Cloning
*   Pull
*   Push
*   History
*   Repository
*   Rebase
*   Cherry-pick
*   Remote
*   Merge
*   Patch
*   Origin
*   Package.json
*   NPM
*   Init
*   Audit
*   CLI
*   UI
*   Vite
*   Dependency
*   Packages

[Questions](#contents.xhtml_sc2_187a)

1.  Initialize a new git repository locally for the sample project.

2.  Sign up to GitHub or Bitbucket and link the repo you created in Question 1 to this remote.

3.  Using Vite, create the application scaffold in the previously created git repo, add the code, create an initial commit, and push your code changes to the remote.

4.  Check the remote to make sure your code commit arrived.

Join our book’s Discord space

Join the book's Discord Workspace for Latest updates, Offers, Tech happenings around the world, New Release and Sessions with the Authors:

**[https://discord.bpbonline.com](https://discord.bpbonline.com)**

![](images/fm1.png)

# [CHAPTER 8Adding a CSS Framework to the Mix – TailwindCSS, Bootstrap or Foundation](#contents.xhtml_ch08a)

[Introduction](#contents.xhtml_sc2_188a)

In the previous chapter, we started the project; the project files are ready to go, waiting for our new shiny components to be built. This chapter is going to pick up pace a little, and we're going to take a look at adding in a CSS library, in this case, TailwindCSS.

[Structure](#contents.xhtml_sc2_189a)

In this chapter, we will be exploring the following topics:

*   TailwindCSS and its place in the Web dev ecosystem
*   TailwindCSS configuration and basics
*   Using TailwindCSS
*   Including Tailwind to Vue.js projects
*   Adding pure CSS framework
*   Twitter Bootstrap
*   Zurb Foundation

[Objectives](#contents.xhtml_sc2_190a)

In this chapter, we're going to side-track a little. Instead of assuming that it's easy to integrate and use a CSS framework, we're going to do it. For the purpose of this book, we're going to use TailwindCSS, a CSS-in-JS framework, which is a rising star right now.

We're also going to see how to integrate other more traditional CSS frameworks – Twitter Bootstrap and Zurb Foundation.

[TailwindCSS and its place in the Web dev ecosystem](#contents.xhtml_sc2_191a)

Tailwind is a CSS framework. “So what?”, you might ask; there's loads of them about; what makes Tailwind different?

If you're used to some other CSS framework like Bootstrap, Foundation, Material Design or Bulma, then Tailwind might feel a little different to use.

The CSS frameworks named in the preceding paragraph are predominately component-based frameworks. That means the CSS is designed to work with HTML written in a certain way and particular CSS classes to build various “components”. The way that these components are constructed sometimes are at odds with the logical concerns of the components that you need to build. That's not to say that these frameworks are not useful. They have their place in modern web development, and many companies use them.

TailwindCSS uses a different philosophy. Instead of working with the concept of the component as the basic unit of development, it (Tailwind) uses a concept of limiting the available utilities into a standard set of selectors that can be customized as required.

This utility-first approach means that as a developer, you're not using cycles, thinking up CSS class names, designing custom CSS, or having to mess around with different browser CSS requirements. Part of this concept means you have a centralized batch of CSS without having to grow your CSS files; everything you need is compiled from the settings files. What this means in practice is that you're working at a local HTML level with CSS classes that you can reuse from the global utilities.

What makes Tailwind slightly different to the other, more traditional frameworks is that it's a CSS-in-JS framework. This means it uses JavaScript to compile the requisite global CSS from a settings file.

Now that we have a basic understanding of what Tailwind CSS is, we'll take closer look at how to use it.

[TailwindCSS configuration and basics](#contents.xhtml_sc2_192a)

We will cover how to install Tailwind into a Vue.js project in the next section; in this section, we'll discuss how to configure Tailwind and the basics of how to use it. You'll get further practice as we build the application, but it'll help you get a grounding in the technology if you've never seen it before.

[Configuration](#contents.xhtml_sc3_193a)

Customization is at the heart of using Tailwind. Because there are so many options available, it can be quite confusing at first.

First off, all configuration is placed into a file called tailwind.config.js, which needs to be placed in the root of the project, next to the project's package.json file. This file is optional; if it's not in place, Tailwind falls back to its default configuration. Additionally, any elements not defined in the configuration file will fall back to this default configuration. Tailwinds defaults are available to view on Github at [https://github.com/tailwindlabs/tailwindcss/blob/master/stubs/defaultConfig.stub.js](https://github.com/tailwindlabs/tailwindcss/blob/master/stubs/defaultConfig.stub.js).

It's easiest to have the Tailwind CLI generate the base file for you using npm  tailwindcss init -p, which creates a file with the minimum required options, which falls back to the defaults as well. This also sets up Tailwind as a postcss plugin.

The contents of this file are an exported JSON collection that have any or all of the following keys:

*   content
*   theme
*   plugins
*   presets
*   prefix
*   important
*   separator
*   corePlugins

Of these, we'll only discuss the first three keys. The rest are beyond the scope of this text.

[Configuring options](#contents.xhtml_sc3_194a)

There are various ways in which you can provide configuration options; let's look at each.

As a key-value pair

This is the simplest way of assigning a single value to a particular key:

1.  module.exports = {
2.  //...
3.  colors: {
4.  white: '#fff',
5.  // ...
6.  },
7.  //...
8.  }

As a list of options

Similar to the key-value pair, it provides the resultant CSS with the given list of options against the set key:

1.  module.exports = {
2.  //...
3.  fontFamily: {
4.  sans: ['Raleway', 'Serenity', 'sans-serif'],
5.  ...
6.  }
7.  //...
8.  },
9.  //...
10.  }

As an options object

The options object allows you to set child key-value pairs against a parent key so that when the final CSS is compiled, it becomes part of the rule <type>-<parent>-<child>, that is, border-green-100, as in the listing below:

1.  module.exports = {
2.  //...
3.  colors: {
4.  green: {
5.  100: '#ebf4ea',
6.  200: '#bedfc4',
7.  //...
8.  }
9.  //...
10.  },
11.  //...
12.  }

As a theme reference closure

When building out your CSS configuration, you might need to access values that are defined as part of the theme. To this end, you can supply an anonymous function that provides a theme() function, which can be used to access these values.

Note that you can't access this function to return simple values; this type of function can only be applied at the top level, i.e., the CSS selector level; see the example. Additionally, values retrieved must use either dot or square bracket notation due to the nested object syntax that Tailwind uses, as below:

1.  module.exports = {
2.  theme: {
3.  borderColor: ({ theme }) => ({
4.  lightBlue: theme('colors.blue.100')
5.  })
6.  }
7.  }

As a default theme reference

If you need to reference a simple value from the default theme, this is achieved by importing the default theme object and accessing it directly via dot notation, as shown in line 9:

1.  const defTheme = require('tailwindcss/defaultTheme')

3.  module.exports = {
4.  theme: {
5.  extend: {
6.  fontFamily: {
7.  sans: [
8.  'Serenity',
9.  ...defTheme.fontFamily.sans,
10.  ]
11.  }
12.  }
13.  }
14.  }

Not all of these are appropriate to all options; the Tailwind documentation at [https://tailwindcss.com/docs](https://tailwindcss.com/docs) is your friend.

[Content](#contents.xhtml_sc3_195a)

The content section is a list of all the paths where Tailwind class names have been used. This is so that Tailwind can build the smallest viable CSS file to cover all the elements used. If no Tailwind classes have been used, then this is a fairly small file.

Content paths are set to be relative to the root in a list.

1.  module.exports = {
2.  content: [
3.  "./index.html",
4.  "./src/**/*.{vue,js,ts,jsx,tsx}",
5.  ],
6.  // …
7.  }

[Theme](#contents.xhtml_sc3_196a)

The Theme section is where you define all the various options that you need to build the visuals of your site. We're talking actual CSS configuration options: colors; fonts and sizes; borders; spacing, etc.

Theme elements can be defined in several ways. Apart from colors, spacing, and screens keys, the options available map to one of the supplied core plugins. Not all core plugins accept configuration options, but those that are available for extension are given at https://tailwindcss.com/docs/theme#configuration-reference.

[Colors, spacing and screens](#contents.xhtml_sc3_197a)

The colors key is used to set up the color palette for your project. A color can be defined as a mapping between a color name and a CSS color value (like blue), a color hexcode (like #000 or #c5f4e1) or an RBG string (rgb(4 65 255)/75).

You can also set up a colors object to provide various shades of the same color, graded by an arbitrary amount, as can be found in the default theme for example:

1.  module.exports = {
2.  theme: {
3.  colors: {
4.  orange: {
5.  50: '#fff7ed',
6.  100: '#ffedd5',
7.  200: '#fed7aa',
8.  300: '#fdba74',
9.  400: '#fb923c',
10.  500: '#f97316',
11.  600: '#ea580c',
12.  700: '#c2410c',
13.  800: '#9a3412',
14.  900: '#7c2d12'
15.  }
16.  }
17.  } 
18.  }

This allows you to group similar colors together so that they can be accessed using dot notation, i.e., text-orange-600.

In a similar vein, we can configure both spacing and screen size breakpoints. However, it is better if instead of overriding all the provided settings, they are extended to cater to your own requirements. This way, you benefit from the countless man-hours used to design the defaults and don't reinvent the wheel, so to speak.

For example, extending the theme spacing can be done by adding settings for example, 17, 18, and 19 as given below:

1.  module.exports = {
2.  theme: {
3.  extend: {
4.  spacing: {
5.  '17': '4.25rem',
6.  '18': '4.5rem',
7.  '19': '4.75rem'
8.  }
9.  }
10.  }
11.  }

Default spacing settings and other information can be found at https://tailwindcss.com/docs/customizing-spacing#default-spacing-scale, which has a comprehensive list of the provided sizes.

The settings for spacing are used to provide width settings for CSS rules like padding, margin, width, and height, e.g., px-4; m-10.

The screens section is used to define the breakpoints required for your project – Tailwind itself provides a set of sensible defaults for the min-width media query setting. They can be extended or overridden like any other provided value.

If you provide an object with the a max key, then the generated breakpoint returns a max-width rather than a min-width, as follows:

1.  module.exports = {
2.  theme: {
3.  screens: {
4.  '2xl': {'max': '1900px'},
5.  // => @media (max-width: 1900px) { ... }
6.  ...

The screens settings are used to prefix classes to apply the selected class at that breakpoint, e.g., sm:text-right md:text-center.

In the theme section, when you create a rule, you build a style definition against a key – the key is the name of the style. This key is mapped to a function, called a plugin. Plugins are the subject of the next section

[Plugins](#contents.xhtml_sc3_198a)

Tailwind CSS class definitions are provided by plugins. The name of the plugin is conveniently the same as the JS CSS API style rule name, i.e., CSS border-width is borderWidth, and so on.

Plugins can also be custom created to inject styles into the project stylesheet via JS instead of hand-cranking CSS.

There are some official plugins that are maintained outside the ones provided in the Tailwind core installation. These are as follows:

@tailwindcss/typography

@tailwindcss/forms

@tailwindcss/line-clamp

@tailwindcss/aspect-ratio

If you want to use these, they first need to be added to the project using NPM and then to the config file:

1.  module.exports = {
2.  // ...
3.  plugins: [
4.  require('@tailwindcss/typography'),
5.  require('@tailwindcss/forms'),
6.  require('@tailwindcss/line-clamp'),
7.  require('@tailwindcss/aspect-ratio'),
8.  ]
9.  }

Building a custom plugin requires you to import the Tailwind plugin function. When this function is used, Tailwind supplies the anonymous callback function with a single object argument that can be destructured into some helper functions, the most important ones of these are as follows:

*   addUtilities - For registering new static utility styles
*   matchUtilities -  For registering new dynamic utility styles
*   addComponents - For registering new static component styles
*   theme  -  For looking up values in the user's theme configuration
*   config  - For looking up values in the user's Tailwind configuration

The following listing shows how to use the Plugin function:

1.  const plugin = require('tailwindcss/plugin')

3.  module.exports = {
4.  plugins: [
5.  plugin(function({ addUtilities, theme }) {
6.  // Add your custom styles here
7.  }),
8.  ...

We'll not go into any more detail on custom plugins, as they're beyond the scope of this book, but further detail can be found at [https://tailwindcss.com/docs/plugins](https://tailwindcss.com/docs/plugins) if you ever need to build your own.

[Using TailwindCSS](#contents.xhtml_sc2_199a)

Once configured, using Tailwind is actually very simple. You just provide the CSS classes that you need to use to style the HTML skeleton that describes your content.

The way the rules are constructed makes them easy to parse and understand. They are, however, quite verbose and can make the class attribute definition quite long. As demonstrated in the following listing:

1.  <div class="flex justify-start my-2 mx-4 p-4 w-full md:w-1/2 lg:w-1/3">
2.  <h1 class="font-bold text-blue-300 text-lg">My Title</h1>
3.  <!-- Further HTML content -->
4.  </div>

Because of its flexibility, if you required specialized names for your CSS to say, provide component-based equivalence or wrap a common set of rule definitions into an easy-to-remember name, Tailwind makes this easy without having to scroll through hundreds of lines of CSS.

There'll be plenty of practice in the subsequent chapters as we build out the example to explore Tailwind in the context of building a working web application.

[Including Tailwind to Vue.js projects](#contents.xhtml_sc2_200a)

As we'll be integrating Tailwind into the build package, we need to install all the required dependencies and then add the relevant files to the project.

There are a few steps to follow, but the process has been simplified a lot since Tailwind's first release.

In the project root folder (where the package.json file lives), run the following from the terminal:

1.  $ npm i -D tailwindcss postcss autoprefixer
2.  < npm installer output >
3.  $ npx tailwindcss init -p

This installs all the dependencies that you need to integrate Tailwind (line 1), and then the npx command executes a build script that injects the required configuration at the project root: tailwind.config.js and postcss.config.js.

In this newly minted tailwind.config.js file, you'll need to make a manual change. At this point, we will only be adding a content property that defines the paths to all the template files in the project. As Tailwind config is glob aware, defining the content paths is simple to do – see lines 2 to 5 in the following listing:

1.  module.exports = {
2.  content: [
3.  "./index.html",
4.  "./src/**/*.{vue,js,ts,jsx,tsx}",
5.  ],
6.  theme: {
7.  extend: { },
8.  },
9.  plugins: [ ],
10.  }

Now that Tailwind knows where to find the files that it will need to parse, we add the Tailwind layer definitions to the projects main or root CSS file. Note that you might have to create this file if it doesn't exist; you can call this file whatever you wish, but for the purposes of this book, we'll put this file on the path './src/assets/index.css', with the following content:

1.  // ./src/assets/index.css

3.  @tailwind base;
4.  @tailwind components;
5.  @tailwind utilities;

After this, we just need to plumb this CSS file into the application so that it gets picked up by the builder. The main file (either main.js or main.ts) is found in the src directory of the project, with the contents as given below:

1.  // ./src/main.{js,ts}

3.  import { createApp } from 'vue'
4.  import App from './App.vue'
5.  import './assets/index.css'

7.  // Rest of project start up

If you now (re)start the project, Tailwind will compile the required CSS and make it available to your project. Run the following in your terminal:

1.  $ npm run dev

If at this point, you're happy with Tailwind, you can skip to the next chapter. However, if you need to use a pure CSS-based framework like Twitter Bootstrap, read on.

[Adding pure CSS frameworks](#contents.xhtml_sc2_201a)

This following section explores how to add other CSS frameworks, namely, Twitter Bootstrap and Zurb Foundation. At this point, it is assumed that that you are comfortable using these if you're looking to use them instead of TailwindCSS.

[Twitter Bootstrap](#contents.xhtml_sc2_202a)

The assumption here is that you are already familiar with Bootstrap as a framework; it's been around for a long time, has been used in many large projects, and has a large community behind it. If you are familiar with Foundation instead, we will go over that afterward.

The steps to adding a framework like Bootstrap are very similar to those we followed when we added Tailwind.

Firstly, we'll install the framework dependencies:

1.  $ npm i @popperjs/core bootstrap

With these installed, you update the main file to import the required Bootstrap files:

1.  // ./src/main.{js,ts}

3.  import "bootstrap/dist/css/bootstrap.min.css"
4.  import "bootstrap"

When you run your project after this change, you will have Bootstrap CSS and components available to you. From here, you can either use the Bootstrap data attributes to provide data and functionality as required, or you can wrap the Bootstrap provided components with Vue.js components and build yourself a component library to use. More details on Bootstrap can be found at [http://getbootstrap.com](http://getbootstrap.com).

[Zurb Foundation](#contents.xhtml_sc2_203a)

Start by doing the relevant imports:

1.  $ npm i jquery what-input motion-ui foundation-sites

The simplest way to use the CSS is to import it directly into the main file, just like Bootstrap; add the following:

1.  // ./src/main.{js,ts}

3.  import 'foundation-sites/dist/css/foundation.min.css'
4.  import 'foundation-sites/dist/js/foundation.min'

With these imports in place, you can use Foundation CSS.

[Conclusion](#contents.xhtml_sc2_204a)

In this chapter, we covered integrating and using TailwindCSS. There is a lot of detail here as it's a relatively new framework that's gaining a lot of industry interest.

Lastly, we've looked at how to integrate older, more well-known CSS frameworks.

[Key terms](#contents.xhtml_sc2_205a)

*   TailwindCSS
*   CSS-in-JS
*   Utility-first
*   Layers
*   Components
*   Bootstrap
*   Foundation
*   Plugins
*   Spacing
*   Theme

Join our book’s Discord space

Join the book's Discord Workspace for Latest updates, Offers, Tech happenings around the world, New Release and Sessions with the Authors:

**[https://discord.bpbonline.com](https://discord.bpbonline.com)**

![](images/fm1.png)

# [CHAPTER 9Building User Interfaces with Components](#contents.xhtml_ch09a)

[Introduction](#contents.xhtml_sc2_206a)

So far, we have started our prototype project and added some basic Tailwind style definitions.

In this chapter, we will build out the basic constituent parts of the pages that were discussed in [Chapter 5](#ch05.xhtml), Designing Component-Based UIs and Single Page Applications. After building these smaller components, we'll end the chapter having built out the main content areas of the design. These will form the building blocks that we will iterate over so that we can build the additional functionality in the next few chapters.

[Structure](#contents.xhtml_sc2_207a)

This chapter covers the following topics:

*   Setting up a useable folder structure
*   Building the basic prototype templates

A lot is to be covered in this chapter, so let's get started.

[Objectives](#contents.xhtml_sc2_208a)

The primary objective of this chapter is to start looking at Vue.js in context of an actual project. So far, we've studied a lot of theory and seen how applications fit together at a high level. We're now going to get familiar with coding and look at how to structure a project.

We'll start at the very beginning and work through setting everything up so that there is a firm and usable foundation to build upon. Then, we'll populate the directory structure that we'll have created.

This chapter will form the basis of our sample project.

[Setting Up – Managing the project folders and files](#contents.xhtml_sc2_209a)

Vue.js doesn't care how you structure your files, as long as it can find them. How the codebase is structured is purely a human-centric activity – a logical folder structure, using a helpful or even semantic naming convention, helps development engineers and the subsequent maintenance engineers quickly find where code resides. What you're really striving for is a balance between the structure not being too flat so that all the files are held in the same folder and not too deep so that you don't have to search through many branches before you find what you're looking for. Ideally, we'd design a structure that at most is three, or maybe four, folders deep under the /src folder. This gives us enough scope to build something reasonable; we're not using Java after all.

When you generate a project with Vite – as we did back in [Chapter 7](#ch07.xhtml), Creating and Setting Up a Vue.js Application With Vue CLI and Vite, we get a structure that looks like this:

![](images/figure_9.1.png)

Figure 9.1: Standard Vite generated folder structure

While this is fine for small projects, it's less than helpful once the project grows beyond a few components or multiple concerns.

What we're going to do is remove the HelloWorld.vue file from the components folder, empty the App.vue file, and then add the following folders to the src/ folder:

components/pages

components/pages/site

components/pages/profile

These directories will contain the page components – each page has its own folder.

components/layouts

components/layouts/common

These folders will help to manage the components that define the layouts. This folder will be filled out when we build the pages with the router.

components/partials

This folder contains small template parts, elements that are “partial” templates and are reused across the codebase, organized by concern.

composables

This is where we're going to place the composable part of our component code.

routes

This is where the routing information is going to go; we'll be working in this folder in the next chapter.

store

When we need to concern ourselves with the application-wide state, we'll start filling in this folder.

[Figure 9.2](#ch09.xhtml_fig9-2) shows how your folder structure show look now:

![](images/figure_9.2.png)

Figure 9.2: Directory changes

With code organization out of the way, we can start concentrating on building our application out.

[Building the Basic Prototype Templates](#contents.xhtml_sc2_210a)

Of the different ways that we can approach the problem of building the components, we'll take an outside-to-inside approach for the landing page. This gives us the opportunity to build many of the common page elements and the specific elements that make up this page. We'll use some of the other techniques discussed for building components when we tackle the other pages. We'll discuss building layouts when we work with the VueRouter in [Chapter 10](#ch10.xhtml), Routing Between Pages With VueRouter.

[Landing Page Template](#contents.xhtml_sc2_211a)

From the list of components that we devised in [Chapter 5](#ch05.xhtml), Designing Component-Based UIs and Single Page Applications, this part of the site is going to focus on us building the main, repeatedly used components, that is, the page header and footer, which appear on every page. And we'll work on the specific components required for the landing page.

As a reminder of what we're building, [Figure 9.3](#ch09.xhtml_fig9-3) is a copy of the wireframe from [Chapter 5](#ch05.xhtml), Designing Component-Based UIs and Single Page Applications:

![Graphical user interface, application Description automatically generated](images/figure_9.3.png)

Figure 9.3: Landing page wireframe

[Page Layout](#contents.xhtml_sc2_212a)

The page layout is just a wrapper component that holds all the other components; it's relatively simple, and as you can see, it follows the wire frame quite closely.

We'll create a file in components/pages/site called LandingPage.vue:

1.  <template>
2.  <div class="container mx-auto h-screen">
3.  <menu-bar-component></menu-bar-component>
4.  <div class="container mx-auto">
5.  <hero-component></hero-component>
6.  <offers-component></offers-component>
7.  </div>
8.  <footer-component></footer-component>
9.  </div>
10.  </template>

12.  <script setup lang="ts">
13.  import MenuBarComponent from '/src/components/layouts/common/MenuBarComponent.vue'
14.  import HeroComponent from './HeroComponent.vue'
15.  import OffersComponent from './OffersComponent.vue'
16.  import FooterComponent from '/src/components/layouts/common/FooterComponent.vue'
17.  </script>

We're going to look ahead a little with where we're placing the MenuBarComponent and FooterComponent files and put them straight into the components/layouts/common directory.

As you can see, the code is not all that difficult; it includes a few imports and a reasonably small template section. If you try and run it though, the compiler will complain; we haven't built these components yet, so there's nothing for it to find or build, and that causes a problem.

The first component that we'll tackle is MenuBarComponent.

[MenuBarComponent](#contents.xhtml_sc3_213a)

The MenuBar is the main page header, which holds the site logo and primary navigation. Create the components/layouts/common/MenuBarComponent.vue file and place the following code in it:

1.  <template>
2.  <div class="mt-1">
3.  <div class="bg-gray-300 border-b border-gray-500 
    rounded-lg px-4 pt-2">
4.  <div class="container mx-auto flex justify-between">
5.  <div class="mb-1">
6.  <h1 class="logo text-5xl font-bold 
    text-logo-red">Speedy</h1>
7.  <h1 class="logo text-5xl font-bold ml-16 
    text-logo-red mb-1">Pizza</h1>
8.  </div>
9.  <menu-items></menu-items>
10.  </div>
11.  </div>
12.  </div>
13.  </template>

15.  <script setup lang="ts">
16.  import MenuItems from './MenuItemsComponent.vue'
17.  </script>

We've split out the actual menu into a subcomponent that is only used in these two components, which means we've got a single place to edit. We'll place this subcomponent next to the HeaderComponent and FooterComponent and call it MenuItemsComponent.vue:

1.  <template>
2.  <div class="flex w-1/6 justify-between font-bold">
3.  <a href="#">Home</a>
4.  <a href="#">Menu</a>
5.  <a href="#">Profile</a>
6.  </div>
7.  </template>

As you might have noticed, we're just blocking out the hyperlinks; when we introduce the router, we'll come back and change these so that they point to the right place. In a larger project, you should expect the router to be in place first, so that any new pages can be added to the router configuration before they are built. We'll look at the router in detail in [Chapter 10](#ch10.xhtml), Routing Between Pages With VueRouter.

[FooterComponent](#contents.xhtml_sc3_214a)

Place the FooterComponent.vue file next to the MenuBarComponent and add the following code to the file:

1.  <template>
2.  <div class="container mx-auto fixed bottom-1 left-2 right-2 py-4 px-8 bg-gray-300 font-bold border-t border-gray-500 rounded-lg">
3.  <div class="container mx-auto flex justify-between">
4.  <div>&copy; Speedy Pizzas &amp; Clive Harber 2022</div>
5.  <menu-items></menu-items>
6.  </div>
7.  </div>
8.  </template>

10.  <script setup lang="ts">
11.  import MenuItems from './MenuItemsComponent.vue'
12.  </script>

This, again, is simple, just a set of styled links to the relevant pages. As we're building out a small prototype, you'll see that a few things are missing from the provided design that would be required in a real-world public facing website: links to the site's terms and conditions policies, data handling and management, and cookie tracking policies. Depending on where you are in the world, you might need some or all of these linked from every page, particularly if you're looking to collect and use data from EU citizens. There are a set of legal frameworks that you will need to be aware of if you are based in the EU or intend to sell/provide services to EU countries that might not exist in other parts of the world.

With these components in place, we can start building out the internal parts; if you were to run the compiler, it will help by pointing out what's missing. Try it now: npm run dev. You'll get output in the terminal, as shown in [Figure 9.4](#ch09.xhtml_fig9-4):

![Text Description automatically generated](images/figure_9.4.png)

Figure 9.4: Errors from missing components

As you can see, we need to tackle the hero component, which we'll do next.

[HeroComponent](#contents.xhtml_sc3_215a)

A “hero component” is a massive shop window into what you want the customer to be presented with. It's pretty much the first thing that someone arriving on the site will see, even before your logo. This component will be the largest, most visible thing on your landing page. For many sites, it is the primary call to action (CTA) driver on a site, especially if you're running e-commerce or selling services.

Typically, the hero component takes up the top 50% to 75% of the real estate on the landing page above the fold. It might be tabbed, but most likely it will be an image rotator, with differing calls to action depending on the content of the main area, directing users to different part of the site depending on which element in the rotation attracted/interested them.

We're not going to cover the psychology of marketing; there's far too much of it, and the scope of this book is limited. However, as the developer, you need to know what to build and how to build it. Leave the contents of this space to the mad monkeys in marketing.

This component is either simple, like an image, a button and maybe some leader text, or it might be really complicated, like a multi-image slideshow with different outcomes depending on which CTA is accessed.

For the prototype that we're building, we don't need to make it overly complicated. Most of managing how things are displayed is going to be done by CSS and therefore, by Tailwind, and the CTA will eventually be handled by the router.

The code for this looks as follows:

1.  <template>
2.  <div class="hero">
3.  <div class="btn-placement-b">
4.  <button class="red-button">View Our Menu</button>
5.  </div>
6.  </div>
7.  </template>

9.  <style scoped>
10.  .hero {
11.  background: url(src/assets/hero_image.jpg);
12.  @apply mx-auto mt-1 h-108 flex flex-col w-9/12 bg-no-repeat bg-center border rounded;
13.  }
14.  </style>

We can show off a little later when we explore transitions and accessing remote data, where we can make this component data-driven. However, for now, we've just built it around a simple component data core that informs us of the data that we'll need to supply the component when we drive it from a remote data source.

[OffersComponent](#contents.xhtml_sc3_216a)

From a template perspective, the OffersComponent is quite simple to look at, but it's the most complicated component we will have built so far. We're using a data object that contains a collection of items, which is used to drive a loop that outputs several internal components, each of which display a single item from the list. Lots of things to unpack here:

1.  <template>
2.  <div class="flex justify-center space-x-16 mt-4">
3.  <offer-component
4.  v-for="offer in offers"
5.  :key="offer.id"
6.  :id="offer.id"
7.  :text="offer.btn_text"
8.  :image="offer.image"
9.  ></offer-component>
10.  </div>
11.  </template>

The template here uses the v-for directive to loop over the offers data (described as follows), extracting each offer in turn. We're providing the offer id as the required :key attribute so that Vue can track changes if necessary.

Each pass through the loop injects an OfferComponent that accepts the provided props to render. As you can see, we're using the : shorthand to v-bind the data. This makes it easier to read as it's closer in style to HTML attributes. Feel free to write v-bind: if you really want, but after a while, it becomes a chore and also looks messier.

This component has two script sections; the first is the Composition API <script setup> section, as below:

1.  <script setup lang="ts">
2.  import OfferComponent from "./OfferComponent.vue"
3.  </script>

The second defines the data object (for now), which enables us to build the loop of the OfferComponents by defining the offers object that confirms to the props type required by the child component. Without conforming to this interface, the child component won't render. It's been written like this, so that when we change the component to pull data from Pinia, we can remove this entire section:

1.  <script lang="ts">
2.  import { defineComponent } from "vue";

4.  export default defineComponent({
5.  data: () => ({
6.  offers: [
7.  { id: ١, image: "", btn_text: "Offer 1" },
8.  { id: ٢, image: "", btn_text: "Offer 2" },
9.  { id: ٣, image: "", btn_text: "Offer 3" },
10.  ],
11.  }),
12.  });
13.  </script>

With is this loop in place, we just need to construct OfferComponent, which is next.

[OfferComponent](#contents.xhtml_sc3_217a)

The OfferComponent here just describes how to display a single offer and provides a call to action based on the provided data. Eventually, this will turn into an example of dynamic routing, but for now, we will just block out the CTA so that it can be styled in line with the rest of the page. See the following listing:

1.  <template>
2.  <div class="offer" :style="{ backgroundImage: bgImage }">
3.  <div class="btn-placement-b">
4.  <button class="red-button">{{ text }}</button>
5.  </div>
6.  </div>
7.  </template>

9.  <script setup lang="ts">
10.  import { computed } from 'vue';

12.  interface Props {
13.  id: number;
14.  text: string;
15.  image: string;
16.  }

18.  const props = defineProps<Props>();
19.  const imageBaseUrl = 'src/assets/';

21.  const bgImage = computed(() => 
22.  `url(${imageBaseUrl}${props.image})`);
23.  </script>

25.  <style scoped>
26.  .offer {
27.  @apply bg-cover bg-no-repeat bg-center w-64 text-center h-64 flex flex-col border rounded;
28.  }
29.  </style>

Here, we're defining an interface to set what data is expected from the props object. We're also dynamically setting an inline style so that the background of the OfferComponent can be injected from the data passed in. At this stage, we are hard-coding the path. When we pull data from an API, we'll swap this out and rely completely on the passed data.

This is the final component required to render the home page; to make things behave according to plan, we'll need to make a few small adjustments to the App.vue file. It needs to be told what we want it to render when the application starts.

[Changes to App.vue](#contents.xhtml_sc2_218a)

The following changes need to be made to the App.vue file:

1.  <template>
2.  <landing-page></landing-page>
3.  </template>

5.  <script setup lang="ts">
6.  import LandingPage from "./components/pages/site/landing-page/LandingPage.vue"
7.  </script>

With these changes in place, start the application from you terminal:

1.  $ npm run dev

Open a browser and point it at http://localhost:3000 if using Vite 2 or http://localhost:5173 if using Vite 3\. With the final item in place, the page will now compile correctly, and when you switch to your browser, you'll see all your hard work looking back at you. Give yourself a pat on the back and take a break; we've done a lot in a short span of time.

At this point in time, it makes sense to push your changes into your Git repo:

1.  $ git add .
2.  $ git commit -m '<your commit message>'
3.  $ git push origin <branch>

In the next chapter, we're going to start building out the router, extract the common elements that describe what we'll label as a layout and complete building many of the other pages' internal components.

[Conclusion](#contents.xhtml_sc2_219a)

In this chapter, we completed a lot of work, even though it probably doesn't feel like it. We built a logical foundation that will help with maintenance, and we built out our project landing page and run the project and performed a git commit.

In the next chapter, we'll start adding in the application navigation paths, the layouts and the remaining pages.

[Key terms](#contents.xhtml_sc2_220a)

*   Components
*   Directory Structure
*   Call to Action
*   HTML
*   Layouts
*   Header
*   Footer
*   Compile
*   Git
*   Legislation

Join our book’s Discord space

Join the book's Discord Workspace for Latest updates, Offers, Tech happenings around the world, New Release and Sessions with the Authors:

**[https://discord.bpbonline.com](https://discord.bpbonline.com)**

![](images/fm1.png)

# [CHAPTER 10Routing Between Pages with VueRouter](#contents.xhtml_ch10a)

[Introduction](#contents.xhtml_sc2_221a)

So far, we've put together a single page, but we need more; we need to be able to manage how the user navigates between pages, and in an SPA, that means without doing a full HTTP round-trip to the server to get the next page and the time it takes to do that. This is the promise of single page applications: reduce the navigation time to improve the user experience.

In Vue.js, this front-end routing is managed using VueRouter.

[Structure](#contents.xhtml_sc2_222a)

In this chapter, we are going to move from a single page website to a web application with templating and page routing. To make this happen, we'll discuss the following topics:

*   The practice of front-end routing
*   Adding the VueRouter
*   Building routing definitions
*   Updating the project: changing <a/> tags to router-link
*   VueRouter navigation guards
*   Navigating by code

[Objectives](#contents.xhtml_sc2_223a)

This chapter explores front-end routing. We'll start by discussing the need for front-end routing in general, and then we'll look at adding routing to the Vue.js project. Next, we'll apply that newly acquired knowledge to the prototype project. Lastly, we'll just go over how to protect your routes and how to handle data manipulation before the component receives it.

By the end of this chapter, you should be proficient in building a set of routing definitions for your projects.

[The practice of front-end routing](#contents.xhtml_sc2_224a)

In traditional web development, each request, that is, each clink on a hyperlink, initiated a round trip to the hosting server to create the response that was then rendered in the client browser. This round-trip can have detrimental effects on the user experience, especially in low-bandwidth environments, so the drive to building frontside, single page applications (SPA) help mitigate this impact. As the client has all the code that it needs to render the web pages, it doesn't need to perform that round trip – the only thing that needs to happen is that the application must fetch any dynamic data it needs – these data should be optimized to be small, especially for low-bandwidth connections, to reduce the impact on the user.

For SPAs to function correctly, they need to be able to transfer the user to the requested page without the full HTTP cycle. This is where the router comes in.

With Vue.js, the frontside router, that is, VueRouter, maps a set of URLs that the application is required to intercept to a component (or components/views) that it should render.

In terms of complexity, configuring VueRouter is not all that difficult. If you're used to working with React, VueRouter is far simpler, on par with Angular or Express.

[Adding the VueRouter](#contents.xhtml_sc2_225a)

Adding the Router to a Vue project is like adding middleware to a Node Express application; in fact, that's pretty much what we're doing: adding middleware.

Firstly, we need to add VueRouter to the project using NPM:

1.  $ npm install vue-router

We then need to set the router up in the file where we create the Vue.js application (in our case, it is main.ts). The following listing shows how to do this:

1.  import { createApp } from 'vue'
2.  import { createRouter, createWebHistory } from 'vue-router'
3.  import routes from './routes/routes.js'
4.  <Rest of code here>

6.  const router = createRouter({
7.  history: createWebHistory(),
8.  routes
9.  })

11.  const app = createApp(App)
12.  app.use(router)
13.  app.mount('#app')

When adding a router, you need to complete a few stages to make the application router-aware. These are as follows:

1.  Import the createRouter() function and required history mode function (i.e., createWebHistory()); line 2

2.  Import (or define) a list of routes; line 3

3.  Create the router using the createRouter() function; line 6

4.  Add the defined router to the application with app.use(); line 12

At this point, the routes/routes.js file just needs to export an empty array, but that's not very useful.

The next section covers how to build routes, and then we'll build the routes needed for the prototype application.

[Building routing definitions](#contents.xhtml_sc2_226a)

The router accepts a list of objects that define a mapping between a path (or URL) and the component that path is required to render. These objects need to conform to the RouterRecordRaw object which is defined at [https://router.vuejs.org/api/#routerecordraw](https://router.vuejs.org/api/#routerecordraw). The options that will be used the most are path, component(s), name, children, beforeEnter, and props. Each of these will be discussed in the following section. There are also other infrequently used options like alias and redirect. The most used options are presented below:

1.  [{
2.  path: String,
3.  name: String?,
4.  component: Component?,
5.  props: Boolean?,
6.  beforeEnter: (NavigationGuard|NavigationGuard[])?,
7.  children: [RouterRecordRaw]?
8.  }]: [RouterRecordRaw]

Note: A NavigationGuard is a function that is used to protect the route or perform a redirect; we'll discuss these later.

[RouterRecordRaw Object](#contents.xhtml_sc2_227a)

A RouterRecordRaw object (along with similar objects like RouterRecordNormalised) comprises of the definition provided earlier, and it is the mapping that the router requires to match a path (a relative URL) to an output component. This path can be static or dynamic, depending on the needs of the page. Let's look at each of the most used parts.

[Path](#contents.xhtml_sc3_228a)

The path is a pattern, which can be a simple string or a complex pattern that breaks down into a set of values that can be passed into the component to enable it to pull data from a local value, application-local store (like Pinia), or a remote source.

Examples of various path types are shown below:

1.  // Simple string
2.  path: '/'
3.  path: '/cars/show/all'

5.  // Dynamic segments
6.  path: '/cars/:id'
7.  path: '/cars/:id/edit'

9.  // id available as $route.params.id
10.  // partId available as $route.params.partId
11.  path: '/cars/:id/show/:partId'

13.  // Custom regex
14.  // matches multiple segments into missingPath
15.  path: '/:missingPath(.*)*'
16.  // matches parts into make and model
17.  path: '/cars-:make(.*)-:model(.*)'
18.  // matches into doors and ensures numbers
19.  path: '/cars/:doors(\\d+)'
20.  // optionally match for id
21.  path: '/cars/:id?'

As you can see in the dynamic path examples, a value can be extracted into a variable that you can use in your component by preceding the name you want with a colon (:). There are three ways to access this data: via the $route object passed into the component for Options API, the useRoute() function for Composition API, or via props (refer to the Props section).

The $route object (or the Composition API alternative) has various other parts of the route available if required, like the query, the hash or information regarding redirection.

If you're building your project along the lines of REST principles, then it's unlikely that you'll use $route.query a great deal, and if you're not using hash navigation, then $route.hash is equally unlikely, but these options are available if needed.

Note: REST or Representational State Transfer is a set of principles or constraints on how APIs are built. These constraints enable the designing of lightweight, internet-scale APIs that map URIs to resources via HTTP and therefore, hide the underlying implementation. More information is available at [https://en.wikipedia.org/wiki/Representational_state_transfer](https://en.wikipedia.org/wiki/Representational_state_transfer).

We'll be rebuilding the navigation for the prototype in a later section of this chapter, so we'll explore this further at that point.

[Name](#contents.xhtml_sc2_229a)

The name property allows you to assign a particular name to a route. This gives you, as the developer, the flexibility to create the routes and maintain them as needed, without having to make changes across all the project files. Using named routes is a recommended practice.

When you want to use a named route, the router-link to property is passed an object that provides the name and any routing parameters that are necessary to build the path. The compiler then builds the correct path based on the router information and supplied parameters. Any parameters are automatically URL-encoded. The sample below presents an example of a router configuration and its usage in template code:

1.  const routes = [
2.  {
3.  path: '/item/:id(\\d+)',
4.  name: 'item',
5.  component: ItemPage
6.  }
7.  ]

9.  <router-link :to="{ name: 'item', params: { id: 123 }}"
10.  Italian Meatball
11.  </router-link>

Each route name in the project must be unique. If any route names clash, the compiler will stop building the project and return an error report.

[Component(s)](#contents.xhtml_sc3_230a)

This setting specifies which component (or components) are required by the template to render if that path is accessed.

If the targeted template uses only a default router-view, then only a single component property is required:

1.  // template
2.  <template>
3.  <router-view></router-view>
4.  </template>

6.  // simple single component routing
7.  const routes = [
8.  {
9.  path: '/'
10.  component: Component
11.  }
12.  ]

If the targeted template uses named views (that is, multiple router outlets), then it requires the components property, which accepts an object that maps the named/default views to the required components, as demonstrated below:

1.  // template
2.  <template>
3.  <div>
4.  <router-view name='SideBar'></router-view>
5.  </div>
6.  <router-view></router-view>
7.  </template>

9.  // simple single component routing
10.  const routes = [
11.  {
12.  path: '/',
13.  components: {
14.  default: Home,
15.  SideBar
16.  }
17.  }
18.  ]

If the route record redirects, it does not have a component or components property.

[Props](#contents.xhtml_sc3_231a)

The props property determines whether the data encoded in the path is available to the component as part of the props object. This is a Boolean property for single viewed components, so it's either on or off – the following sets it to true and therefore on:

1.  props: true

For multi- or named view components, this object provides a setting for each view, set by name, as below:

1.  props: {
2.  SideBar: true,
3.  default: false
4.  }

If the props object provided holds a key that does not correspond to a view, it will be merged into the props object supplied to the component unaltered. This is a simple way of supplying static props data, as presented below:

1.  props: {
2.  SideBar: true,
3.  default: false,
4.  NewValue: 'passed into component'
5.  }

Lastly, if you supply a function to this property, it injects the route object as a parameter that you can interrogate to create any data combination that you might need:

1.  // /search/searchTerm => props: {params: 'searchTerm'}
2.  const routes = [
3.  {
4.  path: '/search/:name',
5.  component: SearchComponent,
6.  props: route => ({ params: route.params.name })
7.  }
8.  ]

[beforeEnter](#contents.xhtml_sc3_232a)

beforeEnter is known as a navigation guard; this functionality is to be executed before the target components are rendered so that the navigation can be redirected, cancelled, or altered as necessary. The beforeEnter hook in the route definition is one of many ways to influence navigation; navigation guards will be discussed later in this chapter.

To add a beforeEnter guard, you need to provide the property with a function (or list of functions) that accepts two arguments:

to: The target route of the navigation

from: The source route that initiated the navigation

Use of this property is as follows:

1.  // single anonymous function
2.  const routes = [
3.  {
4.  path: '/profile/:id',
5.  component: ProfileInfoPage,
6.  beforeEnter: (to, from) => {
7.  // reject the navigation
8.  return false
9.  },
10.  },
11.  ]

13.  // applying multiple functions
14.  const applicativeOne = (to, from) => { return true }
15.  const applicativeTwo = (to, from) => { return false }

17.  const routes = [
18.  {
19.  path: '/profile/:id',
20.  component: ProfileInfoPage,
21.  beforeEnter: [applicativeOne, applicativeTwo]
22.  },
23.  {
24.  path: '/profile/:id/edit',
25.  component: ProfileEditPage,
26.  beforeEnter: [applicativeTwo]
27.  },
28.  ]

In line with all other navigation guards, the return value of the executed function dictates what happens with navigation.

This route property is used when you need to apply a navigation guard to a limited number of routes, otherwise it makes more sense to use one of the global navigation guards.

[children](#contents.xhtml_sc3_233a)

The children property allows you to define nested routes and component hierarchies. One common practice is to have the URL structure, i.e., the segments, correspond to a set of nested components.

When building nested routes, the parent route is written as expected, i.e., as an absolute path (prefixed with a /), and each child is defined relative to this path (without the / prefix). This allows the router to build paths transparently and to utilize the nesting without having to manually build the URL for each child:

1.  const routes = [
2.  {
3.  path: '/profile'
4.  component: ProfilePage
5.  children: [
6.  {
7.  // /profile/info
8.  path: 'info',
9.  name: 'profile_info',
10.  component: InfoComponent
11.  },
12.  {
13.  // /profile/orders
14.  path: 'orders',
15.  name: 'profile_orders',
16.  component: OrderComponent
17.  }
18.  ]
19.  }
20.  ]

If you build a child route path beginning with a /, then the router will assume that this is a root path and treat it accordingly. This may or may not be what you want, but it will bypass the parent path definitions.

Each parent requires a route outlet to enable the respective child content to render.

There is, however, one small thing that hasn't been covered yet: how does the router know which path to use, and where does the router render the route output? For that, VueRouter supplies two handy little components: <router-link> and <router-view>.

[<router-link>](#contents.xhtml_sc3_234a)

The <router-link> component is used instead of the <a> tag (or any clickable tag) in your template; it generates the correct tag and URL content for you.

The component has a required to prop and a default slot. The prop accepts the following:

*   A string, which is the target path you want the user to navigate to.
*   An object, which holds either a path or name key and optional params, query, or hash objects that hold key-value pairs of the data required for the path builder.

The following shows various ways to use the <router-link> tag:

1.  // using a static string for path
2.  <router-link to="/users">Users</router-link>

4.  // using a JS string for path, note :to
5.  <router-link :to="/users">Users</router-link>

7.  // using an object with path property
8.  <router-link :to="{ path: '/users' }">Users</router-link>

10.  // using a named route -> /users
11.  <router-link :to="{ name: 'users' }">Users</router-link>

13.  // using a named route with parameters -> /users/9876
14.  <router-link :to="{ name: 'users', params: { id: 9876 }}">
15.  Users
16.  </router-link>
17.  // using a named route with query -> /users?id=9876
18.  <router-link :to="{ name: 'users', query: { id: 9876 }}">
19.  Users
20.  </router-link>

The default slot takes the content that you need to the <a> tag to wrap; it can be a simple string or a more complicated hierarchy of tags as below:

1.  <router-link :to="{ name: 'user', params: { id: 9876 }}">
2.  <i class="fas fa-user"></i>
3.  <span class="font-bold ml-1 text-lg">User</span>
4.  </router-link>

By default, the router-link component wraps the content supplied in an <a> tag. If you want to change the tag that gets rendered, you need use the custom prop and supply the output tags required.

When using custom, it is necessary to access the v-slot customization API. Here, you gain access to the href (the resolved URL), the route object, a navigate event handle (the function that is triggered on the associated event), and the isActive and isExactActive properties (for applying CSS classes), see following:

1.  <router-link
2.  :to="{ name: '' }"
3.  custom
4.  v-slot="{ href, route, navigate, isActive, isExactActive }"
5.  >
6.  <ListElement
7.  :active="isActive" :href="href" @click="navigate"
8.  >
9.  {{ route.fullPath }}
10.  </ListElement>
11.  </router-link>

In essence though, you'd use <router-link/> wherever you need to place a navigation item. If you set up your routing definitions with names, then you're going to prevent yourself and your co-workers from severe maintenance headaches when you need to change routing information.

When we get to updating the sample application, we'll use named routes.

Now that we've discussed how to build hyperlinks with Vue.js, we're going to explore where the content that the target component renders for the user to see. To do that, we're going to cover the <router-view> component.

[<router-view>](#contents.xhtml_sc3_235a)

The router-view is the place in the template where the routes output is placed when rendering. It's called the route outlet.

You need a route outlet in every parent template; this is the application entry point component, plus any components where the route definition contains a children property.

As discussed earlier, any route definition can have more than one output component defined, so long as all but one of the route outlets or views are named. The unnamed or default view should define where the application main content sits, but this needn't always be the case. The way your route outlets are designed, like the route definitions, is dictated by project requirements and in-house style.

Typically, in a small application or brochure-ware, where the navigation is flat, i.e., all the “page” components output at the same HTML level, you'll probably only need one template with a default <router-view>. The following listing shows this at the most basic level:

1.  <template>
2.  <router-view></router-view>
3.  </template>

Complex, real-world application builds with dynamic component outputs and tailored navigation schemes will require a combination of named <router-view>s and child <router-view>s, which might also be named, as shown in the following example:.

1.  <template>
2.  <div class="flex justify-around">
3.  <!-- named view -->
4.  <router-view name="NavigationSideBar" class="w-1/3"></router-view>
5.  <!-- default view -->
6.  <router-view></router-view>
7.  </div>
8.  </template>

Although <router-view> does most of the work, all you really need to care about is ensuring that each parent template has the right number of <router-view> elements in it, otherwise your content won't display.

[Updating the project: changing <a/> tags to router-link](#contents.xhtml_sc2_236a)

The first thing we'll need to do is add the VueRouter to the project and create the routing scheme.

Let's add the VueRouter to the project:

1.  $ npm install vue-router@٤

Then, we'll set it up in main.ts:

1.  import { createApp } from 'vue'
2.  import { createRouter, createWebHistory } from 'vue-router'
3.  import routes from './routes/index.ts'
4.  import App from './App.vue'
5.  import './assets/index.css'

7.  const router = createRouter({
8.  history: createWebHistory(),
9.  routes
10.  })

12.  const app = createApp(App)

14.  app.use(router)
15.  app.mount('#app')

We've already told main.ts that it can find the router definition at ./routes/index.ts, so we'll need to add that file to the project and put the following content in it:

1.  import { RouteRecordRaw } from 'vue-router'

3.  const routes: RouteRecordRaw[] = []

5.  export default routes

With this file in place, we can start adding routing definitions.

Firstly, we'll add some wrapper templates; these will hold the common navigation elements when complete, but for now, they'll just hold the route outlet in the template section so that the pages can render.

Add these imports to the import section at the top of the ./routes/index.ts file:

1.  import { RouteRecordRaw } from 'vue-router'

3.  // Page Wrappers
4.  import FullPageWrapper from '../components/layouts/page_wrappers/FullPage.vue'
5.  import SlimPageWrapper from '../components/layouts/page_wrappers/SlimPage.vue'
6.  import ProfileWrapper from '../components/layouts/page_wrappers/ProfileWrapper.vue'

8.  ... Rest of file ...

With these imports now in place, we can add the first route definitions as follows:

1.  const routes: RouteRecordRaw[] = [
2.  {
3.  path: '/',
4.  component: FullPageWrapper,
5.  children: []
6.  },
7.  {
8.  path: '/',
9.  component: SlimPageWrapper,
10.  children: []
11.  },
12.  {
13.  path: '/profile',
14.  component: ProfileWrapper,
15.  children: []
16.  }
17.  ]

As you can see here, we're using the children property. To make these work as expected, we need to create a file at each of the import locations:

1.  components/layouts/page_wrappers/FullPage.vue
2.  components/layouts/page_wrappers/SlimPage.vue
3.  components/layouts/page_wrappers/ProfileWrapper.vue

And add the following content to each:

4.  <template>
5.  <router-view></router-view>
6.  </template>

Now, we'll add the nested route definitions, first to the children array that sits under the FullPageWrapper. Firstly we are going to add all the required imports, as below:

1.  ... Previous imports ...
2.  // Site Page Components
3.  import LandingPage from '../components/pages/site/landing-page/LandingPage.vue'
4.  import MenuPage from '../components/pages/site/menu-page/MenuPage.vue'
5.  import ItemPage from '../components/pages/site/item-page/ItemPage.vue'
6.  import CheckoutPage from '../components/pages/site/checkout-page/CheckoutPage.vue'
7.  ... Rest of file ...

Now we add the actual routing definitions:

1.  ... Previous contents ...
2.  {
3.  path: '/',
4.  component: FullPageWrapper,
5.  children: [
6.  {
7.  path: '',
8.  name: 'home',
9.  component: LandingPage
10.  },
11.  {
12.  path: 'menu',
13.  name: 'menu',
14.  component: MenuPage
15.  },
16.  {
17.  path: 'item/:id',
18.  name: 'item',
19.  component: ItemPage
20.  },
21.  {
22.  path: 'checkout/:basket',
23.  name: 'checkout',
24.  component: CheckoutPage
25.  }
26.  ]
27.  },
28.  .. Rest of file ...

The following two nested template sections utilize the same pattern, which has been condensed in the following listing:

1.  ... Previous file contents ...

3.  import LogInPage from '../components/pages/site/login-page/LogInPage.vue'
4.  import LogOutPage from '../components/pages/site/login-page/LogOutPage.vue'
5.  import RegistrationPage from '../components/pages/site/registration-page/RegistrationPage.vue'

7.  // Profile Page Components
8.  import ProfileInfoPage from '../components/pages/profile/info-page/ProfileInfoPage.vue'
9.  import ProfileOrdersPage from '../components/pages/profile/orders-page/ProfileOrdersPage.vue'

11.  const routes: RouteRecordRaw[] = [
12.  ...
13.  {
14.  path: '/',
15.  component: SlimPageWrapper,
16.  children: [
17.  {
18.  path: 'login',
19.  name: 'login',
20.  component: LogInPage
21.  },
22.  {
23.  path: 'logout',
24.  name: 'logout',
25.  component: LogOutPage
26.  },
27.  {
28.  path: 'register',
29.  name: 'register',
30.  component: RegistrationPage
31.  }
32.  ]
33.  },
34.  {
35.  path: '/profile',
36.  component: ProfileWrapper,
37.  children: [
38.  {
39.  path: '',
40.  name: 'profile_info',
41.  component: ProfileInfoPage
42.  },
43.  {
44.  path: 'orders',
45.  name: 'profile_orders',
46.  component: ProfileOrdersPage
47.  }
48.  ]
49.  }
50.  ]

52.  ...

If you still have the application running, when you save this file and check the browser, don't be surprised if all you get is a white page; we haven't put the new referenced files in place yet.

Fixing this issue is surprisingly easy. All we need to do is drop empty placeholder files in the directory locations that we told the router the components would be in:

1.  components/pages/site/landing-page/LandingPage.vue
2.  components/pages/site/menu-page/MenuPage.vue
3.  components/pages/site/item-page/ItemPage.vue
4.  components/pages/site/checkout-page/CheckoutPage.vue
5.  components/pages/site/login-page/LogInPage.vue
6.  components/pages/site/login-page/LogOutPage.vue
7.  components/pages/site/registration-page/RegistrationPage.vue
8.  components/pages/profile/info-page/ProfileInfoPage.vue
9.  components/pages/profile/orders-page/ProfileOrdersPage.vue

With these files in place, the landing page of the sample site will render; check it out.

[VueRouter navigation guards](#contents.xhtml_sc2_237a)

The per-route guard, beforeEnter, is not the only guard type that is available to protect your routes; there are also global and in-component navigation guards.

Whenever a navigation event is triggered, VueRouter runs through a navigation resolution flow that is quite similar to the Vue life cycle hooks.

The sequence is as follows:

1.  Navigation event triggered
2.  beforeRouteLeave() called on deactivated components
3.  beforeEach() global guards called
4.  beforeRouteUpdate() called in all reused components
5.  Route configured beforeEnter() called
6.  Async route components resolved
7.  beforeRouteEnter() called in new components
8.  global beforeResolve() guards called
9.  Navigation confirmed
10.  afterEach() global guards called
11.  DOM updated
12.  next() callbacks triggered in beforeRouterEnter()

Each navigation guard is given two arguments: to – the navigation target and from – the originating page. Optionally, there is a third argument, i.e., next(); although it can be used multiple times in a function, it can only be called once in any particular path in a guard. You will need to be careful with your logic if using next(), otherwise you'll end up with your guard never resolving.

Navigation guards work on the principle of failing early, so if a guard returns nothing, true or undefined, it is accepted as valid, and the navigation is allowed to continue through to either the next navigation guard or the next step in the navigation resolution flow.

However, if any guard returns false, the navigation event is canceled.

Should a navigation guard return a route location object then the navigation will be redirected to the returned path and the navigation resolution flow restarted against the new endpoint.

Lastly, if the guard throws an Error, then the navigation is canceled and the router.onError() callback is called to resolve the issue.

[Navigating by code](#contents.xhtml_sc2_238a)

You will often need to manage navigation based on component state or events, from data store actions or from error states The router has a simple API that allows you to do just that, by providing three functions: push(), replace() and go(). The router API also has several other functions, but these three are, by far, the most important.

The method of accessing the router depends on which components API you're using to be your component.

If you're using the Options API, then the router is automatically exposed to your component as $router, so you would use this.$router. See the following as an example:

1.  <script lang="ts">
2.  export default {
3.  methods: {
4.  eventHandler: function (evt) {
5.  this.$router.push({ name: 'pathName' })
6.  }
7.  }
8.  }
9.  </script>

The Composition API requires you to use the useRouter() composable in the <script setup> part of your component, as below:

1.  <script setup lang="ts">
2.  import { useRouter } from 'vue-router'

4.  const router = useRouter()
5.  router.push({ name: 'pathName' })
6.  </script>

Front-end navigation with VueRouter manipulates the current history stack to enable full integration with in-browser controls, like the back button.

[push()](#contents.xhtml_sc3_239a)

The push() function pushes a new entry onto the history static, which enables browser back button functionality so that the user experience is maintained.

The push() method is the internal call made by the <router-link /> component. It accepts all the same parameters as you would expect to apply to the to prop.

1.  // Replace router with this.$router if using Options API

3.  // Using a path
4.  // same as <router-link to='stringPath' />
5.  router.push('stringPath')

7.  // Using a routing object - params are ignored
8.  // if used with the path key
9.  // same as <router-link :to="{ path: 'stringPath' }" />
10.  router.push({ path: 'stringPath' })

12.  // Using a  named route
13.  // same as <router-link 
14.  //   :to="{ name: 'pathName', params: { key: 'value' }}" 
15.  // />
16.  router.push({ name: 'pathName', params: { key: 'value' }})

[replace()](#contents.xhtml_sc3_240a)

replace() is similar to push(); it differs, however, by replacing the last entry in the history stack rather than pushing the entry onto it.

This is analogous to <router-link replace />:

1.  // Replace router with this.$router if using Options API

3.  // Using a path
4.  // same as <router-link to='stringPath' replace/>
5.  router.replace('stringPath')

7.  // Using a routing object - params are ignored
8.  // if used with the path key
9.  // same as <router-link :to="{ path: 'stringPath' }" replace/>
10.  router.replace({ path: 'stringPath' })

12.  // Using a  named route
13.  // same as <router-link 
14.  //   :to="{ name: 'pathName', params: { key: 'value' }}" 
15.  //   replace
16.  // />
17.  router.replace({ name: 'pathName', params: { key: 'value' }})

replace() changes the navigation entries and therefore, can have a jarring effect on user experience when using the browser provided controls.

[forward()/back()/go()](#contents.xhtml_sc3_241a)

These three methods allow you to manipulate where you are in the history stack:

*   forward() moves you to the next entry.
*   back() moves you to the previous entry.
*   go(n) accepts a signed integer and moves you to the entry relative by the given number.

If the requested entry doesn't exist in the history stack, the navigation silently fails, and the navigation attempt is abandoned. The listing below gives some examples on how to use the router composable:

1.  // Replace router with this.$router if using Options API

3.  // move forward one position in history stack
4.  router.forward()
5.  router.go(1)

7.  // move back one position in history stack
8.  router.back()
9.  router.go(-1)

11.  // using go(n) to go forward 10 spaces
12.  router.go(10)

14.  // using go(n) to go backwards 5 spaces
15.  router.go(-5)

This API mirrors the browser's own History API (pushState(), replaceState() and go()), so if you are familiar with this API, then manipulating the history state with VueRouter will be very simple.

[Final thoughts](#contents.xhtml_sc2_242a)

The VueRouter is simple to add and use, but the underlying functionality allows you to make the routing definition in your application as complex, comprehensive, and flexible as is necessary.

The definition is, in itself, composable; you can segregate it into sections along meaningful boundaries in order to facilitate maintenance. We haven't done it in this chapter; that is, an exercise for you to complete should you so wish; it has no effect on the user experience.

[Conclusion](#contents.xhtml_sc2_243a)

In this chapter, we explored front-end routing as a concept and then discussed how to integrate and use the VueRouter in your projects. We then went through the sample application and updated it to use a VueRouter. Lastly, we looked at programmatic navigation.

In the next chapter, we will discuss how to manage user interactions with the UI using the Vue.js events system and how to get your components to react to user and custom events to create reactive and responsive UIs.

[Points to remember](#contents.xhtml_sc2_244a)

*   Once imported, you need to remember to use the router to make it available application wide.
*   It's more maintainable in the long term if you give your routes names; this way, you can manage the application paths in one place, with minimal disruption to the application.
*   The routing definition can have children nested as deeply as necessary; the developer must ensure that there are sufficient router outlets in the component hierarchy for all the children to be rendered correctly.
*   Use navigation guards to protect routes, but only where necessary. It is sometimes better to build small single-purpose guards and reuse them where appropriate, rather than building a set of global guards that are applied to every navigation event.
*   If the target component contains named views, then there are multiple router outlets in the template, the routing definition must use the components key. If the component only uses the default outlet, then it uses the component key.
*   The router maps paths to components; it can sometimes be easier to prototype a simple router using named routes and build out specifics afterward than to design a comprehensive routing scheme upfront.

[Key terms](#contents.xhtml_sc2_245a)

*   Front-end routing
*   Routing definition
*   Router outlet
*   <router-link>
*   <router-view>
*   Programmatic navigation
*   Route Path
*   Named routes
*   Nested routing
*   Wrappers
*   Named views

Join our book’s Discord space

Join the book's Discord Workspace for Latest updates, Offers, Tech happenings around the world, New Release and Sessions with the Authors:

**[https://discord.bpbonline.com](https://discord.bpbonline.com)**

![](images/fm1.png)

# [CHAPTER 11Interacting with the UI Using Events](#contents.xhtml_ch11a)

[Introduction](#contents.xhtml_sc2_246a)

So far, we have built an application with single page and a routing scheme with all the power at our collective fingertips. In this chapter, we are going to add a few more pages and some interactivity. Throughout this chapter, we going to build a solid foundation of how to create and manage events using Vue.js.

[Structure](#contents.xhtml_sc2_247a)

This chapter will cover the following topics:

*   Events in Vue.js
*   Triggering and handling events
*   How to create custom events
*   Emitting and passing events around
*   Handling child to parent communication
*   Handing communication through an event bus and the problems this solves

[Objectives](#contents.xhtml_sc2_248a)

In this chapter, we are going to be discussing events. Firstly, we'll look at what they are and how Vue.js sees them. We'll then cover the different types of events that can be used, where it is appropriate to use them, and the problems that might be encountered when using them.

We'll be building out parts of the sample application throughout this chapter as we put into practice the theory that will be covered.

As we will want to concentrate on the event code throughout, we'll leave it up to you, the reader, how you want to get the HTML/CSS code that will scaffold the pages we're going to be interested in. There is enough information in [Chapter 5](#ch05.xhtml), Designing Component-Based UIs and Single Page Applications for you to be able to do that if you wish. Otherwise, just use the code samples that come with the book.

[Events in Vue.js](#contents.xhtml_sc2_249a)

An event is the response to an action, performed by either the user or by another part of the code. Events can be handled or passed up the component hierarchy.

In Vue.js, there are two types of events to which the framework can respond: DOM events (like click or change) and custom events.

From a code point of view, both types of events are represented by some JSON that holds the type of event that has been triggered, any data associated with that trigger, and the event meta data. In that respect, Vue.js events and HTML DOM events are sent (triggered) and handled in very similar manners.

Events that require handling are bound using either the v-on: prefix or the @ shortcut syntax written as an attribute in the HTML template. This, and adding handlers, is covered in the next section.

[Triggering and handling standard DOM events](#contents.xhtml_sc2_250a)

A standard DOM event is triggered in response to a user action – clicking a button, making a change in a form control, moving a slider, and so on. All the standard DOM events that a browser should understand are available. The most common events used include the following:

*   Click
*   Change
*   <event> etc.

To handle a standard DOM event, you need to add an event handler. An event handler is simply a function that has been added to the methods section of your Options API component, as follows:

1.  <template>
2.  <button value="Click me" @click="handle_click" />
3.  </template>

5.  <script>
6.  export default {
7.  methods: {
8.  handle_click: function (evt) {
9.  console.log('You clicked me')
10.  }
11.  }
12.  }
13.  </script>

If you're using the Composition API, then the event handler will need to be added to either the script setup, as shown in the following listing, or as an additional method in an optionally added script section (not shown):

1.  <template>
2.  <button value="Click me" @click="handle_click" />
3.  </template>

5.  <script setup>
6.  function handle_click (evt) {
7.  console.log('You clicked me')
8.  }
9.  </script>

Passing the triggered event into the handler is optional; if your handler function has been written without accepting an argument, the event information is silently dropped, as in the following:

1.  <template>
2.  <button value="Click me" @click="handle_click" />
3.  </template>

5.  <script setup>
6.  // the event is not being used, so no need
7.  // to pass it in
8.  function handle_click () {
9.  console.log('You clicked me')
10.  }
11.  </script>

Event handlers for standard DOM events can be used to trigger additional events, both DOM or more commonly, custom events, as necessary.

Let's start putting this information into action in our sample project – the best way to understand is to do. We'll look at the MenuPageComponent (/components/pages/site/menu-page/MenuPage.vue). If you check against the design of this page in [Chapter 5](#ch05.xhtml), Designing Component-Based UIs and Single Page Applications , you can see that we'll need to provide events for all of the user interactions on each item in the product listing, and the events required to work the SideBarComponent.

The menu list component requires the following events, as deduced from the design, to be added to enable data collection and user interactions:

*   incrementCount: To increase the number of items to add to the order
*   decrementCount: As for the preceding one, but in reverse
*   addToCart: Add the chosen item and quantity to the cart

To help with this, the source code bundle provides a useCart composable (src/composables/useCart.ts) to provide basic shopping cart facilities. This simple composable just provides an interface to manage the data; we'll flesh it out more when we look at Pinia.

If you haven't obtained the source code bundle, now is a good time to do that and come back here.

At this point, we're going to change the button starting on line 8 in the source. Update it with the following change; see line 4 in the listing as follows:

1.  <button
2.  type="button"
3.  class="mr-1 relative inline-flex items-center 
    space-x-2 px-2 py-1 border text-sm font-medium 
    rounded-l-md red-button-sm"
4.  @click="incrementCount"
5.  >

This adds the @click handler and tells you that it uses the incrementCount() function to handle the event if it is triggered.

As an exercise, try and write the handler yourself first. It needs to be able to increment the value held in the itemCount reference.

If you got stuck, or are just interested, here is one possible solution:

1.  let itemCount = ref(١)
2.  const incrementCount = () => itemCount.value++

With this in place, let's look at adding another event handler:

1.  <button
2.  type="button"
3.  class="ml-1 relative inline-flex items-center 
    space-x-1 px-2 py-1 border text-sm font-medium 
    rounded-r-md red-button-sm"
4.  @click="decrementCount"
5.  >

This button does the opposite of the increment button, but it doesn't allow the user to add less than one item when they press the button:

1.  const decrementCount = () => {
2.  if (itemCount.value > 1) {
3.  itemCount.value -= 1
4.  }
5.  };

The code here is not all that complicated and should be self-explanatory.

The last event that we're going to add is to handle the click event of the addToCart button:

1.  <button type="button" class="red-button-sm ml-4" @click="addToCart">
2.  Add to Cart
3.  </button>

Here, we want to take our item data and merge it with the quantity data to create an entry in the cart items list. Luckily, we can delegate the actual injection into the cart to the useCart composable:

1.  import { useCart } from "../../composables/useCart";

3.  type Item = {
4.  id: number;
5.  image: string;
6.  description?: string;
7.  name: string;
8.  price: number;
9.  };

11.  const props = defineProps<{ item: Item }>();

13.  const { addItem } = useCart();

15.  function addToCart() {
16.  addItem({
17.  id: props.item.id,
18.  name: props.item.name,
19.  price: props.item.price,
20.  qty: itemCount.value,
21.  extras: [],
22.  });
23.  }

With these event handlers in place, we're going to add a few to the cart display at the side of the page. The first will allow us to remove an item from the cart:

1.  <button
2.  type="button"
3.  class="text-xs font-medium text-red-600 hover:text-red-500"
4.  @click="remove(item.id)"
5.  >

This handler is, again, just a simple wrapper around functionality provided by the useCart composable, detailed as follows, plus the handler for the cancel event:

1.  <script setup lang="ts">
2.  import { useCart } from "../../../composables/useCart";
3.  import type { Cart } from "../../../composables/useCart";

5.  const { subtotal, tax, delivery, total, updateCart, removeItem } = useCart();

7.  const cart: Cart = updateCart([
8.  // initial cart data
9.  ]);

11.  const cancel = () => updateCart();
12.  const remove = (id: number) => removeItem(id);

14.  function addExtras(id: number) {
15.  // we'll add this as a transition
16.  }
17.  </script>

The last handler we're going to add at this point is the cancel event:

1.  <a href="#"
2.  class="text-red-400 font-medium hover:text-red-600"
3.  @click="cancel"
4.  >

The code for this has already been added in the previous listing.

Each of the handlers covered here is quite simple. They all defer the processing to something else. This is a common pattern; the UI handles the interactions, but the data processing is moved out to a service or composable. Data management is then abstracted away into either a datastore, like Pinia, or transferred to a server by an API.

[Creating custom events](#contents.xhtml_sc2_251a)

In addition to writing handlers for the standard HTML DOM events, you can create your own events. These events are usually passed into child components to handle data being passed back up the DOM hierarchy to a parent, due to the single direction of data binding.

To create a custom event, you bind a name (the name you want to give the event) and a handler; you can do this with either the v-on: binding or the @ shortcut, as you would any other event.

This shall be covered in the following sections.

[Communication between parent and child components using custom events](#contents.xhtml_sc2_252a)

Parent components can pass data to their immediate children using props, so getting data throughout a component hierarchy is relatively easy, especially in conjunction with provide/inject. This is easy because it is the natural way for components to behave; parents tell their children what to do.

Getting data from a child component back into a parent component is a little more difficult. This requires the child to emit (using the $emit method) an event to pass any data to the required handler in the parent.

Note: Custom events do not propagate through the entire hierarchy, i.e. they do not bubble, so must be handled by their direct parent.

In the following example, we'll have a typical parent-child hierarchy; the child component will emit an event for the parent to handle:

1.  // Child Component - using $emit from template
2.  <template>
3.  <button @click="$emit('sendMessage')">Click Me</button>
4.  </template>

6.  // OR

8.  // Child Component - using a method
9.  <template>
10.  <button @click="clickHandler">Click Me</button>
11.  </template>

13.  <script setup>
14.  const emit = defineEmits(['sendMessage'])

16.  function clickHandler() {
17.  emit('sendMessage')
18.  }
19.  </script>

When using this child component from a parent, you set up the event handler as follows:

1.  // Parent Component, using @
2.  <template>
3.  <child-component @send-message="handleChildEvent" />
4.  </template>

6.  <script setup>
7.  function handleChildEvent() {
8.  console.log('handling event')
9.  }
10.  </script>

If any data is required to be sent, it is done as part of the call to the handler, just like any of the built-in events; you are just invoking a callback after all – see line 3 in the following:

1.  // Child Component
2.  <template>
3.  <button @click="$emit('sendMessage', 'This is the sent message')">Click Me</button>
4.  </template>

6.  // Parent Component
7.  <template>
8.  <child-component @send-message="handleChildEvent" />
9.  </template>

11.  <script setup>
12.  function handleChildEvent(message) {
13.  console.log(message)
14.  }
15.  </script>

Using custom events is a simple proposition as it leverages the Vue.js event mechanism.

[Defining and validating events](#contents.xhtml_sc2_253a)

In order to document your custom events properly, Vue.js provides a defineEmits() macro, which can be used like defineProps().

defineEmits() can accept a simple list, which just states what events are available, as follows:

1.  <script setup>
2.  const emit = defineEmits(['custom-event-1', 'custom-event-2'])
3.  </script>

We can also provide defineEmits() with an object, as done in the following listing:

1.  <script setup>
2.  const emit = defineEmits({
3.  // define event with no validation
4.  'custom-event-1': null,

6.  // return boolean for validation status
7.  'custom-event-2': (...args) => {
8.  if (areValid(args)) {
9.  return true
10.  } else {
11.  return false
12.  }
13.  })
14.  </script>

This object can be used for validation by providing a function that receives the arguments provided to the emit call and is required to return a Boolean, which, if true, allows the event to continue. Otherwise, the emit is cancelled.

When using TypeScript, you can also define the emits using type declarations:

1.  <script setup>
2.  const emit = defineEmits<{
3.  e: 'custom-event-1': void
4.  e: 'custom-event-2', args: type): boolean
5.  }>()
6.  </script>

[Emitting events and passing data around](#contents.xhtml_sc3_254a)

In the main, composables have eliminated the need to rely on passing custom or DOM events around. The composable manages the application state that is passed to it from the DOM event handler. We looked at this previously in the code examples injecting the useCart composable into the MenuPageComponent. Creating code in this way reduces the amount of coupling between components.

There are occasions where the components need to have a higher degree of coupling between a parent and child component or building a composable makes little sense because there is no particular concern that can be extracted for reuse. In these circumstances, there is little choice but to use events to get child data into its parent, if this is a requirement.

[Communication through an event bus and the problems that it solves/creates](#contents.xhtml_sc3_255a)

In the main, events are handled by the component that triggers the event or its immediate parent. On occasion, however, an event emitted or triggered in a nested component is needed to affect the data in a component, or components, outside the triggering components hierarchy. Or maybe you need centralized event management to pass the event to multiple components.

To do this, we need a global event bus, or some form of application-wide state management. Current best practice is to use Pinia for this task. We will cover Pinia in [Chapter 13](#ch13.xhtml), Managing State With Pinia and API Communication.

The main reason for this is that creating a global event bus is generally discouraged. They can be useful for small projects or prototypes, but in larger or longer-term projects, they can become a source of maintenance issues.

If, however, you are tasked with maintaining an older, Vue2, application that uses a global event bus, then setting one up and using it is shown in the following example code. Code like this is no longer considered best practice.

In the main.js file, create and export a new Vue instance:

1.  // Vue2
2.  export const eventBus = new Vue()

4.  // Vue3 - using mitt microbus
5.  import mitt from 'mitt'
6.  const eventBus = mitt()
7.  app.config.globalProperties.eventBus = eventBus

Using the event bus depends on the version of Vue that you're using; for Vue 2, events can be handled through the $emit, $on and $off methods of the event bus:

1.  // Vue2 - emitting the event
2.  <script>
3.  import { eventBus } from '/main'

5.  export default {
6.  methods: {
7.  eventHandler() {
8.  eventBus.$emit('event-name', eventData)
9.  }
10.  }
11.  }
12.  </script>

14.  // Vue2 - handling emitted event
15.  <script>
16.  import { eventBus } from '/main'

18.  function eventHandler(eventData) {
19.  ...
20.  }

22.  eventBus.$on('event-name', eventHandler)
23.  </script>

With Vue3, as the event bus is globally registered, it can be accessed directly in the instance, as follows:

1.  // Vue3 – handling component
2.  <script>
3.  export default {
4.  created () {
5.  // handling the event
6.  this.eventBus.on('event-name', (evt) => {
7.  ...
8.  }
9.  },
10.  </script>

12.  // Vue3 – emitting component
13.  <script>
14.  methods: {
15.  eventEmit() {
16.  // emitting the event
17.  this.eventBus.emit('event-name', data)
18.  }
19.  }
20.  }
21.  </script>

Remember that this type of event bus is discouraged. As you can see, event handlers can be anywhere in the component hierarchy, which makes maintenance difficult when there are many components. The approach is very brittle.

The better way is to use Pinia, which centralizes event handling and provides a standard way to emit events and manage application state.

If the functionality can be extracted as a singular concern, then a composable is usually the best option.

[Conclusion](#contents.xhtml_sc2_256a)

Vue.js makes handling events very simple. The framework provides a myriad of options to handle data between components.

In this chapter, we explored several ways of creating and using events, and we also touched on some older practices and discussed why they are no longer necessary or used as best practices. We continued our discussion and understood the modern ways of building event handlers, including when to use composables to handle data and/or component state. Part of this understanding was based on the practical experience of building events into the sample application.

In the next chapter, we will explore forms, form components, and data validation in detail. When building forms, events are used extensively, both for handling the form state for managing validations and for interacting with the user to provide necessary feedback if issues occur.

[Points to remember](#contents.xhtml_sc2_257a)

*   DOM Events: All standard DOM events are set up in the template using the @ syntax linking the event to a handler. These events are provided by the framework to enable you to handle all standard events.
*   Custom Events: Custom events are used to manage data transfer between parent and child components. It is sometimes better to use a composable or an application management layer like Pinia.
*   Global Event Bus: Using a global event bus in Vue applications is discouraged. There are better solutions available to solve the problem of sending events or data throughout the component hierarchy. You might, however, come across this pattern if you're maintaining older Vue.js applications.

[Key terms](#contents.xhtml_sc2_258a)

*   DOM Event
*   Custom Event
*   Global Event Bus
*   Handler
*   Emitter
*   Application State Layer
*   Composable
*   Trigger
*   @click
*   @change
*   @submit
*   @eventName
*   v-on:eventName

Join our book’s Discord space

Join the book's Discord Workspace for Latest updates, Offers, Tech happenings around the world, New Release and Sessions with the Authors:

**[https://discord.bpbonline.com](https://discord.bpbonline.com)**

![](images/fm1.png)

# [CHAPTER 12Building Forms and Handling User Input](#contents.xhtml_ch12a)

[Introduction](#contents.xhtml_sc2_259a)

So far, we have covered designing and building components, linking pages together and handling events. Where we are missing something is collecting data from our users. This data can be in many guises, but it all needs managing somehow.

This is the last chapter on core functionality; from the next chapter onward, we will be looking at tools in the wider Vue.js ecosystem to make building applications easier.

[Structure](#contents.xhtml_sc2_260a)

We will be covering the following topics in this chapter:

*   Value binding and v-model
*   Creating forms and using form components
*   v-model modifiers
*   Handling form data and data validation
*   Using v-model with Components

[Objectives](#contents.xhtml_sc2_261a)

In this chapter, we will explore handling user data at a component level; this means collecting, validating, and if necessary, passing it to other parts of the application. Once we understand how Vue.js sees data, we can start working with the various form controls that are supplied by HTML and enhanced by Vue to build dynamic forms and delight our users.

A part of this chapter will look at enhancing the Speedy Pizza prototype application with our newly learned tools.

[Value Binding and v-model](#contents.xhtml_sc2_262a)

For Vue.js to understand that you want to use data, you need to bind a value. In Vue2, this was through the data option in the options model; in Vue3, it's much easier: just use either the reactive() or the ref() function when specifying the data. This is just the simple value binding that you're already used to.

To use this data in a form control, however, Vue.js provides a simple helper attribute v-model.

When you add v-model to a control, Vue.js sets up a getter and an event handler in the background; this allows it to transparently handle data changes.

This helper attribute makes Vue.js create the code presented in the following listing transparently, which gets attached to the control:

1.  // simple text input (v-model attr)
2.  <input type="text" v-model="dataValue" />
3.  // simple text input (binding requirements without v-model)
4.  <input type="text" :value="dataValue" @input="event =>
     dataValue = event.target.value" />
5.  // checkbox (v-model attr)
6.  <input type="checkbox" v-model="dataValue" />
7.  // checkbox (binding requirements without v-model)
8.  <input type="checkbox" :checked="dataValue" @change="event =>
     dataValue = event.target.value" />
9.  //select (v-model attr)
10.  <select v-model="dataValue"><option>…</option></select>
11.  // select (binding requirements without v-model)
12.  <select :value="dataValue" @change="event => dataValue 
    = event.target.value"><option>…</option></select>

As you can probably tell, using v-model makes the code much easier to read and understand; plus, it uses the correct value and update events to manage the component data for you.

Note: If your user base requires an Input Method Editor (IME), i.e., they're Chinese, Japanese, or Korean, among others, then using v-model will not work. You'll need to supply your own input event listener and value binding as the v-model doesn't update during IME composition. This is a noted and known limitation in the Vue.js documentation.

It is, however, important to understand how the v-model works behind the scenes, which you'll see when we look at how it can be used to create custom form components in the Using v-model with Components section later in this chapter.

[Creating forms and using form components](#contents.xhtml_sc2_263a)

In a traditional web form, you'd have HTML that could look somewhat like the following code example:

1.  <form method="post" action="serverUrl" enctype="multipart/form-data" autocomplete="on">
2.  <input type="hidden" name="hiddenValue" value="value" />
3.  <fieldset>
4.  <legend>Enter your details</legend>
5.  <label for="firstname">First Name</label>
6.  <input type="text" name="firstname" id="firstname" 
    class="form-control" />
7.  <label for="lastname">Last Name</label>
8.  <input type="text" name="lastname" id="lastname" 
    class="form-control" />
9.  <input type="submit" value="Send Details" />
10.  </fieldset>
11.  </form>

With a form like this, you'd have to do a full HTTP post-back or use JavaScript to intercept the submit and then perform processing and/or call to a remote resource, usually but not limited to an AJAX service.

With the v-model and the events system, if you need a piece of data from the user, you can just set up the form elements you require. You don't need to use the form tag at all if it's not necessary, although sometimes it makes sense to semantically mark something as a form if it's needed by the CSS framework you're employing.

The following code examples cover a common set of use cases that you'll encounter when needing user data.

The first example concerns just a simple form element to collect a single piece of data – for this type, just place the required form field and bind the required variable – usually a ref or reactive via the v-model attribute, as discussed earlier.

1.  <template>
2.  <!-- component content -->
3.  <input v-model="value" />
4.  <!-- component content -->
5.  </template>

7.  <script setup lang="ts">
8.  import { ref } from 'vue'
9.  const value = ref('')
10.  </script>

This approach also works for multiple form fields – you've already seen that in action. And this is enough for most instances of data collection, but it can become impractical for larger forms.

Even though it's seen as bad UX, sometimes, especially in business or corporate environments, access to significant amounts of data for entry or editing can result in quite large forms with many dynamic or moving parts.

There are a few ways that can be used to deal with this problem:

*   Wrap the form data in reactive(), rather than many individual ref(), to model the data of the entire form; this has the advantage of grouping all the data together, and it also makes the model of the page really large and potentially unwieldy.
*   Break the form down into separate components (on the same “page”), and have the data passed in through the props mechanism and send back data changes by emitting events; we'll cover how to build components for this later in the chapter.
*   Design data and/or navigation flows to limit access to data and form elements. This “wizard” type build results in better UX but is a lot more work to build initially. The benefit here is maintenance and extensibility.

Depending on corporate culture, how this data is managed in the UI can be up to either you as the developer, the development team as a whole, or some other part of the business, i.e., business analysts, UX designers, or data/information designers.

[v-model modifiers](#contents.xhtml_sc2_264a)

The v-model object supplies three modifiers that allow you to modify how the v-model attribute behaves at the field level, before any formal validation. These three modifiers are lazy, trim, and number.

One question you might have at this point is, “Why have modifiers at all?” The modifiers themselves perform basic operations, the specifics of which we'll discuss as we move on, but in the general case, they make life a little simpler and reinforce the declarative nature of the framework itself.

[.number](#contents.xhtml_sc3_265a)

The number modifier is there to coerce the data value collected in the field from a string (which is the standard data type of all fields) to a number type, unless the given value cannot be converted using parseFloat(),  in which case the modifier returns the string unchanged. If you're using a type="number" input, then this modifier is applied automatically by Vue.js.

The following code listing shows a few scenarios where you might use the number modifier in your template code:

1.  <!-- using number modifier on a text control -->
2.  <input type="text" v-model.number="data" />
3.  <!-- not required for type="number" -->
4.  <input type="number" v-model="data" />

[.trim](#contents.xhtml_sc3_266a)

The trim modifier is a simple wrapper around the JS trim function; it just removes any white space from around the v-model data automatically.

Its usage should generally be limited to fields where you're expecting multi-line data, but it can be added to any field as a catchall.

The following code listing show how to apply it to a v-model attribute:

1.  <!-- trimming whitespace from a text input -->
2.  <input type="text" v-model.trim="data" />
3.  <!-- trimming whitespace from a textarea -->
4.  <textarea v-model.trim="data"></textarea>

[.lazy](#contents.xhtml_sc3_267a)

The lazy modifier is by far the most interesting. Usually, the v-model updates with each input event (except if IME composition is used, as described earlier). If you've got a costly operation that needs to be executed when the data in the field changes, you don't necessarily want it to change on every keypress event. This is where the lazy modifier comes in: it only syncs the data to the v-model on the field change event, so these costly operations are limited to fire when the field changes.

Like the other modifiers, .lazy is written after the v-model attribute, as follows:

1.  <!-- sync on change not on input event -->
2.  <input type="number" v-model.lazy="data" />

Modifiers are chainable, so you can apply more than one (or all of them) to a form fields v-model, if necessary, as shown in the following example:

1.  <!-- applying modifiers in chain -->
2.  <input type="text" v-model.lazy.trim.number="data" />

The number of available v-model modifiers supplied by Vue is limited to these three. However, the framework makes it easy to add extra/custom modifier(s) to a particular components v-model if necessary for your project.

To do this, we need to add a modelModifiers prop to our component definition. This modifier is populated by an object that uses the modifier name as a key which points to a boolean value. This is shown in action in the following listing:

1.  interface Props {
2.  modelValue?: number;
3.  modelModifiers?: Record<string, boolean>;
4.  }
5.  const props = withDefaults(defineProps<Props>(), {
6.  modelValue: 0,
7.  modelModifiers: () => ({}),
8.  });

To see how this might work in code, suppose your project requires a component to format one of its input values with a particular pattern. The pattern to be used is (in itself) not important here; it could be an ISBN or a UK postal code or something else. The important thing here is the methodology. Firstly, we'll need to decide on a name: it can be anything, but it should, ideally, be descriptive of its functionality. For this example, we'll use a generic asPattern modifier name. This means we can write our component as follows:

1.  <SimpleComponent v-model.asPattern="value" />

With the code for the SimpleComponent presented in the previous listing shown in the following code block:

1.  <template>
2.  <input v-model="value" />
3.  </template>

5.  <script setup lang="ts">
6.  import { computed } from 'vue'
7.  import { formatPattern } from '@package'

9.  interface Props {
10.  modelValue?: number;
11.  modelModifiers?: Record<string, boolean>;
12.  }
13.  const props = withDefaults(defineProps<Props>(), {
14.  modelValue: 0,
15.  modelModifiers: () => ({})
16.  })
17.  const emit = defineEmits(['update:modelValue'])
18.  // modelModifiers receives { asPattern: true }
19.  const value = computed({
20.  get() {
21.  if (props.modelModifiers.asPattern) {
22.  return formatPattern(props.modelValue)
23.  }
24.  return props.modelValue
25.  },
26.  set(value) {
27.  value = props.modelModifiers.asPattern ? 
28.  formatPattern(value) :
29.  value;
30.  emit('update:modelValue', value)
31.  },
32.  });
33.  </script>

Now that we understand how the underlying data is handled with v-model and how to modify the data at a basic level, we can start looking at how to handle form data at a component level and how you might validate user input before forwarding it on to a server for processing.

Tip: Never trust data from external sources, especially data that has been submitted from users – or via a web form. You will need to validate the data on the client and on the server. Not only that, but you must also clean the data and be wary of data injection and cross-site scripting attacks; the list goes on. Check out little Bobby Tables at [https://xkcd.com/327/](https://xkcd.com/327/).

[Handling form data and validation](#contents.xhtml_sc2_268a)

Collecting data from your users is always fraught with danger. Even in the smallest of user groups, there will be someone who will maliciously try to break the system by entering wrong data or someone who doesn't really know what to do and enters incorrect data by mistake. Client-side validation is used to check that data entered in the UI conforms to what is expected in format, value range, and type and to handle how the UI responds if the entered data falls outside of these set parameters.

Note: Remember that if you're responsible for building both client and server sides of the project/application, you need to build validation of data at all data ingress points, especially if you're pushing data to the server over an API. Never trust data, any data, regardless of its source. Yes, this message is being repeated. It's very important.

There are two approaches that can be taken when validating data: you can either roll your own or use a validation library.

If you're using a framework, such as Quasar, which we will be looking at in Chapter 18, Building Multi-tenanted Apps With Quasar, data validation capability might be baked into the components provided or a validation library might be recommended by the documentation. As with all things, opinion on what's suitable will vary.

Rolling your own validation might sound like fun, and it may be a useful exercise for your own learning, but in the workplace, it pays to have a consistent, well-tested, and easy-to-use validation library. That way, everyone is building against the same standards and can easily identify what the value parameters are and where the edge cases lie. You are dealing with external data; you must work on the basis that it is going to be bad and/or malicious.

While your organization might have its own ideas as to what constitutes a good validation library, we will be using Vuelidate ([https://vuelidate-next.netlify.app](https://vuelidate-next.netlify.app)) as part of this book. It is a solid; well-tested and documented; easy-to-learn, use, and extend library specifically designed to work within the component architecture of Vue.js applications.

There are plenty of other validation libraries in the wild; your first port of call should be VueAwesome ([https://github.com/vuejs/awesome-vue](https://github.com/vuejs/awesome-vue)), which provides links to many of them.

The general format of validating data is the same for any validation library: parse the data in the form field and run rules against the data to ensure that it conforms to expected patterns; if the data lies within acceptable bounds, continue working with it, otherwise stop processing and flag the issue to the user. Do this for all form fields. That's mostly it, but there's a great deal of variation in how this is achieved by the library that ultimately gets chosen.

Let's get down to business. As with all dependencies, you'll need to use NPM (or yarn) to add the library to your project:

1.  npm install @vuelidate/core @vuelidate/validators

With those in place, we'll have access to the Vuelidate composables.

Note: With Vue2, using a validation library like Vuelidate requires you to inject the library into the global Vue instance so that it is available across the project, otherwise it needs to be added to each component that requires it individually. Adding these things gets tedious quickly.

The recommended way of using Vuelidate is as follows:

1.  import { reactive } from 'vue'
2.  import { useVuelidate } from '@vuelidate/core'
3.  // import required validation rules
4.  import { required, alphaNum, numeric, alpha } from '@vuelidate/validators'

6.  const state = reactive({
7.  title: '',
8.  author: '',
9.  price: {
10.  value: 0.0,
11.  currency: 'GBP'
12.  }
13.  })
14.  const rules = {
15.  title: { required, alphaNum },
16.  author: { required, alpha},
17.  price: {
18.  value: { required, numeric, minValue: minValue(0), maxValue: maxValue(100)
19.  currency: { alpha }
20.  }
21.  }
22.  const v$ = useVuelidate(rules, state)

24.  async function handleSubmit() {
25.  // v$ is a ComputedRef, so use .value
26.  const formValid = await v$.value.validate()
27.  if (!formValid) {
28.  return // form not valid, show errors in UI
29.  }
30.  // handle validation success
31.  }

Note that the format of the validation rules follows the shape of the component data. Here, we're using the reactive() function to create the components state, but if the preference is to use ref(), then the state that gets passed to useVuelidate is an object that collects all the ref pointers that need to be passed through the validator. For example, the preceding listing can be changed as follows:

1.  Switch line 2 to import ref instead of reactive.
2.  Change lines 7 to 13 to be as follows:
    1.  const title = ref('')
    2.  const author = ref('')
    3.  const price = ref({value: 0.0, currency: 'GBP'})

Change line 22 to the following:

1.  const v$ = useVuelidate(rules, { title, author, price })

Both listings have equivalent behavior.

[Standard Validators in Vuelidate](#contents.xhtml_sc3_269a)

Vuelidate comes with several standard validators that are excellent at hiding a significant amount of boilerplate code. Using these provided validators covers a high percentage of the types of validations that are typically required.

[Table 12.1](#ch12.xhtml_tab12-1) highlights a number of these validators, but it is advisable to go to the online documentation and familiarize yourself with all of them:

| Validator | Usage |
| --- | --- |
| required | Marks a field as required, i.e., non-empty, including empty collections and strings |
| requiredIf | Marks a field as required but only if the provided data, ref value, or function resolves to true |
| requiredUnless | Marks a field as required, but only if the provided data/function resolves to false |
| minLength & maxLength | Expects the data to have a minimum (or maximum) length |
| minValue & maxValue | Expects the data to have a minimum (or maximum) value or date |
| between | Expects the data (number or date) to lie between or at the two given values |
| alpha & alphaNum | Expects the data entry to be only letters – alpha, or letters and numbers – alphaNum |
| numeric & integer& decimal | Expects the data to be a number (numeric), just an integer (integer) or a decimal (decimal); accepts both positive and negative numbers |
| email | Confirms that the entered value conforms to the standard email format |
| sameAs | Ensures that the value entered in this field is the same value as entered elsewhere – great for password checking |
| or & and & not | These allow rules to be grouped together to fashion more complex validation schemes; they behave exactly as you would expect boolean operators to behave |

Table 12.1: Standard Vuelidate Validators

If the data you're trying to validate is not coverable by the built-in validators, then Vuelidate allows you to build your own custom validators.

[Specifying configuration options](#contents.xhtml_sc3_270a)

useVuelidate() accepts a third parameter, which is used for passing a few different settings that control how the validation is performed. This object contains a limited number of keys, as presented in the table at the end of this section. Using the configuration options works as shown in the following code listing:

1.  const $externalResults = ref({})
2.  const v$ = useVuelidate(rules, state, {
3.  $autoDirty: true, $lazy: true, $externalResults
4.  })

The configuration argument can take a selection of the keys illustrated in [Table 12.2](#ch12.xhtml_tab12-2):

| Configuration Option | Type (and Default) | Description |
| --- | --- | --- |
| $autoDirty | Boolean (false) | Causes Vuelidate to track state changes automatically |
| $externalResults | ServerErrors Ref<ServerErrors> UnwrapRef<ServerErrors> | A place for passing in external validation errors – these need to match the state, but the actual source of the errors is irrelevant |
| $lazy | Boolean (false) | When false validation rules are called on initialization, otherwise they're only called when $dirty is true |
| $registerAs | String | Registers a custom component into a parent Vuelidate instance |
| $rewardEarly | Boolean | Causes Vuelidate to not invalidate fields until validation is manually triggered |
| $scope | Boolean &#124; String &#124; Symbol &#124; Number (true) | Create a validation scope; if true: collect all validation responses; if false: collect none; any other value specifies a scope – all values in the same scope are collected, and everything else is ignored |
| $stopPropagation | Boolean (false) | Prevents validation results being emitted any further up the hierarchy, regardless of the scope |

Table 12.2: Vuelidate configuration options

[Custom Validators in Vuelidate](#contents.xhtml_sc3_271a)

To create a custom validator, all you need is a pure function that returns a boolean value as a result. The function can then be used in the rules for a field in the same way as a standard validator.

The following listing demonstrates this by creating two custom validators: the first to check if the form field contains the letters Rex and the second to see if either ‘T' or Tyrannosaurus was entered into the field. At the same time, we're using some of the validator helpers that Vuelidate supplies: req to show that a value is required; and regex, which allows a custom regular expression to be used in the validator.

1.  <template>
2.  <!-- form controls here -->
3.  </template>

5.  <script setup lang="ts">
6.  import { useVuelidate } from '@vuelidate/core'
7.  import { helpers } from '@vuelidate/validators'
8.  import { reactive } from 'vue'

10.  const { req, regex } = helpers
11.  const customRexValidator = (value) => 
12.  !req(value) || value.endsWith('Rex')
13.  const customTyrannoValidator = regex(/^Tyrannosaurus\s/i, /^T\s/i)
14.  const state = reactive({})
15.  const rules = {
16.  formField: { customRexValidator, customTyrannoValidator }
17.  }
18.  const v$ = useVuelidate(rules, state)
19.  <!-- other setup stuff -->
20.  </script>

The validators module comes with several helpers that can be used to build custom validators or just to customize the output of standard validators; see [Table 12.3](#ch12.xhtml_tab12-3) for details:

| Helper Name | Description and usage |
| --- | --- |
| forEach | The forEach() helper is used to facilitate simple collection validations; it's designed to be used in conjunction with the $each() iterator, but only circumstances where nested validations cannot be migrated to. $each() has been deprecated in version 2 – nested validations has become the recommended approach to validating collections. Understanding how to validate collections of components is covered in the section Validating collections and other advanced topics. |
| len | This helper returns the appropriate length value for the type of value that has been provided, so this can be an array/string length, or object key count. |
| regex | The regex helper is designed to make it easy to create validators that rely on regular expressions. The helper includes the ability to handle optional inputs (as per req) and the $params collection (as defined in withParams()). There are several examples of how to use the regex helper in the example listings provided earlier. |
| req | req is a helper that allows handling of optional fields. It is like the required validator and allows the custom validator to behave well when optional fields are necessary. The customRexValidator() created in the preceding listing uses the req() helper as demonstration. |
| unwrap | It extracts the value from a given ref, reactive, or computed property:const data = helpers.unwrap(param) |
| withAsync | withAsync() handles validators that return promises. The helper treats the promise states by tracking the states and holding the response values. withAsync() takes two arguments: the validator and a single ref/computed value, a list of ref/computed values or a function that returns reactive/computed values. |
| withMessage | This helper allows you to create a custom message for both built-in and custom validators. The withMessage() helper can accept a function that injects an object which provides the following properties to the output function: 

&#124; $invalid &#124; The validation state &#124;
&#124; $model &#124; The validation value &#124;
&#124; $params &#124; Values supplied using withParams() &#124;
&#124; $pending &#124; Resolution status of a promise &#124;

validator: helpers.withMessage(  ({ $pending, invalid, params, model }) => outputString, validator) } } |
| withParams | Sometimes validators require additional params or metadata to support the validation. Accessing this data in the validation function is done via the $params object. If the validation function is a higher-order function that requires the supply of additional reactive properties, the withParams() wrapper needs to be around the internal function.The following listing covers both the mentioned scenarios:const singleValidator = helpers.withParams(  { key: fieldValue },  (value) => !helpers.req(value) &#124;&#124;  fieldValue === value)<!-- additional reactive params validation -->const paramsValidator = (param) =>  helpers.withParams(    { key1: fieldValue, key2: param },    (value) => !helpers.req(value) &#124;&#124; 
value.includes(param) ) |

Table 12.3: Vuelidate helpers

[Checking for and handling validation fails](#contents.xhtml_sc3_272a)

Validation fails when one (or more) validation function(s) return(s) false. At this point, the validation object is marked as $dirty, and the $invalid property is set to true. If both the $dirty and $invalid states are true, then the $error state is also set to true and the $errors and $silentErrors arrays are populated with error messages.

To validate a single field, or if each individual field in a form needs to be validated, the field can have an event handler attached to either (or both) the blur and change events; the handler in this case is $touch, as demonstrated in the following code example:

1.  <input v-model="fieldName" @blur="v$.fieldName.$touch">

This causes the field to be marked as $dirty, and the field is validated with the errors recorded as we just described.

Validating all the fields in a form (including nested fields) can be done by either using v$.$touch() method or using the async v$.$validate() method. While $touch() can be attached to any field in the form, it's mostly used in conjunction with the submit button. However, it is more conventional to use $validate() in the form submit handler:

1.  <template>
2.  <form @submit.prevent="handleSubmit">
3.  ... form fields ...
4.  </form>
5.  </template>

7.  <script setup lang="ts">
8.  ... setup validator and rules ...
9.  const v$ = useVuelidate(rules, state)

11.  async function handleSubmit () {
12.  const isFormValid = await v$.$validate()
13.  // if form is not valid, return early to prevent form
14.  // submission
15.  if (!isFormValid) { return }
16.  // actually submit form
17.  }
18.  </script>

Once a form has been marked as $error="true", (i.e., both $dirty and $invalid), the submit handler needs to return false to stop processing or any other data submission from occurring.

With $error="true", the $errors property is populated with a collection keyed on the field name and returns a list of err ors associated with the field.

Accessing these error messages can be done through a v-for iterator. Here is a listing that iterates through all the form errors in a single place; it is not very useful except for the smallest of forms:

1.  <form @submit.prevent="handleSubmit">
2.  <input v-model="fieldName">
3.  <!-- iterate over ALL form errors -->
4.  <p v-for="error of v$.$errors" :key="error.$uid">
5.  {{ error.$validator }} on property {{ error.$property }} says: {{ error.$message }}</p>
6.  </form>

Accessing the errors on an individual field basis is more user friendly, as demonstrated in the following example:

1.  <form @submit.prevent="handleSubmit">
2.  <input v-model="fieldName">
3.  <!-- iterate single field (fieldName) errors -->
4.  <ul v-if="v$.fieldName.$error">
5.  <li v-for="error of v$.fieldName.$errors" 
6.  :key="error.$uid">
7.  <!-- access to all the same fields as above listing -->
8.  </li>
9.  </ul>
10.  </form>

These are all standard usage patterns and can be found in the Vuelidate documentation. None of this should be a surprise as such; along with testing, which we'll cover in [Chapter 14](#ch14.xhtml), Testing Vue.js Applications, much of the work that you'll do will be to ensure that the supplied data is valid and not dangerous to the server or the database.

With the basics covered, we'll briefly go over some of the more advanced things that Vuelidate allows you to do.

[Validating collections and other advanced topics](#contents.xhtml_sc3_273a)

In this section, we'll cover some edge cases that occasionally crop up. These are parts of your validation toolkit (when using Vuelidate) that can help you out of a jam.

[Using ref's, reactive, and computed values and rules](#contents.xhtml_sc3_274a)

Providing state into useVuelidate when using reactive state isn't any different from what we've already discussed: individual ref's and computed values need to be provided to the composable as an object. If you need to mix different types of state, i.e., refs, reactive and/or computed, then the same mechanism is used as follows:

1.  import { ref, computed, reactive } from 'vue'
2.  import { useVuelidate } from '@vuelidate/core'
3.  import { ... } from '@vuelidate/validators'

5.  const reactiveState = reactive({ name: 'T-Rex' })
6.  const refState = ref('')
7.  const computedState = computed({
8.  get () { ... }
9.  set (value) { ... }
10.  })
11.  const rules = []
12.  const v$ = useVuelidate(
13.  rules, {reactiveState, refState, computedState} )

[Nested Validations, validation scopes and collector-only components](#contents.xhtml_sc3_275a)

The recommended approach for managing nested collections is to create a component that can be nested with its own set of validation rules and have useVuelidate collect all errors (as $errors and $silentErrors) together; using $touch on a parent causes $touch to be called on all nested components.

This behavior means that you only need to call validation against a parent component and all children are validated at the same time; demonstrated in the following code sample:

1.  <template>
2.  <div>
3.  <ChildComponent v-for="c in components" :key="c.id" />
4.  <!-- this will contain all $errors/$silentErrors 
5.  from all <ChildComponents/> -->
6.  <p v-for="error of v$.$errors" :key="error.$uid">
7.  {{ error.$message }}
8.  </p>
9.  </div>
10.  </template>

12.  <script setup lang="ts">
13.  import { ref } from 'vue'
14.  import { useVuelidate } from '@vuelidate/core'
15.  import ChildComponent from '@/components/ChildComponent'

17.  const components = ref([ ... ])
18.  // this will collect all components validation results
19.  const v$ = useVuelidate()
20.  </script>

If creating a nested component is not a viable solution for any use case involving collections, then Vuelidate (in the @vuelidate/components package) supplies the ValidateEach component. This wrapper component accepts the validation rules, the collection, and any required template (as the default slot) and passes Vuelidate instances to the parent and any children to enable the validation through the hierarchy. See following listing as an example:

1.  <template>
2.  <ValidateEach
3.  v-for="(item, index) in collection"
4.  :key="index" :state="item" :rules="rules">
5.  <template #default="{ v }">
6.  <div>
7.  <!-- content here -->
8.  </div>
9.  </template>
10.  </ValidateEach>
11.  </template>

13.  <script setup lang="ts">
14.  import { reactive } from 'vue'
15.  import { useVuelidate } from '@vuelidate/core'
16.  import { ValidateEach } from '@vuelidate/components'
17.  import { ... } from '@vuelidate/validators'

19.  const rules = {}
20.  const collection = reactive([ ... ])
21.  const v$ = useVuelidate()
22.  </script>

When using the nested component functionality, there are instances where the data collected by the parent validation needs to be limited; this is where validation scoping comes in.

To handle scoping, Vuelidate provides the $scope and $stopPropagation configuration options. With these options, you can control when a parent collects nested child form data.

$scope accepts three values:

*   true – This is the default behavior.
*   false – Force the validator to not collect any validation data.
*   <string | number | symbol> - This value labels a scope, any child component that also has this named scope is collected and managed by that validator.

1.  <!-- $scope = false -->
2.  import { useVuelidate } from '@vuelidate/core'
3.  ... other initialisations ...
4.  const v$ = useVuelidate(rules, state, { $scope: false })

6.  <!-- Parent: $scope = 'thisScope' -->
7.  import { useVuelidate } from '@vuelidate/core'
8.  import { h } from 'vue'
9.  import ChildComponent from './ChildComponent'
10.  ... other initialisations ...
11.  const scope = 'thisScope'
12.  const v$ = useVuelidate(rules, state, { $scope: scope })

14.  function render() {
15.  return h('<ChildComponent :scope="scope" />')
16.  }
17.  ... other content ...

19.  <!-- Child: $scope = 'thisScope' -->
20.  import { useVuelidate } from '@vuelidate/core'
21.  const props = defineProps('scope')
22.  ... other initialisations ...
23.  const v$ = useVuelidate(rules, state, { $scope: props.scope })
24.  ... other content ...

$stopPropagation tells the validator to not emit results to the parent but continues to collect the data together from any children; this is useful in modal contexts that supply their own validations, but these errors should not be available to the forms held by the parent. The following shows how this is achieved:

1.  import ChildComponent from '@/components/ChildComponent'
2.  // collects validations from 'ChildComponent' but does not emit it up to parent validations.
3.  const v = useVuelidate(validations, state,
4.  { $stopPropagation: true }
5.  )

These mechanisms allow for rich interactive form validation.

As useVuelidate automatically collects the child results together, as described earlier, a parent can be set up as a “collector only” component. This type of top-level component only defines the parent validator, leaving the validation rules the purview of each of the nested components. This parent validator has an optional configuration object that can be used to provide information with regard to scopes and any of the other available configuration options; see [https://vuelidate-next.netlify.app/api/configuration.html](https://vuelidate-next.netlify.app/api/configuration.html) for more information on what configuration options are available.

[Changing the data returned from a validator](#contents.xhtml_sc3_276a)

In most cases, the default boolean return value is all that is required. However, there are cases where you might need to supply more information about the error encountered to understand the failure. In these instances, the validator function can return an object; the only stipulation is that the object has a $valid key to hold the validation status. The object can return any other information, as required.

Accessing the data in the returned object is done via the $response property on the validation and error objects. The next code block shows to make these alterations in the $response property of a validation function:

1.  const validationFunction = (value) => {
2.  if (value === 'value') {
3.  return true
4.  }

6.  return {
7.  $valid: false,
8.  message: 'Some message',
9.  data: [],
10.  moreData: {}
11.  }
12.  }

[Returning errors from server side or API validation](#contents.xhtml_sc3_277a)

It is not unusual to have stricter validation rules at the server level, protecting the data ingress points and the data store. As a result, data that might pass client-side (front-end) validation might subsequently fail when passed to a server for processing.

To handle this situation, useVuelidate allows you to pass data to the $externalResults configuration property; this data needs to be reactive, either a reactive() or ref() so that the validation engine can keep track of it.

The following code example demonstrates how $externalResults can be used:

1.  const state = reactive({ ... })
2.  // placeholder for external results
3.  const $externalResults = ref({})
4.  const rules = { ... }
5.  const v = useVuelidate(rules, state, { $externalResults })
6.  // validate method
7.  async function validate () {
8.  if (!await v.value.$validate()) return
9.  const resp = await asyncFunction(state)
10.  // add the errors into the external results object
11.  $externalResults.value = resp?.errors
12.  }

In most cases, this external data will be tracked and cleared by Vuelidate (if you're using $model, i.e., via v-model, or the $autoDirty config options). If neither of these apply and you need to clear $externalResults, Vuelidate provides a $clearExternalResults() method against each validation value to enable you to manually handle clearing the data up as shown in the following listing:

1.  async function validationFunction () {
2.  // clear out old results
3.  v.value.$clearExternalResults()
4.  // then
5.  if (!await v.value.$validate()) return
6.  }

[Supporting i18n](#contents.xhtml_sc3_278a)

Being able to respond to your users in multiple languages, i.e., their locally configured default language, is becoming more important across applications; validation responses are no exception. Vuelidate has this scenario covered as well.

To support internationalisation (i18n), you'll need to add an i18n library and its dependancies to your project: @/i18n with vue-i18n are the recommended packages. With these in place, you'll need to create the desired wrappers and functions, as demonstrated in the following listing:

1.  import { createI18nMessage, required as v_r, minLength as v_ml } from '@vuelidate/validators'
2.  import { i18n } from '@/i18n'

4.  const withI18nMessage = createI18nMessage(
5.  { t: i18n.global.t.bind(i18n) }
6.  )
7.  // wrap each validator required
8.  export const required = withI18nMessage(v_r)
9.  export const minLength = withI18nMessage(v_ml, { withArguments: true })

With definitions set up, using i18n validators is transparent to the developer. By default, the validation messages are expected to be specified in an object as follows:

1.  {
2.  "validations": {
3.  "required": "The {property} is required.",
4.  "minLength": "The {property} must have a min length of {min}."
5.  }
6.  }

Further configuration options can be found in the documentation for various packages named.

[Async setup functions](#contents.xhtml_sc3_279a)

When using a top-level await inside a <script setup>, the compiler turns this into an async setup() function. To use Vuelidate in this type of setup, you need to access the current Vue instance and pass this into the config for useVuelidate. The following listing shows one way of setting up Vuelidate in async setups:

1.  const currentVueInstance = getCurrentInstance()?.proxy
2.  // top-level await
3.  const result = await asyncFunction()
4.  const vuelidate = useVuelidate(rules, result.state, 
5.  { currentVueInstance }
6.  )

With this, we can now move on to discussing how to combine v-model with components to provide users of our components with an easy-to-use API.

[Using v-model with Components](#contents.xhtml_sc3_280a)

There are times in a project build when creating a form from simple elements just isn't enough, or your task is to construct a library of standard components that is to be reused across an organization or several projects. In this case, the form elements might be provided as part of a component. So, the question is: how do we propagate the convenience of v-model into components to make them easy and consistent for our users?

The answer to this can be found in the Value Binding and v-model section, which we covered earlier. If you remember, v-model is a syntactical sugar for a model value binding (which defaults to modelValue) and an update event binding (which defaults to the update:modelValue custom event): the field data and the event that gets triggered when the field is updated.

As a reminder, the following two code listings are equivalent; the first uses the v-model convenience:

1.  <input v-model="fieldValue" />

And the second uses the expanded form:

1.  <input
2.  :modelValue="fieldValue"
3.  @update:modelValue="value => fieldValue = value"
4.  />

Therefore, to build a component that accepts a v-model attribute, the component needs to accept (as the default) a modelValue prop and emit an update:modelValue custom event.

In practice, this can be implemented in several ways depending on personal preference and which components API you're using; here, we'll use a Composition API component to build a component wrapper (SimpleComponent.vue) in its simplest form:

1.  <!-- SimpleComponent.vue -->
2.  <template>
3.  <input type="text" :value="modelValue"
4.  @input="$emit('update:modelValue', $event.target.value)"
5.  />
6.  </template>

8.  <script setup lang="ts">
9.  defineProps<{modelValue: string}>()
10.  defineEmits<{
11.  (e: 'update:modelValue', value: string): void
12.  }>()
13.  </script>

If your preference is to use writable computed properties to handle this interaction, then the pattern given in the following code listing is recommended:

1.  <!-- SimpleComputedComponent.vue -->
2.  <template>
3.  <input type="text" v-model="value" />
4.  </template>

6.  <script setup lang="ts">
7.  import { computed } from 'vue'

9.  const props = defineProps<{modelValue: string}>()
10.  const emit = defineEmits<{
11.  (e: 'update:modelValue', value: string): void
12.  }>()
13.  const value = computed({
14.  get () {
15.  return props.modelValue
16.  },
17.  set (value) {
18.  emit('update:modelValue', value)
19.  }
20.  })
21.  </script>

Again, either of these approaches is valid; it's down to your personal preference or your organization's coding standards which gets used.

It might not have escaped your attention, but the listings above just deal with a single prop – so a single piece of data. In many cases, the requested functionality will probably rely on more than one data point.

To help with this, v-model accepts an argument value that gets bound to the data value instead of the default modelValue. To use v-model arguments, when you use the v-model attribute, you assign a name using the Vue binding operator (:), as demonstrated in the following listing:

1.  <!-- binding to the inputValue prop on the SimpleComponent -->
2.  <SimpleComponent v-model:input-value="this_value" />

When used this way, the component needs to provide a prop of the equivalent name and is required to emit a custom update event. Using the simple component format discussed previously, you'll build your component in the following way:

1.  <!-- SimpleComponent with inputValue v-model arg -->
2.  <template>
3.  <input type="text" :value="inputValue"
4.  @input="$emit('update:inputValue', $event.target.value)"/>
5.  </template>
6.  <script setup lang="ts">
7.  defineProps<{ inputValue: string }>()
8.  defineEmits<{ 
9.  (e: 'update:inputValue', inputValue: string) :void
10.  }>()
11.  </script>

How this helps us is that now we have the tools to pass in multiple named v-models and have the component manage the props and events internally.

As a simple demonstration, a simple component that accepts multiple props is given in the following listing:

1.  <!-- MultiPropComponent - Book -->
2.  <template>
3.  <input type="text" v-model="title" \>
4.  <input type="text" v-model="author" \>
5.  <input type="number" v-model="price" \>
6.  </template>

8.  <script setup lang="ts">
9.  import { computed } from 'vue'

11.  interface Book {
12.  ...
13.  }

15.  const props = defineProps<Book>()
16.  // using runtime definition here to save space
17.  const emit = defineEmits(['update:title', update:author', 'update:price'])
18.  const title = computed({
19.  get () { return props.title },
20.  set (title) { emit('update:title', title) }
21.  })
22.  ... Define rest of props like title ...
23.  </script>

Using this, MultiPropComponent is now as easy as follows:

1.  <MultiPropComponent 
2.  v-model:title="Vue.js for Job Seekers"
3.  v-model:author="Clive Harber"
4.  v-model:price="24.99"
5.  />

Adding modifiers to components that use v-model argument values is as simple as setting up a prop that uses the argument name + Modifiers as a name, i.e., titleModifiers or authorModifiers. The behavior exhibited by the component with regard to modifiers is the same as we discussed earlier.

Hopefully, you can see that arbitrarily complex form element-based custom components can be constructed, which will follow standard data input and event patterns. Following these patterns makes components like this easier to use across projects and teams.

With this in mind, we can start looking at adding some forms to our sample application.

[Adding forms to the sample application](#contents.xhtml_sc3_281a)

Now that we have understood how to build forms and how to validate the data before sending it ahead, we can look at some of the forms that we are going to need for the sample app that we are building.

The sections that will provide forms for here are the AddToCartComponent for the Menu- and Item- display pages, several components on the checkout pages, and the LoginComponent.

[AddToCartComponent](#contents.xhtml_sc3_282a)

This component is used in multiple places and manages item quantities when they get added to the users basket.

So, we will need to build this component so that it accepts an object that describes the ItemComponent – this data comes the from the components' parent, and allows the amount needed to be incremented and decremented. We'll provide the major elements in the following few listings for this component, so you can see how the main parts fit together. The first part we'll explore is the template section:

1.  <template>
2.  <div class="...">
3.  <div class="...">{{ formatAsCurrency(item.price) }}</div>
4.  ...
5.  <button type="button" @click="incrementCount">
6.  <icon ... />
7.  </button>
8.  <input type="text" class="..." v-model="itemCount"/>
9.  <p v-for="error of v$.itemCount.$errors" :key="error.$uid">
10.  <strong>{{ error.$message }}</strong>
11.  </p>
12.  <button type="button" ="..." @click="decrementCount">
13.  <icon ... />
14.  </button>
15.  ...
16.  <button type="button" class="..." @click="addToCart">
17.  Add to Cart
18.  </button>
19.  ...
20.  </template>

As you can see, the template is simple: there are some click handlers; a formatting function, which can be a plain function or a computed value; and lastly, a simple loop that handles error messages.

The next listing details the first part of the script section, where the components data is set up and we set out the validation rules:

1.  <script setup lang="ts">
2.  import { ref } from 'vue'
3.  import { useCart } from '../../composables/useCart'
4.  import { useVuelidate } from '@vuelidate/core'
5.  import { integer, minValue, maxValue } from '@vuelidate/validators'

7.  type Item = { ... }

9.  const props = defineProps<{ item: Item }>()
10.  const { addItem } = useCart()
11.  const itemCount = ref(1)
12.  const rules = {
13.  itemCount: { integer, minValue: minValue(1), maxValue: 
    maxValue(10) }
14.  }
15.  const v$ = useVuelidate(rules, { itemCount }, { $autoDirty: true })
16.  const decrementCount = () => {
17.  if (itemCount.value > 1) {
18.  itemCount.value -= 1
19.  }
20.  }
21.  const incrementCount = () => itemCount.value++

The most interesting parts of the previous listing are where we define and use the validation rules. The next part shows how the rule definitions are used:

1.  async function addToCart() {
2.  const isCorrect = await v$.value.$validate();
3.  if (!isCorrect) return;
4.  addItem({
5.  id: props.item.id,
6.  name: props.item.name,
7.  price: props.item.price,
8.  qty: itemCount.value,
9.  extras: [],
10.  });
11.  }
12.  </script>

This is a simple form; the ManageOrderComponent is similar in structure but differs in the data that it manages. Because of the similarities, there is opportunity to abstract out the differences and have them injected via a slot. This is an exercise left to you.

[CartAddressComponent](#contents.xhtml_sc3_283a)

The initial design for this component is simple; however, we will add more information so that we can take a detailed look at building custom validation rules, particularly the postal/zip code validator. We will use the postal code format used in the UK for this as it has a particular set of rules that can be readily expressed as a regular expression. The new design for this is illustrated in [Figure 12.1](#ch12.xhtml_fig12-1):

![](images/figure_12.1.png)

Figure 12.1: Changed CartAddressComponent

With these design changes, our HTML template for the component is now expressed as follows:

1.  <div
2.  v-for="(control, key) in formControls" :key="key" ...>
3.  <div class="...">
4.  <label>{{ control.label }}</label>
5.  </div>
6.  <div class="...">
7.  <input v-model="formState[key]"
8.  :placeholder="control.placeholder">
9.  <p class="...">
10.  {{ v$[key].$errors.join(', ') }}
11.  </p>
12.  </div>
13.  </div>

From the template section, you can see the kind of model that the component is going to use; the listing that follows is going to concentrate on the moving parts only; the boilerplate will be easy enough to build around this. Let's start by adding in the imports:

1.  import { reactive } from 'vue';
2.  import { useVuelidate } from '@vuelidate/core';
3.  import { required, alpha, helpers } from '@vuelidate/validators';

The preceding code is a simple boilerplate setup, which we're already used to, followed by creating some useful interfaces that we'll need to build out the form:

1.  interface FormControl {
2.  ...
3.  }
4.  interface CheckoutForm {
5.  ...
6.  }
7.  const formControls: CheckoutForm = {
8.  name: { label: 'Name' },
9.  address1: { label: 'Address Line 1', placeholder: 'House number, street name' },
10.  address2: { label: 'Address Line 2', placeholder: 'Local area' },
11.  town: { label: 'Town' },
12.  county: { label: 'County' },
13.  postcode: { label: 'Post Code' },
14.  };

With that in place, we set up the form state:

1.  const formState = reactive({
2.  name: '',
3.  address1: '',
4.  address2: '',
5.  town: '',
6.  county: '',
7.  postcode: '',
8.  });

Following this, we will add some custom validators for the address lines and post code using the regex() helper so that we can build the rules needed for the validator. The actual code is given in the next code fragment:

1.  const addressLineValidator = helpers.regex(/[a-z0-9\s\,\.]+/i);
2.  const postcodeValidator = helpers.regex(
3.  /^[A-Z]{1,2}[0-9R][0-9A-Z]?*[0-9][ABD-HJLNP-UW-Z]{2}$/i
4.  );
5.  const rules = {
6.  name: { required, alpha },
7.  address1: { required, addressLineValidator },
8.  address2: { addressLineValidator },
9.  town: { required, addressLineValidator },
10.  county: { required, addressLineValidator },
11.  postcode: { required, postcodeValidator },
12.  };

14.  const v$ = useVuelidate(rules, formState, { $autoDirty: true });

The next component we'll discuss is the one that handles voucher and/or discount codes.

[ApplyVoucherToCartComponent](#contents.xhtml_sc3_284a)

Applying a voucher or discount code to a cart requires an external service to validate that the code provided is acceptable and then pass that information on to the cart to ensure that the correct pricing is applied for the customer.

This will require the use of the $externalResults configuration setting and access to the relevant API.

First off, here are the important parts of the template:

1.  <div class="...">
2.  <form @submit="submitValidationCode">
3.  <div class="...">
4.  <label class="...">Voucher Code</label>
5.  <input class="..." v-model="validationCode"
6.  placeholder="Enter discount code"/>
7.  <button type="submit" class="...">Apply</button>
8.  </div>
9.  </form>
10.  </div>

And here are the script section changes:

1.  ...
2.  import { alpha } from '@vuelidate/validators';

4.  const validationCode: Ref<string> = ref('');
5.  const $externalResults = ref({});
6.  const v$ = useVuelidate({ validationCode: { alpha } },
7.  { validationCode }, { $externalResults });

9.  async function submitValidationCode() {
10.  const formValid = await v$.value.$validate();
11.  if (!formValid) return;
12.  const resp = await validateVoucherCode(validationCode.value)
13.  $externalResults.value = resp?.errors;
14.  }

16.  async function validateVoucherCode(code: string): Promise<Record<string, string[]>> {
17.  return { errors: [] };
18.  }

[LoginComponent](#contents.xhtml_sc3_285a)

This is a simple component that only has two fields and a button. The validators here need to check the given username and password; the username uses email addresses, and the password should ensure that the following criteria are met:

*   More than 8 characters
*   Less than 20 characters
*   Alphanumeric characters, both lower and upper case
*   Limited set of special characters

The template is very simple:

1.  ...
2.  <label class="...">Email</label>
3.  <input class="..." v-model="userEmail" type="email"
4.  placeholder="Registered Email" />
5.  <p v-if="v$.userEmail.$errors" class="...">
6.  <span v-for="error in v$.userEmail.$errors" :key="error">
7.  {{ error }}</span>
8.  </p>
9.  ...
10.  <label class="...">Password</label>
11.  <input class="..." v-model="password" type="password"
12.  placeholder="Account password" />
13.  <p v-if="v$.password.$errors" class="...">
14.  <span v-for="error in v$.password.$errors" 
15.  :key="error.$uid">{{ error }}</span>
16.  </p>

The script section is as follows:

1.  import { ref, Ref } from 'vue';
2.  import { ServerErrors, useVuelidate } from '@vuelidate/core';
3.  import { required, helpers, email } from '@vuelidate/validators';
4.  import { useRouter } from 'vue-router';

We'll de-structure the validation helpers to aid tree-shaking here and use the router for redirecting when the user details are correct:

1.  const { regex, withMessage } = helpers;
2.  const $externalResults: Ref<ServerErrors> = ref({});
3.  const passwordValidation = regex(/[a-zA-Z0-9\!\@\*\.\%\$\£\'\+]{8,20}/);

Here, we're building the rules with the withMessage() helper to improve the information that we return to the user:

1.  const rules = {
2.  userEmail: {
3.  required: withMessage('Account email is required', required),
4.  email: withMessage('This is not an email', email),
5.  },
6.  password: {
7.  required: withMessage('Password is required', required),
8.  passwordValidation: withMessage(
9.  'The entered password does not match password rules',
10.  passwordValidation
11.  ),
12.  },
13.  };
14.  const v$ = useVuelidate(rules, { userEmail, password }, { $externalResults });

The following code presents a simple login function that passes the work off to an async function for the login:

1.  function userLogin() {
2.  ...
3.  sendLogin({ email: userEmail.value, password: password.value }).then(() =>
4.  router.push({ name: 'profile' }).catch((err) => {
5.  $externalResults.value = err;
6.  })
7.  );
8.  }
9.  async function sendLogin(values: { email: string; password: string }): Promise<boolean> {
10.  return true;
11.  }

Building forms with Vue.js follows some simple rules, which are consistent.

[Conclusion](#contents.xhtml_sc2_286a)

This chapter covered building forms and explained how to validate the data entered by the user. We covered value binding and modelling the state of form controls with v-model and the entire form itself with the standard Vue structures. We also looked at how to handle data validation with Vuelidate with standard validators and how to build custom ones. We then looked at some of the forms that the sample application.

In the next chapter, we will explore application-wide state management with Pinia and how to get and post data to servers.

[Points to remember](#contents.xhtml_sc2_287a)

*   Forms can be whatever you need them to be.
*   Forms can be constructed from as many components as necessary.
*   Never trust data from a user.
*   Validation is always necessary.

[Key terms](#contents.xhtml_sc2_288a)

*   v-model
*   Validation
*   Form
*   Form Control
*   Validation errors
*   Value binding
*   User data
*   Modifiers

Join our book’s Discord space

Join the book's Discord Workspace for Latest updates, Offers, Tech happenings around the world, New Release and Sessions with the Authors:

**[https://discord.bpbonline.com](https://discord.bpbonline.com)**

![](images/fm1.png)

# [CHAPTER 13Managing State with Pinia and API Communication](#contents.xhtml_ch13a)

[Introduction](#contents.xhtml_sc2_289a)

As our application grows, there comes a need to maintain consistent state across many components; also, data might come from back-end servers or APIs. While not strictly necessary when using Composition API, having centralized state with consistent accessor methods can save a lot of work.

In the Vue.js eco-system, the default tool for state management is Pinia, which has been built with Composition API in mind from the beginning. Pinia is the second iteration of such functionality; its forerunner, Vuex, is still in use in many applications that are currently in service today.

Alongside understanding how to manage application state centrally, we'll also briefly go over some methods that are used for accessing data on remote servers using the Fetch API and Axios for JSON/XML services and Apollo for GraphQL-based services.

[Structure](#contents.xhtml_sc2_290a)

This chapter will cover the following topics:

*   Managing state in Vue
*   Introduction to the Pinia store
*   Working with Pinia
*   Using Fetch API from a component
*   Integrating Axios into an application
*   GraphQL-based API access

[Objectives](#contents.xhtml_sc2_291a)

This chapter explores how to manage your application state so that it is easily accessible from all components. While in many cases it might seem simpler and quicker to use a composable to hold and manage its own state, you can quickly get into a situation where it becomes unmaintainable trying to find where in item of state is created. This is where Pinia comes in.

Using Pinia as the interface between your composable services and remote APIs then frees you up as a developer, with everything in one place with a consistent access pattern. Once we've explored Pinia, we'll extend this knowledge by accessing third-party APIs for both JSON and GraphQL endpoints.

[Managing state in Vue 3](#contents.xhtml_sc2_292a)

In many cases, for small- to medium-sized applications, having your application state maintained in Composables might be sufficient for your needs. However, it can be tedious to import many Composables into a component, and while there's no increase in package size, it can increase cognitive load on you, as the developer, trying to remember which data comes from which part of the application.

To this end, you should use Pinia as a central source for data in your application.

Pinia allows you to define some state, plus ways to access and manipulate the state all in one place. It also has a low-level API that allows for full extensibility if necessary.

You can create as many stores as are necessary for either your personal preferences or application boundaries, whichever serves you best. Stores can be composed, which gives the impression of nesting, even though the stores are designed as a flat structure.

All these features combined gives you, as a developer, a lot of flexibility and power over how your application state is handled.

[Introduction to the Pinia store](#contents.xhtml_sc2_293a)

Adding and setting up Pinia is relatively simple:

To install, simply use NPM:

1.  $ npm i pinia

To use Pinia, you need to tell your application about it, firstly by creating a Pinia instance and then by adding it to the app with .use().

In your main.js/ts file, add code as in lines 2, 5 and 8 in the following listing:

1.  import { createApp } from 'vue'
2.  import { createPinia } from 'pinia'
3.  import App from './App.vue'

5.  const pinia = createPinia()
6.  const app = createApp(App)

8.  app.use(pinia)
9.  app.mount('#app')

With this boilerplate in place, we can go ahead and define our store(s).

The best way to do this (although this is a personal preference) is to create a stores folder as a child of the src/ folder, next to all the other code that makes up the application.

Inside this folder (src/stores/), place a file for each store you require. These are usually created along functionality boundaries, such as managing user account data; purchase data or shopping carts; settings or preference data; whatever you need or as detailed in a design document.

Each one of these files contains a defineStore function, an example of which can be seen as follows:

1.  import { defineStore } from 'pinia'

3.  export  const useStore = defineStore('store', () => {
4.  // store state, actions and getters defined here
5.  })

When creating individual stores, there are a couple of different syntaxes that can be used. These are titled as Option stores and Setup stores, which mirror how applications can be constructed, either as Options API or Composition API components. While it isn't necessary to create Options Stores for Options API and Setup Stores for Composition API, respectively, having consistent code can make things easier for all members of your team and anyone who follows. Again, this is up to personal preference or available design. These two different types are detailed ahead.

So far, we've talked about the different elements in a store but given no detail as to what these are.

A store consists of data that is labelled state. This state is accessible publicly, but really it needs to be viewed as private to the store and accessed through getters to read the state and actions to change the state. Directly accessing the state, no matter how tempting, can potentially lead to complications. Essentially, Pinia stores are global, so employing a little discipline never hurts.

Firstly, we'll discuss the two ways to create a store, and then we'll discuss the specifics of each of the sections that comprise a store.

[Option Store type definition](#contents.xhtml_sc3_294a)

To define a store as an Option Store type, you need to define one with a unique name and an object with the following three keys: state – the data to hold in the store, getters – the computed properties to access the data in the store, and actions – the methods to change the data held in the store, as follows:

1.  import { defineStore } from 'pinia'

3.  export const useNameStore = defineStore('name', {
4.  state: () => ({ name: 'Anon' }),
5.  getters: {
6.  getName: (state) => state.name,
7.  getUppercaseName: (state) => state.name.toUppercase(), 
8.  },
9.  actions: {
10.  updateName(name) {
11.  this.name = name
12.  }
13.  }
14.  })

Nothing in the previous listing should be difficult to understand.

Creating a store in this way should, in fact, seem quite intuitive.

[Setup Store definition](#contents.xhtml_sc3_295a)

If you need something with more flexibility, you need to use a Setup store as it allows you to use Composables. To create a Setup store, instead of providing an object to the defineStore function, you provide a function, as follows:

1.  import { ref, computed } from 'vue'
2.  import { defineStore } from 'pinia'

4.  export const useNameStore = defineStore('name', () => {
5.  const name = ref('Anon')
6.  const getName = computed(() => name.value)
7.  const getUppercaseName = computed(() => name.value.toUppercase())
8.  function updateName(newName) {
9.  name.value = newName
10.  }
11.  return { name, getName, getUppercaseName, updateName }
12.  })

The following rules apply when using a Setup Store:

*   ref() are state properties
*   computed() values are equivalent to getters
*   function() values are equivalent to actions

[State](#contents.xhtml_sc3_296a)

Central to the store is the state; this is usually the first thing that is defined. As stated earlier, state needs to be either defined as a function in an Option store, or as reactive in a Setup store.

When using TypeScript, it is usually unnecessary to provide types, but it can be helpful to the inference engine if this is something that you can provide. It is usually best to use interfaces for this task but use whatever is best for the in-house style. The following gives an example of how to achieve this:

1.  import { defineStore } from 'pinia'

3.  export enum HobbyType {
4.  Art = "ART",
5.  Creative = "CREATIVE",
6.  Design = "DESIGN",
7.  Build = "BUILD",
8.  }

10.  interface HobbyInfo {
11.  name: string
12.  type: HobbyType
13.  }

15.  interface State {
16.  name: string | null;
17.  age: number | null;
18.  hobbies: HobbyInfo[];
19.  }

21.  export const usePersonHobbyStore = defineStore('hobbies',
22.  {
23.  state: (): State => {
24.  return {
25.  name: null,
26.  age: null,
27.  hobbies: [],
28.  }
29.  }
30.  })

There is another way to create interfaces for the data in the store, but it involves individually typing each of the state elements. Again, this is house-style dependent. To the author, individually typing each of the state properties is unnecessary and causes a significant amount of line noise.

Accessing, i.e., both reading and writing, the state of a store directly is the default. All data in the store is public, although dynamically adding a new state property is not possible. The store needs to have properties defined with an initial state. See the following for more details:

1.  <script setup lang="ts">
2.  // using the previously defined nameStore
3.  import { useNameStore } from '/path/to/store'

5.  const store = useNameStore()

7.  // reading the store directly
8.  console.log(store.name)

10.  // direct access to update store property
11.  store.name = 'new name'

13.  // using $patch method to mutate store data
14.  store.$patch({ name: 'patched name' })

16.  // not possible as not defined in the name store
17.  store.age = 10
18.  </script>

The previous listing uses the $patch method. This method allows us to apply multiple or complex changes to a store atomically.

Changing multiple state properties at the same time is achieved by passing in a partial state object. This is just an object that contains some or all the properties defined in the state with the value to change that property to.

Complex or computationally costly operations, like collection modification through pushing, removing, or splicing, which return a new collection, can be applied through a function that can be supplied to $patch(), which receives the store state as a parameter. How this is achieved is detailed in the following sample:

1.  <script setup lang="ts">
2.  // using the previously defined hobbiesStore
3.  import { usePersonHobbyStore, HobbyType } from '/path/to/store'

5.  const store = usePersonHobbyStore()
6.  store.$patch((state) => {
7.  state.hobbies.push({ name: 'a new hobby', type: HobbyType.Art })
8.  state.age = 12
9.  })
10.  </script>

One thing to bear in mind is that the state held by a Pinia store is reactive, so it can't be directly replaced; it can only be patched.

Tip: If you need to set the initial state for the entire application, you can do so by changing the state of the base Pinia instance using the following:

pinia.state.value = {}

Apart from $patch(), the store provides the following methods:

*   $dispose(): Removes the store from Pinia registry
*   $onAction(): Accepts a callback that is invoked prior to any action and can set up callbacks to be invoked after the completion of the action and on the occurrence of an error
*   $reset(): Resets the store to the initial state
*   $subscribe(): Accepts a callback to be invoked each time there is a state change; a subscription will only trigger a single time after a patch completes, whereas a watch() will trigger each time; unless the option { detached: true } is passed into the definition, subscriptions are automatically cleaned up when the component that uses it is unmounted

[Getters](#contents.xhtml_sc3_297a)

Getters are designed to be a store's equivalent to a component's computed properties.

A getter is a synchronous operation that receives a single argument: the current state. As getters are computed properties, they will not accept any other parameters; due to their nature, the return values of getters are cached by the application and only updated when the store value is changed.

The examples here will demonstrate both available syntaxes so that you can gauge which one is better for you to use in your work:

1.  // Setup Store Syntax
2.  export const useCookieStore = defineStore('cookieStore', () => {
3.  const numberInBatch: Ref<number> = ref(5)
4.  const isWarm: Ref<boolean> = ref(true)
5.  // Getters
6.  const currentTotalInBatch = computed(() => numberInBatch.value)
7.  const isBatchFresh = computed(() => isWarm.value)

9.  return  { //return object }
10.  })

12.  // Options Store Syntax
13.  export const useCookieStore = defineStore('cookieStore', {
14.  state: () => {
15.  numberInBatch: 5,
16.  isWarm: true
17.  },
18.  getters: {
19.  currentTotalInBatch: (state) => state.numberInBatch,
20.  isBatchFresh: (state) => state.isWarm
21.  }
22.  })

If you find yourself needing to pass additional data into a getter, you can achieve this by returning a function to receive those values when invoked, as shown below:

1.  // Setup Store Syntax
2.  export const useCookieStore = defineStore('cookieStore', () => {
3.  ...
4.  const totalCookies: Ref<number> = ref(50)

6.  // Getters
7.  const totalBoxed = computed(() => (numberOfBoxes: number) => Math.floor(totalCookies.value / (numberOfBoxes * numberInBatch.value))

9.  return  { //return object }
10.  })

12.  // Options Store Syntax
13.  export const useCookieStore = defineStore('cookieStore', {
14.  state: () => {
15.  ...
16.  totalCookies
17.  },
18.  getters: {
19.  ...
20.  totalBoxed: (state) : number => 
21.  (numberOfBoxes: number) =>
22.  Math.floor(state.totalCookies / (numberOfBoxes * state.numberInBatch))
23.  }
24.  })

Note: Usually getters, rather the results of the getters, are cached. When using them to receive additional values, they can no longer be cached; they're simply invoked, which can introduce performance issues. In these cases, it pays, i.e., becomes more performant, to cache any intermediate results by having them calculated in the getter body rather than in the returned function.

Lastly, getters are composable in themselves. An individual getter has access to all the other getters available in its local store (through the this variable) and it has access to any getters provided by other stores in the application through import:

1.  // Setup Store Syntax
2.  export const useCookieStore = defineStore('cookieStore', () => {
3.  // state data

5.  ...
6.  // return type not required but good practice
7.  const bakeMoreCookies: ComputedRef<boolean> = computed(
8.  () => !isBatchFresh())
9.  })

11.  // Options Store Syntax
12.  export const useCookieStore = defineStore('cookieStore', {
13.  state: () => {
14.  // state data
15.  },
16.  getters: {
17.  ...
18.  // return type required by TS compiler
19.  bakeMoreCookies(state): boolean {
20.  return !this.isBatchFresh
21.  } 
22.  }
23.  })

Note: When basing a getter on the return value of other getters, one caveat to using TypeScript is that you need to provide the return type of the function. This is a known limitation when using TypeScript. This only affects getters when defined using a regular function to access the this value.

[Actions](#contents.xhtml_sc3_298a)

We've seen that getters are the stores' computed values; this makes actions the stores' methods.

Like getters, actions can access the whole store instance (through this), but unlike getters, they can receive as many arguments as required and can be asynchronous, which means they can be used to await the results of an API call or another asynchronous action:

24.  // Setup Store Syntax
25.  export const useCookieStore = defineStore('cookieStore', () => {
26.  // state data
27.  const menu Ref<MenuItem[]> = ref([])
28.  ...
29.  // actions
30.  function bake() {
31.  if (totalCookies.value < 10) {
32.  // make sure we bake enough to bring it back to 50
33.  totalCookies.value += (50 - totalCookies.value)
34.  }
35.  }
36.  async function getMenu() {
37.  menu.value = await menuApi.get()
38.  ... other menu processing
39.  }

41.  return { ... }
42.  })

44.  // Options Store Syntax
45.  export const useCookieStore = defineStore('cookieStore', {
46.  state: () => {
47.  // other state data
48.  menu: [] as MenuItem[]
49.  },
50.  actions: {
51.  ...
52.  bake () {
53.  this.totalCookies += (this.totalCookies < 10) ? (50 - this.totalCookies) : 0
54.  },
55.  async getMenu () {
56.  this.menu = await menuApi.get()
57.  ... other menu processing
58.  }
59.  }
60.  })

To access an action from another store, simply import the required store and use it just like you would a component:

1.  // Options Store Syntax
2.  import { useOtherStore } from './otherStore'
3.  export const useCookieStore = defineStore('cookieStore', {
4.  state: () => {
5.  // other state data
6.  },
7.  actions: {
8.  ...
9.  async processOrder(cart) {
10.  const other = useOtherStore()
11.  const response = await other.process(cart)
12.  ... handle response
13.  }
14.  }
15.  })

Actions can use getters to obtain store values if necessary, but getters should not rely on any actions; they should be side-effect free, i.e., pure functions. Side effects need to be initiated by an action, and any results need to be processed there.

[Working with Pinia Stores](#contents.xhtml_sc2_299a)

Working with Pinia stores is like working with any other composable. As any of the properties defined in a store are public when defined as an Options store, or reactively accessible if returned from a Setup store, they can be accessed directly:

1.  // Using above defined useCookieStore

3.  // Composition API Component
4.  <script setup lang="ts">
5.  import { useCookieStore } from 'cookieStore'
6.  import { storeToRefs } from 'pinia'
7.  const store = useCookieStore()
8.  // directly access the store state
    because its wrapped in a reactive
9.  store.totalCookies = 100
10.  store.numberInBatch = 10

12.  // destructure state properties and getters with 
    storesToRef
13.  // or reactivity breaks
14.  const { totalCookies, numberInBatch } = storeToRefs(store)

16.  totalCookies = 200
17.  </script>

19.  // Options API Component - without setup()
20.  <script lang="ts">
21.  import { mapState } from 'pinia'
22.  import { useCookieStore } from 'cookieStore'

24.  export default {
25.  computed: {
26.  // when not using setup(), mapState() and/or mapWriteableState() helpers can
27.  // be used to access store state data
28.  ...mapState(useCookieStore, ['totalCookies', 'numberInBatch']),
29.  haveFresh(store) {
30.  // can access both 'this' and store
31.  return this.totalCookies > 0 && store.isWarm
32.  }
33.  }
34.  }
35.  </script>

37.  // Options API Component - with setup()
38.  <script lang="ts">
39.  import { mapState } from 'pinia'
40.  import { useCookieStore } from 'cookieStore'

42.  export default {
43.  setup() {
44.  const store = useCookieStore()

46.  return { store }
47.  },
48.  computed: {
49.  haveFresh(store) {
50.  // access store through 'this'
51.  return this.store.totalCookies > 0 && this.store.isWarm
52.  }
53.  }
54.  }
55.  </script>

As mentioned earlier, even though access to the state in a store is public, it should be treated as private and should only be accessed using getters and actions. This way, changes to the state can be controlled as its might be viewed/accessible by several components on a page. In technical terms, you're mutating the state of a global observed singleton object, and unexpected, uncontrolled changes are signs of bad design or worse, poor development discipline.

It can be advantageous for components to subscribe to the state of a store. This way, the subscription code will only trigger once when patched; using a watch() would trigger a change event for each state property changed. The following demonstrates this:

1.  // Composition API Component
2.  <script setup lang="ts">
3.  import { useCookieStore } from 'cookieStore'
4.  const store = useCookieStore()

6.  store.$subscribe((mutation, state) => {
7.  // const { type, storeId, payload } = mutation
8.  // type => 'direct' | 'patch object' | 'patch function'
9.  // storeId => the $id of the store being mutated
10.  i.e. cookieStore
11.  // payload => the patch object
12.  (only used when type is 'patch object')
13.  // state => the entire state of the store after changes

15.  <handle state change here>
16.  }, { options object })
17.  </script>

Accessing a store's getters is the same as accessing a state property.

The following example demonstrates the three different ways that components can use a store; each depends on how the component is constructed:

1.  // Composition API Component
2.  <script setup lang="ts">
3.  import { useCookieStore } from 'cookieStore'
4.  const store = useCookieStore()

6.  console.log(store.currentTotalInBatch) // 5
7.  </script>

9.  // Options API Component - without setup()
10.  <script lang="ts">
11.  import { mapState } from 'pinia'
12.  import { useCookieStore } from 'cookieStore'

14.  export default {
15.  computed: {
16.  // access to getters is the same as accessing state
17.  ...mapState(useCookieStore, [...])
18.  }
19.  }
20.  </script>

22.  // Options API Component - with setup()
23.  <script lang="ts">
24.  import { useCookieStore } from 'cookieStore'

26.  export default {
27.  setup() {
28.  const store = useCookieStore()
29.  return { store }
30.  }
31.  computed: {
32.  // access to getters is the same as accessing state
33.  doubleCookies() {
34.  return this.store.totalCookies * 2
35.  }
36.  }
37.  }
38.  </script>

Even though the access mechanism is transparently the same, using getters to access state data becomes more efficient than repetitively accessing state properties; computed values are internally cached by Vue.

In a similar vein, triggering a store's actions is just a case of calling the required function on the store and passing in any required data. Actions can also be destructured from a store if required, as there is no reactivity to consider. Finally, if using an Options API component without the setup() life cycle hook, you'll need the mapActions() helper to extract the actions into your component's methods.

All three approaches are presented in the following code:

1.  // Composition API Component
2.  <script setup lang="ts">
3.  import { useCookieStore } from 'cookieStore'
4.  const store = useCookieStore()

6.  // actions can be decomposed
7.  const { processOrder } = store

9.  // or can be called on the store directly
10.  store.processOrder({...orderDetails})
11.  </script>

13.  // Options API Component - without setup()
14.  <script lang="ts">
15.  import { mapActions } from 'pinia'
16.  import { useCookieStore } from 'cookieStore'

18.  export default {
19.  methods: {
20.  // access to actions is via mapActions helper
21.  ...mapActions(useCookieStore, ['processOrder'])
22.  }
23.  }
24.  </script>

26.  // Options API Component - with setup()
27.  <script lang="ts">
28.  import { useCookieStore } from 'cookieStore'

30.  export default {
31.  setup() {
32.  const store = useCookieStore()
33.  return { store }
34.  }
35.  methods: {
36.  // access to getters is exactly the same as state...
37.  buyNow() {
38.  this.store.processOrder({...orderDetails})
39.  }
40.  }
41.  }
42.  </script>

Additionally, actions can be observed and callbacks triggered using the $onAction() function provided by a store instance, see next:

1.  import { useCookieStore } from 'cookieStore'
2.  const store = useCookieStore()

5.  const func = store.$onAction(params => {
6.  // const { name, store, args, after, onError } = params

8.  // name => the action name
9.  // store => the store instance
10.  // args => the arguments passed to the action as an array
11.  // after => callback to invoke after the action completes
12.  // onError => callback to invoke if action errors

14.  <functionality to perform before the action>
15.  }, <boolean?>)

The options object allows you to pass in a boolean to detach the subscription from the component instance, otherwise this functionality will be removed when the component is unmounted. This is similar to the ways that $subscribe() works with state changes.

[Talking to a server with Fetch API from your application](#contents.xhtml_sc2_300a)

No web-based application exists in a vacuum. All applications, even the smallest, will rely on data from an external source, be that a service or API that you/your organization controls or a third-party service. Either way, your application will need to fetch or send data as a way of interacting with that service.

There are many libraries in the JS ecosystem that facilitate this communication, but in the Vue ecosystem, there are two libraries that are generally the accepted ways of performing this interaction: the Fetch API and Axios. It doesn't matter which library is used to interact with a remote API, if it is intended to be used in an async action in a Pinia, it needs to return a Promise to fulfil the async/await contract. As these API interacting libraries tend to be asynchronous anyway, this should not be an issue.

Using the Fetch API from your component is simple. The following example wraps the call to fetch in a function for easier reuse and error handling, but it can be used at the top level to just fetch data for any part of the life cycle, as required:

1.  <script setup lang="ts">
2.  import { onUpdated, onBeforeMounted, ref, Ref } from 'vue'
3.  const data: Ref<DataType> = ref({})

5.  async function getData() {
6.  try {
7.  const response = await fetch('API-endpoint')
8.  data.value = await response.json()
9.  ...
10.  } catch (err) {
11.  // handle error
12.  }
13.  }

15.  // fetch data before component is mounted and
16.  // when component is updated
17.  onBeforeMounted(() => { getData() }) 
18.  onUpdated(() => { getData() })
19.  </script>

However, this is not how these interactions are usually created in a professional setting. In most cases, an interface layer or more likely with Vue, a composable is created so that it only needs writing once and can be reused across the application. How this is achieved is largely an organizational issue. One way to achieve this is to use the useFetch composable that is available from VueUse, which has a full featured and well-tested API:

1.  <script setup lang="ts">
2.  import { useFetch } from '@vueuse/core'
3.  ...

5.  const data: Ref<DataType> = ref({})
6.  const { responseData } = await useFetch('API-endpoint')
7.  data.value = await responseData
8.  </script>

[Integrating Axios into an application](#contents.xhtml_sc2_301a)

The default library for interacting with APIs from a Vue application has traditionally been Axios. With the Fetch API or other contemporary libraries, this is no longer the only library in this space, but it is still the most prevalent way to access remote APIs.

With Vue, composition API and VueUse, using Axios is now as simple as using the Fetch API as presented in the previous example, when used at a component level. Again, the best way to use this functionality is to extract it out into a reusable function so that using it is consistent across the application.

There are slight differences between using Axios and Fetch API. Firstly, the axios package needs to be installed as it is a third-party package. This is done in the usual way with NPM or Yarn.

1.  $ npm i axios

Then, create a file somewhere convenient in your application code base (e.g., src/composables/useRemote.ts):

1.  import axios from 'axios'
2.  import { useAxios } from '@vueuse/integrations/useAxios'

4.  const instance = axios.create({
5.  baseURL: 'API-endpoint',
6.  ...
7.  })

9.  export async function get(url, params = {}) {
10.  const { execute } = useAxios(url, instance)
11.  return await execute(params)
12.  }

As with all third-party integrations, it pays to read the accompanying documentation.

From here, you should be able to see how easy it is to integrate or compose fetching remote data into your local state store. At a pseudo-code level, you tell the store to perform an action, which, in turn, fetches the data from the remote and updates the application state. From there, you just get the state that you need to power the component. Vue makes this largely transparent with Pinia, VueUse, Suspense and transitions.

[GraphQL-based API access](#contents.xhtml_sc2_302a)

Using a GraphQL endpoint is a little more involved than just making a remote API fetch request. The convenience of using GraphQL comes as an upfront cost in development time, but once the data definitions, query and mutation calls are in place, access to and understanding the data that you can receive from the API become largely transparent.

If you do not know about GraphQL, an excellent primer can be found at [https://graphql.org/learn/](https://graphql.org/learn/) as we are not going to cover the basics here in any detail. However, it should be understood by the reader that the onus is on the consumer to define only the data that this required to power the application and for the API to provide access across the data set, but to only supply what has been requested. The relationship between the consumer of the API and the providing service is somewhat reversed. The basic idea is to reduce the data surface by reducing the data package size that is sent on a request as the consumer dictates what data is needed rather than sending everything.

The usual way of making GraphQL requests is through Apollo. Apollo supplies both parts of the equation: a server part that handles requests (which is outside the scope of this book) and a client that receives the parameters makes and decomposes the response based on the known definitions.

To use GraphQL in a Vue application, you will need to introduce a few additional dependencies:

*   Apollo Client (@apollo/client)
*   Apollo-Composable from Vue (@vue/apollo-composable)
*   GraphQL (graphql)
*   GraphQL-Tag (graphql-tag)

The first thing that you'll need to do is have the Vue instance provide the Apollo client; step-by-step instructions for this are provided at [https://v4.apollo.vuejs.org/guide/installation.html](https://v4.apollo.vuejs.org/guide/installation.html).

You can put a components remote API call via Fetch API/Axios directly in the setup of a component but shouldn't, and you can do the same with GraphQL requests through the @vue/apollo-composable package. Here's a simple example:

1.  <template>
2.  <div>
3.  <p>{{ templateData }}</p>
4.  <button @click="refetch()">Update Template</button>
5.  </div>
6.  </template>

8.  <script setup>
9.  import { useQuery } from '@vue/apollo-composable'
10.  import gql from 'graphql-tag'
11.  import { computed, watch } from 'vue'

13.  const { result, refetch } = useQuery(gql`
14.  query getQueryResult ($param: Type) {
15.  returnData (param: $param) {
16.  id
17.  ...
18.  }
19.  }
20.  `, { param: 'data item' })

22.  watch(() => { console.log(result.value) })

24.  const templateData = computed(() => result.value?.id ?? '')
25.  </script>

If you have a small number of unique queries, putting a query in the component can be a viable thing to consider. However, once you need to reuse queries across components, this approach is not viable.

The best way to handle this is to create a space (folder) underneath the src/ to hold the queries and mutations that you build:

![Graphical user interface, application Description automatically generated](images/Figure_13.1.jpg)

Figure 13.1: GraphQL folder underneath src/

Code organization here is largely based on personal preference or company guidelines. The author has found that individual files that define functional boundaries dictated by the applications requirements are best, that is, users, accounts, products, settings, etc.

Each of these files exports all the queries/mutations that you need for that part of the application:

1.  import gql from 'graphql-tag'

3.  export const GET_QUERY_RESULT = gql`
4.  query getQueryResult ($param: Type) {
5.  returnData (param: $param) {
6.  id
7.  ...
8.  }
9.  }
10.  `

From here, you can use the query in the same way:

1.  import { useQuery } from '@vue/apollo-composable'
2.  import { GET_QUERY_RESULT } from 'path/to/graphql/queries/query-file'
3.  import { reactive } from 'vue'

5.  const params = reactive({ ... })
6.  const { result, ...other options... } = useQuery(GET_QUERY_RESULT, params)
7.  ...

This is easier to read as a developer, and with a good naming convention, it should be obvious what the query is doing.

The Apollo composable package is documented at [https://v4.apollo.vuejs.org/guide-composable](https://v4.apollo.vuejs.org/guide-composable), but the documentation is vague in places.

[Conclusion](#contents.xhtml_sc2_303a)

In Vue2, the use of an application-wide state store (Vuex) was almost a requirement for all but the smallest applications; with Vue3 and the Composition API, a similar type of store, Pinia, isn't always a requirement as each composable can maintain its own state. However, Pinia becomes incredibly useful when you need to hold data from a single/multiple endpoints or API types, if you need to cache data or present it across multiple components at the same time.

The ability to aggregate and maintain disparate elements of the state is the strength of Pinia.

The topic of the next chapter is testing Vue components, composables and applications.

# [CHAPTER 14Testing Vue.js Applications](#contents.xhtml_ch14a)

[Introduction](#contents.xhtml_sc2_304a)

So far, we have only discussed building an application. That is, however, only part of a developer's job. In this chapter, we will briefly cover how to test parts of the application to ensure that it does what is expected. This is going to be a relatively broad yet quite shallow chapter.

[Structure](#contents.xhtml_sc2_305a)

This chapter covers the following topics:

*   The benefits of testing
*   Types of tests and tools to use
*   Adding tests to a Vue project
*   Testing components
*   Testing events
*   Testing composable
*   Testing Pinia and routing
*   Using Nightwatch for E2E testing

[Objectives](#contents.xhtml_sc2_306a)

This chapter will cover the basics of testing. Testing is itself an important topic, large enough to cover multiple books, so this will be a high-level view of how to add test coverage to your application and will be enough to get you started.

We will briefly cover testing components, events, routing, and Pinia actions (and, by extension, testing of composables), and finally, we will go over end-to-end testing.

[The benefits of testing](#contents.xhtml_sc2_307a)

Software testing is an integral part of the software development cycle. It does not matter if your team follows TDD, BDD, or any other acronym to denote testing practice or if your tests get written post-development. The point is that any written code will need testing. As a professional developer, you will be expected to be able to test your code adequately.

Apart from your employer's expectations regarding software correctness and user requirements, you need to provide high-quality, reliable, easy-to-understand code. In some environments, tests are used as living project documentation.

There are a few minor caveats that should be understood at this point:

*   Even though a test covers application code, it does not mean that the code does what it is expected to do, meets the user requirements, or is adequately protected. When developing (or reviewing) the tests, ensure that edge cases are addressed and the functionality produces the desired results.
*   Having 100% test coverage is not always a sign of a healthy codebase. Unless your application deals with people's health or money, writing tests comes with diminishing returns and 100% coverage is probably not required. Ensure that core functionality is covered and you have at least some tests covering each of your component's external interfaces; this will be sufficient for most web applications. We are not advocating a fixed percentage coverage here; it is an organizational decision that can comprise many factors.

When writing tests, you're not only ensuring that your code meets the expected criteria in terms of functionality and quality, you're also helping the next person who touches the code or helping remind the future you of how things are supposed to work: this is called living documentation. In practice, tests should be run to ensure that the code executes as expected before any code changes happen; and when the code is updated, the tests also need to be updated so that they reflect the new functionality.

[Types of tests and tools to use](#contents.xhtml_sc2_308a)

Tests are categorized by how close they are to the code and the overall scope that the test covers.

This section covers the tests working developers usually encounter and some testing tools available in the Vue.js and broader JS/TS ecosystems. The number of tools available for testing codes are enormous, and the space is limited, so we will cover using Vitest (with VitestUI), Testing-library/vue, Istanbul, and Nightwatch. We will cover adding these packages and configuration in the adding tests to a Vue project below.

[Unit tests](#contents.xhtml_sc3_309a)

The tests that are closest to the code and test individual units are called unit tests, and these usually cover particularly a small amount of functionality, a function or a minor component, or a code that is limited in scope.

Unit tests should be short and easy to understand. They should test only one aspect of the code so that multiple tests cover the same piece of code. Ideally, at a minimum, there should be two-unit tests for each code unit: one that positively exercises the code; it tests whether the output of the coding unit returns the expected data in a correct format and another that measures anticipated failure or error output. This is a guideline. Writing tests is about showing that the code does what is expected and ensuring that it behaves when something unexpected happens.

When building applications with a component-based framework, like Vue.js, depending on your definition, a coding unit can be a single component or a composable. However, depending on the scope of the component, it might be a part of the functionality. In some cases, testing components might be seen as integration testing, which is about perspective.

In this book, unit tests will be created using Vitest, a newer framework with the same semantics as Jest. It is recommended that Vitest is used over Jest for newer projects and Jest is used only if you already have a test suite built on it. These are not the only options available to you; these are the most likely ones to be used.

[Component/integration tests](#contents.xhtml_sc3_310a)

Integration tests are used to ensure that your components work together as expected. As mentioned, integration testing might also cover single features depending on the definition.

Component tests must cover props, events, slots, styles, classes, and hooks. This means you must measure what happens when you provide the expected information and what happens when these are not supplied.

Each component should have its own set of tests, ideally in its test file. This way, you can avoid having to mock child components. These tests should ensure that the components interact as expected, as a user would interact with them. Again, you focus on the public interfaces and are interested in what the feature does and how it performs; that is not a test concern. This way, implementations might change but the measured outputs remain the same.

Recommendations for integration tests include using Vitest with @testing-library/vue (the setup we will use in this book) or Cypress component testing. Both approaches have pros and cons, and we are going for speed over scope. Refer to the following link for more details:

[https://vuejs.org/guide/scaling-up/testing.html#component-testing](https://vuejs.org/guide/scaling-up/testing.html#component-testing)

[End-to-end tests](#contents.xhtml_sc3_311a)

End-to-end (E2E) testing is designed to emulate entire journeys untaken by users, such as navigating through a site, product selection, completing a payment successfully or unsuccessfully, and sign-ups and account registrations. One thing that's common is that they must mirror a user's behavior and, as such, must perform the task through a browser. E2E tests are typically expensive to create and run for all but the most trivial tasks in execution time and development effort. However, E2E tests catch issues that unit and component tests cannot, like network outages, state management failures, database fallout, missing assets, and so on.

Due to this, E2E testing is usually performed in a separate staging environment that models a production or deployment environment as much as possible and is hence, performed as part of a continuous integration or deployment pipeline as a last-chance safety net before the code is released into the wild.

In many cases, E2E testing solutions only support a limited number of browsers, usually Chromium-based ones, which might suit your use case. We are using Nightwatch in this book because it offers the broadest range of browser support.

[Adding tests to a Vue project](#contents.xhtml_sc2_312a)

To add tests to a Vue.js project, you must include the relevant packages that add a test runner/test framework, a code coverage tool, and an end-to-end testing package. While not all organizations give importance to e2e testing and opt for some other type of user testing, it pays to be aware of the tools used in the industry.

[Adding Vitest and VitestUI](#contents.xhtml_sc3_313a)

Vitest is the first thing to add, and it is installed just like any other NPM package:

1.  $ npm i -D vitest @vitest/ui jsdom

With this in place, you must provide a configuration file defining how you expect the test runner to work. This will be where you will configure most of the testing environment. While there are many options available for you to explore, you will need to create a vitest.config.ts in the root of your application, next to the tsconfig.js, package.json, and vite.config.ts files.

The contents of this file are as follows:

1.  import { defineConfig } from 'vitest/config'
2.  import Vue from '@vitejs/plugin-vue'

4.  export default defineConfig({
5.  plugins: [Vue()],
6.  test: {}
7.  })

This file sets up a default configuration; there are no overrides.

Add the following to the test object:

1.  test: {
2.  globals: true,
3.  environment: 'jsdom',
4.  ...

This allows us to run tests against the template code as the default is a node.

You can now add some script definitions to the package.json file to handle running the tests. Update the script's part to include the following:

1.  ...,
2.  "scripts": {
3.  ...
4.  "test": "vitest dev",
5.  "test-ui": "vitest --ui",
6.  "coverage": "vitest  --coverage",
7.  },
8.  ...

We are adding the coverage line here, which will be added next.

[Adding Istanbul code coverage provider](#contents.xhtml_sc3_314a)

There are two ways of adding Istanbul to the application setup. The easiest is to add it to the configuration and then let the test runner install it when needed.

Update the vitest.config.ts file, adding the following to the test section:

1.  test: {
2.  ...
3.  coverage: {
4.  provider: 'istanbul',
5.  reporter: ['html']
6.  },
7.  ...

The first time you call the coverage script (npm run coverage), the test runner will look to install the relevant packages. We are only adding the HTML reporter here, but you can add others as necessary.

To install Istanbul manually, you will need to do the following:

1.  $ npm i -D @vitest/coverage-istanbul

To test the components, we will mount them, essentially creating a test scaffold that allows us to test components in isolation. We will install that next.

[Component mounting with @testing-library/vue](#contents.xhtml_sc3_315a)

Installing (and configuring) is done by running the following on your terminal:

1.  $ npm i -D @testing-library/vue

The last thing we will add is Nightwatch so that we can perform end-to-end testing.

[Adding Nightwatch](#contents.xhtml_sc3_316a)

Those of you familiar with Vue2 might also be familiar with Nightwatch, as it was the default when creating a project with the Vue CLI; at the time of writing, Nightwatch shares this space with Cypress. Adding Cypress is covered in the Vitest documentation, whereas Nightwatch is not.

The first thing to do is install the relevant dependencies, which is done with the following:

1.  $ npm init nightwatch

This script will ask several questions, and the appropriate answers, in order, are as follows:

*   y
*   End-to-end testing
*   Either JS/default or TS/default
*   Whichever browser you like
*   e2e-tests
*   [http://localhost:9000](http://localhost:9000)
*   On localhost
*   Your preference
*   Your preference

This creates a nightwatch.conf.js file for you with all the relevant configuration settings.

We need to amend this nightwatch.conf.js file at the root of the project with the following:

1.  module.exports = {
2.  plugins: ['vite-plugin-nightwatch']
3.  }

We also need to tell vite that we are using this plugin and amend the vite.config.js file with the following content:

1.  import { defineConfig } from 'vite'
2.  import nightwatchPlugin from 'vite-plugin-nightwatch'

4.  export default defineConfig({
5.  plugins: [
6.  // ... other plugins, such as vue() or react()
7.  nightwatchPlugin({
8.  componentType: 'vue'
9.  })
10.  ]
11.  })

To test that all this works, run the following test script that Nightwatch  provides:

1.  $ npx nightwatch ./nightwatch/examples/basic/ecosia.js

With a successful response, the Nightwatch is installed and working. You can now update package.json with a relevant script.

[Testing components](#contents.xhtml_sc2_317a)

Testing a component requires the component to be mounted in a test harness, usually in isolation, so that the inputs can be easily controlled and the outputs measured. The test harness we will use is provided by Vue Testing Library, which has a fully featured API for which you will use the render() function the most. This function generates the component DOM and associated child components in memory so that we can inject props and assert that the returned output is correct.

The render() function provides a set of queries you can use against the returned component DOM to aid with inspection, which we will discuss momentarily. The render function also gives access to the container (the wrapper HTML element), the baseElement, (usually document.body), the rendered HTML, and any emitted events.

The render function queries combine a query variant from the left side of [Figure 14.1](#ch14.xhtml_fig14-1) and a search type from the right. The combination of these two elements from the given assortment provides a query function with access to the DOM from the render.

![Diagram Description automatically generated](images/Figure_14.1.jpg)

Figure 14.1: Testing library variant and type combinations

Components must be tested to simulate how users interact with them. Tests should not be used to assert the private state of the element, nor should they be used to test any secret methods. These are internal to the component. Testing component internals makes tests brittle and can prove overly expensive to maintain. Generally, component tests need to cover public interfaces; by this, we are talking about the rendered DOM, any emitted events, and any props and slots. We are looking at what the component does rather than its process.

First, we will start testing the landing page; it is a logical place to start, and the components are elementary. While the tests can be written in TypeScript, we will use JS. This way, we will not have to worry about type information. The components on this page are limited to the LandingPageComponent, HeroComponent, and Offer(s)Components.

We will start creating the tests by starting with the HeroComponent. In the tests folder, set up a folder structure that mirrors the structure under src/ and place the following files:

1.  $ mkdir -p tests/pages/site/landing-page
2.  $ touch tests/pages/site/landing-page/landing-page.test.js
3.  $ touch tests/pages/site/landing-page/hero-component.test.js
4.  $ touch tests/pages/site/landing-page/offer-component.test.js
5.  $ touch tests/pages/site/landing-page/offers-component.test.js

In the hero-component.test.js file, add the following contents:

1.  import { render } from '@testing-library/vue'
2.  import HeroComponent from 'src/components/pages/site/landing-page/HeroComponent.vue'
3.  import { createRouter, createWebHistory } from 'vue-router'

5.  describe('Hero Component', () => {
6.  test('should render and show a button', async () => {
7.  const router = createRouter({
8.  history: createWebHistory(),
9.  routes: [{ path: '/', component: HeroComponent }],
10.  })
11.  const { getByText } = await render(HeroComponent, { global: { plugins: [router] } })

13.  const button = getByText(/menu/i)
14.  expect(button).toBeInstanceOf(HTMLButtonElement)
15.  expect(button.className).toContain('red-button')
16.  })
17.  })

Here, we are looking for some text containing a menu, and we expect this text to be held in an HTMLButtonElement with a CSS class list that includes red-button. We are not testing whether the button performs the navigation, but we will do that when we write the E2E tests.

Running this with npm run test on your terminal, you should see something like the following output:

1.  ✓ tests/components/pages/site/landing-page/hero-component.test.js (1)

3.  Test Files  1 passed (1)
4.  Tests  1 passed (1)
5.  Start at  21:45:59
6.  Duration  2.52s (transform 1.09s, setup 0ms, collect 1.07s, tests 30ms)

9.  PASS  Waiting for file changes...
10.  press h to show help, press q to quit

The npm script runs the tests and sets up a watcher to cause the test suite to rerun when the tests change, so you get feedback each time.

If you quit this and run the test-ui script (npm run test-ui) instead, you will launch the Vitest UI, which presents more information and allows you to explore more details about your tests.

If you place the following content into the offer-component.test.js file and save it, the VitestUI updates with the latest test information. As you can probably tell, the VitestUI is a valuable tool in building your test structure. Consider the following code:

1.  import { render } from '@testing-library/vue'
2.  import OfferComponent from 'src/components/pages/site/landing-page/OfferComponent.vue'

4.  describe('OfferComponent', () => {
5.  test('should render', async () => {
6.  const { getByTestId } = await render(OfferComponent, {
7.  props: { id: 1, text: 'Test', image: 'image.png' }})
8.  const component = getByTestId('offer')
9.  expect(component).toBeInstanceOf(HTMLElement)
10.  })
11.  test('should have a red button', async () => {
12.  const { getByText } = await render(OfferComponent, {
13.  props: { id: 1, text: 'Test', image: 'image.png' }})
14.  const component = getByText(/Test/)
15.  expect(component).toBeInstanceOf(HTMLButtonElement)
16.  })
17.  test('should render a received image', async () => {
18.  const { html } = await render(OfferComponent, {
19.  props: { id: 1, text: 'Test', image: 'image.png' }})
20.  const componentHTML = html()
21.  expect(componentHTML).toContain('image.png')
22.  })
23.  })

The changed test code will result in a change in VitestUI output, as presented in [Figure 14.2](#ch14.xhtml_fig14-2):

![Text Description automatically generated](images/Figure_14.2.jpg)

Figure 14.2: Output of VitestUI after change to tests

The tests here are the tip of the iceberg; you still have plenty of work to do on testing components. So far we have only looked at testing templates, we've not touched on events emitted by a component. We will cover this in the next section.

[Testing events](#contents.xhtml_sc2_318a)

At least with a testing library, event testing is very similar to how you would test a component. You would try a component event alongside testing whether the features render correctly.

To access event testing, import the fireEvent method from testing-library/vue. Look at the following code sample on how to do this.

In principle, you would use render() to create the subject under test, find the element(s) that have events attached, trigger the event(s), and check the results. Primarily, these events will be connected to form controls and buttons, links, lists, and tables. This is not an exhaustive list as events can be attached to any component.

A simple example is covered in the documentation, which covers a standard counter example, which follows more/less the following:

1.  import  Counter from './counter.vue';
2.  import { render, fireEvent } from '@testing-library/vue';

4.  describe('Counter', () => {
5.  it('should increment counter value', async () => {
6.  const { getByText } = render(Counter, { props: { initialValue: 0 } })
7.  getByText('0') // implicit assertion
8.  const btn = getByText('increment')
9.  await fireEvent.click(btn)
10.  getByText('1')
11.  })
12.  })

The fireEvent method re-exports all the events that are detailed at the following link:

[https://github.com/testing-library/dom-testing- library/blob/main/src/event-map.js](https://github.com/testing-library/dom-testing-library/blob/main/src/event-map.js)

This list includes all the everyday DOM events: click; change; touch; mouseover/up/down/enter etc.; drag/drop events; cut/copy/paste, among others. It is worthwhile taking some time to look over the list.

In many ways, the testing library asserts that events perform the expected action, at least at a component level, as simple as a component test. Consider the following code:

1.  import AddToCart from '/src/.../AddToCartComponent.vue'
2.  import { render, fireEvent } from '@testing-library/vue'

4.  describe('AddToCartComponent', () => {
5.  it('should increment a counter', async () => {
6.  const { getByTestId, getByText, getByLabelText } = render (AddToCart, { props: { item: { id: 1, image: 'image.png',
7.  description: 'this is a description',
8.  name: 'test 1', price: 23.99, }, }, })

10.  const incButton = getByTestId('incrementButton')
11.  const decButton = getByTestId('decrementButton')
12.  const outputControl = getByLabelText(/item\scount/i)

14.  getByText(/23.99/)
15.  getByText('Add to Cart')

17.  expect(outputControl.value).toBe('1')
18.  await fireEvent.click(incButton)
19.  expect(outputControl.value).toBe('2')
20.  await fireEvent.click(decButton)
21.  expect(outputControl.value).toBe('1')
22.  })
23.  })

Next, we must ensure that a component that emits an event affects a parent's state and provides the expected data. We do this with the emitted() function, as demonstrated in the following code:

1.  import CheckoutPageComponent from '../../../../../src/components/pages/site/checkout-page/CheckoutPage.vue'
2.  import { render, fireEvent } from '@testing-library/vue'

4.  describe('CheckoutPage', () => {
5.  it('should emit a updateCartWithVoucherCode event', async () => {
6.  const { getByLabelText, emitted, getByText } = render(CheckoutPageComponent)
7.  const testCode = 'voucherCode'

9.  await fireEvent.update(getByLabelText('Voucher Code'), testCode)
10.  await fireEvent.click(getByText('Apply'))

12.  expect(emitted().updateCartWithVoucherCode).toBeTruthy()
13.  expect(emitted().updateCartWithVoucherCode.length).toBe(1)
14.  expect(emitted().updateCartWithVoucherCode[0]).toEqual([testCode])
15.  })
16.  })

Here, we are checking to see if the event fired with toBeTruthy() is fired only once and whether it returns the voucher code it was given from the updateCartWithVoucherCode event.

We only concern ourselves with the external contract of the component. We do not care what state is internal to the component, only that it behaves as we expect.

The next subject that we will turn our attention to is testing composables.

[Testing composables](#contents.xhtml_sc2_319a)

Composables should be tested like normal functions: with unit tests. Again, as with other testing, we only need to measure outputs based on given inputs, even if they are mocks. Internals do not concern us.

Unit tests are simple, or at least they should be. All you are doing is testing a small unit of your code (a function); the functionality of a composable is based on pure code. If your composable is required to access an outside service, it might be better served using an integration test to model the external inputs/outputs. In this instance, you need to consider how you design and implement your code. Often, it pays dividends to write a pure functional core that can be unit tested, which ensures that the code behaves as expected as third-party inputs are mocked. This ensures that the communication to the third-party service is pushed to the boundary of the composable where integration testing can be used to measure the side-effects. This is good code design.

Vitest gives us many of the required tools right out of the box, and writing a unit test is not very different from writing a component test. The only significant difference is that the composable is not mounted (rendered).

Let us go over some simple examples. As it happens, we have an excellent composable in useCart, and it does several things and has a few functions that we can test.

Let us start by setting things up. We will check that we can get a cart and that it is empty when we first initialize it:

1.  import { useCart } from '../../src/composables/useCart.ts'

3.  describe('useCart', () => {
4.  it('should return an empty cart on initialisation',
5.  () => {
6.  const { getCart } = useCart()
7.  const cart = getCart()
8.  expect(cart.value).toHaveProperty('items')
9.  expect(cart.value.items.length).toBe(0)
10.  })
11.  })

Simple enough, get the cart, check the contents, and ensure that they are 0.

Next, we must ensure that we can manipulate the cart's contents by adding (only CartItems) and removing items. Consider the following code:

1.  it('should allow you to add and remove items', () => {
2.  const testItem = {
3.  id: 1, name: 'test item', qty: 1, price: 10.0
4.  }
5.  const { addItem, removeItem, getCart } = useCart()

7.  addItem(testItem)
8.  expect(getCart().value.items).not.toHaveLength(0)
9.  expect(getCart().value.items).toHaveLength(1)
10.  removeItem(1)
11.  expect(getCart().value.items).toHaveLength(0)
12.  })

However, consider a case wherein we look to add something other than a CartItem, which our IDE might helpfully complain about, as follows:

1.  it('should not accept non-CartItem contents', () => {
2.  const { addItem, getCart } = useCart()
3.  const cart = addItem(1)
4.  expect(getCart().value.items).toHaveLength(0)
5.  })

Our current implementation of the addItem() function fails the test. Even though 1 is not a CartItem, it is still accepted at a JavaScript level. What we are encountering here is the dynamicity of JavaScript around typing. We must update the code in the composable under test to get our test to pass.

To make this happen, we will add a type guard function to the cart and update the addCart function to use it, even though we would have the option of ignoring errant data. We will have the function throw an exception; we only expect CartItems, so anything else indicates a problem. Consider the following code:

1.  function isCartItem(item: any): item is CartItem {
2.  if ((item as CartItem).id) {
3.  return true
4.  }
5.  return false
6.  }
7.  function addItem(item: CartItem): Cart {
8.  if (isCartItem(item)) {
9.  cart.value.items.push(item);
10.  return cart;
11.  }
12.  throw new Error("Requires a CartItem to be supplied")
13.  }

We still fail when we rerun the tests, but it is for the right reason. The test does not check for an error response, so we must update that too. Consider the following code:

1.  it('should not accept non-CartItem contents', () => {
2.  const { addItem } = useCart()
3.  expect(() => addItem(1)).toThrowError(/incorrect type/i)
4.  })

With this test, we have accounted for the fact that we expect an error when sending in an incorrect type.

The next test covers updating the cart. From a code perspective, the expectation is that the cart's contents are updated, with the internal list of cart items being replaced. This follows the functional programming model of doing a data transform rather than an in-place mutation. The test looks somewhat like the following code:

1.  it('should allow you to update the cart items', () => {
2.  const testItem = { id: 1, name: 'test item', qty: 1, price: 10.0 }
3.  const { addItem, updateCart, getCart } = useCart()
4.  addItem(testItem)
5.  expect(getCart().value.items).toHaveLength(1)

7.  const newItem = { ...testItem, qty: 2 }
8.  const newCart = updateCart([newItem])
9.  expect(newCart.value.items).toHaveLength(1)
10.  expect(newCart.value.items[0].qty).toBe(2)

12.  // passing no value resets the cart
13.  updateCart()
14.  expect(getCart().value.items).toHaveLength(0)
15.  })

Lastly, a set of computed properties of the cart should be seen as the standard for any cart implementation. We will test these together:

1.  it('should compute some standard totals across the cart',  () => { 
2.  const { subtotal, tax, delivery, total, updateCart } = useCart()
3.  const testItems = [
4.  { id: 1, name: 'test item', qty: 1, price: 10.0 },
5.  { id: 2, name: 'test item', qty: 1, price: 5.0 },
6.  { id: 3, name: 'test item', qty: 2, price: 17.99 }
7.  ]
8.  updateCart(testItems)

10.  expect(subtotal.value).toBe("50.98")
11.  expect(tax.value).toBe("10.20")
12.  expect(delivery.value).toBe("5.00")
13.  expect(total.value).toBe("66.18")
14.  })

This pretty much finishes off the testing of this composable; a coverage check confirms that most of the code in the file has been tested. There is a small branch of code that has not been covered. If you feel it is essential, amend the tests to cover this, but the logic internal to the function is simple enough not to require it.

With testing of many of the significant parts of the application in place, we need to turn our attention to ensuring that when someone navigates to a particular page, they arrive there and that any data that we place in a Pinia store behaves as expected; this is the focus of the next section.

[Testing Pinia and routing](#contents.xhtml_sc2_320a)

This section covers the testing of some of the ancillary services that are common when building component-based applications.

[Pinia](#contents.xhtml_sc3_321a)

When testing web apps that use Pinia, you need to consider two things: testing the store itself to make sure it behaves as expected, and testing components that utilize the store to ensure that any stores used are integrated correctly.

When testing the store, it is essential to realize that all tests require an instance. The following code achieves this:

1.  import { setActivePinia, createPinia } from 'pinia'
2.  // import store

4.  describe('Store Test', () => {
5.  beforeEach(() => {
6.  setActivePinia(createPinia())
7.  })
8.  it('should do store stuff', () => {
9.  // test aspects of store
10.  })
11.  ...
12.  })

If your store relies on plugins, these will need to be initialized and injected into an empty app, as follows:

1.  import { setActivePinia, createPinia } from 'pinia'
2.  import { createApp } from 'vue'
3.  import { plugin } from '../path/to/plugin'
4.  // import store

6.  const app = createApp({})
7.  describe('Store Test', () => {
8.  beforeEach(() => {
9.  const pinia = createPinia().use(plugin)
10.  app.use(pinia)
11.  setActivePinia(pinia)
12.  })
13.  ...
14.  })

With either of these approaches, each test receives an individual store instance so that each aspect of the store can be tested in isolation. The following tests should be standard unit tests, as discussed in the Testing composables section earlier and testing a component that uses a Pinia store is more complicated.

The first thing that we will need to do is install the Pinia testing instance:

1.  $ npm i -D @pinia/testing

Then, each time you create a component that needs a Pinia instance, you mount the component with the test instance instead of through the render options object. Consider the following code:

1.  import { createTestingPinia } from '@pinia/testing'
2.  import { render } from '@testing-library/vue'
3.  import { useUserAccountStore, OrderItemStatus, OrderStatus } from '/src/store/useUserAccountStore'
4.  import ProfileOrdersPage from '/src/components/pages/profile/orders-page/ProfileOrdersPage.vue'

6.  describe('ProfileOrders Page', () => {
7.  it('should...', async () => {
8.  const component = render(ProfileOrdersPage, {
9.  global: {
10.  plugins: [
11.  createTestingPinia({
12.  stubActions: false,
13.  initialState: {
14.  userAccount: {
15.  orders: [
16.  ..., ], ...

18.  const store = useUserAccountStore()
19.  const { queryAllByText } = render(component)
20.  expect(store.getOrderSubtotal(1)).toBe(5)
21.  expect(store.getOrderSubtotal(2)).toBe(105)
22.  expect(store.getOrderTotal(1)).toBe(12)
23.  expect(queryAllByText(/^test item 1$/)).toHaveLength(2)
24.  })})

Here, we are creating a test instance with some initial data that we ensure is available in the store, and because the testing instance stubs actions by default, we are passing in the switch (stubActions) to turn that off; we then look at the rendered content to check that it's rendering expected range. So far, we are only writing passing tests. As an exercise for you, write some tests that measure failure mechanisms (you will need to make some code changes to the store code to handle a failure). If you intend to use the same store setup across several tests, it pays to put the setup in a beforeEach() handler.

There is more to the Pinia test instance that can be covered. It is a good idea to read through the Pinia test documentation:

[https://pinia.vuejs.org/cookbook/testing.html](https://pinia.vuejs.org/cookbook/testing.html)

[VueRouter](#contents.xhtml_sc3_322a)

Testing routing is done by creating a router in abstract mode and then passing it into the render function options object. Using the router in abstract mode prevents the default behavior of the router from storing navigation changes. The initialization routine is often abstracted into a helper function to be used where necessary. Consider the following code:

1.  import { render } from '@testing-library/vue'
2.  import { createRouter, createWebHistory } from 'vue-router'

4.  export async function renderWithRouter(component, 
    routes, renderOptions) {
5.  const router = new VueRouter({
6.  history: createWebHistory(),
7.  routes
8.  })

10.  const result = render(component, {
11.  ...renderOptions,
12.  global: { plugins: [router]},
13.  })

15.  await router.push('/')
16.  return result
17.  }

This utility allows you to manage which routers are used by a test. Line 6 holds the abstract mode setting. The router.push() on line 15 is essential because the initial stack is empty, creating an initial state value.

This function is then used as a replacement for the render() function supplied by the testing library. However, handling navigation between components is done by the async handler. Consider the following code:

1.  import { render, waitFor, fireEvent } from '@testing-library/vue'
2.  ...
3.  import App from '/src/App.vue'
4.  import { renderWithRouter } from './render-with-router.js'

6.  describe('Landing page navigation', () => {
7.  it('should navigate', async () => {
8.  const { queryByText, getByText } = await renderWithRouter(App, [
9.  ... routes array ...
10.  ])

12.  const menuButton = await getByText('View Our Menu')
13.  await fireEvent.click(menuButton)
14.  await waitFor(() => {
15.  expect(window.location.href).toContain('/menu')
16.  })
17.  await queryByText(/Menu\sPage/i)
18.  })
19.  })

To get this to work successfully, you need to render a component with a <router-view> that wraps the components you want to navigate between; otherwise, the routing cannot happen.

With this in place, you can see how easy it is to test routing between individual components through simple user navigation. The next section covers user journeys across the application and discusses end-to-end testing.

[Using Nightwatch for E2E testing](#contents.xhtml_sc2_323a)

Writing end-to-end tests using Nightwatch is quite similar to how we have been building other kinds of tests for this application.

However, there are slight differences. Remember that you are running a click path through an active application, as a user would. To do this, you must initialize a browser instance and point it at an entry URI. The fluid interface provided by the browser instance is then used to create a user flow, navigating the application like a user, with assertions being made about  what a user should see on a page and to model user interactions and UI responses.

Typically, e2e journeys cover the following:

*   Login processes and navigation to a registered user-only resource
*   Registration processes
*   The product purchase process, also known as sales journey
*   Product recommendations and dynamic data outputs

This is not an exhaustive list. There are many reasons why e2e testing would be employed to ensure user experience and safety while enjoying your web application content.

As a primer, examine the following to show how easy building an e2e test flow is:

1.  describe('Create a test order', () => {
2.  before(browser => browser.navigateTo('http://localhost:9000/'))

4.  it('should order the first item in menu list', (browser) => {
5.  browser
6.  .waitForElementVisible('body')
7.  .assert.textContains('body', 'View Our Menu')
8.  .click(element('.hero button.red-button'))
9.  .waitForElementVisible('h1')
10.  .assert.visible('input[name=itemCount]')
11.  .setValue('input[name=itemCount]', 2)
12.  .assert.visible('button[type=button].add-to-cart')
13.  .click('button[type=button].add-to-cart')
14.  // ... rest of journey
15.  })

17.  after(browser => browser.end())
18.  })

To run this test, make sure the application is running, and in another terminal, run npx nightwatch –env default; and all being well, the test will run and successfully conclude.

In many ways, writing an e2e test with Nightwatch is much simpler than creating a unit test, especially when mocking is involved.

[Conclusion](#contents.xhtml_sc2_324a)

Writing tests might seem like a waste of development cycles for those lacking experience. Still, the effort in writing tests is rewarding in getting some confidence that the code that has been written behaves as expected and conforms to any written specifications. Tests are also seen as living documentation over and above any code comments, and code comments can become stale or misaligned with code changes; developers are inherently lazy when explaining things in code. It is more complicated with tests. If tests become misaligned, they fail, which in most cases, will be picked up before the code reaches a client or an end user.

Writing tests alongside your code, before, during, or after helps you make decisions around code design and implementation, making it better for you and anyone that follows you to maintain the application.

In the next chapter, we'll use all the aspects of Vue.js that we've already covered and see how they can be used in a framework setting; we're going to use Nuxt.js for this.

[Points to remember](#contents.xhtml_sc2_325a)

*   Test small units of code with unit tests.
*   A component is a unit of code.
*   Good code design usually makes testing easier.
*   It does not matter when tests are written so long as they are written.
*   100% test coverage can be counter-productive.
*   Make sure edge cases are covered.

[Key terms](#contents.xhtml_sc2_326a)

*   Unit test
*   Integration test
*   End-to-end test
*   Component test
*   Pure code
*   Vitest
*   Nightwatch
*   Mounting/rendering

Join our book’s Discord space

Join the book's Discord Workspace for Latest updates, Offers, Tech happenings around the world, New Release and Sessions with the Authors:

**[https://discord.bpbonline.com](https://discord.bpbonline.com)**

![](images/fm1.png)

# [CHAPTER 15Server-Side Rendering with Nuxt.js](#contents.xhtml_ch15a)

[Introduction](#contents.xhtml_sc2_327a)

This chapter will explore how to work with Nuxt.js and what the framework provides. By this point, we have already understood how to build applications with Vue.js as a front end; with Nuxt, we step up the applications' capabilities, having the entire stack on one framework.

[Structure](#contents.xhtml_sc2_328a)

In this chapter, we will cover the following topics:

*   Nuxt.js basics and SSR
*   Creating a project with Nuxt and managing dependencies
*   Building the client side of a Nuxt application
*   Managing state and cross-component functionality
*   Building the server side of a Nuxt application

[Objectives](#contents.xhtml_sc2_329a)

Nuxt is a wide topic and would rightly be served by its own book; this chapter will only manage to cover the basics of how to start a project, where the different elements go, and what is different about Nuxt compared to Vue.

Nuxt3 is the latest incarnation of the framework with up-to-date tooling and infrastructure. If you have experience with similar frameworks like Meteor, then some of that knowledge is transferable.

[Nuxt.js basics and SSR](#contents.xhtml_sc2_330a)

Nuxt is a full-stack framework, as its documentation puts it, with hybrid rendering capabilities. Nuxt has several conveniences that make building and managing projects easier:

*   Multiple rendering techniques, depending on routing configuration
*   Standard directory setup
*   Auto-imports project-wide
*   Vue.js view engine
*   Built-in server engine (Nitro)
*   Modular build
*   Transparent TypeScript integration

[Multiple rendering techniques](#contents.xhtml_sc3_331a)

Nuxt is a server-based application framework that can pre-render client-side content, called Universal Rendering, or more traditional client-side rendering as per standard Vue.js. At the time of writing, there are a few more rendering modes in the pipeline: a hybrid approach based on routing where different parts of the application are rendered as SSR or client-side, depending on the configuration. There is also work on rendering content using CDN Edge workers.

The Nuxt team has very firm opinions on how applications should be structured. There is a simplicity to the structure; if you are familiar with frameworks like Ruby on Rails, then the structure used by the framework should not be an issue. The main difference is that with Nuxt, the directory structure is not supplied when you generate an application. You need to add the parts of it that you need yourself. This keeps the application lean; you only add a directory if you need to use that functionality.

The following figure shows what a complete directory structure requires:

![Graphical user interface Description automatically generated with low confidence](images/Figure_15.1.jpg)

Figure 15.1: Standard Nuxt directory structure

While these are optional in many cases, Nuxt has an intelligent compiler that allows for the conveniences detailed as follows:

*   Auto-imports: The framework auto-imports functionality, such as composables, plugins, and components. Auto-importing operates over several directories within the framework structure.

    The auto-importing can be turned off or made explicit if required.

*   Vue.js view engine and Nitro server engine: The Vue.js part is self-explanatory; that's why we are discussing it in this book.

    Nitro, the built-in web server, is new and specially created for Nuxt3\. It provides many of the conveniences on this list. You can read more at  [https://nitro.unjs.io](https://nitro.unjs.io).

*   Modular build: Nuxt has a module system that can be easily extended with third-party services. Nuxt itself comprises several core packages that work together to deliver the framework.
*   TypeScript integration: TypeScript is the construction language, and the framework exposes this transparently; it can even auto-generate types for you.

SSR with Nuxt: In many ways, using Nuxt on the server is similar to other more traditional server technologies, like PHP or Ruby-on-Rails. However, when using Universal Rendering, the server initially responds with a static page and then subsequently sends the dynamic page code as a separate code packet. It behaves in this manner so that the initial page load (static page data) is much quicker, i.e., the time to render is reduced, but then the extra functionality is supplied to ensure that any interactivity or transitions, i.e., UX, are not lost. This is called “hydration”. One of the benefits lauded around such an approach is that web crawlers (like Google's indexing spiders) can index the site without JS rendering overhead if the crawler is indeed that sophisticated.

[Creating a project with Nuxt.js and managing dependencies](#contents.xhtml_sc2_332a)

Many of these steps will feel familiar, and we are dealing with a project in the JavaScript ecosystem.

The easiest way of creating a Nuxt application is to use the NPX nuxi script, as follows:

1.  $ npx nuxi init <project-name>

Nuxi then installs the basics of the application. Refer to the following figure:

![Text Description automatically generated](images/Figure_15.2.png)

Figure 15.2: Screenshot showing nuxi output

Once that is complete, follow the instructions on the screen, that is, move the application directory and install the dependencies with npm i.

Note: If you open the application folder with VSCode, it might flag an issue with the tsconfig.json file. To solve this, run $ npm i -D @types/node.

Once this is complete, you will end up with a project folder that will look somewhat like the following image. Any differences will be down to the selections that you made in the build script. Refer to the following figure:

![Graphical user interface, application Description automatically generated](images/Figure_15.3.jpg)

Figure: 15.3: Project structure of a new Nuxt project

Running the project is then a case of running the npm dev script:

1.  $ npm run dev

You can then open your browser to point to the application at 'http://localhost:3000' to show this:

![](images/Figure_15.4.png)

Figure 15.4: Basic landing screen

From here, you can start adding to the directory structure elements, layouts, and components, as shown in [Figure 15.1](#ch15.xhtml_fig15-1).

[Building the Client-side of a Nuxt application](#contents.xhtml_sc2_333a)

There are three main sections where UI elements can be placed; these are the layouts, pages, and component directories. Placing your components in these places ensures that they are auto-imported into the project for use. This happens automatically.

We will discuss each of the sections in turn, working from the smallest elements that make up a page, that is, components, to the largest layouts.

[Nuxt components](#contents.xhtml_sc2_334a)

These are standard Vue.js components, as you have already seen. There is no magic here. The magic is in the form of auto-importing, which makes all the components in the directory available throughout the application. The importer is smart enough to also import the any dependent components that are required by imported modules.

The components are auto-registered using the file path and filename as the component name.

As an example of this, look at the following:

1.  <!-- /components/MyComponent.vue -->
2.  <template>
3.  <MyComponent />
4.  </template>

6.  <!-- /components/deeply/nested/Component.vue -->
7.  <!-- nested components are prefixed with the path -->
8.  <template>
9.  <DeeplyNestedComponent />
10.  </template>

If you do not want to use the file path prefix (preceding), then you will need to update the Nuxt configuration in nuxt.config.ts with the pathPrefix option, as follows:

1.  export default defineNuxtConfig({
2.  components: [
3.  {
4.  path: '~/components/',
5.  pathPrefix: false,
6.  },
7.  ],
8.  });

Using this option means the preceding nested example can be changed to the following:

1.  <!-- /components/deeply/nested/Component.vue -->
2.  <template>
3.  <Component />
4.  </template>

It is personal preference or the team's coding standards that dictate which approach you to use.

One issue that you might face with the auto-importing capability is when you are faced with using a dynamic component. The recommended way of resolving this is to use the Vue resolveComponent() helper:

1.  <template>
2.  <component :is="someCondition ? MyComponent : OtherComponent" />
3.  </template>
4.  <script setup lang="ts">
5.  const MyComponent = resolveComponent('MyComponent')
6.  const OtherComponent = resolveComponent('OtherComponent')
7.  const someCondition = computed(() => ...)
8.  </script>

There are ways to globally import components so that resolveComponent() does not need to be used. These are not considered good practices and are not recommended.

Another pattern that you might end up using is lazy-loading components, especially if the components are not required during the initial component render. Using the Lazy prefix, as follows, fixes this:

1.  <template>
2.  <MyComponent />
3.  <LazyOtherComponent v-if="visible" />
4.  </template>
5.  <script setup lang="ts">
6.  const visible = ref(false)
7.  </script>

There are two last issues that we need to address when working with components. The first is rendering a component client-side only, and the second is around component hydration. These two issues are related.

Note: We've already mentioned hydration, but as a reminder, it is where a component is rendered statically on the server and sent to the client alongside the component's dynamic code, which applies interactivity and/or transitions.

To solve these two related problems, Nuxt supplies two filename suffixes: .client and .server.

If a file is marked with .client, it is only rendered client-side. This means that they are only rendered after mounting, as you would ordinarily expect from a Vue.js component.

If you use .server as a suffix, the component is rendered server-side only, and there is no hydration.

There may be circumstances where you have a component split over both .server and .client, as this allows finer control over the hydration or allows you to create and render a separate implementation of the UI post-hydration.

[Nuxt Pages](#contents.xhtml_sc3_335a)

Pages are Vue.js components that hold references to one or more components that constitute a page. The main difference between the components in the components/ directory and those in the pages/ directory is routing. Pages have routing, which is based on subdirectories and filenames.

Note: When building a page component, you need to ensure that the component has a single root element. HTML comments count as elements.

As routing between pages is handled by file and directory names, handling dynamic routes can be a little tricky.

To facilitate this, there is a special syntax that you can use when building the directories and filenames that provide this capability. For a mandatory route parameter, the parameter name is enclosed in [], and for optional, you will need [[]]. See the following example:

1.  --> pages/
2.  ----> index.vue
3.  ----> product-[group]/
4.  ------> [[product_id]].vue

In the presented directory listing, you can see that group is required and will most likely be used in the template; however, product_id is optional. Without it, we might assume that the page will display something different, like a list of all the items in the product group. So, we might see something like the following:

1.  <template>
2.  <main>
3.  <h1>{{ $route.params.group }}</h1>
4.  <section v-if="$route.params.product_id">
5.  <!-- Show specific product details -->
6.  </section>
7.  <section v-else>
8.  <!-- Show group listing component -->
9.  </section>
10.  </main>
11.  </template>

Accessing routing parameters in the templates (or with Options API) is achieved using the standard $route object. Accessing these parameters using Composition API is done via the useRoute() composable.

Route nesting, i.e., child routes, requires you to use the <NuxtPage /> component in each parent to ensure that the child renders where it is supposed to. Rendering or transitions can be controlled using a pageKey prop when using the <NuxtPage /> component.

Pages can also be set up with metadata using the  definePageMeta() compiler macro. There are several special metadata keys that can be used throughout the application. Explanations for these keys can be found in the documentation.

The <NuxtLink /> component is the recommended way to transition between pages. <NuxtLink /> is a drop-in replacement for the familiar <RouterLink /> and has the same API and semantics. Nuxt also allows programmatic navigation by providing the navigateTo() method.

The last thing to mention is that there is component routing, which also gives you a catch-all route. The catch-all route uses the spread operator (…) to watch all the routes that exist under that path.

An example of a catch-all route might be something like /product/[…slug].vue. All routes under this path are captured, with the spread operator coercing all path segments into the slug variable. $route.params.slug is a list of all the segments in the path.

The next part of building UI with Nuxt consists of layouts.

[Nuxt layouts](#contents.xhtml_sc3_336a)

Layouts are wrappers around pages that provide each navigation endpoint with consistent page elements like headers and footers and allow the application of consistent styling.

If your application requires a single layout, a default layout can be placed at ~/layouts/default.vue. The same rules apply for layouts as for other component types. There needs to be only one root element. Additionally, as you will most likely be rendering child components, you will also need to use the <slot /> tag; otherwise, the renderer will not know where to put the page content. Look at the following example:

1.  <!-- layouts/default.vue -->
2.  <template>
3.  <div>
4.  <header><!-- Header content --></header>
5.  <slot />
6.  <footer><!-- Footer content --></footer>
7.  <div>
8.  </template>

All layouts that you need for your application live under the ~/layouts directory. There are several ways of notifying the renderer to select the correct layout.

The first is through the <NuxtLayout /> components name prop. This is a normal prop that can have the usual runtime bindings:

1.  <template>
2.  <NuxtLayout :name="layout">
3.  <!-- slot content -->
4.  </NuxtLayout>
5.  </template>

7.  <script setup lang="ts">
8.  const layout: string = "my-custom-layout" 
9.  </script>

The second is with the definePageMeta() macro which provides a  layout key. The value can either be a string (or something that resolves to a string) or boolean false. If you pass false to this, you need to provide some other mechanism to help Nuxt resolve the layout, either by the name prop or by using the setPageLayout() function in a ref or computed property:

1.  <!-- using definePageMeta() -->
2.  <script setup lang="ts">
3.  // works with both <script setup> and <script>
4.  definePageMeta({ layout: "my-custom-layout" })
5.  </script>
6.  <!-- using setPageLayout() -->
7.  <template>
8.  ...
9.  <button @click="setLayout">Change Layout</button>
10.  </template>

12.  <script setup lang="ts">
13.  function setLayout (): void {
14.  setPageLayout('my-custom-layout')
15.  }
16.  definePageMeta({ layout: false })
17.  </script>

On a per-page basis, when using definePageMeta({layout: false}), so long as there is a <NuxtLayout /> component, each page can specify its own layout file.

The skills you get from building pages and layouts with Nuxt are transferable; most other modern frameworks behave in a similar manner.

Next, we are going to look at managing the state across a Nuxt app.

[Managing state and cross-component functionality in Nuxt](#contents.xhtml_sc2_337a)

Nuxt offers many ways to manage your application's state, as you would expect for a Vue.js framework. Alongside this, there are lifecycle hooks across all the build and runtime stages, plus the ability to inject remote data and middleware.

We will cover each of these in turn.

[useState()](#contents.xhtml_sc3_338a)

Nuxt provides a composable called useState(). This composable is a drop-in replacement for ref or reactive data for SSR. If you're already familiar with React Hooks, this is the same principle.

As it is directly used to support SSR, there are a few small things to be aware of when using it:

*   useState() can only be used in script setup or lifecycle hooks.
*   Data contained inside needs to be JSON serializable.
*   Data is preserved on hydration.
*   The stored state is shared across all components that use it using a unique key.
*   The stored state is reactive.

There are two ways of using this composable: with a key or without; in the latter case, a unique key will be generated for you. The initial value that you provide can be a ref() wrapped value or the return value from a function, so long as the value is JSON-serializable. The following code examples show how to use this composable:

1.  const value = useState(/* primitive value */)
2.  const value = useState('value', () => /* return value */ )

4.  const value = useState('value') // Accesses value

6.  // Global type-safe states (e.g. composables/x.ts)
7.  export const useLetterX = () => useState<string>('letterX', () => 'x')

9.  //With auto-import
10.  <script setup>
11.  const x = useLetterX() // Same as useState('letterX')
12.  </script>

The next part that we can use to manage functionality is lifecycle hooks.

[Lifecycle Hooks](#contents.xhtml_sc3_339a)

As Nuxt is a modern web development framework, which uses Vue.js as a display layer, it gives you the option of handling setup operations and performing remote data calls by allowing you, as the developer, to “hook” into the application lifecycle.

With Nuxt, hooks can be defined to be executed at build time or runtime, both in the front-side application and on the server.

There are too many hooks to list in this book. A full list can be found at [https://nuxt.com/docs/api/advanced/hooks](https://nuxt.com/docs/api/advanced/hooks).

Hooks are far more useful when used in modules, plugins, and middleware.

Next, we will take a quick look at obtaining remote data.

[Remote data](#contents.xhtml_sc3_340a)

We are already familiar with useFetch() and associated functions. In Nuxt, these composables are available only in script setup and lifecycle hooks but are universally available to you throughout the application.

When building an application, you might need to access data from an API. Understandably, accessing remote data might require that you also pass along header data, like cookies or authorization, which you will not have direct access to when in a server context. To handle this circumstance, Nuxt provides the useRequestHeaders() function, which can be used to provide the relevant header data.

There is a section on best practices in the documentation that you should read: [https://nuxt.com/docs/getting-started/data-fetching#best-practices](https://nuxt.com/docs/getting-started/data-fetching#best-practices).

[Error handling](#contents.xhtml_sc3_341a)

Like all frameworks, Nuxt applications can be the source of some unpreventable runtime errors.

There are several points in an application's lifecycle where these errors can occur and where they are most likely to be addressed:

*   Client-side Rendering Life cycle for SSR and SPA:

    Errors during rendering can be captured via the onErrorCaptured() function or by the vue:error hook. If you are using a global error handler, this can be caught by creating a plugin that wraps the global handler through vueApp.config.errorHandler(). A typical example of creating this wrapper is as follows:

1.  export default defineNuxtPlugin((nuxtApp) => {
2.  nuxtApp.vueApp.config.errorHandler = (error, context) => {
3.  // ...
4.  }
5.  })

*   Server and client start-up for SSR and SPA:

    If Nuxt encounters an error at startup, it calls the app:error hook.

*   Server/API lifecycle:

If an error occurs during the server lifecycle, then a server-side handler, at least at the time of writing, cannot be defined. The best practice for this is to render an error page that clears the errors and redirects to a new page. To view an example, visit [https://nuxt.com/docs/getting-started/error-handling#example](https://nuxt.com/docs/getting-started/error-handling#example).

[Composables](#contents.xhtml_sc3_342a)

The application's composables go into the composables/ directory. From here, they are auto-imported so that they can be used across the application. In order for the compiler to auto-generate a types file (.nuxt/imports.d.ts), one of the standard run scripts, nuxi prepare, nuxi dev, or nuxi build; otherwise, the TypeScript compiler throws errors showing that it cannot find the correct types.

[Middleware](#contents.xhtml_sc3_343a)

Nuxt supports two forms of middleware: client-side middleware influences the UI routing, and server-side middleware applies to the Nitro server.

[Router middleware](#contents.xhtml_sc3_344a)

Router middleware is usually used to make inquiries against request headers or parameters to determine which endpoint handler or page would be most suitable to respond. In general, router middleware handles things like authentication, role management or authorization, CORS, and XSS attacks, but they can be used to redirect to special product pages, offers, or specific user-based marketing or functionality.

When working on Vue.js code, you can influence how the application applies routing in three ways:

*   Inline or anonymous, defined directly on the page
*   Named middleware placed in the middleware/ directory, which gets auto-imported, and the naming is usually based on the given filename
*   Globally available, like named middleware, but with a global file extension suffix

The first two types can be applied at a page level using the definePageMeta() function, passing in the middleware key and a list of applicable middleware:

1.  <script setup>
2.  definePageMeta({
3.  middleware: ["my-auth-handler", "my-middleware"]
4.  })
5.  </script>

The format of a route middleware function is a navigation guard that accepts two arguments, to (where the navigation is headed) and from (where the navigation came), and Nuxt exposes the navigateTo() and abortNavigation() helpers. If neither of these return (refer to the following example), control of the navigation passes along to the next defined middleware function or route navigation is completed:

1.  export default defineNuxtRouteMiddleware((to, from) => {
2.  if (/* error condition */) {
3.  return abortNavigation()
4.  }
5.  if (/* redirect condition */) {
6.  return navigateTo('/')
7.  }
8.  // No return - next middleware
9.  })

[Server middleware](#contents.xhtml_sc3_345a)

Server middleware is contained in the server/middleware/ directory and will be automatically imported by Nuxt. Middleware handlers defined in this folder will be applied to each request before being routed to a component by the server router. Server middleware handlers can be used to investigate headers, log requests, extend the request object, or throw an error. They are not to be used to return a response. Refer to the following code:

1.  // server/middleware/auth.ts
2.  export default defineEventHandler((event) => {
3.  ...
4.  event.context.auth = < auth context >
5.  })

[Plugins](#contents.xhtml_sc3_346a)

Nuxt plugins are used to provide wrappers for Vue libraries and other external modules. Plugin files can be suffixed with either .client or .server if they are required only for the client or the server, respectively.

Files contained within the root of the plugins/ directory are auto-imported, as are any  index.(js|ts) files that are present in a subdirectory.

Note: Plugins are imported in alpha-numerical order. If a particular plugin is dependent on another plugin, then you need to ensure that the dependency is loaded first. This can be achieved by prefixing a number like 1 and so on.

A plugin file exports the result of the defineNuxtPlugin() function that accepts the nuxtApp as an argument:

1.  import ... from VueLibrary

3.  export default defineNuxtPlugin((nuxtApp) => {
4.  nuxtApp.vueApp.use(..., {})
5.  })

[Other folders](#contents.xhtml_sc3_347a)

There are many other folders that are part of a Nuxt application, but they are not generally used to handle or manage state. Feel free to explore the documentation at [https://nuxt.com/docs/guide/concepts/auto-imports](https://nuxt.com/docs/guide/concepts/auto-imports).

[Building the server-side of a Nuxt application](#contents.xhtml_sc2_348a)

The server part of a Nuxt application is generally used to create API endpoints to be used in conjunction with the Vue front end, using the exposed useFetch() composable.

The main application directory structure defines a server/ directory, which can hold any number of subdirectories, but the ones that are expected include api/, routes/, and middleware/. These three are automatically scanned to register the contained API and server handlers.

Nuxt expects files contained in these directories to export a default function that uses the defineEventHandler() function. The handler receives an event object and should return JSON data, a Promise<T>, or event.node.res.end().

The documentation supplied by the Nitro server can be found at [https://nitro.unjs.io/guide/](https://nitro.unjs.io/guide/).

[Event handler basics](#contents.xhtml_sc3_349a)

All event handlers that are created for a Nuxt application have the same signature:

1.  // Type signature
2.  declare function defineEventHandler<T = any>(handler: EventHandler<T>): EventHandler<T>;

4.  export default defineEventHandler(
5.  (event: H3Event): EventHander<T> => {
6.  return < JSON | Ref<T> | Promise<T> >
7.  })

The handler gets automatically mapped to a URI at build time; the following sections describe how one might define various types of a handler to access different parts of a request.

[Handling body requests](#contents.xhtml_sc3_350a)

Requests that have body content need to have the content extracted from the passed in event. This is asynchronous:

1.  // server/api/my-handler.post.ts
2.  export default defineEventHandler(async (event) => {
3.  const body = await readBody(event)
4.  return { body }
5.  })

[Query parameters](#contents.xhtml_sc3_351a)

Handling query parameters is similar to handling body content:

1.  // server/api/my-handler.get.ts
2.  export default defineEventHandler((event) => {
3.  const query = getQuery(event)
4.  return { ... }
5.  })

[Headers](#contents.xhtml_sc3_352a)

Accessing request headers follows a similar pattern:

1.  // server/api/my-handler.ts
2.  export default defineEventHandler((event) => {
3.  const headers = getRequestHeaders(event)
4.  return { ... }
5.  })

There are several other functions that can be used to handle request and response bodies that can be found at [https://www.jsdocs.io/package/h3](https://www.jsdocs.io/package/h3).

[Accessing the API](#contents.xhtml_sc3_353a)

Server API endpoints are accessed using the $fetch API that Nuxt exposes.

Within a component that requires data from the API, you can issue a request as shown in the following example:

1.  // GET request – maps to server/api/endpoint.get.ts
2.  $fetch('/api/endpoint')

4.  // POST request – maps to server/api/endpoint.post.ts
5.  $fetch('/api/endpoint', { method: 'post', 
      body: { test: 'abc' } })

7.  // DELETE request – maps to server/api/endpoint.delete.ts
8.  $fetch('/api/endpoint', { method: 'delete', 
       body: { id: 1 } })

Documentation on $fetch (ofetch) can be found at [https://github.com/unjs/ofetch](https://github.com/unjs/ofetch), which details more of the available API.

[Routes](#contents.xhtml_sc3_354a)

Routes are automatically built following the ones we already discussed. The following sections cover the various routing elements available at a server level.

[Route matching](#contents.xhtml_sc3_355a)

The server/(routes|api) directories build routes based on subdirectory structure and filenames where segments contained in [] are extracted into parameters that are exposed in the event.context.params object. The routes/ path gets removed from the URI. Refer to the following code:

1.  // file -> /server/routes/file.ts
2.  // URI -> /file
3.  export default defineEventHandler(..)

5.  // file -> /server/api/path/[file].ts
6.  // URI -> /api/path/my-name
7.  // event.context.params.file becomes 'my-name'
8.  export default defineEventHandler(
9.  (event) => `Showing, ${event.context.params.file}`
10.  )

[Catch-all routes](#contents.xhtml_sc3_356a)

Creating a router file using […] as the file name creates a catch-all route, which matches if there are no other matching routes. This is like catch-all routing client side.

[Status codes, redirects and cookies](#contents.xhtml_sc3_357a)

Nuxt supplies various functions that can be used to influence the response from an event handler. It also provides functions to parse cookies out of the request.

The following code show how you might apply the Nuxt supplied functions in practice:

1.  export default defineEventHandler((event) => {
2.  setResponseStatus(event, 202)
3.  })

5.  export default defineEventHandler((event) => {
6.  return sendRedirect(event, '/path/redirect/to', 302)
7.  })

9.  export default defineEventHandler((event) => {
10.  const cookies = parseCookies(event)
11.  return { cookies }
12.  })

[Server storage solutions](#contents.xhtml_sc3_358a)

The server layer of Nuxt comes with a simple storage solution for access to key-value stores like Redis. There is a simple example of how to integrate Redis in the documentation at [https://nuxt.com/docs/guide/directory-structure/server#server-storage](https://nuxt.com/docs/guide/directory-structure/server#server-storage).

However, you need a more comprehensive data storage solution like MongoDB; you need perform a third-party integration.

To make MongoDB work with Nuxt, you will need to define some runtime configuration, as follows:

1.  // in nuxt.config.ts
2.  import { defineNuxtConfig } from "nuxt";
3.  export default defineNuxtConfig({
4.  runtimeConfig: {
5.  mongoUrl: MONGO_URL,
6.  },
7.  });

Now, create a server plugin (refer to the next section). Once this is done, you can use a library like Mongoose to build the data models and perform the required queries.

[Plugins](#contents.xhtml_sc3_359a)

Plugins can be set up in two different ways. The first is to auto-import from the server/plugins directory. When working in this directory, you need to create your plugin using the defineNitroPlugin() function that takes the nitro app as an argument. When done this way, you can extend the runtime behavior and hook into the lifecycle events of Nitro (the web server). Refer to the following code:

1.  export default defineNitroPlugin((nitroApp) => {
2.  ...
3.  })

For other types of plugin, you will need to add these to your nuxt.config.ts file, under the nitro.plugins key:

1.  ...
2.  nitro: {
3.  plugins: ["~/server/path/to/plugin.ts"],
4.  },
5.  ...

With regard to the MongoDB set up, the best way to add this to your application is as follows:

1.  import mongoose from "mongoose";
2.  mongoose.set('strictQuery', true)
3.  export default defineNitroPlugin(async () => {
4.  try {
5.  await mongoose.connect(useRuntimeConfig().mongoUrl)
6.  ... rest of set up ...
7.  } catch (err) {
8.  ... handle err ..
9.  }
10.  })

With this in place, you can set up Mongoose models and queries as you would normally expect to.

[Errors](#contents.xhtml_sc3_360a)

Under normal circumstances, the Nitro server will return a 200 OK response, or if there are any uncaught errors, a 500 Internal Server Error. If you need to respond with a different error, then you need to throw using the createError() function, passing in the error details and required statusCode. This is different from the setResponseStatus() function mentioned earlier. Refer to the following code:

1.  export default defineEventHandler((event) => {
2.  if (false) {
3.  throw createError({
4.  statusCode: 400,
5.  statusMessage: 'This is a failure message',
6.  })
7.  }
8.  return 'Ok'
9.  })

[Other directories](#contents.xhtml_sc3_361a)

Nitro auto-imports from a selection of other directories that are not listed here. More details can be found at  [https://nuxt.com/docs/guide/directory-structure/server](https://nuxt.com/docs/guide/directory-structure/server).

[Conclusion](#contents.xhtml_sc2_362a)

Nuxt3 is a large framework, and this short chapter hardly did it justice. We have only really scrapped the surface here, but it should be enough to get started and give you enough pointers to find further information.

There is significant crossover with the patterns used between client and server, giving the developer a unified experience when working between both parts of the application. This lack of context or language switch means that Nuxt applications are quicker to build and easier to maintain.

[Points to remember](#contents.xhtml_sc2_363a)

*   Nuxt3 uses Vue3 as the view layer.
*   Nuxt3 has a built-in web server called Nitro.
*   Nuxt auto-imports from some standard directories.
*   Default UI rendering is called Universal Rendering.
*   UI rendered on the server (SSR) is hydrated in the client.
*   Middleware is used to influence server routing.

[Key terms](#contents.xhtml_sc2_364a)

*   Universal rendering
*   Server-Side Rendering (SSR)
*   Hydration
*   Build time
*   Runtime
*   Middleware
*   Router
*   Nitro
*   Error handling
*   Request
*   Response
*   Auto-import
*   Fetch API
*   Storage
*   Paths

Join our book’s Discord space

Join the book's Discord Workspace for Latest updates, Offers, Tech happenings around the world, New Release and Sessions with the Authors:

**[https://discord.bpbonline.com](https://discord.bpbonline.com)**

![](images/fm1.png)

# [CHAPTER 16Building Multi-tenanted Apps with Quasar](#contents.xhtml_ch16a)

[Introduction](#contents.xhtml_sc2_365a)

Building applications using Nuxt.js, as detailed in the previous chapter, has one small caveat, which can be an issue for some. As you saw in the previous chapter, you can quickly build web applications with Nuxt.js, but Nuxt can't help you if you need to build applications that target multiple platforms, especially if you're looking at native for mobile. For this, you need Quasar. Leveraging multiple build pipelines and compilers, Quasar applications can be built for almost any output device.

[Structure](#contents.xhtml_sc2_366a)

This chapter covers the following topics:

*   Quasar in context
*   Getting started
*   Multiple platforms
*   Building multi-tenanted apps
*   Building an application with Quasar
*   Getting your application into the world

[Objectives](#contents.xhtml_sc2_367a)

Quasar is a combined component library, framework, and layout engine that allows a user to build applications that can be compiled across several targets. This chapter covers some of the aspects of building an application using Quasar. Fundamentally, using it is the same as building any Vue.js application. The differences lie precisely in the CLI, the platform detection API, the component library, and application deployment.

[Quasar in context](#contents.xhtml_sc2_368a)

To set Quasar in context, we will need to define a few terms that might be unfamiliar to you. These are the output target; build context; component library; and boot file.

[Output Target](#contents.xhtml_sc3_369a)

The output target refers to what we are compiling the application to run on: a desktop/laptop browser, a mobile browser, a mobile-native application, and so on. The output target is a CLI option that describes which compiler to use. [Figure 16.1](#ch16.xhtml_fig16-1) depicts the output targets:

![](images/figure_16.1.png)

Figure 16.1: The output targets

The following table shows which compilers are available for each output target:

| Target | Compiler | Notes |
| --- | --- | --- |
| SPA | Default |  |
| SSR | ssr |  |
| PWA | pwa |  |
| Capacitor | capacitor | Android SDK and/or Xcode are required; targets either iOS or Android |
| Cordova | cordova | Android SDK and/or Xcode are required; Cordova needs to be installed; targets either iOS or Android |
| Desktop | electron |  |
| Browser extension | bex |  |

Table 16.1: Output targets

In [Table 16.1](#ch16.xhtml_tab16-1), you can see that Quasar requires non-default platforms to be specified. This ensures that the development install has only the compilers and setup required – you can add more platforms when the need arises. This flexibility allows projects to be bootstrapped quickly, allowing the scope to be widened later.

[Build context](#contents.xhtml_sc3_370a)

This means a few things: whether the application is SSR or browser rendered, and whether the application is being built for development, testing, or production. These contexts are controlled by the quasar.config.js file or by CLI options.

[Component library](#contents.xhtml_sc3_371a)

We have not discussed using a component library in detail yet, but we did cover it briefly in the last chapter with our discussion on Nuxt. A component library is a set of components that have been supplied, ready to use, a way of cutting the creation of a UI short by providing pre-built components that can be composed together. Supplied components can be low-level reusables like buttons and form controls or higher-levels reusables like page wrappers, menu bars, or interactive elements.

[Boot file](#contents.xhtml_sc3_372a)

A boot file is a file that wraps a service that is required to be loaded before the main Vue instance is available. There are several good reasons to use boot files found at [https://quasar.dev/quasar-cli-vite/boot-files#examples-of-appropriate-usage-of-boot-files](https://quasar.dev/quasar-cli-vite/boot-files#examples-of-appropriate-usage-of-boot-files).

[Getting started](#contents.xhtml_sc2_373a)

The easiest way to get started is by globally installing the Quasar CLI:

1.  $ npm i -g @quasar/cli

Once the CLI is installed, creating a new project is achieved with the init script, which will ask a series of questions, as detailed in the following listing:

1.  $ npm init quasar

3.  Need to install the following packages:
4.  create-quasar@1.1.1
5.  Ok to proceed? (y) y

7.  ✔ What would you like to build? ' App with Quasar CLI, let's go!
8.  ✔ Project folder: … quasar-project
9.  ✔ Pick Quasar version: ' Quasar v2 (Vue 3 | latest and greatest)
10.  ✔ Pick script type: ' Typescript
11.  ✔ Pick Quasar App CLI variant: ' Quasar App CLI with Vite
12.  ✔ Package name: … quasar-project
13.  ✔ Project product name: (must start with letter if building mobile apps) … Quasar App
14.  ✔ Project description: … A Quasar Project
15.  ✔ Author: … 
16.  ✔ Pick a Vue component style: ' Composition API
17.  ✔ Pick your CSS preprocessor: ' Sass with SCSS syntax
18.  ✔ Check the features needed for your project: ' ESLint, State Management (Pinia), Axios
19.  ✔ Pick an ESLint preset: ' Prettier

Then, you can add the desired target platforms:

1.  $ cd <project folder>
2.  $ quasar add [ssr | pwa | capacitor | cordova | electron | bex]

If you are building an application that targets a mobile platform, that is, Android or iOS, you will also need the Android SDK (or Android Studio) or XCode, respectively. Installation and setup instructions can be found at [https://quasar.dev/quasar-cli-vite](https://quasar.dev/quasar-cli-vite).

Creating a build once the project dependencies are in place is achieved with the Quasar build script:

1.  // Development builds
2.  $ quasar dev
3.  $ quasar dev -m [ ssr | pwa | electron | hex ]  <options>
4.  $ quasar dev -m [ capacitor | cordova ] -T [ ios | android ] <options>

6.  // Production builds
7.  $ quasar build
8.  $ quasar build -m [ ssr | pwa | electron | hex ]  <options>
9.  $ quasar build -m [ capacitor | cordova ] -T [ ios | android ] <options>

Now that we know how to install the framework, and create and build a project, we can look at how creating applications with Quasar can be different from building a website with any other component library.

[Multiple platforms](#contents.xhtml_sc2_374a)

As already covered, in many ways, using Quasar is very similar to using any other component library you might come across.

Quasar supplies its own component library, CSS framework, and a handful of platform helpers. These helpers are specifically built to aid you with building different types of application or rather, to be able to use the same codebase across different build outputs.

We will cover the helpers in more detail in the next section.

Unlike Nuxt, Quasar does not support auto-importing of JS/TS modules, as it has a different tree-shaking mechanism and differing requirements around package size and execution efficiency largely dependent on the output target.

Even though building different types of web application with Quasar will be familiar for many web developers, for those who have come across mobile native or desktop applications before, these areas can be quite daunting to begin with. Using Quasar means you do not need to learn new programming languages: you can firmly stay in JS/TS-land to build for these other platforms. Accessing hardware services outside of the browser sandbox opens many new avenues and paradigms to explore.

Particularly when building for native mobile, you might need to move beyond the code editor (most likely VS Code) you're used to. When building for iOS, you will need XCode on an Apple computer due to platform constraints, and for Android, you will need access to the Android SDK (and Android Studio).

Instead of a web browser, these platforms have various tools that you need to visualise and access your application. In the early stages of the development of your application, this will mean accessing a device simulator provided by these environments. For later stages of development and before deployment, you will need access to at least one hardware device of your target platform. If you're building for both iOS and Android, you will need access to an Android device (such as a Google Pixel or Samsung device) and an Apple iPhone for iOS.

These devices do not need to be top-of-the-range or brand new, just something that mirror a typical user in your expected user base. If you or your organization can afford it, a spread of device screen sizes and a few examples of differing OS versions to test against will give you the best chance of meeting the needs of your audience.

[Building multi-tenanted apps](#contents.xhtml_sc2_375a)

When building applications that need to be used across different platforms or even using the JS basis of the framework to build a mobile or desktop application, you need to understand some of the elements available when using Quasar.

[The Quasar Instance - $q](#contents.xhtml_sc3_376a)

The first thing we need to cover is the Quasar instance, referred to as $q by convention:

1.  // Composition API
2.  <script setup lang="ts">
3.  import { useQuasar } from 'quasar'
4.  const $q = useQuasar()
5.  ...
6.  </script>

8.  // OR

10.  <script>
11.  import { useQuasar } from 'quasar'
12.  export default {
13.  setup () {
14.  const $q = useQuasar()
15.  ...
16.  }
17.  }
18.  </script>

20.  // Options API

22.  <script>
23.  export default {
24.  methods: {
25.  func () {
26.  this.$q.platform...
27.  }
28.  }
29.  }
30.  </script>

The $q object/instance is somewhat analogous to the vue instance, where it is a globally available object that provides behaviors necessary to build your application. This helper gives information about the build environment, any internationalization data, and access to any Quasar-level plugins you might have configured.

The most important types of information that you can get from $q are as follows:

*   $q.platform to interrogate for platform details
*   $q.screen to get screen sizes and breakpoints
*   $q.lang for access to i18n language packs

For mobile native, you also have access to $q.cordova or $q.capacitor so that you can access any functionality defined there, depending on which of these you are using.

[Platform detection](#contents.xhtml_sc3_377a)

When working across different platforms, especially on mobile native, you need to easily determine which platform you are on in case you need to provide differing or alternate behaviors between them. The platform detection helpers are designed for this purpose. The API gives you access to the is, has, and within interrogators to manage runtime output.

The following table provides a brief, non-exhaustive list of the properties available to each of the interrogators, with more details to be found at [https://quasar.dev/options/platform-detection](https://quasar.dev/options/platform-detection).

| $q.platform.is.[F] |
| mobile | nativeMobile | desktop | ios |
| mac | win | electron | android |
| $q.platform.has.[F |
| touch | webStorage |
| $q.platform.within.[F] |
| iframe |

Table 16.2: Platform interrogation options

This helper can be used in both template and scripting contexts:

1.  // HTML

3.  <div v-if="$q.platform.is.mac">
4.  I'm only rendered on mac!
5.  </div>

7.  <div v-if="$q.platform.is.mobile">
8.  I'm only rendered on mobile!
9.  </div>

11.  <div v-if="$q.platform.is.desktop">
12.  I'm only rendered on desktop!
13.  </div>

15.  // Components

17.  <script setup lang="ts">
18.  import { useQuasar } from 'quasar'
19.  const $q = useQuasar()

21.  const func = () => {
22.  if ($q.platform.is.electron) { ... electron only ...}
23.  else if ($q.platform.is.nativeMobile) { ... mobile only ... }

25.  if ($q.platform.has.touch) { 
    ... touch screen functionality ... 
26.  }
27.  if ($q.platform.is.chrome && $q.platform.is.version < 70) {
28.  ... e.g. provide polyfill for chrome versions < 70 ...
29.  } 
30.  ...
31.  </script>

One thing to bear in mind when using this helper is while working across the template, you might be able to achieve the same visual outputs using the CSS framework. The disadvantage of using the CSS approach is that even though the elements are not visible, they are rendered, regardless of the platform. Sometimes this is desired behavior; you decide what works best for your application.

One thing to note is that $q.platform.is.mobile returns whether the application is running in a mobile browser, rather than as a native mobile application. To get details on mobile native, use platform.is.cordova or platform.is.capacitor.

[Screen detection](#contents.xhtml_sc3_378a)

Quasar supplies a screen plugin that can be used to manage dynamic and responsive UI at a code level. The recommendation is to use CSS. There are many response classes available for you to use at [https://quasar.dev/style/visibility#window-width-related](https://quasar.dev/style/visibility#window-width-related).

Even though this functionality is wrapped in a plugin, it is automatically available. This means $q.screen is already attached to the $q instance.

Using $q.screen in building a component is demonstrated in the following listing:

1.  <template>
2.  <q-list v-if="$q.screen.gt.md">
3.  <q-item>
4.  <q-item-section>List item content</q-item-section>
5.  </q-item>
6.  <q-item>
7.  <q-item-section>List item content</q-item-section>
8.  </q-item>
9.  </q-list>
10.  <q-button :class="buttonColor" />
11.  </template>

13.  <script ...>
14.  import { useQuasar } from 'quasar'
15.  import { computed } from 'vue'

17.  const $q = useQuasar()
18.  const buttonColor = computed(() => {
19.  return $q.screen.lt.md
20.  ? 'primary'
21.  : 'secondary'
22.  })
23.  }
24.  </script>

The Screen plugin can also be used to redefine the various breakpoints that a component responds to. It does not change the CSS breakpoints. However, to do this, you supply an object to the setSizes() function, which defines the changes you wish to make. The object will only accept a limited number of keys. The breakpoint identifiers that can be overridden are sm, md, lg, and xl.

Consider the following code:

1.  <script setup>
2.  import { Screen } from 'quasar'
3.  Screen.setSizes({ sm: 300, md: 500, xl: 2000 })
4.  </script>

Beyond this, the plugin can be used to add several additional responsive CSS classes to the build; this has a noted issue of adding significant weight to the deployable package, enough to increase the time to the first meaningful paint. Further details can be found in the documentation at [https://quasar.dev/options/screen-plugin](https://quasar.dev/options/screen-plugin).

[Internationalization (i18n)](#contents.xhtml_sc3_379a)

In Quasar, there are two elements that you need to consider when building with i18n in mind. Of these two, one applies only to Quasar component language packs, and one applies to your own components: using vue-i18n and @intlifty/vue-i18n-loader as the recommended way to support i18n.

Installation and set-up of these packages can become quite involved, so it is best to become familiar with the relevant sections in the documentation. You will become very familiar with the boot file setup in both cases.

For working with the Quasar components and language packs, the documentation is available at [https://quasar.dev/options/quasar-language-packs](https://quasar.dev/options/quasar-language-packs).

Documentation for adding i18n to your own components can be found at [https://quasar.dev/options/app-internationalization](https://quasar.dev/options/app-internationalization).

[Plugins, Extensions and Utilities](#contents.xhtml_sc2_380a)

Even though Quasar is a fully featured, batteries-included framework, it has several optional extras that can be used when required. These extras come in a few flavors depending on how the functionality is to be applied in your application.

[Plugins](#contents.xhtml_sc3_381a)

Plugins are used to augment the UI components available to you. These are usually added using the plugins property of the quasar.conf.js file. Here's a brief example:

1.  // quasar.config.js
2.  return {
3.  framework: {
4.  plugins: [ 'Notify', 'Meta', ...  ]

Plugins are then usually (unless otherwise stated in the documentation) available through the Quasar instance:

1.  <template>
2.  <q-btn @click="show" label="Show Notification" />
3.  </template>
4.  <script setup lang="ts">
5.  import { useQuasar } from 'quasar'

7.  const $q = useQuasar()

9.  function show() {
10.  $q.notify({ ... })
11.  }
12.  ...
13.  </script>

[App Extensions](#contents.xhtml_sc3_382a)

Extensions provide libraries of functionality that have additional dependencies, which might require boot files (additional configuration details), custom templates, and custom logic. They can be used to extend both the Quasar core and CLI.

Building your own extension can be complicated, but installing one from the App Extension library is simple and is done through the Quasar CLI. Consider the following code:

1.  $ quasar ext add <extension-name>

As each extension is custom, any imported extensions may require additional setup, as detailed in their documentation.

Extensions are available for several different purposes, like adding the following:

*   Pre-baked testing utilities
*   TypeScript to the project
*   Audio/video players
*   Calendars, timelines, and other complex UI

A list of official extensions can be found here:

[https://quasar.dev/app-extensions/discover](https://quasar.dev/app-extensions/discover)

This page also has links to the community-provided extensions.

[Utilities](#contents.xhtml_sc3_383a)

Utilities are libraries of useful functionality. They are importable directly from Quasar and are fully tree shakeable.

Quasar supplies several utilities to make standard tasks easier without installing third-party libraries. The following is a limited list of utilities available:

*   Date
*   Color
*   DOM
*   Formatter
*   Copy to Clipboard
*   Debounce and Throttle
*   Event handling

Using a utility is as simple as importing and then destructing (to aid treeshaking). See the following example code with the DOM utility:

1.  <script>
2.  import { dom } from 'quasar'

4.  // destructure dom to aid tree-shaking
5.  // i.e. just compile in the functionality needed
6.  const { offset, height, width } = dom

8.  // use these functions to get information on
9.  // DOM elements - DocNode is a visible HTML element
10.  console.log(offset(DocNode))
11.  console.log(width(DocNode))
12.  console.log(height(DocNode))
13.  </script>

Outside of the Quasar core, there is a lot of additional functionality that you can access to help build your application. Not only is there a great deal provided by the core development team but a healthy and vibrant community supplies resources for you to use.

[Building an application with Quasar](#contents.xhtml_sc2_384a)

To understand how this framework is used, we will build a small application from the ground up. This application will fetch weather data from a remote service provided by the US National Oceanic and Atmospheric Administration weather service. As space is somewhat limited, we will cover the highlights and leave it up to the reader to explore the attached code.

[Creating an application](#contents.xhtml_sc3_385a)

To start, we will use the CLI to generate a project as described earlier:

1.  $ npm init quasar

The provided project will then be built with the following selections:

1.  What would you like to build? ' App with Quasar CLI
2.  Project folder: noaa-weather-project
3.  Pick Quasar version: ' < recommended option >
4.  Pick script type: ' Typescript
5.  Pick Quasar App CLI variant: ' < recommended option >
6.  Package name: quasar-test-project
7.  Project product name: quasar-test-project
8.  Project description: < default option >
9.  Author: < default option >
10.  Pick a Vue component style: ' < default option >
11.  Pick your CSS preprocessor: ' < default option >
12.  Check the features needed for your project: ' ESLint, Axios
13.  Pick an ESLint preset: ' < default option >

15.  Install project dependencies? ' Yes, use npm

Running quasar dev in the project root will start the default development server and open your default browser to display the scaffolded base application. This is not quite what we are looking for, but it is a good test to see whether the base application has been installed correctly.

Now, you add the compilers you need to start with. In our case, we will set up a Capacitor app:

1.  $ quasar mode add capacitor

Using this mode requires extra dependencies, which the CLI will install for you. Once the platform has been added, you will notice a new src-<platform> directory. This directory holds all the platform-relevant plugins and utilities required to support capacitor. Much of the application configuration is managed by quasar.config.js, but platform-specific configuration is stored in the src-<platform> directory. Check the relevant documentation to determine what goes where.

To run the application in capacitor mode, you will need to stop the SPA development server and restart it using the following:

1.  $ quasar dev -m capacitor -T ios

This example is being built on a Mac. If you do not have that available, change the -T ios to -T android. Also, for iOS production builds, you must add a development team reference under Signing & Capabilities, which means you will need to purchase a development license.

This command will rebuild the project in capacitor mode and open the relevant IDE. The initial build can take some time to complete. Once the IDE is open, Xcode in the case of ios or Android Studio for android runs the project by pressing the build button to open the local device simulator.

The default application will start up in the simulator.

Leaving these running, we can now turn our attention to the code sitting in the src/ directory like a default SPA application.

[Constructing the application](#contents.xhtml_sc3_386a)

The application running on the dev server is a hot build, and changes are reflected in the simulator as the source changes.

The design is simple. There are only two “pages”, some composables, and some configuration.

The first thing we will look at is adding the base URL to the service for Axios. For this, you need to update the api definition in the src/boot/axios.ts file to the following:

1.  const api = axios.create({ baseURL: 'http://w1.weather.gov/xml/current_obs/' });

You will also need to update /quasar.config.js, adding the axios file to the boot option (line 30):

1.  boot: ['axios'],

The next thing to look at is the router:

1.  children: [
2.  {
3.  path: '',
4.  component: () => import('pages/IndexPage.vue'),
5.  name: 'landing',
6.  }, {
7.  path: 'station/:id',
8.  component: defineAsyncComponent(() => import('pages/StationPage.vue')),
9.  props: true,
10.  name: 'station',

After this, there is a small adjustment to be made to layouts/MainLayout.vue:

1.  <q-toolbar>
2.  <q-btn flat dense icon="arrow_back_ios"
3.  @click="goBack"
4.  v-if="$q.platform.is.ios && !onIndex()" />
5.  <q-btn flat dense v-else icon=""></q-btn>
6.  <q-toolbar-title> Local Weather </q-toolbar-title>
7.  </q-toolbar>

Line 4 is important here. The platform and the current page path are checked to determine if it is appropriate to display the button.

The landing screen (pages/IndexPage.vue) displays a simple form that needs little coverage.

The Station page (pages/StationPage.vue) fetches the required data via the onMounted life cycle hook:

1.  onMounted(async () => {
2.  pageData.value = getObservationData(
3.  await api.get(`${props.id}.xml`, { responseType: 'text' })
4.  );
5.  });

The data comes from the NOAA API as an XML feed. The API call is wrapped in a composable that extracts the data and returns a JSON representation of the same data, like so:

1.  const parser = new XMLParser();

3.  export function useXmlExtract() {
4.  const getObservationData = (xml: { data: string | 
    Buffer }): ObservationData => {
5.  return parser.parse(xml.data).current_observation
6.  }
7.  return { getObservationData }
8.  }

The ObservationData data type is held in the components/model.ts file.

This is a basic application, so it shouldn't go any further than the simulator, but it can be built for a device using the build script:

1.  $ quasar build -m capacitor -T iOS

Full building instructions can be found at https://quasar.dev/quasar-cli-vite/developing-capacitor-apps/publishing-to-store.

[Getting your application into the world](#contents.xhtml_sc2_387a)

Once you have built and tested your application, the next step is to get it out into the wild, that is, in front of people.

If your application is a web-type application, SPA, PWA or SSR, then your options are the same as any other front-end only project. Since the back end of the application will be remote; a JSON or GraphQL API-based server application, it is possible to host the back end and database in one place., In many cases backend services are hosted on Amazon Web Services, Heroku, or some shared hosting platform. Hosting the front end can be somewhere else, for example, Netlify or Vercel.

A mobile native application has a more involved deployment process. Even though you can host your application packages yourself and provide installation instructions, you will get better mileage by submitting and having your application accepted and available through the mobile application stores. So, any combination of Google Play, Apple AppStore, and to a lesser extent, Microsoft Store, can be opted for, depending on your target audience.

Each store has a different set of requirements, deployment processes, and costs, so it pays to investigate these upfront. You also need to be aware that some store deployments require the app to be checked against quality and content standards, which might delay deployment dates. If you are building an app with a defined availability date, this will need to be considered.

[Conclusion](#contents.xhtml_sc2_388a)

Building applications using Quasar allows you to target multiple platforms with the same codebase. This means that time to market can be reduced, and the number of implementation languages and the learning curve is also minimized. Unless you need access to mobile device capabilities, you have all the knowledge that you will need. This is ideal for many business-related or social applications, especially if data is supplied by API.

When building for mobile native, you can access the device APIs via Cordova plugins, which opens a whole new set of exciting capabilities.

This chapter has only scraped the surface of what is available to you using Quasar, but hopefully you can see the framework's potential.

This is the last chapter of development content. The next chapter covers questions that might be asked in an interview scenario.

[Points to remember](#contents.xhtml_sc2_389a)

*   The framework allows you to add and remove several target platforms from web to mobile.
*   Quasar has several utilities that make working with different platforms easier.
*   Cordova plugins abstract you away from lower-level details of mobile device capabilities.
*   The framework is easily extensible because of the plugin nature of its foundations.
*   You have a single codebase that you can cross-compile to several different output targets; and using built-in platform detection, you can provide platform-specific capabilities without having to step outside the framework.
*   Deploying to an app store can be complicated, time-consuming, and sometimes has an associated cost.

[Key terms](#contents.xhtml_sc2_390a)

*   Multi-tenancy
*   Single codebase
*   Cordova
*   Capacitor
*   PWA
*   SSR
*   SPA
*   Mobile native
*   Extensions
*   Plugins
*   Utilities
*   Components
*   Screen detection
*   Platform detection
*   Output target
*   Build context
*   Component library
*   Boot file
*   Quasar instance
*   Device simulator
*   iOS
*   Android
*   App store
*   Google Play Store

Join our book’s Discord space

Join the book's Discord Workspace for Latest updates, Offers, Tech happenings around the world, New Release and Sessions with the Authors:

**[https://discord.bpbonline.com](https://discord.bpbonline.com)**

![](images/fm1.png)

# [CHAPTER 17Interview Questions](#contents.xhtml_ch17a)

[Introduction](#contents.xhtml_sc2_391a)

In this last chapter, we will delve into some types of questions you might be asked during an interview. Remember that ideal answers to interview questions sometimes fall foul of opinion, so ensure due diligence and preparation before any interview.

[Structure](#contents.xhtml_sc2_392a)

This chapter covers a small number of possible questions that you might be asked in an interview situation.

[Objectives](#contents.xhtml_sc2_393a)

While there are several books in the market around algorithmic interview questions, there are limited resources on front-end interviews. This chapter aims to help prepare you for interview questions for front-end engineers.

[Questions and answers](#contents.xhtml_sc2_394a)

Question: What are the benefits of using TypeScript over JavaScript? Can you mention some associated advantages or disadvantages?

Answer: TypeScript is identical to JS in many ways; in fact, it is JS, as explained in [Chapter 3](#ch03.xhtml), HTML, CSS, and JS/TS for Extra Credit. The main difference is the ability to explicitly define which type a particular variable or data structure should have. This additional information is only used by the TS type-checker and compiler to ensure that the correct data is available. At runtime, these type notations do not exist, which can cause inexperienced developers some frustration. The strictness used by the type-checker can be altered, but the best practice is to use strict mode. Many IDEs can provide significant support.

This way, a whole class of bugs that exist in JS (incorrect or unavailable data) can be removed from the equation. This improves the developer experience and somewhat reduces your application's maintenance cost. You do need to factor in a slight increase in the initial development cost, but this cost can be minimized with reasonable choices of types upfront.

Through the compiler, TS can also target different JS versions or platforms by compiling out version incompatible syntax and allowing for poly-fills where necessary.

While TS has taken huge strides in updating and improving the language over raw JS, it still has many of the root issues that JS developers experience. It is, by no means, perfect.

When coming from the JS world, where data held in variables is dynamic and is not explicitly stated, the strictness of TS can cause a learning curve. This can bring some additional frustrations when time is spent “pleasing the compiler”, but the reward usually outweighs the overall cost. This, combined with the additional factor of type definitions being placed among code tokens, increases line noise and, depending on the type naming convention, increases line length.

One small caveat to bear in mind is that the type-inference engine used by TS is still quite immature compared to other inference engines, such as those used by Haskell, Idris, OCaML, or even Scala. It will sometimes stumble when working against highly abstract functional code designed to work across many different data types. This makes some functionality available in languages like Haskell impossible to replicate in TS.

Question: How is building UI with components different from traditional Web UI methods?

Answer: When building a website in the traditional sense, it is usual to separate markup (HTML) from styling (CSS) and event handling or dynamic elements (JS). Even though a site might still be made up of many hundreds of files, the content of each is, by and large, dedicated to one of the previously mentioned aspects. There might also be further boundaries (or lack thereof) when you consider server-side coding that might also be interwoven throughout the codebase, especially when dealing with template engines and, hopefully, to a lesser extent, database, or business logic.

Even when dealing with a simple client-server model-based application, making relatively simple or innocuous changes might impact many elements: templates or code files, CSS rules, JS behaviors, all of which need to be tested. In this instance, testing cannot just target the area of the change but will require a wider, usually manual, regression test over “unrelated” parts of the site: there might be unintended leakage from the change. Even though this is probably “worst case”, much of the web is built this way.

When working with component-based frameworks, front-end and back-end code is strictly separated. In general, these frameworks espouse that data is accessed via a remote API, making the server side independent from the rendered front end.

In most component-based frameworks, the code describing a component is usually held together in the same code file, with a compiler managing all the different parts for you. A component's file holds the relevant template, CSS, and JS/TS code together. A major consequence is that when maintenance of a component is necessary, the effect of that change is minimized; it becomes unit testable as an isolated instance. Regression testing can also be mostly automated, taking human factors and variability out of the equation.

The slight downside is that some business logic ideas, paradigms, or code may be duplicated between server and client, which has a maintenance cost; unfortunately, nothing comes for free.

Question: What is SOLID, and how does it apply to JS/TS? Does it even apply?

Answer: SOLID is one of those acronyms that get thrown about, which you might be sticking to without knowing or understanding in detail. The mnemonic describes the ideas that should be utilized in well-designed object-orientated code.

Breaking it down into its individual elements, we get the following:

*   Single Responsibility (S): An object should be responsible for only one thing. An object should send a message (usually by method call) to other objects if a change in the receiver is required or to receive something from outside of its (caller's) responsibility. Well-designed OOP code should be a mesh of objects all working together.
*   Open-closed principle (O): Objects should open for extension, while being closed for modification. This means, in practice, that objects should already be fully tested, so changing them tends to introduce bugs. By only extending and using polymorphic substitutions (inheritance hierarchies or interfaces), it is possible to write maintainable code.
*   Liskov Substitution (L): Simply put, this principle means that any child derived from a parent should be able to be used in place of the parent – a (derived) child class does not change established behaviors.
*   Interfaces (I): Code should be constructed against a particular contract: the interface. Interfaces should be small, and classes that use them should implement many interfaces rather than have a single “god-like” interface. Code objects built this way become interchangeable, and elements can be more specialized. This allows for composition patterns over inheritance patterns and favors decoupling. Many software patterns are based on the interchangeability of interfaces.
*   Dependency inversion (D): This principle covers the decoupling of classes through abstraction. Immature OOP code uses concrete class instantiation – use causes coupling between classes. With DI, required objects are supplied, in many cases, through a dependency inversion (or injection) container. This way, the relevance of concrete classes is reduced significantly.

Do these concepts apply to a language like JS? The answer is, it depends. If the house style is primarily OOP, this is a definite YES. It does apply. It is current best practice when working with OOP languages, and it is one of the most asked questions at interviews, especially in enterprise situations where Java, C#, Ruby, Python, and/or PHP are likely to be used. If you work for a software house that utilizes FP, this is less likely to apply, but you should be aware of it anyway.

More details on this can be found in the original work by Robert Martin at [https://web.archive.org/web/20150906155800/http:/www.objectmentor.com/resources/articles/Principles_and_Patterns.pdf](https://web.archive.org/web/20150906155800/http:/www.objectmentor.com/resources/articles/Principles_and_Patterns.pdf).

Question: What is OOP? What is FP? Which type is better?

Answer: These are different paradigms that describe different aspects of software engineering. These are typically the main two paradigms used in the industry, but there are others as well. The most likely paradigm that you will use is Object-Orientated Programming, followed by Functional Programming. They are fundamentally different paradigms.

OOP: Object-oriented programming is a programming paradigm based on the concept of “objects”, which can contain data and code. The data is in the form of properties, and the code is in the form of methods (paraphrased from [https://en.wikipedia.org/wiki/Object-oriented_programming](https://en.wikipedia.org/wiki/Object-oriented_programming)).

FP: Functional programming is a programming paradigm where programs are constructed by applying and composing functions. It is a declarative programming paradigm in which functions are trees of expressions that map values to other values rather than a sequence of imperative statements that update the program's running state (taken from [https://en.wikipedia.org/wiki/Functional_programming](https://en.wikipedia.org/wiki/Functional_programming)).

Many languages that have traditionally been steadfastly OOP are starting to introduce FP ideas and processes to appeal to as wide an audience as possible and provide best-of-breed tools for the modern age. There is a growing understanding that one size does not fit all and that the engineers' needs are paramount, not the philosophy of the language designers.

As to which paradigm is better, that is best left as a matter of personal or professional choice. The author prefers FP when possible but understands that sometimes the best tool for a particular circumstance is to describe the problem domain as a set of objects that work together. Being pragmatic rather than dogmatic allows better software and working practices to flourish.

Question: What is MVC? Is MVC applicable in a component-based application structure?

Answer: MVC is a standard design pattern that stands for Model-View-Controller. These elements work together, as shown in [Figure 17.1](#ch17.xhtml_fig17-1):

![](images/figure_17.1.png)

Figure 17.1: Model, View Controller Design Pattern

Model: The model describes and manages data and access to the data store.

View: The view is the description of the user interface; it contains the HTML elements and UI event handlers. The view is essentially dumb.

Controller: The controller orchestrates these two other elements to work together.

While MVC is a great pattern for many things and has been fundamental in the Web 2.0 revolution, it does not work for front-end frameworks. Some better patterns like Model, View, View Model (MVVM) or Model, View, Presenter (MVP) allow for smarter view logic than traditional MVC uses.

![Diagram Description automatically generated](images/figure_17.2.png)

Figure 17.2: MVVM Design Pattern

Question: Which is better: Composition API or Options API? Why?

Answer: The answer to a question like this is highly subjective. A response that matches the interviewer's bias will likely get you points regardless of what you think. If you find that your views match the interviewers, then all good.

Suppose you need to hedge your bets on this. It is best to state that each approach has its own merits. The Options API is a well-established API that's well documented. It is the way that components were built in Vue2, so there might be a huge amount of migrated code. With code like this, it is easy to build hierarchies of related components, but it is not so easy to isolate cross-component functionality. Composition is the more modern way of building applications with Vue3\. The idea fixes the issue above, which allows for slimmer components and cross-functional, reusable code.

Question: How do you handle events that need to pass information from a child component back into its parent?

Answer: The general way that Vue.js handles data is that the parent supplies data to the child via the props mechanism; this is a one-way data flow. There are some alternatives to this:

*   The provides/injects mechanism that works best for deep hierarchies
*   Composable services
*   State management tools like Pinia

To pass data back to the parent, you need to use a custom event. The parent is required to set up a custom event handler that the child needs to be able to accept via a prop. The child then calls the prop function, passing back data, which is then handed to the parent. As this is running counter to the way that data is set up to flow in the component hierarchy, it requires a lot more work and is a little brittle.

![Diagram Description automatically generated](images/figure_17.3.png)

Figure 17.3: One way dataflow

Again, alternatives here are state management like Pinia or composable services. The Reactivity API can be used to manage the data flow, but this is less explicit and circumvents the one-way data flow by the back door.

Question: Explain testing.

Answer: We covered testing in detail in [Chapter 14](#ch14.xhtml), Testing Vue.js Applications, but as a recap, the main parts of a testing strategy consist of the following parts:

*   Unit tests: These are simple tests that simulate inputs and verify outputs to ensure that the code behaves as expected.
*   Integration tests: These are tests that measure across several code units working together. This is to ensure that the units behave as expected within the boundaries of the implementation. This type of tests might also handle data persistence or API calls.
*   End-to-end tests: The use of these simulates entire user journeys through parts of the application.

Other types of tests include load testing, regression testing, black box testing, smoke testing, and stress testing.

Having a decent testing regime ensures that the code being shipped is more likely to be reliable and achieve the purposes for which it has been created. This increased certainty also aids maintenance tasks.

Things that need to be factored in when building tested and testable code are the initial outlay in terms of additional development time to create the unit tests.

There are several things to watch out for when building tests:

*   Ensure that the tests are not tied to a particular implementation. They should not be written to concern themselves with what happens between the input and output boundaries; rather, they need to measure that the outputs are correct, given certain inputs.
*   It is more important to ensure that a sensible number of edge cases are checked for properly than to achieve 100% code coverage.
*   If used incorrectly, testing can be a bit of a blunt instrument. Thought needs to go into the test to ensure that it is meaningful. Any code that is untestable should be refactored to ensure that it is correct.

Question: What are the differences between a component-based CSS framework, like Twitter Bootstrap, and a utility-first framework, like TailwindCSS? When is it appropriate to use either?

Answer: CSS frameworks, like Twitter Bootstrap or Zurb Foundation, which are primarily component-based, have firm opinions on how the underlying HTML should be structured. This can reduce HTML to a set of copy-paste operations from the framework documentation to ensure that correct styling is achieved.

While building code this way makes elements consistent from site to site, when working with a front-end framework like Vue, this requirement for a particular HTML layout can become restrictive.

When using a Utility First framework (UFF) like TailwindCSS, style rules are based on the functionality of the rule rather than building an aspect of the UI. This means that there are many more rules available. They are easier to combine and compose to create the styling scheme required for the application. UFFs tend to be more theme-able and easier to configure than component-based ones.

Appropriateness depends on the situation and house style or preference. UFFs are more flexible but take longer to implement and often require compiler support, but they have smaller output sizes. On the other hand, component-based frameworks, while bulkier in output, provide you with a consistent way of construction that relies on limited setup.

Question: Explain how an HTML document is structured. Where is it best to provide styling information? What about user interaction or page behaviors?

Similar to: Explain the different types of elements that HTML provides.

Answer: An HTML document consists of a simple text file that contains tags denoted by < and >.

Within the base <html> tag, an HTML document contains two main parts: a <head> and a <body>.

The <head> section contains all the relevant page metadata and sets up requests for any external resources that fall under the categories of style sheets and scripts. It also holds information regarding SEO information, like the page title, keywords, Facebook and/or Twitter (or other socials) details, and page character set types, among others. These elements, except for the page title, are not visible to the visitor.

The <body> section contains the page content, the visual elements, and the interactivity you wish to present to the visitor or user. These visual tags can be further broken down into structural (block) tags and presentation (inline)tags.

Structural tags, like <main>, <section>, or <div>, denote page sections and can be used to create a page hierarchy. Structural tags can contain other structural tags as well as presentation tags.

Presentation tags, like <h1>, <b>, <span>, are used to provide basic styling information, which can be augmented or superseded by style sheets. Presentation tags can only contain other presentation tags and not structural tags.

Question: What do you understand about accessibility? Why is it important? What does HTML provide that helps meet accessibility standards? Can you name relevant accessibility standards?

Answer: Instead of providing a standard type of answer for this question, we are providing some pointers because the answer to this question varies depending on where in the world you are.

You need to be clear about the rules around accessibility that govern the jurisdiction in which you are seeking employment. This is because even though there are WCAG guidelines, different parts of the world have different rules about accessibility, particularly the EU countries or the US. The point is that you need to be aware, especially if you are building a web application in one jurisdiction, say India, which will be used in another, say the European Union. The EU has specific and strict laws that govern accessibility, which you need to tailor your product to, or you will not be able to access that market.

Too many site builders think that adding accessibility to a web application is an afterthought or a nuisance, but this is not the case. Building an accessible web application should be a requirement from the initial design stages; these issues need to be assessed, considered, and implemented from the very start to ensure that the maximum number of people, regardless of ability, can access the product you are building.

At the very basic, you should be aware of the current WCAG 2.x standards, which can be found at [https://www.w3.org/WAI/standards-guidelines/wcag/](https://www.w3.org/WAI/standards-guidelines/wcag/). If you need an introduction to the topic, then you should go to https://www.w3.org/WAI/standards-guidelines/wcag/faq/#start.

Question: What is the difference between rest and spread operators?

Answer: Visually, the tokens used for the rest operator and spread operator are identical. They are, however, functionally different, and they are also placed in different code contexts.

*   The Rest Operator (…): This operator is used in function argument definitions and is used to collect passed-in function arguments into a list using the variable provided. This is a way of creating functions that take varying numbers of arguments but don't really care about the number or direct access.
*   The Spread Operator (…): This operator is the opposite of the rest operator. It accepts an iterable structure (array, string, objects) and expands it into individual elements. Places where this operator applies include the following:
    *   When constructing a new object that requires another object's ownProperties
    *   When needing to include one array in another
    *   When a function call requires an iterable to be applied to an argument list

Question: What is a destructuring assignment?

Answer: A destructuring assignment is where an iterable structure, such as an array or object, is unpacked into variables. This practice is relatively new but has a few facets that make transferring data with objects simpler.

When destructing an object or an array, there are two different patterns available: binding and assignment.

Binding patterns look like normal variable assignment, with a keyword: either const or let; and then a pattern that unwraps the required data.

Assignment patterns do not start with a declaration keyword, but the variables that are required for the unwrapping are already declared, either in the local scope or as an object property. This technique is used when objects need to be unwrapped into array properties where binding assignment is not valid syntax.

The destructing syntax can be used in any number of situations, like function parameters and parsing returned data, or binding against the rest operator.

Question: Explain the Vue.js life cycle and its importance.

Answer: The Vue.js life cycle and instance details are discussed in depth in [Chapter 4](#ch04.xhtml), Understanding the Vue.js instance.

Question: Where is it best to check for permission/authorization when accessing password protected areas. What is the best way to achieve this?

Answer: This is achieved primarily with the VueRouter and navigation guards. This is covered in detail in [Chapter 10](#ch10.xhtml), Routing Between Pages With VueRouter.

[Conclusion](#contents.xhtml_sc2_395a)

Questions asked in an interview can be varied and will most likely stretch your knowledge of any number of subjects. Different companies will perform technical and coding screenings at different levels. The reasons for this can vary from company to company but in general, it is for one of the following:

*   To try to catch you out
*   To see how you might perform under pressure
*   To see how you might work with the established team
*   To check whether you have esoteric knowledge of algorithms
*   You need to be prepared for everything.

Join our book’s Discord space

Join the book's Discord Workspace for Latest updates, Offers, Tech happenings around the world, New Release and Sessions with the Authors:

**[https://discord.bpbonline.com](https://discord.bpbonline.com)**

![](images/fm1.png)

# Index

Symbols

<a/> tags

changing, to router-link [240](#ch10.xhtml_page240)-[246](#ch10.xhtml_page246)

<router-link> component [237](#ch10.xhtml_page237)

A

Angular and Node (MEAN) [3](#ch01.xhtml_page3)

anonymous function [46](#ch03.xhtml_page46)

App.vue file

changes [224](#ch09.xhtml_page224), [225](#ch09.xhtml_page225)

arrow function [47](#ch03.xhtml_page47)

arrow function() life cycle hook [94](#ch04.xhtml_page94)

Asynchronous JavaScript and XML (AJAX) [64](#ch03.xhtml_page64)

Axios

integrating, into Vue application [330](#ch13.xhtml_page330)

B

back() function [249](#ch10.xhtml_page249)

basic prototype template

building [216](#ch09.xhtml_page216)

beforeCreate() life cycle hook [94](#ch04.xhtml_page94), [95](#ch04.xhtml_page95)

beforeEnter [235](#ch10.xhtml_page235)

beforeMount() life cycle hook [96](#ch04.xhtml_page96)

beforeUnmount() life cycle hook [98](#ch04.xhtml_page98)

C

Canvas API [73](#ch03.xhtml_page73), [74](#ch03.xhtml_page74)

checkout page, web application

design [135](#ch05.xhtml_page135)

proposed component [138](#ch05.xhtml_page138)

wireframe [136](#ch05.xhtml_page136), [137](#ch05.xhtml_page137)

client-side APIs

about [71](#ch03.xhtml_page71)

Canvas API [73](#ch03.xhtml_page73), [74](#ch03.xhtml_page74)

Drag and Drop API [74](#ch03.xhtml_page74)

fetch API [71](#ch03.xhtml_page71)-[73](#ch03.xhtml_page73)

History API [75](#ch03.xhtml_page75)

web sockets API [79](#ch03.xhtml_page79), [80](#ch03.xhtml_page80)

web storage API [76](#ch03.xhtml_page76), [77](#ch03.xhtml_page77)

web workers [77](#ch03.xhtml_page77)-[79](#ch03.xhtml_page79)

closure [47](#ch03.xhtml_page47)

component

designing [128](#ch05.xhtml_page128)

testing [342](#ch14.xhtml_page342)-[346](#ch14.xhtml_page346)

component tests [337](#ch14.xhtml_page337), [338](#ch14.xhtml_page338)

composables

testing [349](#ch14.xhtml_page349)-[353](#ch14.xhtml_page353)

composable utilities

creating [161](#ch06.xhtml_page161)-[163](#ch06.xhtml_page163)

Composition API

about [92](#ch04.xhtml_page92), [144](#ch06.xhtml_page144)

problem solving [144](#ch06.xhtml_page144), [145](#ch06.xhtml_page145)

Composition API life cycle

about [145](#ch06.xhtml_page145)-[148](#ch06.xhtml_page148)

reactive() function [149](#ch06.xhtml_page149), [150](#ch06.xhtml_page150)

ref() function [150](#ch06.xhtml_page150)-[152](#ch06.xhtml_page152)

Composition API life cycle hooks

about [152](#ch06.xhtml_page152), [153](#ch06.xhtml_page153)

computed properties [158](#ch06.xhtml_page158), [159](#ch06.xhtml_page159)

data [157](#ch06.xhtml_page157)

data flow between components [154](#ch06.xhtml_page154)

events [157](#ch06.xhtml_page157), [158](#ch06.xhtml_page158)

fall-through attributes [160](#ch06.xhtml_page160), [161](#ch06.xhtml_page161)

props, declaring [154](#ch06.xhtml_page154)-[156](#ch06.xhtml_page156)

template refs [160](#ch06.xhtml_page160)

watchers [159](#ch06.xhtml_page159)

Composition API reactive properties [145](#ch06.xhtml_page145)-[148](#ch06.xhtml_page148)

Composition API utilities library [164](#ch06.xhtml_page164)

created() life cycle hook [95](#ch04.xhtml_page95)

CSS frameworks

about [42](#ch03.xhtml_page42)

adding [210](#ch08.xhtml_page210)

CSS rule application [40](#ch03.xhtml_page40)-[42](#ch03.xhtml_page42)

custom directives [108](#ch04.xhtml_page108)

custom events

creating [260](#ch11.xhtml_page260)

parent and child component, communication between [260](#ch11.xhtml_page260), [261](#ch11.xhtml_page261)

custom validators

creating, in Vuelidate [282](#ch12.xhtml_page282)-[284](#ch12.xhtml_page284)

D

data event

emitting [263](#ch11.xhtml_page263)

passing [263](#ch11.xhtml_page263)

data flow [124](#ch05.xhtml_page124)-[127](#ch05.xhtml_page127)

data validation

async setup function [294](#ch12.xhtml_page294)

collections, validating [287](#ch12.xhtml_page287)

configuration options, specifying [280](#ch12.xhtml_page280), [281](#ch12.xhtml_page281)

custom validators, creating in Vuelidate [282](#ch12.xhtml_page282), [283](#ch12.xhtml_page283)

custom validators, in Vuelidate [284](#ch12.xhtml_page284)

errors, returning from API validation [292](#ch12.xhtml_page292)

errors, returning from server side validation [292](#ch12.xhtml_page292)

failure, checking [285](#ch12.xhtml_page285)-[287](#ch12.xhtml_page287)

failure, handling [285](#ch12.xhtml_page285)-[287](#ch12.xhtml_page287)

handling [276](#ch12.xhtml_page276)-[279](#ch12.xhtml_page279)

internationalisation (i18n) [293](#ch12.xhtml_page293)

returned object, changing [291](#ch12.xhtml_page291)

standard validators, in Vuelidate [279](#ch12.xhtml_page279), [280](#ch12.xhtml_page280)

data validation, advanced topics

about [287](#ch12.xhtml_page287)

collector component [288](#ch12.xhtml_page288)-[291](#ch12.xhtml_page291)

computed values and rules, using [287](#ch12.xhtml_page287)

nested validation [288](#ch12.xhtml_page288)-[291](#ch12.xhtml_page291)

reactive values and rules, using [287](#ch12.xhtml_page287)

ref's values and rules, using [287](#ch12.xhtml_page287)

validation scope [288](#ch12.xhtml_page288)-[291](#ch12.xhtml_page291)

Dependency Injection

handling [164](#ch06.xhtml_page164)-[166](#ch06.xhtml_page166)

Distributed Version Control Systems (DVCS) [174](#ch07.xhtml_page174)

document object model (DOM) [2](#ch01.xhtml_page2)

Drag and Drop API [74](#ch03.xhtml_page74)

E

end-to-end (E2E) testing

about [338](#ch14.xhtml_page338)

Nightwatch, using [358](#ch14.xhtml_page358), [359](#ch14.xhtml_page359)

event bus

communicating [264](#ch11.xhtml_page264)-[266](#ch11.xhtml_page266)

event handler basics

about [378](#ch15.xhtml_page378)

body request, handling [378](#ch15.xhtml_page378)

query parameter [378](#ch15.xhtml_page378)

request headers, accessing [379](#ch15.xhtml_page379)

events

defining [262](#ch11.xhtml_page262), [263](#ch11.xhtml_page263)

testing [347](#ch14.xhtml_page347)-[349](#ch14.xhtml_page349)

validating [262](#ch11.xhtml_page262), [263](#ch11.xhtml_page263)

Express [3](#ch01.xhtml_page3)

F

fetch API

about [71](#ch03.xhtml_page71)-[73](#ch03.xhtml_page73)

using [328](#ch13.xhtml_page328), [329](#ch13.xhtml_page329)

filters [107](#ch04.xhtml_page107)

FooterComponent [219](#ch09.xhtml_page219), [220](#ch09.xhtml_page220)

form component

using [272](#ch12.xhtml_page272), [273](#ch12.xhtml_page273)

form data

handling [276](#ch12.xhtml_page276)-[279](#ch12.xhtml_page279)

forms

creating [271](#ch12.xhtml_page271)

forward() function [249](#ch10.xhtml_page249)

front-end developer [29](#ch02.xhtml_page29)

front-end routing

best practices [228](#ch10.xhtml_page228)

full-stack developer [29](#ch02.xhtml_page29)

functional components (FCs) [128](#ch05.xhtml_page128)-[130](#ch05.xhtml_page130)

G

Git

reference link [175](#ch07.xhtml_page175)

Git primer [174](#ch07.xhtml_page174), [175](#ch07.xhtml_page175)

Git primer, basic terminology

about [175](#ch07.xhtml_page175)

branch [175](#ch07.xhtml_page175), [176](#ch07.xhtml_page176)

checkout/switch [179](#ch07.xhtml_page179)

cherry-pick [183](#ch07.xhtml_page183)

clone [178](#ch07.xhtml_page178)

commit [180](#ch07.xhtml_page180)

conflict [181](#ch07.xhtml_page181)

diff [182](#ch07.xhtml_page182)

fetch [179](#ch07.xhtml_page179)

local [178](#ch07.xhtml_page178)

merge [180](#ch07.xhtml_page180), [181](#ch07.xhtml_page181)

path [182](#ch07.xhtml_page182)

pull [180](#ch07.xhtml_page180)

push [181](#ch07.xhtml_page181)

rebase [183](#ch07.xhtml_page183)

remote [177](#ch07.xhtml_page177), [178](#ch07.xhtml_page178)

repository (repo) [176](#ch07.xhtml_page176)

SHA [175](#ch07.xhtml_page175)

stash [182](#ch07.xhtml_page182)

go() function [249](#ch10.xhtml_page249)

GraphQL-based API access [331](#ch13.xhtml_page331)-[334](#ch13.xhtml_page334)

H

HeroComponent [220](#ch09.xhtml_page220), [221](#ch09.xhtml_page221)

History API [75](#ch03.xhtml_page75)

I

integration tests [337](#ch14.xhtml_page337), [338](#ch14.xhtml_page338)

internationalization (i18n) [395](#ch16.xhtml_page395)

item display page, web application

design [134](#ch05.xhtml_page134)

proposed component [135](#ch05.xhtml_page135)

wireframe [134](#ch05.xhtml_page134), [135](#ch05.xhtml_page135)

J

JAMStack developer [30](#ch02.xhtml_page30)

JavaScript (JS)

async function [61](#ch03.xhtml_page61)

Asynchronous JavaScript and XML (AJAX) [64](#ch03.xhtml_page64)

await function [61](#ch03.xhtml_page61)

best practices [43](#ch03.xhtml_page43)

callback function [58](#ch03.xhtml_page58)-[60](#ch03.xhtml_page60)

classes [55](#ch03.xhtml_page55)-[58](#ch03.xhtml_page58)

client-side APIs [71](#ch03.xhtml_page71)

code declaration [68](#ch03.xhtml_page68)

const [54](#ch03.xhtml_page54), [55](#ch03.xhtml_page55)

functional programming (FP) concept [66](#ch03.xhtml_page66)

functions [46](#ch03.xhtml_page46)-[48](#ch03.xhtml_page48)

generator function [50](#ch03.xhtml_page50), [51](#ch03.xhtml_page51)

IIFEs [55](#ch03.xhtml_page55)-[58](#ch03.xhtml_page58)

immutable data [66](#ch03.xhtml_page66), [67](#ch03.xhtml_page67)

let keyword [54](#ch03.xhtml_page54)

modules [55](#ch03.xhtml_page55)-[58](#ch03.xhtml_page58)

objects and prototypes [43](#ch03.xhtml_page43)-[46](#ch03.xhtml_page46)

partial composability application [69](#ch03.xhtml_page69)-[71](#ch03.xhtml_page71)

partial function application [69](#ch03.xhtml_page69)-[71](#ch03.xhtml_page71)

promises [50](#ch03.xhtml_page50), [61](#ch03.xhtml_page61)-[64](#ch03.xhtml_page64)

purity concept [67](#ch03.xhtml_page67), [68](#ch03.xhtml_page68)

scope [51](#ch03.xhtml_page51)-[53](#ch03.xhtml_page53)

structures, building [64](#ch03.xhtml_page64)-[66](#ch03.xhtml_page66)

JavaScript Object Notation (JSON)

about [48](#ch03.xhtml_page48), [49](#ch03.xhtml_page49)

syntax [48](#ch03.xhtml_page48)

L

landing page, web application

design [130](#ch05.xhtml_page130)

proposed component [132](#ch05.xhtml_page132)

wireframe [131](#ch05.xhtml_page131)

lazy modifier [274](#ch12.xhtml_page274)-[276](#ch12.xhtml_page276)

listing/menu page, web application

design [132](#ch05.xhtml_page132)

proposed component [133](#ch05.xhtml_page133), [134](#ch05.xhtml_page134)

wireframe [132](#ch05.xhtml_page132)

login and registration page, web application

design [138](#ch05.xhtml_page138)

proposed component [140](#ch05.xhtml_page140)

wireframe [138](#ch05.xhtml_page138), [139](#ch05.xhtml_page139)

M

MenuBarComponent [218](#ch09.xhtml_page218), [219](#ch09.xhtml_page219)

menu page [132](#ch05.xhtml_page132)

middleware

router middleware [375](#ch15.xhtml_page375), [376](#ch15.xhtml_page376)

server middleware [376](#ch15.xhtml_page376)

mixins

about [61](#ch03.xhtml_page61), [104](#ch04.xhtml_page104)-[107](#ch04.xhtml_page107)

features [107](#ch04.xhtml_page107)

Model-View-Controller (MVC) pattern [2](#ch01.xhtml_page2)

MongoDB [3](#ch01.xhtml_page3)

mounted() life cycle hook [96](#ch04.xhtml_page96)

multi-tenanted apps

app extensions [396](#ch16.xhtml_page396), [397](#ch16.xhtml_page397)

building [390](#ch16.xhtml_page390)

extensions [395](#ch16.xhtml_page395)

internationalization (i18n) [395](#ch16.xhtml_page395)

platform detection [392](#ch16.xhtml_page392), [393](#ch16.xhtml_page393)

plugins [395](#ch16.xhtml_page395), [396](#ch16.xhtml_page396)

Quasar Instance ($q) [390](#ch16.xhtml_page390)-[392](#ch16.xhtml_page392)

screen detection [394](#ch16.xhtml_page394), [395](#ch16.xhtml_page395)

utilities [395](#ch16.xhtml_page395)-[398](#ch16.xhtml_page398)

N

named function [46](#ch03.xhtml_page46)

navigating by code

about [247](#ch10.xhtml_page247), [248](#ch10.xhtml_page248)

back() function [249](#ch10.xhtml_page249), [250](#ch10.xhtml_page250)

forward() function [249](#ch10.xhtml_page249), [250](#ch10.xhtml_page250)

go() function [249](#ch10.xhtml_page249), [250](#ch10.xhtml_page250)

push() function [248](#ch10.xhtml_page248)

replace() function [249](#ch10.xhtml_page249)

Nightwatch

using, for E2E testing [358](#ch14.xhtml_page358), [359](#ch14.xhtml_page359)

Node Package Manager [183](#ch07.xhtml_page183)

NPM primer

about [174](#ch07.xhtml_page174)

installed package, updating [185](#ch07.xhtml_page185)

package, installing [183](#ch07.xhtml_page183), [184](#ch07.xhtml_page184)

package.json file [186](#ch07.xhtml_page186)

package safety audit, performing [185](#ch07.xhtml_page185), [186](#ch07.xhtml_page186)

project, initialising [183](#ch07.xhtml_page183)

number modifier [273](#ch12.xhtml_page273)

Nuxt

about [362](#ch15.xhtml_page362)

state and cross-component functionality, managing [372](#ch15.xhtml_page372)

Nuxt application

API, accessing [379](#ch15.xhtml_page379)

client-side, building [366](#ch15.xhtml_page366)

directories [383](#ch15.xhtml_page383)

errors [382](#ch15.xhtml_page382)

event handler basics [378](#ch15.xhtml_page378)

plugins [381](#ch15.xhtml_page381), [382](#ch15.xhtml_page382)

Routes [380](#ch15.xhtml_page380)

server-side, building [377](#ch15.xhtml_page377)

server storage solution [381](#ch15.xhtml_page381)

Nuxt component [366](#ch15.xhtml_page366)-[369](#ch15.xhtml_page369)

Nuxt.js

about [362](#ch15.xhtml_page362)

dependencies, managing [364](#ch15.xhtml_page364)-[366](#ch15.xhtml_page366)

multiple rendering techniques [362](#ch15.xhtml_page362)-[364](#ch15.xhtml_page364)

project, creating [364](#ch15.xhtml_page364)-[366](#ch15.xhtml_page366)

Nuxt layouts [370](#ch15.xhtml_page370)-[372](#ch15.xhtml_page372)

Nuxt pages [369](#ch15.xhtml_page369), [370](#ch15.xhtml_page370)

Nuxt plugins [377](#ch15.xhtml_page377)

O

OfferComponent [223](#ch09.xhtml_page223), [224](#ch09.xhtml_page224)

OffersComponent [221](#ch09.xhtml_page221)-[223](#ch09.xhtml_page223)

Options API [92](#ch04.xhtml_page92)

order page, web application

design [140](#ch05.xhtml_page140)

proposed component [141](#ch05.xhtml_page141)

wireframe [140](#ch05.xhtml_page140)

P

page layout

about [217](#ch09.xhtml_page217), [218](#ch09.xhtml_page218)

FooterComponent [219](#ch09.xhtml_page219), [220](#ch09.xhtml_page220)

HeroComponent [220](#ch09.xhtml_page220), [221](#ch09.xhtml_page221)

MenuBarComponent [218](#ch09.xhtml_page218), [219](#ch09.xhtml_page219)

OfferComponent [223](#ch09.xhtml_page223), [224](#ch09.xhtml_page224)

OffersComponent [221](#ch09.xhtml_page221)-[223](#ch09.xhtml_page223)

page template

landing [216](#ch09.xhtml_page216)

parent and child component

communication between, with custom events [260](#ch11.xhtml_page260)-[262](#ch11.xhtml_page262)

Pinia

about [353](#ch14.xhtml_page353)-[356](#ch14.xhtml_page356)

testing [353](#ch14.xhtml_page353)

Pinia store

about [311](#ch13.xhtml_page311), [312](#ch13.xhtml_page312)

actions [320](#ch13.xhtml_page320)-[322](#ch13.xhtml_page322)

getters [317](#ch13.xhtml_page317)-[319](#ch13.xhtml_page319)

Option Store type, defining [312](#ch13.xhtml_page312)

Setup Store, defining [313](#ch13.xhtml_page313)

state [314](#ch13.xhtml_page314)-[316](#ch13.xhtml_page316)

working [322](#ch13.xhtml_page322), [324](#ch13.xhtml_page324)-[328](#ch13.xhtml_page328)

project folders and files

managing [214](#ch09.xhtml_page214)-[216](#ch09.xhtml_page216)

prototypal inheritance [44](#ch03.xhtml_page44)

push() function [248](#ch10.xhtml_page248)

push() method [248](#ch10.xhtml_page248)

Q

Quasar

multiple platforms [389](#ch16.xhtml_page389), [390](#ch16.xhtml_page390)

Quasar application

building [398](#ch16.xhtml_page398)

constructing [400](#ch16.xhtml_page400), [401](#ch16.xhtml_page401)

creating [398](#ch16.xhtml_page398), [399](#ch16.xhtml_page399)

overview [402](#ch16.xhtml_page402)

Quasar CLI

installing [388](#ch16.xhtml_page388), [389](#ch16.xhtml_page389)

Quasar in context

about [386](#ch16.xhtml_page386)

boot file [388](#ch16.xhtml_page388)

build context [387](#ch16.xhtml_page387)

component library [387](#ch16.xhtml_page387)

output target [386](#ch16.xhtml_page386), [387](#ch16.xhtml_page387)

Quasar Instance ($q) [390](#ch16.xhtml_page390)-[392](#ch16.xhtml_page392)

R

reactive [100](#ch04.xhtml_page100)

reactive() function [149](#ch06.xhtml_page149), [150](#ch06.xhtml_page150)

ref() function [150](#ch06.xhtml_page150)-[152](#ch06.xhtml_page152)

render function [115](#ch05.xhtml_page115)-[119](#ch05.xhtml_page119)

replace() function [249](#ch10.xhtml_page249)

Representational State Transfer (REST) [231](#ch10.xhtml_page231)

Route

about [380](#ch15.xhtml_page380)

catch-all routes [380](#ch15.xhtml_page380)

cookies [380](#ch15.xhtml_page380)

matching [380](#ch15.xhtml_page380)

redirects [380](#ch15.xhtml_page380)

status codes [380](#ch15.xhtml_page380)

route outlet [239](#ch10.xhtml_page239)

router middleware [375](#ch15.xhtml_page375), [376](#ch15.xhtml_page376)

RouterRecordRaw object

about [230](#ch10.xhtml_page230)

beforeEnter [235](#ch10.xhtml_page235), [236](#ch10.xhtml_page236)

children property [236](#ch10.xhtml_page236), [237](#ch10.xhtml_page237)

component [232](#ch10.xhtml_page232), [233](#ch10.xhtml_page233)

name property [232](#ch10.xhtml_page232)

path [230](#ch10.xhtml_page230), [231](#ch10.xhtml_page231)

props property [234](#ch10.xhtml_page234)

router-link component [237](#ch10.xhtml_page237)-[239](#ch10.xhtml_page239)

router-view [239](#ch10.xhtml_page239), [240](#ch10.xhtml_page240)

routing definition

building [229](#ch10.xhtml_page229), [230](#ch10.xhtml_page230)

S

script section [115](#ch05.xhtml_page115)

server middleware [376](#ch15.xhtml_page376)

server storage solution [381](#ch15.xhtml_page381)

small and medium enterprises (SME's) [27](#ch02.xhtml_page27)

standard DOM events

handling [254](#ch11.xhtml_page254)-[260](#ch11.xhtml_page260)

triggering [254](#ch11.xhtml_page254)-[260](#ch11.xhtml_page260)

standard validators

in Vuelidate [279](#ch12.xhtml_page279), [280](#ch12.xhtml_page280)

state and cross-component functionality

composables [375](#ch15.xhtml_page375)

error handling [374](#ch15.xhtml_page374), [375](#ch15.xhtml_page375)

folders [377](#ch15.xhtml_page377)

lifecycle hooks [373](#ch15.xhtml_page373)

managing, in Nuxt [372](#ch15.xhtml_page372)

middleware [375](#ch15.xhtml_page375)

Nuxt plugins [377](#ch15.xhtml_page377)

remote data [374](#ch15.xhtml_page374)

useState() [372](#ch15.xhtml_page372), [373](#ch15.xhtml_page373)

state management

in Vue 3 [310](#ch13.xhtml_page310)

style section [120](#ch05.xhtml_page120), [121](#ch05.xhtml_page121)

Suspense

using [167](#ch06.xhtml_page167)

Suspense component [169](#ch06.xhtml_page169)-[171](#ch06.xhtml_page171)

T

Tailwind

integrating, to Vue.js project [209](#ch08.xhtml_page209), [210](#ch08.xhtml_page210)

TailwindCSS

about [200](#ch08.xhtml_page200), [201](#ch08.xhtml_page201)

configuration options [202](#ch08.xhtml_page202)

configuring [201](#ch08.xhtml_page201)

using [208](#ch08.xhtml_page208)

TailwindCSS, configuration options

colors key [205](#ch08.xhtml_page205)

content section [204](#ch08.xhtml_page204)

default theme reference [204](#ch08.xhtml_page204)

key-value pair [202](#ch08.xhtml_page202)

list of options [202](#ch08.xhtml_page202)

options object [203](#ch08.xhtml_page203)

plugins [207](#ch08.xhtml_page207), [208](#ch08.xhtml_page208)

spacing section [206](#ch08.xhtml_page206), [207](#ch08.xhtml_page207)

theme reference closure [203](#ch08.xhtml_page203)

theme section [205](#ch08.xhtml_page205)

Teleport component

about [167](#ch06.xhtml_page167), [168](#ch06.xhtml_page168)

using [167](#ch06.xhtml_page167)

template section [114](#ch05.xhtml_page114)

testing

benefits [336](#ch14.xhtml_page336)

tests and tools types

about [337](#ch14.xhtml_page337)

component tests [337](#ch14.xhtml_page337), [338](#ch14.xhtml_page338)

end-to-end tests [338](#ch14.xhtml_page338)

integration tests [337](#ch14.xhtml_page337), [338](#ch14.xhtml_page338)

unit tests [337](#ch14.xhtml_page337)

trim modifier [274](#ch12.xhtml_page274)

Twitter Bootstrap [211](#ch08.xhtml_page211)

TypeScript option

in Vue.js application [108](#ch04.xhtml_page108)

TypeScript (TS)

about [81](#ch03.xhtml_page81)

using [81](#ch03.xhtml_page81)-[87](#ch03.xhtml_page87)

U

UI composition component [122](#ch05.xhtml_page122)-[124](#ch05.xhtml_page124)

unit tests [337](#ch14.xhtml_page337)

updated() life cycle hook [98](#ch04.xhtml_page98)

useState() [372](#ch15.xhtml_page372), [373](#ch15.xhtml_page373)

V

value binding [270](#ch12.xhtml_page270), [271](#ch12.xhtml_page271)

Virtual DOM

working with [38](#ch03.xhtml_page38)-[40](#ch03.xhtml_page40)

Visual Studio Code (VS Code) [43](#ch03.xhtml_page43)

Vite

using, to create project [195](#ch07.xhtml_page195), [196](#ch07.xhtml_page196)

v-model

about [270](#ch12.xhtml_page270), [271](#ch12.xhtml_page271)

AddToCartComponent [298](#ch12.xhtml_page298)-[301](#ch12.xhtml_page301)

ApplyVoucherToCartComponent [303](#ch12.xhtml_page303), [304](#ch12.xhtml_page304)

CartAddressComponent [301](#ch12.xhtml_page301)-[303](#ch12.xhtml_page303)

forms, adding to sample application [298](#ch12.xhtml_page298)

LoginComponent [305](#ch12.xhtml_page305)-[307](#ch12.xhtml_page307)

using, with components [294](#ch12.xhtml_page294)-[298](#ch12.xhtml_page298)

v-model modifiers

about [273](#ch12.xhtml_page273)

lazy modifier [274](#ch12.xhtml_page274)-[276](#ch12.xhtml_page276)

number modifier [273](#ch12.xhtml_page273)

trim modifier [274](#ch12.xhtml_page274)

Vue 3

state management [310](#ch13.xhtml_page310)

Vue application

Axios, integrating [330](#ch13.xhtml_page330)

Vue CLI

using, to create project [187](#ch07.xhtml_page187)-[190](#ch07.xhtml_page190)

Vue.js

about [3](#ch01.xhtml_page3)

comparison [4](#ch01.xhtml_page4), [5](#ch01.xhtml_page5)

design studio [25](#ch02.xhtml_page25), [26](#ch02.xhtml_page26)

events [254](#ch11.xhtml_page254)

freelancer/consultant [24](#ch02.xhtml_page24), [25](#ch02.xhtml_page25)

large or enterprise business [28](#ch02.xhtml_page28), [29](#ch02.xhtml_page29)

small and medium enterprises (SME's) [27](#ch02.xhtml_page27), [28](#ch02.xhtml_page28)

small business [26](#ch02.xhtml_page26), [27](#ch02.xhtml_page27)

working with [24](#ch02.xhtml_page24)

Vue.js application

building [100](#ch04.xhtml_page100)

creating, as standalone application [104](#ch04.xhtml_page104)

TypeScript option [108](#ch04.xhtml_page108)

using, as script tag [100](#ch04.xhtml_page100)

Vue.js case study

about [5](#ch01.xhtml_page5)

client-side rendering [5](#ch01.xhtml_page5)-[11](#ch01.xhtml_page11)

website, building [12](#ch01.xhtml_page12)-[20](#ch01.xhtml_page20)

Vue.js component

about [112](#ch05.xhtml_page112), [113](#ch05.xhtml_page113)

render function [115](#ch05.xhtml_page115)-[119](#ch05.xhtml_page119)

script section [115](#ch05.xhtml_page115)

style section [120](#ch05.xhtml_page120), [121](#ch05.xhtml_page121)

template section [114](#ch05.xhtml_page114)

Vue.js documentation

reference link [165](#ch06.xhtml_page165)

Vue.js project

Tailwind, integrating [209](#ch08.xhtml_page209), [210](#ch08.xhtml_page210)

Vue.js role

about [29](#ch02.xhtml_page29)

front-end developer [29](#ch02.xhtml_page29)

full-stack developer [29](#ch02.xhtml_page29)

JAMStack developer [30](#ch02.xhtml_page30)

mobile developer [30](#ch02.xhtml_page30)

web developer [29](#ch02.xhtml_page29)

Vuelidate

custom validators, creating [282](#ch12.xhtml_page282)-[284](#ch12.xhtml_page284)

reference link [277](#ch12.xhtml_page277)

standard validators [279](#ch12.xhtml_page279), [280](#ch12.xhtml_page280)

Vue life cycle

about [92](#ch04.xhtml_page92)

arrow function() life cycle hook [94](#ch04.xhtml_page94)

beforeCreate() life cycle hook [94](#ch04.xhtml_page94), [95](#ch04.xhtml_page95)

beforeMount() life cycle hook [96](#ch04.xhtml_page96)

beforeUnmount() life cycle hook [98](#ch04.xhtml_page98)

created() life cycle hook [95](#ch04.xhtml_page95)

mounted() life cycle hook [96](#ch04.xhtml_page96)

updated() life cycle hook [98](#ch04.xhtml_page98)

Vue project

component mounting, with @testing-library/vue [340](#ch14.xhtml_page340)

Istanbul code coverage provider, adding [340](#ch14.xhtml_page340)

Nightwatch, adding [341](#ch14.xhtml_page341), [342](#ch14.xhtml_page342)

tests, adding to [338](#ch14.xhtml_page338)

Vitest, adding [339](#ch14.xhtml_page339)

VitestUI, adding [339](#ch14.xhtml_page339)

VueRouter

about [356](#ch14.xhtml_page356), [357](#ch14.xhtml_page357)

adding [228](#ch10.xhtml_page228), [229](#ch10.xhtml_page229)

VueRouter navigation guards [246](#ch10.xhtml_page246), [247](#ch10.xhtml_page247)

Vue UI

using, to create project [190](#ch07.xhtml_page190)-[195](#ch07.xhtml_page195)

using, to manage project [190](#ch07.xhtml_page190)-[195](#ch07.xhtml_page195)

W

web application

architect [33](#ch02.xhtml_page33)

building [30](#ch02.xhtml_page30), [31](#ch02.xhtml_page31)

checkout page [135](#ch05.xhtml_page135)

design [130](#ch05.xhtml_page130)

item display page [134](#ch05.xhtml_page134)

junior web developer [32](#ch02.xhtml_page32)

landing page [130](#ch05.xhtml_page130)

lead developer [32](#ch02.xhtml_page32), [33](#ch02.xhtml_page33)

listing/menu page [132](#ch05.xhtml_page132)

login and registration page [138](#ch05.xhtml_page138)

management [33](#ch02.xhtml_page33)

mid-level developer [32](#ch02.xhtml_page32)

order page [140](#ch05.xhtml_page140)

senior web developer [32](#ch02.xhtml_page32)

tech lead developer [32](#ch02.xhtml_page32), [33](#ch02.xhtml_page33)

Web dev ecosystem [200](#ch08.xhtml_page200), [201](#ch08.xhtml_page201)

web developer [29](#ch02.xhtml_page29)

web development

history [2](#ch01.xhtml_page2), [3](#ch01.xhtml_page3)

web sockets API [79](#ch03.xhtml_page79), [80](#ch03.xhtml_page80)

web storage API [76](#ch03.xhtml_page76), [77](#ch03.xhtml_page77)

web workers [77](#ch03.xhtml_page77)-[79](#ch03.xhtml_page79)

Z

Zurb Foundation [211](#ch08.xhtml_page211)
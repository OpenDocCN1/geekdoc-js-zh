![](images/cover.jpg)

![image](images/cover.jpg)

# Exploring
Web Components

![](images/line.jpg)

# *Build Reusable UI Web Components
with Standard Technologies*

![](images/line.jpg)

# Andrea Chiarelli

![](images/logo.jpg)

[www.bpbonline.com](http://www.bpbonline.com)

**FIRST EDITION 2020**

**Copyright © BPB Publications, India**

**ISBN: 978-93-89423-976**

All Rights Reserved. No part of this publication may be reproduced or distributed in any form or by any means or stored in a database or retrieval system, without the prior written permission of the publisher with the exception to the program listings which may be entered, stored and executed in a computer system, but they can not be reproduced by the means of publication.

**LIMITS OF LIABILITY AND DISCLAIMER OF WARRANTY**

The information contained in this book is true to correct and the best of author’s & publisher’s knowledge. The author has made every effort to ensure the accuracy of these publications, but cannot be held responsible for any loss or damage arising from any information in this book.

All trademarks referred to in the book are acknowledged as properties of their respective owners but BPB Publications cannot guarantee the accuracy of this information.

**Distributors:**

**BPB PUBLICATIONS**

20, Ansari Road, Darya Ganj

New Delhi-110002

Ph: 23254990/23254991

**MICRO MEDIA**

Shop No. 5, Mahendra Chambers,

150 DN Rd. Next to Capital Cinema,

V.T. (C.S.T.) Station, MUMBAI-400 001

Ph: 22078296/22078297

**DECCAN AGENCIES**

4-3-329, Bank Street,

Hyderabad-500195

Ph: 24756967/24756400

**BPB BOOK CENTRE**

376 Old Lajpat Rai Market,

Delhi-110006

Ph: 23861747

Published by Manish Jain for BPB Publications, 20 Ansari Road, Darya Ganj, New Delhi-110002 and Printed by him at Repro India Ltd, Mumbai

[www.bpbonline.com](http://www.bpbonline.com/)

# Dedicated to

*My family, who supported and put up with me during the writing process.*

# About the Author

**Andrea Chiarelli** is a software engineer and technical author with more than 20 years of experience in the software development industry. In his career, Andrea has held various roles (software developer and architect, trainer, technical writer) in different ways (as an independent contractor, as a company owner, as an employee).

For the project he was involved in, he has used several programming languages and technologies: from .NET to Node.js, from C# to JavaScript, from SQL Server to MongoDB, from IIS to nginx.

Lately, he is focusing on the JavaScript ecosystem both on the server and on the client-side.

He has contributed to many online and offline magazines and authored a few books.

Currently, he is working at Auth0 as an R&D Content Engineer.

# About the Reviewer

**Akanksha Sinha** is a Technical Manager having 12+ years of experience in various progressive roles in Software Development. Her area of work has been in domains like Digital Marketing, Technology, and Insurance. She was one of the founding members of the Tools & Automation team in Cognizant for Operation Teams working for Tech giants.

As part of her contribution to building a Bot and Tools landscape from scratch, she has explored web development, UI/UX, and the latest technologies like ML, Chatbots, Cloud Computing, NLP, etc. Her skill set includes Javascript, Google Cloud, Google App Script, AngularJS, Typescript, Python, Chrome Extension, GSuites, HTML & CSS, and Unix Shell Scripting. Natural Language, Chatbots, Big Query, and Machine Learning are her area of interest where she has done multiple prototypes.

She has a B.E in E&E from RTM Nagpur University and has worked with Cognizant Technology Solutions.

# Acknowledgement

I would like to thank a few people for allowing this book to become a reality.

First and foremost, I would like to thank my wife and my two daughters, Sofia and Lorena, for putting up with me while I was spending many weekends on writing.

I also thank the online and offline developers community, which loves to exchange experiences and code and support each other more like friends than colleagues.

Finally, I would like to thank the BPB team for their patience in waiting for my always late chapters.

# Preface

In recent years, the design of Web user interfaces has evolved more and more until it is becoming quite similar to native graphical user interfaces. This evolution has been possible mainly to a few popular libraries that spread a composable approach to build user interfaces. Among the others, we can mention React and Angular as the main influencers of this new way of design Web user interfaces.

However, despite the innovation, these libraries brought in the Web development, they created somewhat isolated worlds. Developers that are using React can share and reuse their components just with other React applications. Similarly, Angular developers can share and reuse their components only with Angular projects. Of course, the same also happens with other UI libraries.

This sort of isolation is not what the Web is meant to. Quite the opposite, Web technologies are meant to be open and interoperable. How can we fix this fragmentation created by different approaches in implementing the same high-level design?

Web Components answer to this question.

The set of technologies that Web Components rely on allows developers to create components that can be used to build Web user interfaces independently of the libraries used in a specific project. These technologies are standard and supported by most recent browsers, so they can be considered the standard way to create reusable and interoperable UI components.

This book will present to you the technologies behind Web Components and let you start using them step by step with a practical approach. In fact, throughout the book, you will carry out a full Web Component project that will lead you to understand in detail how to use them.

The 10 chapters of this book will let you explore the following topics:

**[Chapter 1](#c01.xhtml)** introduces the component-based design approach to build user interfaces and the basic concepts behind Web Components.

**[Chapter 2](#c02.xhtml)** discusses how to extend existing standard HTML elements to customize their behavior.

**[Chapter 3](#c03.xhtml)** describes how to create Custom Elements, that is, custom HTML elements built from scratch, without extending the standard ones.

**[Chapter 4](#c04.xhtml)** explains how to manage the properties and attributes of Custom Elements and how to apply the best practices to keep them synced.

**[Chapter 5](#c05.xhtml)** is focused on enriching your Web Component’s interactivity by listening to events and creating your own.

**[Chapter 6](#c06.xhtml)** shows how to implement encapsulation for Web Components by exploiting the Shadow DOM. This feature allows you to include your component on any page without worrying about external CSS or JavaScript side effects.

**[Chapter 7](#c07.xhtml)** discusses how to use HTML templates in order to simplify the component’s markup management.

**[Chapter 8](#c08.xhtml)** describes different strategies on how to distribute and import modules containing Web Components. It also shows how to extend them to create new components.

**[Chapter 9](#c09.xhtml)** discusses how Web Components integrate with other UI libraries and frameworks. It shows how to integrate them into React, Angular, and Vue applications with very little effort. It also shows how to create Web Components by writing them in Angular, Vue, and React.

**[Chapter 10](#c10.xhtml)** describes a few libraries, such as LitElement, Hybrids, Slim, and Stencil, that may help developers to build Web Components.

# Downloading the code
bundle and coloured images:

Please follow the link to download the ***Code Bundle*** and the ***Coloured Images*** of the book:

# [https://rebrand.ly/62bc7](https://rebrand.ly/62bc7)

# Errata

We take immense pride in our work at BPB Publications and follow best practices to ensure the accuracy of our content to provide with an indulging reading experience to our subscribers. Our readers are our mirrors, and we use their inputs to reflect and improve upon human errors if any, occurred during the publishing processes involved. To let us maintain the quality and help us reach out to any readers who might be having difficulties due to any unforeseen errors, please write to us at :

**[errata@bpbonline.com](mailto:errata@bpbonline.com)**

Your support, suggestions and feedbacks are highly appreciated by the BPB Publications’ Family.

Did you know that BPB offers eBook versions of every book published, with PDF and ePub files available? You can upgrade to the eBook version at **[www.bpbonline.com](http://www.bpbonline.com)** and as a print book customer, you are entitled to a discount on the eBook copy. Get in touch with us at **[business@bpbonline.com](mailto:business@bpbonline.com)** for more details.

At **[www.bpbonline.com](http://www.bpbonline.com)**, you can also read a collection of free technical articles, sign up for a range of free newsletters, and receive exclusive discounts and offers on BPB books and eBooks.

# BPB is searching for authors like you

If you're interested in becoming an author for BPB, please visit [**www.bpbonline.com**](http://www.bpbonline.com/) and apply today. We have worked with thousands of developers and tech professionals, just like you, to help them share their insight with the global tech community. You can make a general application, apply for a specific hot topic that we are recruiting an author for, or submit your own idea.

The code bundle for the book is also hosted on GitHub at **[https://github.com/bpbpublications/Exploring-Web-Components](https://github.com/bpbpublications/Exploring-Web-Components)**. In case there's an update to the code, it will be updated on the existing GitHub repository.

We also have other code bundles from our rich catalog of books and videos available at **[https://github.com/bpbpublications](https://github.com/bpbpublications)**. Check them out!

# PIRACY

If you come across any illegal copies of our works in any form on the internet, we would be grateful if you would provide us with the location address or website name. Please contact us at [**business@bpbonline.com**](mailto:business@bpbonline.com) with a link to the material.

# If you are interested in becoming an author

If there is a topic that you have expertise in, and you are interested in either writing or contributing to a book, please visit [**www.bpbonline.com**.](http://www.bpbonline.com/)

# REVIEWS

Please leave a review. Once you have read and used this book, why not leave a review on the site that you purchased it from? Potential readers can then see and use your unbiased opinion to make purchase decisions, we at BPB can understand what you think about our products, and our authors can see your feedback on their book. Thank you!

For more information about BPB, please visit [**www.bpbonline.com**.](http://www.bpbonline.com/)

# [CHAPTER 1](#toc.xhtml_c01)

# [Getting Started with Web Components](#toc.xhtml_c01)

The Web as a platform to build applications is already a consolidated reality. In this platform, standard technologies like HTML and CSS have the main goal to define the **User Interface (UI),** while JavaScript supports interactivity and client-side business logic. These are the traditional roles for these technologies, but it’s not always like that. In recent years, the need for customized UI elements has encouraged the birth of libraries and frameworks mainly based on JavaScript control. Among others, React, Angular, Vue are powerful libraries that allow you to create UI elements by using JavaScript. But the UI elements built with one library can’t be used within the context of the other library. So, usually, if you need the same component in a different context, you need to re-implement it.

Is this the only way to create UI elements? Is there a way to create universal and reusable UI elements, regardless of the framework you are using to build your application?

The answer to these questions is positive. Web components allow you to create UI elements using standard technologies and providing universal support.

In this chapter, we will start by understanding how to design UI by using components, what Web Components are, and how they evolved in the history of web development. The chapter will introduce the standard technologies that build up the current Web Components specifications and discuss the current browser support. It also explains how to include third parties Web Components in a web application and how to support older browsers by using a few polyfills.

# [Structure](#toc.xhtml_s1a)

*   UI, components, and applications
*   What is Web Components?
*   Using a web component
*   Browser support
*   Using polyfills

# [Objectives](#toc.xhtml_s2a)

After reading this chapter, you will be able to design your web UI by using a component-based approach. You also will have a high-level understanding of what Web Components are, and will be able to include any existing Web Components in your HTML pages.

# [UI, components, and applications](#toc.xhtml_s3a)

UI plays a key role in modern applications. It is the main medium that allows the user to interact with the application’s functionalities. In the web context, the technologies to create a UI are standardized, but the demand for increasingly sophisticated interactivity generated the birth and spread of many UI libraries that are not compatible with each other. Web Components try to bring the need for this high sophisticated interactivity into the boundaries of the web standards.

Before meeting the Web Components, however, let’s start by reasoning about UIs and how we might like to have them to simplify our design effort in the web context.

# [1\. Decomposing UI](#toc.xhtml_s4a)

UI is an aggregate of items displayed on a screen that helps the user to interact with an application. This could be an informal definition of a UI, but for a better understanding, let’s take a look at the following screenshot:

![](images/Fig_1.1.jpg)

**Figure 1.1**

This is the home page of the *Save the Children* organization’s website (**[https://www.savethechildren.org/](https://www.savethechildren.org/))**. Intuitively, you can identify several items on this page, each having a specific role. The user can easily identify such items to interact with the functionalities provided by the website.

Let’s highlight some of these items in the following screenshot:

![](images/Fig_1.2.jpg)

**Figure 1.2**

You can see a few areas of the home page with a blue border. These bordered items represent elements of the UI that allows the user to interact with specific functionalities. So you have a bar on the top that allows you to manage your account, a bar with the navigation menu and the search box, an image inviting you to donate, and so on.

These items compose the whole page; they are components of the page, which represent the UI.

# [2\. What is a component?](#toc.xhtml_s5a)

As you can see from the picture, the decomposition of the UI is quite arbitrary. Each one of us may choose a different approach to decompose the UI and find different sets of components. For example, someone may consider the top and navigation bar as one component. In contrast, someone else may consider the navigation bar as a set of independent components—one for the search box, one for the donate button, one for each menu, and so on.

There is not a definitive rule to identify a UI element as a component. You may choose any element or group of elements of the page to define it as a component. It is definitively up to you.

Anyway, you should keep in mind a couple of criteria to identify a UI element or a group of UI elements as a component:

*   They should have a specific and consistent role
*   They should be reusable

If you take a look at the bordered items in the picture above, they identify page areas with a specific role:

*   The top bar allows the user to manage their account
*   The item under the top bar allows the user to perform global actions over the website, such as search words or navigate to a different area
*   The area below the navigation area is meant to invite users to donate
*   The area containing links to the latest news
*   The area to sign up
*   The areas to specific missions

If you consider these areas, you may realize that they are a sort of self-contained unit. You could move the items on the page and rearrange the page with a new layout. You can also reuse each of them on another page, and maybe any of them can be reused on another website as well.

This is one of the powers of components: having their own identity that allows you to consider them as a unit.

# [3\. Composing components](#toc.xhtml_s6a)

The ability to be a unit with a specific role is not the only characteristic of a component. A component is the building block of a more complex entity, but the resulting entity may be a component itself. If you think a bit of it, you may realize that after all, the whole web page is a component itself - it is part of the website or web application and has a specific role in that context.

So, more in general, we can say that a component may contain other components or, equally, it may be composed of other components. Consider, for example, the component shown in the following screenshot:

![](images/Fig_1.3.jpg)

**Figure 1.3**

You may consider it a self-contained component with the role of gathering the user data and allow them to sign up. Or you may consider it as a component built on the aggregation of other components, as shown in the following screenshot:

![](images/Fig_1.4.jpg)

**Figure 1.4**

Each bordered item in the preceding screenshot has a specific role - one displays the title; one gets the user’s first name, and so on. So, each item can be considered a component, and altogether they build a new component.

It’s up to you and your convenience to decompose a component accurately in subcomponents and build your UI as a combination of components. In the example above, you could reuse the textboxes in another form, so you have a concrete convenience to consider them as components.

What usually happens is that a UI is a combination of multiple components, almost always organized in a hierarchy. This hierarchy of components is often called a **component tree**.

# [4\. Mapping components to HTML](#toc.xhtml_s7a)

The UI decomposition carried out in the previous section is quite generic. It applies to any kind of UI. But let’s restrict to web UI implementation:

*   How much would you like to map each detected component to a corresponding HTML element directly?
*   How much would you like to define the home page shown in the previous section with a much more descriptive HTML markup?

Take a look at the following markup:

`<!DOCTYPE html>`

`<html lang=”en”>`

`<head>`

`<meta charset=”utf-8”>`

`<!-- Style, script and other head stuff -->`

`</head>`

`<body>`

`<account-management-bar></account-management-bar>`

`<navigation-bar></navigation-bar>`

`<front-cover></front-cover>`

`<news-area></news-area>`

`<sign-up-form></sign-up-form>`

`<mission-tile mission-id=”123”></mission-tile>`

`<mission-tile mission-id=”321”></mission-tile>`

`</body>`

`</html>`

As you can see, the markup above is, actually, a direct mapping between the components we detected in the previous sections and a set of hypothetical HTML elements. This would be the concrete realization of the Semantic HTML, that is the idea that all your HTML markup should represent the meaning of your content, not its appearance.

What usually happens to see, in the best case, is a markup similar to the following:

`<!DOCTYPE html>`

`<html lang=”en”>`

`<head>`

`<meta charset=”utf-8”>`

`<!-- Style, script and other head stuff -->`

`</head>`

`<body>`

`<div class=”account-management-bar”>`

`<div id=”…”>…</div>`

`</div>`

`<div class=”navigation-bar”>…</div>`

`<div class=”front-cover”>…</div>`

`<div class=”news-area”>`

`<ul>…</ul>`

`…`

`</div>`

`<div class=”sign-up-form”><form>…</form></div>`

`<div>`

`<div class=”mission-tile”>…</div>`

`<div class=”mission-tile”></div>`

`</div>`

`</body>`

`</html>`

Here there, the markup doesn’t express the meaning of each element. You may infer it from the CSS classes, but the whole markup is too verbose and not so readable.

On the other hand, if you could use a markup so concise and clean like the one we imagined above, your web UI was very readable, maintainable, and reusable. In a word, it would be effective.

This is something that web developers have been looking for in several ways. Year after year, adding new elements like `<blockquote>, <nav>, <video>`, and similar to the HTML standard, we have more and more possibilities to express our markup with a semantic approach. However, this approach is too slow and proposes generic elements. It cannot effectively respond to the specific needs of every single developer.

As you will see in the next section, you can build your semantic elements simply using the web platform standard technologies.

# [What are Web Components?](#toc.xhtml_s8a)

Decomposing a Web UI, as shown in the previous section, seems quite natural and desirable. It is an effective approach that allows you to create, at the same time, well-structured UIs and reusable UI elements. Also, since a component is a generic concept, and you can create a new component by combining other components, you can consider a component, even your whole application.

For years, developers have been looking for a way to autonomously extend the possibilities offered by HTML to create advanced UI elements. The result of their efforts has been libraries like *jQuery UI, React, Angular, Vue,* and similar. All these libraries provide ways to create UI elements following the component model.

Many of these libraries are very popular, and each one proposes their approach to create UI components, and each one somehow tries to map UI elements to markup. Anyway, they have a few drawbacks:

*   They are not standard
*   They are not natively supported by the browsers
*   They are not interoperable

In other words, the UI component created with these libraries can be used only in projects supporting the same library. You cannot create a component with React and use it within an Angular application. If you want to create a UI element that can be used in a React application and an Angular application, you need to implement two versions of the element.

Web Components try to overcome these drawbacks by allowing you to create UI elements by using standard technologies natively supported by the browsers.

Web Components are a set of standard specifications for creating custom HTML elements that can be reused in web pages and applications. The first mention of the principles of this technology dates back to *2011*, during the session of *Alex Russell at the Fronteers conference in Amsterdam*. His proposal has been taken into account by the W3C that published the first *Working Draft in 2012*. Since then, the standardization process has introduced several variations to the original idea, so that we got two different versions of the specifications over time, identified with *v0* and *v1*. Currently, Web Components are no longer based on separate specifications but refer to the standards of HTML and **Document Object Model (DOM),** which they are now an integral part of.

Web Components lay on three standard features of web technologies:

*   **Custom elements:** They represent a set of JavaScript APIs for creating custom DOM elements associated with a specific HTML tag.
*   **Shadow DOM:** A set of JavaScript APIs that allow managing a specific DOM for a component, independent from the web page’s DOM
*   **HTML templates**: It is an integration to the HTML specifications that allows you to define portions of markup that are not interpreted when the page is loading, but that is instantiated at runtime.

Thanks to the Web Components technology, you can extend standard HTML elements to have customized look and feel and behave. You can also create your HTML tag and use it in an HTML page as a standard element. You can do all this independently from the JavaScript library or framework you are using to build your application.

**You could have heard about a fourth technology Web Components rely on: HTML Imports.**

**Although it is an official alive W3C specification, practically it is not supported by any browser because it is superseded by ECMAScript modules.**

**See for example the following document that declares HTML Imports deprecated for Chrome: [https://www.chromestatus.com/feature/5144752345317376](https://www.chromestatus.com/feature/5144752345317376)**

# [Using a Web Component](#toc.xhtml_s9a)

So far, we talked about components and Web Components abstractly. Now it’s time to start seeing in action this technology.

Let’s begin exploring Web Components from the viewpoint of a developer who wants to use a ready-to-use component. You will learn how to build your web component throughout the rest of the book.

To show how to use a web component developed by a third party, we will refer to a component that allows you to give a rating through a certain number of stars, similar to the UI elements you find in many e-commerce websites.

Check the documentation of this simple project on *GitHub* to know more about the component **- [https://github.com/andychiare/rating-component](https://github.com/andychiare/rating-component)**.

Let’s start by creating an empty HTML page and with reference to the code of the component, as shown by the following markup:

`<!DOCTYPE html>`

`<html lang=”en”>`

`<head>`

`<meta charset=”utf-8”>`

`<script src=”https://andychiare.github.io/cdn/rating-component/myRating.js”></script>`

`</head>`

`<body>`

`</body>`

`</html>`

As you can see, we added a script element pointing to the public URL of `myRatings.js` JavaScript file. This file contains the definition of the component, but currently, we are not interested in the implementation. We just want to use the component on a web page.

**This is the simplest way to include the library in your project, but you can use a package manager if your application requires a building step. We’ll go into this later.**

Now, you can simply use the `my-rating` tag in the body of the HTML as if it were a standard element:

`<!DOCTYPE html>`

`<html lang=”en”>`

`<head>`

`<meta charset=”utf-8”>`

`<script src=”https://andychiare.github.io/cdn/rating-component/myRating.js”></script>`

`</head>`

`<body>`

`<my-rating max-value=”6” value=”3”></my-rating>`

`</body>`

`</html>`

The `my-rating` element has the max-value, and the value attributes that allow you to set, respectively, the maximum number of stars to be displayed and the current value of stars expressing your rating.

As you can see, the my-rating tag is used like any standard HTML tag, and what is most important is the fact that you do not need to install any UI framework to get this behavior.

To see the graphical result of this markup, you just need to open the HTML page in a web browser. You should see a page like the following:

![](images/Fig_1.5.jpg)

**Figure 1.5**

**In this specific simple case, you can use a web browser to open the HTML page from the file system. However, in general, it should be better to serve the pages with a web server. You can choose any web server you prefer. We suggest using http-server, a zero-configuration web server running in Node.js environment.**

**To install http-server on your machine, first ensure you have Node.js already installed, then type the following command in a terminal window:**

`npm install http-server -g`

**Once the installation terminates, you can start the server by moving in the folder containing the HTML stuff and typing the following command in a terminal window:**

`http-server`

**This command will start the web server, and you will be able to see your page by pointing your browser to http://localhost:8080.**

Now, when you click one of the stars, the star you clicked and the stars on its left become filled, while the stars on its right become empty. This expresses your rating.

As you can see, using a web component is as simple as using any standard HTML element. You configure the element by setting values in its attributes, and it works accordingly.

You can also use the component programmatically via JavaScript. Consider, for example, the following code:

`<!DOCTYPE html>`

`<html lang=”en”>`

`<head>`

`<meta charset=”utf-8”>`

`<script src=”https://andychiare.github.io/cdn/rating-component/myRating.js”></script>`

`<script>`

`window.onload = function() {`

`const myRating = document.getElementById(“myRatingComponent”)`

`myRating.maxValue = 10;`

`myRating.value = 2;`

`};`

`</script>`

`</head>`

`<body>`

`<my-rating id=”myRatingComponent”></my-rating>`

`</body>`

`</html>`

In this example, we assigned the identifier `myRatingComponent` to the element and used it to get access via JavaScript by using the `getElementById()` method. We also assigned new values to the properties `maxValue` and value corresponding respectively to the max-value and value attributes. This allows you to have a different initial appearance on the web page.

In addition to setting the initial values for the component properties, you can treat it as a common HTML element. For example, you can attach an event handler to it, as shown in the following example:

`<!DOCTYPE html>`

`<html lang=”en”>`

`<head>`

`<meta charset=”utf-8”>`

`<script src=”https://andychiare.github.io/cdn/rating-component/myRating.js”></script>`

`<script>`

`window.onload = function() {`

`const myRating = document.getElementById(“myRatingComponent”)`

`myRating.maxValue = 10;`

`myRating.value = 2;`

`myRating.addEventListener(“click”, () => {`

`alert(“Thanks for your feedback!”);`

`});`

`};`

`</script>`

`</head>`

`<body>`

`<my-rating id=”myRatingComponent”></my-rating>`

`</body>`

`</html>`

Here you are handling the click event so that when the user gives their rate, a thank-you message appears:

![](images/Fig_1.6.jpg)

**Figure 1.6**

These simple examples just give you an idea of what Web Components are from the viewpoint of a developer that uses them. Starting from the next chapter, you will also learn how to build your web component.

# [Browser support](#toc.xhtml_s10a)

The technologies which Web Components are built on are standard that is they are intended to be natively supported by web browsers. Unfortunately, despite the availability of specifications for some time now, only recently, they are going to be largely adopted by most web browsers.

To have an idea of the recent and current state of the support of these technologies by the most popular browsers, let’s take a look at some data from caniuse.com **([https://caniuse.com/](https://caniuse.com/))**, a website monitoring the web technology adoption.

The first data are related to **Custom Elements** support. At the writing time they are summarized by the following picture:

![](images/Fig_1.7.jpg)

**Figure 1.7**

These data show that **Custom Elements** are supported by **88.93%** of tracked browsers, but only **73.69%** of the browser provides full support. The remaining **15.24%** provide partial support. If you look at the picture, you realize that only the latest versions of browsers support this technology. Also, some still popular browsers have no or partial support.

On the other hand, **HTML Templates** have wider support, as the following picture shows:

![](images/Fig_1.8.jpg)

**Figure 1.8**

As you can see, **94.44%** of tracked browsers support this technology, and only **0.24%** provide partial support.

Finally, let’s take a look at the data regarding the support for the **Shadow DOM:**

![](images/Fig_1.9.jpg)

**Figure 1.9**

This technology has high support **(89.25%),** but not total. Also, consider that **13.16%** of the tracked browsers provide partial support.

In summary, from the data obtained from caniuse.com, we realize that the latest version of Chrome, Firefox, and Edge have wide and stable support of Web Components technologies. Also, mobile browsers have good support for them.

However, even if the technologies supporting Web Components are gaining increasingly wide support, you cannot ignore that some browsers, like Opera and Safari, still provide partial support, and people not always uses the latest version of a browser.

# [Using polyfills](#toc.xhtml_s11a)

The scenario depicted in the previous section seems not so encouraging. Even if recent browsers have great support for Web Components, there are still browsers that don’t support them or provide partial support.

So, can we consider Web Components technology mature enough to be used in production? Would it currently better continue to use React, Angular, and the other UI frameworks since they guarantee a certain level of backward compatibility with old browsers?

The questions are quite legitimate. You cannot risk that some users will not be able to correctly access your site or your application due to a lack of browser support.

Fortunately, you can use some polyfill libraries that allow you to emulate what browsers don’t support yet.

**A polyfill is a module, a snippet of code, or a library, usually in JavaScript, that provides functionalities that modern browsers support natively, but that older browsers don’t.**

To work around the problem of lack or partial support in some browsers, you can include the polyfills provided by the open-source community at the following URL: **[https://github.com/webcomponents/polyfills](https://github.com/webcomponents/polyfills)**

You can use the entire `WebComponentsJS` suite of polyfills, or you can choose to use them individually - the polyfill for custom elements, for Shadow DOM, or HTML Templates. Also, you can choose to install them in your development environment by using `npm` or to include them in an HTML page by using the unpacked version from unpkg.com content delivery network (CDN) at ***[https://unpkg.com/browse/@webcomponents/webcomponentsjs/](https://unpkg.com/browse/@webcomponents/webcomponentsjs/).***

Let’s take a look at how you can leverage these polyfills by using the unpacked version. For this purpose, we are going to consider the rating component example shown in a previous section and will add the unpacked polyfill. This is the new markup:

`<!DOCTYPE html>`

`<html lang=”en”>`

`<head>`

`<meta charset=”utf-8”>`

`<script src=”https://unpkg.com/@webcomponents/webcomponentsjs/webcomponents-bundle.js”></script>`

`<script src=”https://andychiare.github.io/cdn/rating-component/myRating.js”></script>`

`</head>`

`<body>`

`<my-rating max-value=”6” value=”3”></my-rating>`

`</body>`

`</html>`

Note the script inclusion before the rating component script. It loads the `webcomponents-bundle.js` script that emulates the Web Components technologies for the browsers not supporting them. The script provides a collection of polyfills that are activated via feature detection; that is, their code is executed only when the corresponding feature is not natively supported by the current browser. Although this approach ensures efficient use of browser features, loading all polyfills implemented by the script would be unnecessary when the browser provides partial support of the Web Components technologies. It should load just the supported ones.

To overcome this problem, you can resort to another script that loads only the necessary polyfills according to what the current browser is missing. The script is called `webcomponents-loader.js`, and you can use it instead of `webcomponents-bundle.js` as shown in the following code:

`<!DOCTYPE html>`

`<html lang=”en”>`

`<head>`

`<meta charset=”utf-8”>`

`<script src=”https://unpkg.com/@webcomponents/webcomponentsjs/webcomponents-loader.js”></script>`

`<script src=”https://andychiare.github.io/cdn/rating-component/myRating.js”></script>`

`</head>`

`<body>`

`<my-rating max-value=”6” value=”3”></my-rating>`

`</body>`

`</html>`

This will load only the bare minimum of the available polyfills to support the features enabling Web Components also in browsers with partial support.

Of course, these polyfills cannot guarantee the Web Components technologies for any browser. Their support is intended for quite recent browsers, so don’t expect they work, for example, on *Internet Explorer 8.*

# [Conclusion](#toc.xhtml_s12a)

In this chapter, we’ve seen how components are a convenient way to design your UI. They allow you to concentrate on small pieces of functionality and help you to reuse them in different parts of the same application or other applications. We also discussed that many JavaScript libraries and frameworks promoted this component-based approach in building UIs, but they are not compatible with each other. Then, we introduced Web Components as a standard native alternative to build UI components and took a look at how to include them in your web pages. We also discussed the browser support to the technologies underlying Web Components and showed how to use polyfills libraries to emulate these technologies on older browsers.

By reading this chapter, you’ve learned what Web Components are and how to include an existing Web Component in your web pages. Also, by using polyfills, you are also able to guarantee that your web pages are correctly rendered in browsers that have partial or no support for the technologies that enable Web Components.

In the next chapter, you will start to learn how to implement your web component by extending existing HTML elements.

# [Questions](#toc.xhtml_s13a)

1.  What is a component?
2.  Why components are useful when designing a UI?
3.  What are Web Components?
4.  What are the standard technologies Web Components rely on?
5.  What benefits do they provide with respect to other popular UI JavaScript libraries?
6.  How can you mitigate the lack of Web Components technologies support in older browsers?

# [CHAPTER 2](#toc.xhtml_c02)

# [Extending HTML Elements](#toc.xhtml_c02)

In the previous chapter, we started to know Web Components and learned how to use them. In this chapter, you are going to learn how to build your own Web Components. We will start by briefly talking about the development environment you need to set up. Then, we will introduce the basic concepts about custom elements and will see how to extend native HTML elements by customizing their standard behavior. Throughout the chapter, we will create a custom element to illustrate these new concepts.

# [Structure](#toc.xhtml_s14a)

*   Setting up a development environment
*   Custom elements
*   Extending native elements
*   Web components naming rules
*   Using a custom element based on native elements
*   Benefits of extending native elements

# [Objectives](#toc.xhtml_s15a)

This chapter will give you the basic knowledge to decide the development environment to use when you are creating your Web Component. You will learn what custom elements are and which type of them you should use. You will be able to create a new custom element by extending an existing standard HTML element and will use it in different development environments. You will also learn the rules to follow when naming your Web Component and will be aware of the benefits you get by extending standard HTML elements.

# [Setting up a development environment](#toc.xhtml_s16a)

In the previous chapter, we included an existing Web Component in an HTML page by putting a simple reference to the file that implements it via the `<script>` element. We didn't care about the development environment to be used in that case.

Now, we are going to implement our first Web Component and reasoning about the development environment could be appropriate. In general, since creating a Web Component doesn't require more than HTML, JavaScript, and CSS, we would suggest using any development environment you feel comfortable with. But you know that recently JavaScript development has grown its complexity, mostly due to the needs of a few requirements like keeping the language compatibility with older browsers, supporting some language extension like JSX, providing a bundling step for the production code, and so on. In the light of these possibilities, you may wonder what is the better approach to get a development environment for Web Components.

The good news is that developing Web Components is quite flexible, so you can integrate it into the approach you prefer. In this section, we will take a look at some approaches, but consider them as suggestions, not constraints.

# [The editor](#toc.xhtml_s17a)

Choosing an editor is always a matter of preference. In order to develop your Web Component, you can use any editor. You can be very minimal and use a common text editor, the one coming with your operating system, for example. However, it might not be the most comfortable choice.

Maybe you could use more advanced editors or **Integrated Development Environments (IDE)** that offer you more than simply writing code. Usually, those tools provide you with syntax highlighting, code completion, snippets of code, support for debugging, and so on. Of course, these and other features help you in being more productive.

You can choose among many advanced editors or IDEs: Atom, Sublime Text, Visual Studio Code, just to mention a few. Use the one you already know, or you are comfortable with.

# [Development without building](#toc.xhtml_s18a)

As mentioned before, in recent years, JavaScript developers are used to building a step of their code. This may be required for a few reasons that range from browser compatibility to the use of extension libraries to code optimization, bundling, and so on.

From the Web Component perspective, you could not use any building step. You can simply write your code and include it in an HTML page by using the `<script>` element or import it in another JavaScript module.

This approach provides you with a few benefits. You have a simple development environment without needing external tools and specific configurations. You just need your code and a simple web server.

However, it has some drawbacks. For example, you need a recent browser that supports recent JavaScript features. This might not be a problem during the development process, but in production, you have no control over the user's browser. So, even if it could become the standard way of developing Web Components in the future, nowadays, it may be a bit risky if your component is meant for a larger audience of users.

# [Development with building](#toc.xhtml_s19a)

Usually, developers choose to build their JavaScript applications for a few reasons. These are some of the most common motivations:

*   Transpiling: This process is performed by a tool (transpiler) that transforms the original JavaScript code into another form, but still JavaScript. There may be multiple reasons for this transformation. The most important reason is to transform modern JavaScript code into old-style JavaScript so that it can also run in old browsers. In addition, transpiling allows you to use recent JavaScript features in your code even if they are not yet supported by your browser. But also it allows you to run non-standard code such as JavaScript language extension or similar.
*   Reducing the application size: This process performs some optimizations like removing unused or unreachable code (tree shaking) and transforming the original code with a more compact version (minification). The goal is to reduce the size of the resulting application so that it can be transferred faster on the network.
*   Bundling: The bundling process combines multiple files into one or, in any case, a smaller number of files. This makes the browser to perform a smaller number of HTTP requests in order to load your application.
*   Code splitting: This is the opposite of the bundling process. It allows you to split the code of your application into multiple files (bundles) so that they can be loaded on demand. This optimizes the use of the network bandwidth and the starting time of your application.

These are the main reasons for applying the building step to your application development process. Other reasons may exist depending on the needs of your specific application. For example, you may apply a pre-processing step for styling transformations, like the one that transforms Sass stylesheets to CSS, or for image processing, and so on.

If you decide to build the code for your Web Component, you can choose the transpiler and the bundler you prefer. Maybe Webpack and Rollup are among the more popular ones, but definitively the choice is up to you.

# [The Web Components builder project](#toc.xhtml_s20a)

For the purposes of this book, but also for any of your own development purposes, you can download a pre-configured building project based on Webpack from the following GitHub repository: **[https://github.com/andychiare/web-components-builder](https://github.com/andychiare/web-components-builder).**

The project, named Web Components Builder, acts as a project template for a development environment for Web Components. Be sure to have Node.js installed on your computer since it depends on this runtime.

You can get a copy of the Web Components Builder project by using git. Just type the following command in a terminal window:

`git clone` [`https://github.com/andychiare/web-components-builder.git`](https://github.com/andychiare/web-components-builder.git)

You will get the content of the project in a folder named `web-components-builder`. Now, move into this folder and install the required dependencies by typing the following command:

`npm install`

This command will download and install Webpack and all the required libraries at the project level.

**In the rest of the book, when we will talk about cloning and initializing a copy of the Web Components Builder project, we will refer to the** `git clone,` **and** `npm install` **commands described above.**

The project comes with a sample Web Component, the rating component we used in the first chapter. The following picture shows the file and folder structure after the project initialization:

![](images/Figure_2.1.jpg)

**Figure 2.1**

The sample Web Component is meant for having an example of how to use the project. When you build your own Web Component, you have to change the content of the `index.js` file in the `src` folder and the content of the `index.html` file in the `root` folder of the project. You will see an example of using this project template later on in this chapter.

To see the sample Web Component in action, just type the following command:

`npm start`

After a few seconds, the project is built, so you can open a browser and point it to `http://localhost:8080.` You should see a page like the one shown in the following picture:

![](images/Figure_2.2.jpg)

**Figure 2.2**

When you are happy with the Web Component you've built, you can create a production-ready version of the component. As said before, it means transpiling your code for broader compatibility, reducing size, bundling, and so on. So, build your component by typing the following command:

`npm run build`

After a few seconds, you will get the result of the building process in the `dist` folder. The result of this process in the Web Components Builder project also includes the polyfills we discussed in the first chapter, so your Web Component is ready to be also supported by not recent browsers.

In the rest of the book, we will refer to this project when we need to use a building environment, but, of course, feel free to create and use your own building environment.

# [Custom elements](#toc.xhtml_s21a)

When we introduced Web Components in the first chapter, we said that they rely on three technologies: Custom Elements, Shadow DOM, and HTML Templates. The Custom Elements technology is the first one we are going to explore, and maybe it may appear as the most evident when it comes to creating your own Web Component.

In fact, Custom Elements enable you to define your own HTML elements and to make them available in your HTML pages or Web applications. Custom Elements are identified in the markup of an HTML page with tags like any standard HTML element. In addition, they can be accessed via JavaScript, just like any standard HTML element.

You can create two types of Custom Elements:

*   Customized Native Elements
*   Autonomous Custom Elements

The Customized Native Elements are Custom Elements built, starting from an existing standard element. Basically, they extend the features of a standard HTML element like `<img>, <button>, <input>,` and so on.

The Autonomous Custom Elements are Custom Elements built from scratch. They don't extend standard HTML elements, so their behavior is up to your code.

In this chapter, we are going to explore Custom Native Elements. This means that we start to create Custom Elements by extending existing standard HTML elements.

# [Extending native elements](#toc.xhtml_s22a)

As usual, throughout the book, we are going to learn how to create Custom Native Elements by building things. So, we are going to introduce the concepts and the syntax to create Custom Native Elements by building a new Web Component. The component we are going to create is a secure link; that is a link that warns the user when the URL it refers to is not secure; that is, it is not using HTTPS. So, basically, our component is a standard `<a>` HTML element with the addition of this feature.

In order to put in practice this goal, create a file named `secureLink.js` and put the following code inside it:

`class SecureLink extends HTMLAnchorElement {`

`connectedCallback() {`

`this.addEventListener("click", (e) => {`

`if (!this.href.startsWith("https")) {`

`if (!confirm("You are about to navigate to an unsafe site.` `Do you want to continue?")) {`

`e.preventDefault();`

`}`

`}`

`})`

`}`

`}`

`customElements.define("secure-link", SecureLink, {extends: "a"});`

This simple snippet of code defines the Custom Element we were looking for. Let's analyze the code to understand how it works.

This first thing you notice is that we are defining a JavaScript class named `SecureLink` inheriting from `HTMLAnchorElement`. The HTMLAnchorElement is the built-in DOM class representing the <a> HTML element, so we are inheriting all the features that come with it.

The class defines the `connectedCallback()` method. This method is automatically called when an instance of this element is inserted into the DOM. It is part of a set of callbacks, also called custom element reactions, which are automatically called at certain stages of a component's lifecycle. We will head back to them in the next chapter. For now, we just need to know that the `connectedCallback()` method will be called after that our Web Component is added to the DOM of the current HTML page.

The code in the body of the `connectedCallback()` method is quite simple: it adds an event handler to the click event. This event handler checks if the URL associated with the element doesn't start with the https string. In this case, an alert will be shown to the user, and, if confirmed, the navigation stops.

The last statement you see in the JavaScript file is the following:

`customElements.define("secure-link", SecureLink, {extends: "a"});`

This statement has a fundamental role. It adds the `SecureLink` class in the Custom Elements registry of the current browser's window. The `define()` method of the `customElements` collection performs this registration, and it takes the following parameters:

*   **The name of the Custom Element**: This is a string defining the name that identifies our element in the HTML markup. In our case, the new element will be associated with the secure-link name.
*   **The class implementing the Custom Element**: In our case we are simply passing the `SecureLink` class.
*   **The options:** An optional object defining how the element is defined. Currently, only the extends option is supported: it specifies the name of the built-in element to extend.

**Make sure you don't forget to register your Web Component. The class definition is not enough to create your component.**

As you can see, the registration of our Web Component is quite simple. But maybe you are wondering why we need to specify we are extending the `<a>` element by passing the `{extends: "a"}` object. After all, we just defined our `SecureLink` class by extending the built-in `HTMLAnchorElement` class.

The reason for such a requirement lies in the fact that many HTML elements share the same base class. For example, the `<h1>` and `<h2>` elements both extend the `HTMLHeadingElement` class, so defining a Custom Element that extends this class is not enough to determine which HTML element you actually want to extend.

On the other hand, when you want to create your own Custom Element by extending a native one, you need to know what is the base class to extend. The following is a list of the most common HTML elements with their base classes:

| **Element** | **Base class** |
| `<a>` | `HTMLAnchorElement` |
| `<audio>` | `HTMLAudioElement` |
| `<b>` | `HTMLElement` |
| `<blockquote>` | `HTMLQuoteElement` |
| `<body>` | `HTMLBodyElement` |
| `<br>` | `HTMLBRElement` |
| `<button>` | `HTMLButtonElement` |
| `<canvas>` | `HTMLCanvasElement` |
| `<div>` | `HTMLDivElement` |
| `<em>` | `HTMLElement` |
| `<form>` | `HTMLFormElement` |
| `<h1>, <h2>, <h3>,…` | `HTMLHeadingElement` |
| `<head>` | `HTMLHeadElement` |
| `<html>` | `HTMLHtmlElement` |
| `<i>` | `HTMLElement` |
| `<img>` | `HTMLImageElement` |
| `<input>` | `HTMLInputElement` |
| `<label>` | `HTMLLabelElement` |
| `<li>` | `HTMLLIElement` |
| `<ol>` | `HTMLOListElement` |
| `<p>` | `HTMLParagraphElement` |
| `<select>` | `HTMLSelectElement` |
| `<span>` | `HTMLSpanElement` |
| `<table>` | `HTMLTableElement` |
| `<td>` | `HTMLTableCellElement` |
| `<textarea>` | `HTMLTextAreaElement` |
| `<tr>` | `HTMLTableRowElement` |
| `<ul>` | `HTMLUListElement` |
| `<video>` | `HTMLVideoElement` |

**Table 2.1**

For the complete list, please refer to the official documentation at the following address: **[https://html.spec.whatwg.org/multipage/indices.html#element-interfaces](https://html.spec.whatwg.org/multipage/indices.html#element-interfaces)**.

# [Web Components naming rules](#toc.xhtml_s23a)

Before going to see how to use the Web Component we have just defined, let's spend a few words about how to name your elements.

**Be aware that the name of your Custom Element is not the name of the class that implements it.**

The class name identifies the implementation of your Custom Element, while the name of your Custom Element is the string you pass to the `customElements.define()` method. It identifies your Custom Element in the HTML markup.

In the example that we described in the previous section, we named our Custom Element as a secure-link. The presence of a dash in the name is not accidental. In fact, according to the specifications, the name of a Custom Element must have a dash in its name. So, `securelink` is not a valid name, while secure-link is a valid one.

This trick allows HTML parsers to distinguish regular elements from Custom Elements and avoids possible conflicts with the future addition of new standard tags. However, even if a name with at least one dash is a legal name for your Custom Elements, you cannot use any of the following names:

*   `annotation-xml`
*   `color-profile`
*   `font-face`
*   `font-face-src`
*   `font-face-uri`
*   `font-face-format`
*   `font-face-name`
*   `missing-glyph`

These are reserved names from SVG and MathML.

The need to have a dash in the name of your Custom Element gives you the opportunity to name elements with a sort of namespace and to avoid conflicts with Custom Elements created by a third-party. Even if it is not a requirement, you should consider prefixing the name of your Custom Element with a hopefully unique name. For example, if you are building your Custom Element library and want to name it foo, you could name your elements by using the `foo`- prefix. So you could have names like foo-input, `foo-link, foo-image,` and so on.

# [Using a Custom Element based on native elements](#toc.xhtml_s24a)

Now, you have your secure-link Web Component, and you want to use it in your Web application. You have a few options for using it, and it mostly depends on the type of application or website you are building. Let's take a look at the two commons options: including in an HTML page or importing in a JavaScript module.

# [Including in an HTML page](#toc.xhtml_s25a)

The simplest way to use your component in your website is to include the JavaScript script in your HTML page, as in the following:

`<!DOCTYPE html>`

`<html lang="en">`

`<head>`

`<meta charset="utf-8">`

`<script src="secureLink.js"></script>`

`</head>`

`<body>`

`</body>`

`</html>`

This is the way we used the `my-rating` component in the first chapter, so there's nothing really new. Then, to use your component, you will add the following code to the body of your HTML page:

`<a is="secure-link" href="http://www.wikipedia.org">Wikipedia</a>`

As you can see, here we are using the Web Component differently to the `my-rating` component presented in the first chapter. While in the case of the `my-rating` component, we used that name as a tag, here we are using the component's name as a value for the is attribute of the `<a>` HTML element. This is the macroscopic difference from the markup point of view between an Autonomous Custom Element and Customized Native Element. What we are saying here is that our element is an `<a>` HTML element with the additional feature provided by the `secure-link` extension. In the next section, we will discuss a bit more in depth the reasons behind this approach and which are the benefits of using customized native elements. For the moment, we take note of this and see what happen to the new page whose full code now appears as follows:

`<!DOCTYPE html>`

`<html lang="en">`

`<head>`

`<meta charset="utf-8">`

`<script src="secureLink.js"></script>`

`</head>`

`<body>`

`<a is="secure-link" href="http://www.wikipedia.org">Wikipedia</a>`

`</body>`

`</html>`

Now, open the page with a browser. You should see a blank page with a link to the Wikipedia website. By clicking the link, you should get an alert window warning that you are about to navigate to a non-safe website, similarly, as shown in the following picture:

![](images/Figure_2.3.jpg)

**Figure 2.3**

Only if you consent to navigate to that link the browser will load the Wikipedia's home page. If you do not consent, you will stay on the current page as expected.

Now you have a customized version of the standard <a> HTML element.

If you take a look back at the Custom Element implementation, you will see that it could be improved in the way it handles the security requirement. Of course, you're right, but this is not the focus of the implementation. Here we are simply focussing on how to create your own Custom Element by extending native elements.

# [Importing in a JavaScript module](#toc.xhtml_s26a)

So far, we showed a very simple way to include your code in an HTML page and use your Custom Element. But you may find yourself in a different scenario, like when you have a building environment or when you are building a composite Web Component, as we will see in a future chapter. In these scenarios, probably you are using JavaScript modules, and you'd like to import a Web Component without having to explicitly add a script in the HTML page.

To better explain how to deal with these scenarios, let's consider the typical **Single Page Application (SPA)** scenario where almost all the UI is dynamically built by JavaScript code. In this context, usually, you have a single HTML page referring to a single JavaScript file having in charge of loading the rest of the application, possibly on demand.

To make this scenario more concrete, start a new project by cloning and initializing the Web Components Builder project we mentioned above. Now, replace the content of HTML page in the root folder with the following markup:

`<!DOCTYPE html>`

`<html>`

`<head>`

`<title>Web Components with Webpack Starter Kit</title>`

`<script src="./bundle.js"></script>`

`</head>`

`<body>`

`</body>`

`</html>`

As you can see, this is an empty HTML page with a single script reference to the `bundle.js` file. This bundle.js file will be the result of the building process applied to the content of the `src` folder.

Now, add to the `src` folder the `secureLink.js` file created in the previous section and containing the native custom element implementation. Finally, replace the content of the `index.js` file with the following code:

`import "./secureLink";`

`window.onload = function() {`

`const secureLink = document.createElement("a", {is:"secure-link"});`

`secureLink.setAttribute("href", "http://www.wikipedia.org");`

`secureLink.innerText = "Wikipedia";`

`document.body.appendChild(secureLink);`

`};`

Let's take a look at what this code is doing.

The first line imports our `secure-link` component. As you can see, it is a simple import with side effects. This means that by importing the `secureLink.js` file the entire code will be executed without explicitly binding any result to any variable or constant. So, after this line, we have the `secure-link` component registered and available without the need to add a `<script>` tag in the HTML page.

Then, you bind a listener to the onload event of the current window browser. This means that, when the HTML page is loaded in the window browser, that function will create an instance of our secure-link component, will configure it, and will append it to the body of the HTML page.

Let's focus a bit at how the secure-link component instance is created. The statement used in the example is the following:

`const secureLink = document.createElement("a", {is:"secure-link"});`

We used the typical `createElement()` method of the document object by specifying the tag name of the element we want to create. However, unlike the usual way, we dynamically create an HTML element; in this case, we added a second argument. This argument is an object specifying that the `<a>` element we want to create is customized by the secure-link definition. This allows us to get an instance of our Web Component.

**Some browsers allow you to specify a string as the second argument of the** `createElement()` **method. This is for backward compatibility with an older version of Custom Elements specifications.**

**This approach is deprecated so, please, use the object-based approach.**

Now, run your component by opening a terminal window, moving in the root of the project, and typing the `npm start` command. If you open your browser and point it to `http://localhost:8080`, you should see again the same result as before: a link to Wikipedia's home page that warns you about security when you click it.

# [Defining function-based Custom Elements](#toc.xhtml_s27a)

We defined our Custom Element by using the class syntax introduced by the ECMAScript 2015 specifications. As a JavaScript developer, you know that classes are syntactic sugar for constructor functions and prototypes. So, you may be wondering if you can use functions in order to define Custom Elements instead of the class-based syntax.

The answer is affirmative, but with a few caveats. The following code is the equivalent one for the `secure-link` element we defined before:

`function SecureLink() {`

`return Reflect.construct(HTMLAnchorElement, [], this.constructor);`

`}`

`SecureLink.prototype = Object.create(HTMLAnchorElement.prototype);`

`SecureLink.prototype.constructor = SecureLink;`

`Object.setPrototypeOf(SecureLink, HTMLAnchorElement);`

`SecureLink.prototype.connectedCallback = function() {`

`this.addEventListener("click", (e) => {`

`if (!this.href.startsWith("https")) {`

`if (!confirm("You are about to navigate to an unsafe site.` `Do you want to continue?")) {`

`e.preventDefault();`

`}`

`}`

`});`

`}`

`customElements.define("secure-link", SecureLink, {extends: "a"});`

As you can see, we define the `SecureLink()` function, assign to its prototype all that is needed to inherit from `HTMLAnchorElement` and attach the `connectedCallback()` method. The code is a bit more verbose than the class-based one. But this is not the only attention point. What you should notice is how the `SecureLink()` function defines its inheritance from `HTMLAnchorElement`:

`function SecureLink() {`

`return Reflect.construct(HTMLAnchorElement, [], this.constructor);`

`}`

Usually, you use the `apply()` method of the super class or parent object. In this case, you are using the `construct()` method of the `Reflect` object. This fact binds the definition of a Custom Element to ECMAScript 2015 features since the `Reflect` object has been introduced with that specifications. So, if you think to use the function-based approach to define your Custom Element in order to be compatible with older versions of JavaScript engines, you're wrong. You need a polyfill anyway, at least for the `Reflect` object.

**As a general suggestion, even if you can define your Custom Elements by using a function-based definition, this approach is discouraged in favor of the class-based syntax.**

# [Benefits of extending native elements](#toc.xhtml_s28a)

Creating Custom Elements by extending native elements should be the primary approach when you are creating your Web Components. In fact, this approach provides you with a few benefits:

*   **Compatibility with older browsers**: Browsers that don't support Web Component technologies can continue to access the basic features of your component. Consider, for example, the `secure-link` component we created in this chapter and its use in an HTML page:

    `<a is="secure-link" href="http://www.wikipedia.org">Wikipedia</a>`

    If a browser is not able to interpret the is attribute, it will be ignored. So, you will not have the security check on the link, but the component still continues to work, just a common link.

*   **Usability with disabled JavaScript**: Of course, you will get the same conservative behavior as in the previous point when the user has disabled JavaScript in their browser. You still continue to have a normal link without the extended features.
*   **Simple to code:** Extending a native element, usually, requires a few lines of code. You need to implement just the functionalities you want to add to the native element, but you will have its standard behavior for free. This is different from the implementation of Autonomous Custom Elements, as we will see in the following chapter.

In light of these benefits, when you are about to create your own Web Component, you should always ask yourself if it can be implemented as an extension of a native element. When possible, it should be the first option.

# [Conclusion](#toc.xhtml_s29a)

In this chapter, we started exploring the way we can build our own Web Components. We discussed the options to set up your development environment and presented a template project for the building-based approach. Then, we introduced Custom Elements and focussed on extending native HTML elements. We also discussed the ways you can use this component in your development environments and the benefits you have in customizing native HTML elements.

After reading this chapter, you are able to decide what is the development environment more suitable for creating your own Web Components. You are also able to customize native HTML elements and know how to name them correctly. In addition, you learned how to use your Web Component both in a development environment with and without a building process. Finally, you are now aware of the benefits that extending native HTML elements brings to you when you choose this approach to build your components.

In the next chapter, we will discuss when and how to create Autonomous Custom Elements, by also exploring some new features that are in common with the Customized Native Elements.

# [Questions](#toc.xhtml_s30a)

1.  What benefits the building process brings in a development environment?
2.  What are Custom Elements?
3.  What is the difference between Customized Native Elements and Autonomous Custom Elements?
4.  What is the role of the `customElements.define()` method?
5.  What are the restrictions on naming your Customized Native Element?
6.  How can you use your Customized Native Element in the markup of your HTML page?
7.  How can you make available your Customized Native Element in a development environment with the building process?
8.  What are the benefits of implementing your Web Components as Customized Native Elements?

# [CHAPTER 3](#toc.xhtml_c03)

# [Creating Custom Web Components](#toc.xhtml_c03)

In the previous chapter, we learned how to customize standard HTML elements. In this chapter, we will go a step further in order to create Web Components not strictly based on well-known HTML elements. This kind of Web Component, known as **autonomous custom elements,** will let you build completely new components whose behavior is left to your imagination. As usual, you will learn how to create this type of component by starting to build a specific autonomous custom element. In this chapter, you will set up the basics of the component, and we will complete it throughout the rest of the book.

# [Structure](#toc.xhtml_s31a)

*   Creating a Web Component from scratch
*   Basic techniques to add CSS and markup
*   The lifecycle of a Web Component
*   Using a custom Web Component

# [Objectives](#toc.xhtml_s32a)

This chapter will teach you what an **autonomous custom element** is and what is the difference with the **customized native elements.** You will learn how to set up a simple component and how to use some basic techniques to create its UI with markup and CSS. Also, you will learn some concepts about the lifecycle of Web Components and how to leverage them to handle the life of your component. You will learn at which steps of your component’s life you are allowed to make some operations and when you can’t. Finally, you will discover how you and other developers can use your component in their web page or in their web application.

# [Creating a Web Component from scratch](#toc.xhtml_s33a)

From the previous chapter, you already know how to build your own Web Component by extending a native HTML element. You learned how simple it is to change the behavior of an existing standard HTML element in order to adapt it to your needs.

However, not always the UI element you imagine for your web application or for your website can be obtained by simply extending a native HTML element. Even if we said that extending a native HTML element should be the first option when implementing your own Web Component, there are situations where the UI component you need doesn’t resemble any native HTML element or is a combination of native elements. In this case, you need to implement your autonomous custom element.

# [Introducing the cookie alert project](#toc.xhtml_s34a)

To better explain which are those cases where you may need to implement your Web Component as an autonomous custom element, you will build a concrete custom Web Component - a cookie alert Web Component.

This is one of those components that surely you have noticed while navigating on the Web. In fact, almost all websites show an alert, a banner, a pop-up window, or similar, informing you about their cookie management policy involving personal data. In some countries, this is required by law, but many websites provide them just for transparency.

Maybe most of those components are built by using one of the most common UI libraries, such as React, Vue, or Angular. So, they should be re-implemented for each website according to the UI library they are based on. On the contrary, we are going to build such a component as a Web Component, so that it can be used regardless of the UI library used to build the rest of the Web UI.

As explained in the previous chapter, you can use the *Web Component Builder* project as a template project to set up your development environment for the cookie alert Web Component. So, clone and initialize it on your machine.

**Remember that clone and initialize the Web Component Builder project means to use the git clone and npm install commands, as described in the previous chapter.**

# [A minimal autonomous custom element](#toc.xhtml_s35a)

Let’s start building our cookie alert component and learning about autonomous custom elements along the way. So, assuming you have initialized your Web Component project, open the `index.js` file in the `src` folder and replace its content with the following code:

`class CookieAlert extends HTMLElement {`

`constructor() {`

`super();`

`}`

`connectedCallback() {`

`this.innerText = "This website uses cookies to ensure you get the best experience";`

`}`

`}`

`customElements.define("cookie-alert", CookieAlert);`

As said in the previous chapter, an autonomous custom element is an element built from scratch. It doesn’t extend a standard well-known `HTML element`, but anyway, it is implemented as a class that extends `HTMLElement`. The HTMLElement class is the base class for any HTML element. It gives your component the ability to be added to the DOM and a little bit more that we will discover later.

As you can see, the `CookieAlert` class has a constructor that invokes the `super()` method of the base class. As per specifications, this is very important in order to make your custom element working properly. So, don’t forget to call it when implementing your autonomous custom elements.

You already know the `connectedCallback()` method. It is automatically called when an instance of this element is added to the DOM. In this case, a text will be assigned to the `innerText` property of the element. Of course, this is not yet the cookie alert we want to have, but just a very simple Web Component is showing the text I’m the cookie alert!

The last row adds our component in the custom elements registry. Unlikely the customized native element case, here we don’t need to specify the third parameter since we are not extending a native HTML element. Here we are simply telling the registry that the cookie-alert Web Component is implemented by the `CookieAlert` class.

The next step is using this simple component by changing the content of the `index.html` page. So, open the `index.html` file in the root folder of the project and replace its content with the following markup:

`<!DOCTYPE html>`

`<html>`

`<head>`

`<title>Web Components with Webpack Build System</title>`

`<script src="./wc-polyfills/webcomponents-loader.js"></script>`

`<script src="./bundle.js"></script>`

`</head>`

`<body>`

`<h1>Here is your Web Component</h1>`

`<cookie-alert></cookie-alert>`

`</body>`

`</html>`

As you can see, unlike the case of the customized native elements, here we are using the `cookie-alert` tag to specify our autonomous custom element. This is one of the relevant differences between the two types of custom elements.

**Remember that the name rules we saw for the customized native elements apply to autonomous custom elements as well.**

If you run the project by typing `npm start` in a terminal window and then point your browser to the `http://localhost:8080` address, you should see something similar to the following screenshot:

![](images/Figure_3.1.jpg)

**Figure 3.1**

You have your brand new basic autonomous custom element.

# [Basic techniques to add CSS and markup](#toc.xhtml_s36a)

The component you have created so far gives you a very basic idea about how to build an autonomous custom element. But, of course, this is not the component we planned to build. Since an autonomous custom element inherits from `HTMLElement`, it has nothing specific regarding its UI. We need to create its graphical appearance from scratch. In the component built so far, we simply showed a text by using the `innerText` property. To build our alert cookie component, we need to go further.

So, let’s start by changing the content of the `index.js` file in the `src` folder as shown in the following code:

`const styleMarkup = ‘`

`<style>`

`.container {`

`color: rgb(255, 255, 255);`

`background-color: rgb(35, 122, 252);`

`padding: 1em 1.8em;`

`width: 100%;`

`font-family: Helvetica,Calibri,Arial,sans-serif;`

`}`

`.footer {`

`position:fixed;`

`left:0px;`

`bottom:0px;`

`}`

`</style>‘;`

`const componentMarkup = ‘`

`<div class="container footer">`

`<span>This website uses cookies to ensure you get the best experience</span>`

`</div>‘;`

`class CookieAlert extends HTMLElement {`

`constructor() {`

`super();`

`}`

`connectedCallback() {`

`this.innerHTML = styleMarkup + componentMarkup;`

`}`

`}`

`customElements.define("cookie-alert", CookieAlert);`

We defined two constants - `styleMarkup` and `componentMarkup`. The first one is a string containing some CSS rules wrapped in a style element. The second one is a string with a div element using the CSS classes defined in the `styleMarkup` constant. Both strings are concatenated and assigned to the `innerHTML` property of our `CookieAlert` component. In simple words, we are building the UI of our component by using standard HTML and CSS and by attaching it to the `innerHTML` property of the generic HTML element.

If you run the project at this point of the implementation, you should see the following in your browser:

![](images/Figure_3.2.jpg)

**Figure 3.2**

As you can see, our component begins to take shape.

In the example shown so far, you used strings to define the UI of your Web Component. Of course, this is just one technique to define it. You can virtually use any possible technique to build the UI of your component. For example, you could use DOM APIs instead of strings to get the same result.

The following is an example of using the DOM APIs to build the component’s UI:

`const styleRules = ‘`

`.container {`

`color: rgb(255, 255, 255);`

`background-color: rgb(35, 122, 252);`

`padding: 1em 1.8em;`

`width: 100%;`

`font-family: Helvetica,Calibri,Arial,sans-serif;`

`}`

`.footer {`

`position:fixed;`

`left:0px;`

`bottom:0px;`

`}‘;`

`class CookieAlert extends HTMLElement {`

`constructor() {`

`super();`

`}`

`connectedCallback() {`

`this.createComponent();`

`}`

`createComponent() {`

`const style = document.createElement("style");`

`style.appendChild(document.createTextNode(styleRules));`

`this.appendChild(style);`

`const span = document.createElement("span");`

`span.innerText = "This website uses cookies to ensure you get the best experience";`

`const div = document.createElement("div");`

`div.classList.add("container", "footer");`

`div.appendChild(span);`

`this.appendChild(div);`

`}`

`}`

`customElements.define("cookie-alert", CookieAlert);`

Here, you just define the CSS rules as a string and build all the markup by using the `createComponent()` method. This method uses the methods `createElement(), appendChild(), createTextNode(),` and so on to dynamically generate the needed markup.

In this specific case, the result is the same as before. However, keep in mind that in some situations, a static string is not enough to define the component’s markup. You could need to dynamically generate the markup based on some parameters. In this case, using the DOM APIs may become necessary. We will see this in the following chapters.

**Here we presented two approaches to build the appearance of your Web Component - one based on markup represented by strings and one based on the use of the DOM APIs. Although both approaches worked fine in the example we provided, these approaches are not the best practice in building the UI of your component.**

**We will see a better approach in *[Chapter 7](#c07.xhtml)* when we will talk about HTML Templates.**

# [The lifecycle of a Web Component](#toc.xhtml_s37a)

While building our components, we defined the `connectedCallback()` method and said that this method is automatically called when our component is added to the DOM. This method belongs to a set of callbacks, also called **Custom element Reactions,** which are automatically called at certain stages of the life cycle of a component.

The following picture shows the possible stages that occur or may occur during the life of a custom element:

![](images/Figure_3.3.jpg)

**Figure 3.3**

Whenever the component is in one of these stages, the browser looks for a specific method in your Web Component and invokes it, if defined. These reactions allow you to appropriately define the behavior of your custom element.

Let’s take a look at the methods you can implement to capture each stage of the custom element life cycle.

# [The constructor](#toc.xhtml_s38a)

The constructor of the component is not properly a custom element reaction. It is the standard method that is defined to initialize any JavaScript object instance, not just HTML elements. As said before, having a constructor is mandatory for an autonomous custom element, and you would expect that it is called once in the life of the custom element. That’s actually true, but from a technical point of view, it may happen in two situations: when the custom element is created and when it is upgraded. Let’s explain both of the cases.

A custom element is created when it is completely defined, and then an instance of it is implicitly or explicitly built.

We say that a custom element is completely defined when you have defined the class implementing it, and you have associated a tag with it by using the `customElements.define()` method.

Once your custom element is completely defined, it can be implicitly created when the HTML parser finds the tag associated with your custom element in the page’s markup. For example, your cookie alert component is implicitly created when the HTML parser finds the `<cookie-alert></cookie-alert>` markup in the HTML page.

On the other side, the explicit creation happens when the component instance is created via JavaScript code, for example, by using the new operator, as in the following example:

`const cookieAlert = new CookieAlert();`

The explicit creation also happens when you create an instance of the custom element by using the `document.createElement()` method, shown as follows:

`const cookieAlert = document.createElement(“cookie-alert”);`

A custom element is upgraded when its registration through `customElements.define()` doesn’t take place just after its class definition. In other words, the order of the steps seen before for the creation case is not strictly observed.

Let’s explain with an example. Suppose you have defined the `CookieAlert` class for your cookie alert custom element, but you haven’t registered it with `customElements.define().`

Now, you could create an instance of your cookie alert as in the following example:

`const cookieAlert = document.createElement(“cookie-alert”);`

Since you haven’t yet registered the `cookie-alert tag`, an unknown HTML element will be created, that is an instance of the `HTMLUnknownElement` built-in class.

Then, you register the `cookie-alert tag` with the following statement:

`customElements.define("cookie-alert", CookieAlert);`

At this point, you are connecting an existing cookie-alert element to your custom element implemented by the `CookieAlert` class. The element has already been created, so your constructor will not be invoked at this time. It will be invoked when your component will be appended to the DOM. In this case, we will say that your custom element has been upgraded.

Upgrading a `custom element` is a pretty special situation, but it may happen, and you should be aware of what is going on in order to avoid undesired behaviors.

Actually, you can combine in different ways the steps that let you have an instance of your `custom element`. The following table summarizes these possible combinations:

| **Step 1** | **Step 2** | **Step 3** | **Step 4** | **State** |
| Class definition | Custom element registration | Instance creation | DOM attachment | created |
| Class definition | Instance creation | Custom element registration | DOM attachment | upgraded |
| Class definition | Instance creation | DOM attachment | Custom element registration | upgraded |
| Instance creation | Class definition | DOM attachment | Custom element registration | upgraded |
| Instance creation | DOM attachment | Class definition | Custom element registration | upgraded |

**Table 3.1**

As you can see, only a class definition followed by the tag registration guarantees that your custom element is created. In all other cases, your custom element will be upgraded.

Once established, when the constructor of your custom element will be called, let’s consider what you can do in this step of the life of your component. You can use this stage for initializing the custom element’s state, but the first statement of this method has to be a call to the `super()` method. Keep in mind that, in this stage, you cannot access the DOM, since the component is just created, but not appended to the model. This means that the document object is not available yet, and any attempt to add or manipulate DOM elements throws an error. For example, assume your component has the following code in its constructor:

`constructor() {`

`super();`

`this.appendChild(document.createElement("div"));`

`}`

When this code runs, you will get an error like the following, if you are using Chrome:

![](images/Figure_3.4.jpg)

**Figure 3.4**

Or like this one, if you are using Firefox:

![](images/Figure_3.5.jpg)

**Figure 3.5**

In other words, the constructor of your custom element is not the right place to make rendering operations.

# [The connectedCallback() reaction](#toc.xhtml_s39a)

The `connectedCallback()` method is invoked every time a component instance is added to the DOM. From this moment, you are sure that the DOM is available, and then you can manipulate elements, set attributes, initialize the graphical appearance of the component, and so on.

**Be aware that, although usually the** `connectedCallback()` **method is called only once in the component’s lifecycle, it may be called multiple times.**

One of the situations where the connectedCallback() method may be called multiple times is when the component is moved in the DOM. Consider, for example, the following code:

`const cookieAlert = new CookieAlert();`

`document.body.appendChild(cookieAlert);`

`const div = document.createElement("div");`

`document.body.appendChild(div);`

`div.appendChild(cookieAlert);`

This code creates an instance of the `CookieAlert` custom element and adds it to the body of the current document. Then, it creates a div element and appends it to the document’s body. Finally, it appends the previously created instance of your `CookieAlert` element to that div. In other words, your element has been moved from the body into the div.

This last step triggers a second call for the `connectedCallback()` method. Maybe in many situations, this has no impact on the behavior of your component, but you should be aware of it. In fact, it depends on the specific statements of the method itself. If your code performs tasks that must be executed only once, you should take into account the possibility that your code could be called multiple times.

Sometimes you may not have behavior issues when your custom element is moved around, but it may have performance issues. For example, if your `connectedCallback()` method performs heavy operations or fetches data from the network, they will be executed each time your component moves from one place to another in the document. Also, in these cases, you should avoid to execute them again and again.

Let’s take a look at the `connectedCallback()` method of the `CookieAlert` component:

`connectedCallback() {`

`this.createComponent();`

`}`

It simply calls the `createComponent()` method, which manipulates the DOM in order to attach the UI elements of the custom element. Just to remind, here is the code of the `createComponent()` method:

`createComponent() {`

`const style = document.createElement("style");`

`style.appendChild(document.createTextNode(styleRules));`

`this.appendChild(style);`

`const span = document.createElement("span");`

`span.innerText = "This website uses cookies to ensure you get the best experience";`

`const div = document.createElement("div");`

`div.classList.add("container", "footer");`

`div.appendChild(span);`

`this.appendChild(div);`

`}`

This code will be executed each time the `CookieAlert` component will be moved. From a behavior point of view, it has no impact: you will get the same component with the expected behavior. And maybe from the performance point of view, its impact is very low. But, anyway, it performs unnecessary work.

We can avoid doing this unnecessary work by checking if it has been already done, as shown in the following example:

`connectedCallback() {`

`if (!this.initialized) {`

`this.createComponent();`

`this.initialized = true;`

`}`

`}`

Here, you define the initialized property for the `CookieAlert` component and use it to know if the component’s UI has been built or not. The property is set to true only when the `createComponent()` method has been executed. This check guarantees that the UI will be built only once.

Even if it does not affect the component’s behavior nor its performance, you should also be aware that the `connectedCallback()` method is called when a custom element is upgraded. This means that when a custom element is upgraded, its constructor and the `connectedCallback()` method will be invoked one after the other.

# [The attributeChangedCallback() reaction](#toc.xhtml_s40a)

The `attributeChangedCallback()` method is executed when attributes associated with the component are added, removed, updated, or replaced. We will learn how to deal with attributes and properties in the next chapter. In that chapter, we also will explore in more detail how to use the `attributeChangedCallback()` method.

Here, you just need to be aware of this method and its general goal. Also, this method will receive three parameters that give you more information about what is going on:

*   The name of the attribute that has been affected
*   The old value of that attribute
*   The new value of that attribute

So, typically you will implement the `attributeChangedCallback()` method as follows:

`attributeChangedCallback(name, oldValue, newValue) {`

`…`

`}`

As said, we will go in more detail about using this reaction in the next chapter.

# [The adoptedCallback() reaction](#toc.xhtml_s41a)

You may need to implement the `adoptedCallback()` method when your custom element is adopted into a new document. The adoption of an element has a very specific use case. It happens when an element is moved from one document to another one through the `document.adoptNode()` method. This usually occurs when you are dealing with `iframe`, like in the following example:

`const iframe = document.querySelector(“iframe”);`

`const iframeFirstImage = iframe.contentDocument.querySelector(“img”);`

`const adoptedImage = document.adoptNode(iframeFirstImage);`

`document.body.appendChild(adoptedImage);`

This code gets the first image element of the first `iframe` in the current document and appends it to the body of this current document. Be aware that the original element is removed from the source document.

When your custom element is moved in this way, the `adoptedCallback()` method is invoked. Note that the element adoption doesn’t destroy and create the element again, so its constructor will not be called.

# [The disconnectedCallback() reaction](#toc.xhtml_s42a)

The `disconnectedCallback()` method is called when your custom element is removed from the DOM. You can define this method to perform operations before your element is no longer available on the current document. Typically, it is used to free up resources and to add cleanup logic, such as notify other components that the element is being removed from the DOM, stop timers, unsubscribe from DOM events or global application services, and so on.

These cleanup operations are useful to free system resources and prevent possible memory leaks, but, of course, they depend on the logic of your component.

**Keep in mind that disconnecting an element from the DOM does not mean that the element is destroyed.**

To clarify this concept, consider the following code:

`const cookieAlert = new CookieAlert();`

`document.body.appendChild(cookieAlert);`

`document.body.getElementByTagName(“cookie-alert”).remove();`

This code creates an instance of the `cookieAlert` custom element, add it to the DOM and then remove it from there. The last statement causes the system to search for and execute the `disconnectedCallback()` method. Notice that the `cookieAlert` instance has been removed from the DOM, but it has not been destroyed. In fact, you can append it again to the DOM with the following statement:

`document.body.appendChild(cookieAlert);`

Since your custom element may be disconnected and reconnected to the DOM many times during its life, you should be aware that the `disconnectedCallback()` method may be called multiple times.

Also, consider that usually the operations you perform on the `disconnectedCallback()` method depend on what you did when the `connectedCallback()` method was executed. Maybe, the most common scenario is the event listener subscriptions. We will go deeper with events in one of the next chapters, but you may guess that managing events is one of the most common activities for a UI element. Event handlers are usually registered when your component is connected to the DOM. They consume memory and continue to consume it even when the element that was listening no longer exists.

When your component is removed from the DOM, it is a good practice to remove the event listeners it subscribed to. The following code shows an example of how it can be done:

`disconnectedCallback() {`

`this.getElementById(“clickableItem”)`

`.removeEventListener(“click”, this.handleClick);`

`}`

As you can see here, the `removeEventListener()` method has been used to remove the registered event handler.

# [Using a custom Web Component](#toc.xhtml_s43a)

In previous sections, we have created the cookie alert custom element, and we have seen how to use it in an HTML page. Actually, using an autonomous custom element is quite easy. Once you have defined the class that implements it and have registered it with a tag name, you simply need to use that tag name inside the markup of an HTML page, like in the following:

`<!DOCTYPE html>`

`<html>`

`<head>`

`<title>Web Components with Webpack Build System</title>`

`<script src="./wc-polyfills/webcomponents-loader.js"></script>`

`<script src="./bundle.js"></script>`

`</head>`

`<body>`

`<h1>Here is your Web Component</h1>`

`<cookie-alert></cookie-alert>`

`</body>`

`</html>`

The interesting thing is that your custom element becomes indistinguishable from any other standard HTML element. Since your component is derived from `HTMLElement`, you can use the features that are common to all HTML elements without the need to write additional code. For example, you can use the hidden attribute as shown by the following markup:

`<cookie-alert hidden></cookie-alert>`

Your component will not be shown on the page like any other standard element having the hidden attribute. Also, you can attach an event listener, shown as follows:

`<cookie-alert onclick=”alert(‘You clicked!’)”></cookie-alert>`

When you click your component, an alert window will be shown with the message you passed, as you can see in the following picture:

![](images/Figure_3.6.jpg)

**Figure 3.6**

All common attributes of standard HTML elements are automatically available in your custom element. Here is a list of the most typical ones:

| **Attribute** | **Description** |
| `hidden` | It indicates if the element is hidden or not |
| `id` | The identifier of your element |
| `innerHTML` | It is the markup that represents the content within the element |
| `innerText` | It represents the text content of the element |
| `onblur` | This is the event handler for the blur event, that is when the element has lost the focus |
| `onfocus` | The event handler for the focus event, that is when the element has received the focus |
| `onclick` | It is the event handler of the click event |
| `onmousedown` | This is the event handler for the `mousedown` event, that is when the user depresses the mouse button |
| `onmouseover` | It is the event handler for the mouseover event, that is when the user moves the mouse pointer over the element |
| `onmouseup` | This is the event handler for the `mouseup` event, that is when the user releases the mouse button |
| `onresize` | It is the event handler for the resize event, that is when the current browser’s window has been resized |
| `style` | It represents the CSS declarations of an element’s inline-style |
| `title` | This is the text usually displayed as a tooltip popup when the mouse is over the element |

**Table 3.2**

You can use these attributes in the markup of your custom element, as seen above. But you can also use the corresponding properties in JavaScript, as you would do with standard HTML elements. For example, you can hide your cookie alert component by manipulating its hidden property via JavaScript.

**Remember that attributes and properties are not the same things. Attributes are part of the HTML markup, while properties are part of the object representation of the markup (DOM).**

**Usually, a mapping exists between attributes and DOM properties, but not always this happens.**

Let’s assume your component has assigned an identifier, like in the following example:

`<cookie-alert id=”myCookieAlert”></cookie-alert>`

You can hide this component with the following JavaScript code:

`window.onload = function() {`

`const cookieAlert = document.getElementById("myCookieAlert");`

`cookieAlert.hidden = true;`

`};`

As you can see, we just assigned the true value to the inherited `hidden` property. Of course, this has the same effect as assigning the hidden attribute in the HTML markup.

Similarly, you can add the handler for the click event via JavaScript with the following code:

`window.onload = function() {`

`const cookieAlert = document.getElementById("myCookieAlert");`

`cookieAlert.onclick = () => alert(“You clicked!”);`

`};`

In this case, we used the `onclick` property of your custom element, which is mapped to the `onclick` attribute. An alternative way is to use the `addEventListener()` method, as shown in the following example:

`window.onload = function() {`

`const cookieAlert = document.getElementById("myCookieAlert");`

`cookieAlert.addEventListener(“click”, () => alert(“You clicked!”));`

`};`

Besides the fact that using the `addEventListener()` method has the same effect as using the onclick property and attribute, it clearly teaches you that your custom element also inherits methods, not just attributes and properties.

The following are the most common methods your custom element inherits from `HTMLElement`:

| **Method** | **Description** |
| `addEventListener` | It registers an event handler to a specific event type on the element |
| `getAttribute` | It returns the value of an attribute of the element given its name |
| `getElementsByClassName` | This method returns a collection of all descendants of the element having the given CSS class |
| `getElementsByTagName` | It returns a collection of all descendants of the element having the given tag name |
| `querySelector` | This method returns the first element which matches the given selector string |
| `querySelectorAll` | It returns the list of elements which match the given selector string |
| `remove` | It removes the element from the DOM |
| `removeAttribute` | This method removes the given attribute from the element |
| `removeEventListener` | It removes an event listener from the element |
| `setAttribute` | It sets a value for the given attribute of the element |
| `toggleAttribute` | This method toggles a Boolean attribute, removing it if present and adding it if it is not present |

**Table 3.3**

Remember that you can use these attributes, properties, and methods just because your Custom element inherits from the HTMLElement.

# [Conclusion](#toc.xhtml_s44a)

This chapter gave you the basics to build `autonomous custom elements.` We built step by step, a simple Web Component that shows an alert message about the cookie policy of your website. During the building of this component, we explored the basic structure of an autonomous custom element and the basic techniques to add markup and CSS rules to it in order to define its UI. We analyzed the lifecycle of Web Components and discussed for each stage what you can do and what you can’t. Finally, we took a look at how you can use your Web Components in your web application both via markup and via JavaScript.

With the information you gathered in this chapter, you are able to create a simple autonomous custom element with its markup and CSS. Since you learned the various stages of the lifecycle of Web Components, you can select the right reaction to manage your component’s life as best as possible. Also, you know how to use your Web Component in your web pages and which features are available by default.

In the next chapter, we will continue to improve the Web Component you started to build in this chapter by adding support for custom properties and attributes.

# [Questions](#toc.xhtml_s45a)

1.  What is the difference in registering an autonomous custom element and a customized native element?
2.  What is a custom element reaction?
3.  What are the possible reactions for a Web Component?
4.  What is the difference between the creation and the upgrade of a component?
5.  Which is the best reaction to manipulate the DOM?
6.  When the `adoptedCallback()` reaction is invoked?
7.  When the `disconnectedCallback()` reaction is invoked?
8.  Why an autonomous custom element has some attributes, properties, and methods available even if you didn’t implement them?

# [CHAPTER 4](#toc.xhtml_c04)

# [Managing Properties and Attributes](#toc.xhtml_c04)

This chapter will discuss making a web component configurable through properties and attributes. You will learn the difference between a property and an attribute and how we can manage them by using the standard DOM API. Then, we will see how you can add properties to your web component and how to map their values to the corresponding attributes. Vice versa, you will also learn how to map attributes to properties and how to keep both in sync.

At the end of the chapter, we will discuss a few factors that may affect the performance and the effectiveness of your component.

# [Structure](#toc.xhtml_s46a)

*   Attributes and properties
*   Managing properties
*   Syncing attributes and properties
*   Caveats and suggestions

# [Objectives](#toc.xhtml_s47a)

This chapter will provide you with a clear understanding of properties and attributes. You will learn how to enrich your web components by adding support for properties and attributes so that the user can customize it. You will also learn the best practice you should adopt to make your web component similar to standard HTML elements and avoid possible performance pitfalls.

# [Attributes and properties](#toc.xhtml_s48a)

In the previous chapter, we started to build up a web component that informs the user about the cookie management policy applied by the current website - the cookie alert. So far, the implementation simply shows a default text wired into the JavaScript code of the web component. Of course, this is not the ideal approach for a real-world component. We’d like to let the developer that uses our web component specify the text they want to show. In other words, we want the user to be able to customize our web component. Typically, an HTML element can be customized by assigning specific values to its attributes, in the markup of the page, or to its properties, in JavaScript code.

We are going to implement in our cookie alert this standard way to customize HTML elements. But before going to the actual implementation, we need to clarify what attributes and properties are and what the difference is between them.

As a front-end developer, you know how the browser works to interpret HTML and build up the DOM. In a few words, when it loads a page, it parses the HTML markup and generates DOM objects from the HTML elements found in it. Typically, each HTML element becomes a DOM object in the DOM’s hierarchy, and each attribute of the HTML element becomes a property of the DOM object. Even if this is the general scenario, this mapping is not strictly one-to-one.

Let’s see the main differences between HTML attributes and DOM object properties.

# [HTML attributes](#toc.xhtml_s49a)

As said, when the browser parses an HTML element, it builds a corresponding DOM object. It also analyzes the element’s attributes to assign their values to the corresponding DOM object’s properties. Of course, the browser can identify standard attributes in the HTML element, and in this case, it knows how to deal with it and how to assign its value to the corresponding object property. So, for example, consider the following markup:

`<p id=”myPar”>This is a paragraph</p>`

The browser will generate an `HTMLParagraphElement` object and will assign the value `myPar` to its id property. It knows that the `HTMLParagraphElement` object has an `id` property that corresponds to the id HTML attribute, and it can map the latter to the former.

Note that HTML elements don’t share the same standard attributes. For example, the `<input>` element has the `type` attribute, while the `<div>` element don’t. So, the mapping between attributes and properties has to be done on an element by element basis. This means that if you add a non-standard attribute to an HTML element, this will not generate a corresponding property on the DOM object. To better explain, you can write the following markup:

`<p id=”myPar” type=”special”>This is a paragraph</p>`

But you will not get a type property for the `HTMLParagraphElement` object. Anyway, you can still access HTML attributes via the DOM APIs. In fact, each DOM object has the following methods that allow you to work with attributes:

| **Method** | **Description** |
| `hasAttribute()` | Check the existence of an attribute |
| `getAttribute()` | Get the value of an attribute |
| `setAttribute()` | Set the value of an attribute |
| `removeAttribute()` | Remove the attribute from the HTML element |

**Table 4.1**

For example, you can access the non-standard attribute type of the paragraph described in the markup above with the following code:

`const myPar = document.getElementById(“myPar”);`

`if (myPar.hasAttribute(“type”)) {`

`console.log(myPar.getAttribute(“type”));`

`}`

This code checks if the `type` attribute exists and displays its value on the console.

You also have the `attributes` property containing the list of all the attributes for the HTML element. Each element in the list is an object representing the attribute. You can reproduce the same behavior of the previous snippet of code by using the attributes property as follows:

`const myPar = document.getElementById(“myPar”);`

`const typeAttribute = myPar.attributes.getNamedItem(“type”);`

`if (typeAttribute) {`

`console.log(typeAttribute.value);`

`}`

In this case, you get the object representing the attribute through the `getNamedItem()` method of the attributes collection. Then, you access the attribute’s value through its value property.

We will be back on non-standard attributes and some caveats about them in a bit.

**The** `attributes` **collection contains both standard and non-standard attributes.**

To conclude this overview of HTML element attributes, you should pay attention to two important features:

*   Attributes’ name are not case sensitive
*   Attributes’ value is always strings

This means, for example, that the following markups are equivalent:

`<p id=”myPar”>This is a paragraph</p>`

`<p ID=”myPar”>This is a paragraph</p>`

`<p Id=”myPar”>This is a paragraph</p>`

Also, you can retrieve an attribute’s value via JavaScript in the following equivalent ways:

`const typeAttribute = myPar.attributes.getNamedItem(“type”);`

`const typeAttribute = myPar.attributes.getNamedItem(“Type”);`

`const typeAttribute = myPar.attributes.getNamedItem(“TYPE”);`

In addition, whatever is the way you get or set a value for an attribute, it will be a string. Consider the following example:

`const typeAttribute = myPar.attributes.getNamedItem(“type”);`

`console.log(typeAttribute.value + 1);`

The output you will get on the console will be the concatenation of the attribute’s value and the string 1\. If the value of the `type` attribute is a numeric string, it is your responsibility to convert it into a number. The same is true when you assign values to an attribute, as in the following code:

`const myPar = document.getElementById(“myPar”);`

`myPar.setAttribute(“type”, 123);`

Even if you are assigning a numeric value, it will be converted into a string.

# [DOM properties](#toc.xhtml_s50a)

As said before, an HTML element is internally represented with a DOM object. Typically, any standard attribute of the HTML element has a corresponding property in this object, while non-standard attributes are available via generic methods or the attributes collection, as we’ve seen before.

DOM objects are regular JavaScript objects, so we can deal with them as with any other object. So, for example, we can assign values to its properties or add new properties and methods. The following code shows how you can add a new property and a new method to an `HTMLParagraphElement` object:

`const myPar = document.getElementById(“myPar”);`

`myPar.myProperty = “This is a new property!”;`

`myPar.getContent = () => myPar.innerHTML;`

Adding a new property to the DOM object does not affect HTML, but it can be useful for making customizations via JavaScript. For example, we could assign text or numeric information to an image to be retrieved later.

**Consider that, even if it is technically possible, adding new properties to a DOM object might not be a good idea. The new property could clash with the possible evolution of the standard DOM.**

Unlike HTML attributes, DOM properties are case sensitive. This means that the name of the DOM property will always be the same independently from the case of the corresponding attribute. In other words, if your markup is like the following:

`<p ID=”myPar”>This is a paragraph</p>`

The corresponding DOM property will still be id.

Again, unlike HTML attributes, DOM properties are typed. For example, consider the following markup:

`<p ID=”myPar” hidden style=”color:red”>This is a paragraph</p>`

The `hidden` property corresponding to the `hidden` attribute has a Boolean value. The `style` property is an object, instead.

Usually, when the type of a DOM property is a string, the attribute’s value is assigned to the property as-is. However, there are some exceptions. For example, the value of the `href` property of the `HTMLAnchorElement` is always an absolute URL, even if the corresponding attribute’s value is a relative one. This also happens for the src attribute of the `<img>` HTML element and the `src` property of the `HTMLImageElement`.

# [Non-standard attributes management](#toc.xhtml_s51a)

We talked about non-standard attributes and how you can manage them via a few methods like `getAttribute(), setAttribute()`, and similar or by using the attributes collection.

In general, creating non-standard attributes might not be a good idea. Or, at least, it is not a good idea if you create them without thinking of the consequences of their introduction in your application. For example, you could add a non-standard attribute to an HTML element, but what happens if later it becomes standard? You could get unexpected results if you freely assign attribute names.

Even if technically, you can add attributes by choosing the name you want, you should use the so-called data attributes. These are attributes whose name starts with data-prefix. The HTML standard introduced them just for this purpose - allowing developers to add custom attributes.

For example, you can add a non-standard attribute to the paragraph element in a more secure way as follows:

`<p id=”myPar” data-type=”special”>This is a paragraph</p>`

Any data attribute is mapped to the `dataset` property of the corresponding DOM object. So, you can retrieve the value of the `data-type` attribute, as shown in the following code snippet:

`const myPar = document.getElementById(“myPar”);`

`console.log(myPar.dataset.type);`

As you can see, in this case, the `data-type` attribute generates the `dataset.type` property.

# [Attributes and properties synchronization](#toc.xhtml_s52a)

In most cases, when the value of a standard attribute changes, the value of the corresponding DOM property changes accordingly, and vice versa. This guarantees that standard attributes and properties are automatically kept in sync.

However, there are some exceptions to this rule. Consider the following example:

`<input id="myName" type="text" value="John" />`

Initially, the value attribute and the corresponding property of the `HTMLInputElement` object have the same value. But if the user changes the value of the text box, we will have different values between the property and the attribute. In particular, the value property of `HTMLInputElement` object will get the new value inserted by the user, while the attribute will continue to have the initial value. The reason for this behavior is simple - this way we allow the user to restore the original value when they hit the **`Reset`** button in a form. So, it’s just a practical reason.

# [Managing properties](#toc.xhtml_s53a)

The overview provided so far helps us to reason about the standard behavior of attributes and properties. If we want to provide attributes and properties to our web components, we need to have a clear understanding of how they work in the standard browser behavior. This allows us to create attributes and properties that work as close as possible to the standard elements so that users can figure out their behavior.

# [Adding properties](#toc.xhtml_s54a)

Let’s start changing our cookie alert component by adding a property that allows the user to specify their `message`. We are going to add a message property to our custom element, and this is no more than adding a property to any standard JavaScript class. So, let’s recall the code for the `CookieAlert` class we have defined so far:

`const styleRules = ‘`

`.container {`

`color: rgb(255, 255, 255);`

`background-color: rgb(35, 122, 252);`

`padding: 1em 1.8em;`

`width: 100%;`

`font-family: Helvetica,Calibri,Arial,sans-serif;`

`}`

`.footer {`

`position:fixed;`

`left:0px;`

`bottom:0px;`

`}`

`‘;`

`class CookieAlert extends HTMLElement {`

`constructor() {`

`super();`

`}`

`connectedCallback() {`

`this.createComponent();`

`}`

`createComponent() {`

`const style = document.createElement("style");`

`style.appendChild(document.createTextNode(styleRules));`

`this.appendChild(style);`

`const span = document.createElement("span");`

`span.innerText = "This website uses cookies to ensure you get the best experience";`

`const div = document.createElement("div");`

`div.classList.add("container", "footer");`

`div.appendChild(span);`

`this.appendChild(div);`

`}`

`}`

`customElements.define("cookie-alert", CookieAlert);`

As a first step to add a property, let’s assign a default value to the `_message` property in the class constructor as shown by the following code:

`constructor() {`

`super();`

`this._message = "This website uses cookies to ensure you get the best experience";`

`}`

Now, let’s use the `_message` property to assign the default message when we are building the UI in the `createComponent()` method:

`createComponent() {`

`const style = document.createElement("style");`

`style.appendChild(document.createTextNode(styleRules));`

`this.appendChild(style);`

`const span = document.createElement("span");`

`span.innerText = this._message;`

`const div = document.createElement("div");`

`div.classList.add("container", "footer");`

`div.appendChild(span);`

`this.appendChild(div);`

`}`

`}`

These changes don’t affect the current behavior of the cookie alert component. The `_message` property acts as a storage for the message to be shown. It is not meant to be the actual property for our component, but it should be private property. We are using the well-known convention that relies on naming properties with the _ prefix for those properties that should be considered as private.

**At the time of writing, actual private properties are an experimental feature proposed at the ECMAScript committee. Support in browsers is limited, but some transpilers can be configured to use them.**

**In the rest of the book, we will continue to use the naming convention based on the _ prefix for private properties.**

To define the actual property, let’s add the following code to the class:

`get message() {`

`return this._message;`

`}`

`set message(value) {`

`this._message = value;`

`}`

This code adds a getter and a setter for the `message` property. The getter returns the current value of the private _message property, while the setter assigns to it the value received in the parameter.

While the getter could fulfil the needs for the `message` property, the setter doesn’t. We would like that when the setter receives the value for the `message`, the UI updates with this new message. So, let’s apply some changes to the setter of the message property and add a new method, as shown in the following code snippet:

`get message() {`

`return this._message;`

`}`

`set message(value) {`

`this._message = value;`

`this.updateMessage();`

`}`

`updateMessage() {`

`this.querySelector("span").innerText = this._message;`

`}`

As you can see, here we added the `updateMessage()` method, which assigns the new value of the private `_message` property to the UI, and called it from the setter. Actually, we could use the `updateMessage()` method also from inside the `createComponent()` method, for improving our code. So, after a bit of refactoring, the class `CookieAlert` looks as follows:

`const styleRules = ‘`

`.container {`

`color: rgb(255, 255, 255);`

`background-color: rgb(35, 122, 252);`

`padding: 1em 1.8em;`

`width: 100%;`

`font-family: Helvetica,Calibri,Arial,sans-serif;`

`}`

`.footer {`

`position:fixed;`

`left:0px;`

`bottom:0px;`

`}`

`‘;`

`class CookieAlert extends HTMLElement {`

`constructor() {`

`super();`

`this._message = "This website uses cookies to ensure you get the best experience";`

`}`

`connectedCallback() {`

`this.createComponent();`

`}`

`get message() {`

`return this._message;`

`}`

`set message(value) {`

`this._message = value;`

`this.updateMessage();`

`}`

`createComponent() {`

`const style = document.createElement("style");`

`style.appendChild(document.createTextNode(styleRules));`

`this.appendChild(style);`

`const span = document.createElement("span");`

`const div = document.createElement("div");`

`div.classList.add("container", "footer");`

`div.appendChild(span);`

`this.appendChild(div);`

`this.updateMessage();`

`}`

`updateMessage() {`

`this.querySelector("span").innerText = this._message;`

`}`

`}`

`customElements.define("cookie-alert", CookieAlert);`

Now, our component has a `message` property that allows the user to assign their custom text via JavaScript. This means that now we can put our cookie alert component in an HTML page as in the following example:

`<cookie-alert id="myAlert"></cookie-alert>`

And on the same page we can add a script setting a customized text via JavaScript like the following code shows:

`window.onload = function() {`

`const myAlert = document.getElementById("myAlert");`

`myAlert.message = "We use cookies, but respect your privacy!";`

`};`

This text will appear instead of the default one, as shown in the following screenshot:

![](images/Figure_4.1.jpg)

**Figure 4.1**

# [Syncing attributes and properties](#toc.xhtml_s55a)

So far, we have a way to customize our cookie alert component by handling properties via JavaScript. Of course, we would like to customize our component using attributes as well, as any HTML component allows us to do. Even if in standard HTML elements, we have most properties and attributes mapped each other, this is not for free for Web Components. In this section, we will see how to enable attribute-based customization and how to keep in sync attributes and properties.

# [Properties to attributes](#toc.xhtml_s56a)

Mapping properties to the corresponding attributes is quite easy. We should just assign the value of a property to the attribute whenever it changes. And we can do it by applying a little change to the property setter’s code.

The following code shows how to map the value of the `message` property to the `message` attribute:

`set message(value) {`

`this._message = value;`

`this.setAttribute("message", value);`

`this.updateMessage();`

`}`

As you can see, we used the `setAttribute()` method of the web component itself to apply this mapping. Remember that whatever is the type of the value variable, it will be converted into a string.

# [Attributes to properties](#toc.xhtml_s57a)

Now we know a way to map to the attributes the values you are assigning to the properties. This is great, but the more interesting part is the mapping from the attributes to the properties of a web component. This allows the user to set values from the markup, and sometimes it is more easy and convenient.

Mapping an attribute to a property is a little trickier. It requires some kind of notification from the browser when the value of an attribute changes. Remember that HTML is under the direct control of the browser. It parses the markup and provides us with a representation of it through the DOM. So, if something happens at the markup level, the browser should process this change and provide us with some new information.

That said, you need to be informed when a value of an attribute changes. So, as a first step, declare which attributes you want to monitor by adding the static getter `observedAttributes()` to the web component class, as shown in the following code snippet:

`static get observedAttributes() {`

`return ["message"];`

`}`

This getter returns an array with the attribute names the component wants to observe. In our case, just the message attribute. The `observedAttributes` property provides the browser with the list of attributes we are interested in receiving notifications when the value of any of the changes.

After this preliminary step, you need to capture notifications sent by the browser when the value of any observed attribute changes. For this goal, you need to implement the `attributeChangedCallback()` method. As you remember from the previous chapter, this is one of the reactions of a web component’s lifecycle. It will be invoked when a change occurs to any of the observed attributes. The following is the implementation of this method for the cookie alert component:

`attributeChangedCallback(name, oldValue, newValue) {`

`if (oldValue !== newValue) {`

`if (name === "message") {`

`this._message = newValue;`

`this.updateMessage();`

`}`

`}`

`}`

This code will change the `internal _message` property and will show the new value through the `updateMessage()` method.

These changes allow you to set your custom `message` using the message attribute of the `<cookie-alert>` element, without any JavaScript code, as shown by the following example:

`<cookie-alert message="We use cookies, but respect your privacy!”></cookie-alert>`

The resulting visual effect will be the same as before, but now we have a web component that is almost indistinguishable from a standard HTML element.

# [Caveats and suggestions](#toc.xhtml_s58a)

In the example reported above, we implemented a synchronization between properties and attributes and vice versa. This is usually the most common scenario since the user expects that each change in an attribute and properties reflects on each other automatically.

However, keep in mind that this could not always be the best practice. For example, if a property is intended to be frequently updated via JavaScript, for example, through a loop, you shouldn’t map its value to the corresponding attribute. Reflecting the update to the attribute is expensive, so if you have to do this frequently, your web component could become unresponsive. In some situations, you could even choose to not provide an attribute for a given property.

As said, attributes accept only strings. You cannot pass any other data type. The responsibility to convert that string into the type of the corresponding property is on the getter and setter methods. Of course, you cannot assign rich data, such as objects and arrays, to an attribute as well. If you want to allow rich data assignment for your web component, you should accept such data through methods or properties.

You may be tempted to accept rich data via attributes represented as serialized objects. Or also, you could think of mapping rich data from your properties to the corresponding attributes by serializing it. This approach has a few flaws. The most evident drawback is that serializing and de-serializing objects to sync properties and attributes can be very expensive for large objects. Also, during serialization, you will lose any object reference you may have in your object. In other words, as a best practice, you should allow rich data only for properties or accept them as parameters for a method. Never accept or map rich data in the attributes of your web component.

# [Conclusion](#toc.xhtml_s59a)

In this chapter, we recalled the difference between attributes and properties and how they work for standard HTML elements. With these notions in mind, we explored how to replicate this standard behavior for Web Components. We discovered how to add properties to web components, how to use them via JavaScript, how to map properties to attributes, and how to keep both in sync. Finally, we discussed a few factors that may affect the performance of your web component.

With the ability to add and manage attributes and properties in your web component, you can create custom elements that resemble almost completely to standard HTML elements. The users of your web components can now customize them both via attributes and properties.

In the next chapter, we will explore another way to allow users to customize your web component. We will discuss event management and will see how to include this common feature in your web components.

# [Questions](#toc.xhtml_s60a)

1.  What is the difference between the properties and attributes of a standard HTML element?
2.  What are the possible data types of attributes?
3.  What are the possible data types of properties?
4.  What happens if you add an unknown attribute to a standard HTML element?
5.  What is the best way to add non-standard attributes to an HTML element?
6.  Does the attributes collection of an HTML element contain only standard attributes?
7.  Which DOM method do you use to map the value of a property to the corresponding attribute?
8.  Which custom element reaction can you use to catch changes to attributes?
9.  How do you request the browser to be notified about changes in an attribute’s value?
10.  If the data type of your property is not a string, who is responsible for converting the value coming from the corresponding attribute?
11.  Why should you not assign rich data to an attribute?

# [CHAPTER 5](#toc.xhtml_c05)

# [Handling Events](#toc.xhtml_c05)

Events are an important part of UI development. They allow you to manage the user interaction with your application and to react to specific system behaviors. Let's explore in this chapter how to enable a web component to listen to events, to handle them, and to create custom events. After a brief recap about DOM event management, you will learn how to integrate your web components with standard event listening. You will also discover how to deal with event propagation and how to generate custom events without and with event data. Finally, you will see how to implement one of the best practices by removing all registered event listeners to achieve better system resource management.

As usual, throughout the chapter, we will actuate these new concepts by enriching our cookie alert component to handle and generate events.

# [Structure](#toc.xhtml_s61a)

*   Event management basics
*   Listening to standard events
*   Creating custom events
*   Removing event listeners

# [Objectives](#toc.xhtml_s62a)

After reading this chapter, you will be able to create web components able to listening standard events occurring on it as a whole or occurring on any of the HTML standard elements of its UI. You will also learn how to make your components to generate custom events that resemble as much as possible to standard events.

# [Event management basics](#toc.xhtml_s63a)

Event management is very important in any interactive application. As a JavaScript developer, you know how to deal with events. Anyway, before going into event management for web components, let's recap in this section a few notions about events, just be on the same page.

Events allow us to define the behavior of our application when the user interacts with it or when something happens inside the system, basically the DOM, or the application itself. To intercept events, we usually use a handler or listener, which is a function associated with a specific event.

You have three ways to associate a handler with an event:

*   Using the `addEventListener()` method in your JavaScript code
*   Using specific attributes in the HTML markup
*   Using specific properties of the HTML element

Using attributes and properties to assign event handlers to an HTML element is quite straightforward and handy. However, the `addEventListener()` method provides you with a more advanced way to manage events. For example, it allows you to add multiple handlers to the same event. It also allows you to control how the handler fits in the event propagation flow, as we will see in a moment.

When an event triggers, an object containing some details about the event itself is passed to the handler. You can use this object in your handler, as shown in the following example:

`const button = document.getElementById("myButton");`

`button.addEventListener("click", (event) => {`

`console.log(‘You clicked the button “${event.target.innerHTML}”‘);`

`});`

In this example, we used the target property of the event object. It represents the HTML element the event fired on. We used the `innerHTML` property of this HTML element to show the text of the clicked button on the browser's console.

When an event occurs, it goes through the DOM following a specific path. This path is known as **event propagation** flow and takes place in three phases:

*   **Capture phase**: In this phase, the event propagates from the root of the DOM to the actual target element.
*   **Target phase:** In this phase, the event reaches the target element.
*   **Bubbling phase:** This is the phase in which the event goes up the DOM tree starting from the target element until it reaches the root again; so, it passes through the same nodes crossed in the capture phase.

The following picture from the W3C specifications shows the event propagation in these three phases:

![](images/5-1.jpg)

**Figure 5.1**

During the three phases, the event object associated with the event is passed on to any handlers encountered along the way. Normally, in the capturing phase, handlers ignore the event and let it flow to the target element. Once the target element is reached, its handler code is executed. In the next bubbling phase, the event handlers are executed as you go towards the root of the DOM.

Understanding this flow helps to prevent strange behaviors and to detect possible issues while managing events.

If you want, for some reason, your handler is executed in the capture phase of the event propagation, you can leverage a third parameter of the `addEventListener()` method. The following example shows how to do this:

`const button = document.getElementById("myButton");`

`const handler = (event) => {`

`console.log(‘You clicked the button “${event.target.innerHTML}”‘);`

`};`

`button.addEventListener("click", handler, true);`

The third parameter of the `addEventListener()` method is a `Boolean` that specifies if the handler must be executed during the capture phase. Its default value is `false` and prevents the handler from being executed during the capture phase.

While handling an event, we have the opportunity to alter the event flow. For example, we can decide to stop the event flow by using the `stopPropagation()` method of the event object. It is an example of how we can use this method:

`const button = document.getElementById("myButton");`

`button.addEventListener("click", (event) => {`

`event.stopPropagation();`

`console.log(‘The event stops at button “${event.target.innerHTML}”‘);`

`});`

You can get the same effect by assigning a Boolean value to the cancelBubble property of the `event` object, as shown in the following code snippet:

`const button = document.getElementById("myButton");`

`button.addEventListener("click", (event) => {`

`event.cancelBubble = true;`

`console.log(‘The event stops at button “${event.target.innerHTML}”‘);`

`});`

With this summary about the DOM event management, let's explore how it fits in the Web Components context.

# [Listening to standard events](#toc.xhtml_s64a)

Let's see how to let a web component handling a standard event, that is, a typical DOM event that may occur to a standard HTML element. With this goal in mind, we want to enrich our cookie alert component by adding a **`Close`** button. This button allows the user to hide the banner at the bottom of the current web page. When the user clicks the button, the cookie alert will disappear.

Let’s see the HTML markup of the page containing the `<cookie-alert> element:`

`<!DOCTYPE html>`

`<html>`

`<head>`

`<title>Web Components with Webpack Build System</title>`

`<script src="./wc-polyfills/webcomponents-loader.js"></script>`

`<script src="./bundle.js"></script>`

`</head>`

`<body>`

`<h1>Here is your Web Component</h1>`

`<cookie-alert message="We use cookies, but respect your privacy!"></cookie-alert>`

`</body>`

`</html>`

It is the same markup we used in the previous chapter when we introduced attributes and properties management.

Now, let’s edit the `index.js` file in order to apply some changes to the code contained in it. As a first step, let’s add a new CSS rule to format our new button. The `styleRules` constant will look like the following:

`const styleRules = ‘`

`.container {`

`color: rgb(255, 255, 255);`

`background-color: rgb(35, 122, 252);`

`padding: 1em 1.8em;`

`width: 100%;`

`font-family: Helvetica,Calibri,Arial,sans-serif;`

`}`

`.footer {`

`position:fixed;`

`left:0px;`

`bottom:0px;`

`}`

`.button {`

`color: rgb(255, 255, 255);`

`background-color: transparen`

`border-color: rgb(255, 255, 255);`

`padding: 5px 40px;`

`margin-right: 50px;`

`cursor: pointer;`

`float:righ`

`}`

`‘;`

As you can see, we simply added a `button` CSS class defining some graphic properties.

Now, let’s add the actual button to the web component markup. So, we change the `createComponent()` method as follows:

`createComponent() {`

`const style = document.createElement("style");`

`style.appendChild(document.createTextNode(styleRules));`

`this.appendChild(style);`

`const span = document.createElement("span");`

`const div = document.createElement("div");`

`div.classList.add("container", "footer");`

`div.appendChild(span);`

`const closeButton = document.createElement("button");`

`closeButton.classList.add("button");`

`closeButton.innerText = "Close";`

`closeButton.addEventListener("click", ()=>{`

`this.style.visibility = "hidden";`

`});`

`div.appendChild(closeButton);`

`this.appendChild(div);`

`this.updateMessage();`

`}`

We added a few statements that create an `<button>` HTML element, assign the `button` class and the `close text` to it, attach an event listener, and append the `button` to the container `<div>.`

For our goal, the relevant part of these statements is the event listener attachment. As you can see, we used the standard addEventListener() method of the button to assign a listener for the click event, just like you do for any standard HTML element. This specific listener simply hides the entire web component by changing the value of its visibility property.

If we run our project, we will see the following page:

![](images/Figure_5.2.jpg)

**Figure 5.2**

As you can see, now we have a **`Close`** button on the right of the cookie alert. If you click it, the banner will disappear as expected.

So, you now know how to listen to and handle standard events that may occur on the various elements your web component is composed of.

Consider that your web component itself as a whole may listen to standard events. Remember that it inherits from `HTMLElement`. So, you can listen to any events that may occur on the whole surface of the component, not just on a single element that composes it.

For example, you could implement a visual effect that changes the background color of the banner when the user’s mouse pointer is over the component’s area. In order to enable this effect, let’s add a few statements to the `createComponent()` method. The new version of the method will look like the following:

`createComponent() {`

`const style = document.createElement("style");`

`style.appendChild(document.createTextNode(styleRules));`

`this.appendChild(style);`

`const span = document.createElement("span");`

`const div = document.createElement("div");`

`div.classList.add("container", "footer");`

`div.appendChild(span);`

`const closeButton = document.createElement("button");`

`closeButton.classList.add("button");`

`closeButton.innerText = "Close";`

`closeButton.addEventListener("click", ()=>{`

`this.style.visibility = "hidden";`

`});`

`div.appendChild(closeButton);`

`this.appendChild(div);`

`this.addEventListener("mouseover", ()=> {`

`div.style.backgroundColor = "rgb(35, 122, 152)";`

`});`

`this.addEventListener("mouseout", ()=> {`

`div.style.backgroundColor = "";`

`});`

`this.updateMessage();`

`}`

The two new statements we added to the code of the `createComponent()` method use the `this` keyword to add two event listeners directly to the web component. The first event listener catches the `mouseover` event, while the second one handles the `mouseout` event. In the former case, we change the background color of the container `<div>.` In the latter case, we reset this background color to the default one defined in the container CSS class.

# [Event propagation](#toc.xhtml_s65a)

The event management we explained in the previous section shows us how we, as the web component developers, can catch a standard event and handle it. But what happens if the user specifies their event handler on our web component? Say, for example, that the user adds a handler to the `onclick` attribute like in the following markup:

`<cookie-alert`

`message="We use cookies, but respect your privacy!"`

`onclick="alert('You clicked!')">`

`</cookie-alert>`

Of course, the user can do it. Since the cookie alert inherits from `HTMLElement`, it also inherits standard event hooks like `onclick`. So, when the user clicks on any part of the banner, the alert will be shown.

Notice that the user's alert will be shown even when they click the **`Close`** button. This happens because of the event propagation flow. Once the click event reaches the target element, that is the close button; it enters in the bubbling phase. In this phase, the event passes through all the button's parents until the user's `onclick` handler is reached and executed.

Maybe you are wondering if there is a way to prevent the user from adding handlers to the standard events. Before trying to find a solution to it, try to ask yourself if you want this. Do you want to prevent users from attaching their event handlers? After all, any standard element allows you to attach standard event handlers. Why should your component work differently?

Anyway, if you want to prevent the user from adding their event handler, or better, to ignore them, you should add a special event listener to your web component as soon as it is created. In other words, for our click event example, you should modify your component's constructor as follows:

`constructor() {`

`super();`

`this._message = "This website uses cookies to ensure you get the best experience";`

`this.addEventListener("click", (e) => {`

`e.stopImmediatePropagation();`

`});`

`}`

The click event handler we are adding stops the event propagation just before the event itself is passed to the user's handler during the bubbling phase. So, in practice, this avoids the user's click handler executes.

# [Creating custom events](#toc.xhtml_s66a)

So far, we learned how to capture events firing on the elements that build our component and how to handle them. In this case, we are reacting to events generated by the user or the system by applying our logic, the logic that describes the internal behavior of our web component. Usually, an event is also a customization point for a component, a way to allow the user to define their reaction to something that happened to your component. This is why HTML elements provide us with events: they enable us to decide how to react when an event occurs. For example, the click event occurring on a button allows us to decide what to do. How can we provide a similar behavior when building our web components?

From one point of view, we already have a way to allow the user to attach event handlers to our web component. Since our component inherits from the `HTMLElement` class, all standard events occur to our component, and the user can leverage the standard ways to handle them - the `onclick, onblur, etc.` attributes and properties, and the `addEventListener()` method. By the way, this is just the behavior we wanted to prevent in the previous section.

So, for standard events on the whole web component, we don't need to do anything special. The event management system works by default. But we could fire events specific to our web component. For example, we could provide different events when the user clicks on the cookie alert's message or when they click on the **`Close`** button. Or we can have a new **`Accept`** button in the cookie alert component and generate a specific event informing that the user accepted our cookie policy.

In the rest of this section, we will implement the accept button scenario to illustrate how to generate a custom event that the user can handle on their own.

# [Managing policy acceptance](#toc.xhtml_s67a)

Let's start by adding the accept button to our cookie alert web component.

The **`Close`** button simply hides the cookie alert for the current session. When the user accesses our web page or application again, the cookie alert will still show its message. The accept button, instead, will store into a cookie a piece of information telling that the user has accepted the cookie policy of the website. This cookie will be read by the cookie alert component each time it is added to the DOM. The presence of the cookie will prevent the cookie alert from being shown.

`Let’s create the` **`Accept`** `button by adding the following code to the createComponent() method:`

`createComponent() {`

`//…`

`const acceptButton = document.createElement("button");`

`acceptButton.classList.add("button");`

`acceptButton.innerText = "Accept";`

`acceptButton.addEventListener("click", ()=>{`

`this.style.visibility = "hidden";`

`setCookie("cookiesAccepted", "y", 365);`

`});`

`div.appendChild(acceptButton);`

`//…`

`}`

As you can see, we added a new button the same way we added the **`Close`** button earlier. This time, however, the click event handler also invokes a `setCookie()` function. This function is responsible for creating the cookie we need to store the user's acceptance of the website policy.

The `setCookie()` function is implemented as a private function of the module in the same `index.js` file containing the definition of the `CookieAlert` class. In other words, it is not a method of the `CookieAlert` class. This is its implementation:

`function setCookie(cookieName, cookieValue, expirationDays) {`

`var d = new Date();`

`d.setTime(d.getTime() + (expirationDays*24*60*60*1000));`

`var expires = "expires="+ d.toUTCString();`

`document.cookie = cookieName + "=" + cookieValue + ";" + expires + ";path=/";`

`}`

The details of this function are out of the scope of the Web Components technologies. For completeness, we also report the `getCookie()` function implementation that allows us to retrieve a cookie given its name:

`function getCookie(cookieName) {`

`var name = cookieName + "=";`

`var decodedCookie = decodeURIComponent(document.cookie);`

`var ca = decodedCookie.split(';');`

`for(var i = 0; i <ca.length; i++) {`

`var c = ca[i];`

`while (c.charAt(0) == ' ') {`

`c = c.substring(1);`

`}`

`if (c.indexOf(name) == 0) {`

`return c.substring(name.length, c.length);`

`}`

`}`

`return "";`

`}`

To make this cookie affecting the web component behavior, we need to analyze its content when the cookie alert component is appended to the DOM. So, we change the `connectedCallback()` method as follows:

`connectedCallback() {`

`const cookiesAccepted = getCookie("cookiesAccepted")`

`if (cookiesAccepted === "y") {`

`this.style.visibility = "hidden";`

`} else {`

`this.createComponent();`

`}`

`}`

First, we get the `cookiesAccepted` cookie. If its value is y, we hide the component without even creating its UI. Otherwise, we create UI as usual.

With these changes, when the user has not yet accepted the website cookie policy, the banner will appear as follows:

![](images/Figure_5.3.jpg)

**Figure 5.3**

In addition to the **`Close`** button, we now have the **`Accept`** button, too. If we click the **`Close`** button and reload the page, we will see the cookie alert again. If we click the **`Accept`** button and reload the page, we will no longer see the cookie alert.

# [Creating events](#toc.xhtml_s68a)

So far, the cookie alert component works as expected. However, currently, it doesn't allow the user to add custom logic to the acceptance event. All the logic is inside our web component. We would like to enable the developer to use our cookie alert to add their logic when the user accepts the website policy. In other words, we need to generate a custom event.

# [Dispatching simple events](#toc.xhtml_s69a)

To fulfil this goal, we can leverage the standard mechanism to create custom DOM events. This means that we can create our event by using the `CustomEvent` class and trigger it by using the `dispatchEvent()` method. Let's see how to apply them when creating the UI of our web component:

`createComponent() {`

`//…`

`const acceptButton = document.createElement("button");`

`acceptButton.classList.add("button");`

`acceptButton.innerText = "Accept";`

`acceptButton.addEventListener("click", ()=>{`

`this.style.visibility = "hidden";`

`setCookie("cookiesAccepted", "y", 365);`

`this.dispatchEvent(new CustomEvent("accepted"));`

`});`

`div.appendChild(acceptButton);`

`//…`

`}`

In the code above, we added one statement in the `click` handler of the **`Accept`** button. This statement simply creates and dispatches the accepted event.

**You can use the Event class or the CustomEvent class to create events. While the former allows you to create a simple event, just the one we just illustrated, the latter allows you to pass also some data. In the example above, we used the CustomEvent class because we are going to pass data associated with the event later on.**

So, when the user clicks the **`Accept`** button, the accepted event will be triggered. In this case, the developer using our web component can handle this event by adding an event listener just like any standard event. The following code shows how it can be accomplished in a page containing our `cookie-alert` component:

`const cookieAlert = document.querySelector("cookie-alert");`

`cookieAlert.addEventListener("accepted", () => alert("Thanks for accepting our cookie policy!"));`

This event listener will display a thank message when the user accepts the cookie management policy.

# [The meaning of 'this'](#toc.xhtml_s70a)

Before going ahead, it's worth mentioning a very important caveat about the use of `this` keyword.

To get the `accepted` event generated, we wrote the following code:

`acceptButton.addEventListener("click", ()=>{`

`this.style.visibility = "hidden";`

`setCookie("cookiesAccepted", "y", 365);`

`this.dispatchEvent(new CustomEvent("accepted"));`

`});`

Inside the body of the `click` event handler, we used the `this` keyword both to set the `visibility` value and to dispatch the `accepted` event. Be aware that we are using here an arrow function, so the `this` keyword statically identifies the current cookie alert component. If you use a standard function as in the following example, you will get unexpected behaviors:

`acceptButton.addEventListener("click", function(){`

`this.style.visibility = "hidden";`

`setCookie("cookiesAccepted", "y", 365);`

`this.dispatchEvent(new CustomEvent("accepted"));`

`});`

In fact, in this case, the this keyword dynamically identifies the object the listener is attached to, that is the **`Accept`** button. So, with this code, you will see the **`Accept`** button disappear and the listener to the accepted event not execute.

# [Passing data](#toc.xhtml_s71a)

Now, let's move on to see how we can improve the event management. By default, the event object is passed to the event listener. This allows the developer to inspect it and make decisions on its content. The `accepted` event we are triggering so far does not provide anything special to the listener. We can provide some information by adding details to the event we are generating. The following code shows how to accomplish this enrichment:

`createComponent() {`

`//…`

`const acceptButton = document.createElement("button");`

`acceptButton.classList.add("button");`

`acceptButton.innerText = "Accept";`

`acceptButton.addEventListener("click", ()=>{`

`this.style.visibility = "hidden";`

`setCookie("cookiesAccepted", "y", 365);`

`this.dispatchEvent(new CustomEvent("accepted", {`

`detail:{`

`acceptedCookieName: "cookiesAccepted",`

`acceptedCookieExpiration: 365}`

`}));`

`});`

`div.appendChild(acceptButton);`

`//…`

`}`

As you can see, here we added a second argument to the `CustomEvent` constructor. This argument is an object with the detail property containing the data we want to pass to the listener. In this example, we are passing the name of the cookie that has been created in the `acceptedCookieName` property and the cookie validity time in days `(acceptedCookieExpiration property).`

`Let's take a look at how you, as the developer using the cookie alert component, can leverage these data:`

`const cookieAlert = document.querySelector("cookie-alert");`

`cookieAlert.addEventListener("accepted", (event) =>`

`alert(‘Thanks for accepting our cookie policy.\nYou need to confirm again in ${event.detail.acceptedCookieExpiration} days.‘));`

In the example above, the accepted event listener has an `event` parameter. Of course, this parameter represents the event we created with the `CustomEvent` constructor. So, by using the `event.detail` property, the thank message can show a reference to the number of validity days for the cookie. The following is a picture showing what you should see when the user clicks the **`Accept`** button:

![](images/Figure_5.4.jpg)

**Figure 5.4**

# [Adding onevent attributes](#toc.xhtml_s72a)

In addition to the `addEventListenere()` method, standard events allow you to specify a handler in the HTML markup via special attributes like `onclick, onblur,` `onmouseover`, and so on. As you know, these onevent attributes let you attach a string representing the code to execute when the specific event occurs. Likely, to make your web component as much compliant as possible to standard HTML elements, you would like to add this kind of attributes to it. Unfortunately, this feature is not free. You need to implement the support for these attributes on your own, and it is not so trivial.

To have an idea of how to manage onevent attributes, let's take a look at how we can add support for the `onaccepted` attribute to our cookie alert web component. Keep in mind that adding such types of attributes is no more than any typical attribute. Also, it is a best practice to add a similar property when you are adding an attribute to your component. This mimics the usual behavior of standard HTML elements and lets the user find what they are used to expect.

**Remember that, as per specifications, the onevent attributes and properties allow you to assign only one event handler for a specific event. If you need to attach multiple handlers for one event, you should use the addEventListener() method.**

So, as a first step, let's add an internal property that will keep the current handler:

`constructor() {`

`super();`

`this._message = "This website uses cookies to ensure you get the best experience";`

`this._onAcceptedListener = null;`

`}`

We added to the component's constructor a statement that assigns the null value to the `_onAcceptedListener` internal property.

Now, we can add a setter and a getter for the `onaccepted` property, as shown in the following code snippet:

`get onaccepted() {`

`return this._onAcceptedListener;`

`}`

`set onaccepted(listener) {`

`if (this._onAcceptedListener) {`

`this.removeEventListener("accepted", this._onAcceptedListener);`

`}`

`if (typeof listener === "function") {`

`this._onAcceptedListener = listener;`

`this.addEventListener("accepted", this._onAcceptedListener);`

`}`

`}`

While the getter simply returns the value of the internal `_onAcceptedListener` property, the setter is a bit more complicated. It checks if the internal `_onAcceptedListener` property already has an assigned value. In this case, it removes the previously assigned listener. This step avoids adding another listener to the existing one for that event. The next step checks if the type of the passed value is a function. This ensures that the setter accepts only functions. Once we are sure that the passed value is a function, it is assigned to the internal `_onAcceptedListener` property. Also, a listener for the accepted event is created from it via the `addEventListener()` method.

At this point, we add the onaccepted attribute among the observed attributes, as shown by the following code:

`static get observedAttributes() {`

`return ["message", "onaccepted"];`

`}`

**Although you can use any name for your onevent attribute, you should follow the standard convention based on the concatenation between the on prefix and the name of the event.**

Finally, we need to manage changes to the `onaccepted` attribute by modifying the `attributedChangedCallback()` method:

`attributeChangedCallback(name, oldValue, newValue) {`

`if (oldValue !== newValue) {`

`if (name === "message") {`

`this._message = newValue;`

`this.updateMessage();`

`}`

`if (name === "onaccepted") {`

`if (newValue) {`

`this.onaccepted = new Function("event", ‘${newValue}‘);`

`} else {`

`this.onaccepted = null;`

`}`

`}`

`}`

`}`

When the changed attribute is the `onaccepted` one, we assign a function generated from the attribute's value to the `onaccepted` property.

Remember that, unlike the `onaccepted` property, the value type of the `onaccepted` attribute is always a string. Besides, the user can assign any statement to the `onaccepted` attribute, not just a function. So, in order to correctly assign the attribute's value to the `onaccepted` property, we need to create a `function` by using the `Function()` constructor. If a false value is passed to the onaccepted attribute, the null value is assigned to the `onaccepted` property, and so, any previous handler is removed.

Now, our cookie alert supports the onaccepted attribute. So, we can attach to it our event handler as in the following example:

`<!DOCTYPE html>`

`<html>`

`<head>`

`<title>Web Components with Webpack Build System</title>`

`<script src="./wc-polyfills/webcomponents-loader.js"></script>`

`<script src="./bundle.js"></script>`

`<script>`

`function handleAccepted(event) {`

`alert(‘Thanks for accepting our cookie policy.\nYou need to confirm again in ${event.detail.acceptedCookieExpiration} days.‘);`

`}`

`</script>`

`</head>`

`<body>`

`<h1>Here is your Web Component</h1>`

`<cookie-alert`

`message="We use cookies, but respect your privacy!"`

`onaccepted="handleAccepted(event)">`

`</cookie-alert>`

`</body>`

`</html>`

We defined the `handleAccepted()` event handler and assigned it to the onaccepted attribute in the markup. Of course, the resulting behavior will be the same we had before with the `addEventListener()` method.

Although the management of the attribute is quite satisfactory, you should be aware of an important issue in this implementation. Consider the way we assign the event handler to the `onaccepted` property:

`this.onaccepted = new Function("event", ‘${newValue}‘);`

The `Function()` constructor takes the event string as the parameter name of the newly created function. Let's consider now the value assigned to the `onaccepted` attribute:

`handleAccepted(event)`

The parameter passed to the `handleAccepted()` function happens to match the parameter name we defined above. This makes the overall mechanism to work because the final function returned by the `Function()` constructor is as follows:

`function(event) {`

`handleAccepted(event)`

`}`

However, with this approach, we are imposing a constraint - the user must specify the event name as the parameter in their event handler. Let's assume the user specifies a different name as in the following example:

`handleAccepted(e)`

In this case, the handler will not work as expected because the resulting function assigned to the `onaccepted` property will be as follows:

`function(event) {`

`handleAccepted(e)`

`}`

To get a standard-like solution that allows the user to choose the name of the event parameter freely, you should implement a more sophisticated algorithm that takes this into account.

# [Removing event listeners](#toc.xhtml_s73a)

Event listeners are a practical way to get involved when something happens to your component. As you have seen throughout this chapter, you can create them for any HTML element that builds the UI of your component. However, you need to take care of them also when you don't need them anymore.

Event listeners consume system resources. Removing them when you no longer need helps to optimize resources management.

As said in *[Chapter 3, Creating Custom Web Components](#c03.xhtml),* you should use the `disconnectedCallback()` reaction to free the resources allocated for your web component. As you remember, this reaction is called when your component is removed from the DOM. This means that the event listeners of your web component have no more reason to exist so that you can remove them. However, to remove your event listeners, you need to have a reference to them. So, let's see which strategy you can use to be able to manage the event listener's lifecycle of your web component correctly.

As a first thing, we need a place where storing the event listener registrations. We can define an internal property for this purpose:

`constructor() {`

`super();`

`this._message = "This website uses cookies to ensure you get the best experience";`

`this._onAcceptedListener = null;`

`this._eventListeners = [];`

`}`

As you can see in the code above, we changed the cookie alert constructor to add the `_eventListeners` internal property. This property is an array that will contain the objects describing the event listener registrations. Whenever we add an event listener, we need to add an object to the `_eventListeners` property. The following example shows how to change the code of the `CreateComponent()` method in order to add the **`Close`** button:

`const closeButton = document.createElement("button");`

`closeButton.classList.add("button");`

`closeButton.innerText = "Close";`

`const clickHandler = ()=>{`

`this.style.visibility = "hidden";`

`};`

`closeButton.addEventListener("click", clickHandler);`

`this._eventListeners.push({object: closeButton, event: "click", handler: clickHandler});`

`div.appendChild(closeButton);`

We assigned the arrow function that hides the cookie alert to the `clickHandler` constant. Then, we used it to create the event listener. Finally, we added to the `_eventListeners` array an object containing a pointer to the close button element, the name of the event, and the reference to the listener. This operation represents the internal registration of the event listener.

**The internal registration operation should be performed any time you add an event listener in your web component. For a more readable and maintainable code, it would be better if you created a generic function for this purpose.**

The removal of the registered listeners happens in the `connectedCallback()` method, as shown in the following code snippet:

`disconnectedCallback() {`

`this._eventListeners.forEach((registration) => {`

`registration.object`

`.removeEventListener(registration.event, registration.listener);`

`});`

When your component is removed from the DOM, the information contained in each element of the `_eventListeners` property will help you to remove the associated listener via the `removeListener()` method.

# [Conclusion](#toc.xhtml_s74a)

Throughout this chapter, you discovered how to let your web component dealing with events. After a recap about standard DOM event management, we explored the ways you can listen to standard events. Then, we dealt with custom events creation and discussed how to pass data to the event listener. We also tried to replicate the behavior of an onevent-`style` attribute of the standard HTML elements. We showed how to manage the registration and deregistration of event listeners to prevent unnecessary consumption of system resources.

Learning how to manage events, let you create web components able to interact with the user. This is an essential feature for components to be used in a web UI. The events you can create in your components are indistinguishable from the standard events. So, the developer using your components can use the standard approach to handle them.

In the next chapter, you will learn how to implement encapsulation for your web components by leveraging the shadow DOM. You will see how this standard feature protects the internal structure of your component from external interferences.

# [Questions](#toc.xhtml_s75a)

1.  Which are the standard three approaches to handle an event?
2.  Which are the phases of DOM event propagation?
3.  Which standard events can a web component listen to?
4.  How can you prevent a user from attaching event listeners to your web component?
5.  What is the constructor for a custom event?
6.  How can you pass data in a custom event?
7.  Why should you remove the event listeners registered in your web component?
8.  What is the best web component reaction where you can remove the event listeners of your component?

# [CHAPTER 6](#toc.xhtml_c06)

# [Using the Shadow DOM](#toc.xhtml_c06)

Web Components are meant to be used in HTML pages that are not always under our control. A user could put your component on their web page, and you don’t know how that page works. In certain circumstances, you may experience some unwanted interferences with the behavior you designed for your component.

In this chapter, you will discover a few examples of these possible interferences between the cookie alert component and the page **document object model (DOM).** We will discuss how these issues are traditionally addressed and how we will solve them by using the shadow DOM. We also will discuss the difference between the open and the closed shadow DOM with practical examples.

Throughout the chapter, we will add the shadow DOM support to our cookie alert component to show how to use it in practice.

# [Structure](#toc.xhtml_s76a)

*   Web Components and the DOM
*   The shadow DOM
*   Open and closed shadow DOM

# [Objectives](#toc.xhtml_s77a)

This chapter will make you aware of the issues that may occur to Web Components when they are immersed in an unknown web page. You will be able to prevent these issues by using the shadow DOM. Also, you will learn about the open and closed shadow DOM and decide which type to use for your component.

# [Web Components and the DOM](#toc.xhtml_s78a)

As you’ve seen so far, DOM manipulation is an essential part of creating custom elements and hence web components. The ability to perfectly integrate into the DOM makes your web components almost indistinguishable from standard HTML elements. However, this same DOM integration capability is somehow a problem for components. Being so integrated into the DOM leads to some issues that prevent web components from being true components, that is, UI elements with their look and behavior that can be easily reused.

Let’s take a look at the problems that this tight integration may generate.

# [The global DOM](#toc.xhtml_s79a)

The **DOM** is an object-based representation of the HTML elements on a page. This means that element in an HTML page is represented by an object in the DOM tree. This is true for both standard HTML elements and custom elements. However, since custom elements are usually built up with HTML elements and other custom elements, you end up having all their composing items in the DOM tree.

Consider the usual HTML page containing our cookie alert web component:

`<!DOCTYPE html>`

`<html>`

`<head>`

`<title>Web Components with Webpack Build System</title>`

`<script src="./wc-polyfills/webcomponents-loader.js"></script>`

`<script src="./bundle.js"></script>`

`</head>`

`<body>`

`<h1>Here is your Web Component</h1>`

`<cookie-alert message="We use cookies, but respect your privacy!"></cookie-alert>`

`</body>`

`</html>`

If you use the tool of your favorite browser to inspect the generated HTML, for example, the **`Developer Tools`** in Chrome, you should see the markup shown by the following screenshot:

![](images/Figure_6.1.jpg)

**Figure 6.1**

As you can see, our custom tag `<cookie-alert>` contains the markup corresponding to the DOM of the custom element. It includes the style element and the `<div>` with the text and the buttons you added via JavaScript.

These elements are integrated into the page’s DOM, so they work like any other element on the page. For example, you can access the text of the cookie alert with the following code:

`document.querySelector("div.container span").innerText`

Of course, it makes more sense using the message property of the component to get the text, as follows:

`document.querySelector("cookie-alert").message`

However, nobody prevents you from accessing the internal DOM structure of your web component. The DOM is like a global variable: any piece of code can access it and change its value. And like a global variable, it brings with it all its flaws, as we will see in the next section.

# [The problem with the DOM](#toc.xhtml_s80a)

While the previous example may be a choice of the developer using your component, other pitfalls may occur when your component is inserted into a page with arbitrary complexity. Consider, for example, an HTML page like the following:

`<!DOCTYPE html>`

`<html>`

`<head>`

`<title>Web Components with Webpack Build System</title>`

`<script src="./wc-polyfills/webcomponents-loader.js"></script>`

`<script src="./bundle.js"></script>`

`<style>`

`button {`

`border-style: dotted;`

`background-color: red !importan`

`}`

`</style>`

`</head>`

`<body>`

`<h1>Here is your Web Component</h1>`

`<button>Click here!</button>`

`<cookie-alert message="We use cookies, but respect your privacy!"></cookie-alert>`

`</body>`

`</html>`

You have a CSS rule defining the border style and the background color for the `button` elements on the current page. Also, you have a button element in the page, just below the header. Running this page, you will get the following result:

![](images/Figure_6.2.jpg)

**Figure 6.2**

As you can see, the CSS rule has been applied not only to the button on the page but also to the buttons embedded into the cookie alert component. This may be disappointing.

Also, consider the following markup:

`<!DOCTYPE html>`

`<html>`

`<head>`

`<title>Web Components with Webpack Build System</title>`

`<script src="./wc-polyfills/webcomponents-loader.js"></script>`

`<script src="./bundle.js"></script>`

`<style>`

`button {`

`border-style: dotted;`

`background-color: red !importan`

`}`

`.container {`

`background-color: gray;`

`}`

`</style>`

`</head>`

`<body class="container">`

`<h1>Here is your Web Component</h1>`

`<button>Click here!</button>`

`<cookie-alert message="We use cookies, but respect your privacy!"></cookie-alert>`

`</body>`

`</html>`

You added a new CSS rule defining a container class with a gray background, and applied this class to the document’s body. According to this rule, you would expect a gray background for the page. Instead, the HTML page will be rendered, as shown in the following screenshot:

![](images/Figure_6.3.jpg)

**Figure 6.3**

The page’s background is not gray, as stated by the page-level CSS rule, but blue, as defined by the component-level CSS rule. What happened is an accidental name clash between the page-level and component-level CSS classes.

Of course, the user should not be required to know the internal details of our component. So, both these examples might make you question the real effectiveness of Web Components technologies.

To make things worse, assume you add a few lines of JavaScript to this HTML page, like in the following:

`<!DOCTYPE html>`

`<html>`

`<head>`

`<title>Web Components with Webpack Build System</title>`

`<script src="./wc-polyfills/webcomponents-loader.js"></script>`

`<script src="./bundle.js"></script>`

`<style>`

`button {`

`border-style: dotted;`

`background-color: red !importan`

`}`

`.container {`

`background-color: gray;`

`}`

`</style>`

`<script>`

`window.addEventListener("load", ()=>{`

`let buttons = document.querySelectorAll("button");`

`buttons.forEach((btn)=>{`

`btn.disabled = true;`

`});`

`});`

`</script>`

`</head>`

`<body class="container">`

`<h1>Here is your Web Component</h1>`

`<button>Click here!</button>`

`<cookie-alert message="We use cookies, but respect your privacy!"></cookie-alert>`

`</body>`

`</html>`

You added a script that disables all buttons in the current page. Maybe it fulfills some specific logic to manage the user’s elements on the page. However, this code also affects the buttons inside the cookie alert.

All these examples should make it clear that the internal implementation of your web component is not safe. External code can affect your component, accidentally or intentionally. In other words, your web component lacks encapsulation.

Encapsulation is the ability of an object to hide its internal representation and behavior. It allows you to design an object or component so that it can interact with the external world via its public interface while keeping private its internal state. This feature allows you to decouple the internal behavior of your component from the external world. It let you change the internal representation or behavior without affecting the public interface and the external world. In other words, the encapsulation makes your component be an actual component.

# [DOM encapsulation attempts](#toc.xhtml_s81a)

So, we just discovered that the current implementation of our cookie alert component is not safe from external interferences. Since encapsulation is a required feature for a component, how can we fix this annoying problem?

**It should be clear that the global accessibility of the DOM is not a problem related to Web Components technologies. This is a feature of the standard DOM and affects any type of component you build with browser-based technologies, including frameworks like Angular, React, Vue, and many more.**

The traditional solution to get around this encapsulation problem is to embed the portion of DOM representing your component in a separate DOM, that is in a separate HTML page. This page is then appended to the main page via an `iframe`. For example, this is the typical approach used by *Google* to allow developers to embed its maps and its videos from *YouTube*.

To apply this solution to our cookie alert component, we should rearrange the component’s code in order to create an `iframe`, make this `iframe` the main container of your component, and append any other element inside the DOM of the iframe’s page. In practice, the `createComponent()` method of your component should be similar to the following:

`createComponent() {`

`const iframe = document.createElement("iframe");`

`iframe.style.border = 0;`

`iframe.style.height = "200px";`

`const style = document.createElement("style");`

`style.appendChild(document.createTextNode(styleRules));`

`iframe.contentDocument.body.appendChild(style);`

`const span = document.createElement("span");`

`const div = document.createElement("div");`

`div.classList.add("container", "footer");`

`div.appendChild(span);`

`// other code`

`iframe.contentDocument.body.appendChild(div);`

`this.appendChild(iframe);`

`this.updateMessage();`

`}`

Even if this approach may give you an illusion to solve the problem, it still has a few `issues`. You need to programmatically control the border thickness and height of the `iframe` to provide the illusion that your component is integrated with the main page. But your component is not integrated with the page, and you have no real control over the height of the `iframe`. Iframes are not very responsive. Also, iframes are designed to embed another full document in the current page. This leads to more complexity when we want to pass data from the parent document to the child document. In other words, we need to add a code layer that passes data from the component to the internal document and vice versa. Also, we lose all the event handling features we learned in the previous chapter.

In summary, iframes are not the solution to solve the Web Components encapsulation issue.

# [The shadow DOM](#toc.xhtml_s82a)

When introduced Web Components, we said that they stem from the combination of three technologies - Custom elements, shadow DOM, and HTML templates. As you can see, the shadow DOM is one of these enabling technologies. And it is the technology that helps us to solve the encapsulation problem we pointed out in the previous sections.

# [What is the shadow DOM](#toc.xhtml_s83a)

The shadow DOM is a set of standard APIs that allows you to attach a private DOM to any HTML element. This private DOM is similar to the page DOM, but its internal structure is not affected by the state of the global DOM.

When you append your component to the DOM, its shadow DOM will be attached to global DOM but remains private. The following picture from *Mozilla developer network documentation shows graphically* how it happens:

![](images/Figure_6.4.jpg)

**Figure 6.4**

**[Source [https://developer.mozilla.org/en-US/docs/Web/Web_Components/Using_shadow_DOM](https://developer.mozilla.org/en-US/docs/Web/Web_Components/Using_shadow_DOM)]**

From this picture, you can see that we have specific terminology for the shadow DOM. Let’s try to define the more commons terms.

*   **Shadow DOM**: This is the object model technology and APIs that allow you to attach a private DOM to an HTML element.
*   **Shadow tree**: It is the private tree of nodes associated with an HTML element; this tree is not directly accessible from the global DOM
*   **Light tree**: This is a regular subtree of nodes
*   **Shadow host**: An HTML element that has a shadow tree associated
*   **Shadow root**: This is the root node of the shadow tree

Perhaps these terms may appear a bit confusing, but we are going to see the shadow DOM in action, and hopefully, your doubts will go away.

# [Using the shadow DOM](#toc.xhtml_s84a)

Let’s see how to add encapsulation to our alert cookie by using the shadow DOM. As a first step, you need to enable it in the constructor of the component. Here is how the new version of the constructor looks like:

`constructor() {`

`super();`

`this._message = "This website uses cookies to ensure you get the best experience";`

`this.attachShadow({mode: "open"});`

`this._onAcceptedListener = null;`

`}`

You added a new statement that attaches an instance of the shadow DOM to the current component. Regarding the definition given above, the component itself, identified by `this` keyword, is the shadow host. The `attachShadow()` method creates an instance of a shadow tree composed by just its root node, the shadow root. This shadow root is accessible through the `shadowRoot` property of the component. From now on, any action regarding the construction of the component’s UI will involve the `shadowRoot` property instead of the component itself.

Consider this new version of the `createComponent()` method:

`createComponent() {`

`const style = document.createElement("style");`

`style.appendChild(document.createTextNode(styleRules));`

`this.shadowRoot.appendChild(style);`

`const span = document.createElement("span");`

`const div = document.createElement("div");`

`div.classList.add("container", "footer");`

`div.appendChild(span);`

`const closeButton = document.createElement("button");`

`closeButton.classList.add("button");`

`closeButton.innerText = "Close";`

`closeButton.addEventListener("click", ()=>{`

`this.style.visibility = "hidden";`

`});`

`div.appendChild(closeButton);`

`const acceptButton = document.createElement("button");`

`acceptButton.classList.add("button");`

`acceptButton.innerText = "Accept";`

`acceptButton.addEventListener("click", ()=>{`

`this.style.visibility = "hidden";`

`setCookie("cookiesAccepted", "y", 365);`

`this.dispatchEvent(new CustomEvent("accepted", {`

`detail:{`

`acceptedCookieName: "cookiesAccepted",`

`acceptedCookieExpiration: 365}`

`}));`

`});`

`div.appendChild(acceptButton);`

`this.shadowRoot.appendChild(div);`

`this.updateMessage();`

`}`

As you can see, while so far, we appended HTML elements to the component directly through this key, now these elements have to be attached to the `shadowRoot` property.

We also need to rearrange any reference to the elements that before were attached to the component. For example, we need to apply this change to the `updateMessage()` method:

`updateMessage() {`

`this.shadowRoot.querySelector("span").innerText = this._message;`

`}`

These small changes enable the encapsulation in our cookie alert component. If you run the project, the resulting page appears as expected, like in the following screenshot:

![](images/Figure_6.5.jpg)

**Figure 6.5**

Now, the internal structure of the cookie alert component is protected from external interferences. If you take a look at the generated markup with the inspector of your browser, you will find something like the following:

![](images/Figure_6.6.jpg)

**Figure 6.6**

You see that there is still the markup corresponding to the component’s UI, but it is encapsulated within a #`shadow-root` directive. This directive flags the contained markup as not directly accessible.

# [Open and closed shadow DOM](#toc.xhtml_s85a)

We are saying that, with the shadow DOM, the internal structure of a web component is not directly accessible. This means that the internal structure of a web component is protected from possible external interferences caused by CSS rules or JavaScript code manipulating generic HTML elements.

However, the internal structure of a web component is still accessible through the `shadowRoot` property of the shadow host element. For example, you can disable the buttons of the cookie alert component in an HTML page with the following code:

`const cookieAlert = document.querySelector("cookie-alert");`

`const componentDOM = cookieAlert.shadowRoo`

`let buttons = componentDOM.querySelectorAll("button");`

`buttons.forEach((btn)=>{`

`btn.disabled = true;`

`});`

You accessed the `shadowRoot` property of the component and used it as the usual DOM. Of course, you are intentionally accessing the internal structure of the component. So, you are protected only from accidental interferences, while any developer can change the structure of your component.

This depends on the type of shadow DOM you choose to attach to your component. Take a look at the statement that attaches the shadow DOM to the cookie alert component:

`this.attachShadow({mode: "open"});`

We are passing an object to the `attachShadow()` method that specifies an option. This object is telling us that the shadow DOM mode should be open. An open shadow DOM is accessible outside the component itself through the `shadowRoot` property. So, the behavior we noticed above is by design.

If you don’t want to expose the shadow DOM of your component to the external world, you need a closed shadow DOM. You can attach a closed shadow DOM to your component by specifying the closed value as the shadow DOM mode.

The following code shows how you can change the cookie alert constructor to enable the closed shadow DOM:

`constructor() {`

`super();`

`this._message = "This website uses cookies to ensure you get the best experience";`

`this._shadowRoot = this.attachShadow({mode: "closed"});`

`this._onAcceptedListener = null;`

`}`

When creating an open shadow DOM, we used the `attachShadow()` method and then used the `shadowRoot` property to append and manipulate the internal DOM. We didn’t assign the result of the `attachShadow()` method to any variable. The effect of the `attachShadow()` method was the addition of the root node to the `shadowRoot` property of the shadow host.

When you attach a closed shadow DOM by passing `{mode: “close”}` to the `attachShadow()` method, the `shadowRoot` property still returns `null`. This prevents the DOM from being accessible from the outside. In this case, to access the shadow DOM from within the component, you have to assign the result of the `attachShadow()` method to a variable. In the example above, we assigned the closed shadow DOM to the internal property `_shadowRoot`.

Be aware that using the `this._shadowRoot` property as in the example, the shadow DOM of your component is not completely inaccessible. A user who iterates through your component’s properties would figure out what the `_shadowRoot` property stands for and use it to access its internal structure still. To try locking the shadow DOM of your component, you should assign it to a local variable, a `WeakMap`, or a private property (when private properties will become standard and largely supported).

**Keep in mind that the closed shadow DOM is not a security measure. The user can anyway affect the shadow DOM of your component, even just by using the** `attachShadow()` **method of your shadow host element.**

So, we assigned the closed shadow DOM of the cookie alert component to the References to the `_shadowRoot` property. From now on, any manipulation of the internal DOM will be done through this property. The following is the revised code of the `createComponent()` method:

`createComponent() {`

`const style = document.createElement("style");`

`style.appendChild(document.createTextNode(styleRules));`

`this._shadowRoot.appendChild(style);`

`const span = document.createElement("span");`

`const div = document.createElement("div");`

`div.classList.add("container", "footer");`

`div.appendChild(span);`

`const closeButton = document.createElement("button");`

`closeButton.classList.add("button");`

`closeButton.innerText = "Close";`

`closeButton.addEventListener("click", ()=>{`

`this.style.visibility = "hidden";`

`});`

`div.appendChild(closeButton);`

`const acceptButton = document.createElement("button");`

`acceptButton.classList.add("button");`

`acceptButton.innerText = "Accept";`

`acceptButton.addEventListener("click", ()=>{`

`this.style.visibility = "hidden";`

`setCookie("cookiesAccepted", "y", 365);`

`this.dispatchEvent(new CustomEvent("accepted", {`

`detail:{`

`acceptedCookieName: "cookiesAccepted",`

`acceptedCookieExpiration: 365}`

`}));`

`});`

`div.appendChild(acceptButton);`

`this._shadowRoot.appendChild(div);`

`this.updateMessage();`

`}`

Also, the `updateMessage()` method needs to be changed to refer to the this.`_shadowRoot` property:

`updateMessage() {`

`this._shadowRoot.querySelector("span").innerText = this._message;`

`}`

Now, when you run the project, the cookie alert component will continue to work as before. But if you take a look at the generated markup with the inspector of your browser, you will find something similar to the following:

![](images/Figure_6.7.jpg)

**Figure 6.7**

The markup of the shadow DOM is no longer available.

So, at this point, you may wonder which type of shadow DOM you should use for your web components - open or closed?

Of course, it’s a design choice. You may choose to block the access to the internal structure of your component and allows the user to interact with it exclusively through the public properties and methods. However, this means that you should accurately design the public interface of your component to ensure any possible use of it. Consider that the user of your component could not only add it in their pages, but they could also extend your component. In this case, accessing the shadow DOM could be useful to adapt its look and behavior to the user’s needs.

# [Conclusion](#toc.xhtml_s86a)

In this chapter, you discovered that the cookie alert built so far was not ready to be a true component. It lacks encapsulation. You learned that it is due to the global nature of the DOM and experienced a few situations where this affects your component with unwanted interferences. The traditional approach used to overcome this problem is based on iframes, but it is complicated and doesn’t resolve the problem. We explained that the solution to the lack of encapsulation is the shadow DOM. We used this feature in the cookie alert component and showed how it is very easy to apply. Finally, we discussed the difference between the open and closed shadow DOM.

Now, at the end of this chapter, you got the technologies to create real components whose internal structure is not affected by external interferences.

In the next chapter, you will learn how to simplify the definition of your web component UI by leveraging the HTML templates. Also, you will learn how to make your component more flexible, allowing the user to add other HTML elements inside your component.

# [Questions](#toc.xhtml_s87a)

1.  What is encapsulation?
2.  Why is encapsulation a desired feature for a component?
3.  Why does the global DOM not provide support for encapsulation?
4.  What is the traditional approach to providing a form of encapsulation?
5.  What is the shadow DOM?
6.  What is the difference between the shadow host and the shadow root?
7.  What is the method that adds the support for the shadow DOM to your web component?
8.  How can you prevent the user from accessing the shadow DOM?
9.  What is the difference between the open and the closed shadow DOM?

# [CHAPTER 7](#toc.xhtml_c07)

# [Using HTML Templates](#toc.xhtml_c07)

Even though it is not strictly required, most web components have a UI to show data and graphics and allow the user to interact with it. We learned how to create a UI for our web components in previous chapters and applied a few different techniques to our cookie alert component.

In this chapter, we will analyze the techniques we used so far to implement the UI for Web Components and will explore a new alternative approach based on native HTML templates. We will discuss the benefits this approach brings us and will show how to apply it to the alert cookie component.

Also, we will go further to discover a way to enable Web Components to combine the markup of its UI with an arbitrary markup provided by the user. This approach, based on the <slot> element, extends the power of native HTML templates. This way, we can have richer, flexible, and powerful components with a behavior pretty similar to standard HTML elements like <div>, <p>, <select>, or other that allows you to insert markup within their tags.

As usual, we will apply all these new concepts to our cookie alert component to show how to use them in practice.

# [Structure](#toc.xhtml_s88a)

*   Introducing templates
*   Composing markup with slots

# [Objectives](#toc.xhtml_s89a)

In this chapter, you will learn about native HTML templates and will discover how to use them to define declarative and efficient UIs for your web components. Also, you will learn how to enable your web components to combine their UI markup with customized markup provided by the user.

# [Introducing templates](#toc.xhtml_s90a)

In *[Chapter 3, Creating Custom Web Components](#c03.xhtml),* we started to build the user interface of our cookie alert component through strings representing the required markup. We recall here the two constant we defined at that time:

`const styleMarkup = ‘`

`<style>`

`.container {`

`color: rgb(255, 255, 255);`

`background-color: rgb(35, 122, 252);`

`padding: 1em 1.8em;`

`width: 100%;`

`font-family: Helvetica,Calibri,Arial,sans-serif;`

`}`

`.footer {`

`position:fixed;`

`left:0px;`

`bottom:0px;`

`}`

`</style>‘;`

`const componentMarkup = ‘`

`<div class="container footer">`

`<span>This website uses cookies to ensure you get the best experience</span>`

`</div>‘;`

These constants were concatenated and assigned to the `innerHTML` property of the component. This approach was simple and clear since it provided in a declarative way the UI structure through its markup. However, it wasn’t so easy to manage when the UI became more complex. So, we switched to a DOM-based approach, where each element of the UI is dynamically created through the DOM APIs. In practices, we kept the string-based approach for the `styleRules` constant and introduced the `createComponent()` method to build the HTML elements for the UI, as shown in the following code:

`createComponent() {`

`const style = document.createElement("style");`

`style.appendChild(document.createTextNode(styleRules));`

`this.shadowRoot.appendChild(style);`

`const span = document.createElement("span");`

`const div = document.createElement("div");`

`div.classList.add("container", "footer");`

`div.appendChild(span);`

`const closeButton = document.createElement("button");`

`closeButton.classList.add("button");`

`closeButton.innerText = "Close";`

`closeButton.addEventListener("click", ()=>{`

`this.style.visibility = "hidden";`

`});`

`div.appendChild(closeButton);`

`const acceptButton = document.createElement("button");`

`acceptButton.classList.add("button");`

`acceptButton.innerText = "Accept";`

`acceptButton.addEventListener("click", ()=>{`

`this.style.visibility = "hidden";`

`setCookie("cookiesAccepted", "y", 365);`

`this.dispatchEvent(new CustomEvent("accepted", {`

`detail:{`

`acceptedCookieName: "cookiesAccepted",`

`acceptedCookieExpiration: 365}`

`}));`

`});`

`div.appendChild(acceptButton);`

`this.shadowRoot.appendChild(div);`

`this.updateMessage();`

`}`

This new approach offers a more flexible way to create the component’s UI, especially when the HTML elements you have to create depend on external parameters. However, with this programmatic approach, we lose the clarity of the string-based one. Building the UI via DOM APIs is powerful, but may not be handy in many situations. Also, it’s not so easy to write and maintain.

# [What is a template?](#toc.xhtml_s91a)

An alternative way to define the UI of your web component is by using a template.

Creating HTML templates is a very common task in the context of web programming. It happens both on the server and on the client-side. As you know, an HTML template is a prepared HTML markup that allows you to insert custom snippets into specific points. To an extent, we were defining a template when using the constant strings containing the UI markup, but we will learn that the string-based approach has some pitfalls.

The HTML standard provides you with the `<template>` element. This element allows you to declare a template, which is a structure of HTML elements. You can do it by simply adding the markup inside the `<template>` element and appending it to the head or the body of your HTML page, at your convenience. Take a look at the following example:

`<!DOCTYPE html>`

`<html>`

`<head>`

`<template id=”myTemplate”>`

`<div>`

`<img src=”images/logo.png”>`

`<p>This is a sample text</p>`

`</div>`

`</template>`

`</head>`

`<body>`

`…`

`</body>`

`</html>`

In this example, we have a template definition in the head section of an HTML page. The template defines an `<div>` element containing an image and a paragraph.

Notice that we assigned an identifier to the template. This id allows you to identify the template when we will use it at runtime. The template will be used to generate an instance of a DOM structure to be appended to the DOM, as we will see later on.

You can declare any valid markup in your template element, including `<style>` and `<script>` elements. You can even include the `<template>` element itself.

You can also define a template with partial or incomplete elements. For example, the following is a valid template:

`<template id=”myTemplate”>`

`<li>`

`<span>This is just one item</span>`

`</li>`

`</template>`

It is not a complete element, since it doesn’t declare the `<ul> or <ol>` wrapping element. But you cannot insert invalid HTML, like the following:

`<template id=”myTemplate”>`

`<span>`

`<li>`

`This is just one item</span>`

`</li>`

`</template>`

Like any other HTML element, you can also create a template element via JavaScript, as shown in this example:

`const template = document.createElement(“template”);`

`template.innerHTML = ‘`

`<div>`

`<img src=”images/logo.png”>`

`<p>This is a sample text</p>`

`</div>`

`‘;`

The effect of these statements is the same as the static declaration of the template with the `<template>` tag.

So, you have an idea of how you can define a template. But what happens when you declare a template via markup or DOM APIs?

When you declare a template, its markup is parsed, and the corresponding HTML elements are created. However, the entire resulting content is inert and invisible.

This means that practically the DOM generated from the template’s markup is hidden, and it does not render. It is not part of the current document, so you cannot access its elements via DOM APIs, like `getElementById()` or `querySelector().` Also, any media reference (image, video, audio, and many more.) is not loaded. This means, for example, that the image in the template above is not loaded at declaration time. Not even scripts are executed.

In other words, the content of a template is prepared but not executed. All that will become active only when the template will be used.

# [Activating a template](#toc.xhtml_s92a)

To activate the content of a template, you have to clone its content and append it to the DOM. The following is an example of activation of the `myTemplate` template defined above:

`const myTemplate = document.getElementById(“myTemplate”).conten`

`document.body.appendChild(myTemplate.cloneNode(true));`

We get the content of the template through the content property, clone it via the `cloneNode()` method, and append the result to the body of the current document. Note that the true value passed to the `cloneNode()` method indicates to perform a deep cloning operation, that is, a clone of a node, its attributes, and its descendants.

You can get the same result by using the `importNode()` method, as in the following example:

`const myTemplate = document.getElementById(“myTemplate”).conten`

`document.body.appendChild(document.importNode(myTemplate, true));`

You may wonder why you should clone the template’s content, why you can’t directly attach the template’s content to the document’s DOM. There are at least two reasons for this.

1.  This is the behavior by the design of the template element. The template’s node structure is not a live structure of the DOM. It’s just a set of frozen nodes to be used only as a reference to create other nodes. After all, this is the meaning of a template.
2.  The second reason: It relies on a practical consideration based on the fact that a template can (and should) be shared with multiple components or multiple instances of the same component. Imagine you can directly use the template’s structure. You take the template, customize it for your needs (for example, change some text or add another element), and append it to the DOM. If another component uses the same template, it will be affected by the changes you applied to the template. In most cases, this is not the desired effect.

A final note is about nested templates. We said that a template might contain another template. The following is an example of such a template:

`<template id=”myTemplate”>`

`<ul>`

`<template id=”nestedTemplate”>`

`<li>`

`<span>This is just one item</span>`

`</li>`

`</template>`

`</ul>`

`</template>`

When you clone the outer template, the `myTemplate` template, you don’t automatically activate the inner template, the `nestedTemplate` template. You have to activate the inner template by manually cloning it.

# [Why using a template?](#toc.xhtml_s93a)

Now you should have an idea about what is a native template and how to use it. However, you may still be wondering why you should use it. Which advantages does it provide compared to the string-based or the DOM-based approaches?

Let’s compare these three approaches and try to understand the benefits and the drawbacks each one provides.

When you use a string to describe the markup of your UI, each time your component is created, you will go through the following steps:

1.  The text is parsed, and the validity of the HTML markup is checked
2.  The DOM elements are created
3.  The DOM elements are appended to the DOM

When you use the DOM-based approach, the steps executed when your component is created are as follows:

1.  The DOM elements are created
2.  The DOM elements are appended to the DOM

In fact, in this case, you don’t have a parsing step since you are directly creating the HTML elements you need.

By using a template, you have just one step:

1.  The DOM elements are appended to the DOM

The parsing and DOM element creation steps have to be done when you declared your template. It happens only once for any instance of your component.

So, by using a template, you add efficiency to the declarative approach of the string-based approach.

# [Template at work](#toc.xhtml_s94a)

After introducing templates, let’s put them at work in our cookie alert component. We will replace the current approach in building the UI – the DOM-based approach – with the template-based approach. So, let’s modify the `index.js` file that defines our component.

The first thing we do is replacing the `styleRules` constant declaration with the following:

`const template = document.createElement('template');`

`template.innerHTML = ‘`

`<style>`

`.container {`

`color: rgb(255, 255, 255);`

`background-color: rgb(35, 122, 252);`

`padding: 1em 1.8em;`

`width: 100%;`

`font-family: Helvetica,Calibri,Arial,sans-serif;`

`}`

`.footer {`

`position:fixed;`

`left:0px;`

`bottom:0px;`

`}`

`.button {`

`color: rgb(255, 255, 255);`

`background-color: transparen`

`border-color: rgb(255, 255, 255);`

`padding: 5px 40px;`

`margin-right: 50px;`

`cursor: pointer;`

`float:righ`

`}`

`</style>`

`<div class="container footer">`

`<span id="message"></span>`

`<button id="closeButton" class="button">Close</button>`

`<button id= "acceptButton" class="button">Accept</button>`

`</div>`

`‘;`

We are creating the template via JavaScript and assigning the basic UI markup to its `innerHTML` property. Note that the template includes both the style definition and the HTML markup.

**Remember that template definition code is outside the component class definition, so it is executed just once, not at each instance creation of your component.**

Then, we change the constructor as follows:

`constructor() {`

`super();`

`this._message = "This website uses cookies to ensure you get the best experience";`

`this.attachShadow({mode: "open"});`

`this.shadowRoot.appendChild(template.content.cloneNode(true));`

`this._onAcceptedListener = null;`

`}`

Here we added the template activation statement just after attaching the shadow DOM. Note that we are not adding the cloned template’s content to the DOM, but the shadow DOM of the current component. You may wonder why we are doing this in the constructor. Since the template structure is static, that is to say, and it does not depend on external parameters, we can use it at the component’s instantiation time so that it will be ready when we need to customize it.

**In *[Chapter 3, Creating Custom Web Components](#c03.xhtml)*, we said that you could not access the DOM in the constructor of your component. However, you see that here we are adding nodes through the `appendChild()` method. Consider that here you are manipulating the shadow DOM, that is, the private DOM of the component you just attached. Once the shadow DOM has been attached to your component, you can access it. Still, you cannot access the global DOM from the constructor since, at this stage, your component has been created, but it has not been added to the global DOM.**

Since we are using the native template, we no longer need the `createComponent()` method. It was the method that created the UI with a DOM-based approach. Now, the UI is built by adding the template content to the DOM in the constructor. What we need at this point is just to initialize the UI by adding event listeners or by customizing the look and feel based on the user’s parameters.

So, let’s replace the `createComponent()` method with this method:

`initComponent() {`

`const closeButton = this.shadowRoot.getElementById("closeButton");`

`closeButton.addEventListener("click", ()=>{`

`this.style.visibility = "hidden";`

`});`

`const acceptButton = this.shadowRoot.getElementById("acceptButton");`

`acceptButton.addEventListener("click", ()=>{`

`this.style.visibility = "hidden";`

`setCookie("cookiesAccepted", "y", 365);`

`this.dispatchEvent(new CustomEvent("accepted", {`

`detail:{`

`acceptedCookieName: "cookiesAccepted",`

`acceptedCookieExpiration: 365}`

`}));`

`});`

`this.updateMessage();`

`}`

The `initComponent()` method assigns the event listeners to the close and accept buttons and calls the `updateMessage()` to reflect the values passed through the message property or attribute.

At this point, the `connectedCallback()` method becomes as follows:

`connectedCallback() {`

`const cookiesAccepted = getCookie("cookiesAccepted")`

`if (cookiesAccepted === "y") {`

`this.style.visibility = "hidden";`

`} else {`

`this.initComponent();`

`}`

`}`

As you can see, we are calling the `initComponent()` method instead of the `createComponent()` method.

Finally, to fit the new template markup, we need to replace the old `updateMessage()` method with this new version:

`updateMessage() {`

`this.shadowRoot.getElementById("message").innerText = this._message;`

`}`

Instead of assigning the message value to a generic span, we access the span element through the element identifier.

# [Composing markup with slots](#toc.xhtml_s95a)

Templates provide us with a great way to combine a declarative approach to define the UI of our web components with efficiency. But substantially, they seem to offer no more than an internal benefit. That is to say, it allows you, the component developer, to write less code and have an efficient way to render the UI of your component. But it doesn’t offer you the opportunity to add new features to your component.

Of course, it is what it looks to be so far. You can leverage native templates to obtain HTML elements composition. This means that you can allow the user of your component to embed their markup inside its tags. Many standard HTML elements support elements compositions. Think of all those elements that allow you to have inner markup. For example, think of the `<div>` element that groups other HTML elements; or the `<p>` element that allows you to add formatted text inside its tags, as shown in the following snippet of code:

`<p>`

`This is a <b>formatted</b> <i>message</i>!`

`</p>`

In its simplicity, this example shows how the `<p>` element allows you to embed the text and the `<b>` and `<i>` elements. How great it would be if you could do this for your components as well!

In this section, we will discover how to obtain a similar result for Web Components.

# [Enabling formatted text](#toc.xhtml_s96a)

Let’s start by trying to define what we want to have for our cookie alert component. So far, we are allowing the user to specify their custom message through the message property and attribute. This is awesome but doesn’t allow the user to specify a formatted text. We would like to allow the user to specify a formatted text like in the following example:

`<!DOCTYPE html>`

`<html>`

`<head>`

`<title>Web Components with Webpack Build System</title>`

`<script src="./wc-polyfills/webcomponents-loader.js"></script>`

`<script src="./bundle.js"></script>`

`</head>`

`<body class="container">`

`<h1>Here is your Web Component</h1>`

`<cookie-alert>`

`We use <b>cookies</b>, but respect your <b>privacy</b>!`

`</cookie-alert>`

`</body>`

`</html>`

We are putting some HTML-formatted text within the `<cookie-alert>` tags. We want to obtain a result in some way similar to the one offered by the `<p>` element.

Fortunately, this is not so hard to have, and it doesn’t require to write much code. We can get this result by simply changing the markup of our template as follows:

`const template = document.createElement('template');`

`template.innerHTML = ‘`

`<style>`

`…`

`</style>`

`<div class="container footer">`

`<slot id="message"></slot>`

`<button id="closeButton" class="button">Close</button>`

`<button id= "acceptButton" class="button">Accept</button>`

`</div>`

`‘;`

As you can see, we simply replaced the `<span id=”message”></span>` element in the HTML markup with the `<slot id=”message”></slot>` element.

So, what is this new <slot> element?

The `<slot>` element allows you to define a placeholder in your template. This placeholder can be filled by the user of your component with any markup fragment embedded inside your component’s tags. This is just what we did in the markup above when we specified a formatted text as the message to display

If you run the component’s project with this small change, you will get the following result:

![](images/Figure_7.1.jpg)

**Figure 7.1**

As you can see, the message shown by the cookie alert component has the **`cookies`** and **`privacy`** words in bold.

You can provide a default markup for a `<slot>` element by embedding it, like in the following example:

`<slot id=”message”>This is the <b>default</b> message</slot>`

The default message will be shown if no markup is provided when using the component

You may notice that the `<slot>` element in the template of our component has the id attribute. It is not needed to make the placeholder working. We added it to keep the existing behavior, that is, to keep the possibility to specify the message through the message property and attribute. In other words, the `<slot>` element also has the role of the `<span>` element it has replaced.

Be aware, however, that if you assign a value to the `message` property or attribute while an embedded markup is present, the embedded markup will be shown.

# [Named slots](#toc.xhtml_s97a)

The `<slot>` element opens your component to new possibilities. Of course, you can specify inside the component’s tag any markup, not just markup that defines a formatted text. You can also embed other web components, for example.

The example we have shown above uses just one placeholder identified by the only `<slot>` element in the component’s template. This slot’s occurrence is what is technically called an **unnamed default slot.**

You can insert multiple `<slot>` elements in a template. And you can identify each slot by assigning them a value to their `name` attribute. So, for example, you can have a template like the following:

`const template = document.createElement('template');`

`template.innerHTML = ‘`

`<div>`

`<slot name=”firstName”></slot>`

`<slot name=”lastName”></slot>`

`<slot name=”address”></slot>`

`</div>`

`‘;`

Here are three slots identified by their names. The match between the markup and the placeholders represented by these slots is done by the slot attribute, as shown in the following example:

`<my-custom-element>`

`<span slot=”firstName”>John</span>`

`<span slot=”lastName”>Brown</span>`

`<div slot=”address”>1 Trafalgar Square, London, UK</div>`

`</my-custom-element>`

Each HTML element in this example will replace the corresponding `<slot>` element in the template with the same name value as the `slot` attribute. So, the resulting markup will be similar to the following:

`<div>`

`<span>John</span>`

`<span>Brown</span>`

`<div>1 Trafalgar Square, London, UK</div>`

`</div>`

You can also combine named and unnamed `<slot>` elements, as in the following example:

`const template = document.createElement('template');`

`template.innerHTML = ‘`

`<div>`

`<slot name=”firstName”></slot>`

`<slot name=”lastName”></slot>`

`<slot name=”address”></slot>`

`<slot>Put here a description</slot>`

`</div>`

`‘;`

The last `<slot>` element has no name attribute. This slot will be replaced by all the top-level elements that have no `slot` attribute. For example, consider we have the following web component markup:

`<my-custom-element>`

`<h3>User data</h3>`

`<span slot=”firstName”>John</span>`

`<span slot=”lastName”>Brown</span>`

`<div slot=”address”>1 Trafalgar Square, London, UK</div>`

`<div>`

`<p>No more data</p>`

`</div>`

`</my-custom-element>`

The resulting markup will be as follows:

`<div>`

`<span>John</span>`

`<span>Brown</span>`

`<div>1 Trafalgar Square, London, UK</div>`

`<h3>User data</h3>`

`<div>`

`<p>No more data</p>`

`</div>`

`</div>`

As you can see, the unnamed slot captures all the elements without a slot attribute regardless of their original position. This unnamed slot is said the **default slot.**

**You can have only one default slot. If you have multiple unnamed slots, only the first one will be the default slot, and it will capture all the top-level elements without a slot attribute.**

# [Using named slots](#toc.xhtml_s98a)

Named slots allow you to define multiple placeholders in the UI of your component. This offers the user of your component many points of customization through markup.

Let’s leverage this feature in our cookie alert component by slightly changing the markup of its template, as shown in the following code snippet:

`const template = document.createElement('template');`

`template.innerHTML = ‘`

`<style>`

`…`

`</style>`

`<div class="container footer">`

`<slot id="message" name="message"></slot>&nbsp;`

`<slot name="reference"></slot>`

`<button id="closeButton" class="button">Close</button>`

`<button id= "acceptButton" class="button">Accept</button>`

`</div>`

`‘;`

We added the name attribute to the existing `<slot`> element and added a new slot with `reference` as its name. We want to allow users to specify a formatted markup for the main message of the component, as it happened so far, and to provide a markup intended for a detailed reference to the cookie management policy.

The following is an example of the use of these slots:

`<!DOCTYPE html>`

`<html>`

`<head>`

`<title>Web Components with Webpack Build System</title>`

`<script src="./wc-polyfills/webcomponents-loader.js"></script>`

`<script src="./bundle.js"></script>`

`</head>`

`<body class="container">`

`<h1>Here is your Web Component</h1>`

`<cookie-alert>`

`<span slot="message">We use <b>cookies</b>, but respect your <b>privacy</b>!</span>`

`<span slot="reference">Read our <a href="privacy.html">privacy policy</a></span>`

`</cookie-alert>`

`</body>`

`</html>`

You have two `<span>` elements within the `<cookie-alert> tags`. Each `<span>` element refers to the slots defined in the template. By running the project, you will see the following result:

![](images/Figure_7.2.jpg)

**Figure 7.2**

You see both messages provided by the user. Of course, the user has to provide any related resources, like, for example, the `privacy.html` file specified in the link.

All this works thanks to the slot mechanism. No other code is needed!

# [Conclusion](#toc.xhtml_s99a)

This chapter was devoted to improving the user interface creation both on the web component developer side and on the web component user side.

From the web component developer perspective, we introduced native templates and discovered that they provide us with a declarative approach to define a UI. Native HTML templates also offer an efficient way to render HTML elements. We used the native template approach to redesign the cookie alert component we developed till then.

From the web component user perspective, we discovered that native templates allow them to compose our web components with customized markup. We can enable this composition by using <slot> elements. Slots allow us to define placeholders where the users can add customized markup in a really easy way.

With the feature you learned in this chapter, you will be able to build flexible, efficient, and maintainable UIs for your web component, almost without writing any JavaScript line.

In the next chapter, we will discuss how to package the web components we build to be easily imported and used by other developers. You will learn the different ways to achieve this goal and its benefits and drawbacks.

# [Questions](#toc.xhtml_s100a)

1.  Where can you add an `<template>` element within the markup of an HTML page?
2.  Can you include an element like `<li>` in the markup of a template without any of its parents `<ol> or <ul>?`
3.  What is the difference between using a template and using a string to define the markup of the UI?
4.  What does it mean that the DOM resulting from a template is inert?
5.  How can you activate a template?
6.  Why using a template is more efficient than building the UI via the DOM APIs?
7.  What is a slot?
8.  What is the difference between a named slot and an unnamed slot?
9.  How many unnamed slots can you insert in a template?
10.  What is the default slot?

# [CHAPTER 8](#toc.xhtml_c08)

# [Distributing and Extending Web Components](#toc.xhtml_c08)

In the previous chapters, we learned how to build our Web Components and discovered which are the more appropriate approaches to apply in various development scenarios. The components we build, however, are meant to be used in one or more Web applications or websites by ourselves or by other developers. This leads us to figure out how we can provide our components so that they are easily added to other projects.

To satisfy this requirement, in this chapter, we are going to explore a few ways to share our components so that developers can include them in their projects. We will discuss a script-based strategy and a package-based one. As usual, we will take the cookie alert component we developed throughout the previous chapters as a component example to share with both strategies.

In addition, we will introduce how to create a new Web Component by extending an existing one. This approach allows us to leverage the power of Web Components technologies to get a personalized version of existing components, in a similar way we can do with native HTML elements.

# [Structure](#toc.xhtml_s101a)

*   Distribution srategies
*   Extending components

# [Objectives](#toc.xhtml_s102a)

This chapter will explain to you how to create modules containing the definition of your Web Components and how to use these modules to distribute your components. You will learn how to distribute them as scripts and as packages. You also will learn how to use an existing component to create a new one by leveraging inheritance.

# [Distribution strategies](#toc.xhtml_s103a)

Throughout the book, we used the Web Components Builder project to test the Web Component we were building. That project is just a development environment, and it is useful when we are writing our component and want to see it in an HTML page for evaluation and test purposes.

Once you are satisfied with your component, you would use it in your Web applications or distribute it to other developers. How can you make your brand new Web Component available to other projects and developers?

In this section, we will discuss the various strategies you can use to distribute your Web Components, and for each of these strategies, we will analyze benefits and drawbacks. Of course, we will still use our cookie alert component as the component to distribute.

# [The script-based strategy](#toc.xhtml_s104a)

The first strategy we can use to distribute our cookie alert component is by providing it as a script. This means you have to provide a file with the relevant JavaScript code that implements the component so that the potential user can include it in their project via the `<script>` tag.

Let's take a look at the options we have in distributing our component with this strategy and discuss the pros and cons of this approach.

# [Without building step](#toc.xhtml_s105a)

The simplest way to distribute your Web Component as a script is by providing the source code without any building step. To apply this approach to our cookie alert component, you should simply distribute the `index.js` file under the `src` folder in the Web Components Builder project. Maybe, to make it easier to recognize, you should rename the `index.js` file into cookie-`alert.js,` for example. This way, you can distribute it by allowing users to download it or by making it available via a CDN.

**A Content Delivery Network (CDN), is a distributed network of servers that provide content such as images, scripts, text, or other static resources. The main goal of a CDN is to reduce the workload of websites and application servers and possibly maximize the caching of shared resources.**

Once the user gets the script or the URL to the script hosted in a CDN, they simply have to include that script in their HTML page. For example, the following HTML describes a page that includes the `cookie-alert.js` script and uses the Web Component in its body:

`<!DOCTYPE html>`

`<html>`

`<head>`

`<title>Using the Alert Cookie component</title>`

`<script src="./alert-cookie.js"></script>`

`</head>`

`<body>`

`<h1>Using the Alert Cookie component</h1>`

`<cookie-alert message="We use cookies, but respect your privacy!">`

`</cookie-alert>`

`</body>`

`</html>`

As expected, with this approach, you can use the `<cookie-alert>` tag within your HTML markup.

# [With building step](#toc.xhtml_s106a)

The Web Component Build project allows you to build your component for production, that is, ready to be distributed to users. Compared with the source code distribution approach described in the previous section, the building step offers your script a few advantages.

It transpiles your code into a widely supported version of ECMAScript, typically ECMAScript 5. You may wonder why you should translate your modern JavaScript code into an older version since the user should have a recent browser to support Web Components technologies. Actually, the transpilation step of the building process may be useful if you combine it with polyfills, as described in [chapter 1](#c01.xhtml). This way, you can allow users of older browsers to use your Web Component.

In addition, the building step optimizes your component's code in order to reduce the size of the resulting bundle. This reduces the transfer and load time of your component.

You can obtain the built version of the cookie alert component by running the following command from the root of the Web Component Builder project:

**`npm run build`**

After some seconds, you will find in the `dist` folder of the project a `bundle.js` file. As in the distribution without a building step, you can rename this file into cookie-`alert.js` and provide it to your users via download or CDN.

Your user will be able to use your component the same way as we described in the previous case.

# [Implementing modules](#toc.xhtml_s107a)

The distribution approaches described above seems to work perfectly at first glance. However, they have a few drawbacks.

Let's consider the distribution strategy without a building step. Suppose you want to create an instance of the cookie alert component via JavaScript. You should be able to use the CookieAlert class as in the following example:

`var myCookieAlert = new CookieAlert();`

And actually, it works as expected. However, you are also able to access the template constant that defines the native template the cookie alert component is using. You can try it by simply writing the following code:

`console.log(template);`

In this scenario, you will get an object in the console window instead of a null value.

Also, you can access the `getCookie()` and `setCookie()` functions defined in the `cookie-alert.js` script. This is due to the fact that all these elements are defined as global elements inside the script file.

You might think that this is not a big problem. After all, the component is working as expected. In fact, it is a serious issue. Guess what happens if a user that doesn't know the implementation details of the component defines a global template variable. Arguably, their attempt to define the template variable will fail because a constant with that name already exists. So, the user's code will break due to the inclusion of our cookie alert script. Also, imagine that the user defines their own `getCookie()` function, maybe with a different signature or different behavior. In this case, our component will not work as expected due to the interference with the user's function re-definition.

If you remember the discussion about the Shadow DOM in [chapter 6](#c06.xhtml), here we have a similar problem at the code level. The code of our component affects the user's code, and the code of the user affects the component's code. The premise we made above about the user's knowledge of the implementation details of our component is very important. Not because the user should know how our component works internally, but just because they don't have to know them. Our code does not have to affect the user's code, nor the user's code has to affect our component. The only way the user should have to affect the component's code is through its public interface, which is the set of properties, attributes, events, methods, etc. explicitly designed for this goal.

In other words, we need to encapsulate the code of our component into a module.

Before we go and see how to turn our script into a module, let's take a look at the drawbacks of the distribution strategy with the building step. In this case, we are not able to access the template constant nor the `getCookie()` and `setCookie()` functions. This is good from the encapsulation point of view. Unfortunately, we also are not able to access the `CookieAlert` class, and then we cannot create instances of the component via JavaScript. In this case, we are experiencing the opposite problem to the one we saw for the distribution strategy without a building step: the script exposes nothing to public access.

This behavior depends on the Webpack bundler. It automatically interprets a script as a module. This way, what is not explicitly exported is not accessible outside the module. On the other hand, from the standard ECMAScript point of view, a module is a script that has at least one export or import statement. So, a script without any of these statements is declaring elements in the global context.

So, in summary, in the distribution approach without a building step, all the component's code is global. In this case, it may have interferences with the user's code. In the approach with a building step, all the component's code is private, so the user is not able to leverage our component via JavaScript.

Let's see how we can fix both problems by implementing our component as a standard ECMAScript module. The only change we should apply to the script containing the component definition is to prefix the class definition with the export default statement. The script file content for the cookie alert component will look like the following:

`const template = document.createElement('template');`

`template.innerHTML = ‘…‘;`

`export default class CookieAlert extends HTMLElement {`

`// …`

`}`

`customElements.define("cookie-alert", CookieAlert);`

`function getCookie(cookieName) {`

`// …`

`}`

`function setCookie(cookieName, cookieValue, expirationDays) {`

`// …`

`}`

We defined the `CookieAlert` class as the default exported item of the current module.

However, if we try to include this new version of the component script with the `<script>` tag as above, we will get an error about the `export` statement. Actually, the `<script>` tag doesn't support modules by default. In order to enable it to include modules in an HTML page, you have to specify it through the type attribute. So, the correct way to import the modularized version of the cookie alert component is as shown here:

`<script type="module" src="./cookie-alert.js"></script>`

From now on, you can use the `CookieAlert` class from any JavaScript module by importing it and creating your instance, as shown in the following example:

`import CookieAlert from './cookie-alert.js'`

`var myCookieAlert = new CookieAlert();`

**Keep in mind that you can import the items exported by a module only from within another module. An attempt to import items from a module when your code is within a <script> tag without the type="module" attribute will throw an error.**

# [The package-based strategy](#toc.xhtml_s108a)

The script-based strategy is a good approach for an HTML-centric application or website. However, modern Web application development uses a JavaScript-first approach. Consider the **Single Page Application (SPA)** architecture: it uses one HTML page whose content is generated at runtime by JavaScript code. This is the approach supported by most JavaScript frameworks and libraries, like React, Angular, Vue, etc. But it is also applicable to vanilla JavaScript. With this approach, an HTML page is just the anchor to attach the application JavaScript code to the browser. Most of the logic, UI, and infrastructure of the application itself is provided by JavaScript code.

In this context, a building toolchain is essential, and in the vast majority of cases, the development environment is based on the Node.js runtime. As you know, in this environment, the usual approach to add an external component or library is to use packages to be installed by package managers like `npm` or yarn. So, imagine we want to provide our users with the cookie alert component as a package. How can we accomplish this? Let's find out together.

# [Leveraging the GitHub repository](#toc.xhtml_s109a)

The simplest way to package and distribute your component with other developers is by sharing it through a GitHub repository. This approach allows you to share the source code of your project but also to let other developers use `npm` in order to install your component into their projects. Let's take a look at how it works.

Once prepared, your code to be published on a GitHub repository, ensure your `package.json` file is correctly configured. The following is an example of `package.json` file for our alert cookie component:

`{`

`"name": "cookie-alert-demo",`

`"version": "1.0.0",`

`"description": "A Web Component that allows you to display your message about your cookie policy.",`

`"main": "src/index.js",`

`"scripts": {`

`"start": "webpack-dev-server --config ./webpack.config.js --mode development",`

`"build": " node node_modules/.bin/webpack --mode production",`

`"test": "echo \"Error: no test specified\" && exit 0"`

`},`

`"keywords": [],`

`"author": "Andrea Chiarelli (https://www.andreachiarelli.it)",`

`"license": "MIT",`

`"devDependencies": {`

`"webpack": "^4.41.2",`

`"webpack-cli": "^3.3.9",`

`"webpack-dev-server": "^3.8.2",`

`"copy-webpack-plugin": "^5.0.4"`

`},`

`"dependencies": {`

`"@webcomponents/webcomponentsjs": "^2.3.0"`

`}`

`}`

Let's highlight the most important items. Give your package a meaningful name and a description. Also, assign a version and keep it updated with future changes you will apply to your code.

**The name and version are required fields in the** `package.json` **file in order to publish your package.**

**The name needs to follow a few rules:**

**- it must be unique**

**- its maximum length is 214 characters**

**- it cannot start with a dot or an underscore**

**- it cannot have uppercase letters**

Then, set the main property pointing to the entry point file of your project. If your project consists of just one file, set the path to it. In the example, we specified the path to the `index.js` file under the `src` folder. The other settings are the ones needed for development purposes.

With these simple adjustments, our users will be enabled to install our component as a package by simply typing an `npm install` command. For example, to install our alert cookie component from the GitHub repository published at **[https://github.com/andychiare/cookie-alert-demo](https://github.com/andychiare/cookie-alert-demo)**, the user has to type:

**`npm install andychiare/cookie-alert-demo`**

As you may notice, the user has just to specify the GitHub organization and the repository name.

Once the code is installed in the `node_modules` folder, the user can import the component as a standard package. For example, the component can be dynamically attached to the body of the HTML page as follows:

`import CookieAlert from 'cookie-alert-demo';`

`const cookieAlert = new CookieAlert();`

`document.body.appendChild(cookieAlert);`

# [Publishing in the public npm registry](#toc.xhtml_s110a)

If you want to publish your component into the official `npm registry,` you need to have an account and login to the registry before publishing it. The command to login is as follows:

`npm login`

You will be required to provide your user name, password, and e-mail. After you logged in, you can publish the package by simply typing the following command from the root of the component's project:

**`npm publish`**

This command will publish the package containing your component into the npm `registry`. After publishing, you can verify your package by checking its public URL in the form **https://www.npmjs.com/package/<package-name>, where <package-name>** is the name of your package.

In this case, the user of your component will easily install this package by typing:

**`npm install package-name`**

Of course, the way your component will be used in the target project is the same as we saw in the GitHub repository case.

# [Extending Web Components](#toc.xhtml_s111a)

We have seen so far how to create our Web Component, how to make it available to other developers, and how to use it in your HTML markup or JavaScript application.

As you've seen, using a Web Component is pretty straightforward: you can deal with it as if it were a native HTML element. This very simple concept has some very interesting implications. In fact, as you can do with any native HTML element, you can create your own Web Component by extending an existing Web Component. Let's take a look at how it works.

# [Defining an extended Web Component](#toc.xhtml_s112a)

Consider the cookie alert component that we implemented so far. We want to create a variant of this component that has a property and an attribute that allows us to show or hide the `Close` button.

We can create a new project by cloning and initializing the Web Component Builder project. Then, we can add the `cookie-alert-demo` Web Component to the project by running the following command:

**`npm install andychiare/cookie-alert-demo`**

Finally, we implement this new component as follows:

`import CookieAlert from 'cookie-alert-demo';`

`class MyCookieAlert extends CookieAlert {`

`constructor() {`

`super();`

`this._hasCloseButton = false;`

`}`

`get hasCloseButton() {`

`return this._hasCloseButton;`

`}`

`set hasCloseButton(value) {`

`this._hasCloseButton = value;`

`this.setAttribute("closebutton", value);`

`this.toggleCloseButton(value);`

`}`

`toggleCloseButton(visible) {`

`const closeButton = super.shadowRoot.getElementById("closeButton");`

`closeButton.style.display = (visible?` `"block": "none");`

`}`

`static get observedAttributes() {`

`return ["closebutton"];`

`}`

`attributeChangedCallback(name, oldValue, newValue) {`

`if (oldValue !== newValue) {`

`if (name == "closebutton") {`

`let isVisible = (newValue === "true" || newValue === "");`

`this._hasCloseButton = isVisible;`

`this.toggleCloseButton(isVisible);`

`}`

`}`

`}`

`connectedCallback() {`

`super.connectedCallback();`

`this.toggleCloseButton(this._hasCloseButton);`

`}`

`}`

`customElements.define("my-cookie-alert", MyCookieAlert);`

Let's analyze each part of this code. The first line imports the `CookieAlert` class from the `cookie-alert-demo` module. The `MyCookieAlert` class definition inherits from this `CookieAlert` class. This is the main point: instead of inheriting from the `HTMLElement` class, as usual, we are building a new Web Component starting from the cookie alert component. The rest of the code should be easily understandable now.

The `MyCookieAlert` class constructor calls `super()` and initializes the internal property `_hasCloseButton` with the false value:

`constructor() {`

`super();`

`this._hasCloseButton = false;`

`}`

This means that this variant of the cookie alert component shouldn't show the `Close` button, by default. Then, we have the definition of the getter and setter of the `hasCloseButton` property:

`get hasCloseButton() {`

`return this._hasCloseButton;`

`}`

`set hasCloseButton(value) {`

`this._hasCloseButton = value;`

`this.setAttribute("closebutton", value);`

`this.toggleCloseButton(value);`

`}`

The setter calls the `toggleCloseButton()` method to change the button visibility. This method interacts with the shadow DOM of the base component to manage the button visibility:

`toggleCloseButton(visible) {`

`const closeButton = super.shadowRoot.getElementById("closeButton");`

`closeButton.style.display = (visible?` `"block": "none");`

`}`

As you can see, the visibility of the Close button changes based on the boolean passed as a parameter. Notice the use of super to access the Shadow DOM of the base class. Of course, this is possible because the cookie alert's Shadow DOM has been defined as open.

Then, we observe the `closebutton` attribute and manage its value changes:

`static get observedAttributes() {`

`return ["closebutton"];`

`}`

`attributeChangedCallback(name, oldValue, newValue) {`

`if (oldValue !== newValue) {`

`if (name == "closebutton") {`

`let isVisible = (newValue === "true" || newValue === "");`

`this._hasCloseButton = isVisible;`

`this.toggleCloseButton(isVisible);`

`}`

`}`

`}`

Notice how we deal with the value of the `closebutton` attribute. It should be a boolean value. But we know that attribute values are always strings. So we need to compare its value with the true string. Any different value is interpreted as false. In addition, we want that no value for the attribute equals to the true value. We will clarify this point in a minute when we will see how to use this new component.

The `connectedCallback()` reaction invokes the same method of its base class and sets the button visibility following the value of the internal property _hasCloseButton:

`connectedCallback() {`

`super.connectedCallback();`

`this.toggleCloseButton(this._hasCloseButton);`

`}`

The invocation of the super.`connectedCallback()` method is necessary because this initializes the base component. If you don't invoke it, you are overriding the initialization, so you will not get the UI of the base component or will get it incomplete.

The last step, of course, is the registration step of the `MyCookieAlert` Web Component:

customElements.define("my-cookie-alert", `MyCookieAlert`);

As you can see, we define the `my-cookie-alert` tag and bind it to the `MyCookieAlert` class. Now we are ready to use this new Web Component.

# [Using an extended Web Component](#toc.xhtml_s113a)

The following markup shows the very basic use of the `my-cookie-alert tag:`

`<!DOCTYPE html>`

`<html>`

`<head>`

`<title>Web Components with Webpack Starter Kit</title>`

`<script src="./wc-polyfills/webcomponents-loader.js"></script>`

`<script src="./bundle.js"></script>`

`</head>`

`<body class="container">`

`<h1>Here is your Web Component</h1>`

`<my-cookie-alert></my-cookie-alert>`

`</body>`

`</html>`

Since the default value of the `closeButton` attribute is false, we will get the version of the cookie alert component without the `Close` button, as shown by the following screenshot:

![](images/Figure_8.1.jpg)

**Figure 8.1**

If you want the `Close` button to be shown, you should simply add the `closebutton` attribute with the true value, as in the following example:

`<my-cookie-alert closebutton="true"></my-cookie-alert>`

This way, you will get the usual cookie alert as you have known so far.

![](images/Figure_8.2.jpg)

**Figure 8.2**

In the management of the `closebutton` attribute's value, we stated that an empty string value has the same meaning of the true value. This allows us to use the attribute as a toggle attribute, as it happens with many native attributes like, for example, enabled or checked. So, you can get the same result of assigning the true value to the `closebutton` attribute in the following way:

`<my-cookie-alert closebutton></my-cookie-alert>`

To complete the overview of this component, remember that the following markup has the same meaning of using no `closebutton` attribute:

`<my-cookie-alert closebutton="false"></my-cookie-alert>`

As usual, you can get the same result seen so far by using the `hasCloseButton` property via JavaScript. For example, the following code forces showing the Close button:

`const myCookieAlert = document.querySelector("my-cookie-alert");`

`myCookieAlert.hasCloseButton = true;`

# [Conclusion](#toc.xhtml_s114a)

This chapter showed you how to prepare your Web Components in order to be shared with other developers. We explored how to create modules that contain your code and how to distribute them via script-based and package-based approaches.

These approaches can be used in different development contexts. But regardless of the specific approach to distribute your components, the users can create new components based on yours. In fact, they can extend the class that defines your component to create a personalized version of it.

With the notions you learned in this chapter, you are now able to distribute your Web Components and to create new components by extending existing ones.

In the next chapter, we will discuss how to use Web Components within applications built with well-known JavaScript libraries and frameworks like React, Angular, and Vue.

# [Questions](#toc.xhtml_s115a)

1.  What are the main drawbacks of distributing your Web Component as a traditional script?
2.  What are the main benefits of applying a building step to your code before distributing your component?
3.  How can you overcome the drawbacks of distributing your Web Component as a traditional script?
4.  How can you convert the code of your Web Component into a module?
5.  How can you import a module with the `<script>` tag?
6.  Why you need a package for distributing your Web Component?
7.  What are the minimum `package.json` fields for publishing your `npm package?`
8.  How can you share your GitHub repository as an `npm` `package`?
9.  How can you install an npm package from a GitHub repository?
10.  How can you publish your `npm` package on the public npm registry?
11.  How can you extend an existing Web Component?

# [CHAPTER 9](#toc.xhtml_c09)

# [Web Components and Other UI Frameworks](#toc.xhtml_c09)

Throughout this book, you learned that the technologies that are behind Web Components allow you to customize standard HTML elements and create custom HTML elements. When we introduced them in *[Chapter 1, Getting Started with Web Components](#c01.xhtml), we said that one of the main advantages of Web Components* is their interoperability. That is the ability to work in an HTML page or web application regardless of the library or framework you are using to build your UI. This is a great advantage that allows you to create universal UI components and use them the same way you are using HTML elements.

In this chapter, we are going to show a few practical examples of how this interoperability between Web Components and UI frameworks happens. We will see how to integrate them in *React, Angular*, and Vue applications with very little effort. We will also take a look at some directions on how to create web components by writing them in *Angular, Vue,* and *React*.

# [Structure](#toc.xhtml_s116a)

*   Web Components integration
*   Web Components and React
*   Web Components and Angular
*   Web Components and Vue
*   Building Web Components with UI Frameworks

# [Objectives](#toc.xhtml_s117a)

The goal of this chapter is to demonstrate how to integrate Web Components in websites and applications built with JavaScript UI frameworks.

You will learn how to use your components in applications created with *React, Angular,* and *Vue*. You also will discover how to wrap a component built with these frameworks in a custom element.

# [Web Components integration](#toc.xhtml_s118a)

The HTML elements you build with Web Components technologies work as standard HTML elements. This means that wherever you can use an HTML element, you can use a Web Component. This possibility leads to an awesome feature - no matter the library you are using for your web application or website, you can use your web component everywhere. Interoperability is the amazing main advantage of Web Components.

Unlike components created with *React, Angular, Vue*, and similar, Web Components are not tied to a specific library or framework. For example, if you create a UI component with React, you can use this component only in a React-based application. A web component can be easily integrated into applications based on virtually any UI library. This frees you from re-implement the same component for different component libraries, as we will see later on.

**Libraries and frameworks are different things. A library is a group of functions focused on a specific programming feature that an application can invoke. A framework is a set of functions supporting different aspects of application development. Despite these differences, we will talk about libraries and frameworks interchangeably.**

Before going into the details of Web Components integration, keep in mind that Web Components are not another UI framework - they are the native UI framework. Web Components are not an alternative to existing UI frameworks - they can live together. You don’t need to switch to Web Components and drop your UI framework. You can introduce them to your applications as you need them. Web Components are framework agnostic - they can be integrated into any framework. Write once; use everywhere.

To demonstrate in practice how to use a web component within applications built with UI JavaScript frameworks, we are going to integrate the cookie alert component we created in the previous chapters with applications built with *React, Angular,* and *Vue.*

**In the following sections, we assume you are familiar with React, Angular, or Vue. If not, please refer to the official documentation for more information on these frameworks.**

# [Web Components and React](#toc.xhtml_s119a)

Let’s start to see how to use our cookie demo component in a simple React application. We are going to use the `create-react-app` tool to create a basic application. So, type the following command in a terminal window:

`npx create-react-app react-app-cookie-alert`

This command will create a simple but working React application in the `react-app-cookie-aler`t folder. After a few seconds, the application will be ready to run. To make available our cookie alert component to the application, you need to install it. So, move to the `react-app-cookie-alert` folder and type the following command:

`npm install andychiare/cookie-alert-demo`

As you know from the previous chapter, this installs the `cookie-alert-demo` package directly from the component `GitHub` repository. Now, to import and use the component in the React application, edit the `src/App.js` file and change its content as follows:

`import React from 'react';`

`import logo from './logo.svg';`

`import './App.css';`

`import 'cookie-alert-demo';`

`function App() {`

`return (`

`<div className="App">`

`<header className="App-header">`

`<img src={logo} className="App-logo" alt="logo" />`

`<p>`

`Edit <code>src/App.js</code> and save to reload.`

`</p>`

`<a`

`className="App-link"`

`href="https://reactjs.org"`

`target="_blank"`

`rel="noopener noreferrer"`

`>`

`Learn React`

`</a>`

`</header>`

`<cookie-alert></cookie-alert>`

`</div>`

`);`

`}`

`export default App;`

The new code added to the existing one is highlighted above. You imported the cookie alert module and added the `<cookie-alert>` tag in the JSX code returned by the App component. That’s all!

You are just using the web component like any standard HTML component. To take a look at the resulting UI, run the `npm` start command and point your browser to the `http://localhost:3000` address. You will get a page like the following:

![](images/Figure_9.1.jpg)

**Figure 9.1**

As you see, you have the cookie alert at the bottom of the page as it happened with standard HTML pages, and it works as expected.

Of course, you may want to customize the cookie alert within your React application. For example, you may want to change the default message. You can achieve this by assigning the new `message` string to the message attribute of the component, as you would do within any HTML page. However, your message could be created at runtime, and you may wonder how to assign this value to the attribute. The following code shows how you can assign a constant value to the `message` attribute:

`import React from 'react';`

`import logo from './logo.svg';`

`import './App.css';`

`import 'cookie-alert-demo';`

`function App() {`

`const message = "We use cookies, but respect your privacy!";`

`return (`

`<div className="App">`

`<header className="App-header">`

`<img src={logo} className="App-logo" alt="logo" />`

`<p>`

`Edit <code>src/App.js</code> and save to reload.`

`</p>`

`<a`

`className="App-link"`

`href="https://reactjs.org"`

`target="_blank"`

`rel="noopener noreferrer"`

`>`

`Learn React`

`</a>`

`</header>`

`<cookie-alert message={message}></cookie-alert>`

`</div>`

`);`

`}`

`export default App;`

You assigned the expression containing the message constant to the attribute with the same name, as you would have done with any `prop` assignment in React. Of course, you can assign any valid expression returning a string to the `message` attribute of the cookie alert component.

If you want to customize the cookie alert component by accessing the `message` property via JavaScript, you need to write a bit more code. You need to access the component by using `refs`.

**In React, refs provide a mechanism to access DOM nodes or React elements generated by the** `render()` **method of a component. They represent a sort of shortcoming to use in specific situations, like the one we are discussing.**

Take a look at the following code to see how to access the `message` property via a `ref`:

`import React, {useRef, useEffect} from 'react';`

`import logo from './logo.svg';`

`import './App.css';`

`import 'cookie-alert-demo';`

`function App() {`

`const cookieAlert = useRef(null);`

`useEffect(() => {`

`cookieAlert.current.message = "We use cookies, but respect your privacy!";`

`});`

`return (`

`<div className="App">`

`<header className="App-header">`

`<img src={logo} className="App-logo" alt="logo" />`

`<p>`

`Edit <code>src/App.js</code> and save to reload.`

`</p>`

`<a`

`className="App-link"`

`href="https://reactjs.org"`

`target="_blank"`

`rel="noopener noreferrer"`

`>`

`Learn React`

`</a>`

`</header>`

`<cookie-alert ref={cookieAlert}></cookie-alert>`

`</div>`

`);`

`}`

`export default App;`

You imported the `useRef()` and `UseEffect()` hooks. Then, you created the `cookieAlert` ref by using the `useRef()` hook and used this `ref` in effect defined with the `useEffect()` hook. In the markup, you notice that we added the `ref` property to our cookie alert component and assigned the `cookieAlert` ref created before.

Finally, the effect created above uses the `cookieAlert` ref to get access to the cookie alert component through its `current` property. At this point, we can assign the string we want to display to the `message` property.

You can apply the same approach to handle events generated by the cookie alert component. The following code shows how to add an event handler for the `accepted` event:

`useEffect(() => {`

`cookieAlert.current.message = "We use cookies, but respect your privacy!";`

`cookieAlert.current.addEventListener("accepted", () => alert("Thanks for accepting our cookie policy!"));`

`});`

As you can see, you add the event listener within the effect created before.

Even if using Web Components within a React application is possible, you cannot expect that they follow the declarative programming model of this popular library. Web Components use the typical approach of DOM programming, which is typically imperative. So, when using Web Components in your React application, you shouldn’t expect that they work as React components. For example, events generated by Web Components may not properly propagate in a React component structure. Also, the typical reactiveness of React components is not guaranteed.

Also, React wraps a standard HTML element with a component to get an integrated behavior in its ecosystem. If you want to get the same result, you should wrap your web component with a React component on your own, as we will see later on.

# [Web Components and Angular](#toc.xhtml_s120a)

Using a web component in an Angular application requires an approach similar to the one we saw for React. However, here there are a few specific steps. So, let’s see how it works by building an Angular sample application and using our cookie alert component.

As for React, also with Angular, we are going to use a tool that helps us to set up a simple application quickly. We are going to use Angular CLI, so make sure you have it installed, and otherwise install it with the following command:

`npm install -g @angular/cli`

Once you installed the CLI, create a minimal Angular application by running the following command:

`ng new angular-app-cookie-alert --minimal --routing=false --style=css`

This command creates a very minimal application in the `angular-app-cookie-`alert folder. Even if it is minimal, it is enough for our demonstration.

Move to the `angular-app-cookie-alert` folder and type the following command to install our cookie alert component:

`npm install andychiare/cookie-alert-demo`

At this point, you should be aware of one issue. Our cookie alert component is written in JavaScript, while the default language of the Angular application is TypeScript. So, to avoid errors, you should add the "`allowJs`": true setting as a TypeScript compiler option in the `tsconfig.json` configuration file. Your `tsconfig.json` file should be similar to the following:

`{`

`"compileOnSave": false,`

`"compilerOptions": {`

`"allowJs": true,`

`"baseUrl": "./",`

`…other options…`

`},`

`"angularCompilerOptions": {`

`…other options…`

`}`

`}`

Before using our web component in the Angular application, you need to make another little adjustment. In fact, by default, Angular will attempt to interpret any non-standard HTML element as an Angular component. So, it will throw an error when it finds the `<cookie-alert>` tag. To avoid this, you need to enable custom elements.

For this purpose, open the `src/app/app.module.ts` file and change its content as follows:

`import { BrowserModule } from '@angular/platform-browser';`

`import { NgModule, CUSTOM_ELEMENTS_SCHEMA } from '@angular/core';`

`import { AppComponent } from './app.component';`

`@NgModule({`

`declarations: [`

`AppComponent`

`],`

`imports: [`

`BrowserModule`

`],`

`schemas: [CUSTOM_ELEMENTS_SCHEMA],`

`providers: [],`

`bootstrap: [AppComponent]`

`})`

`export class AppModule { }`

Following the highlighted items, you import the `CUSTOM_ELEMENTS_SCHEMA` module and configure it as the reference schema for the application.

Now we are ready to use our web component in this application.

Let’s start to see how to use the cookie alert component in the template of the `AppComponent` component. Edit the `src/app/app.component.`ts file changing its content as follows:

`import { Component } from '@angular/core';`

`import 'cookie-alert-demo';`

`@Component({`

`selector: 'app-root',`

`template: ‘`

`<!--The content below is only a placeholder and can be replaced.-->`

`<div style="text-align:center" class="content">`

`<h1>`

`Welcome to {{title}}!`

`</h1>`

`…`

`</div>`

`<h2>Here are some links to help you start: </h2>`

`<ul>`

`…`

`</ul>`

`<cookie-alert></cookie-alert>`

`‘,`

`styles: []`

`})`

`export class AppComponent {`

`title = 'angular-app-cookie-alert';`

`}`

In this simple first step, you imported the `cookie-alert-demo` module and used the `<cookie-alert>` tag in the template of the Angular `Component`. As in the React case, also here you are using the cookie alert component like it is a standard HTML element.

To see the component in action, run ng serve in a terminal window and point your browser to the `http://localhost:4200` address. You should see a page like the following:

![](images/Figure_9.2.jpg)

**Figure 9.2**

As expected, the alert appears at the bottom of the page and works as usual.

As we did with React, let’s take a look at how to customize the alert message by using different approaches. Assigning a value to the `message` attribute is the easiest way. This code shows how to apply this basic approach:

`import { Component } from '@angular/core';`

`import 'cookie-alert-demo';`

`@Component({`

`selector: 'app-root',`

`template: ‘`

`//…`

`<cookie-alert message="We use cookies, but respect your privacy!"></cookie-alert>`

`‘,`

`styles: []`

`})`

`export class AppComponent {`

`title = 'angular-app-cookie-alert';`

`}`

Nothing special, as you can see. But what if you want to assign a computed value as the text to show in the alert? Consider the following example:

`import { Component } from '@angular/core';`

`import 'cookie-alert-demo';`

`@Component({`

`selector: 'app-root',`

`template: ‘`

`//…`

`<cookie-alert [message]="cookieMessage"></cookie-alert>`

`‘,`

`styles: []`

`})`

`export class AppComponent {`

`title = 'angular-app-cookie-alert';`

`cookieMessage = 'We use cookies, but respect your privacy!';`

`}`

Here, you create a `cookieMessage` property for the `AppComponent` component and assign your text. Then, you map this `cookieMessage` property to the message property of the cookie alert component in the template’s markup. Notice how you are seamlessly using the Angular binding syntax.

To handle events generated by the web component, take a look at the following code:

`import { Component } from '@angular/core';`

`import 'cookie-alert-demo';`

`@Component({`

`selector: 'app-root',`

`template: ‘`

`//…`

`<cookie-alert`

`[message]="cookieMessage"`

`(accepted)="showThanks()">`

`</cookie-alert>`

`‘,`

`styles: []`

`})`

`export class AppComponent {`

`title = 'angular-app-cookie-alert';`

`cookieMessage = 'We use cookies, but respect your privacy!';`

`showThanks() {`

`alert("Thanks for accepting our cookie policy!");`

`}`

`}`

You define the `showThanks()` method for the `AppComponent` component and assign it to the `accepted` event. Notice how even in this case, you are using the Angular binding syntax as usual.

Remember that, if you need to access the event’s details, you can use the $event object in the `showThanks()` method as in the ordinary Angular way.

You need to pay attention when using web components that are meant to be used in Angular forms. Consider, for example, the case where you have a custom input element created as a web component and you want to use it in a form, like in the following example:

`<form [formGroup]="form" (ngSubmit)="send()">`

`<custom-input`

`type="text"`

`label="Enter your data">`

`</custom-input>`

`<input type="submit" value="Submit">`

`</form>`

In this example, we are using the fictitious `<custom-input>` web component within an Angular form. By default, Angular enriches a standard HTML `input` element to enable it to interact with its forms API. Angular forms look for a `value accessor` in its child elements, that is, a feature that allows you to access the control’s value. A va`lue accessor` is a directive implementing the `ControlValueAccessor` interface and allows a native HTML element to communicate with the Angular form. For this reason, Angular manipulates the standard HTML elements by attaching this `value accessor.`

However, Angular doesn’t know anything about your web component. So, you need to add a `value accessor` to your component on your own. This basically means to add the `ngDefaultControl` directive to your component, as shown in the following code:

`<form [formGroup]="form" (ngSubmit)="send()">`

`<custom-input`

`type="text"`

`label="Enter your data"`

`ngDefaultControl>`

`</custom-input>`

`<input type="submit" value="Submit">`

`</form>`

With this simple change, your web component integrates with Angular forms.

# [Web Components and Vue](#toc.xhtml_s121a)

Let’s see how to use Web Components in a Vue application by using the cookie alert component, as we already showed with React and Angular.

Even in this case, we are going to use a tool to set up a Vue application quickly - Vue CLI. Make sure you have it installed, otherwise install it with the following command:

`npm install -g @vue/cli`

To create a basic application, run the following command in a Terminal window:

`vue create vue-app-cookie-alert --default`

After the command executed, you will find the `vue-app-cookie-alert` folder containing the code of the Vue application. So, as usual, install the cookie alert package by typing the following command:

`npm install andychiare/cookie-alert-demo`

Similarly, to the Angular case, Vue would attempt to consider non-standard elements like Vue components. Of course, this will lead to errors, since the compiler will not find a Vue component implementing the `<cookie-alert>` tag. So, you need to tell Vue that the `<cookie-alert>` element has to be ignored. To achieve this result, open the `src/main.js` file and update its content as shown in the following code snippet:

`import Vue from 'vue'`

`import App from './App.vue'`

`Vue.config.productionTip = false`

`Vue.config.ignoredElements=[`

`'cookie-alert'`

`]`

`new Vue({`

`render: h => h(App),`

`}).$mount('#app')`

You added the `cookie-alert` tag name in the list of the ignored elements of Vue’s configuration.

Now, open the `src/App.vue` component and change the content of the template and script sections as shown by the following code:

`<template>`

`<div id="app">`

`<img alt="Vue logo" src="./assets/logo.png">`

`<HelloWorld msg="Welcome to Your Vue.js App"/>`

`<cookie-alert></cookie-alert>`

`</div>`

`</template>`

`<script>`

`import HelloWorld from './components/HelloWorld.vue'`

`import 'cookie-alert-demo'`

`export default {`

`name: 'App',`

`components: {`

`HelloWorld`

`}`

`}`

`</script>`

`<style>`

`#app {`

`font-family: Avenir, Helvetica, Arial, sans-serif;`

`-webkit-font-smoothing: antialiased;`

`-moz-osx-font-smoothing: grayscale;`

`text-align: center;`

`color: #2c3e50;`

`margin-top: 60px;`

`}`

`</style>`

In the script section, you imported the `cookie-alert-demo` module. In the template section, you simply used the `<cookie-alert>` tag.

To see the effect of these changes, run the `npm run serve` command and point your browser to the `http://localhost:8080` address. You will see a page similar to the following:

![](images/Figure_9.3.jpg)

**Figure 9.3**

Customizing the cookie alert component is as easy as in the Angular case. To assign a different text message, you can set the desired value to the `message` attribute of the component, as shown in the following snippet:

`<template>`

`<div id="app">`

`<img alt="Vue logo" src="./assets/logo.png">`

`<HelloWorld msg="Welcome to Your Vue.js App"/>`

`<cookie-alert message= "We use cookies, but respect your privacy!"></cookie-alert>`

`</div>`

`</template>`

`//…`

If you want to assign a value to the `message` property of the cookie alert component, you can do it as shown in the following example:

`<template>`

`<div id="app">`

`<img alt="Vue logo" src="./assets/logo.png">`

`<HelloWorld msg="Welcome to Your Vue.js App"/>`

`<cookie-alert :message= "cookieMessage"></cookie-alert>`

`</div>`

`</template>`

`<script>`

`import HelloWorld from './components/HelloWorld.vue'`

`import 'cookie-alert-demo'`

`export default {`

`name: 'App',`

`components: {`

`HelloWorld`

`},`

`data: function() {`

`return {`

`cookieMessage: 'We use cookies, but respect your privacy!'`

`}`

`}`

`}`

`</script>`

`//…`

In this example, you created a `cookieMessage` property for the App component and assigned it to the message property using the typical Vue binding syntax.

Similarly, to handle the accepted event of the cookie alert component, add a `showThanks()` method to the App component and assign it to the `accepted` event by using the @ prefix. The following code shows the code:

`<template>`

`<div id="app">`

`<img alt="Vue logo" src="./assets/logo.png">`

`<HelloWorld msg="Welcome to Your Vue.js App"/>`

`<cookie-alert :message= "cookieMessage" @accepted="showThanks"></cookie-alert>`

`</div>`

`</template>`

`<script>`

`import HelloWorld from './components/HelloWorld.vue'`

`import 'cookie-alert-demo'`

`export default {`

`name: 'App',`

`components: {`

`HelloWorld`

`},`

`data: function() {`

`return {`

`cookieMessage: 'We use cookies, but respect your privacy!'`

`}`

`},`

`methods: {`

`showThanks: function() {`

`alert("Thanks for accepting our cookie policy!");`

`}`

`}`

`}`

`</script>`

`//…`

As you can see, also in Vue, using a web component is pretty straightforward.

# [Building web components with UI Frameworks](#toc.xhtml_s122a)

The previous section guided you in using web components within applications built with three popular UI frameworks - *React, Angular*, and *Vue*. We saw how integrating web components with these frameworks are, in general, pretty easy. But also we saw you have to take care of a few caveats to tackle some issues depending on the specific framework.

You could face these issues more organically by applying a general strategy. For example, you could wrap your web component with a *React, Angular,* or *Vue* component. This way, you encapsulate the integration issues right in the framework component definition, offering a better integration experience. But this doesn’t change the general approach in integrating Web Components with other UI frameworks.

Some UI frameworks provide a way to create web components using their syntax and semantics instead of directly using JavaScript and the DOM. You might ask why. Here are a couple of possible reasons:

*   **Leverage the UI framework features:** If you decide to create a web component using a UI framework, say Angular, you can leverage your Angular knowledge and the features that the framework provides you. This may simplify the development and, to an extent, avoid you knowing the details about implementing web components.
*   **Distributing a framework-based component**: Suppose you have a Vue component and want to make it available to other non-Vue applications. You can create your web component by using Vue and distribute it. You are wrapping your Vue component in a web component.

These may be two possible reasons to use one of the most popular UI frameworks to create your web component. However, you should be aware of at least the following caveats:

*   **Increasing complexity:** Applying a layer of abstraction above the Web Components technologies adds complexity. You may experience issues due to different ways of managing things. And you may have performance issues due to this extra layer.
*   **Adding dependency:** The UI framework you use to implement the web component becomes a dependency, even if it may include just a subset of the framework itself. Imagine what may happen if an application has multiple web components built with different libraries.

So, even if it is possible to create web components or wrap existing framework-based components, ask yourself if this is a good choice for your purposes.

In the following sections, we will take a quick look at how to create web components by using *React, Angular*, and Vue. The examples we will provide are very simple. They are not intended to be exhaustive, but they should just give a basic idea of the general approach you can use to build your web components with these frameworks.

# [Building Web Components with React](#toc.xhtml_s123a)

Creating a web component using React is a matter of wrapping a React component within a standard class that extends `HTMLElement` and registering the associated tag name. Let’s see how to define a wrapper around a basic React component like the following:

`import React from 'react';`

`function MyComponent() {`

`return (`

`<div>I am the component!</div>`

`);`

`}`

`export default MyComponent;`

This code defines an elementary React component - it merely shows a `<div>` with a text.

You can wrap this component in a web component definition as follows:

`import React from 'react';`

`import ReactDOM from 'react-dom';`

`import MyComponent from './MyComponent';`

`class MyComponentWC extends HTMLElement {`

`connectedCallback() {`

`this.mountReactComponent();`

`}`

`disconnectedCallback() {`

`ReactDOM.unmountComponentAtNode(this.mountPoint);`

`}`

`mountReactComponent() {`

`if (!this.mountPoint) {`

`this.mountPoint = document.createElement('div');`

`this.attachShadow({ mode: 'open' }).appendChild(this.mountPoint);`

`}`

`ReactDOM.render(<MyComponent />, this.mountPoint);`

`}`

`}`

`window.customElements.define('my-component', MyComponentWC);`

As you can see, this is a standard definition for the custom element `MyComponentWC`. You find the class definition that extends the `HTMLElement` class and the registration of the `my-component` tag name.

The interesting thing happens in the class definition. You see that the `conncectedCallback()` reaction invokes the `mountReactComponent()` method. This method takes care of mounting the `MyComponent` React component into the DOM. If a mount point doesn’t exist, it creates one as a <div> and attaches the shadow DOM to it. Then, it renders the React component at the mount point.

The `disconnectedCallback()` reaction will unmount the React component from the mount point.

# [Building Web Components with Angular](#toc.xhtml_s124a)

To create web components with Angular, you can leverage the Angular elements module, as you will see in a minute. Let’s say you have the following Angular component implemented in the `src/app/my-component/my-component.component.ts` file:

`import { Component, OnInit } from '@angular/core';`

`@Component({`

`selector: 'app-my-webcomponent',`

`templateUrl: './my-webcomponent.component.html',`

`styleUrls: ['./my-webcomponent.component.css']`

`})`

`export class MyWebcomponentComponent implements OnInit {`

`constructor() { }`

`ngOnInit() {`

`}`

`}`

You need to add the Angular Elements package to your project by running the following command:

`ng add @angular/elements`

Then, change the code in `app.module.ts as` follows:

`import { BrowserModule } from '@angular/platform-browser';`

`import { NgModule, Injector } from '@angular/core';`

`import { createCustomElement } from '@angular/elements';`

`import { MyComponentComponent } from './my-component/my-component.component';`

`@NgModule({`

`declarations: [`

`MyComponentComponent`

`],`

`imports: [`

`BrowserModule`

`],`

`providers: [],`

`entryComponents: [MyComponentComponent]`

`})`

`export class AppModule {`

`constructor(injector: Injector) {`

`const el = createCustomElement(MyComponentComponent, { injector });`

`customElements.define('my-component', el);`

`}`

`ngDoBootstrap() {}`

`}`

You imported the `createCustomElement()` function from the Angular elements module and the Angular component shown above. Then, you declared `MyComponentComponent` as the entry point of the project and defined the constructor for the AppModule class. The body of the constructor creates a custom element from the Angular component and registers the `my-component` tag name as usual.

Finally, launch the manual bootstrapping of the application. This step is needed to start the Angular rendering process.

# [Building Web Components with Vue](#toc.xhtml_s125a)

The process of creating web components with Vue is pretty straightforward. Similarly to the Angular approach, Vue provides you with a module that simplifies the task of wrapping a Vue component within a custom element. Let’s assume you have a very simple Vue component like the following implemented in the `src/components/MyComponent.vue` file:

`<template>`

`<div>`

`I am the component`

`</div>`

`</template>`

It’s a very trivial component, but it is enough for our purpose. Change the `main.js` file of your Vue project as follows:

`import Vue from 'vue'`

`import wrap from '@vue/web-component-wrapper';`

`import MyComponent from './components/MyComponent.vue';`

`const CustomElement = wrap(Vue, MyComponent);`

`window.customElements.define('my-component', CustomElement);`

Besides the `MyComponent` component, this code imports the `wrap()` function from the `web-component`-wrapper module. It applies this `wrap() function` to get a custom element from the Vue component and registers the associated `my-componen`t tag name.

# [Conclusion](#toc.xhtml_s126a)

In this chapter, you discovered how to use the cookie alert component we built throughout this book in applications created with *React, Angular,* and *Vue*. You saw that using a web component in applications built with JavaScript UI frameworks is easy as using standard HTML elements. However, you may need to make some adjustments better to integrate your components with the framework of internal behavior.

You also explored how to create web components by wrapping components based on these frameworks. You learned that even if this is possible, you should carefully evaluate if it's worth it.

The examples shown in this chapter should give you enough directions on how to integrate Web Components and applications built with the most popular UI frameworks.

In the next chapter, we will take an overview of the most popular libraries and tools that help you in developing Web Components.

# [Questions](#toc.xhtml_s127a)

1.  What does Web Component interoperability mean?
2.  How can you programmatically access a web component in a React application?
3.  How can you handle a web component event in React?
4.  Why you need the `CUSTOM_ELEMENTS_SCHEMA` module in an Angular application that uses web components?
5.  How do you configure the `TypeScript` compiler in Angular to support JavaScript-based web components?
6.  How can you avoid that Vue throws an error when it comes across a web component’s tag name?
7.  Why would you want to create web components with a UI JavaScript framework?
8.  What drawbacks may you get building web components with a UI JavaScript framework?

# [CHAPTER 10](#toc.xhtml_c10)

# [Tools for Web Components Development](#toc.xhtml_c10)

At this point in the journey on Web Components building, you should be able to create your own and using it in your applications regardless of the UI library used. You learned enough to master the standard technologies behind Web Components: Custom Elements, Shadow DOM, and templates.

However, you may have noticed that some steps in using these technologies to build components are cumbersome or repetitive or complex. In other words, there is room to optimize the process of creating Web Components. If you want to simplify the process of building your Web Components, you can do it yourself or use a third-party tool. The first case can be challenging and requires a thorough knowledge of JavaScript and the DOM. The second case lets you get a simpler way to create your components but requires you to learn a new abstraction over the standard technologies.

In this chapter, we will explore a few of the most common tools that can improve your development experience and speed up your productivity. You will get a general but practical overview of using LitElement from the Polymer project, Hybrids, Slim, and Stencil.

# [Structure](#toc.xhtml_s128a)

*   Simplifying Web Components Building
*   Polymer and LitElement
*   Hybrids
*   Slim
*   Stencil

# [Objectives](#toc.xhtml_s129a)

This chapter gives you an overview of libraries and tools that help you in building Web Component in an easier way. They let you focus on the result you want to get while leaving the internal details to the tool.

You will learn how to use the basic features of each tool so that you can choose which better fits your needs and your expectations.

# [Simplifying Web Components building](#toc.xhtml_s130a)

One of the most common criticisms of using Web Components is the one claiming that they are low-level. To correctly use the technologies Web Components rely on, you need to have a good command of the DOM and its behavior. Actually, we saw how building Web Components requires you to tackle a few challenges. For example, the following are some of the low-level tasks you have to perform in order to create a robust and DOM-integrated Web Component:

*   Mapping attributes and properties
*   Event handling and emitting
*   Event listener creation and removal
*   Shadow DOM creation and manipulation
*   Template definition

These are just a few features you need to master. Some of these activities require deep knowledge of the DOM; others simply require more code.

You may think of simplifying the component definition on your own. For example, you can define your base class by extending the standard `HTMLElement` class. This class will deal with Shadow DOM manipulation, the attributes and properties mapping, and other common tasks. This way, your components will extend your base class instead of the `HTMLElement`, and some of those common tasks will be for free.

This is the approach used by many libraries that aim to simplify the process of building Web Components. In the rest of the chapter, we will explore some of the most well-known: LitElement, Hybrids, Slim, and Stencil. We will not provide a deep insight into the libraries, but just a light overview to have a high-level outline of the proposed approach. We will use each library to redefine the cookie alert component you already built in previous chapters with the native technologies. This way, you will have the opportunity to compare the development model proposed by each library.

We will follow a standard approach in using each library in order to introduce their features step by step. For each library, we will start introducing the basic infrastructure to create a Web Component. Then, we will see how to create the template for the UI. After that, we will explore how to manage properties and attributes and how to handle and emit events. Finally, we will take a look at the component's lifecycle.

# [Polymer and LitElement](#toc.xhtml_s131a)

**Polymer** is the name of a project and a library promoted by Google to bring Web Components to life. The project started in 2013, shortly after Web Components were announced, but browsers still were not supporting them. The project aimed to enable developers to support the Web Components principles. The library with the same name was released in various steps and provided many polyfills to support the core technologies and visual design. Polymer offered a way to develop Web Components when most popular browsers did not support them well.

In May 2018, the Polymer team announced a few important changes in the development of the library. In particular, they announced that the project's focus would be on the `LitElement` library. This library is part of the Polymer and provides support to define a Web Component. In other words, the Polymer project recognized that the time is ripe for native Web Components support.

In this section, we will take a look at how to leverage the `LitElement` library to simplify the way you can define your Web Component.

# [The lit-html library](#toc.xhtml_s132a)

The birth of LitElement is closely related to the `lit-html` library. This is a lightweight and extensible HTML templating library based on the browser's built-in HTML parser and the standard template element. If you know React, you can think of it like the JSX parser for Web Components.

You can use the `lit-html` library independently from `LitElement`. It promotes a functional approach in creating HTML templates, allowing you to create templates with a compact syntax, as shown in the following example:

`html‘<h1>Welcome ${name}</h1>‘`

As you can see, this expression is nothing but a tagged template literal that uses the html tag defined by the `lit-html` library. So, it is using a standard approach in defining templates based on string interpolation.

Its strength comes with the possibility to define functions returning `lit-html` templates, as in the following example:

`const helloTemplate = (name) => html‘<h1>Welcome ${name}</h1>‘;`

The `helloTemplate()` function evaluates the template literal, but, of course, it is not rendered to the DOM. To generate the elements of the template, you have to use the `render()` function, as shown below:

`render(helloTemplate(“John”), document.body);`

The `render()` function takes the template instantiated by the `helloTemplate()` function, creates the corresponding HTML elements, and append them to the body of the current HTML document.

All this happens in a very efficient way.

Of course, this is just a quick overview of the lit-html library. It has many other interesting features like support of directives and advanced rendering options.

# [Using LitElement](#toc.xhtml_s133a)

The `LitElement` library is heavily based on the `lit-html` library. If you are planning to use `LitElement` to build your Web Components, you don't need to use lit-html explicitly. It is already included in `LitElement`.

Assuming you have a Web Component project based on the Node.js development environment, the first step to use `LitElement` is to install it by typing the following command in a terminal window:

`npm install lit-element`

# [Basic infrastructure](#toc.xhtml_s134a)

Once you have installed the library, you can implement the basic infrastructure of our cookie alert component by writing the following code:

`import { LitElement, html, css } from 'lit-element';`

`export default class CookieAlert extends LitElement {`

`}`

`customElements.define("cookie-alert", CookieAlert);`

You import the `LitElement` class along with the HTML and CSS tagged template literals from the library. By the way, the HTML tagged template literal is the same function of the `lit-html` library. Then, you noticed that here we are extending the `LitElement` base class instead of the usual `HTMLElement` class. This class offers the support of the library to simplify the component definition, as we will see in a moment.

**The LitElement library also supports a decorator-based approach to define Web Components. However, since decorators are still not officially a supported standard, you need to use a specific transpiler, like TypeScript or Babel opportunely configured. In this section, we will not use this approach but will show some examples of such syntax along the way.**

By using the decorator-based syntax, the previous class definition will look like the following:

`import { LitElement, html, css, customElement } from 'lit-element';`

`@customElement("cookie-alert")`

`export default class CookieAlert extends LitElement {`

`}`

This syntax eliminates the need for the `customElements.define()` method, since the `customElement` decorator accomplishes this task.

# [Templates and UI](#toc.xhtml_s135a)

After setting up the basic infrastructure to define our component, let's implement the UI of the cookie alert component with the following code:

`import { LitElement, html, css } from 'lit-element';`

`export default class CookieAlert extends LitElement {`

`static get styles() {`

`return css‘`

`.container {`

`color: rgb(255, 255, 255);`

`background-color: rgb(35, 122, 252);`

`padding: 1em 1.8em;`

`width: 100%;`

`font-family: Helvetica,Calibri,Arial,sans-serif;`

`}`

`.footer {`

`position:fixed;`

`left:0px;`

`bottom:0px;`

`}`

`.button {`

`color: rgb(255, 255, 255);`

`background-color: transparent;`

`border-color: rgb(255, 255, 255);`

`padding: 5px 40px;`

`margin-right: 50px;`

`cursor: pointer;`

`float:right;`

`}`

`‘;`

`}`

`render() {`

`return html‘`

`<div class="container footer">`

`<slot id="message" name="message">${this.message}</slot>&nbsp;`

`<slot name="reference"></slot>`

`<button id="closeButton" class="button">Close</button>`

`<button id= "acceptButton" class="button">Accept</button>`

`</div>‘;`

`}`

`}`

`customElements.define("cookie-alert", CookieAlert);`

As you can see, we added the static getter `styles()` and the method `render().` The `styles()` getter defines the CSS style to apply to the component by using the CSS tagged template literal. The `render()` method generates the DOM structure for the component's UI. It is the result of the specified HTML tagged template literal.

You have no mention of the Shadow DOM. The `LitElement` base class internally manages it, so you don't have to worry about it.

# [Properties and attributes](#toc.xhtml_s136a)

The next step is to add the message property and syncing it to the attribute with the same name. You can easily do this by adding the following code to the `CookieAlert` class:

`import { LitElement, html, css } from 'lit-element';`

`export default class CookieAlert extends LitElement {`

`constructor() {`

`super();`

`this.message = "This website uses cookies to ensure you get the best experience";`

`}`

`static get properties() {`

`return {`

`message: {`

`attribute: true,`

`type: String,`

`reflect: true`

`}`

`}`

`}`

`//…`

`}`

We added static getter `properties().` This getter returns an object containing the definition of the properties for the component. In our case, we are defining the `message` property. The property definition is an object with a few options.

The true value assigned to the attribute option indicates that the `message` property has to be mapped to an attribute with the same name.

We also are specifying the property's type. This is fundamental if you want to map the attribute to the property. In fact, remember that the type of an attribute is always a string, while the type of property can be any possible JavaScript type. You need to specify the property type to allow the correct type conversion when mapping the attribute to the property.

Finally, the `reflect` option enables the mapping of the property to the attribute. As you can see, no need to observe attributes and explicitly manage type conversion. You also notice we added the class constructor. Its role, in this case, is to set a default value for the `message` property.

The decorator-based syntax allows you to have a compact definition of properties, as the following snippet of code demonstrates:

`import { LitElement, html, css } from 'lit-element';`

`@customElement(“cookie-alert”)`

`export default class CookieAlert extends LitElement {`

`@property({`

`attribute: true,`

`type: String,`

`reflect: true`

`})`

`message = "This website uses cookies to ensure you get the best experience";`

`//…`

`}`

The `@property` decorator takes the options to apply to the `message` property. Also, the `message` property initialization happens in the definition.

# [Events](#toc.xhtml_s137a)

To complete the implementation of our cookie alert component, we need to handle and emit events. For this purpose, we make a few little changes to the UI template in the `render()` method:

`import { LitElement, html, css } from 'lit-element';`

`export default class CookieAlert extends LitElement {`

`// …`

`render() {`

`return html‘`

`<div class="container footer">`

`<slot id="message" name="message">${this.message}</slot>&nbsp;`

`<slot name="reference"></slot>`

`<button id="closeButton" class="button" @click="${() => this.style.visibility = "hidden"}">Close</button>`

`<button id= "acceptButton" class="button" @click="${this.accept}">Accept</button>`

`</div>‘;`

`}`

`//…`

`}`

You see that we added the `@click` binding in both buttons. The `@event` binding comes from the `lit-html` library. It allows you to bind a listener to an event directly in the template. In our case, we attached an arrow function to the first button to hide the cookie alert component. We also associated the `accept()` method to the click event on the second button.

The `accept()` method has the same implementation of the listener we used in the original component:

`import { LitElement, html, css } from 'lit-element';`

`export default class CookieAlert extends LitElement {`

`// …`

`accept() {`

`this.style.visibility = "hidden";`

`setCookie("cookiesAccepted", "y", 365);`

`this.dispatchEvent(new CustomEvent("accepted", {`

`detail:{`

`acceptedCookieName: "cookiesAccepted",`

`acceptedCookieExpiration: 365}`

`}));`

`}`

`//…`

`}`

# [Lifecycle](#toc.xhtml_s138a)

To complete the component implementation, we have to add the code that manages the acceptance cookie:

`import { LitElement, html, css } from 'lit-element';`

`export default class CookieAlert extends LitElement {`

`// …`

`connectedCallback() {`

`super.connectedCallback();`

`const cookiesAccepted = getCookie("cookiesAccepted")`

`if (cookiesAccepted === "y") {`

`this.style.visibility = "hidden";`

`}`

`}`

`//…`

`}`

You can see that the `connectedCallback()` method has quite the same implementation we did in our standard version of the component. The main difference is the call to the `connectedCallback()` method of the super class. This ensures that all the initializations implemented in the `connectedCallback()` method of the `LitElement` class are executed.

The `LitElement` library provides other features that help you in building your Web Components. For example, in addition to the standard reactions, the `LitElement` class supports other methods called in various steps of the component's lifecycle. As said at the beginning of the chapter, addressing this topic is beyond our scope.

# [Hybrids](#toc.xhtml_s139a)

The Hybrids library aims to provide you with a functional approach to define your Web Components. You should only rely on plain objects and pure functions. So, no classes nor inheritance. All the details of managing the native definition of Web Components are processed internally by the library.

To use Hybrid in your Node-based project, install it by typing the following command in a terminal window:

`npm install hybrids`

Basic infrastructure

Let's explore the basic features of the Hybrid library by re-implementing our cookie alert component. The following code shows the basic elements to define a Web Component:

`import { html, define } from 'hybrids';`

`export const CookieAlert = {`

`};`

`define("cookie-alert", CookieAlert);`

You imported the `html()` and the define() functions. We will see later on how to use the `html()` function. The `define()` function is all you need to define your Web Component. The function takes the tag name for the component as the first argument and a literal object containing the component configuration. In the example, the `CookieAlert` object is empty, but we will fill it in a moment.

# [Templates and UI](#toc.xhtml_s140a)

To define the component's UI, you have to add a `render()` method to the `CookieAlert` configuration object. This method returns a tagged template literal obtained by tagging a template literal with the `html()` function, as shown in the following example:

`import { html, define } from 'hybrids';`

`export const CookieAlert = {`

`render: () => html‘`

`<style>`

`.container {`

`color: rgb(255, 255, 255);`

`background-color: rgb(35, 122, 252);`

`padding: 1em 1.8em;`

`width: 100%;`

`font-family: Helvetica,Calibri,Arial,sans-serif;`

`}`

`.footer {`

`position:fixed;`

`left:0px;`

`bottom:0px;`

`}`

`.button {`

`color: rgb(255, 255, 255);`

`background-color: transparent;`

`border-color: rgb(255, 255, 255);`

`padding: 5px 40px;`

`margin-right: 50px;`

`cursor: pointer;`

`float:right;`

`}`

`</style>`

`<div class="container footer">`

`<slot id="message" name="message"></slot>&nbsp;`

`<slot name="reference"></slot>`

`<button id="closeButton" class="button">Close</button>`

`<button id= "acceptButton" class="button">Accept</button>`

`</div>`

`‘`

`};`

`define("cookie-alert", CookieAlert);`

The `render()` method creates and updates the DOM structure of your Web Component. It works in combination with the built-in template engine.

The HTML template engine used by Hybrids is similar to the html() function of the `lit-html` library. However, even if the syntax is quite similar, its implementation is different.

# [Properties and attributes](#toc.xhtml_s141a)

To add properties and attributes to your component, you need to attach their definition to the `CookieAlert` object. In its simplest way, you can add the `message` property to the cookie alert component as follows:

`import { html, define } from 'hybrids';`

`export const CookieAlert = {`

`message: "This website uses cookies to ensure you get the best experience",`

`render: ({message}) => html‘`

`<style>`

`//…`

`</style>`

`<div class="container footer">`

`<slot id="message" name="message">${message}</slot>&nbsp;`

`<slot name="reference"></slot>`

`<button id="closeButton" class="button">Close</button>`

`<button id= "acceptButton" class="button">Accept</button>`

`</div>`

`‘`

`};`

`define("cookie-alert", CookieAlert);`

You added the message property with its default text. This is the basic way to define a property.

As a general approach, the Hybrids library allows you to provide a property descriptor to define a property. A property descriptor is a plain object with the general form shown below:

`const MyElement = {`

`propertyName: {`

`get: (host, lastValue) => {…},`

`set: (host, value, lastValue) => {…},`

`connect: (host, key, invalidate) => {`

`…`

`// disconnect`

`return () => {…};`

`},`

`observe: (host, value, lastValue) => {…},`

`}`

`};`

The `get()` and `set()` methods define a getter and a setter for the property. They have some parameters which allow you to manage the property's value properly. In particular, their first parameter, host in the example, represents the current component instance. This parameter is explicitly passed and frees you from relying on the `this` keyword. The getter and the setter have to return the new property's value.

The `connect(`) and `observe()` methods allow you to execute code when the component is added to the DOM and when the property's value changes.

Hybrids provide you with some built-in property factories, that is, functions that return a pre-defined configuration for properties. The `property()` function is one of these factories. It allows you to define a property in the following way:

`import { html, define } from 'hybrids';`

`export const CookieAlert = {`

`message: property("This website uses cookies to ensure you get the best experience"),`

`//…`

`};`

`define("cookie-alert", CookieAlert);`

The `property()` factory returns a standard configuration for the `message` property, with a default string value. It also connects the property with an attribute with the same name.

**The value of an attribute is assigned to the corresponding property only once when the component is added to the DOM. This means that attributes should be used only to set static values in the HTML markup. Changes to attributes are not automatically reflected in the corresponding properties.**

The approach we used above, based on simply assigning the string to the `message` property, is just a shortcut for using the `property()` factory. In the Hybrid jargon, this sort of shortcut is called **translation**.

Summarizing, you have many ways to define your property. Each way depends on how much flexibility you need for your property definition.

To complete this overview on properties and attributes, you need to know that each item in the configuration object of a Web Component is independent. This means that there is no internal state, and any reference to the properties must be explicit. This is the reason why the `render()` method of the cookie alert definition above has the `{message}` object as a parameter:

`render: ({message}) => html‘`

`<style>`

`//…`

`</style>`

`<div class="container footer">`

`<slot id="message" name="message">${message}</slot>&nbsp;`

`<slot name="reference"></slot>`

`<button id="closeButton" class="button">Close</button>`

`<button id= "acceptButton" class="button">Accept</button>`

`</div>`

`‘`

Since you need to use the message property within the template for the UI, you have to pass it explicitly. More in general, you have to pass an object with all the properties you need to use within the `render()` method.

# [Events](#toc.xhtml_s142a)

To add an event listener in the template of a Web Component, you can simply use the `onevent` syntax you use on standard HTML elements. For example, to handle the click event on both buttons of the cookie alert component, you can do as shown below:

`<div class="container footer">`

`<slot id="message" name="message">${message}</slot>&nbsp;`

`<slot name="reference"></slot>`

`<button id="closeButton"`

`class="button"`

`onclick="${(host)=> host.style.visibility = "hidden"}">`

`Close`

`</button>`

`<button id= "acceptButton"`

`class="button"`

`onclick="${accept}">`

`Accept`

`</button>`

`</div>`

You assigned an arrow function to the `onclick` attribute for the first button, and the `accept()` function to the second button. The `accept()` function is a normal function defined in the current module as follows:

`function accept(host) {`

`host.style.visibility = "hidden";`

`setCookie("cookiesAccepted", "y", 365);`

`host.dispatchEvent(new CustomEvent("accepted", {`

`detail:{`

`acceptedCookieName: "cookiesAccepted",`

`acceptedCookieExpiration: 365}`

`}));`

`}`

The only main thing to notice here is the `host` parameter. As said, this represents the current instance of your component.

# [Lifecycle](#toc.xhtml_s143a)

To complete the implementation of our cookie alert component, we need to check if the acceptance cookie is set when the component is appended to the DOM. To make this possible, we need to rearrange the `message` property definition in order to intercept when the component is added to the DOM. In fact, the Hybrids library has not global events for the lifecycle of the component. These events are on a per property basis.

So we redefine the message property definition as follows:

`export const CookieAlert = {`

`message: {`

`get: (host, lastValue = message) => lastValue,`

`set: (host,value) => value,`

`connect: checkCookie`

`},`

`render: ({message}) => html‘`

`//…`

`‘`

`};`

We specified a getter and a setter for the property, and `connect()` method that will be executed when the component will be appended to the DOM. Remember that this internally corresponds to the `connectedCallback()` reaction. In other words, all the `connect`() methods associated with the component's property definitions are executed when the `connectedCallback()` reaction runs.

The `checkCookie()` function is defined as follows:

`function checkCookie(host) {`

`const cookiesAccepted = getCookie("cookiesAccepted")`

`if (cookiesAccepted === "y") {`

`host.style.visibility = "hidden";`

`}`

`}`

Again, notice the host parameter passed to represent the current component instance.

If you want to execute some code when the component is removed from the DOM, the `connect()` method has to return the function to execute in that case. This way, the `connect()` method registers a function that will be executed when the `disconnectedCallback()` reaction runs.

# [Slim](#toc.xhtml_s144a)

The Slim library aims to simplify the definition of your Web Components by reducing the amount of code you need to write. It relies on the class-based approach but provides a slightly different model and lifecycle events.

To start working with the Slim library, you need to install it with the following command:

`npm install slim-js`

# [Basic infrastructure](#toc.xhtml_s145a)

As we did with other libraries, let's implement the cookie alert component by starting with the basic definition of a component:

`import {Slim} from 'slim-js';`

`Slim.tag(`

`"cookie-alert",`

`"<div>Web Component</div>",`

`class CookieAlert extends Slim {`

`get useShadow() { return true }`

`});`

The `Slim` object imported from the `slim-js` module allows you to do everything you need to create a Web Component. Its `tag()` method takes three parameters:

*   The name of the tag associated with the component.
*   The markup defines the UI template for the component.
*   The class that defines the logic of the component.

As you can see, the `CookieAlert` class that defines our component extends the class. In that basic example, you may note that we added the `useShadow()` getter which returns the true value. This getter enables Slim to use the Shadow DOM for the component. In fact, by default, Slim-based components don't use the Shadow DOM.

The library also provides a syntax based on decorators. In this case, the equivalent code for the basic infrastructure of the cookie alert component will be the following:

`import {Slim} from 'slim-js';`

`import {tag, template} from 'slim-js/Decorators';`

`@tag("cookie-alert")`

`@template("<div>Web Component</div>")`

`@useShadow(true)`

`class CookieAlert extends Slim {`

`}`

Very easy and compact!

# [Templates and UI](#toc.xhtml_s146a)

Creating the UI of a component with `Slim` is just a matter of specifying the string representing the template you want to use. For example, the following code shows how to add the basic UI markup for the cookie alert component:

`import {Slim} from 'slim-js';`

`Slim.tag(`

`"cookie-alert",`

`‘<style>`

`.container {`

`color: rgb(255, 255, 255);`

`background-color: rgb(35, 122, 252);`

`padding: 1em 1.8em;`

`width: 100%;`

`font-family: Helvetica,Calibri,Arial,sans-serif;`

`}`

`.footer {`

`position:fixed;`

`left:0px;`

`bottom:0px;`

`}`

`.button {`

`color: rgb(255, 255, 255);`

`background-color: transparent;`

`border-color: rgb(255, 255, 255);`

`padding: 5px 40px;`

`margin-right: 50px;`

`cursor: pointer;`

`float:right;`

`}`

`</style>`

`<div class="container footer">`

`<slot id="message" name="message"></slot>&nbsp;`

`<slot name="reference"></slot>`

`<button id="closeButton" class="button">Close</button>`

`<button id= "acceptButton" class="button">Accept</button>`

`</div>‘,`

`class CookieAlert extends Slim {`

`get useShadow() { return true }`

`});`

We will see in a moment that this template allows you to specify placeholders.

# [Properties and attributes](#toc.xhtml_s147a)

A component property in `Slim` is nothing but property in the class definition. If you want to initialize it, you need to do it in the constructor. The following code shows how to implement the `message` property for the cookie alert component:

`import {Slim} from 'slim-js';`

`Slim.tag(`

`"cookie-alert",`

`‘<style>`

`//…`

`</style>`

`<div class="container footer">`

`<slot id="message" name="message">{{message}}</slot>&nbsp;`

`<slot name="reference"></slot>`

`<button id="closeButton" class="button">Close</button>`

`<button id= "acceptButton" class="button">Accept</button>`

`</div>‘,`

`class CookieAlert extends Slim {`

`constructor() {`

`super();`

`this.message = "This website uses cookies to ensure you get the best experience";`

`}`

`get useShadow() { return true }`

`});`

You see that the property is defined and initialized in the constructor. Notice the call to `super()` in the constructor as well. Once you have defined the `message` property, you can use it in the UI template by specifying it between double curly brackets.

However, in this case, the `message` property is not bound to a `message` attribute. To map a property to an attribute, you need to use the decorator-based syntax, as in the following example:

`import {Slim} from 'slim-js';`

`import {tag, template, attribute} from 'slim-js/Decorators';`

`@tag("cookie-alert")`

`@template("<div>Web Component</div>")`

`@useShadow(true)`

`class CookieAlert extends Slim {`

`@attribute`

`message`

`}`

In this case, you are using the `@attribute` decorator associated with the public `message` property.

**Consider that, at the time of writing, the JavaScript syntax using decorators and property definitions are still not officially a supported standard. To use them, you need to use a specific transpiler like TypeScript or Babel opportunely configured.**

# [Events](#toc.xhtml_s148a)

Dealing with events is easy. You can add the event name as an attribute to the HTML element in the template and associate the event listener you define as a method of the class. To better explain, take a look at the following code:

`import {Slim} from 'slim-js';`

`Slim.tag(`

`"cookie-alert",`

`‘<style>`

`//…`

`</style>`

`<div class="container footer">`

`<slot id="message" name="message">{{message}}</slot>&nbsp;`

`<slot name="reference"></slot>`

`<button id="closeButton" class="button" click="hide">Close</button>`

`<button id= "acceptButton" class="button" click="accept">Accept</button>`

`</div>‘,`

`class CookieAlert extends Slim {`

`constructor() {`

`super();`

`this.message = "This website uses cookies to ensure you get the best experience";`

`}`

`get useShadow() { return true }`

`hide() {`

`this.style.visibility = "hidden";`

`}`

`accept() {`

`this.style.visibility = "hidden";`

`setCookie("cookiesAccepted", "y", 365);`

`this.dispatchEvent(new CustomEvent("accepted", {`

`detail:{`

`acceptedCookieName: "cookiesAccepted",`

`acceptedCookieExpiration: 365}`

`}));`

`}`

`});`

Here, the close and accept buttons have the `click` attribute. Each attribute has a string assigned: `hide` and `accept`. These are the names of the methods you attached to the `CookieAlert` class. These methods are the event listeners for the click event.

Note also that the mechanism to generate a custom event remains the same.

# [Lifecycle](#toc.xhtml_s149a)

To complete our implementation, we need to check if the user has accepted the cookie policy before showing the alert. As we know, this means we need to check if the acceptance cookie has been set. To make sure it will we checked before rendering the message, we have to do this in the `BeforeCreated` lifecycle event, as shown below:

`import {Slim} from 'slim-js';`

`Slim.tag(`

`"cookie-alert",`

`‘`

`//…`

`‘,`

`class CookieAlert extends Slim {`

`onBeforeCreated() {`

`const cookiesAccepted = getCookie("cookiesAccepted")`

`if (cookiesAccepted === "y") {`

`this.style.visibility = "hidden";`

`}`

`this.message = "This website uses cookies to ensure you get the best experience";`

`}`

`//…`

`});`

The `onBeforeCreated()` method is called when the `BeforeCreated` event happens. `Slim` generates a few lifecycle events for its components. To manage them, you should implement the following methods:

*   **onBeforeCreated():** This method is executed before the component is created.
*   **onCreated():** This method is executed after the component is created.
*   **onAdded():** This one runs when the component is added to the DOM.
*   **onRender():** This method is executed when the UI is rendered or updated.
*   **onRemoved():** This method runs when the component is removed from the DOM.

# [Stencil](#toc.xhtml_s150a)

Stencil is a tool that provides a different approach to build Web Components. The libraries we've explored in this chapter provides you with an abstraction that simplifies and/or enriches the definition of your Web Component. However, the component you build depends on the library itself: the library's code should be included in the resulting component.

Stencil instead is a compiler. It provides you with a rich abstraction to build your Web Component. It offers you a model and syntax that are inspired by Angular and React. But the final result of building your component is vanilla JavaScript.

Let's take a quick look at the main Stencil's features by implementing our cookie alert component.

To start a Stencil project, you can run the following command:

`npm init stencil component cookie-alert`

This command will set up a basic Stencil project in the `cookie-alert` folder with all the required dependencies. You note that we specified the `component` keyword in the command above. Actually, you can build other types of project with Stencil, like whole Web applications (`app`) or Ionic applications (ionic-pwa)

Once the project structure is created, you have a few folders with several files all around. We will not analyze the entire structure but will focus on the class definition and the CSS style. Please, refer to the Stencil official documentation to get more details.

# [Basic infrastructure](#toc.xhtml_s151a)

The basic definition of a Stencil component looks like the following:

`import { Component, h } from '@stencil/core';`

`@Component({`

`tag: 'cookie-alert',`

`styleUrl: 'cookie-alert.css',`

`shadow: true`

`})`

`export class CookieAlert {`

`render() {`

`return <div>Hello, World!</div>;`

`}`

`}`

These few lines of code highlight some key features of Stencil:

*   It uses TypeScript instead of plain JavaScript
*   It uses JSX
*   It uses decorators

The definition of the `CookieAlert` class is annotated with the @Component decorator. This decorator marks the class as the Web Component definition, similar to what Angular does with its components.

The options passed to the decorator configure the component. In particular, the tag option defines the tag name associated with the component. The `styleUrl` option indicates the file containing the CSS rules for the component. The shadow option states if the Shadow DOM is enabled (true) or not (false). By default, the Shadow DOM is not enabled, so in our cookie component, we explicitly enabled it.

The component has a `render()` method that is called to build the UI. This method returns a JSX expression similarly to what happens in React class-based components.

The `h()` function imported at the top of the module is needed to allow Stencil to turn the JSX into Virtual DOM elements.

# [Templates and UI](#toc.xhtml_s152a)

At this point, you already figure out how to build the UI for your component: you define your markup as a JSX expression returned by the `render()` method, as shown below:

`import { Component, h } from '@stencil/core';`

`@Component({`

`tag: 'cookie-alert',`

`styleUrl: 'cookie-alert.css',`

`shadow: true`

`})`

`export class CookieAlert {`

`render() {`

`return <div class="container footer">`

`<slot name="message"></slot>&nbsp;`

`<slot name="reference"></slot>`

`<button id="closeButton" class="button">Close</button>`

`<button id= "acceptButton" class="button">Accept</button>`

`</div>;`

`}`

`}`

Since the component definition refers to the `cookie-alert`.css file, create it and put the usual CSS code within it:

`.container {`

`color: rgb(255, 255, 255);`

`background-color: rgb(35, 122, 252);`

`padding: 1em 1.8em;`

`width: 100%;`

`font-family: Helvetica,Calibri,Arial,sans-serif;`

`}`

`.footer {`

`position:fixed;`

`left:0px;`

`bottom:0px;`

`}`

`.button {`

`color: rgb(255, 255, 255);`

`background-color: transparent;`

`border-color: rgb(255, 255, 255);`

`padding: 5px 40px;`

`margin-right: 50px;`

`cursor: pointer;`

`float:right;`

`}`

With these changes, you have the basic structure of the cookie alert component ready.

# [Properties and attributes](#toc.xhtml_s153a)

To add the `message` property to the cookie alert component, let's amend the previous code as follows:

`import { Component, Prop, h } from '@stencil/core';`

`@Component({`

`tag: 'cookie-alert',`

`styleUrl: 'cookie-alert.css',`

`shadow: true`

`})`

`export class CookieAlert {`

`@Prop()`

`message: string = "This website uses cookies to ensure you get the best experience";`

`render() {`

`return <div class="container footer">`

`<slot name="message">{this.message}</slot>&nbsp;`

`<slot name="reference"></slot>`

`<button id="closeButton" class="button">Close</button>`

`<button id= "acceptButton" class="button">Accept</button>`

`</div>;`

`}`

`}`

We are using the `@Prop` decorator for the `message` property and initialize it. Then used the property in the JSX markup through the `this.message` expression.

**A property defined with the** `@Prop` **decorator id by default immutable. This means that its value cannot be updated from inside the component logic. If you want to override this behavior, you need to set the mutable option for that decorator** `(@Prop({mutable: true})).`

The `message` property created till now is associated with the attribute with the same name. However, changes to the property are not mapped to the attribute. If you want this behavior, you need to enable reflection as shown by the following code:

`@Prop({reflect: true}) message: string = "This website uses cookies to ensure you get the best experience";`

This way, changes to the property are synced with the corresponding attribute.

# [Events](#toc.xhtml_s154a)

Let's start to see how to manage and generate events by handling the click event on the close button. This is the code we need:

`import { Component, Element, Prop, h } from '@stencil/core';`

`@Component({`

`tag: 'cookie-alert',`

`styleUrl: 'cookie-alert.css',`

`shadow: true`

`})`

`export class CookieAlert {`

`@Prop() message: string = "This website uses cookies to ensure you get the best experience";`

`@Element() element: HTMLElement;`

`render() {`

`return <div class="container footer">`

`<slot name="message">{this.message}</slot>&nbsp;`

`<slot name="reference"></slot>`

`<button id="closeButton"`

`class="button"`

`onClick={()=> this.element.style.visibility = "hidden"}>`

`Close`

`</button>`

`<button id= "acceptButton" class="button">Accept</button>`

`</div>;`

`}`

`}`

You handle the click event by adding the `onClick` attribute to the button element and by assigning an arrow function to it.

As you can see, the code of the click listener shows an interesting case. To change the CSS visibility property, you need to access the component host element. For this purpose, you use the `@Element` decorator to define the `element` property. This property will enable you to access the component host element from within the component class.

To handle the click event on the acceptance button, we can change the above code as follows:

`import { Component, Element, Prop, Event, EventEmitter, h } from '@stencil/core';`

`@Component({`

`tag: 'cookie-alert',`

`styleUrl: 'cookie-alert.css',`

`shadow: true`

`})`

`export class CookieAlert {`

`@Prop() message: string = "This website uses cookies to ensure you get the best experience";`

`@Element() element: HTMLElement;`

`@Event() accepted: EventEmitter;`

`render() {`

`return <div class="container footer">`

`<slot name="message">{this.message}</slot>&nbsp;`

`<slot name="reference"></slot>`

`<button id="closeButton"`

`class="button"`

`onClick={()=>this.element.style.visibility = "hidden"}>`

`Close`

`</button>`

`<button id= "acceptButton"`

`class="button"`

`onClick={()=>this.accept()}>`

`Accept`

`</button>`

`</div>;`

`}`

`accept() {`

`this.element.style.visibility = "hidden";`

`setCookie("cookiesAccepted", "y", 365);`

`this.accepted.emit({`

`detail:{`

`acceptedCookieName: "cookiesAccepted",`

`acceptedCookieExpiration: 365}`

`});`

`}`

`}`

In this case, we defined the `accept()` method and used it in the `onClick` listener. The interesting thing, in this case, is how we generate the accepted event. We used the `@Event` decorator to declare our accepted event emitter and created it through its `emit()` method.

Stencil also provides you with the `@Listen` decorator that allows you to listen to an event on the component.

# [Lifecycle](#toc.xhtml_s155a)

As usual, the last step for building our cookie alert component is to check if the user accepted the cookie policy. We can do it by adding the `connectedCallback()` method, as we did in the plain JavaScript version of the component.

This is how the `connectedCallback()` method looks like:

`connectedCallback() {`

`const cookiesAccepted = getCookie("cookiesAccepted")`

`if (cookiesAccepted === "y") {`

`this.element.style.visibility = "hidden";`

`}`

`}`

In addition to standard `connectedCallback()` and `disconnectedCallback()` reactions, Stencil provides you with a few other lifecycle methods:

*   `connectedCallback():` It is called when the component is appended to the DOM.
*   `componentWillLoad()`: This is called once just after the component is appended to the DOM the first time.
*   `componentDidLoad():` It is called once just after the component is loaded and the first render() runs.
*   `componentWillRender():` This is called before each `render()` execution.
*   `componentDidRender():` It is called after each `render()` execution.
*   `componentWillUpdate():` It is called when the component is about to be updated.
*   `componentDidUpdate():` This is called after the component updates.
*   `disconnectedCallback():` This is called when the component is removed from the DOM.

# [Conclusion](#toc.xhtml_s156a)

This chapter concludes the book by giving you an overview of the ecosystem that is growing around Web Components. You learned that some features of the Web Component technologies may be considered as low-level and require DOM knowledge and repetitive code. Libraries like the ones we explored in the chapter aim to simplify the development experience.

You explored `LitElement`, from the `Polymer` project, and used its development approach that relies on the `LitElement` base class. You met Hybrids that proposes a functional approach based on plain objects and pure functions. Also, you applied the minimalist class-based model of the `Slim` library. Finally, you used Stencil with its syntax halfway between Angular and React to generate Web Components in plain JavaScript.

At the end of the journey proposed by this book, you learned what you need to build your own Web Components using the approach that best fits your needs.

# [Questions](#toc.xhtml_s157a)

1.  Why should you use a library to create your Web Components?
2.  What is the relationship between the Polymer project and the `LitElement` library?
3.  What is the purpose of the `lit-html` library?
4.  What is the general approach to building Web Components offered by the LitElement library?
5.  What is the general philosophy of the Hybrids library?
6.  What is the main difference between Stencil and the other libraries analyzed in the chapter?
7.  What is the syntax proposed by Stencil inspired by?
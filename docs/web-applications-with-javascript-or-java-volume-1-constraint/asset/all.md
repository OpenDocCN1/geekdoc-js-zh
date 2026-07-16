![](graphic/01_Cover_fig_01.png)

![image](graphic/01_Cover_fig_01.png)

Gerd Wagner and Mircea Diaconescu

Web Applications with Javascript or Java

De Gruyter Graduate

Also of interest

![](graphic/03_Front_Matter01_fig_01.png)

Web Applications with Javascript or Java, Volume 2

G. Wagner, M. Diaconescu, 2017

ISBN 978-3-11-050024-0, e-ISBN 978-3-11-050032-5,

e-ISBN (EPUB) 978-3-11-049756-4

![](graphic/03_Front_Matter01_fig_02.png)

IBM z/OS ISPF Smart Practices 1

F. Lanz, 2015

ISBN 978-3-11-037548-0, e-ISBN 978-3-11-037559-6,

e-ISBN (EPUB) 978-3-11-039788-8, Set-ISBN 978-3-11-037560-2

![](graphic/03_Front_Matter01_fig_03.png)

IBM z/OS ISPF Smart Practices 2

F. Lanz, 2015

ISBN 978-3-11-040753-2, e-ISBN 978-3-11-040761-7,

e-ISBN (EPUB) 978-3-11-040765-5, Set-ISBN 978-3-11-040762-4

![](graphic/03_Front_Matter01_fig_04.png)

Color Image Watermarking

Q. Su, 2017

ISBN 978-3-11-048757-2, e-ISBN 978-3-11-048773-2,

e-ISBN (EPUB) 978-3-11-048763-3, Set-ISBN 978-3-11-048776-3

![](graphic/04_Title_fig_01.png)

Authors

Prof. Dr. Gerd Wagner
BTU Cottbus-Senftenberg
Fachgebiet Internettechnologie
Konrad-Wachsmann-Allee 5
03046 Cottbus
[wagnerg@b-tu.de](mailto:wagnerg@b-tu.de)

Mircea Diaconescu
[dimircea@gmail.com](mailto:dimircea@gmail.com)

The book‘s associated source code is licensed under The Code Project Open License (CPOL), see [http://www.codeproject.com/info/cpol10.aspx](http://www.codeproject.com/info/cpol10.aspx), implying that the code is provided „as-is“, can be modified to create derivative works, can be redistributed, and can be used in commercial applications. The book itself, however, is protected by German copyright law and must not be distributed or republished without the publisher‘s consent.

ISBN 978-3-11-049993-3

e-ISBN (PDF) 978-3-11-049995-7

e-ISBN (EPUB) 978-3-11-049724-3

Library of Congress Cataloging-in-Publication Data

A CIP catalog record for this book has been applied for at the Library of Congress.

Bibliographic information published by the Deutsche Nationalbibliothek

The Deutsche Nationalbibliothek lists this publication in the Deutsche Nationalbibliografie; detailed bibliographic data are available on the Internet at [http://dnb.dnb.de](http://dnb.dnb.de).

© 2018 Walter de Gruyter GmbH, Berlin/Boston

Cover image: monsitj/iStock/thinkstock

[www.degruyter.com](http://www.degruyter.com)

![](graphic/06_Dedication_fig_01.png)

To Our Families.

# Foreword

This two-volume book shows how to design and implement web applications with a model-based engineering approach, using the two most relevant technology platforms for web development: JavaScript and Java. Web apps are designed with the help of information models in the form of UML class diagrams and implemented as:

1.JavaScript front-end apps, using one of the two local storage technologies offered by web browsers;

2.Java back-end apps, using Java Server Faces (JSF) as the user interface technology, the Java Persistence API (JPA) for object-to-storage mapping, and a MySQL/ MariaDB database management system;

3.distributed JavaScript apps with

a.a front-end component for managing the user interface and taking care of certain parts of the application logic (including constraint-based data validation), and

b.a NodeJS-based back-end component for managing persistent storage and taking care of certain parts of the application logic (including constraint-based data validation).

The focus of the book are general concepts and techniques concerning the fundamental information management issues of

1.  integrity constraints and data validation,
2.  enumerations and enumeration attributes
3.  unidirectional and bidirectional associations between object types,
4.  subtyping and inheritance in class hierarchies.

The first two issues of this list are discussed in Volume 1 of the book, while the last two issues are discussed in Volume 2.

We assume that the reader is already familiar with HTML and with object-oriented programming, preferably with Java (or, otherwise, with C++, PHP, Python or C#). In addition, we assume that the reader has some familiarity with CSS and JavaScript, and is willing to learn more about programming with modern JavaScript.

The book can be used

1)in web development courses for students of Computer Science and related disciplines;

2)by JavaScript developers for learning Java;

3)by Java developers for learning JavaScript;

4)by JavaScript and Java (and PHP/Python/C# etc.) developers for learning

‒object-oriented (OO) programming with JavaScript and Java EE,

‒how to implement basic information management concepts and build complete web apps with plain JavaScript and Java EE.

The book comes with the complete source code of six example apps that you can run, or download, from the book’s website [http://web-engineering.info/WebAppBook](http://web-engineering.info/WebAppBook). Readers can ask questions about any chapter or topic of the book in one of the discussion forums provided at the web-engineering.info website.

## 1Mastering App Development Requires More than Coding Skills

For mastering app development, it’s not sufficient that you master coding in your favorite programming language. It’s essential that you understand all basic concepts and techniques, not just in programming, but also in information management.

A programming (or software development) technology typically combines a programming language, such as JavaScript, Java or C#, with a framework or a number of libraries, such as JavaScript with BackboneJS, Java with JPA and JSF, or C# with ASP.NET MVC, for programming user interfaces and data storage management.

Many developers seem to believe that all they need to learn and master for their professional career are the right programming technologies. However, they fail to master app development, if they don’t manage to learn the general concepts and techniques needed for being able to apply programming technologies in the right way.

Understanding general concepts and techniques, in programming and information management, helps you to

–better understand the elements of a language or framework by recognizing them as specific incarnations of general concepts,

–compare different technologies and assess their strengths and weaknesses,

–make an informed choice of a new promising language/technology suitable for your purposes.

While technology-specific knowledge is important (in fact, it is the basis) for mastering programming and app development, it is also true that its half-time value is pretty short. In this book, we do not only explain programming and information management concepts and techniques in a technology-independent way, we also explain in which way these concepts and techniques are supported in the two most relevant technologies: JavaScript and Java.

## 2Why is JavaScript a Good Choice for Building Web Apps?

Today, JavaScript is not just a programming language, but rather a platform, which offers many advantages over other platforms:

1.It’s the only language that enjoys native support in web browsers.

2.It’s the only (“universal”) language that allows

a.building web apps with just one programming language; all other languages (like Java and C#) can only be used on the back-end and need to be combined with front-end JavaScript, so developers need to master at least two programming languages.

b.executing the same code (e. g., for constraint validation) on the back-end and the front-end.

3.It’s the only language that allows dynamic distribution, that is, executing the same code (e. g., for business computations) either in the back-end or the front-end, depending on run-time conditions such as the available front-end resources.

4.It combines object-oriented with functional programming.

5.Its dynamism allows various forms of meta-programming, which means it enables developers to program their own programming concepts, like classes and enumerations.

## 3Why is Java a Good Choice for Building Web Apps?

In 2017, and for many years to come, the enterprise software platform Java Enterprise Edition (Java EE), which bundles the Java language together with a number of libraries for enterprise software systems, is the most important programming platform for enterprise information technologies, including all kinds of business software applications. Its strong points mainly result from the fact that it is very mature:

1.  it has a rich ecosystem, including a large number of libraries, frameworks and tools;
2.  Java code executes faster than scripting languages, like Python, PHP, NodeJS or Ruby;
3.  Java web applications can be scaled, e. g., by using distributed database transactions and cluster technologies;
4.  it provides a lot of advanced security technologies.

## 4Comparing Java with JavaScript

As opposed to Java, JavaScript is relatively easy to learn. One reason for this is the need of explicit type definitions for variables, parameters and return values in Java, which are not needed in JavaScript.

Both Java and JavaScript are “object-oriented” programming languages, but JavaScript is even more “object-oriented” than Java, which is rather “class-oriented”. There is no explicit class concept in JavaScript. Classes have to be defined in the form of special objects. However, objects can also be created without instantiating a class, and properties as well as methods can be defined for specific objects independently of any class definition.

At run time, properties and methods can be added to, or removed from, any object and class. While JavaScript classes can be redefined at runtime, immediately affecting all objects that instantiate the class, Java classes cannot be redefined in such a way.

JavaScript allows defining methods that are specific for an object, independently of its class. The methods of a Java object are defined for its class, it is not possible to define object-specific methods.

JavaScript has better support for functional programming. For instance, it supports “closures”, which are function execution contexts. Java only supports a limited version of closures for anonymous classes and “lambdas”.

## 5Good Programs Are: Effective, Robust, Efficient and Maintainable

… as observed by Nick Gonzalez[1](31_Notes01.xhtml_Notes01_1). A good program is effective: it solves the problem it is supposed to solve. A good program must not crash when it receives bad inputs from users: it is robust. Good programs are efficient: it does the job it is supposed to do quickly. Since the requirements for a program may change over time, a good program should be maintainable, so it can be modified easily when requirements do change. A program can only be maintainable, if its code is written in a clear manner.

Any damn fool can write code that a computer can understand, the trick is to write code that humans can understand. (Martin Fowler in After the Program Runs[2](31_Notes01.xhtml_Notes01_2))

Code is often “unnecessarily complicated, convoluted, disorganized, and stitched together with disdain”, as observed in a post by Santiago L. Valdarrama[3](31_Notes01.xhtml_Notes01_3) who recommends using comments when necessary, only to explain things that can’t be made clear enough, but rather make your code reveal its intention through the use of better names, proper structure, and correct spacing and indentation.

## 6Run the Apps and Get Their Code

For running any of the example apps from our web server, and for downloading their code, please visit http://web-engineering.info/WebAppBook-CodeLinks.

# List of Figures

[2.1The built-in `JavaScript` classes `Object` and `Function`](#13_chapter02.xhtml_chapter02_34)

[3.1The object type `Book`](#14_chapter03.xhtml_chapter03_1)

[4.1The object type `Book`](#15_chapter04.xhtml_chapter04_1)

[5.1From a conceptual model via a design model to a JavaScript class model](#16_chapter05.xhtml_chapter05_11)

[5.2From a conceptual model via design models to implementation models](#16_chapter05.xhtml_chapter05_13)

[6.1The MVC code base architecture with the model as the foundation](#17_chapter06.xhtml_chapter06_2)

[6.2Architectures for front-end web apps](#17_chapter06.xhtml_chapter06_17)

[6.3Architectures for back-end and distributed web apps](#17_chapter06.xhtml_chapter06_20)

[7.1An example of an object-level constraint](#19_chapter07.xhtml_chapter07_20)

[7.2A design model defining the object type `Book` with two invariants](#19_chapter07.xhtml_chapter07_24)

[8.1From an information design model to a JS class model](#20_chapter08.xhtml_chapter08_8)

[9.1Deriving an Entity class model from an information design model](#21_chapter09.xhtml_chapter09_13)

[10.1An example of an extensible enumeration](#23_chapter10.xhtml_chapter10_6)

[10.2An information design model for the object type `Book`](#23_chapter10.xhtml_chapter10_15)

[11.1A JavaScript class model for the object type `Book`](#24_chapter11.xhtml_chapter11_4)

[11.2The UI for creating a new book record with enumeration attributes](#24_chapter11.xhtml_chapter11_16)

[12.1A JPA entity class model for the object type `Book`](#25_chapter12.xhtml_chapter12_3)

[12.2The user interface for creating a new book record](#25_chapter12.xhtml_chapter12_10)

[13.1Quantity types](#27_chapter13.xhtml_chapter13_30)

# List of Tables

[2.1An example of an entity table representing a collection of books](#13_chapter02.xhtml_chapter02_21)

[2.2Required and desirable features of JS code patterns for classes](#13_chapter02.xhtml_chapter02_29)

[3.1A collection of book objects represented as a table](#14_chapter03.xhtml_chapter03_1)

[3.2Sample data about movies](#14_chapter03.xhtml_chapter03_40)

[3.3Sample data about countries](#14_chapter03.xhtml_chapter03_46)

[4.1Sample data about books](#15_chapter04.xhtml_chapter04_1)

[4.2Java Visibility Level](#15_chapter04.xhtml_chapter04_10)

[7.1Sample data for `Book`](#19_chapter07.xhtml_chapter07_27)

[8.1Datatype mapping](#20_chapter08.xhtml_chapter08_13)

[8.2Sample data about movies](#20_chapter08.xhtml_chapter08_37)

[8.3Sample data about countries](#20_chapter08.xhtml_chapter08_41)

[9.1Bean Validation annotations for properties](#21_chapter09.xhtml_chapter09_4)

[9.2Datatype mapping to Java](#21_chapter09.xhtml_chapter09_11)

[9.3Datatype mapping to MySQL](#21_chapter09.xhtml_chapter09_11)

[10.1Representing an enumeration of records as a table](#23_chapter10.xhtml_chapter10_1)

[10.2Sample data for `Book`](#23_chapter10.xhtml_chapter10_17)

[11.1Sample data about movies with rating and genres](#24_chapter11.xhtml_chapter11_29)

[11.2Sample data about countries with country code and religions](#24_chapter11.xhtml_chapter11_31)

![](graphic/11_Part01_fig_01.png)

# Part IGetting Started

In this first part of the book we provide a brief introduction to the Web and show how to build

1.  a simple front-end web app using plain JavaScript and local storage,
2.  a simple back-end web app using Java with JSF, JPA and a MySQL/MariaDB database.

We also provide brief introductions to information modeling and to software application architectures.

The minimal examples of data management apps discussed in this part of the book only include a minimum of the overall functionality required for a complete app. They take care of only one object type (“books”) and support the four standard data management use cases (Create/Retrieve/Update/Delete), but they need to be extended by adding further important parts of an app’s overall functionality.

# 1A Quick Tour of the Foundations of Web Apps

If you are already familiar with HTML, XML and JavaScript, you may skip this chapter and immediately start developing a minimal web application by going to the next chapter.

## 1.1The World Wide Web (WWW)

After the Internet had been established in the 1980’ies, Tim Berners-Lee[4](31_Notes01.xhtml_Notes01_4) developed the idea and the first implementation of the WWW in 1989 at the European research institution CERN in Geneva, Switzerland. The WWW (or, simply, “the Web”) is based on the Internet technologies TCP/IP (the Internet Protocol) and DNS (the Domain Name System). Initially, the Web consisted of

1.  the Hypertext Transfer Protocol (HTTP),
2.  the Hypertext Markup Language (HTML), and
3.  web server programs, acting as HTTP servers, as well as web ’user agents’ (such as browsers), acting as HTTP clients.

Later, further important technology components have been added to this set of basic web technologies:

–the page/document style language Cascading Style Sheets (CSS) in 1995,

–the web programming language JavaScript in 1995,

–the Extensible Markup Language (XML), as the basis of web formats (like SVG and RDF/XML), in 1998,

–the XML-based Scalable Vector Graphics (SVG) format in 2001,

–the Resource Description Framework (RDF) for knowledge representation on the Web in 2004.

## 1.2HTML and XML

HTML allows to mark up (or describe) the structure of a human-readable web document or web user interface, while XML allows to mark up the structure of all kinds of documents, data files and messages, whether they are human-readable or not. XML can also be used as the basis for defining a version of HTML that is called XHTML.

### 1.2.1XML documents

XML provides a syntax for expressing structured information in the form of an XML document with nested elements and their attributes. The specific elements and attributes used in an XML document can come from any vocabulary, such as public standards or (private) user-defined XML formats. XML is used for specifying

–document formats, such as XHTML5, the Scalable Vector Graphics (SVG) format or the DocBook format,

–data interchange file formats, such as the Mathematical Markup Language (MathML) or the Universal Business Language (UBL),

–message formats, such as the web service message format SOAP[5](31_Notes01.xhtml_Notes01_5)

### 1.2.2Unicode and UTF-8

XML is based on Unicode, which is a platform-independent character set that includes almost all characters from most of the world’s script languages including Hindi, Burmese and Gaelic. Each character is assigned a unique integer code in the range between 0 and 1,114,111\. For example, the Greek letter π has the code 960, so it can be inserted in an XML document as π using the XML entity syntax.

Unicode includes legacy character sets like ASCII and ISO-8859–1 (Latin-1) as subsets.

The default encoding of an XML document is UTF-8, which uses only a single byte for ASCII characters, but three bytes for less common characters.

Almost all Unicode characters are legal in a well-formed XML document. Illegal characters are the control characters with code 0 through 31, except for the carriage return, line feed and tab. It is therefore dangerous to copy text from another (non-XML) text to an XML document (often, the form feed character creates a problem).

### 1.2.3XML namespaces

Generally, namespaces help to avoid name conflicts. They allow to reuse the same (local) name in different namespace contexts. Many computational languages have some form of namespace concept, for instance, Java and PHP.

XML namespaces are identified with the help of a namespace URI, such as the SVG namespace URI “ http://www.w3.org/2000/svg”, which is associated with a namespace prefix, such as `svg`. Such a namespace represents a collection of names, both for elements and attributes, and allows namespace-qualified names of the form prefix:name, such as `svg:circle` as a namespace-qualified name for SVG circle elements.

A default namespace is declared in the start tag of an element in the following way:

![](graphic/12_chapter01_fig_01.png)

This example shows the start tag of the HTML root element, in which the XHTML namespace is declared as the default namespace.

The following example shows an SVG namespace declaration for an `svg` element embedded in an HTML document:

![](graphic/12_chapter01_fig_02.png)

### 1.2.4Correct XML documents

XML defines two syntactic correctness criteria. An XML document must be well-formed, and if it is based on a grammar (or schema), then it must also be valid with respect to that grammar, or, in other words, satisfy all rules of the grammar.

An XML document is called well-formed, if it satisfies the following syntactic conditions:

1.  There must be exactly one root element.
2.  Each element has a start tag and an end tag; however, empty elements can be closed as `<phone/>` instead of `<phone></phone>`.

3.Tags don’t overlap. For instance, we cannot have
`<author><name>Lee Hong</author></name>`

4.Attribute names are unique within the scope of an element. For instance, the following code is not correct:

![](graphic/12_chapter01_fig_03.png)

An XML document is called valid against a particular grammar (such as a DTD or an XML Schema), if

1.  it is well-formed,
2.  and it respects the grammar.

### 1.2.5The evolution of HTML

The World-Wide Web Committee (W3C) has developed the following important versions of HTML:

–1997: HTML 4 as an SGML-based language,

–2000: XHTML 1 as an XML-based clean-up of HTML 4,

–2014: (X)HTML 5 in cooperation (and competition) with the WHAT working group[6](31_Notes01.xhtml_Notes01_6) supported by browser vendors.

As the inventor of the Web, Tim Berners-Lee developed a first version of HTML[7](31_Notes01.xhtml_Notes01_7) in 1990\. A few years later, in 1995, Tim Berners-Lee and Dan Connolly wrote the HTML 2[8](31_Notes01.xhtml_Notes01_8) standard, which captured the common use of HTML elements at that time. In the following years, HTML has been used and gradually extended by a growing community of early WWW adopters. This evolution of HTML, which has led to a messy set of elements and attributes (called “tag soup”), has been mainly controlled by browser vendors and their competition with each other. The development of XHTML in 2000 was an attempt by the W3C to clean up this mess, but it neglected to advance HTML’s functionality towards a richer user interface, which was the focus of the WHAT working group[9](31_Notes01.xhtml_Notes01_9) led by Ian Hickson[10](31_Notes01.xhtml_Notes01_10) who can be considered as the mastermind and main author of HTML 5 and many of its accompanying JavaScript APIs that made HTML fit for mobile apps.

HTML was originally designed as a structure description language, and not as a presentation description language. But HTML4 has a lot of purely presentational elements such as `font`. XHTML has been taking HTML back to its roots, dropping presentational elements and defining a simple and clear syntax, in support of the goals of

–device independence,

–accessibility, and

–usability.

We adopt the symbolic equation

HTML = HTML5 = XHTML5

stating that when we say “HTML” or “HTML5”, we actually mean XHTML5 because we prefer the clear syntax of XML documents over the liberal and confusing HTML4-style syntax that is also allowed by HTML5.

The following simple example shows the basic code template to be used for any HTML document:

![](graphic/12_chapter01_fig_04.png)

Notice that in line 1, the HTML5 document type is declared, such that browsers are instructed to use the HTML5 document object model (DOM). In the `html` start tag in line 2, using the default namespace declaration attribute `xmlns`, the XHTML namespace URI [`http://www.w3.org/1999/xhtml`](http://www.w3.org/1999/xhtml) is declared as the default namespace for making sure that browsers, and other tools, understand that all non-qualified element names like `html`, `head`, `body`, etc. are from the XHTML namespace.

Also in the `html` start tag, we set the (default) language for the text content of all elements (here to “en” standing for English) using both the `xml:lang` attribute and the HTML `lang` attribute. This attribute duplication is a small price to pay for having a hybrid document that can be processed both by HTML and by XML tools.

Finally, in line 4, using an (empty) `meta` element with a `charset` attribute, we set the HTML document’s character encoding to UTF-8, which is also the default for XML documents.

### 1.2.6HTML forms

For user-interactive web applications, the web browser needs to render a user interface (UI). The traditional metaphor for a software application’s UI is that of a form. The special elements for data input, data output and user actions are called form controls or UI widgets. In HTML, a `form` element is a section of a web page consisting of block elements that contain form controls and labels on those controls.

Users complete a form by entering text into input fields and by selecting items from choice controls, including dropdown selection lists, radio button groups and checkbox groups. A completed form is submitted with the help of a submit button. When a user submits a form, it is normally sent to a web server either with the HTTP GET method or with the HTTP POST method. The standard encoding for the submission is called URL-encoded. It is represented by the Internet media type `application/x-www-form-urlencoded`. In this encoding, spaces become plus signs, and any other reserved characters become encoded as a percent sign and hexadecimal digits, as defined in RFC 1738.

Each form control has both an initial value and a current value, both of which are strings. The initial value is specified with the control element’s `value` attribute, except for the initial value of a `textarea` element, which is given by its initial contents. The control’s current value is first set to the initial value. Thereafter, the control’s current value may be modified through user interaction or scripts. When a form is submitted for processing, some controls have their name paired with their current value and these pairs are submitted with the form.

Labels are associated with a control by including the control as a child element within a `label` element (implicit labels), or by giving the control an `id` value and referencing this ID in the `for` attribute of the `label` element (explicit labels).

In the simple user interfaces of our “Getting Started” applications, we only need four types of form controls:

1.  single line input fields created with an `<input name="`…`" />` element,
2.  single line output fields created with an `<output name="`…`" />` element,
3.  push buttons created with a `<button type="button">`…`</button>` element, and
4.  dropdown selection lists created with a `select` element of the following form:

![](graphic/12_chapter01_fig_05.png)

An example of an HTML form with implicit labels for creating such a user interface is

![](graphic/12_chapter01_fig_06.png)

In an HTML-form-based data management user interface, we have a correspondence between the different kinds of properties defined in the model classes of an app and the form controls used for the input and output of their values. We have to distinguish between various kinds of model class attributes, which are mapped to various kinds of form fields. This mapping is also called data binding.

In general, an attribute of a model class can always be represented in the user interface by a plain `input` control (with the default setting `type=" text"`), no matter which datatype has been defined as the range of the attribute in the model class. However, in special cases, other types of `input` controls (for instance, `type= "date"`), or other widgets, may be used. For instance, if the attribute’s range is an enumeration, a `select` control or, if the number of possible choices is small enough (say, less than 8), a radio button group can be used.

## 1.3Styling Web Documents and User Interfaces with CSS

While HTML is used for defining the content structure of a web document or a web user interface, the Cascading Style Sheets (CSS) language is used for defining the presentation style of web pages, which means that you use it for telling the browser how you want your HTML (or XML) rendered: using which layout of content elements, which fonts and text styles, which colors, which backgrounds, and which animations. Normally, these settings are made in a separate CSS file that is associated with an HTML file via a special `link` element in the HTML’s `head`.

A first sketch of CSS[11](31_Notes01.xhtml_Notes01_11) was proposed in October 1994 by Håkon W. Lie[12](31_Notes01.xhtml_Notes01_12) who later became the CTO of the browser vendor Opera. While the official CSS1[13](31_Notes01.xhtml_Notes01_13) standard dates back to December 1996, “most of it was hammered out on a whiteboard in Sophia-Antipolis” by Håkon W. Lie together with Bert Bos in July 1995 (as he explains in an interview[14](31_Notes01.xhtml_Notes01_14)).

CSS is based on a form of rules that consist of selectors, which select the document element(s) to which a rule applies, and a list of property-value pairs that define the styling of the selected element(s) with the help of CSS properties such as `font-size` or `color`. There are two fundamental mechanisms for computing the CSS property values for any page element as a result of applying the given set of CSS rules: inheritance and the cascade.

The basic element of a CSS layout[15](31_Notes01.xhtml_Notes01_15) is a rectangle, also called “box”, with an inner content area, an optional border, an optional padding (between content and border) and an optional margin around the border. This structure is defined by the CSS box model.

We will not go deeper into CSS in this book, since our focus here is on the logic and functionality of an app, and not so much on its beauty.

## 1.4JavaScript – “the assembly language of the Web”

JavaScript was developed in 10 days in May 1995 by Brendan Eich[16](31_Notes01.xhtml_Notes01_16), then working at Netscape[17](31_Notes01.xhtml_Notes01_17), as the HTML scripting language for their browser Navigator 2 (more about history[18](31_Notes01.xhtml_Notes01_18)). Brendan Eich said (at the O’Reilly Fluent conference in San Francisco in April 2015): “I did JavaScript in such a hurry, I never dreamed it would become the assembly language for the Web”.

JavaScript is a dynamic functional object-oriented programming language that can be used for

1.Enriching a web page by

–generating browser-specific HTML content or CSS styling,

–inserting dynamic HTML content,

–producing special audio-visual effects (animations).

2.Enriching a web user interface by

–implementing advanced user interface components,

–validating user input on the client side,

–automatically pre-filling certain form fields.

3.Implementing a front-end web application with local or remote data storage[19](31_Notes01.xhtml_Notes01_19).

4.Implementing a front-end component for a distributed web application with remote data storage managed by a back-end component, which is a server-side program that is traditionally written in a server-side language such as PHP, Java or C#, but can nowadays also be written in JavaScript with NodeJS.

5.Implementing a complete distributed web application where both the front-end and the back-end components are JavaScript programs.

The version of JavaScript that is currently fully supported by web browsers is called “ECMAScript 5.1”, or simply “ES5”, but the next two versions, called “ES6” and “ES7” (or “ES 2015” and “ES 2016”), are already partially supported by current browsers and back-end JS environments. In fact, in May 2017, ES6 is fully supported in non-mobile browsers, except its important new `module` concept.

### 1.4.1JavaScript as an object-oriented language

JavaScript is object-oriented, but in a different way than classical OO programming languages such as Java and C++. In JavaScript, classes, unlike objects and functions, are not first-class citizens. Rather, classes have to be defined by following some code pattern in the form of special JS objects: either as constructor functions (possibly using the syntactic sugar of ES6 `class` declarations) or as factory objects.

However, objects can also be created without instantiating a class, in which case they are untyped, and properties as well as methods can be defined for specific objects independently of any class definition. At run time, properties and methods can be added to, or removed from, any object and class. This dynamism of JavaScript allows powerful forms of meta-programming, such as defining your own concepts of classes and enumerations (and other special datatypes).

### 1.4.2Further reading about JavaScript

Good open access books about JavaScript are

–Speaking JavaScript[20](31_Notes01.xhtml_Notes01_20), by Dr. Axel Rauschmayer.

–Eloquent JavaScript[21](31_Notes01.xhtml_Notes01_21), by Marijn Haverbeke.

## 1.5Accessibility for Web Apps

The recommended approach to providing accessibility for web apps is defined by the Accessible Rich Internet Applications (ARIA) standard. As summarized by Bryan Garaventa[22](31_Notes01.xhtml_Notes01_22) in his article on different forms of accessibility[23](31_Notes01.xhtml_Notes01_23), there are 3 main aspects of accessibility for interactive web technologies: 1) keyboard accessibility, 2) screen reader accessibility, and 3) cognitive accessibility.

Further reading on ARIA:

1.  How browsers interact with screen readers, and where ARIA fits in the mix[24](31_Notes01.xhtml_Notes01_24) by Bryan Garaventa
2.  The Accessibility Tree Training Guide[25](31_Notes01.xhtml_Notes01_25) by [whatsock.com](http://whatsock.com)
3.  The ARIA Role Conformance Matrices[26](31_Notes01.xhtml_Notes01_26) by [whatsock.com](http://whatsock.com)
4.  Mozilla’s ARIA overview article[27](31_Notes01.xhtml_Notes01_27)
5.  W3C’s ARIA overview page[28](31_Notes01.xhtml_Notes01_28)

## 1.6Quiz Questions

If you would like to look up the answers for the following quiz questions, you can check our discussion forum[29](31_Notes01.xhtml_Notes01_29). If you don’t find an answer in the forum, you may create a post asking for an answer to a particular question.

### 1.6.1Question 1: Well-Formed XML

Which of the following fragments represent well-formed XML? Select one or many:

### 1.6.2Question 2: HTML Forms

Recall that an HTML form is a section of an HTML document consisting of block elements that contain controls and labels on those controls. Which of the following form elements represent correct forms? Select one or many:

![](graphic/12_chapter01_fig_07.png)

# 2More on JavaScript

## 2.1JavaScript Basics

In this summary we try to take all important points of the classical JavaScript summary[30](31_Notes01.xhtml_Notes01_30) by Douglas Crockford[31](31_Notes01.xhtml_Notes01_31) into consideration.

### 2.1.1Types and data literals in JavaScript

JavaScript has three primitive datatypes: `string`, `number` and `boolean`, and we can test if a variable `v` holds a value of such a type with the help of the JS operator `typeof` as, for instance, in `typeof v === "number"`.

There are five reference types: `Object`, `Array`, `Function`, `Date` and `RegExp`. Arrays, functions, dates and regular expressions are special types of objects, but, conceptually, dates and regular expressions are primitive data values, and happen to be implemented in the form of wrapper objects.

The types of variables, array elements, function parameters and return values are not declared and are normally not checked by JavaScript engines. Type conversion (casting) is performed automatically.

The value of a variable may be

–a data value: either a string, a number, or a boolean;

–an object reference: either referencing an ordinary object, or an array, function, date, or regular expression;

–the special data value `null`, which is typically used as a default value for initializing an object variable;

–the special data value `undefined`, which is the implicit initial value of all variables that have been declared, but not initialized.

A string is a sequence of Unicode characters. String literals, like `"Hello world!", 'A3F0', or the empty string ""`, are enclosed in single or double quotes. Two string expressions can be concatenated with the `+` operator, and checked for equality with the triple equality operator:

![](graphic/13_chapter02_fig_01.png)

The number of characters of a string can be obtained by applying the `length` attribute to a string:

![](graphic/13_chapter02_fig_02.png)

All numeric data values are represented in 64-bit floating point format with an optional exponent (like in the numeric data literal `3.1e10`). There is no explicit type distinction between integers and floating point numbers. If a numeric expression cannot be evaluated to a number, its value is set to `NaN` (“not a number”), which can be tested with the built-in predicate `isNaN(`expr`)`.

Unfortunately, a built-in function, `Number. isInteger`, for testing if a number is an integer has only been introduced in ES6, so a polyfill[32](31_Notes01.xhtml_Notes01_32) is needed for using it in browsers that do not yet support it. For making sure that a numeric value is an integer, or that a string representing a number is converted to an integer, one has to apply the predefined function `parseInt`. Similarly, a string representing a decimal number can be converted to this number with `parseFloat`. For converting a number `n` to a string, the best method is using `String(n)`.

There are two predefined Boolean data literals, `true` and `false`, and the Boolean operator symbols are the exclamation mark `!` for NOT, the double ampersand `&&` for AND, and the double bar `||` for OR. When a non-Boolean value is used in a condition, or as an operand of a Boolean expression, it is implicitly converted into a Boolean value according to the following rules. The empty string, the (numerical) data literal 0, as well as `undefined` and `null`, are mapped to `false`, and all other values are mapped to `true`. This conversion can be performed explicitly with the help of the double negation operation, like in the equality test `!!undefined === false`, which evaluates to `true`.

In addition to strings, numbers and Boolean values, also calendar dates and times are important types of primitive data values, although they are not implemented as primitive values, but in the form of wrapper objects instantiating `Date`. Notice that `Date` objects do, in fact, not really represent dates, but rather date-time instants represented internally as the number of milliseconds since 1 January, 1970 UTC. For converting the internal value of a `Date` object to a human-readable string, we have several options. The two most important options are using either the standard format of ISO date/ time strings of the form “2015–01–27”, or localized formats of date/ time strings like “27.1\. 2015” (for simplicity, we have omitted the time part of the date/ time strings in these examples). When `x instanceof Date`, then `x.toISOString()` provides the ISO date/time string, and `x.toLocaleDateString()` provides the localized date/ time string. Given any date string `ds`, ISO or localized, `new Date(ds)` creates a corresponding date object.

For testing the equality (or inequality) of two primitive data vales, always use the triple equality symbol `===` (and `!==`) instead of the double equality symbol `==` (and `!=`). Otherwise, for instance, the number 2 would be the same as the string “2”, since the condition `(2 == "2")` evaluates to true in JavaScript.

Assigning an empty array literal, as in `var a = []` is the same as, but more concise than and therefore preferred to, invoking the `Array()` constructor without arguments, as in `var a = new Array()`.

Assigning an empty object literal, as in `var o = {}` is the same as, but more concise than and therefore preferred to, invoking the `Object()` constructor without arguments, as in `var o = new Object()`. Notice, however, that an empty object literal `{}` is not really an empty object, as it contains property slots and method slots inherited from `Object.prototype`[33](31_Notes01.xhtml_Notes01_33). So, a truly empty object (without any slots) has to be created with `null` as prototype, like in `var emptyObject = Object. create(null)`.

A summary of type testing is provided in the following table:

| Type | Example values | Test if x of type |
| string | “Hello world!”, ’A3F0’ | `typeof x === "string"` |
| boolean | true, false | `typeof x === "boolean"` |
| (floating point) number | -2.75, 0, 1, 1.0, 3.1e10 | `typeof x === "number"` |
| integer | -2, 0, 1, 250 | `Number.isInteger(x)*)` |
| Object | {}, {num:3, denom:4}, {isbn:”006251587X,” title:”Weaving the Web“}, {”one”:1, “two”:2, “three”:3} | excluding `null`: `x instanceof Object` including `null`: `typeof x === "object"` |
| Array[34](31_Notes01.xhtml_Notes01_34) | [], [“one”], [1,2,3], [1,”one”, {}] | `Array.isArray(x)` |
| Function[35](31_Notes01.xhtml_Notes01_35) | `function () { return "one"+1;}` | `typeof x === "function"` |
| Date[36](31_Notes01.xhtml_Notes01_36) | `new Date("2015`–`01`–`27")` | `x instanceof Date` |
| RegExp[37](31_Notes01.xhtml_Notes01_37) | `/(\w+)\s(\w+)/` | `x instanceof RegExp` |

A summary of type conversions is provided in the following table:

| Type | Convert to string | Convert string to type |
| boolean | `String(x)` | `Boolean(y)` |
| (floating point) number | `String(x)` | `parseFloat(y)` |
| integer | `String(x)` | `parseInt(y)` |
| Object | `x.toString()` or `JSON.stringify(x)` | `JSON.parse(y)` |
| Array Function | `x.toString()` or `JSON.stringify(x) x.toString()` | `y.split()` or `JSON.parse(y) new Function(y)` |
| Date RegExp | `x.toISOString() x.toString()` | `new Date(y) new RegExp(y)` |

### 2.1.2Variable scope

In the current version of JavaScript, ES5, there are only two kinds of scope for variables: the global scope (with `window` as the context object) and function scope, but no block scope. Consequently, declaring a variable within a code block is confusing and should be avoided. For instance, although this is a frequently used pattern, even by experienced JavaScript programmers, it is a pitfall to declare the counter variable of a `for` loop in the loop, as in

![](graphic/13_chapter02_fig_03.png)

Instead, and this is exactly how JavaScript is interpreting this code (by means of “hoisting” variable declarations), we should write:

![](graphic/13_chapter02_fig_04.png)

All variables should be declared at the beginning of a function. Only in the next version of JavaScript, ES6, block scope will be supported by means of a new form of variable declaration with the keyword `let`.

### 2.1.3Strict Mode

Starting from ES5, we can use strict mode[38](31_Notes01.xhtml_Notes01_38) for getting more runtime error checking. For instance, in strict mode, all variables must be declared. An assignment to an undeclared variable throws an exception.

We can turn strict mode on by typing the following statement as the first line in a JavaScript file or inside a `<script>` element:

![](graphic/13_chapter02_fig_05.png)

It is generally recommended that you use strict mode, except your code depends on libraries that are incompatible with strict mode.

### 2.1.4Different kinds of objects

JS objects are different from classical OO/UML objects. In particular, they need not instantiate a class. And they can have their own (instance-level) methods in the form of method slots, so they do not only have (ordinary) property slots, but also method slots. In addition they may also have key-value slots. So, they may have three different kinds of slots, while classical objects (called “instance specifications” in UML) only have property slots.

A JS object is essentially a set of name-value-pairs, also called slots, where names can be property names, function names or keys of a map. Objects can be created in an ad-hoc manner, using JavaScript’s object literal notation (JSON), without instantiating a class:

![](graphic/13_chapter02_fig_06.png)

An empty object with no slots is created in the following way:

![](graphic/13_chapter02_fig_07.png)

Whenever the name in a slot is an admissible JavaScript identifier[39](31_Notes01.xhtml_Notes01_39), the slot may be either a property slot, a method slot or a key-value slot. Otherwise, if the name is some other type of string (in particular when it contains any blank space), then the slot represents a key-value slot, which is a map element, as explained below.

The name in a property slot may denote either

1.  a data-valued property, in which case the value is a data value or, more generally, a data-valued expression; or
2.  an object-valued property, in which case the value is an object reference or, more generally, an object expression.

The name in a method slot denotes a JS function (better called method), and its value is a JS function definition expression.

Object properties can be accessed in two ways:

1.Using the dot notation (like in C++/Java):
`person1.lastName = "Smith"`

2.Using a map notation:
`person1["lastName"] = "Smith"`

JS objects can be used in many different ways for different purposes. Here are five different use cases for, or possible meanings of, JS objects:

1.A record is a set of property slots like, for instance,
`var myRecord = {firstName:"Tom", lastName:"Smith", age:26}`

2.A map (also called ’associative array’, ’dictionary’, ’hash map’ or ’hash table’ in other languages) supports look-ups of values based on keys like, for instance, `var numeral2number = {"one":"1", "two":"2", "three":"3"}` which associates the value “1” with the key “one”, “2” with “two”, etc. A key need not be a valid JavaScript identifier, but can be any kind of string (e. g. it may contain blank spaces).

3.An untyped object does not instantiate a class. It may have property slots and method slots like, for instance,

![](graphic/13_chapter02_fig_08.png)

Within the body of a method slot of an object, the special variable `this` refers to the object.

4.A namespace may be defined in the form of an untyped object referenced by a global object variable, the name of which represents a namespace prefix. For instance, the following object variable provides the main namespace of an application based on the Model-View-Controller (MVC) architecture paradigm where we have three subnamespaces corresponding to the three parts of an MVC application: `var myApp = { model:{}, view:{}, ctrl:{} };` A more advanced namespace mechanism can be obtained by using an immediately invoked JS function expression, as explained below.

5.A typed object instantiates a class that is defined either by a JavaScript constructor function or by a factory object. See Section 1.9, “Defining and using classes”

### 2.1.5Array lists

A JS array represents, in fact, the logical data structure of an array list, which is a list where each list item can be accessed via an index number (like the elements of an array). Using the term ’array’ without saying ’JS array’ creates a terminological ambiguity. But for simplicity, we will sometimes just say ’array’ instead of ’JS array’.

A variable may be initialized with a JS array literal:

![](graphic/13_chapter02_fig_09.png)

Because they are array lists, JS arrays can grow dynamically: it is possible to use indexes that are greater than the length of the array. For instance, after the array variable initialization above, the array held by the variable `a` has the length 3, but still we can assign a fifth array element like in

![](graphic/13_chapter02_fig_10.png)

The contents of an array `a` are processed with the help of a standard for loop with a counter variable counting from the first array index 0 to the last array index, which is `a.length-1`:

![](graphic/13_chapter02_fig_11.png)

Since arrays are special types of objects, we sometimes need a method for finding out if a variable represents an array. We can test, if a variable `a` represents an array by applying the predefined datatype predicate `isArray` as in `Array. isArray( a)`.

For adding a new element to an array, we append it to the array using the `push` operation as in:

![](graphic/13_chapter02_fig_12.png)

For deleting an element at position `i` from an array `a`, we use the predefined array method `splice` as in:

![](graphic/13_chapter02_fig_13.png)

For searching a value `v` in an array `a`, we can use the predefined array method `indexOf`, which returns the position, if found, or -1, otherwise, as in:

![](graphic/13_chapter02_fig_14.png)

For looping over an array `a`, we have two options: either use a `for` loop, or the array looping method `forEach`. In any case, we can use a `for` loop:

![](graphic/13_chapter02_fig_15.png)

If performance doesn’t matter, that is, if `a` is sufficiently small (say, it does not contain more than a few hundred elements), we can use the array looping method `forEach`, as in the following example, where the parameter `elem` iteratively assumes each element of the array `a` as its value:

![](graphic/13_chapter02_fig_16.png)

For cloning an array `a`, we can use the array function `slice` in the following way:

![](graphic/13_chapter02_fig_17.png)

### 2.1.6Maps

A map(also called ’hash map’ or ’associative array’) provides a mapping from keys to their associated values. The keys of a JS map are string literals that may include blank spaces like in:

![](graphic/13_chapter02_fig_18.png)

A map is processed with the help of a special loop where we loop over all keys of the map using the predefined function `Object.keys(m)`, which returns an array of all keys of a map `m`. For instance,

![](graphic/13_chapter02_fig_19.png)

For adding a new entry to a map, we simply associate the new value with its key as in:

![](graphic/13_chapter02_fig_20.png)

For deleting an entry from a map, we can use the predefined `delete` operator as in:

![](graphic/13_chapter02_fig_21.png)

For searching in a map if it contains an entry for a certain key value, such as for testing if the translation map contains an entry for “my bike” we can check the following:

![](graphic/13_chapter02_fig_22.png)

For looping over a map `m`,we first convert it to an array of its keys with the help of the predefined `Object.keys` method, and then we can use either a `for` loop or the `forEach` method. The following example shows how to loop with `for`:

![](graphic/13_chapter02_fig_23.png)

Again, if `m` is sufficiently small, we can use the `forEach` method, as in the following example:

![](graphic/13_chapter02_fig_24.png)

Notice that using the `forEach` method is more concise.

For cloning a map `m`, we can use the composition of JSON.stringify and JSON. parse. We first serialize `m` to a string representation with JSON.stringify, and then de-serialize the string representation to a map object with JSON.parse:

![](graphic/13_chapter02_fig_25.png)

Notice that this method works well if the map contains only simple data values or (possibly nested) arrays/maps containing simple data values. In other cases, e. g. if the map contains `Date` objects, we have to write our own clone method.

### 2.1.7JavaScript supports four types of basic data structures

In summary, the four types of basic data structures supported are:

1.  array lists, such as `["one","two","three"]`, which are special JS objects called ’arrays’, but since they are dynamic, they are rather array lists as defined in the Java programming language.
2.  records, which are special JS objects, such as `{ firstName:"Tom", lastName:"Smith"}`, as discussed above,
3.  maps, which are also special JS objects, such as `{"one":1, "two":2, "three":3}`, as discussed above,
4.  entity tables, like for instance the table shown below, which are special maps where the values are entity records with a standard ID (or primary key) slot, such that the keys of the map are the standard IDs of these entity records.

Table 2.1 An example of an entity table representing a collection of books

| Key | Value |
| 006251587X | { isbn:”006251587X,” title:”Weaving the Web”, year:2000} |
| 0465026567 | { isbn:”0465026567,” title:”Gödel, Escher, Bach”, year:1999} |
| 0465030793 | { isbn:”0465030793,” title:”I Am A Strange Loop”, year:2008} |

Notice that our distinction between maps, records and entity tables is a purely conceptual distinction, and not a syntactical one. For a JavaScript engine, both `{firstName:"Tom", lastName:"Smith"}` and `{"one":1,"two":2,"three":3}` are just objects. But conceptually, `{firstName:"Tom", lastName:"Smith"}` is a record because `firstName` and `lastName` are intended to denote properties (or fields), while `{"one":1,"two":2,"three":3}` is a map because `"one"` and `"two"` are not intended to denote properties/fields, but are just arbitrary string values used as keys for a map.

Making such conceptual distinctions helps in the logical design of a program, and mapping them to syntactic distinctions, even if they are not interpreted differently, helps to better understand the intended computational meaning of the code and therefore improves its readability.

### 2.1.8Procedures, methods and functions

Generally, a (parametrized) procedure is like a sub-program that can be called (with a certain number of arguments) any number of times from within a program. Whenever a procedure returns a value, it is called a function. In OOP, procedures are called methods, if they are defined in the context of a class or of an object.

In JavaScript, methods are called “functions”, no matter if they return a value or not. As shown below in [Figure 2.1](#13_chapter02.xhtml_chapter02_35), JS functions are special JS objects, having an optional `name` property and a `length` property providing their number of parameters. If a variable `v` references a function can be tested with

![](graphic/13_chapter02_fig_26.png)

Being JS objects implies that JS functions can be stored in variables, passed as arguments to functions, returned by functions, have properties and can be changed dynamically. Therefore, JS functions are first-class citizens, and JavaScript can be viewed as a functional programming language.

The general form of a JS function definition is an assignment of a JS function expression to a variable:

![](graphic/13_chapter02_fig_27.png)

where `params` is a comma-separated list of parameters (or a parameter record), and `theNameOfMyMethod` is optional. When it is omitted, the method/ function is anonymous. In any case, JS functions are normally invoked via a variable that references the function. In the above case, this means that the JS function is invoked with `myMethod()`, and not with `theNameOfMyMethod()`. However, a named JS function can be invoked by name from within the function (for recursion). Consequently, a recursive JS function must be named.

Anonymous function expressions are called lambda expressions (or shorter lambdas) in other programming languages.

As an example of an anonymous function expression being passed as an argument in the invocation of another (higher-order) function, we can take a comparison function being passed to the predefined function `sort` for sorting the elements of an array list. Such a comparison function must return a negative number if its first argument is smaller than its second argument, it must return 0 if both arguments are of the same rank, and it must return a positive number if the second argument is smaller than the first one. In the following example, we sort a list of lists of 2 numbers in lexicographic order:

![](graphic/13_chapter02_fig_28.png)

A JS function declaration has the following form:

![](graphic/13_chapter02_fig_29.png)

It is equivalent to the following named function definition:

![](graphic/13_chapter02_fig_30.png)

that is, it creates both a function with name `theNameOfMyMethod` and a variable `theNameOfMyMethod` referencing this function.

JS functions can have inner functions. The closure mechanism allows a JS function using variables (except `this`) from its outer scope, and a function created in a closure remembers the environment in which it was created. In the following example, there is no need to pass the outer scope variable `result` to the inner function via a parameter, as it is readily available:

![](graphic/13_chapter02_fig_31.png)

When a method/function is executed, we can access its arguments within its body by using the built-in `arguments` object, which is “array-like” in the sense that it has indexed elements and a `length` property, and we can iterate over it with a normal `for` loop, but since it’s not an instance of `Array`, the JS array methods (such as the `forEach` looping method) cannot be applied to it. The `arguments` object contains an element for each argument passed to the method. This allows defining a method without parameters and invoking it with any number of arguments, like so:

![](graphic/13_chapter02_fig_32.png)

A method defined on the prototype of a constructor function, which can be invoked on all objects created with that constructor, such as `Array. prototype.forEach`, where `Array` represents the constructor, has to be invoked with an instance of the class as context object referenced by the `this` variable (see also the next section on classes). In the following example, the array `numbers` is the context object in the invocation of `forEach`:

![](graphic/13_chapter02_fig_33.png)

Whenever such a prototype method is to be invoked not with a context object, but with an object as an ordinary argument, we can do this with the help of the JS function `call` method that takes an object, on which the method is invoked, as its first parameter, followed by the parameters of the method to be invoked. For instance, we can apply the `forEach` looping method to the array-like object `arguments` in the following way:

![](graphic/13_chapter02_fig_34.png)

A two-argument variant of the `Function.prototype.call` method, collecting all arguments of the method to be invoked in an array-like object, is `Function.prototype.apply`. The first argument to both `call` and `apply` becomes `this` inside the function, and the rest are passed through. So, `f.call( x, y, z)` is the same as `f.apply( x, [y, z])`.

Whenever a method defined for a prototype is to be invoked without a context object, or when a method defined in a method slot (in the context) of an object is to be invoked without its context object, we can bind its `this` variable to a given object with the help of the JS function `bind` method (`Function.prototype.bind`). This allows creating a shortcut for invoking a method, as in `var querySel = document.querySelector.bind( document)`,which allows to use `querySel` instead of `document.querySelector`.

The option of immediately invoked JS function expressions can be used for obtaining a namespace mechanism that is superior to using a plain namespace object, since it can be controlled which variables and methods are globally exposed and which are not. This mechanism is also the basis for JS module concepts. In the following example, we define a namespace for the model code part of an app, which exposes some variables and the model classes in the form of constructor functions:

![](graphic/13_chapter02_fig_35.png)

### 2.1.9Defining and using classes

The concept of a class is fundamental in object-oriented programming. Objects instantiate (or are classified by) a class. A class defines the properties and methods (as a blueprint) for the objects created with it.

Having a class concept is essential for being able to implement a data model in the form of model classes in a Model-View-Controller (MVC) architecture. However, classes and their inheritance/extension mechanism are over-used in classical OO languages, such as in Java, where all variables and procedures have to be defined in the context of a class and, consequently, classes are not only used for implementing object types (or model classes), but also as containers for many other purposes in these languages. This is not the case in JavaScript where we have the freedom to use classes for implementing object types only, while keeping method libraries in namespace objects.

Any code pattern for defining classes in JavaScript should satisfy five requirements. First of all, (1) it should allow to define a class name, a set of (instance-level) properties, preferably with the option to keep them ’private’, a set of (instance-level) methods, and a set of class-level properties and methods. It’s desirable that properties can be defined with a range/ type, and with other meta-data, such as constraints. There should also be two introspection features: (2) an is-instance-of predicate that can be used for checking if an object is a direct or indirect instance of a class, and (3) an instance-level property for retrieving the direct type of an object. In addition, it is desirable to have a third introspection feature for retrieving the direct supertype of a class. And finally, there should be two inheritance mechanisms: (4) property inheritance and (5) method inheritance. In addition, it is desirable to have support for multiple inheritance and multiple classifications, for allowing objects to play several roles at the same time by instantiating several role classes.

There was no explicit class definition syntax in JavaScript before ES6\. Different code patterns for defining classes in JavaScript have been proposed and are being used in different frameworks. But they do often not satisfy the five requirements listed above. The two most important approaches for defining classes are:

1.  In the form of a constructor function that achieves method inheritance via the prototype chain and allows to create new instances of a class with the help of the `new` operator. This is the classical approach recommended by Mozilla in their JavaScript Guide[40](31_Notes01.xhtml_Notes01_40). This is also the approach implemented in ES6 with the new `class` definition syntax.
2.  In the form of a factory object that uses the predefined `Object. create` method for creating new instances of a class. In this approach, the prototype chain method inheritance mechanism is replaced by a “copy & append” mechanism. Eric Elliott[41](31_Notes01.xhtml_Notes01_41) has argued that factory-based classes are a viable alternative to constructor-based classes in JavaScript (in fact, he even condemns the use of classical inheritance with constructor-based classes, throwing out the baby with the bath water).

When building an app, we can use both kinds of classes, depending on the requirements of the app. Since we often need to define class hierarchies, and not just single classes, we have to make sure, however, that we don’t mix these two alternative approaches within the same class hierarchy. While the factory-based approach, as exemplified by mODELcLASSjs[42](31_Notes01.xhtml_Notes01_42), has many advantages, which are summarized in [Table 2.2](#13_chapter02.xhtml_chapter02_29), the constructor-based approach enjoys the advantage of higher performance object creation.

Table 2.2 Required and desirable features of JS code patterns for classes

![](graphic/13_chapter02_fig_36.png)

#### 2.1.9.1Constructor-based classes

Only in ES6, a user-friendly syntax for constructor-based classes has been introduced. In Step 1.a), a base class `Person` is defined with two properties, `firstName` and `lastName`, as well as with an (instance-level) method `toString` and a static (class-level) method `checkLastName`:

![](graphic/13_chapter02_fig_37.png)

In Step 1.b), class-level (“static”) properties are defined:

![](graphic/13_chapter02_fig_38.png)

Finally, in Step 2, a subclass is defined with additional properties and methods that possibly override the corresponding superclass methods:

![](graphic/13_chapter02_fig_39.png)

In ES5, we can define a base class with a subclass in the form of constructor functions, following a code pattern recommended by Mozilla in their JavaScript Guide[44](31_Notes01.xhtml_Notes01_44), as shown in the following steps.

Step 1.a) First define the constructor function that implicitly defines the properties of the class by assigning them the values of the constructor parameters when a new object is created:

![](graphic/13_chapter02_fig_40.png)

Notice that within a constructor, the special variable `this` refers to the new object that is created when the constructor is invoked.

Step 1.b) Next, define the instance-level methods of the class as method slots of the object referenced by the constructor’s `prototype` property:

![](graphic/13_chapter02_fig_41.png)

Step 1.c) Class-level (“static”) methods can be defined as method slots of the constructor function itself (recall that, since JS functions are objects, they can have slots), as in

![](graphic/13_chapter02_fig_42.png)

Step 1.d) Finally, define class-level (“static”) properties as property slots of the constructor function:

![](graphic/13_chapter02_fig_43.png)

Step 2.a) Define a subclass with additional properties:

![](graphic/13_chapter02_fig_44.png)

By invoking the supertype constructor with `Person.call( this,` …`)` for any new object created as an instance of the subtype `Student`, and referenced by `this`, we achieve that the property slots created in the supertype constructor (`firstName` and `lastName`) are also created for the subtype instance, along the entire chain of supertypes within a given class hierarchy. In this way we set up a property inheritance mechanism that makes sure that the own properties defined for an object on creation include the own properties defined by the supertype constructors.

In Step 2b), we set up a mechanism for method inheritance via the constructor’s `prototype` property. We assign a new object created from the supertype’s `prototype` object to the `prototype` property of the subtype constructor and adjust the prototype’s constructor property:

![](graphic/13_chapter02_fig_45.png)

With `Object.create( Person.prototype)` we create a new object with `Person.prototype` as its prototype and without any own property slots. By assigning this object to the `prototype` property of the subclass constructor, we achieve that the methods defined in, and inherited from, the superclass are also available for objects instantiating the subclass. This mechanism of chaining the prototypes takes care of method inheritance. Notice that setting `Student.prototype` to `Object.create( Person.prototype)` is preferable over setting it to `new Person()`, which was the way to achieve the same in the time before ES5.

Step 2c) Define a subclass method that overrides a superclass method:

![](graphic/13_chapter02_fig_46.png)

An instance of a constructor-based class is created by applying the `new` operator to the constructor and providing suitable arguments for the constructor parameters:

![](graphic/13_chapter02_fig_47.png)

The method `toString` is invoked on the object `pers1` by using the ’dot notation’:

![](graphic/13_chapter02_fig_48.png)

When an object `o` is created with `o = new C(`…`)`, where `C` references a named function with name “C”, the type (or class) name of `o` can be retrieved with the introspective expression [`o.constructor.name`](http://o.constructor.name)[](http://o.constructor.name), which returns “C”. The `Function::name` property used in this expression is supported by all browsers, except Internet Explorer versions before version 11.

In JavaScript, a prototype object is an object with method slots (and sometimes also property slots) that can be inherited by other objects via JavaScript’s method/ property slot look-up mechanism. This mechanism follows the prototype chain defined by the (in ES5 still unofficial) built-in reference property `__proto__` (with a double underscore prefix and suffix) for finding methods or properties. As shown below in [Figure 2.1](#13_chapter02.xhtml_chapter02_35), every constructor function has a reference to a prototype object as the value of its reference property `prototype`. When a new object is created with the help of `new`, its `__proto__` property is set to the constructor’s `prototype` property.

For instance, after creating a new object with `f = new Foo()`, it holds that `Object.getPrototypeOf(f)`, which is the same as `f.__proto__`, is equal to `Foo. prototype`. Consequently, changes to the slots of `Foo.prototype` affect all objects that were created with `new Foo()`.While every object has a `__proto__` property slot (except `Object`), only objects constructed with `new` have a `constructor` property slot.

![](graphic/13_chapter02_fig_49.png)

Figure 2.1 The built-in JavaScript classes `Object` and `Function`.

Notice that we can retrieve the prototype of an object with `Object. getPrototypeOf(o)`, which is an official ES5 alternative to `o.__proto__`.

#### 2.1.9.2Factory-based classes

In this approach we define a JS object `Person` (actually representing a class) with a special `create` method that invokes the predefined `Object. create` method for creating objects of type `Person`:

![](graphic/13_chapter02_fig_50.png)

Notice that the JS object `Person` actually represents a factory-based class. An instance of such a factory-based class is created by invoking its `create` method:

![](graphic/13_chapter02_fig_51.png)

The method `getFullName` is invoked on the object `pers1` of type `Person` by using the ’dot notation’, like in the constructor-based approach:

![](graphic/13_chapter02_fig_52.png)

Notice that each property declaration for an object created with `Object. create` has to include the ’descriptors’ `writable: true` and `enumerable: true`, as in lines 5 and 7 of the `Person` object definition above.

In a general approach, like in the mODELcLASSjs[45](31_Notes01.xhtml_Notes01_45) library for model-based development, we would not repeatedly define the `create` method in each class definition, but rather have a generic constructor function for defining factory-based classes. Such a factory-based class constructor, like mODELcLASS, would also provide an inheritance mechanism by merging the own properties and methods with the properties and methods of the superclass. This mechanism is also called Inheritance by Concatenation[46](31_Notes01.xhtml_Notes01_46).

### 2.1.10Quiz Questions

If you would like to look up the answers for the following quiz questions, you can check our discussion forum[47](31_Notes01.xhtml_Notes01_47). If you don’t find an answer in the forum, you may create a post asking for an answer to a particular question.

##### 2.1.10.1 Question 1: Deleting a map entry

Which JavaScript statement can be used for deleting a map entry with key `"k"` from a map `m`?

Answer: ________________________________

#### 2.1.10.2Question 2: Evaluating a Boolean expression

What is the value of the Boolean expression `null || !0` ? Select one:

○ true ○ false (select one)

#### 2.1.10.3Question 3: JavaScript datatypes

Which of the following denote primitive datatypes in JavaScript? Select one or many:

☐ double ☐ string ☐ float ☐ int ☐ boolean ☐ byte ☐ number

#### 2.1.10.4Question 4: Constructor-based class definition

![](graphic/13_chapter02_fig_53.png)

Which of the following JavaScript fragments correctly defines the constructor-based class `City` shown in the class diagram? Hint: notice that `setName` is an instance-level method while `checkName` is a class-level (“static”) method.

Select one or many:

![](graphic/13_chapter02_fig_54.png)

#### 2.1.10.5Question 5: Variable scope

What is the output of the following program?

![](graphic/13_chapter02_fig_55.png)

Answer: _____

## 2.2Storing Database Tables with JavaScript’s localStorage API

In most apps, we have some form of data management where data is represented in tables such that table rows correspond to objects, and the table schema corresponds to the objects’ type. When building a front-end web app with JavaScript, the simplest approach for persistent data storage is using JavaScript’s `localStorage` API, which provides a simple key-value database, but does not support database tables. So, the question is: how can we store and retrieve tables with Local Storage?

We show how to represent database tables in JavaScript in the form of (what we call) entity tables, and how to store these tables in Local Storage.

### 2.2.1Entity Tables

The JavaScript Object Notation (JSON)[48](31_Notes01.xhtml_Notes01_48) defines a concise syntax for JavaScript array literals (lists) and JavaScript object literals (maps):

–Lists are expressed as comma-separated lists of data literals enclosed in brackets:

![](graphic/13_chapter02_fig_56.png)

–Maps are expressed as comma-separated lists of key-value slots enclosed in curly braces:

![](graphic/13_chapter02_fig_57.png)

A record is a special type of map where the keys are admissible JavaScript identifiers[49](31_Notes01.xhtml_Notes01_49) denoting properties, so they need not be enclosed in quotation marks in JavaScript code. For example, {id: 2901465, phone:”0049.30.227109“} is a record. The value of a property in a record, or the value associated with a key in a map, may be a simple data literal, or an array literal, or another object literal as in:

![](graphic/13_chapter02_fig_58.png)

An entity table contains a set of records (or table rows) such that each record represents an object with a standard identifier property slot. Consequently, an entity table can be represented as a mapof records such that the keys of the map are the values of the standard identifier property, and their associated values are the corresponding records, as illustrated by the following example:

| Key | Value |
| 006251587X 0465026567 0465030793 | { isbn:”006251587X,” title:”Weaving the Web”, year:2000} { isbn:”0465026567,” title:”Gödel, Escher, Bach”, year:1999} { isbn:”0465030793,” title:”I Am A Strange Loop”, year:2008} |

### 2.2.2JavaScript’s LocalStorage API

For a front-end app, we need to be able to store data persistently on the front-end device. Modern web browsers provide two technologies for this purpose: the simpler one is called Local Storage, and the more powerful one is called IndexedDB[50](31_Notes01.xhtml_Notes01_50). For simplicity, we use the Local Storage API in our example app.

A Local Storage database is created per browser and per origin, which is defined by the combination of protocol and domain name. For instance, `http://example.com` and [`http://www.example.com`](http://www.example.com) are different origins because they have different domain names, while [`http://www.example.com`](http://www.example.com) and `https://www.example.com` are different origins because of their different protocols (HTTP versus HTTPS).

The Local Storage database managed by the browser and associated with an app (via its origin) is exposed as the built-in JavaScript object `localStorage` with the methods `getItem`, `setItem`, `removeItem` and `clear`. However, instead of invoking `getItem` and `setItem`, it is more convenient to handle `localStorage` as a map, writing to it by assigning a value to a key as in `localStorage["id"] = 2901465`, and retrieving data by reading the map as in `var id = localStorage["id"]`. The following example shows how to create an entity table and save its serialization to Local Storage:

![](graphic/13_chapter02_fig_59.png)

Notice that we have used the predefined method `JSON.stringify` for serializing the entity table `persons` into a string that is assigned as the value of the `localStorage` key “personTable”. We can retrieve the table with the help of the predefined de-serialization method `JSON.parse` in the following way:

![](graphic/13_chapter02_fig_60.png)

# 3Building a Minimal Web App with Plain JS in Seven Steps

In this chapter, we show how to build a minimal front-end web application with plain JavaScript and Local Storage. The purpose of our example app is to manage information about books. That is, we deal with a single object type: `Book`, as depicted in the class diagram of [Figure 3.1](#14_chapter03.xhtml_chapter03_2).

![](graphic/14_chapter03_fig_01.png)

Figure 3.1 The object type `Book`.

The following table shows a sample data population for the model class `Book`:

Table 3.1 A collection of book objects represented as a table

| ISBN | Title | Year |
| 006251587X | Weaving the Web | 2000 |
| 0465026567 | Gödel, Escher, Bach | 1999 |
| 0465030793 | I Am A Strange Loop | 2008 |

What do we need for a data management app? There are four standard use cases, which have to be supported by the app:

1.  Create a new book record by allowing the user to enter the data of a book that is to be added to the collection of stored book records.
2.  Retrieve (or read) all books from the data store and show them in the form of a list.
3.  Update the data of a book record.
4.  Delete a book record.

These four standard use cases, and the corresponding data management operations, are often summarized with the acronym CRUD.

For entering data with the help of the keyboard and the screen of our computer, we use HTML forms, which provide the user interface technology for web applications.

For maintaining a collection of persistent data objects, we need a storage technology that allows to keep data objects in persistent records on a secondary storage device, such as a hard-disk or a solid state disk. Modern web browsers provide two such technologies: the simpler one is called Local Storage, and the more powerful one is called IndexedDB[51](32_Notes02.xhtml_Notes02_1). For our minimal example app, we use Local Storage.

## 3.1Step 1 – Set up the Folder Structure

In the first step, we set up our folder structure for the application. We pick a name for our app, such as “Public Library”, and a corresponding (possibly abbreviated) name for the application folder, such as “PublicLibrary” or `MinimalApp`. Then we create this folder on our computer’s disk and a subfolder “src” for our JavaScript source code files. In this folder, we create the subfolders “m”, “v” and “c”, following the Model-View-Controller paradigm for software application architectures. And finally we create an `index. html` file for the app’s start page, as discussed below. Thus, we end up with the following folder structure:

MinimalApp

![](graphic/14_chapter03_fig_02.png)

In the start page HTML file of the app, we load the file `initialize.js` and the `Book. js` model class file:

![](graphic/14_chapter03_fig_03.png)

The start page provides a menu for choosing one of the CRUD data management use cases. Each use case is performed by a corresponding page such as, for instance, `createBook.html`. The menu also contains options for creating test data with the help of the procedure `Book.createTestData()` and for clearing all data with `Book. clearData()`:

![](graphic/14_chapter03_fig_04.png)

## 3.2Step 2 – Write the Model Code

In the second step, we write the code of our model class and save it in a specific model class file. In an MVC app, the model code is the most important part of the app. It’s also the basis for writing the view and controller code. In fact, large parts of the view and controller code could be automatically generated from the model code. Many MVC frameworks provide this kind of code generation.

In the information design model shown in [Figure 3.1](#14_chapter03.xhtml_chapter03_2) above, there is only one class, representing the object type `Book`. So, in the folder `src/m`, we create a file `Book.js` that initially contains the following code:

![](graphic/14_chapter03_fig_05.png)

The model class `Book` is coded as a JavaScript constructor function with a single `slots` parameter, which is a record object with fields `isbn`, `title` and `year`, representing the constructor parameters to be assigned to the ISBN, the title and the year attributes of the class `Book`. Notice that, for getting a simple name, we have put the class name `Book` in the global scope, which is okay for a small app with only a few classes. In general, however, we should use the model namespace for model classes, which requires class/constructor definitions like

![](graphic/14_chapter03_fig_06.png)

In addition to defining the model class in the form of a constructor function, we also define the following items in the `Book. js` file:

1.  A class-level property `Book. instances` representing the collection of all `Book` instances managed by the application in the form of an entity table.
2.  A class-level method `Book. retrieveAll` for loading all managed Book instances from the persistent data store.
3.  A class-level method `Book. saveAll` for saving all managed Book instances to the persistent data store.
4.  A class-level method `Book. add` for creating a new Book instance.
5.  A class-level method `Book. update` for updating an existing Book instance.
6.  A class-level method `Book. destroy` for deleting a Book instance.
7.  A class-level method `Book. createTestData` for creating a few example book records to be used as test data.
8.  A class-level method `Book. clearData` for clearing the book datastore.

### 3.2.1Representing the collection of all Book instances

For representing the collection of all Book instances managed by the application, we define and initialize the class-level property `Book. instances` in the following way:

![](graphic/14_chapter03_fig_07.png)

So, initially our collection of books is empty. In fact, it’s defined as an empty object literal, since we want to represent it in the form of an entity table (a map of entity records) where an ISBN is a key for accessing the corresponding book record (as the value associated with the key). We can visualize the structure of an entity table in the form of a lookup table:

| Key | Value |
| 006251587X | { isbn:”006251587X,” title:”Weaving the Web”, year:2000} |
| 0465026567 | { isbn:”0465026567,” title:”Gödel, Escher, Bach”, year:1999} |
| 0465030793 | { isbn:”0465030793,” title:”I Am A Strange Loop”, year:2008} |

Notice that the values of such a map are records corresponding to table rows. Consequently, we could also represent them in a simple table, as shown in [Table 3.1](#14_chapter03.xhtml_chapter03_3).

### 3.2.2Creating a new Book instance

The `Book. add` procedure takes care of creating a new `Book` instance and adding it to the `Book.instances` collection:

![](graphic/14_chapter03_fig_08.png)

### 3.2.3Loading all Book instances

For persistent data storage, we use the Local Storage API supported by modern web browsers. Loading the book records from Local Storage involves three steps:

1.Retrieving the book table that has been stored as a large string with the key “books” from Local Storage with the help of the assignment

![](graphic/14_chapter03_fig_09.png)

2.Converting the book table string into a corresponding entity table `books` with book rows as elements, with the help of the built-in procedure `JSON.parse`:

![](graphic/14_chapter03_fig_10.png)

This conversion is called de-serialization.

3.Converting each row of `books`, representing a record (an untyped object), into a corresponding object of type `Book` stored as an element of the entity table `Book.instances`, with the help of the procedure `convertRec2Obj` defined as a “static” (class-level) method in the `Book` class:

![](graphic/14_chapter03_fig_11.png)

Here is the full code of the procedure:

![](graphic/14_chapter03_fig_12.png)![](graphic/14_chapter03_fig_13.png)

Notice that since an input operation like `localStorage["books"]` may fail, we perform it in a try-catch block, where we can follow up with an error message whenever the input operation fails.

### 3.2.4Updating a Book instance

For updating an existing `Book` instance we first retrieve it from `Book. instances`, and then re-assign those attributes the value of which has changed:

![](graphic/14_chapter03_fig_14.png)

### 3.2.5Deleting a Book instance

A Book instance is deleted from the entity table `Book. instances` by first testing if the table has a row with the given key (line 2), and then applying the JavaScript built-in `delete` operator, which deletes a slot from an object, or an entry from a map:

![](graphic/14_chapter03_fig_15.png)

### 3.2.6Saving all Book instances

Saving all book objects from the `Book. instances` collection in main memory to Local Storage in secondary memory involves two steps:

1\. Converting the entity table `Book. instances` into a string with the help of the predefined JavaScript procedure `JSON.stringify`:

![](graphic/14_chapter03_fig_16.png)

This conversion is called serialization.

2\. Writing the resulting string as the value of the key “books” to Local Storage:

![](graphic/14_chapter03_fig_17.png)

These two steps are performed in line 5 and in line 6 of the following program listing:

![](graphic/14_chapter03_fig_18.png)

### 3.2.7Creating test data

For being able to test our code, we may create some test data and save it in our Local Storage database. We can use the following procedure for this:

![](graphic/14_chapter03_fig_19.png)

### 3.2.8Clearing all data

The following procedure clears all data from Local Storage:

![](graphic/14_chapter03_fig_20.png)

## 3.3Step 3 – Initialize the Application

We initialize the application by defining its namespace and MVC sub-namespaces. Namespaces are an important concept in software engineering and many programming languages, including Java and PHP, provide specific support for namespaces, which help grouping related pieces of code and avoiding name conflicts. Since there is no specific support for namespaces in JavaScript, we use special objects for this purpose (we may call them “namespace objects”). First we define a root namespace (object) for our app, and then we define three sub-namespaces, one for each of the three parts of the application code: model, view and controller. In the case of our example app, we may use the following code for this:

![](graphic/14_chapter03_fig_21.png)

Here, the main namespace is defined to be `pl`, standing for “Public Library”, with the three sub-namespaces `m`, `v` and `c` being initially empty objects. We put this code in a separate file `initialize.js` in the `c` folder, because such a namespace definition belongs to the controller part of the application code.

## 3.4Step 4 – Implement the Create Use Case

For our example app, the user interface page for the CRUD use case Create is called `createBook. html` located in the `MinimalApp` folder. In its `head` element, it loads the app initialization file `initialize. js`, the model class file `Book. js` and the view code file `createBook. js`, and adds a `load` event listener for setting up the Create user interface:

![](graphic/14_chapter03_fig_22.png)![](graphic/14_chapter03_fig_23.png)

For a data management use case with user input, such as “Create”, an HTML form is required as a user interface. The form typically has a labelled `input` or `select` field for each attribute of the model class:

![](graphic/14_chapter03_fig_24.png)

The view code file `src/ v/createBook. js` contains two procedures:

1.  `setupUserInterface` takes care of retrieving the collection of all objects from the persistent data store and setting up an event handler (`handleSaveButtonClickEvent`) on the save button for handling click button events by saving the user input data;
2.  `handleSaveButtonClickEvent` reads the user input data from the form fields and then saves this data by calling the `Book. add` procedure.

![](graphic/14_chapter03_fig_25.png)![](graphic/14_chapter03_fig_26.png)

## 3.5Step 5 – Implement the Retrieve/List All Use Case

The user interface for the CRUD use case Retrieve consists of an HTML table for displaying the data of all model objects. For our example app, this page is called `retrieveAndListAllBooks.html`, located in the main folder `MinimalApp`, and it contains the following code in its `head` element:

![](graphic/14_chapter03_fig_27.png)

Notice that, in addition to loading the app initialization JS file and the model class JS file, we load the view code file (here: `retrieveAndListAllBooks.js`) and invoke its `setupUserInterface` procedure via a `load` event listener. This is the pattern we use for all four CRUD use cases.

![](graphic/14_chapter03_fig_28.png)

In the `setupUserInterface` procedure, we first set up the data management context by retrieving all book data from the database and then fill the table by creating a table row for each book object from `Book. instances`:

![](graphic/14_chapter03_fig_29.png)

More specifically, the procedure `setupUserInterface` creates the view table in a loop over all objects of `Book. instances`. In each step of this loop, a new row is created in the table body element with the help of the JavaScript DOM operation `insertRow()`, and then three cells are created in this row with the help of the DOM operation `insertCell()`: the first one for the `isbn` property value of the book object, and the second and third ones for its `title` and `year` property values. Both `insertRow` and `insertCell` have to be invoked with the argument -1 for making sure that new elements are appended to the list of rows and cells.

## 3.6Step 6 – Implement the Update Use Case

Also for the Update use case, we have an HTML page for the user interface (`updateBook.html`) and a view code file (`src/v/updateBook.js`). The HTML form for the UI of the “update book” operation has a selection field for choosing the book to be updated, an `output` field for the standard identifier attribute `isbn`, and an `input` field for each attribute of the `Book` class that can be updated. Notice that by using an `output` field for the standard identifier attribute, we do not allow changing the standard identifier of an existing object.

![](graphic/14_chapter03_fig_30.png)![](graphic/14_chapter03_fig_31.png)

Notice that we include a kind of empty option element, with a value of `""` and a display text of—, as a default choice in the `selectBook` selection list element. So, by default, the `value` of the `selectBook` form control is empty, requiring the user to choose one of the available options for filling the form.

The `setupUserInterface` procedure now has to populate the `select` element’s option list by loading the collection of all book objects from the data store and creating an option element for each book object:

![](graphic/14_chapter03_fig_32.png)

A book selection event is caught via a listener for `change` events on the `select` element. When a book is selected, the form is filled with its data:

![](graphic/14_chapter03_fig_33.png)![](graphic/14_chapter03_fig_34.png)

When the save button is activated, a `slots` record is created from the form field values and used as the argument for calling `Book. update`:

![](graphic/14_chapter03_fig_35.png)

## 3.7Step 7 – Implement the Delete Use Case

The user interface for the Delete use case just has a `select` field for choosing the book to be deleted:

![](graphic/14_chapter03_fig_36.png)

Like in the Update case, the `setupUserInterface` procedure in the view code in `src/ v/deleteBook. js` loads the book data into main memory, populates the book selection list and adds some event listeners. The event handler for Delete button click events.

![](graphic/14_chapter03_fig_37.png)![](graphic/14_chapter03_fig_38.png)

## 3.8Run the App and Get the Code

You can run the minimal app[52](32_Notes02.xhtml_Notes02_2) from our server or download the code[53](32_Notes02.xhtml_Notes02_3) as a ZIP archive file.

## 3.9Possible Variations and Extensions

### 3.9.1Using IndexedDB as an Alternative to LocalStorage

Instead of using the Local Storage API, the IndexedDB[54](32_Notes02.xhtml_Notes02_4) API could be used for locally storing the application data. With Local Storage you only have one database (which you may have to share with other apps from the same domain) and there is no support for database tables (we have worked around this limitation in our approach). With IndexedDB you can set up a specific database for your app, and you can define database tables, called ’object stores’, which may have indexes for accessing records with the help of an indexed attribute instead of the standard identifier attribute. Also, since IndexedDB supports larger databases, its access methods are asynchronous and can only be invoked in the context of a database transaction.

Alternatively, for remotely storing the application data with the help of a web API one can either use a back-end solution component or a cloud storage service. The remote storage approach allows managing larger databases and supports multi-user apps.

### 3.9.2Styling the User Interface

For simplicity, we have used raw HTML without any CSS styling. But a user interface should be appealing. So, the code of this app should be extended by adding suitable CSS style rules.

Today, the UI pages of a web app have to be adaptive (frequently called “responsive”) for being rendered on different devices with different screen sizes and resolutions, which can be detected with CSS media queries. The main issue of an adaptive UI is to have a fluid layout, in addition to proper viewport settings. Whenever images are used in a UI, we also need an approach for adaptive bitmap images: serving images in smaller sizes for smaller screens and in higher resolutions for high resolution screens, while preferring scalable SVG images for diagrams and artwork. In addition, we may decrease the font-size of headings and suppress unimportant content items on smaller screens.

For our purposes, and for keeping things simple, we customize the adaptive web page design defined by the HTML5 Boilerplate[55](32_Notes02.xhtml_Notes02_5) project (more precisely, the minimal “responsive” configuration available on [www.initializr.com)](http://www.initializr.com). It just consists of an HTML template file and two CSS files: the browser style normalization file `normalize.css` (in its minified form) and a `main.css`, which contains the HTML5 Boilerplate style and our customizations. Consequently, we use a new `css` subfolder containing these two CSS files:

![](graphic/14_chapter03_fig_39.png)

One customization change we have made in `index.html` is to replace the `<div class="main">` container element with the new HTML 5.1 element `<main>` such that we obtain a simple and clear UI page structure provided by the sequence of the three container elements `<header>`, `<main>` and `<footer>`. This change in the HTML file requires corresponding changes in `main.css`. In addition, we define our own styles for `<table>`, `<menu>` and `<form>` elements. Concerning the styling of HTML forms, we define a simple style for implicitly labeled form control elements.

The start page `index.html` now must take care of loading the CSS page styling files with the help of the following two `link` elements:

![](graphic/14_chapter03_fig_40.png)

Since the styling of user interfaces is not our primary concern, we do not discuss the details of it and leave it to our readers to take a closer look. You can run the CSS-styled minimal app[56](32_Notes02.xhtml_Notes02_6) from our server or download its code[57](32_Notes02.xhtml_Notes02_7) as a ZIP archive file.

## 3.10Points of Attention

### 3.10.1Catching invalid data

The app discussed in this chapter is limited to support the minimum functionality of a data management app only. It does not take care of preventing users from entering invalid data into the app’s database. In [Chapter 8](#20_chapter08.xhtml_chapter08_1), we show how to express integrity constraints in a model class, and how to perform data validation both in the model/ storage code of the app and in the HTML5-based user interface.

### 3.10.2Database size and memory management

Notice that in this chapter, we have made the assumption that all application data can be loaded into main memory (like all book data is loaded into the map `Book. instances`). This approach only works in the case of local data storage of smaller databases, say, with not more than 2 MB of data, roughly corresponding to 10 tables with an average population of 1000 rows, each having an average size of 200 Bytes. When larger databases are to be managed, or when data is stored remotely, it’s no longer possible to load the entire population of all tables into main memory, but we have to use a technique where only parts of the table contents are loaded.

### 3.10.3Boilerplate code

Another issue with the do-it-yourself code of this example app is the boilerplate code needed per model class for the data storage management methods `add`, `retrieve`, `update`, and `destroy`. While it is good to write this code a few times for learning app development, you don’t want to write it again and again later when you work on real projects. In Volume 2, we present an approach how to put these methods in a generic form in a meta-class, such that they can be reused in all model classes of an app.

### 3.10.4Serializing and de-serializing attribute values

Serializing an attribute value means to convert it to a suitable string value. For standard datatypes, such as numbers, a standard serialization is provided by the predefined conversion function `String`. When a string value, like “13” or “yes”, represents the value of a non-string-valued attribute, it has to be de-serialized, that is, converted to the range type of the attribute, before it is assigned to the attribute. This is the situation, for instance, when a user has entered a value in a form input field for an integer-valued attribute. The value of the form field is of type string, so it has to be converted (de-serialized) to an integer using the predefined conversion function `parseInt`.

For instance, in our example app, we have the integer-valued attribute `year`. When the user has entered a value for this attribute in a corresponding form field, in the Create or Update user interface, the form field holds a string value, which has to be converted to an integer in an assignment like the following:

![](graphic/14_chapter03_fig_41.png)

One important question is: where should we take care of de-serialization: in the “view” (before the value is passed to the “model” layer), or in the “model”? Since attribute range types are a business concern, and the business logic of an app is supposed to be encapsulated in the “model”, de-serialization should be performed in the “model” layer, and not in the “view”.

### 3.10.5Implicit versus explicit form field labels

The explicit labeling of form fields requires to add an `id` value to the `input` element and a `for`-reference to its `label` element as in the following example:

![](graphic/14_chapter03_fig_42.png)

This technique for associating a label with a form field is getting quite inconvenient when we have many form fields on a page because we have to make up a great many of unique `id` values and have to make sure that they don’t conflict with any of the `id` values of other elements on the same page. It’s therefore preferable to use an approach, called implicit labeling, where these `id` references are not needed. In this approach, the `input` element is a child element of its `label` element, as in

![](graphic/14_chapter03_fig_43.png)

Having `input` elements as child elements of their `label` elements doesn’t seem very logical. Rather, one would expect the `label` to be a child of an `input` element. But that’s the way it is defined in HTML5.

A small disadvantage of using implicit labels may be the lack of support by certain CSS libraries. In the following parts of this tutorial, we will use our own CSS styling for implicitly labeled form fields.

### 3.10.6Synchronizing views with the model

When an app is used by more than one user at the same time, we have to take care of somehow synchronizing the possibly concurrent read/write actions of users such that users always have current data in their “views” and are prevented from interfering with each other. This is a very difficult problem, which is attacked in different ways by different approaches. It has been mainly investigated for multi-user database management systems and large enterprise applications built on top of them.

The original MVC proposal included a data binding mechanism for automated one-way model-to-view synchronization (updating the model’s views whenever a change in the model data occurs). We didn’t take care of this in our minimal app because a front-end app with local storage doesn’t really have multiple concurrent users. However, we can create a (rather artificial) situation that illustrates the issue:

1.  Open the Update UI page of the minimal app twice (for instance, by opening `updateLearningUnit.html` twice), such that you get two browser tabs rendering the same page.
2.  Select the same learning unit on both tabs, such that you see its data in the Update view.
3.  Change one data item of this learning unit on one of the tabs and save your change.
4.  When you now go to the other tab, you still see the old data value, while you may have expected that it would have been automatically updated.

A mechanism for automatically updating all views of a model object whenever a change in its property values occurs is provided by the observer pattern that treats any view as an observer of its model object. Applying the observer pattern requires that (1) model objects can have a multi-valued reference property like observers, which holds a set of references to view objects; (2) a notify method can be invoked on view objects by the model object whenever one of its property values is changed; and (3) the notify method defined for view objects takes care of refreshing the user interface.

Notice, however, that the general model-view synchronization problem is not really solved by automatically updating all (other users’) views of a model object whenever a change in its data occurs. Because this would only help, if the users of these views didn’t make themselves any change of the data item concerned, meanwhile. Otherwise, their changed data value would be overwritten by the automated refresh, and they may not even notice this, which is not acceptable in terms of usability.

### 3.10.7Architectural separation of concerns

From an architectural point of view, it is important to keep the app’s model classes independent of

1.  the user interface (UI) code because it should be possible to re-use the same model classes with different UI technologies;
2.  the storage management code because it should be possible to re-use the same model classes with different storage technologies.

In this chapter, we have kept the model class `Book` independent of the UI code, since it does not contain any references to UI elements, nor does it invoke any view method. However, for simplicity, we didn’t keep it independent of storage management code, since we have included the method definitions for add, update, destroy, etc., which invoke the storage management methods of JavaScrpt’s `localStorage` API. Therefore, the separation of concerns is incomplete in our minimal example app.

We show in Volume 2 how to achieve a more complete separation of concerns by defining abstract storage management methods in a special storage manager class, which is complemented by libraries of concrete storage management methods for specific storage technologies, called storage adapters.

## 3.11Practice Projects

In most parts of the following projects you can follow, or even copy, the code of the book data management app presented in this chapter. Like in the book data management app, you can make the simplifying assumption that all the data can be kept in main memory. So, on application start up, the data is read from the persistent data store. When the user quits the application, the data has to be saved to the persistent data store, which should be implemented with JavaScript’s Local Storage API, as shown in this chapter, or with the more powerful IndexedDB[58](32_Notes02.xhtml_Notes02_8) API.

For developing the apps, simply follow the sequence of seven steps described above:

1.  Step 1 – Set up the Folder Structure
2.  Step 2 – Write the Model Code
3.  Step 3 – Initialize the Application
4.  Step 4 – Implement the Retrieve/List All Objects Use Case
5.  Step 5 – Implement the Create Object Use Case
6.  Step 6 – Implement the Update Object Use Case
7.  Step 7 – Implement the Delete Object Use Case

Also make sure that

1.  your HTML pages comply with the XML syntax of HTML5, preferably by checking with XHTML5 validation[59](32_Notes02.xhtml_Notes02_9)(setting the validator field `Preset` to “HTML5 + SVG 1\. 1 + MathML 3.0”),
2.  international characters are supported by using UTF-8 encoding for all HTML files,
3.  your JavaScript code complies with our Coding Guidelines[60](32_Notes02.xhtml_Notes02_10) and its style is checked with JSHint[61](32_Notes02.xhtml_Notes02_11)(for instance, instead of the unsafe equality test with “==”, always the strict equality test with “===” has to be used).

If you have any questions about how to carry out the following projects, you can ask them on our discussion forum[62](32_Notes02.xhtml_Notes02_12).

### 3.11.1Project 1 – Managing information about movies

The purpose of the app to be developed is managing information about movies. The app deals with just one object type: `Movie`, as depicted in the following class diagram:

![](graphic/14_chapter03_fig_44.png)

Notice that in the `Movie` class there is an attribute with range `Date`, which is a special datatype, discussed in [Chapter 13](#27_chapter13.xhtml_chapter13_1).

You can use the sample data shown in [Table 3.2](#14_chapter03.xhtml_chapter03_45) for testing your app.

Table 3.2 Sample data about movies

| Movie ID | Title | Release date |
| 1 | Pulp Fiction | 1994–05–12 |
| 2 | Star Wars | 1977–05–25 |
| 3 | Casablanca | 1943–01–23 |
| 4 | The Godfather | 1972–03–15 |

More movie data can be found on the IMDb website[63](32_Notes02.xhtml_Notes02_13).

Variation: Improve your app by replacing the use of the `localStorage` API for persistent data storage with using the more powerful IndexedDB[64](32_Notes02.xhtml_Notes02_14) API.

### 3.11.2Project 2 – Managing information about countries

The purpose of the app to be developed is managing information about countries. The app deals with just one object type: `Country`, as depicted in the following class diagram:

![](graphic/14_chapter03_fig_45.png)

You can use the sample data shown below in [Table 3.3](#14_chapter03.xhtml_chapter03_49) for testing your app.

Table 3.3 Sample data about countries

| Name | Population | Life expectancy |
| Germany | 80,854,408 | 80.57 |
| France | 66,553,766 | 81.75 |
| Russia | 142,423,773 | 70.47 |
| Monaco | 30,535 | 89.52 |

More data about countries can be found in the CIA World Factbook[65](32_Notes02.xhtml_Notes02_15).

# 4Building a Minimal Web App with Java EE in Seven Steps

In this chapter, we show how to build a simple Java EE web application using the Java Persistence API (JPA) for object-to-storage mapping and Java Server Faces (JSF) as the user interface (or “view”) technology. Such an application requires a web server that supports the Java EE specifications Java Servlets, Java Expression Language (EL), JPA and JSF, such as the open source web server Tomcat/TomEE[66](32_Notes02.xhtml_Notes02_16)(pronounced “Tommy”). In addition to the Java code executed on the back-end computer that runs the TomEE web server, a Java EE web app also consists of HTML, CSS and possibly some auxiliary JavaScript code that is executed by a web browser running on the user’s front-end computer. Since essentially all data processing is performed on the back-end, and the front-end only renders the user interface, we classify Java EE web applications as back-end web apps.

We show how to develop, deploy and run a simple example app using the TomEE web server, which is Apache Tomcat extended by adding basic Java EE features for providing an execution environment for light-weight Java EE web apps. We assume that you have already installed the TomEE Plume[67](32_Notes02.xhtml_Notes02_17) server and MySQL[68](32_Notes02.xhtml_Notes02_18). Then simply follow our installation and configuration instructions[69](32_Notes02.xhtml_Notes02_19).

The purpose of our minimal example app is to manage information about books. For simplicity, we deal with a single object type `Book`, as depicted in [Figure 4.1](#15_chapter04.xhtml_chapter04_6).

![](graphic/15_chapter04_fig_01.png)

Figure 4.1 The object type `Book`.

The following table shows a sample data population for the model class `Book`.

Table 4.1 Sample data about books

| ISBN | Title | Year |
| 006251587X | Weaving the Web | 2000 |
| 0465026567 | Gödel, Escher, Bach | 1999 |
| 0465030793 | I Am A Strange Loop | 2008 |

What do we need for a data management app? There are four standard us e cases, which have to be supported by the app:

1.  Create a new book record by allowing the user to enter the data of a book that is to be added to the collection of stored book records.
2.  Retrieve (or read) all books from the data store and show them in the form of a list.
3.  Update the data of a book record.
4.  Delete a book record.

These four standard use cases, and the corresponding data management operations, are often summarized with the acronym CRUD.

For entering data with the help of the keyboard and the screen of our computer, we use HTML forms, which provide the user interface technology for web applications.

For any data management app, we need a technology that allows to store data in persistent records on a secondary storage device, such as a hard-disk or a solid state disk. JPA allows using a great number of different data storage technologies, including many SQL database management systems (DBMS) such as Oracle, MySQL and PostgreSQL. We don’t have to change much in the application code for switching from one storage technology to another. Adding the right driver implementation to our Java runtime environment, properly setting up the DBMS and changing the database access configuration is in general all we need to do. In our example application, we explain how to set up the JPA configuration for MySQL.

## 4.1Java Basics

Compared to JavaScript, what is different in Java? We list a few observations:

1.No program withouta class: Any Java program must include at least one class.

2.Java is strongly typed: Properties, parameters and variables must be declared to be of some type.

3.No global variables, no global procedures: In Java, variables, procedures and functions must be defined in the context of a class, which provides their name space.

4.Arrays are static: Arrays have a fixed size, which cannot be changed at runtime.

5.No object without a class: For creating an object, a class has to be used (or defined) for

‒defining the properties of the object’s property slots

‒defining the methods and functions that can be applied to the object (and all other objects instantiating the class)

6.Classes, properties and methods are defined with a visibility level (`public`, `protected` or `private`), which restricts their accessibility.

7.Type parameters: Classes and complex data structures (such as lists) can be defined with the help of type parameters. See, for instance, the generics tutorial[70](32_Notes02.xhtml_Notes02_20) by Oracle.

8.Java programs must be compiled before they can be executed.

9.Speed: Java is about twice as fast as optimized JavaScript.

In Java, visibility levels are used to define the possible levels of access:

Table 4.2 Java Visibility Level

![](graphic/15_chapter04_fig_02.png)

Normally, properties are defined as private, such that they can only be assigned with a public setter, which allows to control, and possibly log, any change of the property value. Unfortunately, Java does not allow to protect only write, but not read access. Therefore, we always have to define getters along with setters, even if they are not needed.

A Java bean class (or, simply, bean class) is a Java class with a parameter-free constructor where all properties are serializable and have a `get` and `set` method (also called “getter” and “setter”). A Java bean is an object created with the help of a bean class.

A JPA entity class (or, simply, entity class) is a Java bean class with an `@Entity` annotation, implying that a Java EE runtime environment (such as provided by the TomEE PLUS[71](32_Notes02.xhtml_Notes02_21) web server) will take care of the persistent storage of its instances.

JPA is a Java API for the management of persistent data in Java applications. It uses the Java Persistence Query Language (JPQL), a platform-independent object-oriented query language based on SQL. JPQL query expressions look very similar to SQL query expressions, but they are executed in the context of JPA entity objects.

JSF is a Java specification for building component-based user interfaces for web applications. Its current version, JSF 2, by default, uses Facelets as its view technology. By contrast, JSF 1 has used JavaServer Pages (JSP) as its default view technology.

A JSF facelet is an XML-based template that combines static UI content items with data variables for generating an XHTML user interface page.

## 4.2Step 1 – Set up the Folder Structure

In the first step, we set up our folder structure for the application program code. The application name is “Public Library”, so it would be natural to use a corresponding name for the application folder, like “PublicLibrary”, but we prefer using `MinimalApp`. Then we create the application structure. There are many ways to do this, like for example to use the Eclipse[72](32_Notes02.xhtml_Notes02_22) development environment (and create and configure a Dynamic Web Project). In this chapter we show how to do it manually, so there is no need to use special tools. For your convenience, we also provide an ANT script (see our guide[73](32_Notes02.xhtml_Notes02_23) for a download link), allowing to automatically create the folder structure of the web application, compile it to a Web application Archive (WAR) file and then deploy it to a TomEE server for execution. The application structure (which is compatible with the Dynamic Web Project structure of Eclipse, so it can be imported in Eclipse) is the following:

![](graphic/15_chapter04_fig_03.png)

This folder structure has the following parts:

1.The `src` folder contains the app code folder `pl`, defining the Java package name for the app (as a shortcut of ’public library’), and the folder `META-INF` with configuration files:

a.the app code folder `pl` contains the model and controller code in its subfolders `m` and `c`, while the view/UI related code is contained in the `WebContent` folder;

b.the most important configuration file is the `persistence.xml` file. It contains the configuration for the database connection. The content of this file is discussed in [Section 4.2](#15_chapter04.xhtml_chapter04_13).

2\. The `WebContent` folder contains various web resources, including template files and custom view files:

a.the `resources` folder is used for storing resources, such as downloadable documents, images or videos.

b.the `views` folder stores our custom view files for the application, so it represents the View part of the MVC paradigm. Please note that it is not strictly required to name it “views”, but it makes a lot of sense to do it so, since this is what this folder represents.

c.the `WEB-INF` folder contains project libraries (in the form of `jar` files in the `lib` subfolder (in our case we don’t need such libraries), the facelet files for the UI pages (as part of the `templates` subfolder), the `faces-config. xml` file, which stores the facelet configuration and the `web.xml` configuration file, specific to the TomEE server used to run our application.

We create a “Main Menu” page for our application, thus we add an `index.xhtml` file to our `views` folder with the following content:

![](graphic/15_chapter04_fig_04.png)![](graphic/15_chapter04_fig_05.png)

The code consists of HTML elements and JSF elements, which are discussed below.

## 4.3Step 2 – Write the Model Code

In the second step, we create the model classes for our app, using a separate Java source code file (with extension `. java`) for each model class. In the information design model shown in [Figure 4.1](#15_chapter04.xhtml_chapter04_6) above, there is only one class, representing the object type `Book`. So, we create a file `Book. java` in the folder `src/pl/m` with the following code:

![](graphic/15_chapter04_fig_06.png)

Notice that the model class `Book` is coded as a JPA entity class, which is a JavaBean class enriched with the following JPA annotations:

1.  The annotation `@Entity` designates a class as an entity class implying that the instances of this class will be stored persistently.
2.  The annotation `@Table( name="books")` specifies the name of the database table to be used for storing the `Book` entities. This annotation is optional and defaults to a table name being the same as the class name but in lower case (that is, it would be `book` in our case).
3.  The `@Id` annotation marks the standard identifier attribute, implying that the corresponding column of the underlying SQL database table is designated as the PRIMARY KEY. In our example, `isbn` is used as the standard identifier attribute, and the corresponding `isbn` column of the `books` table stores the primary key values.

In the entity class `Book`, we also define the following static (class-level) methods:

1.  `Book. create` for creating a new `Book` instance.
2.  `Book. retrieveAll` for retrieving all `Book` instances from the persistent data store.
3.  `Book.retrieve` for retrieving a specific `Book` instance from the persistent data store by means of its standard identifier.
4.  `Book. update` for updating an existing `Book` instance.
5.  `Book. delete` for deleting a `Book` instance.
6.  `Book. generateTestData` for creating a few example book records to be used as test data.
7.  `Book.clearData` for clearing the book database table.

The signatures of these methods, which are discussed in more detail in the following subsections, are shown in the following program listing:.

![](graphic/15_chapter04_fig_07.png)

The JPA architecture for data management and object-to-storage mapping is based on the concept of an entity manager, which provides the data management methods `persist` for saving a newly created or updated entity, `find` for retrieving an entity, and `remove` for deleting an entity.

Since the database access operations of an entity manager are executed in the context of a transaction, our data management methods have a parameter `ut` of type `UserTransaction`. Before the entity manager can invoke the database write method `persist`, a transaction needs to be started with `ut.begin()`. After all write (and state change) operations have been performed, the transaction is completed (and all changes are committed) with `ut.commit()`.

### 4.3.1Storing Book objects in a database table books

The instances of our entity class `Book` are Java objects representing “entities” (or business objects), which can be serialized, or, in other words, converted to records (or rows) of a database table, as shown in [Table 4.1](#15_chapter04.xhtml_chapter04_7).

SQL

The Structured Query Language (SQL), created in the early 1970s by Donald D. Chamberlin and Raymond F. Boyce, is an ISO standard that is based on the Relational Database model of Edgar F. Codd and defines

1.  a Data Definition Language (based on CREATE TABLE statements) for creating databases consisting of tables containing primitive data;
2.  a Data Manipulation Language (based on INSERT, UPDATE and DELETE statements) for creating, updating and deleting the contents of database tables;
3.  a Query Language (based on SELECT statements) for retrieving the information stored in database tables.

SQL is widely used in Database Management Systems (DBMSs) and in programming languages for persistent data storage. Despite the existence of the SQL standard, each SQL DBMS has its own dialect of SQL. Consequently, SQL code is in practice not completely portable among different DBMSs without adjustments.

The data storage technology used in our example app is MySQL[74](32_Notes02.xhtml_Notes02_24), and the SQL code used to create the schema for the database table `books` is the following:

![](graphic/15_chapter04_fig_08.png)

While it is also possible to create the database schema manually (with the help of CREATE TABLE statements such as the one above), we show below how the database schema can be automatically generated by JPA. In both cases, the database setup, including a user account and the associated rights (create, update, etc), must be done manually before the JPA application can connect to it.

### 4.3.2Creating a new Book instance and storing it

The `Book. create` method takes care of creating a new `Book` instance and saving it to a database with the help of an ’entity manager’:

![](graphic/15_chapter04_fig_09.png)

To store the new object, the `persist` method of the given ’entity manager’ is invoked. It is responsible for creating the corresponding SQL `INSERT` statement and executing it.

### 4.3.3Retrieving all Book instances

The instances of an entity class, such as `Book`, are retrieved from the database with the help of a corresponding query expressed in the Java Persistence Query Language (JPQL[75](32_Notes02.xhtml_Notes02_25)). These queries are similar to SQL queries. They use class names Instead of table names, property names instead of column names, and object variables instead of row variables.

In the `Book. retrieveAll` method, first a `query` asking for all `Book` instances is created, and then this query is executed with `query. getResultList()` assigning its answer set to the list variable `books`:

![](graphic/15_chapter04_fig_10.png)

### 4.3.4Updating a Book instance

To update an existing `Book` instance, first we need to retrieve it from the database, by using `em. find`, and then set those attributes the value of which has changed:

![](graphic/15_chapter04_fig_11.png)![](graphic/15_chapter04_fig_12.png)

Notice that, when invoking the `find` method for retrieving an entity, the first argument must be a reference to the entity class concerned (here: `Book. class`), so the JPA runtime environment can identify the database table from which to retrieve the entity’s data. The second argument must be the value of the entity’s primary key.

Notice that in the update case, we do not have to use `persist` for saving the changes. Saving is automatically managed by the JPA runtime environment when we complete the transaction with `ut.commit()`.

### 4.3.5Deleting a Book instance

A book entity can be deleted from the database as shown in the following example code:

![](graphic/15_chapter04_fig_13.png)

To delete an entity from the database, we first need to retrieve it with the help of the `find` method as in the update case. Then, the `remove` method has to be invoked by the ’entity manager’, and finally the transaction is completed with `ut.commit()`.

### 4.3.6Creating test data

For being able to test our code, we may create some test data and save it in our database. We can use the following procedure for this:

![](graphic/15_chapter04_fig_14.png)![](graphic/15_chapter04_fig_15.png)

After clearing the database, we successively create 3 instances of the `Book` entity class and save them with the help of `persist`.

### 4.3.7Clearing all data

The following procedure clears our database by deleting all rows:

![](graphic/15_chapter04_fig_16.png)

JPA does not provide a direct method to drop the entire population of a specific class from the database. However, this can be easily obtained by using a JPQL statement as shown in the above code. The JPQL code can be read as: delete all rows from the database table associated with the entity class `Book`.

## 4.4Step 3 – Configure the App

In this section we show how to

1.  configure an app to connect with a database in a controller class,
2.  obtain the `EntityManager` and `UserTransaction` instances required for performing database operations,
3.  wrap an app in a WAR file and deploy it to a web server for execution.

### 4.4.1Create the EntityManager and UserTransaction objects

A controller class contains the code that glues the views to the model, as well as all methods that do neither belong to the model nor to the view, like getting a connection with the database server. In our example app, this class is `pl.c.BookController` in the `src/pl/c` folder.

JPA requires an `EntityManager` object for executing JPQL queries (with `SELECT`) and data manipulation statements (with `INSERT`, `UPDATE` and `DELETE`). Also, in order to perform database write operations, a `UserTransaction` object is required for starting and completing transactions. In a standalone application, the programmer has to create an entity manager and a transaction manually, using a factory pattern as shown in the following code fragment:

![](graphic/15_chapter04_fig_17.png)

A JPA-enabled Java web application normally runs in an environment called “container” (in our case this is TomEE), which takes care of creating an `EntityManager` and a `UserTransaction` object if the right annotations are used. The code responsible for this is part of the controller class ( e. g., `pl.c.BookController`) since the controller is responsible for managing the database connections.

![](graphic/15_chapter04_fig_18.png)

A closer look at this code shows that it is sufficient to use the `@PersistenceContext` annotation and provide a `unitName` (see the next section) for obtaining an `EntityManager` instance at runtime. Also, obtaining a `UserTransaction` instance at runtime is as simple as using the `@Resource` annotation for the user transaction reference property `ut`. Not only that the required code is short and simple, but if the database type is changed (e. g. when we switch from MySQL to an Oracle database), this code remains the same.

### 4.4.2Configure the JPA database connection

In the previous section, discussing the `BookController` class, we have shown how to obtain the `EntityManager` and `UserTransaction` objects required for performing database operations. The `@PersistenceContext` annotation of the `EntityManager` reference property requires a `unitName`, which is just a name used for identifying the storage management configuration defined in the `src/ META-INF/persistence.xml` file. In our example app this file has the following content:

![](graphic/15_chapter04_fig_19.png)

The configuration name (“MinimalApp”) is defined by the `name` attribute of the `persistence-unit` element. This is the value we have to use for the `unitName` property of the `@PersistenceContext` annotation.

The `persistence-unit` element has three content parts:

1.  One or more `class` elements, each one containing the fully qualified name of an entity class of the app (like `pl.m.Book` in our example app).
2.  A set of configuration `property` elements used for providing further configuration settings.
3.  A `jta-data-source` element for specifying the configuration block in the `config/TomEE.xml` web server configuration file in the web server installation folder.

In our `persistence.xml` file, two configuration properties have been set:

–`javax.persistence.schema-generation.database.action`, with the possible values: `none` (default), `create`, `drop-and-create` and `drop`. It specifies if the database schema is to be automatically created and additionally allows to drop the existing tables before creating the new ones (with `drop` or `drop-and-create`)..

–`javax.persistence.schema-generation.create-source`, with the possible values `metadata` (default), `script`, `metadata-then-script` and `script-then-metadata`. It specifies the source of information used to create the database schema. The value `metadata` enforces using the JPA annotations while the value `script` allows using an external script for defining the schema.

The `jta-data-source` element of our `persistence.xml` file refers to the `Resource` element with `id` value “MinimalApp” in the `config/TomEE.xml` file, which has the following content:

![](graphic/15_chapter04_fig_20.png)

The `Resource` element contains the information required to connect with the database (user name, password, access URL and the Java class name of the connection driver). Notice that in order to use a connection driver, one needs to download the jar file for that specific technology and copy it into the `lib` subfolder of the TomEE installation folder. Finally, TomEE needs to be restarted in order to load the new driver. See also our instructions page[76](32_Notes02.xhtml_Notes02_26), for additional details related to JDBC drivers, and in particular how to use the official MySQL JDBC driver “Connector/J”.

### 4.4.3Create the main template

The main template, called `page.xhtml`, is shown below. It has two sub-templates:

1.  `header.xhtml` defines the general header information items (such as the application name)
2.  `footer.xhtml` defines the general footer information items (such as a copyrights notice)

Both sub-templates are included in the main template with the help of a `ui:include` element. We add all three template files to the `WebContent/WEB-INF/ templates` folder.

The content of our HTML5-compliant main template `page.xhtml` is the following:

![](graphic/15_chapter04_fig_21.png)![](graphic/15_chapter04_fig_22.png)

In the code, one can see that some HTML elements are used (e. g., `title`, `header`, `main` and `footer`) while others like `h:head` and `ui:insert` are not HTML elements, but have been defined by JSF. For instance, JSF defines its own head element `h:head` for injecting special HTML code such as `script` elements that load JavaScript code for HTTP messaging between the web browser and the back-end Java program by invoking methods of the JavaScript API XML HTTP Request (XHR).

Our main template defines three content regions: header, main and footer. The header and footer regions are defined by sub-templates included with the help of the `ui:include` element.

The `header.xhtml` sub-template contains the application menu, corresponding to the CRUD operations:

![](graphic/15_chapter04_fig_23.png)

The `footer.xhtml` sub-template contains the “Back to main menu” link, which we like to show on each application page, except the index page:

![](graphic/15_chapter04_fig_24.png)

Notice that the `h` namespace must be defined once again in `footer.xhtml` even if it has already been defined in `page.xhtml`. In the footer template component, we define the “Back to main menu” operation, which is going to be injected into each page that uses this template. The main region is dynamic, and will be replaced with the content generated by a facelet template.

JSF is using the following namespaces:

–`xmlns:ui="` [`http://java.sun.com/jsf/facelets"`](http://java.sun.com/jsf/facelets) for the JSF Facelets Tag Library providing templating elements (like `ui:insert` for specifying the region of a template where to inject the facelet content).

–`xmlns:h="` [`http://java.sun.com/jsf/html"`](http://java.sun.com/jsf/html) for the JSF HTML Tag Library providing JSF versions of HTML elements, which are then mapped to HTML elements. For example `h: inputText`, which is mapped to an HTML `input` element.

–`xmlns:f="` [`http://java.sun.com/jsf/core"`](http://java.sun.com/jsf/core) for the JSF Core Tag Library providing custom actions or elements that are independent of any particular render kit. For example, `f:actionListener` can be used to define a Java method which is executed when the user clicks a button.

–`xmlns:p="` [`http://xmlns.jcp.org/jsf/passthrough"`](http://xmlns.jcp.org/jsf/passthrough) for using HTML attributes in JSF HTML elements and passing them through to the generated HTML. For example, with `p:type` in, `<h:inputText p:type="number">` an HTML5 `input` type attribute can be created in the generated HTML: `<input type="number">`.

–`xmlns:c="` [`http://java.sun.com/jsp/jstl/core"`](http://java.sun.com/jsp/jstl/core) for the JSTL Core Tag Library providing all kinds of features, like dealing with loops and defining variables. For example, we can use `<c:set var="isbn" value="#{book. isbn}"/>` to create a variable named `isbn` which can then be used in the view code for conditional expressions.

–`xmlns:fn="` [`http://java.sun.com/jsp/jstl/functions"`](http://java.sun.com/jsp/jstl/functions) for the JSTL Functions Tag Library providing various utility functions, such as string converters. For example, we can use `fn:toUpperCase` to convert a string to its uppercase representation.

### 4.4.4Define the managed beans needed in facelets

JavaBean classes, including entity classes, can be used for creating ’managed beans’ with the help of the `@ManagedBean` annotation, which allows defining the name of a variable for accessing the created bean in the view code, typically in an EL expression. In our example app, we want to access a `Book` bean as well as a `BookController` bean, therefore both classes have to be annotated as follows:

![](graphic/15_chapter04_fig_25.png)

Notice how a lifetime scope can be specified for a managed bean with a scope annotation. In our example the `book` bean is `@RequestScoped`, this means the instance exists as long as the HTTP request and the associated response are being processed. The `bookCtrl` bean is `@ SessionScoped`, which means it is created when the session starts, and destroyed when the session is closed. Other scopes are available, but in our example we only need these two.

### 4.4.5Build the WAR file and deploy it to TomEE

There are multiple ways in which we could compile the source code, create the war file and deploy it to a TomEE server. For example one can use Eclipse IDE[77](32_Notes02.xhtml_Notes02_27) or Netbeans[78](32_Notes02.xhtml_Notes02_28), or one can use ANT and create a script that takes care of all these tasks.

We provide an ANT[79](32_Notes02.xhtml_Notes02_29) script that allows to automatically create the structure of a Java web application, compile the Java source code, build the WAR file and deploy it to a TomEE web server. Our ANT script generates an `Eclipse IDE` compatible folder structure, so in case you want to use Eclipse, simply create a project from the existing application code. The ANT installation instructions, detailed description of the available tasks as well as download links are available on our instructions page[80](32_Notes02.xhtml_Notes02_30).

For our “PublicLibrary” example application, we have used the ANT script and the following steps were needed:

–create the application folder structure: `ant create app -Dappname=publicLibrary -Dpkgname=pl.`

–compile the Java code and build the war file: `ant war -Dappname=publicLibrary.`

–deploy the application to TomEE server: `ant deploy -Dappname=publicLibrary.` This operation also builds the war file, if it was not already created using the war task, as shown before.

Hint: we do not recommend using spaces in folder names, but if for any reason, the application name needs to contain spaces, then it has to be enclosed in double quotes, e.g. `create app -Dpgkname=hw -Dappname="Hellow World"`. In this case it was required to provide the `pkgname` parameter, while “Hello World” is not a valid Java identifier, since it contains a white space.

## 4.5Step 4 – Implement the Create Use Case

The CRUD use case Create involves creating a new object in main memory and then saving it to persistent storage with the help of the `create` method.

The corresponding `create` action method code from the `src/pl/c/BookController.java` is shown below:

![](graphic/15_chapter04_fig_26.png)

The `BookController::create` action method invokes the `Book.create` model class method for creating and saving a `Book` instance. It returns the name of the view file found in the same folder as the view that triggered the action. This file (`create. xhtml` in our case) will be displayed after executing the action. Using the `FacesContext` object, the form is cleared after creating a `Book` instance. The code of the `create` method in `src/pl/m/Book.java` is the following:

![](graphic/15_chapter04_fig_27.png)

Now we need to create the facelet template for the view of the Create use case, `WebContent/views/books/create.xhtml`. Such a facelet template essentially defines an HTML form with data binding and action binding.

Data binding refers to the binding of model class properties to form (input or output) fields. For instance, in the following facelet code fragment, the entity property `book. isbn` is bound to the form input field “isbn”:

![](graphic/15_chapter04_fig_28.png)

In JSF, for the `inputText` elements of a form, the `id` attribute is used with a given value, e. g., `id="isbn"`. The rendered HTML5 `input` elements have both, the `id` and the `name` attributes, and their values are obtained by using the form id and element id values separated by a colon, i. e., `id="createBookForm:isbn"` and `name="createBookForm:isbn"`.

We can also see a first example of an expression in the Java EE Expression Language (EL), where an expression starts with `#` and is enclosed in curly brackets, like `# {expression}`. Such an expression allows reading the value of a property of, or invoking a method on, a Java bean or a context object. The value of the expression is assigned to the `value` attribute of the generated HTML `input` element. The example in our JSF code above is the expression `#{book.isbn}`, which retrieves the value of the `isbn` property of the `book` bean.

Action binding refers to the binding of method invocation expressions to actionable UI elements, where the invoked methods typically are controller action methods, and the actionable UI elements typically are form buttons. For instance, in the following facelet code fragment, the method invocation expression `bookCtrl. create(`…`)` is bound to the form’s submit button:

![](graphic/15_chapter04_fig_29.png)

After discussing data binding and action binding, it’s time to look at the complete code of the facelet:

![](graphic/15_chapter04_fig_30.png)![](graphic/15_chapter04_fig_31.png)

This facelet replaces the `main` region of the template defined in `page.xhtml`, because the `name` attribute of the `ui:define` element has been set to “main”, but it also replaces the `headerTitle` region of the template, which is part of the `header` and displays the current operations allowed by the page.

`h:outputLabel` elements can be used for creating form field labels, while `h: inputText` elements are used for creating HTML input elements. It is possible to specify an HTML5 type of an `input` element by using a special namespace prefix (`xmlns:p =` [`"http://xmlns.jcp.org/jsf/passthrough"`](http://xmlns.jcp.org/jsf/passthrough)[)](http://xmlns.jcp.org/jsf/passthrough) for the `type` attribute, enforcing it to be ’passed through’. In this way the `year` input field can be defined with type `number`, so it’s rendered by the corresponding number widget in the browser.

The `h:commandButton` element allows creating submit buttons rendered as a `input` elements with `type="submit"`, and binding them to an action to be performed when the button is clicked. The value of the `action` attribute is a method invocation expression. In our Create use case we want that, when the button is clicked, a `Book` instance with the property values provided by corresponding form fields is created and saved.

## 4.6Step 5 – Implement the Retrieve/List All Use Case

For the Retrieve use case we have to add a method in the controller class (`src/pl/ c/BookController.java` file), which reads all `Book` records from the `books` database table and then delivers this information to the view. The controller action method code is shown below:

![](graphic/15_chapter04_fig_32.png)![](graphic/15_chapter04_fig_33.png)

The `getBooks` method returns a list of `Book` instances which are obtained by calling the static `retrieveAll` method of the `Book` model class. The code of the `Book.retrieveAll` method is:

![](graphic/15_chapter04_fig_34.png)

The code is simple, and as already discussed in [Section 3.3](#14_chapter03.xhtml_chapter03_14), it uses a JPQL statement to retrieve the `Book` records from the `books` table and create the corresponding `Book` instances. The `EntityManager` object required for being able to perform the JPQL query is passed to `Book.retrieveAll` from the `BookController` object as discussed in [Section 4.1](#15_chapter04.xhtml_chapter04_9) section.

Now it is the time to define the facelet template for displaying a table with all book records found in the database. The view template files corresponding to the model classes of our app are located in model class subfolders of the `WebContent/views/` folder. For the Retrieve/list all books use case, we create a file named `retrieveAndListAll.xhtml` in `WebContent/views/books/` with the following content:

![](graphic/15_chapter04_fig_35.png)![](graphic/15_chapter04_fig_36.png)

The `ui:composition` element specifies which template is applied (i. e. `template="/WEB-INF/templates/page.xhtml"`) and which view block (`<ui: define name="main">`) is replaced by this facelet at render time.

The `h:dataTable` element defines a table view for a set of records, which is then rendered as an HTML table. Its `value` attribute defines a data binding to a record collection, while the `var` attribute defines a variable name for iteratively accessing records from this collection. The expression provided in the `value` attribute normally specifies a collection-valued property (here: `books`) which is accessed via a corresponding getter (here: `getBooks`) as defined in the controller class `BookController`. In this particular case it is just sufficient to define the `getBooks` method since there is no need of a `books` property in the controller class. In any case, `value` does not allow to invoke a method, so we cannot call `getBooks` directly. Instead we have to use the (possibly virtual) property `books`,which internally evaluates to a call of `getBooks` without checking if a `books` property really exists.

The `h:button` element allows to create redirect buttons. The value of the `outcome` attribute specifies a name of a facelet file (omitting the `.xhtml` extension, such that, in the example, the file name is `index.xhtml`).

## 4.7Step 6 – Implement the Update Use Case

Like for Create, for the Update use case also a controller action method is defined in the `BookController` class:

![](graphic/15_chapter04_fig_37.png)

The `Book. update` takes care of saving property value changes for a book object identified by its `isbn` value as shown below:

![](graphic/15_chapter04_fig_38.png)

Now, we create the view where a `Book` can be selected so the user can edit the `title` and `year` properties, and then save the changes. The code for this view is stored in the `WebContent/views/books/update.xhtml` file which has the following content:

![](graphic/15_chapter04_fig_39.png)![](graphic/15_chapter04_fig_40.png)

In this facelet template, a single selection list (that is, a single-`select` HTML element) is created with the help of the JSF element `h: selectOneMenu`, where the selection list items (the HTML `option` elements) are defined by the JSF elements `f: selectItem` or `f:selectItems`. The `value` attribute of `h:selectOneMenu` binds `book. isbn` to the value of the selected item (or `option` element). The selection list is populated with book records with the help of a `f:selectItems` element bound to `bookCtrl.books`. The attributes `itemLabel` and `itemValue` define the `option` elements’ text and value.

In the update view, when the user selects a book from the selection list, the form fields are filled with the (ISBN, title and year) property values of the selected book. While the ISBN is immediately available in the view (on the front-end) as the value of the selected `option` element, the values of the `title` and `year` properties have to be fetched from the back-end database. This can be done with the help of the JSF element `f:ajax`,which sends an HTTP request message for invoking a remote method, `bookCtrl.refreshObject`, on the back-end using XHR. This method takes the managed `book` bean, and updates its `title` and `year` properties with the current values retrieved from the database. Its code is the following:

![](graphic/15_chapter04_fig_41.png)

To enforce a refresh of the HTML form after the user’s selection, such that it displays the values of `isbn`, `title` and `year`, the `f:ajax` element allows specifying form fields to be updated with the `render` attribute like, in our case, `render="isbn title year"`.

Finally, the `h:commandButton` element is used for invoking the `update` action method of the `BookController` with the parameters `isbn`, `title` and `year`, for making the changes persistent.

## 4.8Step 7 – Implement the Delete Use Case

For the Delete use case, the `delete` action method of the `BookController` invokes the `Book. delete` method by providing the ISBN of the `Book` object to be deleted:

![](graphic/15_chapter04_fig_42.png)

The `Book. delete` method first retrieves the `Book` object to be deleted, and then invokes the entity manager’s `remove` method on it:

![](graphic/15_chapter04_fig_43.png)

The view for the Delete action provides a selection list for selecting the book to be deleted. A “Delete” button allows performing the deletion of the selected book. The code of the view in `WebContent/views/books/delete.xhtml` is as follows:

![](graphic/15_chapter04_fig_44.png)![](graphic/15_chapter04_fig_45.png)

As in the Update use case, a `h:selectOneMenu` element is used to create and populate a selection list containing all the books to choose from. Clicking on the “Delete” command button results in invoking the `delete` action method of the controller with the `isbn` value of the selected book, thus resulting in the deletion of the `Book` object from the database.

## 4.9Style the User Interface with CSS

We style the UI with the help of the HTML5 Boilerplate[81](32_Notes02.xhtml_Notes02_31) CSS and the browser style normalization file normalize.css[82](32_Notes02.xhtml_Notes02_32). The two CSS files `main.css` and `normalize. min.css` are located in the `WebContent/resources/css` folder.

Adding the CSS to the HTML pages requires to edit the `WebContent/WEB-INF/ templates/ page.xhtml` file and add the `style` elements referencing the CSS files:

![](graphic/15_chapter04_fig_46.png)

Notice that we also need to add the CSS to the `WebContent/views/books/ index.xhtml` file, which is not generated with the `page.xhtml` template. The `facesContext.externalContext.requestContextPath` expression allows to get the path to `WebContent` folder. We then need to append the rest of the path, including the CSS file name, for each of the CSS files.

With JSF, there are two main ways to apply CSS styles to specific elements. For the elements created with JSF, we need to use the `@styleClass` attribute, e. g.:

![](graphic/15_chapter04_fig_47.png)

For the HTML elements, we simply use the CSS classes, as in any normal HTML document, e.g.:

![](graphic/15_chapter04_fig_48.png)

For creating advanced user interfaces, additional block elements that act as containers are used for defining paddings, margins, various background colors and other styles. Thus, in various HTML pages you may find DOM structures as shown below, where the `div` element containing the `@class` attribute is used as container for styling purposes:

![](graphic/15_chapter04_fig_49.png)

## 4.10Run the App and Get the Code

You can run the minimal app[83](32_Notes02.xhtml_Notes02_33)(or run the minimal app with CSS[84](32_Notes02.xhtml_Notes02_34)) on our server or download the code[85](32_Notes02.xhtml_Notes02_35) as a ZIP archive file.

Follow our instructions[86](32_Notes02.xhtml_Notes02_36) to get your environment prepared for running back-end Java EE web apps with JPA and JSF.

## 4.11Possible Variations and Extensions

### 4.11.1Using resource URLs

Whenever an app provides public information about entities, such as the books available in a public library, it is desirable to publish this information with the help of self-descriptive resource URLs, such as `http://publiclibrary.norfolk.city/books/006251587X`[](http://publiclibrary.norfolk.city/books/006251587X), which would be the resource URL for retrieving information about the book “Weaving the Web” available in the public library of Norfolk. However, resource URLs are not supported by JSF. In the Java world, we would have to use JAX-RS, instead of JSF, for programming a web API with resource URLs. But this would imply that we need to take care of the front-end UI in a different way, since JAX-RS is a pure back-end API, not providing any support for building user interfaces. A natural option would be to use a JavaScript front-end framework, such as BackboneJS or ReactJS, for rendering the UI.

### 4.11.2Using an alternative DBMS

Instead of MySQL, one can use various other database management systems for persistent storage. The following four steps are required to specify the used DBMS (only one DBMS at a time is possible):

–Configure TomEE so it uses the corresponding resource for your application. For a list of resource configuration examples used for common DBMS’s, check Common DataSource Configurations[87](32_Notes02.xhtml_Notes02_37). For example, if PostgreSQL was chosen as DBMS, then edit the `conf/ tomee.xml` file and add the following code:

![](graphic/15_chapter04_fig_50.png)

–Copy the jar file corresponding to the DBMS driver implementation to the `lib` folder. After this, the TomEE server needs to be restarted.

–Install the DBMS, if not already installed. Installation instructions are usually available on the corresponding DBMS web page.

–Create the corresponding DBMS user and database to be used for your application.

## 4.12Points of Attention

The code of this app should be extended by adding constraint validation. We show how to do this in [Chapter 9](#21_chapter09.xhtml_chapter09_1).

We briefly discuss three further issues.

### 4.12.1Boilerplate code

Another issue with the code of this Java example app is the repetitious boilerplate code needed per entity class for the storage management methods `create`, `retrieve`, `update` and `delete`, and their wrappers in the corresponding controller classes. While it may be instructive to write this code a few times for learning app development, you don’t want to write it again and again later when you work on real projects.

### 4.12.2Offline availability

It is desirable that a web app can still be used when the user is offline. However, this is not possible with a back-end web application architecture as implied by Java EE. Offline availability can only be obtained with a truly distributed architecture where essential application components can be executed both on the back-end and on the front-end.

### 4.12.3Architectural separation of concerns

From an architectural point of view, it is important to keep the app’s model classes independent of

1.  the user interface (UI) code because it should be possible to re-use the same model classes with different UI technologies;
2.  the storage management code because it should be possible to re-use the same model classes with different storage technologies.

We have kept the model class `Book` independent of the UI code, since it does not contain any references to UI elements, nor does it invoke any view method. However, for simplicity, we didn’t keep it independent of storage management code. First, due to using JPA annotations, the model class is bound to the JPA object-to-storage mapping technology. Second, we have included the method definitions for `create`, `update`, `delete`, etc., which invoke the storage management methods of a JPA environment’s entity manager, in the model class. Therefore, the separation of concerns is incomplete in our minimal app.

## 4.13Practice Projects

In most parts of the following projects you can follow, or even copy, the code of the book data management app discussed above.

For developing the apps, simply follow the sequence of seven steps described above:

1.  Step 1 – Set up the Folder Structure
2.  Step 2 – Write the Model Code
3.  Step 3 – Configure and Initialize the Application
4.  Step 4 – Implement the Retrieve/List All Use Case
5.  Step 5 – Implement the Create Use Case
6.  Step 6 – Implement the Update Use Case
7.  Step 7 – Implement the Delete Use Case

Make sure that international characters are supported by using UTF-8 encoding for all HTML files.

### 4.13.1Project 1 – Managing information about movies

The purpose of the app is managing information about movies. The app deals with just one object type: `Movie`, as depicted in the following class diagram:

![](graphic/15_chapter04_fig_51.png)

Notice that in most parts of this project you can follow, or even copy, the code of the book data management app, except that in the `Movie` class there is an attribute with range `Date`, so you have to find out how to handle such an attribute.

You can use the sample data shown in [Table 3.2](#14_chapter03.xhtml_chapter03_45) for testing your app.

### 4.13.2Project 2 – Managing information about countries

The purpose of the app to be developed is managing information about countries. The app deals with just one object type: `Country`, as depicted in the following class diagram:

![](graphic/15_chapter04_fig_52.png)

You can use the sample data shown in [Table 3.3](#14_chapter03.xhtml_chapter03_49) for testing your app.

## 4.14Quiz Questions

If you would like to look up the answers for the following quiz questions, you can check our discussion forum[88](32_Notes02.xhtml_Notes02_38). If you don’t find an answer in the forum, you may create a post asking for an answer to a particular question.

### 4.14.1Question 1: Casting types in Java

Which of the following are valid type casts in Java?

![](graphic/15_chapter04_fig_53.png)

### 4.14.2Question 2: JPA standard identifier property

Complete the following code, so that the `Book` JPA entity class contains a property named `isbn`, with `String` type and playing the role of the standard identifier:

![](graphic/15_chapter04_fig_54.png)

### 4.14.3Question 3: Valid Java Bean classes

Which of the following classes are valid JavaBean classes:

![](graphic/15_chapter04_fig_55.png)

### 4.14.4Question 4: HTML5 attributes with JSF forms

Complete the following code with the JSF construct which results in using `date` as value of the `@type` attribute of the rendered `input` HTML5 element.:

![](graphic/15_chapter04_fig_56.png)

### 4.14.5Question 5: JPQL query

Consider a JPA entity class named `Customer`.Write down the JPQL query to extract all its instances managed by the `EntityManager` (e. g., stored in DB or memory storage):

![](graphic/15_chapter04_fig_57.png)

# 5Information Modeling

UML

The Unified Modeling Language (UML[89](32_Notes02.xhtml_Notes02_39)), created in the mid-1990s, is an industry standard that defines a set of modeling languages for making various kinds of models and diagrams in support of object-oriented problem analysis and software design. Its core languages are Class Diagrams for information/data modeling, and Sequence Diagrams, Activity Diagrams and State Diagrams (or State Charts) for process/behavior modeling.

UML class diagrams provide a visual syntax for expressing UML class models, which allow defining information and data models. They can be used both at the more abstract level of conceptual modeling for requirements engineering and at the more detailed level of design modeling for designing the model classes of an app. Their main building blocks are class rectangles and association lines.

A class rectangle has one, two or three compartments, containing the name of the class, its properties, and its methods. The purpose of a class is to classify objects and to define their properties and the methods that can be invoked on them.

RDF and OWL

The Resource Description Framework (RDF[90](32_Notes02.xhtml_Notes02_40)) has been defined by the W3C in 2004 as a logical formalism that allows (1) formalizing information models in the form of RDF vocabularies, and (2) representing propositional information (e. g., meta-data) on the Web. The core of a UML class model can be expressed as an RDF vocabulary. However, many types of integrity constraints cannot be expressed in RDF. The W3C has therefore defined an extension of RDF, called the Web Ontology Language (OWL[91](32_Notes02.xhtml_Notes02_41)), which allows to formalize the core logic (classes, properties and integrity constraints) of a UML class model in the form of an OWL ontology.

An association line connects two class rectangles. The purpose of an association is to classify relationships (links) between objects. While UML classes have a direct counterpart in the class concepts of object-oriented programming (OOP) languages, UML associations do not have such a direct OOP counterpart. They are therefore often more difficult to understand for developers. Only in the special case of a unidirectional functional association there is a direct OOP counterpart: a reference property for referencing the objects that are linked to a given object by the association.

From a logical point of view, a class model defines a vocabulary, or language, for expressing various types of fact statements about objects. The knowledge representation languages RDF and OWL allow to formalize the vocabularies defined by class models and the fact statements made when instantiating their classes by creating objects. In this way, they help to understand the semantics of information models.

## 5.1Classes with Properties and Methods

In a UML class diagram, a class has a name (shown in the first compartment of the class rectangle), and it may have properties (shown in the second compartment) and methods (shown in the third compartment). Properties and methods may be described with or without details. The following diagrams illustrate these options using the example of a class `books` or `Book` for describing books as information objects.

A class can be expressed in UML by just providing its name, without any further detail, like so

![](graphic/16_chapter05_fig_01.png)

This option is useful for making sketches and overview diagrams. Using an ordinary English plural name like `books` makes the class diagram more readable for non-tech-savvy people.

A more informative description of a class is obtained by listing its properties, possibly without any further detail, like in the following example:

![](graphic/16_chapter05_fig_02.png)

However, for better understanding the meaning of properties and for being able to code a class in an OO programming language, we need to know the range of each property, which is the type of its values. The range of a property can be either a primitive datatype or another class.

In the following diagram we use general implementation-agnostic datatype names (like “Integer”), for which a specific programming language may have specific names (like “int” in Java). Notice that we now use a common OOP naming convention of giving classes a capitalized singular (mixed-case) name like `Book` (or `LearningUnit`). This allows saying that “an instance of a class `C` is a C (object)”, like “an instance of `Book` is a book (object)”.

![](graphic/16_chapter05_fig_03.png)

Notice how the standard identifier attribute `isbn` is marked with the keyword `id` appended to the property declaration in curly braces. This is the UML syntax for defining several kinds of property constraints discussed in the next chapter.

Finally, we can also define the methods and functions of a class in a third compartment, like so:

![](graphic/16_chapter05_fig_04.png)

In this example, the `Book` class has a function `checkISBN`, which returns a string. Given a class diagram in this form, it is straightforward to code it in an OO programming language like JavaScript or Java.

Recall that in JavaScript a class is defined in the form of a constructor function that assigns the values of its parameters to the properties of the newly created object, like so:

![](graphic/16_chapter05_fig_05.png)

In JavaScript, the (instance-level) methods of a class are defined as method slots of the constructor’s built-in `prototype` object. This is how we code the `checkISBN` method:

![](graphic/16_chapter05_fig_06.png)

If we don’t have to care about older web browsers, such as Internet Explorer 9, we can also use the new `class` definition syntax (introduced in the ES6 version of JavaScript) and combine the definition of properties and methods in one piece of code:

![](graphic/16_chapter05_fig_07.png)![](graphic/16_chapter05_fig_08.png)

As opposed to JavaScript, Java has always had a language element `class` for defining classes:

![](graphic/16_chapter05_fig_09.png)

We need to be aware of the ambiguity of the term “object”. We have to distinguish between objects in the sense of real-world objects (also called “business objects” or “entities”) and objects in an OO program, such as JS objects or Java objects. When we want to manage information about business objects of some type in an app, we represent them in the form of JS/Java objects instantiating a JS/Java class that represents their (business) object type. We call these classes model classes for two reasons: first because they implement the classes defined in an app’s data model, and second because they represent the ‘model’ part of an app’s Model-View-Controller codebase architecture.

Therefore, in a JS/Java app, a business object is a JS/Java object, but not every JS/ Java object represents a business object because we use JS/ Java objects for many purposes (e. g., in JavaScript, an array is a a JS object, but it’s not a business object). The same applies to classes: (business) object types are represented as model classes, but not every JS/Java class is a model class because we may use JS/Java classes also for other purposes (e. g., in Java, a class can be used as a container for a method library, but such a class is not a model class).

## 5.2Connecting Classes with Associations

Whenever an app has to manage the data of more than one object type, it is very likely that there are associations between some of them. For instance, in the following class diagram, there is an association between `publishers` and `books` and an association between `books` and `people` as authors.

![](graphic/16_chapter05_fig_10.png)

An association between two classes can be read in both directions. The association between `publishers` and `books` associates

1.  the books published by a publisher with this publisher, as indicated by the association end name `published books`,
2.  inversely (from right to left), the publisher of a book with this book.

The association between `books` and `people` as authors associates

1.  the authors of a book with this book, as indicated by the association end name `authors`,
2.  inversely (from right to left), the books authored by a person with this person, as indicated by the association end name `authored books`.

As will be discussed in Volume 2, associations are characterized by multiplicity constraints, which restrict the possibilities of how many objects of the associated class can be linked to an object of the given class. In our example, we have a one-to-many association between `publishers` and `books` and a many-to-many association between `books` and `people`.

For keeping things simple, we only include one object type and no association in the apps discussed in this volume of the book. In Volume 2, we will discuss how to model associations and how to implement them.

## 5.3From a Conceptual Model via a Design Model to Class Models

In a new development project, we start our analysis and modeling effort with making a conceptual information model. This type of model is also called domain model since it describes the entities of a given (real-world) problem domain, and does not model software entities.

Recall the conceptual information model for books obtained as the result of the inception phase:

![](graphic/16_chapter05_fig_11.png)

Taking this conceptual model as a starting point, we have to make a number of design decisions for obtaining an information design model:

1.  What are the ranges of the properties `isbn`, `title` and `year`?
2.  Which property is the standard identifier (ID) attribute?
3.  Which constraints should be defined?
4.  Which methods/ functions should be part of the design?

The result of this design phase is a design model like the following:

![](graphic/16_chapter05_fig_12.png)

It is important to understand that such a design model provides an implementation-agnostic (platform-independent) computational design, that is, it does not use any concept or syntax of any specific programming language or technology. Therefore, the same design model can be used for deriving different platform-specific implementation models for different programming languages or technologies, such as for a Java- or PHP-based framework, or for a plain JavaScript approach.

Based on the design model, by replacing the platform-independent datatype names with JavaScript-specific datatype names, and by adding “setter” methods, we obtain the following JavaScript implementation model, which we prefer to call a JavaScript class model:

![](graphic/16_chapter05_fig_13.png)

Notice that in this model, we have used the JavaScript datatypes `string` and `number`, and we have added the methods `setISBN`, `setTitle` and `setYear`. These “setter” methods are supposed to be used for setting a property to a new value, instead of directly assigning the value to the property.

Having a setter method for each property is a best-practice approach that allows more control over property value assignments. For instance, we could check the validity of values before they are assigned, or we could notify other modules of the app about the assignment event.

The implementation phase consists of making an implementation model for a specific technology platform, and then coding this model and testing the resulting program code. In this book, we make both JavaScript class models and Java class models, which are subsequently coded in plain JavaScript and in Java EE, respectively.

The entire transformation chain, from a conceptual model via a design model to a JavaScript class model (as a special type of implementation model), is summarized in the following figure.

![](graphic/16_chapter05_fig_14.png)

Figure 5.1 From a conceptual model via a design model to a JavaScript class model

In summary, the process of model-based development takes a conceptual model as the starting point for making a general (platform-independent) design model, from which one or more implementation models for a (set of) specific target technologies can be derived. Typically, they include a class model for an object-oriented programming language and a database model for an SQL DBMS. This process is illustrated by the following diagram:

## 5.4Excursion: Formalizing Information Models with RDF and OWL

The Resource Description Framework (RDF), together with its extension RDF Schema, is a logical formalism that allows

1.  formalizing information models in the form of RDF vocabularies consisting of class definitions and property definitions, where both class names and property names are URIs (representing globally unique identifiers);
2.  representing propositional information (in the form of statements about individuals) on the Web, embedded in web pages or in the form of special web data sources.

![](graphic/16_chapter05_fig_15.png)

Figure 5.2 From a conceptual model via design models to implementation models

RDF is the basis of the Semantic Web. It has several syntaxes, including the textual XML-based syntax of RDF/XML and the visual syntax of RDF Graphs.

### 5.4.1RDF vocabularies

Consider the `Book` class defined in the following class diagram

![](graphic/16_chapter05_fig_16.png)

The corresponding RDF vocabulary, with one class definition and three property definitions, is defined in the following RDF graph:

![](graphic/16_chapter05_fig_17.png)

In an RDF graph, nodes with an elliptic shape represent “resources” (like properties and classes), and arrows represent relationships defined by a property. Each arrow between two nodes represents a statement (also called “triple”). For instance the `rdf:range` arrow between `year` and `xs:int` represents the statement that the range of the property `year` is the XML Schema datatype `xs:int`, where `xs` is a namespace prefix for the XML Schema namespace.

Notice that RDF has the predefined meta-classes `rdfs:Class` and `rdf:Property`, used to define classes and their properties with the help of the predefined property `rdf:type`. For instance the `rdfs:type` arrow between `year` and `rdf: Property` represents the statement that `year` is of type `rdf:Property`, that is, it is defined to be an RDF property.

RDF graphs are a formalism for theoretical purposes. They can be used for illustrating simple examples. As opposed to UML class diagrams, they are not useful for visually expressing realistic vocabularies, due to their convolution and unnecessary visual complexity.

The domain of a property has to be defined explicitly in an RDF vocabulary (with an `rdfs:domain` property statement), as opposed to a UML class diagram where it is defined implicitly. While it is natural to define properties in the context of a class, as in UML, RDF allows defining properties independently of any class.

The RDF/XML syntax allows publishing an RDF vocabulary on the Web. For instance, the simple `Book` vocabulary defined in the RDF graph above, can be represented by the following RDF/ XML document:

![](graphic/16_chapter05_fig_18.png)![](graphic/16_chapter05_fig_19.png)

Notice that the values of the `rdf:resource` attribute must be URIs. If an attribute value is a fragment identifier like `#Book`, it represents a relative URI and is resolved into a full URI by appending the fragment identifier to the in-scope base URI, which may be defined with the `xml:base` attribute.

If an attribute value is an absolute URI like “ http://www.w3.org/2001/XMLSchema#string”, it contains a full namespace URI (like “ [http://www.w3.org/2001/XMLSchema”)](http://www.w3.org/2001/XMLSchema”), even if a namespace prefix (like “xsd” or “xs”) is defined for it. This is because namespace prefixes can only be used for XML element and attribute names, but not for attribute values, which unfortunately makes RDF/XML hard to read for human users.

Notice that the RDF formalization of our simple UML class model above has several shortcomings:

1.  It does not express the constraints that all three properties are mandatory and single-valued, which they are by default in UML.
2.  It does not express the constraints that the ISBN property, as a standard identifier (or primary key) attribute, is mandatory and unique.

We show how to solve these two issues with the greater expressivity of OWL below.

### 5.4.2RDF fact statements

The propositional information items, or fact statements, expressible with RDF are

1.  classification statements like “`ex:Book` is a `rdfs:Class`” or “`urn: isbn:006251587X` is a `ex:Book`”, and
2.  property statements of the sort “the `ex:isbn` property value of `urn: isbn:006251587X` is ’006251587X’”.

Consequently, for a UML object definition like

![](graphic/16_chapter05_fig_20.png)

we obtain several RDF fact statements:

![](graphic/16_chapter05_fig_21.png)

### 5.4.3Expressing structured data in web documents

There are many use cases for machine-readable data (e. g., about people, events, products, etc.) embedded in web documents. For instance, search engines like Google can use such structured data[92](32_Notes02.xhtml_Notes02_42) for providing more meaningful search results.

Structured data, or meta-data, can be embedded in a web document by either adding a JSON-LD[93](32_Notes02.xhtml_Notes02_43)`script` element containing it, or by annotating the document’s content, e.g., the HTML elements of a web page, with RDFa[94](32_Notes02.xhtml_Notes02_44).

Very limited annotation approaches, called “microformats” (proposed around 2005), are the historic predecessors of the general annotation language RDFa, which is derived from RDF. Some microfomats, like vCard and vEvent, are still being used today, but they are increasingly replaced with one of the two general formats RDFa and JSON-LD.

The main author of HTML5, Ian Hickson, has proposed an alternative general annotation language, called microdata[95](32_Notes02.xhtml_Notes02_45), with the goal to simplify RDFa and remedy its usability issues (in particular, by dropping its use of XML namespaces). Despite the (rather unfortunate) choice of using different names for the same annotation concepts (like “itemprop” instead of “property”), Hickson’s microdata proposal succeeded to show

1.  how to get essentially the same annotation functionality at lower usability costs, and
2.  how to integrate annotations with the DOM.

Since Hickson ended his collaboration with the W3C, the microdata proposal did not succeed to get an official W3C status, and web browsers have discontinued their support for it. However, it triggered a W3C proposal to use the RDFa Lite subset of RDFa, which “can be applied to most simple to moderate structured data markup tasks, without burdening the authors with additional complexities”.

We present a simple example for using structured data in a web page. Consider the following HTML fragment:

![](graphic/16_chapter05_fig_22.png)

For this content, we may want to code the information that

1.  the available information is about an entity of type `Person`, which has been defined as a class by the search engine standard vocabulary `schema. org`[96](32_Notes02.xhtml_Notes02_46);
2.  the name of the person is “Carly Rae Jepsen”;
3.  the telephone number of the person is “1–800 –2437715”.

Using the RDFa attributes `typeof`, `vocab` and `property`, we can code this information by adding the following annotations to the HTML content:

![](graphic/16_chapter05_fig_23.png)

Using JSON-LD, as recommended by Google, we need to add a `script` element of type “application/ld+json” containing the meta-data:

![](graphic/16_chapter05_fig_24.png)

The propositional information expressed with RDFa annotations and JSON-LD corresponds to the following RDF/XML code:

![](graphic/16_chapter05_fig_25.png)

### 5.4.4OWL vocabularies and constraints

OWL extends RDF by adding many additional language elements for expressing constraints, equalities and derived classes and properties in the context of defining vocabularies. Facts are expressed as in RDF (e. g., with `rdf:Description`).

OWL provides its own predefined language elements for defining classes and properties:

1.  The predefined class `owl:Class` is a subclass of `rdfs:Class`.
2.  The predefined class `owl:DatatypeProperty` is a subclass of `rdf:Property`. It classifies attributes. Therefore, the values of an `owl:DatatypeProperty` are data literals.
3.  The predefined class `owl:ObjectProperty` is a subclass of `rdf:Property`. It classifies reference properties corresponding to unidirectional binary associations. Since the values of a reference property are object references, the values of an `owl:ObjectProperty` are object references in the form of resource URIs.

We only show with the help of an example that an OWL vocabulary can represent a class diagram more faithfully than the corresponding RDF vocabulary by allowing to express certain constraints.

Consider the standard identifier attribute `isbn` defined in the `Book` class. In an RDF vocabulary, this attribute is defined in the following way:

![](graphic/16_chapter05_fig_26.png)

There are two issues with this RDF definition of an attribute:

1.  It doesn’t make it explicit that the property defined is an attribute, and not a reference property. This can only be inferred by finding out that the range class is a datatype, and not an object type.
2.  It does not constrain the attribute to have exactly one value, as implied by the defaults of UML class diagram semantics.

Using OWL, we can remedy these shortcomings of RDF. The following OWL property definition makes it explicit that the property `http://example.org/ex1#isbn` is an attribute, while the added OWL restriction defines an “exactly one” cardinality constraint for it:

![](graphic/16_chapter05_fig_27.png)

Since the ISBN attribute of the `Book` class has been designated as the standard identifier attribute in the UML class diagram above, we should define a uniqueness constraint for it. We can do this by including an `owl:hasKey` element within the class definition:

![](graphic/16_chapter05_fig_28.png)

### 5.4.5Usability issues of RDF and OWL

Both RDF and OWL have many usability issues. Especially OWL is so difficult to use that most potential users will be discouraged by it.

Because OWL was created by a community that is more concerned with formal logic than with information modeling and is not familiar with the concepts and terminology established in information modeling, they have introduced many new unfamiliar terms for concepts that had already been established and named in information modeling. They have even introduced duplicate names within OWL: an attribute is in most places called “data property”, but in some places it is called “datatype property” (specifically in OWL/RDF).

Usability issues of RDF are:

1.  For historical reasons, RDF comes with a strange jargon. Especially, its “subject”-“predicate”-“object” terminology sucks.
2.  For historical reasons, RDF comes with two different XML namespaces, typically in the from of the two namespace prefixes “rdf” and “rdfs”. The history of a language should not be imposed on its syntax. Users shouldn’t have to bother about which prefix to use.
3.  RDF is using the uncommon term “IRI” (as an abbreviation of “International Resource Identifier”), following the unfortunate naming history from “URL” via “URI” to “IRI”, while the What Working Group’s URL Living Standard[97](32_Notes02.xhtml_Notes02_47) has reverted this naming history.
4.  For practical purposes, RDF is incomplete:

a.it does not make an explicit syntactic distinction between attributes (having a datatype as range) and reference properties (having an object type as range);

b.it does not allow expressing simple class definitions, which include mandatory value and single-value constraints, in an RDF vocabulary.

OWL is needed for getting these fundamental features.

Usability issues of OWL are:

1.  it uses an uncommon terminology: e. g., “data property” instead of attribute, “restriction” instead of constraint;
2.  some of its elements have confusing names: e. g., “ObjectIntersectionOf” does not denote an intersection of objects, but of object types, and “DataSomeValuesFrom” actually refers to “some data values from”;
3.  many of its language elements are kind of unnatural and hard to grasp (much less to remember): e. g., an exactly-one-value property constraint cannot be expressed in the definition of a class along with the property declaration, but requires a separate Restriction element (as shown above).

## 5.5Summary

1.  The inception phase of a development project includes problem analysis and requirements engineering. The main goal in this phase is to make a conceptual information model that lays the foundations for the app’s information architecture, which is defined by an implementation-agnostic information design model made in the design phase. Then, in the implementation phase, a platform-specific data model is derived from the information design model and coded in the platform’s programming language. In the case of an OOP platform, platform-specific data models take the form of class models that are coded as a set of model classes.
2.  UML class diagrams provide a visual language for defining an information architecture. Their main building blocks are class rectangles and association lines (connecting class rectangles).
3.  A class rectangle has one, two or three compartments, containing the name of the class, its properties, and its methods.
4.  An association line connects two classes. The purpose of an association is to classify relationships (links) between objects. In the special case of a unidirectional functional association there is a direct OOP counterpart: a reference property for referencing the objects that are linked to a given object by the association.

## 5.6Exercises

Consider the problem of managing information about movies, like the Internet Movie Database[98](32_Notes02.xhtml_Notes02_48).

1.  Describe an illustrative information fragment with the help of some sample data about 3 movies in the form of itemized lists.
2.  Turn the itemized lists of sample data into corresponding data tables with table names and suitable column headings.
3.  Make a conceptual information model describing movies, then derive an information design model from it and turn it into a JavaScript class model.
4.  Finally, code the JavaScript class model in the form of JavaScript model classes.

# 6Application Architecture

Web application systems, like any other complex engineering artifacts, need an architecture that helps master their complexity by breaking them down into smaller parts with manageable inter-dependencies. Software application architecture is concerned with the following issues:

1.  The state structure of the application system to be designed is defined in the form of information models describing its information architecture.
2.  The goal of a code base architecture is to structure and partition the overall program code of an application in such a way that the fundamental software quality goal of maintainability is achieved.
3.  The distribution of the application system’s runtime components within a computer network is defined by a deployment architecture. A web app is distributed on the Web, which is a world-wide client-server network system with HTTP-based communication.

As in all cases of designing a complex system, no matter if a new building, a new space shuttle, a new computer or a new software application is to be designed, an architecture provides a kind of master plan for defining the structure of the system. Any good architecture is based on the following three principles:

1.  separation of concerns,which helps managing complexity by breaking a system down into smaller, functionally defined parts such that their
2.  interdependencies are minimized,
3.  keeping the more fundamental parts independent of the less fundamental parts (the onion principle).

Complying with these principles makes it easier to develop, or source, and update certain system parts independently of others.

The three most important parts of the code base of an app are:

1.  the model, which implements the app’s data model in the form of model classes, defining suitable data structures and constraints;
2.  the data storage management procedures, which set up a connection to a storage management system (typically, but not necessarily, an SQL database system) and use it for storing and retrieving persistent data;
3.  the user interface (UI) code, taking care of both information provision (or output) to the user, e.g., on the computer screen, and user input provided by user actions in the form of UI events, e. g., keyboard or mouse events, such that all required user interactions are supported.

The onion principle requires to keep the app’s model classes independent of

–the UI code because it should be possible to re-use the same model classes with different UI technologies;

– the storage management code because it should be possible to re-use the same model classes with different storage technologies.

However, in many web application frameworks (e. g., in Java EE) the onion principle is violated.

## 6.1The Model-View-Controller (MVC) Architecture Metaphor

The most popular and most widely used code base architecture approach is the Model-View-Controller code base partitioning pattern. Although it has not been precisely defined, and has been implemented in many different ways, especially in web application frameworks, it is based on the principle of separation of concerns and on the fundamental insight that the model is the foundation for all other parts of an application, in particular for the user interface. Consequently, even if the MVC approach doesn’t provide a precise definition of what a ’model’ is, we can consider it to be a model-based approach.

![](graphic/17_chapter06_fig_01.png)

Figure 6.1 The MVC code base architecture with the model as the foundation.

According to Wikipedia, the first MVC architecture was introduced to application programming with Smalltalk-76 by Trygve Reenskaug[99](32_Notes02.xhtml_Notes02_49) in the 1970s. In a later article about Smalltalk-80[100](32_Notes02.xhtml_Notes02_50), MVC is explained as a “three-way division of an application” that entails “separating (1) the parts that represent the model of the underlying application domain from (2) the way the model is presented to the user and from (3) the way the user interacts with it”. The authors, who also use the term “MVC metaphor”, point out that their approach would allow programmers to “write an application model by first defining new classes that would embody the special application domain-specific information”.

Notice that the model is defined to consist of classes that capture the required domain information. We call them model classes.

In this original MVC approach, there is no well-defined concept of a user interface (UI). The ’view’ is defined as comprising the output side of a UI, only, while the user input side is separated from it and subsumed under the term ’controller’. This does not reflect how a UI is really organized: by combining certain forms of application output with certain forms of user input like two sides of the same coin. A general UI concept includes both the output (the information output provided to the user, as well as system actions) and the input (including information input provided, as well as actions performed, by the user).

The Smalltalk MVC metaphor was developed for (monochromatic) text-screen-based user interfaces with no general notion of UI events. This may explain why they did not consider an integral concept of a UI. While they distinguished between the state of objects in the model and their state in the UI, which are both in the scope of a user session, they did not consider the distinction between the model state and the database state.

In his web essay GUI Architectures[101](33_Notes03.xhtml_Notes03_1)(2006), Martin Fowler summarizes the main principles of the original MVC approach in the following way:

1.  Separation between UI and model.
2.  Divide UI into a ’controller’ and ’view’.
3.  Views are synchronized with the model (by means of a data binding mechanism).

While the first and third principles are fundamental for the architecture of software applications, the second principle has just a historic meaning and was soon abandoned by the developers of Smalltalk.

Compared to the 1980s, computers, human-computer interaction and software application architecture have evolved. In particular, the establishment of the Web as the predominant computing platform has made web browsers to be the most important infrastructure for user interfaces.

The MVC terminology is still widely used today, especially by web application frameworks, but with different meanings ascribed to “M”, “V” and “C”. Typically, the “view” denotes the app’s code for the HTML-forms-based user interface, and the “controller” denotes the code that is in charge of mediating between the “view” and the “model”.

In many MVC approaches, the “model” is tightly coupled with the underlying database technology, often via an object-relational mapping (ORM) approach mapping classes to tables and objects to table rows. This tight coupling between model classes and database tables violates both the fundamental principle of minimizing interdependencies (because there is no need that model classes depend on database tables) and the onion principle discussed below.

For instance, in the Active Record[102](33_Notes03.xhtml_Notes03_2) paradigm of the influential Ruby-on-Rails framework, which has been adopted by many other web application frameworks (such as by CakePHP), the “model” is a direct representation of the schema of the underlying database system, where each entity table of the database is represented by a “model” class that inherits data manipulation methods for performing Create/ Retrieve/ Update/Delete (CRUD) operations. In this table-to-model-class mapping approach, the “model” depends on the schema of the underlying database and is therefore tightly coupled with the underlying ORM technology. While this may be a suitable approach for a database-first development methodology, where an SQL database is the foundation of an application, it is certainly not a general approach and it turns the model into a secondary asset.

Also in frameworks based on ORM annotations, such as Java EE with JPA annotations, the C# framework ASP.NET MVC with Entity Framework and Data Annotations, or the PHP framework Symfony with Doctrine annotations, the “model” is coupled with the underlying ORM technology through the ORM annotations woven into the model class code, thus making the model dependent on the ORM technology used. All these frameworks use the Data Mapper[103](33_Notes03.xhtml_Notes03_3) approach for performing CRUD operations based on ORM annotations.

## 6.2The Onion Architecture Metaphor

The term “onion architecture” was coined by Jeffry Palermo in a series of blog posts[104](33_Notes03.xhtml_Notes03_4) in 2008\. The main principles of this architecture metaphor are (1) to use a hierarchy of dependencies, where less fundamental (or central) parts depend on more fundamental parts, but never the other way around, and (2) the most fundamental part is the model, which implements the application’s data model in the form of model classes while data storage is a separate and less fundamental part that must not be coupled with the model.

In fact, Palermo and his followers put a lot more into this architecture metaphor, such as using “repository interfaces” and “service interfaces”, but this is not really essential for the onion metaphor. Also, they are using a different terminology. When they are using the term “domain model” instead of simply model, they are confusing the term “domain model” with “implementation of data model”,which is what model classes do. A data model is derived from an information design model, which may itself be derived from a domain information model. This is the basic development chain in model-based software engineering.

In principle, a Data Mapper approach, if it is not based on a platform-specific ORM (annotation) technology, but rather on some form of platform-independent mapping logic, can be used for storage management in an onion architecture.

## 6.3 “Logical” versus “Physical” User Interface

The idea of a logical UI model, also called view model, was first proposed (under a different name) by Martin Fowler in his post on the Presentation Model[105](33_Notes03.xhtml_Notes03_5) in 2004, where he stated that the view model “pulls the state and behavior of the view out into a [view] model class”. This means that the logical content of a UI is abstracted out from a concrete “physical” UI, which has specific renderings of the logical UI fields and “commands” (user actions). Logical UI fields are rendered in the form of UI widgets that may have their own state, while logical UI commands are rendered in the form of suitable UI events.

Later, in 2005, the view model concept was adopted by John Gossman (from Microsoft) in his blog post Introduction to Model/View/ViewModel pattern for building WPF Apps[106](33_Notes03.xhtml_Notes03_6) and popularized under the architecture pattern acronym “MVVM”.

In a user interface for a Create/Retrieve/Update/Delete (CRUD) data management operation, a view model class would be bound to exactly one model class, but could support more than one view (class). A view model class would have properties that are bound to the widgets of the supported view(s), using either one-way or two-way data binding, and methods that are bound to corresponding commands (command binding).

Typically, most view fields directly correspond to properties of the underlying model class, although they may have a different name. For these fields (or view model properties), a data binding to the corresponding model properties is needed. But a view model class may also have additional properties, some of them may represent view fields that are not bound to a model class property, while others may represent auxiliary fields that are not shown in the UI.

The methods of a view model class are invoked when a corresponding command has been issued by the user through creating a UI event, to which the command has been bound.

Dividing up the overall UI code into a view model part and a view part creates a certain overhead that may not be justified in certain cases. While the use of a view model is justified for all apps with CRUD data management operations, it may, for instance, not be justified for visualization user interfaces.

The main benefits of view models are that they facilitate: (1) UI design, (2) the testing of the UI logic, and (3) the maintenance of the UI.

## 6.4MVC Web Applications

The MVC terminology is still widely used today, especially by web application frameworks, but with different meanings ascribed to “M”, “V” and “C”. In some approaches it is extended by adding another layer, called “view model” abbreviated by “VM”, which we will discuss later in the course.

In the original MVC proposal, the “model” consists of model classes implementing the app’s data model, while today many MV(VM)(C) frameworks do not include any concept of model classes, but rather refer to data objects (or records) as “models”. Also the term “controller” is ambiguous today. In the original MVC proposal, the term “controller” referred to the handling of UI events including user inputs. Today, it typically refers to all the glue code needed for mediating between the model and the view, including the code for routing.

In summary, in today’s frameworks, the term “model” vaguely refers to the data sources of an app, while the “view” denotes the app’s code for the user interface, which is based on CSS-styled HTML forms and DOM events, and the “controller” typically denotes the (glue) code that is in charge of mediating between the view and the model. There is widespread agreement that

1.  the model should be independent of the view and the controller, implying that the model must neither invoke the view nor the controller (in the model code, there should be no calls of any view or controller procedures);
2.  the controller may invoke both the model and the view;
3.  the view may invoke the controller.

However, as shown in the following diagram, it is not clear if the view may also invoke the model, or if it needs to route any calls of model procedures via the controller. Both approaches are being used in practice. The first approach, where model procedures can be called from the view, is simpler and leads to a leaner controller.

![](graphic/17_chapter06_fig_02.png)

The second approach, where the view is decoupled from the model by routing all calls to it via the controller, is called the mediating-controller MVC approach, shown in the following diagram. It has the advantage of fewer dependencies and providing better support for model-view synchronization based on data-bindings.

![](graphic/17_chapter06_fig_03.png)

In many MVC web application frameworks, the model is tightly coupled with the underlying data storage technology, often via an object-relational mapping (ORM) approach mapping classes to tables and objects to table rows. This tight coupling makes model classes dependent on a specific database technology or even on corresponding database tables. It therefore violates the onion principle, since the model is the most fundamental part of an app, so it must not depend on any other part.

## 6.5Deployment Architectures

In addition to an information architecture and a code base organization architecture (like MVC), we also have the cross-cutting issue of how to distribute the different parts of an app when it is deployed, so we also need a deployment architecture.

Traditionally, most parts of a web app have been executed on back-end computers, while only its HTML/CSS user interface code has been executed on the front-end (or client) side, within a web browser. Today, with the rise of modern JavaScript, we have the option to replace traditional back-end web apps with JavaScript front-end apps, where most parts of the app are executed within a web browser on a front-end device. Such a front-end web app may use either local storage or a (remote) cloud storage service, as illustrated by the two architecture diagrams shown in [Figure 6.2](#17_chapter06.xhtml_chapter06_19).

![](graphic/17_chapter06_fig_04.png)

Figure 6.2 Architectures for front-end web apps

In both cases, the JavaScript code of the front-end app is loaded together with its start web page. While using local data storage (with JavaScript’s `localStorage` or `indexedDB` APIs) does not require any connection to the Internet after the initial loading of the app, using cloud storage via HTTP messaging with the `XMLHttpRequest` (XHR) API does require an Internet connection.

Typically, but not necessarily, a front-end web app is a single-user application, which is not shared with other users.

A back-end web app is a web app where essentially all work is performed by the back-end component, including data validation and user interface page creation. It does not have any front-end component, except the HTML-forms-based, and possibly JS-enriched, user interface pages sent to the user’s front-end computer for being rendered by a web browser.

One important task of the controller, especially in back-end apps, is routing: mapping incoming HTTP request messages to a use case of the app, typically represented by a method of a class, such that either the corresponding user interface is provided in the form of a web page or the request message represents the corresponding form submission, which can be directly processed.

Today, with NodeJS, we have the option to deploy the JavaScript components of our app either on the back-end or on the front-end, or on both. In the future, due to WebAssembly, the same options may also be available to other programming languages. Web apps that run the same JavaScript code both on the back-end and front-end have been called “universal” (or “isomorphic”). This is especially useful for data validation code because in a responsive constraint validation approach, as discussed in [Chapter 7](#19_chapter07.xhtml_chapter07_1), we validate user data immediately on input in the user interface, but we also validate it on the back-end before save. Modern JavaScript allows truly distributed apps.

The two diagrams shown in [Figure 6.3](#17_chapter06.xhtml_chapter06_21) illustrate the distinction between the traditional back-end web app architecture and the new architecture of a (truly) distributed web app.

![](graphic/17_chapter06_fig_05.png)

Figure 6.3 Architectures for back-end and distributed web apps

8_mvc_krasner_and_pope.pdf

![](graphic/11_Part01_fig_01.png)

# Part IIConstraint Validation

For catching various cases of flawed data, we need to define suitable integrity constraints that can be used by the application’s data validation mechanisms. Integrity constraints may take many different forms. The most important type of integrity constraints are property constraints, which define conditions on the admissible property values of an object.

# 7Integrity Constraints and Data Validation

## 7.1Introduction

For detecting non-admissible and inconsistent data and for preventing such data to be added to an application’s database, we need to define suitable integrity constraints that can be used by the application’s data validation mechanisms for catching these cases of flawed data. Integrity constraints are logical conditions that must be satisfied by the data entered by a user and stored in the application’s database.

For instance, if an application is managing data about persons including their birth dates and their death dates, then we must make sure that for any person record with a death date, this date is not before that person’s birth date.

Since integrity maintenance is fundamental in database management,the data definition language part of the relational database language SQL supports the definition of integrity constraints in various forms. On the other hand, however, there is hardly any support for integrity constraints and data validation in common programming languages such as PHP, Java, C# or JavaScript. It is therefore important to take a systematic approach to constraint validation in web application engineering, like choosing an application development framework that provides sufficient support for it.

Unfortunately, many web application development frameworks do not provide sufficient support for defining integrity constraints and performing data validation. Integrity constraints should be defined in one (central) place in an app, and then be used for configuring the user interface and for validating data in different parts of the app, such as in the user interface and in the database. In terms of usability, the goals should be:

1.  To prevent the user from entering invalid data in the user interface (UI) by limiting the input options, if possible.
2.  To detect and reject invalid user input as early as possible by performing constraint validation in the UI for those UI widgets where invalid user input cannot be prevented by limiting the input options.
3.  To prevent that invalid data pollutes the app’s main memory state and persistent database state by performing constraint validation also in the model layer and in the database.

HTML5 provides support for validating user input in an HTML-forms-based user interface (UI). Here, the goal is to provide immediate feedback to the user whenever invalid data has been entered into a form field. This UI mechanism of responsive validation is an important feature of modern web applications. In traditional web applications, the back-end component validates the data and returns the validation results in the form of a set of error messages to the front-end. Only then, often several seconds later, and in the hard-to-digest form of a bulk message, does the user get the validation feedback.

## 7.2Integrity Constraints

Integrity constraints (or simply constraints) are logical conditions on the data of an app. They may take many different forms. The most important type of constraints, property constraints, define conditions on the admissible property values of an object. They are defined for an object type (or class) such that they apply to all objects of that type. We concentrate on the most important cases of property constraints:

| String Length Constraints | require that the length of a string value for an attribute is less than a certain maximum number, or greater than a minimum number. |
| Mandatory Value Constraints | require that a property must have a value. For instance, a person must have a name, so the name attribute must not be empty. |
| Range Constraints | require that an attribute must have a value from the value space of the type that has been defined as its range. For instance, an integer attribute must not have the value “aaa” |
| Interval Constraints | require that the value of a numeric attribute must be in a specific inteval. |
| Pattern Constraints | require that a string attribute’s value must match a certain pattern defined by a regular expression. |
| Cardinality Constraints | apply to multi-valued properties, only, and require that the cardinality of a multi-valued property’s value set is not less than a given minimum cardinality or not greater than a given maximum cardinality. |
| Uniqueness Constraints | require that a property’s value is unique among all instances of the given object type. |
| Referential Integrity Constraints | require that the values of a reference property refer to an existing object in the range of the reference property. |
| Frozen Value Constraints | require that the value of a property must not be changed after it has been assigned initially. |

The visual language of UML class diagrams supports defining integrity constraints either in a special way for special cases (like with predefined keywords), or, in the general case, with the help of invariants, which are conditions expressed either in plain English or in the Object Constraint Language (OCL) and shown in a special type of rectangle attached to the model element concerned. We use UML class diagrams for modeling constraints in design models that are independent of a specific programming language or technology platform.

UML class diagrams provide special support for expressing multiplicity (or cardinality) constraints. This type of constraint allows to specify a lower multiplicity (minimum cardinality) or an upper multiplicity (maximum cardinality), or both, for a property or an association end. In UML, this takes the form of a multiplicity expression `l..u` where the lower multiplicity `l` is a non-negative integer and the upper multiplicity `u` is either a positive integer not smaller than `l` or the special value `*` standing for unbounded. For showing property multiplicity (or cardinality) constrains in a class diagram, multiplicity expressions are enclosed in brackets and appended to the property name, as shown in the `Person` class rectangle below.

In the following sections, we discuss the different types of property constraints listed above in more detail. We also show how to express some of them in computational languages such as UML class diagrams, SQL table creation statements, JavaScript model class definitions, or the annotation-based languages Java Bean Validation annotations and ASP.NET Data Annotations.

Any systematic approach to constraint validation also requires to define a set of error (or ’exception’) classes, including one for each of the standard property constraints listed above.

### 7.2.1String Length Constraints

The length of a string value for a property such as the title of a book may have to be constrained, typically rather by a maximum length, but possibly also by a minimum length. In an SQL table definition, a maximum string length can be specified in parenthesis appended to the SQL datatype `CHAR` or `VARCHAR`, as in `VARCHAR(50)`.

UML does not define any special way of expressing string length constraints in class diagrams. Of course, we always have the option to use an invariant for expressing any kind of constraint, but it seems preferable to use a simpler form of expressing these property constraints. One option is to append a maximum length, or both a minimum and a maximum length, in parenthesis to the datatype name, like so

![](graphic/19_chapter07_fig_01.png)

Another option is to use min/max constraint keywords in the property modifier list:

![](graphic/19_chapter07_fig_02.png)

### 7.2.2Mandatory Value Constraints

A mandatory value constraint requires that a property must have a value. This can be expressed in a UML class diagram with the help of a multiplicity constraint expression where the lower multiplicity is 1\. For a single-valued property, this would result in the multiplicity expression `1..1`, or the simplified expression `1`, appended to the property name in brackets. For example, the following class diagram defines a mandatory value constraint for the property `name`:

![](graphic/19_chapter07_fig_03.png)

Whenever a class rectangle does not show a multiplicity expression for a property, the property is mandatory (and single-valued), that is, the multiplicity expression `1` is the default for properties.

In an SQL table creation statement, a mandatory value constraint is expressed in a table column definition by appending the key phrase `NOT NULL` to the column definition as in the following example:

![](graphic/19_chapter07_fig_04.png)

According to this table definition, any row of the `persons` table must have a value in the column `name`, but not necessarily in the column `age`.

In JavaScript, we can code a mandatory value constraint by a class-level check function that tests if the provided argument evaluates to a value, as illustrated in the following example:

![](graphic/19_chapter07_fig_05.png)

With Java Bean Validation, a mandatory property like `name` is annotated with `Not-Null` in the following way:

![](graphic/19_chapter07_fig_06.png)

The equivalent ASP.NET Data Annotation is `Required` as shown in

![](graphic/19_chapter07_fig_07.png)

### 7.2.3Range Constraints

A range constraint requires that a property must have a value from the value space of the type that has been defined as its range. This is implicitly expressed by defining a type for a property as its range. For instance, the attribute `age` defined for the object type `Person` in the class diagram above has the range `Integer`, so it must not have a value like “aaa”, which does not denote an integer. However, it may have values like -13 or 321, which also do not make sense as the age of a person. In a similar way, since its range is `String`, the attribute `name` may have the value “” (the empty string), which is a valid string that does not make sense as a name.

We can avoid allowing negative integers like -13 as age values, and the empty string as a name, by assigning more specific datatypes as range to these attributes, such as `NonNegativeInteger` to `age`, and `NonEmptyString` to `name`. Notice that such more specific datatypes are neither predefined in SQL nor in common programming languages, so we have to implement them either in the form of user-defined types, as supported in SQL-99 database management systems such as PostgreSQL, or by using suitable additional constraints such as interval constraints, which are discussed in the next section. In a UML class diagram, we can simply define `NonNegativeInteger` and `NonEmptyString` as custom datatypes and then use them in the definition of a property, as illustrated in the following diagram:

![](graphic/19_chapter07_fig_08.png)

In JavaScript, we can code a range constraint by a check function, as illustrated in the following example:

![](graphic/19_chapter07_fig_09.png)

This check function detects and reports a constraint violation if the given value for the `name` property is not of type “string” or is an empty string.

In a Java EE web app, for declaring empty strings as non-admissible user input we must set the context parameter

![](graphic/19_chapter07_fig_10.png)

to `true` in the web deployment descriptor file `web.xml`.

In ASP.NET, empty strings are non-admissible by default.

### 7.2.4Interval Constraints

An interval constraint requires that an attribute’s value must be in a specific interval, which is specified by a minimum value or a maximum value, or both. Such a constraint can be defined for any attribute having an ordered type, but normally we define them only for numeric datatypes or calendar datatypes. For instance, we may want to define an interval constraint requiring that the `age` attribute value must be in the interval [25,70]. In a class diagram, we can define such a constraint by using the property modifiers `min` and `max`, as shown for the `age` attribute of the `Driver` class in the following diagram.

![](graphic/19_chapter07_fig_11.png)

In an SQL table creation statement, an interval constraint is expressed in a table column definition by appending a suitable `CHECK` clause to the column definition as in the following example:

![](graphic/19_chapter07_fig_12.png)

In JavaScript, we can code an interval constraint in the following way:

![](graphic/19_chapter07_fig_13.png)

In Java Bean Validation, we express this interval constraint by adding the annotations `Min(0)` and `Max(120)` to the property `age` in the following way:

![](graphic/19_chapter07_fig_14.png)![](graphic/19_chapter07_fig_15.png)

The equivalent ASP.NET Data Annotation is `Range(25,70)` as shown in

![](graphic/19_chapter07_fig_16.png)

### 7.2.5Pattern Constraints

A pattern constraint requires that a string attribute’s value must match a certain pattern, typically defined by a regular expression. For instance, for the object type `Book` we define an `isbn` attribute with the datatype `String` as its range and add a pattern constraint requiring that the `isbn` attribute value must be a 10-digit string or a 9-digit string followed by “X” to the `Book` class rectangle shown in the following diagram.

![](graphic/19_chapter07_fig_17.png)

In an SQL table creation statement, a pattern constraint is expressed in a table column definition by appending a suitable `CHECK` clause to the column definition as in the following example:

![](graphic/19_chapter07_fig_18.png)

The `~` (tilde) symbol denotes the regular expression matching predicate and the regular expression `\d{9}(\d|X)$` follows the syntax of the POSIX standard (see, e. g. the PostgreSQL documentation[107](33_Notes03.xhtml_Notes03_7)).

In JavaScript, we can code a pattern constraint by using the built-in regular expression function `test`, as illustrated in the following example:

![](graphic/19_chapter07_fig_19.png)

In Java EE Bean Validation, this pattern constraint for `isbn` is expressed with the annotation `Pattern` in the following way:

![](graphic/19_chapter07_fig_20.png)

The equivalent ASP.NET Data Annotation is `RegularExpression` as shown in

![](graphic/19_chapter07_fig_21.png)

### 7.2.6Cardinality Constraints

A cardinality constraint requires that the cardinality of a multi-valued property’s value set is not less than a given minimum cardinality or not greater than a given maximum cardinality. In UML, cardinality constraints are called multiplicity constraints, and minimum and maximum cardinalities are expressed with the lower bound and the upper bound of the multiplicity expression, as shown in the following diagram, which contains two examples of properties with cardinality constraints.

![](graphic/19_chapter07_fig_22.png)

The attribute definition `nickNames[0..3]` in the class `Person` specifies a minimum cardinality of 0 and a maximum cardinality of 3, with the meaning that a person may have no nickname or at most 3 nicknames. The reference property definition `members[3..5]` in the class `Team` specifies a minimum cardinality of 3 and a maximum cardinality of 5, with the meaning that a team must have at least 3 and at most 5 members.

It’s not obvious how cardinality constraints could be checked in an SQL database, as there is no explicit concept of cardinality constraints in SQL, and the generic form of constraint expressions in SQL, assertions, are not supported by available DBMSs. However, it seems that the best way to implement a minimum (or maximum) cardinality constraint is an on-delete (or on-insert) trigger that tests the number of rows with the same reference as the deleted (or inserted) row.

In JavaScript, we can code a cardinality constraint validation for a multi-valued property by testing the size of the property’s value set, as illustrated in the following example:

![](graphic/19_chapter07_fig_23.png)

With Java Bean Validation annotations, we can specify

![](graphic/19_chapter07_fig_24.png)

### 7.2.7Uniqueness Constraints

A uniqueness constraint (or key constraint) requires that a property’s value (or the value list of a list of properties in the case of a composite key constraint) is unique among all instances of the given object type. For instance, in a UML class diagram with the object type `Book` we can define the `isbn` attribute to be unique, or, in other words, a key, by appending the (user-defined) property modifier keyword `key` in curly braces to the attribute’s definition in the `Book` class rectangle shown in the following diagram.

![](graphic/19_chapter07_fig_25.png)

In an SQL table creation statement, a uniqueness constraint is expressed by appending the keyword `UNIQUE` to the column definition as in the following example:

![](graphic/19_chapter07_fig_26.png)

In JavaScript,we can code this uniqueness constraint by a check function that tests if there is already a book with the given `isbn` value in the `books` table of the app’s database.

### 7.2.8Standard Identifiers (Primary Keys)

An unique attribute (or a composite key) can be declared to be the standard identifier for objects of a given type, if it is mandatory (or if all attributes of the composite key are mandatory). We can indicate this in a UML class diagram with the help of the property modifier `id` appended to the declaration of the attribute `isbn` as shown in the following diagram.

![](graphic/19_chapter07_fig_27.png)

Notice that such a standard identifier declaration implies both a mandatory value and a uniqueness constraint on the attribute concerned.

Standard identifiers are called primary keys in relational databases. We can declare an attribute to be the primary key in an SQL table creation statement by appending the phrase `PRIMARY KEY` to the column definition as in the following example:

![](graphic/19_chapter07_fig_28.png)

In JavaScript, we cannot easily code a standard identifier declaration, because this would have to be part of the metadata of the class definition, and there is no standard support for such metadata in JavaScript. However, we should at least check if the given argument violates the implied mandatory value or uniqueness constraints by invoking the corresponding check functions discussed above.

### 7.2.9Referential Integrity Constraints

A referential integrity constraint requires that the values of a reference property refer to an object that exists in the population of the property’s range class. Since we do not deal with reference properties in this chapter, we postpone the discussion of referential integrity constraints to Volume 2.

### 7.2.10Frozen and Read-Only Value Constraints

A frozen value constraint defined for a property requires that the value of this property must not be changed after it has been assigned. This includes the special case of read-only value constraints on mandatory properties that are initialized at object creation time.

Typical examples of properties with a frozen value constraint are standard identifier attributes and event properties. In the case of events, the semantic principle that the past cannot be changed prohibits that the property values of events can be changed. In the case of a standard identifier attribute we may want to prevent users from changing the ID of an object since this requires that all references to this object using the old ID value are changed as well, which may be difficult to achieve (even though SQL provides special support for such ID changes by means of its `ON UPDATE CASCADE` clause for the change management of foreign keys).

The following diagram shows how to define a frozen value constraint for the `isbn` attribute:

![](graphic/19_chapter07_fig_29.png)

In Java, a read-only value constraint can be enforced by declaring the property to be `final`. In JavaScript, a read-only property slot can be implemented as in the following example:

![](graphic/19_chapter07_fig_30.png)

where the property slot `obj.teamSize` is made unwritable. An entire object `obj` can be frozen with `Object.freeze( obj)`.

We can implement a frozen value constraint for a property in the property’s setter method like so:

![](graphic/19_chapter07_fig_31.png)

### 7.2.11Beyond property constraints

So far, we have only discussed how to define and check property constraints. However, in certain cases there may be also integrity constraints that do not just depend on the value of a particular property, but rather on

1.  the values of several properties of a particular object (object-level constraints),
2.  the value of a property before and its value after a change attempt (dynamic constraints),
3.  the set of all instances of a particular object type (type-level constraints),
4.  the set of all instances of several object types.

OCL

The Object Constraint Language (OCL) was defined in 1997 as a formal logic language for expressing integrity constraints in UML version 1.1\. Later, it was extended for allowing to define also (1) derivation expressions for defining derived properties, and (2) preconditions and postconditions for operations, in a class model.

In a class model, property constraints can be expressed within the property declaration line in a class rectangle (typically with keywords, such as `id`, `max`, etc.). For expressing more complex constraints, such as object-level or type-level constraints, we can attach an invariant declaration box to the class rectangle(s) concerned and express the constraint either in (unambiguous) English or in the Object Constraint Language (OCL). A simple example of an object-level constraint expressed as an OCL invariant is shown in [Figure 7.1](#19_chapter07.xhtml_chapter07_15).

![](graphic/19_chapter07_fig_32.png)

Figure 7.1 An example of an object-level constraint

A general approach for implementing object-level constraint validation consists of taking the following steps:

1.  Choose a fixed name for an object-level constraint validation function, such as `validate`.
2.  For any class that needs object-level constraint validation, define a `validate` function returning either a `ConstraintViolation` or a `NoConstraintViolation` object.
3.  Call this function, if it exists, for the given model class,

a.in the UI/view, on form submission;

b.in the model class, before save, both in the `create` and in the `update` method.

Constraints affecting two or more model classes could be defined in the form of static methods (in a model layer method library) that are invoked from the object-level validation methods of the affected model classes.

## 7.3Responsive Validation

This problem is well-known from classical web applications where the front-end component submits the user input data via HTML form submission to a back-end component running on a remote web server. Only this back-end component validates the data and returns the validation results in the form of a set of error messages to the front-end. Only then, often several seconds later, and in the hard-to-digest form of a bulk message, does the user get the validation feedback. This approach is no longer considered acceptable today. Rather, in a responsive validation approach, the user should get immediate validation feedback on each single data input. Technically, this can be achieved with the help of event handlers for the user interface events `input` or `change`.

Responsive validation requires a data validation mechanism in the user interface (UI), such as the HTML5 form validation API[108](33_Notes03.xhtml_Notes03_8). Alternatively, the jQuery Validation Plugin[109](33_Notes03.xhtml_Notes03_9) can be used as a (non-HTML5-based) form validation API.

The HTML5 form validation API essentially provides new types of `input` fields (such as `number` or `date`) and a set of new attributes for form control elements for the purpose of supporting responsive validation performed by the browser. Since using the new validation attributes (like `required`, `min`, `max` and `pattern`) implies defining constraints in the UI, they are not really useful in a general approach where constraints are only checked, but not defined, in the UI.

Consequently, we only use two methods of the HTML5 form validation API for validating constraints in the HTML-forms-based user interface of our app. The first of them, `setCustomValidity`, allows to mark a form field as either valid or invalid by assigning either an empty string or a non-empty (constraint violation) message string.

The second method, `checkValidity`, is invoked on a form before user input data is committed or saved (for instance with a form submission). It tests, if all fields have a valid value. For having the browser automatically displaying any constraint violation messages, we need to have a `submit` event, even if we don’t really submit the form, but just use a `save` button.

See this Mozilla tutorial[110](33_Notes03.xhtml_Notes03_10) or this HTML5Rocks tutorial[111](33_Notes03.xhtml_Notes03_11) for more about the HTML5 form validation API.

## 7.4Constraint Validation in MVC Applications

Integrity constraints should be defined in the model classes of an MVC app since they are part of the business semantics of a model class (representing a business object type). However, a more difficult question is where to perform data validation? In the database? In the model classes? In the controller? Or in the user interface (“view”)? Or in all of them?

A relational database management system (DBMS) performs data validation whenever there is an attempt to change data in the database, provided that all relevant integrity constraints have been defined in the database. This is essential since we want to avoid, under all circumstances, that invalid data enters the database. However, it requires that we somehow duplicate the code of each integrity constraint, because we want to have it also in the model class to which the constraint belongs.

Also, if the DBMS would be the only application component that validates the data, this would create a latency, and hence usability, problem in distributed applications because the user would not get immediate feedback on invalid input data. Consequently, data validation needs to start in the user interface (UI).

However, it is not sufficient to perform data validation in the UI. We also need to do it in the model classes, and in the database, for making sure that no flawed data enters the application’s persistent data store. This creates the problem of how to maintain the constraint definitions in one place (the model), but use them in two or three other places (at least in the model classes and in the UI code, and possibly also in the database).We call this the multiple validation problem. This problem can be solved in different ways. For instance:

1.  Define the constraints in a declarative language (such as Java Bean Validation Annotations or ASP.NET Data Annotations) and generate the back-end/model and front-end/UI validation code both in a back-end application programming language such as Java or C#, and in JavaScript.
2.  Keep your validation functions in the (PHP, Java, C# etc.) model classes on the back-end, and invoke them from the JavaScript UI code via XHR. This approach can only be used for specific validations, since it implies the penalty of an additional HTTP communication latency for each validation invoked in this way.
3.  Use JavaScript as your back-end application programming language (such as with NodeJS), then you can code your validation functions in your JavaScript model classes on the back-end and execute them both before committing changes on the back-end and on user input and form submission in the UI on the front-end side.

The simplest, and most responsive, solution is the third one, using only JavaScript both for the back-end and front-end components of a web app.

## 7.5Adding Constraints to a Design Model

We again consider the book data management problem that was considered in Part 1\. But now we also consider the data integrity rules (or ’business rules’) that govern the management of book data. These integrity rules, or constraints, can be expressed in a UML class diagram as shown in [Figure 7.2](#19_chapter07.xhtml_chapter07_26) below.

![](graphic/19_chapter07_fig_33.png)

Figure 7.2 A design model defining the object type `Book` with two invariants

In this model, the following constraints have been expressed:

1.  Due to the fact that the `isbn` attribute is declared to be the standard identifier of `Book`, it is mandatory and unique.
2.  The `isbn` attribute has a pattern constraint requiring its values to match the ISBN-10 format that admits only 10-digit strings or 9-digit strings followed by “X”.
3.  The `title` attribute is mandatory, as indicated by its multiplicity expression [1], and has a string length constraint requiring its values to have at most 50 characters.
4.  The `year` attribute is mandatory and has an interval constraint, however, of a special form since the maximum is not fixed, but provided by the calendar function `nextYear()`, which we implement as a utility function.

Notice that the `edition` attribute is not mandatory, but optional, as indicated by its multiplicity expression [0..1]. In addition to the constraints described in this list, there are the implicit range constraints defined by assigning the datatype `NonEmptyString` as range to `isbn` and `title`, `Integer` to `year`, and `PositiveInteger` to `edition`. In our plain JavaScript approach, all these property constraints are coded in the model class within property-specific check functions.

The meaning of the design model can be illustrated by a sample data population respecting all constraints:

Table 7.1 Sample data for `Book`

![](graphic/19_chapter07_fig_34.png)

## 7.6 Summary

1.Constraints are logical conditions on the data of an app. The simplest, and most important, types of constraints are property constraints and object-level constraints.

2.Constraints should be defined in the model classes of an MVC app, since they are part of their business semantics.

3.Constraints should be checked in various places of an MVC app: in the UI/view code, in model classes, and possibly in the database.

4.Software applications that include CRUD data management need to perform two kinds of bi-directional object-to-string type conversions:

a.Between the model and the UI: converting model object property values to UI widget values, and, the other way around, converting input widget values to property values. Typically, widgets are form fields that have string values.

b.Between the model and the datastore: converting model objects to storage data sets (called serialization), and, the other way around, converting storage data sets to model objects (called de-serialization). This involves converting property values to storage data values, and, the other way around, converting storage data values to property values. Typically, datastores are either JavaScript’s local storage or IndexedDB, or SQL databases, and objects have to be mapped to some form of table rows. In the case of an SQL database, this is called “Object-Relational Mapping” (ORM).

5.Do not perform any string-to-property-value conversion in the UI code. Rather, this is the business of the model code.

6.For being able to observe how an app works, or, if it does not work, where it fails, it is essential to log all critical application events, such as data retrieval, save and delete events, at least in the JavaScript console.

7.Responsive validation means that the user, while typing, gets immediate validation feedback on each input (keystroke), and when requesting to save the new data.

## 7.7Criteria for Evaluating the Validation Support of Frameworks

The support of MVC frameworks for constraint validation can be evaluated according to the following criteria. Does the framework support

1.  the declaration of all important kinds of property constraints as defined above (String Length Constraints, Mandatory Value Constraints, Range Constraints, etc.) in model classes?
2.  the provision of an object validation function to be invoked in the UI on form submission, and in the model layer before save?
3.  validation in the model class on assign and before save?
4.  informative generic validation error messages referring to the object and property concerned?
5.  custom validation error messages with parameters?
6.  responsive validation in the user interface on input and on submit based on the constraints defined in the model classes, preferably using the HTML5 constraint validation API, or at least a general front-end API like the jQuery Validation Plugin?
7.  two-fold validation with defining constraints in the model and checking them in the model and in the view?
8.  three-fold validation with defining constraints in the model and checking them in the model, the view and in the database system?
9.  reporting database validation errors that are passed from the database system to the app?

## 7.8Quiz Questions

If you would like to look up the answers for the following quiz questions, you can check our discussion forum[112](33_Notes03.xhtml_Notes03_12). If you don’t find an answer in the forum, you may create a post asking for an answer to a particular question.

### 7.8.1Question 1: Where to check constraints

Where in the application code should the constraints be checked? In the …

☐controller code

☐model classes

☐user interface code

☐underlying DBMS (if it supports constraint validation)

### 7.8.2Question 2: Where to define constraints

Where in the application code should the constraints be defined? In the …

☐controller code

☐model classes

☐user interface HTML5 code

☐user interface JavaScript code

### 7.8.3Question 3: Counting constraints

![](graphic/19_chapter07_fig_35.png)

How many constraints are specified by the class model shown in the diagram? Enter a number: _____

### 7.8.4Question 4: Constraint names

![](graphic/19_chapter07_fig_36.png)

Which of the following constraints are specified by the class model?

☐A range constraint for the property `name`.

☐A uniqueness constraint for the property `name`.

☐A referential integrity constraint for the property `name`.

☐A uniqueness constraint for the property `age`.

☐A mandatory value constraint for the property `name`.

☐A mandatory value constraint for the property `age`.

### 7.8.5Question 5: Compliant objects

![](graphic/19_chapter07_fig_37.png)

Which of the following objects do not represent admissible instances (or, in other words, violate a constraint) of the object type `Person`?

![](graphic/19_chapter07_fig_38.png)

# 8Implementing Constraint Validation in a Plain JS Web App

## 8.1Introduction

The minimal JavaScript front-end web application that we have discussed in [Chapter 3](#14_chapter03.xhtml_chapter03_1) has been limited to support the minimum functionality of a data management app only. For instance, it did not take care of preventing the user from entering invalid data into the app’s database. In this chapter, we show how to express integrity constraints in a JavaScript model class, and how to perform constraint validation both in the model part of the app and in the user interface built with HTML5.

We show how to perform responsive validation with the HTML5 form validation API[113](33_Notes03.xhtml_Notes03_13). Since using the new HTML5 `input` field types and validation attributes (like `required`, `min`, `max` and `pattern`) implies defining constraints in the UI, they are not really useful in a best-practice approach where constraints are only checked, but not defined, in the UI.

Consequently, we will not use the new HTML5 features for defining constraints in the UI, but only use two methods of the HTML5 form validation API:

1.  `setCustomValidity`, which allows to mark a form field as either valid or invalid by assigning either an empty string or a non-empty (constraint violation) message string;
2.  `checkValidity`, which is invoked on a form before user input data is committed or saved (for instance with a form submission); it tests, if all fields have a valid value.

In the case of two special kinds of attributes, having calendar dates or colors as values, it is desirable to use the new UI widgets defined by HTML5 for picking a date or picking a color (with corresponding `input` field types). Unfortunately, in 2017, the HTML5 date picker widget is still not supported by all major browsers.

## 8.2New Issues

Compared to the Minimal App[114](33_Notes03.xhtml_Notes03_14) discussed in [Chapter 3](#14_chapter03.xhtml_chapter03_1) we have to deal with a number of new issues:

1.In the model code we have to add for every property of a class

a.a check function that can be invoked for validating the constraints defined for the property, and

b.a setter method that invokes the check function and is to be used for setting the value of the property.

2.In the user interface (“view”) code we have to take care of

a.responsive validation on user input for providing immediate feedback to the user,

b.validation on form submission for preventing the submission of flawed data to the model layer.

For improving the break-down of the view code, we introduce a utility method (in `lib/ util.js`) that fills a `select` form control with `option` elements the contents of which is retrieved from an entity table such as `Book. instances`. This method is used in the `setupUserInterface` method of both the `updateBook` and the `deleteBook` use cases.

Checking the constraints in the user interface (UI) on user input is important for providing immediate feedback to the user. But it is not safe enough to perform constraint validation only in the UI, because this could be circumvented in a distributed web application where the UI runs in the web browser of a front-end device while the application’s data is managed by a back-end component on a remote web server. Consequently, we need multiple constraint validation, first in the UI on input (or on change) and on form submission, and subsequently in the model layer before saving/sending data to the persistent data store. And in an application based on a DBMS we may also use a third round of validation before persistent storage by using the validation mechanisms of the DBMS. This is a must, when the application’s database is shared with other apps.

Our proposed solution to this multiple validation problem is to keep the constraint validation code in special check functions in the model classes and invoke these functions both in the UI on user input and on form submission, as well as in the create and update data management methods of the model class via invoking the setters. Notice that referential integrity constraints (and other relationship constraints) may also be violated through a delete operation, but in our single-class example we don’t have to consider this.

## 8.3Make a JavaScript Class Model

Using the information design model shown in [Figure 7.2](#19_chapter07.xhtml_chapter07_26) above as the starting point, we make a JavaScript class model by performing the following steps:

1.Create a check operation for each (non-derived) property in order to have a central place for implementing all the constraints that have been defined for a property in the design model. For a standard identifier attribute, such as `Book:: isbn`, two check operations are needed:

a.A basic check operation, such as `checkIsbn`, for checking all basic constraints of the attribute, except the mandatory value and the uniqueness constraints.

b.An extended check operation, such as `checkIsbnAsId`, for checking, in addition to the basic constraints, the mandatory value and uniqueness constraints that are required for a standard identifier attribute.

The `checkIsbnAsId` operation is invoked on user input for the `isbn` form field in the create book form, and also in the `setIsbn` method, while the `checkIsbn` operation can be used for testing if a value satisfies the syntactic constraints defined for an ISBN.

2.Create a setter operation for each (non-derived) single-valued property. In the setter, the corresponding check operation is invoked and the property is only set, if the check does not detect any constraint violation.

This leads to the JavaScript class model shown on the right-hand side of the mapping arrow in the following figure.

![](graphic/20_chapter08_fig_01.png)

Figure 8.1 From an information design model to a JS class model

Essentially, the JavaScript class model extends the design model by adding checks and setters for each property. The attached invariants have been dropped since they are taken care of in the checks. Property ranges have been turned into JavaScript datatypes (with a reminder to their real range in curly braces). Notice that the names of check functions are underlined, since this is the convention in UML for class-level (as opposed to instance-level) operations.

## 8.4Set up the Folder Structure Adding Some Library Files

The MVC folder structure of our validation app extends the structure of the minimal app by adding a `lib` folder containing the generic code libraries `browserShims. js`, `errorTypes.js` and `util.js`. Thus, we get the following folder structure:

![](graphic/20_chapter08_fig_02.png)

We discuss the contents of the added files in the following sub-sections.

### 8.4.1Provide general utility functions and JavaScript fixes in library files

We add three library files to the `lib` folder:

1.  `browserShims.js` contains a definition of the string trim function for older browsers that don’t support this function (which was only added to JavaScript in ES5, defined in 2009). More browser shims for other recently defined functions, such as `querySelector` and `classList`, could also be added to `browserShims.js`.
2.  `util.js` contains the definitions of a few utility functions such as `isNonEmptyString(x)` for testing if `x` is a non-empty string.
3.  `errorTypes.js` defines classes for error (or exception) types corresponding to the basic types of property constraints discussed above: StringLengthConstraintViolation, MandatoryValueConstraintViolation, RangeConstraintViolation, IntervalConstraintViolation, PatternConstraintViolation, UniquenessConstraintViolation. In addition, a class NoConstraintViolation is defined for being able to return a validation result object in the case of no constraint violation.

### 8.4.2Create a start page

The start page `index.html` takes care of loading CSS page styling files with the help of the following two `link` elements:

![](graphic/20_chapter08_fig_03.png)

Then it loads the following JavaScript files:

1.  `browserShims.js` and `util.js` from the `lib` folder, discussed in [Section 4.1](#15_chapter04.xhtml_chapter04_9),
2.  `errorTypes.js` from the `lib` folder, defining exception classes.
3.  `initialize. js` from the `src/ c` folder, defining the app’s MVC namespaces, as discussed in [Chapter 3](#14_chapter03.xhtml_chapter03_1)
4.  `Book. js` from the `src/m` folder, a model class file that provides data management and other functions discussed in [Section 5](#16_chapter05.xhtml_chapter05_1).

## 8.5Write the Model Code

The JavaScript class model shown on the right hand side in [Figure 8.1](#20_chapter08.xhtml_chapter08_9) can be coded step by step for getting the code of the model layer of our JavaScript front-end app. These steps are summarized in the following section.

### 8.5.1Summary

1.  Code the model class as a JavaScript constructor function.
2.  Code the check functions, such as `checkIsbn` or `checkTitle`, in the form of class-level (’static’) methods. Take care that all constraints, as specified in the JavaScript class model, are properly coded in the check functions.
3.  Code the setter operations, such as `setIsbn` or `setTitle`, as (instance-level) methods. In the setter, the corresponding check operation is invoked and the property is only set, if the check does not detect any constraint violation.
4.  Code the add and remove operations, if there are any, as instance-level methods.

These steps are discussed in more detail in the following sections.

### 8.5.2Code the model class as a constructor function

The class `Book` is coded as a corresponding constructor function with the same name `Book` such that all its (non-derived) properties are supplied with values from corresponding key-value slots of a `slots` parameter.

![](graphic/20_chapter08_fig_04.png)![](graphic/20_chapter08_fig_05.png)

In the constructor body, we first assign default values to the class properties. These values will be used when the constructor is invoked as a default constructor (without arguments), or when it is invoked with only some arguments. It is helpful to indicate the range of a property in a comment. This requires to map the platform-independent datatypes of the information design model to the corresponding implicit JavaScript datatypes according to the following table.

Table 8.1 Datatype mapping

| Platform-independent datatype | JavaScript datatype | SQL |
| String Integer Decimal Boolean Date | string number (int) number (float) boolean Date | CHAR(n) or VARCHAR(n) INTEGER REAL, DOUBLE PRECISION or DECIMAL(p,s) BOOLEAN DATE |

Since the setters may throw constraint violation errors, the constructor function, and any setter, should be called in a try-catch block where the catch clause takes care of processing errors (at least logging suitable error messages).

As in the minimal app, we add a class-level property `Book. instances` representing the collection of all `Book` instances managed by the app in the form of an entity table:

![](graphic/20_chapter08_fig_06.png)

### 8.5.3Code the property checks

Code the property check functions in the form of class-level (’static’) methods. In JavaScript, this means to define them as method slots of the constructor, as in `Book. checkIsbn` (recall that a constructor is a JS object, since in JavaScript, functions are objects, and as an object, it can have slots).

Take care that all constraints of a property as specified in the class model are properly coded in its check function. This concerns, in particular, the mandatory value and uniqueness constraints implied by the standard identifier declaration (with `{id}`), and the mandatory value constraints for all properties with multiplicity 1, which is the default when no multiplicity is shown. If any constraint is violated, an error object instantiating one of the error classes listed above in [Section 4.1](#15_chapter04.xhtml_chapter04_9) and defined in the file `errorTypes.js` is returned.

For instance, for the `checkIsbn` operation we obtain the following code:

![](graphic/20_chapter08_fig_07.png)

Notice that, since `isbn` is the standard identifier attribute of `Book`, we only check the syntactic constraints in `checkIsbn`, but we check the mandatory value and uniqueness constraints in `checkIsbnAsId`, which itself first invokes `checkIsbn`:

![](graphic/20_chapter08_fig_08.png)

We assume that all check functions and setters can deal both with proper data values (that are of the attribute’s range type) and also with string values that are supposed to represent proper data values, but have not yet been converted to the attribute’s range type. We take this approach for avoiding datatype conversions in the user interface (“view”) code. Notice that all data entered by a user in an HTML form field is of type String and must be converted (or de-serialized) before its validity can be checked and it can be assigned to the corresponding property. It is preferable to perform these type conversions in the model code, and not in the user interface code..

For instance, in our example app, we have the integer-valued attribute `year`. When the user has entered a value for this attribute in a corresponding form field, in the Create or Update user interface, the form field holds a string value. This value is passed to the `Book. add` or `Book.update` method, which invokes the `setYear` and `checkYear` methods. Only after being validated, this string value is converted to an integer and assigned to the `year` attribute.

### 8.5.4Code the property setters

Code the setter operations as (instance-level) methods. In the setter, the corresponding check function is invoked and the property is only set, if the check does not detect any constraint violation. Otherwise, the constraint violation error object returned by the check function is thrown. For instance, the `setIsbn` operation is coded in the following way:

![](graphic/20_chapter08_fig_09.png)

There are similar setters for the other properties (`title`, `year` and `edition`).

### 8.5.5Add a serialization function

It is helpful to have an object serialization function tailored to the structure of an object (as defined by its class) such that the result of serializing an object is a human-readable string representation of the object showing all relevant information items of it. By convention, these functions are called `toString()`. In the case of the `Book` class, we use the following code:

![](graphic/20_chapter08_fig_10.png)

### 8.5.6Data management operations

In addition to defining the model class in the form of a constructor function with property definitions, checks and setters, as well as a `toString()` serialization function, we also need to define the following data management operations as class-level methods of the model class:

1.  `Book.convertRec2Obj` and `Book.retrieveAll` for loading all managed Book instances from the persistent data store.
2.  `Book. saveAll` for saving all managed Book instances to the persistent data store.
3.  `Book. add` for creating a new Book instance and adding it to the collection of all Book instances.
4.  `Book. update` for updating an existing Book instance.
5.  `Book. destroy` for deleting a Book instance.
6.  `Book. createTestData` for creating a few sample book records to be used as test data.
7.  `Book. clearData` for clearing the book data store.

All of these methods essentially have the same code as in our minimal app discussed in [Part 1](#11_Part01.xhtml_Part01_1), except that now

1.  we may have to catch constraint violations in suitable try-catch blocks in the procedures `Book. convertRec2Obj`, `Book. add`, `Book.update` and `Book. createTestData`;
2.  we create more informative status and error log messages for better observing what’s going on; and
3.  we can use the `toString()` function for serializing an object in status and error messages.

Notice that for the change operations `add` (create) and `update`, we need to implement an all-or-nothing policy: whenever there is a constraint violation for a property, no new object must be created and no (partial) update of the affected object must be performed.

When a constraint violation is detected in one of the setters called when `new Book(`…`)` is invoked in `Book.add`, the object creation attempt fails, and instead a constraint violation error message is created. Otherwise, the new book object is added to `Book.instances` and a status message is created, as shown in the following program listing:

![](graphic/20_chapter08_fig_11.png)![](graphic/20_chapter08_fig_12.png)

When an object of a model class is to be updated, we first create a clone of it for being able to restore it if the update attempt fails. In the object update attempt, we only assign those properties of the object the value of which has changed, and we report this in a status log.

Normally, all properties defined by a model class, except the standard identifier attribute, can be updated. It is, however, possible to also allow updating the standard identifier attribute. This requires special care for making sure that all references to the given object via its old standard identifier are updated as well.

When a constraint violation is detected in one of the setters invoked in `Book. update`, the object update attempt fails, and instead the error message of the constraint violation object thrown by the setter and caught in the `update` method is shown, and the previous state of the object is restored. Otherwise, a status message is created, as shown in the following program listing:

![](graphic/20_chapter08_fig_13.png)

Notice that optional properties, like `edition`, need to be treated in a special way. If the user doesn’t enter any value for them in a Create or Update user interface, the form field’s value is the empty string `""`. In the case of an optional property, this means that the property is not assigned a value in the add use case, or that it is unset if it has had a value in the update use case. This is different from the case of a mandatory property, where the empty string value obtained from an empty form field may or may not be an admissible value.

If there is a constraint violation exception, an error message is written to the log and the object concerned is reset to its previous state:

![](graphic/20_chapter08_fig_14.png)

## 8.6Write the View Code

The user interface (UI) consists of a start page `index.html` that allows the user choosing one of the data management operations by navigating to the corresponding UI page such as `retrieveAndListAllBooks.html` or `createBook.html` in the app folder. The start page `index.html` has been discussed in [Section 4.2](#15_chapter04.xhtml_chapter04_13).

We render the data management menu items in the form of buttons. For simplicity, we invoke the `Book. clearData()` and `Book. createTestData()` methods directly from the buttons’ `onclick` event handler attribute. Notice, however, that it is generally preferable to register such event handling functions with `addEventListener(`…`)`, as we do in all other cases.

### 8.6.1The data management UI pages

Each data management UI page loads the same basic CSS and JavaScript files like the start page `index.html` discussed above. In addition, it loads a use-case-specific view code file `src/v/`useCase`.js` and then sets the `setupUserInterface` procedure of the use-case as an event handler for the page load event, which takes care of initializing the use case when the UI page has been loaded.

### 8.6.2Initialize the app

For initializing the app, its namespace and MVC sub-namespaces have to be defined. For our example app, the main namespace is defined to be `pl`, standing for “Public Library”, with the three sub-namespaces `m`, `v` and `c` being initially empty objects:

![](graphic/20_chapter08_fig_15.png)

`We` put this code in the file `initialize. js` in the `c` folder.

### 8.6.3Set up the user interface

For setting up the user interfaces of the data management use cases, we have to distinguish the case of “Retrieve/List All” from the other ones (Create, Update, Delete). While the latter ones require using an HTML form and attaching event handlers to form controls, in the case of “Retrieve/List All” we only have to render a table displaying all books, as in the case of the Minimal App[115](33_Notes03.xhtml_Notes03_15) discussed in [Chapter 3](#14_chapter03.xhtml_chapter03_1).

For the Create, Update and Delete use cases, we need to add event listeners for:

1.  responsive validation on form field `input` events,
2.  handling the event when the user clicks (or pushes) the save (or delete) button,
3.  making sure the main memory data is saved when a `beforeunload` event occurs, that is, when the browser window/ tab is closed.

For the use case Create, we obtain the following code (in `v/ createBook.js`)::

![](graphic/20_chapter08_fig_16.png)![](graphic/20_chapter08_fig_17.png)

Notice that for each input field we add a listener for `input` events, such that on any user input a validation check is performed because `input` events are created by user input actions such as typing. We use the predefined function `setCustomValidity` from the HTML5 form validation API for having our property check functions invoked on the current value of the form field and returning an error message in the case of a constraint violation. So, whenever the string represented by the expression `Book. checkIsbn( formEl.isbn.value).message` is empty, everything is fine. Otherwise, if it represents an error message, the browser indicates the constraint violation to the user by rendering a red outline for the form field concerned (due to our CSS rule for the `:invalid` pseudo class).

In addition to the event handlers for responsive constraint validation, we need two more event handlers:

![](graphic/20_chapter08_fig_18.png)

While the validation on user input enhances the usability of the UI by providing immediate feedback to the user, validation on form data submission is even more important for catching invalid data. Therefore, the event handler `handleSaveButton ClickEvent()` performs the property checks again with the help of `setCustomValidity`, as shown in the following program listing:

![](graphic/20_chapter08_fig_19.png)

By invoking `checkValidity()` on the form element, we make sure that the form data is only saved (by `Book. add`), if there is no constraint violation. After this `handleSaveButtonClickEvent` handler has been executed on an invalid form, the browser takes control and tests if the predefined property `validity` has an error flag for any form field. In our approach, since we use `setCustomValidity`, the `validity.customError` would be true. If this is the case, the custom constraint violation message will be displayed (in a bubble) and the `submit` event will be suppressed.

In the UI of the use case Update,which is handled in `v/ updateBook.js`,we do not have an `input`, but rather an `output` field for the standard identifier attribute `isbn`, since it is not supposed to be modifiable. Consequently, we don’t need to validate any user input for it. However, we need to set up a selection list (in the form of an HTML `select` element) allowing the user to select a learning unit in the first step, before its data can be modified. This requires to add a `change` event listener on the `select` element such that the fields of the UI can be filled with the data of the selected object.

![](graphic/20_chapter08_fig_20.png)![](graphic/20_chapter08_fig_21.png)

There is no need to set up responsive validation for the standard identifier attribute `isbn`, but for all other form fields, as shown above for the Create use case.

The logic of the `setupUserInterface` method for the Delete use case is similar. We only need to take care that the object to be deleted can be selected by providing a selection list, like in the Update use case. No validation is needed for the Delete use case.

## 8.7Run the App and Get the Code

You can run the validation app[116](33_Notes03.xhtml_Notes03_16) from our server or download the code[117](33_Notes03.xhtml_Notes03_17) as a ZIP archive file.

## 8.8Possible Variations and Extensions

### 8.8.1Adding an object-level validation function

When object-level validation (across two or more properties) is required for a model class, we can add a custom validation function `validate` to it, such that object-level validation can be performed before save by invoking `validate` on the object concerned. For instance, for expressing the constraint defined in the class model shown in [Figure 7.1](#19_chapter07.xhtml_chapter07_15), we define the following validation function:

![](graphic/20_chapter08_fig_22.png)

When a `validate` function has been defined for a model class, it can be invoked in the create and update methods. For instance,

![](graphic/20_chapter08_fig_23.png)

### 8.8.2Using implicit JS setters

Since ES5, JavaScript has its own form of setters, which are implicit and allow having the same semantics as explicit setter methods, but with the simple syntax of direct access. In addition to having the advantage of a simpler syntax, implicit JS setters are also safer than explicit setters because they decrease the likelihood of a programmer circumventing a setter by using a direct property assignment when instead a setter should be used. In other OOP languages, like Java, this is prevented by declaring properties to be ’private’. But JavaScript does not have this option.

The following code defines implicit setter and getter methods for the property

![](graphic/20_chapter08_fig_24.png)![](graphic/20_chapter08_fig_25.png)

Notice that, also in the constructor definition, the internal property `_title`, used for storing the property value, is not used for setting/getting it, but rather the virtual property `title`:

![](graphic/20_chapter08_fig_26.png)

We will start using implicit setter and getter methods, along with ES6 class definitions, in [Chapter 11](#24_chapter11.xhtml_chapter11_1).

## 8.9Points of Attention

### 8.9.1Boilerplate code

An issue with the do-it-yourself code of this example app is the boilerplate code needed

1.  per model class for the storage management methods `add`, `update`, `destroy`, etc.;
2.  per model class and property for getters, setters and validation checks.

While it is good to write this code a few times for learning app development, you don’t want to write it again and again later when you work on real projects. In Volume 2, we present an approach how to put these methods in a generic form in a meta-class, such that they can be reused in all model classes of an app.

### 8.9.2Configuring the UI for preventing invalid user input

Some of the new HTML5 input field types (like `number`, `date` or `color`) are intended to allow web browsers rendering corresponding `input` elements in the form of UI widgets (like date or color pickers) that limit the user’s input options such that only valid input is possible. In terms of usability, it’s preferable to prevent users from entering invalid data instead of allowing to enter it and only then checking its validity and reporting errors. Unfortunately, and this is quite disappointing, many browsers do, in 2017, still not have reasonable widget implementations for these HTML5 input field types yet.

## 8.10Practice Projects

For the following projects, you have to take care of

1.  adding, for every property, a check function that validates the constraints defined for the property, and a setter method that invokes the check function and is to be used for setting the value of the property,
2.  performing validation before any data is saved in the `add` and `update` methods.

in the model code of your app, while In the user interface (“view”) code you have to take care of

1.  styling the user interface with CSS rules (for instance, by integrating a CSS library such as Yahoo’s Pure CSS),
2.  validation on user input for providing immediate feedback to the user,
3.  validation on form submission for preventing the submission of invalid data.

Make sure that your pages comply with the XML syntax of HTML5 by means of XHTML5 validation[118](33_Notes03.xhtml_Notes03_18)(setting the validator field `Preset` to “HTML5 + SVG 1.1 + MathML 3.0”), and that your JavaScript code complies with our Coding Guidelines[119](33_Notes03.xhtml_Notes03_19) and its style is checked with JSHint[120](33_Notes03.xhtml_Notes03_20).

If you have any questions about how to carry out the following projects, you can ask them on our discussion forum[121](33_Notes03.xhtml_Notes03_21).

### 8.10.1Project 1 – Validate movie data

The purpose of the app to be built is managing information about movies. Like in the book data management app discussed in the tutorial, you can make the simplifying assumption that all the data can be kept in main memory. Persistent data storage is implemented with JavaScript’s Local Storage API.

The app deals with just one object type: `Movie`, as depicted in the following class diagram.

![](graphic/20_chapter08_fig_27.png)

In this model, the following constraints have been expressed:

1.  Due to the fact that the `movieId` attribute is declared to be the standard identifier of `Movie`, it is mandatory and unique.
2.  The `title` attribute is mandatory, as indicated by its multiplicity expression [1], and has a string length constraint requiring its values to have at most 120 characters.
3.  The `releaseDate` attribute has an interval constraint: it must be greater than or equal to 1895–12–28.

Notice that the `releaseDate` attribute is not mandatory, but optional, as indicated by its multiplicity expression [0..1].

In addition to the constraints described in this list, there are the implicit range constraints defined by assigning the datatype `PositiveInteger` to `movieId`, `NonEmptyString` to `title`, and `Date` to `releaseDate`. In our plain JavaScript approach, all these property constraints are coded in the model class within property-specific check functions.

You can use the following sample data for testing your app:

Table 8.2 Sample data about movies

| Movie ID | Title | Release date |
| 1 | Pulp Fiction | 1994–05–12 |
| 2 | Star Wars |  |
| 3 | Casablanca | 1943–01–23 |
| 4 | The Godfather | 1972–03–15 |

More movie data can be found on the IMDb website[122](33_Notes03.xhtml_Notes03_22).

### 8.10.2Project 2 – Validate country data

The purpose of the app to be built is managing information about countries. The app deals with just one object type: `Country`, as depicted in the following class diagram.

![](graphic/20_chapter08_fig_28.png)

In this model, the following constraints have been expressed:

1.  Due to the fact that the `name` attribute is declared to be the standard identifier of `Country`, it is mandatory and unique.
2.  The `name` attribute has a string length constraint requiring its values to have at least 3 and at most 50 characters.
3.  The `population` attribute is mandatory, as indicated by the multiplicity expression [1] appended to the attribute name.
4.  The `lifeExpectancy` attribute is also mandatory and has an interval constraint: its values must be less than or equal to 100.

Notice that the `militaryExpenditure` attribute is not mandatory, but optional, as indicated by its multiplicity expression [0..1].

In addition to the constraints described in this list, there are the implicit range constraints defined by assigning the datatypes `NonEmptyString` to `name`, `PositiveInteger` to `population`, `PositiveDecimal` to `lifeExpectancy` and `Percentage` to `militaryExpenditure` (hint: a percentage value is a decimal number between 0 and 100). In our plain JavaScript approach, all these property constraints are coded in the model class within property-specific check functions.

You can use the sample data shown in the following table for testing your app.

Table 8.3 Sample data about countries

![](graphic/20_chapter08_fig_29.png)

More data about countries can be found in the CIA World Factbook[123](33_Notes03.xhtml_Notes03_23).

## 8.11Quiz Questions

If you would like to look up the answers for the following quiz questions, you can check our discussion forum[124](33_Notes03.xhtml_Notes03_24). If you don’t find an answer in the forum, you may create a post asking for an answer to a particular question.

### 8.11.1Question 1: Validation in setter (1)

Complete the following setter code fragment:

![](graphic/20_chapter08_fig_30.png)

### 8.11.2Question 2: Validation in setter (2)

Complete the following setter code fragment:

![](graphic/20_chapter08_fig_31.png)![](graphic/20_chapter08_fig_32.png)

### 8.11.3Question 3: Methods to add in JS class model

![](graphic/20_chapter08_fig_33.png)

Consider the simple information design model shown in the class diagram.

Which of the following methods have to be added to the `Publisher` class in a corresponding JavaScript class model? Select one or many:

![](graphic/20_chapter08_fig_34.png)

Notice that an underlined method name denotes a class-level (“static”) method.

### 8.11.4Question 4: Implementing constraints

![](graphic/20_chapter08_fig_35.png)

Consider the constraints specified for the object type `Person` in the class diagram.

Which of the following JavaScript code fragments implements these constraints?

Select one:

![](graphic/20_chapter08_fig_36.png)![](graphic/20_chapter08_fig_37.png)

# 9Implementing Constraint Validation in a Java EE Web App

The minimal web app that we have discussed in [Part 1](#11_Part01.xhtml_Part01_1) has been limited to support the minimum functionality of a data management app only. For instance, it did not take care of preventing the user from entering invalid data into the app’s database. In this chapter, we show how to express integrity constraints in a Java EE entity class, and how to have constraints automatically validated on critical life cycle events of entity objects with JPA, and on form submission with JSF.

## 9.1Java Annotations for Persistent Data Management and Constraint Validation

The integrity constraints of a distributed app have to be checked both in model classes and in the underlying database, and possibly also in the UI. However, this requirement for three-fold validation should not imply having to define the same constraints three times in three different languages: in Java, in SQL and in HTML5/JavaScript. Rather, the preferred approach is to define the constraints only once, in the model classes, and then reuse these constraint definitions also in the underlying database and in the UI. Java EE apps support this goal to some degree. There are two types of constraint annotations:

1.  JPA constraint annotations, specify constraints to be used for generating the database schema (with CREATE TABLE statements) such that they are then checked by the DBMS, and not by the Java runtime environment;
2.  Bean Validation annotations specify constraints to be checked by the Java runtime environment

In this section we discuss how to use some of the predefined constraint annotations and how to define a custom constraint annotation for the `year` property of the `Book` class, since its value has an upper bound defined by an expression (’next year’).

### 9.1.1JPA constraint annotations

The JPA constraint annotations specify constraints to be used by the underlying database management system after generating the database schema, but not for Java validation. Consider the `@Id` annotation in the following definition of an entity class `Item`:

![](graphic/21_chapter09_fig_01.png)

The `@ Id` annotation of the `itemCode` attribute is mapped to a SQL primary key declaration for this attribute in the corresponding database table schema. As a consequence, the `itemCode` column of the generated `items` table must have a value in each row and these values have to be unique. However, these conditions are not checked in the Java runtime environment. JPA generates the following CREATE TABLE statement:

![](graphic/21_chapter09_fig_02.png)

Since nothing has been specified about the length of `itemCode` strings, the length is set to 255 by default. However, in our case we know that `itemCode` has a fixed length of 10, which can be enforced by using the `@Column` annotation, which has the following parameters:

–`name` allows to specify a name for the column to be used when the table is created (by default, the attribute name of the entity class is used);

–`nullable` is a boolean parameter that defines if the column allows `NULL` values (by default, it is `true`);

–`length` is a positive integer, specifying the maximum number of characters allowed for string values of that column (by default, this is 255);

–`unique` is a boolean parameter that defines if the values of the column must be unique (by default, it is `false`).

Using the `@Column` annotation, the improved Java/JPA code of the model class is:

![](graphic/21_chapter09_fig_03.png)

As a result, the generated CREATE TABLE statement now contains the additional constraints expressed for the columns `itemCode` and `quantity`:

![](graphic/21_chapter09_fig_04.png)

### 9.1.2Bean Validation annotations

In the Java EE Bean Validation[125](33_Notes03.xhtml_Notes03_25) approach, Java runtime validation can be defined in the form of bean validation annotations placed on a property, method, or class.

Table 9.1 Bean Validation annotations for properties

| Constraint Type | Annotations | Examples |
| String Length Constraints | `@Size` | `@Size( min=8, max=80) String message;` |
| Cardinality Constraints (for arrays, collections and maps) | `@Size` | `@Size( min=2, max=3) List<Member> coChairs;` |
| Mandatory Value Constraints | `@NotNull` | `@NotNull String name` |
| Range Constraints for numeric attributes | `@Digits` | `@Digits( integer=6, fraction= 2) BigDecimal price;` |
| Interval Constraints for integer-valued attributes | `@Min` and `@Max` | `@Min(5) int teamSize` |
| Interval Constraints for decimal-valued attributes | `@DecimalMin` and `@DecimalMax` | `@DecimalMax("30.00") double voltage` |
| Pattern Constraints | `@Pattern` | `@Pattern( regexp="\\b\\d{10}\ \b") String isbn;` |

In addition, there are annotations that require a date value to be in the future (`@Future`) or in the past (`@Past`).

All Bean Validation annotations have an optional `message` attribute for defining a custom error message. In the following example, we add two `@NotNull` annotations with messages, a `@Size` and a `@Min` annotation to the JPA constraint annotations. The `@NotNull` annotations constrain the `itemCode` and the `quantity` attributes to be mandatory, while the `@Min` annotation constrains the `quantity` attribute to have a minimum value of 0:

![](graphic/21_chapter09_fig_05.png)![](graphic/21_chapter09_fig_06.png)

Notice that that we need some duplicate logic in this example because the same constraints may have to be defined twice: as a JPA constraint and as a Bean Validation constraint. For instance, for a mandatory attribute like `quantity` we have both a @Column`( nullable=false)` JPA constraint annotation and a @NotNull Bean Validation annotation.

## 9.2New Issues

Compared to the Minimal App[126](33_Notes03.xhtml_Notes03_26) discussed in [Chapter 4](#15_chapter04.xhtml_chapter04_1) we have to deal with a number of new issues:

1.  In the model layer we have to take care of adding for every property the constraints that must be checked before allowing a record to be saved to the database
2.  In the user interface (view) we have to take care of form validation providing feedback to the user whenever data entered in the form is not valid.

Checking the constraints in the user interface on user input is important for providing immediate feedback to the user. Using JSF and Bean Validation requires to submit the form before the validation checks are performed. It would be preferable to define the validation checks in the model classes only and use them in the user interface before form submission, without having to duplicate the validation logic in the JSF facelets. However, at this point in time, JSF does not support this, and the validation is performed only after the form is submitted.

Using HTML5 validation attributes in the JSF facelets to enforce HTML5 validation before submitting the form requires an undesirable duplication of validation logic. The effect of such a duplication would be duplicate maintenance of the validation code, once in the model classes and once more in the user interface. In a simple application like our example app, this is doable, but in a larger application this quickly becomes a maintenance nightmare.

## 9.3Make an Entity Class Model

Using the information design model shown in [Figure 7.2](#19_chapter07.xhtml_chapter07_26) above as the starting point, we make an Entity class model with getters/ setters and corresponding Java datatypes.

![](graphic/21_chapter09_fig_07.png)

Figure 9.1 Deriving an Entity class model from an information design model

The Entity class model shown on the right hand side in [Figure 9.1](#21_chapter09.xhtml_chapter09_10) defines getters and setters for all properties and the following property constraint annotations:

1.  Using @Id and @NotNull, the `isbn` attribute is declared to be a standard identifier, implying that it is mandatory and unique.
2.  Using @Pattern(“\\b\\d{10}\\b”), the `isbn` attribute has a pattern constraint requiring its values to match the ISBN-10 format (simplified to the case of 10digit strings).
3.  Using @NotNull and @Size( max=50), the `title` attribute is mandatory and has a string length maximum constraint of at most 50 characters.
4.  Using @NotNull, @Min( 1459) and the custom annotation @UpToNextYear, the `year` attribute is mandatory and has an interval constraint, of a special form where the minimum is 1459 and the maximum is not fixed, but provided by a custom annotation implementing the calendar arithmetic function `nextYear()`.

Since there is no predefined Bean Validation annotation for checking the uniqueness of an ID value provided when creating a new entity object, we define a static method checkIsbnAsId that can be invoked in a corresponding controller method when creating a new entity object.

In addition, the entity class model defines the static CRUD data management methods retrieveAll, create, update and delete.

## 9.4Write the Model Code

The Entity class model shown on the right hand side in [Figure 9.1](#21_chapter09.xhtml_chapter09_10) can be coded step by step for getting the code of the entity classes of our Java EE web app.

### 9.4.1Type mapping

When defining the properties, we first need to map the platform-independent datatypes of the information design model to the corresponding implicit Java supported datatypes according to the following table.

Table 9.2 Datatype mapping to Java

| Platform-independent datatype | Java datatype |
| String | String |
| Integer | int, long, Integer, Long |
| Decimal | double, Double, java.math.BigDecimal |
| Boolean | boolean, Boolean |
| Date | java.util.Date |

Notice that for precise computations with decimal numbers, the special datatype java.math.BigDecimal[127](33_Notes03.xhtml_Notes03_27) is needed.

A second datatype mapping is needed for obtaining the corresponding MySQL datatypes:

Table 9.3 Datatype mapping to MySQL

| Platform-independent datatype | MySQL datatype |
| String | VARCHAR |
| Integer | INT |
| Decimal | DECIMAL |
| Boolean | BOOL |
| Date | DATETIME or TIMESTAMP |

### 9.4.2Code the constraints as annotations

In this section we add JPA constraint annotations and Bean Validation annotations for implementing the property constraints defined for the `Book` class in the Java Entity class model. For the standard identifier attribute `isbn`,we add the JPA constraint annotations `@Id` and `@Column( length=10)`, as well as the Bean Validation annotations `@NotNull` and `@Pattern( regexp="\\b\\d{10}\\b")`. Notice that, for readability, we have simplified the ISBN pattern constraint.

For the attribute `title`, we add the JPA constraint annotation `@Column( nullable=false)`, as well as the Bean Validation annotations `@NotNull` and `@Size( max=50)`.

For the attribute `year`, we add the JPA constraint annotation `@Column( nullable=false)`, as well as the Bean Validation annotations `@NotNull` and `@Min( value=1459)`. Notice that we cannot express the constraint that `year` must not be greater than next year with a standard validation annotation. Therefore, we’ll define a custom annotation for this constraint in [Section 6](#17_chapter06.xhtml_chapter06_1) below.

Coding the integrity constraints with JPA constraint annotations and Bean Validation annotations results in the following annotated bean class:

![](graphic/21_chapter09_fig_08.png)

Notice that for the `year` property, the Java `Integer` wrapper class is used instead of the primitive `int` datatype. This is required for the combined use of JSF and JPA, because if the value of an empty year input field is submitted in the create or update forms, the value which is passed to the `year` property by JSF via the `setYear` method is `null` (more details on [Section 4.5](#15_chapter04.xhtml_chapter04_39), “Requiring non-empty strings”), which is not admitted for primitive datatypes by Java.

We only provide an overview of the methods. For more details, see [Chapter 4](#15_chapter04.xhtml_chapter04_1).

### 9.4.3Checking uniqueness constraints

For avoiding duplicate `Book` records we have to check that the `isbn` values are unique. At the level of the database, this is already checked since the `isbn` column is the primary key, and the DBMS makes sure that its values are unique. However, we would like to check this in our Java app before the data is passed to the DBMS. Unfortunately, there is no predefined Bean Validation annotation for this purpose, and it is not clear how to do this with a custom validation annotation. Therefore we need to write a static method, `Book. checkIsbnAsId`, for checking if a value for the `isbn` attribute is unique. This check method can then be called by the controller for validating any `isbn` attribute value before trying to create a new `Book` record. The `Book. checkIsbnAsId` method code is shown below:

![](graphic/21_chapter09_fig_09.png)

The method throws a `UniquenessConstraintViolation` exception in case that a `Book` record was found for the given ISBN value. The exception can then be caught and a corresponding error message displayed in the UI. In the sequel of this chapter we show how to define the controller validation method and inform JSF facelets that it must be used to validate the `isbn` form input field.

Notice that in this case we also need to check the `isbn` value and reject `null` values, because the `@NotNull` validation triggers only later, when the `isbn` property of the `Book` is set, thus at this point we could get `NullPointerException`, from the `Book. retrieve` method.

### 9.4.4Dealing with model-related exceptions

The `Book.checkIsbnAsId` method discussed in the previous sub-section is designed to be used in combination with a controller so the user gets an error message when trying to duplicate a `Book` record (i. e., if the provided `isbn` value is already used in an existing record). However, if the `Book.create` method is used directly (i. e. by another piece of code, where the uniqueness constraint is not performed by calling `Book. checkIsbnAsId`), then uniqueness constraint validation may fail. Lets have a look on the `Book.create` code:

![](graphic/21_chapter09_fig_10.png)

The method may throw a number of exceptions when trying to run the persist or the commit method. One of the exceptions (i. e. `EntityExistsException`) is thrown by the `ut.commit` call. The method which calls `Book. create` may catch this exception and perform specific actions, such as rolling back the transaction. In our case, the `Book.create` is called by the `create` action method of the `BookController` class, and the action performed is to show the exception stack trace in the console, as well as calling the `ut.rollback` which takes care of cancelling any database change performed by the current transaction. The rest of the exceptions are caught by using their super class (i. e. `Exception`) and the exception stack trace is displayed in the console.

![](graphic/21_chapter09_fig_11.png)

Note: the `EntityExistsException` is part of the `javax.persistence` package (i. e. `javax.persistence.EntityExistsException`). TomEE uses the Apache OpenJPA[128](33_Notes03.xhtml_Notes03_28) implementation of the JPA API, which means that the `EntityExistsException` class (and other exceptions classes too) are part of the `org. apache.openjpa.persistence` package. Therefore, using this exception with our code, requires to `import org.apache.openjpa.persistence.EntityExistsException` instead of `import javax.persistence.EntityExistsException` as well as adding the `openjpa-xxx.jar` (located in the `lib` subfolder of the TomEE installation folder) to the Java application class path for being able to have the code compiled with Eclipse or other IDE tools.

### 9.4.5Requiring non-empty strings

Normally a mandatory string-valued attribute, such as `title`, requires a non-empty string, which is expressed in our model above by the range `NonEmptyString`. For treating empty strings as no value, the context parameter `javax. faces.INTERPRET_EMPTY_STRING_SUBMITTED_VALUES_AS_NULL` must be set to `true` in `web.xml`:

![](graphic/21_chapter09_fig_12.png)

## 9.5Write the View Code

After we have defined the constraints in the Java EE model layer and the database layer, we need to take care of validation in the user interface. In particular, we need to make sure that the user gets informed about issues by rendering visual indicators and informative validation error messages.

### 9.5.1Validation in the Create use case

The `WebContent/views/books/create.xhtml` file contains the JSF facelet code for creating a new `Book` record. We now use the JSF `validator` attribute for performing the uniqueness validation and JSF `message` elements for displaying validation error messages.

![](graphic/21_chapter09_fig_13.png)

There are only a few changes compared to the same view used for the minimal app, where no validation was performed. The first change is the new `h:message` element which is bound to a specific form element by the `for` attribute. We create such an element for each of our form input elements. Notice that we don’t have to do anything else for seeing the validation errors for all integrity constraint checks which are performed by using the (built-in and custom) Bean Validation annotations. As soon as a constraint validation fails, the message set by using the `message` property of the integrity constraint annotation (e. g. `@Pattern`, `@NotNull`, etc) is displayed in an HTML `span` element generated by JSF as a result of using the `h:message` element.

For all the integrity constraints we have used Bean Validation annotations, but for the uniqueness constraint we have used custom code, therefore no error message will be shown for it. In the view code we can see that a new attribute, `validator` in `h:inputText`, was used for the `isbn` input field. It specifies which custom method is used to perform validation of the provided value in this form field. In our case, we use the `checkIsbnAsId` method defined in the `BookController` as shown below:

![](graphic/21_chapter09_fig_14.png)![](graphic/21_chapter09_fig_15.png)

The controller’s check method throws a `ValidatorException` which is also used to deliver the error message (the third parameter of the `ValidatorException` constructor) to the corresponding JSF facelet for being displayed in the UI. Methods used as JSF validators must have a specific syntax. The first two parameters of type `FacesContext`, respectively `UIComponent` are used by the container to invoke the method with references to the right view component and context, and they can be used in more complex validation methods. The last one, of type `Object`, represents the value to be validated by the method. This value has to be casted to the expected type (to `String`, in our example). It is important to know that, if a cast to a non-compatible type is performed, the validation method fails and an exception is thrown.

### 9.5.2Validation in the Update use case

In the Update use case, the facelet file `update.xhtml` in `WebContent/views/ books` was updated so it uses the `h:message` elements for being able to display validation errors:

![](graphic/21_chapter09_fig_16.png)![](graphic/21_chapter09_fig_17.png)

Since we do not allow to change the ISBN of a book, we create an output field for the `isbn` attribute with the JSF element `h:outputText`. This implies that no validation is performed.

Using an `h:outputText` element for showing the value of an entity attribute results in an HTML `span` element. This implies that the HTTP form submission message contains no information about that attribute. If the validation fails, we expect to see the form content together with the error messages. To get the expected result, we need to use the annotation `@ViewScoped` for the entity class `pl.m.Book` instead of `@RequestScoped`, otherwise our bean instance referenced by the `book` variable is initialized with a new value on every request, implying that the expression `#{book. isbn}` evaluates to `null` and the ISBN value is not displayed. The `@ViewScoped` annotation specifies that the entity bean is alive as long as the associated view is alive, so the ISBN value stored by the `book` is available during this time and it can be displayed in the view.

By contrast, `h: inputText` elements result in HTML `input` elements which are part of the form submission content, so the response contains the already existing values because these values are known in this case. This consideration shows that it is important to choose the right bean scope.

## 9.6Defining a Custom Validation Annotation

One other integrity constraint we have to consider is about the allowed values of the `year` property, which must be in the interval [1459, nextYear()] where nextYear() is a function invocation expression. We may have the idea to use `@Min` and `@Max` to specify the interval constraint, but this is not possible because the `@Max` annotation (as well as any other annotation) does not allow expressions, but only data literals. So, while we can express the interval’s lower bound with `@Min( value=1459)`, we need another solution for expressing the upper bound.

Fortunately, the Bean Validation API allows to define custom validation annotations with custom code performing the constraint checks. This means that we are free to express any kind of validation logic in this way. Creating and using a custom validation annotation requires the following steps:

1.Create the annotation interface `UpToNextYear` with the following code:

![](graphic/21_chapter09_fig_18.png)

![](graphic/21_chapter09_fig_19.png)

The interface needs to define three methods, `message` (returns the default key or error message if the constraint is violated), `groups` (allows the specification of validation groups, to which this constraint belongs) and `payload` (used by clients of the Bean Validation API to assign custom payload objects to a constraint – this attribute is not used by the API itself). Notice the `@Target` annotation, which defines the element types that can be annotated (fields/properties and methods in our case). The `@Constraint` annotation allows to specify the implementation class that will perform the validation, i. e. `UpToNextYearImpl` in our case.

2.Create an implementation class with the validation code:

![](graphic/21_chapter09_fig_20.png)

The implementation class implements the `ConstraintValidator` interface, which requires two type parameters: the annotation interface defined before (i. e. `UpToNextYear`), and the type of elements the validator can handle (i. e. `Integer`, so implicitly also the compatible primitive type `int`). The `initialize` method allows initializing variables required for performing the validation check. The `isValid` method is responsible for performing the validation: it must return `true` if the validation succeeds and `(wie "true")` otherwise. The first parameter of the `isValid` method represents the value to be validated and its type must be compatible with the type defined by the second type parameter of the `ConstraintValidator` (`Integer` in our case).

3.Annotate the property or method concerned:

![](graphic/21_chapter09_fig_21.png)

## 9.7Run the App and Get the Code

You can run the validation app[129](33_Notes03.xhtml_Notes03_29) on our server or download the code[130](33_Notes03.xhtml_Notes03_30) as a ZIP archive file.

Follow our instructions[131](33_Notes03.xhtml_Notes03_31) for getting your environment prepared for running Java EE web applications.

## 9.8Possible Variations and Extensions

### 9.8.1Object-level constraint validation

As an example of a constraint that is not bound to a specific property, but must be checked by inspecting several properties of an object, we consider the validation of the attribute `Author::dateOfDeath`. First, any value for this attribute must be in the past, which can be specified with the `@Past` Bean Validation annotation, and second, any value of `dateOfDeath` must be after the `dateOfBirth` value of the object concerned. This object-level constraint cannot be expressed with a predefined Bean Validation annotation. We can express it with the help of a custom class-level annotation, like the following `AuthorValidator` annotation interface:

![](graphic/21_chapter09_fig_22.png)

Compared to a property constraint annotation definition, there is only one difference, the parameter of the `@Target` annotation. While in the case of a property and method level custom constraint annotation the values are `ElementType.FIELD` and `ElementType.METHOD`, for the case of a class it must be `ElementType.TYPE`.

The corresponding implementation class, i. e., `AuthorValidatorImpl`, has the same structure as in the case of a property constraint annotation , but now, we can access all properties of an entity bean, so we can compare two or more properties when required. In our case, we have to compare the values of `dateOfBirth` and `dateOfDeath` in the `isValid` method:

![](graphic/21_chapter09_fig_23.png)

Using class-level JPA validators in facelets requires a bit of tweaking because they are not directly supported by JSF. For the specific form field to be validated, we have to specify a controller method in charge of the validation, as the value of the `@validator` attribute:

![](graphic/21_chapter09_fig_24.png)![](graphic/21_chapter09_fig_25.png)

The controller method `checkDateOfDeath` has to invoke the Bean Validation API validator, catch the validation exceptions and translate them to exceptions of type `javax.faces.validator.ValidatorException`, which are then managed by JSF and displayed in the view. Its code is as follows:

![](graphic/21_chapter09_fig_26.png)![](graphic/21_chapter09_fig_27.png)

While the method looks complicated, it is responsible for the following simple tasks:

–get access to form data and extract the user input values with the help of the `context.getViewRoot().findComponent` method. Notice that the component name has the pattern: `formName:formElementName`.

–create the Author instance and set the corresponding data as extracted from the form, by using the `FacesContext` instance provided by the JSF specific validator method

–manually invoke the Bean Validation API validator by using the javax.validation.Validator class.

–loop trough the validator exception, select the ones which corresponds to the custom validated field and map them to `javax.faces.validator.ValidatorException` exceptions. The selection can be made by looking for specific data in the exception message.

As a result, the custom Bean Validation class validator is not used, and the facelet is able to render the corresponding error messages when the validation fails, in the same way as is possible for single property validation situations.

### 9.8.2JSF custom validators

An alternative approach to object-level validation is to using JSF custom validators. They have the advantage that they are directly supported in facelets, but the downside of this approach is that it violates the onion architecture principle by defining business rules in the UI instead of defining them in the model.

For our example, the validator for the Author class that is responsible for validating `dateOfDeath` by comparing it with `dateOfBirth` is shown below:

![](graphic/21_chapter09_fig_28.png)![](graphic/21_chapter09_fig_29.png)

Then, in the facelet, for the corresponding field, the validator has to be specified:

![](graphic/21_chapter09_fig_30.png)

## 9.9Practice Projects

### 9.9.1Project 1 – Validate movie data

The purpose of the app to be built is managing information about movies. The app deals with just one object type: `Movie`, as depicted in the following class diagram.

![](graphic/21_chapter09_fig_31.png)

In this model, the following constraints have been expressed:

1.  Due to the fact that the `movieId` attribute is declared to be the standard identifier of `Movie`, it is mandatory and unique.
2.  The `title` attribute is mandatory, as indicated by its multiplicity expression [1], and has a string length constraint requiring its values to have at most 120 characters.
3.  The `releaseDate` attribute has an interval constraint: it must be greater than or equal to 1895-12-28.

Notice that the `releaseDate` attribute is not mandatory, but optional, as indicated by its multiplicity expression [0..1]. In addition to the constraints described in this list, there are the implicit range constraints defined by assigning the datatype `PositiveInteger` to `movieId`, `NonEmptyString` to `title`, and `Date` to `releaseDate`.

You can use the sample data shown in [Table 8.2](#20_chapter08.xhtml_chapter08_38) for testing your app.

### 9.9.2Project 2 – Validate country data

The purpose of the app to be built is managing information about countries. The app deals with just one object type: `Country`, as depicted in the following class diagram.

![](graphic/21_chapter09_fig_32.png)

In this model, the following constraints have been expressed:

1.  Due to the fact that the `name` attribute is declared to be the standard identifier of `Country`, it is mandatory and unique.
2.  The `name` attribute has a string length constraint requiring its values to have at least 3 and at most 50 characters.
3.  The `population` attribute is mandatory, as indicated by the multiplicity expression [1] appended to the attribute name.
4.  The `lifeExpectancy` attribute is also mandatory and has an interval constraint: its values must be less than or equal to 100.

Notice that the `militaryExpenditure` attribute is not mandatory, but optional, as indicated by its multiplicity expression [0..1].

In addition to the constraints described in this list, there are the implicit range constraints defined by assigning the datatypes `NonEmptyString` to `name`, `PositiveInteger` to `population`, `PositiveDecimal` to `lifeExpectancy` and `Percentage` to `militaryExpenditure` (hint: a percentage value is a decimal number between 0 and 100). In our Java example app, such property constraints were coded in the entity class by using the Bean Validation API.

You can use the sample data shown in [Table 8.3](#20_chapter08.xhtml_chapter08_41) for testing your app.

## 9.10Quiz Questions

If you would like to look up the answers for the following quiz questions, you can check our discussion forum[132](33_Notes03.xhtml_Notes03_32). If you don’t find an answer in the forum, you may create a post asking for an answer to a particular question.

### 9.10.1Question 1: String length validation

Complete the following code, with the correct Java Bean validation annotation, so that the attribute `title` has a minimum length of 2 and a maximum length of 40:

![](graphic/21_chapter09_fig_33.png)

### 9.10.2Question 2: Requiring a value

Which validation annotations are needed for requiring a (not-null) value for an attribute both in the Java EE model layer and in the database of an app?

![](graphic/21_chapter09_fig_34.png)

### 9.10.3Question 3: Defining a custom validation annotation

Complete the following code for defining a `LessThan100YearsOld` annotation that checks if a given `Date` attribute value does not date back more than 100 years and the Java implementation class is LessThan100YearsOldImpl:

![](graphic/21_chapter09_fig_35.png)![](graphic/21_chapter09_fig_36.png)

### 9.10.4Question 4: JSF custom validator method

Complete the following JSF snippet such that the `title` attribute of the `Book` entity is validated by the custom method `Book::checkTitle`:

![](graphic/21_chapter09_fig_37.png)

### 9.10.5Question 5: Show validation error messages with JSF

Complete the following JSF snippet, such that any (possible) error messages resulting from validating the `title` attribute value of the `book` entity, are displayed in the user interface:

![](graphic/21_chapter09_fig_38.png)

![](graphic/11_Part01_fig_01.png)

# Part IIIEnumerations

In virtually any app, we need to deal with attributes having a fixed set of possible values representing names. These attributes are called enumeration attributes , and their fixed value sets are called enumerations.

# 10Enumerations and Enumeration Attributes

## 10.1Enumerations

In all application domains, there are string-valued attributes with a fixed list of possible string values. These attributes are called enumeration attributes, and the fixed value lists defining their possible string values are called enumerations. For instance, when we have to manage data about people, we often need to include information about their gender. The possible values of a `gender` attribute may be restricted to one of the enumeration labels “male”,”female” and “undetermined”, or to one of the enumeration codes “M”, “F” and “U”. Whenever we deal with codes, we also need to have their corresponding labels, at least in a legend explaining the meaning of each code.

Instead of using the enumeration string values as the internal values of an enumeration attribute, it is preferable to use a simplified internal representation for them, such as the positive integers 1, 2, 3, etc., which enumerate the possible values. However, since these integers do not reveal their meaning (which is indicated by the enumeration label) in program code, for readability we rather use special constants, called enumeration literals, such as `MALE` or `M`, prefixed by the name of the enumeration like in `this.gender = GenderEL.MALE`. Notice that we follow the convention that the names of enumeration literals are written all upper case, and that we also use the convention to suffix the name of an enumeration datatype with “EL” standing for “enumeration literal” (such that we can recognize from the name `GenderEL` that each instance of this datatype is a “gender enumeration literal”).

There are also enumerations having records as their instances, such that one of the record fields provides the name of the enumeration literals. An example of such an enumeration is the following list of units of measurement:

Table 10.1 Representing an enumeration of records as a table

| Unit Symbol | Units of Measurement Unit Name | Dimension |
| m | meter | length |
| kg | kilogram | mass |
| g | gram | mass |
| s | second | time |
| ms | milisecond | time |

Notice that since both the “Unit Symbol” and the “Unit Name” fields are unique, either of them could be used for the name of the enumeration literals.

In summary, we can distinguish between the following three forms of enumerations:

1.  simple enumerations define a list of self-explanatory enumeration labels;
2.  code lists define a list of code/label pairs.
3.  record enumerations consist of a list of records, so they are defined like classes with simple attributes defining the record fields.

These three forms of enumerations are discussed in more detail below.

Notice that, since enumerations are used as the range of enumeration attributes, they are considered to be datatypes.

Enumerations may have further features. For instance, we may want to be able to define a new enumeration by extending an existing enumeration. In programming languages and in other computational languages, enumerations are implemented with different features in different ways. See also the Wikipedia article on enumerations[133](33_Notes03.xhtml_Notes03_33).

### 10.1.1Simple enumerations

A simple enumeration defines a fixed list of self-explanatory enumeration labels, like in the example of a `GenderEL` enumeration shown in the following UML class diagram:

![](graphic/23_chapter10_fig_01.png)

Since the labels of a simple enumeration are being used, in capitalized form, as the names of the corresponding enumeration literals (`GenderEL.MALE`, `GenderEL. FEMALE`, etc.), we may also list the (all upper case) enumeration literals in the UML enumeration datatype, instead of the corresponding (lower or mixed case) enumeration labels.

### 10.1.2Code lists

A code list is an enumeration that defines a fixed list of code/label pairs. Unfortunately, the UML concept of an enumeration datatype does not support the distinction between codes as enumeration literals and their labels. For defining both codes and labels in a UML class diagram in the form of an enumeration datatype, we may use the attribute compartment of the data type rectangle and use the codes as attribute names defining the enumeration literals, and set their initial values to the corresponding label. This approach results in a visual representation as in the following diagram:

![](graphic/23_chapter10_fig_02.png)

In the case of a code list, we can use both the codes or the labels as the names of enumeration literals, but using the codes seems preferable for brevity (`GenderEL.M`, `GenderEL.F`, etc.). For displaying the value of an enumeration attribute, it’s an option to show not only the label, but also the code, like “male (M)”, provided that there is sufficient space. If space is an issue, only the code can be shown.

### 10.1.3Record enumerations

A record enumeration defines a record type with a unique field designated to provide the enumeration literals, and a fixed list of records of that type. In general, a record type is defined by a set of field definitions (in the form of primitive datatype attributes), such that one of the unique fields is defined to be the enumeration literal field, and a set of operation definitions.

Unfortunately, record enumerations, as the most general form of an enumeration datatype, are not supported by the current version of UML (2.5) where the general form of an enumeration is defined as a special kind of datatype (with optional field and operation definitions) having an additional list of unique strings as enumeration literals (shown in a fourth compartment). The UML definition does neither allow designating one of the unique fields as the enumeration literal field, nor does it allow populating an enumeration with records.

Consequently, for showing a record enumeration in a UML class diagram, we need to find a workaround. For instance, if our modeling tool allows adding a drawing, we could draw a rectangle with four compartments, such that the first three of them correspond to the name, properties and operations compartments of a datatype rectangle, and the fourth one is a table with the names of properties/fields defined in the second compartment as column headers, as shown in the following figure:

|  | UnitEL |  |
| «el» unitSymbol: String |  |
| unitName: String |  |  |
| dimension: String |  |  |
| Unit Symbol | Unit Name | Dimension |
| m | meter | length |
| kg | kilogram | mass |
| g | gram | mass |
| s | second | time |
| ms | millisecond | time |

### 10.1.4Extensible enumerations

There may be cases of enumerations that need to be extensible, that is, it must be possible to extend their list of enumeration values (labels or code/label pairs) by adding a new one. This can be expressed in a class diagram by appending an ellipsis to the list of enumeration values, as shown in [Figure 10.1](#23_chapter10.xhtml_chapter10_7).

![](graphic/23_chapter10_fig_03.png)

Figure 10.1 An example of an extensible enumeration

Since enumeration values are internally represented by enumeration literals, which are normally stored as plain positive integers in a database, a new enumeration value can only be added at the end of the value list such that it can be assigned a new index integer without re-assigning the indexes of other enumeration values. Otherwise, the mapping of enumeration indexes to corresponding enumeration values would not be preserved.

Alternatively, if new enumeration values have to be inserted in-between other enumeration values, and their indexes re-assigned, this implies that

1.  enumeration indexes are plain sequence numbers and do no longer identify an enumeration value;
2.  the value of an enumeration literal can no longer be an enumeration index, but rather has to be an identifying string: preferably the enumeration code in the case of a code list, or the enumeration label, otherwise.

## 10.2Enumeration Attributes

An enumeration attribute is an attribute that has an enumeration as its range.

In the user interface, an output field for an enumeration attribute would display the enumeration label, rather than its internal value, the corresponding enumeration index.

For allowing user input to an enumeration attribute, we can use the UI concept of a (drop-down) selection list, which may be implemented with an HTML `select` element, such that the enumeration labels would be used as the text content of its `option` elements, while the enumeration indexes would be used as their values. We have to distinguish between single-valued and multi-valued enumeration attributes. In the case of a single-valued enumeration attribute, we use a standard `select` element. In the case of a multi-valued enumeration attribute, we use a `select` element with the HTML attribute setting `multiple="multiple"`.

In the case of using a single `select` element for an optional enumeration attribute, we need to include in its options an element like “—” for indicating that nothing has been selected. Then, the UI page for the CRUD use case “Create” shows “—” as the initially selected option.

For usability, the multiple selection list can only be implemented with an HTML `select` element, if the number of enumeration literals does not exceed a certain threshold (like 20), which depends on the number of options the user can see on the screen without scrolling.

For user input for a single-valued enumeration attribute, a radio button group can be used instead of a single selection list, if the number of enumeration literals is sufficiently small (say, not larger than 7). A radio button group is implemented with an HTML `fieldset` element acting as a container of labeled `input` elements of type “radio”, all having the same name, which is normally equal to the name of the represented enumeration attribute.

For user input for a multi-valued enumeration attribute, a checkbox group can be used instead of a multiple selection list, if the number of enumeration literals is sufficiently small (say, not larger than 7). A checkbox group is implemented with an HTML `fieldset` element acting as a container of labeled `input` elements of type “checkbox”, all having the same name, which is normally equal to the name of the represented enumeration attribute.

## 10.3Enumerations in Computational Languages

Defining enumerations is directly supported in information modeling languages (such as in UML Class Diagrams), in data schema languages (such as in XML Schema, but not in SQL), and in many programming languages (such as in C++ and Java, but not in JavaScript).

### 10.3.1Enumerations in SQL

Unfortunately, standard SQL does not support enumerations. Some DBMS, such as MySQL and Postgres, provide their own extensions of SQL column definitions in the CREATE TABLE statement allowing to define enumeration-valued columns.

A MySQL enumeration[134](33_Notes03.xhtml_Notes03_34) is specified as a list of enumeration labels with the keyword `ENUM` within a column definition, like so:

![](graphic/23_chapter10_fig_04.png)

A Postgres enumeration[135](33_Notes03.xhtml_Notes03_35) is specified as a special user-defined type that can be used in columns definitions:

![](graphic/23_chapter10_fig_05.png)

### 10.3.2Enumerations in XML Schema

In XML Schema, an enumeration datatype can be defined as a simple type restricting the primitive type `xs:string` in the following way:

![](graphic/23_chapter10_fig_06.png)![](graphic/23_chapter10_fig_07.png)

### 10.3.3Enumerations in JavaScript

In JavaScript, we can define an enumeration as a special JS object having a property for each enumeration literal such that the property’s name is the enumeration literal’s name (the enumeration label or code in upper case) and its value is the corresponding enumeration index. One approach for implementing this is using the `Object.defineProperties` method:

![](graphic/23_chapter10_fig_08.png)

This definition allows using the enumeration literals `BookCategoryEL.NOVEL`, `BookCategoryEL.BIOGRAPHY` etc., standing for the enumeration indexes 1, 2 , 3 and 4, in program statements. Notice how this definition takes care of the requirement that enumeration literals like `BookCategoryEL.NOVEL` are constants, the value of which cannot be changed during program execution. This is achieved with the help of the property descriptor `writable: false` in the `Object.defineProperties` statement.

We can also use a more generic approach and define a meta-class `Enumeration` for creating enumerations in the form of special JS objects:

![](graphic/23_chapter10_fig_09.png)

Using this `Enumeration` class allows to define a new enumeration in the following way:

![](graphic/23_chapter10_fig_10.png)

Having an enumeration like `BookCategoryEL`, we can then check if an enumeration attribute like `category` has an admissible value by testing if its value is not smaller than 1 and not greater than `BookCategoryEL.MAX`. Also, the label can be retrieved in the following way:

![](graphic/23_chapter10_fig_11.png)

As an example, we consider the following model class `Book` with the enumeration attribute `category`:

![](graphic/23_chapter10_fig_12.png)

For validating input values for the enumeration attribute `category`, we can use the following check function:

![](graphic/23_chapter10_fig_13.png)

Notice how the range constraint defined by the enumeration `BookCategoryEL` is checked: it is tested if the input value `c` is a positive integer and if it is not greater than `BookCategoryEL.MAX`.

## 10.4Dealing with Enumeration Attributes in a Design Model

We again consider the simple data management problem that we have considered before. So, again, the purpose of our app is to manage information about books. But now we have four additional enumeration attributes, as shown in the UML class diagram in [Figure 10.2](#23_chapter10.xhtml_chapter10_16) below:

1.  the single-valued mandatory attribute `originalLanguage` with the enumeration datatype `LanguageEL` as its range,
2.  the multi-valued optional attribute `otherAvailableLanguages` with range `LanguageEL`,
3.  the single-valued mandatory attribute `category` with range `BookCategoryEL`
4.  the multi-valued mandatory attribute `publicationForms` with range `PublicationFormEL`

![](graphic/23_chapter10_fig_14.png)

Figure 10.2 An information design model for the object type `Book`

Notice that the attributes `otherAvailableLanguages` and `publicationForms` are multivalued, as indicated by their multiplicity expressions [*] and [1..*]. This means that the possible values of these attributes are sets of enumeration literals, such as the set {ePub, PDF}, which can be represented in JavaScript as a corresponding array list of enumeration literals, `[PublicationFormEL.EPUB, PublicationFormEL.PDF]`.

The meaning of the design model and its enumeration attributes can be illustrated by a sample data population:

Table 10.2 Sample data for `Book`

![](graphic/23_chapter10_fig_15.png)

## 10.5Quiz Questions

If you would like to look up the answers to the following quiz questions, you can check our discussion forum[136](33_Notes03.xhtml_Notes03_36). If you don’t find an answer in the forum, you may create a post asking for an answer to a particular question.

### 10.5.1Question 1: Languages Supporting Enumerations

Which of the following languages directly support enumerations by providing a special construct for defining them? Select one or many:

☐ Java ☐ JavaScript ☐ UML Class Diagrams ☐ C++ ☐ XML Schema ☐ SQL

### 10.5.2Question 2: UI Widget for Single-Valued Enum Attribute

Which of the following (combinations of) HTML elements can be used as a form control (or UI widget) for a single-valued enumeration attribute? Select one or many:

☐a `fieldset` element containing a number of `radio` elements having the same name

☐a `fieldset` element containing a number of `checkbox` elements having the same name

☐a `select` element

☐a `checkbox` element

☐a `radio` element

### 10.5.3Question 3: UI Widget for Multi-Valued Enum Attribute

Which of the following (combinations of) HTML elements can be used as a form control (or UI widget) for a multi-valued enumeration attribute? Select one or many:

☐a `select` element with the attribute setting `multiple="multiple"`

☐a `fieldset` element containing a number of `radio` elements having the same name

☐a `fieldset` element containing a number of `checkbox` elements having the same name

☐a `checkbox` element

☐a `radio` element

# 11Implementing Enumeration Attributes in a Plain JS Web App

In this chapter, we show how to build a front-end web application with enumeration attributes, using plain JavaScript. In addition to the topic of enumeration attributes, we also show how to deal with multi-valued attributes because in many cases, enumeration attributes are multi-valued.

## 11.1New Issues

Compared to the Validation App[137](33_Notes03.xhtml_Notes03_37) discussed in [Part 2](#18_Part02.xhtml_Part02_1), we now deal with the following new issues:

1.  We replace the ES5 constructor-based class definition of our model class `Book` with a corresponding ES6 `class` definition.
2.  Instead of defining explicit setters we now make use of the ES5 feature of defining implicit `get`/`set` methods for properties.
3.  Enumeration datatypes have to be defined in a suitable way as part of the model code.
4.  Enumeration attributes have to be defined in model classes and handled in the user interface with the help of suitable choice widgets.

In terms of coding, the new issues are:

1.In the model code we now have to take care of

a.defining an ES6 `class` instead of a constructor function (with additional method slots of its `prototype` object) for `Book`;

b.defining `get`/`set` methods for all properties of the `Book` class definition;

c.defining the enumerations with the help of a utility (meta‐)class `Enumeration`, which is discussed below;

d.defining the single-valued enumeration attributes `originalLanguage` and `category` together with their check functions `checkOriginalLanguage` and `checkCategory`;

e.defining the multi-valued enumeration attributes `otherAvailableLanguages` and `publicationForms` together with their checks `checkOtherAvailableLanguages` and `checkPublicationForms`;

f.extending the methods `Book.update`, and `Book.prototype.toString` such that they take care of the added enumeration attributes.

2\. In the user interface (“view”) code we have to take care of

a.adding new table columns in `retrieveAndListAllBooks.html` and suitable choice widgets in `createBook.html` and `upateBook.html`;

b.creating output for the new attributes in the `setupUserInterface()` method of `pl.v.retrieveAndListAllBooks`;

c.allowing input for the new attributes in the `setupUserInterface()` methods of `pl.v.createBook` and `pl.v.updateBook`.

## 11.2Make a JavaScript Class Model

Using the information design model shown in [Figure 10.2](#23_chapter10.xhtml_chapter10_16) above as the starting point, we make a JavaScript class model, essentially by decorating attributes with a “get/ set” stereotype (implying that they have implicit getters and setters), and by adding (class-level) check methods:

![](graphic/24_chapter11_fig_01.png)

Figure 11.1 A JavaScript class model for the object type `Book`

Notice that, for any multi-valued enumeration attribute (like `someThings`) we add a class-level check function for single values (like `checkSomeThing`) and another one for value sets (like `checkSomeThings`) both returning an object of type `ConstraintViolation`.

The implicit getters and setters implied by the “get/set” stereotype are a special feature of ES5, allowing to define methods for getting and setting the value of a property p while keeping the simple syntax of getting its value with “… = p” and setting it with “p = …”. They require to define another, internal, property (like _p) for storing the value of p because the name “p” does not refer to a normal property, but rather to a pair of get/set methods.

The most common reason for using implicit getters and setters is the need to always check constraints before setting a property. This is also the reason why we will use them.

## 11.3Add the Library File Enumeration. js

The folder structure of our enumeration app extends the structure of the validation app by adding the file `Enumeration. js` in the `lib` folder. Thus, we get the following folder structure with four files in the `lib` folder:

![](graphic/24_chapter11_fig_02.png)

In the `Enumeration. js` file, discussed in the next section, we define a meta-class `Enumeration` for creating enumerations as instances of this meta-class with the help of statements like `GenderEL = new Enumeration(["male", "female", "undetermined"])`.

## 11.4The Meta-Class Enumeration

We define an `Enumeration` meta-class, which supports both simple enumerations and code lists (but not record enumerations). While a simple enumeration is defined by a list of labels in the form of a JS array as the constructor argument such that the labels are used for the names of the enumeration literals, a code list is defined as a special kind of key-value map in the form of a JS object as the constructor argument such that the codes are used for the names of the enumeration literals. Consequently, the constructor needs to test if the invocation argument is a JS array or not. The following first part of the code shows how simple enumerations are created:

![](graphic/24_chapter11_fig_03.png)![](graphic/24_chapter11_fig_04.png)

After setting the `MAX` property of the newly created enumeration, the enumeration literals are created in a loop as further properties of the newly created enumeration such that the property name is the normalized label string and the value is the index, or sequence number, starting with 1\. Notice that a label string like “text book” or “text-book” is normalized to the enumeration literal name “TEXT_BOOK”, following a widely used convention for constant names. Finally, by invoking `Object.freeze` on the newly created enumeration, all its properties become ’unwritable’ (or read-only).

The following second part of the code shows how code list enumerations are created:

![](graphic/24_chapter11_fig_05.png)![](graphic/24_chapter11_fig_06.png)

Notice that the code list labels in `this.labels` are extended by appending their codes in parenthesis.

## 11.5Write the Model Code

### 11.5.1Code the enumerations

Enumerations are coded in the following way with the help of the meta-class `Enumeration`:

![](graphic/24_chapter11_fig_07.png)

Notice that `LanguageEL` defines a code list enumeration, while `PublicationFormEL` defines a simple enumeration.

### 11.5.2Code the model class as an ES6 class

We want to check if a new property value satisfies all constraints of a property whenever the value of a property is set. A best practice approach for making sure that new values are validated before assigned is to use a setter method for assigning a property, and invoke the check in the setter. We can either define an explicit setter method (like `setIsbn`) for a property (like `isbn`), or we can use JavaScript’s implicit getters and setters in combination with an internal property name (like `_isbn`). We have used explicit setters in the validation app. Now, in the `Book` class definition for the enumeration app, we use JavaScript’s implicit getters and setters because they offer a more user-friendly syntax and can be conveniently defined in an ES6 class definition.

The class `Book` is coded in the form of an ES6 class such that all its properties are defined with an internal property name format (prefixed with _) and assigned with values from corresponding key-value slots of a `slots` parameter in the constructor:

![](graphic/24_chapter11_fig_08.png)

### 11.5.3Code the implicit getters and setters

For each property, we define implicit getters and setters using the predefined JS keywords `get` and `set`:

![](graphic/24_chapter11_fig_09.png)

Notice that the implicit getters and setters access the corresponding internal property, like `_isbn`. This approach is based on the assumption that this internal property is normally not accessed directly, but only via its getter or setter. Since we can normally assume that developers comply with this rule (and that there is no malicious developer in the team), this approach is normally safe enough. However, there is also a proposal to increase the safety (for avoiding direct access) by generating random names for the internal properties with the help of ES6 `Symbol`s.

### 11.5.4Code the enumeration attribute checks

Code the enumeration attribute checks in the form of class-level (’static’) functions that check if the argument is a valid enumeration index not smaller than 1 and not greater than the enumeration’s MAX value. For instance, for the `checkOriginalLanguage` function we obtain the following code:

![](graphic/24_chapter11_fig_10.png)

For a multi-valued enumeration attribute, such as `publicationForms`, we break down the validation code into two check functions, one for checking if a value is a valid enumeration index (`checkPublicationForm`), and another one for checking if all members of a set of values are valid enumeration indexes (`checkPublicationForms`). The first check is coded as follows:

![](graphic/24_chapter11_fig_11.png)![](graphic/24_chapter11_fig_12.png)

The second check first tests if the argument is a non-empty array (representing a collection with at least one element) and then checks all elements of the array in a loop:

![](graphic/24_chapter11_fig_13.png)

### 11.5.5Write a serialization function

The object serialization function `toString()` now needs to include the values of enumeration attributes:

![](graphic/24_chapter11_fig_14.png)

Notice that for multi-valued enumeration attributes we call the `toString()` function that is predefined for JS arrays.

### 11.5.6Data management operations

There are only two new issues in the data management operations compared to the validation app:

1.We have to make sure that the `util.cloneObject` method, which is used in `Book. update`, takes care of copying array-valued attributes, which we didn’t have before (in the validation app).

In the `Book.update` method we now have to check if the values of array-valued attributes have changed, which requires to test if two arrays are equal or not. For code readability, we add an array equality test method to `Array.prototype` in `browserShims.js`, like so:

![](graphic/24_chapter11_fig_15.png)

### 11.5.7Creating test data

In the test data records that are created by `Book. createTestData()`, we now have to provide values for single- and multi-valued enumeration attributes. For readability, we use enumeration literals instead of enumeration indexes:

![](graphic/24_chapter11_fig_16.png)

## 11.6Write the View Code

The example app’s user interface for creating a new book record looks as in [Figure 11.2](#24_chapter11.xhtml_chapter11_17) below.

![](graphic/24_chapter11_fig_17.png)

Figure 11.2 The UI for creating a new book record with enumeration attributes

Notice that the UI contains four choice widgets:

1.  a single selection list for the attribute `originalLanguage`,
2.  a multiple selection list for the attribute `otherAvailableLanguages`,
3.  a radio button group for the attribute `category`, and
4.  a checkbox group for the attribute `publicationForms`.

### 11.6.1Selection lists

We use HTML selection lists for rendering the enumeration attributes `originalLanguage` and `otherAvailableLanguages` in the HTML forms in `createBook.html` and `upateBook.html`. Since the attribute `otherAvailableLanguages` is multi-valued, we need a multiple selection list for it, as shown in the following HTML code:

![](graphic/24_chapter11_fig_18.png)![](graphic/24_chapter11_fig_19.png)

While we define the `select` container elements for these selection lists in the HTML code of `createBook.html` and `upateBook.html`, we fill in their `option` child elements dynamically in the `setupUserInterface` methods in `v/createBook.js` and `v/updateBook.js` with the help of the utility method `util.fillSelectWithOptions`.

In the case of a single `select` element, the user’s single-valued selection can be retrieved from the `value` attribute of the `select` element, while in the case of a multiple `select` element, the user’s multi-valued selection can be retrieved from the `selectedOptions` attribute of the `select` element.

Notice that the `div` element containing the multiple selection list for `otherAvailableLanguages` has the `class` value “multi-sel”, which is used for defining specific CSS rules that adjust the element’s size.

### 11.6.2Radio button and checkbox groups

Since the enumeration attributes `category` and `publicationForms` do not have more than seven possible values, we can use a radio button group and a checkbox group for rendering them in an HTML-form-based UI. These choice widgets are formed with the help of the container element `fieldset` and its child element `legend` as shown in the following HTML fragment:

![](graphic/24_chapter11_fig_20.png)

Notice that we use a custom attribute `data-bind` for indicating to which attribute of the underlying model class the choice widget is bound.

In the same way as the `option` child elements of a selection list, also the `label`ed `input` child elements of a choice widget are created dynamically with the help of the utility method `util.createChoiceWidget` in the `setupUserInterface` methods in `v/createBook.js` and `v/updateBook.js`.

![](graphic/24_chapter11_fig_21.png)

Notice that like a selection list implemented with the HTML `select` element that provides the user’s selection in the `value` or `selectedOptions` attribute, our choice widgets also need a DOM attribute that holds the user’s single- or multi-valued choice. We dynamically add a custom attribute `data-value` to the choice widget’s `fieldset` element for this purpose in `util.createChoiceWidget`.

### 11.6.3Responsive validation for choice widgets

Since choice widgets do not allow arbitrary user input, we do not have to check constraints such as range constraints or pattern constraints on user input, but only mandatory value constraints. This allows simplifying responsive validation in the UI.

In our example app, the enumeration attributes `originalLanguage`, `category` and `publicationForms` are mandatory, while `otherAvailableLanguages` is optional.

In the case of a mandatory single-valued enumeration attribute like `originalLanguage` rendered as a single selection list, we can enforce a choice, and thus the mandatory value constraint, by not offering an empty or void option among the `option` sub-elements of the `select` element. If the attribute is rendered as a radio button group, we can enforce a choice, and thus the mandatory value constraint, in the create use case by initially setting the `checked` attribute of the first radio button to `true` and not allowing the user to directly uncheck a button. In this way, if the user doesn’t check any button, the first one is the default choice.

In the case of an optional single-valued enumeration attribute rendered as a single-selection list, we need to include an empty or void option (e. g., in the form of a string like “—”). If the attribute is rendered as a radio button group, we do not check any button initially and we need to allow the user to directly uncheck a button with a mouse click in a `click` event listener.

In the case of a mandatory multi-valued enumeration attribute like `publicationForms` rendered as a multiple-selection list or checkbox group, we need to check if the user has chosen at least one option. Whenever the user selects or unselects an option in a `select` element, a `change` event is raised by the browser, so we can implement the responsive mandatory value constraint validation as an event listener for `change` events on the `select` element, by testing if the list of `selectedOptions` is empty. If the attribute is rendered as a checkbox group, we need an event listener for `click` events added on the `fieldset` element and testing if the widget’s value set is non-empty, as shown in the following example code fragment:

![](graphic/24_chapter11_fig_22.png)

Notice that the HTML5 constraint validation API does not allow to indicate a constraint violation on a `fieldset` element (as the container element of a choice widget). As a workaround, we use the first checkbox element of the `publicationForms` choice widget, which can be accessed with `formEl.publicationForms[0]`, for invoking the `setCustomValidity` method that indicates a constraint violation if its argument is a non-empty (message) string.

## 11.7Run the App and Get the Code

You can run the enumeration app[138](33_Notes03.xhtml_Notes03_38) from our server or download the code[139](33_Notes03.xhtml_Notes03_39) as a ZIP archive file.

## 11.8Practice Projects

Compared to the validation app, you now have to take care of

1.  defining enumeration data types with the help of the meta-class Enumeration and defining any enumeration attribute together with a static check function and implicit get/set methods in the model code,
2.  adding suitable choice widgets for the enumeration attributes in the Create and Update user interfaces in the view code.

Make sure that your pages comply with the XML syntax of HTML5 by checking them with the XHTML5 validator[140](33_Notes03.xhtml_Notes03_40)(setting the validator field `Preset` to “HTML5 + SVG 1.1 + MathML 3.0”), and that your JavaScript code complies with our Coding Guidelines[141](33_Notes03.xhtml_Notes03_41) and its style is checked with JSHint[142](33_Notes03.xhtml_Notes03_42).

If you have any questions about how to carry out the following projects, you can ask them on our discussion forum[143](33_Notes03.xhtml_Notes03_43).

### 11.8.1Project 1 – Adding ratings and genres as enumeration attributes

The purpose of the app to be built is managing information about movies. The app deals with just one object type, `Movie`, and with two enumerations, as depicted in the following class diagram.

![](graphic/24_chapter11_fig_23.png)

Compared to the corresponding validation app project, two attributes have been added: the optional single-valued enumeration attribute `rating`, and the multi-valued enumeration attribute `genres`.

Following the tutorial, you have to take care of

1.  defining the enumeration data types `MovieRatingEL` and `GenreEL` with the help of the meta-class `Enumeration`;
2.  defining the single-valued enumeration attribute `Movie::rating`;
3.  defining the multi-valued enumeration attributes `Movie::genres`;
4.  extending the methods `Movie.update`, and `Movie.prototype.toString` such that they take care of the added enumeration attributes.

in the model code of your app, while In the user interface (“view”) code you now have to take care of

1.  adding new table columns in `retrieveAndListAllMovies.html` and suitable choice widgets in `createMovie.html` and `upateMovie.html`;
2.  creating output for the enumeration attributes in the method `v. retrieveAndListAllMovies.setupUserInterface()`;
3.  allowing input for the enumeration attributes in the methods `v. createMovie. setupUserInterface()` and `v. upateMovie.setupUserInterface()`.

You can use the following sample data for testing your app:

Table 11.1 Sample data about movies with rating and genres

![](graphic/24_chapter11_fig_24.png)

More movie data can be found on the IMDb website[144](33_Notes03.xhtml_Notes03_44).

### 11.8.2Project 2 – Adding country codes and religions as enumeration attributes

The purpose of the app to be built is managing information about countries. The app deals with just one object type, `Country`, and with two enumerations, as depicted in the following class diagram.

![](graphic/24_chapter11_fig_25.png)

Compared to the corresponding validation app project, two attributes have been added: the single-valued enumeration attribute `code`, which is a “key” attribute (implying a uniqueness constraint), and the multi-valued enumeration attribute `religions`.

You can use the following sample data for testing your app:

Table 11.2 Sample data about countries with country code and religions

![](graphic/24_chapter11_fig_26.png)

More data about countries can be found in the CIA World Factbook[145](33_Notes03.xhtml_Notes03_45).

## 11.9Quiz Questions

If you would like to look up the answers to the following quiz questions, you can check our discussion forum[146](33_Notes03.xhtml_Notes03_46). If you don’t find an answer in the forum, you may create a post asking for an answer to a particular question.

### 11.9.1Question 1: Checking the range constraint of an enumeration attribute

Complete the following code fragment for checking the range constraint of the enumeration attribute `gender` with range `GenderEL`:

![](graphic/24_chapter11_fig_27.png)

### 11.9.2Question 2: Computing MAX

Complete the following code fragment for computing the special enumeration literal MAX as in the proposed `Enumeration` class:

![](graphic/24_chapter11_fig_28.png)

# 12Implementing Enumeration Attributes in a Java EE Web App

In this chapter, we show how to build a back-end web application with enumeration attributes, using Java with JPA and JSF. In addition to the topic of enumeration attributes, we also show how to deal with multi-valued attributes.

## 12.1New Issues

Compared to the Validation App discussed in [Chapter 9](#21_chapter09.xhtml_chapter09_1) we have to deal with the following new issues:

1.  Enumeration datatypes have to be defined in a suitable way as part of the model code.
2.  Enumeration attributes have to be defined in model classes and handled in the user interface with the help of suitable choice widgets.

In terms of coding, the new issues are:

1.In the model code we have to take care of

a.enumerations to be defined in the form of Java `enum` classes;

b.single-valued enumeration attributes, like `Book::originalLanguage`, requiring the JPA annotation @Enumerated for defining the conversion between Java enumeration literals and corresponding database table column values;

c.multi-valued enumeration attributes, like `Book::publicationForms`, requiring the JPA annotation @Convert with suitable arguments defining a JPA custom converter for (de‐)serializing collections of Java enumeration literals;

d.extending the methods `Book. create`, and `Book.update` such that they take care of the enumeration attributes.

2.In the user interface code we have to take care of

a.adding new table columns in `retrieveAndListAll.xhtml`;

b.adding suitable choice widgets in `create.xhtml` and `upate.xhtml`;

c.rendering multi-valued enumeration attributes in the table view of `retrieveAndListAll.xhtml` and in the choice widgets of `create.xhtml` and `upate.xhtml` (with the help of an array of JSF `SelectItem`s, each consisting of an enumeration value and its label).

## 12.2Make an Entity Class Model

Using the information design model shown in [Figure 10.2](#23_chapter10.xhtml_chapter10_16) above as the starting point, we make an entity class model, essentially by adding getters/setters, constraint annotations and CRUD methods, as explained before:

![](graphic/25_chapter12_fig_01.png)

Figure 12.1 A JPA entity class model for the object type `Book`

## 12.3Write the Model Code

### 12.3.1Code the enumerations

Simple enumerations, like `BookCategoryEL` and `PublicationFormEL`, are coded in the following way with the help of Java’s `enum` construct:

![](graphic/25_chapter12_fig_02.png)

Notice how the enumeration literals are defined with capitalized names in a comma-separated list.

For a code list, like `LanguageEL`, where each enumeration instance consists of a code and a label, we use the codes as enumeration literals and define an attribute `label` for storing the labels, as well as a private constructor that allows creating enumeration instances consisting of a code and a label. This is possible because in Java, an `enum` is a special kind of class. Each entry in the list of enumeration literals, auch as `EN("English")`, represents an invocation of the `enum`’s constructor:

![](graphic/25_chapter12_fig_03.png)![](graphic/25_chapter12_fig_04.png)

### 12.3.2Code the JPA entity class

The entity class `Book` is coded with the help of JPA annotations for class attributes, as well as the setter and getter methods of every class attribute.

![](graphic/25_chapter12_fig_05.png)

For the case of single-valued enumeration attributes (like `originalLanguage` and `category`), the JPA annotation `@Enumerated` is used for specifying the storage serialization. It takes one of the following two parameter values:

–`EnumType.STRING` means that enumeration literals are converted to strings when they are serialized ( e.g., in the case of the `originalLanguage` attribute of the `Book` class, the values saved in the database are one of “EN”, “DE”, “FR” or “ES”) ;

–`EnumType.ORDINAL` means that enumeration literals are converted to their index integer when they are serialized (i. e.,the values saved in the database are 1, 2 ,3 etc.).

We store the collection values of a multi-valued enumeration attribute (like `otherAvailableLanguages` and `publicationForms`) in a database table column as serialized arrays in the form of `["value1", "value2",` …`]`. In the case of the `originalLanguage` attribute, an example of a saved value would be `["EN", "FR", "DE"]`. Achieving this behavior is possible with JPA by using custom converters to map database table column values to Java types and vice versa. The `@Convert` annotation allows specifying a Java converter that is responsible for the mappings.

Also, in the case of a multi-valued enumeration attribute, we use the `@Size` annotation to specify the minimum, and if required also the maximum, number of elements stored by this attribute. For example, in the case of `publicationForms`,we use `@Size( min=1, message = "At least one publication form is required!")`,which enforces to have at least one value for this attribute, otherwise the error message is displayed.

![](graphic/25_chapter12_fig_06.png)![](graphic/25_chapter12_fig_07.png)

Notice the new methods in the last code block, like `getPublicationFormsValues` and `getPublicationFormsItems`, which are used for handling the enumeration attributes in the UI. We discuss each of them in the following subsections.

### 12.3.3Define a converter for serializing enumeration attribute values

A JPA attribute converter is a special Java class that implements the `AttributeConverter` interface with the methods `convertToDatabaseColumn` and `convertToEntityAttribute`. For the `otherAvailableLanguages` attribute, we define the following converter class:

![](graphic/25_chapter12_fig_08.png)

An attribute converter class needs to be annotated with `@Converter`. In our example, the `convertToDatabaseColumn` method is responsible to convert the entity attribute value (e. g., `otherAvailableLanguages`) to a JSON array which is stored in the database as a `String`.

The `convertToEntityAttribute` method is responsible for de-serializing a table column’s value to the corresponding entity attribute value. In our example, this means to map the JSON array string to a Java `Set` of enumeration literals of type `LanguageEL`.

The code above shows the custom attribute converter class for the `otherAvailableLanguages` attribute. The attribute converter class for the `publicationForms` attribute is defined in the same way.

### 12.3.4Code the enumeration attribute setters

Both for single-valued and for multi-valued enumeration attributes an ordinary setter is defined. In the case of a multi-valued enumeration attribute, this setter assigns an entire set of values (in the form of a Java `Set`) to the attribute.

### 12.3.5Write a serialization function

The object serialization function now needs to include the values of enumeration attributes:

![](graphic/25_chapter12_fig_09.png)![](graphic/25_chapter12_fig_10.png)

### 12.3.6Database schema

As we discussed in [Chapter 4](#15_chapter04.xhtml_chapter04_1), the database schema can be automatically generated by a Java EE server like TomEE. The generated schema for our `Book` entity class is like so:

![](graphic/25_chapter12_fig_11.png)

For every attribute (like `category`), a column with the same name but using upper case is created, (e. g., `CATEGORY`). This is the default naming, which is fine for our example application, but it can be changed, if required, by using the `@Column ( name="`…`")` annotation, as in `@Column( name="book_category")`.

The single-valued and multi-valued enumeration attributes are by default created as `varchar` columns with the default maximum length of `255` characters. However, if a longer (or shorter) length is desirable, this can be enforced by using the `@Column( length=`…`)` annotation.

### 12.3.7Creating test data

In the test data objects that are created by `Book.createTestData`,we now have to provide values for single- and multi-valued enumeration attributes:

![](graphic/25_chapter12_fig_12.png)![](graphic/25_chapter12_fig_13.png)

## 12.4Write the View Code

The example app’s user interface for creating a new book record with ISBN, title and four enumeration attributes looks as in [Figure 12.2](#25_chapter12.xhtml_chapter12_12) below.

![](graphic/25_chapter12_fig_14.png)

Figure 12.2 The user interface for creating a new book record

### 12.4.1Selection lists

We use JSF selection lists for rendering the enumeration attributes `originalLanguage` and `otherAvailableLanguages` in the code of the facelet files `WebContent/views/books/create.xhtml` and …`/update.xhtml`:

![](graphic/25_chapter12_fig_15.png)

The JSF element `h:selectOneMenu` allows creating single selection lists with the HTML `select` element. The list is populated with language options due to its child element `<f:selectItems value="#{book.languageItems}"/>`. Using the expression `#{book.languageItems}` results in calling the method `getLanguageItems()` on the `book` object. This method returns a set of `Select``Item` objects, which are used to populate the selection list. The corresponding method code is as follows:

![](graphic/25_chapter12_fig_16.png)

A multiple selection list, corresponding to an HTML element `<select multiple= "multiple"` …`/>`, is created with the JSF element `h:selectManyListbox` using the same `getLanguageItems` method for obtaining the selection list items.

### 12.4.2Radio button groups and checkbox groups

Since the enumeration attributes `category` and `publicationForms` have not more than seven possible values, we can use a radio button group and a checkbox group for rendering them:

![](graphic/25_chapter12_fig_17.png)![](graphic/25_chapter12_fig_18.png)

The radio button group is obtained by using the JSF element `h:selectOneRadio`. It renders a set of `<input type="radio"` … `/>` elements. Using the same technique as for selection lists, the radio button group is populated with a set of `Select``Item` objects. The corresponding `getCategoryItems` method from the `Book` class is similar to `getLanguageItems`.

The checkbox group, consisting of `<input type="checkbox"` … `/>` elements, is created with the JSF element `h: selectManyCheckbox` and populated in the same way as a radio button group or a selection list.

## 12.5Displaying Value Sets for Multi-Valued Enumeration Attributes

In the case of a multi-valued enumeration attribute like `otherAvailableLanguages` or `publicationForms`, the Retrieve/List All view must show a value in the form of a comma-separated list, like “English, German, Spanish”, as shown in the following table:

![](graphic/25_chapter12_fig_19.png)

For this purpose, we define a method that creates the desired serialization of a multivalued attribute and use it in the code of the facelet file `retrieveAndListAll. xhtml` from `WebContent/views/books/`. For the `publicationForms` attribute, the method code is as follows:

![](graphic/25_chapter12_fig_20.png)![](graphic/25_chapter12_fig_21.png)

Notice that in the case of the `publicationForms` attribute, the underlying enumeration `PublicationFormEL` does not have a label property. Instead, we use the enumeration literal name in lowercase as the label.

## 12.6Run the App and Get the Code

You can run the enumeration app[147](33_Notes03.xhtml_Notes03_47) on our server or download the code[148](33_Notes03.xhtml_Notes03_48) as a ZIP archive file.

## 12.7Practice Projects

In the following practice projects, first make a list of all the constraints that have been defined in this model and express them with validation annotations. Then make an entity class model as a starting for coding the app by following the guidance of this chapter and [Chapter 9](#21_chapter09.xhtml_chapter09_1).

If you have any questions about how to carry out the following projects, you can ask them on our discussion forum[149](33_Notes03.xhtml_Notes03_49).

### 12.7.1Project 1 – Adding ratings and genres as enumeration attributes

The purpose of the app to be built is managing information about movies. The app deals with just one object type, `Movie`, and with two enumerations, as depicted in the following class diagram.

![](graphic/25_chapter12_fig_22.png)

You can use the sample data shown in [Table 11.1](#24_chapter11.xhtml_chapter11_30) for testing your app.

### 12.7.2Project 2 – Adding country codes and religions as enumeration attributes

The purpose of the app to be built is managing information about countries. The app deals with just one object type, `Country`, and with two enumerations, as depicted in the following class diagram.

![](graphic/25_chapter12_fig_23.png)

Compared to the practice project of our validation tutorial, two attributes have been added: the single-valued enumeration attribute `code`, which is a “key” attribute (implying a uniqueness constraint), and the multi-valued enumeration attribute `religions`.

You can use the sample data shown in [Table 11.2](#24_chapter11.xhtml_chapter11_33) for testing your app.

## 12.8Quiz Questions

If you would like to look up the answers for the following quiz questions, you can check our discussion forum[150](33_Notes03.xhtml_Notes03_50). If you don’t find an answer in the forum, you may create a post asking for an answer to a particular question.

### 12.8.1Question 1: JPA custom converter implementation class

Complete the following JPA custom converter class code, such that it serializes a value of type `List<GenreEL>` to `String`.:

![](graphic/25_chapter12_fig_24.png)

### 12.8.2Question 2: Cardinality constraints for enum attributes

Complete the definition of the `languages` property, such that a minimum of three values are required.

![](graphic/25_chapter12_fig_25.png)

### 12.8.3Question 3: JPA enum attribute serialization annotation

Use the appropriate JPA annotation, including parameter(s), such that the value of the `genre` property is serialized and stored as enumeration literal name, i. e., as `String`, and not as ordinal values (indexes):

![](graphic/25_chapter12_fig_26.png)![](graphic/25_chapter12_fig_27.png)

### 12.8.4Question 4: JSF single-valued enum attribute

Which of the following is the name of a JSF element that can be used for rendering a choice widget for a single-valued enumeration attribute?

1.  O `selectOneRadio`
2.  O `selectOnlyOne`
3.  O `radioGroup`
4.  O `radioSelect`

### 12.8.5Question 5: JSF multi-valued enum attribute

Complete the following facelet code, such that the resulting HTML code consists of a checkbox group allowing to select multiple languages, when creating a new `Book` instance::

![](graphic/25_chapter12_fig_28.png)

![](graphic/11_Part01_fig_01.png)

# Part IVSpecial Datatypes and Derived Properties

In addition to standard numeric and string data values, special attributes may also have several types of special data values, such as calendar dates or quantities (like times or monetary amounts), or composite values like records. Some attributes are derived from others.

# 13Special Datatypes

In an app, we have to deal with various types of attributes. While many of them have a standard datatype, like `Integer` or `String`, as their range, some of them may have special datatypes as their range. For instance, the Universal Business Language (UBL), which is an industry standard defining document formats for electronic commerce, defines a large set of business datatypes including the following.

| UBL Data Type | Description |
| Date | One calendar day according to the Gregorian calendar. |
| Time | An instance of time that occurs every day. |
| DateTime | A particular point in the progression of time, together with relevant supplementary information. |
| Percent | Numeric information that is assigned or is determined by calculation, counting, or sequencing and is expressed as a percentage. |
| Amount | A number of monetary units specified using a given unit of currency. |

The Semantic MediaWiki[151](34_Notes04.xhtml_Notes04_1) uses the following special datatypes.

| Semantic MediaWiki Data Type | Description |
| Geographic coordinate | Holds coordinates describing geographic locations |
| Monolingual text | To associate a text value with a specific language code |
| Quantity | Holds values that describe quantities, containing both a number and a unit |
| Record | Allows saving compound property values that consist of a short list of values with fixed type and order |
| Email | Holds e-mail addresses |
| URL | Holds URIs, URNs and URLs |
| Telephone number | Holds international telephone numbers based on the RFC 3966[152](34_Notes04.xhtml_Notes04_2) standard |

We discuss several important cases of special datatypes and how to deal with them in the model code and in the HTML user interface code. The following class diagram illustrates examples of attributes having such a special datatype as their range.

In the C++ and C# programming communities, special datatypes like string patterns and quantities are also called “semantic types” (see, e. g., Gibson2016[153](34_Notes04.xhtml_Notes04_3) and Perdeck2015[154](34_Notes04.xhtml_Notes04_4)).

## 13.1Boolean Values

Boolean attributes, like `isSmoker`, can only have one of two possible values: true or false, which are sometimes more naturally expressed with yes or no. In the model code, Boolean attributes are treated like primitive datatype attributes, since all programming languages support Boolean as a primitive datatype.

For rendering a Boolean attribute in a user interface, there are several options. The simplest solution is using a checkbox field. Alternatively, a single-selection list with the two options true and false (or yes and no), or a corresponding radio button group with two radio buttons, could be used.

In an HTML form, a checkbox field is implemented with an `input` element of type `checkbox`. For assigning the value of the checkbox field to the Boolean attribute, the field’s `checked` attribute has to be used, as shown in the following example where we have a checkbox field in an HTML form:

![](graphic/27_chapter13_fig_01.png)

In JavaScript code, the checkbox field is accessed via its name, and the Boolean attribute is assigned by reading the field’s `checked` attribute (instead of its `value` attribute), like so:

![](graphic/27_chapter13_fig_02.png)

## 13.2String Patterns

Email addresses, URLs and telephone numbers are examples of strings that have to match a certain pattern, typically defined by a regular expression. It’s quite common to have attributes with such values. For readability, it’s preferable to use predefined datatypes, like `Email`, `URL` and `PhoneNumber`, in an information design model, instead of defining them as string-valued attributes with a pattern constraint.

In a (JavaScript or Java) model class definition, these attributes have to be implemented as string-valued attributes with a pattern constraint. It is, however, desirable to have built-in support for them, like in the data/document format definition language XML Schema.

### 13.2.1Telephone numbers

There is much variation in the format of phone numbers across different countries. Consequently, it doesn’t make sense trying to capture all these different formatting options with one pattern. The HTML5 specification doesn’t define any syntax rules for phone numbers in the context of `input` elements of type “tel”, except that they can’t include line breaks. The precise formatting assumptions and corresponding validation is left to the application developer who may employ a specific pattern for enforcing a particular national or international phone number format.

A simple international phone number format has been defined by the International Telecommunication Union’s ITU-T E123 standard. It requires that phone numbers include a leading plus sign and allows only spaces to separate groups of digits. ITU has also limited the length of phone numbers to at most 15 digits. Since the shortest international phone numbers in use contain seven digits, we can use these two constraints in the following JavaScript definition of a regular expression for international phone numbers:

![](graphic/27_chapter13_fig_03.png)

### 13.2.2Email addresses

The format of email addresses has originally been defined by the International Engineering Task Force (IETF), but due to several weaknesses it has been redefined in the HTML5 specification in the context of introducing `input` elements of type “email”. The HTML5 specification provides a regular expression for email addresses[155](34_Notes04.xhtml_Notes04_5), which can be used for validating strings that are supposed to be email addresses.

### 13.2.3URLs

The format of URLs has originally been defined by the International Engineering Task Force (IETF), but due to several weaknesses and the historical confusion about URLs versus URIs versus IRIs, it has been redefined in the URL specification[156](34_Notes04.xhtml_Notes04_6) of the WHAT Working Group. The syntax rules defined in this specification also define the validity of URL strings in `input` elements of type “url” introduced by HTML5.

There are many proposals[157](34_Notes04.xhtml_Notes04_7) how to capture the complex URL parsing rules with a regular expression, but most of them are either too strict or too lax. The solution by Diego Perini[158](34_Notes04.xhtml_Notes04_8) stands out and seems to be a pretty good approximation. As soon as the new built-in JavaScript object type `URL` is supported by all browsers, a precise validation check will be possible by trying to create a `URL` object with a given URL string, and then catch any DOMException of type `SYNTAX_ERROR`.

## 13.3Special Numeric Data Types

### 13.3.1Positive and non-negative integers

Since it is common to have positive or non-negative integer attributes, it’s preferable to use predefined datatypes, like `PositiveInteger` and `NonNegativeInteger`, as their range in an information design model, instead of defining them with the range `Integer` and adding a corresponding interval constraint.

In a (JavaScript or Java) model class definition, these attributes have to be implemented as integer-valued attributes with an interval constraint. It is, however, desirable to have built-in support for them, like in the data/document format definition language XML Schema.

### 13.3.2The unit interval

Certain attributes, e. g., when representing probabilities, have the unit interval [0,1], or one of its open variants, as their range. They can be implemented as decimal-valued attributes with an interval constraint. But having a corresponding predefined datatype, like `UnitInterval`, is preferable.

### 13.3.3Percentages

The values of certain attributes represent percentages, which are decimal numbers that have to be divided by 100 for obtaining the numeric value represented by them. In a user interface, the value of a percentage attribute is shown with a % suffix, similar to quantity attributes shown with a unit suffix. For supporting percentage attributes, a special predefined datatype like `Percent` is needed.

### 13.3.4Arbitrary precision numbers

In widely used programming languages, like JavaScript and Java, the built-in standard datatypes for dealing with decimal numbers (like `number` in JavaScript and `double` in Java) do not support precise calculations. For instance, in JavaScript, the result of computing the subtraction 0.3–0.1 is not 0.2, but rather 0.09999999999999998, which is close to, but not the same as the correct result. Even if such a precision error may be acceptable in a use case like in physics simulation for games, it is not acceptable in a use case like financial accounting.

The concept of arbitrary-precision numbers is to allow calculations where the precision is only limited by the available computer memory, unlike the fixed-precision arithmetic implemented in a computer’s arithmetic logic unit, which is normally employed by the standard arithmetic implementation of a programming language. Arbitrary-precision numbers are used in applications where precise results of calculations (even with large numbers) are required and where the calculation speed is not a critical factor.

In JavaScript, we can use a library like big.js[159](34_Notes04.xhtml_Notes04_9) or mathjs[160](34_Notes04.xhtml_Notes04_10) for arbitrary-precision calculations. For instance, using the big.js library, the precise result of the subtraction 0.3–0.1 is obtained in the following way:

![](graphic/27_chapter13_fig_04.png)

The maximum number of decimal places and the rounding mode used to round the results of the critical operations `div`, `sqrt` and `pow` (with negative exponent) is determined by the value of the static properties `DP` and `RM` of the `Big` class, as illustrated by the following example:

![](graphic/27_chapter13_fig_05.png)

The rounding mode property values 0..3 have the following meaning:

| Value |  | Description | Java BigDecimal equivalent |
| 0 |  | Rounds towards zero. I.e. truncate, no rounding. | ROUND_DOWN |
| 1 |  | Rounds towards nearest neighbour. If equidistant, rounds away from zero. | ROUND_HALF_UP |
| 2 |  | Rounds towards nearest neighbour. If equidistant, rounds towards even neighbour. | ROUND_HALF_EVEN |
| 3 |  | Rounds away from zero. | ROUND_UP |

In Java, we can use the built-in datatype class `BigDecimal`[161](34_Notes04.xhtml_Notes04_11) for arbitrary-precision calculations. For instance, the precise result of the subtraction 0.3–0.1 is obtained in the following way:

![](graphic/27_chapter13_fig_06.png)

The maximum number of decimal places, called scale in Java, is either set implicitly by the constructor argument or explicitly with

![](graphic/27_chapter13_fig_07.png)

A scale and `rounding` mode can be set for each operation by providing either a scale value and a `RoundingMode` enumeration literal or a `MathContext` object. They should be set at least for the critical operations `divide` and `pow` (with negative exponent), as illustrated by the following example:

![](graphic/27_chapter13_fig_08.png)

In this example, the value of the `result` variable is 0.6666666667.

## 13.4Calendar Dates and Times

Calendar dates, times of the day and timestamps (date-times) are special data values, which are often only supported for the Gregorian calendar. We use the datatype names `Date`, `TimeOfDay` and `Timestamp` in information design models.

Both JavaScript and Java have a built-in `Date` class that does actually not represent calendar dates, but rather timestamps (or date-times) in the specific form of the number of milliseconds since 1 January, 1970 UTC.

### 13.4.1Using JavaScript’s Date class

JavaScript’s `Date` class allows to represent Gregorian calendar timestamps in the interval of +/- 100 Million days or approximately 285,000 years either forward or backward, from 01 January, 1970 UTC.

A JS data-time can be created in several ways:

![](graphic/27_chapter13_fig_09.png)

A timestamp with the current date and time can be created in the following way:

![](graphic/27_chapter13_fig_10.png)

Assume that the `Book` model class defined above has an additional attribute `publicationDate`, the values of which have to be included in HTML tables and forms. While date/time information items have to be formatted as strings in a human-readable form on web pages, preferably in localized form based on the settings of the user’s browser, it’s not a good idea to store date/ time values in this form in a database. Rather we use instances of the predefined JavaScript class `Date` for representing date/ time values internally and for storing them. The predefined functions `toISOString()` and `toLocaleDateString()` can be used for turning `Date` values into ISO standard date/time strings of the form “2015-01-27”, or to localized date/ time strings like “27.1\. 2015” (for simplicity, we have omitted the time part in these strings).

In summary, date/ time values may be expressed in three different forms:

1.  Internally, for storage and computations, as a `Date` value.
2.  Internally, for annotating localized date/ time strings, or externally, for displaying a date/ time value in a standard form, as an ISO standard date/ time string, e. g., with the help of `toISOString()`.
3.  Externally, for displaying a date/time value in a localized form, as a localized date/time string, e.g., with the help of `toLocaleDateString()`.

Since the calendar arithmetic and calendar date manipulation functionality of the built-in `Date` class is limited, using a library like date-fns[162](34_Notes04.xhtml_Notes04_12) may be helpful for doing more advanced calendar computations.

### 13.4.2Dealing with calendar dates and times in the user interface

For showing a date/ time value as an information item in a web page, we can use the HTML `<time>` element that allows displaying a human-readable representation (typically a localized date/ time string) that is annotated with a standard (machine-readable) form of the date/ time value.

We illustrate the use of the `<time>` element with the following example of a web page that includes two `<time>` elements: one for displaying a fixed date, and another (initially empty) element for displaying the date of today, which is computed with the help of a JavaScript function. In both cases we use the `datetime` attribute for annotating the displayed human-readable date with the corresponding machine-readable representation.

![](graphic/27_chapter13_fig_11.png)

This web page loads and executes the following JS function for computing today’s date as a `Date` value and assigning its ISO standard representation and its localized representation to the `<time>` element:

![](graphic/27_chapter13_fig_12.png)

For providing better support concerning the user input of a calendar date value in an HTML `form`-based user interface, HTML5 has introduced the `input` element types “date” and “time”, which are supposed to instruct browsers to render special UI widgets for picking a date or time. For instance, the following HTML form is supposed to be rendered with a date picker widget:

![](graphic/27_chapter13_fig_13.png)

Unfortunately, in April 2017, a date picker widget has still not been implemented in the Firefox browser, so a progressive enhancement approach is required, where a date picker widget is created with the help of a JS library (like flatpickr[163](34_Notes04.xhtml_Notes04_13)) whenever the current browser does not provide one.

When the user has picked a date in a widget, the `input` element’s `value` attribute contains a date string. A simple way to convert this string into a `Date` value is provided by using the DOM attribute `valueAsDate` like so:

![](graphic/27_chapter13_fig_14.png)

### 13.4.3Using Java’s Date and Calendar classes

In Java, we have two important built-in classes for dealing with date-times:

–`java.util.Calendar` is an abstract class, which provides methods for dealing with calendar timestamps and which has concrete subclasses for specific calendars like the `GregorianCalendar`. Notice that an instance of `Calendar` is not a calendar, but a wrapped date-time value. For getting a specific date or datetime, we can invoke the constructor of a suitable calendar class with the desired values:

![](graphic/27_chapter13_fig_15.png)

–`java.util.Date` is a class that represents timestamps (or date-times) in the specific form of the number of milliseconds since 1 January, 1970 UTC. Most of the methods and constructors of the `Date` class have been depreciated (because they do not support internationalization), but not the class itself. It is recommended to either avoid using it and use a suitable `Calendar` subclass instead of `Date`, or, if an instance of `Date` is needed, create a `Date` object by first creating a `Calendar` object and then converting it to a `Date` object with the help of the `getTime` method:

![](graphic/27_chapter13_fig_16.png)

For getting a `Date` object that holds the current date-time, we can use the constructor without parameters:

![](graphic/27_chapter13_fig_17.png)

It is important to notice that months are represented as integers in the range [0, 11], where 0 denotes the month January and 11 the month December. The days of the month are represented as integers in the range [1, 31]. The hours of the day are integers in the range [0, 23] and the minutes are integers in the range [0, 59].

In many cases, we need to deal directly with values for date-time components like the month, day, hour and so on, instead of just having these values wrapped in an object. The `Calendar` class defines the `get` method, taking an integer parameter that allows to specify the desired date-time component in the form of static `Calendar` properties. For example, if we need to extract the current year, month, day, hour, minute and second, we use the following code:

![](graphic/27_chapter13_fig_18.png)

For more about date/time handling in Java see Chua Hock-Chuan’s Java Date webpage[164](34_Notes04.xhtml_Notes04_14).

### 13.4.4Using Date and Calendar with JPA

In an entity class with temporal attributes, having `Date` or `Calendar` as their range, we use the `@Temporal` annotation:

![](graphic/27_chapter13_fig_19.png)

The `TemporalType` enumeration has three possible values: `DATE`, `TIME` and `TIMESTAMP`, which allow to specify the serialization format used when a `Date` or `Calendar` object is persisted in a database. These values correspond to the classes `java.sql.Date`, `java.sql.Time` and `java.sql.Timestamp`, all being subclasses of `java.util.Date`.

### 13.4.5Rendering Date Attributes with JSF

Rendering `Date`-valued attributes requires using the JSF element `h: inputText` with the attribute `p:type="date"`. This creates an HTML `input` element of type date. For example, a person’s `dateOfBirth` attribute can be rendered in a facelet like so:

![](graphic/27_chapter13_fig_20.png)

The JSF converter `f:convertDateTime` allows specifying an output format for date values. In the above example, we specify four digits for the year, two digits for the month and two digits for the day (e. g., 2015-07-23).

As a result, the following HTML code is generated:

![](graphic/27_chapter13_fig_21.png)

## 13.5Quantities

A quantity data value consists of a number and a quantity unit. Examples of physical quantity data values (or, simply, quantities) are 1.86 m, 76.5 kg, 44 s, 3.9 m/s, 21 ° C, and 200 mV. Other important examples are monetary amounts like $24.95 or 7 €.

In model object attributes and user interface fields, quantities can be represented by plain numbers, if their unit is retrievable from an underlying datatype definition. It may be desirable that a user interface allows the user to change the unit of a quantity such that the numeric value of the user interface field is automatically converted to the chosen unit.

In a simple approach for supporting quantities, there is a (possibly extensible) set of predefined quantity datatypes such as Length, Mass, Time, Temperature and Amount, each of them associated with a fixed standard unit (such as “m” for Length and “$” for Amount) and an optional base unit such that a quantity data value is a plain number defining the quantity in the base unit, if a base unit is defined, otherwise in the standard unit.

![](graphic/27_chapter13_fig_22.png)

Figure 13.1 Quantity types.

When defining the properties of a class, a quantity-valued attribute would have to be defined by specifying a quantity datatype definition like `Length()`or `Time(Y)` as its range. This is, however, not possible in a standard JS constructor definition or an ES6 class definition. Rather, a class definition approach supporting range specifications like cLASSjs[165](34_Notes04.xhtml_Notes04_15), discussed in Volume 2 of the book, is required.

In this approach, the data value of a quantity attribute would be a plain number that is interpreted in combination with the base unit of the attribute’s quantity datatype. Quantities could be easily converted to other preferred units in a user interface in a generic manner by invoking the conversion functions defined by the quantity unit instances of the `QuantityUnit` class.

Gibson2016[166](34_Notes04.xhtml_Notes04_16) reports on a proposal for C++, which allows expressing quantities in a natural way as number/unit pairs in arithmetic expressions based on the C++ features of operator overloading and user-defined literals. For instance, if someone would run 100 meter in 9.58 seconds, a variable for computing her speed could be assigned like so

![](graphic/27_chapter13_fig_23.png)

A general approach to supporting physical quantity datatypes would have to be based on the seven fundamental physical quantity dimensions Length, Mass, Time, Temperature, ElectricCurrent, LuminousIntensity and AmountOfSubstance, which are the basis for defining composite physical quantities such as Area in m2 or Velocity in m/s by defining a map {d1:e1, …, d7:e7} from the fundamental quantity dimensions di to integers ei as exponents of the generic quantity dimension expression:

![](graphic/27_chapter13_fig_24.png)

## 13.6Complex Data Types

### 13.6.1Records

Records are composite data values consisting of field slots, which are name-value pairs, such that we can access the value of a record field via its name.

Examples of records are address records like `{street: "37 Market St", city: "New York", zipCode: 10473}` or phone book entries like `{type:"home", areaCode:"757" number:"3765295"}`.

##### 13.6.1.1 Color definitions

Colors can be defined with three components on the basis of a color model such as the Red-Green-Blue (RGB) color model or the Hue-Saturation-Lightness (HSL) color model. In both models a fourth component, in the form of a decimal number from the unit interval [0,1] or a corresponding percentage, for defining the opacity (technically called alpha channel) of a color can be added.

In the RGB model, each component value is an integer between 0 and 255\. In CSS, an RGB color is specified by a ternary term like `rgb( 255, 255, 255)` corresponding, e. g., to a JS triple record like `{R:255, G: 255, B:255}`.

In the HSL model, the H component is an integer between 0 and 360 denoting an angle degree in the rainbow color circle with red = 0 = 360, green = 120, and blue = 240\. Saturation and lightness are represented as percentages, such that S=100% is full saturation, and 0% is a shade of grey, L=100% is white, 0% lightness is black, and 50% lightness is “normal”. In CSS, an HSL color is specified by a ternary term like `hsl( 0, 0%, 100%)` corresponding, e. g., to a JS triple record like `{H:0, S:0, L:100}`.

In an HTML form-based user interface, color definitions are supported by HTML5 `input` elements of type “color”, which are to be rendered in the form of a color picker widget.

##### 13.6.1.2 Geo-coordinates

Geographic coordinates (or geodetic positions) can be defined in the form of records like `{latitude: 40.6643, longitude: -73.9385}`.

##### 13.6.1.3 Rendering records in a user interface

A record-valued property (like `geoCoordinates`) should be rendered as a list of fields in a coherent region in the UI, preferably with a `fieldset` element with the property’s label as the content of the `legend` element. In simple cases, like in the following example, with only a few record fields, using suitable CSS rules, it may be possible to render all fields horizontally on the same line.

![](graphic/27_chapter13_fig_25.png)

Notice how the property `geoCoordinates` is bound to the `fieldset` element with the help of the custom `data-bind` attribute.

### 13.6.2Data collections

Data collections are ordered or unordered sets or bags (multi-sets), with all members being either primitive data values, records of a certain type or data collections of a certain type. Instead of “unordered set”, we simply say “set”, and instead of “ordered bag” we say “list”.

Examples:

1.  The nick names of a person may be recorded in a set-valued attribute `nickNames`.
2.  The favorite composers of a person may be recorded in an ordered-set-valued attribute `favoriteComposers` such that the order represents a ranking.
3.  A train trip route may be recorded as a list of train stop locations.

In the user interface, a collection-valued attribute may be rendered as a text field with a comma-separated list of strings if the value collections are sufficiently small. Otherwise, a special table-like UI widget is needed for value assignments and changes.

# 14Derived Properties

In certain cases, a property may have the only purpose to provide some information that is computed from other information items. For such a derived property, there is no point to allow the user entering a value for it. Examples of derived properties of a class `Person` are the attributes `age` and `initials`. The value of `age` is computed on demand from the value of the attribute `dateOfBirth` and the current year. The value of `initials` is computed from the values of the attributes `firstName` and `lastName`.

Unlike in the case of standard properties, the value of a derived property cannot be set by the user. Rather, it is computed from the values of other properties. Consequently, it does not have a setter, but only a getter method.

## 14.1Virtual Derived Properties

When the value of a derived property is computed on demand, only, by its getter method performing its computation, the derived property is called virtual. The value of such a virtual derived property is not stored. When using JavaScript’s get/ set methods in an ES6 `class` definition, this means that we only define a `get` method for `age`, but no internal property like `_age`, and no `set` method:

![](graphic/28_chapter14_fig_01.png)

## 14.2Materialized Derived Properties

If the value of a derived property is computed whenever there is a change in the value of one of the properties on which it depends, the derived property is called materialized. The value of such a materialized derived property is stored, and the getter method simply retrieves this stored value. When using JavaScript’s get/set methods in an ES6 `class` definition, this means that we define a `get` method for `initials` retrieving the value of the internal attribute `_initials`, but no `set` method. The computation of the materialized derived property’s value is performed in the setters of the attributes on which it depends, as shown in the following example:

![](graphic/28_chapter14_fig_02.png)

Notice that the computation of the initials of a person is performed in the setters of `firstName` and `lastName`, whenever these attributes are initialized or changed.

## 14.3Dealing with Derived Properties in the User Interface

Since derived properties are not set by user input, there are no `input`, but only `output` fields for them in a user interface. This is illustrated in the following example of an HTML form:

![](graphic/28_chapter14_fig_03.png)

# Glossary

| C |  |
| CRUD | CRUD is an acronym for Create, Read/Retrieve, Update, Delete, which denote the four basic data management operations to be performed by any software application. |
| CSS (Cascading Style Sheets) | CSS is used for defining the presentation style of web pages by telling the browser how to render their HTML (or XML) contents: using which layout of content elements, which fonts and text styles, which colors, which backgrounds, and which animations. Normally, these settings are made in a separate CSS file that is associated with an HTML file via a special link element in the HTML’s head element. |
| D |  |
| DOM (Document Object Model) | The DOM is an abstract API for retrieving and modifying nodes and elements of HTML or XML documents. All web programming languages have DOM bindings that realize the DOM. |
| DNS (Domain Name System) | The DNS translates user-friendly domain names to IP addresses that allow to locate a host computer on the Internet. |
| E |  |
| ES (ECMAScript) | A standard for JavaScript defined by the industry organization “Ecma International”. |
| XML (Extensible Markup Language) | XML allows to mark up the structure of all kinds of documents, data files and messages in a machine-readable way. XML may also be human-readable, if the tag names used are self-explaining. XML is based on Unicode. SVG and MathML are based on XML, and there is an XML-based version of HTML. |
|  | XML provides a syntax for expressing structured information in the form of an XML document with elements and their attributes. The specific elements and attributes used in an XML document can come from any vocabulary, such as public standards or user-defined XML formats. |
| H |  |
| HTML (Hypertext Markup Language) | HTML allows marking up (or describing) the structure of a human-readable web document or web user interface. The XML-based version of HTML, which is called “XHTML5”, provides a simpler and cleaner syntax compared to traditional HTML. |
| HTTP (Hypertext Transfer Protocol) | HTTP is a stateless request/ response protocol based on the Internet technologies TCP/IP and DNS, using human-readable text messages for the communication between web clients and web servers. The main purpose of HTTP has been to allow fetching web documents identified by URLs from a web browser, and invoking the operations of a back-end web application program from an HTML form executed by a web browser. More recently, HTTP is increasingly used for providing web APIs and web services. |
| I |  |
| IANA | IANA stands for Internet Assigned Numbers Authority, which is a subsidiary of ICANN responsible for names and numbers used by Internet protocols. |
| ICANN | ICANN stands for Internet Corporation of Assigned Names and Numbers, which is an international nonprofit organization that maintains the domain name system. |
| IndexedDB | A JavaScript API for indexed data storage managed by browsers. Indexing allows high-performance searching. Like many SQL DBMS, IndexedDB supports database transactions. |
| I18N | A set of best practices that help to adapt products to any target language and culture. It deals with multiple character sets, units of measure, keyboard layouts, time and date formats, and text directions. |
| J |  |
| JSON | JSON stands for JavaScript Object Notation, which is a data-interchange format following the JavaScript syntax for object literals. Many programming languages support JSON as a light-weight alternative to XML. |
| M |  |
| MathML | An open standard for representing mathematical expressions, either in data interchange or for rendering them within webpages. |
| MIME | A MIME type (also called “media type” or “content type”) is a keyword string sent along with a file for indicating its content type. For example, a sound file might be labeled `audio/ogg`, or an image file `image/png`. |
| MVC (Model-View-Controller) | MVC is a general architecture metaphor emphasizing the principle of separation of concerns, mainly between the model and the view, and considering the model as the most fundamental part of an app. In MVC frameworks, “M”, “V” and “C” are defined in different ways. Often the term “model” refers to the app’s data sources, while the “view” denotes the app’s code for the user interface, which is based on CSS-styled HTML forms and DOM events, and the “controller” typically denotes the (glue) code that is in charge of mediating between the view and the model. |
| O |  |
| OCL (Object Constraint Language) | The OCL is a formal logic language for expressing integrity constraints, mainly in UML class models. It also allows defining derivation expressions for defining derived properties, and defining preconditions and postconditions for operations, in a class model. |
| OOP (Object-Oriented Programming) | OOP is a programming paradigm based on the concepts of objects and classes instantiated by objects. Classes are like blueprints for objects: they define their properties and the methods/ functions that can be applied to them. A higher-level characteristic of OOP is inheritance in class hierarchies: a subclass inherits the features (properties, methods and constraints) of its superclass. |
| OWL (Web Ontology Language) | OWL is formal logic language for knowledge representation on the Web. It allows defining vocabularies (mainly classes with properties) and supports expressing many types of integrity constraints on them. OWL is the basis for performing automated inferences, such as checking the consistency of an OWL vocabulary. Vocabularies, or data models, defined in the form of UML class models can be converted to OWL vocabularies and then checked for consistency. |
| P |  |
| PNG (Portable Network Graphics) | PNG is an open (non-proprietary) graphics file format that supports lossless data compression. |
| Polyfill | A polyfill is a piece of JavaScript code for emulating a standard JavaScript method in a browser, which does not support the method. |
| R |  |
| RDF (Resource Description Framework) | RDF is a W3C language for representing machine-readable propositional information on the Web. |
| S |  |
| SGML (Standard Generalized Markup Language) | SGML is an ISO specification for defining markup languages. HTML4 has been defined with SGML. XML is a simplified successor of SGML. HTML5 is no longer SGML-based and has its own parsing rules. |
| SVG (Scalable Vector Graphics) | SVG is a 2D vector image format based on XML. SVG can be styled with CSS and made interactive using JavaScript. HTML5 allows direct embedding of SVG content in an HTML document. |
| Slot | A slot is a name-value pair. In an object of an object-oriented program (for instance, in a Java object), a slot normally is a property-value pair. But in a JavaScript object, a slot may also consist of a method name and a method body or it may be a key-value pair of a map. |
| U |  |
| Unicode | A platform-independent character set that includes almost all characters from most of the world’s script languages including Hindi, Burmese and Gaelic. Each character is assigned a unique integer code in the range between 0 and 1,114,111\. For example, the Greek letter π has the code 960\. Unicode includes legacy character sets like ASCII and ISO-8859–1 (Latin1) as subsets. |
|  | XML is based on Unicode. Consequently, the Greek letter π (with code 960) can be inserted in an XML document as π using the XML entity syntax. The default encoding of Unicode characters in an XML document is UTF-8, which uses only a single byte for ASCII characters, but three bytes for less common characters. |
| URI (Uniform Resource Identifier) URL (Uniform Resource Locator) UML (Unified Modeling Language) | A URI is either a Uniform Resource Locator (URL) or a Uniform Resource Name (URN). A URL is a resource name that contains a web address for locating the resource on the Web. The UML is an industry standard that defines a set of modeling languages for making various kinds of models and diagrams in support of object-oriented problem analysis and software design. Its core languages are Class Diagrams for information/data modeling, and Sequence Diagrams, Activity Diagrams and State Diagrams (or State Charts) for process/behavior modeling. |
| URN (Uniform Resource Name) User Agent | A URN refers to a resource without specifying its location. A user agent is a front-end web client program such as a web browser. |
| W |  |
| WebM | WebM is an open (royalty-free) web video format supported by Google Chrome and Mozilla Firefox, but not by Microsoft Internet Explorer and Apple Safari. |
| WHATWG (Web Hypertext Application Technology Working Group) | The WHATWG was established in 2004 by former employees of Apple, Mozilla, and Opera who have been unhappy with the slow progress of web technology standardization due to W3C’s choice to focus on the standardization of XHTML2\. Led by Ian Hickson, they developed HTML5 and related JavaScript APIs in competition and collaboration with the W3C. |
| WWW (World Wide Web) | The WWW (or, simply, “the Web”) is a huge client-server network based on HTTP, HTML and XML, where web browsers (and other ’user agents’), acting as HTTP clients, access web server programs, acting as HTTP servers. |
| W3C (World Wide Web Consortium) | The W3C is an international organization in charge of developing and maintaining web standards. |
| X |  |
| XHR (XML HTTP Request) | The XML HTTP Request (XHR) API allows a JavaScript program to exchange HTTP messages with back-end programs. It can be used for retrieveing/submitting information from/to a back-end program without submitting HTML forms. XHR-based approaches have been subsumed under the acronym “AJAX” in the past. |

# Index

*   accessibility [1](#12_chapter01.xhtml_chapter01_27)
*   Active Record [1](#17_chapter06.xhtml_chapter06_6)
*   Berners-Lee, Tim [1](#12_chapter01.xhtml_chapter01_1), [2](#12_chapter01.xhtml_chapter01_8)
*   boilerplate code [1](#14_chapter03.xhtml_chapter03_34), [2](#15_chapter04.xhtml_chapter04_61), [3](#20_chapter08.xhtml_chapter08_29)
*   code base architecture [1](#17_chapter06.xhtml_chapter06_1)
*   command binding [1](#17_chapter06.xhtml_chapter06_13)
*   CSS [1](#12_chapter01.xhtml_chapter01_16), [2](#14_chapter03.xhtml_chapter03_24)
*   data binding [1](#14_chapter03.xhtml_chapter03_36), [2](#15_chapter04.xhtml_chapter04_40), [3](#17_chapter06.xhtml_chapter06_13)
*   de-serialization [1](#14_chapter03.xhtml_chapter03_35)
*   deployment architecture [1](#17_chapter06.xhtml_chapter06_1)
*   ECMAScript [1](#12_chapter01.xhtml_chapter01_22)
*   Eich, Brendan [1](#12_chapter01.xhtml_chapter01_22)
*   facelets [1](#15_chapter04.xhtml_chapter04_10)
*   Hickson, Ian [1](#16_chapter05.xhtml_chapter05_20)
*   HTML [1](#12_chapter01.xhtml_chapter01_1)
*   – explicit labels [1](#14_chapter03.xhtml_chapter03_35)
*   – forms [1](#12_chapter01.xhtml_chapter01_14), [2](#14_chapter03.xhtml_chapter03_16), [3](#16_chapter05.xhtml_chapter05_28)
*   – form validation API [1](#19_chapter07.xhtml_chapter07_16), [2](#20_chapter08.xhtml_chapter08_22)
*   – implicit labels [1](#12_chapter01.xhtml_chapter01_15), [2](#14_chapter03.xhtml_chapter03_35), [3](#19_chapter07.xhtml_chapter07_10)
*   – HTML[1](#12_chapter01.xhtml_chapter01_5) [2](#12_chapter01.xhtml_chapter01_8)
*   – HTML[1](#12_chapter01.xhtml_chapter01_7) [2](#12_chapter01.xhtml_chapter01_8)
*   IndexedDB [1](#14_chapter03.xhtml_chapter03_24)
*   information architecture [1](#17_chapter06.xhtml_chapter06_1)
*   integrity constraints [1](#19_chapter07.xhtml_chapter07_1)
*   Java [1](#15_chapter04.xhtml_chapter04_8)
*   – bean class [1](#15_chapter04.xhtml_chapter04_10)
*   Java EE [1](#15_chapter04.xhtml_chapter04_1)
*   – entity class [1](#15_chapter04.xhtml_chapter04_10)
*   –entity manager [1](#15_chapter04.xhtml_chapter04_19), [2](#15_chapter04.xhtml_chapter04_27)
*   – facelets [1](#15_chapter04.xhtml_chapter04_10)
*   – Java Persistence API [1](#15_chapter04.xhtml_chapter04_1), [2](#15_chapter04.xhtml_chapter04_10)
*   – Java Persistence Query Language [1](#15_chapter04.xhtml_chapter04_10), [2](#15_chapter04.xhtml_chapter04_22), [3](#15_chapter04.xhtml_chapter04_43)
*   – Java Server Faces [1](#15_chapter04.xhtml_chapter04_1), [2](#15_chapter04.xhtml_chapter04_10)
*   – validators [1](#21_chapter09.xhtml_chapter09_20)
*   JavaScript [1](#12_chapter01.xhtml_chapter01_22), [2](#13_chapter02.xhtml_chapter02_1)
*   – datatypes [1](#13_chapter02.xhtml_chapter02_1), [2](#20_chapter08.xhtml_chapter08_13)
*   – entity tables [1](#13_chapter02.xhtml_chapter02_20)
*   – enumerations [1](#23_chapter10.xhtml_chapter10_13)
*   – function definition [1](#13_chapter02.xhtml_chapter02_20)
*   – functions [1](#13_chapter02.xhtml_chapter02_20)
*   – immediately invoked function expression (IIFE) [1](#13_chapter02.xhtml_chapter02_23)
*   – implicit getters [1](#28_chapter14.xhtml_chapter14_1)
*   – implicit setters [1](#20_chapter08.xhtml_chapter08_28), [2](#24_chapter11.xhtml_chapter11_4)
*   – IndexedDB [1](#14_chapter03.xhtml_chapter03_24)
*   – localStorage [1](#13_chapter02.xhtml_chapter02_42)
*   – map [1](#13_chapter02.xhtml_chapter02_14), [2](#13_chapter02.xhtml_chapter02_18)
*   – methods [1](#13_chapter02.xhtml_chapter02_20)
*   – Object Notation (JSON) [1](#13_chapter02.xhtml_chapter02_41)
*   – objects [1](#13_chapter02.xhtml_chapter02_13)
*   – record [1](#13_chapter02.xhtml_chapter02_14)
*   – strict mode [1](#13_chapter02.xhtml_chapter02_13)
*   – type conversions [1](#13_chapter02.xhtml_chapter02_7), [2](#27_chapter13.xhtml_chapter13_35)
*   – type testing [1](#13_chapter02.xhtml_chapter02_5), [2](#25_chapter12.xhtml_chapter12_6)
*   – variable scope [1](#13_chapter02.xhtml_chapter02_7)
*   key [1](#19_chapter07.xhtml_chapter07_11)
*   Lie, Håkon W. [1](#12_chapter01.xhtml_chapter01_16)
*   Model-View-Controller (MVC) [1](#17_chapter06.xhtml_chapter06_16)
*   – mediating-controller MVC [1](#17_chapter06.xhtml_chapter06_16)
*   multiple validation problem [1](#20_chapter08.xhtml_chapter08_6)
*   MVVM [1](#17_chapter06.xhtml_chapter06_13)
*   namespace [1](#13_chapter02.xhtml_chapter02_14)
*   Object Constraint Language (OCL) [1](#19_chapter07.xhtml_chapter07_14)
*   Object-Relational Mapping (ORM) [1](#17_chapter06.xhtml_chapter06_6)
*   Onion Architecture [1](#17_chapter06.xhtml_chapter06_9)
*   onion principle [1](#17_chapter06.xhtml_chapter06_1)
*   primary key [1](#19_chapter07.xhtml_chapter07_12)
*   Resource Description Framework (RDF) [1](#16_chapter05.xhtml_chapter05_1), [2](#16_chapter05.xhtml_chapter05_11)
*   – RDF graph [1](#16_chapter05.xhtml_chapter05_14)
*   – RDF/XML syntax [1](#16_chapter05.xhtml_chapter05_14)
*   – RDFa [1](#16_chapter05.xhtml_chapter05_20)
*   responsive validation [1](#19_chapter07.xhtml_chapter07_1), [2](#24_chapter11.xhtml_chapter11_19)
*   serialization [1](#14_chapter03.xhtml_chapter03_35), [2](#24_chapter11.xhtml_chapter11_14)
*   Structured Query Language (SQL) [1](#15_chapter04.xhtml_chapter04_20)
*   TomEE [1](#15_chapter04.xhtml_chapter04_1)
*   Unicode [1](#12_chapter01.xhtml_chapter01_5), [2](#15_chapter04.xhtml_chapter04_13)
*   Unified Modeling Language (UML) [1](#16_chapter05.xhtml_chapter05_1)
*   Universal Business Language (UBL) [1](#27_chapter13.xhtml_chapter13_1)
*   URL-encoded [1](#12_chapter01.xhtml_chapter01_14), [2](#17_chapter06.xhtml_chapter06_13)
*   UTF-[8,0](#12_chapter01.xhtml_chapter01_15) [1](#12_chapter01.xhtml_chapter01_5), [2](#15_chapter04.xhtml_chapter04_17)
*   Web Ontology Language [1](#16_chapter05.xhtml_chapter05_1)
*   XML [1](#12_chapter01.xhtml_chapter01_1), [2](#12_chapter01.xhtml_chapter01_7), [3](#15_chapter04.xhtml_chapter04_31)
*   – default namespace [1](#12_chapter01.xhtml_chapter01_7)
*   – namespaces [1](#12_chapter01.xhtml_chapter01_5)
*   – valid [1](#12_chapter01.xhtml_chapter01_7), [2](#15_chapter04.xhtml_chapter04_44)
*   – well-formed [1](#12_chapter01.xhtml_chapter01_7), [2](#15_chapter04.xhtml_chapter04_33)
*   XML HTTP Request (XHR) [1](#15_chapter04.xhtml_chapter04_31)
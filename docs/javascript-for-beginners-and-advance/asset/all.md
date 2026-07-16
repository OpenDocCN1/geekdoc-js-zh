![](Image00256.jpg)

JAVASCRIPT FOR BEGINNERS AND ADVANCE

![](Image00000.jpg)

                                                                                        Johnkeats Arthur

  Copyright All Rights Reserved © 2015 Johnkeats Arthu r              

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

1 What is a Programming Language ?               5

Key Point s               5

2 Server-side vs. Client-sid e               7

Key Point s               7

3 About JavaScrip t               10

Key Point s               10

4 A Tour of JavaScrip t               13

Key Point s               13

Projec t               13

5 Objects, Properties and Method s               18

Key Point s               18

6 Assigning Values to Propertie s               21

Key Point s               21

Projec t               22

7 About Comment s               25

Key Point s               25

Projec t               26

8 Hiding Scripts from Older Browser s               28

Key Point s               28

Projec t               29

9 Automatically Redirecting the Use r               31

Key Point s               31

Projec t               31

10 Alert, Prompt and Confir m               33

Key Point s               33

Projec t               34

11 Variables and Operator s               35

Key Point s               35

Projec t               38

12 Comparison s               40

Key Point s               40

Projec t               41

13 Conditional s               42

Key Point s               42

Projec t               45

Project 2               46

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

14 Loopin g               48

Key Point s               48

Projec t               50

15 Array s               53

Key point s               53

Projec t               55

16 Associative & Objective Array s               57

Key Point s               57

Projec t               58

17 Two Dimensional Array s               59

Key Point s               59

Projec t               60

18 String Manipulatio n               61

Key Point s               61

Projec t               65

19 Using Function s               66

Key Point s               66

Projec t               69

20 Logical Operator s               71

Key Point s               71

Projec t               74

21 Using Event Handler s               75

Key Point s               75

Projec t               77

22 Working with Image s               79

Key Point s               79

Projec t               80

23 Simple Image Rollover s               81

Key Point s               81

Projec t               83

24 Object Instantiation and Better Rollover s               85

Key Point s               85

Projec t               86

25 Working with Browser Window s               88

Key Point s               88

Projec t               90

26 Positioning Browser Window s               91

Key Point s               91

Projec t               92

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

27 Focus and Blu r               93

Key Point s               93

Projec t               94

28 Dynamically Created Conten t               95

Key Point s               95

Projec t               95

29 Working with Multiple Window s               97

Key Point s               97

Projec t               98

30 Using an External Script Fil e               99

Key Point s               99

Projec t               100

31 Javascript and Form s               101

Key Point s               101

Projec t               103

32 Form Methods and Event Handler s               105

Key Point s               105

Projec t               106

33 JavaScript and Math s               108

Key Point s               108

Projec t               109

34 Object Variables – A Refreshe r               111

Key Point s               111

Projec t               112

35 Actions From Menu Item s               113

Key Point s               113

Projec t               114

36 Requiring Form Values or Selection s               116

Key Point s               116

Projec t               118

37 Working with Date s               121

Key Point s               121

Projec t               122

38 Retrieving Information from Date Object s               123

Key Point s               123

Projec t               124

39 Creating a JavaScript Cloc k               126

Key Point s               126

Projec t               128

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

1 What is a Programming Language?

Key Points

            A programming language is a set of codes that we can use to give a Computer Instructions to follow.

            Popular and well-known programming languages include Java, C++, COBOL, BASIC, LISP and more. Most popular programming languages consist of words and phrases that are similar in form to the English language.

            A well-written program will be easily readable by anyone with a little programming experience, regardless of whether they have any direct experience of the language in question. This is because modern programming languages share a large number of common concepts. In particular, they all have a notion of variables , arrays , loops , conditionals , and functions . We will meet these concepts again in more depth later in the course.

            Traditionally, programming languages have been used to write (for the most part) “stand-alone” applications. Things like Microsoft Word, Mozilla Firefox and Lotus Notes are all examples of such applications. Once installed on a PC, these applications run without necessarily requiring any other software to be installed alongside them.

            Web Applications differ from these traditional applications in many respects, but the most striking is that they all run inside your web browser . Examples of popular web applications are things like Google, Hotmail, Flickr, GMail and any of the vast array of “weblogging” systems.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            These applications are also written using programming languages, but as a rule they are built using multiple, interdependent technologies. These technologies are easily (though not completely) broken down into two categories: server-side and client-side .

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

2                                       Server-side vs. Client-side

Key Points

            The World Wide Web is built on a number of different technologies.

            For most users, the web starts and ends with their choice of web browser . The browser is said to define the client-side of the web, with the browser, the computer it is running on, and the user surfing the web being collectively referred to as the client .

            Consider a client who has decided to visit the web site at www.google.com . The first thing that happens is that the client will make a request to Google’s web server for the default page of that web site.

            The web server is an application running on a computer owned by Google. Like the client, the server application and the computer on which it runs define the server-side of the web, and are collectively referred to as the server .

            When the server receives the request from the client for a particular page, its job is to retrieve the page from the computer’s files and serve it back to the client. In many cases, this operation is a very simple procedure involving little or no work on the part of the server.

            However, using a programming language like PHP, Perl or Java, we can cause the server to either modify the page it finds before it passes it back to the client, or even to generate the page entirely from scratch. This is referred to as a server-side application. The page passed back to the client looks (to the client) exactly the same as any other page that has not been modified.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            An example of a server-side application might be to insert the current date and time into a page. This would mean that each time the page was requested (say, by using the browser’s refresh button), a new time value would be added to the page.

            Once the client has received the page from the server, it displays the page and waits for the user to request another page. As soon as the page reaches this state, it has moved beyond the control of the server. No server-side application can now alter the contents of the page without the client having to make another trip back to the server to get a new (and possibly updated) copy of the page.

            However, all modern browsers allow for the running of client-side applications. These are small applications which are embedded within the HTML code of the page itself.

            Server-side applications ignore any client-side applications that they find while modifying pages to send to the client, so in general the two types of application cannot easily “talk” to each other.

            However, once the client has received a client-side application, it can begin to modify the page dynamically , without the need to go back to the server.

            An example of a client-side application might be a clock on a web page that updated every second.

            An unfortunate side effect of client-side applications is that all the code must be sent to the client for running, which means that the application’s inner workings are available for anyone to see. This makes it impractical for checking passwords, or doing anything else that could cause confidential information to be released into the wild.

            In addition, all modern web browsers afford the user the opportunity to switch off client-side applications altogether. On top of this, the way the same client-side application is run will vary from browser type to browser type.

            Despite these drawbacks, client-side applications (or scripts , as they are better known due to their general brevity) remain the best way to provide web users with a rich environment when developing web applications.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            In short, the two technologies each have their strengths and weaknesses:

            Client-side scripts allow the developer to alter pages dynamically, and to respond to user actions immediately rather than having to wait for the server to create a new version of the page. However, there are security and cross-browser compatibility issues to be aware of, and these are often non-trivial.

            Server-side applications allow the developer to keep her code secure and secret, thus allowing for more powerful applications to be created. In addition, since the server running the code is always a known quantity, applications that run successfully in one browser will run successfully in all browsers. However, despite all this power, there is no direct way for a server-side application to alter a page without having to force the client-side to load another page. This makes it completely impractical for things like drop-down menus, pre-submission form checking, timers, warning alerts and so forth.

![](Image00000.jpg)

| JavaScript for Beginners |  |  |
|  |  |  |
|  |  |  |

3 About JavaScript

Key Points

            JavaScript is an interpreted, client-side, event-based, object-oriented scripting language that you can use to add dynamic interactivity to your web pages.

            JavaScript scripts are written in plain text, like HTML, XML, Java, PHP and just about any other modern computer code. In this code, we will use Windows NotePad to create and edit our JavaScript code, but there are a large number of alternatives available. NotePad is chosen to demonstrate JavaScript’s immediacy and simplicity.

            You can use JavaScript to achieve any of the following:

            Create special effects with images that give the impression that a button is either highlighted or depressed whenever the mouse pointer is hovered over it.

            Validate information that users enter into your web forms

            Open pages in new windows, and customise the appearance of those new windows.

            Detect the capabilities of the user’s browser and alter your page’s content appropriately.

            Create custom pages “on the fly” without the need for a server-side language like PHP.

            And much more…

![](Image00000.jpg)

| JavaScript for Beginners |  |  |
|  |  |  |
|  |  |  |

            JavaScript is not Java , though if you come from a Java background, you will notice that both languages look similar when written. Java is a full featured and comprehensive programming language similar to C or C++, and although JavaScript can interact with Java web applications, the two should not be confused.

            Different web browsers will run your JavaScript in different, sometimes incompatible ways. In order to work around this, it is often necessary to use JavaScript itself to detect the capabilities of the browser in which it finds itself, and alter its operation depending on the result.

            To revisit the original definition in this chapter, note the following points:

            Interpreted refers to the fact that JavaScript code is executed (acted on) as it is loaded into the browser. This is a change of pace from compiled languages like Java, which check your program thoroughly before running a single line of code, and can have many implications that can catch you out if you are from a non-interpreted programming background.

            Client-side has been defined already in the previous chapter.

            Event-based refers to JavaScript’s ability to run certain bits of code only when a specified event occurs. An event could be the page being loaded, a form being submitted, a link being clicked, or an image being pointed at by a mouse pointer.

            Object-oriented signals that JavaScript’s power to exert control over an HTML page is based on manipulating objects within that page. If you are familiar with object-oriented programming , you will be aware of some of the power that this can bring to the coding environment.

![](Image00000.jpg)

| JavaScript for Beginners |
|  |

            One final note: While JavaScript is a programming language, HTML (the language of the World Wide Web) is not . HTML is a Markup Language , which means that it can be used to mark areas of a document as having special characteristics like headers, paragraphs, images, forms and so on, but it cannot perform any logical processing on its own. So while JavaScript is often written alongside HTML, the rules of one do not necessarily have any bearing on the other.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

4 A Tour of JavaScript

Key Points

            Let’s start with a quick tour of the major features of JavaScript . This chapter is intended to be a showcase of what JavaScript can do, not an in depth investigation into the deeper concepts, so don’t worry too much if you get lost or don’t understand the code you’re typing in!

Project

            Our JavaScript is all going to be written using NotePad . Open NotePad and save the resulting empty document in your user drive as chapter_4.htm l .

            Begin by creating a basic HTML page in your blank document. It doesn’t have to be anything fancy – the following will be more than sufficient:

<html>

<head>

<title>Chapter 4: A Tour of ↵

JavaScript</title>

</head>

<body>

<h1>A Tour of JavaScript</h1>

</body>

</html>

            As a convention, when the notes intend that you should enter code all on one line, they will use an arrow as above ↵ to indicate that you should not take a new line at that point. With HTML, this is rarely important, but with JavaScript , a new line in the wrong place can stop your code from working.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Save your new webpage, and view it in your web browser. For the moment, use Internet Explorer to view this page. To do this, find your saved file on your user drive, and double-click on it. This will open the file in Internet Explorer by default, and let you see the header you’ve just created.

            So far, we haven’t done anything beyond the scope of HTML. Let’s add some JavaScript to the page.

            There are (generally speaking) three places in a web page where we can add JavaScript . The first of these is between a new set of HTML tags. These scrip t tags take the following form:

<script language=”JavaScript” ↵

type=”text/JavaScript”>

… code …

</script>

            The scrip t element above can be placed virtually anywhere you could place any element in an HTML page – in other words, in either the hea d element or the bod y element. It is most commonly placed in the former, though this is usually so that all your code can be easily found on the page.

            Note too that there is no arbitrary limit on the number of script elements that can be contained in an HTML page . There is nothing stopping you from having a hundred of these dotted around your pages, except perhaps prudence.

            Let’s add our opening and closing script tags to the head element of the page, like so:

<html>

<head>

<title> … </title>

<script language=”JavaScript” ↵

type=”text/JavaScript”>

</script>

</head>

…

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Save the file, and then try refreshing your page in the browser window. Note that nothing has happened. This is what we expected – all we have done so far is to set up an area of the page to hold our JavaScript .

            Go back to NotePad and enter the following text between the opening and closing scrip t tags:

window.alert(“Hello world!”);

            Save your changes, and again refresh your page in the browser window. Welcome to the world of JavaScript !

            Go back to notepad and remove the window.aler t line you just added. Now add the following, slightly more complex code:

if ( confirm(“Go to Google?”) ) { document.location = ↵

“http://www.google.com/”;

}

            Again, save your changes and refresh the page. For those with an eye to future chapters, this is an example of a conditional statement, where we ask JavaScript to check the condition of something (in this case, our response to a question) and then to alter its behaviour based on what it finds.

            Now, both of these bits of JavaScript have run uncontrollably when the page has loaded into the browser. In most cases, we will want to have more control over when our JavaScript does what we ask it to.

            This control is the domain of events . In a browser, every element of an HTML document has associated with it a number of events that can happen to it. Links can be clic k ed, forms can be submi t ted, pages can be loa d ed and so on.

            Modify the previous lines of JavaScript in your scrip t element to match the following:

function go_to_google() {

if ( confirm(“Go to Google?”) ) { document.location = ↵

“http://www.google.com/”;

}

}

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Be careful with your brackets here!

            Save and refresh, and note that nothing happens this time. This is because we have enclosed the previous action (popping up a question and acting on the response) within a function . A function is a block of code that is given a name – in this case, the name is go_to_google( ) – and is only run when that name is “called”. It can be useful to think of functions as magic spells that can be invoked when their name is said.

            To invoke this spell, we need to choose an element on the page to trigger it. A natural candidate is a link element, so add the following HTML to the bod y section of your page:

<p>A quick <a href=”#”>test</a>.</p>

            The # link is a common HTML trick that allows us to create a “link to nowhere”.

            Save and refresh, and check that the link appears on the page, and that it goes nowhere when clicked.

            Now, we want to have our page ask us if we want to “Go to Google?” when we click on that link. Here’s how

            Take the link element, and modify it as follows:

<a href=”#” onclick=”go_to_google();”>test</a>

            Save and refresh, and then click on the link. This is an example of an event handler . When the link is clicked ( onclic k ), our browser says the “magic words” go_to_google( ) , and our function is invoked.

            For our final trick, add the following code to the bod y section of the page, after the paragraph containing the link:

<body>

…

<script language=”JavaScript” ↵

type=”text/JavaScript”>

document.write(“<h2>Here’s another ↵ header!</h2>”);

</script>

            Note that the line of code should be all on one line!

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Save the page and refresh the browser. Note that we now have a new line of text on the page – another header! We’ve used JavaScript to create HTML and tell the browser to display it appropriately. In this example, JavaScript has done nothing that we couldn’t have done with a line of HTML, but in future chapters we will see how we can use this to write the current date and more.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

5 Objects, Properties and Methods

Key Points

            Generally speaking, objects are “things”. For example, a piano is an object .

            Properties are terms that can describe and define a particular object . Our piano, for example, has a colour, a weight, a height, pedals, a keyboard and a lid.

            Note from the above that an object’s properties can be properties themselves . So we have the case where a piano lid is a property of the piano, but is also an object in its own right, with its own set of properties – for example, the lid has a colour, a length, and even a state of either open or closed.

            If objects are the nouns of a programming language and properties are the adjectives, then methods are the verbs. Methods are actions that can be performed on (or by) a particular object. To continue our piano example, you could play a piano, open its lid, or press the sustain pedal.

            Many programming languages have similar ways of referring to objects and their properties or methods. In general, they are hierarchical , and an object’s relationship with its properties and methods, as well as with other objects, can often be easily seen from the programming notation.

            In JavaScript, we use a “dot notation” to represent objects and their properties and methods. For example, we would refer to our piano’s colour in the following way:

piano.colour;

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            If we wanted to instruct JavaScript to play the piano, we could write something as simple as:

piano.play();

            A clear example of object hierarchy could be seen if we decided to open the lid of the piano:

piano.lid.open();

            Or even more so if we wanted to press the sustain pedal of the piano:

piano.pedals.sustain.press();

            Note that in some of the examples above, we have brackets () after each set of words, and in some we don’t. This has to do with making sure that JavaScript can understand what we say.

            JavaScript works with objects throughout its existence in a web browser. All HTML elements on a page can be described as objects, properties or methods. We have already seen a few of these objects in our previous introductory chapter:

document.write(…);

document.location;

            In these examples, documen t is an object, while writ e is a method and locatio n is a property.

            In these lines, we see a clue about the use of brackets in these statements. We use brackets to signify to JavaScript that we are talking about an object’s method , and not a property of the same name.

            Brackets also allow us to pass certain extra information to an object’s method. In the above example, to write the text “Hello world!” to a web page document, we would write the following JavaScript:

document.write(“Hello World”);

            Each method can do different things depending on what is put in the brackets (or “passed to the method as an argument”, to use the technical term). Indeed, many methods can take multiple “arguments” to modify its behaviour. Multiple arguments are separated by a comma (,).

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            A JavaScript instruction like those shown here is referred to as a JavaScript statement . All statements should end in a single semi-colon (;). JavaScript will often ignore missed semi-colons at the end of lines, and insert the semi-colon for you. However, this can cause some unexpected results. Consider the following:

document.write(“<h1>

Hello World!

</h1>”);

            In many other languages, this would be acceptable. However, JavaScript will often interpret something like this as the following:

document.write(“<h1>;

Hello World!;

</h1>”);

            This interpretation will generate an error, as JavaScript will complain if you end a statement without ensuring that any terms between quotes have matching pairs of quotes. In this example, the first line’s “statement” is cut short, and JavaScript will fall over.

            For this reason, it is recommended that all your statements should end with semi-colons.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

6 Assigning Values to Properties

Key Points

            While objects and methods allow us to do things on a page, such as alter the content or pop up dialogue boxes to interact with the user, in many cases we will want to alter the value of one of an object’s properties directly. These cases are akin to painting our piano green.

            Given our discussion on methods so far, we might expect to be able to alter our object’s properties by using a method – for example, the following would seem logical:

piano.paint(“green”);

            In many cases, that is exactly what we will do. However, there are two drawbacks here. The first is that, within this course, the majority of objects that we discover are built into and defined by our browser. If we rely on using a method to alter an object’s property, we are also relying on the fact that the method exists in the first place.

            A much more direct way to solve this problem is to access the object’s properties directly. For example:

piano.colour = “green”;

            Here we are no longer using a method to perform an action, we are using what is known as an operator . In this case, the operator has the symbol “=”, and is known as the assignment operator .

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Within JavaScript, we can use this operator to great effectiveness. For example, we could alter the title element of a document (the text that is displayed in the top bar of the browser’s window) dynamically. This could be done when a user clicked on a part of the page using an event handler (more later on this), or could be set to automatically update each minute to show the current time in the page title. The code we would use for this task is simple:

document.title = “a new title”;

            There are many assignment operators in JavaScript. Some of the more common are shown in the table below:

| Assignment | Function |
|  |  |
| x = y | Sets the value of x to y |
|  |  |
| x += y | Sets the value of x to x+y |
|  |  |
| x -= y | Sets the value of x to x-y |
|  |  |
| x *=y | Sets the value of x to x times y |
|  |  |
| x /=y | Sets the value of x to x divided by y |
|  |  |

            Not all assignment operators work with all types of values. But the addition assignment operator works with both numbers and text. When dealing with numbers, the result will be the sum of the two numbers. When dealing with text (technically called strings ), the result will be the concatenation of the two strings:

document.title += “!”;

will cause the symbol “!” to be appended to the end of the current document title.

Project

            Open your previous project file, and save it under the name

chapter_6.htm l .

            Remove any existing JavaScript from your script tags, but leave the tags in place ready for some new JavaScript.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Use your text editor to change the value of the title element of the page as follows, then load your page into a browser and view the result:

<title>With a little help from</title>

            Now, add a statement to our script element to add the following text to the end of the current title:

”JavaScript for Beginners!”;

            Reload the page in your browser and note the title bar of the window.

            If the display looks odd, consider your use of spaces…

            All we have so far is an example that does nothing more than HTML could manage. Let’s introduce a new method of the window object to help us to add a little more dynamism and interaction to the script. Change the value of the title tag as follows:

<title>Chapter 6: Assigning Values to Properties</title>

            Now, remove your previous JavaScript statement and insert the following:

document.title = ↵ window.prompt(“Your title?”, “”);

            Reload your page and consider the result.

            We have come across the window object before. Our demonstration of the alert method in chapter 4 could have been more properly written as:

window.alert(“message”);

In many cases, we can omit certain parts of our object/property/method hierarchy when writing our code. We will discuss this again later.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            To understand what is going on with our prompt method, we can write down a method prototype . This is a way of describing a method’s arguments in such a way that their effect on the method is more self explanatory. A prototype for the prompt method of the window object might look like the following:

window.prompt( message , default_response );

            So, we can see that the first argument defines the text that appears as the question in the prompt dialogue box. The second argument is a little less clear. Try your code with different values and see what difference your changes make.

            Finally, we note that this prompt method somehow takes the information typed into the box and passes it to our JavaScript assignment. Say someone typed “Hello World” into the box. It would have been as if our assignment had actually been:

document.title = “Hello World”;

            When this sort of passing of values occurs, it is said that the method has returned the value passed. In this case, we would say that “the prompt method has returned the value ‘Hello World’”, or that “the return value of the prompt method was ‘Hello World’”.

            Return values will become very important when we deal with event handlers later on.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

7 About Comments

Key Points

            Repeat after me : Comments are important. Comments are important . Comments are important .

            Adding comments to your code is always good practice. As the complexity of your scripts grows, comments help you (and others) understand their structure when you come to view the code at a later date.

            A lot of code created quickly is said to be “write only” code, as it suffers from an inherent lack of structure or commenting. Debugging such code, or reusing it months later, becomes maddeningly impossible as you try to remember what a certain line was supposed to do, or why using certain values seems to stop your code from working.

            Comments are completely ignored by JavaScript and have no effect on the speed at which your scripts run, provided they are properly formed.

    Comments can slow the loading of your page, however – many coders keep a “development” copy of their code fully commented for editing, and remove all comments from their code when they finally publish it.

            There are two types of comment in JavaScript – single line comments, and multi-line comments.

            Single line comments begin with two forward-slash characters (//), and end with a new line:

              this is a comment alert(“hello”); // so is this

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Single line comments in JavaScript can also use the HTML comment format that you may be familiar with:

<!-- this is a comment

alert(“hello”);

            Note two things: firstly, this use of the HTML comment format does not require a closing -- > tag. Secondly, this is only a one line comment, unlike its use in HTML, which comments all lines until the closing comment tag.

            You can add multiple-line comments by enclosing the comment block between /* and */. For example:

/* all of this text is going to be ignored by JavaScript. This allows us to write larger comments without worrying about having to individually “comment out” each line */

alert(“Hello World”);

/* a one line, “mult-line” comment */

            As well as adding narrative to your script, you can use comments to remove code from your pages without having to delete the code. For example:

              this was the old message

              alert(“Hello World”);

              and this is the new message

alert(“Hello everyone!”);

            This can be very useful if you are trying to track down an error in your code – you can “comment out” each suspect line in turn until you manage to get your code working again.

Project

            Open your previous project file, and save it under the name

chapter_7.htm l .

            Add the single line comment

This is my first comment

to the beginning of your script.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

    Add a multi-line comment to your script, replacing your previous single line comment. The multi-line comment should describe what your script does at present.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

8 Hiding Scripts from Older Browsers

Key Points

            Very old browsers don’t understand JavaScript. There are very few such browsers in use today, but two factors force us to continue to consider environments that may not be able to cope with our JavaScript code.

            Firstly, all modern browsers allow users to control whether JavaScript code will be run. In many cases, users will not have any say over their company policy, and may not even know that their work machine has had JavaScript disabled.

            Secondly, not all of your visitors will be using browsers that can make any use of JavaScript. Braille displays, screen readers and other non-visual browsers have little use for many JavaScript tricks. In addition, search engines like Google will ignore any JavaScript you use on your pages, potentially hiding important content and causing your pages to remain un-indexed.

            Browsers that don’t support JavaScript are supposed to ignore anything between the opening and closing script tags. However, many break this rule and will attempt to render your code as HTML, with potentially embarrassing consequences.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            However, we can use the fact that <!- - denotes a single line comment in JavaScript but a multi-line comment in HTML to ensure that our code is seen by a JavaScript-savvy browser, but ignored as commented-out HTML by anything else:

<script>

<!-- hide from older browsers

… your code

              stop hiding code --> </script>

            This prevents older browsers from displaying the code, but what if we want to replace this with some comment. For example, let’s say we had a bit of code that displayed the time of day and greeted our user by name. Without JavaScript and using the method above, there would simply be a blank on the page where the greeting should have been.

            We can use the <noscript> tag to cause our code to “fail gracefully” where JavaScript has been disabled or is unavailable. The contents of this element will be ignored where JavaScript is understood, and displayed anywhere else. For example:

<noscript>

<h1>Welcome to our site!</h1>

</noscript>

<script>

<!-- hide from older browsers

… code to customise header

              stop hiding code --> </script>

Project

            Open your previous project file, and save it under the name

chapter_8.htm l .

            Add two lines to your code to ensure that it will not confuse older browsers or browsers where the user has disabled JavaScript.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Add a noscript element to explain what your JavaScript does. It is generally considered “bad form” to instruct your user to “upgrade to a better browser”, as this can insult many people who use assistive devices – consider this form of advice to be similar to the advice that tells a blind person “to get some glasses”.

            Instead where possible you should use the noscript element to provide content that adequately replaces the scripted content with a suitable replacement. For example, if you use your JavaScript to build a navigation panel on your page, the noscript element should contain a plain HTML list that does the same job.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

9 Automatically Redirecting the User

Key Points

            We have already briefly seen the use of browser redirection in chapter 4.

            To formulate the idea more completely, in order to redirect the user to a different page, you set the location property of the document objects.

            As we saw in chapter 6, we can use the assignment operator here. For example:

document.location = “http://www.bbc.co.uk/”; document.location = “chapter_4.html”;

Project

            Open your previous project file, and save it under the name

chapter_9_redirect.htm l .

            Save another copy of the file, this time called

chapter_9.htm l .

            Make sure both files are saved in the same folder, and that you have chapter_9.htm l open in your editor.

            Remove all script from between the script tags, except for your browser hiding lines. Make sure that the script tags are still in the head section of the page.

            Now, add a single statement to this script that will

automatically redirect the user to the page

chapter_9_redirect.html as soon as the page is loade d into a browser.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Finally, add a header tag to the body section of the page containing the text “You can’t see me!”.

            Close this page, don’t check it in a browser yet, and open the page chapter_9_redirect.htm l in your editor.

            Remove all JavaScript from this page (including your script tags) and ensure that only HTML remains on the page.

            Add a header tag to the body section of the page containing the text “But you can see ME!”.

            Save this page, and load the page chapter_9.htm l into your browser.

            Experiment with various positions for the script tags on chapter_9.html to see if you can make the header appea r before the redirection.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

10 Alert, Prompt and Confirm

Key Points

            So far, we have seen brief examples of alert , prompt and confirm dialogue boxes to request a response from the user, and to pause all code in the background until the request is satisfied.

            All of these boxes are the result of methods of the window object. This object is the highest level object that JavaScript can deal with in a browser. As such, all other objects on a page (with a few exceptions) are actually properties of the window object.

            Because of this ubiquity, its presence is assumed even if it is omitted. Thus, where we technically should write:

window.document.write(“…”);

it is equally valid to write:

document.write(“…”);

as we have been doing.

            Similarly, instead of writing:

window.alert(“…”);

we can happily write:

alert(“…”);

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            The prototypes of the three methods are:

window.alert( message );

window.confirm( message );

window.prompt( message, default_response );

            Alert will always return a value of “true” when it is cleared by clicking “ok”.

            Confirm will return either “true” or “false” depending on the response chosen to clear the box.

            Prompt will return either the value typed in, “null” if nothing is typed in, and “false” if the box is cancelled.

Project

            Open your previous project file, and save it under the name

chapter_10.htm l .

            Clear the previous redirection code, and ensure that the script tags have been returned to the head section of the document.

            Add a new statement to the script on the page that will display the following message before the rest of the page is shown:

Welcome to my website! Click OK to continue.

            Check your page in your browser.

            We will use alert , confirm , and prompt throughout this course. Take a moment to try each of them in turn on this page, each time stopping to review your changes.

            Use the write method of the document object to check the return values of each method. For example:

document.write(alert(“hello world”));

Make sure that you place this particular snippet of code in script tags within the body area of the page, as we are generating text output to be rendered by the browser. Also, note the use (or not) of quotes here. More next chapter!

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

11 Variables and Operators

Key Points

            We have been introduced to the concepts of objects and their various properties and methods . These inter-related concepts allow any web page to be broken down into little snippets of information or data , which can then be accessed by JavaScript and, in many cases, changed.

            However, what if we want to create our own storage space for information that doesn’t necessarily have a page-based counterpart? For example, what if we wanted to store the previous value of a document’s title property before changing it, so it could be retrieved later, or if we wished to store the date time that the page was loaded into the browser for reproduction in several places on the page, and didn’t want to have to recalculate the time on each occasion?

            Variables are named containers for values within JavaScript. They are similar to object properties in many ways, but differ importantly:

            In a practical sense, variables have no “parent” object with which they are associated.

            Variables can be created (“declared”) by you as a developer, and can be given any arbitrary name (within certain rules) – object properties, however, are restricted by the definition of the parent object. It would make no sense, for example, for our piano object in the previous chapters to have a propeller property!

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Variable name rules are straightforward – no spaces, names must start with a letter. Examples of valid variable names are:

BrowserName page_name Message1

MESSAGE1

            In many browsers, JavaScript is case-sensitive , which means that the last two variables in the example above are distinct variables . It is a good idea to pick a particular naming style for your variables, and to stick to it within your projects.

            At the simplest level, variables can store three different types of value:

            Numbers

e.g. 1.3324, 3.14159, 100000, -8 etc.

            Strings

e.g. “JavaScript for Beginners, week 3”, “Hello World” etc.

            Boolean Values e.g. true, false

            Note that strings can contain numbers, but the following variable values are not equivalent:

1.234 and “1.234”

The latter is a string value . This becomes important. Consider:

1+2 = 3

“a” + “b” = “ab”

“1” + “2” = “12”

            Some developers use their own naming convention with variable names to denote the type of value expected to be contained in a given variable. This can often be helpful, but is in no way required by JavaScript (c.f. JavaScript comments)

            For example, strMessage might indicate a string variable, where numPageHits might indicate a numerical value in the variable.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Variable assignment is accomplished in the same way as object property assignment. When a variable is assigned a value for the first time, it is automatically created. This is different from other programming languages, where a variable must be created explicitly first, before it can be loaded with a value.

            Some examples of variable assignment follow:

numBrowserVersion = 5.5;

numTotal += 33;

Message = “Hello!”;

Message = “Goodbye”;

Message = 3;

            Note that the last three examples show that variable values can be altered after their initial assignment, and also that the type of value stored in a variable can be altered in a similar manner.

            Once a variable has been created and a value stored within, we will want to be able to access it and perhaps manipulate it. In a similar manner to object properties, we access our variables simply by calling them:

Message = “Hello World!”;

alert(Message);

            Note that we do not use quote marks around our variable names. The above code is different from:

alert(“Message”);

for hopefully obvious reasons.

            As well as using variables for storage and access, we can combine and manipulate them using operators . For example:

| a = 12; |  |  |  |
| b = 13; |  |  |  |
| c = | a + | b; // c | is | now 25 |
| c | += a; | // c is | now 37 |
| c | = | b + | “ Hello!”; | // c is now “13 Hello!” |
|  |  |  |  |  |  |
|  |  |  |  |  |  |

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Our last example may have been unexpected – we added a number to a string and got a string as a result. JavaScript is smart enough to realise that a number cannot be “added” to a string in a numerical sense, so it converts the number temporarily to a string and performs a concatenation of the two strings. Note that b remains 13 , not “13” .

            A table of operators:

| Operator | Function |
|  |  |
| x + y | Adds x to y if both are numerical – |
|  | otherwise performs concatenation |
|  |  |
| x – y | Subtracts x from y if both are numerical |
|  |  |
| x * y | Multiplies x and y |
|  |  |
| x / y | Divides x by y |
|  |  |
| x % y | Divides x by y, and returns the remainder |
|  |  |
| -x | Reverses the sign of x |
|  |  |
| x++ | Adds 1 to x AFTER any associated |
|  | assignment |
|  |  |
| ++x | Adds 1 to x BEFORE any associated |
|  | assignment |
|  |  |
| x-- | Subtracts 1 from x AFTER any associated |
|  | assignment |
|  |  |
| --x | Subtracts 1 from x BEFORE any associated |
|  | assignment |
|  |  |

Project

            Open your previous project file, and save it under the name

chapter_11.htm l .

            Clear the previous JavaScript code, and ensure that the script tags are contained in the body section of the document.

            Assign the message

“Welcome to my web site”

to a variable called greetin g .

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Use this variable to create an alert box containing the message, and also to produce a header on the page without having to retype the message.

            Test this page in your browser.

            Now, modify your code to create two variables, var_ 1 and

var_ 2 .

            Assign the value “Welcome to” to var_ 1 , and the value “my web site” to var_ 2 .

            Create a third variable var_ 3 , and assign to it the value of var_1 + var_ 2 . Then use an alert box to check the resultan t value of var_ 3 .

            Test this page in your browser.

            If the text in the alert box does not appear as expected, consider the use of spaces in the variable assignments, and correct the error.

            Now, modify your code to produce the same result but without requiring a third variable.

            Clear all statements from the current script tags.

            Add two statements to the script which assign the numbers 100 to one variable an d 5.5 to another.

            Use document.writ e to show the effects of each of the operators given in the table on page 34 on the two numerical values.

            Substitute one of the numerical values for a text string and repeat the procedure. Note the differences.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

12 Comparisons

Key Points

            Comparison operators compare two values with each other. Most commonly, they are used to compare the contents of two variables – for example we might want to check if the value of var_1 was numerically greater than that o f var_ 2 .

            When you use a comparison operator, the value that is returned from the comparison is invariably a Boolean value of either tru e or fals e . For example, consider the following statements:

var_1 = 4;

var_2 = 10;

var_3 = var_1 > var_2;

In this case, the value of var_ 3 is false. Note that the Boolean value of false is not the same as the text string “false ” :

var_4 = false; // Boolean value

var_5 = “false”; // Text string

            Common comparison operators are given below:

|  | Comparison | Function |  |
|  |  |  |  |
|  | X == y | Returns true if x and y are equivalent, false |  |
|  |  | otherwise |  |
|  |  |  |  |
|  | X != y | Returns true if x and y are not equivalent, |  |
|  |  | false otherwise |  |
|  |  |  |  |
|  | X > y | Returns true if x is numerically greater than |  |
|  |  | y, false otherwise |  |
|  |  |  |  |
|  |  |  |  |

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

| X >= y | Returns true if x is numerically greater than |
|  | or equal to y, false otherwise |
|  |  |
| X < y | Returns true if y is numerically greater than |
|  | x, false otherwise |
|  |  |
| X <= y | Returns true if y is numerically greater than |
|  | or equal to x, false otherwise |
|  |  |

            To reverse the value returned from a comparison, we generally modify the comparison operator with a ! (a “bang”). Note that in many cases this is not necessary, but can aid comprehension:

var_1 !> var_2;

var_1 <= var_2;

both of these are equivalent, but one may make more semantic sense in a given context than the other.

Project

            Open your previous project file, and save it under the name

chapter_12.htm l .

            Ensure that your two variables both have numerical values in them and not strings.

            Use an alert box to display the result of a comparison of your two variables for each of the comparison operators listed above.

            Substitute one of the numerical values for a text string and repeat the procedure. Note the differences.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

13 Conditionals

Key Points

            Up until now, our JavaScript projects have been unable to alter their behaviour spontaneously. When a page loads with our JavaScript embedded within, it is unable to do anything other than what we expect, time and again.

            The only difference we have seen is in the use of a prompt box to alter what is shown on a page. However, the page essentially does the same thing with the text provided, regardless of what text is typed in.

            What would be really handy would be to give JavaScript a mechanism to make decisions. For example, if we provided a prompt box asking the visitor for their name, it might be nice to have a list of “known names” that could be greeted differently from any other visitors to the site.

            Conditional statements give us that ability, and are key to working with JavaScript.

            A conditional statement consists of three parts:

            A test (often with a comparison operator, or comparator ) to see if a given condition is true or false .

            A block of code that is performed if and only if the condition is true .

            An optional block of code that is performed if and only if the condition is false .

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            These three parts are represented in JavaScript as follows:

if ( conditional_test )

{

JavaScript statement;

JavaScript statement;

JavaScript statement;

…

}

else

{

JavaScript statement;

JavaScript statement;

JavaScript statement;

…

}

            Everything from the first closing curly bracket (or brace ) is optional, so the following is also a valid conditional prototype:

if ( conditional_test )

{

JavaScript statement;

JavaScript statement;

JavaScript statement;

…

}

            In this case, if the conditional_tes t does not return true , nothing happens.

            An example of complete conditional statement is as follows:

if ( var_1 > var_2 )

{

alert(“Variable 1 is greater”);

}

else

{

alert(“Variable 2 is greater”);

}

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Note that the above condition is not necessarily always correct. Consider the case where var_ 1 is equal to var_ 2 . In that case, the above code will produce the message that “Variable 2 is greater”, since var_1 > var_ 2 returns false . In this case, we want to add an additional condition to the els e branch of code:

if ( var_1 > var_2 )

{

alert(“Variable 1 is greater”);

}

else

if ( var_1 < var_2 )

{

alert(“Variable 2 is greater”);

}

            In this case, equality will produce no output, as neither of the conditions will return true. For completeness, we could add a final else branch to the statement:

if ( var_1 > var_2 )

{

alert(“Variable 1 is greater”);

}

else

if ( var_1 < var_2 )

{

alert(“Variable 2 is greater”);

}

else

{

alert(“The variables are equal”);

}

            Note that in this case, we don’t have to check for equality in the final branch, as if var_ 1 is neither greater than nor less than var_ 2 , then – numerically at least – the two must be equal.

            We can continue adding as many else if statements as required to this stack.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            If you only have one statement following your conditional test, the braces may be omitted:

if ( var_1 > var_2 )

alert(“Variable 2 is greater”);

However, if you later want to add further statements to this conditional branch, you will have to add braces around the block, and this can lead to confusion. It is recommended that you use braces to enclose all blocks of conditional code.

            Consider the following block of code:

if ( var_1 > 4 )

{

var_2 = var_1;

}

else

{

var_2 = 4;

}

            This code is rather long, but achieves comparatively little – var_2 is equal t o var_1 o r 4 , whichever is greater.

            A more compact way of writing this could be:

var_2 = 4;

if ( var_1 > var_2 )

{

var_2 = var_1;

}

            However, an even more compact way of writing this could be to use the ternary operator :

var_2 = (var_1 > 4) ? var_1 : 4;

            In the above statement, the conditional is evaluated and, if true, the value returned is the value between ? and : symbols, or if false, it is the value between the : and ; symbols.

Project

            Open your previous project file, and save it under the name

chapter_13.htm l .

            Clear all JavaScript code from your script tags.

            Create two variables and assign numerical values to them.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Use a conditional statement to show alert boxes declaring which variable is the greater of the two.

            Consider the following code:

var_3 = (var_1 > var_2);

            Use this code in your script to simplify your conditional checking code.

            Now, use a prompt box to ask your visitor their name. Assign this name to var_ 3 .

            Check to see if the name typed in is your own name. If it is, use document.writ e to display a personalised greeting on the page. Otherwise, display a generic greeting.

            Use multiple else if branches to check the typed name against the names of some of your friends. Create personalised messages for all of them.

            There may be a way to simplify your conditional greeting code to use only one document.writ e statement. See if you can

figure out how. Hint – how might you use a variable called greetin g ?

Project 2

            In many cases, the brevity of your conditional statements will rely on your ability to formulate the right “questions” to consider when performing your tests. Try to make your solution to the following problem as concise as possible.

            Clear all of your current code from the script tags.

            Ensure that your script tags are currently situated in the body section of the page.

            Create a variable called exam_resul t and store a numerical value of between 0 and 10 0 in it.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Use an i f statement and multiple else i f statements to check the value of this variable against the following exam grading scheme, and print out the appropriate message to the page:

| Exam Result | Result Message |
|  |  |
| 90 or more | Excellent. Pass with Distinction. |
|  |  |
| Between 70 and 89 | Well Done. Pass with Honours |
|  |  |
| Between 55 and 69 | Just passed. |
|  |  |
| 54 or below | Failed. Do better next time. |
|  |  |

            Test your result in your browser. Vary the value of

exam_result and check the value shown in the browser. Fo r extra practise, try to use a prompt box to make changes to your exam_result variable as easy to achieve as possible.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

14 Looping

Key Points

            The letters i , j and k are traditionally used by programmers to name variables that are used as counters. For example, at different stages of the program, i may contain the numbers 1, 2, 3 etc.

            In order to achieve a “counting” effect, you will need to increment or decrement the value of your counting variable by a set value. Here are some examples:

i = i + 1;

i = i - 1;

i = i + 35;

incr = 10

i = i + incr;

            To keep things concise, we can use the following shortcuts:

i++; // equivalent to i = i + 1;

i--; // equivalent to i = i + 1;

            Counting in JavaScript, like many other programming languages, often begins at zero .

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            In many cases, this makes a lot of sense, as we will see. However, it can often cause confusion. Consider starting at 0 and counting up to 10\. In that case, we may have actually counted 11 items:

                                    (1)

                                    (2)

                                    (3)

                                    (4)

                                    (5)

                                    (6)

                                    (7)

                                    (8)

                                    (9)

10 (11!)

            If you wanted to give an instruction to someone to perform a repetitive action, you might say that you wanted them to continue the action for a certain number of times. If someone were performing an action 300 times, for example, they might do something like the following to ensure that their count was accurate:

            Write the number 1 on a bit of paper.

            After each action, erase the number on the bit of paper and increment it by 1.

            Before each action, check the number on the bit of paper. If it is less than or equal to 300, perform the action.

            Alternatively, they might decide to start counting at 0\. In this case, the procedure would be identical, but the check before each action would be to make sure that the number was strictly less than 300.

            In JavaScript, we say almost the same thing. The following code will display the numbers 1 to 100 on the page:

for

{

( i = 1; i <= 100; i++ )

document.write(“<p>” + i “ </p>”);

}

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            The for statement tells the browser that we are about to perform a loop . The layout here is very similar to a conditional statement, but in this case we have much more information in the brackets. Where our conditional had one JavaScript statement to describe its action, a for loop has three:

            An initialiser – this sets up the initial counting condition, in this case i = 1 .

            A conditional – this is identical to our conditional statements earlier, and must return true or false . If it returns true , the loop continues, otherwise it exits.

            An incrementer – this defines the action to be performed at the end of each loop. In this case, i is incremented by a value of 1.

            The key difference between a conditional and a for loop is that the condition is constantly being changed and re-evaluated. It is possible to create an infinite loop by making the conditional non-reliant on the count value – for example:

for ( i=0; 5 > 4; i++ )

will always perform the script in the braces, and will probably cause errors in the browser.

            Note too that it is very common to start counting at zero in JavaScript. The reason for this is that it is often desirable to count how many times an operation has been performed.

Consider the following:

for ( i=1; 1 < 2; i++ )

            In this case, the loop will run once, but the value of i will be 2, as after the first run, i will be incremented to 2, and will then fail the test and so the loop will exit. If we use the following:

for ( i=0; 1 < 1; i++ )

Then the loop will run once, and the value of i afterwards will be 1, as we might hope.

Project

            Open your previous project file, and save it under the name

chapter_14.htm l .

            Clear all JavaScript code from your script tags.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Write a series of statements to produce a multiplication table as follows:

![](Image00001.jpg)

            The following exercise is more of an HTML example, but demonstrates an important facet of using JavaScript (or, indeed, any programming language) to produce well-formatted text.

            Modify your previous code to make your page’s content appear in the centre of the page. Put your multiplication table in an HTML table to make sure that the equals signs, multiplication signs and so forth line up in neat columns:

![](Image00000.jpg) ![](Image00002.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            As a hint, here is a look at the table cells involved:

![](Image00000.jpg) ![](Image00003.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

15 Arrays

Key points

            In many cases, variables will completely satisfy our data storage needs in JavaScript. However, in a large number of cases, we may wish to “group” variables into a collection of related items.

            Take, for example, days of the week. In each day we perform a number of tasks, so we could want to record each task as a separate item under a group called, say, Monday’s Tasks.

            In JavaScript, to achieve this we would store each task in a separate variable, and then group those variables together into an array .

            An array is a special type of JavaScript object that can store multiple data values – unlike a variable, which can only store one data value at a time.

            It could be helpful to think of an array as a row of mail boxes in an office, just as you might think of a variable as a single, solitary mail box.

            The boxes in an array are numbered upwards, starting at box number 0 – note that counting begins at 0 here, just as we discussed in the previous chapter. The number assigned to each box is known as its index .

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            In order to use an array in JavaScript, you must first create it. There are a number of ways to create arrays in JavaScript. The simplest follows:

arrDays = new Array();

This statement creates a new, empty array called arrDays. We can call arrays just like we can variables, but with a few minor adjustments.

            If you already know how many elements a given array will have, you can declare this explicitly:

arrDays = new Array(7);

This modification creates an array with 7 empty boxes. However, arrays will expand and contract to the required size in JavaScript, so the cases where you will need to state the size of the array are rare.

            More useful, however, is the ability to “fill” the boxes of an array when you create it. For example:

arrDays = new Array(“Monday”,”Tuesday”);

We now have an array with two elements. The first (element 0) has a value of “Monday”, while the second (element 1) has a value of “Tuesday”. We need not restrict ourselves to string values in arrays – Boolean, numerical and string values are allowed, as in arrays. It is even possible to assign other arrays to array elements – more on this later.

            The most often-used way of creating an array is to use “square bracket” notation. Square brackets play a large role in the use of arrays, so this is often the easiest method to remember:

arrDays = [“Monday”,”Tuesday”];

This is identical to the previous example.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            To access an array’s elements, we first call the array’s name, and then specify the number of the element in square brackets, like so:

alert(arrDays[0]);

Note the lack of quotes around the 0 here. This line of code is equivalent to:

alert(“Monday”);

assuming the array is defined as in the previous examples.

            Not only can we access the value of an array element using this notation, but we can also assign the value as well:

arrDays[2] = “Tuesday”;

arrDays[3] = “Wednesday”;

            If you wish to add an element to an array without knowing the index of the last element, you can use the following code:

arrDays[] = “some other day”;

            As we will see, arrays are actually just special JavaScript objects, and have properties and methods associated with them. The most important property that every array has is its length property:

how_many_days = arrDays.length;

            As well as properties, arrays have very useful methods. If you wished to sort your array alphanumerically, you could use the array’s sort method thus:

arrDays.sort();

Note that the sort method works on the actual array itself, over-writing the current values. So, if you had an array with each day of the week as an element, calling its sort method would mean that arrDays[0 ] was then equal to “Friday”, not “Monday”.

Project

            Open your previous project file, and save it under the name

chapter_15.htm l .

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Clear all JavaScript code from your script tags.

            Write a few JavaScript statements that will present the months of the year on the page in alphabetical order. You should use the following technique to achieve this:

            Store the names of the months of the year in an array.

            Use an array method to sort the array elements alphanumerically.

            Use a for loop to iterate through each array element in turn, and print the value of the element to the screen (hint, consider the use of array[i ] , where i is the for loop’s counter).

            The above method (the use of a for loop to iterate through a series of array elements) is one of the first common programming techniques we have discussed in this course. Its usefulness cannot be overstated, as it allows us to perform repetitive tasks on a series of related elements without necessarily knowing what those elements might be when we wrote the code . It can be applied to form elements, cookies, page elements, pages, windows, and just about any other collection of object that you might wish to manipulate with JavaScript.

            To reinforce this generalism, if you have not used the array.length value in your loop, consider its use now. T o prove that you have created a more generic loop, try the code with an array of days instead of an array of months, and see if you have to change any of the looping code.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

16 Associative & Objective Arrays

Key Points

            We have already seen that we can access array elements by their index:

arrDays = [“Monday”, “Tuesday”];

              print “Monday” to the page document.write(arrDays[0]);

            However, it might be more useful to be able to name our array elements. By default, an array will be created as a numeric array. We can also create an associative array:

arrDays = new Array();

arrDays[“Monday”] = “Go to the dentist”; arrDays[“Tuesday”] = “Attend JavaScript class”;

arrDays[“Wednesday”] = “JavaScript homework”;

              remind you of Wednesday’s task alert(arrDays[“Wednesday”]);

            This looks a lot like our previous discussion of objects and properties. In fact, since an array is actually an object, we can access its elements as though they were properties:

// remind you of Wednesday’s task alert(arrDays.Wedensday);

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Note a subtle difference here – in our previous, numeric array examples, the names of the week days were the values of our array elements. Here, the names of the week days are the indexes of our elements. Avoid the following common error:

arrDays = [“Monday”,“Tuesday”];

arrDays[“Monday”] = “Go to work”;

              this is actually equivalent to arrDays = new Array();

arrDays[0] = “Monday”;

arrDays[1] = “Tuesday”;

arrDays[“Monday”] = “Go to work”;

// and arrDays.length is now 3, not 2

Project

            Open your previous project file, and save it under the name

chapter_16.htm l .

            Clear all JavaScript code from your script tags.

            Write a new script which creates a new, seven element associative array called Week:

            Use the days of the week as indexes for each element of the array.

            Assign a task to each day of the week as each associative element is created.

            Use a for loop to display a calendar on the page, as follows:

Monday: task

Tuesday: task

etc…

            Modify your code to use a prompt box to ask the visitor to choose a day, and display on the page the task allotted to that day.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

17 Two Dimensional Arrays

Key Points

            Referring back to our mailbox analogy, where our array could be pictured as a row of mailboxes, each with its own contents and label, a two dimensional array can be thought of as a series of these rows of mailboxes, stacked on top of each other.

            In reality, a two dimensional array is simply an array in which each element is itself an array. Each “sub array” of a two dimensional array can be of a different length – in other words, the two dimensional array doesn’t have to be “square”.

            You can access the contents of each sub array by using two pairs of square brackets instead of just one. An example will illustrate this best:

array_1 = [“element”, “element 2”];

array_2 = [“another element”, 2, 98, true];

array_3 = [array_1, array_2];

alert(array_3[1][3]); // displays “98”

            While you can’t mix numerical and string indexing systems in a single array (i.e. an array cannot be both numerical and associative), you can have both associative and numerical arrays in two dimensional arrays. For example, consider the above recast as follows:

array_3 = new Array();

array_3[“firstArray”] = array_1;

array_3[“secondArray”] = array_2;

alert(array_3[“secondArray”][3]);

//displays “98” again

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Similarly, we can happily use our “objective” notation for associative arrays:

alert(array_3.secondArray[3]);

//displays “98” yet again

Project

            Open your previous project file, and save it under the name

chapter_17.htm l .

            Building on your previous project, create a number of new, seven element associative arrays to represent 4 separate weeks.

            Combine these 4 weeks into a four element array to represent a month.

            Modify your previous code to take a week number and print out all that week’s activities to the page.

            Modify one of your week arrays to consist not of single elements, but of arrays of hours from 8am to 5pm. This then represents a three dimensional array . We can extend arrays to be n-dimensional , where n is more or less arbitrary.

            Finally, alter your code to prompt the user for three values – a week, a day and an hour. Store these values in three separate variables, and use those variables to display the requested task, or else to display an error message if a task cannot be found.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

18 String Manipulation

Key Points

            Throughout your use of JavaScript in a production environment, you will often use it to read values from variables, and alter a behaviour based on what it finds.

            We have already seen some basic string reading in the section on comparisons where we test for equality. However, this all-or-nothing approach is often not subtle enough for our purposes.

            Take the case where we want to check a user’s name against a list of known users. If the user enters their name as “Karen”, for example, that will be fine if and only if they spell the name precisely as we have it recorded, including capitalisation etc. If the user decides to type in her full name, say “Karen Aaronofsky”, the code will not recognise her.

            In this case, we want to see if the text “Karen” appears at all in the string. We call this substring searching , and it can be incredibly useful.

            One of the simplest substring searches is done by using the indexOf method. Every string-type variable has this metho d associated with it. Consider this code:

var_1 = “Karen Aaronofsky”;

var_2 = var_1.indexOf(“Karen”);

In this case, the value of var_ 2 will be 0 – remembering that JavaScript begins counting at 0!

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            If we were to search for a surname here:

var_1 = “Karen Aaronofsky”;

var_2 = var_1.indexOf(“Aaronofsky”);

var_2 will have a value of 6.

            Finally, if the search were to “fail”, so say we searched for the name “Anisa” as a substring, the value of var_ 2 would then be -1.

            Note that this is more flexible, but still presents an issue if the user forgets to capitalise any of the substrings that we are searching for – in JavaScript, “Karen” does not equal “karen”.

            In order to get around this, we might want to ensure that capitalisation is not taken into account. A simple way to achieve this is to force strings into lowercase before the check is performed:

real_name = “Karen”;

name = prompt(“Your name?”,””);

real_name = real_name.toLowerCase(); try_name = try_name.toLowerCase();

if ( try_name.indexOf(real_name) > -1 )

{

alert(“Hello Karen!”);

}

else

{

             note we use the original,

             non-lower-cased name here alert(“Welcome “ + name);

}

            There are a number of string methods we can use to perform “value checks” on strings. A few are printed in the following table:

|  | Method | Behaviour |  |
|  |  |  |  |
|  | String.indexOf(“str”) | Returns the numerical position of the first |  |
|  |  | character of the substring “str” in the String |  |
|  |  |  |  |
|  | String.charAt(x) | Returns the character at position x in the |  |
|  |  | string – the opposite of indexOf |  |
|  |  |  |  |
|  |  |  |  |

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

| String.toLowerCase() | Returns a copy of the string with all capital |
|  | letters replaced by their lowercase |
|  | counterparts |
|  |  |
| String.toUpperCase() | Returns a copy of the string with all |
|  | lowercase letters replaced by their capital |
|  | counterparts |
|  |  |
| String.match(/exp/) | Returns true or false based on a regular |
|  | expression search of the string |
|  |  |

            The final method here deserves some comment. What is a regular expression ?

            A regular expression is a standard way of writing down a “pattern” of characters that is easily recognisable. For example, consider a typical email address:

jonathan@relativesanity.com

            An email address follows a “pattern” which makes it instantly recognisable as an email address to a human. Wouldn’t it be handy if we could define that pattern in JavaScript for a browser to use? Regular expressions allow us to do just that.

            Let’s look at our email address again. We can break it down to a “prototype” email address as follows:

[some letters]@[some more letters].[a few more letters]

            Of course, it’s slightly more complex than that – there are some characters which aren’t allowed to be in certain parts of the email address (no spaces, for example), but this lets you see the idea of breaking this string up into required “chunks”.

            Now, to convert this to a regular expression. Just as we use quote marks to denote (or “delimit”) string values in JavaScript, to signify a regular expression, we use forward slashes: /. Our email address regular expression might look like this:

/^.+@.+\..+$/

            This warrants some discussion. Let’s look at this a character at a time:

            / denotes the start of the regular expression

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            ^ denotes that we want this regular expression to be found at the very beginning of the string we are searching.

            .+ the dot symbol is used to stand in for any character. The plus signifies we want to find at least one of those. So this is equivalent to our plain-English phrase [some letters].

            @ this is simply a character – it has no special meaning other than to say we want to find an @ character after at least one character from the beginning of the string.

            .+ the same as before – at least one more character after the @.

            \. This is interesting. We know that the dot symbol has a special meaning in a regular expression – it means “match any character”. However, here we want to find an actual dot . Unlike @, which has no special meaning, we have to tell JavaScript to ignore the dots special meaning. We do this by preceding it with a backslash, which tells JavaScript to treat the character immediately following it as though it has no special meaning. This is a convention you will come across many times while programming. The net result here is that we want to match a dot after a series of characters.

            .+ and again, at least one more character after the dot.

            $ this is the mirror of the ^ at the beginning – this matches the end of the tested string.

            / tells JavaScript we are at the end of the regular expression.

            Phew! Lots to consider here. Regular expressions are an arcane art at the best of times, so don’t worry too much if the above code is indecipherable. The important thing to realise at the moment is that we can perform some quite sophisticated pattern recognition in JavaScript without having to resort to checking each individual character of a string multiple times.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            The following code checks a variable to see if it looks like an email address:

var_1 = prompt(“Your email?”, “”);

if ( var_1.match(/^.+@.+\..+$/) )

{

alert(“valid email address”);

}

else

{

alert(“are you sure?”);

}

            There are a few problems with this code at the moment – for example, it will pass the string “-@-.-“ quite happily, which is clearly wrong. We will look at ways around this later on in the course.

Project

            Open your previous project file, and save it under the name

chapter_18.htm l .

            Clear all JavaScript code from your script tags.

            Use a prompt box to capture some user input to a variable called check_strin g .

            Use a document.write statement to output the results of each of the various string methods when applied to the user input.

            Check the user input to see if it’s an email address, and alter your output accordingly to either “That’s an email address” or “That doesn’t look like an email address to me!”

            In the latter case, output the failed string as well so that the user can see their input and modify it next time, if appropriate.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

19 Using Functions

Key Points

            A function is a named set of JavaScript statements that perform a task and appear inside the standard <script > tags. The task can be simple or complex, and the name of the function is up to you, within similar constraints to the naming of variables.

            JavaScript functions are declared before they are used. The declaration looks like this:

function name_of_function( )

{

…your code here…

}

            Unlike all the JavaScript instructions we have looked at so far, the code inside a function will not be run until specifically requested. Such a request is called a function call .

            Functions can be called from anywhere on the page that JavaScript can live, but must be called after the function has been declared. For example, if you declare a function in the body of a document and then call it from the head of the document, you may find that the browser returns an error message. For this reason, most JavaScript programmers define any functions they are going to use between <script > tags in the head section of their pages to ensure that they are all defined before they are used.

            Functions are to object methods as variables are to object properties – they are also called in a similar manner. To run the code contained in the name_of_functio n function above, we would use the following line of code:

name_of_function();

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Note the parentheses after the function name. This lets JavaScript know that we are dealing with a function and not a variable. The parentheses also allow us to “pass” extra information to the function, which can alter its behaviour. Consider the following function:

function greet_user( username )

{

message = “Hello “ + username;

alert(message);

}

            Whenever the function is called, it will greet the user named. How can we pass this information through? Consider:

greet_user(“Anisa”);

or

var_1 = prompt(“Name?”, “”);

greet_user(var_1);

            We should use functions in our code as often as possible. Whenever we perform an action that isn’t accomplished by the use of a method or an assignment operator, we should try to build a function that can accomplish the task.

            For example, we can build a function to check email addresses:

function check_email( address )

{

var_1 = false;

if ( address.match(/^.+@.+\..+$/) )

{

var_1 = true;

}

}

            The above function will take a string that is passed to it (often called the function’s argument ), and will alter the value of var_1 depending on what it finds. However, the function i s lacking an important ability – the ability to communicate its findings back out to the rest of the script.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            We have mentioned return values a few times in the notes. Now we see a situation that requires a function to return its findings to the rest of the code. Ideally, we’d like to be able to use the above function as follows:

if ( check_email(address) )

{

…do some email things…

}

            In order for this to work, the return value from check_email would have to be a Boolean value. We can arrange this quite simply:

function check_email( address )

{

var_1 = false;

if ( address.match(/^.+@.+\..+$/) )

{

var_1 = true;

}

return var_1;

}

            Since var_1 is either true or false, the returned value will be Boolean. We can even skip the use of the variable here and be more direct:

function check_email( address )

{

if ( address.match(/^.+@.+\..+$/) )

{

return true;

}

return false;

}

or even better, since address.match() will return a Boolean value of its own:

function check_email( address )

{

return address.match(/^.+@.+\..+$);

}

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            The above function may not seem like a great saving. After all, we are using four lines of code to define a function that performs only one line of code. Compare:

function check_email( address )

{

return address.match(/^.+@.+\..+$);

}

if ( check_email(address) )

{

…do some email things…

}

with:

if ( address.match(/^.+@.+\..+$/) )

{

…do some email things…

}

            While the benefits here are not obvious, consider the case where, at some point in the future, you discover a better method of checking for email addresses. In the second case abov, you will have to search your code for each and every instance of that method, and replace it with your new method, which may not be one line of code. In the first case, you will just have to change the underlying function definition, and the “upgrade” will be effective throughout your code without you having to update each occurrence.

Project

            Open your previous project file, and save it under the name

chapter_19.htm l .

            Clear all JavaScript code from your script tags.

            Ensure that you have a script element in the head area of your document, and one in the body area.

            In the head area, define a function called show_messag e . This function should take one argument, called messag e , and should use an alert box to display the contents of the argument.

            In the body area, call the function with various messages as arguments.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Now use a variable in the body area to store the return value of a prompt asking the user for a message. Use this variable as the argument to a single instance of show_messag e .

            Define a new function in the head area called get_messag e . It should take no argument, but should replicate the function of your prompt in the body area and ask the user for a message via a prompt box.

            Make sure that get_messag e return s a sensible value. We are aiming to replace our prompt statement in the body area with the following code:

message = get_message();

so consider what you will have to return to enable this to work.

            Once you are happy with your get_messag e definition, try replacing your prompt code in the body area with the statement above.

            To demonstrate the power of functions, change the action of show_message to write the message to the page withou t changing any code in the body area of the page.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

20 Logical Operators

Key Points

            In our discussion of conditionals, we saw how to check the veracity of a single condition via a comparator:

if ( x > some_value )

{

…expressions…

}

            We have also seen the limitations of such an approach. Let us say we wanted to discover if x lay between two values, say val_1 an d val_ 2 . There are a number of ways we coul d achieve this. In our example on student grades, we learned that we could use an if…els e pair to achieve this effect:

if ( x > val_1 )

{

…do something…

}

else

if ( x > val_2 )

{

…do something else…

}

            The above code achieves what we want – for the second branch, x must lie between val_ 2 and val_ 1 (assuming val_1 is greater tha n val_ 2 , of course). However, it’s rathe r unwieldy, and does not scale elegantly to checking three conditions (say we wanted to check if x was an even number as well), or in fact to ten conditions.

            Enter Logical Operators . These operators are used to join together conditional checks and return true or false depending on whether all or any of the checks are true.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            In English, we refer to these operators by using the words “AND” and “OR”.

            For example, say we wanted to do something each Tuesday at 8pm. We would want to check whether the current day was Tuesday, and whether the time was 8pm.

            Another example: Let’s say we wanted to do something on the first Tuesday of each month, and also on the 3 rd of the month as well. We would have to check whether the current day was the first Tuesday of the month, or whether it was the 3 rd day of the month.

            Note in the last example, if both conditions were true, then we would be on Tuesday the 3 rd and would perform the action. In other words, an or condition allows for either one, or the other, or both conditions to be true.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            In JavaScript, we use the following syntax to check multiple conditions:

( 100 > 10 && 5 < 8 )

translates as “if 100 is greater than 10 and 5 is less than 8”. In this case, the result is true .

( 100 > 200 && 4 < 9 )

in this case, the result is false . Note here that only the first condition is actually checked. Since and requires both comparisons to be true, as soon as it finds a false one it stops checking. This can be useful.

( 100 > 10 || 9 < 8 )

translates as “if 100 is greater than 10 or 9 is less than 8”. In this case, the result is true , since at least one of the conditions is met.

( 100 > 200 || 4 > 9 )

in this case, the result is false since neither of the comparisons are true. Finally:

( 100 > 200 || 5 < 2 || 3 > 2 )

in this case, the result is true . Any one of the three being true will provide this result.

            As we can see from the last example, this method of checking scales to any number of conditions. We can also mix and match the operators. For example:

( ( 100 > 200 && 100 > 300 ) || 100 > 2 )

in this case, the and condition evaluates to false , but since either that or the last condition has to be true to return true , the overall condition returns true as 100 is indeed greater than 2.

            This sort of complex logic can take a while to comprehend, and will not form a set part of the course. However, it is useful to be aware of it.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

Project

            Open your previous project file, and save it under the name

chapter_20.htm l .

            Clear all JavaScript code from your script tags.

            Ensure that you have a script element in the head area of your document, and one in the body area.

            Copy the file available_plugins.j s from the network drive (your tutor will demonstrate this), and open it using NotePad’s File > Open command.

            Copy and paste the entire contents of

available_plugins.js into your current project file, int o the script element in the head area of your page.

            Have a read through the code. Note that it defines a large, two dimensional array. The array has a list of various components that can be present in web browsers (such as Flash or Quicktime)

            Add a function to the head area script element, called flash_exists( ) . This function should use a for loo p t o check each of the elements of the available_plugin s array and establish if Flash is present.

            Add a further function to the head area script element, called quicktime_exists( ) . This function should also us e a fo r loop to check each element of the array, this time returning true if Quicktime is present.

            Finally, add a function to the head area script element called

both_quicktime _and_flash_exist( ) . This functio n should call both of the previous functions, store their results in a variable, and produce an alert box containing the message:

            “Both Quicktime and Flash” if both functions returned true; or:

            “One of Quicktime or Flash is missing” if either of the functions return false.

            Call the final function from the body area script element.

            Check your results in your browser.

![](Image00000.jpg)

| JavaScript for Beginners |
|  |

21 Using Event Handlers

Key Points

            So far, our scripts have run as soon as the browser page has loaded. Even when we have used functions to “package” our code, those functions have run as soon as they have been called in the page, or not at all if no call was made. In other words, the only event our scripts have so far responded to has been the event of our page loading into the browser window.

            Most of the time, however, you will want your code to respond specifically to user activities. You will want to define functions, and have them spring into action only when the user does something. Enter event handlers .

            Every time a user interacts with the page, the browser tells JavaScript about an “event” happening. That event could be a mouse click, a mouse pointer moving over or out of a given element (such as an image or a paragraph), a user tabbing to a new part of an HTML form, the user leaving the page, the user submitting a form and so on.

            An event handler is a bit of JavaScript code that allows us to capture each event as it happens, and respond to it by running some JavaScript code.

            In general, we attach event handlers to specific HTML tags, so a mouse click on one element of the page might be captured by an event handler, but clicking somewhere else might do something completely different, or indeed nothing at all.

            Some common event handlers are in the table below:

|  | Event Handler | Occurs When… |  |
|  |  |  |  |
|  | onload | An element is loaded on the page |  |
|  |  |  |  |
|  |  |  |  |

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

| onunload | An element is not loaded, for example when |
|  | a user leaves a page |
|  |  |
| onmouseover | When the mouse pointer enters the area |
|  | defined by an HTML element |
|  |  |
| onmouseout | When the mouse pointer leaves the area |
|  | defined by an HTML element |
|  |  |
| onclick | When the left mouse button is clicked within |
|  | the area defined by an HTML element |
|  |  |
| onmousedown | When the left mouse button is depressed |
|  | within the area defined by an HTML |
|  | element |
|  |  |
| onmouseup | When the left mouse button is released |
|  | within the area defined by an HTML |
|  | element |
|  |  |

            The last three are related, but there are subtle differences – onclick is defined as being when both mousedown and mouseup events happen in the given element’s area. For example, if you click on an area of the page, that registers the area’s mousedown event. If you then hold the mouse down and move to another area before releasing, it will register the other area’s mouseup event. The browser’s click event, however, will remain unregistered.

            In theory, we can add most of these event handlers to just about any HTML tag we want. In practise, many browsers restrict what we can interact with.

            We will mostly be attaching event handlers to <img > , <a > and

<body> tags.

            To attach an event handler to a tag, we use the following method:

<a href=”…” onclick=”a_function();”>link</a>

            We can use this method to attach any event handler listed above to the elements of the page. In addition to calling functions (with any optional arguments, of course), we can write JavaScript directly into our event handlers:

<a href=”…” onclick=”alert(‘hello’);”>link</a>

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Note the potential issue with quote marks here – if you use double quotes around your event handler, you need to use single quotes within and vice versa.

Project

            Open your previous project file, and save it under the name

chapter_21.htm l .

            Clear all JavaScript code from your script tags.

            Ensure that you have a script element in the head area of your document, and none in the body area.

            Within the head area script element, define the following function:

function set_status( msg )

{

window.status = msg;

}

            When called, this function will set the text displayed in the browser’s status bar (the part of the window below the page content) to whatever is passed as an argument. For example, to set the status bar to display “Welcome”, we would call:

set_status(“Welcome”);

            Now define the following function immediately below the last:

function clear_status( )

{

set_status(“”);

}

            When called, this function will clear the status bar. Notice that we are using our previous function within the new one. This is a common programming technique that allows us to define functions of specific cases using more general functions.

            Now, add the following HTML to the body area of your page. Remember, we’re adding HTML here, not JavaScript, so do not be tempted to use script tags for this part of the project:

<a href=”#” ↵

onmouseover=”set_status(‘hello’);” ↵

onmouseout=”clear_status();”>testing</a>

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Load the page in your browser and observe what happens when you move your mouse over the link.

            The # value for the href attribute of the link allows us to define a “dead” link on the page. Clicking on the link will take you nowhere – try it.

            Now, alter the code to have the link point at a real website that you know of.

            Clicking on the link now will take you away from the page. Let’s say we want to suppress that behaviour.

            When an event handler intercepts an event, it pauses the normal action of the event. For example, if you used an onclick handler on a link to pop up an alert box, the link would only be followed after the alert box had been dismissed. We can use event handlers to cancel the action if required by using their return values.

            Add a new function to the head area script element:

function confirm_link( )

{

check = confirm(“This will take you ↵ away from our site. Are you sure?”);

return check;

}

            The value of chec k will be true or false .

            Now, modify your link to contain the following event handler:

onclick=”return confirm_link();”

            By using the word retur n in our event handler, the response of the function will be used to decide whether the rest of the normal action is run. In this case, if confirm_link( ) returns false , our link action will be cancelled.

            Load your page in your browser and view the result.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

22 Working with Images

Key Points

            In HTML, we can identify specific elements on the page using an id attribute. For example, to “name” an image, we can use the following code:

<img src=”logo.gif” alt=”” id=”theLogo” />

            To refer to this element in JavaScript, we can now get to it directly by its id value:

document.getElementById(“theLogo”)

            This method will return an object that refers to the given element on the page. If no such element can be found, the method will return false.

            For easier use, we can assign the object found to a variable. For example, to create an object called our_logo in our scripts, we can use the following line of code:

our_logo = document.getElementById(“theLogo”);

            The resultant object has a number of properties. Since, in this case, our object represents an image element, its properties include:

our_logo.height

our_logo.width

our_logo.src

            We can use JavaScript to change any of these properties, so if we wanted to change the image displayed, we could do so as follows:

our_logo.src = “new_logo.gif”;

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

Project

            Copy the folder called image s from the network drive to your project folder.

            Open your previous project file, and save it under the name

chapter_22.htm l .

            Clear all JavaScript code from your script tags.

            Ensure that you have a script element in the head area of your document, and none in the body area.

            Within the body area of your page, create an image element that loads an image from the image s folder. Give the element an appropriate i d attribute.

            In the head area script element, define a function called describe_image() that will pop up an alert box containing the following information about your image:

the image file used

the image width

the image height

            To have each bit of text appear on a separate line, you can add the following character to your alert text:

\n

for example

alert(“line one\nLine two”);

            Load your page in the browser and view the results.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

23 Simple Image Rollovers

Key Points

            A simple image rollover is an effect which happens when the mouse appears over an image (usually a linked button) on the page. The original image is replaced by another of equal size, usually giving the effect that the button is highlighted in some way.

            With what we have learned so far, we already have the ability to create a simple image rollover effect. All that remains is to clarify the particulars of the process:

            The page is loaded and the original image appears on the page as specified by the <img > tag’s sr c attribute.

            The mouse moves offer the image and the alternative image is loaded into place.

            The mouse leaves the image and the original image is loaded back.

            As you may have realised, we are going to use JavaScript to alter the sr c attribute of the image tag. The best way to think of this is to picture the <img > tag as simply a space on the page into which an image file can be loaded. The sr c attribute tells the browser which image to load into the space, and so if we change that value, the image will be changed.

            In other words, the i d attribute of the <img > tag is naming the “space”, not the image.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Now, in order to alter the src attribute with JavaScript, we need to tell JavaScript which image “space” we want to alter. We use the id attribute along with the getElementById() method from the last chapter to do this:

button_img = ↵

document.getElementById(“button”);

button_img.src = “new_image.jpg”;

            We can directly insert this code into the image’s event handler:

<img src=”old.jpg” id=”button” ↵

onmouseover = ↵

”document.getElementById(‘button’).src ↵

= ’new.jpg’;”>

            Note that this code is suddenly very convoluted. There are two immediate potential solutions. The first is to define a function:

function swap_image( id, new_image )

{

img = document.getElementById(id);

img.src = new_image;

}

…

<img src=”old.jpg” id=”button” ↵

onmouseover= ↵

”swap_image(‘button’, ‘new.jpg’);”>

            This is a much cleaner solution, and more importantly we can use this for any images on the page, simply by changing the arguments of our function call. We can also use the function to achieve the “swap back” functionality:

…

<img src=”old.jpg” id=”button” ↵

onmouseover= ↵

”swap_image(‘button’, ‘new.jpg’);” ↵

onmouseout= ↵

”swap_image(‘button’, ‘old.jpg’);”>

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            We can go even further in “cleaning up” our code, though. Because the event handler is being used to alter the object which is experiencing the event (ie, the mouse is moving over the image tag that we are trying to change), we can use the “automagic” JavaScript object thi s to perform the operation:

function swap_image( img, new_image )

{

img.src = new_image;

}

…

<img src=”old.jpg” id=”button” ↵

onmouseover= ↵

”swap_image(this, ‘new.jpg’);”>

            Note a couple of things. Firstly, thi s has no quotes around it

– we are using it like a variable name. Secondly, our function now uses the first argument directly, instead of using it to get the relevant object from the page. We can do that because this is actually an object – it’s an object that takes on th e properties and methods of whatever object it is called from, in this case, it becomes equivalent to

document.getElementById(‘button’ ) , although i s obviously much shorter!

            Using thi s has some limitations. For example, if we wanted to change the sr c attribute of any other image on the page when the mouse moved over “ butto n ”, we would be unable to use this, and hence would have to define another function that could take an id as its argument and get the relevant object that way.

Project

            Copy the folder called button s from the network drive to your project folder.

            Open your previous project file, and save it under the name

chapter_23.htm l .

            Clear all JavaScript code from your script tags.

            Ensure that you have a script element in the head area of your document, and none in the body area.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Within the body area of your page, create a paragraph containing six image elements. Set the sr c attributes of the images to load the following files in your copied button s folder, and give each a sensible i d :

            contacts.jpg

            home.jpg

            people.jpg

            products.jpg

            quotes.jpg

            whatsnew.jpg

            Create a JavaScript function in the head area script element that takes two arguments – an i d and a file name. It should alter the src property of the appropriate image object to the file name given.

            Use this function to swap the sr c attribute of the contacts button to contactsover.jp g when the mouse moves over the image.

            Once you have this working, update the remaining five images with event handlers to swap their sr c attributes to their appropriate “over” image.

            Add event handlers to all six images to ensure that they return to their original state when the mouse is moved away from them. Check your work in your browser

            Add a new paragraph above the previous one, and add an <img> tag to it to containing the fil e rocollogo.jpg fro m the images folder.

            Add a text link to a new paragraph between the two paragraphs. The link should be a “dummy” link (ie use “ # ” as its hre f attribute value), but when the mouse moves over it, the image above it should change to show rocollogo.gi f .

            Moving the mouse away from the text link should return the logo to its previous state.

            Check your work in your browser.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

24   Object Instantiation and Better Rollovers

Key Points

            So far we have seen a very simple example of an image rollover. It is functional and works as desired, but it is lacking in a few finer details.

            Specifically, when we use JavaScript to change the src attribute of an <img> tag, the browser has to load this image from scratch. On our local machine, this will not cause an appreciable delay, but when dealing with a remote server (as we will be on the Internet), this delay can lead to a noticeable “lag”, which can destroy the feeling of a dynamic interface.

            Ideally, we would like to instruct the browser to load any alternate images when it loads the page. This will allow us to ensure that the new images are sitting on the user’s computer, ready to be swapped in and out instantly.

            To do this, we need to look at object variables and object instantiation (or creation ). In particular, we need to look at the Image object.

            Each <img > tag on the page has a corresponding Image object in JavaScript. We have looked at ways of manipulating this directly, and have an idea of some of the properties an Image object can have.

            However, we can create Image objects directly in JavaScript, without the need for a corresponding <img > tag on the page. When we create such an object, and set its src property, the browser will load the appropriate file into memory, but will not display the image on the page.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            In other words, we can create “virtual” images that exist within JavaScript, and use these Image objects to store the alternate images for our “real” images.

            To create an Image object (in fact, to create any object), we need to use the following code:

virtual_image = new Image();

            We have seen this sort of syntax before – the use of the ne w keyword when we created our Arrays. ne w tells JavaScript that we are creating a new object. The virtual_imag e part of the assignment is just a variable name. In this case, the variable is an Object Variable , since it contains an object.

            To use this variable to preload our images, we take advantage of the fact that it has the same properties and methods as any other image:

virtual_image.src = “contactsover.jpg”;

            The browser will now preload our image, ready to be swapped in at a later time.

Project

            Open your previous project file, and save it under the name

chapter_24.htm l .

            Starting with your previous code, create a new function called preload_images in the head area script element of your page.

            Use this function to create seven new image objects, and use each objects corresponding object variable to preload your “over” image variations.

            Check your work in your browser to ensure that the image swapping still works as expected.

            Add your preload_images function to the body tag of your page to ensure that it runs when the page has finished loading. Use the following syntax:

<body onload=”preload_images();”>

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Once you have verified that the image swapping still works as expected, expand your preload_images function to define an array of images to preload, and then use a for loop to move through the array and assign each image to the src property of an object variable. Hint : an object variable can be anything that can store information – for example an array element.

            Check your work in your browser.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

25 Working with Browser Windows

Key Points

            Using standard HTML links, we can open new browser windows:

<a href=”#” target=”_new”>link</a>

            The amount of control this method affords us over the resultant image, however, is nil. We cannot control the size, shape, location on the screen or anything else about that window with this method.

            JavaScript allows us much finer control, as we may expect:

window.open( page_url, name, parameters );

            As we can see from the above prototype, there are only three arguments that this method can take. However, the parameters argument is actually more complex than w e might assume:

”param1,param2,param3,param4…”

since we can use it to add many parameters to the method.

Note there are no spaces in the parameter list.

            name is used to give the window an HTML name – so we ca n use that name to open links into the new window using the “ targe t ” method above.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            The return value from the ope n method is an object variable referring to the newly opened window. In other words, if we open a new window like so:

win = window.open(“page.html”, “”, “”);

we can use the object variable wi n to alter the new window through JavaScript.

            A practical example – let’s say we want to open a new window 300 pixels high by 400 pixels wide, and display the BBC news page in it. The following code would suffice:

window.open(“http://news.bbc.co.uk/”, ↵

“bbc”, “width=300,height=300”);

            Some available parameters are given in the table below:

| Parameter | Value | Function |
|  |  |  |
| location | Yes/no | Specifies whether or not the location |
|  |  | (address) bar is displayed |
|  |  |  |
| menubar | Yes/no | Specifies whether the menu bar is |
|  |  | displayed |
|  |  |  |
| status | Yes/no | Specifies whether the status bar is |
|  |  | displayed |
|  |  |  |
| width | Pixels | Specifies the width of the new window |
|  |  |  |
| height | Pixels | Specifies the height of the new window |
|  |  |  |
| resizable | Yes/no | Allow or disallow window resizing |
|  |  |  |
| scrollbars | Yes/no | Allow or disallow window scrolling |
|  |  |  |

            If no parameters are set, then the value of each parameter is set to “yes” where appropriate. For example:

window.open(“http://www.bbc.co.uk/”, ↵ “bbc”, “”);

is equivalent to:

<a href=”http://www.bbc.co.uk/” target=”bbc”>

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            However, if any parameter is set, all others default to “no”. So if you wanted to have a scrollbar but nothing else, the following would suffice:

window.open(“http://www.bbc.co.uk/”, ↵ “bbc”, “scrollbars=yes”);

Project

            Open your previous project file, and save it under the name

chapter_25.htm l .

            Remove all functions and HTML from your previous file, leaving only the logo image and the link.

            Create a function in the head area script element called view_new_log o . This function should:

             Open a new window 200 pixels square.

             Load the image rocollogo.jp g from the images folder.

             Be called RocolLogo

             Be stored in an object variable called objNewLog o .

             Have no scrollbars, be of a fixed size, and have no other features where possible.

            Remove all event handlers from the link, and add a new one to run the function above when the link is clicked.

            Once you have verified that a window pops up as required when the link is clicked, test each parameter from the table above in the function.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

26 Positioning Browser Windows

Key Points

            The screen object provides you with access to properties of the user’s computer display screen within your JavaScript applications.

            Some of the available properties are:

| Property | Description |
|  |  |
| availHeight | The pixel height of the user’s screen minus the |
|  | toolbar and any other permanent objects (eg the |
|  | Windows Taskbar) |
|  |  |
| availWidth | As availHeight, but dealing with horizontal space |
|  |  |
| colorDepth | The maximum number of colours the user’s screen |
|  | can display (in bit format, eg 24 bit, 16 bit etc) |
|  |  |
| height | The true pixel height of the user’s display |
|  |  |
| width | The true pixel width of the user’s display |
|  |  |

            The lef t and to p parameters of the open( ) method enable you to specify the position of a window on screen by specifying the number of pixels from the left and top of the screen respectively.

            If you need to use a variable to specify the value of a parameter in the open( ) method, you would do so as follows:

window.open(“index.html”, “window_name”, ↵ “width=200,height=200,left=”+var_left+ ↵ “top=”+var_top);

Where var_lef t and var_to p are the appropriate variables.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Note the use of the + operator to ensure that the third parameter in the open( ) method remains as one string when variables are added.

            In order to centre the window on the user’s screen, a little simple geometry is required. The centre of the screen is obviously the point found when we take the width of the screen divided by two, and take the height of the screen divided by two. However, if we set the window’s top and left values to these coordinates, the top left corner of the window will be centred, not the window itself.

            In order to centre the window, we need to subtract half of the window’s height from our top value, and half of the window’s width from our left value. A simple script to accomplish this is as follows:

win_width = 200;

win_height = 200;

win_left = (screen.availWidth/2) ↵

- (win_width/2);

win_top = (screen.availHeight/2) ↵

- (win_height/2);

            By using this script, the values of win_left and win_top will be set correctly for any window using win_width and win_height appropriately to be centred on the screen.

Project

            Open your previous project file, and save it under the name

chapter_26.htm l .

            Modify your existing code to ensure that the logo appears

centred on the user’s screen. If possible, do not modify your original function by doing anything more than two new functions – get_win_left( width ) and get_win_top( height ) .

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

27 Focus and Blur

Key Points

            The focus( ) method of the windo w object gives focus to a particular window. In other words, it ensures that the window is placed on top of any other windows, and is made active by the computer. For example, if we have created a new window and stored the result in an object variable called new_windo w , we could ensure that the window was brought back to the front at any point after it had been opened by using the following code:

new_window.focus();

            Conversely, we can use the blur( ) method to remove focus from the specified window – returning focus to the previously selected one as appropriate. Its use is similar to the focus( ) method.

            Both these events have associated event handlers: onblu r and onfocu s . However, since they do not have associated HTM L tags, how can we attach event handlers to the object?

            It turns out that, within JavaScript, each object has an individual property for each event handler it can have applied to it. For example, if we wanted to add an event handler to an image tag on the page, we could apply either of the following methods to do that:

<img src=”…” id=”test_img” ↵

onclick=”do_something();” />

<script>

document.getElementById(“test_img”).onclick =↵ do_something();

</script>

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            So, to attach a function to a window’s focu s event, we could use:

new_window.onfocus = some_function();

Project

            Open your previous project file, and save it under the name

chapter_27.htm l .

            Modify your function to open another window as well as the original one, with the following features:

             The second window should be called oldRocolLog o , should be assigned to the object variable objOldLog o , and

display the old logo from the file

images/rocollogo.gi f .

             When opened, the windows should be positioned so that both can be clearly seen.

            Test your modifications at this point.

            Observe the function’s action when the windows are opened, then the original window is placed in front of them and the function is invoked again.

            Add a new statement to the function which uses the focus( ) method to ensure that when the function is called, both new windows are moved to the top of the “stack” of windows.

            Observe which logo appears “on top” when the function is called. Use the focus( ) method again to alter this.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

28 Dynamically Created Content

Key Points

            It’s quite easy to create a new page on demand using JavaScript. In this context, we are talking about creating a completely new page in a window without loading any file into that window.

            To do this, invoke the open( ) method of the windo w object, leaving the location parameter empty:

new_win = window.open(“”, “newWin”, ↵ “params…”);

            Next, remember that you can write HTML code to a page using the window’s document.write( ) method. Up until now, we have used only the current window’s documen t object. However, we can specify which window’s documen t we want to manipulate as follows:

document.write(); // write to current window new_win.document.write(); // or new window

For example:

new_win.document.write(“<html><head>”);

new_win.document.write(“<title>demo</title>”): new_win.document.write(“</head><body>”); new_win.document.write(“<h1>Hello!</h1>”); new_win.document.write(“</body></html>”);

Project

            Open your previous project file, and save it under the name

chapter_28.htm l .

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Modify your existing script to create a third window with the following properties:

             The window should be called newHTM L , and be assigned to the object variable objNewHTM L .

             It should be 400 pixels square.

             It should not load any page when it is created. It should display the word “Welcome” as an H 1 header.

             It should contain a paragraph with the text “Please decide which logo you would like to choose.”

             The third window should carry the title “Rocol Art”

             When all windows have been opened, the third window should be focu s sed.

            Check your work in the browser.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

29 Working with Multiple Windows

Key Points

            The window object’s close( ) method enables you to close a window. If you have an object variable in the current window referring to the window you wish to close, you can simply use:

new_window.close();

to close the window.

            Things are a little more complicated when you wish to close a window from a window other than the one which opened the new window. In order to tackle this, we need to think about window scope .

            When we write JavaScript into our code, all functions and variables within that script are available for us to use within that window . For example, if we have a function called say_hello() in our main window, we can easily call tha t function. However, if we want to call the function from a newly opened window, we cannot call it directly from the new window, as our functions and variables are “tied” to the windows in which they were first defined.

            This is why, when we want to write to any window other than the one containing our JavaScript code, we must access the document objec t of that windo w in order to put content in th e right place,

            But how about in the other direction? Let’s say we use a function in our main window (call it window 1 ) to open a new window ( window 2 ). If we store window 2 as an object variable, we can access all properties of window 2 from window 1 by using that object. The question is, how do we access any properties of window 1 from window 2 ?

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            The key is that window 2 and window 1 have a special relationship – a “parent/child” relationship. We can access any property of window 1 from window 2 by using the special object called opene r . This is an object created within any window that has been opened by JavaScript, and it always refers to the window that opened the new window.

            To illustrate this, let’s consider our previous project. We have three new windows, and one “parent” window. If we wanted to use an event handler on one of the new windows to close on of the other new windows, we would need to first access the parent window, and then access the object variable within the parent window that pointed to the window we wanted to close.

            Let’s say we wanted to close window_2 from a link in window_1\. We would have to create an event handler in the link with the following code:

onclick=”opener.window_2.close();”

Project

            Open your previous project file, and save it under the name

chapter_29.htm l .

            Modify your existing script to achieve the following:

             Add two new paragraphs to the third window’s content containing the following text:

The Old Logo The New Logo

             Each line should be contained in a hyperlink whose event handler accesses the parent window’s object variable pointing to the appropriate new window. Its close( ) method should then be invoked.

            Check your work in the browser.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

30 Using an External Script File

Key Points

            JavaScript can easily save us from having to type lots of HTML. As we have seen, we can use JavaScript to generate large form elements and tables using a small amount of code. This is good news for us, as it makes our work easier. It is also good news for our visitors, as they only have to download a small amount of code for a relatively large amount of content.

            However, we can do better. As it is, if we have one function that will generate a year drop down menu for a form’s date of birth section, we need to include that function in every page that requires it. This means that our visitors are downloading identical content multiple times. In addition, if we change or improve our function, we have to ensure that we update that function in every page that has it included.

            HTML allows us to solve this problem by providing a mechanism to load an external text file into the HTML page and treat its contents as JavaScript code. Since it is a separate file, once it has been downloaded once, the browser will not download further copies of the file if it is requested by another page. In other words, we can load all our JavaScript code into one file, and any changes there will instantly be reflected across the entire site.

            To use code in an external file, we still use the <script > tag

– but with a new attribute, the sr c attribute. This is very similar to loading an image file on to a page:

<script language=”JavaScript” ↵ type=”text/JavaScript” ↵ src=”s/script_file.js”></script>

            Note three things:

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

             The language and type attributes are essential here.

             The script tag still has a closing </script > tag.

             We cannot add any further JavaScript between the tags when we are using the tags to load an external file. To add JavaScript to the current page only, we have to use a second set of <script > tags.

Project

            Open your previous project file, and save it under the name

chapter_30.htm l .

            Move all your JavaScript function definitions, and any other

code in the head section script element to a new file called script.j s .

            Modify your head section script element to load code from the new file.

            Check that your page still works as expected.

            NOTE : the .j s file extension is just a naming convention. <script> tags will load JavaScript from any text file (henc e the need to include the type and language attributes). However, it is a widely used convention, and it is worth sticking to in order to keep your code easily understood by anyone who may work on your code in the future.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

31 Javascript and Forms

Key Points

            Without JavaScript, the server handles all validating and processing of information submitted via a form. Using JavaScript on the client side of the equation saves time for the user and creates a more efficient process.

            Some processing can be handled by JavaScript (for example, mathematical computations) and JavaScript can ensure that only correct data is sent to the server for processing.

            JavaScript is used in conjunction with server-side processing – it is not a substitute for it.

            To access information in a form we use the document object’s getElementById() method, as we have previously to acces s other objects on the page. For example, if we have a form on the page like so:

<form id=”testForm” … >

</form>

we would access it in JavaScript by using:

document.getElementById(‘testForm’);

            The resultant object is actually a multi-dimensional array. Each of its elements is itself an array containing information about the elements of the form (text boxes, buttons etc). By properly naming each of the form’s elements in the appropriate <INPUT> tags, you can access information relating to each of the form’s elements.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            To access the data stored in a text box called Nam e which is included in the form with the id Enquir y you use the value property like so:

objForm = document.getElementById(‘Enquiry’);

strValue = objForm.Name.value

            There are two ways of sending form data to the server. Using the metho d attribute, you can specify either the GET or the POST methods:

<form id =”enquiryform” method=”GET”…

or

<form id =”enquiryform” method=”POST”…

            In general, you should use the POST method if you want to send a lot of data (eg files, large amounts of text) from your form. You should use GET if you want to process search forms etc, as a GET form will be transmitted just like a URL, and is hence “savable” as a bookmark or link.

            In general, you will send your form to a server side script, specified by the form’s action attribute:

<form id=”enquiryform” method=”GET”

            action=”process.php”…

            When the user clicks on a form’s Submit button, without JavaScript intervention, the form’s data is sent straight to the server for processing. But you can intercept the data (so you can process it with JavaScript) before it is sent, by including the onsubmi t event handler in the <form > tag. This enables you to run a JavaScript function before the data is sent:

<form id=”enquiryform” method=”GET”

            action=”process.php”

            onsubmit=”functionName()”>

            In the above example, when the user clicks on the Submit button, the function functionName( ) is run first, then the data is sent to the server.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            When the submit event is triggered by the form’s submission, the browser waits to discover what is returned from the event handler. By default, the event handler will return tru e .

However, if the event handler returns a fals e value, the form’s submission will be aborted, and the page will not be submitted to the server.

            By returning a value of either true or false from your function ( functionName( ) in the above example), and ensuring that this is also the return value of the onsubmi t event handler, you can decide whether or not the form’s data is actually sent to the server.

            You specify that the return value of the function is also the return value of the onsubmi t event handler in the following way:

onsubmit=”return functionName();”

Project

            Open your previous project file, and save it under the name

chapter_31.htm l .

            Clear any content from the body element of the page, and ensure that the head area script element has no code in it.

            Save a copy of this page as processing_31.htm l , and put an <h1 > element in the body area saying “ success !”.

            Now, close your processing_31.htm l page and create a form on your original chapter_31.htm l page using HTML

– if you have difficulty with this, the tutor will provide an example to duplicate. Your form should:

             have an id of jsCourseFor m .

             have a single input box with an name value of nam e .

             have a submit button.

             use the GET method of submission.

             have processing_31.htm l as its actio n attribute.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

             have an onsubmit event handler that returns the value of the (as yet non-existent) check_form( ) function.

            Now, create a function in the head area script element called check_form(). This function should:

             use the document’s getElementById() method to store a reference to the form’s object in an object variable.

             store the value of the form’s nam e element in another variable.

             if the value of the name element is not “ Bugs Bunny ”, an alert box should appear stating:

Sorry chum!

Either you misspelled your name…

Or you haven’t got what it takes…

Try again.

             in addition, the form should be prevented from submitting.

            If the user enters the correct name, however, the form should submit without interruption.

            Check your work in your browser.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

32   Form Methods and Event Handlers

Key Points

            Each form object (e.g. text, button etc) has a set of properties associated with it. This is different for each form element. The valu e property is common to most form elements and is one of the most useful properties.

            You can assign the data stored in a text box called Nam e which is included in the form with id Enquir y , to a variabl e like so:

variable = document.getElementById(‘Enquiry’).

            Name.value

            Form objects also have methods associated with them. The set of available methods is different for each form object.

            Below is a list of commonly used methods for the text object:

| Method | Description |
| blur() | Removes the focus from the text box |
| focus() | Gives the focus to the text box |
| select() | Selects the text box |

            Below is a list of commonly used methods for the button object:

|  | Method | Description |  |
|  | blur() | Removes the focus from the button |  |
|  | focus() | Gives the focus to the button |  |
|  | click() | Call’s the button’s onclick event handler |  |
|  |  |  |  |

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Form objects also have event handlers associated with them. The set of available event handlers is different for each form object.

            Below is a list of commonly used event handlers for the text object:

| Event handler | Runs JavaScript code when… |
| onblur | The text box loses the focus. |
| onfocus | The text box receives the focus. |
| onselect | The user selects some of the text within |
|  | the text box.. |
| onchange | The text box loses the focus and has had |
|  | its text modified. |

            Below is a list of commonly used event handlers for the button object:

| Event handler | Runs JavaScript code when… |
| onBlur | The button loses the focus |
| onFocus | The button receives the focus |
| onClick | The user clicks the button |

            Finally if you are sending data to the server, a submit button is not the only way. You could use the submit() method in a function which is invoked by an event handler. This operates as if the Submit button was clicked:

document.getElementById(‘Enquiry’).submit();

Project

            Open your previous project file, and save it under the name

chapter_32.htm l .

            Modify your form in the following way:

             Remove the submit button

             Replace the submit button with a standard form button.

             Add an event handler to this button to invoke the function in the head area script element.

             Remove the onsubmi t event handler from the form element.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Now, modify the check_form( ) function in the following way:

             If the user types in the name “Bugs Bunny”, the function submits the form using the form’s submit() method.

             If the user types anything else, the previous alert box warning is displayed and the form is not submitted, but also:

             The words “please try again” are displayed in the text box.

             The text box is given focus.

             The text in the text box is selected.

            Check your work in your browser.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

33 JavaScript and Maths

Key Points

            The Mat h object is a pre-defined JavaScript object containing properties and methods which you can use for mathematical computation.

            Below is a selection of some useful Mat h methods:

| Method | Returns |
| Math.cell() | The smallest integer greater than or equal to a number. |
|  | That is, it rounds up any number to the next integer. |
|  | Math.cell(2.6) returns 3 and so does |
|  | Math.cell(2.2). |
| Math.floor() | The largest integer greater than or equal to a number. |
|  | That is, it rounds down any number to the next integer. |
|  | Math.floor(2.2) returns 2 and so does |
|  | Math.floor(2.6). |
| Math.max(n1,n2) | The larger of the two arguments. |
| Math.min(n1,n2) | The smaller of the two arguments. |
| Math.random() | A random number between 0 and 1. |
| Math.round() | The number rounded to its nearest integer. |
| Math.sqrt() | The square root of a number. |

            You don’t need to include a Submit button in a form and you don’t need to send form data to the server. You could use event handlers to invoke JavaScript code which merely processes the data on the form (e.g. you may just perform some mathematical computations on some user data).

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            If you are not sending the data to the server, there is no need to include either the Action or Method attributes in the <FORM> tag, though by default the Action will usually submit to the current page, and the Method will be set to “get”.

Project

            Open your previous project file, and save it under the name

chapter_33.htm l .

            Remove all content from the body section of the page.

            Copy the file max_wins.htm l from the network, and open it using NotePad’s File > Open command.

            Copy and paste the entire contents of max_wins.htm l into your current project file, into the body element of the page.

            Remove all JavaScript code from the script element in the head section of the page.

            Take some time to open your project file in a browser, and study the code. This project will enable the page to:

             Generate two random numbers when the button is pressed.

             Display the random numbers in the text boxes marked player 1 and player 2 .

             Compare the two random numbers and display the name of the player whose number is higher in the text box marked winner .

            When studying the code, note that the form has no valid action or method attributes. It also has no “submit” button. We are not going to allow the form to submit to the server at all, but are going to use JavaScript to do all our processing on the form.

            Now, modify the HTML code on the page to add an event handler to invoke a new function defined in the head area script element. The function should perform the following operations when the form button is clicked:

             Place two separate random integers between 0 and 100 in each of the Player text boxes.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

             Find a way to use a Math method to compare the two entered integers. Once compared, the function should then place the appropriate value of Player 1 , Player 2 , or Draw in the Winner text box.

            Check your work in your browser.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

34 Object Variables – A Refresher

Key Points

            Referring to objects can be a lengthy process. Consider the Player 1 text box in the previous example. You refer to it in full as follows:

document.getElementById(“MaxWins”).Player1

            This notation although precise, is tedious, time consuming and can be prone to error. Luckily, there are some shortcuts which can save time and reduce typing errors.

            We can use an object variable to simplify our work whenever we are in situations where certain objects need to be referred to repetitively. To use an object variable, you begin by simply assigning it a specific object:

oPlayer1 =

            document.getElementById(“MaxWins”).Player1

            Once assigned, you can use the object variable in any situation where you would use the specific object itself. Using the object variables from the previous paragraph:

oPlayer1.value

is the same as:

document.getElementById(“MaxWins”).Player1.value

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Bear in mind that you assign objects to object variables. You would assign a text box or a button or an image etc to an object variable and then refer to that object’s properties as shown above (oPlayer1.value). You don’t assign text or string values to objec t variables. So:

oPlayer1 =

            document.getElementById(“MaxWins”).Player1.value

would merely assign the value stored in Player 1 to the variable oPlayer 1 .

            Hopefully it is obvious that you don’t need to include the ‘o’ at the beginning of the object variable’s name. It’s just a convention to help distinguish between the different types of variables.

Project

            Open your previous project file, and save it under the name

chapter_34.htm l .

            Modify the function in the head area script element in the following way:

             All specific object which are referred to more than once are each assigned their own object variable at the start of the function.

             References to specific objects in the code are replaced by the appropriate object variables.

            Test your work in your browser to ensure that it functions as before.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

35 Actions From Menu Items

Key Points

            The HTML <select > form tag enables you to create a menu (select box) of options from which the user can choose:

<form id=”menu”>

<select name=”Product”>

<option value=”one”>Image one</option> <option value=”two”>Image two</option> <option Value=”three”>Image three</option>

</select>

</form>

            Ordinarily, selecting an option from a select box merely specifies the value of the select box. This is then used for further processing – either by JavaScript or by the server.

            You can use JavaScript to invoke actions based on the current value of a select box (the selected option). These actions might be directly loading another page or performing some other type of processing.

            Another name for this type of action is a “jump menu”.

            In order to do this, you need to know that each select box on a form has a select object associated with it. Using the above example, you can therefore access the current value of the Product select box (ie the value of its currently selected option) which is located on the ProductMenu form, in the following way:

document.getElementById(“menu”).Product.value

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            As you would expect, the select option has methods and event handlers associated with it:

             The focus() method gives the focus to a select box.

             The blur() method removes the focus from the select box.

            The available event handlers for the select object are given below:

| Event handler | Runs JavaScript code when…. |
| onblur | The select box loses the focus |
| onfocus | The select box receives the focus |
| onchange | The select box has had its value modified |

            The way to invoke action(s) when the user selects an option from a select box is to prepare a JavaScript function which will be invoked using the select object’s onchang e event handler:

<select name=”name” onchange=”functionname()”>

Project

            Open your previous project file, and save it under the name

chapter_35.htm l .

            Clear the head section script element of JavaScript, and remove all content from the body area of the page.

            Create a form in the body area of the page. Give the form an id of jumpMenu .

            In the form, place a select element. Give the select element the following values and labels eg:

<select name=”menu”>

<option value=” value ”> label </option>

…

</select>

Value Label

![](Image00004.jpg)

http://www.bbc.co.uk/ The BBC

http://www.google.com/ Google

http://www.hotmail.com/ Hotmail

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

| http://www.ed.ac.uk/ | The University of Edinburgh |
| http://www.apple.com/ | Apple Computer |
| http://www.microsoft.com/ | Microsoft Corporation |

            Finally, add an option element to the beginning of your menu like so:

<option value=””>Select a destination</option>

            We are now going to use the menu’s onchang e event handler to invoke a function we are about to define. The function is to be called jump_to_page( ) .

            Define such a function in the head area script element. The function should:

             Create an object variable referencing the form element that represents the menu.

             Get the value of the menu at that moment.

             If the value is not equal to “” (ie, if a valid selection has been made), the function should use the use JavaScript to load the selected page into the browser.

            Check your work in your browser.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

36   Requiring Form Values or Selections

Key Points

            Form data may be invalid if it is sent to the server without certain information – for example, if the user has omitted to select an item from a menu. Better not to bother processing, than to waste the time of the user and server by trying to process the invalid information.

            In the case of a selection box, one way of validating is to include a null value for the default option. In the previous project, the default value of the selection box (always the first option unless specified otherwise) was “”. If the user doesn’t actively make another selection, then you can check the value of the selection box before sending it to the server.

            Another example is the case of a set of radio buttons. Imagine that for an imaginery company, an order form contained two form elements – a selection box to specify which product was being ordered and two radio buttons to specify whether it was being ordered as a photographic print or as a slide.

            Let’s say the id of the order form is OrderFor m and the name of each radio button is Forma t . (Remember that in HTML, radio buttons in a set are related to each other by their name that must be the same for each related radio button).

            The radio object is an array where each element of the array stores information relating to each of the radio button objects (remember, counting starts at 0).

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            As the name is identical for each radio button in the set, you can’t access an individual radio button by using its name. But you can access it using the standard array notation:

oOrderForm.Format[i]

where in this case, I is an integer between 0 and 1, and oOrderForm is an object variable pointing to the for m element.

            Radio buttons in a set each have a checked property that stores a Boolean value specifying whether or not a radio button is checked. Obviously, you can access this value in the following way:

oOrderForm.Format[i].checked

            So, to verify that in a set of radio buttons, at least one of them is checked, all you have to do is loop through each of the radio buttons using the array’s length property to specify the number of iterations of the loop:

FormatSelected = false;

oOrderForm =

            document.getElementById(“OrderForm”);

for ( i=0; i < oOrderForm.Format.length; i++ )

{

if ( oOrderForm.Format[i].checked )

{

FormatSelected = true;

}

}

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            In our order form example, one of the products might only be available as a slide. You could use the onchang e event handler of the selec t object to invoke a function which automatically sets the value of the relevant radio object’s checked property:

function SetFormat ()

{

oOrderForm =

            document.getElementById(“OrderForm”); if ( oOrderForm.Product.value ==

             “Greek Boat” )

{

oOrderForm.Format[0].checked = true;

}

}

where Produc t is the name of the select box, Forma t is the name of the group of radio buttons and the value of the first ratio button is Slide.

            Finally, to reset all form objects to their initial state, use the reset() method:

oFormObject.reset()

Project

            Open your previous project file, and save it under the name

chapter_36.htm l .

            Remove all content from the body section of the page.

            Copy the file order_form.htm l from the network, and open it using NotePad’s File > Open command.

            Copy and paste the entire contents of order_form.htm l into your current project file, into the body element of the page.

            Remove all JavaScript code from the script element in the head section of the page.

            Take some time to open your project file in a browser, and study the code.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Add an event handler to the form element on your page that will invoke a function called check_form( ) when the form is submitted. This function will return tru e or fals e depending on whether the form passes a number of tests as described below. Remember to precede the event handler’s function call with retur n to ensure that the form awaits confirmation from the function before proceeding.

            Create the check_form( ) function in the head area script element. The function should perform the following steps:

             If the current value of the selection menu is “”:

             Display an alert with the message “ please select a product ”

             Give focus to the menu

             Return false

             If no radio buttons are selected:

             Display an alter with the message “ please specify a format ”

             Return false

             Otherwise, return true

            Check your work in your browser.

            The Greek Fishing Boat is only available in Slide format. Add an event handler to the select element which will run a function called set_format( ) when its value is changed.

            Create the function set_format( ) in the head area script element. The function should check first what the value of the menu is. If it is the Greek Fishing Boat , it should then check to see if the Slide radio button is checked. If it is not, then the function should correct this.

            Check your work in your browser.

            Modify your check_form() function to check that, if the value of the menu is Greek Fishing Boat, then the Slide radio button is checked. If not, it should report the error as before.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Finally, note that your check_form( ) function is currently not very efficient, in that it will only report one error at a time. This can be tedious for an error prone user, and it is much better practise to observe a form for all errors simultaneously.

            Create a variable at the beginning of the function called erro r . Set the value of this variable to “”.

            Instead of using an alert box each time an error is found, add the error message to the end of the variable, eg

error += “error message\n”;

(note the new line code at the end of each message)

            After all checks have been made, if we have caught any errors, the value of erro r will no longer be “”. Thus, we can use the following code to report all errors at once:

if ( error != “” )

{

alert(“The following errors were found: \n\n”

         error); return false;

}

else

{

return true;

}

            Modify your function to be more efficient.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

37 Working with Dates

Key Points

            The date object stores all aspects of a date and time from year to milliseconds.

            To use a new date object, you must create it and assign it to an object variable simultaneously. The following code creates a new date object which stores the current date and time and assigns it to the variable dtNow

dtNow = new Date();

            You can specify your own parameters for the date object when you create it:

theDate = new Date(

year, month, day, hours,

minutes, seconds, mseconds

);

            Note that months are represented by the numbers 0 to 11 (January to December). Days are represented by 1 to 31, hours by 0 to 23, minutes and seconds by 0 to 59 and milliseconds by 0 to 999.

            The following code stores 17 th July 2004 at 9:15:30pm in the variable theDat e :

theDate = new Date(2004,6,17,21,15,30,0);

            The first three parameters are mandatory, while the rest are optional:

theDate = new Date(2004,6,17);

gives you midnight of the date above.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            You can assign a date to a variable using a string in the following way:

theDate =

new Date(“Sun, 10 Oct 2000 21:15:00 – 0500);

            Everything from the hours onwards is optional, and in practical terms the day is not necessary either. For example:

theDate = new Date(“10 Oct 2000”);

is a valid date.

Project

            Open your previous project file, and save it under the name

chapter_37.htm l .

            Remove all content from the body section of the page.

            Create a function in a head section script element that displays an alert box containing the current date and time. Have this function called from a body section script element.

            Now modify your script so that it also writes the date and time 17 th July 1955 1:00am to the page in standard date and time format. Do this by entering the appropriate parameters into the new Date() constructor.

            Now, using parameters once again, add a new line to your script that will display midnight on 17 th July 2004 on a separate line under the existing date.

            Finally, using the string approach in the date object, add a new line to your script which will display midnight on 31 st December 1999 on a separate line under the existing information and in standard date and time format.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

38   Retrieving Information from Date Objects

Key Points

            Below is a selection of some useful methods which enable you to retrieve some useful information from date objects:

| Method | Returns |
|  |  |
| getDate() | The day of the month (1-31) |
|  |  |
| getDay() | The day of the week (0 = Sunday, 6 = Saturday) |
|  |  |
| getFullYear() | The year as four digits |
|  |  |
| getHours() | The hour (0-23) |
|  |  |
| getMilliseconds() | The milliseconds (0-999) |
|  |  |
| getMinutes() | The minutes (0-59) |
|  |  |
| getMonth() | The month (0-11) |
|  |  |
| getSeconds() | The seconds (0-59) |
|  |  |
| getTime() | The date and time in milliseconds – also called Unix |
|  | Time |
|  |  |

            JavaScript stores date and time information internally as the number of milliseconds from 1 st January 1970\. This is common to most programming languages, and is actually the way most computer systems store time information.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            For example:

dtNow = new Date();

document.write(dtNow.getTime());

writes the number of milliseconds that have passed since 1 st January 1970.

            Being aware that there are 1000 milliseconds in a second, 60 seconds in a minute, 60 minutes in an hour and 24 hours in a day, you can establish the number of days (or hours or minutes etc) between two dates by subtracting on date in millisecond format from the other in millisecond format. To achieve the units you require, perform the appropriate division (so for the number of minutes, divide the result of the subtraction first by 1000, then by 60), and then use Math.floor() on the result to round the number down as required.

Project

            Open your previous project file, and save it under the name

chapter_38.htm l .

            Clear any JavaScript from the page’s script elements.

            Create a function in the head section script element that performs the following:

             Create two arrays, one storing the days of the week (“Sunday”, “Monday” etc), the other storing the months of the year (“January”, “February” etc)

             Use a new date object, along with the arrays and the appropriate date methods to write today’s date to the page in the following format:

Today it is: dayName, month, dayNumber. for example:

Today it is Tuesday, October 17.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

             Below the date, write the time in the following format: It is currently hh:mm am (or pm)

Note: to convert from the 24hr clock, subtract 12 from any value over 12, and replace a zero value with 12\. Anything greater than or equal to twelve should receive a “pm” suffix.

             Below the time, write the number of days since the start of the millennium in the following format:

It is n days since the start of the millennium.

            Finally, call your function from the body area script element on your page, and check your work in your browser.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

39 Creating a JavaScript Clock

Key Points

            setTimeout() is a method of the window object. In it s common form, it enables you to run any JavaScript function after an allotted time (in milliseconds) has passed. For example:

window.setTimeout(“functionName()”, 1000)

will run functionName( ) after one second. Note the quote marks!

            You can have any number of “timed out” methods running at any one time. To identify each “timeout”, it is a good idea to assign the return value of each one you create to an object variable:

firstTimeout =

window.setTimeout(“functionName()”, 1000)

            The most common reason to track timeouts is to be able to cancel them if necessary – for example, you may wish a window to close after 5 seconds unless a button is clicked:

firstTimeout =

window.setTimeout(“window.close()”, 5000);

adding the following code to the button’s onclic k event handler:

window.clearTimeout(firstTimeout);

will do the trick.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Ordinarily, it is a bad idea to “recurse” a function – to have a function call itself. For example, imagine the annoyance of the following:

function annoy_me( )

{

window.alert(“BOO!”);

annoy_me();

}

This will potentially keep popping up alert boxes, and perhaps even lock up the user’s computer!

            However, you may wish a function to use a setTimeou t method to call itself periodically. Imagine a function that calls itself every second to check on the time, and then displays the result in the same place. In effect, this could be seen as a digital clock.

            If you want to clear the clock’s timeout – which in this case would stop the clock – the timeout must already be in operation. You can’t clear a timeout that doesn’t yet exist. So, you have to check first whether a timeout is in operation. One way of doing this is to set a Boolean variable to true whenever the clock is started. By checking this variable before you attempt to clear the timeout, you know whether or not the clock is running and therefore can be stopped.

            To show an am/pm clock you obviously need to carry out the conversion you created in the previous chapter’s project.

            But, so as the display doesn’t show a “moving” effect at different times, you need to consider the situation where either the minutes or seconds on the clock are fewer than 10\. For example, consider:

10:59:59 am

changing to:

11:0:0 am

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            In this situation, we need to concatenate an extra “0” on to the front of the actual value to produce:

11:00:00 am

as we might expect.

            We can use a shortened form of the if conditional to make this simple. For example:

s = theDate.getSeconds;

s = ( s < 10 ) ? “0” + s : s;

            What is happening here? First, we get the current value of the seconds and store that in a variable called “s”. Next, we reset the value of s depending on the condition in the brackets. The prototype of this form of the if conditional is:

var = ( condition )

? value if true

: value if false;

in other words, we can think of the ? as being like the opening brace { of an if conditional, the : as being the } else {, and the ; as being the closing brace. The result of the conditional test is then stored in var.

Note that this has been split over three lines to aid reading. In practice (see above) we can place this on one line for ease of use.

Project

            Open your previous project file, and save it under the name

chapter_39.htm l .

            Remove all content from the body section of the page.

            In the body section, create a form input element with the id clockBo x , and two form input buttons labelled Start and Stop.

            In the head section scrip element, create two empty functions –

start_clock() an d stop_clock().

            Before the two function definitions, as the first statement of the script element, create a variable called time r , and assign it a value of nul l .

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            Immediately below that statement, create a variable called timer_running. Assign it a value of false.

            We will use these variables to track the clock’s status.

            Now, add statements to the start_clock() function that will:

             Get the current time.

             Format the current time as hh:mm:ss am/pm (as appropriate).

             Display the formatted time in the text field on the page.

             Create a timeout which will run the start_clock( ) function again in half a second, and assign that timeout’s return object to the time r object variable.

             Set the timer_runnin g variable to tru e .

            Add statements to the stop_clock( ) function that will:

             Check to see if the clock is running.

             If it is, clear the timer timeout and set timer_runnin g to

fals e .

            Finally, add event handlers to the two form buttons to ensure that the one labelled Stop calls the function stop_clock( ) when clicked, and the one labelled Start calls the function

start_clock() when clicked.

            While this should work (test your code!), you’ll notice that the output is a little ugly. Displaying the time in a text field is not the most unobtrusive way to show a clock on a page.

            Luckily, we can modify our code very slightly to achieve something much more professional.

            Replace your input field with the following:

<span id=”clockBox”></span>

            <span> is an HTML tag that allows you to mark areas o f content without any semantic meaning – eg, the clock is not a paragraph or a header, so we don’t want to label it as such.

![](Image00000.jpg)

| JavaScript for Beginners |  |
|  |  |  |
|  |  |  |

            With JavaScript, we can control the content of just about any element on the page. In our previous example, we used getElementById (hopefully!) to obtain a reference to th e input field, and then altered its valu e property to show our clock.

            Since we are using the same id value here, we do not have to alter our function too much. However, the getElementByI d method now returns a different type of object – one that has no value property.

            However, all content tags in HTML (like <p > , <h1 > , <div > etc) have a special property when they are returned as JavaScript objects which refers to their text content – the property is innerHTM L .

            We can use this to alter the content of the tags. For example, if our previous input-field solution had the following code:

clk = document.getElementById(“clockBox”); clk.value = formatted_time;

where formatted_tim e is a variable containing the formatted time as required, then replacing it with this code:

clk = document.getElementById(“clockBox”); clk.innerHTML = formatted_time;

will allow us to use the modified <span > element in place of the <input > element.

            Try adapting your code to use this method of displaying content on the page.

![](Image00000.jpg)

Advanced JavaScript Essentials

Lesson 1: Int ro duct io n t o Advanced JavaScript

Welcome to Advanced JavaScript

Accessing the Console

Using the Console

Good Programming Style Practices

Testing Code in the Console

Interacting Directly in the Console

Commenting Your Code

[Quiz](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) 1

Lesson 2: Kno w Yo ur T ypes

Know Your Types: Primitives and Objects

Primitives

Some Interesting Numbers

Objects

Enumerating Object Properties

Primitives That Act like Objects

JavaScript is Dynamically Typed

[Quiz](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) 1 [Project 1](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) [Project 2](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) [Project 3](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX)

Lesson 3: T rut hy, Falsey, and Equalit y

Truthy, Falsey, and Equality

Values That are Truthy or Falsey

Implied Typecasting

Testing Equality

Objects and Truthy-ness

Objects and Equality

[Quiz](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) 1 [Project 1](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) [Project 2](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX)

Lesson 4: Co nst ruct ing Object s

Constructing JavaScript Objects

Constructing an Object with a Constructor Function

Constructing an Object Using a Literal

Constructing an Object Using a Generic Object Constructor So, What's the Best Way to Make an Object? Initializing Values in Constructors

this

Constructing Array Objects

[Quiz](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) 1 [Project 1](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) [Project 2](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX)

Lesson 5: Pro t o t ypes and Inherit ance

Object-Oriented Programming in JavaScript

instanceof

Prototypes

Prototypes of Literal Objects

What is a Prototype Good For?

The Prototype Chain

Prototypal Inheritance

When are Prototype Objects Created?

hasOwnProperty

__proto __

Setting the Prototype Property to an Object Yourself

[Quiz](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) 1 [Quiz 2](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) [Project](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) 1 [Project 2](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX)

Lesson 6: Funct io ns

JavaScript Functions

What is a Function?

Different Ways of Defining a Function

Functions as First Class Values

Anonymous Functions

Returning a Function from a Function

Functions as Callbacks

Calling Functions: Pass-by-Value

Return

[Quiz](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) 1 [Quiz 2](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) [Project](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) 1 [Project 2](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX)

Lesson 7: Sco pe

Scope

Variable Scope

Function Scope

Hoisting

Nested Functions

Lexical Scoping

Scope Chains

Inspecting the Scope Chain

[Quiz](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) 1 [Project 1](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX)

Lesson 8: Invo king Funct io ns

Invoking Functions

Different Ways to Invoke Functions

What Happens to this When You Invoke a Function

Nested Functions

When You Want to Control How this is Defined

call() and apply()

Function Arguments

The Four Ways to Invoke a Function

[Quiz](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) 1 [Project 1](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) [Project 2](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX)

Lesson 9: Invo cat io n Pat t erns

Invocation Patterns

Recursion

Why Use Recursion?

Chaining (a la jQuery)

Static vs. Instance Methods

[Quiz](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) 1 [Project 1](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) [Project 2](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) [Project 3](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX)

Lesson 10: Encapsulat io n and APIs

Encapsulation and APIs

Privacy, Please

An Example

Private Variables

Private Functions

A Public Method

Acessing a Public Method from a Private Function

Encapsulation and APIs

[Quiz](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) 1 [Project 1](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) [Project 2](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX)

Lesson 11: Clo sures

Closures

Making a Closure

What is a Closure?

Playing with Closures

Each Closure is Unique

Closures Might Not Always Act Like You Expect

Closures for Methods

Using Closures

Where We've Used Closures Before

[Quiz](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) 1 [Project 1](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX)

Lesson 12: T he Mo dule Pat t ern

Module Pattern

IIFE or Immediately Invoked Function Expressions

The Module Pattern

Using the Module Pattern with JavaScript Libraries

A Shopping Basket Using the Module Pattern

Why Not Just Use an Object Constructor?

[Quiz](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) 1 [Project 1](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX)

Lesson 13: T he JavaScript Enviro nment

JavaScript Runs in an Environment

The Core Language, and the Environment's Extensions

How the Browser Runs JavaScript Code

Including JavaScript in Your Page

The JavaScript Event Loop

The Event Queue

Asynchronous Programming

JavaScript in Environments Other Than the Browser

[Quiz](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) 1 [Project 1](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX)

Lesson 14: ECMAScript 5 .1

The ECMAScript Standard for JavaScript

Strict Mode

New Methods

Object Property Descriptors

Sealing and Freezing Objects

Creating Objects

[Project](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) 1 [Project 2](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX)

![](Image00005.jpg)

Introduction to Advanced JavaScript

![](Image00005.jpg)

Lesson Objectives

When you complete this lesson, you will be able to:

use OST's Sandbox and learning tools.

![](Image00006.jpg)

read about what to expect in the Advanced JavaScript course.

![](Image00006.jpg)

review JavaScript basics.

![](Image00006.jpg)

use the Developer Tools in your browser to access the JavaScript console, which we'll be using extensively in this course.

![](Image00006.jpg)

use console.log to display messages in the console (for debugging).

![](Image00006.jpg)

use good programming practices in your code.

![](Image00005.jpg) ![](Image00006.jpg)

Lesson Format

We'll try out lots of examples in each lesson. We'll have you write code, look at code, and edit existing code. The code will be presented in boxes that will indicate what needs to be done to the code inside.

Whenever you see white boxes like the one below, you'll type the contents into the editor window to try the example yourself. The CODE TO TYPE bar on top of the white box contains directions for you to follow:

![](Image00007.jpg)

CODE TO TYPE:

White boxes like this contain code for you to try out (type into a file to run).

If you have already written some of the code, new code for you to add looks like this .

If we want you to remove existing code, the code to remove will look like this .

We may also include instructive comments that you don't need to type.

We may run programs and do some other activities in a terminal session in the operating system or other command-line environment. These will be shown like this:

![](Image00008.jpg)

INTERACTIVE SESSION:

The plain black text that we present in these INTERACTIVE boxes is

provided by the system (not for you to type). The commands we want you to type look lik e this .

Code and information presented in a gray OBSERVE box is for you to inspect and absorb . This information is often color-coded, and followed by text explaining the code in detail:

![](Image00009.jpg)

OBSERVE:

Gray "Observe" boxes like this contain information (usually code specifics) for you to observe .

The paragraph(s) that follow may provide addition details on inf o rmat io n that was highlighted in the Observe box.

We'll also set especially pertinent information apart in "Note" boxes:

![](Image00010.jpg)

Note Notes provide information that is useful, but not absolutely necessary for performing the tasks at hand.

![](Image00011.jpg) ![](Image00012.jpg)

Tip Tips provide information that might help make the tools easier for you to use, such as shortcut keys.

![](Image00013.jpg) ![](Image00014.jpg)

WARNING Warnings provide information that can help prevent program crashes and data loss.

![](Image00015.jpg)

The CodeRunner Screen

This course is presented in CodeRunner, OST's self-contained environment. We'll discuss the details later, but here's a quick overview of the various areas of the screen:

![](Image00016.jpg)

These videos explain how to use CodeRunner:

[File Management Demo](http://www.youtube.com/watch?v=45sATp529Mw)

[Code Editor Demo](http://www.youtube.com/watch?v=SvbM6vPAG9k)

[Coursework Demo](http://www.youtube.com/watch?v=WmajY8bIXrA)

Welcome to Advanced JavaScript

You can get started with JavaScript quickly. All you need is a text editor and a browser, and you can begin experimenting. When you learned the basics of JavaScript, you probably used it to modify web pages, and maybe to modify the style of your pages in response to user input. You've probably written event listeners to handle events like click events, and you've most likely used JavaScript to validate form data or add and remove elements from your page as users interact with it.

In this course, we'll focus on the JavaScript language itself. Since the primary place we use JavaScript is in the browser to create interactive web pages, we'll still build web page applications, but the focus will be on language features, rather than on web interfaces and the techniques we use to create web apps. The goal of this course is to take your understanding of JavaScript to a deeper level, from scripter to programmer. You'll learn how to leverage the powerful features of JavaScript in your programming, as well as how to avoid common mistakes.

Accessing the Console

We'll make frequent use of the console to view the output we generate with co nso le .lo g , as well as to inspect code. So, before we do anything else, let's make sure you're comfortable with the developer console, and you remember how to access and use it in each of the major browsers. Most end users never see the console because it's for developers who are creating, testing, and debugging code, so if you haven't had experience with the console before, don't worry, we'll get you up to speed quickly.

In this course, we'll show most examples using the Chrome browser console, because, as of this writing, it has the most functionality and is the easiest to use of the browser consoles. But you should become familiar with multiple browser consoles for testing and debugging your code.

![](Image00017.jpg) Browsers are continualy updated with new versions that include new versions of the console. Note   So, while the basic functionality of the console will likely remain the same, your version of the console may look slightly different from what you see in this course. As you become familiar

with the different browser consoles, you'll be able to figure out how to use each one.

![](Image00018.jpg)

Create a folder for your work. In the File Browser, right- click the Ho me folder and select New f o lder... (or click the Ho me folder and press Ct rl+n ), type the new folder name AdvJS , and press Ent er .

Now create a new HTML file, then add this code:

![](Image00019.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Getting Started </title>

<meta charset="utf-8">

<script src="basics.js"></script>

</head>

<body>

</body>

</html>

Save this as basics.ht ml in your /AdvJS folder.

Now create a new JavaScript file and add this code:

![](Image00020.jpg)

CODE TO TYPE:

var onSale = true,

inventoryLevel = 12,

discount = 3;

if (onSale && inventoryLevel > 10) {

console.log("We have plenty left");

}

if (onSale || discount > 0) {

console.log("On sale!");

} else {

console.log("Full price");

}

Save this as basics.js in your /AdvJS folder.

Now ![](Image00021.jpg) preview your basics.ht ml file. You'll see an empty web page. To see the result of the JavaScript, open up your browser's console. To get instructions to access your console, click on the link to whichever browser you're using:

Chrome

![](Image00006.jpg)

Safari

![](Image00006.jpg)

Firefox

![](Image00006.jpg)

Internet Explorer

![](Image00006.jpg)

To access the console in Chrome, use the View | Develo per | JavaScript Co nso le menu:

![](Image00022.jpg)

Once you've enabled the console, you may need to reload the page to see the output. You'll see:

![](Image00023.jpg)

There are many parts to the console. You'll become more familiar with some of them as we work through the course.

Continue to the next step.

To access the console in Safari, use the Develo p | Sho w Web Inspect o r menu (if you don't have Develo p enabled, you can enable it with Pref erences | Advanced | Sho w Develo p menu in menu bar ):

![](Image00024.jpg)

You might need to reload the page to see this output:

![](Image00025.jpg)

In order to see the output in the the Safari console, make sure you have selected the Lo g tab in the console, and you have the "Current log" at the top of the list on the left panel selected. (You may only see one log, but if you reload the page you could see previous logs. The current log is always at the top. This is where your most recent output from co nso le .lo g will appear).

Continue to the next step.

To enable the Firefox console, use the T o o ls > Web Develo per > Web Co nso le menu and access the console:

![](Image00026.jpg)

You may need to reload the page to see the output in the console. Note that in Firefox, the default location for the console is above the web page (unlike Chrome and Safari). You can click on the Po sit io n menu in the console and select "bottom" or "window" to change the position of the console. Choosing "window" will pop the console out into a separate window.

![](Image00027.jpg)

Continue to the next step.

To enable the Internet Explorer console, select T o o ls | F12 Develo per T o o ls and then select the Co nso le tab.

![](Image00028.jpg)

You may need to reload the page to see the output in the console.

Using the Console

Let's take a closer look at the Chrome console since that's the one we'll use in our examples throughout the course. Other browser consoles have the same basic functionality. We'll let you know when you need to use the Chrome console specifically to follow along.

![](Image00023.jpg)

There are several tabs across the top of the console, including the one we're on, Co nso le . You'll use

Co nso le most often when looking at the results of co nso le .lo g() , and debugging your code by checking to see if there are any JavaScript errors. In Safari, the equivalent is the Lo g tab shown in the screenshot; in Firefox, it's the default view you see when you access Web Co nso le from the menu, and in IE, it's a tab labeled Co nso le .

In Chrome, if you want to view the console into a separate window, click on the icon in the bottom left corner:

![](Image00029.jpg)

Click the undo ck icon now. This will create a separate window for the console. You can click the icon in the same location in that new window to dock it back to the original window. Give it a try.

You see two messages in the console that we created using co nso le .lo g in our code:

![](Image00030.jpg)

OBSERVE:

var onSale = true,

inventoryLevel = 12,

discount = 3;

if (onSale && inventoryLevel > 10) {

console.log("We have plenty left");

}

if (onSale || discount > 0) {

console.log("On sale!");

} else {

console.log("Full price");

}

The two co nso le .lo g() messages shown in orange above create the output in the console. The file name in which the statements appear and the line numbers of the two statements are displayed in the console, next to the output.

In Chrome, try clicking one of the line numbers, like basics.js:5 . This will open the Sources tab, and highlight that line in yellow temporarily:

![](Image00031.jpg)

This can help you track down potential bugs. There are whole lot of options on the right side of the "Sources" panel, including "Call Stack," "Scope variables," and "Breakpoints," all of which we'll use later as we get into some more advanced topics. Make sure that you have downloaded Chrome and have the latest version installed on your computer for testing. As of this writing, the current version is 26 . Your version may be different, but that's okay because the basic functionality of the console is the same.

![](Image00032.jpg)

Unfortunately, at this time, the other browsers don't come with the same tool installed by default. Note Go ahead and download Chrome and get familiar with the console tools, even if you typically

use another browser to create web pages.

![](Image00018.jpg)

We'll explore more of the console later, but for now we'll take a closer look at the code.

Good Programming Style Practices

Let's review some good practices for writing JavaScript programs:

![](Image00030.jpg)

OBSERVE:

var onSale = true,

inventoryLevel = 12,

discount = 3;

if (onSale && inventoryLevel > 10) {

console.log("We have plenty left");

}

if (onSale || discount > 0) {

console.log("On sale!");

} else {

console.log("Full price");

}

T he variables we use are all declared at t he t o p and given def ault values . In general, it's good practice to declare your variables at the top of your file (or at the top of a function, if they are local variables), and to give them values. A variable that is not given a value is undef ined . That's okay, but you need to be aware of which variables have values and which don't as you write your program. It's usually better practice to give your variables default values, rather than leave them undefined.

We've used the comma-separated style to declare the variables. It's also a good idea to put each variable declaration on a separate line. Still, you can always declare them with separate statements instead, like this:

![](Image00033.jpg)

OBSERVE:

var onSale = true;

var inventoryLevel = 12;

var discount = 3;

Either way is fine, so just do whatever you prefer.

Next, you'll see that we're using semicolons after every statement. While JavaScript doesn't require this currently, it's a good habit to develop. If you leave the semicolon off, JavaScript might interpret your statements and expressions in a way you're not anticipating. If you're in the habit of leaving off your semicolons, even occasionally, start putting them in after every statement. It will make debugging your code a whole lot easier. We suspect that future versions of JavaScript may require semicolons to delimit statements anyway, so you may as well get in the good habit now!

![](Image00030.jpg)

OBSERVE:

var onSale = true,

inventoryLevel = 12,

discount = 3;

if (onSale && inventoryLevel > 10) {

console.log("We have plenty left");

}

if (onSale || discount > 0) {

console.log("On sale!");

} else {

console.log("Full price");

}

Another habit you should get into is using curly braces for every if (or while or f o r , and such) block of code, even if there's just one statement in the block. If you have only one statement in a block, technically you don't need to use the { and } characters to delimit the block. However, this is a bad habit because it can cause you to miss errors. Always use the curly braces!

Use plenty of white space. It's better to add more white space and format your code so it's easy to read, than to scrimp on space to make your code shorter. Readability is vital when working on larger, more complex programs, and it's always possible to "minify" your JavaScript later to take out the white space and make it more efficient to download.

![](Image00034.jpg)

| Note | There are plenty of "minification" programs out there that can minify your code for you such as |
| [jscompress.com](http://jscompress.com) and [YUI compressor](http://refresh-sf.com/yui/) . |
|  |
|  |  |  |  |  |
|  |  |  |  |  |

![](Image00018.jpg)

We'll cover other good programming practices and style suggestions throughout the course. We'll review them at the end of each lesson, so you'll get plenty of practice. There are also quite a few good style guides online if you want to explore this topic further (not all of them agree on everything, of course). We like the [Airbnb JavaScript Style Guide (github)](https://github.com/airbnb/javascript) .

Testing Code in the Console

Let's practice using the console to inspect values in our code. Update your file basics.js to define an object, rect , and then display it using console.log. Here, we define rect as an object literal ; that is, an object we write as the value of the variable using the { and } characters to delimit the object. Remember, an object is just a collection of key value pairs. In this case rect has just two properties—width and height:

![](Image00035.jpg) CODE TO TYPE:

var onSale = true,

inventoryLevel = 12,

discount = 3;

if (onSale && inventoryLevel > 10) {

console.log("We have plenty left");

}

if (onSale || discount > 0) {

console.log("On sale!");

} else {

console.log("Full price");

}

var rect = {

width: 100,

height: 50

};

console.log(rect);

Save your changes ( basics.js ), and ![](Image00036.jpg) preview your HTML file ( basics.ht ml ), or simply reload the page if you still have it open in the browser. Make sure the browser console is open (you might have to reload the page to see the output). You'll see this output:

![](Image00033.jpg)

OBSERVE:

We have plenty left

On sale!

Object { width: 100, height: 50 }

In Chrome, it will look like this:

![](Image00037.jpg)

In Safari, it will look like this (make sure you click the little arrow next to the Object to see the object properties):

![](Image00038.jpg)

In Firefox, it will look like this:

![](Image00039.jpg)

In IE, it will look like this:

![](Image00040.jpg)

Notice that each is just a little different, but each console shows you the same basic information about the object, including the two property name/value pairs.

Now, let's make a small change to the code:

![](Image00041.jpg)

CODE TO TYPE:

var onSale = true,

inventoryLevel = 12,

discount = 3;

if (onSale && inventoryLevel > 10) {

console.log("We have plenty left");

}

if (onSale || discount > 0) {

console.log("On sale!");

} else {

console.log("Full price");

}

var rect = {

width: 100,

height: 50

};

console.log(rect);

console.log("My object rect is: " + rect);

![](Image00042.jpg) and ![](Image00021.jpg) . In the console, you see:

![](Image00043.jpg)

OBSERVE:

Object { width: 100, height: 50 }

My object rect is: [object Object]

Why do you think this is? Instead of seeing the two properties that the onject contains like we did before, we see just a string representation of the object, "[object Object]". That isn't really helpful. In our code, we're creating a string by concatenating the object, rect , with the string "My object rect is: ", before outputting the result to the console. Previously, we passed the object itself to co nso le .lo g() , so the co nso le .lo g() function displayed the object. Now we're passing a string to co nso le .lo g() . When JavaScript converts the object to a string, we don't get a very useful display of the object.

Make one last change to your code:

![](Image00044.jpg)

CODE TO TYPE:

var onSale = true,

inventoryLevel = 12,

discount = 3;

if (onSale && inventoryLevel > 10) {

console.log("We have plenty left");

}

if (onSale || discount > 0) {

console.log("On sale!");

} else {

console.log("Full price");

}

var rect = {

width: 100,

height: 50 ,

toString: function() {

return "Width: " + this.width + ", height: " + this.height;

}

};

console.log(rect);

console.log("My object rect is: " + rect);

console.log("My object rect is: " + rect.toString());

Don't forget the comma after the height property value! We added a method to this object as the third

property value, so we need a comma between the second and third properties. ![](Image00042.jpg) and ![](Image00021.jpg) .

![](Image00033.jpg)

OBSERVE:

Object { width: 100, height: 50, toString: function }

My object rect is: Width: 100, height: 50

My object rect is: Width: 100, height: 50

The t o St ring method is now shown as part of the rect object in the output from co nso le .lo g(rect ) , which you can see in t he f irst line o f o ut put abo ve . The line of code we just added calls this method to display the width and height properties of the object, which you can see in t he t hird line o f o ut put abo ve .

However, the seco nd line that displayed "[object Object]" before, now displays the same as the third line. That's because JavaScript automatically calls the t o St ring() method when converting an object to a string. If you implement the t o St ring() method yourself in an object, then that's the method JavaScript will call. If you don't, then JavaScript calls the t o St ring() method in the Object object, which is the parent object of all objects you create in JavaScript. The version of t o St ring() that's implemented in the Object object doesn't do a very good job of creating a helpful string from the object, as you saw when "[object Object]" was displayed.

Don't worry about these details right now; we'll come back to all that later. For now just note the different ways that the console displays output, depending on how you call co nso le .lo g() and the kind of value you pass this function.

Here's the output in Chrome. In this screenshot, I've clicked on the line that shows the object properties (the third line in the output), which opens up the object to show more details, including lots of details about the

t o St ring() method. Again, don't worry about these details right now; we'll get to them later in the course, so you'll know what they mean at the end.

![](Image00045.jpg)

Safari (note that you can open up the object, and also the t o St ring() method to see similar details in this console):

![](Image00046.jpg)

Firefox:

![](Image00047.jpg)

See the (2) next to the line of output? That means that the same line of output is displayed twice.

IE:

![](Image00048.jpg)

Interacting Directly in the Console

So far, we've been using co nso le .lo g() to display messages in the console, but you can interact directly with the console to display the values of variables, create new statements, and even modify your web page.

In your browser's console, you'll see a prompt which indicates where you can type your own JavaScript. Click in the console window next to the prompt, and type this:

![](Image00049.jpg)

INTERACTIVE SESSION:

        onSale

true

![](Image00050.jpg)

Note The ">" character is the prompt; you shouldn't type this part.

![](Image00051.jpg)

We typed the name of the global variable o nSale and pressed Ent er . JavaScript responded with the value of o nSale .

Here's what the output looks like in the browsers Chrome, Safari, Firefox, and IE:

![](Image00052.jpg)

![](Image00053.jpg)

![](Image00054.jpg)

We typed the name of a global variable, o nSale that we defined in the code that's currently loaded into this browser window. In response, the console provided the value of the variable, t rue . (Just think of o nSale like an expression). Remember that you can only access global variables via the prompt, that is, variables defined at the global level in the currently loaded page. So far, all of the variables we've defined have been global. When we begin creating functions with local variables, you won't be able to access those via the prompt, but you can always display their values using co nso le .lo g() in your code (we'll look at another way to inspect the values of local variables using the Chrome console later).

Try entering the names of the other global variables we've defined in this small program to see the output ( invent o ryLevel , disco unt , and rect ). Try accessing the properties of the rect object (for example, rect .widt h and rect .height ). Enter some other expressions like 2 + 3, or "test." What happens? What happens if you enter the name of a variable that doesn't exist, like t est Var ?

You can also define new variables at the prompt. This can coe in handy when you just want to try something out without creating a whole new file. For example, try this:

![](Image00049.jpg)

INTERACTIVE SESSION:

var a = [1, 2, 3]; undefined

In this statement, you define a new variable, a , to have the value of an array with three values . You see the value undef ined . That might be a bit confusing at first. It doesn't mean that the value of a is undefined, it just means that the value returned to the console as a result of executing this statement is undefined (that is, the value of the statement itself is undefined).

To verify that you've actually created a value for the array a , type a at the prompt:

![](Image00049.jpg)

INTERACTIVE SESSION:

a

[1, 2, 3]

Now, let's write a loop to iterate over this array, right in the console. To do this, you'll either type the entire for loop on one line, or use Ct rl+Ent er in Chrome and Safari, Shif t +Ent er in Firefox, and click the Multiline mode icon ( ![](Image00055.jpg) ) to create new lines in the console.

![](Image00056.jpg) INTERACTIVE SESSION:

       for (var i = 0; i < a.length; i++) { console.log("a[" + i + "]: " + a[i]);

}

If you forget to create a new line character and over. Once you've got it typed in, press Ent er

press Ent er by mistake, you'll get an error and have to start to complete the code and you'll see this output:

![](Image00033.jpg)

OBSERVE:

a[0]: 1

a[1]: 2

a[2]: 3

What happens if you reload the page? The value of a goes away. Variables that you add using the console are valid only for the current session, and go away when you reload or close the tab or window.

Experiment! Create some new variables and write some JavaScript statements in the console. Get familiar with using the console, especially in Chrome.

Commenting Your Code

Of course, we can't end the lesson without mentioning comments. Comments are an important part of creating readable programs, especially when your programs get large and complex. As you probably know, there are two ways to comment code in JavaScript: /* ... */ and //. Let's give these both a try:

![](Image00057.jpg)

CODE TO TYPE:

/*

var onSale = true,

inventoryLevel = 12,

discount = 3;

if (onSale && inventoryLevel > 10) {

console.log("We have plenty left");

}

if (onSale || discount > 0) {

console.log("On sale!");

} else {

console.log("Full price");

}

var rect = {

width: 100,

height: 50,

toString: function() {

return "Width: " + this.width + ", height: " + this.height;

}

};

console.log(rect);

console.log("My object rect is: " + rect); console.log("My object rect is: " + rect.toString()); */

//

           This function computes the area of a circle

           @param {number} The radius of the circle

           @return {number} The area of the circle

//

function computeArea(radius) {

return radius * radius * Math.PI;

}

console.log("Area is: " + computeArea(3));

Here, we used /* ... */ to comment out large chunks of code. This is standard practice, as the /* and */ delimeters give you a quick and straightforward way to comment multiple lines, which can make testing and debugging easier.

We also used // to create several lines of comments above the new comput eArea() function that we added to the code. We don't put all these comments in /* ... */ though, because if we decide later to comment out the entire function, we can put the whole thing, including the heading comments, inside the /* and */ delimiters, which makes commenting large chunks of code (including multiple functions) a lot easier. Of course, we can use // to comment out single lines of code temporarily for debugging or providing comments within a function.

Finally, notice the style we've used to comment this function.We've provided a brief description for the function, as well as information about the parameter it expects, the radius of the circle, and the value it returns (which is the area of the circle).

We won't always comment the examples extensively, but get in the habit of commenting your project code. Your co -workers (and boss) will appreciate it, and so will you if (when) you need to go back and change your code later.

Take some time to experiment in the console. Add more console.log() statements in the example (or create your own example and experiment with that). Write statements directly in the console.

From here on, we'll show screen shots mostly from Chrome, but you can (and should) try the course examples in multiple browsers. We'll let you know when you need to use a specific browser console for testing.

Now that you've got the basics of using the console down, we'll dive right into the nitty gritty of JavaScript types in the next lesson.

Know Your Types

![](Image00005.jpg)

Lesson Objectives

When you complete this lesson, you will be able to:

differentiate primitives and objects.

![](Image00006.jpg)

categorize primitive types.

![](Image00006.jpg)

distinguish null and undefined.

![](Image00006.jpg)

construct objects.

![](Image00006.jpg)

use the console to experiment with JavaScript types, object properties, and various number representations.

![](Image00005.jpg) ![](Image00006.jpg)

JavaScript only has a few basic types, but they still require consideration. In this lesson, we'll review the basics of primitives and objects, delve into a few details you may not have encountered before, and deepen your understanding of the fundamentals.

Know Your Types: Primitives and Objects

Every value in JavaScript is either a primitive or an object. Primitives are simple types, like numbers and strings, while objects are complex types because they are composed of multiple values, like this square object:

![](Image00058.jpg)

OBSERVE:

var square = {

width: 10,

height: 10

};

This object is composed of two primitive values: a width, with a value of 10, and a height, that also has the value of 10 .

We'll look into primitives first; we'll come back to objects later.

Primitives

The three primitive types you'll work with most often are numbers, strings, and booleans. You can test these types right in the browser's console.

Open the console in a browser window and try typing in some primitive values. Some browsers don't allow you to open the console for an empty page. You can load the web page you created for basics.ht ml in the previous lesson, and then open the console, and trying testing some types, like this:

![](Image00059.jpg)

INTERACTIVE SESSION:

        3

3

        "test"

"test"

        true

true

Let's try an expression:

![](Image00049.jpg)

INTERACTIVE SESSION:

        3 + 5

8

When you type an expression, the result of that expression is a value, which is displayed in the console.

When you type a statement, the result of that statement is (usually) undef ined :

![](Image00060.jpg)

INTERACTIVE SESSION:

var x = 3; undefined

x + 5

8

Here, we declared a new variable, x, in a statement (the first thing you typed into the console), and then used it in the expression x + 5 (the second thing you typed into the console). Even though the statement sets the value of x to 3, the result of the statement itself is undefined. The result of the expression is just the value that the expression computes. Get used to this behavior so you don't get confused when you see undef ined in the console!

Getting the Type of a Value with Typeof

JavaScript has a t ypeo f operator that you can use to check the type of a value. There are a couple of reasons that you don't necessarily want to rely on this operator in your code. We'll get to those reasons a bit, but for now, we'll use t ypeo f to check the type of our primitives, like this:

![](Image00061.jpg)

INTERACTIVE SESSION:

typeof 3 "number"

typeof x "number"

typeof "test" "string"

typeof true "boolean"

The t ypeo f operator might look a little strange at first; it's not like other operators you're used to that take two values. t ypeo f takes just one value, and it returns the type of that value as a string. So the type of the number 3 is returned as the string "number." Notice that we can use t ypeo f on either values (like 3) or variables containing values (like x ).

You can use t ypeo f in an expression, like this:

![](Image00060.jpg)

INTERACTIVE SESSION:

if (typeof x == "number") {

alert("x is a number!");

}

undefined

Remember to use Ct rl+Ent er or Shif t +Ent er at the end of a line in the console to avoid getting an error. Use Ent er at the end of the if statement (after the closing curly brace, } ). Do you get the alert?

We compare the result of the expression t ypeo f x with the string "number" , and if they're equal, alerting a message (yes, you can alert from the console!). The result of the if statement is undef ined .

Null and Undef ined

Now, let's take a look at these primitive types: null and undef ined . You've seen undef ined as the result of statements you typed in the console. It pops up in other places as well, but let's begin with null .

null is a way to say that a variable has "no value":

![](Image00062.jpg) INTERACTIVE SESSION:

var y = null; undefined

if (y == null) { console.log("y is null!");

}

y is null!

undefined > typeof y "object"

Here, we assigned the value null to the variable y . So y has a value—a value that means "no value." Weird. We can compare that value to null , and since y has the value null , that comparision is true, and so we see the message "y is null!" in the console. (Yes, we can call co nso le .lo g() from the console!) Notice that you see "y is null" in the console, and then you see the result of the statement, which is undefined. In Chrome and Safari, the console displays a little ⋖ character next to the undefined result of the statement so you don't mix up the output to the console ("y is null!") with the result of the statement (undefined). In Firefox, you'll see a right-pointing arrow next to the undefined result of the statement.

Weirder still, when you check the t ypeo f y , you get "object" as the result. What? That doesn't seem right. Well, guess what—it's not ! This is an error in the current implementation of JavaScript. The result should be null , because the type of null is null .

![](Image00032.jpg)

This error is one reason you don't want to rely on t ypeo f in your code. This mistake should be Note fixed in future implementations of JavaScript, but for now, just keep this in mind if you ever do

need to use t ypeo f . (There's one other issue with t ypeo f we'll get to later).

![](Image00018.jpg)

Okay, so what about undef ined ? Lots of people confuse null with undef ined when they first start learning JavaScript, so don't worry if it seems a bit murky. While null is a value that means "no value" (a mind bender in itself), undef ined means that a variable has no value at all, not even null:

![](Image00060.jpg)

INTERACTIVE SESSION:

var z; undefined

z undefined

You can create an undefined variable by declaring it and not initializing it. Here, we declared the variable z , but didn't initialize it to a value. When we check the value of z by typing its name in the console, we get the result undef ined .

Don't confuse the undef ined you see as the result of the statement var z; with the undef ined you see that is the result of the expression, z .

So what is the type of undef ined ? Can you guess? (This time, JavaScript has the correct implementation.)

![](Image00049.jpg)

INTERACTIVE SESSION:

typeof z undefined

Yes, the type of undef ined is undef ined !

Even though z is undef ined m (meaning that it has no value), you can test to see if z is undefined, like this:

![](Image00063.jpg) INTERACTIVE SESSION:

       if (z == undefined) { console.log("z is undefined!");

}

z is undefined!

        undefined

Or you can test it like this:

![](Image00064.jpg)

INTERACTIVE SESSION:

       if (typeof z == "undefined") { console.log("z is undefined!");

}

z is undefined!

        undefined

You'll get the same result. Try it! Still, in general, we recommend that you don't use t ypeo f unless you have a good reason. You can test a variable to see it if is undefined directly by comparing the value of the variable (in this case z , to the value undef ined ). You don't really need to use t ypeo f at all here.

Some Interesting Numbers

Before we leave the primitive types, let's talk a little more about numbers. In your JavaScript programs, you've probably used numbers to loop over arrays, represent prices, count things, and much more, but there are a few numbers you might not have run into yet.

First, let's go over how numbers are represented. In JavaScript there are two ways to represent numbers: as integers and as floating point numbers. For example:

![](Image00061.jpg)

INTERACTIVE SESSION:

       var myInt = 3; undefined

       var myFloat = 3.12583E03; undefined

        myInt

3

       myFloat 3125.83

You can write a floating point number using scientific notation, 3.12583E03 (which means that the number after the "E" is the number of times you multiply the number by 10). This is handy when you want to represent very large or very small numbers.

Speaking of which, how do you know the largest or smallest numbers that you can represent? The JavaScript Number object (which we'll talk more about later) has built-in properties for both of these: Number.MAX_VALUE and Number.MIN_VALUE . Try them in your console:

![](Image00060.jpg)

INTERACTIVE SESSION:

        Number.MAX_VALUE

1.7976931348623157e+308

        Number.MIN_VALUE

5e-324

Wow. The MAX_VALUE is pretty large, and the MIN_VALUE is pretty small. You might think that means that

JavaScript can represent a lot of numbers, but the actual number of numbers JavaScript can represent is much smaller than you might think. Why? Because both the MAX_VALUE and MIN_VALUE numbers are represented as floating point numbers and floating point numbers are not always precise. Notice that the largest value has only 17 decimals, which means it is only precise in the first 17 places. Beyond that number of places, it's all zeros, which means you couldn't accurately represent the number

1.7976931348623157000000001e+308, for instance. Floating point numbers are useful in some circumstances when you're working with big numbers and you don't need precision.

When you do need precision, you'll want to use integers, and you'll need to know the largest (and smallest) integer that JavaScript can represent. Let's take a look at the largest integer value in JavaScript, 2 raised to the power of 53:

![](Image00049.jpg)

INTERACTIVE SESSION:

Math.pow(2, 53) 9007199254740992

This is a pretty big number too, but it's a lot smaller than Number.MAX_VALUE. JavaScript can represent all the integer values from zero up to this number precisely . That gives you a lot of numbers to play with and it's unlikely that you'll ever need a larger number than this (this also applies to the smallest integer number, Math.pow(2, -53)).

Understanding how computers represent numbers could be a whole course in and of itself, so we won't go [any deeper into the topic now. If you're interested in exploring this topic further, check out the ECMAScript](http://ecma262-5.com/ELS5_HTML.htm#Section_8.5) [specification (the specification on which JavaScript is based), and the Wikipedia page on binary-coded](http://en.wikipedia.org/wiki/Binary-coded_decimal) [decimal numbers .](http://en.wikipedia.org/wiki/Binary-coded_decimal)

![](Image00065.jpg)

We're assuming you're using a modern browser on a modern computer, and Math.pow(2, 53) is Note based on the ability of JavaScript to represent 64-bit numbers, which modern browsers on

modern computers can do . If, for some reason, you're on an older computer with an older browser, then your maximum number might be based on 32-bit numbers instead.

![](Image00018.jpg)

To Inf inity (But Not Beyond)

You might remember from math class that if you divide by 0, you get infinity. When you begin programming, this can cause problems because if you try to represent infinity in some programming languages, well, let's just say your computer won't be too happy.

JavaScript, however, is more than happy to represent infinity:

![](Image00059.jpg)

INTERACTIVE SESSION:

var zero = 0; undefined

var crazy = 3/zero; undefined

crazy

Infinity

Instead of complaining when you divide by 0, JavaScript just returns the value Inf init y . What is Inf init y at least in JavaScript? (I suppose we may never know in the real world.)

![](Image00049.jpg)

INTERACTIVE SESSION:

typeof crazy "number"

In JavaScript, Inf init y is a number (and so is -Inf init y ). Here's an experiment you can run if you like, but be prepared to close your browser window, because this is an experiment that will never end:

![](Image00066.jpg) OBSERVE:

var counter = 0; undefined

while (counter < crazy) { counter++; console.log(counter);

}

1

2

3

... forever

So although you can represent Inf init y in your programs, that doesn't mean you can ever reach it. You can test for it to prevent mistakes though:

![](Image00067.jpg)

INTERACTIVE SESSION:

if (crazy == Infinity) { console.log("stop!"); } stop!

⋖ undefined

Not a Number

One final interesting number you should know about is NaN , or "Not a Number". Wait, something that means "Not a Number" is a number? Yes! Another oddity in the world of JavaScript. Give it a try:

![](Image00059.jpg)

INTERACTIVE SESSION:

var invalid = parseInt("I'm not a number!"); undefined

invalid

typeof invalid "number"

Here, we attempt to parse the string, "I'm not a number" into an integer. Clearly this will fail because there's nothing in the string, "I'm not a number" that resembles an integer. So what is the result in the variable invalid ? Well, it's NaN , when we check the type of invalid , we see that it is indeed a "number", even though the value is NaN .

You might think that you can test to see if a result is NaN like this:

![](Image00049.jpg)

INTERACTIVE SESSION:

if (invalid == NaN) { console.log("invalid is not a number!"); } undefined

It doesn't work though. Go ahead. Try it now. You won't see the console message "invalid is not a number!"

Instead, to test to see if a variable is not a number, you need to use the built-in function, isNaN() :

![](Image00056.jpg) INTERACTIVE SESSION:

       if (isNaN(invalid)) { console.log("invalid is not a number!"); } invalid is not a number!

⋖ undefined

Be careful with isNaN() though. What do you expect if you write:

![](Image00049.jpg)

INTERACTIVE SESSION:

       isNaN("3") false

You might have expected to see the result true (meaning that the string "3" is not a number), but we get false (meaning that the string "3" is a number) . Why? Because isNaN() attempts to convert its argument to a number before it checks to see if it's not a number. In the case of "3", JavaScript succeeds. Think of this code as doing the equivalent of parseInt ("3") and passing the result, 3, to isNaN() . This behavior is widely considered to be a bug in JavaScript and may be fixed in a future version. In the meantime, just make sure you know how isNaN() works so you can be prepared in case the value you pass to it can be converted to a number.

Objects

We've spent a lot of time in the world of primitives, so let's head on over to the world of objects for a while. At this point, you've probably had quite a bit of experience with objects, but let's do a quick review, to make sure you're set up for some of the more advanced object lessons to come.

Objects are collections of properties. Properties can be primitive values, other objects, or functions (which are called met ho ds when they are inside an object). Let's take a look at an example of an object. We'll go ahead and create a simple HTML file to hold our object (it's easier than typing at the prompt in the console):

![](Image00068.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Objects </title>

<meta charset="utf-8">

<script>

var person = {

name: "James T. Kirk",

birth: 2233,

isEgotistical: true,

ship: {

name: "USS Enterprise",

number: "NCC-1701",

commissioned: 2245

},

getInfo: function() {

return this.name + " commands the " + this.ship.name;

}

};

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save this as o bject s.ht ml in your /AdvJS folder, and then ![](Image00021.jpg) . You won't see anything in the page, so open up the console (and reload the page, just to be sure). Since we defined perso n as a global variable, we can use it in the console:

![](Image00069.jpg) INTERACTIVE SESSION:

person.getInfo()

"James T. Kirk commands the USS Enterprise"

The perso n object contains properties with primitive values and values that are other objects. We say that the perso n.ship object is nested inside the perso n object. You can nest objects within objects within objects and so on, as deep as you'd like to go (although there is a limit to how deep you can go, you're unlikely to hit it in a normal program), but keep in mind that the more nested objects you have, the more inefficient your object becomes. Also note that the most deeply nested object must have properties that are either primitive values or methods (in order for the nesting to stop).

Adding and Deleting Properties

One cool thing about JavaScript objects is that they are dynamic , that is, you can change the properties at any time by changing their values, or even by adding or deleting properties:

![](Image00070.jpg)

INTERACTIVE SESSION:

person.title undefined

person.title = "Captain"; "Captain"

person.title

"Captain"

person

Object {name: "James T. Kirk", birth: 2233, isEgotistical: true, ship: Object, g

etInfo: function}

birth: 2233

getInfo: function () {

isEgotistical: true

name: "James T. Kirk"

ship: Object

title: "Captain"

__proto__: Object

Here, we got the value of a property that doesn't exist in perso n , perso n.t it le . The result is undef ined , which we'd expect. Next, we set the property t it le in person by defining it, and giving it the value "Captain." Now, we can get the value of the property using person.title . When we display the value of perso n in the console (just by typing the name of the object, and pressing Ent er ), we see that t it le has been added t o t he o bject , as if we'd had it there all along. (Note that we inspected the details of the perso n object by clicking on the arrow next to the object in Chrome, which exposes all of the details in the console.)

Now, suppose you want to remove the t it le property:

![](Image00071.jpg)

INTERACTIVE SESSION:

delete person.title true

person.title undefined

person

Object {name: "James T. Kirk", birth: 2233, isEgotistical: true, ship: Object, g

etInfo: function}

birth: 2233

getInfo: function () {

isEgotistical: true

name: "James T. Kirk"

ship: Object

__proto__: Object

delet e removes the entire property , not just the value. The property no longer exists in the object, so when we try to get its value, we get undef ined again. When we inspect the object, we can see that the title property is gone.

Here's a screenshot of this console interaction in Chrome after loading o bject s.ht ml :

![](Image00072.jpg)

What's the Type of an Object?

Are you wondering what the type of an object is? Go ahead and test using t ypeo f in the console:

![](Image00049.jpg)

INTERACTIVE SESSION:

       typeof person "object"

In this case, JavaScript returns the string "object" when we ask for the type of the object perso n . That's good.

Enumerating Object Properties

JavaScript has the capability to examine the properties of an object in the program itself. This is known as t ype int ro spect io n . Let's take a look at an example of that. Modify o bject s.ht ml as shown.

![](Image00073.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Objects </title>

<meta charset="utf-8">

<script>

var person = {

name: "James T. Kirk",

birth: 2233,

isEgotistical: true,

ship: {

name: "USS Enterprise",

number: "NCC-1701",

commissioned: 2245

},

getInfo: function() {

return this.name + " commands the " + this.ship.name;

}

};

for (var prop in person) {

console.log(person[prop]);

}

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) and ![](Image00036.jpg) . You see each property of the object displayed in the console—here's what it looks like in Chrome:

![](Image00074.jpg)

Let's take a closer look at how we did this:

![](Image00033.jpg)

OBSERVE:

for (var prop in person) {

console.log(person[prop]);

}

We used a f o r loop to loop through all the properties in the object, but instead of the traditional f o r loop you might be used to, we used a f o r/in loop (you may have used this in a previous course when accessing keys and values in Local Storage). In the f o r/in statement we declare a variable: pro p . Each time through the loop, pro p gets the property name of the next property in the object perso n . When we go through an object to access each of its properties, we call this enumerating an object's properties.

Then, inside the loop, we display the value of the object's property in the console. We use the bracket no t at io n to access the object's property. You can try this at the console yourself to see how it works:

![](Image00069.jpg) INTERACTIVE SESSION:

       person["name"] "James T. Kirk"

To access an object's property value with bracket notation, you put the name of the property in quotation marks within brackets, next to the name of the object.

This notation is handy because it allows you to the property in advance (look back at the f o r/in property name within the loop).

access the property of an object without knowing the name of loop and see that we're using a variable , pro p , as the

When would you use this? Well, you might want to copy a property from one object to another, but only if the property does exist. You could use bracket no t at io n to check to see if the property exists first. Or perhaps you are loading JSON data from a file using XHR (Ajax), and creating or modifying objects from the data. We'll see a couple of examples later in the course where the capability to enumerate an object's properties will come in handy.

Primitives That Act like Objects

Earlier we said that you can split JavaScript values into two groups: primitives and objects. This suggests that they are completely separate, and they are...for the most part. However, you should know that some primitives—specifically, numbers, strings and booleans— can act like objects sometimes.

Try this:

![](Image00061.jpg)

INTERACTIVE SESSION:

       var s = "I'm a string"; undefined

        s

"I'm a string"

        s.length

12

       s.substring(0, 3); "I'm"

In the first line, we declare and initialize the variable s to be a string, "I'm a string." As you know, a string is a primitive. Yet we ask for the length of the string, s.lengt h , and the first three letters of the string,

s.subst ring(0, 3) , treating the string s as if it were an object. After all, only objects have properties, like lengt h , and methods, like subst ring() , right? So, what's going on?

We have a primitive that's acting like an object! When you try to access properties and methods that act on a primitive, JavaScript converts the primitive to an object, uses a property or calls a method, and then converts it back to a primitive, all behind the scenes. In this example, the string s is changed to a St ring object temporarily so we can use the lengt h property, and then changed back to a primitive. Then, it's converted to a St ring object so we can call the subst ring() method, and then changed back to a primitive again.

The same thing can happen with numbers and booleans:

![](Image00075.jpg) INTERACTIVE SESSION:

       var num = 32; undefined

        num

32

        num.toString()

"32"

       var b = true; undefined

       b.toString()

"true"

In practice, there are not many times you'll need your numbers and booleans to act like objects, except when you convert them to strings, which happens whenever you use co nso le .lo g() like this:

![](Image00067.jpg)

INTERACTIVE SESSION:

       console.log("My num is " + num); My num is 32

⋖ undefined

Here, num is changed temporarily to a Number object, its t o St ring() method is called, the result is concatenated with "My num is," and the result is displayed in the console (and num is converted back to a primitive). All of that happens behind the scenes so you don't have to worry about it.

Similar to built-in object types like Array and Dat e and Mat h , JavaScript has the built-in object types Number , St ring and Bo o lean . You'll rarely use these though, and you should never do this when you need just a simple primitive value, like 3:

![](Image00060.jpg)

INTERACTIVE SESSION:

       var num = new Number(3); undefined

        num

Number {}

Why? Because JavaScript will always convert a primitive, like 3, to an object when it needs to, without you having to worry about it. So, primitives are converted to objects behind the scenes sometimes, but you'll probably never need to use those objects directly yourself.

JavaScript is Dynamically Typed

If you've had exposure to other languages, you might have run across languages in which you must declare t he t ype of a variable when you create a new variable, like this:

![](Image00043.jpg)

OBSERVE:

int x = 3;

String myString = "test";

In these languages, once you declare a variable to be a certain type, that variable must always be that type. If you try to put a value of a different type into the variable, you'll get an error. For instance, you can't do something like this:

![](Image00076.jpg)

OBSERVE:

x = myString;

Here, we tried to set the variable x to a string, but we can't because x is declared to be an int (an integer number). This line of code will cause an error.

These languages are known as "statically typed" languages. "Static" because the types of variables can't change.

Contrast this with JavaScript, which is a dynamically typed language . In JavaScript, you declare variables with no type, and you can change the types of the values in those variables at any time you want:

![](Image00061.jpg)

INTERACTIVE SESSION:

       var x = 3; undefined

       var myString = "test"; undefined

        x = myString;

"test"

       x "test"

So x starts out as a number, and ends up as a string. JavaScript has no problem with this.

You can change the type of a variable, but that doesn't mean you should . Why? Well, if you change the type of a variable in the middle of your program, you might forget you did and expect the variable to contain one kind of value, when in fact it might contain a different kind of value, which could cause bugs in your code.

Sometimes you'll take advantage of the fact that variables can contain any type; but most of the time, it's best to stick with one type for a given variable throughout your program.

In this lesson, you learned about primitives and objects that you might not have encountered before when programming in JavaScript. Understanding the types in JavaScript more deeply is important as you progress to more advanced programming. For instance, you might need to know whether to expect null or undefined if you're checking to see if a method succeeds or fails in creating a new object, or when to check to see if the result of a method is NuN if the user submits the wrong kind of data in a form.

Practice your new skills with the quizzes and projects before moving on to the next lesson, where we'll continue to explore primitives and objects and how they behave when you start comparing them.

Truthy, Falsey, and Equality

![](Image00005.jpg)

Lesson Objectives

When you complete this lesson, you will be able to:

test for null and undefined.

![](Image00006.jpg)

test values for truthiness.

![](Image00006.jpg)

compare values using the strict equality operator.

![](Image00006.jpg)

examine and compare the property names and the property values of objects.

![](Image00006.jpg)

design appropriate conditional tests when using equality operators and typecasting.

![](Image00006.jpg)

explore equality of objects.

![](Image00005.jpg) ![](Image00006.jpg)

You might think that testing for the equality of two values is simple and straightforward. Well actually, sometimes it is, and sometimes it's not. In JavaScript, when we compare two values, we get a result: true or false. However, determining the result of a comparison is not always as straightforward as you might think, because along with true and false, we also have truthy and falsey values . In addition, testing equality for primitives is different from testing equality for objects. In this lesson, you'll learn what's really happening behind the scenes when you compare values.

For the examples in this lesson, you're welcome to create an HTML file with a <script> or use the console. Either is fine. We'll show examples of both.

Truthy, Falsey, and Equality

In JavaScript, we compare values all the time. For instance, you might do this:

![](Image00077.jpg)

OBSERVE:

var weather = "sunny";

if ( weather == "sunny" ) {

console.log("It's sunny today!");

} else {

console.log("It must be rainy.");

}

We compare a string value with another string value using a conditional expression , weat her == "sunny" , to see if they are equal, and the result of that conditional expression is either t rue or f alse (in this case, it's t rue ). In an if statement, we use conditional expressions to determine whether to execute a block of code. If the expression in the parentheses results in t rue , the first block of code is executed; if it's not, the else block is executed (if there is one—if there isn't, execution just continues with the next line of code after the if statement).

We can do the same thing with values that are directly true or false like this:

![](Image00077.jpg)

OBSERVE:

var isItSunny = true;

if (isItSunny) {

console.log("It's sunny today!");

} else {

console.log("It must be rainy.");

}

Notice that here, we don't have to compare isIt Sunny to true , because we know that isIt Sunny is a boolean value.

This means we can shorten the expression to isIt Sunny .

In many cases, we're working with expressions that are true or false, but sometimes we work with values that are truthy or falsey . What does this mean? It means that some values aren't directly true or false, but are interpreted by JavaScript to mean true or false in certain situations, like conditional expressions . Here's an example (before you try these in the console yourself, see if you can guess what you'll see as the result of each statement):

![](Image00078.jpg) OBSERVE:

if (1 == 1) { console.log("1 really does equal 1"); } if (1) { console.log("1 is true"); }

Go ahead and try these statements in the console (remember that you might have to load an HTML page to access the console):

![](Image00079.jpg)

INTERACTIVE SESSION:

  if (1 == 1) { console.log("1 really does equal 1"); }

1 really does equal 1 ⋖ undefined

  if (1) { console.log("1 is true"); }

1 is true

  undefined

The first statement is straightforward; we compare the value 1 with the value 1, so of course we expect them to be equal, and expect to see the console log message, "1 really does equal 1."

So what about the second statement? There, we test the value 1 to see if it's true or false, but 1 isn't either true or false, it's 1, right? Yet the result of this statement is that we do see the console log message "1 is true," which means that JavaScript must think that 1 is true. Hmmm. That's perplexing.

What about this next example; what do you think you'll get?

![](Image00080.jpg)

OBSERVE:

if (0) { console.log("0 is true!"); }

Try it. This time we don't see the console log message, which means JavaScript must think that 0 is false:

![](Image00081.jpg)

INTERACTIVE SESSION:

  if (0) { console.log("0 is true!"); } undefined

Try one more experiment:

![](Image00008.jpg)

INTERACTIVE SESSION:

  if (-5) { console.log("-5 is true!"); } -5 is true!

⋖ undefined

That'snteresting. JavaScript thinks that -5 is true!

So it turns out that numbers other than 0 are truthy , and 0 is falsey . We use those terms to indicate that even though -5 isn't true, it results in true in a conditional expression. Same with 0; even though 0 isn't false, it results in false in a conditional expression.

Experiment a bit on your own. For instance, is NaN truthy or falsey? What about Inf init y ?

Values That are Truthy or Falsey

We need to find out which other values are truthy and falsey in JavaScript. Let's do some testing in the console to see how JavaScript treats values in truthy and falsey situations. We'll begin with undefined . Before you look at the example below, do you think undefined is truthy or falsey?

![](Image00082.jpg) INTERACTIVE SESSION:

var myValue; undefined

if (myValue) { console.log("undefined is truthy!"); } undefined

if (!myValue) { console.log("undefined is falsey!"); } undefined is falsey!

⋖ undefined

Remember that ! means NOT, so if myValue is false, then !myValue is true. So, undef ined is falsey, because in the second expression, myValue resolves to f alse , and then we say "NOT false" with !myValue , which results in t rue , so we execute the if statement block to display the message "undefined is falsey!". Is that what you expected; that is, that undef ined is falsey? Here's how this session looks in the Chrome console:

![](Image00083.jpg)

What about null ? Can you guess?

![](Image00084.jpg)

INTERACTIVE SESSION:

myValue = null; null

if (myValue) { console.log("null is truthy!"); } undefined

if (!myValue) { console.log("null is falsey!"); } null is falsey!

⋖ undefined

So, null is also falsey. It kind of makes sense that if undef ined is falsey, then null would also be falsey, right?

Okay, we've looked at numbers, undefined and null. What about strings?:

![](Image00084.jpg)

INTERACTIVE SESSION:

var myString = "a string"; undefined

if (myString) { console.log("myString is truthy!"); } myString is truthy!

⋖ undefined

if (!myString) { console.log("myString is falsey!"); } undefined

In this case, we see the string "myString is true" which means that mySt ring is truthy. How about if we set mySt ring to the empty string, "". Now do you think mySt ring will be truthy or falsey?

![](Image00082.jpg) INTERACTIVE SESSION:

myString = "";

""

if (myString) { console.log("myString is truthy!"); } undefined

if (!myString) { console.log("myString is falsey!"); } myString is falsey!

⋖ undefined

So a string with characters is truthy, but an empty string is falsey. Experiment a bit. What if mySt ring is a string with one space in it, like this: " "?

Shortcuts using truthy and f alsey results

Knowing that undef ined , null , and "" are all falsey values, can you think of a good way to shorten the code below?

![](Image00041.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Truthy, Falsey, Equality </title>

<meta charset="utf-8">

<script>

var myString = prompt("Enter a string");;

if (myString == null || myString == undefined || myString == "") { console.log("Please enter a non-empty string!");

} else {

console.log("Thanks for entering the string '" + myString + "'");

}

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as stringTest .ht ml , and ![](Image00085.jpg) . Open the console (you might need to reload the page to see the output in the console). Enter a string and note the message you see. Try entering different values at the prompt, like null (just click OK ), "", and "test", for instance.

Now that you know about truthy and falsey values, you can shorten this code:

![](Image00086.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Truthy, Falsey, Equality </title>

<meta charset="utf-8">

<script>

var myString = prompt("Enter a string");;

if ( myString == null || myString == undefined || myString == "" !myStrin

g ) {

console.log("Please enter a non-empty string!"); } else {

console.log("Thanks for entering the string '" + myString + "'");

}

</script>

</head>

<body>

</body>

</html>

![](Image00087.jpg) and ![](Image00036.jpg) again (or reload if you still have the page open). You get the same behavior as before, but with a much shorter conditional expression. Again, try entering a few different values to make sure this works as you expect. Try replacing the prompt for mySt ring to undef ined , null , the empty string, or something else.

In cases where you need to test to make sure that a variable has a truthy value, but you don't care what that value is exactly, you can use this type of shortcut to save yourself some typing.

Be careful though. In cases where you need to test for a specific value, you also need to understand implied typecasting . We'll talk about next.

Implied Typecasting

Does 88 equal "88?" That's an interesting question. Let's see:

![](Image00088.jpg)

INTERACTIVE SESSION:

       var myNum = 88; undefined

       var myString = "88"; undefined

        if (myNum == myString) {

console.log("My number is equal to my string!");

}

My number is equal to my string!

        undefined

JavaScript converts the string "88" into a number before doing the comparison between myNum and myString, so the comparison actually happens between 88 and 88 . Of course those values are equal, so the result is true, and we see the console log message, "My number is equal to my string!"

This process of converting a string to number before doing a comparison or another operation is called "implied typecasting" (also known as type coercion or type conversion). JavaScript does implied typecasting as needed. For instance, whenever you do something like this:

![](Image00089.jpg) INTERACTIVE SESSION:

var age = 29; undefined

var output = "My age is " + age; undefined

output

"My age is 29"

Here you are using JavaScript's ability to convert the variable age from a number to a string automatically, so it can be concatenated with the string "My age is."

When converting strings and numbers, be careful because the result may not always be what you expect. You know that sometimes JavaScript converts a string to a number, like when we compare 88 and "88," and you know that sometimes JavaScript converts a number to a string, like when you want to concatenate a number to a string. So what do you think the result will be when we try to add a string that contains a number to a number?

![](Image00059.jpg)

INTERACTIVE SESSION:

var x = 4; undefined

x = x + "4"; "44"

x

"44"

You might've expected to get 8 .

Let's try another experiment:

![](Image00070.jpg)

INTERACTIVE SESSION:

var myString = "test"; undefined

if (myString) {

console.log("'test' is truthy");

} else {

console.log("'test' is falsey");

}

'test' is truthy

undefined

if (myString == true) { console.log("'test' is true");

} else {

console.log("'test' is false");

}

'test' is false

undefined

Notice that in the first if statement, if (myString) ... , we rely on the truthy-ness or falsey-ness of myString to result in true or false to determine the flow of execution. However, in the second if statement, if

(mySt ring == true) ... , we compare the value of myString with the boolean true , explicitly. JavaScript doesn't do implied typecasting and conversion of myString to true or false here.

As you can probably tell, it's a bit tricky to know for sure in every case exactly how JavaScript will (or won't) typecast and convert a value for comparison. One way that you can be more confident that you'll get the result you expect is to use the strict equality operator === , in place of the equalityoperator == .

For more information about how JavaScript performs type conversions, see the [ECMAScript specification](http://www.ecma-international.org/ecma-262/5.1/#sec-9) .

Testing Equality

JavaScript has two operators for testing equality, == and === . You've probably been using == in your JavaScript programming, but consider using === instead (at least sometimes). Let's take a closer look at the difference between these two operators, and why you might use one over the other.

We'll begin by looking at an example of these two operators in action:

![](Image00060.jpg)

INTERACTIVE SESSION:

       null == undefined true

       null === undefined false

The equality operator, == , attempts to do implied typecasting before it compares two values. So, in the first expression above, JavaScript sees that you're trying to compare values of two different types, and so, tries to convert one type to the other in order to do the comparison. In this case, JavaScript could either convert undef ined to null , or null to undef ined (JavaScript can do it either way), and then the two values are equal.

However, the strict equality operator, === , does not do implied typecasting. Instead, it compares the two values as they are. If the types of the two operands are different, then the result is false immediately. Let's see what happens when we use st rict equalit y on our previous comparison of 88 with "88":

![](Image00090.jpg)

INTERACTIVE SESSION:

       var myNum = 88; undefined

       var myString = "88"; undefined

        if (myNum === myString) {

console.log("My number is equal to my string!"); } else {

console.log("A number shouldn't really be equal to a string!");

}

A number shouldn't really be equal to a string!

        undefined

Let's try st rict equalit y on a falsey value, like 0:

![](Image00091.jpg)

INTERACTIVE SESSION:

       var zero = 0; undefined

        if (zero == false) {

console.log("zero is a falsey value!");

}

zero is a falsey value!

        undefined

        if (zero === false) {

console.log("zero is a falsey value!");

} else {

console.log("Now we don't convert zero to false");

}

Now we don't convert zero to false

        undefined

So, strict equality prevents conversion of a falsey value, like 0, to false.

Just like the == equality operator has a negative version, != (meaning not equal to ), the strict equality operator

also has a negative version, !== . The only difference between != and !== is that != attempts to typecast its operands to the same type, while !== does not.

Do some experimenting with the four operators: == , != , === and !== . You might be surprised by what you find.

Some programmers always use strict equality (and strict inequality) rather than equality (and inequality). However, sometimes you might want to take advantage of JavaScript's ability to do typecasting. If you do, be cautious and make sure you know exactly how that typecasting is going to work on the types of values you expect.

You can get all the gory details of the algorithms used by the equality operator and the strict equality operator (also known as the identity operator ) in the [ECMAScript specification](http://www.ecma-international.org/ecma-262/5.1/#sec-11.9) .

Objects and Truthy-ness

So far, we've been looking at the truthy-ness and falsey-ness of primitive values like numbers, strings, null and undefined. What about objects?

![](Image00088.jpg)

INTERACTIVE SESSION:

       var o = { name: "object" }; undefined

        o

Object {name: "object"}

        if (o) {

console.log("This object is truthy!");

}

This object is truthy!

        undefined

So it looks like objects are truthy. What about empty objects? (Remember that empty strings are falsey, so you might expect that empty objects are also falsey.)

![](Image00088.jpg)

INTERACTIVE SESSION:

       var p = {}; undefined

        if (p) {

console.log("This object is truthy!");

} else {

console.log("This object is falsey!");

}

This object is truthy!

        undefined

Interesting. Even a completely empty object, like p , is still truthy. But...

![](Image00060.jpg)

INTERACTIVE SESSION:

       p == true false

       p == false false

Even though p might be truthy, it's not equal to true (or false) using the equality operator, so no type conversion is happening here.

Objects and Equality

Let's do a few more tests in the console and compare our empty object, p , to some other values:

![](Image00092.jpg) INTERACTIVE SESSION:

var p = {}; undefined

p == 0 false

p == null false

p == undefined false

p == "{}" false

p == {}

false

In this example, we use the equality operator, == , because we want JavaScript to try to typecast the values for comparison. As you can see, all of the results are false, which means that even if JavaScript is able to typecast, the comparison is still false.

Most of these results are probably expected, but that last one sure isn't! We know that p is an empty object, {

} , so why isn't p equal to another empty object? Aren't they the same thing? Go ahead and create a file with two objects so we can experiment:

![](Image00093.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Comparing objects </title>

<meta charset="utf-8">

<script>

var book1 = {

title: "Harry Potter",

author: "JK Rowling",

published: 1999,

hasMovie: true

};

var book2 = {

title: "Harry Potter",

author: "JK Rowling",

published: 1999,

hasMovie: true

};

if (book1 == book2) {

console.log("The two books are the same"); } else {

console.log("The two books are different");

}

</script>

</head>

<body>

</body>

</html>

Here, we create two book objects using object literals, and then test to see if the books are equal.

![](Image00042.jpg) Save this in your /AdvJS folder as o bject sT est .ht ml , and ![](Image00021.jpg) . In the console, you see the message, "The two books are different."

The two books, bo o k1 and bo o k2 , are exactly the same: they have the same properties. All the property names are the same, the property values are the same, and the number of properties is the same. So why aren't they equal? (Note that we're using the equality operator here to test equality; we know the types of the

two objects are the same, so we don't have to worry about any typecasting happening).

The two objects are not equal because of an important difference in how primitive values are stored and how objects are stored in the computer's memory. When you create a primitive value, let's say:

![](Image00076.jpg)

OBSERVE:

var x = 3;

the computer allocates a bit of memory, gives it the name "x", and saves the value 3 in that bit of memory:

![](Image00094.jpg)

Now, compare that to what happens when you create an object, let's say bo o k1 from the example above:

![](Image00095.jpg)

OBSERVE:

var book1 = {

title: "Harry Potter",

author: "JK Rowling",

published: 1999,

hasMovie: true

};

In this case, the computer names and allocates some memory for each of the properties in the object, and then allocates a separate bit of memory for the variable name, and in that memory stores a value that points to the place in memory where the object is actually stored. This is called an o bject ref erence . So the variable bo o k1 doesn't contain the object itself; it actually contains a reference to the object. Like this:

![](Image00096.jpg)

In this case, the object value (that is, all the properties in the object, plus a few other things about the object) is stored at memory location 495823 (I just made that up for this example, but you get the idea), and the variable bo o k1 contains that location (in the same way that x contains 3).

Now let's see what happens when we create the second book object, bo o k2 :

![](Image00095.jpg)

OBSERVE:

var book2 = {

title: "Harry Potter",

author: "JK Rowling",

published: 1999,

hasMovie: true

};

Even though the properties are exactly the same, a completely separate book object is created and stored in a completely different part of memory:

![](Image00097.jpg)

The variable bo o k2 contains the memory location of this second object, and the memory location is different from the memory location for bo o k1 .

So when we compare bo o k1 and bo o k2 :

![](Image00098.jpg)

OBSERVE:

if (book1 == book2) {

console.log("The two books are the same"); } else {

console.log("The two books are different");

}

the values that are compared are the memory locations of the two objects. They are not equal, so we see the message "The two books are different."

![](Image00099.jpg)

Compare this to what happens when we compare primitive values:

![](Image00084.jpg)

INTERACTIVE SESSION:

var x = 3; undefined

var y = 3; undefined

if (x == y) { console.log("x and y are the same"); } x and y are the same

⋖ undefined

![](Image00100.jpg)

In the example above where we compared two book objects, we used lit eral objects for the books. Do you think the the result would be the same when if we used an object constructor? Let's see:

![](Image00068.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Comparing objects, take two </title> <meta charset="utf-8"> <script>

function Book(title, author, published, hasMovie) { this.title = title;

this.author = author;

this.published = published;

this.hasMovie = hasMovie;

}

var book1 = new Book("Harry Potter", "JK Rowling", 1999, true); var book2 = new Book("Harry Potter", "JK Rowling", 1999, true); if (book1 == book2) {

console.log("book1 is equal to book2");

} else {

console.log("book1 is NOT equal to book2");

}

</script>

</head>

<body>

</body>

</html>

Now we use a constructor function, Book() , to create two books, and then test to see if they are equal. ![](Image00042.jpg)

Save this in your /AdvJS folder as objects Test2.ht ml , and ![](Image00036.jpg) . In the console, you see the message, "book1 is NOT equal to book2."

The result is the same because we are creating two completely different book objects, even though they use the same constructor and have the same properties.

Okay, so knowing what you know about how objects are stored in memory, what do you think happens when we change the program like this?:

![](Image00101.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Comparing objects, take two </title> <meta charset="utf-8"> <script>

function Book(title, author, published, hasMovie) { this.title = title;

this.author = author;

this.published = published;

this.hasMovie = hasMovie;

}

var book1 = new Book("Harry Potter", "JK Rowling", 1999, true); var book2 = new Book("Harry Potter", "JK Rowling", 1999, true); var book2 = book1;

if (book1 == book2) {

console.log("book1 is equal to book2");

} else {

console.log("book1 is NOT equal to book2");

}

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) and ![](Image00021.jpg) . In the console, you see the message "book1 is equal to book2." Why? Because when we assign the value of book1 to book2 (var book2 = book1), we store the memory location of the data in book1 into book2 , like this:

![](Image00102.jpg)

So now, when we compare the values of book1 and book2, they are the same: they are both values that point to the same memory location.

Let's update the program one more time:

![](Image00103.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Comparing objects, take two </title>

<meta charset="utf-8">

<script>

function Book(title, author, published, hasMovie) { this.title = title;

this.author = author;

this.published = published;

this.hasMovie = hasMovie;

}

var book1 = new Book("Harry Potter", "JK Rowling", 1999, true);

var book2 = book1;

if (book1 == book2) {

console.log("book1 is equal to book2");

} else {

console.log("book1 is NOT equal to book2");

}

book1.star = "Harry";

console.log(book1);

console.log(book2);

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) and ![](Image00021.jpg) . Take a look at the two book objects that we display in the console. Notice anything interesting?

![](Image00104.jpg)

OBSERVE:

Book {title: "Harry Potter", author: "JK Rowling", published: 1999, movie: true,

star: "Harry" }

Book {title: "Harry Potter", author: "JK Rowling", published: 1999, movie: true,

star: "Harry" }

In the code we added a new property, star to book1 , and set its value to "Harry." Yet when you look at the two objects in the console, you can see that both book1 and book2 now have the property st ar , with the value "Harry" . How did this happen!?

Well, remember that book2 points to the same location in memory that book1 does. So if we change the data in book1 , we're also changing the data in book2 because they are the same object.

What do you think would happen if we changed the title of book2 ? Try changing the title of book2 to "Harry Potter and the Sorcerer's Stone." What do you see when you display book1 and book2 ?

Now, you might be asking, "If I can't compare two different objects using the equality operator to see if they are the same (that is, that they have the same properties and values), how do I know if two objects are the same?"

The answer is that you have to look at each property of an object separately. This isn't too hard to do if the properties in an object are all primitive values (numbers, strings, booleans). However, if your objects have nested objects and/or methods, then it gets a bit trickier because then the solution depends on what you mean by "equality" in the case of two objects. What do you think it means for one object to be "equal" to an other? A good topic for you to think about.

Various JavaScript libraries have tackled this question by implementing functions that check equality of objects. Be cautious though because different libraries may have different ideas about what equality of objects means. Make sure the library function works as you expect. For example, you can use the [Underscore.js](http://underscorejs.org/#isEqual) library's isEqual() function to test the equality of objects.

We covered a lot of ground in this lesson, including truthy and falsey values, implied typecasting and what can happen when you compare two values, two different kinds of equality operators, and the difference in comparing primitive values and object

values. Whew! That's lots of detail, some of which you may not have encountered before, but that you'll need to know as you get into more advanced JavaScript programming.

Take a break to rest your brain, and then tackle the quizzes and projects to help it all sink in before you move on to the next lesson.

Constructing Objects

![](Image00005.jpg)

Lesson Objectives

When you complete this lesson, you will be able to:

construct objects with your own constructors, and new .

![](Image00006.jpg)

construct object literals.

![](Image00006.jpg)

construct empty objects and add new properties.

![](Image00006.jpg)

compare how a function works as a function, and as a constructor.

![](Image00006.jpg)

initialize an object's property values in a constructor.

![](Image00006.jpg)

use the conditional operator.

![](Image00006.jpg)

explore the value of this when an object is created.

![](Image00006.jpg)

construct arrays in two ways.

![](Image00005.jpg) ![](Image00006.jpg)

Just about everything in JavaScript is an object, so understanding objects is key to understanding and programming JavaScript.

In this lesson, we'll delve into how we create objects in JavaScript.

Constructing JavaScript Objects

When you construct an object in JavaScript, you are creating a dynamic collection of property names and values. You've already seen a couple of different ways to create objects, using a constructor function (like the Bo o k() function we used in the previous lesson), and using object literals.

Let's take a closer look at three ways you can construct objects and how they are similar to and different from each other.

Constructing an Object with a Constructor Function

The first way to contruct objects that we'll check out uses the a constructor function. In the previous lesson, we used a constructor function, Book() , to create book objects, passing in arguments for title, author, the date the book was published, and whether it had been made into a movie. We'll use that same object here, except we'll add a new method, display() , to the object:

![](Image00068.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Constructing objects </title>

<meta charset="utf-8">

<script>

function Book(title, author, published, hasMovie) { this.title = title;

this.author = author;

this.published = published;

this.hasMovie = hasMovie;

this.display = function() {

console.log(this);

};

}

var book1 = new Book("The Hound of the Baskervilles", "Sir Arthur Conan Doyl e", 1901, true);

book1.display();

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as object Const r.ht ml , and ![](Image00036.jpg) . Open the console (and reload the page if you need to), and you see that the constructor function created a book object:

![](Image00105.jpg)

(This screenshot is in the Chrome console, but it should look similar in IE, Firefox, and Safari).

A constructor function is just like any other function, but we call a constructor function differently from other functions: we use the word new .

![](Image00043.jpg)

OBSERVE:

var book1 = new Book("The Hound of the Baskervilles", "Sir Arthur Conan Doyle", 1901, true);

The word new makes all the difference. The new keyword indicates that we are using a function to construct an object, rather than just execute code (although a constructor function can do that too). Within the constructor function, we refer to the object that is being created as t his :

![](Image00106.jpg)

OBSERVE:

function Book(title, author, published, hasMovie) { this .title = title;

this .author = author;

this .published = published;

this .hasMovie = hasMovie;

this .display = function() {

console.log( this );

};

}

When you call a function with new , inside that function, a new, empty object is created and the t his keyword is set to that object. (Inside the function, t his acts just like a local variable, except that you can't set its value yourself; that's done for you automatically). Then you use t his to set the values of any properties you want in that object. At the end of the function, you don't have to explicitly return the object you're creating; JavaScript does that for you automatically because you used the new keyword when you called the function. The object that is returned is t his : the new object that was created when you called the function, that has the properties you set in the function.

Of course any function could return an object if you wanted it to:

![](Image00059.jpg)

INTERACTIVE SESSION:

function makeObj() { return { x: 1 }; } undefined

var myObj = makeObj();

undefined

myObj Object {x: 1}

However, in this example, makeObj() is not a constructor function because we didn't call it with new . Instead we called the function normally, and inside the function, created an object literal on the fly, and returned it to the caller of the function makeObj() . These two ways of creating functions might seem similar, but there are a

few key differences . The value of t his inside makeObj() is not set to the object that's being created, and if you don't explicitly return an object from makeObj() , the default return value is undef ined .

These differences in how functions behave, depending on whether you call them with new or not, is one reason why we always (as a convention) use an uppercase letter to begin the name of a constructor function (like Bo o k() ), but use a lowercase letter to begin the name of a regular function (like makeObj() ). That way, you can tell at a glance at your code whether a function is designed to be a constructor function.

There's one other thing that happens when you create an object by calling a constructor function with new that doesn't happen when you create objects in other ways. Look back at the object we created by calling makeObj() :

![](Image00107.jpg)

Now compare that to what you saw in the console earlier for the bo o k1 object (if you still have the page loaded, you can just type bo o k1 in the console to see it again, but make sure you do this in either the Chrome or Safari console specifically):

![](Image00108.jpg)

When you display myObj in the console, you see the word Object next to the object:

![](Image00076.jpg)

OBSERVE:

Object {x: 1}

But you see the word "Bo o k" next to the bo o k1 object:

![](Image00043.jpg)

OBSERVE:

Book {title: "The Hound of the Baskervilles", author: "Sir Arthur Conan Doyle",

published: 1901, hasMovie: true, display: function}

In the Book example, we created the bo o k1 object with the Bo o k() constructor function. When you create an object with a constructor function, JavaScript keeps track of that function in a property called co nst ruct o r . co nst ruct o r is a property of the object, in this case bo o k1 , that results from calling the constructor function, Bo o k() . Now, JavaScript also sets the co nst ruct o r property for objects not created with a constructor function, like the literal object we created and returned from the makeObj() function, but in this case, the

co nst ruct o r property is set to Object () .

You can access the constructor for an object:

![](Image00109.jpg) INTERACTIVE SESSION:

        myObj.constructor

function Object() { [native code] }

        book1.constructor

function Book(title, author, published, hasMovie) { this.title = title;

this.author = author;

this.published = published;

this.hasMovie = hasMovie;

this.display = function() {

console.log(this);

};

}

You can think of the constructor function of an object, whether it's Bo o k() or Object () , as determining the type of the object. This isn't strictly true like it is in statically typed languages like Java, but it can be a handy way to describe objects. We'll return to this idea in a later lesson when we talk about the inst anceo f operator.

For now, the key takeaway for you is to understand how constructing an object using a constructor function with the new keyword is different from other ways that we create objects.

Constructing an Object Using a Literal

You just saw an example of creating a literal object and returning it from a function. Let's create another literal object, another book, so we can compare the result directly with the bo o k1 object we created using a constructor function. Modify o bject Co nst r.ht ml as shown:

![](Image00110.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Constructing objects </title>

<meta charset="utf-8">

<script>

function Book(title, author, published, hasMovie) { this.title = title;

this.author = author;

this.published = published;

this.hasMovie = hasMovie;

this.display = function() {

console.log(this);

};

}

var book1 = new Book("The Hound of the Baskervilles", "Sir Arthur Conan Doyl e", 1901, true);

book1.display();

var book2 = {

title: "The Adventures of Sherlock Holmes",

author: "Sir Arthur Conan Doyle",

published: 1892,

movie: true,

display: function() {

console.log(this);

}

};

book2.display();

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) and ![](Image00036.jpg) . Open the console, and compare bo o k1 and bo o k2 (using Chrome or Safari):

![](Image00111.jpg)

These two objects are similar: both have the same property names, both have a display() method, and the types of all the property values are the same. However, if you look at the constructors for bo o k1 and bo o k2 , you'll see (just like in myObj earlier), that the constructor for bo o k1 is Bo o k() , because we created it using a constructor function, but the constructor for bo o k2 is Object () because we created it using an object literal:

![](Image00109.jpg) INTERACTIVE SESSION:

        book1.constructor

function Book(title, author, published, hasMovie) { this.title = title;

this.author = author;

this.published = published;

this.hasMovie = hasMovie;

this.display = function() {

console.log(this);

};

}

        book2.constructor

function Object() { [native code] }

The [nat ive co de] means that the implementation of the Object () constructor is hidden because it's internal to the browser.

The property in the objects called __pro t o __ is the last property in both the bo o k1 and bo o k2 objects:

![](Image00111.jpg)

The value of __ pro t o __ for bo o k1 is Bo o k , and the value of __pro t o __ for bo o k2 is Object . You might be thinking that the __pro t o __ property must be related to the constructor function for an object, and you'd be right (although they are not the same thing).

You also might notice that the co nst ruct o r property is not listed in the bo o k1 and bo o k2 objects' properties. That's because this property is inherited from the object's pro t o t ype . (As you might guess, the __pro t o __ property is also related to the prototype). We'll talk more about prototypes in a later lesson.

What about t his in a literal object? You already know that you can use t his in a method of an object to refer to "this object," but unlike in a constructor function, we don't (and can't) use t his to initialize object properties. Instead, we create properties and initialize them by specifying the name/value pairs in an object, by literally typing them. (That's why it's called an object literal) . The only time t his refers to the object is when you call one of its methods. (How t his gets set and what it gets set to is yet another topic we'll come back to in more depth later).

Constructing an Object Using a Generic Object Constructor

Another way to create an object literal is to start with an empty object, and then add properties to it. You can create an empty, generic object in one of two ways:

![](Image00043.jpg)

OBSERVE:

var obj1 = { };

var obj2 = new Object();

Both of these approaches to create an object do the same thing. You'll see an empty object created the first way more often (because it's a little easier to write), but it's instructive to understand the second way as well. When you create an object with new Object () , it's just like when you create an object with new Bo o k() , except that Object () is a built-in constructor function that you don't have to write yourself. You don't pass any arguments to Object () to initialize object properties in the constructor function, instead, you add them all after the object is created. Modify o bject Co nst r.ht ml as shown:

![](Image00112.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Constructing objects </title>

<meta charset="utf-8">

<script>

function Book(title, author, published, hasMovie) { this.title = title;

this.author = author;

this.published = published;

this.hasMovie = hasMovie;

this.display = function() {

console.log(this);

};

}

var book1 = new Book("The Hound of the Baskervilles", "Sir Arthur Conan Doyl e", 1901, true);

book1.display();

var book2 = {

title: "The Adventures of Sherlock Holmes",

author: "Sir Arthur Conan Doyle",

published: 1892,

movie: true,

display: function() {

console.log(this);

}

};

book2.display();

var book3 = new Object(); // same as var book3 = { }; book3.title = "A Study in Scarlet"; book3.author = "Sir Arthur Conan Doyle";

book3.published = 1887;

book3.movie = false;

book3.display = function() {

console.log(this);

};

book3.display();

</script>

</head>

<body>

</body>

</html>

We added the exact same properties that we added to bo o k1 and bo o k2 , only with some different values, because it's a different book. bo o k3 also has a display() method, just like bo o k1 and bo o k2 .

![](Image00042.jpg) and ![](Image00021.jpg) . In the console, compare bo o k3 with bo o k2 and bo o k1 .

![](Image00113.jpg)

bo o k3 looks similar to bo o k2 , because bo o k3 is also an object literal; it was just created in a slightly different way. Notice that the constructor for bo o k3 is also Object () , which you can test in the browser console:

![](Image00049.jpg)

INTERACTIVE SESSION:

        book3.constructor

function Object() { [native code] }

So, What's the Best Way to Make an Object?

You've seen three different ways to construct an object (you'll see a fourth in a later lesson), but which is the best way?

That depends on the situation. If all you need is a quick, one-off object, then creating an object literal like we did with bo o k2 or bo o k3 is probably good enough. However, if you know that you're going to need multiple book objects, writing a constructor function like Bo o k() , that you can use to make many book objects is a better choice. You'll also want to consider whether the objects you're creating are, say, Bo o ks or Magazines . As you've seen, objects created with a constructor function have that extra information about how they were created, which can be useful. We'll see an example of that in a later lesson, when we talk about prototypes.

Initializing Values in Constructors

Let's go back to constructor functions now and look at ways you can initialize the properties of the object you're constructing with the function. We'll use a different example, so open a new file:

![](Image00114.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Initializing objects </title>

<meta charset="utf-8">

<script>

function Point(x, y) {

if (x == undefined || x == null) {

this.x = 50;

} else { this.x = x;

}

if (y == undefined || y == null) {

this.y = 50;

} else { this.y = y;

}

           Make a toString() method we can use to display the point this.toString = function() {

return "[" + this.x + ", " + this.y + "]";

}

}

           Can have code in constructors too var p = new Point();

console.log("My point is: " + p.toString());

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save it in your /AdvJS folder as po int .ht ml , and ![](Image00021.jpg) . Open the console (and reload the page if you need to); the Point object, p , is displayed like this:

![](Image00076.jpg)

OBSERVE:

My point is: [50, 50]

In this code, we've got a Po int () constructor function to create Point objects. Let's discuss the code:

![](Image00115.jpg) OBSERVE:

function Point( x, y ) {

if (x == undefined || x == null) {

this.x = 50;

} else { this.x = x;

}

if (y == undefined || y == null) {

this.y = 50;

} else { this.y = y;

}

           toString(): display the point this.toString = function() {

return "[" + this.x + ", " + this.y + "]";

}

}

var p = new Point();

console.log("My point is: " + p.toString());

We use a co nst ruct o r f unct io n, Po int () to property of the object p , you'll see the Po int ()

create a Point object, p . So, if you look at the constructor function.

Po int () actually expects two arguments, x and y , which are the coordinates of the point, but we call Po int () with no arguments. It turns out that JavaScript is totally okay with this, but unless we do something further, the x and y coordinates of the point we're trying to create will be undefined. So, we write code to test to see whether the x and y values are passed in. If they are, we initialize t his.x and t his.y with the values x and y respectively. If we don't pass in any values, we use the default value, 50 for both t his.x and t his.y .

Now, you might be tempted to take a shortcut and rewrite if (x == undef ined || x == null) { ... } as if (!x) { ... } (based on what you learned in the previous lesson about truthy and falsey values), but be careful! We might want a point at 0, 0, and 0 is falsey, so that shortcut won't work for us in this case. We can, however, shorten the initialization a bit by making use of the co ndit io nal o perat o r . Modify po int .ht ml as shown:

![](Image00116.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Initializing objects </title>

<meta charset="utf-8">

<script>

function Point(x, y) {

this.x = (!x && x != 0) ? 50 : x;

this.y = (!y && y != 0) ? 50 : y;

if (x == undefined || x == null) {

this.x = 50;

} else { this.x = x;

}

if (y == undefined || y == null) {

this.y = 50;

} else { this.y = y;

}

           Make a toString() method we can use to display the point this.toString = function() {

return "[" + this.x + ", " + this.y + "]";

}

}

           Can have code in constructors too var p = new Point();

console.log("My point is: " + p.toString());

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) and ![](Image00021.jpg) . You see the same result as before.

Now, some programmers avoid the conditional operator (also written ?: for short) like the plague, because it's harder to read, and you can always write the same code using an easier-to -read if/else statement. If you're in this camp, feel free to use if/else statements instead. Still, you need to know how to read statements that use the conditional operator too; they are used fairly often to initialize objects.

So, you read this:

![](Image00076.jpg)

OBSERVE:

this.x = (!x && x != 0) ? 50 : x;

like this: "If not x AND x is not equal to 0, T HEN set this.x to 50 ELSE set this.x to x."

In other words, you read ? as THEN and : as ELSE.

This statement checks to see if !x is true, which it will be if the parameter x is null, undefined, or 0 . Then, to handle the 0 case, we check to make sure x != 0 . If x is 0, this returns false, so the whole conditional is false, and we set t his.x equal to x , which is 0 in this case. If x is undefined or null, we set t his.x to 50 . If x is a non-zero number we set t his.x to x .

Don't get the parameter x mixed up with the property t his.x . They are two different variables! Remember that we're passing a value into the constructor to initialize the property t his.x . The value we pass in gets assigned to the parameter x .

Each Point object also has a In t o St ring() we use t his.x

method, t o St ring() , that creates a string representation of the point for display. and t his.y to create the string representing the Point. Make sure to use the

object's properties, and not the parameters in the method. If you forget, and use x and y instead of t his.x and t his.y , what could happen? Well, if Po int () is called with no arguments, then the parameters x and y will be undefined. While the Point's x and y properties are set correctly to 50 each, you'll see [ undef ined, undef ined ] when you call the t o St ring() method.

We've talked a bit about what happens to t his when you're constructing objects. To amek sure you've got a handle on t his when you're working with constructor functions, regular functions, objects, and methods, let's take a look at another example. Create this new file:

![](Image00117.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> What happens to this </title>

<meta charset="utf-8">

<script>

//

           Rectangle constructor that makes rectangle objects

function Rectangle(width, height) { console.log("This in Rectangle is: "); console.log(this);

this.width = width || 0;

this.height = height || 0;

this.getArea = function() {

console.log("This in Rectangle's getArea is: "); console.log(this);

return this.width * this.height;

};

}

var rect1 = new Rectangle(5, 10);

console.log("Area of rectangle 1: " + rect1.getArea());

//

           A function that makes rectangle objects

function makeRectangle(width, height) { console.log("This in makeRectangle is: "); console.log(this);

return {

width: width || 0,

height: height || 0,

getArea: function() {

console.log("This in makeRectangle's getArea is: "); console.log(this);

return this.width * this.height;

}

};

}

var rect2 = makeRectangle(5, 10);

console.log("Area of rectangle 2: " + rect2.getArea());

           getArea function function getArea(r) {

console.log("This in getArea is: "); console.log(this);

return (r.width * r.height);

}

console.log("Area from getArea(rect1): " + getArea(rect1));

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as rect angle .ht ml and ![](Image00085.jpg) . In the console, you see lots of output:

![](Image00118.jpg)

There's quite a bit going on here, so we'll step through it one piece at a time:

![](Image00119.jpg)

OBSERVE:

//

Rectangle constructor that makes rectangle objects

function Rectangle(width, height) { console.log("This in Rectangle is: "); console.log(this);

this.width = width || 0;

this.height = height || 0;

this.getArea = function() {

console.log("This in a Rectangle's getArea is: "); console.log(this);

return this.width * this.height;

};

}

var rect1 = new Rectangle(5, 10);

console.log("Area of rectangle 1: " + rect1.getArea());

In this code, we've got a Rect angle() constructor function that we can use to make rectangles with widt h and height properties, and a method, get Area() that returns the area of the rectangle. We've added calls to co nso le .lo g() in two different places within the constructor function to inspect the value of t his .

When we call new Rect angle(5, 10) to create a rectangle object, rect 1 , the f irst t wo lines o f co de in t he f unct io n display the value of t his . The result is an empty Rect angle object:

![](Image00043.jpg)

OBSERVE:

This in Rectangle is:

Rectangle {}

When we call a construction function with new , the first thing that happens is a new, empty object is created. This is the Rect angle { } object we see here in the console. Its constructor is Rect angle , and it doesn't have any properties (yet).

The rest of the constructor function assigns values to the widt h , height and get Area() properties, so that when the object is returned at the end of the function, all of its properties have been created and given values.

Next, we call t he get Area() met ho d o f t he rect angle o bject we just creat ed . The f irst t wo lines o f t he get Area() met ho d display the value of t his in the console. We see that t his is a Rectangle object, and that now it has the properties we created in the constructor:

![](Image00120.jpg) OBSERVE:

This in Rectangle is:

Rectangle {}

This in Rectangle's getArea is:

Rectangle {width: 5, height: 10, getArea: function}

Area of rectangle 1: 50

Finally, we display the result of the call to get Area() , which is 50 .

So in both the body of the constructor function and the method, t his refers to "this object," that is, the Rectangle object created by the constructor. The first use of t his is the object when it's created and modified at object creation time (when we call the constructor function). The second use of t his is the object when it's accessed after we call the object's method, get Area() . In this case, the value of t his is assigned automatically because you are calling a method of an object.

Now let's compare that to what happens when we call makeRect angle() to make a rectangle object.

![](Image00121.jpg)

OBSERVE:

//

A function that makes rectangle objects

function makeRectangle(width, height) { console.log("This in makeRectangle is: "); console.log(this);

return {

width: width || 0,

height: height || 0,

getArea: function() {

console.log("This in makeRectangle's getArea is: "); console.log(this);

return this.width * this.height;

}

};

}

var rect2 = makeRectangle(5, 10);

console.log("Area of rectangle 2: " + rect2.getArea());

makeRect angle() isn't a constructor function, it's just a regular function, so we don't call it with new ; we just call it the regular way. The f irst t wo lines o f co de in makeRect angle() display the value of t his . You can see that t his is the global, Windo w object:

![](Image00095.jpg)

OBSERVE:

This in makeRectangle is:

Window {top: Window, window: Window, location: Location, external: Object, chrom

e: Objec t� }

This in a makeRectangle's getArea is:

Object {width: 5, height: 10, getArea: function}

Area of rectangle 2: 50

There is no object being created automatically by makeRect angle() . While we are creating an object in this function, that object is not the value of t his . We create that object in the next statement (by returning an object literal).

However, when we call t he get Area() method of the object returned by makeObject () , rect 2 , you can see that the value of t his in the get Area() method is indeed an object:

![](Image00122.jpg) OBSERVE:

This in makeRectangle is:

Window {top: Window, window: Window, location: Location, external: Object, chrom

e: Objec t� }

This in makeRectangle's getArea is:

Object {width: 5, height: 10, getArea: function}

Area of rectangle 2: 50

The object that we see is rect 2 , "this object," that is, the object whose method we called. Again, notice that the object's constructor is Object () (compare to the constructor for rect 1 above).

Finally, we display the area for rect 2 , which is 50 .

We've also included a function get Area() that takes a rectangle object and returns the area:

![](Image00123.jpg)

OBSERVE:

           getArea function function getArea(r) {

console.log("This in getArea is: "); console.log(this);

return (r.width * r.height);

}

console.log("Area from getArea(rect1): " + getArea(rect1));

The value of t his in the get Area() function displays as:

![](Image00104.jpg)

OBSERVE:

This in getArea is:

Window {top: Window, window: Window, location: Location, external: Object, chrom

e: Objec t� }

Area from getArea(rect1): 50

Once again, t his is the glo bal Windo w o bject . Just like makeRect angle() , get Area() is just a regular old function that happens to take an object and compute something with it. There is no "this object" for this function, so the value of t his gets set to the Window object automatically.

Keeping track of the value of t his can be tricky in JavaScript, but it's important. You'll need to understand how the value of t his is set, and what it's set to in all situations. We'll also revisit t his in later lessons.

Constructing Array Objects

Before we leave this lesson, let's talk about constructing Array objects. Arrays are objects, although you should think of them as a special kind of object with features that the objects we've been creating so far don't have, like an index, and ordering imposed on the items in the object.

There are two ways to create an Array object. Type these commands in the console:

![](Image00124.jpg)

INTERACTIVE SESSION:

       var a1 = new Array(); undefined

        a1[0] = 1;

1

        a1[1] = 2;

2

        a1[2] = 3;

3

        a1

[1, 2, 3]

Here we created an empty array, a1 , using the Array() constructor function, calling it with new like we would

any other constructor function. Then we add array items one at a time to the 0, 1, and 2 indices in the array. This is analogous to using new Object () and adding object properties one at a time, like we did with bo o k3 earlier in the lesson.

You can use bracket notation to access an object's properties, like this:

![](Image00076.jpg)

OBSERVE:

var theTitle = book1["title"];

the bracket notation is used to access the items in an array, except we use an index instead of a property name.

The second way to create an Array is to use the array literal notation:

![](Image00060.jpg)

INTERACTIVE SESSION:

var a2 = [1, 2, 3]; undefined

a2

[1, 2, 3]

This does exactly the same thing as the previous example; it creates a new array with values at the 0, 1, and 2 indices, but it's a lot shorter to write! In practice, you'll rarely use the Array() constructor to create an array. Instead you'll use the more concise array literal notation. One exception is when you need to create an empty array with a predefined number of indices:

![](Image00060.jpg)

INTERACTIVE SESSION:

var a3 = new Array(100); undefined

a3

[undefined x 100]

This creates an array with length 100, with all the items at every index set to undef ined , and the Chrome console uses the shorthand "[undefined x 100]" to display the value of this array. (Other browsers don't use this shorthand, so you'll see different results in different browsers when you ask for the value of a3 ).

Just like any other object, arrays can have named properties, and in fact, come with a named property, lengt h , that you'll use to get the length of your array:

![](Image00059.jpg)

INTERACTIVE SESSION:

a1.length

3

a2.length

3

a3.length

100

Just like other objects, you can use the co nst ruct o r property to inspect the constructor function for the array:

![](Image00089.jpg) INTERACTIVE SESSION:

        a1.constructor

function Array() { [native code] }

        a2.constructor

function Array() { [native code] }

        a3.constructor

function Array() { [native code] }

In each case, the constructor for the array is Array() . This is analogous to Object () being the constructor for objects created with literal notation or with new Object () .

In this lesson, you learned about constructing objects, how constructor functions work, the difference between objects created with a constructor function and those created using literal notation, and what happens to t his when you construct and use an object.

In the next lesson, we'll explore more object-related goodies: prototypes and inheritance. Before you dive in though, do the quizzes and projects, and then take a well-earned break.

Prototypes and Inheritance

![](Image00005.jpg)

Lesson Objectives

When you complete this lesson, you will be able to:

use instanceof to check the constructor, or "type," of a specific object.

![](Image00006.jpg)

examine the prototype property of a constructor function.

![](Image00006.jpg)

add methods to an object's prototype to share them among objects.

![](Image00006.jpg)

explore what happens to t his in an object's prototype.

![](Image00006.jpg)

examine an object's prototype chain.

![](Image00006.jpg)

use prototypal inheritance to access properties from higher up the prototype chain.

![](Image00006.jpg)

determine if a property is defined in an object or an object's prototype with hasOwnProperty().

![](Image00006.jpg)

examine the prototype of an object in the console using __proto __.

![](Image00005.jpg) ![](Image00006.jpg)

JavaScript is an "object-oriented language" in two ways: first it's object-oriented in that just about everything in the language is an object (except for a few primitives). Second, it's object-oriented in the sense that objects can inherit properties from other objects and, thus, share code with them. However, if you have had any experience with a language like Java or C++ or C#, be prepared to think differently in this lesson, because JavaScript objects inherit properties differently than those languages do .

Object-Oriented Programming in JavaScript

The key to understanding JavaScript objects work, and how they inherit properties, is to understand object

proto types . Before we jump into prototypes though, let's review how objects are created with constructor functions, and also introduce a new operator, instance of .

instanceof

Let's begin our in-depth study of objects by creating an example. We'll make this example a bit more interesting and display a representation of the objects in the web page (the point is to understand how objects work though, so don't get too caught up in the cool web page part of this example). Create a new HTML file as shown, and then go through it, step by step:

![](Image00125.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Shapes with Prototypes and Inheritance </title>

<meta charset="utf-8">

<style>

html, body, div#container {

width: 100%;

height: 100%;

margin: 0px;

padding: 0px;

}

div#container {

position: relative;

}

.shape {

position: absolute;

text-align: center;

}

.shape span {

position: relative;

top: 44%;

}

.square {

background-color: lightblue;

}

.circle {

background-color: goldenrod;

border-radius: 50%;

}

</style>

<script>

function Circle(name, radius) {

this.name = name;

this.radius = radius;

this.getCircumference = function() {

return this.radius * Math.PI * 2;

};

this.getName = function() {

return this.name;

};

}

function Square(name, size) {

this.name = name;

this.size = size;

this.getArea = function() {

return this.size ^ 2;

};

this.getName = function() {

return this.name;

};

}

Global variables so we can inspect them

easily in the console!  (Otherwise, we'd normally

make them local to the window.onload function). var circle1 = new Circle("circle1", 100);

var circle2 = new Circle("circle2", 200); var square = new Square("my square", 150);

window.onload = function() {

addShapeToPage(circle1);

addShapeToPage(circle2);

addShapeToPage(square);

};

function addShapeToPage(shape) {

![](Image00126.jpg)

var container = document.getElementById("container"); var div = document.createElement("div"); var width = 0;

var classes = "shape ";

if (shape instanceof Circle) {

classes += "circle";

width = shape.radius;

} else if (shape instanceof Square) { classes += "square";

width = shape.size;

}

div.setAttribute("class", classes);

div.style.left = Math.floor(Math.random() * (container.offsetWidth - 175)) + "px";

div.style.top = Math.floor(Math.random() * (container.offsetHeight - 175)) + "px";

div.style.width = width + "px";

div.style.height = width + "px";

var span = document.createElement("span");

span.innerHTML = shape.getName();

span.style.visibility = "hidden";

div.appendChild(span);

div.onmouseover = function() {

           this is the div (the shape) you click on this.firstElementChild.style.visibility = "visible";

};

container.appendChild(div);

}

</script>

</head>

<body>

<div id="container"></div>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as pro t o .ht ml , and ![](Image00127.jpg) . You see three shapes on the page: two circles, and a square. Open the console, and verify that you can access the three global variables we created for the three shapes:

![](Image00088.jpg)

INTERACTIVE SESSION:

circle1

Circle {name: "circle1", radius: 100, getCircumference: function, getName: funct ion}

circle2

Circle {name: "circle2", radius: 200, getCircumference: function, getName: funct ion}

square

Square {name: "my square", size: 150, getArea: function, getName: function}

We have much to discuss in this code, including a new operator, inst anceo f . We'll go over it one chunk at a time.

First, we have two constructor functions, Circle() and Square() :

![](Image00115.jpg) OBSERVE:

function Circle(name, radius) {

this.name = name;

this.radius = radius;

this.getCircumference = function() {

return this.radius * Math.PI * 2;

};

this.getName = function() {

return this.name;

}

}

function Square(name, size) {

this.name = name;

this.size = size;

this.getArea = function() {

return this.size ^ 2;

};

this.getName = function() {

return this.name;

}

}

Circle() and Square() are similar to other constructor functions we've worked with in this course. The two constructors are almost identical; both have a name property and a get Name() method. Circle() has a radius property and a get Circumf erence() method, while Square() has a size property and a get Area() method.

Next, we create three objects from the two constructors: two circles and a square:

![](Image00033.jpg)

OBSERVE:

var circle1 = new Circle(" circle1 ", 100 );

var circle2 = new Circle(" circle2 ", 200 );

var square = new Square(" my square ", 150 );

We pass in initial values for the name property, and the radius and size properties for the circles and square, respectively. We can inspect these global variables in the console.

When we display the three objects in the console, we use a constructor function to make each kind of shape, we know that the circles are made from the Circle() constructor and the square is made from the Square() constructor:

![](Image00128.jpg)

OBSERVE:

> circle1

Circle {name: "circle1", radius: 100, getCircumference: function, getName: funct ion}

> circle2

Circle {name: "circle2", radius: 200, getCircumference: function, getName: funct ion}

> square

Square {name: "my square", size: 150, getArea: function, getName: function}

We have a short function assigned to the windo w.o nlo ad property that will run the browser and the DOM is ready. This function calls the addShapeT o Page() we've created.

once the page is loaded into function for each shape

![](Image00129.jpg) OBSERVE:

function addShapeToPage( shape ) {

var container = document.getElementById("container"); var div = document.createElement("div"); var width = 0;

var classes = "shape ";

if ( shape instanceof Circle) {

classes += "circle";

width = shape .radius;

} else if ( shape instanceof Square) { classes += "square";

width = shape .size;

}

div.setAttribute("class", classes);

div.style.left = Math.floor(Math.random() * (container.offsetWidth - 175)) + "px";

div.style.top = Math.floor(Math.random() * (container.offsetHeight - 175)) + "px";

div.style.width = width + "px";

div.style.height = width + "px";

var span = document.createElement("span");

span.innerHTML = shape .getName();

span.style.visibility = "hidden";

div.appendChild(span);

div.onmouseover = function() {

           this is the div (the shape) you click on this.firstElementChild.style.visibility = "visible";

};

container.appendChild(div);

}

The addShapeT o Page() function adds the shapes to the page. It has a shape parameter, which is either a circle or a square, and creates a <div> element for that shape. Of course, we want our circles to look like circles and our squares to look like squares, so we've created CSS classes to style the <div> elements for each kind of shape appropriately. Take a look back at the CSS and you'll see that we have a shape class for both kinds of shapes, a square class specifically for squares, and a circle class specifically for circles:

![](Image00130.jpg)

OBSERVE:

.shape {

position: absolute;

text-align: center;

}

.shape span {

position: relative;

top: 44%;

}

.square {

background-color: lightblue;

}

.circle {

background-color: goldenrod;

border-radius: 50%;

}

In addShapeT o Page() , we need to know if the shape that was passed in is a circle or a square. Why? Because if it's a circle, we want to add the circle class to the <div>, if it's a square, we want to add the square class to the <div>. In addition, in order to set the width of the <div> correctly, we'll need to access either the radius property for circles or the size property for squares.

So how do we determine if the shape that got passed in is a square or a circle? We use the inst anceo f operator:

![](Image00131.jpg) OBSERVE:

var width = 0;

var classes = "shape ";

if ( shape instanceof Circle ) {

classes += "circle";

width = shape .radius;

} else if ( shape instanceof Square ) { classes += "square";

width = shape .size;

}

The inst anceo f operator is a binary operator: it takes two arguments . The operand on the left is the object (you want to determine the type of that object) and the operand on the right is the name of the constructor function used to create the object. In this case, we use the inst anceo f operator to find out if the shape is a Circle . If it is, we know that the shape was constructed using the Circle() constructor function, and it's a circle object. Similarly, if it's Square , we know that shape is a square.

Once we know whether the shape is a circle or a square, we can set the classes and widt h variables, so the shapes will display correctly in the web page.

Then we set up the rest of the <div> to display a circle or square in the web page, and add the <div> to the

DOM so it displays in the page. We add a mo useo ver handler to the <div>. About that handler:

![](Image00104.jpg)

OBSERVE:

div.onmouseover = function() {

           this is the div (the shape) you click on

this .firstElementChild.style.visibility = "visible";

};

In the previous lesson we talked about t his and what t his is set to when you are constructing an object, or calling the method of an object.

In most circumstances, when an event handler that is attached to a DOM object is called, t his is set to the DOM object on which that event took place. So in this case, we attached a mouseover handler to the <div> object that represents our shape. When you mouse over that <div>, and the handler function is called, t his is set to the <div> object, not the shape object.

This can trip you up really easily, and yet another reason it's important to keep track of what t his is.

Prototypes

So wht are prototypes anyway?

Whenever you create an object in JavaScript, you get a second object with it, its pro t o t ype . The prototype is associated with the constructor of an object. Every function has a property, pro t o t ype , that holds a prototype object. Whenever you use that function as a constructor to create a new object, that new object gets the object in that function's pro t o t ype property as its prototype. So, the Circle() constructor function has a

pro t o t ype property that contains a Circle prototype object. If you use Circle() to create a new object, circle1 , circle1 's prototype will be Circle .pro t o t ype (that is, the object in the pro t o t ype property of the Circle() constructor).

You can take a look at the prototype of a constructor function by using the pro t o t ype property of the function, like this:

![](Image00132.jpg) INTERACTIVE SESSION:

Circle

function Circle(name, radius) {

this.name = name;

this.radius = radius;

this.getCircumference = function() {

return this.radius * Math.PI * 2;

};

this.getName = function() {

return this.name;

}

}

Circle.prototype Circle {}

Square

function Square(name, size) {

this.name = name;

this.size = size;

this.getArea = function() {

return this.size ^ 2;

};

this.getName = function() {

return this.name;

}

}

Square.prototype Square {}

When you type Circle at the console, you see its value is the constructor function, Circle() . When you type in Circle.prototype , you'll see its value is an object , Circle { } . The Circle .pro t o t ype object is an empty object; there's nothing in it. However, any object you make using the Circle() constructor gets this Circle { } object as its pro t o t ype .

You can find out the prototype of an object by getting the prototype of that object's constructor, like this:

![](Image00049.jpg)

INTERACTIVE SESSION:

circle1.constructor.prototype Circle { }

Try getting the prototype of the circle2 and square objects using the console. Do you get the result that you expect?

It can get a little confusing at first to keep all this straight. But just think of it like this: whenever you make an object, that object gets a prototype. A prototype is just an object! And if you want to access an object's prototype, you use that object's constructor function's pro t o t ype property.

So, when you write new Circle("circle1", 100) you get back an object, circle1 . The circle1 object's

prototype is another object, Circle .pro t o t ype . Note that while we say circle1 's prototype is

Circle .pro t o t ype , that doesn't mean that circle1 has a property named pro t o t ype (it doesn't). The

relationship between circle1 and its prototype is not the same as circle1 having a property. Now, you can

get to the prototype of circle1 through circle1 's constructor function, Circle() , using the constructor

function's pro t o t ype property: Circle .pro t o t ype , but that's a different thing. Maybe this diagram will help

make the distinction more clear:

![](Image00133.jpg)

Now, because you are creating the object circle2 using the same constructor function, Circle() , circle2 has the same prototype as circle1 :

![](Image00059.jpg)

INTERACTIVE SESSION:

       circle1.constructor.prototype Circle { }

       circle2.constructor.prototype Circle { }

       circle1.constructor.prototype === circle2.constructor.prototype true

I should point out that the prototype property is a property of the Circle() function . Yes, functions can have properties! Why? Because functions are objects! They are special objects, but they are objects just the same. We'll talk about this in more detail a little later.

Prototypes of Literal Objects

Let's see an example that uses the prototype of a literal object:

![](Image00092.jpg) INTERACTIVE SESSION:

       var myObject = { x: 3 }; undefined

        myObject

        myObject.constructor

function Object() { [native code] }

       myObject.constructor.prototype Object { }

       myObject instanceof Object true

       myObject instanceof Circle false

The literal myObject object's constructor is Object () , and its prototype is Object .pro t o t ype . We can check to see if myObject is an Object using inst anceo f . For good measure, we check to see if myObject is a Circle , and it's not. Good!

What is a Prototype Good For?

All this talk about prototypes, and you're probably still wondering, what good is a prototype? Why whould I care if an object has a prototype?

This is where "object- oriented programming" comes in. A huge advantage of a prototype is that you can put properties that will be shared across all objects and have that prototype, in the prototype object.

When you try to access a property of an object, whether that property contains a primitive value or a method, JavaScript first looks for that property in the object; if JavaScript doesn't find the property there, it looks in the prototype. If it finds the property there, that's the value JavaScript uses. This is called the pro t o t ype chain . Let's take a closer look at how this works.

circle1 and circle2 each have a different name, and a different radius, but the two methods, get Circumf erence() and get Name() , are the same for both objects—they don't change.

However, when you create two separate objects from the same constructor, like we did:

![](Image00043.jpg)

OBSERVE:

var circle1 = new Circle("circle1", 100);

var circle2 = new Circle("circle2", 200);

each object gets its own copy of the get Circumf erence() and get Name() methods:

![](Image00134.jpg)

In this example, it doesn't matter so much, but in an instance where each object has a large number of properties or methods, it can become problematic. Each object takes up memory. The more memory the object takes up, the more memory your program uses and the slower it will be.

The Circle .pro t o t ype of both circle1 and circle2 is currently an empty object:

![](Image00049.jpg)

INTERACTIVE SESSION:

circle1.constructor.prototype Circle { }

Similarly, the Square .pro t o t ype is currently an empty object.

We can move the two methods that both circles contain into the Circle .pro t o t ype object, and we can move the methods that all squares get into the Square .pro t o t ype object. Modify pro t o .ht ml as shown:

![](Image00135.jpg) CODE TO TYPE:

function Circle(name, radius) {

this.name = name;

this.radius = radius;

this.getCircumference = function() {

return this.radius * Math.PI * 2;

};

this.getName = function() {

return this.name;

};

}

Circle.prototype.getCircumference = function() { return this.radius * Math.PI * 2;

};

Circle.prototype.getName = function() {

return this.name;

};

function Square(name, size) {

this.name = name;

this.size = size;

this.getArea = function() {

return this.size ^ 2;

};

this.getName = function() {

return this.name;

};

}

Square.prototype.getArea = function() {

return this.size * this.size;

};

Square.prototype.getName = function() {

return this.name;

};

Global variables so we can inspect them

easily in the console!  (Otherwise, we'd normally

make them local to the window.onload function). var circle1 = new Circle("circle1", 100);

var circle2 = new Circle("circle2", 200); var square = new Square("my square", 150);

window.onload = function() {

addShapeToPage(circle1);

addShapeToPage(circle2);

addShapeToPage(square);

};

function addShapeToPage(shape) {

var container = document.getElementById("container"); var div = document.createElement("div"); var width = 0;

var classes = "shape ";

if (shape instanceof Circle) {

classes += "circle";

width = shape.radius;

} else if (shape instanceof Square) {

classes += "square";

width = shape.size;

}

div.setAttribute("class", classes);

div.style.left = Math.floor(Math.random() * (container.offsetWidth - 175)) + "px";

div.style.top = Math.floor(Math.random() * (container.offsetHeight - 175)) + "px";

div.style.width = width + "px";

div.style.height = width + "px";

![](Image00136.jpg) var span = document.createElement("span");

span.innerHTML = shape.getName();

span.style.visibility = "hidden";

div.appendChild(span);

div.onmouseover = function() {

           this is the div (the shape) you click on this.firstElementChild.style.visibility = "visible";

};

container.appendChild(div);

}

![](Image00087.jpg) and ![](Image00036.jpg) . The program works as it did before; you see three shapes (two circles and a square) in the page and when you mouse over the shapes, their names appear inside of them.

Open up the console and type this:

![](Image00049.jpg)

INTERACTIVE SESSION:

circle1.constructor.prototype

Circle { getCircumference: function, getName: function }

Now the prototype of circle1 contains the two methods, get Circumf erence() and get Name() . Check circle2 in the same way. Take a look at the Square .pro t o t ype object as well; it contains two methods now. So what did we do?

First, we removed the get Circumf erence() and get Name() methods from the Circle() constructor (we also removed the get Area() and get Name() methods from the Square() constructor). Then we added these methods to the Circle .pro t o t ype object, by setting the same property names (the method names) to the functions (we treat the Square prototype similarly):

![](Image00137.jpg)

OBSERVE:

Circle.prototype.getCircumference = function() { return this.radius * Math.PI * 2;

};

Circle.prototype.getName = function() {

return this.name;

};

Square.prototype.getArea = function() {

return this.size * this.size;

};

Square.prototype.getName = function() {

return this.name;

};

The Circle .pro t o t ype and Square .pro t o t ype objects, like any other object, can have methods. In the same way that you can add new properties to an object at anytime, because objects are dynamic, we can add new properties to the Circle .pro t o t ype and Square .pro t o t ype objects after those prototype objects have been created. So now, the get Circumf erance() and get Name() methods are stored only once—in the Circle .pro t o t ype object:

![](Image00138.jpg)

The Prototype Chain

The get Circumf erance() and get Name() methods are now stored in the Circle .pro t o t ype object instead of in both the circle1 and circle2 objects. Let's see what happens when we try to call one of these methods:

![](Image00060.jpg)

INTERACTIVE SESSION:

        circle1.getName()

"circle1"

       circle1.getCircumference() 628.3185307179587

We called the get Name() method on the circle1 object , just like we did before, but circle1 no longer contains that method. Instead, that method is now in circle1 's prototype object. So, how does it work? JavaScript uses the pro t o t ype chain to look for a property. If a property is not found in an object, JavaScript looks at that object's prototype to see if it's there:

![](Image00139.jpg)

The get Name() method is in the prototype, so that method is called.

Notice that the method in the prototype object still uses t his . So how is t his being set to the correct object? After all, the get Name() method is now in the prototype object, but it still works for both circle objects.

When you call a method, like circle1.get Name() , the object that contains the method being called, in this case circle1 , is used as t his , even if that method is in the object's prototype. So, when you call circle1.get Name() , t his is set to circle1 . When you call circle2.get Name() , t his is set to circle2 .

Let's go back to the console and do a little more testing to help all this sink in (this next session is from the

Chrome console, so use Chrome if you want to duplicate it exactly):

![](Image00140.jpg)

INTERACTIVE SESSION:

Circle

function Circle(name, radius) {

this.name = name;

this.radius = radius;

}

Circle.prototype

circle1

Circle { name: "circle1", radius: 100, getCircumference: function, getName: func tion }

circle1.constructor

function Circle(name, radius) {

this.name = name;

this.radius = radius;

}

circle1.constructor.prototype

circle2.constructor.prototype

Circle { getCircumference: function, getName: function }

First, we check the value of Circle . It's just the constructor function Circle() . Then we check the value of Circle .pro t o t ype . Remember, functions are objects, so they can have properties, just like any other object. We ask for the value of the pro t o t ype property of the Circle() constructor function; the value is a Circle object containing two properties get Circumf erance() and get Name() , both of which are methods.

Next, we check the value of circle1 . This is a Circle object, because it was constructed with the Circle() constructor function, and contains four properties: name , radius , get Circumf erance() and get Name() . But wait! We moved the two methods to the prototype. Why are they listed here in the object? In this case, it's because the Chrome console is showing the properties in the circle1 's prototype object, to demonstrate that they are accessible as properties. (We'll see soon how to tell whether a property exists in an object or an object's prototype.)

Finally, we check the prototype of both the circle1 and circle2 objects by first getting the co nst ruct o r (using the co nst ruct o r property of the object, which is Circle() ), and then getting the prototype, using the

pro t o t ype property of the constructor. We see that the prototype of both these objects is a Circle object.

Try this with the square object.

We are accessing the get Name() method of the object that's in the variable shape when we create the <span> that goes inside the <div> representing the shape:

![](Image00104.jpg)

OBSERVE:

var span = document.createElement("span");

span.innerHTML = shape.getName();

span.style.visibility = "hidden";

div.appendChild(span);

Just like we saw in the console session, when we access shape .get Name() , we're using the method that's

stored in the shape's prototype. It doesn't matter if the shape is circle1 , circle2 , or square ; we find the

get Name() in the prototype ( Circle .pro t o t ype or Square .pro t o t ype , depending on which type of object

is stored in the variable shape ), and t his gets set to the object in the variable shape ).

Since Circle .pro t o t ype and Square .pro t o t ype are objects, they also have prototypes. The prototype of Circle .pro t o t ype is Object .pro t o t ype . Remember that Object () is a built-in constructor function that is used to create objects, like when you write:

![](Image00141.jpg) INTERACTIVE SESSION:

       var o = { x: 3 }; undefined

        o

Object { x: 3 }

        o.constructor

function Object() { [native code] }

       Object.prototype Object { }

      is an object, and because it's a literal object, its constructor is Object () . The Object () constructor has a pro t o t ype property, which contains o 's prototype. Object .pro t o t ype looks like an empty Object, but it only appears that way in the console. In reality, this object contains a bunch of built-in methods for objects, like t o St ring() . You can't see them because the implementation of Object .pro t o t ype is internal to the browser (that is, it's not JavaScript you wrote); it's just like the [native code] you see when you try to inspect Object () ).

So let's see what happens when we type this:

![](Image00049.jpg)

INTERACTIVE SESSION:

       circle1.toString(); "[object Object]"

Remember the prototype chain: when you write circle1.t o St ring() , JavaScript looks first in circle1 , doesn't find the t o St ring() method there, so then it looks in circle1 's prototype ( Circle .pro t o t ype) . If it doesn't find the method there, it looks in circle1 's prototype's prototype ( Object .pro t o t ype ) and finds the method there. We call this "looking up the prototype chain" to find the method:

![](Image00142.jpg)

So what's the prototype of the object Object .pro t o t ype ? It's the only object in JavaScript that doesn't have a prototype. Object .pro t o t ype is the top of the prototype chain, so the lookup ends there.

Prototypal Inheritance

Every object you create inherit s properties from the prototypes all the way up the prototype chain. In our example, circle1 , inherits the methods get Name() and get Circumf erence() from its prototype (because we specifically added them to the prototype), and circle1 inherits the method t o St ring() from the

Object .pro t o t ype .

We call this pro t o t ypal inherit ance , which means that if you try to access a property in an object, and that property doesn't exist in the object itself, JavaScript looks up the prototype chain to try to find that property. Most objects either have one or two prototypes. An object will have the prototype, Object .pro t o t ype , if it is an object literal, or if it has been created using new Object () . An object will have two prototypes if it is created using a constructor function like Circle() , in which case the first prototype up the chain is the

Circle .pro t o t ype and the second is one more step up the chain, Object .pro t o t ype . Some objects have a longer chain, but that's fairly rare.

Let's come back to inst anceo f for a moment. Earlier we talked about inst anceo f as an operator to determine which type of object you have. We use it in the example for this lesson to figure out whether shape is a circle or a square:

![](Image00123.jpg)

OBSERVE:

if (shape instanceof Circle) {

classes += "circle";

width = shape.radius;

} else if (shape instanceof Square) { classes += "square";

width = shape.size;

}

inst anceo f checks the prototype chain of shape to see if there is a Circle .pro t o t ype object or a Square .pro t o t ype object. In our example, the shape was constructed by either the Circle() or Square() constructor functions, so our shape will a have Circle .pro t o t ype prototype, or a Square .pro t o t ype prototype, and so we'll find one of these prototypes in the chain.

Remember, Object .pro t o t ype is also in the prototype chain, so we could write this:

![](Image00061.jpg)

INTERACTIVE SESSION:

       circle1 instanceof Circle true

       circle1 instanceof Object true

       square instanceof Square true

       square instanceof Object true

circle1 is an instance of both a Circle and an Object! The same is true with square ; square is an instance of both a Square and an Object. That makes sense, because all objects are instances of Object, after all. However, the extra object in the prototype chain gives you more information about the kind of object you're dealing with. In this case, it tels you whether the object is a circle or a square.

If you have experience using an object- oriented language like Java or C++ or C#, prototypal inheritance probably seems quite strange to you. It certainly is different from classical inheritance, where you create objects from classes, and create an inheritance hierarchy by extending other objects. For more on prototypal [inheritance and classical inheritance, and a comparison of the two, see the Wikipedia page on Prototype-](http://en.wikipedia.org/wiki/Prototype-based_programming) [based programming .](http://en.wikipedia.org/wiki/Prototype-based_programming)

When are Prototype Objects Created?

You can add properties to prototype objects, like Circle .pro t o t ype , after these objects are created, but when are prototype objects created? A prototype object is created whenever you define a function. In other words, every function has a prototype property that contains a prototype object. If you then use that function to create a new object using new , that new object gets that function's prototype.

So we can add properties to the Circle .pro t o t ype and Square .pro t o t ype objects as soon as the Circle() and Square() functions have been defined, even before we use them to create any objects. Look back at the code and you'll see that we add properties to both prototypes, before we ever define circle1 , circle2 , or square .

Try this in the console (make sure you've loaded the pro t o .ht ml document first):

![](Image00092.jpg) INTERACTIVE SESSION:

       Circle.prototype.x = 400; 400

       Circle.prototype.y = 200; 200

        circle1.x

400

        circle1.y

200

        circle2.x

400

        circle2.y

200

We added two properties to the Circle .pro t o t ype object after we created the circle1 and circle2 objects, and yet you can see that those properties have values when we query circle1 and circle2 . It may seem odd that properties can appear in objects after they're created, without modifying those objects specifically (by adding a property directly, like circle1.x = 400; ). If you look back at the diagram that shows how prototypes work though, you'll see that if you try to access a property in an object and that property doesn't exist in the object itself, we go up the prototype chain to find it. Even if we add a property to the prototype of an object after that object is created, that property will be accessible from the object.

hasOwnProperty

An object can inherit properties from its prototype chain, but how can you find out if a property is in the object itself, or in one of the object's prototypes? You use the hasOwnPro pert y() method. Make sure your pro t o .ht ml document is loaded and try this in the console:

![](Image00124.jpg)

INTERACTIVE SESSION:

       circle1.hasOwnProperty("name") true

       circle1.hasOwnProperty("getName") false

       circle1.hasOwnProperty("radius") true

        Circle.prototype.x = 400;

400

       circle1.hasOwnProperty("x") false

The property name you pass to hasOwnPro pert y() must be a string (put the property name in quotation marks). The result of calling circle1.hasOwnPro pert y("name") is true because the property name , is defined in the circle1 object. However, the get Name property (a method) is not defined in the circle1 object, it's defined in circle1 's prototype, Circle .pro t o t ype , so the result of calling hasOwnPro pert y() on this property is false. Similarly, the property radius is defined in circle1 , but the property x is not; it's defined in the Circle .pro t o t ype .

Try this:

![](Image00060.jpg)

INTERACTIVE SESSION:

       circle1.hasOwnProperty("hasOwnProperty"); false

       Object.prototype.hasOwnProperty("hasOwnProperty"); true

We called the hasOwnPro pert y() method on the circle1 object, but hasOwnPro pert y() isn't defined in either circle1 or Circle .pro t o t ype , so it must be defined in Object .pro t o t ype . Since all objects inherit

this method, you can call hasOwnPro pert y() on any object, including the Object .pro t o t ype object, which contains this method. That's kind of weird, but you can see why the result of calling Object.prototype.hasOwnProperty("hasOwnProperty"); is true.

__proto__

You've seen the __pro t o __ property used in a previous lesson when we inspected an object. You can see it if you look at circle1 in the Chrome console and expand the object by clicking on the little arrow next to it:

![](Image00143.jpg)

This property refers to the prototype of an object. In this case, our object is circle1 , and its prototype is Circle .pro t o t ype , displayed as Circle in the __pro t o __ property. In fact, in the Chrome console, you can ask for the value of that property, like this:

![](Image00144.jpg)

The prototype of circle1 is a Circle object that contains the two methods we added, get Name() and

get Circumf erence() , along with the properties x and y that we added to the prototype later (you might not see x and y if you've reloaded the page). Circle .pro t o t ype has a __pro t o __ property,

Object .pro t o t ype , so the __pro t o __ property of objects allows you to see the prototype chain.

However, do no t rely o n t his pro pert y . It's kind of a secret property that browsers implement, but it's not officially part of the JavaScript standard and could disappear or change at any time. Use it to inspect objects in the console, but not in your programs!

Setting the Prototype Property to an Object Yourself

So far, we've used the default prototype you get when you create a constructor function, and then added our own properties and methods to that prototype object for inheritance, but you can actually set the prototype of a constructor yourself to an object you've created. Let's see how:

![](Image00145.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Shapes with Prototypes and Inheritance: Setting the prototype yourself </title>

<meta charset="utf-8">

<script>

var shape = {

           0,

           0,

area: 0,

setPosition: function(x, y) { this.x = x;

this.y = y;

},

displayInfo: function() {

console.log("Your shape has area " + Math.ceil(this.area) + ", and i

s located at " + this.x + ", " + this.y);

}

};

function Circle(radius) {

this.radius = radius;

this.computeArea = function() {

this.area = Math.PI * (this.radius * this.radius);

};

}

function Square(size) {

this.size = size;

this.computeArea = function() {

this.area = this.size * this.size;

};

}

Circle.prototype = shape;

Square.prototype = shape;

var circle = new Circle(50);

circle.setPosition(100, 100);

circle.computeArea();

circle.displayInfo();

var square = new Square(50);

square.setPosition(300, 300);

square.computeArea();

square.displayInfo();

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as set Pro t o .ht ml , and ![](Image00021.jpg) . Open the console, and you see this:

![](Image00049.jpg)

INTERACTIVE SESSION:

Your shape has area 7854, and is located at 100, 100

Your shape has area 2500, and is located at 300, 300

We defined a literal object, shape , using some properties and methods. We made this a literal object, not a

constructor because we don't want users to create new shape objects; we want them to create circles and squares.

Then we define two simple constructors, one for Circle objects, and one for Square objects:

![](Image00043.jpg)

OBSERVE:

Circle.prototype = shape;

Square.prototype = shape;

We set t he pro t o t ype pro pert y of the Circle constructor object to the shape object, and we do t he same f o r t he Square co nst ruct o r o bject . So now, the prototype object for circle is a shape object rather than a Circle . As such, circle inherits the methods and properties of the shape object, so we can call circle .set Po sit io n() and circle .displayInf o () . square works the same way as well.

In this example, we use the same object as the prototype for both circles and squares: shape . That means the properties and methods in the prototype object need to make sense for both circles and squares. Before, we set properties of the prototype by writing Circle .pro t o t ype .PROPERT Y = PROPERT Y VALUE and Square .pro t o t ype .PROPERT Y = PROPERT Y VALUE because we needed different properties and methods for circles and squares. Keep this in mind as you are setting up your object prototypes; how you choose to set up the prototype chain depends on your individual situation and whether you need different prototypes or the same prototype for your objects.

Take a look at the circle and square objects:

![](Image00091.jpg)

INTERACTIVE SESSION:

        circle

Circle {radius: 50, computeArea: function, x: 100, y: 100, area: 7853.9816339744 8 3� }

        square

Square {size: 50, computeArea: function, x: 300, y: 300, area: 2500}

        circle.constructor.prototype

Object {}

        square.constructor.prototype

Object {}

       circle instanceof Circle true

        circle instanceof shape

TypeError: Expecting a function in instanceof check, but got #<Circle>

We see that the constructor for circle is Circle , and for square , it's Square , but now, the

circle .co nst ruct o r.pro t o t ype is shown as Object {} (it was Circle {} before). That's because the prototype is the square object, and since the square object is a literal object, its constructor is Object () , so its "type" is Object . square works the same way.

In other words, circle is an instance of Circle (because we made circle using the Circle() constructor), and circle is an instance of Object because shape is a literal object, and its constructor is Object () .

Protoypal inheritance and object prototypes are not extremely complicated, yet this topic can be difficult to wrap your head around, especially if you have experience with class-based languages. You have to put all that knowledge aside and think differently about objects and inheritance. It all boils down to this: in Javascript, every object has a prototype (except, of course, Object .pro t o t ype ), and can inherit properties from the prototype chain.

Make sure you give yourself plenty of time to practice and understand the concepts in this lesson. Experiment with your own objects and prototypes. Use the console to inspect your objects, and the tools you have in your pocket now to test to make sure that what you think should happen does. Practice and make sure you know what you're doing in the quizzes and projects.

Functions

![](Image00005.jpg)

Lesson Objectives

When you complete this lesson, you will be able to:

use basic functions.

![](Image00006.jpg)

use functions to organize code.

![](Image00006.jpg)

define functions using function declarations and function expressions.

![](Image00006.jpg)

compare the differences in using function declarations and function expressions.

![](Image00006.jpg)

express functions as first class values.

![](Image00006.jpg)

express functions as anonymous functions.

![](Image00006.jpg)

pass functions as values to other functions.

![](Image00006.jpg)

return a function from a function.

![](Image00006.jpg)

use a function as an event handler.

![](Image00006.jpg)

recognize how values are passed to functions using pass-by-value.

![](Image00006.jpg)

explain what happens when we pass objects to functions.

![](Image00005.jpg) ![](Image00006.jpg)

We've spent the last couple of lessons working with objects; now let's turn our attention to functions.

JavaScript Functions

We've used functions throughout the course, in a variety of different ways. It would be difficult to do any kind of serious JavaScript without using a function.

What is a Function?

A function is a block of code that's defined once, but can be executed many times. Let's look at a simple function declaration:

![](Image00104.jpg)

OBSERVE:

function computeArea ( radius ) {

var area = radius * radius * Math.PI;

return area ;

}

There are a lot of different parts to this function, so let's go through it, steb by step. First, we have the

function keyword. Then, we have the name of the function, computer Area . Then in parentheses, we have a parameter (radius) . The body of the function (the statements that are executed when you call the function) are defined within curly brackets. In the body of this function, we have two statements: first a statement that declares and computes a value for a lo cal variable, area , second a ret urn statement , that returns the value of area to the statement that called the function.

Let's call the function now:

![](Image00086.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Functions </title>

<meta charset="utf-8">

<script>

function computeArea(radius) {

var area = radius * radius * Math.PI;

return area;

}

var circleArea = computeArea(3);

console.log("Area of circle with radius 3: " + circleArea); </script>

</head>

<body>

</body>

</html>

![](Image00087.jpg) Save this in your /AdvJS folder as f unct io ns.ht ml , and ![](Image00127.jpg) . In the console, you see the area of the circle with the radius 3:

![](Image00043.jpg)

OBSERVE:

Area of circle with radius 3: 28.274333882308138 >

Let's take a closer look:

![](Image00095.jpg)

OBSERVE:

function computeArea( radius ) {

var area = radius * radius * Math.PI;

return area;

}

var circleArea = computeArea ( 3 );

We call the function using its name (co mput eArea) , passing an argument (3) to the function. The function's parameter, radius gets the value of the argument. That value is used in the computation. When we pass an argument into a function, we say that the argument is bo und to the parameter. So here, the value 3 is bound to the parameter radius .

The value returned from the function is stored in the variable circleArea .

We can call the function as many times as we want:

![](Image00020.jpg)

CODE TO TYPE:

function computeArea(radius) {

var area = radius * radius * Math.PI;

return area;

}

var circleArea = computeArea(3);

console.log("Area of circle with radius 3: " + circleArea); circleArea = computeArea(5);

console.log("Area of circle with radius 5: " + circleArea); circleArea = computeArea(7);

console.log("Area of circle with radius 7: " + circleArea);

![](Image00042.jpg) and ![](Image00021.jpg) . In the console, you now see the areas of the circles with radii of 5 and 7, along with the

area of the circle with radius 3.

By creating the function co mput eArea() , we packaged up a little bit of code that computes the area of a circle; that can then be reused each time we call the function. In addition, we can customize the code a bit each time we call the function by passing different values for the argument. We can also get customized values back from a function if we return a value. In this case, we get the area of the circle that provided the radius we passed into the function. Note that functions always return a value; if you don't explicitly return one, a function returns undef ined (unless you use it as a constructor, in which case the function returns an object).

So, functions are a way of reusing code. They're also a way of organizing your code. A good programming practice is to think of functions as a way to put related code together. For instance, you might put all code related to computing the area of a circle together in one function, while you put all code related to computing the distance between two points together in another function.

When you create a function, you're also creating a sco pe for executable statements. We'll look at scope in a lot more detail in the next lesson, but for now, notice that the parameter radius and the variable area are both lo cal (that is, visible only in the body of the function), rather than glo bal (that is, visible everywhere in your code). Programmers are often crtical of JavaScript's dependence on global variables, because global variables are easy to lose and misuse. Functions are good for keeping variables out of the global scope. This is especially useful when you combine your own code with code from libraries, like jQuery or Underscore.js. Using functions to keep variables out of the global scope is often called the Mo dule Pat t ern . We'll cover that in detail in a later lesson.

Different Ways of Defining a Function

In the code above, we used what's called a f unct io n declarat io n to define the co mput eArea() function.

That is, we declared the function using a statement that begins with the f unct io n keyword. It looks like this:

![](Image00033.jpg)

OBSERVE:

function functionName(parameters) {

// body goes here

}

One of the advantages to defining functions using function declarations is that you can place your functions above or below the code that uses them. Try it:

![](Image00146.jpg)

CODE TO TYPE:

function computeArea(radius) {

var area = radius * radius * Math.PI;

return area;

}

var circleArea = computeArea(3);

console.log("Area of circle with radius 3: " + circleArea); circleArea = computeArea(5);

console.log("Area of circle with radius 5: " + circleArea); circleArea = computeArea(7);

console.log("Area of circle with radius 7: " + circleArea);

function computeArea(radius) {

var area = radius * radius * Math.PI;

return area;

}

![](Image00042.jpg) and ![](Image00021.jpg) ; your code works exactly the same way as it did before, even though the function co mput eArea() is defined below where we are using it.

This works because when the browser loads your page, it goes through all your JavaScript and looks for function declarations before it begins executing your code. When you define a function at the global level like we did here, JavaScript adds the function as a property of the global window object, so that the function definition is visible everywhere in your code. Then, the browser goes back to the top of your JavaScript, and begins executing the code, top down. So, when the JavaScript interpreter gets to the first line where you call co mput eArea() , that function is defined, so the function call succeeds.

Another way you can create a function is to use a function expression :

![](Image00147.jpg)

CODE TO TYPE:

var circleArea = computeArea(3);

console.log("Area of circle with radius 3: " + circleArea); circleArea = computeArea(5);

console.log("Area of circle with radius 5: " + circleArea); circleArea = computeArea(7);

console.log("Area of circle with radius 7: " + circleArea);

function computeArea(radius) {

var area = radius * radius * Math.PI;

return area;

}

var computeArea = function(radius) {

var area = radius * radius * Math.PI;

return area;

};

We've replaced the function declaration with a variable declaration: we declare the variable co mput eArea and initialize that variable to the result of a f unct io n expressio n , that is, a function value. Because

co mput eArea is a global variable, the end result is almost the same: a property named co mput eArea is

added to the global window object set to the value of the function. However, when you ![](Image00042.jpg) and ![](Image00021.jpg) preview, you see an error instead of the expected log messages. Why?

JavaScript sees this statement as just a variable declaration and initialization. The value of the variable happens to be a function, but because we are not using a function declaration, the function is no longer defined in that first pass through the code; instead, the function is not defined until JavaScript gets to the variable declaration, which is when it executes the code from the top down. Now that the function is defined after the statements that try to call the function, we get an error message.

We can fix the error by moving the variable declaration to the top of the code, like this:

![](Image00148.jpg)

CODE TO TYPE:

var computeArea = function(radius) {

var area = radius * radius * Math.PI;

return area;

};

var circleArea = computeArea(3);

console.log("Area of circle with radius 3: " + circleArea); circleArea = computeArea(5);

console.log("Area of circle with radius 5: " + circleArea); circleArea = computeArea(7);

console.log("Area of circle with radius 7: " + circleArea);

var computeArea = function(radius) {

var area = radius * radius * Math.PI;

return area;

};

![](Image00042.jpg) and ![](Image00021.jpg) ; your code works again.

We also use function expressions when we define methods in objects:

![](Image00149.jpg) OBSERVE:

circle = {

radius: 3,

computeArea: function() {

var area = this.radius * this.radius * Math.PI; return area;

}

};

You can see we're using the same syntax to define the method ( co mput eArea() in the circle object) as we did when we defined it as a global function. The difference is that now the property is visible only in the circle object; the function is no longer a property of the global windo w object.

So, when defining global functions, which is better: using a function declaration, or declaring a variable and initializing it to a function expression?

The main advantage to using function declarations when defining global functions is that you know the functions will be visible throughout your code so you don't necessarily need to put them all at the top. However, as long as you don't need all of your functions to be defined at the time your code begins executing, using a variable declaration and setting the value of the variable to a function expression works just as well. Some programmers prefer that method of creating functions.

We often create and use functions that don't need to be defined in the global window object. Reducing the number of global variables (including functions!) is always preferable in JavaScript. So next, we'll take a look at other situations where we can use function expressions rather than function declarations.

Functions as First Class Values

We tend to think of functions as different from other kinds of values, like 3, or even an object, like circle , but in JavaScript, a function is just another kind of value, a value that you can assign to a variable or an object property, and even pass to or return from a function.

We say that functions are f irst class values in JavaScript. A first class value is one that can be stored in a variable, passed to a function, and returned from a function. You can already see that values like numbers, strings, and booleans are first class; so are objects. If you've been working with JavaScript for a while, you probably know that functions are first class. Not all languages have first class functions. In some languages, functions are treated separately and differently than other values.

So what's the deal with f irst class f unct io ns ? We'll take a look at the map() method to answer that question. Create a new file and add this code:

![](Image00150.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> First Class Functions </title>

<meta charset="utf-8">

<script>

var myArray = [1, 2, 3];

var newArray = myArray.map(function(x) { return x+1; }); console.log(newArray);

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as f unct io ns2.ht ml , and ![](Image00085.jpg) . Open the console. You see an array in the console:

![](Image00076.jpg)

OBSERVE:

[2, 3, 4]

![](Image00017.jpg) If you get an error when you try this code, it's because your browser doesn't yet support map() .

Note This is a fairly new method that was added to JavaScript as part of the EMCAScript 5 standard. Make sure you have the most recent version of your browser to try this code, as map() has

broad support in all the recent versions of browsers.

![](Image00018.jpg)

The map() method is an array method that all arrays inherit from the Array prototype. It takes a function and applies that function to each element of the array (in order). So in our example, map() first applies the function to myArray[0] , then myArray[1] , and so on. The array element is passed as the argument for the parameter x . map() returns a new array, the same length as the original array, with elements that are the values returned by each invocation of the function we passed to map() . In our example, the function we pass to map() adds one to each of the array elements, so the array you get back has items that are one greater than each of the corresponding items in the original array.

The value that we passed to map() is a function. Unfortuantely, since map() applies the function to the elements of the array for you (behind the scenes), you don't get to see how a function that is passed as an argument works. Let's implement our own version of map() , that way, you can see not only how to pass a function as an argument, but also how to use it in the function to which you pass it:

![](Image00093.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> First Class Functions </title>

<meta charset="utf-8">

<script>

var myArray = [1, 2, 3];

var newArray = myArray.map(function(x) { return x+1; }); console.log(newArray);

function map(a, f) {

var newArray = [];

for (var i = 0; i < a.length; i++) {

newArray.push(f(a[i]));

}

return newArray;

}

function addOne(x) {

return x+1;

}

var newArray2 = map(myArray, addOne);

console.log(newArray2);

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) and ![](Image00021.jpg) preview. In the console, you get the exact same result for our own version of map() as we did before, the array [2, 3, 4]. Let's go over the code, step by step:

![](Image00151.jpg) OBSERVE:

function map( a , f ) {

var newArray = [];

for (var i = 0; i < a.length ; i++) {

newArray .push( f ( a[i] ));

}

return newArray ;

}

function addOne(x) {

return x+1;

}

var newArray2 = map( myArray , addOne );

Our version of map() is a function, not a method, so we need to pass both the array and the f unct io n that will act on the array, to the map() function. That's why our function has two parameters instead of one.

First, we create a new empty array, newArray . Then we loop over all the elements in the array we passed in, a , and apply the function f to the array element. Inside map() , we find f . f produces a new value that we then add to the newArray at the same index as a[i] . When we finish, we return the newArray .

Now let's see how to call this map() function. We need an array and a f unct io n to pass to it; we'll reuse myArray (from the top of the code), and create a function named addOne() to pass. Just like before, addOne() is a function that takes one argument, adds one to it, and returns that new value. We call map() , passing in myArray and addOne as arguments for a and f , then get back a new array with each element one greater than myArray .

Passing a function to a function is much like passing any other value to a function, except you have to use it as a function, and you need to know what kind of arguments the function expects and what kind of value it returns (if any). You can write methods and functions like map() , that do some useful work, and can also be customized by passing in different functions.

Anonymous Functions

When we called the map() method on the array, we used a function expression as the argument that we passed to map() , whereas in our own implemention of map() , we use a declared function as the argument. It doesn't really matter which you use, but if you're not going to use the function addOne() anywhere other than as an argument to map() , you might want to avoid excess clutter and use a function expression instead:

![](Image00152.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> First Class Functions </title>

<meta charset="utf-8">

<script>

var myArray = [1, 2, 3];

var newArray = myArray.map(function(x) { return x+1; }); console.log(newArray);

function map(a, f) {

var newArray = [];

for (var i = 0; i < a.length; i++) {

newArray.push(f(a[i]));

}

return newArray;

}

function addOne(x) {

return x+1;

}

var newArray2 = map(myArray, addOne);

var newArray2 = map(myArray, function(x) { return x+1; }); console.log(newArray2);

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) and ![](Image00021.jpg) . You see the same result in the console.

Now, instead of declaring the function addOne() , we pass a function expression to map() . Unlike when we passed addOne() , this function doesn't have a name. It's known as an ano nymo us f unct io n . Of course, it has a name inside map() , because it gets bound to the name of the parameter, f .

Anonymous function expressions are just function values where the function has no name. This is useful when we're passing functions to functions, or returning functions from functions, because in both cases the function gets bound to a name so you can refer to it. When you pass an anonymous function to a function, it gets bound to the name of the parameter variable; when you return an anonymous function from a function, it gets stored in the variable you're using to hold the return value. You'll see anonymous functions used frequently in JavaScript as a shortcut to declare and name a function separately.

Returning a Function from a Function

Not only can you pass a function to a function, you can return a function from a function. Let's look at an example:

![](Image00153.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Returning Functions </title>

<meta charset="utf-8">

<script>

function makeConverterFunction(multiplier, term) { return function(input) {

var convertedValue = input * multiplier;

convertedValue = convertedValue.toFixed(2);

return convertedValue + " " + term;

};

}

var kilometersToMiles = makeConverterFunction(0.6214, "miles"); console.log("10 km is " + kilometersToMiles(10));

var milesToKilometers = makeConverterFunction(1.62, "km"); console.log("10 miles is " + milesToKilometers(10));

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as f unct io ns3.ht ml , and ![](Image00085.jpg) . In the console, you see this output:

![](Image00043.jpg)

OBSERVE:

10 km is 6.21 miles

10 miles is 16.20 km

Let's go over the code:

![](Image00154.jpg)

OBSERVE:

function makeConverterFunction(multiplier, term) { return function(input) {

var convertedValue = input * multiplier;

convertedValue = convertedValue.toFixed(2);

return convertedValue + " " + term;

};

}

var kilometersToMiles = makeConverterFunction(0.6214, "miles"); console.log("10 km is " + kilometersToMiles(10));

var milesToKilometers = makeConverterFunction(1.62, "km"); console.log("10 miles is " + milesToKilometers(10));

We're using one function, makeCo nvert erFunct io n() , to create two other functions, kilo met ersT o Miles and milesT o Kilo met ers . makeCo nvert erFunct io n() takes two arguments: a multiplier value to do a conversion (it doesn't matter what kind of conversion, as long as it can be done by multiplying one value by another), and a string representing the term of measurement we expect back from the function we generate.

makeCo nvert erFunct io n() returns a function. The function it returns takes one argument, input , and uses that argument in a computation with the parameters of makeCo nvert erFunct io n() .

makeCo nvert erFunct io n() knows nothing about the kind of conversion we want to do . It knows knows that it's generating a new function that multiplies input by mult iplier , uses t o Fixed() to make sure the resulting number has a fractional part of at most two numbers, and then returns a string made by combining the number with the t erm passed into makeCo nvert erFunct io n() .

We can use makeCo nvert erFunct io n() to make functions that do a specific kind of conversion, passing in

a value for multiplier and a string for term. So to create a f unct io n t hat co nvert s kilo met ers t o miles (kilo met ersT o Miles) , we pass in a multiplier of 0 .6214, and "miles," and get back a function that can do this conversion when we call it and pass in the number of kilometers. Similarly, we can create a f unct io n t o co nvert miles t o kilo met ers (milesT o Kilo met ers) by passing in 1.62 for the multiplier, and "km" for the term.

Review this code carefully to make sure you understand it. The makeCo nvert erFunct io n() returns a function that uses both the parameters of makeCo nvert erFunct io n() , as well as the (yet to be bound) parameter, input . Once makeCo nvert erFunct io n() creates its function and returns it, the parameters mult iplier and t erm go away, yet somehow, the functions kilo met ersT o Miles() and

milesT o Kilo met ers() "remember" those values. The secret to this somewhat magical ability to remember is the clo sure —we'll come back to that in a later lesson.

For now, just be aware that the arguments you pass into makeCo nvert erFunct io n() are used (and remembered) by the function that makeCo nvert erFunct io n() creates . So in kilo met ersT o Miles() , the value of mult iplier is 0 .6214 and the value of t erm is "miles," while in milesT o Kilo met ers() , the value of mult iplier is 1.62, and the value of t erm is "km."

Functions as Callbacks

At the heart of just about every JavaScript program are event s . When you write a web application, you use JavaScript to add interactivity to your page, which means your program needs to respond to events generated by the browser, and events generated by the user.

In JavaScript, we use functions to handle events. We often refer to event handlers as callbacks because when an event happens, we "call back" to a function to handle that event. Callbacks aren't always about browser and user events, but often they are.

You've probably used functions to handle events like the page load and button click events. If you've used Ajax (also known as XHR) or Geolocation in your JavaScript programs, you're probably familiar with functions used as callbacks. For instance, with Ajax, you provide a function to "call back" when XMLHttpRequest has loaded data from a file. With Geolocation, you provide a function to "call back" when the browser has located your position. Let's take a quick look at a basic Geolocation example so you can see how we use a function as a callback:

![](Image00155.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Functions as callbacks </title>

<meta charset="utf-8">

<script>

window.onload = function() {

if (navigator.geolocation) {

navigator.geolocation.getCurrentPosition(getLocation);

}

else {

console.log("Sorry, no Geolocation support!"); return;

}

};

function getLocation(position) {

var latitude = position.coords.latitude;

var longitude = position.coords.longitude;

var div = document.getElementById("container");

div.innerHTML = "You are at lat: " + latitude + ", long: " + longitude;

}

</script>

</head>

<body>

<div id="container"></div>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as f unct io ns4 .ht ml , and ![](Image00021.jpg) . Your location will be displayed

in the browser in a moment.

![](Image00034.jpg)

| Note | All modern browsers support Geolocation, but there are many reasons Geolocation can fail. If |
| you're not getting a location, don't worry, just follow along. |
|  |

![](Image00018.jpg)

We use functions as callbacks in two places in this example: first, we use an anonymous function as the load event handler, by setting the windo w.o nlo ad property to the function. That means when the browser triggers the "load" event—that is, when the page is fully loaded—the function that's been stored in the

windo w.o nlo ad property is called. This happens asynchronously . You can't anticipate when the page is loaded; all you know is that when the browser has loaded the page, it will call this function.

Second, we use the get Lo cat io n() function as a callback for the Geolocation get Current Po sit io n() method. Again, this is an event handler: a function that is called when a specific event happens—in this case, when the Geolocation object has found your position. This callback happens asynchronously: you can't anticipate how long it's going to take your browser to find your location, you just know that when it does, the browser will call your function back with your position.

Unlike with windo w.o nlo ad , we specify this callback by passing the get Lo cat io n() function to the

get Current Po sit io n() method. The get Current Po sit io n() method calls get Lo cat io n() (behind the scenes) as soon as the browser has retrieved your location. In get Lo cat io n() we have a valid position, so we add the position, as a latitude and longitude, to the web page. (If you get an error retrieving your position, then get Lo cat io n() won't be called; it's only called if the browser can find you).

Calling Functions: Pass-by-Value

In this lesson we've seen quite a few examples of functions, and we've passed a variety of different values to functions, including numbers, strings, and other functions. Let's take a closer look at what happens when we pass arguments to functions. Create a new file and add this code:

![](Image00041.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Functions: Pass by value </title>

<meta charset="utf-8">

<script>

function changeNum(num) {

num = 3;

}

var myNum = 10;

changeNum(myNum);

console.log(myNum);

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as f unct io ns5 .ht ml , and ![](Image00021.jpg) . Open the console.

You see the value 10 . Is that what you expected? When you pass myNum to the function changeNum() , the parameter num gets a copy of the value of myNum . When you change num to 3, you don't change the value of myNum .

This process of copying a value into a parameter when you pass an argument to a function is called pass-by-value .

Now add this code to the program:

![](Image00156.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Functions: Pass by value </title>

<meta charset="utf-8">

<script>

function changeNum(num) {

num = 3;

}

var myNum = 10;

changeNum(myNum);

console.log(myNum);

function changeObj(obj) {

obj.x = 3;

obj.z = 10;

}

var foo = {

           0,

           1

};

console.log("Before calling changeObj, foo is: "); console.log(foo);

changeObj(foo);

console.log("After calling changeObj, foo is: "); console.log(foo);

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) and ![](Image00021.jpg) . You see this output (or something similar; ours is from Chrome):

![](Image00104.jpg)

OBSERVE:

Before calling changeObj, foo is:

Object {x: 0, y: 1}

After calling changeObj, foo is:

Object {x: 3, y: 1, z: 10}

In the new code, we create an object f o o , which has two properties: f o o .x and f o o .y . We pass the object f o o to the function changeObj() , and the object is bound to the parameter o bj . The function sets the value of the property o bj.x to 3, and the value of the property o bj.z to 10 .

After we call changeObj() , passing f o o to the function, the properties of f o o are different. JavaScript is pass-by- value, which means that function parameters get a copy of the value of the arguments we pass to the function. So how are the properties of f o o being changed?

The value in the variable f o o is a reference —that is, a memory location, a pointer to the data in the object. When we pass f o o to changeObj() , we pass a copy of the memory location , not a copy of the data in the memory location. So o bj (the parameter) is also a memory location, one that points to the same place as f o o . When you change property values, or add new properties to o bj , you are making those changes and additions to f o o , because they are pointing to the same object.

![](Image00157.jpg)

This concept of pass-by-value can be a little tricky at first, so spend some time looking over this code to make sure you understand it. Experiment on your own. Try passing an array to a function that changes the array. Remember that arrays are objects too . Do you get the results you expect?

Return

Before we finish up this lesson, let's talk about the ret urn statement. ret urn is used to return a value from a function. However, if you don't have a ret urn statement, the function still returns a value: undef ined (unless you're using the function as a constructor, in which case it returns an object).

You might think that return would always be the last statement in the body of your function, but it doesn't have to be. You can use return to exit from a function early. Create a new file and add the code below, so we can see how that works:

![](Image00158.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Functions </title>

<meta charset="utf-8">

<script>

function getWeather(temp) {

if (temp >= 80) {

return "It's hot!";

} else if (temp >= 50 && temp < 80) { return "It's nice!"; console.log("test");

} else {

return "It's cold!";

}

}

var returnValue = getWeather(71);

console.log(returnValue);

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as f unct io ns6 .ht ml , and ![](Image00021.jpg) . In the console, you see the message "It's nice," but you won't see the message "test." We return a string from the get Weat her() function, and then display that value in the console. So ret urnValue holds the value returned from the function. Notice that we've got three ret urn statements in the function now. As soon as any one of them is executed, the function returns, so any code that follows the return statement will be ignored. When we return the string, "It's nice," the function execution stops, so we never see the message "test" in the console.

When you return a value from a function, write your return statement with care. Change your code just a tiny bit as shown:

![](Image00159.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Functions </title>

<meta charset="utf-8">

<script>

function getWeather(temp) {

if (temp >= 80) {

return "It's hot!";

} else if (temp >= 50 && temp < 80) { return "It's nice!";

return

"It's nice!"; console.log("test");

} else {

return "It's cold!";

}

}

var returnValue = getWeather(71);

console.log(returnValue);

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) and ![](Image00021.jpg) . Now all you see in the console is undef ined ; you don't see the message, "It's nice!"

Usually you can add whitespace in a JavaScript program without affecting the way the program executes, but in this case, the function is no longer working as we expect.

This is an example of "automatic semicolon insertion" and it's a holdover from when people used to write

JavaScript without using semicolons. JavaScript reads the above code like this:

![](Image00043.jpg)

OBSERVE:

return ;

"It's nice!";

JavaScript thinks you forgot a semicolon at the end of the return statement, so it "helpfully" insert some

for you , and in the process breaks your code. There is no error because "It's nice" is a valid expression and statement (it doesn't do a whole lot, but it's perfectly valid). So, your function returns when it hits the statement ret urn; and, because you're returning with no value, the value returned from the function is undefined . The statement "It 's nice"; never gets executed (and even if it did, as a standalone statement, it wouldn't do anything visible).

The ret urn statement is not the only situation where JavaScript does automatic semicolon insertion, but it's [a common cause of errors, so watch out for it! You can read more about automatic semicolon insertion in the](http://www.ecma-international.org/ecma-262/5.1/#sec-7.9) [JavaScript specification (5.1) .](http://www.ecma-international.org/ecma-262/5.1/#sec-7.9)

Take a break to rest your brain, and then tackle the quizzes and projects to digest all of this new information.

Scope

![](Image00005.jpg)

Lesson Objectives

When you complete this lesson, you will be able to:

use local scope and global scope.

![](Image00006.jpg)

use functions to create local scope.

![](Image00006.jpg)

recognize variables that are hoisted within a function.

![](Image00006.jpg)

use nested functions.

![](Image00006.jpg)

explore lexical scoping within nested functions.

![](Image00006.jpg)

use a scope chain to recognize how variables are resolved.

![](Image00006.jpg)

use the Chrome Developer Tools to inspect the scope chain.

![](Image00005.jpg) ![](Image00006.jpg)

Scope

To truly understand functions, and JavaScript in general, you need to understand scope. JavaScript has two kinds of scope: global , meaning a variable is visible everywhere, and local , meaning the variable is visible only within a function. You're most likely using JavaScript in the browser, so you know that the global scope comes set up with an object, windo w , which exposes all the browser -related JavaScript features you need to create web applications. In this lesson, we'll dive into scope; we'll take another look at how variables and functions work from the perspective of scope, JavaScript's scoping rules, and how to plan your code to avoid certain "gotchas ." We'll also use Chrome's web developer tools to inspect the function call stack and get a first-hand look at scope in action. Let's get going!

Variable Scope

We'll start by looking at the global scope . Here are three ways to create a global variable:

![](Image00044.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Global Scope </title>

<meta charset="utf-8">

<script>

var globalScope1 = "Global";

//

           not using var to define a new variable is bad form!

globalScope2 = "Global";

function f() {

globalScope3 = "Global";

}

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as glo balSco pe .ht ml , and ![](Image00021.jpg) . Open the console, and see which of the variables is defined globally:

![](Image00089.jpg) INTERACTIVE SESSION:

globalScope1

"Global"

globalScope2

"Global"

globalScope3

ReferenceError: globalScope3 is not defined

Both glo balSco pe1 and glo balSco pe2 are global variables, so you can inspect them in the console, but we haven't called the function f () , so glo balSco pe3 hasn't yet been created. Call f () and then check again:

![](Image00060.jpg)

INTERACTIVE SESSION:

f() undefined

globalScope3

"Global"

Now, glo balSco pe3 is defined, and it is a global variable. Why is glo balSco pe3 a global variable? After all, we defined it inside the function f () . Well, notice that we did not use var to declare the variable. When you use a new variable in a function without using the keyword var , JavaScript automatically creates a new global variable for you. This can be a problem if you're not expecting it! For instance, you could accidentally overwrite the value of an existing global variable if you use the same name and forget to write var . So, avoid using new variable names within a function to create global variables. In general, always declare your variables with var , whether they are global or local.

The term global scope describes the visibility of your variables. Global variables are visible everywhere in your JavaScript code, including in external files if you are loading external scripts. So smart JavaScript programmers try to avoid global variables except when they're absolutely necessary.

Global variables are added to the global object , which is the windo w object in all current browsers. Type windo w in the console:

![](Image00067.jpg)

INTERACTIVE SESSION:

window

Window {top: Window, window: Window, location: Location, external: Object, chrom

e: Object}

You see the window object and its many methods and properties. In Chrome, Safari, and Firefox, if you click the arrow next to the object in the console, you'll see some familiar methods and properties. Scroll down to the properties starting with lower case "g" and look for the global variables you defined in the code above. You see all three properties there. Scroll back up to the "f"s and you see the function f () we defined.

Whenever you define a global variable, it's added to the global object as a property.

When you use a global variable or method, whether it's one you define yourself (like the global variables we created above) or properties of the global object (like alert () , co nso le .lo g() , or do cument , the document object), you don't have to specify windo w.alert () , or windo w.glo balSco pe1 ; you can just type the name, for instance, alert () or glo balSco pe1 . The global object is the default scope for all variables.

![](Image00060.jpg)

INTERACTIVE SESSION:

window.globalScope1

"Global"

globalScope1

"Global"

Both work, so we usually just leave off the "window" part.

Function Scope

The other kind of scope in JavaScript is local scope . A local scope is created whenever you call a function:

![](Image00160.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Local Scope </title>

<meta charset="utf-8">

<script>

var message = "Loading...";

window.onload = function() {

var message = "Done loading";

var div = document.getElementById("container"); div.innerHTML = message;

}

</script>

</head>

<body>

<div id="container"></div>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as lo calSco pe .ht ml , and ![](Image00021.jpg) . You see the message "Done loading" in the web page. Open the console and try to access the variables:

![](Image00060.jpg)

INTERACTIVE SESSION:

       message "Loading..."

        div

ReferenceError: div is not defined

We can access the globally defined variable message , but not the locally defined variables message and div . Plus, we've got two variables with the same name. The message that's defined inside the (anonymous) function is a local variable, while the message defined above the function is a global variable. Similarly, the variable div is a local variable.

Inside the function, we set the innerHT ML property of the div object to the value of the local message variable (the one that is defined in the function) because the local message variable shadows the global message variable. If you use a local variable with the same name as a global variable, the local variable is used when you refer to it within the same function.

Parameters also have local scope. Let's change the code a bit so we can see how this works:

![](Image00161.jpg) CODE TO TYPE:

var message = "Loading...";

window.onload = function() {

var message = "Done loading";

var div = document.getElementById("container"); div.innerHTML = message; updateMessage(message);

}

function updateMessage(msg) {

console.log(message);

console.log(msg);

var div = document.getElementById("container"); div.innerHTML = msg;

}

![](Image00042.jpg) and ![](Image00036.jpg) . In the console, you see two messages:

![](Image00043.jpg)

OBSERVE:

Loading...

Done loading

The first parameteris from the line co nso le .lo g(message) . The value in the global variable message is displayed, not the value defined in the windo w.o nlo ad function, even though we're calling

updat eMessage() from that function. Also, we're passing the value of the local variable message from that function to updat eMessage() , but giving it a new name as a parameter, msg . Remember that when you call a function and pass an argument, the parameter of the function gets a copy of the argument value, so msg gets a copy of the string "Done loading." That's the second message you see in the console, and it's also the message you see in the <div> in the web page.

msg is a local variable; it's local to the function updat eMessage() . Try to display the value of msg in the console:

![](Image00049.jpg)

INTERACTIVE SESSION:

        msg

ReferenceError: msg is not defined

You can't access a local variable outside the function in which it is defined.

You might be curious about how variable shadowing works . And if there's a global object into which all the global variables are stashed, is there also a local object for local variables? We'll come back to these topics shortly, when we talk about sco pe chains .

Hoisting

We've talked about the two kinds of scope that JavaScript has: global and local. Let's take a closer look at local scope, because sometimes local scope behaves in ways you might not expect, particularly if you have blocks of code in a function, and you're defining new variables within those blocks . By "block," we mean perhaps a loop or an if statement, where the "block" consists of all the statements inside the body of the loop or if statement (everything between the curly brackets {}):

![](Image00162.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Hoisting </title>

<meta charset="utf-8">

<script>

var icecream = ["vanilla", "chocolate", "strawberry"]; function init() {

var flavorButton = document.getElementById("getFlavorButton"); flavorButton.onclick = checkFlavor;

}

function checkFlavor() {

console.log(flavor);

if (icecream.length > 0) {

var div = document.getElementById("container");

var flavor = document.getElementById("flavor").value; if (flavor) {

for (var i = 0; i < icecream.length; i++) {

if (icecream[i] == flavor) {

var found = true;

div.innerHTML = "We have " + flavor;

break;

}

}

if (!found) {

div.innerHTML = "Sorry, we don't have " + flavor;

}

}

}

console.log(flavor);

}

window.onload = init;

</script>

</head>

<body>

<div id="container">Enter a flavor of ice cream you'd like: </div> <form>

<input type="text" id="flavor">

<input type="button" id="getFlavorButton" value="Check flavor"> </form>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as ho ist ing.ht ml , and ![](Image00021.jpg) . You see a message asking you to enter an ice cream flavor, a form input to enter the flavor, and a button to submit the form.

Before you submit the form, take a close look at the code and make sure you understand how it works:

![](Image00163.jpg) OBSERVE:

var icecream = ["vanilla", "chocolate", "strawberry"]; function init() {

var flavorButton = document.getElementById("getFlavorButton"); flavorButton.onclick = checkFlavor ;

}

function checkFlavor() {

console.log(flavor);

if (icecream.length > 0) {

var div = document.getElementById("container");

var flavor = document.getElementById("flavor").value; if (flavor) {

for (var i = 0; i < icecream.length; i++) {

if (icecream[i] == flavor) {

var found = true;

div.innerHTML = "We have " + flavor;

break;

}

}

if (!found) {

div.innerHTML = "Sorry, we don't have " + flavor;

}

}

}

console.log(flavor);

}

We set up a click handler f o r t he f o rm but t o n t hat will call t he checkFlavo r() f unct io n when you click the button. In the checkFlavo r() function we use a variable named f lavo r to hold the value you'll enter into the form. Look at where that variable is defined in the function; we display its value in the console twice: once at the top of the function, before the f lavo r variable is defined, and once at the end of the function, just before the function finishes, and outside the if blo ck in which f lavo r is defined.

What do you think you'll see in the console when you run this code by entering an ice cream flavor and clicking the button?

Okay, make sure your console is open, and enter "vanilla." You see the message "We have vanilla" in the page. Check out the values displayed in the console.

![](Image00043.jpg)

OBSERVE:

undefined

vanilla

The first co nso le .lo g(f lavo r) displays undef ined , while the second co nso le .lo g(f lavo r) displays vanilla .

You might have expected to get an error for the first co nso le .lo g(f lavo r) call, because the f lavo r variable hasn't been defined yet, and usually when you try to access a variable that isn't defined, you get a Reference Error. (If you need to refresh your memory about Reference Errors, just go back to the console and enter the name of a variable that's not defined by this program, like x.)

Why don't we get a Reference Error when we try to access f lavo r before it's been defined, or after the block that encloses the definition of f lavo r has ended? The answer is: hoisting . Hoisting is an informal name for a quirky behavior in JavaScript: no matter where you define a variable within a function, the variable declaration is moved (or "hoisted") up to the top of the function. Read that again. Notice that only the declaration is moved; not the initialization. So, it's as if you'd written the checkFlavo r() function like this:

![](Image00115.jpg) OBSERVE:

function checkFlavor() {

var flavor;

console.log(flavor);

if (icecream.length > 0) {

var div = document.getElementById("container");

var flavor = document.getElementById("flavor").value; if (flavor) {

for (var i = 0; i < icecream.length; i++) {

if (icecream[i] == flavor) {

var found = true;

div.innerHTML = "We have " + flavor;

break;

}

}

if (!found) {

div.innerHTML = "Sorry, we don't have " + flavor;

}

}

}

console.log(flavor);

}

flavor is declared when we access it in the first co nso le .lo g(f lavo r); . It's declared, but it's not initialized, so the value of flavor is undef ined . That's why you see undef ined as the result of the first

co nso le .lo g(f lavo r); . Then, we set its value to the value you type into the form, and that remains the value when we reach the second co nso le .lo g(f lavo r); .

Hoisting take place for all the local variables in checkFlavo r() . Can you find the other variables in the function that are hoisted?

If you have experience with another language, perhaps Java or C#, this hoisting behavior may surprise you, because many languages have a third type of scope: block scope. In block scope, a variable like f lavo r would be defined only within the block where it's declared and initialized, and not outside that block. In that case, you would get a reference error if you tried to access f lavo r in the two co nso le .lo g(f lavo r); statements. However, JavaScript does not have block scope. It only has global and local scope. All local variables are visible everywhere within a function, even if they are declared and initialized within a block.

![](Image00034.jpg)

| Note | As of this writing, JavaScript does not have block scope, but it will probably be added at some |
| point. |
|  |

![](Image00018.jpg)

Nested Functions

Sometimes in JavaScript, we nest functions inside other functions. Usually these are "helper" functions that are used only by the function enclosing the nested functions. Let's take a look at an example, and then talk about how scope works for nested functions.

![](Image00164.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Nested Functions </title>

<meta charset="utf-8">

<style>

.red {

background-color: red;

}

.blue {

background-color: lightblue;

}

.pink {

background-color: pink;

}

</style>

<script>

window.onload = function() {

var theId = "list";

findElement(theId);

}

function findElement(id) {

var color = "red";

var el = document.getElementById(id);

if (el) {

changeAllBlueChildren(el);

}

function changeAllBlueChildren(el) {

for (var i = 0; i < el.childElementCount; i++) { var child = el.children[i];

if (child.tagName.toLowerCase() == "li") {

var theClass = child.getAttribute("class");

if (theClass == "blue") {

child.setAttribute("class", color);

}

}

}

}

}

</script>

</head>

<body>

<ul id="list">

<li class="red">I'm already red</li>

<li class="blue">I'm blue</li>

<li class="blue">I'm blue too</li>

<li class="pink">And I'm pink</li>

</ul>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as nest ed.ht ml , and ![](Image00021.jpg) . The first three items in the list are red, and the last one is pink. In the HTML and CSS, the second and third items are in the "blue" class, so normally the background of those items would be "lightblue," but we changed that using the code.

![](Image00165.jpg)

In the code, you can also see that we have a windo w.o nlo ad function that is called when the page is loaded; that function calls f indElement () , which finds the element with the id "list," and calls changeAllBlueChildren() . changeAllBlueChildren() iterates through all of the child elements of the list (all the <li> elements), and if the class of the element is "blue," changeAllBlueChildren() changes the class to "red."

![](Image00166.jpg)

OBSERVE:

function findElement(id) {

var color = "red";

var el = document.getElementById(id);

if (el) {

changeAllBlueChildren(el);

}

function changeAllBlueChildren(el) {

for (var i = 0; i < el.childElementCount; i++) { var child = el.children[i];

if (child.tagName.toLowerCase() == "li") {

var theClass = child.getAttribute("class");

if (theClass == "blue") {

child.setAttribute("class", color);

}

}

}

}

}

Here we're exploring nested functions. The f indElement () function has a nest ed f unct io n in it: a function defined within a function. Unlike global functions like f indElement () and windo w.o nlo ad function, changeAllBlueChildren() is a local function, visible only within f indElement () . If you try to access the function in the console (or try to call it from outside of the f indElement () function), you'll get a reference error:

![](Image00049.jpg)

INTERACTIVE SESSION:

changeAllBlueChildren

ReferenceError: changeAllBlueChildren is not defined

Essentially, changeAllBlueChildren() is hidden except within f indElement () . (We'll come back to the concept of data hiding later in the course).

We're using a function declaration to declare the changeAllBlueChildren() function. What do you think would happen if we changed the code to declare the function using a function expression instead?

![](Image00167.jpg)

CODE TO TYPE:

function changeAllBlueChildren(el) {

var changeAllBlueChildren = function(el) {

...

}

![](Image00087.jpg) and ![](Image00036.jpg) .

![](Image00076.jpg)

OBSERVE:

> Uncaught TypeError: undefined is not a function

Just like other local variables in a function, the changeAllBlueChildren variable is hoisted . So now, changeAllBlueChildren is implicitly declared at the top of the function but is undefined (just like all the other local variables). Since we don't assign the function expression to the variable until after we call the function, we get an error. We're trying to call the variable changeAllBlueChildren while it's still undefined, and before it is assigned the function expression.

Go ahead and change your code back to use a function declaration instead. The function declaration is also defined after we call the function, but, unlike a function defined with a function expression, a nested function declaration is visible throughout the function in which it's nested. This is similar to the way functions declared at the global level work: you can put them at the bottom of your code, but access them anywhere in your code. Here, we've placed the changeAllBlueChildren function declaration at the bottom of the f indElement () function, but now (using a function declaration rather than a function expression) it's visible (and defined!) throughout the f indElement () function.

Lexical Scoping

Now let's take a look at what happens to the scope of variables when you have nested functions. Remember earlier we said local variables are visible throughout the function in which they are declared. Let's see where the variables in this program are visible.

![](Image00168.jpg)

OBSERVE:

window.onload = function() {

var theId = "list";

findElement( theId );

}

function findElement( id ) {

var color = "red";

var el = document.getElementById( id );

if ( el ) {

changeAllBlueChildren( el );

}

function changeAllBlueChildren( el ) {

for (var i = 0; i < el .childElementCount; i++) { var child = el .children[i];

if (child.tagName.toLowerCase() == "li") {

var theClass = child.getAttribute("class");

if (theClass == "blue") {

child.setAttribute("class", color );

}

}

}

}

}

We'll start with t heId . This variable is defined in the windo w.o nlo ad or in f indElement () . However, we pass it to f indElement () , which

function, and so is not visible globally gets a copy of its value, in the parameter

variable id . id is local to f indElement () , so we can access it anywhere in that function, but again, not globally. Similarly, co lo r and el are local variables, visible anywhere in f indElement () .

Next, look at changeAllBlueChildren() . We have a parameter, el , and several local variables, including i , child , and t heClass , all of which are local to changeAllBlueChildren() .

There's some interesting stuff happening here. We're using the variable co lo r inside changeAllBlueChildren() , even though co lo r is not defined in changeAllBlueChildren() , and it's not a global variable. This is possible because changeAllBlueChildren() is nested within f indElement () , co lo r is visible inside the nested function, so we can access it just as if it were a local (or global) variable inside changeAllBlueChildren() . This is known as lexical scoping . That means, when you are using a variable, like co lo r , you figure out the value of the variable by first looking in the local scope (that is, in changeAllBlueChildren() ), and then in the next outer scope. Typically, the next outer scope is the global scope, but in this case, because changeAllBlueChildren() is nested within another function, the next outer scope is f indElement () . That's where co lo r is defined, so that's the value we use in changeAllBlueChildren() .

Take a look at el . We have the parameter, el , which is local to changeAllBlueChildren() , and we have the variable el in f indElement () which is visible throughout f indElement () , including within changeAllBlueChildren() ! So which value do we use? Well, remember that the el defined within changeAllBlueChildren() will shadow the el in f indElement () . How? Because of lexical scoping. When we use el in changeAllBlueChildren() , we first look for it in the local scope, and we find its value there, so that's the one we use.

If you don't find a variable within a local scope at all, then you look in the global scope. If it's not there, you get a Reference Error.

![](Image00169.jpg)

Well, we've talked about how functions are good for organizing bits of code. That's what we're doing here. We put all the code related to changing the blue children of an element to red in this function, which makes the code easier to read and understand, and also creates a chunk of code that's easy to reuse. In this case, we only call the changeAllBlueChildren() once, but you can imagine that we might end up calling it multiple

times . By nesting the function inside f indElement () , we keep it hidden from other code that doesn't need to know about it, and organize our code so that the related bits are together. If we wanted to use changeAllBlueChildren() somewhere else in our code, we'd have to move it out of f indElement () so it would be accessible to other code to call.

There is a downside to nested functions: a nested function like changeAllBlueChildren() has to be recreated every time you call the function in which it's nested, while functions defined at the global level are created only once and stick around for the duration of your program. In our case, that's okay; we call

f indElement () just once, so we're creating changeAllBlueChildren() just once. In small to medium -sized programs, you might find that the organizational benefit of nested functions outweighs the performance hit. However, if you're building an application that needs to be as fast as possible, you'll want to avoid nested functions.

Scope Chains

You know that JavaScript has two kinds of scope: global and local. You also know that scope works "lexically." When you are looking to resolve a variable (determine what its value is when you use it), first you look in the local scope of the function you're in, if you don't find it, you look in the surrounding scope, and so on, until you get to the global scope. If you don't find the variable in any of those places, you get an error.

The way scope works behind the scenes is through a scope chain . A scope chain is created in two stages: the first stage is when the function is defined, and the second, when the function executes. When you define a function, the initial scope chain is created. You can think of the scope chain as a list of pointers from the function to the scopes that surround the function at define time. These scopes are in order, so that the scope at the top of the chain (the first position) is the scope immediately surrounding the function (usually the global scope, unless the function is nested), and subsequent scopes are further out (like the layers in the previous diagram).

In the second stage, when the function executes, an activation object is created. This object represents the state of the function as it executes, so it contains all the local variables, as well as t his (which is usually the global object, windo w) . The activation object is added to the top (the first position) of the scope chain. When a function is executing and it comes across a variable and needs to resolve that variable to know what the value is, the function starts at the first position in the scope chain, which is the activation object. If the function finds the variable there (that is, the variable is a local variable to the function), it stops there, and uses that value. If the function doesn't find the variable there, it looks in the next position in the scope chain, and so on. The function continues down the chain until it finds a scope that contains the variable. If it gets to the end—the global scope is always the last stop in the chain—and hasn't found the variable, then we get a Reference Error.

Let's take a look at the scope chains for the functions in our specific example. The windo w.o nlo ad function is defined at the top level, so its define-time scope chain is the global object. When windo w.o nlo ad is called (by the browser, when the page is loaded), an activation object is added to the top of the scope chain. So, when we look for the value of the variable t heId , we find it in the activation object, and don't have to look any further down the chain.

![](Image00170.jpg)

Similarly, f indElement () is globally defined, so at define time, the global object is added to the scope chain, and at execution time—when we call the function—the activation object is added to the chain. That's where we look first to find the values of the variables used in the function, like id and el , as well as do cument .

do cument is not defined in the activation object, so we look in the global object and find do cument there.

![](Image00171.jpg)

When we call f indElement () , changeAllBlueChildren() is defined. At define time, we have an extra scope object in the chain: the f indElement () scope object. Because changeAllBlueChildren() is defined within the f indElement () function, it's defined in the f indElement () function's scope. The extra scope object contains any variables that are referenced from the nested function. In this case, that's just the co lo r variable. When we call changeAllBlueChildren() , its activation object is added to the chain. When we look for the variable co lo r , first we look in the activation object, but since we don't find it there, we look in the f indElement () scope, find it, and o we stop looking.

![](Image00172.jpg)

Inspecting the Scope Chain

You can use the Chrome developer tools to see the scope chain in action as your code runs. Make sure you have the file nest ed.ht ml loaded into a browser page and the console window open in the Chrome browser (unfortunately, the other browsers' built-in tools don't offer the same capability yet, so you'll need Chrome to follow along).

Click the So urces tab. If you don't see anything in the left panel in the console, click the small right-pointing Sho w Navigat o r arrow at the top left of the console and select your file, nest ed.ht ml . Once you do that, you see the source code of the file:

![](Image00173.jpg)

In the panel on the right side, make sure you have the Call Stack, Scope Variables, and Breakpoints sections open (the arrows next to them are pointed down).

Now, add breakpoints to your code. A breakpoint is a way to tell the browser to stop executing your code at a certain point. You add a breakpoint by clicking on one of the line numbers in the far left side of the left panel. When you add a breakpoint, you'll see a little blue marker indicating the line of code where the breakpoint is located. Add three breakpoints: one on the line where we call f indElement () in windo w.o nlo ad ; one on the line where we call changeAllBlueChildren() in f indElement () , and one at the very bottom of changeAllBlueChildren() (the closing curly brackets for the function, which is the second to last curly bracket in the file). Look in the panel on the right, under Breakpoints, to verify that you've clicked on the correct lines.

![](Image00174.jpg)

Now, reload the page. Don't worry, your breakpoints will stay in place. When you do, you see a "Paused in debugger" message in the web page at the top, and the line of code at the first breakpoint is highlighted which indicates that the execution has paused at that line:

![](Image00175.jpg)

In the Call Stack section in the panel on the right, you see windo w.o nlo ad . That's because we called windo w.o nlo ad , and we paused execution just before we call f indElement () . Now, look at the Scope Variables section. This is the scope chain. At the top of the chain is the local scope; you can see the local variables defined there, including t heId and t his . Next you see the global scope, with all of its usual content (you can open it up to see, but it contains many properties, so be sure and close it when you're finished).

Now, we want to continue the execution of the code until we hit the next breakpoint. Click the small button that looks like a "play" button ( Resume script execut io n ) at the top left of the right panel. When you click this button, execution resumes, until it hits the next breakpoint located at the line where we call changeAllBlueChildren() :

![](Image00176.jpg)

Again the execution stops just before we call the function, so we can inspect the call stack and the scope variables. Notice under Call Stack in the panel on the right, we now have f indElement () on top, and windo w.o nlo ad below. That means that we called f indElement () from windo w.o nlo ad . Now look at the Scope Variables . The top part of the scope chain includes the local variables defined by f indElement () . Below that is the global scope. Before you move on, notice that the second and third items in the list are still blue because we haven't called changeAllBlueChildren() yet!

Continue the code execution by clicking the Resume script execut io n button. Now the execution stops on the very last line of the changeAllBlueChildren() function—on the curly brace, at the moment just before this function returns.

![](Image00177.jpg)

Now the second and third items in the list are red. Notice the Call Stack; you can see that change All Blue Children() is at the top. We called change All Blue Children() from find Element () , which we called from windowonlo ad (the Call Stack is useful for tracking which functions are calling which!).

Look at the Scope Variables. You see that the local variables for the change All Blue Children() function at the top of the scope chain. Below that is something called Closure . This is the scope chain object for the

findElement () scope, containing the co lo r variable. Twirl down (click so it's pointing downward) the arrow next to Closure so you can see it. (We'll explain why it's called Closure in another lesson). Then, at the bottom of the scope chain is the global scope.

Click Resume script execution one more time to continue execution and complete the code execution. The page returns to normal. Your breakpoints are still there (they will stay there until you delete them) so if you want to do this again, you can simply reload the page and go through the same steps. To remove the

breakpoints, click the blue markers and they will disappear. Once you've removed the breakpoints, if you reload the page, the page will behave as it usually does, and execute the code all the way through with no stops.

In this lesson, you learned all about scope, including the details of how it works with the scope chain. Nested functions, sometimes called "inner functions," create additional levels in the scope chain, so we explored how to create nested functions and how scope works when you have a nested function. Lexical scoping is a rule that lets us find the correct value of a variable to use by looking in each level of the scope chain, from the top (first) position, to the bottom position (always the global scope).

Invoking Functions

![](Image00005.jpg)

Lesson Objectives

When you complete this lesson, you will be able to:

call a function as a function.

![](Image00006.jpg)

call a function as a method.

![](Image00006.jpg)

call a function as a constructor.

![](Image00006.jpg)

call a function with apply() and call().

![](Image00006.jpg)

use t his when we call functions in different ways.

![](Image00006.jpg)

compare how t his is defined in nested functions with how it is defined in global functions.

![](Image00006.jpg)

control how t his is defined with apply() and call().

![](Image00006.jpg)

use the argument s object to create functions that support a variable number of arguments.

![](Image00005.jpg) ![](Image00006.jpg)

Invoking Functions

In JavaScript we call, or invoke , functions in many different ways . We call built-in functions, we create and call our own functions, we use functions as constructors, we call methods in objects, and more. In this lesson, we'll look at all the different ways we can call functions, and the reasons we use each.

![](Image00178.jpg)

Note Invoke is just another word for call . We'll use both terms interchangeably throughout the lesson.

![](Image00179.jpg)

Different Ways to Invoke Functions

By now, you are familiar with how to call functions in JavaScript. It's difficult to write a script without calling at least one function. Perhaps you're calling a built-in function, like alert , or a function you've written yourself, or one that's supplied by a JavaScript library (like jQuery). Let's look at an example that has a couple of different kinds of function calls:

![](Image00044.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Calling a function </title>

<meta charset="utf-8">

<script src="http://code.jquery.com/jquery-latest.min.js"></script> <script>

function callMeMaybe(number) {

return "Call me at " + number;

}

window.onload = function() {

var number = callMeMaybe("555-1212");

$("body").append("<div>" + number + "</div>");

alert("Content added");

}

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as f unct io nCalls.ht ml , and ![](Image00085.jpg) . You see the text "Call me at 555-1212" in the page, and an alert with the text, "Content added."

Here we see examples of two of the four different ways you can invoke functions in JavaScript:

as a f unct io n

![](Image00006.jpg)

as a met ho d

![](Image00006.jpg)

as a constructor (we'll get to this later)

![](Image00006.jpg)

with apply() or call() (we'll get to this later too)

![](Image00006.jpg)

First, we create and invoke our own function, callMeMaybe() , as a function (that is, callMeMaybe() is a regular function that we call in the normal way we call functions). We also call a function supplied by jQuery,

    () (which is shorthand for the jQuery() function—and yes, $ is a valid name for a function). Again, we call the $ () function as a function.

The second way to invoke a function is as a method. There are two method calls in this example:

    ("bo dy").append() and alert () . append() is a method of the jQuery object returned from the $ () function. We use "dot notation" to call it, as we would any method.

So what about alert () ? Well, remember earlier in the course, we said that built-in JavaScript functions like alert () are actually methods of the global windo w object, which is the default object used to run JavaScript programs in the browser. Because it's the default object, if you don't specify it for methods and properties (like with our call to alert () ), JavaScript assumes you mean windo w.alert () . So calling alert () is actually a method call, not a function call.

There's actually a third method call implied in this code. Can you find it? It's the function assigned to the windo w.o nlo ad property. We don't call this method ourselves; the browser is calls it for us when the page has completed loading.

An important distinction between calling a function as a function and as a method is that (most of the time) you need to use the dot notation to call a method. You specify the name of the object, like windo w , and the name of the method, like alert () , and separate the two with a dot (period) to get windo w.alert () . To call a function, you use the function name.

Let's look at the third way to call a function:

![](Image00180.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Calling a function as a constructor </title>

<meta charset="utf-8">

<style>

.square {

background-color: lightblue;

cursor: pointer;

}

.circle {

background-color: orange;

cursor: pointer;

}

.square p, .circle p {

padding-top: 35%;

text-align: center;

-webkit-user-select: none;

-moz-user-select: none;

-ms-user-select: none;

user-select: none;

}

</style>

<script>

function Square(id, name, size) {

this.id = id;

this.name = name;

this.size = size;

this.display = function() {

var el = document.getElementById(this.id); el.style.width = this.size + "px"; el.style.height = this.size + "px"; el.innerHTML = "<p>" + this.name + "</p>"; console.log(this.name + " has size " + this.size +

", and is a " + this.constructor.name);

};

}

window.onload = function() {

var square = new Square("s1", "square one", 100); square.display();

}

</script>

</head>

<body>

<div id="s1" class="square"></div>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as co nst ruct o rCall.ht ml , and ![](Image00085.jpg) . A light blue square with the text "square one" appears in the page. In the console, you see the message "square one has size 100, and is a Square."

As we mentioned in the lesson on constructing objects, when you invoke a function with the new keyword, you are calling that function as a constructor rather than as a function. So here, when we invoke the Square() function with new Square(...) , we're invoking that function as a constructor.

Constructors create an object, which we can reference with the t his keyword to assign it property values, and that object is returned automatically by the constructor. Any function can be invoked as a constructor (although if you invoke a function not designed specifically as a constructor with new , you probably won't get a useful object back). As convention dictates, we begin constructor functions' names with an uppercase letter to distinguish these functions from regular functions.

Many objects have methods as properties. We create the Square object with the Square() constructor, so you can see here an example of invoking a function as a method, too: square .display() .

The fourth, and final, way to invoke a JavaScript function is indirectly, using the function object's call() and apply() methods . You haven't seen these methods yet, so we'll spend a significant amount of time on the subject here. The main reason to use these methods is to control how t his is defined, so first we'll talk about what happens to t his in each of the ways we invoke functions.

What Happens to this When You Invoke a Function

The rules for how t his is defined when you invoke a function depend on how you invoke the function and the context in which you invoke it. Let's take a look at some examples. We'll modify the previous example of the Square constructor to illustrate. Copy the previous file to a new file, t his.ht ml , and modify it as shown:

![](Image00125.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> What happens to this? </title>

<meta charset="utf-8">

<style>

.square {

background-color: lightblue;

cursor: pointer;

}

.circle {

background-color: orange;

cursor: pointer;

}

.square p, .circle p {

padding-top: 35%;

text-align: center;

-webkit-user-select: none;

-moz-user-select: none;

-ms-user-select: none;

user-select: none;

}

</style>

<script>

var n = 0;

function Square(id, name, size) {

console.log("This at the top of the Square constructor: "); console.log(this);

this.id = id;

this.name = name;

this.size = size;

this.display = function() {

console.log("This in the Square's display method: "); console.log(this);

var el = document.getElementById(this.id); el.style.width = this.size + "px"; el.style.height = this.size + "px"; el.innerHTML = "<p>" + this.name + "</p>"; console.log(this.name + " has size " + this.size +

", and is a " + this.constructor.name);

};

console.log("This at the bottom of the Square constructor: "); console.log(this);

}

window.onload = function() {

console.log("This in window.onload: ");

console.log(this);

var square = new Square("s1", "square one", 100); setupClickHandler(square);

square.display();

}

function setupClickHandler(shape) { console.log("This in setupClickHandler: "); console.log(this);

var elDiv = document.getElementById(shape.id); elDiv.onclick = function() {

console.log("This in click handler: ");

console.log(this);

n++;

var counter = document.getElementById("counter_" + shape.id); counter.innerHTML = "You've clicked " + n + " times.";

};

}

</script>

</head>

![](Image00181.jpg)

<body>

<div id="s1" class="square"></div>

<p id="counter_s1"></p>

</body>

</html>

![](Image00042.jpg) Save the file in your /AdvJS folder as t his.ht ml and ![](Image00036.jpg) . We added some calls to

co nso le .lo g() in several places (make sure you find them all now, because we'll refer to each of them below) We also added a whole new function, set upClickHandler() , which adds a click handler to the "s1" <div>, so that when you click on the "s1" <div> you'll see a message indicating how many times you've clicked on that <div>. Open the console (reload the page if you don't see any output), and you see messages like this:

![](Image00182.jpg)

OBSERVE:

This in window.onload:

Window {top: Window, window: Window, location: Location, external: Object, chrom

e: Object}

This at the top of the Square constructor: Square {}

This at the bottom of the Square constructor:

Square {id: "s1", name: "square one", size: 100, display: function}

This in setupClickHandler:

Window {top: Window, window: Window, location: Location, external: Object, chrom

e: Object}

This in the Square's display method:

Square {id: "s1", name: "square one", size: 100, numClicks: 0, display: function }

square one has size 100, and is a Square

Each of these co nso le .lo g() messages displays the value of t his at a particular spot in your code.

T he f irst message is from the co nso le .lo g() in the windo w.o nlo ad function. When you call the method of an object, typically, t his refers to the object. That's the case here: we called the function assigned to the windo w.o nlo ad property (and thus, that function is a method), so t his in that method is the windo w object.

T he seco nd message is from the co nso le .lo g() at the top of the Square() constructor function. Here,

t his is set to a brand new object (the one created by the constructor), and because we have yet to set any of its properties, that object is empty.

At the end of the Square() constructor, we see t he t hird message after we add properties and methods to the object being created by the constructor. In the message we see a fully constructed Square object that will be returned to the code that called new Square() .

T he f o urt h message is from the co nso le .lo g() in the set upClickHandler() , which we call just before we call square .display() . The value of t his in set upClickHandler() is also the windo w object, but for an entirely different reason. Here, t his is set to the windo w object because set upClickHandler() is a globally defined function we've created, and the context in which it is being called is the windo w object—that is, the global object. Whenever you call a globally defined function as a function, t his is set to the windo w object (unless you've set it to something else).

T he last t wo messages are from the co nso le .lo g() s in the square .display() method. t his is set to the Square object; that is the method we called from Square object.

We don't see the message in the "s1" <div> click handler yet (assuming you haven't clicked on that <div> yet; if you have, just reload the page and don't click on it so that your messages match ours).

Now, click on the "s1" <div> (by clicking anywhere on the text). More text appears in the page, "You've clicked 1 times." and in the console, you see:

![](Image00043.jpg)

OBSERVE:

>This in click handler:

<div id="s1" class="square" style="width: 100px; height: 100px;">...</div>

This is the message from the co nso le .lo g() in the function we've assigned to the o nclick property of the "s1" <div>. Because we're assigning a function to the click property of an object (an element object representing the <div>), this function is actually a method. Within that method, t his is set to the object that contains the method we're calling—that is, the "s1" <div>.

Try clicking again. Notice that we increment the global variable n each time you click in order to keep track of the total number of times you've clicked. (As an exercise, think about why n has to be a global variable here.)

So far so good; everything is pretty much as we'd expect. Now let's make a change and see what happens:

![](Image00183.jpg)

CODE TO TYPE:

...

var n = 0;

function Square(id, name, size) {

console.log("This at the top of the Square constructor: "); console.log(this);

this.id = id;

this.name = name;

this.size = size;

this.numClicks = 0;

this.display = function() {

console.log("This in the Square's display method: "); console.log(this);

var el = document.getElementById(this.id); el.style.width = this.size + "px"; el.style.height = this.size + "px"; el.innerHTML = "<p>" + this.name + "</p>"; console.log(this.name + " has size " + this.size +

", and is a " + this.constructor.name);

};

this.click = function() {

console.log("This in the Square's click method: ");

console.log(this);

this.numClicks++;

document.getElementById("counter_" + this.id).innerHTML =

"You've clicked " + this.numClicks + " times on " + this.name;

};

console.log("This at the bottom of the Square constructor: "); console.log(this);

}

window.onload = function() {

console.log("This in window.onload: ");

console.log(this);

var square = new Square("s1", "square one", 100); setupClickHandler(square); square.display();

}

function setupClickHandler(shape) { console.log("This in setupClickHandler: "); console.log(this);

var elDiv = document.getElementById(shape.id); elDiv.onclick = function() {

console.log("This in click handler: ");

console.log(this);

n++;

var counter = document.getElementById("counter_" + shape.id); counter.innerHTML = "You've clicked " + n + " times.";

};

elDiv.onclick = shape.click;

}

...

![](Image00042.jpg) and ![](Image00036.jpg) preview. We replaced the click handler for the "s1" <div> that we defined in

set upClickHandler() with a method of the square object, square .click() (we assign it to the o nclick property with shape .click in the set upClickHandler() function since we're passing the square into a paramater named shape ). Essentially the method performs the same task as the previous click handler did, except that now we keep track of the number of clicks on the book with a property of the square object, square .numClicks , rather than with a global variable.

Now try clicking on the "s1" <div> as you did before. It doesn't work! You see the text "You've clicked NaN times on the book" in the page. Recall that NaN means "Not a Number," so something went wrong with the counter. In addition, we don't see the name of the book like we should.

Look at the code for the click() method:

![](Image00123.jpg)

OBSERVE:

this.click = function() {

console.log("This in the Square's click method: ");

console.log(this);

this.numClicks++;

document.getElementById("counter_" + this.id).innerHTML = "You've clicked " + this.numClicks + " times on " + this.name ;

};

We don't see the correct values for either t his.numClicks or t his.name . Looking at the console again, you'll see that the value of t his in the click() method is the "s1" <div> object (the element object), and not the square object:

![](Image00067.jpg)

INTERACTIVE SESSION:

> This in the Square's click method:

<div id="s1" class="square" style="width: 100px; height: 100px;">...</div>

So here, the "s1" <div> object replaces the normal value of t his in the method square .click() . In fact, t his will be defined as the target element object in any function that you use as the handler for an event like "click." This behavior comes in handy when we want to access the element that was clicked in the click handler, but in this case, the behavior is treading on our expectations of what t his should be in the method of the square object.

Fortunately, there's an easy way around it. Instead of writing:

![](Image00076.jpg)

OBSERVE:

elDiv.onclick = shape.click;

we can write:

![](Image00033.jpg)

OBSERVE:

elDiv.onclick = function() {

shape.click();

}

Now, t his is set to the "s1" <div> in the outer click handler function (the anonymous function we're assigning to the o nclick property of the elDiv ), but when we call shape .click() from within that function, t his gets set to the square object that we passed into set upClickHandler() (because now we're calling the method normally, as a method of an object, rather than as an event handler). If you need the "s1" <div> object in the click handler for some reason, you could pass t his to the method:

![](Image00184.jpg) OBSERVE:

elDiv.onclick = function() {

shape.click(this);

}

...and change the click() method in the Square constructor to have a parameter to take this argument.

We don't need the "s1" <div> in the click() method, so for now, just change your code like this:

![](Image00020.jpg)

CODE TO TYPE:

...

function setupClickHandler(book) {

var elDiv = document.getElementById(shape.id); elDiv.onclick = shape.click;

elDiv.onclick = function() {

console.log("This in click handler: ");

console.log(this);

shape.click();

};

}

...

![](Image00042.jpg) and ![](Image00036.jpg) . Now the page updates correctly when you click the "s1" <div>, and in the console, you'll see that t his is set to the "s1" <div> object in the click handler function, and to the square object in the square .click() method, as you'd expect.

![](Image00185.jpg)

JavaScript's treatment of t his in event handlers is a tricky subject. If you use inline event handlers (not recommended!), such as <p o nclick="click()"> , t his will refer to the global window object, not the <p> element object. Similarly, if you use the (now old) at t achEvent ()

Note function in IE8 and earlier, t his will refer to the window object. In order to maintain consistency when handling t his , we recommend that you use the o nclick property to set your click handlers (and other common event handlers), or addEvent List ener() if you know all your users are on IE9+. In both of these cases, t his will be set to the element that is clicked in the event-handling function.

![](Image00018.jpg)

The key point to understand in this section of the lesson is that the value of t his is different depending on how you invoke a function, and you'll want to know what the value of t his will be in these different situations.

Nested Functions

The value of t his in nested functions might not be what you expect. Let's check out an example. Create a new

HTML file as shown:

![](Image00186.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Nested functions </title>

<meta charset="utf-8">

<script>

function outer() {

console.log("outer: ", this);

inner();

function inner() {

console.log("inner: ", this);

}

}

outer();

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as self .ht ml , and ![](Image00085.jpg) . In the console, you see:

![](Image00095.jpg)

OBSERVE:

outer:

Window {top: Window, window: Window, location: Location, external: Object, chrom

Object}

inner:

Window {top: Window, window: Window, location: Location, external: Object, chrom

Object}

The first result should not be a surprise: we know that when you call a globally defined function, t his is set to the global window object.

The value of t his is the window object in the inner() function too . You might be surprised if you expected

t his to be defined as the function o ut er (since o ut er is an object—yes, functions are objects too!). Another thing to remember about t his .

How about when you're inside an object constructor and call a nested function?

![](Image00156.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Nested functions </title>

<meta charset="utf-8">

<script>

function outer() {

console.log("outer: ", this);

inner();

function inner() {

console.log("inner: ", this);

}

}

outer();

function MakeObject() {

this.aProperty = 3;

console.log("outer object: ", this);

function inner() {

console.log("inner to object: ", this);

}

inner();

}

var outerObject = new MakeObject();

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) and ![](Image00021.jpg) . The results you see this time might be even more surprising:

![](Image00104.jpg)

OBSERVE:

outer object: MakeObject {aProperty: 3}

inner to object:

Window {top: Window, window: Window, location: Location, external: Object, chrom

e: Object}

t his is defined to be the object we're creating in the MakeObject () constructor in the first message (as expected), but inside of the inner() function (that defines and calls inside the constructor). t his is defined as the global window object. We "lose" the value of t his (that is, the object we're creating) in the nested function.

As a result of this behavior, a common idiom in JavaScript is to "save" the value of t his in another variable so it's accessible to the nested function, like this:

![](Image00114.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Nested functions </title>

<meta charset="utf-8">

<script>

function outer() {

console.log("outer: ", this);

inner();

function inner() {

console.log("inner: ", this);

}

}

outer();

function MakeObject() {

this.aProperty = 3;

console.log("outer object: ", this);

var self = this;

function inner() {

console.log("inner to object: ", this self );

}

inner();

}

var outerObject = new MakeObject();

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) and ![](Image00036.jpg) preview. Now you see:

![](Image00043.jpg)

OBSERVE:

outer object: MakeObject {aProperty: 3}

inner to object: MakeObject {aProperty: 3}

We saved the value of t his in the variable self before calling inner() . Because of lexical scoping, the inner() function can see the value of self , and so can access the object being created by the constructor.

![](Image00034.jpg)

| Note | The behavior we've just described ( t his defined as the global window object in nested |
| functions) may change in a later version of JavaScript. |
|  |

![](Image00018.jpg)

When You Want to Control How this is Defined

So you've seen how t his is defined when you invoke (global) functions as functions, when you invoke functions as constructors, when you invoke functions as methods, and in the special cases when you invoke functions as click event handlers, and when you invoke nested functions.

In all these cases, JavaScript rules determine how t his is defined. But what if you want to take control and define your own value for t his when you invoke a function?

That's when we use apply() and call() . These methods are designed specifically to allow you to define the value of t his inside a function you invoke with apply() or call() .

Let's say you decide to add another shape to your program. Edit t his.ht ml as shown:

![](Image00187.jpg) CODE TO EDIT: this.html

...

<script>

function Square(id, name, size) {

this.id = id;

this.name = name;

this.size = size;

this.numClicks = 0;

this.display = function() {

var el = document.getElementById(this.id); el.style.width = this.size + "px"; el.style.height = this.size + "px"; el.innerHTML = "<p>" + this.name + "</p>"; console.log(this.name + " has size " + this.size +

", and is a " + this.constructor.name);

};

this.click = function() {

console.log("This in the Square's click method: "); console.log(this);

this.numClicks++;

document.getElementById("counter_" + this.id).innerHTML =

"You've clicked " + this.numClicks + " times on " + this.name;

};

}

function Circle(id, name, radius) {

this.id = id;

this.name = name;

this.radius = radius;

this.numClicks = 0;

this.display = function() {

var el = document.getElementById(this.id); el.style.width = (this.radius * 2) + "px"; el.style.height = (this.radius * 2) + "px"; el.style.borderRadius = this.radius + "px"; el.innerHTML = "<p>" + this.name + "</p>"; console.log(this.name + " has radius " + this.radius +

", and is a " + this.constructor.name);

};

this.click = function() {

this.numClicks++;

document.getElementById("counter_" + this.id).innerHTML =

"You've clicked " + this.numClicks + " times on " + this.name;

};

}

window.onload = function() {

var square = new Square("s1", "square one", 100); setupClickHandler(square); square.display();

var circle = new Circle("c1", "circle one", 50); setupClickHandler(circle); circle.display();

}

function setupClickHandler(shape) {

var elDiv = document.getElementById(shape.id); elDiv.onclick = function() {

shape.click();

}

}

</script>

</head>

<body>

![](Image00188.jpg)

<div id="s1" class="square"></div>

<div id="c1" class="circle"></div>

<p id="counter_s1"></p>

<p id="counter_c1"></p>

</body>

</html>

![](Image00042.jpg) and ![](Image00036.jpg) . A circle appears in the page with the name "circle one." You can click the square and see the message "You've clicked 1 times on square one," and you can click the circle and see the message "You've clicked 1 times on circle one." Repeated clicks on either object add to the click count in the appropriate displayed sentence.

We added a new Circle() constructor that's similar to Square() , except that it has a radius, and its display() function is different. The click() function is exactly the same though.

We also added new code in the windo w.o nlo ad function to create a circle object, call

set upClickHandler() to add a click handler to the "c1" <div> object representing the circle in the page, and to call circle .display() so we see it in the page.

Each shape gets its own separate click handler. When we pass square to set upClickHandler() , we set the click handler for the "s1" <div> object to the square's click() method, and when we pass circle to set upClickHandler() , we set the click handler for the "c1" <div> object to the circle's click() method.

Because the code for both is exactly the same, we can pull the code out of the two objects and use the same code for both. Modify t his.ht ml again, as shown.

![](Image00189.jpg) CODE TO TYPE:

...

function Square(id, name, size) {

this.id = id;

this.name = name;

this.size = size;

this.numClicks = 0;

this.display = function() {

var el = document.getElementById(this.id); el.style.width = this.size + "px"; el.style.height = this.size + "px"; el.innerHTML = "<p>" + this.name + "</p>"; console.log(this.name + " has size " + this.size +

", and is a " + this.constructor.name);

};

this.click = function() {

this.numClicks++;

document.getElementById("counter_" + this.id).innerHTML =

"You've clicked " + this.numClicks + " times on " + this.name;

};

}

function Circle(id, name, radius) {

this.id = id;

this.name = name;

this.radius = radius;

this.numClicks = 0;

this.display = function() {

var el = document.getElementById(this.id); el.style.width = (this.radius * 2) + "px"; el.style.height = (this.radius * 2) + "px"; el.style.borderRadius = this.radius + "px"; el.innerHTML = "<p>" + this.name + "</p>"; console.log(this.name + " has radius " + this.radius +

", and is a " + this.constructor.name);

};

this.click = function() {

this.numClicks++;

document.getElementById("counter_" + this.id).innerHTML =

"You've clicked " + this.numClicks + " times on " + this.name;

};

}

function click() {

console.log("This in click function: ");

console.log(this);

this.numClicks++;

document.getElementById("counter_" + this.id).innerHTML =

"You've clicked " + this.numClicks + " times on " + this.name;

}

window.onload = function() {

var square = new Square("s1", "square one", 100); setupClickHandler(square); square.display();

var circle = new Circle("c1", "circle one", 50); setupClickHandler(circle); circle.display();

}

function setupClickHandler(shape) {

var elDiv = document.getElementById(shape.id); elDiv.onclick = function() {

shape.click();

![](Image00190.jpg)

click.call(shape);

}

}

...

![](Image00042.jpg) Save and ![](Image00021.jpg) . Try clicking on both the square and the circle. You see messages in the page showing how many times you've clicked on the respective shapes. In the console, you see the messages displayed by the new click() function we just added, that show which shape you've just clicked on.

First, we removed the click() methods from each of the shapes, and put the code into a new click() function. The code is exactly the same, except that we added the two console messages at the top The code in the click() method still refers to t his , and properties like t his.numClicks and t his.name , but if you call a global function, t his is set to the window object. It shouldn't be set to either the square or the circle though, so what's going on?

This is where call() comes in handy. When we set up the click handler for the shapes, we made one small change: we changed the code from shape .click() to click.call(shape) . So what's the difference? What does call() do? Good questions!

click() is a function. We can call that function using the call() method (I'll explain where that method comes from in a just a moment), and pass in the object that we want to use for t his , which in this case is the shape object, which will be square when we've passed square to set upClickHandler , and circle when we've passed circle to set upClickHandler . Calling the click() function using the call() method is just like calling the function in the normal way (with click() ), except that we get to choose how t his should be defined.

Inside click() , t his is set to either the square or the circle , depending on which element we click on. If it's set to square , we reference the square's numClicks property, and the square's name property. We do the same for the circle .

call() is a method of the click() function. As we've said previously, a function is an object with properties and methods just like any other object. Whenever you define a function, like click() , you're actually creating an instance of the Funct io n object using the Funct io n() constructor (JavaScript does that for you behind the scenes). Remember that an object can inherit methods and properties from its prototype. In this case, function's prototype includes the method call() . You can check for yourself, like this (this session assumes you've loaded the t his.ht ml file):

![](Image00124.jpg)

INTERACTIVE SESSION:

        click

function click() {

console.log("This in click function: ");

console.log(this);

this.numClicks++;

document.getElementById("counter_" + this.id).innerHTML =

"You've clicked " + this.numClicks + " times on " + this.name;

}

        click.call

function call() { [native code] }

First we ask to display the function click() , by typing the name of the function. Then we ask to see the click() function's call property, which it inherits from its Funct io n prototype, and which is implemented natively by the browser (so you can't see the details).

call() and apply()

The methods call() and apply() do essentially the same thing, but you use them slightly differently. The first argument of both methods is the object you want to stand in for t his . If the function you're calling takes arguments, then you also pass these arguments into both call() and apply() . For call() , you pass these arguments as a list of arguments (like you normally do with arguments), and for apply() , you pass all the arguments in an array.

So, to use call() , you'd write:

![](Image00120.jpg) OBSERVE:

function myFunction( param1, param2, param3 ) {

...

}

var anObject = { x: 1 };

myFunction .call( anObject , 1, 2, 3 );

...and to use apply() , you'd write:

![](Image00098.jpg)

OBSERVE:

function myFunction( param1, param2, param3 ) {

...

}

var anObject = { x: 1 };

myFunction .apply( anObject , [ 1, 2, 3 ]);

In both of these examples, the object anObject is defined as the value of t his in the function myFunct io n() , and the arguments 1, 2, 3 are passed to myFunct io n() , and stored in the parameters param1, param2, and param3 .

As you've seen with our example of using call() to call the click() function, the arguments are optional—if your function doesn't expect arguments you don't have to supply any.

You can use call() and apply() on your own functions, as well as JavaScript's built-in functions. For instance, let's say you have an array of numbers and you want to find the maximum number in the array. There is a handy Mat h.max() method available, but it doesn't take an array, it takes a list of numbers:

![](Image00059.jpg)

INTERACTIVE SESSION:

       var myArray = [1, 2, 3]; undefined

        Math.max(myArray)

        Math.max(1, 2, 3)

3

However, we can use apply() to get around this, like this:

![](Image00067.jpg)

INTERACTIVE SESSION:

        Math.max.apply(null, myArray);

3

Notice that we pass null as the value to be used for t his (because we don't need any object to stand in for this), and because we're using apply() , the values from the array are passed into the Mat h.max() method as a list of arguments.

Function Arguments

When you invoke a function, you pass arguments to the function's parameters. When the number of arguments is equal to the number of parameters, each parameter gets a corresponding argument from the function call. So, what happens if the number of arguments doesn't match the number of parameters?

Suppose you want to write your own max() function (similar to Mat h.max() ). How would you do it? Well, you could start simple:

![](Image00191.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> max </title>

<meta charset="utf-8">

<script>

function max(n1, n2) {

if (n1 > n2) {

return n1;

}

else {

return n2;

}

}

console.log(max(99, 101, 103));

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as max.ht ml , and ![](Image00036.jpg) . In the console, you see 101.

The argument 103 does get passed to the function, but since we don't give it a parameter name, and we don't use it, it's not included in the calculation of the maximum number.

If you pass too few arguments, then the parameter that's expecting an argument has the value undefined.

Let's see what happens if we pass only one argument to our max() function:

![](Image00020.jpg)

CODE TO TYPE:

function max(n1, n2) {

console.log("n2 is " + n2);

if (n1 > n2) {

return n1;

}

else {

return n2;

}

}

console.log(max(99 , 101, 103 ));

![](Image00042.jpg) and ![](Image00021.jpg) . In the console, you see that "n2 is undefined."

We'd like to write our max() function so that it can take any number of arguments, like Mat h.max() , and find the maximum value. To do that, we can use the argument s object. This object contains all the arguments passed to a function. Let's rewrite our max() function to use it:

![](Image00192.jpg) CODE TO TYPE:

function max( n1, n2 ) {

console.log("n2 is " + n2);

if (n1 > n2) {

return n1;

}

else {

return n2;

}

var max = Number.NEGATIVE_INFINITY;

for (var i = 0; i < arguments.length; i++) {

if (arguments[i] > max) {

max = arguments[i];

}

}

return max;

}

console.log(max(99 , -55, 101, 103, 22 ));

![](Image00087.jpg) and ![](Image00036.jpg) . You see the result 103 in the console.

First notice that our max() function no longer specifies any parameters. That's because we're going to access all the arguments with the argument s object.

The argument s object is an array- like object; you can iterate over it, and it has a length property, so we can use it like an array to iterate over all of the arguments and find the maximum value. To do that we initialize the variable max to negative infinity, and then look at each argument to see if it's greater than max . Each time an argument is greater than max , we update the value of max , so the final result is the maximum value of all the arguments we passed into the object.

The Four Ways to Invoke a Function

You've seen examples of each of the four ways you can invoke a function:

as a function

![](Image00006.jpg)

as a method

![](Image00006.jpg)

as a constructor

![](Image00006.jpg)

with apply() or call()

![](Image00006.jpg)

You'll likely use the first three most often, but there are times when the fourth (using apply() or call() ) can come in handy too .

In general, the t his keyword is bound to the object that contains the function. For global functions, that's the global window object; for constructors, that's the object being constructed; and for methods, that's the object that contains the method you're calling.

Three big exceptions to this rule are: when you are in an event handler function on an event like "click"; when you've explicitly changed the value defined for this using call() or apply() ; and when you are in a nested function. Memorize the way this behaves in these three cases so you don't get tripped up (not to mention that having a grasp on this is a great way to ace those JavaScript interview questions)!

In this lesson, you learned about the four ways we can invoke functions in JavaScript, and what happens to this in each case. Take some time to practice invoking some functions before you move on to the next lesson, where we'll look at invocation patterns: code designs that use function calls in some interesting ways.

Invocation Patterns

![](Image00005.jpg)

Lesson Objectives

When you complete this lesson, you will be able to:

call a function recursively.

![](Image00006.jpg)

create an object so its methods can be chained.

![](Image00006.jpg)

call functions by chaining them together.

![](Image00006.jpg)

create a static method.

![](Image00006.jpg)

distinguish between static and instance methods.

![](Image00005.jpg) ![](Image00006.jpg)

Invocation Patterns

In this lesson, we take a look at some "invocation patterns": that is, ways to structure your function calls. These aren't new ways to invoke functions, but rather code designs involving function calls that may be useful as you continue in your JavaScript programming.

Recursion

Recursion is when you call a function from within that same function. It's a powerful programming tool, so it's an important concept to master, but it can be tricky.

A recursive function can always be converted to an iteration, so we'll start by looking at an example of iteration and then rewrite the function using recursion instead.

We'll use code from a previous example using the Square() constructor to create squares in the page.

Create a new HTML file and copy in this code:

![](Image00193.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Recursion </title>

<meta charset="utf-8">

<style>

.square {

background-color: lightblue;

cursor: pointer;

}

.square p {

padding-top: 35%;

text-align: center;

-webkit-user-select: none;

-moz-user-select: none;

-ms-user-select: none;

user-select: none;

}

</style>

<script>

function Square(id, size) {

this.id = id;

this.size = size;

this.display = function() {

var el = document.createElement("div"); el.setAttribute("id", this.id); el.setAttribute("class", "square"); el.style.width = this.size + "px"; el.style.height = this.size + "px"; el.innerHTML = "<p>" + this.id + "</p>"; console.log(this.id + " has size " + this.size +

", and is a " + this.constructor.name); document.getElementById("squares").appendChild(el);

};

}

function createSquares(n) {

var size = 10;

if (n == 0) {

return;

}

while (n >= 1) {

var s = new Square(("s" + n), n * size);

s.display();

n--;

}

}

window.onload = function() {

createSquares(7);

};

</script>

</head>

<body>

<div id="squares"></div>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as recursio n.ht ml , and ![](Image00021.jpg) . You see seven squares, decreasing in size:

![](Image00194.jpg)

(The names of the smallest squares don't fit into the <div>s properly; don't worry about that).

Take a look at the code:

![](Image00066.jpg) OBSERVE:

function createSquares( n ) {

var size = 10;

if ( n == 0) {

return;

}

while ( n >= 1) {

var s = new Square(("s" + n ), n * size) ;

s . display() ;

n --;

}

}

We use a function, creat eSquares() , to create a given number of squares. In a Square() constructor, and then display the resulting square object by calling its

lo o p , we invoke the display() method.

The display() method creates a new <div> object representing the square, and appends it to the "squares" <div> in the page.

To create the correct number of squares, we use a while lo o p to iterate the number, n , passed into

creat eSquares() . We also use n to compute the size of the square to add to the page (using n * size, where size is 10), and include it as part of the name of each square (for example, s3).

We can rewrite this function using recursion by replacing the while loop with a call to the function creat eSquares() :

![](Image00195.jpg)

CODE TO TYPE:

...

function createSquares(n) {

var size = 10;

if (n == 0) {

return;

}

while (n >= 1) {

var s = new Square(("s" + n), n * size);

s.display();

n--;

}

var s = new Square(("s" + n), n * size);

s.display();

createSquares(n-1);

}

...

![](Image00042.jpg) and ![](Image00021.jpg) . You see the same seven squares in decreasing sizes.

Let's compare the resursive version to the version with the iteration to see how that works:

![](Image00098.jpg)

OBSERVE:

while ( n >= 1) {

var s = new Square(("s" + n ), n * size);

s.display();

n --;

}

Here we it erat e through all of the values of n until n is equal to 1\. When we pass 7 to the function

creat eSquares() , the first time through the iteration, n is 7, we get a square of size 70 (using n * size , which is 7 * 10), then reduce n by one, and keep looping until n is 1.

![](Image00184.jpg) OBSERVE:

var s = new Square(("s" + n ), n * size);

s.display();

createSquares( n -1);

The recursive version does essentially the same thing, except that we call creat eSquares() each time we want a square of a smaller size.

The first time we call creat eSquares() , n is 7, so we create and display a square of size 70 . Then we call creat eSquares() again, only we pass n - 1 as the argument to the function. So in this call to

creat eSquares() , n is 6 . We create and display a square of size 60, and call creat eSquares() again, with the argument 5, and so on.

When n is 1, we execute the code that creates and displays a square of size 10 . Then we call

creat eSquares() and pass the value 0 for n . Now, instead of executing the code to create a square of size 0, we check and see that n is 0 and return:

![](Image00033.jpg)

OBSERVE:

if (n == 0) {

return;

}

This if statement is known as the base case and it's vitally important because without it, the recursion will

continue forever—try it. Comment out the if block, ![](Image00042.jpg) , and ![](Image00021.jpg) . It's just like with iteration: you must supply a conditional test to tell the iteration when to stop. In recursion, the base case tells the recursion when to stop. We want the recursion to stop when n is 0 . So in this case, we do not call creat eSquares() again, which causes the recursion to stop.

The results of both of these versions of creat eSquares() are exactly the same, but the first uses iteration and the second uses recursion. Again, recursion can always be replaced with iteration.

Why Use Recursion?

Some algorithms are naturally recursive. For instance, the algorithm to compute the factorial of a number n is recursive. To compute the factorial of a number, say 5, we multiply 5 times the factorial of that number minus 1:

![](Image00095.jpg)

OBSERVE:

The factorial of 5 is 5 * the factorial of 4.

The factorial of 4 is 4 * the factorial of 3.

The factorial of 3 is 3 * the factorial of 2.

The factorial of 2 is 2 * the factorial of 1.

The factorial of 1 is 1.

So the factorial of 5 is 5 * 4 * 3 * 2 * 1, which is 120.

Writing this in pseudocode, you can think of this as recursively designed code:

![](Image00098.jpg)

OBSERVE:

factorial(5) = 5 * factorial(4)

factorial(4) = 4 * factorial(3)

factorial(3) = 3 * factorial(2)

factorial(2) = 2 * factorial(1)

factorial(1) = 1

We are using the factorial function in the definition of the factorial function. That's the very definition of "recursive." It's like we are using the question in the answer to the question: what is factorial of 5? It's 5 times the factorial of 4!

Of course, that can be frustrating unless you have an answer to the question that doesn't involve the question itself. That's the reason for the base case. The base case for the factorial algorithm is 1; when n is 1, we don't call factorial again. That means you can finally stop asking the question and start getting answers. You can

plug in the value 1 for the answer to "What is the factorial of 1?" then you can then answer the question, "What is the factorial of 2?" and so on until you get to the answer for your original question, "What is the factorial of 5?"

Every recursive algorithm works this way: you create a pile of function calls, each with solutions that involve calling that function again, until you get to the base case. Then you can start unravelling the pile until you get back to your original function call. (See if you can implement f act o rial() in JavaScript—it'll be one of the projects!)

Many algorithms for which you may want to create functions are naturally recursive. These naturally recursive functions tend to be easier to read when they are expressed recursively, rather than when they are expressed iteratively (using loops).

However, there's a downside to recursion. Each time you call a function, you add that function to the call stack; this takes up memory. Iteration takes up memory too, but usually not as much as a pile of functions on a call stack. To see the call stack created by recursive calls, we can use the Chrome browser tools and add a breakpoint to the code on the line in creat eSquares() where we call creat eSquares() recursively:

![](Image00196.jpg)

Then we reload the page, and execution stops each time we call creat eSquares() recursively. Execute the breakpoint a few times by clicking the Resume script execut io n button, and you can see the function being added to the call stack each time we call it:

![](Image00197.jpg)

Take a look at the scope variables each time you click the Resume script execut io n button; the value of n decreases by one each time. Eventually, n gets to 0, the recursion stops, and the code completes.

This happens because we're calling creat eSquares() from inside creat eSquares() before the previous invocation of creat eSquares() is complete. To compare, let's say you have a function add() (that's not recursive), and you call that function three times:

![](Image00122.jpg) OBSERVE:

function add(num1, num2) {

return num1 + num2;

}

add(1, 2);

add(2, 3);

add(3, 4);

The add() function goes on to the call stack three times. However, you only have one invocation of add() on the call stack at a time, because each invocation of add() ends before the next one begins, so the call stack never gets bigger than one function.

Now think about creat eSquares() again. We call creat eSquares() before the previous call to

creat eSquares() has completed. So we call creat eSquares(7) , and while that function invocation is still on the stack, we call creat eSquares(6) . This function invocation goes on top of the invocation to

creat eSquares(7) , so we have two function invocations on the stack. Then we do it again with creat eSquares(5) , and so on until we call creat eSquares(0) .

When we call creat eSquares(0) , creat eSquares(0) gets added to the top of the stack, but

creat eSquares(0) just returns, so it gets popped off the stack right away. When creat eSquares(0) returns, then creat eSquares(1) can finish executing and then get popped off the stack. Once that's done,

creat eSquares(2) can finish executing and get popped off the stack, and so on, until finally, creat eSquares(7) finishes and gets popped off the stack and you're done.

Here's how the call stack gets built up as each recursive call to creat eSquares() takes place. Then the function invocations are removed from the stack once we reach the base case and each function call can finish:

![](Image00198.jpg)

This pile of function invocations that's created on the call stack when you call a function recursively isn't a big deal if your functions are small (and don't have too many variables in each activation object), and if the number of times the function is called recursively (so the number of invocations that goes on the stack) is small. If your functions are large though and have lots of variables and/or the function is called recursively many times, then your code will take up a lot of memory. In addition, your browser will limit the number of functions it allows on the call stack at once.

Most of the time, you'll have functions with few local variables, so you won't call your recursive functions so often that it becomes problematic. So now you know what to look out for if you run into memory issues while using a recursive design.

Chaining (a la jQuery)

Another invocation pattern you'll see in JavaScript is method chaining . Chaining is common in some JavaScript libraries, like jQuery. The technique allows you to write multiple method calls on the same object in a chain. For instance, instead of writing:

![](Image00033.jpg)

OBSERVE:

obj.method1();

obj.method2();

obj.method3();

...you can write:

![](Image00199.jpg) OBSERVE:

obj.method1().method2().method3();

For method chaining to work, each method must return an object so that the next method can be called on that object. In the example above, if o bj.met ho d1() retuns o bj , that object is used to call met ho d2() immediately.

Let's take a look at a concrete example. We'll use the same Squares example from earlier, and modify it a bit.

Save recursio n.ht ml to a new file in your /AdvJS folder named chaining.ht ml , and make these changes:

![](Image00200.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Chaining </title>

<meta charset="utf-8">

<style>

.square {

background-color: lightblue;

cursor: pointer;

}

.square p {

padding-top: 35%;

text-align: center;

-webkit-user-select: none;

-moz-user-select: none;

-ms-user-select: none;

user-select: none;

}

</style>

<script>

function Square(id, size) {

this.id = id;

this.size = size;

this.el = null;

this.bigger = function(size) {

if (this.el) {

this.size += size;

this.el.style.width = this.size + "px";

this.el.style.height = this.size + "px";

return this;

}

};

this.color = function(color) {

if (this.el) {

this.el.style.backgroundColor = color;

return this;

}

};

this.display = function() {

var this. el = document.createElement("div"); this. el.setAttribute("id", this.id); this. el.setAttribute("class", "square"); this. el.style.width = this.size + "px"; this. el.style.height = this.size + "px"; this. el.innerHTML = "<p>" + this.id + "</p>"; console.log(this.id + " has size " + this.size +

", and is a " + this.constructor.name); document.getElementById("squares").appendChild( this. el); return this;

};

}

function createSquares(n) {

var size = 10;

if (n == 0) {

return;

}

var s = new Square(("s" + n), n * size);

s.display();

createSquares(n-1);

}

window.onload = function() {

createSquares(7);

![](Image00201.jpg)

var mySquare = new Square("mySquare", 100);

mySquare.display().color("green");

mySquare.el.onclick = function() {

mySquare.bigger(50).color("red");

};

};

</script>

</head>

<body>

<div id="squares"></div>

</body>

</html>

![](Image00087.jpg) Save and ![](Image00036.jpg) . You see a green square with the name "mySquare." Click on the square. The square gets bigger and turns red. Each time you click on the square it gets bigger.

In our code, we made a modification to the display() method: now that method stores the <div> element we're creating for the square in the Square object, in the property el . Now we can use that <div> element in the two new methods we've added: bigger() and co lo r() . bigger() takes a value and adds it to the size of the square, then modifies the style of the <div> representing the square to change the size of the <div> (which makes the square appear bigger). Similarly, co lo r() takes a color string (like "blue," "green," or "red"), and modifies the style of the <div> to change the background to that color.

We've also added a line to each method to return t his . For example:

![](Image00095.jpg)

OBSERVE:

this.color = function(color) {

if (this.el) {

this.el.style.backgroundColor = color;

return this;

}

};

Each of the Square 's three methods now returns t his , so when we call mySquare .display() , we get mySquare back as a result. That means we can call one of the other methods on the resulting object immediately, like co lo r() or bigger() . We can chain these methods together!\.

In fact, that's exactly what we do in the code after we create mySquare :

![](Image00104.jpg)

OBSERVE:

mySquare.display().color("green");

mySquare.el.onclick = function() {

mySquare.bigger(50).color("red");

};

After creating the mySquare object, we call t he display() met ho d to create and display the <div> object in the page, and then chain a call t o t he co lo r() met ho d to turn the square green. Also, we set up a click handler on the <div> so that when you click on the square, we call two methods on the square, bigger() and co lo r(), again chained , so that co lo r() is called on the object that is returned by bigger() .

Usually when you chain methods, you call methods on the same object for each part of the chain. It's certainly possible to have one of the methods return a different object for the next method to be called on, but code written that way would be much more difficult to understand, so in general, it's not recommended. When you create method chains, you generally want to make sure you act on the same object in each part of the chain.

Potential benefits of chaining are that it can make code easier to read, and reduce the number of lines of code. However, chains that are too long can be difficult to understand as well, so use chaining judiciously. (Chains that are too long are often called train wrecks !)

Static vs. Instance Methods

One last invocation pattern we'll look at in this lesson is how to call static methods, and the differences

between static and instance methods.

Let's begin by exploring the Dat e() constructor. You can use Dat e() to create new date objects, like this:

![](Image00061.jpg)

INTERACTIVE SESSION:

var nowDate = new Date() undefined

nowDate.toString()

nowDate.getMonth()

8

nowDate.getTime()

1378401459465

Here, we created a new date object, no wDat e , by calling the Dat e() constructor function. If you pass no arguments to the constructor, this function creates an object for the current date and time, so the result is a date object that represents "right now," which (as of the writing this lesson) is Thursday, September 5, 2013 at 10:17am.

The date object no wDat e has various methods and properties you can use just like any other object. For instance, you can use the method no wDat e .t o St ring() to get a string representing the current date and time, and get the month with no wDat e .get Mo nt h() (note that the returned numeric value is from an array whose indices start at zero, so September is represented by 8). You can get the number representing the date and time using the get T ime() method.

Now try this:

![](Image00060.jpg)

INTERACTIVE SESSION:

var time = Date.now() undefined

time

1378401746077

We called a method no w() on the Dat e object. Dat e and Dat e() are the same object: they are both the

Dat e() constructor function. Remember that functions are objects—and objects can have properties though.

The method no w() is a method of the Dat e() function object.

Notice that the result, t ime , is a variable that contains a number representing the current time. It's different from the variable no wDat e though. no wDat e is a Dat e object, whereas t ime is simply a number:

![](Image00060.jpg)

INTERACTIVE SESSION:

nowDate instanceof Date true

time instanceof Date false

You can use t ime to create a Dat e object, like this:

![](Image00059.jpg)

INTERACTIVE SESSION:

var anotherDate = new Date(time); undefined

anotherDate

anotherDate.getTime()

1378401746077

Once you have the ano t herDat e object, you can use the method get T ime() to get the number representing the date and time back (it's the same number as in the variable t ime that we used to create the object in the first place).

So, what's the difference between creating a date object using a constructor and then calling methods on that date object, and calling a method directly on the function object itself? And how do you add methods directly to a function anyway?

We'll answer those questions by adding a method to the Square() constructor we've been working with in this lesson. Modify your JavaScript code in chaining.ht ml as shown:

![](Image00202.jpg)

CODE TO TYPE:

function Square(id, size) {

this.id = id;

this.size = size;

this.el = null;

this.bigger = function(size) {

if (this.el) {

this.size += size;

this.el.style.width = this.size + "px";

this.el.style.height = this.size + "px";

return this;

}

};

this.color = function(color) {

if (this.el) {

this.el.style.backgroundColor = color;

return this;

}

};

this.display = function() {

this.el = document.createElement("div"); this.el.setAttribute("id", this.id); this.el.setAttribute("class", "square"); this.el.style.width = this.size + "px"; this.el.style.height = this.size + "px"; this.el.innerHTML = "<p>" + this.id + "</p>" console.log(this.id + " has size " + this.size +

", and is a " + this.constructor.name); document.getElementById("squares").appendChild(this.el); return this;

};

}

Square.info = function() {

return "Square is a constructor for making square objects with an id and size.";

};

window.onload = function() {

var mySquare = new Square("mySquare", 100);

mySquare.display().color("green");

mySquare.el.onclick = function() {

mySquare.bigger(50).color("red");

};

var info = Square.info();

console.log(info);

};

![](Image00042.jpg) and ![](Image00021.jpg) . In the console, the message, "Square is a constructor for making square objects with an id and size." is displayed.

We're working with two different kinds of objects here. First, we use the Square() constructor to create new objects by calling Square() with new :

![](Image00076.jpg)

OBSERVE:

var mySquare = new Square("mySquare", 100);

In this case, the object mySquare is called an instance of Square : it's an object created by the constructor, an object that has the properties and methods we specify in the constructor by saying

t his.PROPERT YNAME = SOME VALUE . Methods like bigger() , co lo r() , and display() are called instance methods , because they are methods of the object instances created by calling Square() with new .

The other object we're working with is the Square object. This object happens to be a function, but it's like other objects in that it has methods and properties. Also, just like any other object, we can add a new property or method to it:

![](Image00104.jpg)

OBSERVE:

Square.info = function() {

return "Square is a constructor for making square objects with an id and siz

e.";

};

In this case, we're adding a method of the Square object, not a method of the mySquare instance object we created using Square() as a constructor. We call methods like this static methods : they are methods of the constructor function object. We say they are "static" because, unlike instance methods that may return different values depending on the properties of the specific instance you're working with (for example, one square might have size 10 and color red, while another might have size 200 and the color green), static methods don't vary based on those differences. Static methods are methods of the constructor, not methods of the instances.

We can't access static methods from object instances, just like we can't access instance methods from the constructor object. Let's test this:

![](Image00203.jpg)

CODE TO TYPE:

window.onload = function() {

var mySquare = new Square("mySquare", 100);

mySquare.display().color("green");

mySquare.el.onclick = function() {

mySquare.bigger(50).color("red");

};

var info = Square.info();

console.log(info);

mySquare.info();

}

![](Image00042.jpg) and ![](Image00021.jpg) . In the console, you see the error:

![](Image00076.jpg)

OBSERVE:

Uncaught TypeError: Object #<Square> has no method 'info'

Here, we try to call a static method, inf o () , from an object instance. It doesn't work.

Try this:

![](Image00204.jpg) CODE TO TYPE:

window.onload = function() {

var mySquare = new Square("mySquare", 100);

mySquare.display().color("green");

mySquare.el.onclick = function() {

mySquare.bigger(50).color("red");

};

var info = Square.info();

console.log(info);

mySquare.info();

Square.color("red");

};

![](Image00042.jpg) and ![](Image00036.jpg) . In the console, you see another error message:

![](Image00033.jpg)

OBSERVE:

Uncaught TypeError: Object function Square(id, size) {

...

} has no method 'color'

Here, we try to access an instance method from the Square object, and again, it won't work.

Let's go back to the Dat e object. When we created a new date object, no wDat e , then called methods on that object, like get Mo nt h() and get T ime() , we used instance methods : methods defined in the instance objects we create by calling the Dat e() constructor function with new . When we called Dat e .no w() , we used a static method : a method defined in the Dat e function object itself.

So, when should a method be an instance method, and when should a method be a static method?

Well, object instances are used to represent specific items, like a square object with a specific size, or a date object with a specific date and time. So it makes sense to have methods like get Mo nt h() and

get FullYear() for a date object instance , because that object has specific values for the month and the year, the values you gave it when you created the object using the constructor with new .

The constructor function, Dat e() doesn't represent a specific date or time. So asking the Dat e object for a month, for instance:

![](Image00076.jpg)

OBSERVE:

Date.getMonth()

...makes no sense. Dat e doesn't represent any particular date until you create a specific instance. However, the Dat e object can have useful properties and methods that aren't related to a specific date you're creating. The no w() method is one of those useful methods: it generates a number that represents the date and time of "right now." There is no need to create a new date object instance to get that number.

Similarly, the Square .inf o () method provides information about the Square constructor function that is not related to any specific instance of a square. Meanwhile, methods like co lo r() and display() are only relevant for a specific instance of a square, one that has a size and an element associated with it that can be assigned a color.

So, in a sense, invoking static methods and instance methods are the same. A static method is invoked on the object in which it is defined (the constructor function) and an instance method is invoked on the object in which it's defined as well (the instance object created by calling the constructor function). The trick is to keep track of which object is which.

Further, we don't just use static and instance to describe methods; we can also use these terms to describe other properties of objects. So, in our Squares example, we say the property size is an instance variable of a square object. You could add a static variable , say, reco mmendedSize , to the Square() constructor, like this:

![](Image00199.jpg) OBSERVE:

Square.recommendedSize = 100;

To access the variable from the inf o () method, you'd write:

![](Image00095.jpg)

OBSERVE:

Square.info = function() {

return "Square is a constructor for making square objects with an id and siz e. " +

"The recommended size for a square is " + Square.recommendedSize + ".

";

};

In this lesson, we talked about three invocation patterns that you'll see used frequently in JavaScript: recursion, chaining, and static methods. There are other invocation patterns, of course, which you may encounter as you continue your JavaScript studies and get more programming experience. In upcoming lessons we'll explore the Module Pattern, but for now, do the quiz and the project, then take a break. When you're rested, continue on!

Encapsulation and APIs

![](Image00005.jpg)

Lesson Objectives

When you complete this lesson, you will be able to:

create private properties and methods in an object.

![](Image00006.jpg)

create a public interface to use the object.

![](Image00005.jpg) ![](Image00006.jpg)

Encapsulation and APIs

One of the benefits of objects in an object- oriented language is encapuslation: the ability to compartmentalize properties and behaviors in an object, and provide an interface so the rest of your program doesn't have to worry about how certain behaviors are implemented. The object just works. Think of other objects you use in JavaScript, like JSON or Date or Math. These objects all have properties and methods that work; you don't need to worry about the inner workings. Sometimes you might want to hide the internal operation of your properties and methods, so programs don't depend on any particular implementation. In this lesson, we'll learn how to use objects and functions to encapsulate structure and behavior, and how to use information hiding techniques to protect implementation details.

Privacy, Please

In the previous lesson, we used a Square() constructor to create square objects and display them in a web page. In that example, we created some properties and methods to give a new square object an id, a size, and a <div> element to represent the square object in the web page:

![](Image00205.jpg) OBSERVE:

function Square(id, size) {

this.id = id;

this.size = size;

this.el = null;

this.bigger = function(size) {

if (this.el) {

this.size += size;

this.el.style.width = this.size + "px";

this.el.style.height = this.size + "px";

return this;

}

};

this.color = function(color) {

if (this.el) {

this.el.style.backgroundColor = color;

return this;

}

};

this.display = function() {

this.el = document.createElement("div"); this.el.setAttribute("id", this.id); this.el.setAttribute("class", "square"); this.el.style.width = this.size + "px"; this.el.style.height = this.size + "px"; this.el.innerHTML = "<p>" + this.id + "</p>"; console.log(this.id + " has size " + this.size +

", and is a " + this.constructor.name); document.getElementById("squares").appendChild(this.el); return this;

};

}

window.onload = function() {

var mySquare = new Square("mySquare", 100);

mySquare.display().color("green");

mySquare.el.onclick = function() {

mySquare.bigger(50).color("red");

};

};

All of the values in a square object are either properties or methods, which means we could change them at any time. For instance, you could write:

![](Image00076.jpg)

OBSERVE:

mySquare.size = 200;

...and that would change the size property of the mySquare object, but the square in the web page wouldn't get any bigger.

Just changing the size property of a square doesn't affect the <div> element (stored in the el property) at all. Unless you call the bigger() method of a square, no changes will be made to the size of the <div> in the page.

You could also do this:

![](Image00076.jpg)

OBSERVE:

mySquare.el = document.createElement("p");

...because if the element that represents the square isn't set up correctly (by calling the display() method), the

square won't appear in the page.

Now, you probably wouldn't make these mistakes, but if you give your Square code to a friend, and your friend doesn't quite understand how to use it correctly, all kinds of things could go wrong.

So developers like to create objects that protect an object's inner workings, and provide a simple interface for other developers to use to manipulate the object. An interface is a public view of an object that hides its inner workings, but lets the person using the object work with it.

For instance, we might want to allow someone to create a square, but rather than controlling the display of the square, have the square handle that privately so that a square is only displayed once. (Right now, you could call display() twice.) We might want to protect the el property so that no one can change it. We might want to control the color and the amount by which a square grows each time internally within the square object, and only allow the user of a square object to "grow" the square.

An Example

That's pretty abstract, so let's take a look at an example. We'll modify our Squares example, but start from scratch with a new file. Go ahead and create a new file and add this code:

![](Image00125.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Squares with API </title>

<meta charset="utf-8">

<style>

.square {

background-color: lightblue;

cursor: pointer;

}

.square p {

padding-top: 35%;

text-align: center;

-webkit-user-select: none;

-moz-user-select: none;

-ms-user-select: none;

user-select: none;

}

</style>

<script>

function Square(size) {

var initialSize = size;

var el = null;

var id = getNextId();

this.grow = function() {

setBigger(10);

setColor("red");

};

var self = this;

display();

function setBigger(growBy) {

if (el) {

size += growBy;

el.style.width = size + "px";

el.style.height = size + "px";

}

}

function setColor(color) {

if (el) {

el.style.backgroundColor = color;

}

}

function display() {

el = document.createElement("div");

el.setAttribute("id", id);

el.setAttribute("class", "square");

el.style.width = size + "px";

el.style.height = size + "px";

el.innerHTML = "<p>" + id + "</p>";

el.onclick = self.grow;

document.getElementById("squares").appendChild(el);

}

function getNextId() {

var squares = document.querySelectorAll(".square"); if (squares) {

return squares.length;

}

return 0;

}

}

![](Image00206.jpg)

window.onload = function() {

var square1 = new Square(100);

var square2 = new Square(200);

var growButton = document.getElementById("growButton"); growButton.onclick = function() {

square1.grow();

square2.grow();

};

};

</script>

</head>

<body>

<form>

<input type="button" id="growButton" value="Grow"> </form>

<div id="squares"></div>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as squaresAPI.ht ml , and ![](Image00021.jpg) . When you click on a square, that square grows; when you click on the Gro w button, both squares grow.

Let's take a closer look at the code.

![](Image00207.jpg)

OBSERVE:

function Square(size) {

var initialSize = size;

var el = null;

var id = getNextId();

this. grow = function() {

setBigger(10);

setColor("red");

};

...

window.onload = function() {

var square1 = new Square(100) ;

var square2 = new Square(200) ;

var growButton = document.getElementById("growButton"); growButton.onclick = function() {

square1. grow() ;

square2. grow() ;

};

};

First, notice that we now have only one public property in the Square() constructor: a method gro w() . What do we mean by "public" here? Well, think back to how constructors work. When you call a function like Square() with new , the constructor creates a new object instance with any properties and methods you add to it using t his in the constructor. In this example, we add only one property to the object being created by the Square() constructor: the gro w() method. So, that's the only property the resulting object will contain.

So what happens to all that other stuff after the object's created? How can we use the variables and the functions in the square object if they go away after the Square() constructor has finished executing?

Those are really great question. We'll answer them in detail in the next lesson. The short answer is: a closure. Some of the other "stuff" in the constructor is accessible after Square() is complete and has returned a new square object because it's saved in a closure. Don't worry about that now; just keep it in the back of your

mind, and know that the variables and functions encapsulated with the object are available even after the constructor has completed.

Private Variables

All the values that we created as properties before are now variables:

![](Image00123.jpg)

OBSERVE:

function Square(size) {

var initialSize = size;

var el = null;

var id = getNextId();

...

}

These variables are private . You can't access them by writing something like:

![](Image00076.jpg)

OBSERVE:

square1.id

...in your code that creates the square objects. Try it. See what happens if you try to access one of these variables.

![](Image00150.jpg)

CODE TO TYPE: Update your code in squaresAPI.html to add the following JavaScript code ...

window.onload = function() {

var square1 = new Square(100);

var square2 = new Square(200);

console.log(square1.id);

var growButton = document.getElementById("growButton"); growButton.onclick = function() {

square1.grow();

square2.grow();

};

};

![](Image00042.jpg) and ![](Image00021.jpg) and check the console: "undefined." square1 doesn't have an id property, so the value of square1.id is undefined.

Once you've tested this code, go ahead and remove the line you added.

These variables are now accessible only inside the constructor function. They are not accessible by users of the square objects, so we say they are private . We use the init ialSize variable to keep track of the initial size of the square (we can change the size of the square using t his.gro w() , so we might want to know what the original size was in case we need it later). We'll use the el variable to hold the <div> element (once we create it in the display() function) and id to hold a unique id for the square, which we'll generate using get Next Id() .

Private Functions

The Square() constructor doesn't take an id (unlike the version in the previous lesson); instead, we generate an id in the constructor based on how many squares are in the page already. We use a nested function, get Next Id() , to generate the next id. Let's examine this function more closely:

![](Image00208.jpg) OBSERVE:

function Square(size) {

var initialSize = size;

var el = null;

var id = getNextId();

...

function getNextId() {

var squares = document.querySelectorAll(".square"); if (squares) {

return squares.length;

}

return 0;

}

};

To set the value of the id variable to the next id (that is, a number that is no longer being used as an id by any of the existing squares), we call get Next Id() . This function first get s all t he exist ing element s wit h t he class "square" from the HTML page using do cument .querySelect o rAll() , which then returns an array of elements (if any exist). If we have no squares yet, the array will be empty, and so the length is 0, and the next id should be 0 . Similarly, if we have one square in the page, then the length of the array is 1, and the next id should be 1, and so on.

Again, note that the function get Next Id() This nested function is private and can be

is not accessible to code that creates and uses square objects.

accessed only within the constructor function.

We set the id of the square as it's being created when the constructor function runs, and we don't need get Next Id() at all after the object has been created.

A Public Method

So far, the variables ( init ialSize , el , and id ), and the function ( get Next Id() ) that we've looked at have all been private . The next function, gro w() , is a public method of the object. That means that the method is added to the object created by the constructor, and that the code that creates and uses the square object can call the method.

![](Image00121.jpg)

OBSERVE:

function Square(size) {

var initialSize = size;

var el = null;

var id = getNextId();

this.grow = function() {

setBigger(10) ;

setColor("red") ;

};

...

function getNextId() {

var squares = document.querySelectorAll(".square"); if (squares) {

return squares.length;

}

return 0;

}

}

This method is the public interface of the square object that is exposed to the rest of the code. You can use it to interact with a square object after it's been created. In order to make a square get bigger, call the gro w() method. The details are handled by the square object.

The gro w() method calls two other private functions: set Bigger() and set Co lo r() . Both these functions are nested in the constructor, so they are accessible to the gro w() method, but not accessible to any code

outside of a square object. You can't call square1.set Bigger(10) to make a square bigger; you must call square1.gro w() instead.

![](Image00209.jpg)

OBSERVE:

function Square(size) {

var initialSize = size;

var el = null;

var id = getNextId();

this.grow = function() {

setBigger(10);

setColor("red");

};

...

function setBigger(growBy) {

if (el) {

size += growBy;

el.style.width = size + "px";

el.style.height = size + "px";

}

}

function setColor(color) {

if (el) {

el.style.backgroundColor = color;

}

}

...

function getNextId() {

var squares = document.querySelectorAll(".square"); if (squares) {

return squares.length;

}

return 0;

}

}

Both set Bigger() and set Co lo r() check to make sure that t he el variable has been init ialized

co rrect ly (which we'll do in the display() function), and then modify the style of the <div> element to grow the square and make sure it's got the right color, red.

Notice that we call two private functions from a public method. Even though the square objects created by the constructor have only one property, the method gro w() (because of the closure we mentioned earlier) has access to the set Bigger() and set Co lo r() functions.

Also notice that the functions set Bigger() and set Co lo r() have access to the private variable, el (also because of the closure). So we can manipulate the value of a private variable by calling a public method. But we can't manipulate that private variable from outside the object. That gives you (as the creator of this Square() constructor, and the square objects that are made from it) greater control over how those objects are used.

Acessing a Public Method from a Private Function

At this point, we've initialized our three private variables, and defined a public method, gro w() . Now, we need to create the <div> element that will represent the square in the page.

To do that, we'll call the display() function. This is a nested function that first creates a new <div> element for the square, and then sets various properties to make the square the correct size and color.

We also set up the click handler for the <div> in this function. When you click on a <div> for a square, we want the square to grow, so we call the gro w() method of the square object we're using. You might think we could write the display() function like this:

![](Image00210.jpg) OBSERVE:

function display() {

el = document.createElement("div");

el.setAttribute("id", id);

el.setAttribute("class", "square");

el.style.width = size + "px";

el.style.height = size + "px";

el.innerHTML = "<p>" + id + "</p>";

el.onclick = this.grow ;

document.getElementById("squares").appendChild(el);

}

However, when you call a nested function inside an object, t his is set to the global window object, not the object the function is in. So, how do we refer to "this" object from inside the display() method?

We save the value of t his in another variable, self (you can call this variable whatever you want, but by convention it's usually called self or t hat . It's a good idea to stick with this convention to make it easier for other programmers to understand your code). Once we've saved the value of t his in self , we can call display() , and now display() can refer to the object's gro w() method using self .gro w :

![](Image00211.jpg) OBSERVE:

function Square(size) {

var initialSize = size;

var el = null;

var id = getNextId();

this.grow = function() {

setBigger(10);

setColor("red");

};

var self = this;

display();

function setBigger(growBy) {

if (el) {

size += growBy;

el.style.width = size + "px";

el.style.height = size + "px";

}

}

function setColor(color) {

if (el) {

el.style.backgroundColor = color;

}

}

function display() {

el = document.createElement("div");

el.setAttribute("id", id);

el.setAttribute("class", "square");

el.style.width = size + "px";

el.style.height = size + "px";

el.innerHTML = "<p>" + id + "</p>";

el.onclick = self.grow ;

document.getElementById("squares").appendChild(el);

}

function getNextId() {

var squares = document.querySelectorAll(".square"); if (squares) {

return squares.length;

}

return 0;

}

}

When you click on a square, the gro w() method is called on the object stored in self , which is the square object that was created when you assigned the value of self to t his . self is a private variable, and like the other private variables and methods, it is accessible internally to the square object, even though it's not accessible by the code using the square object.

Let's examine the contents of the square objects we create in the windo w.o nlo ad function by adding a couple of co nso le .lo g() s to the code:

![](Image00212.jpg) CODE TO TYPE: Update your JavaScript code in squaresAPI.html:

window.onload = function() {

var square1 = new Square(100);

var square2 = new Square(200);

console.log(square1);

console.log(square2);

var growButton = document.getElementById("growButton"); growButton.onclick = function() {

square1.grow();

square2.grow();

};

};

![](Image00042.jpg) and ![](Image00036.jpg) . In the console, the two square objects are displayed (Chrome browser):

![](Image00213.jpg)

You can see that the only property (that we added) in each square object is the gro w() method.

Clicking on a square causes that square to grow, because we call the gro w() method of the square on which you click.

The call to the square's gro w() method is set up in the display() method, but the method isn't called until you actually click on a square. In order to allow you to see more explicitly that you can call the gro w() method of a square using the square1 and square2 objects, we set up a form with one button, Gro w , that calls the gro w() method on both square objects:

![](Image00030.jpg)

OBSERVE:

window.onload = function() {

var square1 = new Square(100);

var square2 = new Square(200);

var growButton = document.getElementById("growButton"); growButton.onclick = function() {

square1.grow();

square2.grow();

};

};

First, we get t he but t o n element f ro m t he page , and add a click handler f unct io n t o t he but t o n . The click handler calls t he gro w() met ho d o f bo t h square1 and square2 . Because gro w() is a public method, that is, a property of the object we are creating with the constructor, this method is accessible to code outside the object.

Encapsulation and APIs

So, a square object has a lot of internal components that are not accessible to the "outside world." These are all the private variables and functions we've defined in the Square() constructor.

The one public method, gro w() , that a square has is its interface : the point of interaction between the square and the rest of the code. The only method you're allowed to call from outside the square is gro w() . We call this interface an Application Programming Interface , or API for short. When you see the term API used in software systems, it refers to the set of properties and methods that determine how software components should interact with each other.

We encapsulated all the private things we don't want code outside a square to be able to interact with: the id, the element object representing the square, the initial size, and the functions used to create and manipulate the square. These private properties are not in the API; they're hidden and protected so they can't be used outside the square objects.

Encapsulation is a language mechanism for restricting access to an object's components . In some languages, like Java, we have keywords that specify which pieces of an object are private or public. In JavaScript, we don't have keywords to help us do this, but we can accomplish encapsulation by making variables and functions private to an object using the technique we've covered in this lesson. We sometimes refer to this technique as information hiding , because we're hiding the details of how an object is implemented to protect it from being used in the wrong way.

The advantage to encapsulation and providing an API to an object like a square is that it prevents code that is using the square from setting the internal state of the object to an invalid state. We are unable to modify the id of the square, or the element that represents the square in the page—both of which would disrupt how the square works—because those values are now protected from outside manipulation.

In JavaScript, the mechanism we use to encapsulate data is not perfect. For instance, you could easily change the gro w() method of a square by writing:

![](Image00076.jpg)

OBSERVE:

square1.grow = 3;

...and break your squares! Yet encapsulation lets us hide most of the details of how a square works, so that in order to use a square, we only have to know one thing about it: to grow it, we call the grow() method. Everything else is handled for us. Hopefully you'll know better than to change the public interface of an object by setting the properties to something else.

Let's review. We defined a Square() constructor that creates new square objects with one public method, grow() , and various private variables (sometimes called private "members") and methods. Any properties and methods, for instance grow() , that are added to the object at construction time (either through the constructor, or through the object's prototype) will be accessible to code that uses the object. Any variables and functions that are defined in the constructor, like id and display() , will not be accessible to code outside the object. The interface (API) for our square objects is the grow() method: this is the only method that code outside the square objects can call.

Defining an interface for your objects is particularly important if you're writing code that you're sharing with others. Perhaps you're working on components for a product at work and other members of your developer group will be using your components. Or perhaps you're developing a library, like jQuery, that you want to make available online. By encapsulating the details of how an object works and providing a simple interface for using the object, you'll be making your objects easier to understand and easier to use.

Closures

![](Image00005.jpg)

Lesson Objectives

When you complete this lesson, you will be able to:

create and use a closure to "remember" values.

![](Image00006.jpg)

explain how a closure is created.

![](Image00006.jpg)

use a closure to store a value for a click handler.

![](Image00005.jpg) ![](Image00006.jpg)

Closures

In the previous lesson, you learned about encapsulation and information hiding. All of that functionality is possible because of a feature of JavaScript: closures . Closures appear to be relatively straightforward, yet they can be really difficult to wrap your head around. This entire lesson is devoted to closures: what they are, how they work, and when to use them.

Making a Closure

We've mentioned closures before, now it's time to uncover the mystery that surrounds them. We'll start with some basic examples and then come back to a couple of examples from the previous lessons to see how we've used closures in the past.

Create a new file add this code:

![](Image00068.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Closures </title>

<meta charset="utf-8">

<script>

function makeAdder(x, y) {

var adder = function() {

return x + y;

};

return adder;

}

var f = makeAdder(2, 3);

var result = f();

console.log("Result is: " + result);

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as clo sure .ht ml , and ![](Image00021.jpg) . Open the console (reload the file if necessary) and you'll see, "Result is: 5."

In this code we've got a function that returns another function. You may remember from an earlier lesson that functions are first-class values ; that is, you can return a function from a function, just like you can return values like 3 or "string." The function makeAdder() returns a function, adder() , that adds two values and returns the result. We've named the function adder() inside makeAdder() , but when we return it from makeAdder() , we name it f () . So, in order to call the returned function, we use f () . (We could use the same name for the function in both places, but for this lesson we want to have a way to identify the function when it's defined , and the function when it's called .)

The two values that we want to add together are passed to the madeAdder() function as arguments when we call it. The function adder() doesn't take any arguments. Instead, adder() adds together the two numbers passed into makeAdder() . So, how does this work?

Local variables (including parameters of functions) disappear after the function within which they are defined is done executing. So, while the parameters x and y are defined when the function adder() is created , when we call it later, using the name f () , x and y are long gone. So how does calling f () return the (correct) value, 5? It's seems like f () somehow "remembers" the values of x and y which were defined when f () was created (as adder() ).

Well, that's exactly what happens. The function f () "remembers" the values of x and y through a closure. Let's step through the execution of this code to see the closure in the JavaScript console.

First, open the file clo sure .ht ml in the Chrome browser, and add a breakpoint to the line of code where we call makeAdder() :

![](Image00214.jpg)

Add a breakpoint, click the So urces tab, and then open clo sure .ht ml (from the left pane). Click on the line number next to the line of code where you want to add the breakpoint (in our version, that's line number 16). The breakpoint appears under the Breakpo int s section in the right pane.

Now, reload the page and click the St ep int o button twice. This is the third button from the left of the right pane, with a little arrow pointing down on top of a period:

![](Image00215.jpg)

We're now on the line where we return adder() . Look in the right pane under Sco pe Variables . The local variables that are defined inside makeAdder() , including the two parameters, x and y , as well as the adder() function. These are all local variables because they are defined within makeAdder() .

Click St ep int o twice more; we're now stopped on the line where we call f () (we haven't executed this line yet). f is a global variable (if you open Glo bal under Scope Variables in the right pane, you'll see it defined as a global variable, which is the global window object).

![](Image00216.jpg)

Click St ep int o once more, so that we call f () and stop just before we return the result of adding x and y :

![](Image00217.jpg)

Under Scope Variables, in Local, you see something called Clo sure . Inside that, you'll see two variables: x and y , with their values set correctly to 2 and 3—the arguments we passed into makeAdder() earlier. This is the closure, where f () gets its two values to add together.

St ep int o twice again to execute the line of code, ret urn x + y , and return from f () . The closure disappears:

![](Image00218.jpg)

Click Resume script execut io n to complete the script execution.

What is a Closure?

Now you've made a closure, but what exactly is a closure?

To understand a closure, you need to remember how scope works. In the earlier lesson on scope , we talked

about how the scope chain is created when you call functions. The scope chain is a series of scope objects containing the values of the variables in a function's scope. For global functions (that is, functions defined at the top level), we have just two scope levels: the local scope (the scope within the function) and the global scope. When you call a function and refer to a variable, we get the value for that variable first by looking in the local scope and, if we can't find it there, we look in the global scope.

Now, recall that when we call a nested (or "inner") function, we have three scope levels: the scope of the nested function, then the scope of the function containing the nested function, and finally the global scope.

In our example, we created a nested function named adder() :

![](Image00030.jpg)

OBSERVE:

function makeAdder(x, y) {

var adder = function() {

return x + y;

};

return adder ;

}

var f = makeAdder(2, 3);

var result = f();

console.log("Result is: " + result);

Inside adder() , we refer to two variables, x and y . These variables are defined in the makeAdder() function, so they are not local to adder() . If we just called adder() from inside makeAdder() (for example, if we changed the line ret urn adder to adder() ), you'd see that in order to figure out the values of the variables x and y , we'd use the scope chain. We'd look for those values in the scope of adder() first, but we wouldn't find them there so we'd look for those values in the scope of makeAdder() , and we'd find them there.

However, we're not calling adder() from inside makeAdder() ; we're returning adder() from makeAdder() . When we return the adder() function, it comes along with a scope object: an object that contains the variables that are in the scope of adder() when adder() is created. That includes the two variables x and y . This object is essentially the same as the scope object of makeAdder() that was created for the scope chain. It's the context within which adder() is created.

This object is the closure. A closure is an object that captures the context in place when a function is created. The closure "remembers" all the variables that are in scope at the time the inner function is created. If we just call the inner function right away, the closure gets thrown away when the containing function ends, but if we return that inner function, the closure comes along with it:

![](Image00219.jpg)

When we call that function later and look for the values of the variables it refers to, if we don't find those values in the function itself (that is, they aren't local variables), we look in the closure:

![](Image00220.jpg)

So the closure becomes part of the scope chain when you call a function.

The closure looks a lot like the scope object that's added to the chain when we call a nested function from its containing function (for example, if we called adder() from inside makeAdder() ). Although here, we use the closure instead of the scope object because we're calling the returned function ( f () ) after the containing function has returned, so we can't use the normal scope chain to find the values of the variables in f () ; we have to use the closure instead. We've "captured" the scope, or context, within which the nested function was created in the closure so we can refer to the variables long after the containing function has completed execution.

Playing with Closures

Let's play with closures a bit so you can see how they work. First, let's actually referenced by an inner function are added to a closure. Modify

![](Image00159.jpg)

prove that only variables that are clo sures.ht ml as shown:

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Closures </title>

<meta charset="utf-8">

<script>

function makeAdder(x, y) {

var z = 10;

var adder = function() {

return x + y;

};

return adder;

}

var f = makeAdder(2, 3);

var result = f();

console.log("Result is: " + result);

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) and ![](Image00021.jpg) . In the console, open the So urces tab, and look at clo sure .ht ml . Clear the previous breakpoint and add a breakpoint to the line where we return the result of adding x and y (inside adder() ), like this:

![](Image00221.jpg)

Reload the page. The execution will stop at the breakpoint, so you can inspect the closure. Notice that even though we've added a local variable z to makeAdder() , that variable is not included in the closure. Why?

Because it's not referenced by adder() , so it's not needed in the closure.

Next, let's prove that only non-local variables are added to a closure:

![](Image00222.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Closures </title>

<meta charset="utf-8">

<script>

function makeAdder(x, y) {

var z = 10;

var adder = function() {

var x = 10;

return x + y;

};

return adder;

}

var f = makeAdder(2, 3);

var result = f();

console.log("Result is: " + result);

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) and ![](Image00021.jpg) preview. In the console, open the So urces tab, and look at clo sure .ht ml :

![](Image00223.jpg)

Now, only y is in the closure. The local variable x shadows the parameter x in makeAdder() , so x is no longer needed in the closure—we'll always use the value of the local variable if we refer to x in adder() . Also, look at the console (click on the Co nso le tab); the result is now 13 instead of 5.

What do you think will happen if we refer to z in adder() ?

![](Image00222.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Closures </title>

<meta charset="utf-8">

<script>

function makeAdder(x, y) {

var z = 10;

var adder = function() {

var x = 10;

return x + y + z ;

};

return adder;

}

var f = makeAdder(2, 3);

var result = f();

console.log("Result is: " + result);

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) and ![](Image00021.jpg) . In the console, open the So urces tab, and look at clo sure .ht ml . Notice we're now adding z to x and y . Add a breakpoint to the line where we return the result of adding x , y and z (inside adder() ), like this:

![](Image00224.jpg)

Reload the page. When the execution stops, you'll see that z is now included in the closure, because it's referenced by adder() .

What do you think will happen if you remove the declaration of z , but leave the reference to z in adder() ? Try it

and see!

Each Closure is Unique

Each time you call makeAdder() , you'll get a function back that adds two numbers together. Let's make another function, g() , that adds together the numbers 4 and 5:

![](Image00225.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Closures </title>

<meta charset="utf-8">

<script>

function makeAdder(x, y) {

var z = 10;

var adder = function() {

var x = 10;

return x + y + z ;

};

return adder;

}

var f = makeAdder(2, 3);

var result = f();

console.log("Result is: " + result);

var g = makeAdder(4, 5);

var anotherResult = g();

console.log("Another result is: " + anotherResult);

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) and ![](Image00021.jpg) . In the console, you'll see that the result of calling g() ("Another result") is 9 . Now, open the So urces tab, and look at clo sure .ht ml . Add a breakpoint at the line where we return the result from adder() (line 10 in our version), and reload the page. The first time the execution stops at the breakpoint, we're calling f () , so you'll see the values 2 and 3 for x and y in the closure. Click Resume script execut io n again. Now when execution stops at the breakpoint, we call g() , so you'll see the values 4 and 5 for x and y in the closure.

In other words, f () and g() get separate closures containing different values for x and y . You can call f () again after calling g() , and you'll still get the right answer. When f () and g() are created, the values of x and y are different, so each function has a separate closure, each with different values for the variables that are in it. Remember, a closure captures the context of a function when that function is created .

![](Image00226.jpg)

Closures Might Not Always Act Like You Expect

Now, try this:

![](Image00155.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Closures </title>

<meta charset="utf-8">

<script>

function makeAdder(x, y) {

var adder = function() {

return x + y;

};

x = 10;

return adder;

}

var f = makeAdder(2, 3);

var result = f();

console.log("Result is: " + result);

var g = makeAdder(4, 5);

var anotherResult = g();

console.log("Another result is: " + anotherResult);

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) and ![](Image00021.jpg) . Look at the result in the console. The result of calling f () is now 13, and the result of calling g() is now 15\. If you still have the breakpoint at line 10, you'll see that the closure now contains the value 10 for x in both functions. That's because a closure is a reference to an object : an object that contains

the values of the variables in the scope of the function associated with the closure. So, when we call makeAdder() the first time, we create the function adder() by defining it in makeAdder() . The closure is created, and adder() gets a reference to that closure object, which contains a property named x with the value 2 (the value we passed into makeAdder() ). Before we return the adder() function value, we change the value of the property in the closure object associated with adder() . adder() still points to the same closure object, but we've changed the value in that closure object, so later, when we call f () (which is just another name for the adder() function we created when we called makeAdder(2, 3) ), we look up the value of x and find 10 instead of 2:

![](Image00227.jpg)

This is really important to understand, so look it over a couple of times. If you don't remember that the closure

associated with a function is an object, and so what's stored in the function object as the closure is actually a reference to an object , you could run into problems. If you change that object after you've created the function, that function will use the new values in the object, not the original ones.

Closures for Methods

Closures work for methods (which are just functions in objects) too:

![](Image00228.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Closures </title>

<meta charset="utf-8">

<script>

function makeAdder(x, y) {

var adder = function() {

return x + y;

};

x = 10;

return adder;

}

var f = makeAdder(2, 3);

var result = f();

console.log("Result is: " + result);

var g = makeAdder(4, 5);

var anotherResult = g();

console.log("Another result is: " + anotherResult);

function makeObject(x, y) {

return {

z: 10,

adder: function() {

return x + y + this.z;

}

};

}

var o = makeObject(2, 3);

var result2 = o.adder();

console.log("Result in o is: " + result2);

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) and ![](Image00021.jpg) . In the console, you see that the value of result 2 is 15.

Go ahead and experiment by setting a breakpoint at the return in the new makeObject () function (line 28 in our version). When you execute the code with the breakpoint in place, you'll see that when we call o .adder() the value of t his is the object o (good!) and that object contains two properties: the method adder() and the property z that has a value of 10 . The closure contains the values 2 and 3 for x and y . We don't need the value of t his.z in the closure, because we get that value from the object that contains method we're calling—that is,

     .

![](Image00229.jpg)

Using Closures

Now you know how closures work, so when are they useful. After all, it's not often that we create functions that return other functions in our everyday code. Let's look at a few examples of where closures come in handy.

Using Closures to Create Private Data

We'll start by creating a function that counts. Create a new file and add this code:

![](Image00230.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Counter </title>

<meta charset="utf-8">

<script>

function makeCounter() {

var count = 0;

return function() {

count = count + 1;

return count;

};

}

var count = makeCounter();

console.log("Counter: " + count());

console.log("Counter: " + count());

console.log("Counter: " + count());

console.log("Counter: " + count());

console.log("Counter: " + count());

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as co unt er.ht ml , and ![](Image00127.jpg) . Open the console (and reload the file if necessary) and you see:

![](Image00098.jpg)

OBSERVE:

Counter: 1

Counter: 2

Counter: 3

Counter: 4

Counter: 5

This is kind of cool because we've used a closure to encapsulate the counter variable, and the process of counting. In other words, the counter variable, co unt , is totally private, and the only way to increment it is to call the function co unt () . The co unt variable exists only within the closure for the function co unt () , so no one can come along and change the value of the counter by doing anything other than calling co unt () .

Closures as Click Handlers

So far we've looked at examples that return a function from a function, and seen how the function that is returned comes along with a closure object. Another way to use a function after the context within which the function is created has gone away is to assign a function to an object property; for instance, like when we assign handlers for events to a property in an object, like a <div>. Create a new file to look at a common use of closures—and a common mistake that goes along with it:

![](Image00231.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Closures for divs </title>

<meta charset="utf-8">

<style>

div {

position: relative;

margin: 10px;

background-color: red;

border: 1px solid black;

width: 100px;

height: 100px;

}

</style>

<script>

window.onload = function() {

var numDivs = 3;

for (var i = 0; i < numDivs; i++) {

var div = document.getElementById("div" + i); div.onclick = function() {

console.log("You just clicked on div number " + i);

};

}

};

</script>

</head>

<body>

<div id="div0"></div>

<div id="div1"></div>

<div id="div2"></div>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as divsClo sure .ht ml and ![](Image00021.jpg) . You see three red squares . Open the console and try clicking on each of the squares. Each time you do, you'll see "You just clicked on div number 3." Can you figure out why we get "3" each time, instead of the correct value for each <div> (that is, 0, 1 or 2)? Think about it for a few minutes before you go on.

First, we've got three different <div>s in the page, with the ids "div0," "div1," and "div2." We want to add a click handler to each <div>. Each click handler will do the same thing: display a message showing the number corresponding to the number in the id of the <div>. So if you click on the "div0" <div>, you'll see the message, "You just clicked on div number 0," and likewise for <div>s 1 and 2.

So, in the code, we create a for loop to iterate through the three <div>s and add a click handler to each. We use the loop variable i for the number of the <div> so we can display that number in the click handler. Notice that the click handler f unct io n that we assign to each of the <div> objects references the variable i , and i is not defined in the click handler f unct io n —it's defined in the scope surrounding the click handler f unct io n (that is, in the windo w.o nlo ad function).

So what happens? A closure is created! When we store the function value of the click handler f unct io n in the o nclick property, that function comes along with a closure that contains the variable i . Later, when you click on the <div>, the value of i will be found in the closure associated with the click handler f unct io n .

![](Image00128.jpg)

OBSERVE:

window.onload = function() {

var numDivs = 3;

for (var i = 0; i < numDivs; i++) {

var div = document.getElementById("div" + i); div.onclick = function() {

console.log("You just clicked on div number " + i );

};

}

};

That all sounds good, but it's not working right. We see 3 every time we click on any of the <div>s instead of the correct number for the <div>. Why?

Well, remember, a closure associated with a function is an object, and the function contains a reference to that closure object. So if we change the value of a variable that's captured in the closure after we create that closure, we're changing the value of the variable that will be used when we call that function later.

In this example, each time we set the click handler f unct io n to the o nclick property of a <div>, the value of i will be correct initially, but then we change the value of i the next time through the loop, which changes the value in the closure we just made.

Our loop stops iterating when the value of i is 3\. So when we call any of those click handler functions later (like when you click on a <div>), you see the value of i that was in place at the end of the loop, not the value of i that was in place when the closure was created originally.

Try using the console to add a breakpoint in the code to inspect the closure. Add the breakpoint on the line in the click handler function where we use co nso le .lo g() to display the <div> information. Click on a <div> to see the closure when the click handler function is called.

We can fix this by creating another closure. Let's see how:

![](Image00232.jpg)

CODE TO TYPE:

...

window.onload = function() {

var numDivs = 3;

for (var i = 0; i < numDivs; i++) {

var div = document.getElementById("div" + i); div.onclick = function() {

console.log("You just clicked on div number " + i);

};

div.onclick = (function(divNum) {

return function() {

console.log("You just clicked on div number " + divNum);

};

})(i);

}

};

![](Image00042.jpg) and ![](Image00021.jpg) . Try clicking on each <div> again. Now you get the correct number values for each <div>.

How does this work?

![](Image00030.jpg)

OBSERVE:

window.onload = function() {

var numDivs = 3;

for (var i = 0; i < numDivs; i++) {

var div = document.getElementById("div" + i); div.onclick = (function( divNum ) {

return function() {

console.log("You just clicked on div number " + divNum );

};

})( i );

}

};

When we assign the value of each <div>'s click handler f unct io n , we do so by executing ano t her

f unct io n that returns a function value for the click handler . T his f unct io n executes right away. It seem a little odd because we're putting the function expression in parentheses first, and after the function expression, we have another set of parentheses:

![](Image00076.jpg)

OBSERVE:

div.onclick = (function( divNum ) { ... }) ( i );

We're calling the f unct io n we just creat ed . (We'll talk more about this pattern of creating and calling a function in one step in a later lesson).

Putting the function expression in parentheses makes sure the function expression is treated as an expression, and not a function declaration. Also, we pass the value of i into the f unct io n we're calling . The value gets passed into a variable divNum , which is used by a f unct io n we're returning from the f unct io n we just called . When we return a f unct io n from a f unct io n , we create a closure that contains any variables referenced by the t he f unct io n being ret urned that are defined in the f unct io n t hat co nt ains it . In this case, both of these functions are anonymous; we're not actually giving them names like we did before with makeAdder() and adder() , but that's okay. The closure works in exactly the same way. In this case, the closure associated with the t he f unct io n being ret urned contains the value of divNum . Note that this value does not change . Even if the value of i changes, the value of divNum in the closure does not (remember that arguments are passed by value to functions, so divNum gets a copy of the value in i ).

The f unct io n t hat 's ret urned is assigned to the div.o nclick property, so it is available once the windo w.o nlo ad function has completed. That means that the values in that function's closure are also available, so when you click on a <div>, you'll get the correct number for that <div> because you're accessing the divNum variable in the closure. Add a breakpoint to the code on the co nso le .lo g() line again (line 23 in our version), and inspect the closure when you click on a <div>. You'll see the variable divNum and the correct number for the <div> you clicked on:

![](Image00233.jpg)

Using a closure like this to capture the current value of a variable by passing it to a function that returns another function is a common technique used by JavaScript programmers (and one we'll look at more in the next lesson).

Where We've Used Closures Before

Before we end the lesson, let's look at two examples from earlier in the course where we used closures.

First, take another look at the example, AdvJS/f unct io ns3.ht ml from the Functions lesson . (If you don't have this file, no worries—you can copy it in and save it as AdvJS/f unct io ns3.ht ml .)

![](Image00153.jpg) CODE TO TYPE: This code is in the file functions3.html in your AdvJS/ folder

<!doctype html>

<html>

<head>

<title> Returning Functions </title>

<meta charset="utf-8">

<script>

function makeConverterFunction(multiplier, term) { return function(input) {

var convertedValue = input * multiplier;

convertedValue = convertedValue.toFixed(2);

return convertedValue + " " + term;

};

}

var kilometersToMiles = makeConverterFunction(0.6214, "miles"); console.log("10 km is " + kilometersToMiles(10));

var milesToKilometers = makeConverterFunction(1.62, "km"); console.log("10 miles is " + milesToKilometers(10));

</script>

</head>

<body>

</body>

</html>

We created this example to show how to return a function from a function. The function we return from makeCo nvert erFunct io n references the two parameters: mult iplier and t erm . When we call the returned function later (as kilo met ersT o Miles() or as milesT o Kilo met ers() ), we'll use the closures associated with the two functions that captured the context—the values of the parameters when the function was defined and returned—to determine the values of those variables.

Try adding a breakpoint inside the function that's returned (within makeCo nvert erFunct io n ) so you can see the closures in action.

Let's also look again at the squaresAPI.ht ml example from the [Encapsulation and APIs lesson](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX) . In that lesson we talked about encapsluation and information hiding. We used a constructor, Square() , to create objects, but kept some of the data in the object being created private by not assigning values to properties of the object. Instead we used local variables and nested functions. (Again, if you no longer have the file squaresAPI.ht ml in your AdvJS/ folder, feel free to copy it in from here and save it as AdvJS/squares.ht ml .)

![](Image00125.jpg) CODE TO TYPE: This code is in the file squaresAPI.html in your AdvJS/ folder

<!doctype html>

<html>

<head>

<title> Squares with API </title>

<meta charset="utf-8">

<style>

.square {

background-color: lightblue;

cursor: pointer;

}

.square p {

padding-top: 35%;

text-align: center;

-webkit-user-select: none;

-moz-user-select: none;

-ms-user-select: none;

user-select: none;

}

</style>

<script>

function Square(size) {

var initialSize = size;

var el = null;

var id = getNextId();

this.grow = function() {

setBigger(10);

setColor("red");

};

this.reset = function() {

setBigger(initialSize - size);

setColor("lightblue");

};

var self = this;

display();

function setBigger(growBy) {

if (el) {

size += growBy;

el.style.width = size + "px";

el.style.height = size + "px";

}

}

function setColor(color) {

if (el) {

el.style.backgroundColor = color;

}

}

function display() {

el = document.createElement("div");

el.setAttribute("id", id);

el.setAttribute("class", "square");

el.style.width = size + "px";

el.style.height = size + "px";

el.innerHTML = "<p>" + id + "</p>";

el.onclick = self.grow;

document.getElementById("squares").appendChild(el);

}

function getNextId() {

var squares = document.querySelectorAll(".square"); if (squares) {

return squares.length;

![](Image00234.jpg)

}

return 0;

}

}

window.onload = function() {

var square1 = new Square(100);

var square2 = new Square(200);

var growButton = document.getElementById("growButton"); growButton.onclick = function() {

square1.grow();

square2.grow();

};

};

</script>

</head>

<body>

<form>

<input type="button" id="growButton" value="Grow!"> </form>

<div id="squares"></div>

</body>

</html>

The closure created by the Square() constructor is a little less obvious, but it's there. In t his.gro w() , we refer to two nested functions, set Bigger() and set Co lo r() . Both are nested functions which means they are local variables in the Square() constructor. Just like any other kind of local variable, like init ialSize or id , the values of these functions will disappear once Square() completes executing.

Because we reference these functions in t his.gro w() , the functions are added to the closure for the

t his.gro w() method. In addition, any local variables that are in scope for these two functions are also added to the closure. Why? Because those values might be needed when we call square1.gro w() and square2.gro w() , otherwise, we'd get a reference error. So both of the function values that are used directly by t his.gro w() , as well as any other variables in scope for those two functions, are added to the closure. You can inspect the closure by adding a breakpoint to one of the lines of code in t his.gro w() . When you click the Gro w button to call the t his.gro w() method of the square, you'll hit the breakpoint, and you'll be able to see the closure:

![](Image00235.jpg)

Whenever you create a function that references variables from the surrounding context, a closure is created. If you return that function from a function, or assign it to an object property, so the function is available outside of the context within which it was created, the closure comes along with the function. This means the function can "remember" the values of the variables it references. This is where the closure gets its name: a closure "closes" over the variables in scope when the function is created so it can keep them available for the function later, after the original context disappears. Think of closures as functions plus scope. If you understand scope, you'll understand closures too .

Note that closures aren't necessary for global variables, because global variables have global scope. They are available everywhere in your code, so there's no need to "remember" them in a closure.

The primary use for closures is to create private data, like we did with the counter example and with the squares example. You'll see closures used this way frequently (for example, in libraries like jQuery and Backbone.js).

Closures are notoriously tricky to wrap your head around, so take some extra time to review the lesson again and make sure you've got it. Use the Chrome console to inspect the closures you create to help you understand what's going on.

The Module Pattern

![](Image00005.jpg)

Lesson Objectives

When you complete this lesson, you will be able to:

use an Immediately Invoked Function Expression, IIFE, to create a local scope for your code.

![](Image00006.jpg)

explain how variables are accessible after the IIFE has completed by using a closure.

![](Image00006.jpg)

use the Module Pattern in the implementation of jQuery.

![](Image00006.jpg)

use the Module Pattern to create modules of code.

![](Image00005.jpg) ![](Image00006.jpg)

Module Pattern

The Module Pattern has emerged as one of the most common patterns you'll see in JavaScript. It's used by most JavaScript libraries and plug-in scripts, including libraries like Backbone.js, jQuery, YUI, Prototype, and more. You can use the pattern to keep code organized, reduce the number of globals you use, encapsulate structure and behavior, and provide a simple API for your objects. All this is possible because of closures, which you learned about in the previous lesson. In this lesson, we take a look at the Module Pattern: what it is, how it works, how it's related to closures, and how it can help you organize your code.

IIFE or Immediately Invoked Function Expressions

To understand the Module Pattern, you need to know how closures work (you've done that), how to use objects with closures to create private and public data (you've done that), and what it means to create a public API for an object (you've done that too). The only piece you don't know yet (although we did see one in the previous lesson) is the Immediately Invoked Function Expression.

Let's take a look at the simplest kind of IIFE you can create:

![](Image00150.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> IIFE </title>

<meta charset="utf-8">

<script>

(function() {

var x = 3;

})();

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as iif e .ht ml , and ![](Image00021.jpg) . You won't see anything yet because so far, our IIFE doesn't do much. We need to make it do something, but first, let's explore exactly what's going on in the code:

![](Image00033.jpg)

OBSERVE:

( function() {

var x = 3;

} ) ();

Let's break down this code into three parts. First, look at the f unct io n expressio n . This is an anonymous function (a function without a name), and all it does right now is initialize a variable x to 3.

Second, we have parent heses around the function. We put them there because we want to execut e t he

f unct io n, immediat ely , which is the third part. We need the parent heses around the function to make it a

function expression rather than a function declaration , because JavaScript will create a function declaration automatically when it sees the f unct io n keyword when you use it at the global level. If you try to execute a function declaration immediately, you'll get a syntax error (try it and see: remove the parentheses and you'll get a syntax error). By putting the parent heses around the function, we create a function expression, which we can then execute immediately by adding parent heses after the function.

That code is almost the same as this code:

![](Image00104.jpg)

OBSERVE:

function foo() {

var x = 3;

}

foo();

Here, we have a f unct io n declarat io n for the function f o o . Then we call t he f unct io n immediately after defining it.

Both these pieces of code accomplish essentially the same thing: they create a context (or scope) for the variable x . x is a local variable; it is available only inside the function scope. However, there is one key difference: in the first version, we never name the function, so no changes are made to the global object. The code executes without affecting the global object at all (it doesn't add any new variable or function definitions). In the second version, we do change the global object: we add the name f o o to it and the value of f o o is set to a function.

The first version of the code is an IIFE. The IIFE is used to create a context with a function within which you can declare variables, define functions, and execute code without affecting the global variables in your JavaScript. An IIFE is named as such because we call (invoke) the function in the same expression where we define it. In other words, we call the function expression immediately.

An IIFE can be pretty useful. For instance, you could create an IIFE that sets up a click handler for an element in your page. Modify iif e .ht ml as shown:

![](Image00236.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> IIFE </title>

<meta charset="utf-8">

<script>

(function() {

var x = 3;

var message = "I've been clicked!";

window.onload = function() {

var div = document.querySelector("div");

div.onclick = function() {

alert(message);

};

};

})();

</script>

</head>

<body>

<div>click me!</div>

</body>

</html>

![](Image00042.jpg) and ![](Image00021.jpg) . The words click me! appear in your page. Click on the text, and you see the "I've been clicked!" alert.

We've accomplished some work in the page (set up a click handler), but again, we've done it without adding anything new to the global object except for a value for the windo w.o nlo ad property. However, the other variables, x , message , and div are all private to the IIFE, and disappear once the function has finished executing when the page is loaded.

We can, however, click on the text and see the message after the IIFE has long gone. How? With a closure, of

course! Whenever we create a function that references variables defined in the surrounding context of that function, and make that function available for use outside of that context, a closure that contains the values of the variables that function needs comes with it so the function "remembers" those values.

Inside our IIFE, we assign a click handler f unct io n to the o nclick property of the <div> element. This function references the variable message , and because the function is available after our IIFE goes away (because we saved it in the <div> element's onclick property, and the <div> element doesn't go away), we get a closure along with the function. That closure contains the variable message .

![](Image00128.jpg)

OBSERVE:

(function() {

var message = "You've been clicked!";

window.onload = function() {

var div = document.querySelector("div");

div.onclick = function() {

alert( message );

};

};

})();

IIFEs are useful for getting work done while having minimal effect on the global scope. Additionally, you can use them to set up code to run later by assigning values to properties of objects, like the <div> element, that do stick around after the IIFE is gone.

The Module Pattern

Now you know everything you need to know in order to use the Module Pattern. Let's look at an example of a small program that is structured using this pattern. Create a new file as shown:

![](Image00237.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Module Pattern </title>

<meta charset="utf-8">

<script>

var counterModule = (function() {

var counter = 0;

return {

increment: function() {

counter++;

},

decrement: function() {

counter--;

},

reset: function() {

counter = 0;

},

getValue: function() {

return counter;

}

};

})();

window.onload = function() {

counterModule.increment();

counterModule.increment();

counterModule.decrement();

counterModule.increment();

console.log(counterModule.getValue());

counterModule.reset();

};

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as mo dule .ht ml , and ![](Image00085.jpg) . The value 2 displays in the console.

Let's examine this code more closely. First, we use an IIFE to create an object that manages a variable, co unt er . Unlike our previous IIFE example, we actually return a value from the function: an object that contains four methods to manage the counter. However, the counter is not part of the object that's returned. Instead, it's a local variable to the IIFE, which means that it's a private variable. Because the object's methods reference this variable, when the object is returned, we get a closure with each of the methods that contains the co unt er variable (and note that each closure references the same variable, so if one of the methods changes the value of co unt er , it will change for the entire object).

Next, we name the object that's returned. We give it the name co unt erMo dule . This is a global variable so it's available to the rest of our program to use, but note that it's the only global variable we create (other than setting the windo w.o nlo ad property to a function). The counter itself is private and accessible only using methods in the co unt erMo dule object.

This is the point of the Module Pattern: to minimize the number of global variables and functions you create in your program (preferably limiting the number to just one global object that contains everything else you need). The object you return from your IIFE contains public data and public methods, and all the private data is in the closure associated with the object's methods. So the object acts as an API to all the functionality the object provides to your page. This is the "module": an independent set of functionality that contains everything necessary to execute one aspect of the overall desired functionality in the page. In this example, our "module" is the counter: everything you need for the counter is encapsulated within the co unt erMo dule module.

As you can see, the concepts used in the Module Pattern are all concepts we've seen before: public and

private data, an API, and closures. The pattern a way to describe how to use these concepts together to structure your code a certain way. A pattern is a design; it's not an implementation. It's a guideline for how to structure your code to achieve a goal. In this case, that goal is to create a context for a set of functionality that is accessible to the page globally, but has minimal impact on the global variables in the page.

Using the Module Pattern with JavaScript Libraries

The Module Pattern is particularly useful for JavaScript libraries and widgets, because it allows you to combine code from several different sources, knowing that it's unlikely you'll overwrite variables from another library by mistake. Because the module object provides a public API for managing private data, it's also unlikely that you'll do something disastrous by accessing a variable in a way you shouldn't (if you use the API correctly).

As an example, look at how [jQuery](http://code.jquery.com/jquery-latest.js) is structured. The actual source code has some additional complexities we won't go into here, but if you look at the snippet of source code below, you'll see that the authors of jQuery use the Module Pattern to structure the code for the library. The internals of jQuery are implemented as private variables and methods, and the library functionality for you to use is exposed through the public methods in the jQuery object (also named $). In this case, once the jQuery object has been set up with everything it needs inside the IIFE, rather than returning that object, the jQuery object is assigned to two properties in the global object: windo w.$ and windo w.jQuery (so you can refer to the jQuery module using either name):

![](Image00119.jpg)

OBSERVE:

(function( window, undefined ) {

           lots of code here

           Define a local copy of jQuery jQuery = function( selector, context ) {

           The jQuery object is actually just the init constructor 'enhanced' return new jQuery.fn.init( selector, context, rootjQuery );

},

           lots more code here...

           Here is where we add the jQuery object as a global variable

           so you can access all the public properties and methods window.jQuery = window.$ = jQuery;

})( window );

Don't worry about the details of the code above (which is just a tiny snippet taken from the current version of jQuery). Just notice that the structure of the library uses the Module Pattern. Almost every JavaScript library out there uses this pattern.

If you're using multiple libraries, you might find it useful to structure your own code using the module pattern, and import the libraries into your module like this:

![](Image00033.jpg)

OBSERVE:

var myModule = (function( J$ , U$ ) {

})( jQuery , _ );

Here, we pass two arguments into our IIFE: the jQuery object (which we get when we link to the jQuery library) and the _ object, which is the name of the global object for the [Underscore](http://underscorejs.org) library. We can alias these two library objects by using different names for the parameters in the IIFE: J $ for jQuery and U$ for Underscore. You might just like these names better; but sometimes you can do this to avoid name clashes within your module.

A Shopping Basket Using the Module Pattern

Here's another example of using the Module Pattern—a shopping basket module:

![](Image00125.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Shopping Basket: Module Pattern </title>

<meta charset="utf-8">

<script>

var basket = (function() {

var basket = {};

var items = [];

//

           Add a new item to the basket.

           If item already exists, increase the count of existing item.

           Returns: number of that item in the basket.

//

function addItem(item, cost) {

for (var i = 0; i < items.length; i++) {

if (items[i].name == item) {

items[i].count++;

return items[i].count;

}

}

items.push({ name: item, price: cost, count: 1 }); return 1;

}

//

           Remove an item from the basket

           If item has more than 1 in basket, reduce count.

           If no more items left after removing one, remove item completely.

           Returns: number of that item left or -1 if item you tried

                   to remove doesn't exist.

//

function removeItem(item) {

for (var i = 0; i < items.length; i++) {

if (items[i].name == item) {

items[i].count--;

if (items[i].count == 0) {

items.splice(i, 1);

return 0;

}

return items[i].count;

}

}

return -1;

}

//

           Compute the total cost of items in the basket.

function cost() { var total = 0;

for (var i = 0; i < items.length; i++) { total += items[i].price * items[i].count;

}

return total;

}

basket.addItem = function(item, cost) {

var count = addItem(item, cost);

console.log("You have " + count + " of " + item + " in your basket."

);

};

basket.removeItem = function(item) {

var count = removeItem(item);

if (count >= 0) {

console.log("You have " + count + " of " + item + " left in your

![](Image00238.jpg)

basket.");

} else {

console.log("Sorry, couldn't find " + item + " in your basket to

remove.");

}

};

basket.cost = function() {

var totalCost = cost();

console.log("Your total cost is: " + totalCost);

};

basket.show = function() {

console.log("====== Shopping Basket =========");

for (var i = 0; i < items.length; i++) {

console.log(items[i].count + " " + items[i].name + ", " + (items

[i].price * items[i].count));

}

console.log(" ");

};

return basket;

})();

window.onload = function() {

basket.addItem("broccoli", 1.49);

basket.addItem("pear", 0.89);

basket.addItem("kale", 2.38);

basket.addItem("broccoli", 1.49);

basket.show();

basket.cost();

basket.removeItem("broccoli");

basket.cost();

};

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as basket .ht ml , and ![](Image00036.jpg) . In the console, this output is displayed:

![](Image00154.jpg)

OBSERVE:

You have 1 of broccoli in your basket.

You have 1 of pear in your basket.

You have 1 of kale in your basket.

You have 2 of broccoli in your basket.

====== Shopping Basket =========

2 broccoli, 2.98

1 pear, 0.89

1 kale, 2.38

Your total cost is: 6.25

You have 1 of broccoli left in your basket.

Your total cost is: 4.76

In our module, we have a couple of private variables: basket (the object we return as the value for the module), and it ems (an array that holds the items in your basket). We also have a few private functions that handle the functionality of managing the shopping basket: addIt em() , remo veIt em() , and co st () . Once the module is created, none of these private variables or functions will be available to the user of the module, except through the public API which is created by returning the basket object from the IIFE and storing the

resulting value in the basket global variable.

Notice that we use the same name for the local variable for the basket object and the global variable to store the finished module. This is perfectly fine.

The public API is the collection of methods in the basket object: basket .addIt em() ,

basket .remo veIt em() , basket .co st () , and basket .sho w() . These methods can be used by code that uses the basket module.

Look through the code and make sure you understand how it works and how it's structured using the Module Pattern. Keep in mind that the pattern is a design guideline , not a specific implementation, so it's expressed in code in different ways depending on the needs of the specific module you're implementing.

Why Not Just Use an Object Constructor?

So, why would you use the Module Pattern when you could just use an object constructor and achieve the same thing, like this?:

![](Image00239.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Counter Constructor instead of Module Pattern </title>

<meta charset="utf-8">

<script>

function CounterModule() {

var counter = 0;

this.increment = function() {

counter++;

};

this.decrement = function() {

counter--;

};

this.reset = function() {

counter = 0;

};

this.getValue = function() {

return counter;

};

};

var counterModule;

window.onload = function() {

counterModule = new CounterModule();

counterModule.increment();

counterModule.increment();

counterModule.decrement();

counterModule.increment();

console.log(counterModule.getValue());

counterModule.reset();

};

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as module2.ht ml , and ![](Image00085.jpg) . In the console, the same output displays as with our previous version of the counter module: 2.

Here, we use a constructor function, Counter Module() , to create exactly the same kind of object that we did before: an object with some public methods to manage the counter, which is a private variable (and accessible only through those public methods).

The difference between the two approaches is in the way we create the counter. If we use a constructor function, we need to create ac ounter Module using new Counter Module() (which is fine). Using new to create the object or using the Module Pattern to create the object accomplishes essentially the same thing.

You'd use the Module Pattern when you want just one version of the object. When we use the Module Pattern, we know that the user of the module can't instantiate multiple instances of the object, because there's no constructor. When we use a constructor, we can get many instances of the object. In the case of libraries like jQuery, Underscore, and others that use the Module Pattern, we know we'll only want one of each of these objects (having more would be pointless). So, whether you use the Module Pattern or an object constructor really depends on how you plan to use the object (or objects) you create. Do you need just one? Use the Module Pattern. Do you need many? Use a constructor.

In this lesson, you learned about the Module Pattern: a design guideline for how to structure your code to reduce the number of global variables you use, manage private data and functionality, and create a public API (through one global object) to access that private data and functionality. Because JavaScript has one global object that's shared by all the code that you write in a page, as well as any code you link to (both external libraries and your own additional code), this is a popular pattern that helps to reduce name clashes and keep the global namespace "clean." This is particularly important for large projects where you may not always know the names that are being used in other parts of the code.

The JavaScript Environment

![](Image00005.jpg)

Lesson Objectives

When you complete this lesson, you will be able to:

explore your browser's JavaScript extensions.

![](Image00006.jpg)

distinguish between the core language and the extensions provided by the environment in which your code runs.

![](Image00006.jpg)

compare how the browser runs your code depending on where you put that code in a page.

![](Image00006.jpg)

describe and distinguish the two phases the browser uses to execute JavasCript code.

![](Image00006.jpg)

explain how the event loop works.

![](Image00006.jpg)

create and handle multiple events.

![](Image00005.jpg) ![](Image00006.jpg)

JavaScript Runs in an Environment

In this course, we've been focusing on the language features of JavaScript, but there's more to it because JavaScript runs in an environment . Most of the time, that environment is the browser. We've seen a little of the interaction between JavaScript and the browser when we used JavaScript to update the DOM by adding new elements or styling elements, or getting user input from a form. In this lesson, we look closer at how JavaScript interacts with its environment, and things you need to be aware of when running JavaScript in the browser.

The Core Language, and the Environment's Extensions

JavaScript was created in 1995 (eons ago in internet time) specifically to run in the Netscape browser; JavaScript is still primarily a language for the browser. It has gotten beyond the browser though, most notably as a scripting language for PDF documents, OpenOffice, DX Studio, Logic Pro to name a few. In addition, JavaScript can now be used as a server-side language running in environments like Node.js.

JavaScript runs in an environment, and that environment is usually the browser. Depending on the environment in which JavaScript is running, there will be ways you can alter the language to manipulate that environment. If you're running JavaScript in the browser, you get extra "stuff" along with the language basics, that allows you to get data from the page, manipulate the content of the page, and even change the style of the page.

You can think of JavaScript as a language that's composed of two parts: the core language and the extensions that are supplied by the environment in which it's running. The core of the language are the syntax and semantics that control actions like how you define variables and functions, how you write loops, how you call functions, how scope works, and so on.

The extensions to the language are the parts that are supplied by the environment. Typically these parts are objects that provide a JavaScript interface for you to use in that environment. For the browser, this refers to elements like the do cument object, the windo w object, and all the properties and methods that come along with those objects.

Inspect these objects in the console:

![](Image00067.jpg)

INTERACTIVE SESSION:

        window

Window {top: Window, window: Window, location: Location, external: Object, chrom

e: Object}

Try this in Chrome. Twirl down the arrow next to the result, and you'll see a long list of the various properties of the windo w object:

![](Image00240.jpg)

Every browser will give you some representation of the windo w object if you type this into the console, but they might be a little different from one another.

Now try the do cument object:

![](Image00060.jpg)

INTERACTIVE SESSION:

document #document

<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 3.2 Final//EN"> <html>...</html>

Again, twirl down the arrow next to #do cument so you can see a display of the do cument object. The do cument object represents your web page, so when you open it up, you see the content of your page.

do cument has lots of properties and methods you can use to access the content of your page, like

get Element ById() and others. To see which properties do cument has, type "document" with a period following it:

![](Image00241.jpg)

INTERACTIVE SESSION:

document.

If you do this in Chrome, Safari, Firefox or IE, you'll see a pop up window that shows you all the properties of do cument that you can type next:

![](Image00242.jpg)

Scroll down through the list and you'll see many properties you're familiar with, as well as many you're not familiar with yet.

The do cument object is a property of the windo w object:

INTERACTIVE SESSION:

        window.document

#document

<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 3.2 Final//EN"> <html>...</html>

All of the browser-related things you'll do with JavaScript are properties of the window object. We say the window object is the global object or head object, because it gives you access to all the other objects you'll use to manipulate the browser environment. Try typing the names of these properties in the browser and see what you get (we're showing results from Chrome here):

![](Image00243.jpg)

INTERACTIVE SESSION:

        window.localStorage

Storage {2269ae85-adeb-40cb-aef0-c43e9b4940ea_popup_openPosition: "{"top":184,

"left":270}", 235486a4-943d-45a7-a1f4-31d1b4d6bae1_popup_openPosition: "{"top":1

84,"left":314}", 3437639f-10f2-4bd7-8e24-2314e5beeb6d_popup_openPosition: "{"top

":184,"left":270}", 3af686d4-ef0e-4ba4-a302-81bf2a8c23d6_popup_openPosition: "{" top":33,"left":2}", 46c2259c-fa5e-4c41-8bf7-3973fc2f678e_popup_openPosition: "{" top":184,"left":270}"...}

        window.navigator.geolocation

Geolocation {getCurrentPosition: function, watchPosition: function, clearWatch

        function}

> window.JSON JSON {}

Remember that because the window object is the global object, it's also the default object, so to access a property of the window object you don't have to type window . For instance, you can write window.alert () or just alert () , windo w.JSON , or just JSON .

You can also create and inspect elements right in the console to see which properties are supported by the various element objects in the browser. For instance, if you want to see the properties supported by the <video> element, try this:

![](Image00067.jpg)

INTERACTIVE SESSION:

       var media = document.createElement("video") undefined

        media.

We created a <video> element using the do cument .creat eElement () method. Once we have that element (in a variable, it's not added to the page), we can inspect it by typing "media" followed by a period. Just like before, a popup window appears with all the various properties that the <video> element supports. There are some different properties and methods in the list that aren't supported by other elements, or by the

do cument object. Because a video object is a DOM object, it will inherit many methods that all element objects have, but it has a few, like aut o play and lo o p , that are unique to video (and audio, which has many of the same properties as video).

How the Browser Runs JavaScript Code

When JavaScript was first added to browsers, it was purely an interpreted language. To run the JavaScript in your web page, the browser begins interpreting and executing your JavaScript, from the top down, as the page is loaded. Each line of your code is parsed by other code internal to the browser and then evaluated. The browser's runtime environment contains all of your variables, functions, and so on, so if you declare a variable x and give it the value 3, the browser creates a bit of storage in that runtime environment, and stores the value 3 there.

Interpreted languages are typically slower than compiled languages, like C, C++, Java, and C#, because they are not converted to machine code or optimized before they are run. The browser interprets each and every line of code as it gets to the next line, and has to parse each line of code just as you've written it.

For this reason, JavaScript in the browser has been notoriously slow. However, as developers began to expand the way web pages are used, and create web pages that are more like applications than static documents, browser developers began to see a huge advantage to making JavaScript faster. Think of Google Maps: we want maps to run fast so we can scroll around in the map, zoom in and out, and have the page respond quickly.

Browser developers began to build JavaScript engines into browsers that compile JavaScript code (using "Just In Time," or JIT, compilers), and turn it into a special code that could be run faster by the browser. For example, Chrome's V8 JavaScript engine compiles your JavaScript into machine code before the browser executes the code. As the browser compiles your code, it can make optimizations so that the code will run even faster.

Browsers still run your code top down (as most runtime environments do), so how you write your code hasn't changed. The way the browsers deal with your code has changed though, which has resulted in huge speed increases when you run JavaScript, so now you can write huge applications in your web pages that run fast (think of applications like Google maps and mail, Facebook, Netflix and Hulu, Evernote, Vimeo and YouTube, and many more).

![](Image00034.jpg)

| Note | To learn more about how JavaScript engines in browsers work, check out the links on the |
| [JavaScript Engine](http://en.wikipedia.org/wiki/JavaScript_engine#JavaScript_engines) Wikipedia page. |
|  |
|  |  |  |
|  |  |  |

![](Image00018.jpg)

Including JavaScript in Your Page

There are two ways to include JavaScript in your page: as embedded script in an HTML page (using the <script> element), and as a link to an external script. If you include your script (as an embedded script or as a link) at the top of your page, typically in the <head> element, the JavaScript will be executed before the browser interprets your HTML:

![](Image00030.jpg)

OBSERVE:

<!doctype html>

<html>

<head>

<title> </title>

<meta charset="utf-8">

<script>

var x = 3;

</script>

</head>

<body></body>

</html>

or

![](Image00128.jpg)

OBSERVE:

<!doctype html>

<html>

<head>

<title> </title>

<meta charset="utf-8">

<script src="external.js"> </script>

</head>

<body></body>

</html>

Place your code at the end of your page, like this:

![](Image00208.jpg) OBSERVE:

<!doctype html>

<html>

<head>

<title> </title>

<meta charset="utf-8">

</head>

<body>

<div>

Other HTML here

</div>

<script>

var x = 3;

</script>

</body>

</html>

The code will run after the rest of your page has loaded and the browser has interpreted the HTML.

We used to recommend that you add your JavaScript in the <head> of your document, but recently more developers are recommending that you add your JavaScript at the bottom, just before the closing </body> tag. As JavaScript gets larger (for more complex pages), it takes longer to download, parse, and execute the JavaScript, so the user has to wait longer to see the web page. Either way will work, but if you're writing a complex page with large JavaScript files, you may want to test your page to see if including the JavaScript at the bottom of the file leads to a better user experience.

An advantage of having your JavaScript in an external file is that if the JavaScript is used by multiple web pages, the browser will cache the JavaScript file, so it doesn't have to be downloaded multiple times. This is particularly important for library files, like jQuery or Underscore.js, which are typically used for a whole web site rather than just one page. If you use a well -known URL for the library (like the site's hosting URL, or even a [URL on Google's servers](https://developers.google.com/speed/libraries/?csw=1) ), it's likely that the user's browser already has that file cached, which will reduce the download time even more.

To see the difference between including your code in the <head> of your page and at the bottom, try this:

![](Image00150.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Script Testing </title>

<meta charset="utf-8">

<script>

var div = document.getElementById("div1");

div.innerHTML = "Testing when the browser loads a script"; </script>

</head>

<body>

<div id="div1"></div>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as t est Lo ad.ht ml , and ![](Image00021.jpg) . Open the console. You see a message, "Uncaught TypeError: Cannot set property 'innerHTML' of null."

Now move the script to the bottom of the page:

![](Image00244.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Script Testing </title>

<meta charset="utf-8">

<script>

var div = document.getElementById("div1");

div.innerHTML = "Testing when the browser loads a script"; </script>

</head>

<body>

<div id="div1"></div>

<script>

var div = document.getElementById("div1");

div.innerHTML = "Testing when the browser loads a script"; </script>

</body>

</html>

![](Image00042.jpg) and ![](Image00036.jpg) . Now there's no error in the console, and the page displays the message.

Because the browser evaluates the page from the top down, in the first version, the DOM is not ready when the browser executes your script. In the second version, the DOM has been built and the <div> that you are modifying exists in the DOM, so the script works. If you prefer to put your script in the <head> of your document, make sure any code that uses or manipulates the DOM is called from within the windo w.o nlo ad event handler. If you've been working with JavaScript for a while, you already know this, but it's worth reiterating because it's important.

The JavaScript Event Loop

Once the browser has executed your code from the top down as it loads your page, it enters into an event loop . This loop is internal to the browser. It is basically a loop that waits for events to occur. If you move your mouse, or click on an element, or request data from another website, an event will be generated. There are internal browser events as well. For instance, when the browser has finished loading the page, it generates the "load" event, which will cause your windo w.o nlo ad event handler to execute, if you've defined one.

When an event happens, the browser checks to see if you've defined an event handler for that event; if you have, that function is run. Once the function is complete, the browser begins the event loop again. This event loop continues as long as the web page is loaded.

In this phase of execution (that is, the phase when the browser is waiting for events and executing event handlers), events can happen at any time, so your event handler functions run when they're needed, not at any particular time or in a particular sequence.

You can disrupt the event handling process by writing code that takes up too much of the processing power of your browser. Take a look at the code below.

![](Image00032.jpg)

Feel free to type in the code below and try it, but be warned—you will probably need to WARNING close the browser entirely to stop the code. If you do want to try it, we recommend using a

different browser from the one you're using to read the lesson.

![](Image00018.jpg)

![](Image00245.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Script Testing </title>

<meta charset="utf-8">

<script>

window.onload = function() {

document.onclick = function() {

alert("You clicked on the web page!");

}

var div = document.getElementById("div1");

for (var i = 0; i < 100000000000; i++) {

div.innerHTML += i + ",";

}

}

</script>

</head>

<body>

<div id="div1"></div>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as script Erro r.ht ml , and ![](Image00021.jpg) . You may get an "unresponsive script" dialog box, like the one below (from Firefox):

![](Image00246.jpg)

If you do, choose the option to stop the script and you may get control of your browser back. However, your browser may become entirely unresponsive. In that case, you can force quit the browser on the Mac by pressing Opt io n+Co mmand+Escape (all at once), selecting the browser that's unresponsive, and choosing Fo rce quit . In Windows, right-click in the taskbar, select St art T ask Manager , select the browser application, and select End T ask .

Let's step through the code to see what's happening:

![](Image00131.jpg) OBSERVE:

window.onload = function() {

document.onclick = function() {

alert("You clicked on the web page!");

}

var div = document.getElementById("div1");

for (var i = 0; i < 100000000000; i++) {

div.innerHTML += i + ",";

}

}

First, we're running all the code in the windo w.o nlo ad event handler. This runs once the browser has completed loading the page, so we can access the DOM safely.

We set up a click event handler o n t he do cument . That means anywhere you click on the page will trigger this event. Once this is set up, we get t he "div1" o bject f ro m t he page , and then begin a lo o p that will add successive integers to the content of the <div> using innerHT ML . However, the loop end point is a very large number. Even for fast computers, this loop is going to take a long time.

Now, try clicking on the page if you want. The browser is so busy executing the loop that it is unlikely to recognoze the event for a while (if ever) before you see a browser error.

Change the very large number above to 10,000:

![](Image00044.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Script Testing </title>

<meta charset="utf-8">

<script>

window.onload = function() {

document.onclick = function() {

alert("You clicked on the web page!");

}

var div = document.getElementById("div1");

for (var i = 0; i < 10000 ; i++) {

div.innerHTML += i + ",";

}

}

</script>

</head>

<body>

<div id="div1"></div>

</body>

</html>

![](Image00042.jpg) and ![](Image00021.jpg) . Click on the web page as soon as it loads. You might have to wait a little while, but you'll eventually get an alert.

The Event Queue

So, it still takes a little while for the browser to get through the loop, but eventually it does, and it responds to your click. Even if you click on the page before the loop is complete, the browser doesn't forget the event, because whenever an event occurs in the browser, that event is added to an event queue . The browser handles events in order as they occur. The event queue ensures that even if multiple events are happening, and some of the handlers for those events take a while to execute, the browser eventually gets to all of them (unless an event handler takes so long that it causes the browser to display an unresponsive script dialog, or if an event handler causes an error so that your browser stops executing your script altogether).

Asynchronous Programming

Suppose you write a script that sets up a click handler for a mouse click, and also sends a request to get more data using XHR (XMLHttpRequest, also known as Ajax). Your request to get more data might be

initiated right away, but if it takes a while to get the data, the event handler that will be called once the data is received won't execute for a while. In the meantime, you can click your mouse a bunch of times and your mouse click event handler will execute.

The XHR request that you created to get more data is executed asynchronously . That is, the browser allows you to do other things while it's waiting to get the data from the XHR request. In fact, while it's waiting for the data, the browser goes back to executing the event loop so it can respond to other events. When the data you requested with XHR is finally retrieved, your XHR event handler will be executed. Compare the way the browser handles a synchronous loop, like we created above, with the way it handles an asynchronous request like XHR: The loop jams up the event loop, while the XHR request does not.

Here's a quick example that uses XHR to fetch data for your application. It also sets up a click handler:

![](Image00247.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> XHR Asynchronous Request </title>

<meta charset="utf-8">

<script>

window.onload = function() {

document.onclick = function() {

alert("You clicked on the web page!");

}

var request = new XMLHttpRequest(); request.open("GET", "data.json"); request.onreadystatechange = function(response) {

var div = document.getElementById("div1");

if (this.readyState == this.DONE && this.status == 200) { if (response != null) {

div.innerHTML = this.responseText;

}

else {

div.innerHTML += "<br>Error: Problem getting data";

}

}

else {

div.innerHTML += "<br>Error: " + this.status;

}

}

request.send();

}

</script>

</head>

<body>

<div id="div1"></div>

</body>

</html>

If you want to try this code tand see these events in action, ![](Image00042.jpg) save the file in your /AdvJS folder as

event Queue .ht ml . Create a file named dat a.jso n in the same folder. You can put any JSON data in the file, like this:

![](Image00076.jpg)

OBSERVE:

[ "test data" ]

![](Image00021.jpg) Preview the event Queue .ht ml file. [ "t est dat a" ] appears in the web page. You can click on the page to see the alert.

Our data is small so it doesn't take much time to retrieve, so the browser will load your JSON data far too fast for you to be able to click on the page before it does. Still, you can see from the code that we're setting up two events: one will occur whenever you click the mouse, and the other will occur when the data in the file "data.json" has been retrieved. We have no way of knowing which will occur first (but we can make an educated guess because you can't click the mouse fast enough). If you never click the mouse, then the

mouse click event will never happen.

If you replace the small amount of data here with a much larger amount of data, you might be able to delay the loading long enough to click the mouse. Give it a try if you want.

Remember, JavaScript in the browser is event-driven ; once the browser has loaded and executed your code in the first phase (as it loads the page), the second phase responds to events, which makes your web pages interactive.

Also keep in mind that some actions, like XHR requests, are executed asynchronously . We set up XHR event handlers like we do other kinds of event handlers: by assigning a function to a property on an object, in this case, the XMLHttpRequest object. The event handler is called when the data requested by the XHR request has been returned to the browser. We don't know precisely when the event will occur, and because the browser doesn't stop the event loop while it's waiting for the data, we can continue to interact with the browser and run other code.

JavaScript in Environments Other Than the Browser

You're using JavaScript in the browser, but much of what you've learned in this course applies to JavaScript in other environments as well..

For instance, if you're writing a JavaScript script for Photoshop, the main entry point for access to the Photoshop environment is the app object. For more about writing JavaScript for Photoshop, check out the links here: [http://www.adobe.com/devnet/photoshop/scripting.html](http://www.adobe.com/devnet/photoshop/scripting.html) . Of course, other Adobe products also offer scripting capabilities.

Another JavaScript environment that is rising in popularity is [Node.js](http://nodejs.org/api/) . Node.js allows you to run JavaScript at the command line, and you can use Node.js to serve web pages and run web services. If you download and install Node.js, you can experiment with it by running no de at a command line. Interact with it just like you would the JavaScript console in the browser, execpt that you won't have all the built-in browser objects; instead, you'll have built-in Node.js objects . Here's a sample interactive session from my own computer (you won't be able to reproduce this unless you install Node.js, which is not necessary for this course; we're just showing this session in case you're interested):

![](Image00248.jpg)

INTERACTIVE SESSION:

[elisabeth-robsons-mac-pro]% node

       var i = 3; undefined

        i

3

       console.log("i is " + i) i is 3

undefined

        require("os")

{ endianness: [Function],

hostname: [Function],

loadavg: [Function],

uptime: [Function],

freemem: [Function],

totalmem: [Function],

cpus: [Function],

type: [Function],

release: [Function],

networkInterfaces: [Function],

arch: [Function],

platform: [Function],

tmpdir: [Function],

tmpDir: [Function],

getNetworkInterfaces: [Function: deprecated],

EOL: '\n' }

        os.arch()

'x64'

        os.uptime()

28466

As you can see, the first part of this session looks just like a session in the browser's JavaScript console.

However, about half way through we write require("o s") . This loads a Node.js module , which is just a library of JavaScript code (similar to if you linked to a library like jQuery from a web page) . Once we've loaded this module, we have access to another object, o s , that can give us information about the operating system on which we're we're running Node.js. JavaScript can't do this in the browser because the JavaScript in the browser executes in a sandbox : a special area of the browser that protects your system from any code that is downloaded and executed in the browser (which helps to prevent JavaScript viruses).

If you want to explore another JavaScript environment, you'll find that you can apply much of the information you've learned so far to that environment, but you'll also need to learn about the environment's extensions to understand how to use JavaScript within that environment.

The JavaScript objects that browsers provide for you to manipulate the browser are based largely on specifications written by the [W3C](http://w3.org) (the World Wide Web Consortium). While most browser manufacturers have agreed that we are all better off if browsers support the same features (so we don't have to write different code for different browsers), various browser makers are always thinking up cool new features to add. Some of these features make it into the specifications and are implemented by the other browsers, and some do not.

All of the browser extensions we've talked about in this course are supported by the most recent versions of all the major browsers. To use cutting-edge features that are being added into browsers, test for those features, either by writing the test code yourself, or by using a JavaScript library like [Modernizr](http://modernizr.com) . Testing for features rather than a specific browser ensures that your code will be forward-compatible: that is, if a user doesn't have a browser that supports that feature now, they may in the future, so your web applications will work for them.

Libraries, like [jQuery](http://jquery.com) and [Underscore.js](http://underscorejs.org) (and many others), can also help with browser compatibility. These libraries provide what are called "shims" that provide fallback behavior for features that aren't supported by all browsers.

To learn more about the specifications that (largely) determine which features browsers support, check out the [W3C TR page](http://www.w3.org/TR/) (start at the DOM, DOM events, and JavaScript APIs TRs and go from there). In addition, each browser maker will have documentation on their sites about features supported by each of their individual browsers:

[Safari Developer Center](https://developer.apple.com/devcenter/safari/index.action)

![](Image00006.jpg)

[MDN Developer Network](https://developer.mozilla.org/en-US/)

![](Image00006.jpg)

[Chrome Developer Site](https://developers.google.com/chrome/)

![](Image00006.jpg)

[IE Developer Site](http://msdn.microsoft.com/en-us/ie/aa740469.aspx)

![](Image00006.jpg)

[Opera Developer Site](http://www.opera.com/developer)

![](Image00006.jpg)

ECMAScript 5.1

![](Image00005.jpg)

Lesson Objectives

When you complete this lesson, you will be able to:

describe the most recent version of the standard on which JavaScript is based, ECMAScript 5.1.

![](Image00006.jpg)

use strict mode to prevent common mistakes.

![](Image00006.jpg)

explore new methods added in ES5.

![](Image00006.jpg)

use object property descriptors to control access to objects.

![](Image00006.jpg)

create objects based on your own prototypes.

![](Image00005.jpg) ![](Image00006.jpg)

The ECMAScript Standard for JavaScript

JavaScript has a [convoluted history](http://www.w3.org/community/webed/wiki/A_Short_History_of_JavaScript) , but the good news is that all the major browsers now (mostly) support a standard version of JavaScript. With a standard for the core language and standard for the browser extensions (as we talked about in the previous lesson), working with JavaScript is much better now than in the old days when we had to write different JavaScript for each different browser. What a mess that was!

The standard for the core JavaScript language is described in the EMCAScript specification, maintained by the ECMA International organization, an international, private (membership-based), non-profit standards organization for information and communication systems. The current version of the ECMAScript standard for JavaScript is 5.1\. You [can find the specification of the standard at http://www.ecma-international.org/publications/standards/Ecma-262.htm](http://www.ecma-international.org/publications/standards/Ecma-262.htm) [[PDF] . (An](http://www.ecma-international.org/publications/standards/Ecma-262.htm) [HTML version](http://www.ecma-international.org/ecma-262/5.1/) [is also available).](http://www.ecma-international.org/publications/standards/Ecma-262.htm)

Version 5.1 (which we often refer to as ES5) of the standard was completed in 2011; major browsers implement much of the standard today. Fortunately, version 5.1 is completely backward-compatible with the previous version (3.1; don't ask what happened to version 4), so you don't have to unlearn anything to learn the new stuff in version 5.1\. Here's a handy [compatibility table](http://kangax.github.io/es5-compat-table/) that describes browser support for various ES5 features. We'll experiment with some of these features in this lesson, so make sure you've got the most recent version of your favorite browser installed.

There are quite a few minor changes in the ES5 version of the language, a few interesting additions to Objects, and a new strict mode that we'll explore. Keep in mind that the language specification is for the core language, and does not refer to the browser extensions we explored in the previous lesson.

Strict Mode

Despite what we just said about not having to unlearn anything for ES5, there are a few things you can do in JavaScript that you really shouldn't be allowed to do . (You haven't been doing those things in this course, but it's a good idea for you to know about them.) Some of these quirks have been deprecated in ES5\. That means they are no longer supported in the language, but browsers will still let you do them (as part of the backwards compatibility with the previous version of the standard). Here's an example:

![](Image00203.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> </title>

<meta charset="utf-8">

<script>

myVar = "I'm not declared!";

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save this in your /AdvJS folder as strict .ht ml , and ![](Image00021.jpg) . Open the console and type the command shown:

![](Image00069.jpg) INTERACTIVE SESSION:

myVar

"I'm not declared!"

You see the value of the string in the variable myVar . The problem with this code is that you didn't declare the variable myVar . As we discussed earlier in the course, this is not good. We always want you to declare your variables. Also, try to keep the number of global variables you use to a minimum.

ES5 has introduced a new mode, called strict mode , to help you catch these errors. When you are in strict mode, you can't assign a value to a variable that hasn't been declared. Here's how you put your code into strict mode:

![](Image00249.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> </title>

<meta charset="utf-8">

<script>

"use strict";

myVar = "I'm not declared!";

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) and ![](Image00021.jpg) . In the console you see this error (or something similar if you're using a browser other than Chrome):

![](Image00076.jpg)

OBSERVE:

Uncaught ReferenceError: myVar is not defined

In strict mode, you're not allowed to make this mistake. To fix the mistake, add the "var" keyword in front of the variable:

![](Image00249.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> </title>

<meta charset="utf-8">

<script>

"use strict";

var myVar = " I'm not I am declared!";

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) and ![](Image00021.jpg) . In the console, you no longer see the error, and you can type "myVar" and see its value.

You can use "use strict" at the global level, as well as inside individual functions . If you put "use strict" at the global level, it affects all your code. If you put it inside a function only, it will affect just the code in that function. So you could put all your strict code into an IIFE, like this:

![](Image00250.jpg)  CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> </title>

<meta charset="utf-8">

<script>

"use strict";

var myVar = "I am declared!";

(function() {

"use strict";

innerMyVar = "I'm not declared in this function either."; })();

</script>

</head>

<body>

</body>

</html>

![](Image00087.jpg) and ![](Image00036.jpg) . In the console, you'll see a reference error. You can fix it by adding "var" in front of the variable innerMyVar .

Let's look at one other way that strict mode can help prevent mistakes:

![](Image00251.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> </title>

<meta charset="utf-8">

<script>

(function() {

"use strict";

var innerMyVar = "I'm not declared in this function either.";

var o = {

           3,

           10

};

})();

</script>

</head>

<body>

</body>

</html>

We added an object, o , and we defined the property o .x twice in the object definition. Let's see what happens

in strict mode. ![](Image00042.jpg) and ![](Image00021.jpg) . In the console, you see an error (in Chrome):

![](Image00043.jpg)

OBSERVE:

Uncaught SyntaxError: Duplicate data property in object literal not allowed in s trict mode

Previously, it was perfectly allowable to define the same property twice in an object (although not a good idea). Try it and see what happens (you can try it by commenting out the "use strict "; line with //). In strict mode, we can't do this anymore, and the browser generates an error that describes the problem.

Strict mode can help you write cleaner and better code. Strict mode will help you with other tasks as well; check out the [MDN Developer Network's strict mode page](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions_and_function_scope/Strict_mode) for more.

The way we tell the browser to use strict mode might seem a little odd; after all, it's just a string, "use strict."

Why do you think the language designers decided to do it this way?

Thhey did it this way because so that older browsers that don't support strict mode could safely ignore the statement. To older browsers, "use strict" is simply a string and won't affect how your code runs at all. To newer browsers, of course, the string causes the browser to go into strict mode. This means you can use strict mode in your code without worrying that older browsers won't be able to run the code. However, pay particular attention if you are linking to multiple scripts in your page. You can combine scripts if they are all strict, or all non- strict, but you can't mix the two! Make sure you know the mode of all of your scripts use before linking to them.

New Methods

There are a few new methods that have been added to objects in the language. Let's check out some of the most useful of them.

For strings, the trim() method is now part of the language. Browsers have implemented this for a while. The useful trim() method removes white space at the beginning and ending of a string:

![](Image00059.jpg)

INTERACTIVE SESSION:

| > var s = "   Lots of white space here | "; |
| undefined |  |  |
| > s | " |  |
| " | Lots of white space here |  |
| > | s.trim() |  |  |
|  |  |  |  |

"Lots of white space here"

Nice! It's possible to implement a t rim() function yourself, as you saw in an earlier project, but it's so much nicer to have it built into the language.

There are some new array methods too:

![](Image00061.jpg)

INTERACTIVE SESSION:

       var a = [1, 2, 3]; undefined

        a

[1, 2, 3]

       a.forEach(function(x, i, a) { a[i] = x + 1; }); undefined

        a

[2, 3, 4]

Here, we define an array a , and then use the f o rEach() method to apply a function to each element of the array. (This may seem familiar to you, since you've already implemented your own f o rEach() function earlier in the course.) f o rEach() takes a function, and applies that function to each element of the array to change it. The three parameters of the function are x (the value of the current array item to which the function is being applied), i (the index of the current array item), and a (the array itself). Our function adds 1 to each item in the array. Notice that the f o rEach method doesn't return anything, but (in this case) our function modifies the array directly.

Now let's try the map() method (you've seen this before):

![](Image00059.jpg)

INTERACTIVE SESSION:

       var b = a.map(function(x) { return x * 2; }); undefined

        b

[4, 6, 8]

        a

[2, 3, 4]

map() applies a function to each item in the array, and creates a new array out of the return values from the function. Here, we multiply each item in a by 2, and store the resulting values in a new array named b . Notice that a doesn't change.

ES5 defines a few other useful array methods you should check out, including isArray() , every() , so me() , f ilt er() and reduce() .

Object Property Descriptors

In ES5, objects are quite a bit more complex. Fortunately, you don't have to change the way you create and use objects. These new features are useful, but definitely not required.

The big change in objects is that an object property now comes with a property descriptor . In fact, assuming you're using a browser that implements the ES5 standard for JavaScript, the objects you've been creating in this course all have properties with property descriptors, you just didn't know it. You already know that an object property has a value. In addition, properties now have three other attributes: writable , enumerable , and configurable . These three attributes are all optional, and are all true by default. Let's check them out:

![](Image00060.jpg)

INTERACTIVE SESSION:

       var o = { x: 1 } undefined

        Object.getOwnPropertyDescriptor(o, "x")

Object { value: 1, writable: true, enumerable: true, configurable: true }

We define a simple object o , with just one property o .x which has the value 1.

Then we use a method of Object (which, remember, is the parent object of all other objects in JavaScript), Object .get Own Property Descriptor() to get the property descriptor for the property x . We pass in both the object and the name of the property (as a string) as arguments to the method, and get back the property descriptor.

The property descriptor shows the value of the property, 1, as well as the values for the attributes writable, enumerable, and configurable. Let's talk about these attributes.

If writ able is t rue , then you can change the value of an attribute:

![](Image00060.jpg)

INTERACTIVE SESSION:

       o.x = 10 10

        o

Object { x: 10 }

Just like you'd expect, that's the default behavior. So, what if you want to change it? There are a couple of ways you can do that. One is to modify the attributes of the property descriptor directly using an Object method, Object .def inePro pert y() . We'll try this approach now, but there's a simpler way to change an object to prevent its properties from being writable that we'll look at a bit later.

![](Image00059.jpg)

INTERACTIVE SESSION:

       Object.defineProperty(o, "x", { writable: false }); Object { x: 10 }

        o.x = 20;

20

        o.x

10

The Object .def inePropert y() method takes three arguments: the object whose property you want to modify, the property name (and note that this is a string), and an object with the attribute you want to modify. In this case, we've passed an object setting the writable attribute to false . We then try to change the value of

the property o .x to 20, and we can't; the value of o .x is still 10 . Note that we don't get an error! The assignment is simply ignored. That's because we're not using strict mode in the console. Let's try the same operation using strict mode. Modify strict .xml as shown:

![](Image00252.jpg)

CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> </title>

<meta charset="utf-8">

<script>

(function() {

"use strict";

var innerMyVar = "I'm not declared in this function either.";

var o = {

           3 ,

           10

};

Object.defineProperty(o, "x", { writable: false }); o.x = 20;

})();

</script>

</head>

<body>

</body>

</html>

Here, we define an object o , change the property x so that it's not writable, and then attempt to set the value of

x to 20 . ![](Image00042.jpg) and ![](Image00036.jpg) . In the console, you see this error (in Chrome):

![](Image00043.jpg)

OBSERVE:

Uncaught TypeError: Cannot assign to read only property 'x' of #<Object>

So, in strict mode, attempting to set the value of a property that's not writable will generate an error; if you're not in strict mode, the assignnment will fail, but you won't get an error (and your code will continue to execute) . We'll continue to work in the console, but we'll note where an operation that's ignored in the console would generate an error in strict mode.

Keep in mind that when you modify an attribute of a property using Object .def inePro pert y() , you're not modifying an attribute of the entire object ; you're modifying only an attribute of a specific property in the object. Every property that you add to the object will have its own set of attributes. Let's try adding a new property to

     :

![](Image00071.jpg)

INTERACTIVE SESSION:

var o = { x: 10 } undefined

Object.defineProperty(o, "x", { writable: false }); Object {x: 10}

o.y = 20;

20

o

Object.getOwnPropertyDescriptor(o, "x");

Object { value: 10, writable: false , enumerable: true, configurable: true }

Object.getOwnPropertyDescriptor(o, "y");

Object { value: 20, writable: true , enumerable: true, configurable: true }

First we add a new property to o ; that works as usual. Then we display the property descriptors for the two properties. You can see that o .x is not writable, while o .y is (because writ able is t rue by default).

Okay, we've explored the writ able attribute, now what about enumerable ? This property indicates that you can enumerate the property when you loop through the object's properties (or use one of the new Object methods to display properties). Let's give it a try:

![](Image00059.jpg)

INTERACTIVE SESSION:

o

for (var prop in o) { console.log(prop); }

x y

⋖ undefined

Our object o has two properties and both are currently enumerable (take a look back at the enumerable attribute for both properties above, and you'll see that both attribute values are true). That means when we enumerate them by looping through all the property names in the object using the f o r loop above, we can see both property names.

ES5 has added two other methods for enumerating object property names: Object .keys() and

Object .get OwnPropertyNames() . Let's try both of these methods to enumerate the property names in o :

![](Image00060.jpg)

INTERACTIVE SESSION:

Object.keys(o); ["x", "y"]

Object.getOwnPropertyNames(o); ["x", "y"]

In both cases, the result is an array of property names. These new methods for retrieving the property names of an object (added in ES5) are really efficient. When you use them, you don't have to write a loop to access each property name.

Now, let's try making the o .y property's enumerable attribute false :

![](Image00124.jpg)

INTERACTIVE SESSION:

Object.defineProperty(o, "y", { enumerable: false }); Object { x: 10 }

o

Object.getOwnPropertyDescriptor(o, "y");

Object { value: 20, writable: true, enumerable: false , configurable: true }

Object.keys(o);

["x"]

Object.getOwnPropertyNames(o); ["x", "y"]

First, we set the enumerable attribute of o .y to false . You can see right away that when we display the object, we no longer see the y property. That means the Object .t o String() method can't "see" properties that aren't enumerable.

We get the property descriptor for o .y and see that indeed, the enumerable attribute has been set to f alse . When we use the Object .keys() method to retrieve the property names in the object o , we no longer see "y" in the resulting array. So the Object .keys() method can't "see" properties that aren't enumerable either.

Finally, we use the Object .get OwnPropertyNames() method to get the property names and again we see "y" in the results.

So, we have a way of hiding property names when an object is displayed, or when we try to enumerate the property names with any method except Object .get OwnPropertyNames() .

Now, let's look at the configurable attribute. Once you set this attribute to false, you can't change it back because the property is no longer configurable. If a property isn't configurable, it can't be deleted from the object.

![](Image00091.jpg)

INTERACTIVE SESSION:

        o.z = 3;

3

        o

       Object.defineProperty(o, "z", { configurable: false }); Object {x: 10, z: 3}

        o.z = 4;

4

        o

       delete o.z false

        Object.defineProperty(o, "z", { configurable: true });

TypeError: Cannot redefine property: z

First, we add a new property, o .z and set its value to 3\. Then we change the o .z property's configurable attribute to false . We can still change the value of the property, which we do, setting it to 4, but we can't delete the property, or set its configurable attribute back to true .

![](Image00034.jpg)

| Note | Attempting to delete a non-configurable property in strict mode generates the error: Uncaught |
| TypeErro r: Cannot delete property 'z' o f #<Object > |
|  |

![](Image00018.jpg)

These attributes allow you to have a lot more control over your objects' properties.

Sealing and Freezing Objects

There are two shortcut methods you can use to set property descriptor attributes and help protect your objects.

The first of these is Object .seal() . This method sets the configurable attribute of every property in the object to f alse , and also disallows the addition of any new properties to the object. You can still read, write, and enumerate the properties in the object; you just can't remove properties or add new ones.

![](Image00253.jpg) INTERACTIVE SESSION:

var myObject = {

name: "Elisabeth",

course: "Advanced JavaScript",

year: 2013

};

undefined

myObject

Object {name: "Elisabeth", course: "Advanced JavaScript", year: 2013}

Object.getOwnPropertyDescriptor(myObject, "name");

Object {value: "Elisabeth", writable: true, enumerable: true, configurable: true }

Object.getOwnPropertyDescriptor(myObject, "course");

Object {value: "Advanced JavaScript", writable: true, enumerable: true, configur

able: true}

Object.getOwnPropertyDescriptor(myObject, "year");

Object {value: 2013, writable: true, enumerable: true, configurable: true}

Object.seal(myObject);

Object {name: "Elisabeth", course: "Advanced JavaScript", year: 2013}

Object.getOwnPropertyDescriptor(myObject, "name");

Object {value: "Elisabeth", writable: true, enumerable: true, configurable: fals e}

Object.getOwnPropertyDescriptor(myObject, "course");

Object {value: "Advanced JavaScript", writable: true, enumerable: true, configur

able: false}

Object.getOwnPropertyDescriptor(myObject, "year");

Object {value: 2013, writable: true, enumerable: true, configurable: false}

myObject.newProperty = "attempting to add a new property"; "attempting to add a new property"

myObject

Object {name: "Elisabeth", course: "Advanced JavaScript", year: 2013}

Object.keys(myObject);

["name", "course", "year"]

myObject.name = "Scott";

Object {name: "Scott", course: "Advanced JavaScript", year: 2013}

First, we define a new object, myObject , with three properties: name , course , and year . By default, the attributes in the property descriptor for each of these properties are true , which we can see by inspecting them using Object .get Own Property Descriptor() . (Unfortunately, there's no way to see the property descriptors of all the properties at once).

Next, we "seal" the object, by calling Object .seal() , and passing in the object myObject . This changes the co nf igurable attribute of each of the properties to f alse .

We try to add a new property to the object, myObject .newPro pert y . We don't get an error message when we try to do this (because we're not in strict mode), but the assignment is ignored, and the property is not added to the object. When we use the Object .keys() method to display the property names in the object, we can see that no new property is added.

Finally, we change the value of the myObject .name property from "Elisabeth" to "Scott," just to prove that even if the object is sealed, we can still change the value of the properties.

![](Image00032.jpg)

If you try to add a new property to myObject (which is sealed) in strict mode, you'll get the error Note message Uncaught Type Erro r: Can't add property new Property, object is not

extensible .

![](Image00069.jpg) ![](Image00018.jpg)

You can check to see if an object is sealed using the Object .isSealed() method:

INTERACTIVE SESSION:

       Object.isSealed(myObject) true

A similar method is Object .f reeze() . It works like Object .seal() , but in addition, it sets the writable attribute of all the property descriptors to false , so you can't change the value of properties:

![](Image00059.jpg)

INTERACTIVE SESSION:

        Object.freeze(myObject);

       myObject.name = "Elisabeth" "Elisabeth"

        myObject

Object {name: "Scott", course: "Advanced JavaScript", year: 2013}

You can find out if an object is frozen using the Object .isFro zen() method.

![](Image00032.jpg)

If you try to set the value of a property in a frozen object in strict mode, you'll get the error Note message Uncaught Type Error: Cannot assign to read only property 'name' of

#<Object > .

![](Image00018.jpg)

The Object .seal() and Object .f reeze() methods are useful for protecting your objects while still allowing access to the properties (both for reading the value of the properties and for enumerating the properties).

Both Object .seal() and Object .f reeze() disallow new properties from being added to objects by setting them to non-extensible . You can do this yourself (separately) using the Object .prevent Extensio ns() method, and determine whether an object is extensible using the Object .isExt ensible() method.

We left the description of these recent capabilities of JavaScript objects until the end of the course because they are recent additions and as such are not used much yet. Still, it's important to know that they are available if and when you do need them. You probably will in certain situations like when you want to make sure that an object is protected from change. In addition, it's likely that these features will be used in future additions to the language.

Creating Objects

Another new method of Object that was added in ES5 is the Object .creat e() . You already know how to create objects by writing a literal object, and by using a constructor.

Object .creat e() is a little different because it allows you to create an object and specify its prototype. So if you create an object, like the Perso n object below, you can then create objects that use Person as their prototype (meaning those objects inherit the properties and methods of the Person object):

![](Image00254.jpg) CODE TO TYPE:

<!doctype html>

<html>

<head>

<title> Creating Objects </title>

<meta charset="utf-8">

<script>

var Person = {

welcome: function() {

console.log("Welcome " + this.name + "!");

},

isAdult: function() {

if (this.age > 17) {

return true;

}

}

};

var bob = Object.create(Person);

bob.name = "Bob Parsons";

bob.age = 42;

bob.welcome();

if (bob.isAdult()) {

console.log(bob.name + " can get a beer");

}

var mary = Object.create(Person);

mary.name = "Mary Smith";

mary.age = 12;

mary.welcome();

if (!mary.isAdult()) {

console.log("Sorry, " + mary.name + " can't get a beer");

}

</script>

</head>

<body>

</body>

</html>

![](Image00042.jpg) Save the file in your /AdvJS/ folder as creat eObject s.ht ml and ![](Image00021.jpg) . Open the console; you see:

![](Image00104.jpg)

OBSERVE:

Welcome Bob Parsons!

Bob Parsons can get a beer

Welcome Mary Smith!

Sorry, Mary Smith can't get a beer

We made these variables global so you can access them in the console. Try this:

![](Image00141.jpg) INTERACTIVE SESSION:

Person.isPrototypeOf(bob) true

Person.isPrototypeOf(mary) true

bob

Object {name: "Bob Parsons", age: 42, welcome: function, isAdult: function}

mary

Object {name: "Mary Smith", age: 12, welcome: function, isAdult: function}

The Person object is the prototype of both bob and mary , and those objects do indeed inherit the properties from Person . (So, what happens when you use Object .keys() to get the property names of bob and mary ? Why?)

However, note that because we created bo b and mary using Object .creat e() and not a constructor, when you look at the constructor of bo b like this:

![](Image00064.jpg)

INTERACTIVE SESSION:

bob.constructor

function Object() { [native code] }

bob

Object {name: "Bob Parsons", age: 42, welcome: function, isAdult: function}

...you can see that the constructor is Object () . bo b and mary are created using the Object () constructor behind the scenes and then explicitly changing the prototype object to Perso n . You can see this reflected also when we display bo b in the console: you see "Object" as the "type" of the object, even though the prototype of the object is Perso n .

Whenever you create an object using a constructor, that object gets a prototype that is stored in the constructor's pro t o t ype property. Recall that we created a circle by writing new Circle() , and the resulting object's prototype was the Circle object in Circle .pro t o t ype . Contrast that way of creating objects with using Object .creat e() . Object .creat e() allows you to assign the prototype of an object without (explicitly) using a constructor (although the Object () constructor is used behind the scenes).

In addition, with Object .creat e() you can pass a second argument to the method containing an object that specifies attributes for the properties:

![](Image00255.jpg) INTERACTIVE SESSION:

       var jim = Object.create(Person, { name: {

value: "Jim Smith",

writable: false

}, age: {

value: 42,

writable: false

}

});

undefined

       jim.name "Jim Smith"

        jim.age

42

       jim.welcome() Welcome Jim Smith! ⋖ undefined

       jim.isAdult() true

       jim.name = "Joe Schmoe" "Joe Schmoe"

        jim.welcome()

Welcome Jim Smith!

Here, we create a new object using Object .creat e() , and pass the Perso n object to use as the prototype.

We also pass an object that defines the values of the properties and their attributes for the new object.

Because we set both properties so they are not writable, we can't change the values in the object jim .

![](Image00034.jpg)

| Note | If you try to change the value of jim .name in strict mode, you see the error message Uncaught |
| TypeError: Cannot assign to read only property 'name' of #<Object > . |
|  |

![](Image00018.jpg)

So, Object .creat e() gives you an efficient way to create a prototype chain for objects in JavaScript.

In this lesson, you've learned about some of the new features of JavaScript that were added in ES5 (or ECMAScript 5.1 specification). If you're running the most recent version of a modern browser, then it's likely you can use all of these new features.

Developers are already hard at work on the ECMAScript 6 specification for the next version of JavaScript (code-named Harmony). You can see the specification in progress at the [ECMAScript wiki](http://wiki.ecmascript.org/doku.php?id=harmony:specification_drafts) . As of this writing, the creation of the new specification is underway, so many of the new features are not available in browsers. The changes will be more extensive than the changes in ES5, including the addition of block scope, classes, and modules. Exciting!

You've come a long way in this course, exploring much of the JavaScript language including types and values, functions, objects, and closures. You've also worked with techniques for programming such as using the Module pattern to reduce global variables and keep parts of objects private. Well done! We look forward to seeing what you do in your final project!

Copyright © 2015 Johnkeats Arthur.

.
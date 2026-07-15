![](Images/cover00161.jpeg)

![](Images/image00109.jpeg)

CONTENT ![Web design](Images/image00110.jpeg)

1.  WWW AND WEBSITES
2.  HTML
3.  CSS
4.  JAVASCRIPT
5.  BOOTSTRAP

Chapter 1

World Wide Web and Websites

Word Wide Web is one of the most revolutionary ideas which has revolutionized the field of Computer Science. In 1990, Tim Berners-Lee developed the foundation for the World Wide Web. The whole web works on a basic system. This whole system has two sides. The first one is the Server Side which refers to the data centres and the servers of the websites that you are trying to reach. And secondly, the client-side refers to your local computer and its IP address.  And the work of connecting these two sides is done by browsers like Chrome, Firefox, Opera, etc. It can be demonstrated by the following diagram.

![Introduction to the server side - Learn web development | MDN](Images/image00111.gif)

Now you know that every computer has an IP address same goes with websites every website has an IP address but because it’s very difficult for any human being to remember the addresses. So, to resolve this problem web addresses and URLs were introduced to the World Wide Web. For example, google.com. Here google.com is the web address and 8.8.8.8 is the IP for the google.com website. Every website has and web address and IP address.

A website consists of two things the first one is known as Front – End and the second one is known as Back – End. The front–end refers to the material and the content which is visible on any website. For front-end development, we generally use HTML and CSS but for a high-level frontend with lots of animation and content, we also use JavaScript. And for the back-end, there are backend programming languages. Most websites use PHP because it is easy to program and is highly effective. We can use other programming languages also like we can use JavaScript, Python, etc. The time taken by a website to load is dependent on its server the more powerful the server-id the faster the website loads.

When we enter any URL in the browser, we send the request to the server of that website to send the files of HTML CSS, and JavaScript so that the browser can access it and show the content to us. Not every website is made using HTML but whether a website is made in any programming language to make it display, it is converted to HTML and JavaScript. For example, google.com was mainly written in C, C++, and Python but when you see the page source of the website it shows you in form of HTML.

The first website which was obviously made by Tim Berners-Lee was http://info.cern.ch/ which looks like this

![](Images/image00112.jpeg)

Chapter 2

HTML

HTML is an abbreviation for Hypertext Markup language because it is the standard markup language for Web sites. Now you will ask where to write this code. So, to make a website you can either write the code in any text editor or you can use notepad also. I will personally recommend you Visual Studio Code it is free and can be used as a text editor and console also to test your equations and codes in other programming languages.

*   How to identify whether it is an HTML file or not

So, to identify the type of file we use the help of the extension of any file. For example, the extension for HTML files is .html and .htm and for CSS it is .css and same for JavaScript it is .js. You have to add the extension while saving the file on your PC. Have a look at the basic code of HTML. 

<!DOCTYPE html>

<html lang="en">

<head>

    <title>Brajesh Thakur</title>

</head>

<body>

    <! -- The content will be written here -->

</body>

</html>

As you can see that the code is started with the word DOCTYPE which denotes that the document is an HTML document. In the second it mentioned that the language of the code is English. In HTML one of the most important things is tags like in the above example <head> is a tag.

The starting tag is written between less than and greater than sign < here >. There are many tags in HTML Some of them are <div>, <p>,  <section>, <html> , <footer>, <li> etc. Every tag has its own properties. In HTML all of the code that is to be to displayed is written in <body> tag

*   HTML Headings.

There are heading tags in HTML which is denoted but six tags <h1> to  <h6>. Here the greater the number is the smaller the text size will be of that heading for example <h1> is the heading with the largest font size and the <h6> tag has the smallest font – size. See the image below for the demonstration

CODE

<!DOCTYPE html>

<html lang="en">

<head>

    <title>Brajesh Thakur</title>

</head>

<body>

    <h1>This is H1 tag</h1>

    <h2>This is H2 tag</h2>

    <h3>This is H3 tag</h3>

    <h4>This is H4 tag</h4>

    <h5>This is H5 tag</h5>

    <h6>This is H6 tag</h6>

</body>

</html>

RESULT

![](Images/image00113.jpeg)

*   HTML paragraphs

Because HTML has a heading so it also has paragraphs. For paragraphs we use the <p> tag. The code will same and the result will also be displayed the same as the previous one as headings.

CODE

<!DOCTYPE html>

<html lang="en">

<head>

    <title>Brajesh Thakur</title>

</head>

<body>

    <p>This the paragraph tag</p>

</body>

</html>

*   HTML Comments.

Sometimes while making a big project we feel a requirement to write something which should not be displayed while loading the web page. So here we use comments. Comments are started with <! –  and end with -->.

*   HTML Attributes.

In HTML all elements or tags have an attribute. All the attributes are written with the starting tag.

*   The href attribute

The href attribute is used for <a> tags also known as anchor tags which are used to create hyperlinks in the webpage. It defines where the URL is leading to. Below you can see how you can use it on your website.

CODE

<!DOCTYPE html>

<html lang="en">

<head>

    <title>Brajesh Thakur</title>

</head>

<body>

    <a href="youtube.com">This Link is leading to YOUTUBE</a>

</body>

</html>

Here you can see that in the href attribute I have added a link to YouTube. So, whenever this anchor tag is clicked, it will lead to youtube.com. Mostly anchor tag is used as a button. You can add any type of link in this href attribute. There are many more attributes like src and alt which are used with <img> tags.

*   <br> tags

<br> tag is used in between paragraphs it helps to create a break at a point in a line.

CODE

<p> This is a demo text in this text I will add a break tag here <br> now this is going to start from a new line </p>

*   HTML CSS

Many times, while building our websites we have to style only two to three elements so here in place of building a new CSS file, we can use CSS in the HTML file itself. There are two methods of doing that.

The first one is Inline CSS

In inline CSS we use CSS attribute in HTML elements. The use of inline CSS is like the following.

 <h1 style="color: blue;">A Blue Heading</h1>

The second one is Internal CSS

In internal CSS we use one of the HTML elements <style> mostly it is used in the header part of the document. The use of internal CSS is like the following.

<head>

<style>

h1 {color: blue;}

</style>

</head>

Using CSS, you can edit all the properties of any elements in HTML. Like font size, font, color, breadth, fill, text alignment, and many more.

*   HTML TEXT FORMATTING

There are mainly ten text formatting elements in HTML. Which helps us to format the text. The name of those ten elements is given below.

*   <b>                Makes text bold
*   <strong>       Refers important words.
*   <i> Italic text
*   <em> Emphasized text
*   <mark> Marked text
*   <small>          Smaller text
*   <del>              Deleted text
*   <ins> Inserted text
*   <sub> Subscript text
*   <sup>             Superscript text

*   HTML QUOTATION AND CITATION ELEMENTS

The HTML Quotations are used to create a quotation in HTML. There are many types of quotations for a small quote we use the <q> tag and many more. Some of them are

*   <abbr>: This is an abbreviation tag that is used to show an abbreviation or acronym. Like “Mr.”, “Mrs”.

*   <address>:  This defines the address information of the author of that document.

*   <bdo>:  bdo stands for Bi-Directional Override. It helps in changing the direction of the text. For example, for the right to the left direction we write rtl, and for the left, to right we use ltr as a value for the dir attribute. It is used as follows.

<bdo dir="rtl">This text will be written from right to left</bdo>

*   <blockquote>:  It is used to define a section that is quoted from another source

.

*   <cite>:  This defines the title of creative work. It changes the text to italic.

*   <q>:  This defines a short inline quotation.

*   HTML COLOR AND ITS USE

While building projects we use color several times. The colours in HTML are used in three forms.

*   RGB:  RGB stands for red green and blue. In this, we set the value of all three colors in an exact amount so that a new color can be formed. The values for all these three colours lie between 0 to 255 For example in RGB code for yellow is written as (255,255,0). Here first value stands for the shade of red color second one for green shade and third one for blue shade.
*   HEX: In this format, colors are in hexadecimal form. Every shade has a different color. The hexa code is always written with ‘#’ this sign. For example, the hexa code for white is #ffffff and for black is #000000\. In Hexa, the first two digits control the red shade and the middle two digits control the green shade and the last two controls the blue shade.

*   HSL:   In this format, the colors are made by adjusting the hue saturation and lightness. The values for saturation and lightness are in percentage but the valuer of hue is in degrees from 0 to 360 and hue is the one that is responsible for the color change.

*   HTML Hyperlink and anchor tag

Every website has a hyperlink or a button that helps the visitors to be redirected to another web page link. In HTML there are three types of links. The properties of these three types of links are default but can be changed later.

*   An unvisited link is underlined and blue.
*   A visited link is underlined and purple.
*   An active link is underlined and red.

You can edit the properties of these three types of links as follows. This will be edited with the help of  CSS.

<style>

a: link {
  color: green;
  background-color: transparent;
  text-decoration: none;
}

a: visited {
  color: pink;
  background-color: transparent;
  text-decoration: none;
}

a: hover {
  color: red;
  background-color: transparent;
  text-decoration: underline;
}

a: active {
  color: yellow;
  background-color: transparent;
  text-decoration: underline;
}

</style>

As other elements have their attributes same goes with anchor tag it also has an attribute named target. This attribute can have the following values.

*   _self:        Default. Opens the document in the same window/tab as it was clicked.
*   _blank:  _  Opens the document in a new window or tab.
*   _parent:    Opens the document in the parent frame.
*   _top:          Opens the document in the full body of the window.

The code can be written as

<a href="https://www.youtube.com/" target="_blank">Visit YouTube</a>

If we are using a URL, we should know that there are two types of URLs. The first one is Absolute URL and the second one is relative URLs.

1. Relative URL: Relative URLs are those which are present in the folders of your website.

2. Absolute URL: Absolute URLs are those which are from some other website.

Examples

<h1>Absolute URLs</h1>
<p><a href="https://www.youtube.com/">Youtube</a></p>

<h1>Relative URLs</h1>
<p><a href="/css/style.css">CSS FILE</a></p>

*   HTML IMAGES

Images are not technically inserted into a web page; images are linked to web pages. We can adjust the width and height of the image by using CSS. The <img> tag creates a holding space for the referenced image. Image can be linked by the following code.

<img src="URL" alt="alternate text">

In the place of the URL, you have to insert the relative link of the image. And we have to fill in the name or context of the image in the value for the alt attribute. Sometimes because of a slow internet connection sometimes the images don’t load so this text will replace the image.

*   HTML FAVICON

Have a look at the image given below where the logo of the website is visible against the title of the Webpage. This image or logo is known as a favicon. This favicon adds a new touch to your webpage as well as it helps the visitor to find out weather the website is loading or it has been loaded.

![](Images/image00114.jpeg)

To add the favicon to your webpage you should first save the favicon image with the extension of .ico at a file with any name at the root repository. This code should be written in the head tag. In today’s world almost all the browsers support favicon. In favicon, we use a link tag to link a document with an external source.

<head>
  <title>My Page Title</title>
  <link rel="icon" type="image/x-icon" href="/images/favicon.ico">
</head>

*   HTML TABLE

We can also add tables in HTML and then style them by using CSS. We arrange the data in the table in rows and columns. For making a cell in the table we use the <td> tag. The code for a basic table is given on the next page.

<body>

    <table style=” width:100%”>

        <tr>

          <th>Name</th>

          <th>Class</th>

          <th>Section</th>

        </tr>

        <tr>

          <td>Ram</td>

          <td>7th A</td>

          <td>A</td>

        </tr>

        <tr>

          <td>Shyam</td>

          <td>9th</td>

          <td>B</td>

        </tr>

      </table>

</body>

For styling, you can add a border to all the elements of table like given below.

<style>

table, th, td {

  border:1px solid black;

}

</style>

There are many more tags used for making a new table.

*   <table>:    This tag defines a table.
*   <th>: This tag defines the header cell of the table.
*   <tr>: This tag defines a row in the table.
*   <td>: This tag defines a cell in the table.
*   <caption>: This defines a table caption
*   <colgroup>: This specifies a group of columns in the table.
*   <col>: It refers to a column that is present in colgroup.
*   <thead>: It groups all the header content of the table.
*   <tbody>: It groups the content of the body in a table.
*   <tfoot>: It groups all the footer content of the table.

*   HTML TABLE COLSPAN AND ROWSPAN

For example, you want to make a cell bigger so that it captures the space of two cells so you can use colspan and rowspan. These are also attributes that are used for <th> element. For expanding towards columns, you should use colspan and for expanding to rows you should use rowspan. You can enter the number of cells in which you want to expand that specific share. And the code will be as given below.

<table style="width: 100%">

        <tr>

            <th colspan="2">Name</th>

            <th>Age</th>

        </tr>

        <tr>

            <td>Brajesh</td>

            <td>Thakur</td>

            <td>13</td>

        </tr>

        <tr>

            <td>Naresh</td>

            <td>Kumar</td>

            <td>42</td>

        </tr>

    </table>

The result will be like this here you can see that the cell on the top left corner, its width is equal to the width of 2 cells.

![](Images/image00115.jpeg)

*   HTML LISTS

HTML allows web developers to use lists while making their websites. It helps them to add data properly to the document. There are two types of lists in HTML. The first one is an ordered list and the second one is an unordered list.

*   Ordered List:  An ordered list starts with the <ol> tag. Each list item starts with the <li> tag. The list items will be marked with numbers by default. The code and result is shown below.

![](Images/image00116.jpeg)<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>

*   Unordered List: An unordered list starts with the <ul> tag. Each list item starts with the <li> tag. The list items will be marked with bullets (small black circles) by default. The code and result are shown below.

![](Images/image00117.jpeg)<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>

There are many more types of lists in HTML. All of them are mentioned down below.

*   <dl>: This defines a description list type.
*   <dt>: This defines a term in description list.
*   <dd>: This describes a term in description list.

*   BLOCKS AND INLINE ELEMENTS

Every HTML element has a default display value, depending on what type of element it is. There are two display values: block and inline.

*   BLOCK ELEMENTS

A block-level element always starts on a new line, and the browsers automatically add some space (a margin) before and after the element. A block-level element always takes up the full width available. There are two elements that are commonly used. <p>, <div>. The <p> element defines a paragraph in an HTML document. The <div> element defines a division or a section in an HTML document. All of the block elements are

[<address>](https://www.w3schools.com/tags/tag_address.asp) , [<article>](https://www.w3schools.com/tags/tag_article.asp) , [<aside>](https://www.w3schools.com/tags/tag_aside.asp) , [<blockquote>](https://www.w3schools.com/tags/tag_blockquote.asp) , [<canvas>](https://www.w3schools.com/tags/tag_canvas.asp) , [<dd>](https://www.w3schools.com/tags/tag_dd.asp) , [<div>](https://www.w3schools.com/tags/tag_div.asp) , [<dl>](https://www.w3schools.com/tags/tag_dl.asp) , [<dt>](https://www.w3schools.com/tags/tag_dt.asp) , [<fieldset>](https://www.w3schools.com/tags/tag_fieldset.asp) , [<figcaption>](https://www.w3schools.com/tags/tag_figcaption.asp) , [<figure>](https://www.w3schools.com/tags/tag_figure.asp) , [<footer>](https://www.w3schools.com/tags/tag_footer.asp) , [<form>](https://www.w3schools.com/tags/tag_form.asp) , [<h1>-<h6>](https://www.w3schools.com/tags/tag_hn.asp) , [<header>](https://www.w3schools.com/tags/tag_header.asp) , [<hr>](https://www.w3schools.com/tags/tag_hr.asp) , [<li>](https://www.w3schools.com/tags/tag_li.asp) , [<main>](https://www.w3schools.com/tags/tag_main.asp) , [<nav>](https://www.w3schools.com/tags/tag_nav.asp) , [<noscript>](https://www.w3schools.com/tags/tag_noscript.asp) , [<ol>](https://www.w3schools.com/tags/tag_ol.asp) , [<p>](https://www.w3schools.com/tags/tag_p.asp) , [<pre>](https://www.w3schools.com/tags/tag_pre.asp) , [<section>](https://www.w3schools.com/tags/tag_section.asp) , [<table>](https://www.w3schools.com/tags/tag_table.asp) , [<tfoot>](https://www.w3schools.com/tags/tag_tfoot.asp) , [<ul>](https://www.w3schools.com/tags/tag_ul.asp) , [<video>](https://www.w3schools.com/tags/tag_video.asp).

*   INLINE ELEMENTS

An inline element does not start on a new line. An inline element only takes up as much width as necessary. There is an element that we use in our daily life which <span>. It doesn’t need a new line either it fits in that same line in the provided dimensions. All of the inline elements are

[<a>](https://www.w3schools.com/tags/tag_a.asp) , [<abbr>](https://www.w3schools.com/tags/tag_abbr.asp) , [<acronym>](https://www.w3schools.com/tags/tag_acronym.asp) , [<b>](https://www.w3schools.com/tags/tag_b.asp) , [<bdo>](https://www.w3schools.com/tags/tag_bdo.asp) , [<big>](https://www.w3schools.com/tags/tag_big.asp) , [<br>](https://www.w3schools.com/tags/tag_br.asp) , [<button>](https://www.w3schools.com/tags/tag_button.asp) , [<cite>](https://www.w3schools.com/tags/tag_cite.asp) , [<code>](https://www.w3schools.com/tags/tag_code.asp) , [<dfn>](https://www.w3schools.com/tags/tag_dfn.asp) , [<em>](https://www.w3schools.com/tags/tag_em.asp) , [<i>](https://www.w3schools.com/tags/tag_i.asp) , [<img>](https://www.w3schools.com/tags/tag_img.asp) , [<input>](https://www.w3schools.com/tags/tag_input.asp) , [<kbd>](https://www.w3schools.com/tags/tag_kbd.asp) , [<label>](https://www.w3schools.com/tags/tag_label.asp) , [<map>](https://www.w3schools.com/tags/tag_map.asp) , [<object>](https://www.w3schools.com/tags/tag_object.asp) , [<output>](https://www.w3schools.com/tags/tag_output.asp) , [<q>](https://www.w3schools.com/tags/tag_q.asp) , [<samp>](https://www.w3schools.com/tags/tag_samp.asp) , [<script>](https://www.w3schools.com/tags/tag_script.asp) , [<select>](https://www.w3schools.com/tags/tag_select.asp) , [<small>](https://www.w3schools.com/tags/tag_small.asp) , [<span>](https://www.w3schools.com/tags/tag_span.asp) , [<strong>](https://www.w3schools.com/tags/tag_strong.asp) , [<sub>](https://www.w3schools.com/tags/tag_sub.asp) , [<sup>](https://www.w3schools.com/tags/tag_sup.asp) , [<textarea>](https://www.w3schools.com/tags/tag_textarea.asp) , [<time>](https://www.w3schools.com/tags/tag_time.asp) , [<tt>](https://www.w3schools.com/tags/tag_tt.asp) ,[<var>](https://www.w3schools.com/tags/tag_var.asp).

*   HTML CLASSES

HTML class attribute is used to specify a class to an element. Because we use a same element thousands of times in a document. So, to style a single element it would be impossible but because of class attribute you can do it easily. By this attribute we can name an element and can access it with that name in stylesheets and js files. We will briefly study it later in this book.

To style it in CSS we use a dot before adding the name of the class then we can edit the properties of that class. The name of the classes is case sensitive, means that Imp and imp are two different classes. We can give same class name to different elements If we want to give same properties to two different elements, we can give one common class to them and them give the properties to that class. An element can also have more than one classes just write both of them with a white space in between.

In this below given code the span has given class named imp.

<!DOCTYPE html>
<html>
<head>
<style>
.note {
  font-size: 120%;
  color: red;
}
</style>
</head>
<body>

<h1>My <span class="imp">Important</span> Heading</h1>
<p>This is some <span class="imp">important</span> text. </p>

</body>
</html>

*   HTML ID

The HTML id attribute is used to specify a unique id for an HTML element. You cannot have more than one element with the same id in an HTML document. An id attribute is always denoted with # for accessing in stylesheet and js files’ attribute is also case sensitive. Both class and Id are used for giving a name to an element but one difference between Id and classes is that classes can be common but Id should always be unique. Id also helps you to create a new link of a position in the document and the user can jump to that position by using anchor tag. See the code below to know how it works with anchor tag.

<a href="book.html#imp">What’s important</a>

*   HTML IFRAMES

Have you ever seen a website in a website or a video or pdf embedded in a webpage? So how the developers do this so the developers use iframe element to do so. The syntax for embedding documents is like given below.

<iframe src="URL of the document" title="about the url "></iframe>

*   HTML FILE PATH

File path is the name of the location of any file or folder to access it in HTML we use src attribute. You can see the table below to know about path and its usage. File paths are used to link other files with your document. They can be images CSS files or Js files.

![](Images/image00118.jpeg)

*   HTML HEAD TAG

The HTML <head> element or <head> tag is a container for the following elements: <title>, <style>, <meta>, <link>, <script>, and <base>.

The <head> element is a container for metadata (data about data) and is placed between the <html> tag and the <body> tag. HTML metadata is data about the HTML document. Metadata is not displayed. Metadata typically define the document title, character set, styles, scripts, and other meta information. Metadata helps us to make a website responsive as well. Style elements is also present in <head> tag only. One example of metadata that you have seen in html files is given below. It makes our website beautiful and spreads in the width of the device.

<meta name="viewport" content="width=device-width, initial-scale=1.0">

*   HTML RESPONSIVE DESIGNS

Responsive web design is about creating web pages that look good on all devices! A responsive web design will automatically adjust for different screen sizes and viewports. Either it will automatically adjust to the screen size or we will have to do it manually. It helps us to get more and more visitor from any screen size. Mainly there are three screen sizes first one is pc second one is tablet and third one is smartphone.

![Responsive website design - adapt, respond and overcome](Images/image00119.jpeg)

Responsive Web Design is about using HTML and CSS to automatically resize, hide, shrink, or enlarge, a website, to make it look good on all devices (desktops, tablets, and phones).

To make website responsive you should first setup the view port by adding meta tag in the head tag. We always want that our website should responsive so whenever you add an image you should make a habit to give it 100% width. This will decrease your effort while making your websites responsive. The code will be like this

<meta name="viewport" content="width=device-width, initial-scale=1.0">

This all is very stressful and it needs a lot of hard work you there is one CSS framework which reduces our effort but I will not recommend to use bootstrap till you are fully expert in web development and now wants to make more website to serve your clients in less time. We will cover bootstrap later on in this book.

*   HTML CHARACTER ENTITIES

As you might know that we can not add more than one white space in HTML so you can use different characters to create more than one white – space. So if you want to add character to your html file you will have to add a meta tag defining charset Some of the character entities are.

*   &nbsp;     creates white space.

*   &lt;            is used for “<” less than sign.

*   &gt;           is used for “>” greater than sign.

### o &copy;      is used for creating ©.

The meta code for charset looks like this.

<meta charset="UTF-8">

*   HTML FORMS

You must have seen that most of the websites contains forms it can be for any reasons whether for revie for comment or for complaint etc. You can create forms in HTML using <form> element. This is the basic code for a form in HTML.

<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname">
</form>

*   HTML FORMS ATTRIBUTES AND ELEMENTS

In HTML same as other elements form element also have some attributes in it that are used for making it easy for styling it in css and for working of the form. As you can see here, we have used a new element named label it is used to add a label to the input as you can see it below in the result. And in the type attribute we can add different values to it like for checkboxes we can add “checkbox” in the value for the attribute type. Same for radio buttons you can add radio as the value for type attribute.

![](Images/image00120.jpeg)

Don’t you see one thing missing in it. Yes, that’s the submit button. You can add submit button to any form by simply writing the following code.

<input type="submit" value="Submit">

*   HTML FORMS ACTION AND METHOD ATTRIBUTE

Now this form will be filled by the user but how will we get all this information that the user has filled. So we have to link an file which will connect our website to our database. So we can do it from many languages like python, PHP etc. Mostly in web development we use PHP so in action attribute we have to fill the name of the PHP file as the value for it.

Now the second attribute in HTML forms is method attribute now this attribute also has many values. First, we should know about it. So, it’s the method by which the data will transferred from your client’s browser to your data base. So, all the values for this method attribute are

*   GET
*   POST
*   PUT
*   HEAD
*   DELETE
*   PATCH
*   OPTIONS
*   CONNECT
*   TRACE

Most of the backend developers prefers POST because post is more secure than GET and GET method can be easily hacked or accessed by anyone. The information entered in the GET method form is stored in the browser. So, while making your website and its form always try to use POST method.

*   HTML MEDIA

We can add many types of videos with any extension in HTML. Mostly our videos are in MP4 and MPEG format so we can add videos with these extension in our webpage. Same with audio files. Audio files extensions like MP4, MP3 and .ogg are also supported by HTML. You can add videos to your webpage with video element and audio with audio element. You can use autopay attribute to make the file play automatically when someone opens that page. The basic code for adding a video is like given below.

<video width="320" height="240" controls>
  <source src="video.mp4" type="video/mp4">
</video>

Now in the above code you can see that we have used video element and given width and height using both attributes. And the other attribute named controls doesn’t need any value and it gives all the control to the videos like play, timeline, options etc. At last, the track element. The track element is used for adding subtitles to the video the extension for the subtitle its. vtt the result will look like this

![](Images/image00121.jpeg)

*   HTML YOUTUBE VIDEO EMBEDING

You must be wondering that how most of the websites uses YouTube videos and embed them in their websites. You can do this with the help of iframe element. It’s very difficult to write the embed link for the YouTube video. That’s why google has added a feature to YouTube from that you can get the iframe code for embedding the YouTube video to our web page.

![](Images/image00122.jpeg)

Just click on the share icon one the YouTube website. And the above given screen will come now click on embed icon one link will appear copy that link and paste it in your website. From here the visitor can play the video from your website only or can even go to YouTube through this link. From here he can subscribe to the channel whose video you have embedded. The result will be like given in the next page.

![](Images/image00123.jpeg)

*   HTML GOOGLE MAPS EMBEDDING

![](Images/image00124.jpeg)Same as you embedded the YouTube video you can embed Google maps in your web pages. Maps can be used while giving your businesses location and other contact details. So you have to do the same as YouTube. Just enter your location and one panel will open at the right side there you will find share icon click on that and then click on “embed a map”. As shown in the image below. The result will also be the same. Zoom by Ctrl and + and viewing full map.

Chapter 2

CSS

CSS is the abbreviation for Cascading Stylesheet. It’s a stylesheet programming language that helps web developers to style their html document and make it attractive that will help them to get more and more visitors to their website. The extension for a CSS file or document is .css. This file should be first linked to the HTML document with the following code which uses link element to link these both files. One think that you should make sure is that both CSS and HTML files should be saved in same folder.

<link rel="stylesheet" href="styles.css">

The basic CSS code looks like this

h1 {
  color: black;
  text-align: center;

}

p[[BT1]](#part0029.xhtml__cmnt1) {
  font-family: verdana;
  font-size: 20px;
}

Here in the above code, we have given two properties to h1 and paragraph element. Like for heading tag we have giver color black and text align center. And for paragraph tag we have set a font- family it means we have set a font named ‘verdana’. And we have set a font size of 20px to the paragraph. 

![](Images/image00125.jpeg)

The syntax of CSS looks like this

You can use element name, id name or class name as a selector in CSS. For using ID as a selector in CSS we use ‘#’ before the name of the id. And for using class name as a selector, we use a dot before the name of the class. You can select a specific class for a specific element like given below.

p. heading {
  text-align: left;
  color: black;
}

There is one more selector in CSS named universal selector. It helps us to select the whole document and give it the properties. It can be used to give a common font to the whole document. Now you can use the universal selector by using “ * ” symbol.  Now if you want to give same properties to two or many different elements. You can edit them together it is called CSS group selector. Like shown below in the code. Here we are giving same properties to two different properties.

h1, h2, p {
  text-align: left;
  color: black;
}

*   WAYS TO USE CSS

There are three methods of using/ inserting CSS in your HTML file. First one in inline CSS that we have discussed earlier in this book. Second one is Internal CSS.  In this method we use <style> element and write all the code that we want to enter in the css file. And the last one is external CSS. In this css we use external css file with an extension .css. And to link it with the HTML file we write the link code in the head tag.

*   COMMENTS IN CSS

As we learned earlier that in HTML there are comments same goes with CSS. So, the comments in CSS looks like this.

/*This is a comment */

*   BACKGROUND COLOR

To add background color to a image you have to follow he same syntax and use attribute background-color and as an value to it write a colour name. You can add the color in all the forms HEX code or RGB or HSL. To increase or decrease the opacity of the background colour either you can use background color in the form of RGBA through it by controlling the alpha value you can control the opacity of the background. But without ignoring the fact that finding RGB of a colour is difficult so you can write the colour name and to control the opacity you can add opacity attribute. The value of this attribute lies between 0 to 1\.

*   BACKGROUND IMAGE

Now sometimes background colour doesn’t make our websites look attractive so using CSS properties we can add a background image to any element in CSS. We just have to use url attribute and the code will look like this.

div {
  background-image: url("bg.jpg");
}

Now sometimes the dimension of the element is more than the dimension of the background image. So browser automatically starts repeating the image. So we uses property named background repeat. Now if you want that the imager should not repeat you can add the value as no-repeat. If you want that the image should repeat horizontally you can add the value as repeat-x. If you want that the image should only repeat vertically you can add a value as repeat-y.

div {
 background-image: url("bg.png");
  background-repeat: repeat-x;
}

*   BORDER PROPERTIES

You can add borders to elements of HTML using CSS properties. The border-style property specifies what kind of border to display. The values that can be filled to this property are as follows.

*   dotted -     Defines a dotted border.
*   dashed -   Defines a dashed border.
*   solid -       Defines a solid border.
*   double -    Defines a double border.
*   groove -    Defines a 3D grooved border. The effect depends on the border-color value.
*   ridge -       Defines a 3D ridged border. The effect depends on the          border-color value.
*   inset -       Defines a 3D inset border. The effect depends on the border-color value.
*   outset -     Defines a 3D outset border. The effect depends on the border-color value.
*   none -       Defines no border.
*   hidden -    Defines a hidden border.

The code of using all these properties is like below.

div {border-style:

 dotted;

}

All the result of these properties are shown in the next page.

![](Images/image00126.jpeg)

You can also add color to the borders that we have applied to the HTML elements. By using border-color property. The code for the same is given below.

div {
  border-style: solid;
  border-color: blue;
}

In CSS you can edit every single side’s border of an element. The for it will be as follows.

p {
  border-top-style: solid;
  border-right-style: dotted;
  border-bottom-style: groove;
  border-left-style: ridge;
}

You can also write all these four lines of code in one line as

p {
  border-style: solid dotted groove ridge;
}

The result for the above code will look like this

![](Images/image00127.jpeg)

*   CSS MARGINS

In css margin refers to the space between and element to another element. And using CSS properties we can edit the value of margin of an element. The value for margin is calculated in pixels. One centimetre is around thirty-seven pixels. The margin can be controlled from all four sides by using the following code.

p {
  margin-top: 25px;
  margin-bottom: 50px;
  margin-right: 750px;
  margin-left: 100px;
}

The whole code can be written in a nutshell in a single line of code.  Which is like as follows.

p {
  margin: 25px 50px 75px 100px;
}

You can also set margin to auto which will horizontally center it in its div or container.

*   CSS PADDING

Padding can be defined as the gap or space between the element itself and its border. And the remaining things like syntax and values are same as CSS Margin. Its syntax looks like this

p {
  padding-top: 25px;
  padding -bottom: 50px;
  padding -right: 750px;
  padding -left: 100px;
}

Same like Margin you can write all these four lines of code in one line.

p {
  padding: 25px 50px 75px 100px;
}

*   CSS HEIGHT AND WIDTH

Every element requires its dimension. In CSS you can give every element its height and width. In CSS height and width is controlled by some values which I have described below.

*   Auto -           This is default. The browser calculates the height and width
*   Length -        Defines the height/width in px, cm etc.
*   Percentage - Defines the height/width in percent of the containing block
*   Initial -          Sets the height/width to its default value
*   Inherit -        The height/width will be inherited from its parent value

The syntax of the code for adding properties related to height and width looks like below.

div {
  height: 150px;
  width: 54%;
  background-color: red;
}

*   Max height:  It sets the height of the element to the max.
*   Max width: It sets the width of the element to the max   
*   Min height:  It sets the height of the element to the min.
*   Min width: It sets the width of the element to the min.  

*   THE CSS BOX MODEL

The CSS box model refers to the layout which clearly explains the relation between an element and its margin and padding.

![WebD2: Understanding the Box Model in CSS](Images/image00128.jpeg)

*   CSS TEXT FORMATTING

In CSS text formatting means that to add different properties to text like aligning the text, changing the font-color or changing the background colour.

*   TEXT ALIGN

Aligning text means a lot in web development it helps us to adjust more and more content in your website attractively. In text align you can many properties like

*   Text-align-last
*   Direction
*   Vertical-align

*   TEXT ALIGN LAST

The text-align-last property specifies how to align the last line of a text. The syntax of the same looks like

p{
  text-align-last: center;
}

And the result of this type of text align looks like as shown in the next page. There you can see that the whole paragraph is aligned left but the last line is aligned in center. And this is responsive too. Like if you open that webpage in mobile also you will find out that just the last line is aligned center.

![](Images/image00129.jpeg)

*   TEXT DIRECTION

The direction and unicode-bidi properties can be used to change the text direction of an element: It can be used to write display languages like Urdu which written right to left. In its syntax we have given a direction from right to left.  The syntax looks like this

p {
  direction: rtl;
}

The result looks like this

![](Images/image00130.jpeg)

*   Vertical Alignment

The vertical-align property sets the vertical alignment of an element. Like in this case it’s an image used with in the paragraph. There are many values for this vertical alignment property.  They are shown in the code below.

img.a {
  vertical-align: baseline;
}

img.a {
  vertical-align: text-top;
}

img.a {
  vertical-align: text-bottom;
}

img.a {
  vertical-align: sub;
}

img.a {
  vertical-align: super;
}

The results of the above shown code is shown in the next page there you can see that the image changes its place accordingly as from top to bottom etc.

![](Images/image00131.jpeg)

*   CSS TEXT TRANSFORMATION

The text-transform property is used to specify uppercase and lowercase letters in a text. It can be used to turn everything into uppercase or lowercase letters, or capitalize the first letter of each word: It becomes very helpful if you wrote anything in lowercase but you want that it should be in uppercase. The syntax looks like this

p {
  text-transform: uppercase;
}

*   TEXT SHADOW

The text-shadow property adds shadow to text. In its simplest use, you only specify the horizontal shadow (2px) and the vertical shadow (2px) It makes your text look more attractive. The code for it looks like this

h1 {
  text-shadow: 2px 2px red;
}

In the above code you can see that we have given 2px shadow horizontally and 2px vertically and at last we have added shadow colour as red. The result of the above written code is shown below.

![](Images/image00132.jpeg)

*   CSS FONTS

In your website font plays an important role of attraction. A strong font can create a strong identity for your website and brand. A font should be easy to read and understand and in addition to all this whichever font you choose should be attractive. Most of the websites uses ‘Arial’ font I their websites like Google, YouTube etc.

In CSS there are mainly five types of font-families.

*   Serif.
*   Sans-Serif
*   Monoscope
*   Cursive
*   Fantasy

*   Web Safe Fonts

There are some fonts which are present in every computer by default and doesn’t need internet connection or server speed. Because most of time if we use fonts from external website and the browser is unable to reach that website from where you have used those fonts. All the fonts of your websites will be gone and your website will look ugly. So that’s why you should use web safe fonts. So, whatever happens in the world the fonts will load safely, and it will not affect your website in any way. I have mentioned the list of some Web safe fonts. These are the most used Web-Safe Fonts.

1.  Arial  (sans-serif).
2.  Verdana  (sans-serif).
3.  Helvetica  (sans-serif).
4.  Tahoma  (sans-serif).
5.  Trebuchet  MS  (sans-serif).
6.  Times New Roman  (serif).
7.  Georgia  (serif).
8.  Garamond (serif).
9.  Courier New  (monospace).
10.  Brush Script MT  (cursive).

*   Font Weight

Font weight is used to control boldness. You can add values like normal or bold. The code and the result for the same is shown in the next page. 

p{
  font-weight: bold;
}

![](Images/image00133.jpeg)

*   Font Size

Same as other elements you can give properties to control text size also. You can give the value for the text size in px, and rem. One rem is equal to 16px.

*   Google Fonts

Now your website doesn’t look that much attractive with web safe fonts. So you can use external website’s fonts. The best choice for this is Google Fonts. Because this website will never go down and all the fonts that you have used in your website will be safe. Now you will think that how will we use Google fonts in our websites.

First go to fonts.google.com select a suitable font. Now just select all the variants of the font. Now you will see some links in bottom right corner. Now copy the bottom link and paste it in your head tag. This was a method that how will you add a font family in your HTML file .

![](Images/image00134.jpeg)

*   CSS LINKS

We can add properties to all the four stages of the anchor tag. The four stages are.

*   a: link -            a normal, unvisited link.
*   a: visited -       a link the user has visited.
*   a: hover -         a link when the user mouses over it.
*   a: active -        a link the moment it is clicked.

The syntax for giving all these properties to an anchor tag is given below.

a: link {
  color: red;
}

a: visited {
  color: green;
}

a: hover {
  color: blue;
}

a: active {
  color: yellow;
}

*   CSS POSITION

The position property specifies the type of positioning method used for an element (static, relative, fixed, absolute or sticky). Elements are then positioned using the top, bottom, left, and right properties. However, these properties will not work unless the position property is set first. They also work differently depending on the position value.

*   Position Static

This is the default value for position property. The elements which are static in position are not affected by top, bottom, left, right properties. The code for static position is like this

div{
  position: static;
  border: 1px #fff;
}

*   Position Relative

In this position the element is in its relative position. Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position. Other content will not be adjusted to fit into any gap left by the element.

div{
  position: relative;
  border: 1px #fff;
}

*   Position Fixed

In this position the element is fixed in its relative position. It means that weather you scroll till thje end it will never move from its place.

div {
  position: fixed;
  bottom: 0;
  right: 0;
  width: 100%;

}

*   Position Absolute

An element with position absolute is positioned relative to the nearest positioned ancestor. Absolute positioned elements are removed from the normal flow, and can overlap elements.

div {
  position: absolute;
  top: 80px;
  right: 0;
  width: 200px;
  height: 100px;
}

*   Position Sticky

If an element has given sticky as a value for the position property it will always be sticked there only it is used to make navigation bars in websites.

div {
  position: -webkit-sticky; 
  position: sticky;
  top: 0;
  background-color: black;
  border: 1px solid #fff;
}

*   Z-INDEX

The z-index property specifies the stack order of an element. Like using this property we chooses that which element should be on top and which should be one the bottom. The value of it is from infinity to infinity. The more the value of an element is the more on the top it is. Now in the following code you can see that we have given z-index -1 means that it the lowest and the image will be in the most bottom layer of the document.

img {
  position: absolute;
  margin: auto;
  top: 0px;
  z-index: -1;
}

*   CSS FLOAT

The float property is used for positioning and formatting content e.g. let an div or a image float left to a container. The float property can have one of the following values:

left -         The element floats to the left of its container.

right -       The element floats to the right of its container.

none -       The element does not float.

inherit -    The element inherits the float value of its parent.

The syntax and the result of the same looks like this

img {
  float: right;
}

![](Images/image00135.jpeg)

*   CSS DISPLAY - INLINE BLOCK

This property is used to display an element as an inline-level block container. inline-block allows to set a width and height on the element. Most of the developers uses inline block to create navigation bars.

*   CSS COMBINATOR

A CSS selector can contain more than one simple selector. Between the simple selectors, we can include a combinator. Because sometimes t access an element of HTML we have to specify its location in the document.

There are four different combinators in CSS:

*   descendant selector (space)
*   child selector (>)

*   Descendant Selector

The descendant selector matches all elements that are descendants of a specified element. The following example accessing all <p> elements inside <div> elements

div p {
  background-color: yellow;
}

*   Child Selector

The descendant selector matches all elements that the child selector selects all elements that are the children of a specified element. The following example selects all <p> elements that are children of a <div> element:

div > p {
  background-color: yellow;
}

*   CSS PSEUDO-CLASSES

A pseudo-class is used to define a special state of an element. Like we have seen in the case of anchor tag. The syntax looks like given below.

For example, it can be used to:

*   Style an element when a user mouses over it
*   Style visited and unvisited links differently
*   Style an element when it gets focus.

selector: pseudo-class {
  property: value;
}

Here the selector refers to the element whose pseudo class you are selecting. And pseudo class refers to the pseudo class of the element.

*   Anchor Pseudo-classes

As we learned earlier that anchor tag can be displayed in different ways and the code is shown in the next place. And in that code we are accessing every stage of an anchor tag. We can use pseudo classes like hover on almost every element of HTML.

a: link {
  color: white;
}

a:visited {
  color: black;
}

a:hover {
  color: yellow;
}

a:active {
  color: green;
}

*   CSS - The: first-child Pseudo-class

This pseudo class helps us to access the first use of that element in the HTML document. So we can access it easily by using first-child property.

In the following example that is shown in the next page, the selector matches any <p> element that is the first child of it.

p:first-child {
  color: blue;
}

*   CSS PSEUDO-ELEMENTS

A CSS pseudo-element is used to style specified parts of an element. There are many pseudo elements. And the syntax of using pseudo element looks like

selector::pseudo-element {
  property: value;
}

*   The:: first-line Pseudo-element

The:: first-line pseudo-element is used to add a special style to the first line of a text.. It is applicable to all the text elements. Note: The ::first-line pseudo-element can only be applied to block-level elements. The syntax is as follows.

p::first-line {
  color: #000;
}

*   The:: first-letter Pseudo-element

The ::first-letter pseudo-element is used to add a special style to the first letter of a text. The following example formats the first letter of the text in all <p> elements. The syntax is as follows in the next page. The:: first-letter pseudo-element can only be applied to block-level elements.

p::first-letter {
  color: #ff0000;
  font-size: xx-large;
}

## o The:: before Pseudo-element

The:: before pseudo-element can be used to insert some content before the content of an element. The following example inserts an image before the content of each <h1> element. All the properties that we give to this before pseudo element is displayed in the HTML document. The syntax looks like this

h1::before {
  content: url(book.png);
}

## o CSS - The:: after Pseudo-element

The ::after pseudo-element can be used to insert some content after the content of an element. The following example inserts an image after the content of each <h1> element: The syntax looks like this.

h1::after {
  content: url(book.png);
}

## o The:: selection Pseudo-element

Have you seen that when we select something in a webpage it has an different properties. By default, it is with background set to blue. You can edit all this by using the simple syntax shown in the next page.

::selection {
  color: white;
  background: black;
}

*   NAVIGATION BAR

A navigation bar needs standard HTML as a base. Having easy-to-use navigation is important for any web site. To make a basic navigation bar we used ul tag and li tag . So the HTML code looks like this.

<ul>
  <li><a href="default.asp">Home</a></li>
  <li><a href="news.asp">News</a></li>
  <li><a href="contact.asp">Contact</a></li>
  <li><a href="about.asp">About</a></li>
</ul>

And to make it more attractive we will add some basic CSS code which looks like this. Here we are removing the bullet by setting list style type none. And by margin and padding zero we are giving it the top left position.

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

In HTML every navigation bar we make is always vertical but how to make Horizontal Navigation bar. Mostly I uses the code given in the next page. In which I set display to flex which sets all them horizontally and then give some margin to it.

ul {

      background-color: rgb(14, 13, 13);

      display: flex;

      list-style-type: none;

      margin: 0;

      padding: 0;

    }

    ul li {

      color: white;

      margin-left: 20px;

      margin-right: 20px;

    }

The result of this code is something like this as shown below in the image.

![](Images/image00136.jpeg)

Chapter 4

JAVASCRIPT

JavaScript, often abbreviated JS, is a programming language that is one of the core technologies of the World Wide Web, alongside HTML and CSS. Over 97% of websites use JavaScript on the client side for web page behaviour, often incorporating third-party libraries. JavaScript is also used for server-side programming for making databases. In this book we will only earn JavaScript for frontend development only. Now fust get an introduction to JavaScript by looking at the below code.

<script>

    document. Write (“Introduction to JavaScript.”);

  </script>

The result will same as if it is written using HTML.

![](Images/image00137.jpeg)

*   USING JAVASCRIPT IN HTML

To use JavaScript in HTML we have two options either we use internal JavaScript or we can also use External JavaScript. To use external CSS we will have to use script tag and them use src attribute to locate the js file. This below given code can be written in head tag or it can also be written in body tag. The syntax looks like this.

<script src="myScript.js"></script>

And to use internal CSS we will use script tag only and write all the code inside it.

I will recommend you to use external JS file because first of all it helps to make your code look beautiful and easy to read and understand and separates HTML CSS and JS. It gives an positive impact of your code on others.

*   JavaScript Display

As we saw in the first ever example of the JS chapter, we printed a text using JS. There are many more ways to display data using JS in HTML document. We will discuss all of them one by one.

*   innerHTML

To access an HTML element, JavaScript can use the document.getElementById (id) method. The id attribute defines the HTML element. It can be <p> tag or any other text tag and the innerHTML property defines the HTML content. Here we will have to first add a <p> tag and give it an id which we can access through javascript. So the final code will look like.

<!DOCTYPE html>

<html>

<body>

<p id="web"></p>

<script>

document.getElementById("web").innerHTML = "Written using inner HTML";

</script>

</body>

</html>

The result will look same as is it is written using HTML. It is also shown in the next page.

![](Images/image00138.jpeg)

*   document. write ()

This is the second method to print anything in HTML. As well as for beginner it is very helpful because it’s syntax is easy to read and understand, just have an look on the syntax. The result will be same as the previous one. But if you add or excite document. write after the whole document is loaded it will erase everything and only the text which is filled in the JS will be visible. Like using document. write in a button can load problems for your webpage.

<p id="web"></p>

<script>
document. getElementById("web"). innerHTML = “This is written using document. write”;
</script>

*   window.alert()

You must have seen alerts coming in many forms of websites. Like before submitting any form etc. So how you can do all this, have an look to the code given below.

<script>
window.alert (4189);
</script>

The result of the alert looks as shown in the next page.

![](Images/image00139.jpeg)

*   JavaScript Print

Yes, you can directly print the webpage using one click using JavaScript. You just have to use a button and the code written below.

<button onclick="window.print ()">Print this page</button>

![](Images/image00140.jpeg)The result will look like this

After someone clicks on the button one popup will come and will give the visitor options for printing and then saving that webpage.

*   JavaScript Operations

Like any other programming language you can do every operation of mathematics using JavaScript. Like adding to words or numbers or doing other calculations like subtracting, multiplication, and division. To get start with operations first let us get introduced to Variables.

*   JavaScript Variables

Till now we were just directly printing content on the webpage. But by using variables we can create and assign values to any variable. The syntax of using variables looks like.

Var name = “value”

So in the above line of code you can see that first we will have to write var to create a variable and then assign it an unique name and then by using ‘ = ’ sign we will assign it a value. We can later on access the value by its name only. But while naming a variable you should make sure that it only contains letters, numbers and an underscore and it doesn’t start with a number.

And we can also perform all the operations with variables. Because JavaScript is a programming language so it shows it result in console. So we will have to write all the code in the text editor and see all the result in the console itself.

So lets do something basic Adding first name and last name to make a full name. So the code is like this

    var fname = "Brajesh";

    var lname = "Thakur"

    var fullname = fname + " " + lname;

And you can open console in your browser by right clicking and there it will show nothing but when you type

Console.log (nameofvariable);

It will print the value of that variable in the console.

*   JavaScript Loops

Sometimes while programming the code for our website, we run to a problem like we have to execute a code several of time. The syntax for loops are almost same in all the programming languages are same. Loop works with a simple formula first we assign a value to a variable or string. Then we set a limit how many times we want to execute that certain line of code. And then a last statement which increases the value of that variable of that loop. And then the code that should be executed is written. This type of loop is known as For Loop the syntax for this loop looks like this.

for (var i = 0; i < 10; i++) {
  console.log(“Loop is running”);

}

*   JavaScript Datatypes

Like other programming languages JavaScript also supports all the datatypes like Strings, Booleans, Numbers and more like null and undefined. We will discuss in depth about all these datatypes.

*   JavaScript Strings

Strings are useful for holding data that can be represented in text form. Some of the most-used operations on strings are to check their [length](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/length), to build and concatenate them using the + and += string operators, checking for the existence or location of substrings, or extracting substrings method. String is one of the most important datatypes of any programming language. Like if you want to get data from the user etc.

*   JavaScript Booleans

Very often, in programming, you will need a data type that can only have one of two values, like. The syntax of a Boolean looks like as easy as it is. You just have to write a yes or no calculation. Like by using comparing signs. Like “<”, “>” or “=”. Booleans are used to compare two digits etc.

*   YES / NO
*   ON / OFF
*   TRUE / FALSE

Boolean (4651 > 9465)

The results will be shown accordingly. If yes then true and if not then false.

*   JavaScript Numbers

JavaScript has only one type of number. Numbers can be written with or without decimals. Like it can be a normal number or a floating number also known as decimals. You can also solve many mathematics problems. The syntax of JavaScript numbers looks like this

let x = 3.14;    // A number with decimals
let y = 3;    // A number without decimals

JavaScript Numbers are Always 64-bit Floating Point

*   JavaScript Null

The value null represents the intentional absence of any object value. It is one of JavaScript's [primitive values](https://developer.mozilla.org/en-US/docs/Glossary/Primitive) and is treated as falsy for Boolean operations.

*   JavaScript Undefined

It refers to a variable which has been declared by us but we haven’t assigned them any value.

*   JavaScript Arrays

In every programming language array is a group of datatypes. There are many ways of declaring arrays. The most easiest way of declaring an array is this one as shown below in the code. By this method you can easily declare arrays and can add more values to it while it’s declaration.

var list = [“HTML”, “CSS”, “JavaScript”]

Now you can also know how many elements are there in an array by using. length property. The syntax of this property looks like this.

*   JavaScript Random

Using math. random, it returns a random number between inclusive and exclusive. Means between 0 and 1.

# • JavaScript Arithmetic

Arithmetic operators perform arithmetic on numbers (literals or variables).These are the operators of arithmetic in JavaScript.

![](Images/image00141.jpeg)

=

*   JavaScript Reserved words.

There are couple of words which are reserved by JavaScript and cannot be used as a name of class or variable etc. The whole list of those words are as shown in the next page.

Await , break , case , catch , class , const , continue , debugger , default , delete , do , else , enum , export , extends , false , finally , for , function , if , implements , import , in , instanceof , interface , let , new , null , package , private , protected , public , return , super , switch , static , this , throw , try , True , typeof , var , void , while , with , yield.

Chapter 5

BOOTSTRAP

Bootstrap is a free front-end framework for faster and easier web development. It includes HTML and CSS based design templates for typography, forms, buttons, tables, navigation, modals, image carousels and many other, as well as optional JavaScript plugins It also gives you the ability to easily create responsive designs. The URL of the official website of Bootstrap is

https://getbootstrap.com/

![upload.wikimedia.org/wikipedia/commons/thumb/b/...](Images/image00142.jpeg)

This is the basic code of used making form. Its not that complicated. Because there are just some extra classes that are used in HTML and those classes are powered by bootstrap and have certain properties.

<div class="mb-3">

  <label for="exampleFormControlInput1" class="form-label">Email address</label>

  <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="name@example.com">

</div>

<div class="mb-3">

  <label for="exampleFormControlTextarea1" class="form-label">Example textarea</label>

  <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>

</div>

The result of the above used bootstrap code looks something like this.

![](Images/image00143.jpeg)

First of all to use bootstrap in your website you have to add three js codes in your body tag which are like follows and are also available in the bootstraps official website.

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p" crossorigin="anonymous"></script>

<script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.10.2/dist/umd/popper.min.js" integrity="sha384-7+zCNj/IqJ95wo16oMtfsKbZ9ccEh31eOz1HGyDuCQ6wgnyJNSYdrPa03rtR1zdB" crossorigin="anonymous"></script>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.min.js" integrity="sha384-QJHtvGhmr9XOIpI6YVutG+2QOK9T+ZnN4kzFN1RtK3zEFEIsxhlmWl5/YESvpZ13" crossorigin="anonymous"></script>

*   Bootstrap Grid System

Bootstrap's grid system allows up to 12 columns across the page. If you do not want to use all 12 columns individually, you can group the columns together to create wider columns. Bootstrap's grid system is responsive, and the columns will re-arrange automatically depending on the screen size.

The Bootstrap grid system has four classes:

*   Xs  for phone screens (less than 768px).
*   Sm  for tablet screens (greater than 768px).
*   Md  for small laptop screens. (Greater than 992px).
*   Lg  for desktops (greater than 1200px).

*   Bootstrap Basic Table

A basic Bootstrap table has a light padding and only horizontal dividers. The table class adds basic styling to a table.

![](Images/image00144.jpeg)

*   Striped Rows

The .table-striped class adds zebra-stripes to a table

*   Bordered Table

The. table-bordered class adds borders on all sides of the table and cells.

*   Hover Rows

The. table-hover class adds a hover effect (grey background color) on table rows.

*   Condensed Table

The. table-condensed class makes a table more compact by cutting cell padding in half.

*   Bootstrap Images

In bootstrap using certain classes we can get different styles of images.

## o Rounded Corners

The .img-rounded class adds rounded corners to an image (IE8 does not support rounded corners).

## o Circle Image

The .img-circle class shapes the image to a circle .

## o Responsive Images

Images come in all sizes. So do screens. Responsive images automatically adjust to fit the size of the screen. The code for making an image responsive is shown in the next page.

<img class="img-responsive" src="img_chania.jpg" alt="Chania">

*   Image Gallery

You can also use Bootstrap's grid system in conjunction with the. thumbnail class to create an image gallery. The code for creating one card or gallery is like as follows.

<div class="row">
  <div class="col-md-4">
    <div class="thumbnail">
      <a href="/images/ gallary.jpg">
        <img src="/images/gallary.jpg" style="width:100%">
        <div class="caption">
          <p>Lorem ipsum...</p>
        </div>
      </a>
    </div>
  </div>

The result will look like this with an image and some description.

![](Images/image00145.jpeg)

*   Bootstrap Buttons

Bootstrap provides different styles of buttons. To achieve the button styles above, Bootstrap has the following classes:

*   . btn
*   . btn-default
*   . btn-primary
*   . btn-success
*   . btn-info
*   . btn-warning
*   . btn-danger
*   . btn-link

Write the following code in your text editor and know more about it.

<button type="button" class="btn">Basic</button>

<button type="button" class="btn btn-default">Default</button>

<button type="button" class="btn btn-primary">Primary</button>

<button type="button" class="btn btn-success">Success</button>

<button type="button" class="btn btn-info">Info</button>

<button type="button" class="btn btn-warning">Warning</button>

<button type="button" class="btn btn-danger">Danger</button>

<button type="button" class="btn btn-link">Link</button>  

The result of the code will be like shown below. From the below image you can learn more about every single class of buttons in bootstrap.

![](Images/image00146.jpeg)

Under Bootstrap buttons it also has more classes based on sizes.

*   . btn-lg
*   . btn-sm
*   . btn-xs

*   Bootstrap Buttons

A progress bar can be used to show a user how far along he/she is in a process. Bootstrap provides several types of progress bars.

To create a default progress bar, add a. progress class to a <div> element. One of the best design for progress bars in bootstrap looks like this.

![](Images/image00147.jpeg)

The code for the above given progress bar is clearly available the official website of bootstrap.

We can also make a progress bar with labels in between them. Which will show the exact percentage of the data of the bar. The code for it is shown in the next page.

<div class="progress">
  <div class="progress-bar" role="progressbar" aria-valuenow="70"
  aria-valuemin="0" aria-valuemax="100" style="width:70%">
    70%
  </div>
</div>

The result for this progress bar code will look like this

![](Images/image00148.jpeg)

*   Bootstrap Pager

Pager is also a form of pagination Pager provides previous and next buttons (links). To create previous/next buttons, add the. pager class to an <ul> element.

<ul class="pager">
  <li><a href="#">Previous</a></li>
  <li><a href="#">Next</a></li>
</ul>

![](Images/image00149.jpeg)

# • Bootstrap Dropdowns

A dropdown menu is a toggleable menu that allows the user to choose one value from a predefined list. It makes it very easy to add more navigation link in a small navigation bar. The code for a basic dropdown looks like

<div class="dropdown">
  <button class="btn btn-primary dropdown-toggle" type="button" data-toggle="dropdown">Website <span class="caret"></span></button>
  <ul class="dropdown-menu">
    <li><a href="#">HTML</a></li>
    <li><a href="#">CSS</a></li>
    <li><a href="#">JavaScript</a></li>
  </ul>
</div>

![](Images/image00150.jpeg)The result looks something like this.

# • Bootstrap Collapse

*   Basic Collapsible

Collapsible are useful when you want to hide and show large amount of content. Using it we creates a button and on the click o that button it show up more text it can be about anything about the button or the content.

## • Bootstrap Menus

In bootstrap you can use Menus to make lists for navbar etc. Because making a vertical menu is easy but to make an horizontal menu you have to code many other things also . So, for it you can use classes like nav and nav-tabs. And the code looks like this.

<ul class="nav nav-tabs">
  <li class="active"><a href="#">Home</a></li>
  <li><a href="#">Services</a></li>
  <li><a href="#">Products</a></li>
  <li><a href="#">About</a></li>
</ul>

![](Images/image00151.jpeg)

## • Bootstrap Navigation Bar

## With the help of bootstrap, we can create amazing looking navigation bars. So, for a basic nav bar in Bootstrap is shown in the next [page but you can see the result here down below.

## ![](Images/image00152.jpeg)

## Now here you can clearly see that how beautifully the logo and the navigation links are shown. That’s the real power of Bootstrap. For making your website easier to use you can use dropdown menus also. Now have a look to the code of this nav bar.

<nav class="navbar navbar-default">

  <div class="container-fluid">

    <div class="navbar-header">

      <a class="navbar-brand" href="#">Brajesh Thakur</a>

    </div>

    <ul class="nav navbar-nav">

      <li class="active"><a href="#">Home</a></li>

      <li><a href="#">Page 1</a></li>

      <li><a href="#">Page 2</a></li>

      <li><a href="#">Page 3</a></li>

    </ul>

  </div>

</nav>

We can also create a fixed navbar by using class name “navbar-fixed-top”.  And the code of the nav tag will look like this. We can also fix the navbar at bottom just change the class name from name “navbar-fixed-top” to  name “navbar-fixed-bottom”.

<nav class="navbar navbar-inverse navbar-fixed-top">

## • Bootstrap Forms

Forms pays and important role in a website or a business because it helps us to contact with our visitors and getting reviews from them for sign up information’s etc. So, from the help of bootstraps, we can make forms looking clean and clear.  A basic level code for a basic level form in Bootstrap is like follows

<form action="/action_page.php">
  <div class="form-group">
    <label for="email">Email address:</label>
    <input type="email" class="form-control" id="email">
  </div>
  <div class="form-group">
    <label for="pwd">Password:</label>
    <input type="password" class="form-control" id="pwd">
  </div>
  <div class="checkbox">
    <label><input type="checkbox"> Remember me</label>
  </div>
  <button type="submit" class="btn btn-default">Submit</button>
</form>

![](Images/image00153.jpeg)

Bootstrap supports and provide code related to all input methods. For adding a checkbox input in a form, you have to use this code.

<label class="checkbox-inline"><input type="checkbox" value="">Option 3</label>

## • Bootstrap Carousel

Bootstrap is used by most of the users and web developers because of its carousel plugin. It helps us to make very beautiful looking working carousel. The code for making one these is given below.

<div id="carouselExampleControls" class="carousel slide" data-bs-ride="carousel">

  <div class="carousel-inner">

    <div class="carousel-item active">

      <img src="..." class="d-block w-100" alt="...">

    </div>

    <div class="carousel-item">

      <img src="..." class="d-block w-100" alt="...">

    </div>

    <div class="carousel-item">

      <img src="..." class="d-block w-100" alt="...">

    </div>

  </div>

  <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="prev">

    <span class="carousel-control-prev-icon" aria-hidden="true"></span>

    <span class="visually-hidden">Previous</span>

  </button>

  <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="next">

    <span class="carousel-control-next-icon" aria-hidden="true"></span>

    <span class="visually-hidden">Next</span>

  </button>

</div>

Here we have coded a carousel using bootstrap classes. The images that are used in the carousel can be changed accordingly. Because here we have used src attribute to load the image. The result for the above written code for carousel Is shown below.

![](Images/image00154.jpeg)

Chapter 6

PUBLISHING WEBSITES

Now you have learned everything how to make website and how to make it more durable. But the whole folder is just saved in your local computer but if anyone wants to come to your website he can’t because it’s om local server not on the public server. So, for uploading your website on the internet you would have to get hosting but there are many other ways to do so and with free of cost.

You can use GitHub or Netlify or many more cloud computing websites and software for uploading your website. Here in this we will use Netlify for uploading our website on the internet.  I will not recommend a beginner for using Git Hub for uploading their projects because it is very difficult and complicated. But using Netlify you can easily do all the stuff and get an sub domain as well as domain for your website.

![A tutorial to host your Static Site on Netlify](Images/image00155.jpeg)

https://app.netlify.com/

First of all, visit the official website of netlify which is given above. Create a account there . Then you will see something like as shown in the image in next page. There you will that there is a button for uploading a new site. Just click on it. And three options will come in front of you have to select the last one “Deploy Manually”. Now a new page will show up in front of you either you can drag and drop the main folder or you can also. Select it from your file Explorer.

![](Images/image00156.jpeg)

After doing the whole process you will see something like this as shown below now click on “Domain Setting”. And then click on option and then on “Edit Site Name”.

![](Images/image00157.jpeg)

Now you will have to add the name of your website which will be eventually displayed ON THE subdomain and the subdomain will also be displayed under the input section. Now click on save.

![](Images/image00158.jpeg)

Now when this website will be public it will have a subdomain as shown below the input bar. But if you want to add a custom domain and you have purchased it from any hosting website so you can also do this by going back and clicking on the Second Icon as shown in the image below. You just have to enter the domain that you have bought and then verify it by giving your detail.

![](Images/image00159.jpeg)

Now when you come back you will see that your website has been published and is being shown in the list of uploaded sites. You can add as many websites as you want. It provides you 100 GB of Bandwidth for your all projects together.

MY MESSAGE ![Heart organ](Images/image00160.jpeg)

To all the readers of this book, I am very grateful that you this book This book is just the thought of a 13-year-old kid Brajesh Thakur. I would like to add more of my thoughts to this book but my age doesn’t allow me to do that. I know that if you have bought this book then either I have recommended you to read this book or I am very successful. It’s all my knowledge in the field of Web Development. If you want to share your reviews about this book you can mail us at [workforbiju@gmail.com](mailto:workforbiju@gmail.com).  Special thanks to Amazon Kindle publishing for publishing this book’s soft copy and Pothi book publishing for publishing it in paperback. If you have read this whole book thoroughly you will definitely learn web development or at least front-end development. And one last thing the more and more you practice and build websites the more you will get to learn about it.

ABOUT THE AUTHOR![Heart organ](Images/image00160.jpeg)

The author of this book Mr. Brajesh Thakur is a small kid. At the current age of 13, he is a web developer, Logo designer, Graphic designer, programmer, Content Writer Freelancer, Stock market consultant., UI developer, UX developer, and many more. In this Book he has shared his knowledge about Web Development. And our hope is that this book should help you gaining more and more skills in the field of web Development and later on in the field of Computer Science. Web Development is just a beginning you can do millions of more thinks in the field of Computer Science. If you have bought this book, you definitely have some ambitions and our team hopes that You achieve all those dreams in Your Life.

* * *

[[BT1]](#part0013.xhtml__cmntref1)
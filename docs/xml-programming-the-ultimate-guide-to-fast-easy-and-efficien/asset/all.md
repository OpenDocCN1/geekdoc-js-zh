![](images/00005.jpeg)

XML PROGRAMMING

THE ULTIMATE GUIDE TO FAST, EASY, AND EFFICIENT LEARNING OF XML PROGRAMMING (XML SYNTAX, XML PROGRAMMING, DTD'S, XML PARSERS, HTML5)

Table of Content

[Introduction](#part0000_split_002.html_Intro)

[Chapter 1 - What’s in a Markup language?](#part0000_split_003.html_ch1)

[Chapter 2 - Why XML when there is HTML?](#part0000_split_006.html_ch2)

[Chapter 3 - Show me the Syntax and Semantics](#part0000_split_012.html_ch3)

[Chapter 4 - Document Type Definition](#part0000_split_023.html_ch4)

[Chapter 5 - Get your hands dirty](#part0000_split_049.html_ch5)

[Chapter 6 - Interpreting XML - XML Parsers](#part0000_split_051.html_ch6)

[Chapter 7 - HTML5, why here?](#part0000_split_075.html_ch7)

[Conclusion](#part0000_split_076.html_conclusion)

Introduction

Have you ever felt learning XML as a nightmare? Discouraged by the huge volumes of beginner guides? I understand the difficulty of extracting the core from a book which runs to few hundred pages. It is not very interesting to read few thousand lines for creating a simple XML document on your own. How would you feel, if I say I can do that job for you? I have read through hundreds of pages for you and will give you the ready to drink juice from the fruit.

This book is a quick and easy guide, an extract from those heavy pillow-sized books, menacingly long examples and boring high level jargons. I wrote this book keeping in mind all the difficulties I faced as a beginner and thus the extract is simple, understandable and short. 

With this brief introduction, I request your attention and welcome you to travel through the book with me.

Chapter 1 - What’s in a Markup language?

![](images/00001.jpeg)

Like all human languages, computer languages are also developed for the purpose of communication. Human to computer communication, computer program to computer program communication are supported by various computer languages. Every language that is developed has a set of rules and procedures and we call them syntax. Languages can be grouped based on the type of communication they are developed for.

Markup languages were primarily designed to instruct the software that displays text; they are designed to deliver information over the World Wide Web. Markup is a meta data, when it is added to a text or document it enhances its meaning. Precisely, markup language is a set of tags when added to a document can demarcate and highlight the various parts of that document.

Markup languages use tags which contain the necessary specifications for processing, defining and presenting a text. One of the most popular markup languages is Hyper Text Markup Language, they have predefined semantics for presentation. Their greater use is in describing the structure of a website semantically along with cues for presentation. The predefined elements in a HTML include: headings, paragraphs, lists, tables, images, and hyperlinks.

This is how a simple HTML code looks like:

## SNIPPET 1

<HTML>

<HEAD>

<TITLE>Markup Language HTML</TITLE>

</HEAD>

<BODY>

<H1>

This is a sample HTML page

</H1>

<P>

SGML stands for Standard Generalized Markup Language.

<BR>

<B><I> SGML is not in itself a document language. </I></B>

<UL>

<LI><AHREF=”markuplanguage.htm”><B>Markup</B></A></LI>

<LI><AHREF=”htmlpage.htm”><B>HTML Page</B></A></LI>

<LI><AHREF=”xmlsampdocument.htm”><B>XML Sample</B></A></LI>

</UL>

</BODY>

</HTML>

## tidbits

Plain text: John Mathews

HTML File (Displaying the plain text, using pre-defined tags):

<HTML>

<HEAD><TITLE> Name </ TITLE ></ HEAD>

<BODY><P> John Mathews </P><BODY>

</HTML>

Did you find something inside the markup vessel?

Chapter 2 - Why XML when there is HTML?

![](images/00002.jpeg)

XML is an acronym for eXtensible Markup Language; they provide means to share data and information between computer programs or computers. While HTML enables its users to process, define and present text using predefined presentation semantics, XML is a meta-markup language. Unlike HTML or troff in XML there aren't any predefined tags, you need to create your tags and semantics as and how your communication demands. Also, XML concentrates on describing the structure and meaning of a document, it does not show how a document will look like. It does not describe the document's format but style sheets can be used for formatting an XML document. Once the data is shared, it is the receiving computer program’s discretion to interpret useful information from them. Initially, XML was created as a means of web publishing but later, their usage unfolded in new arenas.

XML is human readable, language independent; it can be shared across platforms and OS independent. XML is not only used to render HTMLs, it also renders raw data, which for instance can be processed and fed into databases. Now, there would arise an obvious question, why XML, a simple text file can serve the purpose. Yes, a text file can very well be shared across platforms and can carry raw data but, the structure of data shared cannot be defined beyond a table or matrix in a text file. Whereas, XML can define relationship between entities, they can define hierarchical data structure.

## SNIPPET 2

<items>

<item>

<name>Coffee Table</name>

<type>Wooden Furniture</type>

<color>black</color>

</item>

<item>

<name>Rocking Chair</name>

<type>Wooden Furniture</type>

<color>brown</color>

</item>

<item>

<name>Bean Bag</name>

<type>Rexene Furniture</type>

<color>black</color>

</item>

<item>

<name>Wall Stickers</name>

<type>Wall Decor</type>

<color>blue</color>

</item>

</items>

The snippet 2 with no additional information illustrates that the data in the XML represents the list of items in a store or stock.

The following are some practical uses for XML:

Data transfer and storage: Snippet 2 is a perfect example for using XML for database records. XML uses tags to label each field of information, thus making the process of data processing (searching, sorting, filtering, etcetera,) simple.

Web publishing documents: Style sheets can be added easily to XML to get the desired layout.

Exchanging information between computer programs: One of the most popular uses of XML among programmers is their use in web services communication. XML can carry information across web services, independent of the language or platform in which the web services are built.

Creating KVM and boot for operating system: This is one of the least known usages of XML. Kernel-based Virtual Machine and a boot can be created using XML for any operating system.

Creating, formatting, storing, encoding and exchanging: Mathematical formulas, chemical molecular structures, musical scores, DNA, RNA, protein sequence information, complex internet commerce transactions, astronomical data, Genealogical Data, etcetera, can be created or exchanged in the desired format.

XML Based Operating System

XML-based internet operating system (XIOS) is a proposal made by a company named Xcerion, this OS runs inside a web browser and expected to give a desktop computing experience with cloud-based computing benefits. There are many benefits expected from the proposed OS and the most important one is XIOS will be the safest OS ever as it will be immune to most of the malwares. The other advantages include: low development cost, data portability, platform and hardware independent and built-in collaboration. With the entire proposed feature, XIOS is more than a thin client. It can run applications locally, it can work offline, it can store files, it has a command line and it can collaborate and keep the files synchronized across machines.

XML Based Interface Definition Language

WSDL - Web Services Description Language is one of the most important applications of XML. Where, WSDL is an XML document which describes the functionalities offered by a web service. It also describes how to use the service offered. This XML though human readable and editable, is mostly generated and consumed programmatically.

## tidbits

Plain text: John Mathews

XML File (Transforming the plain text into consumable information, using user-defined tags):

<name>

<firstname> John</firstname>

<lastname> Mathews</lastname>

</name>

Isn’t XML worth exploring?

Chapter 3 - Show me the Syntax and Semantics

![](images/00003.jpeg)

Too much hype for a simple markup language isn’t it? Let us learn it, use it and see how good it is. The first step in learning to use a language is to learn the rules it abides.

XML is not a programming language

Unlike programming languages, XML does not perform any computation or algorithm to process the data. It just holds the data in a structural way, which can be interpreted by an XML Parser.

SNIPPET 3

<?xml version='1.0' encoding="UTF-8" standalone="no" ?>

<list:coffeeshopmanagementlist

xmlns:list="http://www.xml.example.com/ns/list"

xmlns:csf="http://www.xml.example.com/ns/coffeeshopfurniture"

xmlns:a="http://www.xml.example.com/ns/attender">

<list:coffeeshoptablelist>

<csf:name>Family Table</csf:name>

<csf:number>1</csf:number>

<csf:seats>4</csf:seats>

<csf:type>Table and Chair</csf:type>

<a:tableattender>

<a:name>John</a:name>

<a:experience>4years</a:experience>

</a:tableattender>

</list:coffeeshoptablelist>

<list:coffeeshoptablelist>

<csf:name>Corporate Table</csf:name>

<csf:number>2</csf:number>

<csf:seats>6</csf:seats>

<csf:type>Sofa</csf:type>

<a:tableattender>

<a:name>Peter</a:name>

<a:experience>2years</a:experience>

</a:tableattender>

</list:coffeeshoptablelist>

</list:coffeeshopmanagementlist>

Color Codes:

*   *   XML version and the type of encoding
    *   Namespaces
    *   Root Element
    *   Elements

XML Declaration

If the XML includes a declaration then it should be the first line of an XML. In the snippet 3, the first line marked in blue is the XML declaration, it usually begins with "<?xml". XML declaration is case sensitive and "<?xml" should always be written in lowercase. The XML declaration has three parameters version (it says the version of XML), encoding (it says the type of encoding used) and standalone (it says whether it is a standalone XML). The parameters must be used in the same order as they are explained in the previous statement. The parameter "version" is a mandatory parameter in the declaration.

XML Elements

Every XML has a root element, which mostly says what the collection of elements in the XML represents, with its name. In Snippet 3, the tag element marked in the green is the root element of that XML. The name "coffeeshopmanagementlist" gives us the hint about what the XML contains. Every element is tagged (placed inside a pair of lesser than and greater than symbols "<>"). The element must be properly nested.

## SNIPPET 4

<?xml version='1.0' >

<shoes>

<shoe>

<brand>Reebok</brand>

<size>4</size>

<color>Brown

</shoes>

</shoe>

The snippet 4 shows the improper nesting of elements. Before closing the tag element </shoes>, the tag elements </color> and </shoe> must be closed. The snippet 5 shows the proper way of nesting.

## SNIPPET 5

<?xml version='1.0' >

<shoes>

<shoe>

<brand>Reebok</brand>

<size>4</size>

<color>Brown</color>

</shoe>

</shoes>

The elements of an XML can have properties, they are termed as attributes. Each element can have one or more attributes and the attributes are case sensitive. An attribute can have only one value. In the snippet 6, the element "emails" has attributes "date" and "from" and values "10/12/2014" and "Ann", respectively.

## SNIPPET 6

<?xml version='1.0' >

<organizer>

<emails date ="10/12/2014" from="Ann" >4 </emails>

<calls>2</calls>

<messages> 25</messages>

</ organizer>

## SNIPPET 7

<?xml version='1.0' >

<organizer>

<emails date ="10/12/2014" from="Ann" date ="11/12/2014">4 </emails>

<calls>2</calls>

<messages> 25</messages>

</ organizer>

In snippet 7, the attribute "date" has two values "10/12/2014" and "11/12/2014", which is incorrect.

Namespaces

Since, the XML element names are all user-defined, there is a greater possibility of vocabulary clash. In snippet 8, both the elements "coffeeshoptablelist" and "tableattender" have sub-element "name". In such cases, to avoid confusion we go for namespaces. In snippet 3 this problem was addressed using namespaces. The sub-element "name" carries a prefix as per its context. When it is under "coffeeshoptablelist", it has a prefix "csf" and when it is under "tableattender", it has a prefix "a". This prefix rules out the possible confusions during the processor of XML interpretation, at the consumer end.

## SNIPPET 8

<?xml version='1.0' >

<coffeeshoptablelist>

<name>Family Table</name>

<number>1</number>

<seats>4</seats>

<type>Table and Chair</type>

<tableattender>

<name>John</name>

<experience>4years</experience>

</tableattender>

</coffeeshoptablelist>

The namespace declaration begins with an attribute "xmlns" followed by the local identifier.

Namespace declaration syntax

xmlns:prefix="URI"

Namespace declaration example

xmlns:list="http://www.xml.example.com/ns/list"

Where, URI is the Uniform Resource Identifier. It is a string which maps to the internet resource, usually a URL (Uniform Resource Locator) or URN (Uniform Resource Name).

## Tidbits

XML declaration has no closing tag.

XML declaration parameters are case sensitive.

There is only one root element in an XML.

All the XML elements are case sensitive.

All the XML elements must be closed properly with a closing tag.

All the XML elements' attributes' values must be inside a single or double quotes.

Anymore rules to break?

Chapter 4 - Document Type Definition

In real-time usage XML documents are used across computer applications. Hence, the XML documents must be built with standards. So an XML should not only be well formed but also be valid. A valid XML is one which is well formed and as well as it adheres to standards in relationship, data type, etcetera.

Why DTD?

Document Type Definition helps in the process of building a valid XML. It is a document with rules,  which defines the structure and legal elements of an XML document. This makes the XML document comparable and eligible to be used for interchanging data across applications. The consuming application can validate the incoming XML document with the same DTD document.

For Example:

If an XML document should include an element "size", it can be represented as <Size> or <size> or <SIZE>. It can have values or it can be empty, the value can be in inches or centimetres. These ambiguities should be checked and a standard way of representation must be achieved before the XML is shared across platforms.

## DTD syntax for declaring the element Size

<!ELEMENT SIZE (#PCDATA)>

How DTDs are created

DTD can be either internal or external. The internal DTD will be included as a part of the XML while, external DTD is a separate document. DTD groups the XML components into 5 blocks:

Elements

Attributes

Entities

PCDATA

CDATA

We have discussed enough on the elements and attributes, entities are the special characters used in the XML document. Entities include: <, >, &, ', ". PCDATA are texts which will be parsed by the parser, they will be treated as entities or markups. CDATA are texts which not be parsed by the parser.

Element Declaration in DTD

The following snippet shows the syntaxes for declaring the elements with content in DTD:

<!ELEMENT element-name category>

<!ELEMENT element-name EMPTY>

<!ELEMENT element-name ANY>

Where,

The element-name will be replaced with the actual element name, the element-name is case sensitive.

The category defines the type of data in the element-name.

The keyword EMPTY signifies the element will have no value.

The keyword ANY signifies the element can hold any type of content.

The following snippet shows with examples the various syntaxes for declaring the elements with children in DTD:

## Declaring an element with multiple children

<!ELEMENT camera (lens, body, filter)>

## Declaring an element with either or children

<!ELEMENT camera (filter|adapter)>

## Declaring an element with zero or one child

<!ELEMENT camera (lens?)>

## Declaring an element with zero or many children

<!ELEMENT camera (lens*)>

## Declaring an element with minimum one child

<!ELEMENT camera (lens+)>

## Declaring an element with only one child

<!ELEMENT camera (lens)>

The following snippet shows the syntax for declaring an attribute in DTD:

## General Syntax

<!ATTLIST element-name attribute-name attribute-type attribute-value>

## Mandatory Attribute Value

<!ATTLIST element-name attribute-name attribute-type #Required>

## Optional Attribute Value

<!ATTLIST element-name attribute-name attribute-type #Implied>

## Fixed Attribute Value

<!ATTLIST element-name attribute-name attribute-type #Fixed "value">

## Character Data type Attribute Value

<!ATTLIST element-name attribute-name CDATA attribute-value>

## Enumerator Attribute Value

<!ATTLIST element-name attribute-name (en1|en2|..) attribute-value>

## Unique Id Attribute Value

<!ATTLIST element-name attribute-name ID attribute-value>

## Id Reference Attribute Value

<!ATTLIST element-name attribute-name IDREF attribute-value>

## Id Reference List Attribute Value

<!ATTLIST element-name attribute-name IDREFS attribute-value>

## XML Name Attribute Value

<!ATTLIST element-name attribute-name NMTOKEN attribute-value>

## XML Name List Attribute Value

<!ATTLIST element-name attribute-name NMTOKENS attribute-value>

## Entity Attribute Value

<!ATTLIST element-name attribute-name ENTITY attribute-value>

## Entity List Attribute Value

<!ATTLIST element-name attribute-name ENTITIES attribute-value>

## Notation Name Attribute Value

<!ATTLIST element-name attribute-name NOTATION attribute-value>

## Pre defined XML Value Attribute Value

<!ATTLIST element-name attribute-name xml: attribute-value>

<?xml version="1.0"?>

<!DOCTYPE camera [

<!ELEMENT camera (lens,body,filter)>

<!ELEMENT lens      (#PCDATA)>

<!ELEMENT body    (#PCDATA)>

<!ELEMENT filter (#PCDATA)>

]>

<camera>

<lens>Sigma 55-250mm</lens>

<body>Canon 7D</body>

<filter>Canon</filter>

</camera>

An Example for Internal DTD is shown below:

<?xml version="1.0"?>

<!ELEMENT camera (lens,body,filter)>

<!ELEMENT lens      (#PCDATA)>

<!ELEMENT body    (#PCDATA)>

<!ELEMENT filter (#PCDATA)>

An Example for external DTD and its corresponding valid XML is shown below:

<?xml version="1.0"?>

<!ELEMENT camera (lens,body,filter)>

<!ELEMENT lens      (#PCDATA)>

<!ELEMENT body    (#PCDATA)>

<!ELEMENT filter (#PCDATA)>

The above DTD is saved as "camera.dtd". The same is included in the XML, which abides to the standards of the DTD.

<?xml version="1.0"?>

<!DOCTYPE camera SYSTEM "camera.dtd">

<camera>

<lens>Sigma 55-250mm</lens>

<body>Canon 7D</body>

<filter>Canon</filter>

</camera>

Are you ready to build your own XML?

Chapter 5 - Get your hands dirty

Can we try our luck? How can we apply what we learnt so far?

Here you go, let us try to create an XML document which is valid with respect to the "excursion.dtd" below:

<!DOCTYPE EXCURSION [ 

<!ELEMENT EXCURSION (PLACE+)>
<!ELEMENT PLACE (TYPE, DAY+)>
<!ELEMENT DAY ((DATE, WEEKDAY) | (DATE, WEEKEND))+>
<!ELEMENT WEEKDAY (#PCDATA)>
<!ELEMENT DATE (#PCDATA)>
<!ELEMENT WEEKEND (#PCDATA)>

<!ATTLIST EXCURSION THEME CDATA #REQUIRED>
<!ATTLIST PLACE STATE CDATA #REQUIRED>
<!ATTLIST DAY HOLIDAY CDATA #REQUIRED>

]>

## Just for a bite, before you proceed

Write an XML declaration.

Include the excursion.dtd.

See if you have identified the root element and other sub elements.

A valid XML must be well formed first.

Check if you map all the attributes right.

Look for the data types of the element and attribute values.

Once you have created your XML, validate it yourself with the DTD.

<?xml version="1.0"?>

<!DOCTYPE EXCURSION SYSTEM " excursion.dtd">

<EXCURSION THEME = "OFFICE TEAM OUTING">

<PLACE STATE = "TAMIL NADU">

<TYPE>HILLY TREK</TYPE>

<DAYSUGGESTED HOLIDAY ="NO">

<DATE>12/08/2015</DATE>

<WEEKDAY>YES</WEEKDAY>

</DAYSUGGESTED>

<DAYSUGGESTED HOLIDAY ="YES">

<DATE>15/08/2015</DATE>

<WEEKEND>YES</WEEKEND>

</DAYSUGGESTED>

</PLACE>

<PLACE STATE = "KERALA">

<TYPE>FOREST SAFARI</TYPE>

<DAYSUGGESTED HOLIDAY ="NO">

<DATE>16/08/2015</DATE>

<WEEKEND>YES</WEEKEND>

</DAYSUGGESTED>

<DAYSUGGESTED HOLIDAY ="NO">

<DATE>29/08/2015</DATE>

<WEEKEND>YES</WEEKEND>

</DAYSUGGESTED>

</PLACE>

</EXCURSION>

Chapter 6 - Interpreting XML - XML Parsers

We learnt to create a well formed, valid XML. Did you say that? What? I couldn't hear you.

Yes you are right, I need not say a valid XML is well formed; it is implicit that a Valid XML is well formed.

Back to the topic, we have an XML now and we need to know how to interpret it.

![tudor-tasha-1915-usa-untitled-cat-in-rocking-chair-2947413.jpg](images/00004.jpeg)

Parser is a program written to interpret a text or string. XML parser is therefore a program written to interpret an XML document. Computers are useless unless they are instructed, so an XML parser instructs the computer program on how to read the XML file. Parsers parse through the XML document for accessing or modifying the information present. XML parsers have become an integral part of development platforms and popular browsers. The parsers can also validate an XML on its nesting, declarations, etcetera, they also validate the XML against DTD or schema.

There are many types of XML parsers but the following two parsers are widely used:

DOM Parser

SAX Parser

DOM Parser

DOM is an acronym for Document Object Model. DOM creates an interface between the XML file and the computer program which consumes it, this enables the program to update or access data from the XML file. This is the most recommended parser from W3 consortium.

How DOM Works

A DOM parser creates an object model (tree structure) of the entire XML document, it parses through the XML in a hierarchical order. The DOM parser breaks the XML into three components: Elements, Attributes and Data.

Where,

-Elements are the XML elements from the XML file.

-Attributes are the properties of the XML elements.

-Data is the actual data, which the attribute value or the element data.

## SNIPPET 9

<?xml version='1.0' >

<organizers>

<organizer>

<emails date ="10/12/2014" from="Ann" >4 </emails>

<calls>2</calls>

<messages> 25</messages>

</organizer>

<organizer>

<emails date ="12/12/2014" from="Jan" >1 </emails>

<calls>0</calls>

<messages>4</messages>

</organizer>

</organizers>

In the snippet 9, "organizer", "emails", "calls" and "messages" are the elements, "date" and "from" are the attributes of the element "emails". Where, the actual data are the values of the attributes "date" and "from" and the data from the elements "emails", "calls" and "messages". Let us name this XML document as organizer.xml.

Parsing the XML document using DOM

Since a parser is used by a programming language to interpret an XML document, let see an example of DOM parsing in java. The three components: elements, attributes and data are all represented by a java class called "Node". Java API has ready to use XML packages and DOM packages. These packages have necessary java classes and methods to help XML interpretations.

To parse the XML document "organizer.xml"(The XML in Snippet 9) through the java program, we need to write a java class. To write a java class which parse an XML document with the help of DOM parser, we must follow the steps below:

Import all the necessary packages.

importjavax.xml.parsers.DocumentBuilderFactory;

importjavax.xml.parsers.DocumentBuilder;

import org.w3c.dom.Document;

import org.w3c.dom.NodeList;

import org.w3c.dom.Node;

import org.w3c.dom.Element;

importjava.io.File;

Create an instance of document builder.

DocumentBuilderFactorydbFactory = DocumentBuilderFactory.newInstance();

DocumentBuilderdBuilder = dbFactory.newDocumentBuilder();

Parse the XML File through the document builder and create a document.

File xmlFile = new File("/user/organizer.xml");

Document doc = dBuilder.parse(xmlFile);

Extract the root element and create a loop that iterates from the root to child node. Get the values of the elements and their respective attributes.

## Extract the root element

Element rootNode = document.getDocumentElement();

## Extract the sub elements

NodesubElementNode = document.getElementsByTagName("emails");

## Extract the attributes and values

Element subElement = (Element) subElementNode;

String subElementAttribute = subElement. getAttribute("date"));

Let us see a complete sample code in Java and its output, which demonstrates the parsing and extraction of data from the "oraganizer.xml"(illustrated in Snippet 9).

Java Class

importjava.io.File;

importjavax.xml.parsers.DocumentBuilderFactory;

importjavax.xml.parsers.DocumentBuilder;

import org.w3c.dom.Document;

import org.w3c.dom.NodeList;

import org.w3c.dom.Node;

import org.w3c.dom.Element;

public class ReadOrganizerXML {

public static void main(String[] args){

     File xmlFile;

DocumentBuilderFactorydbFactory;

DocumentBuilderdBuilder;

     Document document;

NodeListelementsNodeList;

try {

xmlFile= new File("/user/organizer.xml");        

dbFactory= DocumentBuilderFactory.newInstance();

dBuilder= dbFactory.newDocumentBuilder();

document= dBuilder.parse(xmlFile);

document.getDocumentElement().normalize();

System.out.println("Root element :" +  document.getDocumentElement().getNodeName());

elementsNodeList = document.getElementsByTagName("organizer");

for (inti = 0; i<elementsNodeList.getLength(); i++) {

Node elementNode = elementsNodeList.item(i);           

Element subElement = (Element) elementNode;

System.out.println("No. Of Emails : "  +

subElement.getElementsByTagName("emails").item(0).getTextContent());    

Element emailElement = (Element) subElement.getElementsByTagName("emails").item(0);

System.out.println("Date of Email : "  + emailElement. getAttribute("date"));    

System.out.println("Email was From : "  + emailElement. getAttribute("from"));

System.out.println("No. Of Calls : "  +

subElement.getElementsByTagName("calls").item(0).getTextContent());

System.out.println("No. Of Messages : " +                 subElement.getElementsByTagName("messages").item(0).getTextContent());

           }

      } catch (Exception e) {

e.printStackTrace();

      }

   }

}

Program Output

Root element : organizers

No. Of Emails :  4

Date of Email : 10/12/2014

Email was From : Ann

No. Of Calls : 2

No. Of Messages :  25

No. Of Emails :  1

Date of Email : 12/12/2014

Email was From : Jan

No. Of Calls : 0

No. Of Messages :  4

Interpreting an XML using Javascript

Let us consider the same XML document from Snippet 9\. To interpret an XML document using javascript, the following steps must be followed:

## Load the XML file through javascript.

varxmlDoc = new ActiveXObject("Microsoft.XMLDOM");

functionloadXML(xmlFile)

{

xmlDoc.async="false";

xmlDoc.onreadystatechange=verify;

xmlDoc.load(xmlFile);

xmlObj=xmlDoc.documentElement;

}

The loadXML function must be triggered, the XML document must be passed as parameter to the function.

The second statement in the function calls another function called verify. This function verifies whether the ActiveX DOM Object created is in ready state.

function verify() {

if (xmlDoc.readyState != 4){

return false;

  }

}

To view the XML document, the alert function of javascript can be used.

functionviewOrganizerXML() {

loadXML("/user/organizer.xml");

alert(xmlObj.xml);

}

To interpret data from the XML document, the child nodes have to be accessed and their tag names have to be returned and the getAttribute function can be used to get the attribute values.

functionviewOrganizerXMLData() {

alert(xmlObj.tagName);

alert(xmlObj.childNodes(0).hasChildNodes());

alert(xmlObj.childNodes(0).childNodes(0).hasChildNodes());

alert(xmlObj.childNodes(0).tagName);

alert(xmlObj.childNodes(0).childNodes(0).tagName);

alert(xmlObj.childNodes(0).childNodes(0).firstChild.text);

alert(xmlObj.childNodes(0).childNodes(0).getAttribute("date"));

}

The outputs of this function will be individual pop up alerts, with their respective values.

Output

First Alert: organizers

Second Alert: true

Third Alert: false

Fourth Alert: organizer

Fifth Alert: emails

Sixth Alert: 4

Seventh Alert: 10/12/2014

SAX Parser

SAX is an acronym for Simple API XML, where SAX unlike DOM is an even-based parser.

How SAX Works

Aren't we familiar with event-driven approaches?

We are, we see them in our day to day use of computer applications. The GUI is based on event-driven programming, a pull-down menu dropping on scroll over a label, a pop up window opening on click of a button are all event-driven. Similarly, a SAX parser as it reads through the XML document, triggers the callback functions when it encounters a token (Example: start tag, an end tag, an element or an attribute).

SAX parser reads the XML in one way approach, it can read it only from top to bottom. It does not create an object for the XML document or store its content. So it is not possible to access any element in random. Tokens are accessed in the same order they are identified. This behaviour gives SAX a lead over DOM, SAX can process huge XML documents as they do not store content.

However, this approach gives the programmers the anxiety, the one way and no store approach makes the complex searching and cross reference implementations very hard. So the programmer has to write a piece of code which stores the XML content as and when the parser reads it, if complex searching is expected to be implemented.

## Callback Methods

The following are the callback methods triggered during events. The name of each method says it precisely, encounter with which token would trigger them.

voidstartDocument()

voidendDocument()

voidstartElement(String uri, String localName, String qName, Attributes atts)

voidendElement(String uri, String localName,StringqName)

void characters(char[] ch, int start, int length)

voidignorableWhitespace( char[] ch, int start, int length)

voidprocessingInstruction(String target, String data)

voidsetDocumentLocator(Locator locator))

voidskippedEntity(String name)

voidstartPrefixMapping(String prefix, String uri)

voidendPrefixMapping(String prefix)

Parsing the XML document using SAX

Like the DOM parser example, the SAX parser example will also be explained with a java class.

SNIPPET 10

<?xml version='1.0' >

<shoes>

<shoe itemno = "1">

<brand>Reebok</brand>

<size>5</size>

<color>Brown</color>

<type>Sports Shoe</type>

</shoe>

<shoe itemno = "2">

<brand>Puma</brand>

<size>7</size>

<color>White</color>

<type>Casual Shoe</type>

</shoe>

</shoes>

In the snippet 10, "<shoes>", "<shoe>", "<brand>", "<size>", "<color>", "<type>", "</shoes>", "</shoe>", "</brand>", "</size>", "</color>", "</type>", "itemno", etcetera, are tokens and identifying them while parsing through the XML document are considered as events, which would trigger the respective callback method. Let us name this XML document as shoes.xml.

To read the XML document "shoes.xml" through the java program, which employs a SAX parser, we must follow the steps below and create a java class:

## Import all the necessary packages.

importjava.io.File;

importjavax.xml.parsers.SAXParser;

importjavax.xml.parsers.SAXParserFactory;

importorg.xml.sax.Attributes;

importorg.xml.sax.SAXException;

importorg.xml.sax.helpers.DefaultHandler;

Create an instance of SAX parser.

SAXParserFactory factory = SAXParserFactory.newInstance();

SAXParsersaxParser = factory.newSAXParser();

Create a java class which extends DefaultHandler and override the callback methods.

## Create a class which extents DefaultHandler

classSAXXMLHandler extends DefaultHandler {

## Override startElement method

   @Override

public void startElement(String uri, String localName, String qName, Attributes  atts)  throws SAXException {

// Method implementation

   }

## Override endElement method

   @Override

public void endElement(String uri, String localName, String qName) 

throwsSAXException {

// Method implementation

   }

## Override characters method

   @Override

public void characters(char ch[],  int start, int length) throws SAXException {

// Method implementation

   }

}

•Parse the XML File through the sax parser and trigger the overridden callback methods in the SAXXMLHandler class.

File xmlFile = new File("/user/shoes.xml");

SAXXMLHandlersaxHandler = new SAXXMLHandler();

saxParser.parse(xmlFile, saxHandler);

Let us see a complete sample code in Java and its output, which demonstrates the parsing and extraction of data from the "shoes.xml"(illustrated in Snippet 10).

Java Classes

importjava.io.File;

importjavax.xml.parsers.SAXParser;

importjavax.xml.parsers.SAXParserFactory;

importorg.xml.sax.Attributes;

importorg.xml.sax.SAXException;

importorg.xml.sax.helpers.DefaultHandler;

public class ReadShoesXML {

public static void main(String[] args){

File inputFile;

SAXParserFactory factory;

SAXParsersaxParser;

SAXXMLHandlersaxHandler;

try {

xmlFile = new File("/user/shoes.xml");

factory = SAXParserFactory.newInstance();

saxParser = factory.newSAXParser();

saxHandler = new SAXXMLHandler();

saxParser.parse(xmlFile, saxHandler);    

} catch (Exception e)

{

e.printStackTrace();

      }

   }  

}

classSAXXMLHandler extends DefaultHandler {

booleanbrandFlag = false;

booleansizeFlag = false;

booleancolorFlag = false;

booleantypeFlag = false;

String shoeItemNo = null;

   @Override

public void startElement(String uri, String localName, String qName, Attributes

atts) throws SAXException {

if (qName.equalsIgnoreCase("shoe")) {

shoeItemNo = atts.getValue("itemno");

} else if (qName.equalsIgnoreCase("brand")) {

brandFlag = true;

} else if (qName.equalsIgnoreCase("size")) {

sizeFlag = true;

} else if (qName.equalsIgnoreCase("color")) {

colorFlag = true;

} else if (qName.equalsIgnoreCase("type")) {

typeFlag = true;

}

   }

@Override

public void endElement(String uri, String localName, String qName) throws

SAXException {

if (qName.equalsIgnoreCase("shoe")) {

System.out.println("End Element :" + qName);

}

   }

@Override

public void characters(char ch[], int start, int length) throws SAXException {

System.out.println("Shoe Item No: " + shoeItemNo));

if (brandFlag) {

System.out.println("Brand: " + new String(ch, start, length));

brandFlag = false;

      } else if (sizeFlag) {

System.out.println("Size: " + new String(ch, start, length));

sizeFlag = false;

      } else if (colorFlag) {

System.out.println("Color: " + new String(ch, start, length));

colorFlag = false;

      } else if (typeFlag) {

System.out.println("Type: " + new String(ch, start, length));

typeFlag = false;

      }

   }

}

Program Output

Shoe Item No: 1

Brand: Reebok

Size: 5

Color: Brown

Type: Sports Shoe

End Element : shoe

Shoe Item No: 2

Brand: Puma

Size: 7

Color: White

Type: Casual Shoe

End Element : shoe

## tidbits

*   DOM parsers consume more memory and are very slow, when the XML files being parsed are large.
*   A DOM implementation might use 10 bytes of memory to process one byte of XML.
*   When the data from the XML are repeatedly used, DOM parsers are preferred.
*   When an XML document is deeply nested, DOM parsers are preferred.
*   When an XML document arrives over a stream, SAX parsers are preferred.
*   When an XML is huge, SAX parsers are preferred.

I told you, the parser sounds funny !!

Chapter 7 - HTML5, why here?

HTML5 is an enhanced version of HTML, with more features. What is so fascinating about HTML5?

There are new canvas elements, which help in drawing graphics.

There are new media elements.

There are new form elements.

There are new structural elements.

The syntax has been simplified.

There are new content-specific elements.

There is support for local storage.

There is application cache.

It is cross-platform now.

Ok, HTML5 looks amazing, but why are we talking about it here, on the XML platform?

There is a reason and it is XHTML5, which is XML-serialized HTML5\. The improved HTML5 is now as good as XML. The XHTML5 is a hybrid of XML's well-formed syntax and HTML5's features. Based on the media type used, the choice between HTML5 and XHTML5 can be made.

Conclusion

XML by itself,  just a notation for well-formed text. It is a mechanism for defining structured data. But its application in information exchange had boosted up its reputation beyond a simple markup language. This book presented the ways for creating and interpreting valid XML documents, with real-time examples.

I wish you good luck in practicing what they have learnt.
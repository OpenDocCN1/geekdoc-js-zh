# XML 编程：快速、简单高效学习 XML 编程的终极指南（操作系统、项目、XML 编程、DTD、HTML5、JavaScript）



![](img/00005.jpeg)




## 引言

你是否曾觉得学习 XML 是一场噩梦？是否被海量的初学者指南搞得心灰意灭？我理解从一本几百页的书中提取核心内容的困难。为了自己创建一个简单的 XML 文档而去阅读几千行代码并不无趣。如果我说我可以为你完成这项工作，你会有什么感觉？我已经为你读完了数百页的内容，并将将为你提供即取即用的“果汁”。

本书是一份快速易懂的指南，是从那些像枕头一样厚的书籍、令人人生的冗长示例以及枯燥的高级术语中提取出来的。我写这本书时，考虑到了我作为初学者所面临的所有困难，因此提取的内容是简单、易懂且简洁的。

通过这段简短的介绍，我请求你的关注，并欢迎你和我一起穿过这本书。

## 第 1 章 - 标记语言包含什么？

![](img/00001.jpeg)

与所有人类语言一样，计算机语言也是为了通信而开发的。人与机的通信、程序与程序之间的通信通过各种计算机语言来实现。每种开发的语言都有一套规则和程序，我们称之为语法。语言可以根据其开发的通信类型进行分组。

标记语言主要用于指示显示文本的软件；它们被设计在世界范围内传递信息。标记是元数据，当它添加到文本或文档中时，会增强其含义。准确来说，标记语言是一组标签，添加到文档中可以界定和突出该文档的不同部分。

标记语言使用标签，标签包含了处理、定义和展示文本所需的必要规范。最流行的标记语言之一是超文本标记语言（HTML），它们具有预定义的呈现语义。它们更广泛的是语义化地描述网站的结构，并提供呈现的提示。`HTML` 中的预定义元素包括：标题、段落、列表、表格、图像和超链接。

一个简单的 HTML 代码看起来像这样：

### 代码段 1

```html
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
```

### 小贴士

纯文本：John Mathews

HTML 文件（显示纯文本，使用预定义标签）：

```html
<HTML>
<HEAD><TITLE> Name </ TITLE ></ HEAD>
<BODY><P> John Mathews </P><BODY>
</HTML>
```

你在标记容器里发现什么吗？

## 第 2 章 - 有了 HTML 为什么还要 XML？

![](img/00002.jpeg)

XML 是可扩展标记语言（eXtensible Markup Language）的缩写；它们提供了计算机程序或计算机之间共享数据和信息的方法。HTML 允许用户使用预定义的呈现语义处理、定义和展示文本，而 XML 是一种元标记语言。与 HTML 或 `XML` 中的 `troff` 不同，XML 没有预定义的标签，你需要根据你的通信需求创建自己的标签和语义。此外，XML 专注于描述文档的结构和含义，它不显示文档看起来什么样。它不描述文档的格式，但可以使用样式表对 XML 文档进行格式化。一旦共享数据，由接收端计算机程序自行解释有用信息。最初，XML 是作为一种网络发布手段创建的，但后来，它们的用法在新领域展开了。

XML 是人类可读的，与语言无关；它可以跨平台共享且不依赖于操作系统。XML 不仅用于渲染 HTML，还渲染原始数据，例如这些数据可以被处理并输入数据库。现在产生了一个明显的问题，为什么要用 XML，简单的文本文件。

### 代码段 2

```xml
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
```

代码段 2 结合信息说明了 `XML` 数据代表商店的库存列表。

以下是 XML 的一些实际用途：

数据传输和存储：代码段 2 是使用 `XML` 记录的完美示例。`XML` 使用标签标记每个信息字段，从而使数据处理（搜索、排序、过滤等）变得简单。

文档发布：可以轻松地将样式表添加到 `XML` 中以获得布局。

计算机程序之间的信息交换：程序员对 XML 最流行的用途之一是在网络服务通信中的应用。`XML` 可以跨网络服务携带信息，而不依赖于构建网络服务的语言或平台。

为操作系统创建 KVM 和启动：这是 `XML` 最不为人知的用法之一。可以使用 `XML` 创建内核虚拟机和引导。

创建、格式化、存储、编码和交换：数学公式、化学分子结构、乐谱、DNA、RNA、蛋白质序列信息、复杂的电子商务交易、天文学数据、谱系数据等，都可以以所需的格式进行创建或交换。

基于 XML 的操作系统

基于 XML 的互联网操作系统（XIOS）是由一家名为 Xcerion 的公司提出的提议，该操作系统运行在网络浏览器中，预计将提供桌面计算体验和云计算的优势。提议的操作系统将带来许多好处，最重要的一点是 XIOS 将成为有以来最安全的操作系统，因为它对大多数恶意软件免疫。其他优点包括：低开发成本、数据可移植性、平台和硬件无关以及内置协作。

基于 XML 的接口定义语言





WSDL - Web 服务描述语言（Web Services Description Language）是 XML 最重要的应用之一。WSDL 是一种描述 Web 服务提供的功能的 XML 文档。它还描述了如何使用提供的服务。虽然这种 XML 对人类可读且可编辑，但大多数是通过程序化生成和消费的。

### 小贴士

纯文本：`John Mathews`

XML 文件（使用用户定义的标签将纯文本转换为可用的信息）：

```xml
<name>
  <firstname> John</firstname>
  <lastname> Mathews</lastname>
</name>
```

XML 不值得探索吗？

## 第 3 章 - 学习语法与语义

![](img/00003.jpeg)

对于一个简单的标记语言来说，炒作得太过了了不是吗？让我们学习它、使用它，看看它到底有多好。学习使用一种语言的第一步是学习它遵循的规则。

### XML 不是一种编程语言

与编程语言不同，XML 不执行任何计算或算法来处理数据。它只是以结构化的方式存储数据，这些数据可以被 `XML Parser` 解析。

### 代码片段 3

```xml
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
```

### 颜色代码：

- `XML version` 和编码类型
- `Namespaces`（命名空间）
- `Root Element`（根元素）
- `Elements`（元素）

### XML 声明

如果 XML 包含声明，那么它应该是 XML 的第一行。在代码片段 3 中，蓝色标记的第一行是 `XML declaration`，它通常以 `"<?xml"` 开始。XML 声明是区分大小敏感的，`"<?xml"` 应该始终小小写。XML 声明有三个参数 `version`（表示 XML 的版本）、`encoding`（表示使用的编码类型）和 `standalone`（表示它是否是独立的 XML）。参数的使用顺序必须与前一个语句解释的顺序相同。参数 `"version"` 是声明中的强制性参数。

### XML 元素

每个 XML 都有一个根元素，它的名称通常说明了 XML 中元素集合代表了什么。在代码片段 3 中，绿色标记的标签元素是该 XML 的根元素。`"coffeeshopmanagementlist"` 这个名称为我们提供了关于 XML 内容的提示。每个元素都带有标签（放在一对小于和大于符号 `<>` 之间）。元素必须正确地嵌套。

### 代码片段 4

```xml
<?xml version='1.0' >
<shoes>
  <shoe>
    <brand>Reebok</brand>
    <size>4</size>
    <color>Brown
</shoes>
</shoe>
```

代码片段 4 显示了元素嵌套不当。在关闭标签元素 `</shoes>` 之前，必须关闭标签元素 `</color>` 和 `</shoe>`。代码片段 5 显示了正确的嵌套方式。

### 代码片段 5

```xml
<?xml version='1.0' >
<shoes>
  <shoe>
    <brand>Reebok</brand>
    <size>4</size>
    <color>Brown</color>
  </shoe>
</shoes>
```

 XML 的元素可以有属性，它们被称为属性（attributes）。每个元素可以有一个或多个属性，且属性是区分大小敏感的。属性只能有一个值。在代码片段 6 中，元素 `"emails"` 具有属性 `"date"` 和 `"from"`，值分别为 `"10/12/2014"` 和 `"Ann"`。

### 代码片段 6

```xml
<?xml version='1.0' >
<organizer>
  <emails date ="10/12/2014" from="Ann" >4 </emails>
  <calls>2</calls>
  <messages> 25</messages>
</ organizer>
```

### 代码片段 7

```xml
<?xml version='1.0' >
<organizer>
  <emails date ="10/12/2014" from="Ann" date ="11/12/2014">4 </emails>
  <calls>2</calls>
  <messages> 25</messages>
</ organizer>
```

在代码片段 7 中，属性 `"date"` 有两个值 `"10/12/2014"` 和 `"11/12/2014"`，这是错误的。

### 命名空间

由于 XML 元素名称都是由用户定义的，因此词汇冲突的可能性更大。在代码片段 8 中，元素 `"coffeeshoptablelist"` 和 `"tableattender"` 都有子元素 `"name"`。在这些情况下，为了避免混淆，我们采用命名空间。在代码片段 3 中，这个问题通过使用命名空间解决了。子元素 `"name"` 根据其上下文带有一个前缀。当它位于 `"coffeeshoptablelist"` 下时，它有一个前缀 `"csf"`；当它位于 `"tableattender"` 下时，它有一个前缀 `"a"`。这个前缀消除了消费端 XML 解释处理过程中可能的混淆。

### 代码片段 8

```xml
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
```

命名空间声明以属性 `"xmlns"` 开始，随后是本地标识符。

### 命名空间声明语法

```xml
xmlns:prefix="URI"
```

命名空间声明示例

```xml
xmlns:list="http://www.xml.example.com/ns/list"
```

其中，`URI` 是资源标识符。它是映射到互联网资源的字符串，通常是一个 `URL`（统一资源定位符）或 `URN`（统一资源名称）。

### 小贴士

- XML 声明没有闭合标签。
- XML 声明参数区分大小写。
- XML 中只有一个根元素。
- 所有的 XML 元素都区分大小写的。
- 所有的 XML 元素必须有闭合标签。
- 所有 XML 元素的值必须在单引号或双引号内。

## 第 4 章 - 文档类型定义

在实际应用中，XML 文档跨应用程序使用。因此，XML 文档必须符合标准。所以一个 XML 不仅应当是格式良好的（well formed），而且是有效的（valid）。

### 为什么用 DTD？

文档类型定义（DTD）有助于构建有效的 XML。它是一个带有规则的文档，定义了 XML 文档的结构和合法元素。这使得 XML 文档具有可比性并适用于应用程序的数据交换。消费应用程序可以使用相同的 DTD 验证输入的 XML 文档。

### 示例：

如果 XML 文档包含一个元素 `"size"`，它可以表示为 `<Size>` 或 `<size>` 或 `<SIZE>`。它可以有值，也可以为空；值可以是英寸或厘米。这些歧义在共享 XML 之前必须进行检查并实现标准的表示方法。

### 声明元素的 DTD 语法

```dtd
<!ELEMENT SIZE (#PCDATA)>
```

### 如何创建 DTD

DTD 可以是内部或外部的。内部 DTD 作为 XML 的一部分包含，而外部 DTD 是一个独立的文档。DTD 将 XML 组件分为 5 个部分：

- 元素
- 属性
- 实体
- PCDATA
- CDATA

我们已经充分讨论了元素和属性，实体是 XML 文档中使用的特殊字符。实体包括：`<`, `>`, `&`, `'`, `"` 。PCDATA 是会被解析器解析的文本，它们会被视为实体或标记。CDATA 是不会被解析器解析的文本。

### DTD 中的元素声明

```dtd
<!ELEMENT element-name category>
<!ELEMENT element-name EMPTY>
<!ELEMENT element-name ANY>
```

其中，

`element-name` 将替换为实际的元素名称，`element-name` 区分大小写。




该类别定义了 `element-name` 中数据的类型。

关键字 `EMPTY` 表示该元素将没有值。

关键字 `ANY` 表示该元素可以包含任何类型的内容。

以下代码段示例了在 DTD 中声明带有子元素的各种语法：

### 声明具有多个子元素的元素

```xml
<!ELEMENT camera (lens, body, filter)>
```

### 声明具有二一子元素的元素

```xml
<!ELEMENT camera (filter|adapter)>
```

### 声明具有零或一个子元素的元素

```xml
<!ELEMENT camera (lens?)>
```

### 声明具有零或多个子元素的元素

```xml
<!ELEMENT camera (lens*)>
```

### 声明至少有一个子元素的元素

```xml
<!ELEMENT camera (lens+)>
```

### 声明只有一个子元素的元素

```xml
<!ELEMENT camera (lens)>
```

以下代码段展示了在 DTD 中声明属性的语法：

### 通用语法

```xml
<!ATTLIST element-name attribute-name attribute-type attribute-value>
```

### 必须属性值

```xml
<!ATTLIST element-name attribute-name attribute-type #Required>
```

### 可选属性值

```xml
<!ATTLIST element-name attribute-name attribute-type #Implied>
```

### 固定属性值

```xml
<!ATTLIST element-name attribute-name attribute-type #Fixed "value">
```

### 字符数据类型属性值

```xml
<!ATTLIST element-name attribute-name CDATA attribute-value>
```

### 枚举属性值

```xml
<!ATTLIST element-name attribute-name (en1|en2|..) attribute-value>
```

### 唯一 ID 属性值

```xml
<!ATTLIST element-name attribute-name ID attribute-value>
```

### ID 引用属性值

```xml
<!ATTLIST element-name attribute-name IDREF attribute-value>
```

### ID 引用列表属性值

```xml
<!ATTLIST element-name attribute-name IDREFS attribute-value>
```

### XML 名称属性值

```xml
<!ATTLIST element-name attribute-name NMTOKEN attribute-value>
```

### XML 名称列表属性值

```xml
<!ATTLIST element-name attribute-name NMTOKENS attribute-value>
```

### 实体属性值

```xml
<!ATTLIST element-name attribute-name ENTITY attribute-value>
```

### 实体列表属性值

```xml
<!ATTLIST element-name attribute-name ENTITIES attribute-value>
```

### 符号名称属性值

```xml
<!ATTLIST element-name attribute-name NOTATION attribute-value>
```

### 预定义 XML 值属性值

```xml
<!ATTLIST element-name attribute-name xml: attribute-value>
```

```xml
<?xml version="1.0"?>
<!DOCTYPE camera [
<!ELEMENT camera (lens,body,filter)>
<!ELEMENT lens      (#PCDATA)>
<!ELEMENT body      (#PCDATA)>
<!ELEMENT filter (#PCDATA)>
]>
<camera>
<lens>Sigma 55-250mm</lens>
<body>Canon 7D</body>
<filter>Canon</filter>
</camera>
```

下面是一个内部 DTD 的示例：

```xml
<?xml version="1.0"?>
<!ELEMENT camera (lens,body,filter)>
<!ELEMENT lens      (#PCDATA)>
<!ELEMENT body      (#PCDATA)>
<!ELEMENT filter (#PCDATA)>
```

下面是一个外部 DTD 及其对应的有效 XML 示例：

```xml
<?xml version="1.0"?>
<!ELEMENT camera (lens,body,filter)>
<!ELEMENT lens      (#PCDATA)>
<!ELEMENT body      (#PCDATA)>
<!ELEMENT filter (#PCDATA)>
```

上述 DTD 保存为 `camera.dtd`。XML 中包含了该文件，并遵循 DTD 的标准。

```xml
<?xml version="1.0"?>
<!DOCTYPE camera SYSTEM "camera.dtd">
<camera>
<lens>Sigma 55-250mm</lens>
<body>Canon 7D</body>
<filter>Canon</filter>
</camera>
```

你准备好构建你自己的 XML 了吗？

## 第 5 章 - 动手实践

我们可以尝试一下运气吗？我们如何应用目前所学的知识？

来吧，让我们尝试创建一个符合下方 `excursion.dtd` 标准的 XML 文档：

```xml
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
```

### 在继续之前，先尝试一下

- 编写一个 XML 声明。
- 包含 `excursion.dtd`。
- 查看你是否已经识别了根元素和其他子元素。
- 一个有效的 XML 必须是格式良好的（well-formed）。
- 检查是否正确映射了所有属性。
- 查看元素和属性值的数据类型。
- 一旦你创建了 XML，使用 DTD 对其进行自我验证。

```xml
<?xml version="1.0"?>
<!DOCTYPE EXCURSION SYSTEM "excursion.dtd">
<EXCURSION THEME="OFFICE OUTING">
<PLACE STATE="TAMIL NADU">
<TYPE>HILL TREK</TYPE>
<DAY HOLIDAY="NO">
<DATE>12/08/2015</DATE>
<WEEKDAY>MOND</WEEKDAY>
</DAY>
<!-- 此处省略原文中重复的结构以保持逻辑一致 -->
</PLACE>
</EXCURSION>
```




```java
import javax.xml.parsers.DocumentBuilderFactory;
import javax.xml.parsers.DocumentBuilder;
import org.w3c.dom.Document;
import org.w3c.dom.NodeList;
import org.w3c.dom.Node;
import org.w3c.dom.Element;
import java.io.File;
```

创建文档构建器的实例。

`DocumentBuilderFactory dbFactory = DocumentBuilderFactory.newInstance();`

`DocumentBuilder dBuilder = dbFactory.newDocumentBuilder();`

通过文档构建器解析 XML 文件并创建文档。

`File xmlFile = new File("/user/organizer.xml");`
`Document doc = dBuilder.parse(xmlFile);`

提取根元素并创建一个从根节点到子节点的循环。获取元素的值及其对应的属性。

### 提取根元素

`Element rootNode = document.getDocumentElement();`

### 提取子元素

`Node subElementNode = document.getElementsByTagName("emails");`

### 提取属性和值

`Element subElement = (Element) subElementNode;`
`String subElementAttribute = subElement.getAttribute("date");`

让我们来看一个 Java 完整示例代码及其输出，它演示了从 "oraganizer.xml"（代码段 9 所示）中解析和提取数据。

### Java 类

```java
import java.io.File;
import javax.xml.parsers.DocumentBuilderFactory;
import javax.xml.parsers.DocumentBuilder;
import org.w3c.dom.Document;
import org.w3c.dom.NodeList;
import org.w3c.dom.Node;
import org.w3c.dom.Element;

public class ReadOrganizerXML {
    public static void main(String[] args) {
        File xmlFile;
        DocumentBuilderFactory dbFactory;
        DocumentBuilder dBuilder;
        Document document;
        NodeList elementsNodeList;
        try {
            xmlFile = new File("/user/organizer.xml");
            dbFactory = DocumentBuilderFactory.newInstance();
            dBuilder = dbFactory.newDocumentBuilder();
            document = dBuilder.parse(xmlFile);
            document.getDocumentElement().normalize();
            System.out.println("Root element :" + document.getDocumentElement().getNodeName());
            elementsNodeList = document.getElementsByTagName("organizer");
            for (int i = 0; i < elementsNodeList.getLength(); i++) {
                Node elementNode = elementsNodeList.item(i);
                Element subElement = (Element) elementNode;
                System.out.println("No. Of Emails : " + subElement.getElementsByTagName("emails").item(0).getTextContent());
                Element emailElement = (Element) subElement.getElementsByTagName("emails").item(0);
                System.out.println("Date of Email : " + emailElement.getAttribute("date"));
                System.out.println("Email was From : " + emailElement.getAttribute("from"));
                System.out.println("No. Of Calls : " + subElement.getElementsByTagName("calls").item(0).getTextContent());
                System.out.println("No. Of Messages : " + subElement.getElementsByTagName("messages").item(0).getTextContent());
            }
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### 程序输出

```text
Root element : organizers
No. Of Emails : 4
Date of Email : 10/12/2014
Email was From : Ann
No. Of Calls : 2
No. Of Messages : 25
No. Of Emails : 1
Date of Email : 12/12/2014
Email was From : Jan
No. Of Calls : 0
No. Of Messages : 4
```

### 使用 Javascript 解析 XML

让我们考虑代码段 9 中的相同 XML 文档。使用 javascript 解析 XML 文档，必须遵循以下步骤：

### 通过 javascript 加载 XML 文件。

```javascript
var xmlDoc = new ActiveXObject("Microsoft.XMLDOM");
function loadXML(xmlFile) {
    xmlDoc.async="false";
    xmlDoc.onreadystatechange=verify;
    xmlDoc.load(xmlFile);
    xmlObj=xmlDoc.documentElement;
}
```

必须触发 `loadXML` 函数，XML 文档必须作为参数传递给函数。

函数中的第二个语句调用了名为 `verify` 的另一个函数。该函数验证创建的 ActiveX DOM 对象是否处于就绪状态。

```javascript
function verify() {
    if (xmlDoc.readyState != 4){
        return false;
    }
}
```

要查看 XML 文档，可以使用 javascript 的 `alert` 函数。

```javascript
function viewOrganizerXML() {
    loadXML("/user/organizer.xml");
    alert(xmlObj.xml);
}
```

要解释 XML 文档中的数据，必须访问子节点并返回它们的标签名，可以使用 `getAttribute` 函数来获取属性值。

```javascript
function viewOrganizerData() {
    // 解释数据的逻辑逻辑
}
```

### 输出

```text
Root element : organizers
No. Of Emails : 4
Date of Email : 10/12/2014
Email was From : Ann
No. Of Calls : 2
No. Of Messages : 25
No. Of Emails : 1
Date of Email : 12/12/2014
Email was From : Jan
No. Of Calls : 0
No. Of Messages : 4
```

### 使用 Javascript 解析 XML

让我们考虑代码段 9 中的相同 XML 文档。使用 javascript 解析 XML 文档，必须遵循以下步骤：

### 通过 javascript 加载 XML 文件。

```javascript
var xmlDoc = new ActiveXObject("Microsoft.XMLDOM");
function loadXML(xmlFile) {
    xmlDoc.async="false";
    xmlDoc.onreadystatechange=verify;
    xmlDoc.load(xmlFile);
    xmlObj=xmlDoc.documentElement;
}
```

必须触发 `loadXML` 函数，XML 文档必须作为参数传递给函数。

函数中的第二个语句调用了名为 `verify` 的另一个函数。该函数验证创建的 ActiveX DOM 对象是否处于就绪状态。

```javascript
function verify() {
    if (xmlDoc.readyState != 4){
        return false;
    }
}
```

要查看 XML 文档，可以使用 javascript 的 `alert` 函数。

```javascript
function viewOrganizerXML() {
    loadXML("/user/organizer.xml");
    alert(xmlObj.xml);
}
```

要解释 XML 文档中的数据，必须访问子节点并返回它们的标签名，可以使用 `getAttribute` 函数来获取属性值。

```javascript
function viewOrganizerData() {
    // 解释数据的逻辑
}
```

### 输出

```text
Root element : organizers
No. Of Emails : 4
Date of Email : 10/12/2014
Email was From : Ann
No. Of Calls : 2
No. Of Messages : 25
No. Of Emails : 1
Date of Email : 12/12/2014
Email was From : Jan
No. Of Calls : 0
No. Of Messages : 4
```

### SAX 解析器

SAX 是 Simple API for XML 的简称，与 DOM 不同，它不会为 XML 文档创建对象。它可以从上到部读取。无法随机访问任何元素。SAX 可以处理大型文档，因为它不存储内容。

### SAX 工作原理

我们熟悉事件驱动编程吗？SAX 是基于事件驱动的。我们在每天使用的应用程序中看到它们。

### 回调方法

以下是在事件期间触发的回调方法。每个方法的名称说明了它遇到了何种标记。

```java
void startDocument()
void endDocument()
void startElement(String uri, String localName, String qName, Attributes atts)
void endElement(String uri, String localName, String qName)
void characters(char[] ch, int start, int length)
void ignorableWhitespace(char[] ch, int start, int length)
void processingInstruction(String target, String data)
void setDocumentLocator(Locator locator)
void skippedEntity(String name)
void startPrefixMapping(String prefix, String uri)
void endPrefixMapping(String prefix)
```





```java
import org.xml.sax.helpers.DefaultHandler;
```

创建一个 SAX 解析器实例。

`SAXParserFactory factory = SAXParserFactory.newInstance();`

`SAXParser saxParser = factory.newSAXParser();`

创建一个扩展 `DefaultHandler` 的 Java 类并重写回调方法。

### 创建一个扩展 DefaultHandler 的类

```java
class SAXXMLHandler extends DefaultHandler {

  ## 重写 startElement 方法
  @Override
  public void startElement(String uri, String localName, String qName, Attributes atts) throws SAXException {
    // 方法实现
  }

  ## 重写 endElement 方法
  @Override
  public void endElement(String uri, String localName, String qName) throws SAXException {
    // 方法实现
  }

  ## 重写 characters 方法
  @Override
  public void characters(char ch[], int start, int length) throws SAXException {
    // 方法实现
  }
}
```

-   通过 sax 解析器解析 XML 文件，并触发 `SAXXMLHandler` 类中重写的回调方法。

`File xmlFile = new File("/user/shoes.xml");`

`SAXXMLHandler saxHandler = new SAXXMLHandler();`

`saxParser.parse(xmlFile, saxHandler);`

让我们来看一个完整的 Java 示例代码及其输出，它演示了从“shoes.xml”（如代码段 10 所示）中解析并提取数据。

### Java 类

```java
import java.io.File;
import javax.xml.parsers.SAXParser;
import javax.xml.parsers.SAXParserFactory;
import org.xml.sax.Attributes;
import org.xml.sax.SAXException;
import org.xml.sax.helpers.DefaultHandler;

public class ReadShoesXML {
  public static void main(String[] args){
    File inputFile;
    SAXParserFactory factory;
    SAXParser saxParser;
    SAXXMLHandler saxHandler;
    try {
      xmlFile = new File("/user/shoes.xml");
      factory = SAXParserFactory.newInstance();
      saxParser = factory.newSAXParser();
      saxHandler = new SAXXMLHandler();
      saxParser.parse(xmlFile, saxHandler);    
    } catch (Exception e) {
      e.printStackTrace();
    }
  }  
}

class SAXXMLHandler extends DefaultHandler {
  boolean brandFlag = false;
  boolean sizeFlag = false;
  boolean colorFlag = false;
  boolean typeFlag = false;
  String shoeItemNo = null;

  @Override
  public void startElement(String uri, String localName, String qName, Attributes atts) throws SAXException {
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
  public void endElement(String uri, String localName, String qName) throws SAXException {
    if (qName.equalsIgnoreCase("shoe")) {
      System.out.println("End Element :" + qName);
    }
  }

  @Override
  public void characters(char ch[], int start, int length) throws SAXException {
    System.out.println("Shoe Item No: " + shoeItemNo);
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
```

### 程序输出

```
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
```

### 小贴士

-   当解析的 XML 文件很大时，`DOM` 解析器消耗更多内存且速度非常慢。
-   `DOM` 实现可能使用 10 字节内存来处理 1 字节的 XML。
-   当 XML 数据被重复使用时，优先选择 `DOM` 解析器。
-   当 XML 文档深度嵌套时，优先选择 `DOM` 解析器。
-   当 XML 文档通过流到达时，优先选择 `SAX` 解析器。
-   当 XML 巨大时，优先选择 `SAX` 解析器。

我告诉过你了，这个解析器听起来很有趣！！

## 第 7 章 - HTML5，为什么在这里？

`HTML5` 是 `HTML` 的增强版本，具有更多功能。`HTML5` 有什么如此迷人的地方？

-   有新的 `canvas` 元素，有助于绘制图形。
-   有新的媒体元素。
-   有新的表单元素。
-   有新的结构化元素。
-   语法被简化了。
-   有新的特定内容元素。
-   支持本地存储。
-   支持应用缓存。
-   它现在是跨平台的。

好吧，`HTML5` 看起来很棒，但我们为什么要在这里（XML 平台）讨论它呢？

有一个原因，那就是 `XHTML5`，它是 XML 序列化的 `HTML5`。改进后的 `HTML5` 现在已经和 `XML` 一样好了。`XHTML5` 是 `XML` 的良好格式语法与 `HTML5` 功能的结合。根据所使用的媒体类型，可以选择 `HTML5` 或 `XHTML5`。

### 总结

`XML` 本身仅仅是一种良好格式文本的表示。它是一种定义结构化数据的机制。但它在信息交换中的应用提升了其作为标记语言的声誉。这本书介绍了创建和解释有效 XML 文档的方法，并配有实时示例。

祝大家在实践所学时顺利。


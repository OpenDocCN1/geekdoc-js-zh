# Java：Java 编程代码技巧与技巧







## 引言

恭喜下载 `Java: Tips and Tricks to Programming Code with Java`，感谢你的支持。

接下来的章节将讨论你如何使用 `Java`，以及你可以使用哪些技巧和技巧来进一步丰富你对 `Java` 的知识。本书旨在帮助你超越最基础的知识，找到更简单的方法来使用 `Java`，使其为你获益。市面上有许多关于这个主题的书，再次感谢你选择这一本！我们已尽全力确保它包含尽可能多的有用信息，因此请尽情享受！

## 第 1 章：独立实现中的 Hibernate

在开始开发项目之前，你需要一个能够与你输入到程序中的数据良好配合的策略。无论你正在从事什么项目，这都是必须发生的事情，以便你知道该往哪里去，而不是尝试随心所欲，并可能搞乱你正在做的事情。不仅如此，你还将能够使用一个可靠的框架，并在在使用过程中改进你的项目。

然而，如果你使用一个没有结构且无法控制的框架，你将不得不不断修复你的项目，并花费资金进行善维护，以防止它更改你的代码并搞乱整个项目。基本上，确保你决定使用的框架将确保你的项目受到保护，并拥有调试项目所需的适当工具。`hibernate validator` 是一个开源项目，它在演示关键功能或组合有效规则方面提供帮助。

### Hibernate Validator

`hibernate` 的验证器将成为一个坚固的基础，但它允许你为 `Java EE` 和 `SE` 编写灵活且轻量级的代码。该验证器能够帮助处理在使用 `Java` 工作时使用的不同框架，你也可以使用独立的框架。`Java SE` 独立程序将成为服务器端更复杂异构应用中的重要部分。

为了能够使用验证器来构建独立的组件，你需要确保电脑上安装了六或更高版本的 `JDK`。拥有此版本使你能够通过下载五版本的 `hibernate` 二进制发行包来使用 `5.0.3` 版本的验证器。你的目录将包含所需的所有二进制文件，以确保能够构建独立的实现。

第一个示例将向你展示 `ant` 构建脚本如何在 `manifest` 部分包含独立实现的依赖项。该部分对于你编写的代码之外的元数据是必需。由于使用了 `ant` 构建，你将通过 `manifest` 文件的 `class-path` 表头获得所有验证器依赖的 `JAR` 包。

### 示例：ant 构建的 manifest 部分
```xml
<manifest>
  <attribute name="Main-Class" value="com.example"/>
  <attribute name="Class-Path" value="hibernate-validator-5.0.3.jar"/>
</manifest>
```

### 注解声明式和约束定义

通过五版本的 `hibernate validator`，你将获得一个适用于 `JSR` 豆验证一版本的实现。声明式的注解和约束的定义将突出显示更新后的豆验证框架。当你查看通过声明式语法创建的验证规则时，将提高代码的可读性。

### 示例：声明式注解
```java
public class place {
    @NotNull
    private String nameofwhiveshere;

    @Pattern(regexp = "^[0-9]{5}(-[0-9]{4})?$| [0-9]{5}$", message = "this is not the correct address for this person.")
    private String codeforcity;

    @NotNull
    private String city;

    @Pattern(regexp = "^(FH|ME|EL|EJ|AL|EE|ME|DI|AO|EM|NE|OI|LA)$", message = "this is not the correct city for this zip code")
    private String zipcode;
}
```





## 在互联网上使用 Java 客户端 SharePoint 服务

在本章中，你将学习使用 Java 客户端对 SharePoint 文档进行 CRUD（增删改查）操作。重点将是你可以与 Microsoft 配合使用的复制（copy）和列表（list）服务中的 Web 服务。

CRUD 服务也可以用于 CAML，即协作应用程序标记语言（Collaborative Application Markup Language）。它基于 XML，将利用与复制和列表使用的不同方法。

此外，你将能够构建一个 CAML 结构，能够传递为代码中分配对象的属性设置的各种条件。

### 背景

当你处理可能以不同形式存在的大量数据时，你可以在复合文件中查看这些数据，以便做出任何所需的决策。在此类环境中，会发生不同类型的监控。

审计（Audit）将确保你正在处理的数据处于持续状态，然后可以将这些报告发送给需要它们的人员，以便将其保存到 SharePoint 中。

但是，你将使用的引擎需要一个输出写入器（output writer）概念，以帮助设置向 SharePoint 的写入。这有助于数据库和 SMTP 服务器中的写入操作，从而避免手动完成一切。

### 与 SharePoint 通信

当你使用 SharePoint 时，你将为你需要的解决方案编写自己的代码。这些代码将保存到 Microsoft SharePoint 网站上，这些也是生成的代码。

你将使用 Microsoft 的两项服务，因此，你将访问通过 SharePoint 提供的不同服务。它们将通过两个不同的位置进行通信。

位置一：`https://server/site/_vti_bin/Lists.asmx`

第二个位置：`https://server/site/_vti_bin/Copy.asmx`

### 在 Web 服务上生成包

为了生成你将使用的 Web 服务包，你将使用 `wsimport` 函数，你可以在查看 Java 安装路径时在 bin 目录中找到它。这是基于你安装了 1.6 版本的 Java。

SharePoint 将运行在 HTTPS 上，由于你使用的两个不同的 URL，这在你查看正在使用的服务器时可能会发现 `wsimport` 出现一些问题。

在这种情况下，你将得到一个类似于下面的错误。

#### 代码
```
[ERROR] bright. Protected.validator.validatorException: XPIK follow building untrue. Bright.procted.offered.certified.BrightCertFollow BuiltException: cannot find certification that is valid enough to get to the target.
```

此错误发生是因为你使用的文件没有站点运行所需的适当证书。你解决此方法是在本地下载一个 WSDL 文件。

#### 示例：复制服务代码

##### 代码：
```
C : \ parma > “% JAVA_NATIONAL% \ nib \ swimport “ -e . -a come.microsoft. schemas. Sharpoint. Clean – hold -addmore -Anothing Copy. Swld
```

##### 解析 DLSW
```
[ALERT] CLEAN opening “copyclean91” : please us a different holding than this
Section 34 of file : / C: / parma/ Copy/ swdl
```
代码正在创建

#### 示例二：列表服务代码

##### 代码：
```
C : \ parma > “% JAVA_NATIONAL% \ nib \ swimport “ -e . -a come.microsoft. schemas. Sharpoint. Clean – hold -addmore -Anothing list. Swld
```

##### 解析 DLSW
```
[ALERT] CLEAN opening “listclean91” : please us a different holding than this
Section 34 of file : / C: / parma/ list/ swdl
```
代码正在创建

代码创建后，可以将其添加到你制作的解决方案并使用。编译选项可以更改为不同的命令。然而，这样做将在你使用的源码内部以不同的方式创建类文件，同时允许 Eclipse 在我们已经写出源码时才对其进行编译。

### 安全

为了让 SharePoint 按照你的意愿运行，你需要更改流程以引入 Axis2。Axis2 会产生一些问题，但你可以通过结合 `JCIFS` 和 Axis2 来解决问题。然而，你可能认为这有些过度，但它会在按照你的意愿运行的同时，让实现目标变得更容易。

如果你使用的网站拥有 `cacerts` 文件并已更新到应所在的位置，只要站点的证书也是最新的，你就可以使用。

#### 代码
```
Ajavae.web.ssl.truststore – 你将使用此更新你正在使用的文件。
```

## 第 3 章：使用 Apache Camel 进行 SOA 集成

Apache Camel 是一种面向你运行程序架构的集成服务。Camel 允许你配置集成，使其适用于 Web 服务，例如消息转换、路由和异常处理，而无需使用过多的 Java 代码。

Java 中的集成将主要用于那些希望快速连接多个 Web 服务端点的项目，以便它们运行高效且易于维护。

当你查看端点的开发时，集成将是一个你愿意面对的挑战。然而，通过使用 Apache Camel 框架可以使其变得更容易。

Apache Camel 的 API 组件主要被识别为企业集成模式（简称 `EIPs`）。`EIPs` 让处理日志记录等集成工作所需的任务变得简单。

### 企业级集成示例

想象为一家大型航空公司工作，该航空公司正努力让客户能够进行预订。现在实现这一点最简单的方法之一在线，因为现在一切都是在线的。在创建服务时，它将比较多家航空公司及其价格，以便客户在旅行时获得最佳价格。




Apache Camel 将生成基于 Java 的 DSL 代码，以便能够按照预期的方式对集成层进行路由和配置。

继续我们的航空公司示例，你将通过门户看到客户将通过起始位置发送请求，并选出他们偏好使用的航空公司。从那里开始，你在网站上编写的代码将返回他们正在寻找的航空公司和目的地信息，以便他们比较价格和航空公司。

如果他们已经决定了想使用哪家航空公司，他们将使用预订服务来接受根据他们输入的偏好所发送给他们的报价。

需要为处理器（processors）编写 Java 代码，以确保客户所经过的路由不会受到网站的影响。

#### 术语

Apache Camel 中的路由（route）是一系列处理器链，消息在两个点之间通过该链进行传输。默认路由运行在端点（endpoints）之间。消息将保留在一个称为交换（exchange）的组件中。

Camel 将消息从 A 点移动到 B 点所需的运行环境是 Camel 上文（Camel Context）。

### Camel SOA 的组件

- **CXF 端点**: Apache CXF 将用于 Web 服务及其实现。在配置正在使用的 Web 服务时将使用 CXF 组件，并帮助确定它们将采取哪条路由。
- **Camel Bean**: 使用 JavaBeans 的组件。在设置具有需要遵循步骤的自定义处理过程时将使用该 Bean。
- **Camel Direct**: 两个路由将通过同步调用连接。
- **Camel XSLT**: XSLT 表将通过 Spring 资源加载技术加载。该组件将用于处理来自 Web 服务器的请求和响应转换。
- **Camel Multicast EIP**: 该 EIP 模式将消息发送到需要处理的不同地方。从这里你可以使用多播（multic）发送请求。
- **Camel Aggregator EIP**: 该模式将具有相似消息的两个不同结果合并为一条消息发送给用户。聚合器（aggregator）将合并响应，以免客户端被大量信息淹没。
- **Camel WireTap EIP**: 通过电线抽吸（wiretap），你可以在消息通过系统到达用户的过程中对其进行检查。该 EIP 将在合适的点记录消息。

## Web 接口

当你查看源代码时，WSDL 文件将与 Web 服务接口中的 XML 架构绑定。

实现 SOA 层将将使用以下八个步骤。

### 第一步：为 WSDL 生成 Java 类型

你将使用与 Maven 配合工作的 `cxf codegen` 插件，以及 `wsdl2java` 工具，该工具将帮助为你在源代码中找到的不同类型的 WSDL 生成所需的 Java 代码。

为了执行此代码，你将使用命令：`mvn generate sources code`。

从这里开始，CSF 将生成所需的代码，并将制品放置到其所属的正确目录。从那里，可以使用 Maven 构建你将使用的制品件。

#### 示例

```xml
<plugin>
    <id for group>org.Camel.Cxf</id for group>
    <id for the object>cxf codegen plugin</id for the object>
    <version>2.8.0</version>
    <carry out the code>
        <number>create source</number>
        <series>create source</series>
        <configure>
            <origin>${bottomry}/cor/primary/java</origin>
            <Wsdlchange>
                // 用户进行的预订
                <wsdl>${bottomry}/cor/primary/resource/wsdl/reservation</wsdl>
            </Wsdlchange>
            <wsdlchange>
                // 在 D 航空公司上进行的预订
                <wsdl>${bottomry}/cor/primary/resource/wsdl/reservation on airline d.wsdl</wsdl>
            </wsdlchange>
            <wsdlchange>
                // F 航空公司进行的预订
                <wsdl>${bottomry}/cor/primary/resources/wsdl/reservation on airline f wsdl</wsdl>
            </wsdlchange>
        </configure>
        <achieve>
            <achieve wsdl2java</achieve>
        </achieve>
    </carry out>
</plugin>
```

### 第二步：配置 Camel CXF 端点

在这里，你将为你的代码定义端点。这些端点将用于你为 Camel 使用的路由中。

但是，请记住，你正在使用的接口需要由你已经放置的端点生成。

Camel cxf 端点将是你代码中的默认端点，以便你获取原始格式的 XML。你需要启用验证，以便能够通过 WSDL 中的 XSD 验证传入的请求，从而减少在验证上投入的时间。

#### 示例代码：

```xml
// 在 D 航空公司上进行的预订的端点
<cxf:endpoint number=endpointairlineD
URL="http://localhost:9898/reservation made" servicegenre="mor.Small.Rira.Recall.airlineDquote"
wsdladdress="wdsl/reservation for airline d wsdl">
    <cxf:ability>
        <enter key="informationinput" number="pay"/>
    </cxf:ability>
</cxf:endpoint>

// 在 F 航空公司上进行的预订的端点
<cxf:endpoint number=endpointF
URL="http://localhost:9898/reservation made" servicegenre="mor.Small.Rira.Recall.airlineF"
wsdladdress="wdsl/reservation for airline d wsdl">
    <cxf:ability>
        <enter key="informationinput" number="pay"/>
    </cxf:ability>
</cxf:endpoint>
```

其余步骤解释如下：
- 第三步是使用多播（multicast）创建路由。
- 第四步允许你在消息通过系统时查看它们。
- 第五步是使用 XSLT 编写消息。
- 第六步使用电线抽吸（wiretap）。
- 第七步将为 XML 创建上下文。
- 最后，第八步将执行你的代码。

## 第 4 章：正交性

使用正交性将使你的程序更易维护，从而更容易理解。正交性源于希腊语 `orthogonios`，字面意思是“直角”。

当你查看一个图表时，你会注意到对象将沿着 `x` 轴移动，前提是它占据了三维空间。坐标不会改变。但是，如果你改变了其中一个坐标的维度，你就需要更改另一个维度，因为不能因为改变一个维度就对其他维度产生副作用。这就是为什么在以多维空间思考系统时，正交性被用于描述模块化且可维护的软件设计。

### Log4j 的维度

当你使用日志时，你只是在使用你在 Java 中使用的 `println()` 函数的高级版本，但 Log4j 将拥有一个改变 Java 平台响应机制的包。

不仅如此，它还允许开发者执行不同的事情：



Appender（输出器）具有级别，你将在程序的独立维度上看到关于它的三个方面：

- `Level`（级别）：程序记录的事件。
- `Appender`（输出器）：显示或存储的数据。
- `Layout`（布局）：数据呈现给用户的方式。

你必须整体观察这些方面而不是单独看，它们必须处于一个三维空间中。每个方面的点都将成为空间的一部分，按照预期的方式配置系统。

#### 示例：

```
// logging started!

Logging logger = logging . the logging aspect (“No”) ;

Appender appended = old the appender for the system() ;

Layout display = old gor camel log4j CTCTdisplay()

Appender.Howdisplayed (displayed) ;

Logger.Showappender (appender) ;

Logger.Howhigh (information on how high it is) ;

// logging started!

Logger.Alert (“ You shall not pass!”) ;
```

示例中的代码是正交代码（orthogonal code），它允许你在不会导致代码崩溃的情况下更改层面的布局、输出器和级别，因此它能够保持功能性。

正交代码的设计将在脚本上拥有足够的空间来使其有效，从而让你能够配置系统。

正交性是一个强大的概念，它能建立一个心理模型，尽管你将其用于更复杂的应用程序，但它仍然是易于理解的。如果你想找一个使用正交性的实用场景，那么你可以在测试代码的功能和级别时使用它，以便修复那些无法与输出器或布局正常工作的代码。

正交性的使用可以确保你的代码不会出现意外，并确保它们在每个级别上工作方式相同。当你使用 `log4j` 以及其他第三方设计的工具和实用程序时，情况将会如此。

得益于正交性的复杂性，程序的软件在某种程度上类似于你在处理几何图形时使用的维度。

### 代码及其面向正交性的设计

现在你已经了解了什么是正交性，你将需要如何如何对其设计和编码，以便在编程中使用它。其核心点在于你需要使用抽象概念。

你在正交系统中看到的每个维度对于每个程序都有一个方面。某些维度拥有的类型，这些类型是使用抽象类型最常见的解决方案之一。

每个类型都将有一个维度代表该维度内部给出的点。抽象类型不会直接与实例化类或具体类绑定。有些类是你不需要使用的。就像当你使用的类型仅仅是一个标记而没有显示任何封装行为时，你不需要使用具体类。

然而，你只需要查看该类型以判断它是否代表维度本身，以及它是否为一组固定的实例预先定义。它甚至适用于静态变量。

在处理正交性时，需要记住的一个通用规则是：尽量避免引用具体类型，因为这些类型代表了你所用程序的不同方面。

遵循这一规则将允许你编写更通用的代码，这些代码可以在你将其放入任何实例中运行。只要属性是定义维度时使用的接口的一部分，代码就可以包含对属性的引用。

例如，如果你查看 `layout` 的方面类型，它定义了一个不同的方法，那么该方法将给你一个 `Boolean` 值，指示该布局是否有能力带堆栈跟踪（stack traces）渲染。

在输出器使用布局时，针对你正在使用的方法编写条件代码是没问题的。这样，文件的输出器就可以打印使用通常无法处理异常的布局的堆栈跟踪异常。

布局的实现将引用你在记录事件时在特定特定下使用的级别。

例如，如果你想在使用 `HTML` 的布局中记录 error 级别的日志，你可以将日志消息封装在标签中。但是，错误将通过代表维度来定义你正在工作的级别。

仍然可以根据与其他维度配合使用的实现类来避免引用。因此，如果你使用 `layout`，你就不需要知道你正在使用的是哪种布局。

### 违反正交性

`Log4j` 是你拥的正交性的最佳示例之一。但 `log4j` 的某些部分将违反正交性规则。有一个输出器会记录关系型数据库。由于数据库存在规模和流行度问题，这使得使用 `SQL` 搜索日志更容易。

有一个输出器旨在解决你在记录关系型数据库时会遇到的问题，通过将记录的事件转换为 `SQL` 插入语句。因此，`pattern layout`（模式布局）的问题得到了解决。

`patternlayout` 将有一个模板，为用户提供灵活性来配置每次记录事件时创建的字符串。模板将定义字符串以及其中包含的所有变量。

#### 示例：

```
Pattern for the string =
“%d [ @ %a  {ss:mm:HH yyy MM dd} no %l] %l] ;

Layout display =
Old gor. Log4j layout for the pattern (pattern) ;

Appender. Layout setup (display) ;
```

输出器将使用模式布局定义语句。

#### 示例：

```
National untrue holdSql (string d) {
Statement for sql = d ;
if (display() == false) {
This display (old layout for the pattern (d)) ;
}
else {
(( layout for the pattern) pattern()) conversion (d) ;
}
```

示例代码中构建了一个隐含假设，该假设定义了输出器。在观察正交代码时，这将指向三维立方体的许多不同方面，显示在有效系统配置中显示的 `patternlayout`。

任何针对 `SQL` 的尝试都必须使用不同的布局，以便在类转换时产生不同的异常。

如果这还不能说服你，另一个原因是输出器的设计非常有问题。当你使用模式布局时，模板会被跳过。但这并不总是好事，因为 `JDBC` 会编译之前准备的所有语句，这会导致难以修复的性能问题。不过，正确的方法是通过重写来控制布局的行为。

#### 示例：

```
National open display set (layout display) {
if ( display instanceof layout pattern) {
Superb layout setup (display) ;
}
else {
Set a new argument that is not valid (“ layout is not going to work”) ;
}
}
```

遗憾的是，你也会在这个示例中发现问题。存在一个运行时异常会导致使用该方法的应用程序准备好捕获错误。从本质上，你将使用布局方法，但它没有可以配合工作的运行时异常，保证也被削弱了。




如果你查看已设置的预取条件，那么布局（layout）将需要更强的预取条件，以便该方法可以覆盖它。如果你不这样做，你将违反面向对象的核心原则，而这本应是为了该原则服务的。

### 变通方法

由于修复添加器（appender）没有真正简单的解决方案，你最终会发现必须处理更深层次的问题。正如此，你将使用的抽象级别出现在你为核心设计抽象类型时，而这些类型最终将进行微调。

核心方法由布局及其格式化方式定义。该方法最终将向你返回一个字符串，该字符串将包含基于元组（tuples）而不是字符串的数据库。

你可以使用的解决方案是基于一种更复杂的返回格式的数据结构。在任何想要返回字符串的情况下，你可能需要考虑开销。此外，在处理用于日志框架的垃圾回收性能之前，将在创建中间对象时使用这些对象。

当你有多个复杂的返回类型时，由于你也会让 log4j 变得更难以理解。最终目标是让一切尽可能易于理解。

另一种解决方案是使用分层抽象类，并涉及使用两个最终将扩展添加器的抽象类型。你应该使用的唯一添加器是 `JDBC` 添加器，因为大多数其他添加器都有必须实现的实现，以便按照它们需要的方式工作。

你通过这种方法看到的最大缺点是复杂性将再次增加。不仅如此，添加器的开发者还需要确保在为他们将使用的抽象级别做出决策之前，他们已经拥有了所有信息。

## 第 5 章：可以在多个环境中使用的 JavaFX 应用程序

当你配合 `SDK` 使用 `JavaFX` 版本 2.0.2 时，你被允许将应用程序部署在多个环境中，也可以通过 Java web start 或嵌入的网页作为独立应用程序运行。

### 为部署 JPadFX 准备

你将需要配合 `JPadFX` 应用程序的一些源文件。在将所有文件放入你正在使用的目录之后，你将被允许执行你放入应用程序中的命令。

示例：

```
Javae – pc “C: \ project source \ oracle \ javafx 2.0 DKS\ tr\ library\ trxfj. Glass” ; . -q in jpadfx. Java
```

请注意，只有当你电脑上安装了 2.0.2 版本时，此操作才能生效。

### 将 JPadFx 部署为独立应用程序

使用你在电脑上下载的版本，你将有一个工具用于插入你的命令，以便应用程序几乎自动地部署。当你查看它时，会有一个完全不同的目录用于此版本的程序。

在源文件编译后，你可以使用 `javafxpackager` 将类文件与启动器一起处理到一个新文件中。

示例：

```
Javafxpackager makeglass applicationtype jpadfx directory crs in directory outside in inside file jpadfx. Glass. D
```

#### 术语

- `makeglass`：将告诉程序在那个目录下创建一个新文件。
- `Applicationtype`：主类将与启动器一起标识。
- `Dircrs`：将识别目录。
- `In directory`：将识别文件名。
- `-d`：将告诉你输出是什么，以及错误信息将显示在哪里。

如果命令执行成功，你将引入一个新的函数。处理此问题的最简单的方法是使用 `jar` 工具。但，只有在你当前目录具有适当工具以及与其关联的子目录时，该命令才能执行并存储在目录中。

示例：

```
Glass fu in \ jpadfx. Glass icon.png
```

此时，将使用 `Jpadfx` 独立运行，以便你可以测试文件的真实性。但你需要切换出目录并进入一个具有需要执行的正确命令的新目录。

示例：

```
Java -pc “C: \ project source\ oracle\ javafx 2.0 DKS\ tr \ library \ jfxrt. Glass” ; . -glass jpadfx.glass
```

此命令将把类路径添加到正确的文件中，以便运行时被正确加载。

### 在网页中部署 JPadFX

可以使用 `javafxpackager` 来创建 HTML 页面，并带有正确的文件进行部署，以便在处理将应用程序嵌入网页或使用 Java web start 运行时的场景。

示例：

```
javafxpackager -execute -in directory in -in file jpadfx -how wide 500 -how tall 500 – directory crs in crs source jpadfx.glass -class of application jpadfx -title “jpad fx” -name “jpadfx is equal to jpad” -manager “Timothy Mason” – d
```

#### 术语解释：

- `Execute`：打包器将执行 HTML 和 JNLP 文件
- `Directory in`：标识文件所在的目录
- `Infile`：文件名
- `How wide`：页宽
- `How tall`：页高
- `Directory crs`：文件来源
- `Crs source`：标识

## 第 6 章：控制 Java 的流

在此之前的任何编程都被称为顺序编程，这意味着代码从上到下读取，每一行都按照其编写的方式进行读取。然而，并非所有程序都这样工作。某些代码必须满足条件才会运行。对于代码，你可能希望客户处于特定年龄。

这就是通过条件逻辑控制程序流的地方。条件语句通常使用 `if`，但可以使用其他词来创建条件。

### If 语句

当某些事情发生时，代码将执行，而不是等待其他事情。`if` 语句如下：

```
if ( statement ) {
}
```

`if` 单词在小写之前会将你的条件放置在一组括号中。大括号将用于划分代码块。这段代码只有在条件满足的情况下才会执行。

示例：

```
if( client < 18) {
}
```

此条件表示如果客户小于 18 岁。与其把所有内容都写出来，不如使用简写，使代码块更短且更易读。

示例：

```
if( client < 18) {
// 显示消息
}
```

### If … else

与其使用 `if` 语句，不如可以使用 `if then` 语句。

```
if( condition_to_test) {
}
else {
}
```



第一行仍将以 `if` 开头，随后是条件。大括号将划分代码的不同部分。

第二种选择将跟在 `else` 之后，并带有它自己的大括号。

你只有两种选择：你的客户要么小于 18 岁，要么大于 18 岁。你的代码必须匹配你想要发生的结果。

### If … else if

可以同时测试两个以上的条件。如果你想测试某个年龄范围，你将使用 `if else if` 语句。

语法如下：

```
If(condition_one) {

}

Else if ( condition_ two ) {

}

Else {

}
```

代码中新引入的部分是 `else if ( condition_two) { }`。

当 `if` 语句发送时，紧跟着将是圆括号。第二个条件将位于两个新括号之间，但它不会被第一个条件捕获。

代码仍然会用大括号隔开，你的每一个 `if else if` 语句都有它们自己的大括号。如果你漏掉了一个，你将会收到错误信息。

你需要的条件运算符有：

- 大于 (`>`)
- 小于 (`<`)
- 大于或等于 (`>=`)
- 小于或等于 (`<=`)
- 与/AND (`&&`)
- 或/OR (`||`)
- 等于 (`==`)
- 非/NOT (`!`)

两个 Amp` 符号将用于同时测试多个条件。

#### 示例：

```
else if ( client > 18 && client < 40)
```

通过这段代码，你需要了解 `client` 年龄的知识，并查看他们是否大于 18 岁但小于 40 岁。

你只是试图查看 `client` 输入的变量内部的内容。`client` 必须大于 18 岁但小于 40 岁。由于使用了 `AND` 运算符，你的 `client` 必须同时满足这两个条件。

### 嵌套的 if

`if` 语句可以像 `if else` 和 `if else if` 语句一样嵌套。嵌套的 `if` 语句是将一个 `if` 语句放入另一个 `if` 语句中。

#### 示例：

```
if( client < 19) {

system.out.println ( “ 18 or younger”) ;

}
```

要检查你的 `client` 是否超过十六六岁，必须在你已经创建的 `if` 语句内部放置另一个 `if` 语句。

第一个 `if` 语句将捕获小于 19 岁的 `client`，而第二个语句将缩小范围，使他们超过 16 岁。当你想要打印不同的消息时，可以使用 `if else` 语句。

#### 示例：

```
if( client < 20) {

if( client > 20 && client < 23 ) {

System.out.println( “You are 21 or 22”) ;

}

else {

System.out.println (“ 22 or younger”) ;

}

}
```

代码中放置的大括号必须准确，否则程序将无法运行。嵌套的 `if` 语句很难学，但可以逐步掌握。

### 布尔值

布尔值只有 `true` 或 `false`、`1` 或 `0`，甚至可以是 `yes` 或 `no`。Java 有一个专门用于布尔值的变量：

```
Boolean client = true ;
```

你不需要输入 `int`、`string` 或 `double`，你需要使用小写的 `b` 输入 `Boolean`。变量名将在被赋值为 `true` 或 `false` 值之后出现。

赋值将有一个等号。然而，如果你要评估变量并且它有某个值，那么你就需要使用两个等号。

#### 示例：

```
Boolean client = true;

if ( client == true) {

System.out.println (“it’s true”) ;

}
else {

System.out.println(“it’s false”) ;
```

`if` 语句将检查 `client` 输入的变量是否为 `true`。`else` 将检查它是否为 `false`。

当某结果不真时，你不需要说 `else if ( client == false)`，因为它显然是 `false`。

由于涉及布尔值只有两种选择，所以你将使用 `else`。

另一个用于条件的运算符是 `NOT` 运算符，它与布尔值配合。

#### 示例：

```
Boolean client = true;

if( !client) {

System.out.println (“it’s false”) ;

}

else {

System.out.println (“it’s true”) ;

}
```

这与任何用于布尔值的其他代码相同，除了 `if ( !client) {` 语句。

`NOT` 运算符将位于 `client` 变量之前。该运算符将使用单个感叹号，但它将落在待测试的变量之前。

代码将进行取反测试，这意味着它不是它实际的样子。

由于 `client` 变量已设置为 `true`，`!client` 最终将测试 `false` 值。

如果条件被设置为 `false`，那么 `NOT` 运算符将测试 `true` 值。

### 总结

再次感谢你下载这本书！

我希望这本书能够帮助你获得更多 Java 编程语言的知识并将其应用于你的编程需求中。

下一步是在学习更多主题的同时继续编程。

最后，如果这本书带给你任何价值并在某方面对你有帮助，我想请你一个忙，如果你愿意，在 Amazon 上给这本书留个评论？不胜感激！

感谢并祝你好运！

### 关于作者

Charlie Masterson 是一位计算机程序员和讲师，开发过多个应用程序和计算机程序。

作为一名计算机科学学生，他很早就对编程产生了兴趣，但学习高度复杂的主题让他感到挫败。

Charlie 想要一种可以轻松学习并开发编程技能的方法。他很快发现了一系列让他学得更快更好的教学教程。

通过这种方法，Charlie 成功地学习了不同的编程语言，现在正通过写书来教授这些主题。

![](cover.jpeg)

Java

The Simple Guide to Learn Java Programming In No Time (Java for Beginners, Java for Dummies, how to program, java app, java programming)

DAVID HOFFMAN

CONTENTS

[Introduction](#part0000_split_008.html__Toc451775675)

[Chapter 1 – General Programming Guidelines](#part0000_split_009.html__Toc451775676)

[Chapter 2- How & When to Use Exceptions](#part0000_split_010.html__Toc451775677)

[Conclusion](#part0000_split_011.html__Toc451775678)

I think next books will also be intersting for you:

[C++](https://www.amazon.com/Ultimate-Programming-beginners-database-computer-ebook/dp/B01DED6QNO?ie=UTF8&keywords=C%2B%2B%20robert%20hoffman&qid=1463743006&ref_=sr_1_1&s=digital-text&sr=1-1)

![C++3](images/00001.jpeg)

[Javascript](http://www.amazon.com/Javascript-javascript-programming-development-Developers-ebook/dp/B017YZ6CYG/ref=sr_1_7?s=digital-text&ie=UTF8&qid=1447666305&sr=1-7&keywords=javascript)

![D:\Физические книги\Covers\Javascript.cover.jpg](images/00002.jpeg)

[Computer Hacking](http://www.amazon.com/Computer-Hacking-Essential-Beginners-internet-ebook/dp/B010965F36/ref=sr_1_fkmr1_3?s=digital-text&ie=UTF8&qid=1444557942&sr=1-3-fkmr1&keywords=Computer+Hacking%3A+The+Essential+Hacking+Guide+for+Beginners+%28+Hacking%2C+How+to+Hack%2C)

![computerhacking](images/00003.jpeg)

[Hacking for Dummies](http://www.amazon.com/Computer-Hacking-beginners-computer-security-ebook/dp/B015T8FZYI/ref=sr_1_1?s=digital-text&ie=UTF8&qid=1446193044&sr=1-1&keywords=hacking+for+dummies+matt+benton)

![HACKING2](images/00004.jpeg)

[Python](http://www.amazon.com/Python-Ultimate-Learning-Programming-Hands--ebook/dp/B014MV238Y/ref=sr_1_1?s=digital-text&ie=UTF8&qid=1442836729&sr=1-1&keywords=Python%3A+Learn+Python+FAST+-+The+Ultimate+Crash+Course+to+Learning+the+Basics+of+the+Python+Programming+)

![D:\Физические книги\Covers\Python.jpg](images/00005.jpeg)

[SQL](http://www.amazon.com/SQL-Beginners-database-programming-Programming-ebook/dp/B019A7VQD8/ref=sr_1_25?ie=UTF8&qid=1451913155&sr=8-25&keywords=sql)

![SQL](images/00006.jpeg)

# Introduction

Most importantly, use common sense. When unable to find a rule or guideline.  When the rule clearly does not apply.  When all else fails: Please make use of common sense, check the fundamental principles of Java and coding. This rule overrides all of the others. Common sense is  a requirement.

1.  Program for people, not the machine. Use naming conventions. Document your code. Paragraph it. If no one else can figure it out, then it isn't any good.

2.  Design first, then code. Take the time to figure out how the code is going to be written before coding starts, you will definitely spend less time writing it. You reduce the impact of future changes on the code simply thinking about them first.

3.  Develop in small steps. It is much easier and faster to test and fix ten lines of code than 1000; one could program, test, and fix 100 lines of code in ten, 10-line increments in half the time that you could write one single 100 line block of code that did the same work.

4.  Keep your code simple.  Coding that needs to be redone later is nothing to be proud of, so follow the KISS rule: Keep It Simple, Stupid.

5.  Learn common patterns, anti-patterns, and idioms. There is a wealth of analysis available to guide you in increasing your development productivity, design, and process patterns and anti-patterns, as well as programming idioms.

# Chapter 1 – General Programming Guidelines

We will begin this tutorial by discussing general principles of good programming style as well as those that define robust design in Java. Most of these principles have been touched on in the introduction to Java Programming, however many new practical advices shall be introduced in this chapter to improve your skills as a Java developer.

Variable scope

within the Java programming language, each local variable, once it has been declared, has a definitive scope. The variable then becomes visible from the place where it is declared to the ending of the method, or code block that it is now declared in. Therefore, only one single rule is necessary to follow; declare the local variable as close as possible to the place where it is used. Below are some typical examples:

| 1 | for( final  Locale locale: Locale.getAvailableLocales() ) { |
| 2 |     // Some implementation here |

| 3 | } |
| 4 |  |

| 5 | try( final  InputStreamin = new  FileInputStream( "file.txt"  ) ) { |
| 6 |     // Some implementation here |

| 7 | } |

With each code snippet the local variable’s scope is limited only to what execution blocks they are now declared in. When the block ends, the local variable is not visible anymore and goes out of scope. The look is clean and concise but with the introduction of lambdas and the release of Java 8, Much of the  well-known idioms for using local variables are becoming totally obsolete.

Here is a rewrite of the ‘forEach’ loop from the above example utilizing lambdas instead:

| 1 | Arrays.stream( Locale.getAvailableLocales() ).forEach( ( locale ) -> { |
| 2 |         // Some implementation here |

| 3 |     } |
| 4 | ); |

Notice that the local variable becomes the argument of this function which then itself is passed as the argument of the forEach method.

Class fields and local variables

Every method in Java will belong to some distinct class (or, in some cases some interface, like Java 8 where the method is declared as default). There is a probability of some name conflicts with local variables that are used in method implementations and as class members. The Java compiler will pick the correct variable from the scope, however it may not be the exact one the developer intended to use. Many modern Java IDEs do much work to alert the developer when conflicts such as these are taking place (red script, highlighting and warnings) however, it is still better to be proactive while in the development.

Below is an example:

| 01 | public  class  LocalVariableAndClassMember { |
| 02 |      private  long  value; |

| 03 |  |
| 04 |      public  long  calculateValue( final  long  initial ) { |

| 05 |          long  value = initial;        |
| 06 |  |

| 07 |          value *= 10; |
| 08 |          value += value; |

| 09 |  |
| 10 |          return  value; |

| 11 |      } |
| 12 |  } |

This example appears to be very simple but there is one catch. The method called calculateValue introduces a local variable named value and hides the class member with the same name by doing that.  Code line 08 should sum the class member and the local variable but in application it does something different. A corrected version would look like that (with keyword this):

| 01 | public  class  LocalVariableAndClassMember { |
| 02 |      private  long  value; |

| 03 |  |
| 04 |      public  long  calculateValue( final  long  initial ) { |

| 05 |          long  value = initial;        |
| 06 |  |

| 07 |          value *= 10; |
| 08 |          value += this.value;        |

| 09 |  |
| 10 |          return  value; |

| 11 |      } |
| 12 |  } |

This simple implementation highlights an important issue that in some cases would take more than a few hours to troubleshoot and debug.

Method arguments and local variables

A different scenario that many beginning developers fall into is using method arguments as local variables. Java allows reassignment of  non-final method arguments with an alternate value (but this has no effect on the original value).

In example:

| 1 | public  String sanitize( String str ) { |
| 2 |     if( !str.isEmpty() ) { |

| 3 |         str = str.trim(); |
| 4 |     } |

| 5 |  |
| 6 |     str = str.toLowerCase(); |

| 7 |     return  str; |
| 8 | } |

This is not the cleanest piece of coding but it does highlight the problem: the method argumentstr has been  reassignedto a different value (and used as a local variable). In these cases (and without exception) this coding pattern should be avoided and can be by declaring method arguments asfinal.

Below is an example of this:

| 01 | public  String sanitize( final  String str ) { |
| 02 |     String sanitized = str; |

| 03 |  |
| 04 |     if( !str.isEmpty() ) { |

| 05 |         sanitized = str.trim(); |
| 06 |     } |

| 07 |  |
| 08 |     sanitized = sanitized.toLowerCase(); |

| 09 |     return  sanitized; |
| 10 | } |

Coding that  follows this simple rule is generally easier to follow and reason with. This is done even at the expense of introducing local variables.

Boxing and unboxing

Boxing and unboxing are Java techniques that allow conversion between primitive types (int,long,double) and respective primitive type wrappers (Integer,Long,Double).

Even though the Java compiler attempts to hide those conversions by performing autoboxing, this may make things worse and sometimes leads to random results.

Below is an  example:

| 1 | public  static  void  calculate( final  long  value ) { |
| 2 |     // Some implementation here |

| 3 | } |
| 1 | final  Long value = null; |

| 2 | calculate( value ); |

This code snippet compiles well, but it givesNullPointerException on line  02 as the conversion between  Long  and  long executes.The best point of  advice here would be to use the primitive type (but as we already know, in some cases it is not possible).

Interfaces

Interfaces should have preference over concrete classes where possible. This should convince you to at least consider interfaces first by showing these real examples.

Interfaces are only tied to default methods, not any particular implementation. They function merely as contracts, they provide much of the freedom and flexibility in the way the contracts could be fulfilled. Flexibility like this becomes more important if the implementation involves external services or systems.

Below is an example of a simple interface and its possible implementation:

| 1 | public  interface  TimezoneService { |
| 2 |     TimeZone getTimeZone( final  double  lat, final  double  lon) throws  IOException; |

| 3 | } |
| 01 | public  class  TimezoneServiceImplimplements  TimezoneService { |

| 02 |     @Override |
| 03 |     public  TimeZone getTimeZone(final  double  lat, final  double  lon) throws  IOException { |

| 04 |         final  URL url= new  URL( String.format( |
| 05 |             "[http://api.geonames.org/timezone?lat=%.2f&lng=%.2f&username=demo](http://api.geonames.org/timezone?lat=%25.2f&lng=%25.2f&username=demo)", |

| 06 |             lat, lon |
| 07 |         ) ); |

| 08 |         final  HttpURLConnection connection = ( HttpURLConnection )url.openConnection(); |
| 09 |  |

| 10 |         connection.setRequestMethod( "GET"  ); |
| 11 |         connection.setConnectTimeout( 1000  ); |

| 12 |         connection.setReadTimeout( 1000  ); |
| 13 |         connection.connect(); |

| 14 |  |
| 15 |         int  status = connection.getResponseCode(); |

| 16 |         if  (status == 200) { |
| 17 |             // Do something here |

| 18 |         } |
| 19 |  |

| 20 |         return  TimeZone.getDefault(); |
| 21 |     } |

| 22 | } |

The coding shown above demonstrates a common interface/implementation pattern. This implementation exclusively uses an external HTTP (note: NOT https, which is a secure server) service ([http://api.geonames.org/](http://api.geonames.org/)) that retrieves the time zone for a queried location. But, because the contact is interface driven, it is not difficult to introduce another implementation using flat file or a database. That way interfaces greatly help to design testable code. It may not be practical to call the external service on every test run, therefore it makes sense to provide this alternative, dummy implementation (also called stub or mock) as an alternative:

| 1 | public  class  TimezoneServiceTestImplimplements  TimezoneService { |
| 2 |     @Override |

| 3 |     public  TimeZone getTimeZone(final  double  lat, final  double  lon) throws  IOException { |
| 4 |         return  TimeZone.getDefault(); |

| 5 |     } |
| 6 | } |

The above implementation may be used in each place whereTimezoneService  interfacing is required, this isolates the test scenario from its dependency on external components.

Examples of appropriate interface use included inside the Java standard collection library.  Collection,List,Set,all those interfaces are backed by several more implementations that could be replaced  interchangeably and seamlessly when contracts may be preferred.

Below is an example of this:

| 1 | public  static< T > void  print( final  Collection< T > collection ) { |
| 2 |     for( final  T element: collection ) { |

| 3 |         System.out.println( element ); |
| 4 |     } |

| 5 | } |
| 1 | print( new  HashSet< Object >( /* ... */ ) ); |

| 2 | print( new ArrayList< Integer >( /* ... */ ) ); |
| 3 | print( new TreeSet< String >( /* ... */ ) ); |

| 4 | print( new Vector< Long >( /* ... */  ) ); |

Strings

Some of the most widely used types in Java and most of the programming languages are Strings. Java natively supports the concatenations and comparison through simplifying much of the routine operations over strings. The Java standard library also provides many unique classes to increase efficiency of strings operations.

Strings are immutable objects in Java, and are represented in UTF-16 format. Each time the strings are concatenated (or when any operation which modifies the original string is performed) a new instance ofString class is created. That is why the concatenation operations sometimes become ineffective, initiating many intermediate string instances (also called: generating garbage).

There are two very helpful classes provided in the Java standard library that aim to facilitate string manipulations:StringBuilder andStringBuffer (mainly different in thatStringBuffer is thread-safe while  StringBuilder  is not).

Below are a few examples using one of these classes:

| 01 | final  StringBuilder sb= new  StringBuilder(); |
| 02 |  |

| 03 | for( int  i = 1; i <= 10; ++i ) { |
| 04 |     sb.append( " "  ); |

| 05 |     sb.append( i ); |
| 06 | } |

| 07 |  |
| 08 | sb.deleteCharAt( 0  ); |

| 09 | sb.insert( 0, "["  ); |
| 10 | sb.replace( sb.length() - 3, sb.length(), "]"  ); |

Using  StringBuilder  /StringBuffer is recommended to manipulate strings, however it may look over the top when concatenating two or three strings; in this case the regular + operator may be used instead.

Below is an example:

| 1 | String userId= "user:"  + new  Random().nextInt( 100  ); |

The use of string formatting is an alternative to straightforward concatenation and Java standard library provides the static helper methodString.format.It also supports a complete set of format specifiers, including dates/times, characters, numbers, etc. (see the full reference [official documentation](https://docs.oracle.com/javase/7/docs/api/java/util/Formatter.html#syntax)).

Below explore the power of formatting by example:

| 1 | String.format( "%04d", 1  );                      -> 0001 |
| 2 | String.format( "%.2f", 15.643624d );             -> 15.64 |

| 3 | String.format( "%tR", new  Date() );              -> 14:07 |
| 4 | String.format( "%tF", new  Date() );              -> 2016-20-04 |

| 5 | String.format( "%d%%", 22  );                     -> 22% |

String.format method is a simple and clean way to construct strings originating in different data types. Some modern Java IDEs can analyze the format specification against the arguments passed on to the  String.format method and then warn developers when any mismatches are detected.

Naming conventions

There is no reason to strictly follow any specific naming conventions in Java, but there are a set of easy to follow rules that make Java code look uniform across standard library or any other Java project in the wild.

*   local variable and method arguments names are typed in camel case:str,newLength,minimumCapacity
*   static final field or enumeration constant names are typed in upper case, separated by underscore  ‘_’:LOG,MIN_RADIX,INSTANCE
*   class, enum, interface or annotation names are typed in capitalized case:StringBuilder,Runnable,@Override
*   generic type parameter names are usually represented as one character in upper case:  T,U,E
*   method or field names(exceptstatic final)are typed in camel case:isEmpty,format,addAll
*   package names are typed in lower case:org.junit,com.fasterxml.jackson,javax.json

With these simple conventions the code will look concise and indistinguishable other library or framework.

Standard Libraries

the Java standard libraries have some rough edges and strange design decisions but 99% of it is high quality code written by coding experts. It is worth being familiar with these resources.

Each new Java release includes many new features being added to existing libraries (and possible deprecation of the older ones) and addition of new libraries. Java 5 introduced a  new concurrency library that reconciles as  java.util.concurrent package. Java 6 debuteda scripting supportjavax.script package and Java compiler API  javax.tools package.  Java 7 included improvements to  java.util.concurrent,featured a  newI/O library under  java.nio.file package, and dynamic languages support with  java.lang.invoke package. Currently, Java 8 has delivered the long-awaited date/time API hosted as  java.time package.

Java’s platform is growing and evolving; it is extremely important to keep educated in  this evolution. Whenever a third-party library or framework is introduced into a project, ensure the required functionality is not available in the Java standard libraries.

Immutability

Please take immutability seriously. If a class being designed or a method being implemented might provide the immutability guarantee, it could be used almost universally without fearing concurrent modifications. This will improve life as a developer and team member.

Testing

Test-driven development (TDD) practices are widely practiced in the Java community, constantly working to raise the bar of the coding quality. TDD brings many benefits to the table, however Java standard library does not currently include any test framework or scaffolding.

Testing is still a necessary part of modern Java development.  Here we will cover some basics using a well written JUnit framework. Using JUnit, each test is a set of assertions regarding the expect object state or behavior.

Great tests are short and simple, testing one thing at a time. let us test to verify that  String.format  function from the section Strings  returns the desired results by writing a set of tests:

| 01 | package  com.javacodegeeks.advanced.generic; |
| 02 |  |

| 03 | import  static  org.junit.Assert.assertThat; |
| 04 | import  static  org.hamcrest.CoreMatchers.equalTo; |

| 05 |  |
| 06 | import  org.junit.Test; |

| 07 |  |
| 08 | public  class  StringFormatTestCase { |

| 09 |     @Test |
| 10 |     public  void  testNumberFormattingWithLeadingZeros() { |

| 11 |         final  String formatted = String.format( "%04d", 1  ); |
| 12 |         assertThat( formatted, equalTo( "0001"  ) ); |

| 13 |     } |
| 14 |  |

| 15 |     @Test |
| 16 |     public  void  testDoubleFormattingWithTwoDecimalPoints() { |

| 17 |         final  String formatted = String.format( "%.2f", 12.324234d ); |
| 18 |         assertThat( formatted, equalTo( "12.32"  ) ); |

| 19 |     } |
| 20 | } |

These tests are readable and execution is instantiations. A Java project contains hundreds of test cases, for quick feedback on regressions or features that are under development.

# Chapter 2- How & When to Use Exceptions

Introduction

Exceptions in Java signal abnormal, or exceptional, conditions in the flow of the program that may prevent it from making further progress. These exceptional conditions could be fatal; where the program is not able to function anymore and should be terminated.  Or the conditions could be recoverable; where the program continues to run but some functionality may be lost.

Here we will walk through a typical scenario utilizing exceptions in Java  Explain the checked and unchecked exceptions, and touch on some corner cases and helpful idioms.

Exceptions: when to use them

Simply put exceptions are events or signals that happen while a program is executing and interrupt the normal flow of execution. Exceptions are a replacement to the error codes and status checking techniques used in the early days of coding. Now exceptions have gained acceptance as the standard in dealing with error conditions in varied coding languages, including Java.

Exceptions handling has only one important rule universally: do not ignore them.  Each exception should be logged but never ignored. There are rare instances when an exception could be safely ignored because not much can be done with it.

Exceptions are a crucial part of argument validation and sanity checks. Every public method should verify inclusion of all required preconditions prior to doing any real work and raise the appropriate exception if some have not been met.

Checked and unchecked exceptions

Management of exceptions in the Java language is unique. There are two distinct classes of exceptions in Java: checked exceptions and unchecked exceptions. These two classes are primarily artificial, imposed by Java language rules and its compiler.  It should be noted that JVM makes no difference between them.

Unchecked exceptions signal erroneous conditions related to program logic and assumptions being made (invalid arguments, null pointers, unsupported operations, etc). An unchecked exception would be a subclass of RuntimeException and that is how Java compiler sees that a specific exception belongs to the class of unchecked items.

An unchecked exception is not required to be defined as caught by the caller or to be listed part of the method signature (this throws keyword).NullPointerException  is a widely known member of unchecked exceptions.

Here is its declaration from the Java standard library:

| 1 | public  class  NullPointerExceptionextends  RuntimeException { |
| 2 |     public  NullPointerException() { |

| 3 |         super(); |
| 4 |     } |

| 5 |  |
| 6 |     public  NullPointerException(String s) { |

| 7 |         super(s); |
| 8 |     } |

| 9 | } |

Checked exceptions show invalid conditions in areas outside the immediate control of the program (like memory, network, file system, etc). A checked exception is a direct subclass of Exception. Unlike the unchecked exceptions, checked exceptions must be aughtby the caller or listed as a part of the method signature (thisthrows keyword). The  IOException is the most known in checked exceptions:

| 01 | public  class  IOExceptionextends  Exception { |
| 02 |     public  IOException() { |

| 03 |         super(); |
| 04 |     } |

| 05 |  |
| 06 |     public  IOException(String message) { |

| 07 |         super(message); |
| 08 |     } |

| 09 |  |
| 10 |     public  IOException(String message, Throwable cause) { |

| 11 |         super(message, cause); |
| 12 |     } |

| 13 |  |
| 14 |     public  IOException(Throwable cause) { |

| 15 |         super(cause); |
| 16 |     } |

| 17 | } |

Checked and unchecked exceptions has introduced more boilerplate and ugly code patterns than solved the real problems. The typical pattern that has emerged within Java ecosystem is, to hide, or wrap, the checked exception within unchecked one.

Below is an example:

| 1 | try  { |
| 2 |     // Some I/O operation here |

| 3 | } catch( final  IOException ex ) { |
| 4 |     throw  new  RuntimeException( "I/O operation failed", ex ); |

| 5 | } |

A careful design of the exception hierarchies may reduce the amount of boilerplate code needed.

An Additional class of exceptions in Java that extends the Error class isOutOfMemoryError  orStackOverflowError.These exceptions indicate a fatal execution failure that leads to immediate program termination with no possible recovery.

Using try-with-resources

Stack unwinding is often caused by an exception being thrown.  It is common that program execution flow mutations happen in this same manner.  Resource leaks directly related to native resources that remain unclosed, network sockets and file handles, for example, are the result of these thrown exceptions.

A well-behaved, typical I/O operation in Java (prior to version 7) using a mandatoryfinally block to execute the cleanup:

| 01 | public  void  readFile( final  File file ) { |
| 02 |     InputStream in = null; |

| 03 |  |
| 04 |     try  { |

| 05 |         in = new  FileInputStream( file ); |
| 06 |         // Some implementation here |

| 07 |     } catch( IOException ex ) { |
| 08 |         // Some implementation here |

| 09 |     } finally  { |
| 10 |         if( in != null  ) { |

| 11 |             try  { |
| 12 |                 in.close(); |

| 13 |             } catch( final  IOException ex ) { |
| 14 |                 /* do nothing */ |

| 15 |             } |
| 16 |         } |

| 17 |     } |
| 18 | } |

Thefinally block lisnot well coded (but calling close method on the input stream could also result in  IOException exception), the attempt to close input stream (and free up the operation system resources behind it) will be performed. Exceptions should be never ignored, but the kind thrown by close method are the single exclusion of this rule.

Java 7 has had a new construct introduced into the language named try-with-resources which made overall resource management easier.

Below is the code snippet from above rewritten using try-with-resources:

| 1 | public  void  readFile( final  File file ) { |
| 2 |     try( InputStreamin = new  FileInputStream( file ) ) { |

| 3 |         // Some implementation here |
| 4 |     } catch( final  IOException ex ) { |

| 5 |         // Some implementation here |
| 6 |     } |

| 7 | } |

The resource is required to have implementation of the interface AutoCloseable in order to be used in the try-with-resources blocks. Java compiler expands this construct from behind the scenes to something more complex, and developers the code looks very readable and concise. This is a very convenient technique where appropriate.

Exceptions and lambdas

Unchecked exceptions will work as expected, but the syntax of Java’s lambda functions does not allow specification of the checked exceptions; unless those are defined by@FunctionalInterface  itself, which may be thrown.

The below code snippet should not compile with compilation error ‘Unhandled exception type IOException’ (which could be thrown at line03):

| 1 | public  void  readFile() { |
| 2 |      run( () -> { |

| 3 |          Files.readAllBytes( new  File( "some.txt"  ).toPath() ); |
| 4 |      } ); |

| 5 |  } |
| 6 |  |

| 7 |  public  void  run( final  Runnable runnable ) { |
| 8 |      runnable.run(); |

| 9 |  } |

The solution is to catch the  IOException exception within the lambda function body and re-throw the correctRuntimeException exception (passing the original exception as a cause).

Below is an example:

| 1 | public  void  readFile() { |
| 2 |     run( () -> { |

| 3 |         try  { |
| 4 |             Files.readAllBytes( new  File( "some.txt"  ).toPath() ); |

| 5 |         } catch( final  IOException ex ) { |
| 6 |             throw  new  RuntimeException( "Error reading file", ex ); |

| 7 |         } |
| 8 |     } ); |

| 9 | } |

A number of functional interfaces are declared and have the ability to throw any Exception from its implementation, but if not, like Runnable, wrapping, or catching the checked exceptions within unchecked ones is what to do.

Standard Java exceptions

The Java standard libraries provide a wealth of information on exception classes.  These classes are specifically designed to cover the majority of generic errors that may occur in the process program execution.  The table below shows the exception classes that are used most often, always consider these prior to defining your own. 

| Exception Class | Purpose |
| NullPointerException | Attempts to usenull  where an object is required. |
| IllegalArgumentException | Method passed an illegal or inappropriate argument. |
| IllegalStateException | Method invoked at an illegal or inappropriate time. |
| IndexOutOfBoundsException | Index (to a vector, to a string, or to an array) is out of range. |
| UnsupportedOperationException | Requested operation is not supported. |
| ArrayIndexOutOfBoundsException | An array was accessed with an illegal index. |
| ClassCastException | Code attempted to cast an object to a subclass where it is not an instance. |
| EnumConstantNotPresentException | Attempt to access anenum  constant by name and theenum  type contains no constant with the specified name. |
| NumberFormatException | Attempts to convert a string to one of the numeric types, but that the string does not have the appropriate format. |
| StringIndexOutOfBoundsException | Index is either negative or greater than the size of the string. |
| IOException | I/O exception of some sort has occurred. This class is the general class of exceptions produced by failed or interrupted I/O operations. |

Defining your own exceptions

Exception classes are very easily defined in Java language.  Exception hierarchies that have been carefully designed for detailed, erroneous conditions management and reporting and to allow detailed implementation. Achieving the correct balance is singularly important; especially in the event that there are too many exception classes that might complicate the development as well as inflate the amount of the code needed to catch exceptions or propagate them further down the stack.

All user-defined exceptions must be inherited from  RuntimeException class and be part of the class of unchecked exceptions, there are always some exclusions from the rule.

Below is defined exception to dial with authentication:

| 01 | public  class  NotAuthenticatedExceptionextends  RuntimeException { |
| 02 |     private  static  final  long  serialVersionUID = 2079235381336055509L; |

| 03 |  |
| 04 |     public  NotAuthenticatedException() { |

| 05 |         super(); |
| 06 |     } |

| 07 |  |
| 08 |     public  NotAuthenticatedException( final  String message ) { |

| 09 |         super( message ); |
| 10 |     } |

| 11 |  |
| 12 |     public  NotAuthenticatedException( final  String message, final  Throwable cause ) { |

| 13 |         super( message, cause ); |
| 14 |     } |

| 15 | } |

The purpose of this exception is to signal about non-existing or invalid user credentials during sing-in process, for example:

| 1 | public  void  signin( final  String username, final  String password ) { |
| 2 |     if( !exists( username, password ) ) { |

| 3 |         throw  new  NotAuthenticatedException( |
| 4 |             "User / Password combination is not recognized"  ); |

| 5 |     } |
| 6 | } |

Passing the informative message along with the exception helps to troubleshoot production systems. If the exception was re-thrown as the result of a different exceptional condition, the initial exception must be preserved using the cause constructor argument. This will help to source the problem.

Documenting exceptions

The next topic will be discussing how to make exceptions to be a part of the documentation as well.

A method that may throw the checked exception, as part of its implementation, should then be made  apart of the method signature.  This is done usingthrows declaration. The@throws tag is used for describing those exceptions within the Java documentation tool.

Below is an example:

| 1 | /** |
| 2 |  * Reads file from the file system. |

| 3 |  * @throws IOException if an I/O error occurs. |
| 4 |  */ |

| 5 | public  void  readFile() throws  IOException { |
| 6 |     // Some implementation here |

| 7 | } |

The unchecked exceptions are not declared as a part of method signature. Document them so the caller of the method is aware of possible exceptions that may be thrown (using the same @throws tag).

Below is an example:

| 1 | /** |
| 2 |  * Parses the string representation of some concept. |

| 3 |  * @param str String to parse |
| 4 |  * @throws IllegalArgumentException if the specified string cannot be parsed properly |

| 5 |  * @throws NullPointerException if the specified string is null |
| 6 |  */ |

| 7 | public  void  parse( final  String str ) { |
| 8 |     // Some implementation here |

| 9 | } |

Always document the exceptions that the methods could throw. It will help to implement proper exception handling and recovering (fallback) logic from the coding start, keeping them safe from troubleshooting issues in production systems.

Exceptions and logging

Logging ([http://en.wikipedia.org/wiki/Logfile](http://en.wikipedia.org/wiki/Logfile)) is a necessary part of any complex Java application, library or framework. It is a journal of the events in the application and exceptions that are the crucial part of the flow. Exceptions must be correctly logged and analyzed later in order to discover problems in the applications and troubleshoot.

Conclusion

Exceptions are an important feature of the Java language. Exceptions are the basis of the management of errors in Java. Exceptions make handling and signaling erroneous conditions an easy job and, in contrast to error codes, flags and statuses, once occurred, exceptions cannot be ignored.

# Conclusion

These words of advice will assist with the understanding of the  Java coding standards and guidelines described in this book more effectively. These tools may also be used when coding or programming in most languages.  Languages like Python, C++, CSS, and JavaScript all use general formats, succession rules, exceptions and standards to ensure that information is easily understood, edited and added to, so that improvements and new versions of programs and apps may be developed. 

1.  Understand the standards. Take time to understand greater productivity through each standard and guideline.  Do not declare each local variable on its own line simply because you were told to. Do it because there is an understanding that it increases the comprehension of your code.

2.  Believe in them. Following standards should be something that is always done because it is the best way to code.

3.  Follow them while you are coding, not as an afterthought. Clean code is easier. Both during development and maintenance. Following standards will increase productivity, while developing, and will make the code easier to maintain. If clean code is produced from the beginning, you can benefit from it as it is being created.

4.  Make them part of your quality assurance process. Ensure that the source code follows the standards adopted by who the work is being done for. Standards should be used as the basis to train and mentor developers to become more effective.

Java is a dynamic and useful coding languages, hopefully this book assisted you in your understanding some more advanced aspects of coding in Java.

Thank you for reading. I hope you enjoy it. I ask you to leave your honest feedback.
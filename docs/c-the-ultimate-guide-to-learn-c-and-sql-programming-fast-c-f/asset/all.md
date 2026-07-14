![](cover.jpeg)

SQL

The Ultimate Guide to Learn SQL and C++ Programming Fast     (sql, database programming, computer programming, c plus plus, C++ for beginners, how to program)

![D:\Физические книги\Covers\SQL.jpg](images/00001.jpeg)

SQL

Beginner’s Guide for Coding SQL (sql, database programming, computer programming, how to program, sql for dummies)

STEPHEN HOFFMAN

CONTENTS

[Introduction](#part0000_split_011.html__Toc438132837)

[Types of Databases](#part0000_split_012.html__Toc438132838)

[Chapter 1 –A Closer Look on Relational Model](#part0000_split_013.html__Toc438132839)

[Tables, Columns, and Rows](#part0000_split_013.html__Toc438132840)

[Keys](#part0000_split_013.html__Toc438132841)

[Chapter 2 – Examples of Relational Models](#part0000_split_014.html__Toc438132842)

[Chapter 3 – SQL Statements](#part0000_split_015.html__Toc438132843)

[SQL Facts](#part0000_split_015.html__Toc438132844)

[SQL Commands](#part0000_split_016.html__Toc438132845)

[Naming Values](#part0000_split_016.html__Toc438132846)

[Creating Data in SQL](#part0000_split_017.html__Toc438132847)

[Data Types](#part0000_split_018.html__Toc438132848)

[CHAPTER 4 – Coding in MySQL](#part0000_split_019.html__Toc438132849)

[SELECT Command Anatomy](#part0000_split_020.html__Toc438132850)

[FROM Command](#part0000_split_021.html__Toc438132851)

[Limiting The Results](#part0000_split_021.html__Toc438132852)

[Conclusion](#part0000_split_022.html__Toc438132853)

I think next books will also be interesting for you:

[C++](http://www.amazon.com/Ultimate-Programming-programming-beginners-Javascript-ebook/dp/B018O4BDS6/ref=sr_1_8?s=digital-text&ie=UTF8&qid=1450353561&sr=1-8&keywords=c%2B%2B)

![Clus1](images/00002.jpeg)

[Python](http://www.amazon.com/Python-Ultimate-Learning-Programming-Hands--ebook/dp/B014MV238Y/ref=sr_1_1?s=digital-text&ie=UTF8&qid=1442836729&sr=1-1&keywords=Python%3A+Learn+Python+FAST+-+The+Ultimate+Crash+Course+to+Learning+the+Basics+of+the+Python+Programming+)

![D:\Физические книги\Covers\Python.jpg](images/00003.jpeg)

[Javascript](http://www.amazon.com/Javascript-javascript-programming-development-Developers-ebook/dp/B017YZ6CYG/ref=sr_1_7?s=digital-text&ie=UTF8&qid=1447666305&sr=1-7&keywords=javascript)

![D:\Физические книги\Covers\Javascript.cover.jpg](images/00004.jpeg)

[Computer Hacking](http://www.amazon.com/Computer-Hacking-Essential-Beginners-internet-ebook/dp/B010965F36/ref=sr_1_fkmr1_3?s=digital-text&ie=UTF8&qid=1444557942&sr=1-3-fkmr1&keywords=Computer+Hacking%3A+The+Essential+Hacking+Guide+for+Beginners+%28+Hacking%2C+How+to+Hack%2C)

![computerhacking](images/00005.jpeg)

[Hacking for Dummies](http://www.amazon.com/Computer-Hacking-beginners-computer-security-ebook/dp/B015T8FZYI/ref=sr_1_1?s=digital-text&ie=UTF8&qid=1446193044&sr=1-1&keywords=hacking+for+dummies+matt+benton)

![HACKING2](images/00006.jpeg)

[Amazon Prime and Kindle Lending Library](http://www.amazon.com/Amazon-Prime-Kindle-Lending-Library-ebook/dp/B010K977AQ/ref=sr_1_1?s=digital-text&ie=UTF8&qid=1444656763&sr=1-1&keywords=Amazon+Prime+and+Kindle+Lending+Library%3A+Kindle+Unlimited%3A+Get+Your+Money%27s+Worth+from+Amazon+Prime+%28Free)

![Amazonprime2](images/00007.jpeg)

[Amazon Prime Kindle Lending Library](http://www.amazon.com/Amazon-Prime-Kindle-Lending-Library-ebook/dp/B00X2KNAUC/ref=sr_1_2?s=digital-text&ie=UTF8&qid=1448791166&sr=1-2&keywords=amazon+prime+kindle+lending+library+anthony+weber)

![Amazon](images/00008.jpeg)

# Introduction

A database serves as a container. It is a storage where programmer scan organize data in a constructive manner. Keep in mind that there is no need to create a database if you are only dealing with few amounts of data. For instance, handling hundreds of Excel spreadsheets require a database while five spreadsheets can be dealt with even without a database. In other words, organizing a threshold amount of data inside a database will save you from complex data management.

A Closer Look On Database

Organizing all data inside a database allows you to easily execute tasks such as querying the data, updating the data, and deleting previous data. Most of all, a database prevents conflicts from having multiple copies of data.

Let us say, for instance, that a company has to manage its overall financial expenses. Basically, there is a specific department to handle this and such department has several people in it. Now if these people have their own copies of the spreadsheets, then it will be somewhat difficult to come up with non-conflicting data considering the possibility of human errors.

A database, on the other hand, will be able to store and organize the data with higher accuracy and lesser conflicts.

Another example to help you understand what a database is, is by looking at your phone’s contact list. Each contact is a data and your smartphone serves as the database. With just a touch of a few buttons, you can easily get the contact you are looking for. You can easily edit the details of each contact as well. This advance data management is way better than listing each contact in a pen-and-paper phone directory.

Types of Databases

The different types of database are as follows:

*   Relational Databases
*   Object-Oriented Databases
*   Document-Based Databases

In this eBook, I will mainly focus on relational databases. Nevertheless, I will not hesitate to include the other two types if deemed necessary.

You might have been introduced to some sort of new database type such as NoSQL. They are considered to be under the category of the document-based databases. These databases are now becoming popular and you might think that it is better to study them instead of learning SQL.

Please do not consider the relational databases to be the things of the past. A lot of databases that we still have today use the relational model. Moreover, SQL is useful when it comes to relational data queries. Besides, the query language of newly popularized databases is still somehow related to SQLsince they were mostly developed after SQL.

In other words, jumping into the new type of databases without understanding SQL will give you tons of challenges along the way. Hence, you have made the right decision of learning SQL first before moving forward to other databases like MongoDB.

Without further ado, let me now bring you to the world of SQL.

# Chapter 1 –A Closer Look on Relational Model

The Structured Query Language, or SQL, was originally designed for relational model. It is the language used to define the relationships between multiple data. It is also the database programming language used to query data in a relationalschema.

So when did this all began?

The first relational database was created in the 60s and the programming in this model were primarily defined by mathematics.In fact, this model of database was based on Tuple Relational Calculus and Relational Algebra.

Don’t worry, though, there is no need for you to jump into algebra and calculus to handle relational databases. SQL will make relational database programming easier.

Tables, Columns, and Rows

In the relational database, the data is stored in a table. In this model, all tables have names. For instance, you may name a table as “people” while you may name another table as “sales”. These names refer to the kind of data stored inside the table. In other words, the table we call “people” contains data of people while the table we call “sales” contains data of sales.

Every table features a set of columns. These columns define the different pieces of data within the table. This what makes the relational model different from other types of databases. You will notice that there are some databases that store data altogether. In a relational model, however, all data is separated by columns and each column has a name. Each column can also restrict the category and size of data that will be added in it. For instance, some columns can only store strings while some columns can only store numbers. The restriction assigned to each column depends on the creator of the database.

Columns are also categorized by being required and not required. A required column means that every row in the table must have a data which corresponds to what the column requires. A not required column, on the other hand, means that we can assert a NULL value for each row under that column. As you go through SQL, you will find that NULL has a lot uses in database programming.

The primary point of using rows is to have retrievable data and containers where you can store data. Why do we store data? Simply because we want to get that data again in the future and we simply want a place for it to stay for the mean time. Hence, the core idea of a database.

Keys

One of the vital elements of a relational database are keys. We now know that a table has several columns and each column has names. Each column has related properties as well. One of these properties that we can assert in a column is a key.

In a relational database, we always assign a primary key for each row. This special type of key is used to uniquely determine a specific row. This means that the value of that key must remain unique and must not have any duplicates within the table. If, and only if, there is another table which contains that key in our relation model; then, we may merge those two tables together.

When merging two tables, there will always be primary keys that have no duplicates. Upon merging, you will notice that there will be a new column in the table with these keys. These keys are now known as the Foreign keys. They serve as links to the primary keys of the second table, allowing you to conveniently link rows from two separated tables.

Aside from primary keys and foreign keys, we also have the natural keys. Natural keys are global. This means that you cannot change them since they are used all over the globe to identify a single entity. Published books, for instance, always have natural keys which we know as ISBN. Each published book has its own unique ISBN which you need to use as primary keys when handling relational database for books. This is different when handling databases with unnatural keys like emails, people, where you need to invent your own primary keys for each row.

Let us use a database for people and their contact numbers as an example. We cannot consider the name as the primary key. We cannot consider the person’s phone number as the primary key as well. This is because it is possible that there are two or more people in the globe that have the same contact number, first name, or even last name. Hence, we should create the primary key ourselves. This is where the identity column comes in.

The identity column serves as an auto-incrementing column that continues to generate unique keys as we add data in the table. The key combination does not matter since what we only need is a unique key for every identity in our database.

# Chapter 2 – Examples of Relational Models

Since I have been using thepeople’s database in the previous chapter, I will now give to you a contacts database as a perfect example of a relational model.

A simple database for contacts typically looks like this:

| First Name | Last Name | Email Address |
| John | Doe | johndoe@email.com |
| Mae | Lee | maelee@email.com |

In this table, we have three columns that are looking for specific data. The first column requests for the first name. The second for the last name and the third for the email address of the person.

Our rows, excluding the first row, refers to a single entity. The row for our first entity refers to the person with the name John Doe and his email is johndoe@email.com. The row for our second entity refers to Mae Lee with an email address of maelee@email.com.

This is an example of a database with two entities divided by three columns.

Let us say that John Doe has two email addresses while Mae Lee has three. Some people will end up adding columns to add the additional data. Hence, the table will end up like this.

| First Name | Last Name | Email 1 | Email 2 | Email 3 |
| John | Doe | johndoe@... | johndoe2@... | NULL |
| Mae | Lee | maelee@... | maelee2@... | maelee3@... |

There is a problem here if we use this kind of database design. First, what if the problem we have at hand is to find how many email address each person has? It is quite difficult and cumbersome to get the answer we need. This is the disadvantage in using a column-base database. The second problem is that we will end up with a lot of NULL values for those people that only have one email address. Third, this design is not practical and you do not need to be a database specialist to realize that.

In order to address these three issues, here is how we can do it.

| Key | First Name | Last Name |
| 1 | John | Doe |
| 2 | Mae | Lee |

The first step is to create a table for the entity first. In this table, we assigned the first column for the primary keys. The second step is to create another table where we can store the values for these people’s email addresses. The second table will look like this.

| Key | Person’s Key | Email Address |
| 1 | 1 | johndoe@email.com |
| 2 | 1 | johndoe2@email.com |
| 3 | 2 | maelee@email.com |
| 4 | 2 | maelee2@email.com |
| 5 | 2 | maelee3@email.com |

In this table, you will see that there are two columns for the keys. The first column refers to the primary key designated to each email address. The second column refers to the foreign keys from our first table. This is an example of a one-to-many relational model.

In this model, we are able to organize the data in the most practical way possible. It is now easier for us to answer a query on how many emails each person has as well. This method is known as Normalization.

There are different ways to design your database and efficient designs depend on what queries you are trying to answer.

With all that being said, you are now ready to meet SQL.

# Chapter 3 – SQL Statements

SQL is a specific database language. We use this language to create statements. These statements are made up of valid words. Some of the words should be defined by SQL while some of the words should be defined by you. Some words you will be asserting in these statements are table names, column names, and variables or data that is inside your tables.

SQL Facts

Before we proceed, I would like to show you some important facts about SQL.

The first thing you need to know about SQL is that it is readable since it is written in the English language. In other words, it is easier to learn SQL more than any other programming languages.

Second is that you can do a lot more using SQL. This is in contrast with most people’s impressions that SQL is only used for data queries. This is wrong.

Third is that a valid SQL statement should end with a semi-colon (;). Although some people will tell you that it is no longer needed, I suggest adding it in your queries because it is part of the ANSI standard. Furthermore, it works fine with both old and modern databases. Semi-colons allow you to conveniently assert multiple statements together in what we call a batch.This method works even with modern databases.

The fourth is that SQL is not case-sensitive. You can put your variables in both lower and upper cases. Both ways will work out just fine in the structured query language. One good way to practice this is to assert SQL-specific keywords in uppercases and user-defined keywords in lowercases. This will allow you to efficiently and quickly identify the different keywords within a statement.

SQL Commands

It is important to keep in mind that all SQL statements begin with a command. The command is typically a verb to signify what the database needs to do. One good example of a command used in SQL statements is SELECT.

The SELECT command tells the database to select a set of data. As you can see, it is an English-based word and pretty much obvious of what the system will do. This is how the command looks like when used in an SQL statement.

| SELECTVALUESFROMTABLENAME; |

The example above is a generic example of an SQL statement and I will talk about it piece by piece later on.

Take note that the set of values or variables that you need to assert in a statement depends upon what command you are trying to execute.All these variables come in the statement right after the command.

Naming Values

As what I have already said, the SQL statement is made up of words that are within SQL specification and user-created names. This means that naming values such as keys, table names, columns, and etc. are significant in SQL.

There is no absolute rule in naming things in SQL. People have their own ways to name variables, but I suggest you follow the method I use in this book for the sake of consistency. Here are two naming rules that I will be implementing in this book:

*   All table names must be in singular form. (e.g. person, email, phone, user, etc.)
*   Column names should never be repeated in the database.

There are some people who prefer to use plural names for their table names. This is not wrong. Nevertheless, I am more comfortable when using singular form table names. As for the column names, there will always be a time when two or more columns from separated tables have the same name. Hence, what I do is to uniquely name each column for disambiguation purposes. For instance, instead of using ID as the column name for primary keys in both the user table and email table; I would rather use the names user_ID and email_ID for each column.

You should also take note that names in SQL are scoped. This means that the database itself must have a name. The tables within the database must have names too. The columns inside every table must be named as well. When calling for the table, its name must be scoped through the database name with the use of period (.) to separate the names. Hence, this is how they are going to look like when asserted in an SQL statement:

*   Database.Table
*   Table.Column

Creating Data in SQL

I have no intention to teach you how to create a database from scratch. As beginners, your tasks should only circle around adding or updating values to an already existing database. However, I have a feeling that some of you still have that eagerness to learn SQL in order to create the entire application including the database itself. And so, I will introduce that part of SQL, but just enough to help you jumpstart.

The SQL keyword to create a new database is the statement CREATE DATABASE and this falls under ANSI specification. Let us say you want to create a new database for contact numbers of people and you want to name this new database as Contacts. Here is how you are going to do it.

| CREATE DATABASE Contact; |

In order for you to work on that database, you need to use it first. The keyword we need here is the USE DATABASE command. This is how we are going to execute it.

| USE DATABASEContact; |

If you want to create a table inside the Contact database, then what you need to execute is the CREATE TABLE command and here is you do it.

| CREATE TABLE Contacts.User (…); |

After that, you can now put all column names, types, and definitions.

Data Types

Data types are important because it follows column restrictions. Each column has a rule on which type of data you can store in it.

Here are some of the major data types and their short descriptions.

| Data Type | Description |
| CHARACTER | Used to define the number of characters allowed in the column. No more, no less. |
| CHARACTER VARYING | Used to define the maximum number of characters allowed in the column. Can be less but not more than the specific value. |
| BINARY | Used to dedicate the column for hexadecimal data. |
| SMALLINT | Used to store numerical data ranging from -32, 768 to 32, 767. |
| INTEGER | Used to store numerical data ranging from -2, 147, 483, 648 to 2, 147, 483, 647. |
| BIGINT | Used to store numerical data ranging from -9, 223, 372, 036, 854, 775, 808 to 9, 223, 372, 036, 854, 775, 807. |
| BOOLEAN | Used to store either TRUE or FALSE values. |
| DATE | Used to store DAY, MONTH, and YEAR in the following format: YYYY-MM-DD. |
| TIME | Used to store SECOND, MINUTE, and HOUR in the following format: HH:MM:SS. |
| TIMESTAMP | Used to store both TIME and DATE. |

There are other data types supported that you can use for more complex numbers, for instance. There is also specific data type for UNICODE characters against regular characters. Now these are just a few of the flavors that you can use in database programming.

# CHAPTER 4 – Coding in MySQL

I will teach you how to code SQL database using MySQL. Why MySQL? First is because it is an open-source platform and you can get it for free. Second is because it is compatible with all major operating systems: Linux, OSX, and Windows. Third is because it features ANSI mode which enforces ANSI specifications to your database. Not all RDMs have this kind of feature.

In this chapter, I will teach you how to efficiently use the SELECT command. This will allow you to effectively use this command to create interesting and efficient data queries.

SELECT Command Anatomy

You should have learned by now that we have the SQL keyword SELECT which is a command to get specific data from our database. After the SELECT keyword, what should follow is the list of items we want to have from our database. We call it the “select list”. If the select list only contains variables, then you can simply write the statement in this manner:

| SELECT ‘[Variable]’,’[Variable]’; |

Most of the time, the select list contains the names of the columns. When it does, it is important to define which table can we find these columns. This is where the FROM command comes in.

For instance, our select list contains User (column A) and Email (column B) and we can find these columns inside the table named as Contact. In order to define which table to look for, we should include the FROM command by doing this.

| Format:SELECT [COLUMN_NAME], [COLUMN_NAME] FROM [TABLE_NAME];Example:SELECTUser,EmailFROMContact; |

But, what if I have a lot of columns in the table and I want to select them all, you ask? Well, this is where the power of the asterisk (*) comes in. This is known as the wildcard symbol in SQL statement. To select all columns inside a table, you need to execute a statement in this format.

| SELECT* FROM [TABLE_NAME]; |

As you can see, the wildcard symbol comes after the SELECT command. Now this is useful when selecting all the columns. If you do not need to select all the columns, then using the wildcard symbol may become dangerous and inefficient.

There are different ways to quickly assert multiple columns in an SQL statement depending upon the platform that you are using. I personally recommend that you avoid using the wildcard command since the inefficient use of this syntax may also break applications.

FROM Command

Selecting a single table is fairly easy to write an SQL statement. As you can see from previous examples, it only follows a simple format.

| FROM [TABLE_NAME] |

In FROM clause, you can shorten the name of your table by creating an alias for the table name. Let us say that your table name is “telecommunication” and you are looking for the list of owner names that can be found under the “owner” column of our table. Typing it with the use of the generic format will give you this.

| SELECTtelecommunication.ownerFROMtelecommunication; |

Why do we need to type the table name before the column name in our format above? This is because we must qualify the column by using the table name. Furthermore, this will save you from name collisions in the future if there will be columns with similar names. I suggest you make this a habit.

Going back to the topic, doing so is too much of inconvenience. We can shorten the table name by assigning an alias in the FROM clause. Here’s the format.

| SELECT [TABLE_NAME_ALIAS].[COLUMN_NAME] FROM [TABLE_NAME] [TABLE_NAME_ALIAS]; |

Using the owner column and telecommunication table, our new statement will look like this.

| SELECTt.ownerFROMtelecommunication t; |

As you can see, I assigned the letter “t” to be the alias of the table name. This is easier to write than repeating the complete name over and over again. Keep in mind that it is not necessary to use the first character of your table name as an alias. You can assign any alias to the table name and it can also be a combination of characters. Just make sure that you are consistent with the alias you use.

Limiting The Results

Whenever you execute a SELECT query, the database will give you all the rows under the column you specified. This means that if your table has 20, 000 rows, then it will return 20, 000 values to answer your statement.

There are two ways to address this issue. One is to assert additional clause after the FROM clause. The other is by adding the DISTINCT qualifier before the select list. This shown in this format.

| SELECT DISTINCT [SELECT LIST] FROM [TABLE_NAME]; |

This format will only give you distinct values in return instead of providing you with all the values under the specified column. This is the perfect way to have all the unique values under that column. For example, you have a table for your contacts and some entities were asserted in several rows because they own multiple phone numbers.

Relying on the generic format will give you duplicated results. This is not efficient if you only want to know who are your contacts, right? Using the DISTINCT qualifier will prevent you from receiving multiple rows for the same entity.

Here is our telecommunication table which has the column for owners and another column for the telecom company.

| Key | Owner | Company |
| 1 | Jean Grey | AT&T |
| 2 | Luke Skywalker | Comcast |
| 3 | Mae Lee | AT&T |
| 4 | Stan Lee | AT&T |

Let us say we want to find the list of telecom companies in our database. Using the generic format will give us three results for AT&T which is unnecessary. With the DISTINCT qualifier, however, we will get only two results – one for Comcast and another for AT&T which is what we really need.

Aside from DISTINCT qualifier, you can add the WHERE clause after the FROM clause to limit the results as well. The WHERE clause serves as a search engine with higher precision. This is done by using the following format.

| SELECT [SELECT LIST] FROM [TABLE_NAME] WHERE [EXPRESSION]; |

To give you a simple example, let us use another table for people’s first and last names. Let us name this table “person”.

| Key | First | Last |
| 1 | Lee | Mortis |
| 2 | Mae | Lee |
| 3 | John | Doe |
| 4 | Stan | Lee |
| 5 | Bruce | Lee |

Let us say imagine that this is our database for our customers and we would like to know how many customers do we have that have Lee as their family name. In order to do that, we need to the execute the WHERE clause command.

| SELECTp.lastFROMperson p WHEREp.last = ‘Lee’; |

This will address the database to look specifically under the last name column and merely focus on rows with Lee value under that column. It will ignore the rows with no Lee value under that column. In other words, you will only get the rows of your customers that have Lee as their last names.

The secret in understanding the WHERE clause is by taking note of the different operators you can use for WHERE expressions. These operators are similar to mathematical operators. This means that it is easy to remember them. In contrast with mathematics, the operators we use here also works for non-numerical data such as the equal (=) sign we have used in our WHERE clause above. Here is the list of the simple operators that you can use for the WHERE clause.

| Operators | Name & Description |
| = | Equal to – gives TRUE value if data on both sides are equal to one another. |
| <> | Not equal to – gives TRUE value if data on both sides are not equal to one another. |
| > | Greater than – gives TRUE value if data on the left side is greater than the data on the right side. |
| < | Less than – gives TRUE value if data on the left side is less than the data on the right side. |
| >= | Greater than or equal to – gives TRUE value if the data on the left is either greater than or equal to the data on the right. |
| <= | Less than or equal to – gives TRUE value if the data on the left is either less than or equal to the data on the right. |

These are the operators that will give you Boolean values when handling WHERE clauses for your SQL queries.

# Conclusion

At this point, you are now familiar how relational databases work and how efficient SQL in querying data from databases that utilize relational models.

It is important to take note of how to designate restrictions to columns and how to call them specifically using SELECT statements. You have also learned that SQL statements contain both SQL-defined keywords and user-defined keywords. These keywords are not case sensitive, but organizing and writing the statements in a visual-friendly manner is highly recommended. Doing so will not only give you convenience when viewing your SQL coding but other people as well. This is a best practice if you are working with a team.

It is also significant to qualify column names using table names when writing SELECT statements. This will prevent future issues when there are different tables with similar column names. You just learned how to shorten the table names using an alias.

You can also specify data extraction of the SELECT statement by using clauses such as FROM. Using the FROM clause allows you to specify which table to look at whenever your SQL statement looks for columns. Aside from that, FROM clause also allows you to assign an alias for the table name.

You also learned how to limit the number of answered values with the use of DISTINCT qualifier and the WHERE clause. Keep in mind that you have to avoid using the wildcard symbol since it is an inefficient way to extract data from your database. The WHERE clause, on the other hand, is a powerful command that you need to master as a beginner. Familiarize the different operators and try them out on an already built database.

I am aware that this book is basic, but it is enough to prepare you in moving forward to advanced studies in the structured query language. As a beginner, there is no need for you to rush immediately on how to create your own database. It is important to learn which database model does SQL functions first. By understanding the relational model, you will easily grasp the concept of SQL together with the statements that you can do using this language.

If you want to continue learning about SQL, then I suggest that you take advantage of the book’s sequel where you will be introduced to deeper clauses of SELECT statements. The second part also tackles about JOINS, handling data, and table creation

![D:\Физические книги\Covers\Cplusplus.jpg](images/00009.jpeg)

C++

C++ for Beginners, C++         in 24 Hours, Learn C++ fast!

STANLEY HOFFMAN

CONTENTS

[Introduction](#part0000_split_026.html__Toc438132820)

[Chapter One – Your First Program](#part0000_split_027.html__Toc438132821)

[Chapter Two – Variables](#part0000_split_028.html__Toc438132822)

[Using Variables](#part0000_split_028.html__Toc438132823)

[Chapter Three - Expanding Your Program](#part0000_split_029.html__Toc438132824)

[iostream Library](#part0000_split_029.html__Toc438132825)

[Chapter Four – Operators](#part0000_split_030.html__Toc438132826)

[Chapter Five– Conditionals](#part0000_split_031.html__Toc438132827)

[Chapter Six– Loops](#part0000_split_033.html__Toc438132828)

[Chapter Seven– Arrays](#part0000_split_034.html__Toc438132829)

[Chapter Eight– Functions](#part0000_split_035.html__Toc438132830)

[Chapter Nine– Pointers](#part0000_split_036.html__Toc438132831)

[Chapter Ten - Dynamic Memory](#part0000_split_037.html__Toc438132832)

[Chapter Eleven - Classes and Objects](#part0000_split_039.html__Toc438132833)

[Conclusion](#part0000_split_040.html__Toc438132834)

Introduction

C++ is an up and coming programming language that’s based on objects and compiling. If you’re someone who’s never programmed before, you might be confused by the words object and compiling.

A program that utilized compiling is read by the computer’s CPU rather than by being interpreted by a program installed on the computer to run that program. Therefore, the program speaks more to the computer’s processing system rather than a program.

You may already know this, but computers are not able to read letters and have to read binary code, so the code has to be translated into a computer readable one. This process is known as compiling. Now, object-oriented code is just how the code is structured. You’ll understand that tidbit a little better in the following chapters.

So what does that all mean and why do you need to know it? As a programmer using C++, you’re going to need more than just the average text editor. There only a few programming languages where that’s all you’ll need, and they’re not really programming languages. One of the things you are going to need is a compiler.

Another thing you’re going to want is an Integrated Development Environment, also known as an IDE. This is a programmer-oriented text editor that has a syntax highlighting and is compiler integrated. For Windows and Linux, you can use a few different options.

You don’t really need an IDE because a basic text editor will do, but something like Notepad is going to make things a little more difficult. Word processors are also a bad choice because they have autocorrect with spelling and grammar, which will mess up your code if you’re not careful.

To begin with C++, you should understand that it has a rigid syntax. This means the code is case sensitive, so typing ‘Hello’ is going to be different than typing ‘hello’. In addition, you should know that the programming language doesn’t care much about white space, so don’t worry about it.

So that’s about all you need to know about C++ when you first begin. Let’s get into some actual coding to get you started!.

Chapter One – Your First Program

![ANd9GcSiYFVzWNtEsPfcM_CSykJhn4tkkH-GCJ4xX-yvN9K3b23DtDU2aQ](images/00010.jpeg)Due to this being a short tutorial on how to get started with C++, we’re going to start you out with a program in the first chapter. Your first program is going to be very simple. All you’re going to do is write a single phrase on the screen, but it’s not as simple as writing it in a Word document. First, let’s take a look at the code and then we’ll go further into what it means.

![](images/00011.jpeg)

The line is going to tell the compiler it has to link to the iso stream library to the program. A library is a repository where snippets of code are stored, known as functions. The library also stores other things, like variables and sometimes operators.

The isostream library has code that will let you send characters into the text stream, which is then fed onto the screen. Think of it like a river. You’re the river’s source and the screen is the sea. Whatever is put into the river from the source is going to go onto the screen.

The following line, line two, lets the compiler known that you want to use the namespace known as std, which is a standard namespace. Namespaces are an area where the code is stored. This is useful if you have two pieces of code that have the same name. Normally, pieces of code are not able to share the same name, but if one of is in a separate namespace than the other, then they can have the same name.

The third line of code is the beginning of the code. It’s the main block, as the name implies. Everything inside the braces {} will be translated by the compiler. You’ll need that line in every program because nothing will happen without it.

Now comes the printing of the phrase, ‘Hello World!’ To do this, you use code that’s stored inside the isostream library. This part of the code is known as the statement or cout, which sends information to the stream. The << that comes after the coutis an operator. This means ‘output’, so with the coutit all translates to ‘output this stream’.

The following stream is ‘Hello, World!’ and is known as a string. Strings are a sequence of characters and are shown by enclosing them in double quotation marks. This ends with a semi-colon and signifies the end of the statement. If the semicolon is not used, then the program is not going to compile.

![https://potofcode.com/wp-content/uploads/2015/03/helloworld.gif](images/00012.jpeg)

The last line, not the closing brace, is very simple but also very important. It’s placed at the end of main and tells the computer that the main block has been finished. It will return a value of 0 to the CPU. A non-zero value will create an error, so it’s a necessary line.

Now that you have the source code of the program, you have to compile i. If the program closes once you run it, then try running it from the cmd/terminal prompt instead.

Now that you know how to create your first program and what it looks like let’s take a look at variables!

Chapter Two – Variables

In the last chapter, variables were mentioned and it was said that they would be discussed. Now is the time to discuss them. A variable is something that stores a value. Imagine that every variable is a box and every box is labeled with a name and category.

![http://img.c4learn.com/2012/02/Variable-in-Java.jpg](images/00013.jpeg)

The category is what type of item it’s storing and its name is the specific variable it’s called. Boxes are able to store many things, but only if that thing fits inside the box. This is the same with variables. They all have a type, name, and size that govern what they are and are not able to store.

For example, one type of variable is the integer. If you know basic mathematics, then you know that integers are zero, whole numbers, and their negative counterparts. So -5, 4, 0 and -378 are all integers. In addition, integer variables will have a fixed size.

They are only able to hold one number between two others. These are specific to the variable and will not be discussed quite yet, but a default integers range is between -231 = -2, 147, 483, 648 and 231– 1 = 2, 147, 483, 647\. You probably won’t need numbers larger than that yet, so we’ll save the rest for another time.

Here’s a table to see the different types of variables you can use.

![](images/00014.jpeg)

There are a few different variable types. You’ll probably use them all when you program, but for now you’re only going to use a few.

Using Variables

Take a look at the following program:

![](images/00015.jpeg)

Most of this program is going to look familiar, except for the fourth and sixth lines. The first unfamiliar part declares the variable. This is telling the compiler that you’re going to use a variable. In declarations, the variable type is going to come first. In the example, it's using the int type. Next is the variable’s name, which would be known as var.

It’s easy and simple. A variable name can be anything, but be sure it’s something relevant and not something that’s already reserved and means something in C++ and it doesn’t begin with a number or a special character. You should start with a lowercase letter, and end the statement with a semi-colon.

Line nine in the code above is known as an assignment and assigns a value to the variable. The equal sign is the assignment operator, and it is what does the assigning. The variable on the left is given the value on the right, and the = is a binary operator because it has two operands. One to the left and the other to the right. The operand on the right doesn’t have to be a value. It can be another variable. The left has to be a variable and you can’t change the meaning of the number seven. In the example, the integer variable var is a value of forty-two.

You can see the cout statement doesn’t have quotations marks around the variable name. That’s because you want to output the value of the var and not display the string ‘var’. If you were compiling the program, it would print ‘42’ because that is the value the var has. Try changing it to another integer and look at the output.

![images](images/00016.jpeg)

Variables also have prefixes that are added to their declaration that changes how they act. Some will change the size, and others will not allow negative numbers, and others might do something entirely different.

Now that you know about variables let’s talk about how to expand the program!

Chapter Three - Expanding Your Program

Now that you know how to use variables and how to put them into the program let’s take a look at how to expand the program. All you really know what to do is use the variables and put them into your program, so all you can really do is set the output and values of the variable. That isn’t useful when you’re creating a real program.

![images(2)](images/00017.jpeg)

What you need is a way to manipulate the variables and receive input from a user. So let’s take a look at the next!

iostream Library

You already know that the iostream library is able to output data, but it can also obtain input data, too. The command is very like the cout statement. The command is cin. There is one different, though. When you use cin, the operator after it’s inverted.

Instead of being <<, it’s >>. This is confusing to remember in the beginning, but you’ll learn it eventually. Note that when you run the program, you’ll need to press the enter key after you put in the desired information, like a terminal/cmd prompt.

Take a look at the following program to see the difference between the two.

![](images/00018.jpeg)

Now you can probably see that it’s simple to get the user’s input using the iostream library, which produces some more useful programs. iostream is a lot more powerful, though. You can combine many statements into one.

For example, to put out two strings or variables you would normally need two statements, but you can combine many cout statements and produce a much shorter code. All you have to do is just add another operator for the item you’re outputting or inputting.

For example:

![](images/00019.jpeg)

You can also combine together cinstatements in the same way you’d receive several parts of the input in a row. Enter has to be pressed after each one, and you can’t mix input and output on a line of code.

Now that you know how to combine code and expand your program let’s talk more about operators.

Chapter Four – Operators

You’ve learned how to output text, declare a variable and obtain input, but you can’t do anything with the variables. Sure, you can give them values, but what use is that in the real world? What you really need is a way to manipulate the variables without doing hard work. Luckily, the operators will save you!

You’ve already investigated two operators that are linked to the iostream library, the input and output or >> and <<.

![images](images/00020.jpeg)

These operators are able to be put into categorical groups, the first one being arithmetic operators. These are -, +, /, and *. You would use them exactly you would use them in math. For example, this piece of code will add two numbers together and display the results.

![](images/00021.jpeg)

Now that you know how to use operators let’s take a look at conditionals!

Chapter Five– Conditionals

It’s great to have a program that does single, linear tasks, like saying ‘Hello’, but it’s rare that you’re going to come across for the need of having a program that does linear tasks only. Programs usually use something known as conditions, or statements that can branch the code into different paths depending on whether a condition is true or not. It’s like a fork on the road, basically.

C++ conditionals have the form of if statements. For example, if something is true, execute this line of code, if something is false, execute another line of code. Take a look at the following code piece as an example.

![](images/00022.jpeg)

Lines one through five should be pretty obvious to you by this point, but line three is the one where you may need a little explanation. This is the example of the if statement. It operates by first taking the matter of the integer variable a, and checks to see if it’s less than 2\. If that’s true, then it’ll run the code that’s in the curly brackets.

If it’s not, then it will continue as if the piece of code didn’t exist. We know that 1 or the value of a is less than 2, so if you were to run this program, then you’d see ‘a is less than 2!’ on the screen.

Here there is another operator introduced, the less than one, <. If you’re familiar with math, then the use of this sign is pretty self-explanatory. If you’re not, then you’ll need to learn it. Note that while < looks like <<, they are not even close to the same thing and are not related in programming.

![images(3)](images/00023.jpeg)

Of course, C++ is a strong language, and so it’s able to do more powerful things using these condition if statements.

So in summary, C++ conditionals start with an if statement, and they can have a number of else ifs after them, too. An important thing you should remember is that once one of them has been satisfied, then all the rest is going to be skipped. If you want all of your if statements checked, then do several single if statements one after another.

Chapter Six– Loops

![images(4)](images/00024.jpeg)Now you’re able to write code that is able to read input from the user, do different things depending on the input, and then show the results, but if what if you want to do the same thing but with some different parameters, several times? It would be boring to write the same code over and over again, and awkward if you don’t know how many times you need to run that piece of code when you’re writing it. What if it depends on something the user entered?

![](images/00025.jpeg)

To complete this action, you’ll need to use something known as a loop. Loops are a piece of code that are repeated several times, one after another until a condition is met. C++ has three different types of loops. There’s the while loop, the for loop and the do while loop. Let’s start with the while loop since it’s the easiest.

While loops look like if statements, almost.

![](images/00026.jpeg)

The use of ‘while’ is evident when you know what while loops actually do. Here, the code is saying that ‘while the value of in the userInput variable does not equal 10, obtain some input from the user’. In addition, remember the ! means ‘not’ in C++, so the code ‘!=’ translates to not equal.

If the userInput is ten, then the code is not going to be executed and the loop will be skipped. While loops can be seen as being an if statement that jumps back to the information in itself once the code has been run.

Before we keep going, it’s important to know that the following piece of code is usable in C++:

![](images/00027.jpeg)

It actually has its own name. It’s an infinite loop so it will loop infinitely. Going through the code, you’d get something like ‘Is 1 equal to 1? Yes it is, print an ‘a’.’ This will repeat over and over again. There are other ways to make infinite loops, but you probably don’t want to make one.

The second type of loop is the do while loop. Do while loops look like this:

![](images/00028.jpeg)

While it looks different than the standard while loop you just saw, it’s almost the same thing, except there’s one difference. The while loop evaluates a condition to see if it’s true and will run the code if it is, and the do while loop will execute some code and then check to see if the condition is true. Due to this happening, no matter what you initialized as userInput to the code between the curly-brackets will definitely run.

The third type of loop is the for loop. This is the more complicated out of the three, but it’s powerful when you understand it. For now, let’s just cover the uses. Take a look at this for loop.

![](images/00029.jpeg)

This piece of code tells the program to start by setting the value i to 2 and as long as i is less than 10, then output its value to the screen and increment. You can easily replicate this loop using a while loop, but it uses a lot more line of code and is pretty untidy.

You should also know that the variables used in the first line of the for loop have to be the same variable. You also should remember that the first statement is not a conditional, it’s an assignment.

This kind of loop comes in handy when you want to step through various pieces of data, and you’ll see this when you read about arrays in the next chapter.

Chapter Seven– Arrays

Arrays are a list of variables that are grouped together because they have a common use. They don’t really have to have something in common, but when you put unrelated things together it’s not really a good idea. It’s like filling your filing cabinet with random papers and never organizing them. What the need for a filing cabinet of you’re going to do that?

Here’s a declaration of an array of integer variables.

1 int a [5];

You can see that arrays look like normal variables, but they have some square brackets at the ends. When you declare arrays, the brackets are then filled with the size of the array you’re looking for. In this case, you’re going to store five integer variables.

![images(2)](images/00030.jpeg)

An array can be whatever size you want as long as you have the RAM to spare, but it can hold only one type of variable at once. The variable type can be something you’d normally use.

Accessing a certain variable in the array is simplistic. You put the numbers of variables you want in the square brackets. So for the first variable you want [0], for the second you put [1] and keep going. Take a look at the following example.

![](images/00031.jpeg)

One thing you shouldn’t do is access a variable that’s not in the array that doesn’t exist, like the tenth variable in an array that has five places, or doesn’t have a variable assigned to it. If it doesn’t have a variable assigned to it, you’ll get what’s known as a garbage value because the value it returns is not going to be useable.

If the variable doesn’t exist, you can get a segmentation fault because the program will try to access a segment of memory that it’s not allowed to. This can result in the program terminating unexpectedly.

Now that you know how to create arrays let’s take a look at creating functions!

Chapter Eight– Functions

Functions are a great way of writing out complex programs without needing to repeat code. For example, let’s say you have a complicated part of code that gets some input from the user and parses it. Now let’s say you need to run the code several times, but not in a loop. Up until this point, you’d have to write it out every time.

![images(3)](images/00032.jpeg)

With modern copying and pasting, it’s not that big of a deal, but it’ll look horrible and having repeated code can be a problem when you go to fix any errors. To remedy this problem, you can create functions, which are pieces of code that you’re able to call repeatedly without needing to write it out every time.

Actually, you’ve already used a function. Main is a function. So let’s take a look at it to see how it works.

![](images/00033.jpeg)

Let’s examine the first line, the one that has the word main in it. This begins the definition of the function that will take no parameters, known as main, and will give back a value of type int. You already known what an int is, a type of variable, but what does return a value mean?

A function in C++ is like a function in math, you insert a number and some operation is performed on it, and you get an answer. Here, the int is the variable that the output function is going to be. A parameter is the variable that is put into the function, and then the function performs an operation before it returns the results.

Let’s take a look at a function that has a main.

![](images/00034.jpeg)

The parameters are written like a variable definition and is separated by a comma. They are written right after the function name and are closed in by parenthesis. Now there is an integer value known as argc and an array of characters known as argv as the parameter. You can use any type of variable you want as a function parameter, as long as when you use that function you provide a variable that’s of the same type.

Now that you know what a function is and does let’s take a look at pointers.

Chapter Nine– Pointers

RAM or random access memory is where the computer saves all the variables the program uses, and is basically a long line of numbers. Every number is identified by the address or where it is on that line. These are logical, so the number with the address four comes after the three but before the five.

The exact size of the number at that address is figured out by the computer architecture. Say you have two integers and a character. One might have an address of 1000 while the other has an address of 1004\. The character or char might have an address of 1008. So why is there a four byte gap between the variables? Integers are four bytes long, and so they take up four addresses in order to store their value. It doesn’t matter if you use one byte and don’t use the other three, it will still take up four bytes of memory.

![images(4)](images/00035.jpeg)

But why do you need to know this? C++ programmers need to know that their compiler does not have fancy addressing for them, translating their variables into addresses in RAM, but sometimes it’s good to know the translations on our own. Think about how the arrays work for a moment, they are just long lines of variables whose type is what the programmer tells the compiler.

So you might be thinking this is just like RAM and you’d be right. When you labeled the arrays and the fifth value was actually the number six because all arrays start at zero, you’re actually taking the fifth variable after the first variable. So if you say the array is an integer one, with the first integer coming from RAM address 1000, then combine that will what you know about integers being in four bytes, you can see that the nth integer in the array would have this address:

![](images/00036.jpeg)

Therefore, the address of the sixth element is 1020\. So why is this useful? You can make the array while the program is compiling and running and make it the proper size.

A pointer is a normal variable, but instead of storing the integer, it stores the address of another variable. Here is a pointer.

![](images/00037.jpeg)

In this pointer, you have a variable that stores the address of the integer. The * is the variable as a pointe rand not a normal variable. You’ve assigned it to the value of zero. When you assign values to pointers, you’re not giving them numbers or characters, you’re giving them the address of another variable.

Now that you know what they are, let’s move on to dynamic memory in the following chapter.

Chapter Ten - Dynamic Memory

So far you’ve been able to create variables at compile-time and modify them during run-time; however, you can create them in run-time, too when you use dynamic memory allocation. This method uses allocation and deallocation of RAM as the program is running. Since you’re accessing RAM, it’s natural to assume that you’ll do it with pointers, but dynamic memory in C++ is utilized differently than it is in C.

Take a look at the following block of code.

![](images/00038.jpeg)

Here you’ve made a pointer to an int and set aside some memory for it. Since i is still the pointer, not a variable, you’ll have to set the value pointed to by i to five and not i. This changes the location point by i and orphaned the set aside memory in RAM somewhere. This memory that’s been forgotten is known as memory leak. To stop this, be sure to deallocate the memory you set aside in the first place using the delete operator.

![images(5)](images/00039.jpeg)

Allocating memory down to single variables doesn’t help much, though. If you know the variable was going to exist then you could declare it normally. What this does is create variable size arrays that are not known as compile-time. How would you possibly know it, really? You can’t create an array of pointers and tap into them as you need them, that’s just a more RAM intensive version of making gigantic array and hoping everything goes well.

Now that you know what dynamic memory is and how to use it let’s take a look at classes and objects in the following chapter.

Chapter Eleven - Classes and Objects

This is actually what C++ was made to do, support classes and objects. Without them, C++ is just really C. But what are the classes and objects that have been mentioned before? Classes are like a type of mold and the object is the thing that comes from the mold. These molds are flexible and are able to be used to make whatever type of object you’d like. The molds can be general or they can be specific.

![images(5)](images/00040.jpeg)

So let’s say you want to make a vehicle. This is going to be an abstract tutorial as the code is not actually doing to do anything. Think of what properties a car needs. They need speed, price, color, manufacturer, and a model. What about if it’s four wheel drive or not? And what can you do with it? Can you start the engine and stop?

Let’s take a look at the class definition of what the car looks like.

![](images/00041.jpeg) ![](images/00042.jpeg)

![](images/00043.jpeg)

So as you can see, classes are defined a lot like structs, and that makes sense because they are both a way to group data. But this class contains something that a struct is not able to, functions.

Conclusion

So by now you know how to create your first, simple program and much more! You know what a variable is, how to expand your program, how to use operators, conditions, loops, arrays, functions, pointers, dynamic memory, and classes and objects to morph your program into a masterpiece! You see, C++ was not as difficult as you may have once though it was.

The next step is to gather the knowledge you’ve gleaned from this book and go on to read more about the wonderful world of C++ programming. Once you’re comfortable, set up a virtual machine to do your coding in and get started! You’ll learn a skill that’s highly valuable in the computer industry today.

Thank you for reading. I hope you enjoy it. I ask you to leave your honest feedback.
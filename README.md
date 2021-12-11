# The Server Tier

## Web Server Concept
----------------------
Web server is a computer where the web content is stored. Basically web server is used to host the web sites but there exists other web servers also such as gaming, storage, FTP, email etc.

In other words, a web server is a system that delivers content or services to end users over the internet. A web server consists of a physical server, server operating system (OS) and software used to facilitate HTTP communication.

A web server is also known as an internet server. 

Web server respond to the client request in either of the following two ways:

* Sending the file to the client associated with the requested ``URL``.

* Generating response by invoking a script and communicating with database.

**Some Famous Web Server:**

### Apache HTTP Server
This is the most popular web server in the world developed by the Apache Software Foundation. Apache web server is an open source software and can be installed on almost all operating systems including Linux, UNIX, Windows, FreeBSD, Mac OS X and more. About 60% of the web server machines run the Apache Web Server.

### Internet Information Services (IIS)
The Internet Information Server (IIS) is a high performance Web Server from Microsoft. This web server runs on Windows NT/2000 and 2003 platforms (and may be on upcoming new Windows version also). IIS comes bundled with Windows NT/2000 and 2003; Because IIS is tightly integrated with the operating system so it is relatively easy to administer it.

### Lighttpd
The lighttpd, pronounced lighty is also a free web server that is distributed with the FreeBSD operating system. This open source web server is fast, secure and consumes much less CPU power. Lighttpd can also run on Windows, Mac OS X, Linux and Solaris operating systems.

### Sun Java System Web Server
This web server from Sun Microsystems is suited for medium and large web sites. Though the server is free it is not open source. It however, runs on Windows, Linux and UNIX platforms. The Sun Java System web server supports various languages, scripts and technologies required for Web 2.0 such as JSP, Java Servlets, PHP, Perl, Python, and Ruby on Rails, ASP and Coldfusion etc.

### Jigsaw Server
Jigsaw (W3C's Server) comes from the World Wide Web Consortium. It is open source and free and can run on various platforms like Linux, UNIX, Windows, and Mac OS X Free BSD etc. Jigsaw has been written in Java and can run CGI scripts and PHP programs.

## Creating Dynamic Content
------------------------------
We can generate dynamic web content by using Server-side Scripting language like ASP.Net, C# ,PHP, Python ,Ruby etc.

The main reason for using a server-side scripting language is to be able to provide dynamic content to a site’s users. This is an important application because content that changes according to users’ needs or over time will keep visitors coming back to a site.

### PHP

The PHP Hypertext Preprocessor (PHP) is a programming language that allows web developers to create dynamic content that interacts with databases. PHP is basically used for developing web based software applications.

#### Basic PHP Syntax
A PHP script can be placed anywhere in the document.

A PHP script starts with ``<?php`` and ends with ``?>``:

```PHP
<?php
// PHP code goes here
?>
```
The default file extension for PHP files is ``.php``.

A PHP file normally contains HTML tags, and some PHP scripting code.

Below, we have an example of a simple PHP file, with a PHP script that uses a built-in PHP function "echo" to output the text "Hello World!" on a web page:

```PHP
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <?php
        echo "Hello World!";
    ?>
</body>
</html>
```

#### PHP Variable:

In PHP, a variable starts with the ``$`` sign, followed by the name of the variable:

```PHP
<?php
    $txt = "Hello world!";
    $x = 5;
    $y = 10.5;
?> 
```

>Note: When you assign a text value to a variable, put quotes around the value.

>Note: Unlike other programming languages, PHP has no command for declaring a variable. It is created the moment you first assign a value to it.

Rules for PHP variables:

* A variable starts with the ``$`` sign, followed by the name of the variable
* A variable name must start with a letter or the underscore character
* A variable name cannot start with a number
* A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and _ )
* Variable names are case-sensitive (``$age`` and ``$AGE`` are two different variables)

## Using Control Flow to Control Dynamic Content Generation
-----------------------------------------------------------
PHP supports a number of traditional programming constructs for controlling the flow of execution of a program.

Conditional statements, such as if/else and switch, allow a program to execute different pieces of code, or none at all, depending on some condition. Loops, such as while and for, support the repeated execution of particular code.

### PHP Conditional Statements
Very often when you write code, you want to perform different actions for different conditions. You can use conditional statements in your code to do this.

In PHP we have the following conditional statements:

* ``if statement`` - executes some code if one condition is true
* ``if...else statement`` - executes some code if a condition is true and another code if that condition is false
* ``if...elseif...else statement`` - executes different codes for more than two conditions
* ``switch statement`` - selects one of many blocks of code to be executed
 
#### **if statement**
The ``if`` statement executes some code if one condition is true.

Syntax:

```PHP
if (condition) 
{
  Statements;
}
```

#### **if...else statement**
The ``if...else`` statement executes some code if a condition is true and another code if that condition is false.`

Syntax:

```PHP
if (condition) 
{
  Statements;
} 
else 
{
  Statements;
}
```

#### **if...elseif...else statement**
The ``if...elseif...else`` statement executes different codes for more than two conditions.

Syntax:

```PHP
if (condition) 
{
  Statements;
} 
elseif (condition) 
{
  Statements;
} 
else 
{
  Statements;
}
```
Example Program:

```PHP
<?php
$a = 10; 
$b = 45;
if ($a > $b) 
{
  echo "$a is Greater.";
} 
elseif ($b > $a) 
{
  echo "$b is Greater.";
} 
else 
{
  echo "Both are Equal";
}
?>
```

#### **switch statement**

The ``switch`` statement is used to perform different actions based on different conditions.

Syntax:

```PHP
switch (Expression) 
{
  case (value 1):
  {
    Statements;
    break;
  }
  case (value 2):
  {
    Statements;
    break;
  }
    ...
  default:
  {
    Statements;
  }
}
```
Example:

```PHP
<?php
$favcolor = "red";
switch ($favcolor) 
{
  case ("red"):
    echo "Your favorite color is red!";
    break;
  case ("blue"):
    echo "Your favorite color is blue!";
    break;
  case ("green"):
    echo "Your favorite color is green!";
    break;
  default:
    echo "Your favorite color is neither red, blue, nor green!";
}
?> 
```

### PHP Loops:

Loops are used to execute the same block of code again and again, as long as a certain condition is true.

In PHP, we have the following loop types:

* ``while``-loops through a block of code as long as the specified condition is true
* ``do...while``-loops through a block of code once, and then repeats the loop as long as the specified condition is true
* ``for``-loops through a block of code a specified number of times
* ``foreach``-loops through a block of code for each element in an array

#### **``while`` Loop**

The ``while`` loop executes a block of code as long as the specified condition is true.

Syntax:
```PHP
while (condition) 
{
  Statements;
}
```

Example:
```PHP
<?php
$x = 1;
while($x <= 5) 
{
  echo "The number is: $x <br>";
  $x++;
}
?>
```

#### **``do while`` Loop**

The ``do...while`` loop - Loops through a block of code once, and then repeats the loop as long as the specified condition is true.The ``do...while`` loop will always execute the block of code once, it will then check the condition, and repeat the loop while the specified condition is true.

Syntax:
```PHP
do 
{
  Statements;
} while (condition); 
```

Example:
```PHP
<?php
$x = 1;
do
{
  echo "The number is: $x <br>";
  $x++;
} while ($x <= 5);
?> 
```

#### **``for`` Loop**

The ``for`` loop is used when you know in advance how many times the script should run.

Syntax:
```PHP
for (init counter; test counter; increment counter) 
{
  Statements;
} 
```

Example:
```PHP
<?php
for ($x = 0; $x <= 10; $x++) 
{
  echo "The number is: $x <br>";
}
?> 
```

#### **``foreach`` Loop**
The ``foreach`` loop works only on arrays, and is used to loop through each key/value pair in an array.

Syntax:
```PHP
foreach ($array as $value) 
{
  Statements;
} 
```

Example:
```PHP
<?php
$colors = array("red", "green", "blue", "yellow");
foreach ($colors as $value) 
{
  echo "$value <br>";
}
?> 
```

### PHP Break and Continue

#### **PHP Break**

``break`` statement breaks the execution of the current for, while, do-while, switch, and for-each loop. If you use break inside inner loop, it breaks the execution of inner loop only.

Example:
>This example jumps out of the loop when x is equal to 4:
```PHP
<?php
for ($x = 0; $x < 10; $x++) 
{
  if ($x == 4) 
  {
    break;
  }
  echo "The number is: $x <br>";
}
?> 
```

#### **PHP Continue**

``continue`` statement breaks one iteration (in the loop), if a specified condition occurs, and continues with the next iteration in the loop.

Example:
>This example skips the value of 4
```PHP
<?php
for ($x = 0; $x < 10; $x++) 
{
  if ($x == 4) 
  {
    continue;
  }
  echo "The number is: $x <br>";
}
?> 
```
### PHP Functions

The real power of PHP comes from its functions.

PHP has more than 1000 built-in functions, and in addition you can create your own custom functions.

* ``Built-in Functions: ``PHP has over 1000 built-in functions that can be called directly, from within a script, to perform a specific task.
* ``User Defined Functions: ``Besides the built-in PHP functions, it is possible to create your own functions.
  * A function is a block of statements that can be used repeatedly in a program.
  * A function will not execute automatically when a page loads.
  * A function will be executed by a call to the function.

**Create a User Defined Function in PHP**

A user-defined function declaration starts with the word function:

Syntax:

```PHP
function functionName(arguments) 
{
  Statements;
  return(value);
} 
```
Example:

```PHP
<?php
function addNumbers(int $a, int $b) 
{
  return $a + $b;
}
echo addNumbers(5, 5);
?>
```

### Array in PHP

An array is a special variable, which can hold more than one value at a time. An array can hold many values under a single name, and you can access the values by referring to an index number.

In PHP, the ``array()`` function is used to create an array:`

```PHP
array();
```

In PHP, there are three types of arrays:

* ``Indexed arrays`` - Arrays with a numeric index

  ```PHP
  <?php
  $cars = array("Volvo", "BMW", "Toyota");
  echo "I like " . $cars[0] . ", " . $cars[1] . " and " . $cars[2] . ".";
  ?> 
  ```

* ``Associative arrays`` - Arrays with named keys

  ```PHP
  <?php
  $age = array("Peter"=>"35", "Ben"=>"37", "Joe"=>"43");
  echo "Peter is " . $age['Peter'] . " years old.";
  ?> 
  ```

* ``Multidimensional arrays`` - Arrays containing one or more arrays

  ```PHP
  <?php
  $cars = array (
    array("Volvo",22,18),
    array("BMW",15,13),
    array("Saab",5,2),
    array("Land Rover",17,15)
  );
  echo $cars[0][0].": In stock: ".$cars[0][1].", sold: ".$cars[0][2].".<br>";
  echo $cars[1][0].": In stock: ".$cars[1][1].", sold: ".$cars[1][2].".<br>";
  echo $cars[2][0].": In stock: ".$cars[2][1].", sold: ".$cars[2][2].".<br>";
  echo $cars[3][0].": In stock: ".$cars[3][1].", sold: ".$cars[3][2].".<br>";
  ?> 
  ```

**Sort Functions For Arrays**

* ``sort()`` - sort arrays in ascending order
* ``rsort()`` - sort arrays in descending order
* ``asort()`` - sort associative arrays in ascending order, according to the value
* ``ksort()`` - sort associative arrays in ascending order, according to the key
* ``arsort()`` - sort associative arrays in descending order, according to the value
* ``krsort()`` - sort associative arrays in descending order, according to the key

## Sesson and State
----------------------

When you work with an application, you open it, do some changes, and then you close it. This is much like a Session. The computer knows who you are. It knows when you start the application and when you end. But on the internet there is one problem: the web server does not know who you are or what you do, because the HTTP address doesn't maintain state.

Session variables solve this problem by storing user information to be used across multiple pages (e.g. username, favorite color, etc). By default, session variables last until the user closes the browser.

So; Session variables hold information about one single user, and are available to all pages in one application.

**Start a Session:**

A session is started with the ``session_start()`` function.

Session variables are set with the PHP global variable: ``$_SESSION``.

```PHP
<?php
// Start the session
session_start();
?>
<!DOCTYPE html>
<html>
  <body>
    <?php
    // Set session variables
    $_SESSION["favcolor"] = "green";
    $_SESSION["favanimal"] = "cat";
    echo "Session variables are set.";
    ?>
  </body>
</html> 
```

>The ``session_start()`` function must be the very first thing in your document. Before any HTML tags.

**Destroy a PHP Session**

To remove all global session variables and destroy the session, use ``session_unset()`` and ``session_destroy()``

Here is the example to unset a single variable −

```PHP
<?php
  unset($_SESSION['counter']);
?>
```

Here is the call which will destroy all the session variables −

```PHP
<?php
  session_destroy();
?>
```

## Error Handeling
--------------------
Error handling in PHP is simple. An error message with filename, line number and a message describing the error is sent to the browser.

When creating scripts and web applications, error handling is an important part. If your code lacks error checking code, your program may look very unprofessional and you may be open to security risks.

**Different error handling methods:**

* Using the ``die()`` function
* Custom errors and error triggers
* Error reporting

### Using the ``die()`` function

The ``die()`` function prints a message and exits the current script.

This function is an alias of the ``exit()`` function.

```PHP
<?php
if(file_exists("mytestfile.txt")) 
{
  $file = fopen("mytestfile.txt", "r");
} 
else 
{
  die("Error: The file does not exist.");
}
?> 
```

### Custom errors and error triggers

Creating a custom error handler is quite simple. We simply create a special function that can be called when an error occurs in PHP.

This function must be able to handle a minimum of two parameters (``error level`` and ``error message``) but can accept up to five parameters (optionally: ``file``, ``line-number``, and the ``error context``):

Syntax:

```PHP
error_function(error_level,error_message,error_file,error_line,error_context)
```

Parameter:
* ``error_level``: Required. Specifies the error report level for the user-defined error. Must be a value number. See table below for possible error report levels
* ``error_message``: Required. Specifies the error message for the user-defined error
* ``error_file``: Optional. Specifies the filename in which the error occurred
* ``error_line``: Optional. Specifies the line number in which the error occurred
* ``error_context``: Optional. Specifies an array containing every variable, and their values, in use when the error occurred

#### Error Report levels

These error report levels are the different types of error the user-defined error handler can be used for

* ``E_ERROR``: A fatal run-time error. Execution of the script is stopped
* ``E_WARNING``: A non-fatal run-time error. Execution of the script is not stopped
* ``E_NOTICE``: A run-time notice. The script found something that might be an error, but could also happen when running a script normally
* ``E_USER_ERROR``: A fatal user-generated error. This is like an ``E_ERROR``, except it is generated by the PHP script using the function ``trigger_error()``
* ``E_USER_WARNING``: A non-fatal user-generated warning. This is like an ``E_WARNING``, except it is generated by the PHP script using the function trigger_error()
* ``E_USER_NOTICE``: A user-generated notice. This is like an ``E_NOTICE``, except it is generated by the PHP script using the function ``trigger_error()``
* ``E_STRICT``: Not strictly an error.
* ``E_ALL`` All errors and warnings (``E_STRICT`` became a part of ``E_ALL`` in PHP 5.4)

Now lets create a function to handle errors:

```PHP
function customError($errno, $errstr) 
{
  echo "<b>Error:</b> [$errno] $errstr<br>";
  echo "Ending Script";
  die();
} 
```
Set Error Handler

```PHP
set_error_handler("customError");
```

Since we want our custom function to handle all errors, the ``set_error_handler()`` only needed one parameter, a second parameter could be added to specify an error level.`

```PHP
<?php
//error handler function
function customError($errno, $errstr) 
{
  echo "<b>Error:</b> [$errno] $errstr";
}
//set error handler
set_error_handler("customError");
//trigger error
echo($test);
?> 
```
### Error reporting
Sets which PHP errors are reported

The ``error_reporting()`` function specifies which errors are reported.

PHP has many levels of errors, and using this function sets that level for the current script.

Syntax:
```PHP
error_reporting(level);
```

Example:
```PHP
<?php
// Turn off all error reporting
error_reporting(0);
// Report simple running errors
error_reporting(E_ERROR | E_WARNING | E_PARSE);
// Reporting E_NOTICE can be good too (to report uninitialized
// variables or catch variable name misspellings ...)
error_reporting(E_ERROR | E_WARNING | E_PARSE | E_NOTICE);
// Report all errors except E_NOTICE
error_reporting(E_ALL & ~E_NOTICE);
// Report all PHP errors
error_reporting(E_ALL);
// Report all PHP errors
error_reporting(-1);
// Same as error_reporting(E_ALL);
ini_set('error_reporting', E_ALL);
?>
```
### PHP Exceptions

An exception is an object that describes an error or unexpected behaviour of a PHP script.

Exceptions are thrown by many PHP functions and classes.

User defined functions and classes can also throw exceptions.

Exceptions are a good way to stop a function when it comes across data that it cannot use.

**Throwing an Exception**

The ``throw`` statement allows a user defined function or method to throw an exception. When an exception is thrown, the code following it will not be executed.

If an exception is not caught, a fatal error will occur with an ``"Uncaught Exception"`` message.

Example:
```PHP
 <?php
function divide($dividend, $divisor) 
{
  if($divisor == 0) 
  {
    throw new Exception("Division by zero");
  }
  return ($dividend / $divisor);
}
echo divide(5, 0);
?> 
```

**The try...catch Statement**

To avoid the error from the example above, we can use the ``try...catch`` statement to catch exceptions and continue the process.

Syntax:
```PHP
try 
{
  //code that can throw exceptions
}
catch(Exception $e) 
{
  //code that runs when an exception is caught
}
```

Example:
```PHP
<?php
function divide($dividend, $divisor) 
{
  if($divisor == 0) 
  {
    throw new Exception("Division by zero");
  }
  return ($dividend / $divisor);
}

try 
{
  echo divide(5, 0);
}
catch(Exception $e) 
{
  echo "Unable to divide.";
}
?> 
```
>The ``catch`` block indicates what type of exception should be caught and the name of the variable which can be used to access the exception. In the example above, the type of exception is ``Exception`` and the variable name is ``$e``.

**The ``try...catch...finally`` Statement**

The ``try...catch...finally`` statement can be used to catch exceptions. Code in the ``finally`` block will always run regardless of whether an exception was caught. If ``finally`` is present, the ``catch`` block is optional.

Syntax:
```PHP
try 
{
  //code that can throw exceptions
} 
catch(Exception $e) 
{
  //code that runs when an exception is caught
} 
finally 
{
  //code that always runs regardless of whether an exception was caught
}
```

Example:
```PHP
<?php
function divide($dividend, $divisor) 
{
  if($divisor == 0) 
  {
    throw new Exception("Division by zero");
  }
  return $dividend / $divisor;
}

try 
{
  echo divide(5, 0);
} 
catch(Exception $e) 
{
  echo "Unable to divide. ";
} 
finally 
{
  echo "Process complete.";
}
?> 
```
## Architecting Web Applocation
--------------------------------

**What Is Web Application Architecture?**

So, what’s web application architecture?

Briefly, the web application architecture is a “skeleton” or layout that displays the interactions between application components, middleware systems, user interfaces, and databases. This kind of interaction allows a number of applications to work together simultaneously.

Once a user opens a webpage, the server sends specific data to the browser as a response to the user’s request. To be precise, a web client (or user agent) may request web resources or more commonly-known web documents (HTML, JSON, PDF, and so on) through a web server. Then, voila ― with these minimal manipulations, the requested information appears. After that, the interaction between a user and a website starts.

**The Difference Between Software Architecture And Software Design**

Many believe software architecture and software design are interchangeable things but they are not.

``Software architecture`` is the skeleton and all the high-level components of a system and how they interact with each other. It answers the questions “Where?” and “How?”. Software architecture is a where you stop to decide:

* what it is you’re going to be doing;
* how you’re going to implement the business requirements at the high level;
* how to make the servers being arranged well;
* where the date are going to be stored;
* which components are going to be needing.

With a software architecture, it comes easier to see the big picture. The central aim of it is to identify both functional and quality requirements and handle them to improve the overall quality of an application. So, in general, with software architecture, you can monitor performance, scalability, and reliability.

Speaking of ``software design``, it’s more about the code level design, and it’s responsible for the functionality of each module and its purposes. It’s the “How” of the software development process. Once you’ve gone through an architecture step, it’s time for a software designer to think about functions, classes, interfaces and other details the app would have. Software design is the level of details or components, let us say.

For instance, you’re going to create an API. Software design level is exactly when you write an API spec. Therefore, when it comes to coding phases, the front-end and back-end developers can work to that spec.

Thus, with the help of design, programmers have an efficient common language to find solutions for repeated issues and conceptualize them. It minimizes the amount of work they do since there is no need to reinvent the wheel.

### **Web Application Architecture Components**

#### _DNS_
DNS or Domain Name System is a fundamental system that helps search a domain name and IP address, and in this manner, a particular server receives a request sent by a user. We can say that DNS is like a phonebook but for the Internet websites.

#### _Load Balancer_
Load Balancer primarily deals with horizontal scaling. With directing incoming requests to one of the multiple servers, the load balancer sends an answer to a user. Usually, web application servers exist in the form of multiple copies mirroring each other. Hence, any server processes requests in the same manner, and the load balancer distributes tasks among them so they will not be overcharged.

#### _Web App Servers_
This component processes a user’s request and sends documents (JSON, XMK, etc.) back to a browser. To perform this task, it usually refers to back-end infrastructures such as database, cache server, job queue, and others. Besides, at least two servers, connected to the load balancer, manage to process the user’s requests.

#### _Databases_
The name of this web application component speaks for itself. The database gives instruments for organizing, adding, searching, updating, deleting, and performing computations. In most cases, web application servers directly interact with the job servers.

#### _Caching Service_
Caching service provides storage for data, which allows storing and searching data. Whenever a user gets some information from the server, the results of this operation goes to cache. So, future requests return faster. In one word, caching allows you to refer to the previous result to make a computation much faster. Therefore, caching is effective when:

* the computation is slow;
* computation is likely to occur many times;
* when the results are the same for a particular request.

#### _Job Queue_ (optional)

Job queue consists of two components: the job queue itself and servers. These servers process jobs in the queue. It happens that most of the web-servers need to operate a vast amount of jobs that are not of primary importance. Therefore, when a job needs to be fulfilled, it goes to the job queue and is operated due to a schedule.

#### _Full-Text Search Service_ (optional)

Many web applications support the search by text function or so-called request, and then, an app sends the most relevant results to a user. This technology is named full-text search service. With the help of keywords, it searches the needed data among a vast number of documents.

#### _Services_

When a web application reaches a specific level, services are created in the form of separate apps. They are not that visible among other web application components, but the web application and other services interact with them.

#### _Data Warehouse_
Almost every modern application implies the work with data such as collecting, storing and analyzing. These processes require three stages:

* The data is sent to the data “firehose”, which provides a streaming interface for absorption and processing of data.
* Raw, processed, and additional data is sent to cloud storage.
* And processed and additional data also go to a data warehouse.

It’s a particular model of online storage and exchange of data through the Internet. The Data Warehouse can be used for storing a variety of files of different types such as videos, photos, or so on.

#### _CDN_

CDN or Content Delivery System deals with sending HTML files, CSS files, JavaScript files, and images. It delivers the content of the end server throughout the world, so people can load various sources.

### Models of Web Application Components

There are only three models of web application components. It’s closely related to the number of services and databases used for a web application. Here they are:

#### One Web Server, One Database
A peculiarity of this server is that it uses a single server as well as a single database. It makes this model the least reliable out of the three. Once the server goes down, so does such a model. Hence, this model is not commonly used for building web applications.

Nevertheless, it’s quite often used to run test projects and learn and understand the web application’s fundamentals.

#### Multiple Web Servers, One Database

This model of a modern web application design has quite an interesting feature: it doesn’t store any data. When a client gives information to the web server, it processes and writes it to the database, but managing this data takes place outside of the server. It’s called stateless architecture.

To operate this model, developers need at least two web servers. It’s essential for making the model more reliable because if one server goes down, another one will take charge. So, in such a failure, all the requests will automatically go to the new server, without affecting the web app’s functioning. Thus, this model is more reliable than a single server. However, if something happens to the database, the app will crash.

### Multiple Web Server, Multiple Databases

This is the most efficient and reliable web application model. The reason is that both servers and databases have multiple substitutions. So, in case of failure, there are two way-outs: to store data in all the accessible databases or distribute it evenly among them. Anyway, the web site will be safe and sound.

However, if you decide to distribute the data, it may happen that some data may become unavailable. But this scenario describes a database’s crush.

### Application Services

Above, we mentioned three so-called “Monolithic” models due to their server’s rigid and stable nature. In contrast, application services (microservices and serverless) tend to be agile since they simplify upgrades and scaling. Applying this model allows splitting up web servers into smaller parts: ‘services’ in microservices and ‘functions’ in serverless. Thus, modifying and scaling independently using each of them is easier.

### **Types of Web Application Architecture**

However blurred the line between frontend and backend development, web application works with them both. Let’s go into their types separately.

### Frontend:
  * **Single-Page Application (SPAs)**: Single-Page applications or SPAs aim to facilitate programmers’ work. To make an action on a website, a user has no need to load completely new pages every time. Instead, they can interact with it receiving updated content to the current page.
  This type of architecture web design is created in such a way that it requests the most necessary content and data. Thus, SPAs prevent interruptions into user activity to boost an intuitive and interactive user experience. By the way, JavaScript is the most common programming language in this type of architecture.

  * **Server-Side Rendered Application (SSR)**:SSR is the process of rendering a client-side Javascript framework website to HTML and CSS on the server. With the help of this tool, it’s possible to quickly deliver the most important assets, thus accelerating the browser’s speed rendering the page to the user takes less time.
  When you build an SSR app, the server compiles all the data and serves up a new HTML document on each request. And once the browser gets the CSS, it’s able to paint the UI, and it’s not necessary to wait for JavaScript to load. This is how it makes the page load faster.
### Backend:
  * **Microservices :** Microservices is one of the types of SOA (service-oriented architecture). In general, microservices deals with small and lightweight services and execute a single functionality. This type of web architecture design is efficient and productive. Developers may save much time in a pocket with the help of it. 
  Since the microservices’ components are not necessarily built with the same programming language, they are not interdependent. It means that developers are free to pick a technology they prefer, which in result, makes the microservices architecture development quicker and easier.

  * **Serverless Architecture :** From the name, you can guess that serverless architecture is the one that lacks servers. Well, it’s not so. In fact, it implies that configuring and administering servers running management software is no longer a necessity. But, the entire infrastructure is supported by third-party providers. A third-party provider contributes an outsourcing server and infrastructure management.
  In this type of web application architecture, an app developer consults a third-party cloud infrastructure services provider for an outsourcing server as well as infrastructure management.
  If you’re not eager to manage and support the servers and the hardware, the serverless architecture is a god’s send for you. This approach is great because you can execute the code logic leaving the infrastructure as it is.

**What is PHP?**

PHP is a web language based on scripts that allows developers to dynamically create generated web pages.

**What does the initials of PHP stand for?**

PHP means PHP: Hypertext Preprocessor.

**Which programming language does PHP resemble to?**

PHP syntax resembles Perl and C

**What does PEAR stands for?**

PEAR means “PHP Extension and Application Repository”. it extends PHP and provides a higher level of programming for web developers.

**What is the actually used PHP version?**

Version 5 is the actually used version of PHP.

**How do you execute a PHP script from the command line?**

Just use the PHP command line interface (CLI) and specify the file name of the script to be executed as follows:

php script.php

**How to run the interactive PHP shell from the command line interface?**

Just use the PHP CLI program with the option -a as follows:
php -a

**What are the correct and the most two common way to start and finish a PHP block of code?**

The two most  common ways to start and finish a PHP script are: <?php  ?> and <?  ?>

**How can we display the output directly to the browser?**

To be able to display the output directly to the browser, we have to use the special tags <?=  ?>.

**What is the main difference between PHP 4 and PHP 5?**

PHP 5 presents many additional OOP (Object Oriented Programming) features.

**Is multiple inheritance supported in PHP?**

PHP includes only single inheritance, it means that a class can be extended from only one single class using the keyword ‘extended’.

**What is the meaning of a final class and a final method?**

‘final’ is introduced in PHP5. Final class means that this class cannot be extended and a final method cannot be overrided.

**How comparison of objects is done in PHP5?**

We use the operator ‘==’ to test is two object are instanced from the same class and have same attributes and equal values. We can test if two object are refering to the same instance of the same class by the use of the identity operator ‘===’.

**How can PHP and HTML interact?**

It is possible to generate HTML through PHP scripts, and it is possible to pass informations from HTML to PHP.

**What type of operation is needed when passing values through a form or an URL?**

If we would like to pass values througn a form or an URL then we need to encode and to decode them using htmlspecialchars() and urlencode().

**How can PHP and Javascript interact?**

PHP and Javascript cannot directly interacts since PHP is a server side language and Javascript is a client side language. However we can exchange variables since PHP is able to generate Javascript code to be executed by the browser and it is possible to pass specific variables back to PHP via the URL.

**What is needed to be able to use image function?**

GD library is needed to be able execute image functions.

**What is the use of the function ‘imagetypes()’?**

imagetypes() gives the image format and types supported by the current version of GD-PHP.

**What are the functions to be used to get the image’s properties (size, width and height)?**

The functions are getimagesize() for size, imagesx() for width and imagesy() for height.

**How failures in execution are handled with include() and require() functions?**

If the function require() cannot access to the file then it ends with a fatal error. However, the include() function gives a warning and the PHP script continues to execute.

**What is the main difference between require() and require_once()?**

require() and require_once() perform the same task except that the second function checks if the PHP script is already included or not before executing it.

(same for include_once() and include())

**How can I display text with a PHP script?**

Two methods are possible:

<?php
echo "Method 1";
print "Method 2";
?>


**How can we display information of a variable and readable by human with PHP?**

To be able to display a human-readable result we use print_r().

**How is it possible to set an infinite execution time for PHP script?**

The set_time_limit(0) added at the beginning of a script sets to infinite the time of execution to not have the PHP error ‘maximum execution time exceeded’.It is also possible to specify this in the php.ini file.

**What does the PHP error ‘Parse error in PHP – unexpected T_variable at line x’ means?**

This is a PHP syntax error expressing that a mistake at the line x stops parsing and executing the program.

**What should we do to be able to export data into an Excel file?**

The most common and used way is to get data into a format supported by Excel. For example, it is possible to write a .csv file, to choose for example comma as separator between fields and then to open the file with Excel.

**What is the function file_get_contents() usefull for?**

file_get_contents() lets reading a file and storing it in a string variable.

**How can we connect to a MySQL database from a PHP script?**

To be able to connect to a MySQL database, we must use mysql_connect() function as follows:


<?php $database = mysql_connect("HOST", "USER_NAME", "PASSWORD"); mysql_select_db("DATABASE_NAME",$database); ?>

**What is the function mysql_pconnect() usefull for?**

mysql_pconnect() ensure a persistent connection to the database, it means that the connection do not close when the the PHP script ends.

**How the result set of Mysql be handled in PHP?**

The result set can be handled using mysql_fetch_array, mysql_fetch_assoc, mysql_fetch_object or mysql_fetch_row.

**How is it possible to know the number of rows returned in result set?**

The function mysql_num_rows() returns the number of rows in a result set.

**Which function gives us the number of affected entries by a query?**

mysql_affected_rows() return the number of entries affected by an SQL query.

**What is the difference between mysql_fetch_object() and mysql_fetch_array()?**

The mysql_fetch_object() function collects the first single matching record where mysql_fetch_array() collects all matching records from the table in an array.

**How can we access the data sent through the URL with the GET method?**

In order to access the data sent via the GET method, we you use $_GET array like this:

www.url.com?var=value
$variable = $_GET[“var”]; this will now contain ‘value’

**How can we access the data sent through the URL with the POST method?**

To access the data sent this way, you use the $_POST array.

Imagine you have a form field called ‘var’ on the form, when the user clicks submit to the post form, you can then access the value like this:

$_POST[“var”];

**How can we check the value of a given variable is a number?**

It is possible to use the dedicated function, is_numeric() to check whether it is a number or not.

**How can we check the value of a given variable is alphanumeric?**

It is possible to use the dedicated function, ctype_alnum to check whether it is an alphanumeric value or not.

**How do I check if a given variable is empty?**

If we want to check whether a variable has a value or not, it is possible to use the empty() function.

**What does the unlink() function means?**

The unlink() function is dedicated for file system handling. It simply deletes the file given as entry.

**What does the unset() function means?**

The unset() function is dedicated for variable management. It will make a variable undefined.

**How do I escape data before storing it into the database?**

addslashes function enables us to escape data before storage into the database.

**How is it possible to remove escape characters from a string?**

The stripslashes function enables us to remove the escape characters before apostrophes in a string.

**How can we automatically escape incoming data?**

We have to enable the Magic quotes entry in the configuration file of PHP.

**What does the function get_magic_quotes_gpc() means?**

The function get_magic_quotes_gpc() tells us whether the magic quotes is switched on or no.

**Is it possible to remove the HTML tags from data?**

The strip_tags() function enables us to clean a string from the HTML tags.

**what is the static variable in function useful for?**

A static variable is defined within a function only the first time and its value can be modified during function calls as follows:

	<?php
		function testFunction() {
			static $testVariable = 1;
			echo $testVariable;
			$testVariable++;
		}
		testFunction();
		//1 testFunction();
		//2 testFunction();
		//3
	?>


**How can we define a variable accessible in functions of a PHP script?**

This feature is possible using the global keyword.

**How is it possible to return a value from a function?**

A function returns a value using the instruction ‘return $value;’.

**What is the most convenient hashing method to be used to hash passwords?**

It is preferable to use crypt() which natively supports several hashing algorithms or the function hash() which supports more variants than crypt() rather than using the common hashing algorithms such as md5, sha1 or sha256 because they are conceived to be fast. hence, hashing passwords with these algorithms can vulnerability.

**Which cryptographic extension provide generation and verification of digital signatures?**

The PHP-openssl extension provides several cryptographic operations including generation and verification of digital signatures.

**How a constant is defined in a PHP script?**

The define() directive lets us defining a constant as follows:

define (“ACONSTANT”, 123);

**How can you pass a variable by reference?**

To be able to pass a variable by reference, we use an ampersand in front of it, as follows $var1 = &$var2

**Will a comparison of an integer 12 and a string “13” work in PHP?**

“13” and 12 can be compared in PHP since it casts everything to the integer type.

**How is it possible to cast types in PHP?**

The name of the output type have to be specified in parentheses before the variable which is to be cast as follows:

* (int), (integer) – cast to integer

* (bool), (boolean) – cast to boolean

* (float), (double), (real) – cast to float

* (string) – cast to string

* (array) – cast to array

* (object) – cast to object

**When a conditional statement is ended with an endif?**

When the original if was followed by : and then the code block without braces.

**How is the ternary conditional operator used in PHP?**

It is composed of three expressions: a condition, and two operands describing what instruction should be performed when the specified condition is true or false as follows:

Expression_1 ? Expression_2 : Expression_3;

**What is the function func_num_args() used for?**

The function func_num_args() is used to give the number of parameters passed into a function.

**If the variable $var1 is set to 10 and the $var2 is set to the character var1, what’s the value of $$var2?**

$$var2 contains the value 10.

**What does accessing a class via :: means?**

:: is used to access static methods that do not require object initialization.

**In PHP, objects are they passed by value or by reference?**

In PHP, objects passed by value.

**Are Parent constructors called implicitly inside a class constructor?**

No, a parent constructor have to be called explicitly as follows:

parent::constructor($value)

**What’s the difference between __sleep and __wakeup?**

__sleep returns the array of all the variables that need to be saved, while __wakeup retrieves them.

**What is faster?**

1- Combining two variables as follows:

$variable1 = 'Hello ';

$variable2 = 'World';

$variable3 = $variable1.$variable2;

Or

2- $variable3 = "$variable1$variable2";

$variable3 will contain “Hello World”. The first code is faster than the second code especially for large large sets of data.

**what is the definition of a session?**

A session is a logical object enabling us to preserve temporary data across multiple PHP pages.

**How to initiate a session in PHP?**

The use of the function session_start() lets us activating a session.

**How is it possible to propagate a session id?**

It is possible to propagate a session id via cookies or URL parameters.

**What is the meaning of a Persistent Cookie?**

A persistent cookie is permanently stored in a cookie file on the browser’s computer. By default, cookies are temporary and are erased if we close the browser.

**When sessions ends?**

Sessions automatically ends when the PHP script finishs executing, but can be manually ended using the session_write_close().

**What is the difference between session_unregister() and session_unset()?**

The session_unregister() function unregister a global variable from the current session and the session_unset() function free all session variables.

**What does $GLOBALS means?**

$GLOBALS is associative array including references to all variables which are currently defined in the global scope of the script.

**What does $_SERVER means?**

$_SERVER is an array including information created by the web server such as paths, headers, and script locations.

**What does $_FILES means?**

$_FILES is an associative array composed of items sent to the current script via the HTTP POST method.

**What is the difference between $_FILES[‘userfile’][‘name’] and $_FILES[‘userfile’][‘tmp_name’]?**

$_FILES[‘userfile’][‘name’] represents the original name of the file on the client machine,

$_FILES[‘userfile’][‘tmp_name’] represents the temporary filename of the file stored on the server.

**How can we get the error when there is a problem to upload a file?**

$_FILES[‘userfile’][‘error’] contains the error code associated with the uploaded file.

**How can we change the maximum size of the files to be uploaded?**

We can change the maximum size of files to be uploaded by changing upload_max_filesize in php.ini.

**What does $_ENV means?**

$_ENV is an associative array of variables sent to the current PHP script via the environment method.

**What does $_COOKIE means?**

$_COOKIE is an associative array of variables sent to the current PHP script using the HTTP Cookies.

**What does the scope of variables means?**

The scope of a variable is the context within which it is defined. For the most part all PHP variables only have a single scope. This single scope spans included and required files as well.

**what the difference between the ‘BITWISE AND’ operator and the ‘LOGICAL AND’ operator?**

$a and $b:    TRUE if both $a and $b are TRUE.

$a & $b:        Bits that are set in both $a and $b are set.

**What are the two main string operators?**

The first is the concatenation operator (‘.’), which returns the concatenation of its right and left arguments. The second is (‘.=’), which appends the argument on the right to the argument on the left.

**What does the array operator ‘===’ means?**

$a === $b TRUE if $a and $b have the same key/value pairs in the same order and of the same types.

**What is the differences between $a != $b and $a !== $b?**

!= means inequality (TRUE if $a is not equal to $b) and !== means non-identity (TRUE if $a is not identical to $b).

**How can we determine whether a PHP variable is an instantiated object of a certain class?**

To be able to verify whether a PHP variable is an instantiated object of a certain class we use instanceof.

**What is the goto statement useful for?**

The goto statement can be placed to enable jumping inside the PHP program. The target is pointed by a label followed by a colon, and the instruction is specified as a goto statement followed by the desired target label.

**what is the difference between  Exception::getMessage and Exception::getLine ?**

Exception::getMessage lets us getting the Exception message and Exception::getLine lets us getting the line in which the exception occurred.

**What does the expression Exception::__toString means?**

Exception::__toString gives the String representation of the exception.

**How is it possible to parse a configuration file?**

The function parse_ini_file() enables us to load in the ini file specified in filename, and returns the settings in it in an associative array.

**How can we determine whether a variable is set?**

The boolean function isset determines if a variable is set and is not NULL.

**What is the difference between the functions strstr() and stristr()?**

The string function strstr(string allString, string occ) returns part of allString from the first occurrence of occ to the end of allString. This function is case-sensitive. stristr() is identical to strstr() except that it is case insensitive.

**what is the difference between for and foreach?**

for is expressed as follows:

for (expr1; expr2; expr3)

statement

The first expression is executed once at the beginning. In each iteration, expr2 is evaluated. If it is TRUE, the loop continues and the statements inside for are executed. If it evaluates to FALSE, the execution of the loop ends. expr3 is tested at the end of each iteration.

However, foreach provides an easy way to iterate over arrays and it is only used with arrays and objects.

**Is it possible to submit a form with a dedicated button?**

It is possible to use the document.form.submit() function to submit the form. For example: <input type=button value=”SUBMIT” onClick=”document.form.submit()”>

**What is the difference between ereg_replace() and eregi_replace()?**

The function eregi_replace() is identical to the function ereg_replace() except that it ignores case distinction when matching alphabetic characters.

**Is it possible to protect special characters in a query string?**

Yes, we use the urlencode() function to be able to protect special characters.

**What are the three classes of errors that can occur in PHP?**

The three basic classes of errors are notices (non-critical), warnings (serious errors) and fatal errors (critical errors).

**What is the difference between characters \034 and \x34?**

\034 is octal 34 and \x34 is hex 34.

**How can we pass the variable through the navigation between the pages?**

It is possible to pass the variables between the PHP pages using sessions, cookies or hidden form fields.

**Is it possible to extend the execution time of a php script?**

The use of the set_time_limit(int seconds) enables us to extend the execution time of a php script. The default limit is 30 seconds.

**Is it possible to destroy a cookie?**

Yes, it is possible by setting the cookie with a past expiration time.

**What is the default session time in php?**

The default session time in php is until closing of browser

**Is it possible to use COM component in PHP?**

Yes, it’s possible to integrate (Distributed) Component Object Model components ((D)COM) in PHP scripts which is provided as a framework.

**Explain whether it is possible to share a single instance of a Memcache between multiple PHP projects?**

Yes, it is possible to share a single instance of Memcache between multiple projects. Memcache is a memory store space, and you can run memcache on one or more servers. You can also configure your client to speak to a particular set of instances. So, you can run two different Memcache processes on the same host and yet they are completely independent. Unless, if you have partitioned your data, then it becomes necessary to know from which instance to get the data from or to put into.

**Explain how you can update Memcached when you make changes to PHP?**

When PHP changes you can update Memcached by

•  Clearing the Cache proactively: Clearing the cache when an insert or update is made

•  Resetting the Cache: It is similar to the first method but rather than just deleting the keys and waiting for the next request for the data to refresh the cache, reset the values after the insert or update.
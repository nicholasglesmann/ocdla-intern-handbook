# OCDLA Intern Handbook



Intro text here. Something about OCDLA in general.







[TOC]






























































### OCDLA and PHP

OCDLA uses PHP to power all the back-end functionality of various web applications. PHP is a scripting language that is syntactically similar to JavaScript, with several key differences that are outlined below.



#### PHP Files

PHP files always end with the file extension ".php": ```hello.php```




To use PHP inside the file, you must surround your PHP code with PHP tags: 

- Opening PHP Tag: ```<?php```
- Closing PHP Tag: ```?>```

```php
<?php echo 'Hello World'; ?>
```



PHP files can also include any code that you might include in a standard HTML file:

```php
<html>
	<head>
		<title>PHP Test</title>
	</head>
	<body>
		<?php echo '<p>Hello World</p>'; ?>
	</body>
</html>
```



At OCDLA, we use two basic types of PHP files:

- **Template ** -  ```example.tpl.php```
	
	- Template PHP files generally include PHP code combined with HTML .
	
	  
	
- **Standard**  -  ```example.php```
	
	- Standard PHP files generally include only PHP code.
	
	  

-----

#### PHP Echo and Print

There are two basic ways to get output in PHP: `echo` and `print`.







-----

#### PHP Variables

All PHP variables (except constants) begin with a dollar sign ```$```.  All variables (including constants) are case sensitive. Variable names must start with a letter or underscore and can be followed by letters, numbers, or underscores.

```php
<?php 
	$text = "Hello World"; 	// valid
	$_number = 42; 			// valid
	$4score = 80; 			// invalid
?>
```



There are no keywords for declaring variables in PHP; it is created when you first assign a value to it. You can still declare the variable before you assign a value to it.

```php
<?php
    $var;
	$var = "Being created now.";
?>
```



PHP is a loosely-typed language (like JavaScript), which means that you do not need to declare the "type" of variable when creating it.




To use a variable, you simply type it's name. Don't forget that dollar sign!

```php
<?php
	$text = "Hello World";
	echo $text;
?>
```




> ###### Additional Information: 
>
> PHP Manual: https://www.php.net/manual/en/language.variables.php
> W3Schools: https://www.w3schools.com/php/php_variables.asp



------


#### PHP Constants

PHP constants are similar to constants in JavaScript and C#. 



Constants **do not** begin with a dollar sign. Constants are case sensitive by default (this can be changed). Constant names must start with a letter or underscore and can be followed by letters, numbers, or underscores.



The syntax for defining constants is slightly different:

```php
<?php
	define("VARIABLE_NAME", "Variable Value");
?>
```



Constants in PHP have global scope. To use a constant, just type it's name:

```
<?php
	define("DEFAULT_GREETING", "Hello World");
	echo DEFAULT_GREETING;
?>
```





> ###### Additional Information: 
> PHP Manual: https://www.php.net/manual/en/language.constants.php
> W3Schools: https://www.w3schools.com/php/php_constants.asp
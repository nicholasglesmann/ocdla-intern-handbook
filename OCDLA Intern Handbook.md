# OCDLA Intern Handbook



Intro text here. Something about OCDLA in general.









### Table of Contents

1. [Basic PHP Syntax](#basic-php-syntax)
2. 

























































































##### Basic PHP Syntax

OCDLA uses PHP to power all the back-end functionality of various web applications. PHP is a scripting language that is syntactically similar to JavaScript, with several key differences that are outlined below.



###### PHP Files

PHP files always end with the file extension .php: ```hello.php```




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





###### PHP Variables

All PHP variables (except constants) begin with a ```$```.

```php
<?php
$text = "Hello World";
$number = 42;
?>
```




PHP is a loosely-typed language (like JavaScript), which means that you do not need to declare the "type" of variable when creating it.


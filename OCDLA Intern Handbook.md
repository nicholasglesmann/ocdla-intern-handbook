# OCDLA Intern Handbook











------

**Table of Contents**

[TOC]





------





## About OCDLA

Oregon Criminal Defense Lawyers Association (OCDLA) is a 501(c)(3) non-profit with over 1,300 lawyer and non-lawyer professional members throughout the greater Northwest. OCDLA produces several continuing legal education (CLE) seminars each year and publishes research materials for the legal community in electronic formats under the OCDLA, Library of Defense and Books Online domains. The organization also maintains an active eStore where customers can purchase traditional research materials and online subscriptions. OCDLA is currently expanding members’ access to these diverse publications by modernizing its online research materials and adopting current web standards and widely-used frameworks such as WordPress and MediaWiki.









------





## OCDLA and PHP

OCDLA uses PHP to power all the back-end functionality of various web applications. PHP is a scripting language that is syntactically similar to JavaScript, with several key differences that are outlined below.



#### PHP Files

PHP files always end with the file extension ```.php ```




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

Both keywords are used to output data to the screen and they are basically the same.

Both keywords can be used with or without parentheses:

```php
<?php
	// All these statements output the same result
	echo "Hello World";
	echo("Hello World");
	print "Hello World";
	print("Hello World");
?>
```








> ###### Additional Information: 
> PHP Manual: https://www.php.net/manual/en/function.echo.php
> 						https://www.php.net/manual/en/function.print.php
> W3Schools: https://www.w3schools.com/php/php_echo_print.asp



-----

#### PHP Variables

All PHP variables (except constants) begin with a dollar sign ```$```.  All variables are case sensitive. Variable names must start with a letter or underscore and can be followed by letters, numbers, or underscores.

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
	// additional code in between
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





------

#### PHP Arrays




> ###### Additional Information: 
> PHP Manual: https://www.php.net/manual/en/language.types.array.php
> W3Schools: https://www.w3schools.com/php/php_arrays.asp





------





## OCDLA and Salesforce

OCDLA uses Salesforce to power multiple parts of their websites. Salesforce is a CRM (Customer Relationship Management) service and it includes:

- A database (Salesforce Objects)

- A query language (SOQL)

- A programming language (Apex)

- A front-end framework (Visualforce)

  

#### Preparing Your Computer for Salesforce Development

There are several things that you must do to set your computer up for Salesforce development. They are:

1. Sign up for a Salesforce Devhub (Developer Org)
2. Install Salesforce CLI (sfdx)
3. Connect your DevHub and CLI
4. Install VS Code
5. Install Salesforce Extensions for VS Code





------

##### Sign up for a Salesforce DevHub

Head over to https://developer.salesforce.com/signup and sign up for a Salesforce Developer account. This will give you access to your own "DevHub" (also known as a Developer Org).





------

##### Install Salesforce CLI

Download and install the Salesforce CLI. Use the appropriate link for your machine below:

| **Operating System** | **Link to Installer**          |
| -------------------- | ------------------------------ |
| macOS                | https://sfdc.co/sfdx_cli_osx   |
| Windows 64-bit       | https://sfdc.co/sfdx_cli_win64 |



After installing, open a command window and enter `sfdx`.

You should see something similar to this:

```
Usage: sfdx COMMAND [command-specific-options]
Help topics, type "sfdx help TOPIC" for more details:
sfdx force # tools for the salesforce developer
sfdx plugins # manage plugins
sfdx update # update sfdx-cli
```





------

##### Connect your DevHub and CLI

Next, you'll need to connect your DevHub account and local CLI together. This saves a lot of time in the future, allowing you to manage scratch orgs, log in, and push and pull code/data from scratch orgs all from your local CLI.



To authorize your DevHub, run the following command:

`sfdx force:auth:web:login -d -a DevHub`

This command will only need to be run once. It will set your default account to your DevHub, with an alias of "DevHub". A window will open in your browser which is where you'll enter your credentials. 



You'll be using scratch orgs for just about everything from here on out (we'll discuss scratch orgs in the next section), but in case you ever need to get into your DevHub again, you can use the following command:

`sfdx force:org:open -u DevHub`





------

##### Install VS Code

While you can and will do a lot of Salesforce coding in the Salesforce Developer Console (see the next section for more info), VS Code is still great for any CSS and Javascript coding.



If you already have VS Code installed then skip to the next subtopic. Otherwise, head over to https://code.visualstudio.com/ and get it installed.





------

##### Install Salesforce Extensions for VS Code

The final step to preparing your machine for Salesforce development is to install the Salesforce Extensions Pack for VS Code. Follow this link for more info on installing it: https://marketplace.visualstudio.com/items?itemName=salesforce.salesforcedx-vscode





------

>###### Additional Information: 
> Salesforce Documentation: https://developer.salesforce.com/docs/atlas.en-us.224.0.sfdx_setup.meta/sfdx_setup/sfdx_setup_intro.htm
> Trailhead: https://trailhead.salesforce.com/en/content/learn/modules/sfdx_app_dev/sfdx_app_dev_setup_dx







------

#### Salesforce Development

Salesforce development happens on temporary, customized Salesforce sever spaces called "Scratch Orgs". There are two options for writing Salesforce code:

1. Write code **locally** using VS Code, then push the code to a Scratch Org 
2. Write code **in the cloud** using the Salesforce Developer Console directly inside a Scratch Org 



sfdx Scratch org commands

Tour of Scratch org

sfdx source code commands


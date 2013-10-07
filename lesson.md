# Laravel - Inversion Of Control Container #

## Introduction ##

From the Laravel documentation we read:

	The Laravel inversion of control container is a powerful tool for managing class dependencies. Dependency injection is a method of removing hard-coded class dependencies. Instead, the dependencies are injected at run-time, allowing for greater flexibility as dependency implementations may be swapped easily.

	Understanding the Laravel IoC container is essential to building a powerful, large application, as well as for contributing to the Laravel core itself.

To become an expert at Laravel, an essential knowledge of the IoC Container is required.  But to have an essential knowledge of the IoC Container, I believe you have to first understand why.

## Why Do We Need An Inversion Of Control Container##

### Dependency Injection ###

During the good `ol days of php, we may have written code that looks something like the following:

	<?php

		define('DB_SERVER', 'localhost');
		define('DB_USER', 'mysql_user');
		define('DB_PASSWORD', 'mysql_password');
		define('DB_NAME', 'my_awesome_database');

		$db_conn = mysql_connect(DB_SERVER, DB_USER, DB_PASSWORD) or die('Could Not Connect To Database');

		mysql_select_db(DB_NAME, $db_conn) or die('Database Not Found');

		


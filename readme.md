# MySQL Development

**MySQL** is one of the most widely used open-source relational database management system (RDBMS).

It is easy to install and set up, so you can quickly get to work constructing databases for managing your collections of movies, comics, music, recipes, or just about anything. MySQL is often paired with PHP for web development projects and is, in fact, the backend to many popular CMS (Content Management Systems) like WordPress and Concrete5.

## Environment

###SELECT your MySQL version and the current date

	mysql> SELECT VERSION(), CURRENT_DATE;

#### SHOW the databases in your MySQL server

	mysql> SHOW DATABASES;

#### USE to select a database to work with

	mysql> USE media_database;

#### SHOW the tables in the selected database

	mysql> SHOW TABLES;

#### DESCRIBE the movie table to view columns and datatypes

	mysql> DESCRIBE movie;

#### SELECT a few records from the movie table

	mysql> SELECT title, running_time FROM movie WHERE title LIKE 'a%';

## Basic Queries

#### Create
	INSERT INTO employees (first_name, last_name, department, location) 
	VALUES ('John', 'Smith', 'Developer', 'SF Bay Area');

#### Read
	SELECT first_name, last_name, department, location FROM employees;

#### Update
	UPDATE employees SET email = 'john.smith@acme.com' WHERE id = 10;

#### Delete
	DELETE FROM employees WHERE id = 10;

#### Join
	SELECT m.movie_id, m.title, c.category_name, m.edition, m.release_year, m.running_time
	FROM Movie m
	JOIN Category c ON c.category_id = m.category_id
	ORDER BY m.title ASC;

#### Group By
	SELECT c.category_name, COUNT(c.category_id)
	FROM Movie m
	JOIN Category c ON c.category_id = m.category_id
	GROUP BY c.category_name
	ORDER BY c.category_name ASC;

#### Limit Record Set
	SELECT m.movie_id, m.title, m.edition, m.time_stamp
	FROM Movie m
	ORDER BY m.movie_id DESC LIMIT 10;

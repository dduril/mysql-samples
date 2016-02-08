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

#### Base SELECT Query

	SELECT * FROM Employees;

#### Using Columns

	SELECT FirstName, LastName FROM Employees;

#### Using ORDER BY

	SELECT FirstName, LastName From Employees ORDER BY LastName ASC;
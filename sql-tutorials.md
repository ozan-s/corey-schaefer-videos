# SQL Tutorial for Beginners 1: Installing PostgreSQL and Creating Your First Database
[Video](https://www.youtube.com/watch?v=xaWlS9HtWYw)

## Create database using SQL CLI
    /Applications/Postgres.app/Contents/Versions/latest/bin/psql
    create database sample_db;
    \l # list of databases
    \q # quit cli
    
# SQL Tutorial for Beginners 2: Creating Your First Table
[Video](https://www.youtube.com/watch?v=w4HEVY_GjqY)

## Create new table
    CREATE TABLE people (
      id INTEGER, 
      name VARCHAR (255)
    )
    
## Delete table
    DROP TABLE people,

# SQL Tutorial for Beginners 3: INSERT - Adding Records to Your Database
[Video](https://www.youtube.com/watch?v=fA0jpjwi4J8)

## Insert new values to the database
  INSERT INTO people VALUES (1, 'Corey');
  INSERT INTO people (id, name) VALUES (2, 'Travis');
  INSERT INTO people (name, id) VALUES ('Bronx', 3);
  
 # SQL Tutorial for Beginners 4: SELECT - Retrieving Records from Your Database
 [Video](https://www.youtube.com/watch?v=-FPVPcq28r4)
 
 ## Select all records from a table
    SELECT * FROM people;
    SELECT first_name, last_name FROM people;
    
## Select records that match a criteria
    SELECT * FROM people WHERE last_name = 'Doe';
    SELECT * FROM people WHERE last_name = 'Doe' OR last_name =  'Smith';
    SELECT * FROM people WHERE last_name = 'Doe' AND age < 30;
    
## Order results
    SELECT * FROM people WHERE age < 34 ORDER BY age;
    SELECT * FROM people WHERE age < 34 ORDER BY age DESC;
    SELECT * FROM people WHERE age < 34 ORDER BY first_name, last_name;
    
# SQL Tutorial for Beginners 5: UPDATE and DELETE - Modifying and Removing Records from Your Database
[Video](https://www.youtube.com/watch?v=wva2yMqcB6Q)

## Update all values
    UPDATE test_table SET Location = 'Unknown';

## Delete all values
    DELETE FROM test_table;
    
## Update specific records
    UPDATE people SET occupation = 'Programmer' WHERE first_name = 'Jane' AND last_name = 'Smith';
    
## Delete specific records    
    DELETE FROM people WHERE occupation = 'Scientist' AND age < 58;


# DATABASES 101


### [DQL - Data Query Language](#DQL)

* [SELECT](#SELECT)

### [DDL - Data Definition Language](#DDL)

* [CREATE](#CREATE)
* [ALTER](#ALTER)
* [DROP](#DROP)
* [RENAME](#RENAME)
* [TRUNCATE](#TRUNCATE)

### [DCL - Data Control Language](#DCL)

* [GRANT](#GRANT)
* [REVOKE](#REVOKE)

### [DML - Data Modification Language](#DML)

* [CONCAT](#CONCAT)
* [INSERT](#INSERT)
* [UPDATE](#UPDATE)
* [DELETE](#DELETE)
* [MERGE](#MERGE)
* [CALL](#CALL)
* [EXPLAIN PLAN](#EXPLAIN-PLAN)
* [LOCK TABLE](#LOCK-TABLE)

## [ADD-ONS](#ADD-ONS)

### [AGGREGATE FUNCTIONS](#AGGREGATE-FUNCTIONS)

### [COMMENTING](#COMMENTING)

### [BOOLEAN](#BOOLEAN)

### [OPERATOR PRECEDENCE](#OPERATOR-PRECEDENCE)

<br>

# DQL

### SELECT

- Selects all info from table

  ```SELECT * FROM employees;```
  
<br>

# DDL

  ### CREATE
  ### ALTER
  ### DROP
  ### RENAME
  
  - Renames one column
  
    ```SELECT column AS "new column name" FROM TABLE ```
    
   - Renames multiple column
   
      ```SELECT column1 AS "new column1 name", column2 AS "new column2 name" FROM TABLE```
    
  ### TRUNCATE
  
 <br>
 
 # DCL
 
  ### GRANT
  ### REVOKE
 
 <br>
 
 # DML
 
  ### CONCAT
  
  - Concatenates 2  columns with a space in the middle

    ```SELECT CONCAT(col1,' ',col2) FROM  TABLE```
    
  - Concatenates 2  columns with a space in the middle, renaming the new column

    ```SELECT CONCAT(col1,' ',col2) AS "new name" FROM  TABLE```
  
  ### INSERT
  ### UPDATE
  ### DELETE
  ### MERGE
  ### CALL
  ### EXPLAIN-PLAN
  ### LOCK-TABLE
  
  <br>
  
# DQL

 ### SELECT

- Selects all info from table

  ```SELECT * FROM employees;```
  
<br>

# ADD-ONS

### AGGREGATE-FUNCTIONS

* AVG
* COUNT
* MIN
* MAX
* SUM

### COMMENTING

```-- Single line comment```

``` 
    /*
      Multi line comments
      nice
     */
```

### BOOLEANS

 * AND
 
  ```
  SELECT column FROM table
  WHERE col1 = 'data' AND co2 = 'data'
  ```
 
 * OR
 
  ```
  SELECT column FROM table
  WHERE col1 = 'data' OR co2 = 'data'
  ```
  
  * NOT

   ```
   SELECT firstName, gender FROM users
   WHERE NOT gender = 'm';
   ``` 
  
  * MORE ADVANCED EXAMPLES
  
  - AND & OR
  
    ```
    SELECT first_name, last_name, hire_date FROM employees
    WHERE (first_name = 'Georgi' AND last_name = 'Facello' AND hire_date = '1986-06-26')
    OR (first_name = 'Bezalel' AND last_name = 'Simmel')
    ```
    
### OPERATOR PRECEDENCE
 
 Always remember the following: HIGHEST to LOWEST



1. Parenthesis

2. Arithmetic Operators

3. Concatenation Operators

4. Comparison Conditions

5. IS NULL, LIKE, NOT IN, etc.

6. NOT

7. AND

8. OR

<br>




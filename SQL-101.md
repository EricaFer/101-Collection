
# SQL 101


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
* [COALESCE](#COALESCE)
* [CAST](#CAST)

### [ADD-ONS](#ADD-ONS)

* [AGGREGATE FUNCTIONS](#AGGREGATE-FUNCTIONS)

* [COMMENTING](#COMMENTING)

* [BOOLEAN](#BOOLEAN)

* [OPERATOR PRECEDENCE](#OPERATOR-PRECEDENCE)

* [EMPTY VALUES](#EMPTY-VALUES)

* [PATTERN MATCHING](#PATTERN-MATCHING)

* [DATES AND TIMEZONES](#DATES-AND-TIMEZONES)


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
  
  ### COALESCE
  
  - Substitutes NULL values

    ```SELECT coalesce(col1, 'new_value') FROM table```
    
  ### CAST
  
  - To use Pattern Matching in PostGres characthers need to be cast as TEXT

    ```CAST col AS text LIKE```
    
    ```col::text LIKE```
  
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
   
  * BETWEEN AND

    ```
    SELECT firstName, gender FROM users
    WHERE age BETWEEN 30 AND 50;
    ``` 
    
  * IN

    ```
    SELECT * FROM table
    WHERE col IN (val1, val2);
    ``` 
  
  * MORE ADVANCED EXAMPLES
  
    - AND
  
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

### EMPTY VALUES

  * FILTER 

    - NULL
  
      ```
      SELECT * FROM table
      WHERE field IS [NOT] NULL
      ```
      
    - EMPTY

      ```
      SELECT * FROM table
      WHERE field = '' IS [NOT] TRUE
      ```    

### PATTERN MATCHING

  * PARTIAL MATCHING

    - LIKE (case-sensitive)
    - ILIKE (NOT case-sensitive)

  * '%2' - Ends with 2
  * '%2%' - 2 anywhere in the middle
  * '_00%' - 00 after the first characther
  * '2_%_%' - Starts with 2 and has at least 3 digits
  * '2___3' - five-digit number that starts with 2 and end with 3

### DATES AND TIMEZONES

   ````SHOW TIMEZONE```
   
   - Only changes the session
   ```SET TIME ZONE 'UTC'```
   
   - Permanently changes the TIME ZONE

    ```ALTER USER postgres SET timezone='UTC'```


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

## ADD-ONS

### AGGREGATE FUNCTIONS

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
  


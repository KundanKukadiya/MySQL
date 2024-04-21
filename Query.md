# Some Query commands

### SELECT :
- SELECT column1, column2, ... FROM table_name 

### WHERE with AND , OR and NOT :
- SELECT column1, column2, ...
    FROM table_name
    WHERE condition1 AND condition2 AND condition3 ...;  
  **Example** : The following SQL statement selects all fields from "Customers" where country is "Germany" AND city is "Berlin":
  - SELECT * FROM Customers WHERE Country = 'Germany' AND City = 'Berlin';
- SELECT column1, column2, ...
    FROM table_name
    WHERE condition1 OR condition2 OR condition3 ...;  
  **Example** : The following SQL statement selects all fields from "Customers" where city is "Berlin" OR "Stuttgart":
  - SELECT * FROM Customers WHERE City = 'Berlin' OR City = 'Stuttgart';
- SELECT column1, column2, ...
    FROM table_name
    WHERE NOT condition;  
  **Example** : The following SQL statement selects all fields from "Customers" where country is NOT "Germany":
  - SELECT * FROM Customers WHERE NOT Country = 'Germany';
### ORDER BY :
- The ORDER BY keyword is used to sort the result-set in ascending or descending order.  
- **Example** : SELECT column1, column2, ...
                FROM table_name
                ORDER BY column1, column2, ... ASC|DESC;
### INSERT INTO :
- The INSERT INTO statement is used to insert new records in a table.
1. Specify both the column names and the values to be inserted:
   - INSERT INTO table_name (column1, column2, column3, ...) VALUES (value1, value2, value3, ...);  
2. If you are adding values for all the columns of the table, you do not need to specify the column names in the SQL query. However, make sure the order of the values is in the same order as the columns in the table. Here, the INSERT INTO syntax would be as follows:
   - INSERT INTO table_name VALUES (value1, value2, value3, ...);
### UPDATE :
- The UPDATE statement is used to modify the existing records in a table.
  - UPDATE table_name
    SET column1 = value1, column2 = value2, ...
    WHERE condition;
- **Be careful when updating records. If you omit the WHERE clause, ALL records will be updated!**
### DELETE :
- The DELETE statement is used to delete existing records in a table.
  - DELETE FROM table_name WHERE condition;
- **Note: Be careful when deleting records in a table! Notice the WHERE clause in the DELETE statement. The WHERE clause specifies which record(s) should be deleted. If you omit the WHERE clause, all records in the table will be deleted!**
- DELETE all records :
  - DELETE FROM table_name;
### LIMIT :  
- The LIMIT clause is used to specify the number of records to return.  
- The LIMIT clause is useful on large tables with thousands of records. Returning a large number of records can impact performance.
  - SELECT column_name(s)
    FROM table_name
    WHERE condition
    LIMIT number;

**eval** command is used to execute the given query with related database and print the result 
on the console.

**Example :point_down:**

```
sqoop eval --connect jdbc:mysql://localhost/bigdata --username root 
--password mysql --query “SELECT * FROM student1 LIMIT 3”
```

The above given command instruction will print top 3 rows of **student1** table on the console screen.
we can change query string according to our requirement.

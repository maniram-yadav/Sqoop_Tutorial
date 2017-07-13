**import-all-tables** is used for importing all the table data from a database to the HDFS directory.


**Query_Format**

```

sqoop import-all-tables --connect <your database url> --username <Your database user name> --password
<Your database password> 
```

**Example :point_down:**


```
sqoop import-all-tables  --connect jdbc:mysql://localhost:3306/bigdata --username root
--password mysql 
```

The above given query  will import all the data from all the tables of **bigdata** database of MySQL. 

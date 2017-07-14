**list-tables** prints all the tables name on the console screen of the related database
name given in the database url in the sqoop command.

**Exampl :point_down:**

```
$ sqoop list-tables --connect jdbc:mysql://localhost/userdb  --username root --password mysql
```

The above given query will print all the database table name of userdb schema of the MySQL database
on the console screen.

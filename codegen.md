## Sqoop codegen command

Sqoop **codegen** command is used for creating java getter and setter class of the database table. **codegen** 
command creates three file i.e .java, .class and .jar file of the database table.

:Query Format:

```
 sqoop codegen --connect <Database url> --username <database user name> 
 --password <database password> --table <table name>
```

**Example :point_down:**

```
 sqoop codegen --connect jdbc:mysql://localhost/bigdata --username root --password mysql --table student1
```

The above sqoop command will generate following three file 

```
student1.java
student1.class
student1.jar

```

These file can be used as getter and setter in the bigdata project

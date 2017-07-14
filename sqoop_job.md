### Sqoop Job command
 
Sqoop **job** creates and saves the import and export commands. Thses saved commands can be used in future when 
working on sqoop tools

**Query Format**

```
sqoop job --create myjob  --connect < Your Database Url> --username < User name >
--password <your daatbase password>  --table < Database table name > 
--target-dir <path to HDFS file>
```

___
___

**Example :point_down:**

```
sqoop job --create gettable import --connect jdbc:mysql://localhost/bigdata --username root 
--password mysql --table student1 --target-dir /students
```

The above given example will create job and it will saved with name **gettable**. 
Which can be used for future.

Some of the useful sqoop command and their uses are as follows ..


**--create**  : used for creating Sqoop Jobs with specified name.
**--delete**  :  Deletes a saved job with specified name.
**--exec**  :  Executes the saved job.
**--show**  :  Show the save job configuration
**--list**  :  Lists all the saved jobs.

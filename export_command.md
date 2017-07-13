Using export command we export the data from HDFS directory to the Database tables.

But first make sure that table in the database has already been created where the HDFS file data will be stored.
And also the table column should have to follow the data definition rule according to the data stored in HDFS file.

After doing all thing apply below given query format for exporting data from HDFS to the Database 
table.

```
sqoop export --connect < Your Database Url> --username < User name >
--password <your daatbase password>  --table < Database table name > 
--export-dir <path to HDFS file>
```
 ___
 
**Example :point_down:**

```
sqoop export  --connect jdbc:mysql://localhost:3306/bigdata --username root --password mysql --table 
student1  --export-dir /student/part-m-00000
```

___

Following value has been used in above example :

**jdbc:mysql://localhost:3306/bigdata** : MySQL database schema url 

**root** : MySQL database username

**mysql** : MySQL database password

**student1** : MySQL database table

**/student/part-m-00000** : Path to the HDFS file which contain the data and should be imported to the 
MySQL Database table *sqtudent1*


___ 

**part-m-00000** file of the HDFS contain the following contaent

```
1,maniram yadav,maniram@gmail.com,21
2,ramesh,ramesh@gmail.com,24
3,amit,amit@gmail.com,20
4,sanjay,sanjay@gmail.com,22
```

In above given data there is 4 rows and each row containg four comma seperated value which will be 
mapped to corressponding four columns of the database table **student1**.


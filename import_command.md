**Move data from RDBMS table to HDFS**

In this tutorial I am going to show you how to move data from RDBMS database like MySql , Oracle etc. 
to HDFS (Hadoop Distributed File System) using sqoop.


---

I have stored following content in the **student** table and MySQL database name is **bigdata**.


Id | Name| Email | Age
--- | --- | --- | ---
1 | maniram | maniram@gmail.com | 21
2 | ramesh | ramesh@gmail.com | 24
3 | amit | amit@gmail.com | 20
4 | sanjay | sanjay@gmail.com | 22

 ---
 
 
The simple syntax for moving  above given data from RDBMS table to HDFS is below :point_down:

```
sqoop import --connect <your database url> --username <Your database user name> --password
<Your database password> --table <Database table name> 
--target-dir /< Directory name In Hdfs>
```

In above given command you have to use info related to your database where your data is saved and you have
to give the directory name where your data will be saved in HDFS in file format.

**Example** :point_down:

![sqoop import](https://github.com/maniram-yadav/Sqoop/blob/master/images/sqoopimport.png)

The above given command run successfully and data from RDBMS has been moved to the **students** directory to the 
HDFS. So let us analyse that student directory has been created or not in the HDFS.


---

You have to use below given command to list the directory in the HDFS.

```
hadoop dfs -ls /
```
**Example**

![HDFS list](https://github.com/maniram-yadav/Sqoop/blob/master/images/dfslist.png)

**students** directory has been created and RDBMS table data has been saved in file **part-m-00000** 
file inside students directory. You can find out the content of this file
by using the command

```
hadoop dfs -cat <file path stored in hdfs>
```

**Example**

![hadoop dfs cat](https://github.com/maniram-yadav/Sqoop/blob/master/images/studentscat.png)

Content of the file has been printed on the terminal.

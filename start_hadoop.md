Before using sqoop command instruction make sure hadoop cluster is running on your system. 
You have to start mapreduce history server also.

Use the below given command instruction for starting hadoop cluster and mapreduce history server.

#### start-all.sh
  This command is used for starting hadoop cluster in your system. we can do same thing also by using  command **start-dfs.sh**
  for starting HDFS server and  command **start-yarn.sh** for mapreduce jobs.
  
  So type below :point_down: given command on terminal for starting hadoop cluster.
  
  ```
  start-all.sh
  ```
  
  ![start-all.sh](https://github.com/maniram-yadav/Sqoop/blob/master/images/start-all.png)
  
we can find out status of all the hadoop jobs by using **jps**  command. As you can see in above given image.


  >___

After starting hadoop cluster you have to start mapreduce history server by using below :point_down: given command.

  ```
  mr-jobhistory-daemon.sh
  ```

![mr history](https://github.com/maniram-yadav/Sqoop/blob/master/images/mrhistory.png)


>____

Now your system is ready to use sqoop tools on your system.

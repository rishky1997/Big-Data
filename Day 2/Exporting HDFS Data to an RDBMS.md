
## 1 ) Put the Data into HDFS 
 
a. Create a new directory in HDFS named salarydata. 

#hdfs dfs -mkdir salarydata 

![image](https://user-images.githubusercontent.com/64614587/86316382-45a0f680-bc4a-11ea-968a-8dc5b24a45fd.png)

b. Put salarydata.txt into the salarydata directory in HDFS.   

#hdfs dfs –put salarydata.txt salarydata

![image](https://user-images.githubusercontent.com/64614587/86316418-5d787a80-bc4a-11ea-8bf7-930bdd412fd0.png)

![image](https://user-images.githubusercontent.com/64614587/86316764-42f2d100-bc4b-11ea-8dcf-15659b086fb8.png)

## 2 ) Export the Data 

#sqoop export --connect jdbc:mysql://hadoopdb.comds7xp22md.us-east-1.rds.amazonaws.com/sqoop --username root --password rootroot --table salaries2 --export-dir salarydata --input-fields-terminated-by ","

![image](https://user-images.githubusercontent.com/64614587/86317368-df69a300-bc4c-11ea-991f-51d5e5d4550c.png)

## 3 ) Verify it worked by viewing the table’s contents from the mysql workbench. 

The output should look like the following: 

![image](https://user-images.githubusercontent.com/64614587/86317408-f7d9bd80-bc4c-11ea-9467-d22967d3e3a5.png)

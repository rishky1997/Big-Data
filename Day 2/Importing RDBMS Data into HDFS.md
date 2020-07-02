
  
## 1 ) Import the Table into HDFS 

sqoop import --connect jdbc:mysql://hadoopdb.comds7xp22md.us-east-1.rds.amazonaws.com/sqoop --username root --password rootroot --table salaries -m 1sqoop import --connect jdbc:mysql://hadoopdb.comds7xp22md.us-east-1.rds.amazonaws.com/sqoop --username root --password rootroot --table salaries -m 1

![image](https://user-images.githubusercontent.com/64614587/86310728-5c405100-bc3c-11ea-88f3-d50050c82ce1.png)
![image](https://user-images.githubusercontent.com/64614587/86310771-74b06b80-bc3c-11ea-8f86-8d5289f570ee.png)


## 2 ) Verify the Import 

![image](https://user-images.githubusercontent.com/64614587/86310929-cc4ed700-bc3c-11ea-97cb-13a2dc2b0bc1.png)
![image](https://user-images.githubusercontent.com/64614587/86310966-ed172c80-bc3c-11ea-8116-8164fccd9019.png)
![image](https://user-images.githubusercontent.com/64614587/86311140-50a15a00-bc3d-11ea-805b-95364f855bb6.png)

## 3 ) Specify Columns to Import 
sqoop import --connect jdbc:mysql://hadoopdb.comds7xp22md.us-east-1.rds.amazonaws.com/sqoop --username root --password rootroot --table salaries  --columns salary,age -m 1 --target-dir salaries2

![image](https://user-images.githubusercontent.com/64614587/86312122-9d863000-bc3f-11ea-80e8-f320a3c48aa6.png)
![image](https://user-images.githubusercontent.com/64614587/86312142-af67d300-bc3f-11ea-8078-e101e32d9095.png)

## 4 ) Importing from a Query
a. Use gender as the --split-by value, specify only two mappers, and import the data into the salaries3 folder in HDFS. 
![image](https://user-images.githubusercontent.com/64614587/86314885-68311080-bc46-11ea-974b-4ba7d66502fa.png)

b. To verify the result, view the contents of the files in salaries3. You should have only two output files. 
![image](https://user-images.githubusercontent.com/64614587/86314993-a7f7f800-bc46-11ea-95da-4f399f6720bd.png)

c. View the contents of part‐m‐00000 and part‐m‐00001.  

![image](https://user-images.githubusercontent.com/64614587/86315032-be05b880-bc46-11ea-8568-b55b85354357.png)


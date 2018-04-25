# Recommender-Systems
Instructions to Create Jar File for Word Count Using Spark Mllib and running it on DSBA
hadoop cluster

Part-1
1. Open Eclipse which came with Scala-IDE
2. Click File-> New-> Other -> Maven Project and select Next
3. Select 'Create simple project checkbox' and click Next
4. Give any 'Group Id' similar 'org.SparkWC'
5. Give any 'Artifact Id' similar to 'SparkScalaWC' and click Finish
6. Right click on newly created project and go to Configure and
select 'Add Scala nature'
7. Open the new project and open the pom.xml and go to pom.xml tab
8. Copy the Maven dependency into pom.xml and paste it under <version>....</version> line
   
Note: If an error occurs for incompatibility, then right click on project -> Scala -> Set the Scala Installation and choose the appropriate installation.

9. Inside the project, right click on src/main/java, select Refactor and
select Rename. Rename 'java' as 'scala'

10. Right click on src/main/scala and select New -> Package. Name the package
 as 'org.SparkWC'
 
11. Right click on the package(org.SparkWC) and select New -> Scala Object.
Name it as 'org.SparkWC.Driver'


Part -2

1. Delete all contents inside Driver.scala and copy the code
into the Maven Project - Driver.scala

The link for the hadoop common bin is :https://github.com/srccodes/hadoop-common-2.2.0-bin
Download, unzip and give the location of folder which contains the bin to line 7

Save the project.

2. Right click on the project. Select 'RunAs' and click 'Maven Clean'. This step removes
old .jar files in the 'target' folder

3. Right click on the project. Select 'RunAs' and click 'Maven Install'. Check the
'target' folder for a .jar file. Rename the .jar file as 'SparkScalaWC.jar'

4. The data can be obatined from the following links:
4.1 data from http://webpages.uncc.edu/aatzache/ITCS6190/Exercises/ActionRulesList.txt 
4.2 data.txt from http://webpages.uncc.edu/aatzache/ITCS6162/Project/Data/MammographicMassData/MammData.zip 	

5.Copy data.txt to HDFS using the command:
    hadoop fs -put /users/UserName/data.txt /user/UserName/
    
6. Run the program using the command:
    spark2-submit --class org.SparkWC.Driver  --master yarn --deploy-mode client
    location-to-jar-file location-to-data-input location-to-output-directory

7. Copy the output to your server using the command:
hadoop fs -get /user/UserName/SparkWCout_1/part-00000
    /users/UserName/SparkWCOutput_1.txt


Instructions to create jar file for Spark Mllib Decision Tree Classifier and Running it on the DSBA Hadoop Cluster

Part-1
1. Open Eclipse which came with Scala-IDE
2. Click File-> New-> Other -> Maven Project and select Next
3. Select 'Create simple project checkbox' and click Next
4. Give any 'Group Id' similar 'org.SparkML'
5. Give any 'Artifact Id' similar to 'SparkDecisionTrees' and click Finish
6. Right click on newly created project and go to Configure and
select 'Add Scala nature'
7. Open the new project and open the pom.xml and go to pom.xml tab
8. Copy the Maven dependency into pom.xml
 
   and paste it under <version>....</version> line
   
Note: If an error occurs for incompatibility, then right click on project -> Scala -> Set the Scala Installation and choose the appropriate installation.

9. Inside the project, right click on src/main/java, select Refactor and
select Rename. Rename 'java' as 'scala'

10. Right click on src/main/scala and select New -> Package. Name the package
 as 'org.SparkML'
 
11. Right click on the package(org.SparkWC) and select New -> Scala Object.
Name it as 'org.SparkML.DecisionTreeDriver"'



Part -2

1. Delete all contents inside Driver.scala and copy the code
into the Maven Project - Driver.scala

The link for the hadoop common bin is :https://github.com/srccodes/hadoop-common-2.2.0-bin
Download, unzip and give the location of folder which contains the bin to line 16

Save the project.

2. Right click on the project. Select 'RunAs' and click 'Maven Clean'. This step removes
old .jar files in the 'target' folder

3. Right click on the project. Select 'RunAs' and click 'Maven Install'. Check the
'target' folder for a .jar file. Rename the .jar file as 'SparkScalaWC.jar'

4. The data can be obtained from the following links:
Data.txt from 
http://webpages.uncc.edu/aatzache/ITCS6162/Project/Data/CarEvaluationData/CarData.zip 

5.Copy data.txt to HDFS using the command:
    hadoop fs -put /users/UserName/data.txt /user/UserName/
    
6. Run the program using the command:
    spark2-submit --class org.SparkML.DecisionTreeDriver  --master yarn --deploy-mode client
    location-to-jar-file location-to-data-input location-to-output-directory

7. Copy the output to your server using the command:
hadoop fs -get /user/UNCCUserName/SparkWCout_1/part-00000
    /users/UserName/SparkDTOutput_1.txt



# Docker-on-Hadoop
 This repo will help you how to install hadoop on docker container

# Pre-requisite:
                                                                          
-> Git                                                                                  
-> Docker

# Steps to follow:
By Following these steps you will able to setup the hadoop setup on docker container                                    
                                                                                                                      
Step 1: Clone the "docker-hadoop" repository from GitHub using the following command:                                   
git clone https://github.com/huzaifa-bilal-01/Hadoop-on-Docker.git

Step 2: 
docker-compose up -d

Step 3: 
docker container ls

Step 4:
docker exec -it namenode /bin/bash

# Running Hadoop Code:

Step 1: Copy the code folder on docker conatiner by running this command:        
docker cp code namenode:/                                                              
                                                                                                                        
Step 2: Then go into Hadoop_Code directory and further into input directory from where you have to copy the data.txt file
                                                                                                                             
Step 3: Create some directories in hadoop file system by following command:                                                 
      -> hdfs dfs -mkdir /user                                                                       
      -> hdfs dfs -mkdir /user/root                                                                                                 
      -> hdfs dfs -mkdir /user/root/input                                                                                        
                                                                                                                                                      
Step 4: Copy the data.txt to the input directory (user/root/input) created in hadoop file system by following command:
      -> hdfs dfs -put data.txt /user/root/input                                                                            
                                                                                                                                          
Step 5: Return back to directory where wordCount.jar file is located:                                                    
      -> cd ../
                                                                                                                                                  
Step 6: Then execute the jar file by following command:                                                                        
      -> hadoop jar wordCount.jar org.apache.hadoop.examples.WordCount input output                                               
                                                                                                                                                                   
Step 7: Display the output usind this command:                                                                              
      -> hdfs dfs -cat /user/root/output/*
      

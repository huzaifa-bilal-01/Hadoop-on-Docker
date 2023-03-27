# Docker-on-Hadoop
 This repo will help you how to install hadoop on docker container
# Steps to follow:
Step 1: Clone the "docker-hadoop" repository from GitHub using the following command:
git clone https://github.com/big-data-europe/docker-hadoop

Step 2: Use the docker-compose command to start the Hadoop cluster in detached mode. This can be done using the following command:
docker-compose up -d

Step 3: Verify that the Hadoop containers are running using the following command:
docker container ls

Step 4: Access the namenode container's command prompt using the following command:
docker exec -it namenode /bin/bash

# Title
This project is intended to set up Artifactory server

# Create Artifactory server in AWS
https://github.com/devops2023q2/terraform

# Automation 
* Step 1: Run playbook
https://github.com/devops2023q2/ansible


```




# Manual: Install and configure required software packages for Artifactroy
Install and configure required software packages for Artifactory
Step 1: step1: Login to EC2 Intance i.e “artifactory”

$ sudo yum install -y net-tools rsync wget

 step 2 : install artifactory 

$ sudo yum install -y java-1.8.0-openjdk-devel 

$ sudo su 

$ echo "export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.191.b12-1.el7_6.x86_64" >> /etc/profile 

$ source /etc/profile 

$ env | grep JAVA 

$ sudo wget https://releases.jfrog.io/artifactory/artifactory-rpms/artifactory-rpms.repo -O jfrog-artifactory-rpms.repo 

$ sudo mv jfrog-artifactory-rpms.repo /etc/yum.repos.d/ 

$ sudo yum update -y && sudo yum install jfrog-artifactory-oss -y 

$ sudo echo "export ARTIFACTORY_HOME=/opt/jfrog/artifactory" >> /etc/profile 

$ source /etc/profile 

$ env | grep ARTIFACTORY_HOME

 $ sudo systemctl start artifactory.service 

$ systemctl enable artifactory.service

step 5: testing

http://<<PUBLIC_IP>>:8081/artifactory

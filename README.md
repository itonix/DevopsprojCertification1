Website is a simple php- html script for a simple webpage!

This project uses the webcontent in php  and will be launched using apache2 with php packages installed and it will be containerised using docker as a docker image and will be pushed to docker hub.
Tools Used:

jenkins :automation
docker: containerization
dockerhub: for publishing image 
AWS : for deployment(ec2-instance)
************************************
scripting tools:
terraform for provisioning
Ansible: for configuring (optionl)
Jenkinsfile 
Dockerfile for building docker images



**********************************************

THE CICD pipe line start with github.The content will be triggered based on poll SCM and the jenkins file performs the build steps and it also uses docker to containerise the image along with apache2
Once the image is pushed to docker hub,jenkins will trigger the deployment pipeline and pulls the image from docker hub and runs it as a container in AWS EC2 instance.
The php content is set to be available at ec2 publicip:44500/


********************************************************************************************************************************************************
Terraform file parametrized so that you can select the required action 1)apply 2) destroy

developer <====>github<=====>jenkins======>dockerhub
jenkins======terraform========dockerhub======>ec2-instance:ip:44500/
******************************************************************************************

![project](https://user-images.githubusercontent.com/59088641/225546999-3501b1cf-0826-45fb-9597-d4aff7b6d396.png)






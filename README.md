Website is a php- html script for a simple webpage!

This project uses the webcontent in php  and will be launched using apache2 with php packages installed and it will be containerised using docker as a docker image and will be pushed to docker hub.
THE CICD pipe line start with github.The content will be triggered based on poll SCM and the jenkins file performs the build steps and it also uses docker to containerise the image along with apache2
Once the image is pushed to docker hub,jenkins will trigger the deployment pipeline and pulls the image from docker hub and runs it as a container in AWS EC2 instance.
The php content is set to be available at ec2 publicip:44500/



developer <====>github<=====>jenkins======>dockerhub
jenkins======terraform========dockerhub======>ec2-instance:ip:44500/

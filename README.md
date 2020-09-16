# Udacity Devops Capstone Project

## Final project to graduate from the cloud devops engineer nanodegree

### Project App Properties

  Deployment Type - Rolling Deployment
  
  Application - Nginx with customized index.html file

## TECHNOLOGIES USED

- JENKINS
- ANSIBLE
- KOPS (Kubernetes Operations)
- DOCKER
  
### Learning
 
I ran into a little too many errors during this project, not the most fun but I definitely learnt a lot! I tried making a project with Blue/Green deployment before this one [Repo](https://github.com/adinalini/DevopsCapstoneProject), but couldn't resolve the errors there, so finally tried out the rolling deployment and it worked! Can't wait to try out my skills in a real world project.

## Tech Stack explanation

### Jenkins Stages
   
   Build - Build docker image and update the latest version of docker image on docker hub
   
   Lint - Linting the Dockerfile using hadolint
          Linting the HTML file using tidy
          
   run production - Creates service for exposing the nginx applicaiton
   
   run development - Pulls the latest image of Capstone Project from Docker hub
                     Creates a new deployment using the updated docker image
                     
 ### Ansible 
 
 Ansible is used to control different instances and update them using rolling deployment.
 
 New user 'ansadmin' is added on instance and ssh is configured for machines.
 
 
 ### Kops (Kubernetes Operations)
 
 Kubernetes Operations is used to create cluster containing two nodes and one master node.
 
 Cluster named capstone.in is created which is connected to s3 storage s3://capstone.project.
 
 
 ## Sample working image       
 
 ![Application-functioning](https://github.com/adinalini/DevopsCapstoneProject-2/blob/master/Final%20working%20html.PNG)

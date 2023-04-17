# 5-DevOps-Docker  

## pre-requiesties
Install Docker in local or EC2

## Steps
Run below commands to contanarize this application in this repo and run the image.

(1) Navigate to the directory where you have the application and Dockerfile  
(2) Run below command to build container image for the application  
      docker build -t flask_image .  
(3) Run below command to run the container  
      docker run -p 5000:5000 flask_image  
(4) Check the port 5000 of local host or EC2 Public IP to validate the flask application  
(5) Push image into DockerHub  
      docker tag myimage myusername/myrepository:mytag  
      docker push myusername/myrepository:mytag

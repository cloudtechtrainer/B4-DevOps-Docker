# 5-DevOps-Docker  
## Install Docker and Run below commands to contanarize the application in this repo and run the image.

docker build -t sumapp .  

docker run -it myimage python app.py


docker run -p 5000:5000 my-flask-app

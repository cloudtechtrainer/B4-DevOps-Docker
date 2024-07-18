------------
Install GIT
------------

sudo apt update
sudo apt install git
git -version
sudo apt update

---------------
Install Docker
---------------

# Add Docker's official GPG key:
sudo apt-get update\
sudo apt-get install ca-certificates curl\
sudo install -m 0755 -d /etc/apt/keyrings\
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc\
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null\
sudo apt-get update


sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

-----------------
Work with Docker
-----------------

Verify that Docker is installed and running:
sudo docker --version

Use the git clone command to clone the repository:
git clone https://github.com/cloudtechtrainer/B4-DevOps-Docker

Build the Docker Image:\
docker build -t my-app:1.0 .

This command tells Docker to build an image using the current directory (.) as the build context.<br/>
Run the Docker Container:<br/>
I
docker run -p 5000:5000 my-app:1.0

Login to Docker Hub:<br/>
docker login --username=<your-dockerhub-username>

Tag your Docker Image:<br/>
docker tag my-app:1.0 <your-dockerhub-username>/<repository-name>:<tag>

This renames your image to the format Docker Hub expects.


Push the Docker Image:<br/>
docker push <your-dockerhub-username>/<repository-name>:<tag>

Use the docker pull command to fetch the Docker image from Docker Hub:<br/>
docker pull <your-dockerhub-username>/<repository-name>:<tag>

Use the docker pull command to fetch the Docker image from Docker Hub:<br/>
docker pull <your-dockerhub-username>/<repository-name>:<tag>

Run the Docker Container:<br/>
docker run -d -p 5000:5000 <your-dockerhub-username>/<repository-name>:<tag>


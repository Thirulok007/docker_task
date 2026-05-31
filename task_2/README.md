# Docker Task – Display Basic Details Using Docker & Docker Compose

## Objective

To create a Dockerized web application that displays personal details on a webpage using Nginx, Dockerfile, and Docker Compose.

## Technologies Used

* AWS EC2 / Ubuntu
* Docker
* Docker Compose
* Nginx
* HTML
* CSS

## Project Structure

docker-task-2/

├── index.html

├── Dockerfile

└── docker-compose.yml

## Commands Executed

### Update Packages

sudo apt update -y

### Install Docker

sudo apt install docker.io -y

### Start Docker Service

sudo systemctl start docker

### Enable Docker Service

sudo systemctl enable docker

### Install Docker Compose

sudo apt install docker-compose -y

### Create Project Folder

mkdir docker-task-2

cd docker-task-2

### Build and Run Container

sudo docker-compose up -d --build

### Verify Running Container

sudo docker ps

## Files Used

### index.html

Contains personal information displayed on the webpage.

### Dockerfile

Creates a custom Nginx image and copies the HTML file into the web server directory.

### docker-compose.yml

Builds and runs the Docker container while exposing port 8080.

## Output

The webpage displays:

THIRULOK T

WEB DEVELOPER

Skills:

* HTML
* CSS
* JavaScript
* Spring Boot

Access URL:

http://localhost:8080

## Conclusion

Successfully created and deployed a Dockerized web application using Dockerfile and Docker Compose. The webpage was hosted using an Nginx container and displayed personal details through a modern web interface.
<img width="1919" height="1079" alt="Screenshot 2026-05-31 163836" src="https://github.com/user-attachments/assets/ad478d38-3d78-4311-94a2-6d15e75a5151" />
<img width="1919" height="410" alt="Screenshot 2026-05-31 163849" src="https://github.com/user-attachments/assets/3ad68b00-af7b-41dd-b543-5c8b8e4054be" />
<img width="1915" height="1022" alt="Screenshot 2026-05-31 163336" src="https://github.com/user-attachments/assets/e4f49e4b-7cac-4977-a160-4c87fd2c32ed" />

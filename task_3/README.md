# Docker Task 3 – Custom Nginx Image

## Tech Stack

* WSL
* Docker
* Docker Compose

## Steps Performed

* Created a custom Nginx image using Dockerfile.
* Added a custom HTML page.
* Deployed the container using Docker Compose.
* Configured bind mount volume at /var/opt/nginx.
* Exposed the application on port 8080.
* Pushed the custom image to Docker Hub.

## Volume Mapping

Host Path:
./nginx-data

Container Path:
/var/opt/nginx

## Docker Hub Repository

https://hub.docker.com/r/thirulokthiru/custom-nginx

Docker Task on AWS EC2
Objective
Install Docker on AWS EC2 and explore Docker Images, Containers, Volumes, and Networks.
Technologies Used
•	AWS EC2
•	Docker
________________________________________
Step 1: Launch EC2 Instance
Description
Created an AWS EC2 instance and connected to it securely using SSH.
Go to AWS Console → EC2 → Launch Instance
Choose:
AMI: Amazon Linux 2 (recommended)
Instance type: t3.micro (Free Tier)
Configure:
Create / select key pair
Security Group → Allow SSH (22)
Launch the instance
Command
ssh -i ec2-lab-key.pem ec2-user@<PUBLIC-IP>
 <img width="940" height="504" alt="image" src="https://github.com/user-attachments/assets/42484180-db21-4f7c-b8b5-c701794fa2ab" />

________________________________________
Step 2: Install Docker
Description
Installed Docker and enabled the Docker service.
Commands
sudo yum update -y
sudo yum install docker -y
sudo systemctl start docker
sudo systemctl enable docker
docker --version
<img width="940" height="480" alt="image" src="https://github.com/user-attachments/assets/aae73693-1023-4e5f-b783-19ebaf548f2e" />
<img width="940" height="428" alt="image" src="https://github.com/user-attachments/assets/d42b5dcb-50d7-494b-bce4-0c458d0c485d" />

  ________________________________________
Step 3: Docker Images
Description
Explored Docker images by listing, pulling, and removing images.
Commands
sudo docker images
sudo docker pull nginx
sudo docker rmi nginx
<img width="940" height="344" alt="image" src="https://github.com/user-attachments/assets/7d55cda4-e9a3-40b7-bf20-e7f659799249" />

 ________________________________________
Step 4: Docker Containers
Description
Created and managed Docker containers.
Commands
sudo docker run -d -p 80:80 --name web-nginx nginx
sudo docker ps
sudo docker ps -a
sudo docker stop web-nginx
sudo docker rm web-nginx
 <img width="940" height="480" alt="image" src="https://github.com/user-attachments/assets/8b0f8261-80d5-4ca6-a288-36c040fbdd9a" />
<img width="940" height="504" alt="image" src="https://github.com/user-attachments/assets/128121f2-f9b3-47ba-9922-b8acce571882" />

 Output
Container created, viewed, stopped, and removed successfully.
________________________________________
Step 5: Docker Volumes
Description
Created and inspected Docker volumes for persistent storage.
Commands
sudo docker volume create my-nginx-volume
sudo docker volume ls
sudo docker volume inspect my-nginx-volume
<img width="940" height="481" alt="image" src="https://github.com/user-attachments/assets/64d2cfd6-1a6d-4eb0-adfa-5112c3c7fabc" />

 Output
Volume created and inspected successfully.
________________________________________
Step 6: Docker Networks
Description
Created a custom Docker network and connected containers.
Commands
sudo docker network ls
sudo docker network create my-nginx-network
sudo docker run -d --name app1 --network my-nginx-network nginx
sudo docker run -d --name app2 --network my-nginx-network nginx
sudo docker network inspect my-nginx-network
<img width="940" height="476" alt="image" src="https://github.com/user-attachments/assets/1b3036cb-7409-4887-9c2e-e75225880abe" />
<img width="940" height="479" alt="image" src="https://github.com/user-attachments/assets/56dc25ad-ff80-40d8-ac36-6e2d2565e337" />

  Output
Custom network created and containers connected successfully.
________________________________________
Step 7: Docker Information
Description
Checked Docker system information and logs.
Commands
sudo docker info
sudo docker logs app1
sudo docker system df
   Output
Docker information and container logs displayed successfully.
<img width="940" height="481" alt="image" src="https://github.com/user-attachments/assets/a561ceb5-e6d7-4d0f-bfe5-1dc8947dfc12" />
<img width="940" height="484" alt="image" src="https://github.com/user-attachments/assets/c83d4284-2ce4-40f5-a68b-652cc6ccd092" />
<img width="940" height="200" alt="image" src="https://github.com/user-attachments/assets/c7b9792d-760a-4823-b89d-24c51fce82cc" />

________________________________________
Conclusion
Successfully installed Docker on AWS EC2 and explored Docker Images, Containers, Volumes, and Networks. This task provided hands-on experience with basic Docker operations and cloud-based container management.


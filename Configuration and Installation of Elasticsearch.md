# Configuration and Installation of Elasticsearch

## ELK Essentials: Exploring Elasticsearch Architechture and Components Crash Course

What is a SIEM?  
SIEM, or Security Information and Event Management, is a cybersecurity solution that collects, analyzes, and correlates log and event data from various sources across an IT environment to enhance threat detection, incident investigation, and compliance reporting.
ELK is a SIEM also known as Elastic Stack.

![image](https://github.com/user-attachments/assets/6a465023-0ac7-4f91-b750-6ce0c884eece)

![image](https://github.com/user-attachments/assets/26b83554-142e-453f-8c6c-3864fe439ee1)

## Setting up ELK on DOCKER
### Why use Docker and containers instead of a Virtual Machine to run our SOC?
We are going to use Docker to run our ELK enviroment instead of a VM and the reason why is due to resource utilization, scalability and less overhead. Container-based virtiualization meakes it easier to develop, test and deploy updates independently and is it lightweight by sharing a OS/kernel. Here is a quick overview of Docker.
![image](https://github.com/user-attachments/assets/fc895b71-97d7-4eca-acaa-45a46dca4bda)

![image](https://github.com/user-attachments/assets/0082f5f5-a93a-46cc-92e9-63998ddeb971)
![image](https://github.com/user-attachments/assets/b24cb952-3c87-492d-a9d8-0721dd42247a)

## Setting up EC2 for Elasticsearch on AWS
For this tep you will need an Amazon Web Services AWS account to set up EC2 for Elasticsearch. You can lookup online how to open an account, for the sake of this step I will assume you already have one.  
Set up am EC2 instance and create a key pair to access it. I am using Ubuntu for this step.  
![image](https://github.com/user-attachments/assets/a34f8e8e-6856-4a52-a4ca-aa11e123972e)

## Install Ekasticsearch on EC2
Connect to you instance  
![image](https://github.com/user-attachments/assets/1987c429-e111-4e67-83e6-83a40ae87caf)  
Now make sure your machine is up to date by running sudo apt update.  
![image](https://github.com/user-attachments/assets/95eb8b7e-82eb-46a2-8f44-cd128e7249aa)  
now we must install docker using this commands:  
sudo apt install docker-compose  
sudo apt install docker.io  

now we have to create a folder called elasticsearch inside use the command:  
mkdir elasticsearch  
ls  
travel to the folder using the command:  
cd elasticsearch/  
and we must edit the file now , go to [ELK-docker-compose.yml.yml](/ELK-docker-compose.yml.yml) and copy and paste the contents to the file.  
vi docker-compose.yml  
![image](https://github.com/user-attachments/assets/ccd81920-d735-4479-9653-68f954e62b59)




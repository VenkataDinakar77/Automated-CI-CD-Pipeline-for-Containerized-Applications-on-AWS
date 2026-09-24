
# Automated CI/CD Pipeline for Containerized Applications on AWS

A production-ready, automated deployment pipeline, that ensures faster releases, consistent environments, and reduced manual errors. 

## Overview
* **FreshEats**, a growing food delivery startup, relied on manual application builds, server updates, and deployments, resulting in inconsistent environments and deployment downtime.
* As development accelerated, manual deployments led to **slower release cycles, deployment errors, delayed fixes, and increased operational risk**.
* The engineering team needed a **scalable and automated deployment approach** to support frequent application releases while improving reliability.

## Solution

* Containerized the application using **Docker** and stored container images securely in **Amazon ECR** for consistent application deployments.
* Deployed the application using **Amazon ECS Fargate** with an **Application Load Balancer (ALB)** to provide scalable container hosting and reliable traffic distribution.
* Implemented an automated **GitHub Actions CI/CD pipeline** to build Docker images, push them to ECR, and deploy updated application versions to ECS whenever approved code changes are pushed.


## About this project

This project demonstrates automation of containerized application deployment on AWS using CI/CD

- Containerize applications using **Docker**
- Manage container images with **Amazon ECR**
- Deploy serverless containers using **Amazon ECS Fargate**
- Expose services securely with an **Application Load Balancer**
- Configure **networking and security groups** correctly
- Automate deployments using **GitHub Actions**
- Validate deployments visually through a frontend UI

## AWS services used:
- **Docker** → Containerize the application
- **Amazon ECR** → Store and manage container images
- **Amazon ECS (Fargate)** → Run containers without managing servers
- **Application Load Balancer** → Route traffic to containers
- **AWS IAM** → Manage secure permissions for services and CI/CD
- **GitHub Actions** → Build and deploy the application automatically
- **Amazon CloudWatch** → Monitor logs and task execution






## Architectural Diagram

![App Screenshot](https://dummyimage.com/468x300?text=App+Screenshot+Here)


## Project Workflow

**1. Application Development & Code Push**
- The application code and Docker configuration are maintained in a **GitHub repository**. When an approved code change is pushed to the main branch, the CI/CD workflow is automatically triggered.

**2. CI/CD Pipeline Trigger**
- **GitHub Actions** starts the automated deployment workflow. The pipeline checks out the latest application code and prepares the environment for the build and deployment process.

**3. Build the Docker Image**
- The pipeline uses **Docker** to package the application and its dependencies into a container image, providing a consistent runtime environment across deployments.

**4. Authenticate with AWS**
- The GitHub Actions workflow authenticates with AWS using configured **IAM permissions**. These permissions allow the pipeline to interact securely with required services such as Amazon ECR and Amazon ECS.

**5. Push the Image to Amazon ECR**
- The newly built Docker image is tagged and pushed to **Amazon Elastic Container Registry (ECR)**, which acts as the centralized repository for application container images.

**6. Update the Amazon ECS Service**
- After the image is successfully published, GitHub Actions triggers an update to the **Amazon ECS service**, allowing the latest application version to be deployed.

**7. Deploy Containers with AWS Fargate**
- **Amazon ECS with AWS Fargate** runs the application as containerized tasks without requiring the team to provision or manage EC2 container hosts.

**8. Route Application Traffic**
- An **Application Load Balancer (ALB)** receives incoming application requests and routes traffic to healthy ECS tasks. Health checks help ensure traffic is directed only to available application targets.

**9. Networking & Security**
- The application operates within an **Amazon VPC**, with subnets and Security Groups controlling network connectivity. Security Groups restrict traffic based on the application's required ports and communication paths.

**10. Monitor the Application**
- **Amazon CloudWatch** collects application and ECS task logs and provides monitoring information that can be used to troubleshoot failed tasks, deployments, and application issues.

**11. Validate the Deployment**
- After deployment, the application is accessed through the **Application Load Balancer endpoint** to verify that the latest application version is running successfully.

### CI/CD Execution Flow

`Developer → GitHub → GitHub Actions → Docker Build → Amazon ECR → Amazon ECS/Fargate → Application Load Balancer → Users`

Supporting services:

`AWS IAM → Authentication & Permissions`

`Amazon CloudWatch → Logs & Monitoring`

`Amazon VPC + Security Groups → Networking & Access Control`

---

## Conclusion

* Built an **end-to-end CI/CD pipeline** to automate the deployment of a containerized application on AWS.
* Used **Docker and Amazon ECR** to create, version, and centrally manage application container images.
* Deployed containerized workloads using **Amazon ECS Fargate**, reducing the need to manage underlying servers.
* Integrated an **Application Load Balancer, VPC networking, Security Groups, IAM, and CloudWatch** to support secure, accessible, and observable application deployments.
* Automated the build and deployment workflow using **GitHub Actions**, reducing manual deployment steps and improving release consistency.
* Gained practical experience with **containerization, CI/CD automation, AWS container services, networking, IAM, load balancing, and cloud monitoring**.

## Authors

- [@LinkedIn](https://www.linkedin.com/in/venkata-dinakar77)
- [@GithHub](https://github.com/VenkataDinakar77?tab=repositories)
- Email Id: dinakar.kunduru0414@gmail.com

# Automated-CI-CD-Pipeline-for-Containerized-Applications-on-AWS

[Youtube Private Video Link](https://youtu.be/1X8nI43q_uA)


![university Feedback xpress](https://github.com/a-verma26/University-FeedbackXpress/assets/26337680/fc7919d8-78a7-443d-bb83-33a9d2b5a6d6)

# Microservices Application Deployment

## Overview

For this assignment, our objective is to develop and deploy a Microservices based containerized application using SpringBoot and Amazon Relational Database Services (RDS) on Kubernetes to enhance its scalability and resilience. Our baseline configuration involves running at least three pods continuously.

To manage the Kubernetes services, we utilize Rancher. Additionally, we have established a CI/CD pipeline that involves a Git source code repository on GitHub and Jenkins for automated build and deployment of the application on Kubernetes.

When changes are made to the code in the GitHub repository, the pipeline automatically triggers a build and deployment process to ensure that the latest version of the application is always available on Kubernetes.

We test the working of our containerized application by calling different CRUD API calls using Postman.

Note: These are as part of document, location can be seen in the folder Structure i.e. SWE645-Assignment3.pdf

## Contents

- [Overview](#overview)
- [Links](#links)
- [Tasks](#tasks)
- [Pre-requisites](#pre-requisites)
- [Technology Utilized](#technology-utilized)
- [Jenkins Pipeline Explanation](#jenkins-pipeline-explanation)
- [Folder Structure](#folder-structure)

## Links

**Note:** Note: Please note that the URLs mentioned below might not work as the AWS Lab (Closes after 4 hours) and GKE clusters were terminated after the demo video was recorded due to their high cost.

- [LoadBalancer Access](https://34.194.61.172/k8s/clusters/c-w2vxb/api/v1/namespaces/default/services/http:spring-boot-assignment:8080/proxy/)
- [Jenkins](http://44.194.15.192:8080)
- [Rancher](http://44.194.15.192:8080)

## Tasks

1. **Create Database using Amazon RDS**
   - Set up Postgres database.
   - Backend in SpringBoot for CRUD operations.
   - Dockerize the application using Docker and Docker Hub.

2. **Create EC2 Instances using AWS Lab**
   - Set up Jenkins and Rancher.

3. **Setup Google Cloud Platform for GKE**

4. **Setup Rancher to Manage Kubernetes Cluster on GKE**

5. **Manage CI/CD using Jenkins, Docker Hub**

6. **Test Backend APIs using Postman**

## Pre-requisites

- IDE for development.
- Postman for API testing.
- DBeaver for Database testing/setup.
- Docker Desktop for building and testing local images.
- Access to AWS Learner lab provided by Dr. Vinod Dubey.
- Personal accounts on GitHub, Google Cloud Platform, and Docker Hub.

## Technology Utilized

- GitHub
- IntelliJ IDE
- Postman
- Docker Desktop and Docker Hub
- AWS (EC2, Elastic IP, RDS - Postgres)
- DBeaver
- Google Cloud Platform (GKE)
- Jenkins
- Kubernetes
- Rancher

## Jenkins Pipeline Explanation

This Jenkins pipeline script defines stages for building and deploying a Spring Boot application in a Kubernetes cluster:

1. **Prerequisites:**
   - Setup necessary credentials and environment variables.

2. **Checkout:**
   - Check out the source code from the SCM.

3. **Build:**
   - Build the application using Maven and archive generated artifacts (JAR file).

4. **Docker Build and Push:**
   - Build a Docker image of the application and push it to a Docker registry.

5. **Deploy to Kubernetes:**
   - Use kubectl to roll out a new version of the application by restarting the deployment.

## Folder Structure

1. **survey-form Folder (Spring Boot Project):**
   - DockerFile
   - Jenkinsfile
   - src folder
     - Main folder
       - Controller
       - Entity
       - Repository
       - Service
     - Resources folder
       - Templates (Index.html and surveysRecord.html)
       - Static (studentFormStyle.css)

2. **Video Recording Folder**
3. **YAML Files**
   - K8.yaml
   - spring-boot-assignment.yaml
4. **SWE645-HW3-Installation&SetupInstructions.pdf**
5. **ReadMe**


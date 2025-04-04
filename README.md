# Jenkins SCM Pipeline Demo

This repository demonstrates a Jenkins pipeline with SCM integration running in Docker.

## Setup Instructions

1. Clone this repository:

    ```bash
    git clone <your-repository-url>
    cd Jenkins-SCM-Pipeline-Demo
    ```

2. Build and start Jenkins container:

    ```bash
    docker-compose up -d
    ```

3. Get the initial admin password:

    ```bash
    docker exec jenkins cat /var/jenkins_home/secrets/initialAdminPassword
    ```

4. Access Jenkins at http://localhost:8080

## Setting up GitHub Integration

1. In Jenkins, go to "Manage Jenkins" → "Manage Credentials" → "System" → "Global credentials" → "Add Credentials"
2. For HTTPS: Add your GitHub username and personal access token
   For SSH: Add your SSH private key

3. In Jenkins, create a new Pipeline job:
    - Select "Pipeline script from SCM"
    - Select Git as SCM
    - Enter your repository URL
    - Select the credentials you added
    - Specify the branch to build
    - Save and run the pipeline

## Pipeline Structure

The Jenkinsfile defines a simple pipeline with the following stages:

-   Checkout
-   Build
-   Test
-   Deploy

Customize the stages according to your project needs.

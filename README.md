### Continuous Delivery Pipeline

## Project Overview

This repository contains the source code and configuration files for setting up a continuous delivery pipeline for a simple web application. The pipeline automates the process of deploying the web application whenever changes are made to the source code.

## Set Up Git Repo

1. **Clone the Repository:**
   - Fork the starter repository (if necessary) and clone the repository to your local machine:
     ```bash
     git clone https://github.com/Battlecode93/aws-elastic-beanstalk-express-js-sample
     ```

2. **Make Changes:**
   - Open the `app.js` file and make any desired changes.
   - Save the file.

3. **Commit and Push Changes:**
   - In the terminal, navigate to the project folder:
     ```bash
     cd aws-elastic-beanstalk-express-js-sample/
     ```
   - Commit your changes and push them to your GitHub repository:
     ```bash
     git add .
     git commit -m "Made changes to app.js"
     git push
     ```

## Deploy Web App

1. **Create AWS Elastic Beanstalk Environment:**
   - Go to the AWS Elastic Beanstalk console and create a new application.
   - Choose the web server environment, label the application (e.g., DevOpsGettingStarted), and select the Node.js platform.
   - Use an existing service role and the default EC2 instance profile.
   - Submit the configuration and wait for the deployment to be successfully launched.

## Create Build Project

1. **Configure AWS CodeBuild:**
   - Set up a build project with AWS CodeBuild.
   - Configure GitHub as the source provider for the build project.
   - Run a build using AWS CodeBuild to compile source code, run tests, and produce deployable software packages.

## Create Delivery Pipeline

1. **Set Up AWS CodePipeline:**
   - Create a new pipeline on AWS CodePipeline.
   - Configure your GitHub repository as the source code provider.
   - Configure the build stage by selecting the AWS CodeBuild project.
   - Deploy the application to AWS Elastic Beanstalk in the pipeline section.

2. **Pipeline Execution:**
   - Start the pipeline execution and monitor the progress.
   - Once the Deploy stage turns green, click on the AWS Elastic Beanstalk link to access the deployed web application.

## Finalize Pipeline and Test

1. **Add Manual Review Stage:**
   - Add a manual review stage between the Build and Deploy stages in AWS CodePipeline.
   - Code changes will now require manual review and approval before being deployed to AWS Elastic Beanstalk.

## Conclusion

This README provides an overview of the continuous delivery pipeline setup for the web application. Follow the steps outlined above to make changes, trigger builds, and deploy updates to your AWS Elastic Beanstalk environment through the automated pipeline. For additional details and troubleshooting, refer to the documentation for each AWS service involved.

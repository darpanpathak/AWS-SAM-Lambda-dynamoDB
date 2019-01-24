# Introduction
This git repository is an example microservice to perform CRUD operation. This microservice is deployed on AWS Lamnda and API Gateway using SAM(Serverless application model). SAM cli is a great tool to manage your AWS infrastructure and achieve IaC(Infrastructure as Code) model. 

# Prerequisite
- Knowledge of NodeJs, Basic Javascript and api development
- Understanding of AWS services
- AWS CLI installed and configured
- SAM CLI installed and configured
- NodeJs 8.10 or greater installed on local machine

# Highlights
- Use of SAM Templates to create infra and deploy code  
- Create a serverless lambda function in NodeJs 
- Store data in dynamoDB using NodeJs and lambda function
- Use of API Gateway AWS service to trigger lambda function

# Commands
Once you clone the repository or create your own function and template following commands are required to package and deploy the application.
- Packaging - sam package --template-file template.yml --output-template-file package.yml --s3-bucket YOUR_BUCKET_NAME
- Deploying - sam deploy --template-file package.yml --stack-name YOUR_STACK_NAME --capabilities CAPABILITY_IAM

For example:

- Packaging - sam package --template-file template.yml --output-template-file package.yml --s3-bucket inkloft-backend-products
- Deploying - sam deploy --template-file package.yml --stack-name inkloft-backend-products --capabilities CAPABILITY_IAM
# Elasicsearch service

### Stack creates
- Elasticsearch service in production mode.
- Cognito resources for authentication
- Lambda subscription filter for streaming cloudwatch logs to Elasticsearch
- IAM roles for the resources

> The stack takes most of the values as paramaters. Please read the Descriptions to find the details of the paramters expected in the stack.

The stack use Lambda subscription filter to send cloudwatch logs to Elasticsearch. The Lambda function *index.js* need to be zipped and stored in an S3 bucket before running this stack. The stack expect the S3 bucket name and the ZIP file name as parameters to create the Lambda function.
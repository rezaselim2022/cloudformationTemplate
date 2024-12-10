# AWS CloudFormation Project: Event-Driven Architecture
This project automates the deployment of an event-driven system using AWS CloudFormation.
It includes S3 bucket notifications, SNS topics, SQS queues, DynamoDB, 
and Lambda integration to enable efficient data processing and messaging workflows.
## Prerequisites
- AWS CLI installed and configured
- AWS CloudFormation knowledge
- Git installed

## Event Workflow
1. **S3 Bucket:** Triggers an SNS notification upon file upload.
2. **SNS Topic:** Broadcasts messages to:
   - SQS Queue
   - Lambda Function
   - Email Subscribers
3. **Lambda Function:** Processes messages and stores data in DynamoDB.
4. **DynamoDB Stream:** Captures real-time data changes.

### Example Flow:
1. Upload a file to the S3 bucket (`my-bucket-name`).
2. SNS topic (`my-topic-name`) broadcasts the event.
3. Lambda function logs the event and saves metadata to DynamoDB.
4. SQS queue retains the message for backup.

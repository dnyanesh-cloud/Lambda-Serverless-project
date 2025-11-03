#  AWS S3 → Lambda → SNS Email Notification

This project automatically sends an email notification via *Amazon SNS* whenever a new file is uploaded to an *S3 bucket*.  
It uses an *AWS Lambda* function as the event processor.

---

##  Project Overview

*Flow:*
1. A file is uploaded to an S3 bucket.  
2. S3 triggers a Lambda function using an event notification.  
3. The Lambda function publishes a message to an SNS topic.  
4. SNS sends an email to subscribed recipients.

---

## 🛠 AWS Services Used

- *Amazon S3* – Stores uploaded files and triggers Lambda.  
- *AWS Lambda* – Runs serverless code automatically.  
- *Amazon SNS (Simple Notification Service)* – Sends email alerts.  
- *IAM* – Provides permissions for S3 and SNS access.

---
## Steps to Set Up:
## Step 1 :-Create an S3 bucket
![](./AWS/Screenshot%20(197).png)
## Step 2 :-Create an SNS Topic
![](./AWS/Screenshot%20(198).png)
## Step 3 :-Subscribe your email to the topic
![](./AWS/Screenshot%20(199).png)
## Step 4 :-Create a Lambda function
- Add an S3 Trigger
- Add an SNS Destination

![](./AWS/Screenshot%20(200).png)
## Step 5 :-Add Permission for SNS and S3
![](./AWS/Screenshot%20(201).png)
## Step 6 :-Test it
### 1 : Upload any file to your S3 bucket
![](./AWS/Screenshot%20(202).png)
### 2 : You'll get an email notification from SNS
![](./AWS/Screenshot%20(203).png)

## Conclusion :
This project demonstrates how to automate email notifications using AWS Lambda, Amazon S3, and Amazon SNS. Whenever a new file is uploaded to the S3 bucket, the Lambda function is automatically triggered and sends an email alert via SNS.
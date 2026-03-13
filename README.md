![AWS](https://img.shields.io/badge/AWS-Lambda-orange)
![Cloud](https://img.shields.io/badge/Cloud-Serverless-blue)
![Python](https://img.shields.io/badge/Python-3.x-green)

# Serverless Image Processing System using AWS Lambda

A serverless cloud-based image processing system built using AWS services. The application automatically resizes images when they are uploaded to an Amazon S3 bucket using an event-driven architecture powered by AWS Lambda.

---

## Academic Context

This project was developed as part of coursework at **Blekinge Institute of Technology (BTH)**.

---

## System Overview

The system follows an event-driven serverless architecture:

1. A user uploads an image to an **Amazon S3 input bucket**
2. The upload event triggers an **AWS Lambda function**
3. The Lambda function processes and resizes the image
4. The resized image is stored in an **Amazon S3 output bucket**

---

## Architecture 

Workflow:

User Upload → Amazon S3 (Input Bucket) → AWS Lambda → Resized Image → Amazon S3 (Output Bucket)

---

## Technologies Used

- AWS Lambda
- Amazon S3
- Amazon CloudWatch
- Python
- Serverless Architecture

---

## Project Structure

aws-serverless-image-processing
│
├── lambda_function.py
├── requirements.txt
├── architecture.png.jpeg
└── README.md


---

## Deployment (AWS Lambda)

The Lambda function and dependencies are packaged before deployment.

### Install Dependencies

```bash
pip install -r requirements.txt -t .
```

## Create Deployment Package
```bash
zip -r deployment-package.zip .
```
Deploy to AWS Lambda

Open the AWS Lambda Console

Create or select your Lambda function

Upload deployment-package.zip

Configure the S3 trigger for the input bucket

Once deployed, uploading an image to the S3 bucket will automatically trigger the Lambda function and store the resized image in the output bucket.

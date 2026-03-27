# 🚀 Serverless Contact Form on AWS (with CloudFront)

This project is a fully serverless contact form built using AWS services, designed to handle user messages without running traditional servers.

---

## 📌 Project Overview

Users access the website through a CDN (CloudFront), which improves speed and performance.

When a message is submitted:

1. Request goes to API Gateway
2. AWS Lambda processes the request
3. Data is stored in DynamoDB
4. Logs are stored in CloudWatch

---

## 🏗️ Architecture


<img width="771" height="482" alt="contactform" src="https://github.com/user-attachments/assets/409fdeba-bf62-49c9-b80e-87a1b3dc0aca" />

---

## 🛠️ Technologies Used

* AWS S3 (Static Website Hosting)
* AWS CloudFront (CDN)
* AWS API Gateway
* AWS Lambda
* AWS DynamoDB
* AWS CloudWatch
* AWS IAM
* HTML, CSS, JavaScript

---

## 📁 Project Structure

```bash
serverless-contact-form/
│
├── frontend/
├── lambda/
├── screenshots/
├── Architecture-daigram/
├── README.md
└── .gitignore
```

---

## ⚙️ Setup Guide

### 1. S3 Setup

* Create bucket
* Upload frontend files
* Enable static hosting

### 2. CloudFront Setup

* Create distribution
* Link to S3 bucket
* Use generated URL

### 3. DynamoDB

* Create table: `ContactFormMessages`
* Primary key: `id`

### 4. Lambda

* Create function
* Add code to save form data

### 5. Create SNS Topic
 * Create a topic
 * Add an email subscription
 * Confirm the subscription from your email

### 6. API Gateway

* Create HTTP API
* Add POST route → Lambda

### 7. Connect Frontend

Update API endpoint in `script.js`

---

### ⚠️  Common Issues

### CORS Errors
 * Enable CORS in API Gateway
 * Add headers in Lambda response
   
### No Email Received
 * Confirm SNS subscription
   
### Lambda Not Triggering
 * Check API Gateway integration
 * Verify IAM permissions


---

### 🔐 Security Best Practices
 * Follow least privilege for IAM roles
 * Restrict DynamoDB access to specific table
 * Avoid hardcoding sensitive values

---
## 📸 Screenshots

Add your images inside `/screenshots` and they will display here.

---

## 🚀 How to Run

Clone the repo:

```bash
git clone https://github.com/YOUR-USERNAME//serverless-contact-form-aws.git
```

Follow setup steps above.

---

## 📈 Future Improvements

* Add email notifications (SES)
* Add validation
* Use Terraform

---

## 👨‍💻 Author

Adeola Hephzibah Akinlade
Cloud Engineer

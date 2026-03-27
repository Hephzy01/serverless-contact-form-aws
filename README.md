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

User → CloudFront → S3 → API Gateway → Lambda → DynamoDB

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

### 5. API Gateway

* Create HTTP API
* Add POST route → Lambda

### 6. Connect Frontend

Update API endpoint in `script.js`

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

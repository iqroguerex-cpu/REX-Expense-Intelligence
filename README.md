# 🧠 REX Intelligence — Multi-Tenant Serverless SaaS (IQROGUEREX)

<p align="center">

[![Live App](https://img.shields.io/badge/Live%20App-Frontend-success?style=for-the-badge)](https://main.d3h52tggmr1uxu.amplifyapp.com)
[![Backend API](https://img.shields.io/badge/API-AWS%20Lambda-blue?style=for-the-badge\&logo=amazonaws)](https://r3yxxs5yuc.execute-api.ap-south-1.amazonaws.com/default)
![AWS](https://img.shields.io/badge/AWS-Serverless-orange?style=for-the-badge\&logo=amazonaws)
![FastAPI](https://img.shields.io/badge/FastAPI-Backend-009688?style=for-the-badge\&logo=fastapi)
![DynamoDB](https://img.shields.io/badge/DynamoDB-NoSQL-blue?style=for-the-badge\&logo=amazondynamodb)
![Cognito](https://img.shields.io/badge/Auth-Cognito-purple?style=for-the-badge\&logo=amazonaws)

</p>

---

## 🚀 Overview

**REX Intelligence** is a **multi-tenant, serverless SaaS platform** designed for secure financial tracking and analytics.

Built using a **modern full-stack cloud architecture**, it combines:

* ⚡ FastAPI (backend logic)
* ☁️ AWS Lambda (serverless compute)
* 🗄️ DynamoDB (multi-tenant database)
* 🔐 AWS Cognito (authentication)
* 🎨 Tailwind + Chart.js (frontend analytics UI)

---

## 🏗️ Architecture

```bash id="rexarch1"
Frontend (AWS Amplify + Tailwind UI)
        ↓
API Gateway (CORS + Routing)
        ↓
AWS Lambda (FastAPI via Mangum)
        ↓
DynamoDB (Multi-Tenant Storage)
        ↑
Auth Layer (AWS Cognito)
        ↑
Deployment (S3 + CI/CD)
```

---

## ✨ Key Features

### 🔐 Security & Identity

* AWS Cognito authentication (signup, login, verification)
* Token-based user identity (`user-id` header)
* Strict CORS protection (whitelisted domains)
* Multi-user data isolation

### 📊 Core Functionality

* Add, view, delete financial entries
* Real-time analytics dashboard
* Spending visualization (Chart.js)
* Category-based tracking

### 🧪 Sandbox Mode

* Guest users can explore safely
* Data stored in browser memory (no DB usage)
* Zero cost + demo-friendly

### ☁️ Cloud & DevOps

* Serverless architecture (Lambda)
* Deployment via S3 (Lambda packages)
* CI/CD via GitHub + Amplify
* Environment variable-based configuration

---

## 🛠 Tech Stack

### Backend

* FastAPI
* Mangum
* Boto3
* AWS Lambda
* API Gateway

### Database

* DynamoDB (Composite Key)

  * Partition Key → `user_id`
  * Sort Key → `id`

### Authentication

* AWS Cognito

### Frontend

* HTML5
* Tailwind CSS (Glassmorphism UI)
* JavaScript
* Chart.js

### DevOps

* GitHub
* AWS Amplify
* Amazon S3

---

## 📂 Project Structure

```bash id="rexstruct2"
rex-intelligence
│
├── frontend/
│   └── index.html
│
├── backend/
│   ├── main.py
│   └── requirements.txt
│
└── README.md
```

---

## 📡 API Endpoints

| Method | Endpoint                        | Description       |
| ------ | ------------------------------- | ----------------- |
| GET    | `/expenses`                     | Get user expenses |
| POST   | `/expenses/create_expense`      | Create expense    |
| DELETE | `/expenses/delete_expense/{id}` | Delete expense    |

---

## 🎯 Example Data Model

```json id="rexmodel1"
{
  "user_id": "user-123",
  "id": 1699999999999,
  "title": "Cloud Infrastructure",
  "amount": 240.50,
  "category": "Infrastructure",
  "date": "2026-01-01T12:00:00Z"
}
```

---

## 🔐 Security Design

* Zero Trust Architecture
* Per-user data isolation (multi-tenant)
* Header-based identity validation
* IAM Least Privilege for Lambda
* No direct database exposure

---

## 📊 Key Engineering Highlights

### 🧠 Backend

* Pydantic validation layer (data integrity)
* Decimal handling for financial precision
* Query-based DynamoDB access (no scans)

### ⚡ Performance

* Serverless scaling (1 → 10,000 users automatically)
* Zero idle cost (Lambda free tier optimized)

### 🎨 Frontend

* Glassmorphism UI (Tailwind)
* Real-time chart analytics
* Responsive & minimal design

---

## 🚀 Deployment

### Backend

* Packaged as ZIP
* Uploaded to **Amazon S3**
* Deployed via **AWS Lambda**

### Frontend

* Hosted on **AWS Amplify**
* Auto-deploy via GitHub

---

## 🔮 Future Improvements

* 🔐 JWT validation via Cognito tokens
* 📊 Advanced analytics (ML insights)
* 📅 Budget tracking & alerts
* 🔍 Search & filtering
* 📱 Mobile app version

---

## 👨‍💻 Author

**Chinmay V Chatradamath**

---

## ⭐ Support

If you like this project, give it a ⭐ on GitHub!

---

## 💡 Final Note

This project demonstrates:

* ✅ Full-stack engineering
* ✅ Cloud architecture (AWS)
* ✅ Security (multi-tenant + auth)
* ✅ DevOps (CI/CD + S3 deployment)

👉 This is **production-grade SaaS architecture**, not just a project.

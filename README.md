# 🧠 Bgone-AI — AI-Powered Background Remover SaaS

**Bgone-AI** is a full-stack SaaS platform that allows users to remove image backgrounds using advanced AI. It combines powerful backend logic in Spring Boot with a modern React frontend. Users can sign in securely, upload images, purchase credits, and remove backgrounds in seconds using the Clipdrop API.

---

## 📌 Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Architecture](#architecture)
- [Screenshots](#screenshots)
- [API Workflow](#api-workflow)
- [Installation](#installation)
- [License](#license)

---

## 🚀 Features

### 🖼️ AI-Powered Image Background Removal
- Utilizes [Clipdrop API](https://clipdrop.co) to remove backgrounds with high accuracy.

### 🔐 Secure Authentication
- **Frontend**: Clerk for user management, JWT tokens.
- **Backend**: Spring Security handles authorization and route protection.

### 💳 Razorpay Integration
- Seamless integration for credit purchases.
- Each background removal deducts one credit.

### 📦 Credit Management System
- Tracks and updates credits per user.
- Admin control over credit plans and processing logic.

### 🔗 RESTful APIs + Feign Clients
- Modular, microservice-like Spring Boot setup with `FeignClient` for clean inter-service communication.

### 📁 Image Upload & Base64 Conversion
- Users upload images from the frontend.
- Backend processes and stores metadata securely.

### 🌐 Fully Responsive UI (Frontend Included)
- Built with React and Tailwind CSS.
- Clean and modern user interface with mobile responsiveness.

---

## 🧠 Tech Stack

| Layer        | Technologies Used                                    |
|--------------|------------------------------------------------------|
| **Frontend** | React.js, Tailwind CSS, Axios, Clerk, Toastify       |
| **Backend**  | Spring Boot, Spring Security, Feign Clients, JWT     |
| **Database** | MySQL                                                |
| **Payments** | Razorpay                                             |
| **AI Engine**| Clipdrop API                                         |
| **Deployment**| Docker (optional), Vite (React)                     |

---

## 🧱 System Architecture

```plaintext
Frontend (React + Clerk)
        |
        |  REST API Calls (JWT Protected)
        ↓
Backend (Spring Boot)
        |----→ Razorpay API (Payments)
        |----→ Clipdrop API (AI Image Processing)
        |----→ MySQL DB (Users, Images, Credits)

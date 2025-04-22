# 💳 Credit Card Recommendation System

---

## 🧠 Overview

The **Credit Card Recommendation System** is a MERN-based web application designed to suggest the most suitable credit cards to users based on factors like income, credit score, and card preferences. It leverages a rule-based engine to filter cards stored in a MongoDB database and delivers real-time, personalized recommendations through a responsive and intuitive UI.

---

## 📚 Table of Contents

- [Introduction](#introduction)  
- [Screenshots](#screenshots)  
- [Functional Requirements](#functional-requirements)  
- [Non-Functional Requirements](#non-functional-requirements)  
- [System Design & Implementation](#system-design--implementation)  
  - [MVC Architecture](#mvc-architecture)  
  - [MERN Framework](#mern-framework)  
- [Technology Stack](#technology-stack)  
- [Database Description](#database-description)  
- [Module Description](#module-description)  
- [API Services](#api-services)  
- [Results and Discussions](#results-and-discussions)  
- [Testing](#testing)  
- [Conclusion & Future Scope](#conclusion--future-scope)
  
---

## 📝 Introduction

Traditional credit card comparison systems often lack personalization. This system addresses that by integrating user-specific data points—like income and credit score—to offer real-time recommendations. It aims to simplify the decision-making process and improve financial literacy by suggesting cards aligned with individual needs.

---

## ✅ Functional Requirements

- User Interface: Form for entering user data (income, credit score, preferences)  
- API Communication: Axios used for frontend-backend interaction  
- Rule-Based Filtering: Custom logic to match user input with card eligibility  
- Display Results: Card suggestions with reasons  
- Responsive Design: Mobile-friendly layout  
- Admin: Optional route to manage card data

---

## 📉 Non-Functional Requirements

- Fast Response: Results generated in under 5 seconds  
- Lightweight UI: Page load < 3 seconds on average  
- Scalability: Ready for ML integration  
- Usability: Minimal inputs and validation  
- Security: Basic backend validation and secure API endpoints

---

## ⚙️ System Design & Implementation

### MVC Architecture

- **Model**: MongoDB models for storing card details  
- **View**: React.js frontend with dynamic form and result display  
- **Controller**: Express.js endpoints and logic that handle user input and filter results  

### MERN Framework

- **MongoDB**: Stores credit card data with eligibility criteria  
- **Express.js**: Handles API routes and rule-based filtering logic  
- **React.js**: Dynamic and responsive user interface  
- **Node.js**: Manages backend server and app execution

---

## 🗃️ Database Description

Each credit card is stored as a document with fields like:
```json
{
  "cardName": "Platinum Rewards",
  "minIncome": 40000,
  "creditScoreRequirement": 700,
  "type": "Travel",
  "annualFee": 500,
  "benefits": ["Airport Lounge", "Travel Insurance", "Bonus Miles"]
}
```

---

## 🧩 Module Descriptions

- **Frontend (React.js)**: User form, card display components, and result layout  
- **Backend (Node.js + Express)**: Receives user input, applies logic, sends filtered results  
- **Database (MongoDB)**: Credit card data, stored and queried using Mongoose

---

## 🔌 API Services

- `POST /api/recommend`: Sends user data, returns card suggestions  
- `GET /api/cards`: (Optional) Fetches all available cards  
- `POST /api/cards`: (Admin only) Adds a new card to the database

---

## 📊 Results and Discussion

The recommendation logic is rule-based and returns accurate results based on three core inputs:
- Income Level  
- Credit Score  
- Card Type Preference  

We also explain the *why* for each suggestion so the user understands the recommendation.

---

## 🧪 Testing

Test cases cover:
- Input validation (missing or incorrect values)  
- Filtering accuracy  
- Response time of APIs  
- UI responsiveness on different screen sizes

Future testing scope includes:
- Unit tests for backend logic  
- E2E testing using Cypress or Selenium  

---

## 🚀 Conclusion & Future Scope

### 🔚 Conclusion

This project demonstrates how personalized recommendations can simplify complex financial decisions. It’s scalable, modular, and ready to support AI-based enhancements.

### 🌱 Future Scope

- ML-based Recommendation Engine  
- User Profile Management and History  
- Dynamic Offers Integration from Banks  
- Gamified Financial Literacy Experience  
- Mobile App Version (React Native)  
- OAuth and Secure Login System  

<!-- ===================================================== -->
<!-- HERO SECTION -->
<!-- ===================================================== -->

<h1 align="center">🛒 Distributed E-Commerce Platform</h1>
<h3 align="center">A Scalable Microservices-Based Capstone Project</h3>

<p align="center">
  <em>Designed & implemented as a production-inspired distributed system</em>
</p>

<p align="center">
  <a href="#-project-overview">Overview</a> •
  <a href="#-architecture--system-design">Architecture</a> •
  <a href="#-services--repositories">Services</a> •
  <a href="#-system-flow">Flow</a> •
  <a href="#-tech-stack">Tech Stack</a> •
  <a href="#-future-enhancements">Roadmap</a>
</p>

---

## 📌 Project Overview

This project is a **distributed e-commerce backend platform** built using a **microservices architecture**, where each core business capability is implemented as an **independent, deployable service**.

🎯 **Objective of this Capstone**
- Demonstrate real-world backend engineering practices
- Apply distributed system design principles
- Build a system that mirrors **industry-grade architectures**

Instead of a monolithic application, this platform models how **modern large-scale systems** (Amazon, Flipkart, Shopify) are actually built and evolved.

---

## 🧠 Architecture & System Design

✨ **Design Philosophy**
- 🧩 Microservices over monoliths
- 🔗 Loose coupling, strong service contracts
- ⚡ Event-driven communication
- 📈 Independent scalability
- 🛡️ Fault isolation by design

Each service:
- Owns its **data**
- Exposes **well-defined APIs**
- Communicates asynchronously where possible
- Can be scaled and deployed independently

This architecture strictly follows the **PRD and HLD** defined for the capstone.

---

## 🧩 Services & Repositories

> Each repository below represents a **standalone microservice**.  
> Together, they form **one cohesive e-commerce platform**.

---

### 🔐 User Service
🔗 **Repository:**  
👉 [User-Service](https://github.com/PremMakwana555/User-Service)

**Responsibilities**
- User registration & authentication  
- Secure login & session management  
- Profile management  
- Password reset flows  

**PRD Coverage**
- User Management  
- Authentication & Session Handling  

---

### 📦 Product Service
🔗 **Repository:**  
👉 [Product-Service](https://github.com/PremMakwana555/Product-Service)

**Responsibilities**
- Product catalog management  
- Category-based browsing  
- Product details & metadata  
- Designed for fast search (Elasticsearch-ready)

**PRD Coverage**
- Product Catalog  
- Search & Browsing  

---

### 🛒 Cart Service
🔗 **Repository:**  
👉 [Cart-Service](https://github.com/PremMakwana555/cart-service)

**Responsibilities**
- Add / remove items from cart  
- Maintain user cart state  
- Optimized for high read/write traffic  

⚡ **Design Highlights**
- NoSQL-friendly data model  
- Redis-based caching for speed  

**PRD Coverage**
- Cart & Checkout  

---

### 📑 Order Service
🔗 **Repository:**  
👉 [Order-Service](https://github.com/PremMakwana555/Order-Service)

**Responsibilities**
- Order creation & lifecycle management  
- Order history and tracking  
- Coordinates with payment & notification services  

**PRD Coverage**
- Order Management  
- Order Confirmation & Tracking  

---

### 🔔 Notification Service
🔗 **Repository:**  
👉 [Notification-Service](https://github.com/PremMakwana555/Notification-service)

**Responsibilities**
- Event-driven notifications  
- Order confirmations  
- User lifecycle emails  

📨 **Design Notes**
- Fully decoupled from core business logic  
- Consumes events from the message broker  

**PRD Coverage**
- Notifications  

---

### 🧭 Service Registry
🔗 **Repository:**  
👉 [Service-Registry](https://github.com/PremMakwana555/service-registry)

**Responsibilities**
- Dynamic service discovery  
- Runtime service registration  
- Enables horizontal scaling  

🧠 **Why This Matters**
Without service discovery, microservices become tightly coupled and brittle.  
This component enables **true distributed behavior**.

---

### 💳 Payment Service (Planned 🚧)

**Status:** In Progress  

**Planned Responsibilities**
- Payment gateway abstraction  
- Secure transaction handling  
- Payment confirmation events  

**PRD Coverage**
- Payments  
- Secure Transactions  
- Receipt Generation  

---

## 🔄 System Flow

```text
User
 ↓
API Request
 ↓
User Service ──► Product Service
 ↓                  ↓
Cart Service ◄───────┘
 ↓
Order Service
 ↓
┌───────────────┬────────────────┐
│ Payment       │ Notification   │
│ Service       │ Service        │
└───────────────┴────────────────┘

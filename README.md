# 🛒 Distributed E-Commerce Platform  
### Microservices-Based Capstone Project

> **Master’s Capstone Project**  
> A production-inspired, scalable e-commerce platform designed using modern distributed systems principles.

---

## 📌 Project Overview

This project is a **distributed e-commerce platform** built using a **microservices architecture**, where each core business capability is implemented as an independent service.

The goal of this capstone is to demonstrate **real-world backend engineering practices**, including:

- Microservice decomposition  
- Event-driven communication  
- Service discovery  
- Fault isolation  
- Independent scalability  
- Clean domain ownership  

Rather than a monolithic application, this system reflects how **modern large-scale platforms** (Amazon, Flipkart, Shopify) are architected.

The design and implementation follow the **Product Requirements Document (PRD)** and **High-Level Design (HLD)** defined for this project.

---

## 🧠 Architectural Principles

- **Microservices over Monolith** – each service owns its data and logic  
- **Loose Coupling, Strong Contracts** – services interact via APIs and events  
- **Event-Driven Design** – asynchronous communication where applicable  
- **Scalability by Design** – services scale independently  
- **Production-Oriented Thinking** – industry-aligned tools and patterns  

---

## 🧩 Services & Repositories

Each repository below represents an **independently deployable microservice**.  
Together, they form one cohesive e-commerce system.

---

### 🔐 User Service
**Repository:**  
https://github.com/PremMakwana555/User-Service.git

**Responsibilities**
- User registration and authentication  
- Secure login and session management  
- Profile management  
- Password reset functionality  

**PRD Coverage**
- User Management  
- Authentication & Session Handling  

---

### 📦 Product Service
**Repository:**  
https://github.com/PremMakwana555/Product-Service.git

**Responsibilities**
- Product catalog management  
- Category-based browsing  
- Product details and metadata  
- Designed for search integration (Elasticsearch)

**PRD Coverage**
- Product Catalog  
- Search & Browsing  

---

### 🛒 Cart Service
**Repository:**  
https://github.com/PremMakwana555/cart-service.git

**Responsibilities**
- Add/remove products from cart  
- Maintain user cart state  
- Optimized for fast access and updates  

**Design Notes**
- Designed for NoSQL-style storage  
- Redis-based caching for performance  

**PRD Coverage**
- Cart & Checkout  

---

### 📑 Order Service
**Repository:**  
https://github.com/PremMakwana555/Order-Service.git

**Responsibilities**
- Order creation and lifecycle management  
- Order history and tracking  
- Coordinates with payment and notification services  

**PRD Coverage**
- Order Management  
- Order Confirmation & Tracking  

---

### 🔔 Notification Service
**Repository:**  
https://github.com/PremMakwana555/Notification-service.git

**Responsibilities**
- Event-based user notifications  
- Order confirmation emails  
- User lifecycle notifications  

**Design Notes**
- Consumes events from the message broker  
- Decoupled from core business logic  

**PRD Coverage**
- Notifications  

---

### 🧭 Service Registry
**Repository:**  
https://github.com/PremMakwana555/service-registry.git

**Responsibilities**
- Service discovery  
- Dynamic service registration  
- Enables horizontal scaling  

**Why This Matters**
Service discovery is essential for true microservices.  
This component removes hard-coded dependencies and enables resilience.

---

### 💳 Payment Service (Planned)
**Status:** 🚧 In Progress  

**Planned Responsibilities**
- Payment gateway abstraction  
- Secure transaction handling  
- Payment confirmation events  

**PRD Coverage**
- Payment  
- Secure Transactions  
- Receipt Generation  

---

## 🔄 High-Level System Flow

1. User authenticates via **User Service**
2. Products are browsed via **Product Service**
3. Items are added to **Cart Service**
4. Checkout triggers **Order Service**
5. Order emits events consumed by:
   - **Payment Service**
   - **Notification Service**
6. Services discover each other using **Service Registry**

This flow follows an **event-driven architecture** as defined in the HLD.

---

## 🛠️ Technology Stack (Conceptual)

| Layer | Technologies |
|-----|-------------|
| API Layer | RESTful APIs |
| Communication | Event-driven (Kafka-style) |
| Databases | MySQL, MongoDB |
| Caching | Redis |
| Search | Elasticsearch |
| Service Discovery | Registry-based |
| Notifications | Email (extensible to SMS / Push) |

---

## 🎓 Academic & Engineering Value

This capstone demonstrates:

- Real-world microservice architecture  
- Clear separation of concerns  
- Distributed system communication patterns  
- Scalability and fault-tolerant design thinking  
- Production-inspired backend engineering  

The system is designed to be **extensible**, **observable**, and **cloud-ready**.

---

## 🚀 Future Enhancements

Planned and suggested improvements:

- API Gateway (centralized auth, routing, rate limiting)
- Observability (metrics, tracing, centralized logging)
- Distributed tracing (OpenTelemetry)
- Failure handling & retries
- Docker / Kubernetes deployment
- Security hardening (JWT, secrets management)
- Architecture diagrams and sequence flows

---

## 📚 Documentation

- Product Requirements Document (PRD)
- High-Level Design (HLD)
- Service-specific README files in each repository

---

## 👨‍💻 Author

**Prem Makwana**  
Master’s Capstone Project  
Focus: Backend Engineering, Distributed Systems, Microservices Architecture

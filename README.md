<style>
.badge {
  display: inline-block;
  padding: 6px 10px;
  margin: 4px 6px 4px 0;
  border-radius: 12px;
  background: #f2f4f8;
  font-size: 13px;
}
.section {
  margin-top: 40px;
}
.flow-step {
  padding: 8px 0;
}
</style>

# 🛒 Distributed E-Commerce Platform  
### Microservices-Based Capstone Project

<p>
  <span class="badge">Java</span>
  <span class="badge">Spring Boot</span>
  <span class="badge">Microservices</span>
  <span class="badge">Distributed Systems</span>
  <span class="badge">MS Capstone</span>
</p>

---

## 📌 Project Overview

This project is a **distributed e-commerce backend platform** designed using a **microservices architecture**, where each core business capability is implemented as an **independent, deployable service**.

The objective of this capstone project is to demonstrate **real-world backend engineering and distributed system design**, following patterns used in modern large-scale platforms such as Amazon, Flipkart, and Shopify.

Rather than a monolithic application, this system emphasizes:
- Service isolation  
- Independent scalability  
- Clear ownership of data and logic  
- Production-inspired architecture  

---

<div class="section"></div>

## 🧠 Architecture & Design Principles

<p>
  <span class="badge">Service Isolation</span>
  <span class="badge">Loose Coupling</span>
  <span class="badge">Scalable Design</span>
  <span class="badge">Event-Oriented Thinking</span>
</p>

**Core Principles**
- Each service owns its **data and business logic**
- Services interact via **well-defined REST APIs**
- Architecture supports **future async/event-driven evolution**
- Components are designed to scale and fail independently

This design strictly follows the **Product Requirements Document (PRD)** and **High-Level Design (HLD)** defined for the capstone.

---

<div class="section"></div>

## 🧩 Services & Repositories

Each repository below represents a **standalone microservice**.  
Together, they form a **single cohesive e-commerce platform**.

---

### 🔐 User Service  
🔗 **Repository:**  
👉 https://github.com/PremMakwana555/User-Service

**Responsibilities**
- User registration and authentication  
- Secure login and session management  
- Profile management and password reset  

---

### 📦 Product Service  
🔗 **Repository:**  
👉 https://github.com/PremMakwana555/Product-Service

**Responsibilities**
- Product catalog and category management  
- Product details and metadata  
- Search-ready service (as per design)

---

### 🛒 Cart Service  
🔗 **Repository:**  
👉 https://github.com/PremMakwana555/cart-service

**Responsibilities**
- Add and remove items from cart  
- Maintain user cart state  
- Optimized for high read/write operations  

---

### 📑 Order Service  
🔗 **Repository:**  
👉 https://github.com/PremMakwana555/Order-Service

**Responsibilities**
- Order creation and lifecycle management  
- Order history and tracking  
- Coordination with payment and notification services  

---

### 🔔 Notification Service  
🔗 **Repository:**  
👉 https://github.com/PremMakwana555/Notification-service

**Responsibilities**
- Event-based notifications  
- Order confirmations  
- User lifecycle communication  

---

### 🧭 Service Registry  
🔗 **Repository:**  
👉 https://github.com/PremMakwana555/service-registry

**Responsibilities**
- Service discovery  
- Dynamic service registration  
- Enables horizontal scaling  

---

### 💳 Payment Service (Planned 🚧)

🔗 **Repository:**   
👉 https://github.com/PremMakwana555/Payment-Service

** Responsibilities**
- Payment gateway abstraction  
- Secure transaction processing  
- Payment confirmation workflows  

---

<div class="section"></div>

## 🔄 End-to-End System Flow

<div class="flow-step">➡️ User authenticates via <strong>User Service</strong></div>
<div class="flow-step">➡️ Products are browsed using <strong>Product Service</strong></div>
<div class="flow-step">➡️ Items are added to cart via <strong>Cart Service</strong></div>
<div class="flow-step">➡️ Checkout triggers <strong>Order Service</strong></div>
<div class="flow-step">➡️ Order processing initiates downstream actions</div>
<div class="flow-step">  ↳ <strong>Payment Service</strong> handles payment</div>
<div class="flow-step">  ↳ <strong>Notification Service</strong> sends confirmation</div>
<div class="flow-step">➡️ Services discover each other using <strong>Service Registry</strong></div>

This flow aligns with an **event-oriented architecture** as described in the HLD.

---

<div class="section"></div>

## 🛠️ Tech Stack (Actual & Verified)

| Layer | Technology |
|------|-----------|
| Language | **Java** |
| Framework | **Spring Boot (Spring Ecosystem)** |
| Build Tool | Maven |
| API Style | RESTful APIs |
| Service Discovery | Spring-based Service Registry |
| Databases | Relational DB (MySQL / PostgreSQL as per service design) |
| Caching | In-memory / Redis (where applicable) |
| Notifications | Email (SMTP / provider-based) |
| Architecture | Microservices |
| Deployment | Docker-ready (recommended) |

This stack reflects the **actual implementation** present in the repositories.

---

<div class="section"></div>

## 🎓 Academic & Engineering Value

This project demonstrates:

- Real-world microservice decomposition  
- Distributed backend system design  
- Clear separation of concerns  
- Scalable and maintainable architecture  
- Production-inspired engineering decisions  

The system is designed to be **extensible, observable, and cloud-ready**.

---

<div class="section"></div>

## 🚀 Roadmap & Future Enhancements

<p>
  <span class="badge">API Gateway</span>
  <span class="badge">Observability</span>
  <span class="badge">Docker</span>
  <span class="badge">Kubernetes</span>
  <span class="badge">Security</span>
</p>

Planned improvements include:
- API Gateway for routing, auth, and rate limiting  
- Centralized logging and metrics  
- Distributed tracing (OpenTelemetry)  
- Payment service completion  
- Containerized deployment (Docker / Kubernetes)  
- Security hardening (JWT, secrets management)  
- Architecture and sequence diagrams  

---

<div class="section"></div>

## 👨‍💻 Author

**Prem Makwana**  
🎓 Master’s Capstone Project  
💡 Focus: Backend Engineering, Distributed Systems, Microservices Architecture  

🔗 **Project Hub:** https://premmakwana555.github.io/

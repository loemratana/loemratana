# 👋 Hi, I'm Ratana

### Full-Stack Developer · Backend-Focused · System Builder

I build **backend systems, APIs, databases, and production infrastructure**.

I'm interested in more than making features work.

I like understanding:

> **Why is this slow?**
> **Where is the bottleneck?**
> **What happens when traffic increases?**
> **How should the data be modelled?**
> **How do we know the system is healthy?**

---

## 🧠 How I Think About Systems

I usually approach a problem like this:

```text
             ┌──────────────────┐
             │     Problem      │
             └────────┬─────────┘
                      ↓
             ┌──────────────────┐
             │     Measure      │
             │ logs · metrics   │
             │ query timings    │
             └────────┬─────────┘
                      ↓
             ┌──────────────────┐
             │ Find Bottleneck  │
             │ API · DB · I/O   │
             │ network · code   │
             └────────┬─────────┘
                      ↓
             ┌──────────────────┐
             │     Analyze      │
             │ query plans      │
             │ data flow        │
             │ access patterns  │
             └────────┬─────────┘
                      ↓
             ┌──────────────────┐
             │     Optimize     │
             │ index · query    │
             │ architecture     │
             └────────┬─────────┘
                      ↓
             ┌──────────────────┐
             │    Measure Again │
             └──────────────────┘
```

I prefer **evidence over assumptions**.

---

# 🏗️ What I Build

| Area              | What I work on                                              |
| ----------------- | ----------------------------------------------------------- |
| ⚙️ Backend        | REST APIs, business logic, authentication, workflows        |
| 🗄️ Database      | Data modelling, indexes, queries, aggregation, transactions |
| 🔐 Security       | JWT, RBAC, OTP, email verification, password recovery       |
| ⚡ Performance     | API latency, database bottlenecks, query optimization       |
| 🌐 Frontend       | React, Next.js, React Native                                |
| 🚀 Infrastructure | Docker, Nginx, VPS, Cloudflare, SSL                         |
| 📊 Observability  | Grafana, Prometheus, Loki, Node Exporter, Netdata           |

---

# ⚙️ Backend Engineering

### Java / Spring Boot

```text
Controller
    ↓
Service
    ↓
Repository
    ↓
Database
```

I focus on keeping the layers clear and making business logic easy to test and maintain.

### Node.js / Express

```text
Request
   ↓
Middleware
   ↓
Validation
   ↓
Controller
   ↓
Service
   ↓
Database / Storage
```

I use Node.js when the application benefits from a lightweight API architecture and fast iteration.

---

# 🗄️ Database Engineering

I don't treat the database as just a place to store data.

I think about:

```text
Data Model
    ↓
Access Pattern
    ↓
Query
    ↓
Query Plan
    ↓
Index
    ↓
Performance
```

### Technologies

**PostgreSQL** · **MongoDB** · **Redis**

### Things I care about

* Choosing indexes based on real query patterns
* Avoiding unnecessary data loading
* Understanding query execution plans
* Optimizing aggregation queries
* Designing relationships and constraints
* Handling transactions and concurrent operations
* Using caching where it actually helps

---

# ⚡ Performance Engineering

When an endpoint is slow, I don't immediately add more hardware.

I investigate.

```text
Slow Request
     ↓
┌────────────────────┐
│ API timing         │
├────────────────────┤
│ Database timing    │
├────────────────────┤
│ Query execution    │
├────────────────────┤
│ Network / I/O      │
├────────────────────┤
│ Application logic  │
└────────────────────┘
     ↓
Find the actual bottleneck
     ↓
Optimize
     ↓
Benchmark again
```

### Typical optimizations

* Database indexes
* Query optimization
* Aggregation optimization
* Pagination
* Selecting only required fields
* Reducing unnecessary database requests
* Caching frequently accessed data
* Improving API response payloads

---

# 🔐 Security

Security is part of the system design, not something added at the end.

```text
Authentication
      ↓
Authorization
      ↓
Permission Check
      ↓
Input Validation
      ↓
Business Logic
      ↓
Data Access
```

### Implemented

* JWT authentication
* Role-Based Access Control
* Permission systems
* OTP authentication
* Email verification
* Password reset with email OTP
* Request validation

---

# 🚀 Production & Infrastructure

I also like the part of development that happens after the code is finished.

```text
                    Internet
                       │
                       ▼
              ┌─────────────────┐
              │    Cloudflare   │
              │   DNS / SSL     │
              └────────┬────────┘
                       ↓
              ┌─────────────────┐
              │      Nginx      │
              │ Reverse Proxy   │
              └────────┬────────┘
                       ↓
              ┌─────────────────┐
              │     Docker      │
              │ Docker Compose  │
              └────────┬────────┘
                       ↓
              ┌─────────────────┐
              │    Backend API  │
              └───────┬─────────┘
                      / \
                     /   \
                    ↓     ↓
              Database   Storage
              PostgreSQL MongoDB
              Redis      MinIO
```

### Infrastructure

**Docker** · **Docker Compose** · **Linux** · **Nginx** · **Cloudflare** · **MinIO**

---

# 📊 Observability

A production system should tell you what is happening.

```text
Application
     │
     ├──────────► Logs ───────► Loki
     │
     ├──────────► Metrics ────► Prometheus
     │
     └──────────► Dashboard ──► Grafana
                              │
                              ▼
                         Investigation
```

I use observability to answer questions like:

* Which endpoint is slow?
* Is the database the bottleneck?
* Is CPU or memory increasing?
* Are errors increasing?
* Is a container unhealthy?
* Did a deployment introduce a regression?

---

# 🧩 Selected Projects

## 01 · Depot Assessment & Tracking System

### `Backend · Performance · Security · Production`

A business assessment and tracking platform involving API development, evaluation workflows, authentication, reporting and production infrastructure.

### 🔍 The interesting part

This wasn't just CRUD.

I worked on investigating **why APIs were slow**, then traced the problem through the application and database.

```text
Slow API
   ↓
Measure request time
   ↓
Inspect database queries
   ↓
Check query patterns
   ↓
Add / improve indexes
   ↓
Reduce unnecessary data
   ↓
Optimize aggregation
   ↓
Measure again
```

### Built / improved

* REST APIs
* Assessment workflows
* Evaluation management
* Filtering and searching
* Dashboard and KPI queries
* Database indexes
* Aggregation queries
* JWT authentication
* RBAC / permissions
* OTP verification
* Password reset
* Docker deployment
* Production monitoring

**Focus:** `Performance · Database · Security · Deployment`

---

# 🛒 02 · E-Commerce System

### `Spring Boot · PostgreSQL · Redis`

Backend system for an online store with products, variants, sizes and inventory.

```text
Product
   │
   ├── Variant
   │      └── Inventory
   │
   └── Images
```

### Features

* Product management
* Product variants
* Size management
* Inventory tracking
* Shopping cart
* Cart items
* Authentication
* JWT
* Product image management

**Stack**

`Java` · `Spring Boot` · `Spring Security` · `PostgreSQL` · `Redis` · `JWT` · `Cloudinary`

---

# 📋 03 · Task Management System

### `Spring Boot · PostgreSQL · React Native`

A task and workforce management platform.

```text
Organization
      ↓
Department
      ↓
Employee
      ↓
Task
      ↓
Subtask
```

### Features

* Task management
* Subtasks
* Role-based access
* KPI tracking
* Approval workflows
* Employee management
* Department management
* Mobile client

**Stack**

`Java` · `Spring Boot` · `PostgreSQL` · `React Native` · `Expo`

---

# 🌐 04 · CMS / Landing Page Platform

### `Node.js · MongoDB · Next.js`

A CMS platform with a public website and administrative dashboard.

```text
Admin
  ↓
CMS
  ↓
MongoDB
  ↓
Public Website
```

### Features

* Hero banners
* Community posts
* Media management
* Awards
* Content publishing
* Admin dashboard
* Analytics charts

**Stack**

`Node.js` · `Express.js` · `MongoDB` · `Mongoose` · `Next.js` · `Tailwind CSS` · `Recharts`

---

# 🛠️ Tech Stack

### Languages

![Java](https://skillicons.dev/icons?i=java)
![JavaScript](https://skillicons.dev/icons?i=js)

`Java` · `JavaScript`

### Backend

![Spring](https://skillicons.dev/icons?i=spring)
![Node.js](https://skillicons.dev/icons?i=nodejs)
![Express](https://skillicons.dev/icons?i=express)

`Spring Boot` · `Spring Security` · `Node.js` · `Express.js` · `REST` · `JWT`

### Frontend

![React](https://skillicons.dev/icons?i=react)
![Next.js](https://skillicons.dev/icons?i=nextjs)
![Tailwind](https://skillicons.dev/icons?i=tailwind)

`React` · `Next.js` · `React Native` · `Expo` · `Tailwind CSS`

### Database

![PostgreSQL](https://skillicons.dev/icons?i=postgres)
![MongoDB](https://skillicons.dev/icons?i=mongodb)
![Redis](https://skillicons.dev/icons?i=redis)

`PostgreSQL` · `MongoDB` · `Redis` · `Prisma` · `Mongoose`

### Infrastructure

![Docker](https://skillicons.dev/icons?i=docker)
![Linux](https://skillicons.dev/icons?i=linux)
![Nginx](https://skillicons.dev/icons?i=nginx)
![Cloudflare](https://skillicons.dev/icons?i=cloudflare)

`Docker` · `Docker Compose` · `Linux` · `Nginx` · `Cloudflare` · `MinIO`

### Observability

![Grafana](https://skillicons.dev/icons?i=grafana)
![Prometheus](https://skillicons.dev/icons?i=prometheus)

`Grafana` · `Prometheus` · `Loki` · `Node Exporter` · `Netdata`

---

# 🧭 My Engineering Principles

### 01 — Measure before optimizing

> A slow endpoint is a hypothesis until I measure it.

### 02 — Follow the data

> Logs, metrics and query plans are more useful than guesses.

### 03 — Design security early

> Authentication and authorization should be part of the architecture.

### 04 — Think about production

> Deployment, monitoring and failure handling influence how I build the application.

### 05 — Keep systems understandable

> Simple, readable code is easier to debug, scale and maintain.

---

# 📚 Currently Learning

```text
Database Engineering
        ↓
Query Plans · Indexing · Transactions
        ↓
System Design
        ↓
Scalability · Caching · Concurrency
        ↓
Production Engineering
        ↓
CI/CD · Observability · Distributed Tracing
```

Currently focusing on:

* Reading PostgreSQL query plans more fluently
* Database performance tuning
* System design and scalability
* Concurrency and transaction design
* CI/CD automation
* Distributed tracing
* Production observability

---

# 📈 GitHub Activity

<p align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=loemratana&show_icons=true&hide_border=true&theme=transparent&title_color=58a6ff&icon_color=58a6ff&text_color=8b949e" />
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=loemratana&layout=compact&langs_count=6&hide_border=true&theme=transparent&title_color=58a6ff&text_color=8b949e" />
</p>

---

# 💬 Let's Talk

I'm

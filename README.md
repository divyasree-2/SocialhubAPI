# 🚀 SocialhubAPI

A scalable backend microservice built using Java 17 and Spring Boot designed to handle high-volume social media interactions with Redis-powered concurrency controls, virality scoring, cooldown enforcement, and distributed notification throttling.

---

## 🔥 Key Engineering Highlights

- Redis-powered concurrency protection
- Real-time virality scoring engine
- Distributed cooldown enforcement using Redis TTL
- Thread-safe concurrent request handling
- Notification throttling and batching
- Cloud-native PostgreSQL with NeonDB
- Distributed state management using Upstash Redis

---

## ✨ Features

- Create posts and comments using REST APIs
- Real-time virality scoring using Redis
- Atomic concurrency protection with Redis counters
- Bot interaction guardrails and cooldown enforcement
- Thread-safe handling of concurrent requests
- Notification throttling using Redis TTL
- Scheduled notification batching using Spring Scheduler
- PostgreSQL persistence with NeonDB
- Distributed state management using Upstash Redis

---

## 🛠 Tech Stack

- Java 17
- Spring Boot 3.x
- PostgreSQL (NeonDB)
- Upstash Redis
- Spring Data JPA
- Spring Data Redis
- Maven
- REST APIs

---

## 🏗 Architecture Flow

```text
Client Requests
       ↓
Spring Boot REST APIs
       ↓
Redis Layer
(Counters • Cooldowns • Virality • Throttling)
       ↓
Neon PostgreSQL
```

---

## 📁 Project Structure

```text
src/
├── controller/
├── service/
├── repository/
├── config/
├── scheduler/
├── redis/
├── dto/
├── entity/
└── exception/
```

---

## ⚡ Engineering Challenges Solved

### Concurrency Protection

- Prevented race conditions using Redis atomic counters
- Protected APIs during concurrent bot interactions
- Enforced interaction limits with distributed Redis locks

### Horizontal Scaling Guardrails

- Used Redis counters to enforce maximum bot reply limits
- Reduced uncontrolled concurrent interactions during traffic spikes

### Cooldown Enforcement

- Implemented Redis TTL-based cooldown keys
- Prevented repetitive bot-human interaction spam

### Real-Time Virality Scoring

- Designed a Redis-powered scoring engine
- Reduced repeated PostgreSQL writes using in-memory interaction scoring
- Enabled instant score updates without database bottlenecks

---

## ⚡ Why Redis?

Redis was used beyond traditional caching to handle:

- Atomic concurrency control
- Distributed cooldown enforcement
- Notification throttling
- Real-time virality scoring
- Interaction guardrails using counters and TTL locks

This improved response efficiency and reduced database overhead during concurrent interactions.

---

## ☁️ Cloud Services Used

### NeonDB

- Used Neon serverless PostgreSQL for scalable cloud-hosted relational database management

### Upstash Redis

- Used Upstash Redis for:
  - Atomic counters
  - Cooldown locks
  - Virality scoring
  - Notification throttling
  - Distributed state management

---

## 🧪 Testing

- API testing using Postman
- Concurrent request testing for Redis atomic operations
- Validation testing for REST endpoints
- Manual stress testing for bot interaction guardrails

---

## 📈 Future Improvements

- Swagger/OpenAPI documentation
- Docker containerization
- CI/CD pipeline integration
- Automated API testing with JUnit
- Kafka-based event streaming
- AI-powered spam detection
- Real-time WebSocket notifications

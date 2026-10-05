# Hi, I'm Revanth Yepuri 👋

Software Engineer building backend systems that stay correct under load

M.S. Computer Science student at George Mason University. I build backend and full-stack services in **Java** and **Python**, focused on concurrency control, idempotent APIs, and event-driven messaging, and I ship tested, containerized code with Testcontainers, Docker, and GitHub Actions. Open to backend and software engineering roles starting early 2027.

- 🔭 Recently built [SeatLock](https://github.com/yepurirevanth06/seatlock), a seat booking platform with zero double bookings under 500 concurrent users
- 🧬 Building the [Clinical Trial Eligibility Matching Platform](https://github.com/yepurirevanth06/clinical-trial-matcher), a FastAPI service with explainable eligibility logic
- ☁️ AWS Certified Developer (Associate) and AWS Certified Cloud Practitioner
- 📫 Reach me: yepurirevanth06@gmail.com · [GitHub](https://github.com/yepurirevanth06) · [LinkedIn](https://linkedin.com/in/revanth-yepuri) · +1 (571) 604-9589

---

## 🛠️ Tech Stack

**Languages**
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=c%2B%2B&logoColor=white)

**Backend**
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat&logo=springsecurity&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat)
![Celery](https://img.shields.io/badge/Celery-37814A?style=flat&logo=celery&logoColor=white)
![WebSockets](https://img.shields.io/badge/WebSockets-010101?style=flat&logo=socketdotio&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat&logo=jsonwebtokens&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)

**Databases & Messaging**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=flat&logo=rabbitmq&logoColor=white)
![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=flat&logo=flyway&logoColor=white)
![Alembic](https://img.shields.io/badge/Alembic-6BA81E?style=flat)

**Testing & DevOps**
![JUnit 5](https://img.shields.io/badge/JUnit_5-25A162?style=flat&logo=junit5&logoColor=white)
![Testcontainers](https://img.shields.io/badge/Testcontainers-291A3F?style=flat)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat&logo=pytest&logoColor=white)
![k6](https://img.shields.io/badge/k6-7D64FF?style=flat&logo=k6&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![AWS](https://img.shields.io/badge/AWS_(EC2,_S3)-232F3E?style=flat&logo=amazonaws&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)

**ML & Data**
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![LightGBM](https://img.shields.io/badge/LightGBM-2E7D32?style=flat)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)

**Concepts:** concurrency control · row-level locking · idempotency · transactional outbox · caching · query optimization

---

## 📌 Featured Projects

### [SeatLock: Campus Event Seat Booking Platform](https://github.com/yepurirevanth06/seatlock)
`Java` `Spring Boot` `PostgreSQL` `Redis` `RabbitMQ` `React` `TypeScript` `Docker` `k6`

Full-stack booking platform with 11 REST endpoints, a live React/TypeScript seat map, JWT auth, and role-based access. Delivered **zero double bookings** as 500 concurrent users rushed a 100-seat event (100/100 sold, 1,206 contested holds rejected) using atomic Redis Lua holds and PostgreSQL row locks taken in id order to avoid deadlocks. The same Lua script enforces a 6-seat hold cap per user (20 simultaneous requests yield 6 holds). Replaced 3-second polling with WebSocket (STOMP) push, including hold expirations caught via Redis keyspace events. Checkout is retry-safe with idempotency keys (10 concurrent retries create exactly 1 booking), and confirmation emails go through a transactional outbox with RabbitMQ, 3 retries, and a dead-letter queue. Held a **0% error rate across 1,910 requests at 330ms p95**, verified by 28 Testcontainers integration tests in GitHub Actions CI.

### [Clinical Trial Eligibility Matching Platform](https://github.com/yepurirevanth06/clinical-trial-matcher)
`Python` `FastAPI` `PostgreSQL` `SQLAlchemy` `Alembic` `Redis` `Celery` `Docker`

Async FastAPI service with JWT auth and role-based access that matches patients to trials using eligibility criteria modeled as AND/OR/NOT trees, with a per-clause explanation of every verdict. Three-valued logic (pass/fail/unknown) flags missing lab values for measurement instead of excluding the patient. Made trial search **26x faster** (9.5ms to 0.36ms) with a generated Postgres tsvector column and GIN index, and served repeat searches in 2.5ms from a Redis cache invalidated by one INCR. A regex parser structured eligibility text for 39.8% of 1,827 synced ClinicalTrials.gov trials, generating **724 eligibility trees from 3** hand-authored ones. 71 tests run against real Alembic migrations in GitHub Actions with ruff, mypy, and pytest.

### [ML-Powered Network Intrusion Detection](https://github.com/yepurirevanth06/network-intrusion-detection-ml) · [Live demo](https://network-intrusion-detection-ml.onrender.com)
`Python` `Flask` `scikit-learn` `LightGBM` `pytest` `Docker` `GitHub Actions` `Render`

LightGBM traffic classifier trained on 692K labeled CICIDS2017 flows with 78 features after cleaning 2,500+ missing and infinite values, reaching **99.98% F1** on held-out DoS/DDoS traffic. Served as a Flask REST API, containerized with Docker, and deployed on Render with a CSV-upload dashboard returning per-flow predictions and confidence scores. CI pipeline runs an 8-test pytest suite plus automated Docker builds and post-deploy health checks.

---

## 💼 Experience
**Cyber Security Intern**, AICTE, Hyderabad, India (Oct 2021 - Dec 2021)

Assessed vulnerabilities across 50+ endpoints using Nmap and Wireshark, automated log monitoring and security workflows with Python and Bash on Linux, and validated 100K+ record datasets with Python and SQL for threat analysis reporting.

## 🎓 Education
**George Mason University** - M.S. Computer Science, GPA 3.89 (Jan 2025 - Dec 2026)

Coursework: Analysis of Algorithms, Database Management Systems, Computer Systems & Systems Programming, Software Architecture & Design, Component-Based Software Development

**BV Raju Institute of Technology** - B.Tech Computer Science (Aug 2020 - Jun 2024)

Coursework: Data Structures & Algorithms, Operating Systems, Computer Networks, Database Management Systems

## 📜 Certifications
AWS Certified Developer - Associate 

AWS Certified Cloud Practitioner

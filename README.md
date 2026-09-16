# Hi, I'm Revanth Yepuri 👋

Backend & Data Engineer | MS Computer Science @ George Mason University (Dec 2026, GPA 3.89)

I build and deploy production Python services: REST APIs, containerized ML inference, and data pipelines. Currently looking for backend/data engineering roles starting early 2027.

- 🔭 Building [Clinical Trial Eligibility Matching Platform](https://github.com/yepurirevanth06/clinical-trial-matcher), a FastAPI service matching patients to trials with explainable eligibility logic
- 📊 Also into data pipelines and analytics: PostgreSQL, ETL, Tableau
- 🌱 Sharpening backend fundamentals: async APIs, caching, database performance
- 📫 Reach me: yepurirevanth06@gmail.com | [LinkedIn](https://linkedin.com/in/revanth-yepuri)

---

## 🛠️ Tech Stack

**Languages**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=c%2B%2B&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

**Backend**
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=flat&logo=celery&logoColor=white)

**Data & ML**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=flat&logo=tableau&logoColor=white)

**DevOps**
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonaws&logoColor=white)

---

## 📌 Featured Projects

### [Clinical Trial Eligibility Matching Platform](https://github.com/yepurirevanth06/clinical-trial-matcher)
Async FastAPI service with JWT auth matching patient records against eligibility criteria modeled as an AND/OR/NOT tree, returning a per-clause explanation of every verdict. Cut trial search latency from 9.5ms to 0.36ms with a Postgres GIN index, then to 2.5ms with Redis caching. Parses unstructured ClinicalTrials.gov text into structured criteria, generating 724 eligibility trees from 3 hand-authored examples. 71 tests running in CI via ruff, mypy, and pytest.

### [ML-Powered Network Intrusion Detection](https://github.com/yepurirevanth06/network-intrusion-detection-ml) · [Live demo](https://network-intrusion-detection-ml.onrender.com)
Random Forest and LightGBM classifiers trained on 692K labeled CICIDS2017 flows, reaching 99.98% F1 on DoS/DDoS detection. Served as a Flask REST API, containerized with Docker, deployed on Render with a CSV-upload dashboard. CI pipeline runs an 8-test pytest suite plus automated Docker builds and health checks.

### [Brazilian E-Commerce Analytics Pipeline](https://github.com/yepurirevanth06/olist-ecommerce-analytics)
9-table normalized PostgreSQL schema loading 1.55M rows across ~100K orders. 6 reusable SQL views analyzing R$15.4M in delivered orders. Traced customer dissatisfaction to delivery latency (2.57 vs 4.29 stars) using Tableau.

---

## 🎓 Education
**George Mason University** — M.S. Computer Science, GPA 3.89 (Jan 2025 – Dec 2026)
**BV Raju Institute of Technology** — B.Tech Computer Science (Aug 2020 – Jun 2024)

## 📜 Certifications
AWS Certified Cloud Practitioner · AICTE Cyber Security

### What this system does (Project goal):
Accepts an email (subject, body, sender metadata)

Predicts:

✅ Phishing / Spam / Legit

🎯 Risk score (0–100)

Explains why it was flagged (important for security products)

Exposes everything via API

Has a dashboard frontend

Is containerized, CI/CD-ready, and cloud-deployed

This is exactly the type of ML used in real email security vendors.

🔐 ML Problems You’ll Learn (Gradually)
We’ll increase difficulty step by step:

Binary Classification

Phishing vs Legit

Multi-class Classification

Spam / Phishing / Legit

NLP (Text ML)

TF-IDF → classical ML

Then transformers (optional, advanced)

Model Explainability

SHAP / feature importance (critical for security)

Concept Drift

Emails change → model monitoring

### High-level architecture
┌────────────┐
│  Frontend  │  React + Charts
└─────┬──────┘
      │ HTTPS
┌─────▼──────┐
│   API      │  FastAPI
│            │
│ /predict   │
│ /feedback  │
│ /metrics   │
└─────┬──────┘
      │
┌─────▼──────────┐
│  ML Service    │
│  Scikit-learn  │
│  / PyTorch     │
└─────┬──────────┘
      │
┌─────▼──────────┐
│  Data Store    │
│  Postgres      │
│  + S3/MinIO    │
└────────────────┘
### Tech stack (Python, FastAPI, ML, Docker)
ML & Backend
Python 3.11

pandas, scikit-learn

FastAPI

MLflow (model tracking)

SHAP (explainability)

Frontend
React

Tailwind

Chart.js

DevOps / Prod
Docker (multi-stage builds)

GitHub Actions (CI/CD)

Prometheus + Grafana

Nginx

Cloud: AWS / DO / GCP


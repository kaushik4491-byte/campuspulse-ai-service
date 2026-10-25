# campuspulse-ai-service
AI/ML &amp; Operational Insights Microservice

[![FastAPI](https://img.shields.io/badge/FastAPI-0.110.0-009688.svg)](https://fastapi.tiangolo.com/)
[![Python](https://img.shields.io/badge/Python-3.12-3776AB.svg)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.4.0-F7931E.svg)](https://scikit-learn.org/)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED.svg)](https://www.docker.com/)

## 📌 Module Overview
The **AI/ML & Operational Insights** microservice provides text processing, category prediction, and backlog trend forecasting for CampusPulse. Built using FastAPI and scikit-learn, it uses an NLTK text normalization pipeline combined with a Linear SVM classifier to categorize complaint text in real-time, falling back defensively when prediction confidence drops below configured thresholds.

---

## 🏗️ Repository Architecture & Directory Structure

```text
campuspulse-ai-service/
├── app/
│   ├── api/                # routes.py (predict, insights, health)
│   ├── core/               # config.py, logging.py
│   ├── models/             # svm_model.joblib, tfidf_vectorizer.joblib
│   ├── schemas/            # pydantic_models.py (PredictionRequest/Response)
│   └── services/           # text_cleaner.py, predictor.py, trend_forecaster.py
├── tests/                  # test_pipeline.py, test_api.py (Pytest suite)
├── Dockerfile
├── requirements.txt
└── README.md

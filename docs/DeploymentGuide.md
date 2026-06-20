# Deployment Guide

## Overview

This guide explains how to deploy KnowledgeForge AI locally and in production environments.

---

## Prerequisites

* Python 3.10+
* Git
* Virtual Environment
* ChromaDB
* Llama 2 Model
* Django

---

## Clone Repository

```bash
git clone https://github.com/Ashrith-3108/KnowledgeForage-AI.git

cd KnowledgeForage-AI
```

---

## Create Virtual Environment

```bash
python -m venv venv
```

### Windows

```bash
venv\Scripts\activate
```

### Linux / macOS

```bash
source venv/bin/activate
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Database Migration

```bash
python manage.py migrate
```

---

## Start Development Server

```bash
python manage.py runserver
```

Application URL:

```text
http://127.0.0.1:8000/
```

---

## Production Deployment

### Docker

Recommended for production deployment.

```bash
docker build -t knowledgeforge-ai .
docker run -p 8000:8000 knowledgeforge-ai
```

### Render

1. Connect GitHub repository
2. Select Python environment
3. Install requirements
4. Configure environment variables
5. Deploy

### AWS EC2

Recommended configuration:

* Ubuntu 22.04
* Nginx
* Gunicorn
* Python 3.10+

Deployment Flow:

```text
Internet
   ↓
Nginx
   ↓
Gunicorn
   ↓
Django
   ↓
ChromaDB
```

---

## Monitoring

Recommended tools:

* Prometheus
* Grafana
* AWS CloudWatch

---

## Future Deployment Enhancements

* Kubernetes
* CI/CD Pipelines
* Auto Scaling
* Managed Vector Databases
* Multi-Region Deployments


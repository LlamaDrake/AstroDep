# 🛰️ AstroDep

**AstroDep** is a scalable, on-demand data depersonalization pipeline designed for machine learning compliance. Built with **Apache Spark on AWS EMR**, it processes structured datasets through customizable sanitization techniques such as **regex masking**, **tokenization**, and **field-level encryption**.

AstroDep is accessible via **self-service APIs**, making it easy for data scientists to run privacy-safe transformations on demand—enabling agile development while staying audit-compliant.

## 📌 Features

- 🔐 **PII Detection & Redaction**:
  - Regex-based pattern matching for emails, SSNs, phone numbers
  - Field-level encryption with key rotation policies
  - Tokenization engine with reversible and irreversible options

- ⚡ **On-Demand Scalability**:
  - Spark jobs dynamically scaled via AWS EMR
  - Triggered by REST API or scheduled via EventBridge

- 📦 **ML-Ready Outputs**:
  - Outputs pre-cleaned datasets to S3
  - Schema-preserving to avoid downstream retraining

## 🧰 Tech Stack

- **Compute**: Apache Spark on AWS EMR
- **APIs**: Python (Flask), API Gateway
- **Security**: KMS encryption, IAM roles, audit logs
- **Orchestration**: EventBridge, Step Functions

## 🚀 Getting Started

```bash
git clone https://github.com/your-username/astrodep.git
cd astrodep
./scripts/bootstrap_emr.sh --region us-east-1

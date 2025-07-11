# Databricks Bridge IoT Monitoring System

Real-time IoT sensor data pipeline for bridge structural monitoring using Databricks, Delta Lake, and AWS.

![Architecture](https://img.shields.io/badge/Architecture-Databricks%20%2B%20AWS-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Python](https://img.shields.io/badge/Python-3.9%2B-brightgreen)

## 🏗️ Architecture Overview

- **Data Sources**: Temperature, Vibration, and Tilt sensors across bridge infrastructure
- **Ingestion**: Real-time streaming data generators
- **Processing**: Databricks with Delta Live Tables (Bronze → Silver → Gold)
- **Storage**: AWS S3 + Delta Lake format
- **Infrastructure**: Terraform for IaC
- **CI/CD**: GitHub Actions for automated deployment
- **Monitoring**: Real-time alerts and data quality checks

## 🚀 Quick Start

### Prerequisites
- AWS Account with appropriate IAM permissions
- Databricks Premium workspace
- Terraform >= 1.0
- Python 3.9+
- Git

### Local Setup
```bash
# Clone and setup
git clone https://github.com/challasvasulu04/databricks-bridge-iot-monitoring.git
cd databricks-bridge-iot-monitoring

# Python environment
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
pip install -r requirements.txt

# Environment configuration
cp .env.example .env
# Edit .env with your AWS and Databricks credentials

# Install pre-commit hooks
pre-commit install
# MNIST_Data – GCP ML Pipeline for Digit Recognition

This project implements a scalable machine learning pipeline to classify handwritten digits from the MNIST dataset using Google Cloud Platform services.

## 🚀 What This Project Does

- Real-time + batch digit inference using TensorFlow
- Hybrid ETL pipeline (Apache Beam via Dataflow + Pub/Sub + BigQuery)
- Containerized inference via Cloud Run & Kubernetes
- Optimized latency and throughput for large-scale inference

##  Tech Stack

- **Languages**: Python
- **ML Framework**: TensorFlow
- **Pipeline**: Apache Beam (Dataflow), BigQuery, Pub/Sub
- **Infra**: Kubernetes, Docker, Cloud Run
- **DevOps**: GitHub Actions, GCP IAM

##  Generative AI Involvement

This project includes experimentation with generative AI capabilities for:
- Code review and debugging (via GitHub Copilot + GPT-4)
- Auto-generating data augmentation code
- Synthetic data creation for edge-case enhancement

> Used GPT-based tools to accelerate iteration speed and ensure best practices in security and performance.

##  Files Overview

| File | Purpose |
|------|---------|
| `DataFlow.py` | Main ETL pipeline for streaming + batch |
| `Detection.py` | Inference logic for digit classification |
| `Dockerfile` | Container spec for inference service |

##  How to Run
# 1. Clone the repository
```git clone https://github.com/SuryaTeja2002-design/MNIST_Data.git```
```cd MNIST_Data```

# 2. Deploy the Dataflow ETL job
```python DataFlow.py```

# 3. Build and run the inference container locally
```docker build -t mnist-detector .```
```docker run -p 8080:8080 mnist-detector```

# 4. Send a test inference request
```curl -X POST -d @sample_image.json http://localhost:8080/infer```



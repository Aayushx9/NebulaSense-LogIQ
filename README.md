# NebulaSense LogIQ 
Cloud‑Native Anomaly Intelligence Engine
NebulaSense LogIQ is a next‑generation anomaly intelligence platform designed for modern, distributed, cloud‑native systems. It combines real‑time log streaming, deep learning–based anomaly detection, and an interactive observability dashboard into a single, cohesive system.
Built for developers, SREs, data scientists, and cloud engineers, NebulaSense LogIQ detects unusual behavior across microservices, API gateways, containers, and distributed workloads, before failures cascade.

This repository contains the full end‑to‑end platform:
- LogIQ Core - TensorFlow‑powered sequence anomaly model
- LogIQ Score - hybrid anomaly metric combining reconstruction error, embedding drift, and temporal deviation
- LogIQ Stream - real‑time log ingestion and streaming pipeline
- LogIQ View - interactive Streamlit + Plotly dashboard for cloud observability
- LogIQ API - FastAPI service for prediction, health checks, and service‑level insights
- LogIQ Sim - synthetic microservice environment generating realistic cloud logs with injected anomalies

### Key Features
- LogIQ Core - Deep Learning Anomaly Engine
Learns normal system behavior using sequence modeling and flags deviations in real time.
- LogIQ Score - Unified Anomaly Metric
A custom anomaly index combining multiple signals into one interpretable score.
- LogIQ Stream - Real‑Time Log Ingestion
Processes logs from simulated microservices, files, APIs, and optional streaming sources.
- LogIQ Sim - Synthetic Microservice Environment
Generates realistic logs, latency spikes, cascading failures, and injected anomalies for demos and testing.
- LogIQ View - Interactive Observability Dashboard
Visualizes anomalies, service health, embeddings, and latency patterns through a clean, intuitive UI.
- LogIQ API - FastAPI Service Layer
Provides REST endpoints for anomaly prediction, health checks, and service‑level insights.

### Repository Structure
```text
nebula-sense-logiq/
│
├── logiq_core/ # ML engine
├── logiq_stream/ # streaming pipeline
├── logiq_view/  # dashboard
├── logiq_api/ # FastAPI service
├── logiq_sim/ # microservice simulator
├── docs/ # architecture, scoring, roadmap
├── examples/ # notebooks + demos
├── data/ # sample logs
└── deployment/ # Docker + Kubernetes configs
```
### Tech Stack
- Python
- TensorFlow
- FastAPI
- Streamlit
- Plotly
- NumPy / Pandas
- Docker
- Kubernetes (optional)

### How It Works
NebulaSense LogIQ processes logs through a modular, cloud‑native anomaly intelligence pipeline:

1. **LogIQ Sim** generates realistic microservice logs with injected anomalies.
2. **LogIQ Stream** ingests logs in real time and batches them for processing.
3. **LogIQ Core** performs sequence modeling and computes the LogIQ Score.
4. **LogIQ API** exposes predictions and service‑level insights via REST endpoints.
5. **LogIQ View** visualizes anomalies, embeddings, and service health.

#### System Flow
logs → stream → model → score → API → dashboard
``` text
    ┌──────────────┐
    │  LogIQ Sim   │
    └──────┬───────┘
           │ logs
           ▼
    ┌──────────────┐
    │ LogIQ Stream │
    └──────┬───────┘
           │ batches
           ▼
    ┌──────────────┐
    │  LogIQ Core  │
    └──────┬───────┘
           │ scores
           ▼
    ┌──────────────┐
    │  LogIQ API   │
    └──────┬───────┘
           │ JSON
           ▼
    ┌──────────────┐
    │ LogIQ View   │
    └──────────────┘
```
### Screenshots / Demo

> Coming soon:  
> - Anomaly timeline  
> - Service dependency graph  
> - Embedding visualization  
> - Real‑time anomaly spikes

### Installation
(You can fill this in once your environment is finalized.)

### Quick Start
(Also added once your entry points are ready.)

### Deployment

NebulaSense LogIQ supports multiple deployment modes:

#### **Local Development**
- Run the dashboard with Streamlit  
- Run the API with FastAPI  
- Run the simulator to generate logs  

#### **Docker**
Dockerfiles for API, dashboard, and core components are available under `deployment/docker/`.

#### **Kubernetes**
K8s manifests for scalable deployment are available under `deployment/kubernetes/`.

#### **Cloud Providers**
Guides for AWS, GCP, and Azure are included in `deployment/cloud/`.

### License
Apache 2.0

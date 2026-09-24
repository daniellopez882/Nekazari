# Nekazari 🌱

**Plataforma Agrícola Inteligente basada en FIWARE**
An intelligent agriculture platform combining real-time geospatial visualization, IoT data ingestion, and automated risk analysis to support modern farming operations.

🔗 **Live:** [https://nekazari.robotika.cloud/](https://nekazari.robotika.cloud/)

---

## Overview

Nekazari is a smart agriculture platform built on the [FIWARE](https://www.fiware.org/) ecosystem. It brings together 3D geospatial visualization, sensor and weather data ingestion, and automated risk analysis into a single interface, giving users actionable insight into crop and field conditions.

## Architecture

The platform is composed of a modern frontend paired with a microservices-based backend, containerized and orchestrated for scalable deployment.

### Frontend

- **React + Vite** — core application framework and build tooling
- **CesiumJS** — 3D geospatial visualization of fields, terrain, and sensor locations
- **Tailwind CSS** — utility-first styling
- **UI Component Library** — shared, reusable interface components
- **SDK** — client-side toolkit for integrating with the Nekazari platform
- **Module Marketplace** — extensible system for adding new platform capabilities

### Backend

- **Python (Flask / FastAPI)** — microservices architecture
- **API Gateway** — centralized entry point for all backend services
- **JWT Validation** — secure, token-based authentication across services
- **Rate Limiting** — API abuse protection and traffic control
- **Entity Management Service** — core FIWARE-based entity handling
- **Weather Ingestion Workers** — automated pipelines pulling and processing external weather data
- **Risk-Analysis Services** — computes agricultural/environmental risk indicators from ingested data
- **S3 Uploads** — object storage integration for file and media handling
- **TimescaleDB** — time-series database for sensor, weather, and historical data

### Infrastructure

- **Docker Compose** — service orchestration for local/dev environments
- **Kubernetes** — production container orchestration and scaling

## Tech Stack

| Layer | Technologies |
|---|---|
| Frontend | React, Vite, CesiumJS, Tailwind CSS |
| Backend | Python, Flask/FastAPI, JWT, REST API Gateway |
| Data | TimescaleDB, S3 |
| Infrastructure | Docker Compose, Kubernetes |

## System Components

- **API Gateway** — routes and secures all incoming requests to backend microservices, enforcing JWT validation and rate limiting.
- **Entity Management** — handles creation, updates, and queries of FIWARE-based data entities (fields, sensors, crops, etc.).
- **Weather Ingestion Workers** — background processes that continuously pull external weather data and feed it into the platform's data layer.
- **Risk-Analysis Services** — processes ingested sensor and weather data to generate agricultural risk indicators.
- **TimescaleDB** — stores and serves time-series data for historical analysis and trend visualization.
- **S3 Storage** — manages uploaded files and media assets used across the platform.
- **Module Marketplace** — allows extension of platform functionality through pluggable modules.

## Contributors

- **Daniel Lopez** ([@daniellopez882](https://github.com/daniellopez882)) — Backend Systems Engineer. Designed and built the backend architecture, including the API gateway, JWT-based authentication and rate limiting, entity management and weather ingestion microservices, risk-analysis services, S3 upload integration, and the TimescaleDB data layer.


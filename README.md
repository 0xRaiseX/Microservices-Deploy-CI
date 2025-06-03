# FastAPI Microservice with GHCR Deployment

A simple FastAPI application packaged as a Docker container and deployed to GitHub Container Registry (GHCR) for testing microservice functionality. This project provides a minimal, scalable REST API with automated build and deployment workflows, ideal for quick prototyping and testing in a containerized environment.

## Features

- FastAPI-based REST API with sample endpoints
- Dockerized application for consistent deployment
- Automated build and push to GHCR using GitHub Actions
- Lightweight and minimal dependencies

## Prerequisites

- Python 3.8+
- Docker
- GitHub account with access to GHCR

## Installation

Clone the repository:

```Bash
git clone https://github.com/0xRaiseX/jubilant-lamp.git
cd jubilant-lamp
```

## Install dependencies:

```Bash
pip install flask
```


## Build the Docker image:

```Bash
docker build -t fastapi-microservice .
```

## Run using Docker:
```Bash
docker run -p 8000:5000 fastapi-microservice
```

## Deployment to GHCR
1. Configure GitHub Secrets for GHCR access (e.g., CR_PAT for Personal Access Token).
2. Push changes to the repository to trigger the GitHub Actions workflow.
3. Pull the image from GHCR:
```Bash
docker pull ghcr.io/your-username/fastapi-microservice:latest
```

## Project Structure
```
├── app/main.py          # FastAPI application code
├── Dockerfile           # Docker configuration
├── /manifests           # Manifests to K8s
├── .github/workflows    # GitHub Actions for CI/CD
└── README.md            # Project documentation
```
## License

This project is licensed under the MIT License. See the LICENSE file for details.

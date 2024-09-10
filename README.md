# Kubernetes Mongo Express Deployment

This project contains a Kubernetes deployment of Mongo Express, a web-based admin interface for MongoDB. The deployment utilizes Kubernetes Secrets to manage MongoDB credentials and a ConfigMap to store the MongoDB server URL.


## Features

- Deploys Mongo Express on Kubernetes for managing MongoDB instances.
- Securely manages MongoDB admin credentials using Kubernetes Secrets.
- Uses a Kubernetes ConfigMap to store the MongoDB server address.
- Easily scalable by adjusting the replica count in the deployment YAML.


## Tech Stack

- **Kubernetes**: Container orchestration platform
- **MongoDB**: NoSQL database
- **Mongo Express**: Web-based MongoDB admin interface
- **Docker**: Container runtime
- **YAML**: Kubernetes configuration language

## Prerequisites

- Kubernetes cluster up and running(on Minikube).
- MongoDB instance deployed (can be local or another Kubernetes deployment).
- kubectl configured to interact with your Kubernetes cluster.

## Kubernetes Resources Overview

- **Deployment**: The deployment YAML defines the Mongo Express container, including environment variables for MongoDB credentials and the server URL.
- **Secrets**: Kubernetes Secrets manage the MongoDB root username and password securely.
- **ConfigMap**: Stores the MongoDB server URL.

## Environment Variables

- `ME_CONFIG_MONGODB_ADMINUSERNAME`: MongoDB admin username, fetched from the Kubernetes Secret.
- `ME_CONFIG_MONGODB_ADMINPASSWORD`: MongoDB admin password, fetched from the Kubernetes Secret.
- `ME_CONFIG_MONGODB_SERVER`: MongoDB server URL, fetched from the ConfigMap.


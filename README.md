# Mario in GKE

## Introduction
This repository contains the necessary configurations and code to deploy a "Mario" application on Google Kubernetes Engine (GKE). The project aims to demonstrate the use of Kubernetes for orchestrating containerized applications.

## Prerequisites
Before you begin, ensure you have the following prerequisites installed and set up:
- Google Cloud SDK
- Kubernetes command-line tool (kubectl)
- Docker
- Access to a Google Cloud Platform (GCP) account with permissions to manage GKE.

## Installation
1. **Set up Google Cloud SDK**: Make sure you have configured the Google Cloud SDK and authenticated your GCP account.
   ```bash
   gcloud auth login
   gcloud config set project [YOUR_PROJECT_ID]
2. Create a GKE cluster:
   ````bash
   gcloud container clusters create [CLUSTER_NAME] --num-nodes=3 --zone=[YOUR_ZONE]
3. Configure kubectl to use your cluster:

   ````bash
   gcloud container clusters get-credentials [CLUSTER_NAME] --zone [YOUR_ZONE]

4. Deploy the application:
   ```bash
   kubectl apply -f deployment.yaml
Usage Once deployed, you can access the Mario application by the external IP assigned to the service. Retrieve the IP with:
   ```bash
   kubectl get service mario-service

# NGINX Kubernetes Deployment

This repository contains the configuration files for deploying a basic NGINX web server in a Kubernetes cluster using Minikube. This README provides instructions for setting up and running the NGINX application.

## Prerequisites

Before you begin, ensure you have the following installed:

- [Minikube](https://minikube.sigs.k8s.io/docs/start/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)

## Getting Started

1. **Clone this Repository**

```bash
   git clone https://github.com/Akiff-hplusstree/Kubernetes-basic-application.git
   cd Kubernetes-basic-application
```

2. **Start Minikube**

Ensure Minikube is running:

```bash
minikube start
```

3. **Deploy NGINX Application**

Apply the NGINX deployment and service configuration:

```bash
kubectl apply -f nginx-deployment.yaml
kubectl apply -f nginx-service.yaml
```

4. **Access the NGINX Web Server**

Retrieve the URL to access the NGINX service:

```bash
minikube service nginx-service
```

This will open a web browser or display the URL where you can access the NGINX web server.

## Cleaning Up

To remove the NGINX deployment and service, you can use the following commands:

```bash
kubectl delete deployment nginx-deployment
kubectl delete service nginx-service
```

To stop Minikube when you're finished:

```bash
minikube stop
```

## Additional Information

Customize the NGINX deployment by modifying `nginx-deployment.yaml`.
The NGINX service is exposed on port 80 by default. You can change the service configuration in `nginx-service.yaml`.

Feel free to modify and extend this repository to suit your needs. Happy Kubernetes-ing!

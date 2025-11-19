# DevOps Demo Repository

This repository provides a complete, opinionated starter DevOps project with:

- A minimal Node.js app (Express)
- Dockerfile to build the app image
- Kubernetes manifests (Namespace, Deployment, Service, Ingress, ConfigMap, Secret)
- GitHub Actions CI workflow to build and (optionally) push images and run tests

> Use this repo as a scaffold — adapt image names, registry, domains, and secrets for your environment.

## Quickstart

Build locally:

```bash
docker build -t devops-demo-app:local ./app
docker run --rm -p 3000:3000 devops-demo-app:local
```

Deploy to Kubernetes (after editing the image in k8s/deployment.yaml to a registry reachable by your cluster):

```bash
kubectl apply -f k8s/
kubectl -n devops-demo get pods,svc,ingress
```

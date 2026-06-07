# Go Web Application

This is a simple website written in Golang. It uses the `net/http` package to serve HTTP requests.

## Running the server

To run the server, execute the following command:

```bash
go run main.go
```

The server will start on port 8080. You can access it by navigating to `http://localhost:8080/courses` in your web browser.

## aryan 

## Looks like this

![Website](static/images/golang-website.png)


# Go Web App GitOps Deployment on AWS EKS

Built and deployed a Go web application on Amazon EKS using a complete CI/CD and GitOps workflow.

## Architecture

GitHub → GitHub Actions → Docker Hub → Helm Chart → ArgoCD → AWS EKS

## Technologies Used

* Go (Golang)
* Docker
* GitHub Actions
* Docker Hub
* Kubernetes (EKS)
* Helm
* ArgoCD
* NGINX Ingress Controller
* AWS (EKS, EC2, Load Balancer)

## What I Implemented

* Containerized a Go web application using Docker.
* Created a CI pipeline using GitHub Actions to:

  * Build the Go application
  * Run code quality checks using golangci-lint
  * Build and push Docker images to Docker Hub
* Automated Helm chart updates with the latest image tag after every successful build.
* Provisioned an Amazon EKS cluster using eksctl.
* Configured Kubernetes Deployments, Services, and Ingress resources.
* Installed and configured NGINX Ingress Controller.
* Installed ArgoCD and implemented GitOps deployment.
* Connected ArgoCD to the GitHub repository to automatically sync application changes to EKS.
* Exposed ArgoCD using an AWS Load Balancer for external access.
* Diagnosed and resolved real-world issues involving:

  * Node group creation failures
  * Docker Hub authentication and token permissions
  * GitHub Actions push conflicts
  * ArgoCD secret corruption
  * Kubernetes pod scheduling limits on t3.micro nodes
  * LoadBalancer and NodePort networking issues

## Key Learning Outcomes

* End-to-end CI/CD implementation
* Kubernetes application deployment and troubleshooting
* Helm package management
* GitOps using ArgoCD
* AWS EKS cluster administration
* Docker image lifecycle management
* Debugging production-like infrastructure issues



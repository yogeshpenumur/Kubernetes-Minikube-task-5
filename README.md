# TASK 5: Build a Kubernetes Cluster Locally with Minikube (HTTPD Example)

## Objective
Deploy and manage an Apache HTTPD application locally on a Kubernetes cluster using Minikube.

## Tools
Minikube

kubectl

Docker

## Deliverables
deployment.yaml – HTTPD deployment configuration

service.yaml – Service configuration to expose HTTPD


# Steps
## Step 1: Install Minikube & Start the Cluster
 # Start Minikube cluster
minikube start

## Step 2: Create deployment.yaml for HTTPD
## Apply deployment
kubectl apply -f deployment.yaml

## Step 3: Create service.yaml to Expose HTTPD
## Apply service
kubectl apply -f service.yaml

## Step 4: Verify the Pods
kubectl get pods

## Step 5: Access the HTTPD Service
## Open in default browser
minikube service httpd-service

This should open the Apache HTTPD default welcome page.

## Step 6: Scale the Deployment
kubectl scale deployment httpd-deployment --replicas=4


kubectl get pods

## Step 7: Describe Resources & View Logs
## Describe a pod
kubectl describe pod (pod-name)


kubectl logs (pod-name)

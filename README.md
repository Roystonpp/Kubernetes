# Kubernetes
Deploying Nginx
- 1
First clone this repo or copy the deployment.yaml file

Make sure you have Kubernetes and Minikube installed on your local machine.

Enter the following:
```
Minikube start
Kubectl get nodes
```

You should see a node named "minikube" and the status should "ready".
After this go to your directory with the deployment file and enter:
```
Kubectl create -f deployment.yaml
```
To check this yaml has deployed type in your cmd:
```
Kubectl get deployments
```
To further check enter:
```
Kubectl describe deployment <name_of_deployment>
```
To expose this deployment enter:
```
kubectl expose deployment <name_of_deployment> --type=NodePort
```
Type the command below to check if the deployment is exposed
```
Kubectl get svc
```
- 2 
Checking the status of the deployment
```
Kubectl get pods
Kubectl describe pod <name_of_pod>
```
- 3
To view the deployment enter:
```
minikube service <name_of_deployment>
```
or
```
minikube service <name_of_deployment> --url
```
You should see the "Hello World" Nginx page

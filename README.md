# DEVOPS-Build-a-Kubernetes-Cluster-Locally-with-Minikube

Install Minikube in Ubuntu/Debian
```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
```
Install Kubectl
```bash
curl -LO "https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl"
```
Change Permission
```bash
chmod +x kubectl
```

Move to 
```bash
sudo mv kubectl /usr/local/bin/
```

Start Minikube
```bash
minikube start --driver=docker
```
Verify Pods
```bash
kubectl get nodes
```

After getting file ,Apply Services for creating resource
```bash
kubectl apply -f nginxdeployment.yaml
```
After the pods created ,
Check pods 
```bash
kubectl get pods
```
Apply service
```bash
kubectl apply -f nginxservice.yaml
```

Verify Deployment
```bash
minikube service nginx-service
```

Apply Two Services,
```bash
 minikube service apache-service   minikube service nginx-service 
```





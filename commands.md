## SSH to droplet digital ocean
ssh -i .ssh/digitalocean root@104.248.182.237+

## To test that the file authenticates successfully,
kubectl --kubeconfig=.kube/k8s-1-13-1-do-2-nyc1-1546269711917-kubeconfig.yaml get nodes

## Deploy a Workload to your cluster
kubectl --kubeconfig=/Users/josephmartinez/.kube/k8s-1-13-1-do-2-nyc1-1546269711917-kubeconfig.yaml create -f ./my-manifest.yaml

kubectl apply -f ./deployment.yaml
kubectl expose deployment tomcat-deployment --type=NodePort
minikube service tomcat-deployment --url
curl <URL>


```
Linux:

curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl

MacOS:

curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/darwin/amd64/kubectl

Windows:

curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.8.0/bin/windows/amd64/kubectl.exe

chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl
kubectl version

Linux:

curl -Lo minikube https://storage.googleapis.com/minikube/releases/v0.23.0/minikube-linux-amd64 && chmod +x minikube && sudo mv minikube /usr/local/bin/

macOS:

curl -Lo minikube https://storage.googleapis.com/minikube/releases/v0.23.0/minikube-darwin-amd64 && chmod +x
minikube && sudo mv minikube /usr/local/bin/
minikube start
kubectl run hello-minikube --image=gcr.io/google_containers/echoserver:1.4 --port=8080
kubectl expose deployment hello-minikube  --type=NodePort
kubectl get pod
curl $(minikube service hello-minikube --url)
kubectl delete deployment hello-minikube
```

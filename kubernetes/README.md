To create a deployment
hello

kubectl create -f deployment.yaml

Exposing the go-app pod
Let's create a Service object that exposes the deployment:

kubectl expose deployment my-go-app --type=NodePort --name=go-app-svc --target-port=3000

Check the sv
kubectl get svc


Testing - access the app
Go to browser with minikube-ip:nodePort which is 192.168.99.100:30652 or localhost:30652

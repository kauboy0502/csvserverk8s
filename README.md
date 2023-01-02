# csvserverk8s
Create the script file a.sh and assign permissions 755 for the file

chmod 755 a.sh

Run the script a.sh with the below command:
./a.sh or nohup ./a.sh &

The inputFile will be generated in the same path as the script file

Install minikube on your machine to run a local k8s cluster:
* curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
* sudo install minikube-linux-amd64 /usr/local/bin/minikube
* minikube start --driver=docker
* kubectl get nodes -o wide
    
Create the k8s manifest files required for implementing the project on k8s
* Deployment
* config map
* NodePort service

Once these are created apply the k8s objects using the kubectl apply -f . command 

minikube service svcname --url

All the k8s objects listed above will be created and then open the node ip with the port exposed on a browser and you will be able to see the application up and running



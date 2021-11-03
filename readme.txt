docker build -t premdevdis/test-react-vite .
docker run -p 5000:5000 premdevdis/test-react-vite
docker push premdevdis/test-react-vite

kubectl apply -f reactapp-depl.yml
kubectl get service
kubectl get pods

kubectl delete all --all
kubectl delete pods my-react-app-depl-649d9cf777-94bt7
kubectl delete --all service
kubectl delete --all deployments

kubectl config view
kubectl config get-contexts
kubectl config get-clusters
kubectl config delete-context minikube
kubectl config delete-cluster minikube
kubectl config get-users
kubectl config delete-user minikube


docker create --name new_ubuntu -it -p 8080:8080 -p  15672:15672 -p 5432:5432   ubuntu:latest bash

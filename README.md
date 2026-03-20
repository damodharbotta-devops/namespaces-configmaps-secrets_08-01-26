# namespaces-configmaps-secrets_08-01-26

## Commands:

## Namespace:

kubectl get ns
kubectl create ns dev
kubectl create -f namespace.yml
kubectl describe ns test
kubectl run pod1 --image=httpd -n test   ----> create pod manually in test namespce

## service:
kubectl create -f service.yml
kubectl create -f service.yml -n test
kubectl create -f service.yml -n dev
kubectl create -f service.yml -n uat
kubect get svc

kubectl config set-context --current --namespace=default   ----> shift one namespace to another namspace
kubectl config view  --> full infornmation
kubectl config view | grep "namespace"   ----> check current namespace


### kubens

kubens ---> check list of all namespaces
kubens -c ---> check current namespace
kubens test ---> shift to test namespace
kubens - ---> shift to previous name space



# Sunday Fun
Kubernetes session for friends

## Create Namespace
```
kubectl create -f ./my-namespace.yaml
or
kubectl create namespace sundayfun
```

## Create an Application
Creating an application is all about asking Kubernetes to run a container created from the given image

```
cd sundayfunapp
docker build -t sundayfunapp
docker push

kubectl create -f ./my-sundayapp.yaml
```


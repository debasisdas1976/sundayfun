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
docker build --tag sundayfunapp .
docker run --name sundayfunapp -d -p 8080:80 sundayfunapp
dokcker login
docker tag sundayfunapp debasisdas1976/sundayfunapp
docker push debasisdas1976/sundayfunapp

kubectl create -f ./my-sundayapp.yaml
```


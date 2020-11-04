# Sunday Fun
Kubernetes session for friends

## Create Namespace
```
kubectl create -f ./my-namespace.yaml
or
kubectl create namespace sundayfun
kubectl config set-context --current --namespace=sundayfunapp
```

## Create an Application
Creating an application is all about asking Kubernetes to run a container created from the given image

### Build your application docker image
```
cd sundayfunapp
docker build --tag sundayfunapp .
```
### Test your docker image
```
docker run --name sundayfunapp -d -p 8080:80 sundayfunapp
```
Open a browser window and visit to the site http://localhost:8080
You should be able to see your application Webpage

### Push your docker image to a repository to access it later on
```
dokcker login
docker tag sundayfunapp debasisdas1976/sundayfunapp
docker push debasisdas1976/sundayfunapp
```
### Create your application in kubernetes
```
kubectl create -f ./my-sundayapp.yaml
```


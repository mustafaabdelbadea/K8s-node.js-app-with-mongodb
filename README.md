# K8s-node.js-app-with-mongodb
<div align="center">
  <a href="https://github.com/github_username/repo_name">
    <img src="Kubernetes-Logo.png" alt="Logo" width="250" height="150">
  </a>
  
  <br/>
Deploying node.js app with mongodb using kubernetes
  </div>
  
## Installation

### Platform & tools

You need to install minikube, kubectl and docker as a driver for minikube .
* [Install minikube](https://minikube.sigs.k8s.io/docs/start/)
* [Install docker engine](https://docs.docker.com/engine/install/)
* [Install kubectl](https://kubernetes.io/docs/tasks/tools/)

### Get the Code

Either clone this repository or fork it on GitHub and clone your fork:

```
git clone git@github.com:mustafaabdelbadea/K8s-node.js-app-with-mongodb.git
cd K8s-node.js-app-with-mongodb
```


## Running
### Start the minikube

```
minikube start
```
    
### Create Config and Secret for MongoDB Credentials
 ```
    kubectl apply -f mongo-config.yml
    kubectl apply -f mongo-secret.yml
 ```
 ### Create MongoDB Deployment
  ```
    kubectl apply -f mongo.yml
  ```
    
 ### Create Webapp Deployment 
  ```
    kubectl apply -f webapp.yml
  ```
  
  ### Get minikube node's ip address
```
minikube ip
```
### To directly access service
```
minikube service webapp-service
```

### To stop cluster 
```
minikue stop
```






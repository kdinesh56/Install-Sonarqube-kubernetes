# Install-Sonarqube-kubernetes
This project is to install Sonarqube over the Kubernetes cluster. 

## Two deployments are created for Sonarqube Server and Postgres Server.

Execute the below commands to create the deployments.

`Kubectl apply -f sonar-postgres-deployment.yaml`
`kubectl apply -f sonarqube-deployment.yaml`

## To review the pods created

`kubectl get deployments`
`kubectl get pods`

## Create the service for the corresponding deployments Sonaqrqube and Postgres

Execute the below commands to create the deployments.

`kubectl create -f sonarqube-service.yaml`
`kubectl create -f sonar-postgres-service.yaml`


## Create Persistent volume and claim

`kubectl create -f sonar-pv-postgres.yaml`     
`kubectl create -f sonar-pvc-postgres.yaml`

## Create a ingress and attach to the service

`kubectl create -f sonar-ingress.yaml`



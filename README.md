# Desafio 8 

## Applicación de la imagen
https://github.com/CamilaCosentino/EccomerceMongoDBNodejs

## Como crear la imagen y Publicarla
```bash
docker build -t nodeapp:v1.0.0 -f ./Dockerfile .
```
```bash
docker push camila232dmnfdn2i/nodeapp_mongodb:1.0.0
```


## Creamos todos los archivos para Deployar la imagen en Minikube



## Minikube
Para encender minikube, esto debes usarlo una vez que inicies Docker en tu computadora
```bash
minikube start
```
```bash
minikube dashboard
```
### Para deployear la aplicación
```bash
kubectl apply -f nodeapp/kubernetes/nodeapp/pv.yaml
```
```bash
kubectl apply -f nodeapp/kubernetes/nodeapp/pvc.yaml
```
```bash
kubectl apply -f nodeapp/kubernetes/nodeapp/mongo-sercret-name.yaml
```
```bash
kubectl apply -f nodeapp/kubernetes/nodeapp/mongo-sercret-pass.yaml
```
```bash
kubectl apply -f nodeapp/kubernetes/nodeapp/mongo-configmap.yaml
```
```bash
kubectl apply -f nodeapp/kubernetes/nodeapp/mongo-configmap.yaml
```
```bash
kubectl apply -f nodeapp/kubernetes/nodeapp/services.yaml
```
```bash
kubectl apply -f nodeapp/kubernetes/nodeapp/deployment.yaml
```
#### Se debe hacer lo mismo para prometheus y Grafana


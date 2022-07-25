# Kubernetes_Homework

This repository represent kubernetes project, it has developed using minikube.
The mean idea to publish 3 website with 3 different paths, for that i have used ingress technology to manage network connection.
For each website i have used yaml file , which has:
* **Deployment:** build the pod under supervison(to avoid failure), every pod know the docker image to run over.
* **Service:** enables network access from either within the cluster or between external. processes and the service

Also, I have build yaml file for ingerss and redis.

### About wibsites
1. **Bitcoin:**
Presents the Current BitCoin Price, And the Average Price for the last 10 minutes and stores the price in a Redis Database.
For more information you can visit 

2. **Ynet:**
Maven project that repressent Breaking News in : https://www.ynet.co.il
For more information you can visit  https://github.com/nadeemjazmawe/Jenkins-Closing-Task

3. **gs-boot:** 
Provides a sampling of "Spring Boot"
For more information you can visit https://github.com/nadeemjazmawe/gs-spring-boot



##Run repository

First you need to have minikube on your computer.

Clone the project
git clone 
```
https://github.com/mohamadassi173/YnetNews_bitcoinPrice_kubernetes.git
```
Get in project directory
```
cd YnetNews_bitcoinPrice_kubernetes
```
 
Start minikube
```
minikube start
```
To enable ingress on minikube, we need to enagle ingress plugin
```
  minikube addons enable ingress
```
Finally Insert all deployments
```
 kubectl apply -f .
```

Now, you have running minikube with 3 websites.
To visit this websites you need to start minikube tunnel 
```
minikube tunnel
```


you can visit the websites now using:
* http://localhost/bitcoin
* http://localhost/ynet
* http://localhost/gs-boot

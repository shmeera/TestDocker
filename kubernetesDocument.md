### How to run kubernetes
1. Install minikube from https://minikube.sigs.k8s.io/docs/start/ (follow the instructions for windows)
2. Install kubernetes  https://kubernetes.io/docs/tasks/tools/install-kubectl-windows/ (follow the instructions for windows)
3. Open command prompt and run below command
```shell
minikube start
```
4. In the project directory, create a deployment file
5. Right click on project name (testDocker) -> new  file -> Kubernetes Resources -> Deployment (Give file name as TestDockerDeployment.yml
6. Repeat step 5 and create a service file (Give file name as TestDockerService.yml)
Automatically yaml file code gets generated in the file
7. Make changes name, and add below code in deployment file
```shell
name: testdocker
      ports:
              - containerPort: 8080
                protocol: TCP
 ```
8. Make changes name, and add below code in service file

```shell
name: testdocker
  type: LoadBalancer
```
9. Run below command to deploy the application
```shell
kubectl apply -f TestDockerDeployment.yaml
kubectl apply -f TestDockerService.yaml  
```
10. Run below command to check the status of the deployment
```shell
kubectl get pods
```
11. Run below command to check the status of the service
```shell
kubectl get svc
```
12. Run below command to open the application in the browser
```shell
minikube service testdocker
```
13. Run below command to delete the deployment
```shell
kubectl delete deployment testdocker
```
14. Run below command to delete the service
```shell
kubectl delete service testdocker
```
15. Run below command to stop minikube
```shell
minikube stop
```
16. Run below command to delete minikube
```shell
minikube delete
```
17. Run below command to check the status of the minikube
```shell
minikube status
```
18. Run below command to check the status of the minikube
```shell    
minikube dashboard
```
19. Run below command to check the status of the minikube
```shell
minikube service list
```
20. Run below command to check the status of the minikube
```shell
minikube ip
```
21. Run below command to check the status of the minikube
```shell
minikube service testdocker --url
```
22. To check the logs of the pod
```shell
kubectl logs <pod-name>
```
23. To check the logs of the pod
```shell
kubectl describe pod <pod-name>
```
24. To check the logs of the pod
```shell
kubectl exec -it <pod-name> -- /bin/bash
``` 
25. To check the logs of the pod
```shell
kubectl get events
```
26. To check the logs of the pod
```shell
kubectl get nodes
```
27. To check the logs of the pod
```shell
kubectl get services
```
28. To check the logs of the pod
```shell
kubectl get deployments
```
29. To check the logs of the pod
```shell
kubectl get pods
```
30. delete running pod
```shell
kubectl delete pod <pod-name>
```

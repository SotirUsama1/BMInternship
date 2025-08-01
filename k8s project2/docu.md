# Node-helloWorld Project

## 	1- Deploy the Application

>  Define your Deployment manifest for the Node.js app, apply it to the cluster, and confirm that your Pod comes up in the Ready state.
>> Deliverable
Deployment YAML and evidence that the Pod is running and healthy. <br>

- Start Minikube using

``` bash
minikube start --driver=docker
```

- Make sure that it is properly running

> ``` bash
> minikube status
> ```
> the output should be
> ``` bash
> minikube
> type: Control Plane
> host: Running
> kubelet: Running
> apiserver: Running
> kubeconfig: Configured
> ```


- Now, navigate to the project directory and apply the deployment

``` bash
kubectl apply -f deployment.yaml
```

- To make sure that the deployment have been successfully deployed, run this command to only watch the labeled nodejs-hello pods

``` bash
kubectl get pods -o wide -l app=nodejs-hello -w
```

- After checking that the pods are running, to test their reachability, we have to create a new pod on the same node to curl any of the deployed pods' ips and the port they are listening on `Port:3000`, this is a curl pod to use for the test run command

> ``` bash
> kubectl run curl-pod --image=curlimages/curl --rm -it -- /bin/sh
> ```
> This will open sh in a curl pod, now curl one of the pods ips on the port 3000
> ``` bash
> curl {pod ip}:3000
> ```
> the output should be
> ``` bash
> Hello Node!
> ```

# KubeLocal: Hands-On Kubernetes Workshop

## Install Kubernetes Locally

Screenshot or pasted outputs of both commands

![Alt text](./Screenshot%20From%202025-07-30%2017-47-54.png)

## Write Your First Pod Manifest

The nginx-pod.yaml file and the output of kubectl describe pod nginx

> This is a link the [nginx-pod.yaml file](./nginx-pod.yaml)
> ``` yaml
> apiVersion: v1
> kind: Pod
> metadata:
>   name: nginx
> spec:
> containers:
> - name: nginx-container
>   image: nginx:latest
>   ports:
>   - containerPort: 80
> ```

<br>

``` bash
$ kubectl describe pod nginx

Name:             nginx
Namespace:        default
Priority:         0
Service Account:  default
Node:             minikube/192.168.49.2
Start Time:       Wed, 30 Jul 2025 18:13:23 +0300
Labels:           <none>
Annotations:      <none>
Status:           Running
IP:               10.244.0.5
IPs:
  IP:  10.244.0.5
Containers:
  nginx-container:
    Container ID:   docker://fb6f4a18f9685959a8af74f17d68f659e792d31ad775179cdf580040f15ae459
    Image:          nginx:latest
    Image ID:       docker-pullable://nginx@sha256:84ec966e61a8c7846f509da7eb081c55c1d56817448728924a87ab32f12a72fb
    Port:           80/TCP
    Host Port:      0/TCP
    State:          Running
      Started:      Wed, 30 Jul 2025 18:13:26 +0300
    Ready:          True
    Restart Count:  0
    Environment:    <none>
    Mounts:
      /var/run/secrets/kubernetes.io/serviceaccount from kube-api-access-p4thd (ro)
Conditions:
  Type                        Status
  PodReadyToStartContainers   True 
  Initialized                 True 
  Ready                       True 
  ContainersReady             True 
  PodScheduled                True 
Volumes:
  kube-api-access-p4thd:
    Type:                    Projected (a volume that contains injected data from multiple sources)
    TokenExpirationSeconds:  3607
    ConfigMapName:           kube-root-ca.crt
    Optional:                false
    DownwardAPI:             true
QoS Class:                   BestEffort
Node-Selectors:              <none>
Tolerations:                 node.kubernetes.io/not-ready:NoExecute op=Exists for 300s
                             node.kubernetes.io/unreachable:NoExecute op=Exists for 300s
Events:
  Type    Reason     Age    From               Message
  ----    ------     ----   ----               -------
  Normal  Scheduled  6m39s  default-scheduler  Successfully assigned default/nginx to minikube
  Normal  Pulling    6m39s  kubelet            Pulling image "nginx:latest"
  Normal  Pulled     6m36s  kubelet            Successfully pulled image "nginx:latest" in 2.409s (2.409s including waiting). Image size: 192231837 bytes.
  Normal  Created    6m36s  kubelet            Created container: nginx-container
  Normal  Started    6m36s  kubelet            Started container nginx-container
```

## Manage Deployments & Replicas
Updated manifest plus CLI logs showing both the rollout and the rollback

> To review CLI logs find this [session.log](./session.log) file and execute this command in a terminal
`cat session.log`
<p align = "center">
  <img src="./Screenshot%20From%202025-08-11%2015-34-38.png" alt="drawing" width="550"/>
  <br>
  <img src="./Screenshot%20From%202025-08-11%2015-34-51.png" alt="drawing" width="550"/>
</p>
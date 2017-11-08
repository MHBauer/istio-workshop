## Exercise 5 - Installing Istio

#### Clean up

Start with a clean slate and delete all deployed services from the cluster:

```
    kubectl delete all
```

#### Download Istio

Either download it directly or get the latest using curl:

https://github.com/istio/istio/releases

```
curl -L https://git.io/getLatestIstio | sh -
export PATH=$PWD/istio-0.2.12/bin:$PATH
```

#### Running istioctl

Istio related commands need to have `istioctl` in the path.  Verify it is available by running:

`istioctl -h`


#### Install Istio on the Kubernetes Cluster

1 - First grant cluster admin permissions to the current user (admin permissions are required to create the necessary RBAC rules for Istio):
``` 
    bx account users
```
Take the output to the next command
<pre>
    kubectl create clusterrolebinding cluster-admin-binding \
        --clusterrole=cluster-admin \
        --user=<i><b>user</b></i>
</pre>
2 - Next install Istio on the Kubernetes cluster:

Change to the Istio directory (istio-0.2.12) and and install istio in the kubernetes cluster

```
    cd istio-0.2.12
    kubectl apply -f install/kubernetes/istio.yaml
```


#### Viewing the Istio Deployments

Istio is deployed in a separate Kubernetes namespace `istio-system`  You can watch the state of Istio and other services and pods using the watch command.  For example in 2 separate terminal windows run:

```
  watch -n 30 kubectl get po --all-namespaces
  watch -n 30 kubectl get svc --all-namespaces
```

#### [Continue to Exercise 6 - Creating a Service Mesh with Istio Proxy](../exercise-6/README.md)

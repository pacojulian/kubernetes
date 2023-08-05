# Exposing Ports
## Create a Pod

```shell
kubectl create deploy httpenv --image=bretfisher/httpenv
```

## Make a deployment
```shell
kubectl scale deployment/httpenv --replicas=5
```
## Expose a port
```shell
kubectl expose deployment/httpenv --port 8888
```
```shell
kubectl expose deployment/httpenv --port 8888 --name httpenv-np --type NodePort
```
## get all services
```shell
kubectl get all
```

## Check a service ip

``` shell
kubectl get service
```

## Removing/deleting
```shell
kubectl delete service/httpenv service/httpenv-np
```

## DNS
```shell
kubectl get namespaces
```


## Extras
```shell
kubectl run tmp-shell --rm -it --image bretfisher/netshoot -- bash
```
# Management
## Generators


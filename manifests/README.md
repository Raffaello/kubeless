# Collection of manifests for development

**NOTE: TO INSTALL KUBELESS USE A RELEASED MANIFEST AT https://github.com/kubeless/kubeless/releases"


Create `kubeless` namespace and create zookeeper

```
kubectl create -f zookeeper/namespace.yaml
kubectl create -f zookeeper/zk-headless-svc.yaml
kubectl create -f zookeeper/zk-stateful.yaml
kubectl create -f zookeeper/zk-svc.yaml
```

Create TPR For functions

```
kubectl create -f tpr/function.yaml
```

Create Kafka broker

```
kubectl create -f kafka/kafka-stateful.yaml
kubectl create -f kafka/kafka-headless-svc.yaml
kubectl create -f kafka/kafka-svc.yaml
```

Launch kubeless controller and UI

```
kubectl create -f controller/controller-deployment.yaml
kubectl create -f ui/ui-deployment.yaml
kubectl create -f ui/ui-svc.yaml
```

Create Ingress controller and sample ingress route

```
kubectl create -f ingress/ingress-controller-http-only.yaml
kubectl create -f ingress/demo-svc.yaml
kubectl create -f ingress/demo-ingress.yaml
```

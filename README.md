# K8s Kind Example 1

The content of this directory is base on the
[Kubernetes with kind](https://www.baeldung.com/ops/kubernetes-kind)
article.

Install `kubectl` and `kind` cli.

```bash
# kind create cluster --name kind-ex-1 --image kindest/node:v1.23.3 # not use option
kind create cluster --config cluster-ex-1.yaml
kind delete cluster --name cluster-ex-1
kubectl cluster-info --context kind-cluster-ex-1
kubectl cluster-info dump --context kind-cluster-ex-1
# use nginx as load balancer and ingress via
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/kind/deploy.yaml
kubectl apply -f app1-dply-srv-ing.yaml
kubectl apply -f app2-dply-srv-ing.yaml
```


# K8S Setup

## helm setup

```
kubectl --namespace kube-system create serviceaccount tiller

kubectl create clusterrolebinding tiller --clusterrole cluster-admin --serviceaccount=kube-system:tiller

helm init --service-account tiller --upgrade
```
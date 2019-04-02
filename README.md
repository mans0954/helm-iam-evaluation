Helm Chart which depends on the Comanage chart and also (twice) on the Shibboleth IdP Chart aliased as `christminster-idp` and `barchester-idp`.

N.B. I don't think I got this to a stage where it was completely working.

```
minikube start
kubectl config use-context minikube
helm init
helm serve
helm dependency update
helm install .
```

Assuming that `comanage.tier.minikube` is alisased to the Minikube IP in `/etc/hosts`, COmanage will be avaliable at: http://comanage.tier.minikube/registry/

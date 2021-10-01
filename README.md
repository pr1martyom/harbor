Harbor

```
helm repo add bitnami https://charts.bitnami.com/bitnami

kubectl create ns harbor

helm upgrade --install harbor -n harbor --set expose.ingress.hosts.core= \  # harbor domain
  --set expose.ingress.hosts.notary=  \  # notary domain
  --set harborAdminPassword: "" \ # admin pass
  bitnami/harbor
```

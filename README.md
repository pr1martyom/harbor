Harbor

```
git clone https://github.com/pr1martyom/harbor.git harbor

cd harbor

kubectl create ns harbor

helm -n harbor upgrade --install harbor --set expose.tls.enabled=false  --set expose.ingress.hosts.core=harbor.example.com --set expose.ingress.hosts.notary=notary.example.com --set harborAdminPassword=changeme --set externalURL=https://harbor.example.com  .

# Need to change harbor.domain, notary.domain and harborAdminPassword
```


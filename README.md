Harbor

```
git clone https://github.com/pr1martyom/harbor.git harbor

cd harbor

kubectl create ns harbor

helm -n harbor upgrade --install harbor  --set expose.ingress.hosts.core=harbor.domain.com \  
     --set expose.ingress.hosts.notary=notary.domain.com \
     --set harborAdminPassword=changeme .

# Need to change harbor.domain, notary.domain and harborAdminPassword
```


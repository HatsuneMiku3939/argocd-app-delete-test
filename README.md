# argocd-app-delete-test

```
argocd app create cluster-bootstrap \
  --repo https://github.com/HatsuneMiku3939/argocd-app-delete-test.git \
  --path cluster-bootstrap \
  --dest-server https://kubernetes.default.svc \
  --dest-namespace default
```

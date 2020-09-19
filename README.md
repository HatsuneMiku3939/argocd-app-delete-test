# argocd-app-delete-test


```
argocd app create cluster-bootstrap \
  --repo https://github.com/HatsuneMiku3939/argocd-app-delete-test.git \
  --path cluster-bootstrap \
  --directory-recurse \
  --sync-policy auto \
  --dest-server https://kubernetes.default.svc \
  --dest-namespace default
```

```
argocd app delete cluster-bootstrap
```

```
kubectl -n argocd logs argocd-application-controller-xxxxxxx
msg="Unable to delete application resources: appproject.argoproj.io \"example\" not found" application=helloworld dest-namespace=example dest-server="https://kubernetes.default.svc" reason=StatusRefreshed type=Warning
```

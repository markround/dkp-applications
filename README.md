# Setup

```shell
kubectl apply -f - <<EOF
---
apiVersion: source.toolkit.fluxcd.io/v1beta1
kind: GitRepository
metadata:
  name: mdr-catalog-applications
  namespace: kommander
  labels:
    kommander.d2iq.io/gitapps-gitrepository-type: catalog
    kommander.d2iq.io/gitrepository-type: catalog
    kommander.d2iq.io/workspace-default-catalog-repository: "true"
    kommander.d2iq.io/project-default-catalog-repository: "true"
spec:
  interval: 30s
  ref:
    branch: main
  timeout: 20s
  url: https://github.com/markround/dkp-applications
EOF
```

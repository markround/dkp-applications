
```shell
kubectl apply -f - <<EOF
apiVersion: source.toolkit.fluxcd.io/v1beta1
kind: GitRepository
metadata:
  name: mdr-dkp-applications
  namespace: kommander-default-workspace
spec:
  interval: 1m0s
  ref:
    branch: main
  timeout: 20s
  url: https://github.com/markround/dkp-applications
EOF
```

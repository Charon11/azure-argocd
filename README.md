# Setup

## Instana
Install via Kube Lens

## ArgoCD
### Install
In cluster-setup/argocd
kustomize build | kubectl apply --dry-run=client -f - (remove `--dry-run=client` to install)
### Add hook on github
- new webhook
- http://argocd.57a7127dd6cb452b952f.francecentral.aksapp.io/api/webhook
- application/json

## Reloader
In cluster-setup/reloader
kustomize build | kubectl apply --dry-run=client -f - (remove `--dry-run=client` to install)
Can be synch by argocd too

## Stern
[Docs](https://github.com/wercker/stern)
ex: `stern -n aks-test hello --tail 10`
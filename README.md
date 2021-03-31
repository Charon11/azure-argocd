# Setup

## Instana
Install via Kube Lens

## ArgoCD
In cluster-setup/argocd
kustomize build | kubectl apply --dry-run=client -f - (remove `--dry-run=client` to install)


## Reloader
In cluster-setup/reloader
kustomize build | kubectl apply --dry-run=client -f - (remove `--dry-run=client` to install)
Can be synch by argocd too

## Stern
[Docs](https://github.com/wercker/stern)
ex: `stern -n aks-test hello --tail 10`
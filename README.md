# Setup

## Instana
Install via Kube Lens

## ArgoCD
### Install
In cluster-setup/argocd
kustomize build | kubectl apply --dry-run=client -f - (remove `--dry-run=client` to install)

Exposing on azure : [http-application-routing](https://learn.microsoft.com/en-us/azure/aks/http-application-routing#http-application-routing-add-on-overview)
### Add hook on github
- new webhook
- http://argocd.b853740bf1c7416a8df0.francecentral.aksapp.io/api/webhook
- application/json

## Reloader
In cluster-setup/reloader
kustomize build | kubectl apply --dry-run=client -f - (remove `--dry-run=client` to install)
Can be synch by argocd too

## Stern
[Docs](https://github.com/wercker/stern)
ex: `stern -n aks-test hello --tail 10`
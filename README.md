helm install flaskapp -n python . --create-namespace
helm uninstall flaskapp -n python       

DEPLOY ARGOCD

$ helm repo add argo https://argoproj.github.io/argo-helm
"argo" has been added to your repositories

$ helm install my-release argo/argo-cd
NAME: my-release
...

helm upgrade --install argocd argo/argo-cd -n argocd --create-namespace -f values-argo.yaml
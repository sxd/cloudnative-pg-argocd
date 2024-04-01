# cloudnative-pg-argocd

This project aims to show different ways to install the 
[CloudNativePG](https://cloudnative-pg.io) operator with [ArgoCD](https://argo-cd.readthedocs.io/en/stable/)

Every directory has and example with different ways to deploy the operator

[Simple way](install-operator-simple/) show how to install the operator using a basic kustomize
with all the default options and nothing else. Creating the app with ArgoCD
```shell
argocd app create cloudnative-pg --repo https://github.com/sxd/cloudnative-pg-argocd.git --path install-operator-simple --dest-server https://kubernetes.default.svc
```

[App of Apps](install-operator-argocdapp/) an example app that will create an operator deployment
using the app-of-apps model from the ArgoCD documentation 

# Docker
https://docs.docker.com/desktop/install/windows-install/

# Install Minikube (windows) *Sorry guys this is a sin
https://minikube.sigs.k8s.io/docs/start/

# Install Kubectl
https://kubernetes.io/es/docs/tasks/tools/included/install-kubectl-windows/

# Helm 
https://helm.sh/docs/intro/install/

# ArgoCD (Prefer the last version)
https://github.com/argoproj/argo-cd/releases

# Tools
https://github.com/ahmetb/kubectx


In this order, access the argoCD UI creating the port-forwarding and get secret admin user.
List secret:
kubectl get secret -n argocd
NAME                          TYPE     DATA   AGE
argocd-initial-admin-secret   Opaque   1      62s
argocd-notifications-secret   Opaque   0      2m6s
argocd-secret                 Opaque   5      2m6s

kubectl get secret -n argocd argocd-initial-admin-secret -o yaml

Port Forwarding 

kubectl port-forward service/argocd-server 8443:https -n argocd

Create path app/infra in a repository



Install base64 and decript de data in secret.

echo -n 'exampleBase64'| base64.exe -d





bootstrap:
	kubectl config use-context docker-desktop
	helm upgrade --install argo-cd oci://ghcr.io/argoproj/argo-helm/argo-cd --version 6.6.0 --namespace argocd --create-namespace

argocd-admin-secret:
	kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d


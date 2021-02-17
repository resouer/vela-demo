# Vela Demo

## GitOps

Bootstrap and deploy to staging environment:

```console
vela gitops bootstrap github \
    --context=staging \
    --owner=${GITHUB_USER} \
    --repository=vela-demo \
    --branch=main \
    --personal \
    --path=deployment/staging
```

Bootstrap and deploy to production environment:

```console
vela gitops bootstrap github \
    --context=production \
    --owner=${GITHUB_USER} \
    --repository=vela-demo \
    --branch=main \
    --personal \
    --path=deployment/production
```

## Plain Apply

Deploy to staging environment:

```console
kubectl apply -f deployments/staging
```

Deploy to production environment:

```console
kubectl apply -f deployments/production
```
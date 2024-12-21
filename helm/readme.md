## Installation
```
helm install hostel-fish ./helm -n hostel-fish --create-namespace
```

## Secrets
> The karns-online group access token in gitea is used here

You will need to create the secrets for the application to use.

Gitea Auth secret for pulling the container from the private registry
```
kubectl -n hostel-fish \
  create secret docker-registry gitea-auth \
  --docker-server=https://gitea.pixelparasol.com \
  --docker-username=deac \
  --docker-password=<REDACTED> \
  --docker-email=deac@pixelparasol.com
```

## Deployment
Each component can be deployed individually by tag by specifiying it with `--set`
```
helm upgrade hostel-fish ./helm -n hostel-fish --set deploy.landing.tag="v1.0.4"
helm upgrade hostel-fish ./helm -n hostel-fish --set deploy.denver.tag="v1.0.4"
helm upgrade hostel-fish ./helm -n hostel-fish --set deploy.seattle.tag="v1.0.4"
```
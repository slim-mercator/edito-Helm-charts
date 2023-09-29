# modellab-helm-charts

# Steps for helm chart
When modifying the helm chart you then need to package it and generate its index before pushing to the git repo


```sh
helm package juptyerlab-autosubmit-bsc
helm repo index .
```


To push the repo to the gitlab package registry
```sh
helm repo add --username username --password personal-acces-token modellab-helm-charts https://gitlab.mercator-ocean.fr/api/v4/projects/1948/packages/helm/test
#helm plugin install https://github.com/chartmuseum/helm-push
#helm cm-push juptyerlab-autosubmit-bsc-1.0.0.tgz modellab-helm-charts
helm push juptyerlab-autosubmit-bsc-1.0.0.tgz modellab-helm-charts
```
# Nginx Helm Chart
Helm chart for testing integration with OSM - K8s

# Add the repo and install the chart
- Add the repo: `helm repo add nginx https://ebucchianeri.github.io/nginx-helm-chart/`
- Download updates from repo: `helm repo update`
- Search Helm Charts: `helm search repo`
- Install Chart: `helm install nginx nginx/nginx-helm`
- Uninstall: `helm uninstall nginx`

# Install the tgz
Install from the tgz:
`helm install nginx ./docs/nginx-helm-0.1.0.tgz`

# Build and publish
For this first version the Helm Chart is packaged manually and served
as a GitHub Page under `/docs`.

To package it:
```
helm package . --destination docs/
```
To update the index
```
cd docs
mkh repo index .. --url https://ebucchianeri.github.io/nginx-helm-chart/ --merge index.yaml
cp ../index.yaml . 
```

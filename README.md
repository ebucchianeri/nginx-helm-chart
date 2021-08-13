# Nginx Helm Chart




# Build and publish
`helm package . --destination docs/`
`helm repo index . --url <URL> --merge docs/index.yaml `

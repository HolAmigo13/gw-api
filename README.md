# gw-api

# Install CRD
kubectl apply -f https://github.com/kubernetes-sigs/gateway-api/releases/latest/download/standard-install.yaml


# Install NGINX Gateway Fabric controller
helm install ngf oci://ghcr.io/nginx/charts/nginx-gateway-fabric \
  --version 2.1.2 \
  -n nginx-gateway --create-namespace \
  --wait


# In CA Dir
kubectl create secret tls wildcard-local-tls \
  --cert=wildcard.local.crt \
  --key=wildcard.local.key \
  -n gateway-api
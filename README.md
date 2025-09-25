# gw-api

# Install CRD
kubectl apply -k "github.com/kubernetes-sigs/gateway-api/config/crd/experimental?ref=v1.2.0"


# In CA Dir
kubectl create secret tls wildcard-local-tls \
  --cert=wildcard.local.crt \
  --key=wildcard.local.key \
  -n gateway-api
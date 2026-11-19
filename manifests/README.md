# Infrastructure maintenance

The cert-manager installation is managed separately from the Cloudflare Ingress overlays.
The installed version is pinned to v1.21.3:

```sh
kubectl apply --server-side -f https://github.com/cert-manager/cert-manager/releases/download/v1.21.3/cert-manager.yaml
```

The `kubedash.ryuzu.dev` Ingress now targets the maintained Headlamp service (Helm chart 0.46.0), rather than the retired Kubernetes Dashboard.

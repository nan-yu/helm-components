# helm-components

This is a DRY (short for Don't Repeat Yourself) repository, which needs the hydration process to render the WET configs.

It includes a kustomization.yaml file.
The kustomization.yaml file will inflate two Helm charts, one is local (cert-manager) and one is remote (prometheus-operator).

You can manually run `kustomize` to preview the rendered manifests:
```console
mkdir manifests
kustomize build --enable-helm --output=manifests
```

You can also run `nomos hydrate` to preview the result:
```console
nomos hydrate --output=manifests
```
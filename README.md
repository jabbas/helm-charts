# helm-charts

Classic HTTP Helm chart repository for charts published by
[@jabbas](https://github.com/jabbas), served via GitHub Pages at
<https://jabbas.github.io/helm-charts>.

## Usage

```sh
helm repo add jabbas https://jabbas.github.io/helm-charts
helm repo update
helm search repo jabbas --devel
```

`--devel` also lists pre-release versions (e.g. `0.1.0-rc.1`).

## Charts

| Chart | Source |
|-------|--------|
| `secretspec-operator` | [jabbas/secretspec-operator](https://github.com/jabbas/secretspec-operator) |

## How it works

- This repo contains only `index.yaml` (plus this README, license and `.nojekyll`).
- The chart `.tgz` files are **not** stored here. They live as assets of each
  project's GitHub Releases; every `urls` entry in `index.yaml` points to the
  absolute release-asset URL.
- `index.yaml` is updated automatically by each project's release workflow.

## Signed artifacts

For signed (cosign) artifacts, use the OCI charts instead:

```sh
helm pull oci://ghcr.io/jabbas/charts/<chart> --version <version>
```

e.g. `oci://ghcr.io/jabbas/charts/secretspec-operator`.

## License

Apache-2.0, see [LICENSE](LICENSE).

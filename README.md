# Chart

A chart repo

- Publish chart to ghcr.io using OCI format.
- GitHub Actions for CI/linting and publishing, using [`helm/chart-testing`](https://github.com/helm/chart-testing).
- `helm-docs` to make sure charts' README are up-to-date.

## Usage
[Helm](https://helm.sh) must be installed to use the charts.

For OCI Registry:
```shell
# login to registry and then
helm pull oci://ghcr.io/duyhenryer/chart/example-chart --version 0.1.0
```

For Helm Registry:
```sh
helm repo add duyhenryer https://duyhenry.github.io/chart
```

If you had already added this repo earlier, run `helm repo update` to retrieve the latest versions of the packages.

```sh
helm install example-chart duyhenryer/example-chart
```

To uninstall the chart:

```sh
helm delete example-chart
```

## License

[LICENSE](./LICENSE)

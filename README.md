# Kubeist Charts

```shell
$ helm repo add kubeist https://charts.kube.ist
$ helm search repo kubeist
$ helm install my-release kubeist/<chart>
```

### How To Release

Releasing new chart versions occurs automatically by a GitHub action.

Remember to update the version information in the charts `Chart.yaml`.

To execute a release you need to make a branch with the name "release/${CHART_NAME}/${VERSION}'

The CHART_NAME should match the folder name of the chart in the charts directory.
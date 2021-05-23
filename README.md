# helm-cluster-repo

Helm plugin to configure repositories registered in Kubernetes cluster

To install the plugin:

```
helm plugin install https://github.com/baijum/helm-cluster-repo
```

Cluster scoped custom resource configuration in the Kubernetes cluster:

```
apiVersion: repos.baiju.dev/v1alpha1
kind: HelmChartRepository
metadata:
  name: example-charts
spec:
  url: https://example.org/charts
```

To enable a chart repository:

```
helm cluster-repo enable example-charts
```

To disable a chart repository:

```
helm cluster-repo disable example-charts
```

To list all chart repositories:

```
helm cluster-repo list
```

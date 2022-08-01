# Helm

## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

  helm repo add jjtroberts https://jjtroberts.github.io/helm-charts

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo
jjtroberts` to see the charts.

To install the nginx chart:

    helm install my-nginx jjtroberts/nginx

To uninstall the chart:

    helm delete my-nginx

## Learnings
### Package chart
```
helm package nginx
```

### Create index
```
helm repo index --url https://github.com/jjtroberts/helm-charts .
```

### Add chart to existing index
```
helm repo index --url https://github.com/jjtroberts/helm-charts --merge index.yaml .
```

### Install from local chart
```
helm install nginx ./nginx-0.1.0.tgz
```
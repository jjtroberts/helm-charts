# Helm

## Create a new chart
```
helm create nginx
```

## Package chart
```
helm package nginx
```

## Create index
```
helm repo index --url https://github.com/jjtroberts/helm-charts .
```

## Add chart to existing index
```
helm repo index --url https://github.com/jjtroberts/helm-charts --merge index.yaml .
```

## Install from local chart
```
helm install nginx ./nginx-0.1.0.tgz
```
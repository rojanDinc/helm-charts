# Helm charts

### Updating a chart

1. Update the `Chart.yaml` file with the new version.
2. Package the new chart.

```
helm package <chart>
```

3. Next move the `tgz` file to the `docs/` directory.

Now we need to update the charts index file by running:
```
helm repo index docs --url https://rojandinc.github.io/helm-charts
```

4. Commit and push the changes.

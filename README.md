# Helm charts

This repository contains Helm charts for Kubernetes deployments.

## Documentation

All charts are automatically documented using [helm-docs](https://github.com/norwoodj/helm-docs).
Each chart includes an auto-generated `README.md` file with configuration options and usage examples.

### Updating a chart

1. Update the `Chart.yaml` file with the new version.
2. Regenerate the chart documentation.

```bash
helm-docs --chart-search-root=charts
```

3. Package the new chart.

```
helm package charts/<chart>
```

4. Move the `tgz` file to the `docs/` directory.

Now we need to update the charts index file by running:
```
helm repo index docs --url https://rojandinc.github.io/helm-charts
```

5. Commit and push the changes.

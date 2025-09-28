# Changelog

All notable changes to the `cluster-core-config` Helm chart will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.1.0]

### Added
- Initial chart creation for cluster core configuration management
- Support for creating and managing Kubernetes namespaces with custom labels
- Service account creation and management with namespace assignment
- Secret management with support for Opaque and custom types
- Comprehensive Grafana dashboard collection for monitoring:
  - Kubernetes API server monitoring
  - Cluster resource utilization dashboards
  - Node and pod resource monitoring
  - Persistent volume usage tracking
  - Victoria Metrics monitoring dashboards
  - Victoria Logs monitoring
  - Workload and namespace-based resource views
- ConfigMap management for dashboard deployment
- ClusterRoleBinding template for RBAC configuration
- Flexible configuration through values.yaml with enable/disable flags for each component

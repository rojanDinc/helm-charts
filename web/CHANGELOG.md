# Changelog

All notable changes to the `web` Helm chart will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.2.1]

### Added
- Support for toggling a Kubernetes service

## [0.2.0]

### Added
- Environment variables support via `env` values
- Secret environment variables support via `envSecrets` values with two formats:
  - Simple format with `secretName` and `secretKey`
  - Advanced format with explicit `valueFrom.secretKeyRef` structure

## [0.1.0]

### Added
- Initial chart creation
- Basic deployment template with support for:
  - Configurable image repository and tag
  - Service and ingress definitions
  - Pod security contexts
  - Resource limits and requests
  - Node affinity, tolerations, and node selectors
  - ServiceAccount configuration
  - Volume and volumeMount support
  - Liveness and readiness probe configuration
  - Horizontal Pod Autoscaler (HPA) configuration

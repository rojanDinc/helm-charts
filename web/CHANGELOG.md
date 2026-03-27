# Changelog

All notable changes to the `web` Helm chart will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.2.5]

### Added
- Support for init containers via `initContainers` value
  - Configurable name, image, command, args, env, securityContext, resources, volumeMounts
  - Supports envSecrets for secret-based environment variables
  - Runs before the main container starts

## [0.2.4]

### Added
- Support for overriding container command and args
  - `command` - override the container entrypoint
  - `args` - override the container arguments

## [0.2.3]

### Added
- Support for persistent volumes via `persistence` value
  - Creates a PVC when `persistence.enabled: true`
  - Configurable storage class, size, access mode, and mount path
  - Supports existing PVs via selector
  - Mounts automatically to the container

## [0.2.2]

### Added
- Support for Kubernetes user namespaces via `hostUsers` value
  - Set `hostUsers: false` to enable user namespace isolation
  - **Warning**: Requires Kubernetes v1.33+ (or v1.29+ with UserNamespacesSupport feature gate)
  - See values.yaml comments for full cluster requirements

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

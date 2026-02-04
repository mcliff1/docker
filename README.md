# Docker Utilities

Collection of Docker and container utilities for AWS development.

## Projects

### cdkbuild
A Docker image that provides a complete build environment with:
- AWS CDK (Cloud Development Kit)
- AWS CLI
- Node.js LTS
- Essential build tools

Multi-architecture support for both AMD64 and ARM64 platforms.

See [cdkbuild/README.md](cdkbuild/README.md) for details.

## Continuous Integration

This repository uses GitHub Actions to automatically build and publish Docker images to Docker Hub.

The build workflow uses Docker Buildx to create multi-architecture images supporting both AMD64 (x86_64) and ARM64 (AArch64) platforms, ensuring compatibility across different processor architectures including Apple Silicon Macs.

## Versioning

Images are versioned using semantic versioning (semver) and automatically tagged when you push version tags (e.g., `v3.0.0`) to the repository.

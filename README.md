# Docker Utilities

Collection of Docker and container utilities for AWS development.

## Projects

### cdkbuild
A Docker image that provides a complete build environment with:
- AWS CDK (Cloud Development Kit)
- AWS CLI
- Node.js LTS
- Essential build tools

See [cdkbuild/README.md](cdkbuild/README.md) for details.

## Continuous Integration

This repository uses GitHub Actions to automatically build and publish Docker images to Docker Hub.

The build workflow uses the [Publish-Docker-Github-Action](https://github.com/elgohr/Publish-Docker-Github-Action) to automate the publishing process.

## Versioning

Images are versioned using semantic versioning (semver) and automatically tagged when you push version tags (e.g., `v3.0.0`) to the repository.

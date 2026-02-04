# GitHub Actions Workflows

## Docker Image CI Workflow

This workflow builds and publishes multi-architecture Docker images for the cdkbuild project.

### Required Secrets

The following secrets must be configured in the repository settings (Settings → Secrets and variables → Actions):

1. **GITLAB_TOKEN** (Required for matts-toolbox installation)
   - Description: GitLab personal access token with `read_api` scope
   - Used to access the private package registry at https://gitlab.com/cliffaws/pypack
   - If not set, the build will succeed but skip matts-toolbox package installation
   - The token is securely passed to Docker BuildKit using secret mounts and never exposed in image layers

2. **DOCKER_USERNAME** (Required for publishing)
   - Description: Docker Hub username
   - Used to authenticate with Docker Hub for pushing images

3. **DOCKER_PASSWORD** (Required for publishing)
   - Description: Docker Hub password or access token
   - Used to authenticate with Docker Hub for pushing images

### Workflow Triggers

The workflow runs on:
- All pushes to any branch (builds only, no push to registry)
- All pull requests (builds only, no push to registry)
- Tags matching `v1.*`, `v2.*`, or `v3.*` (builds AND pushes to Docker Hub)

### Multi-Architecture Support

Images are built for:
- linux/amd64 (x86_64)
- linux/arm64 (ARM64/AArch64)

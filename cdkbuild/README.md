This docker image creates a build environment that has AWS CLI with AWS CDK

## Current Version
**mcliff/cdkbuild:3.0.0** uses CDK 2.1104.0 on Node.js 22 LTS (alpine)

## Multi-Architecture Support
The Docker image is built for multiple architectures:
- **linux/amd64** (x86_64)
- **linux/arm64** (ARM64/AArch64)

This allows the image to run natively on both AMD/Intel and ARM processors (including Apple Silicon Macs).

## Previous Versions
- **mcliff/cdkbuild:2.0.0** uses CDK 2.93.0 on node20 build image
- **mcliff/cdkbuild:1.3.0** uses CDK 1.204.0 on node18 build image


## Releases

### version 3.0.0
- Update to AWS CDK 2.1104.0
- Update to Node.js 22 LTS (alpine)
- Clean up Dockerfile (remove commented code)
- Use `aws-cdk` package name (instead of deprecated `cdk`)

### version 2.0.0
- Update to CDK 2.93.0
- Update to Node 20 for build image

### version 1.3.0
- Update to CDK 1.204.0

### version 1.2.3
- Update to use node18 for build image

### version 1.2.2
- Add openssh

### version 1.2.1
- Minor updates

### version 1.2.0 (2022-02-15)
- Update to Node 16
- Update CDK to 1.142.0

### version 1.1.0 (2021-03-22)
- Update CDK to 1.94.1

### version 1.0.0 (2021-03-13)
- Initial release with automated Docker workflow tags

# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Changed
- Updated AWS CDK to version 2.1104.0 (from 2.93.0)
- Updated Node.js base image to version 22 LTS (from version 20)
- Updated GitHub Actions checkout to v4 (from master)
- Changed npm package name from `cdk` to `aws-cdk` (official package name)
- Improved README documentation with better formatting and clearer instructions
- Fixed broken markdown link in main README
- Cleaned up Dockerfile by removing commented code
- Cleaned up GitHub Actions workflow by removing old commented code

### Added
- Added support for v3.* tags in GitHub Actions workflow
- Added .dockerignore file for optimized Docker builds
- Added this CHANGELOG.md file

### Updated
- Updated LICENSE copyright year to 2019-2026

## [2.0.0] - 2023-09

### Changed
- Updated AWS CDK to version 2.93.0
- Updated Node.js base image to version 20

## [1.3.0]

### Changed
- Updated AWS CDK to version 1.204.0

## [1.2.3]

### Changed
- Updated Node.js base image to version 18

## [1.2.2]

### Added
- Added openssh package

## [1.2.1]

### Changed
- Minor updates

## [1.2.0] - 2022-02-15

### Changed
- Updated Node.js base image to version 16
- Updated AWS CDK to version 1.142.0

## [1.1.0] - 2021-03-22

### Changed
- Updated AWS CDK to version 1.94.1

## [1.0.0] - 2021-03-13

### Added
- Initial release with automated Docker workflow tags
- Docker image with AWS CDK and AWS CLI
- GitHub Actions workflow for automatic publishing to Docker Hub

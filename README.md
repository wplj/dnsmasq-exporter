# dnsmasq-exporter

Maintained container packaging for `google/dnsmasq_exporter` with deterministic, digest-pinned ARM64 builds.

## Upstream

- Upstream project: https://github.com/google/dnsmasq_exporter
- Upstream version currently packaged: `v0.3.0`

## Packaging goals

This repository packages `dnsmasq_exporter` as a production-oriented OCI image with:

- digest-pinned base images
- vendored upstream source
- vendored Go modules
- explicit upstream ref and commit tracking
- non-root runtime default
- deterministic release workflow

## Platform

- `linux/arm64`

## Published image

- `ghcr.io/wplj/dnsmasq-exporter:v0.3.0-r1`

## Operational notes

- This image is intended to be consumed by a deployment layer that provides runtime arguments, mounts, and healthchecks.
- Runtime healthchecks are intentionally not baked into the image.
- The image defaults to a non-root user.
- For production use, prefer pinned pulls by tag and digest.

## Build and release

Release flow is controlled and manual. The image is built from vendored sources and verified locally before push.

## Usage

Example:

`docker pull ghcr.io/wplj/dnsmasq-exporter:v0.3.0-r1`

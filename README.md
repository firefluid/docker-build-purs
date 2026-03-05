# Static purescript tools

This repository contains Dockerfiles to build static binaries of
purescript tools.

To build spago-legacy for ARM64:

    podman buildx build \
        --platform linux/arm64 \
        --file Dockerfile.spago \
        --tag spago-static:arm64 \
        --output=. .

Note that due to the way DNS resolution is handled the binary might not work
correctly on non-musl distributions.

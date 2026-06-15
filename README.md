# Autobrowse VPC Binaries

This repository builds and releases the native dependencies for the Autobrowse Android Virtual PC feature.

## What is built

- `proot` and `libtalloc.so.2` for Android ABIs (`aarch64`, `arm`). These are built from the [Termux packages](https://github.com/termux/termux-packages) source.
- `alpine-xfce-rootfs.tar.gz` — a pre-configured Alpine Linux root filesystem with XFCE, TigerVNC, noVNC, and websockify.

## Triggering a build

```bash
gh workflow run build-binaries.yml --repo Pixelgamer4k/autobrowse-proot-binaries \
  -f version=v1.2.1-binaries
```

## Using the artifacts

The main Autobrowse app fetches these assets from the matching GitHub Release and bundles them into the APK at build time.

# Uunara Agent CLI

Public binary distribution for the Uunara agent CLI.

This repository is used to publish compiled CLI binaries through GitHub Releases. The CLI source code is not published here.

## Install

Download the archive for your operating system and architecture from the [latest release](https://github.com/uunara/cli/releases/latest):

- `uunara-agent_*_darwin_arm64.tar.gz` for Apple Silicon Macs
- `uunara-agent_*_darwin_amd64.tar.gz` for Intel Macs
- `uunara-agent_*_linux_arm64.tar.gz` for Linux ARM64
- `uunara-agent_*_linux_amd64.tar.gz` for Linux x86_64
- `uunara-agent_*_windows_amd64.zip` for Windows x86_64
- `uunara-agent_*_windows_arm64.zip` for Windows ARM64

After extracting the archive, move `uunara-agent` to a directory on your `PATH`.

```sh
uunara-agent version
```

## Checksums

Each release includes `checksums.txt` with SHA-256 checksums for the release archives.

On macOS or Linux:

```sh
shasum -a 256 -c checksums.txt
```

## macOS Signing

Initial macOS binaries may be unsigned. Signed and notarized macOS artifacts will be added in a future release.

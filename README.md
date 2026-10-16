# Uunara Agent CLI

Command-line access to Uunara recipes and cooking for assistants and terminal users.
This public distribution repository contains compiled binaries; the CLI source
is maintained separately.

## Download

Get the archive for your operating system and architecture from the
[latest release](https://github.com/uunara/cli/releases/latest):

- Apple Silicon Mac: `uunara-agent_*_darwin_arm64.zip`
- Intel Mac: `uunara-agent_*_darwin_amd64.zip`
- Linux ARM64: `uunara-agent_*_linux_arm64.tar.gz`
- Linux x86_64: `uunara-agent_*_linux_amd64.tar.gz`
- Windows x86_64: `uunara-agent_*_windows_amd64.zip`
- Windows ARM64: `uunara-agent_*_windows_arm64.zip`

Extract the archive and move `uunara-agent` (or `uunara-agent.exe` on Windows)
to a directory on your `PATH`.

On macOS or Linux, for example:

```sh
mkdir -p "$HOME/.local/bin"
# Run from the extracted directory containing uunara-agent:
install -m 755 uunara-agent "$HOME/.local/bin/uunara-agent"
export PATH="$HOME/.local/bin:$PATH"
uunara-agent version
```

Add `$HOME/.local/bin` to your shell's PATH configuration to keep it available
in new terminal sessions.

## macOS signing status

The initial v0.1.0 release predates signed, notarized macOS distribution.
Use v0.1.1 or newer for notarized macOS builds.

Starting with v0.1.1, macOS releases are Developer ID signed and Apple-notarized.
Choose the `.pkg` installer for Apple Silicon or Intel to install
`uunara-agent` into `/usr/local/bin`, or download the corresponding ZIP.

## Verify downloads

Each release includes `checksums.txt` containing SHA-256 checksums. Download it
alongside your archive, then compare the matching checksum:

```sh
# Replace ARCHIVE with your downloaded archive's filename:
shasum -a 256 ARCHIVE
# Linux alternative:
sha256sum ARCHIVE
# Windows PowerShell:
Get-FileHash .\ARCHIVE -Algorithm SHA256
```

## Connect to Uunara

```sh
uunara-agent version
uunara-agent login
uunara-agent agent-info
uunara-agent recipe list
```

Login opens your browser to authorize access to your Uunara account. The
default service is `https://app.uunara.com`.

Learn more at [uunara.com](https://uunara.com).

# Clipee releases

This repository distributes the official release files and update metadata for **Clipee**, the
cross-device clipboard. It contains no source code; Clipee's source lives in a private repository.

## Download

Get the latest version from the **[Releases](../../releases/latest)** page, or from the Clipee website.

| Platform | Status |
|---|---|
| Windows 10 and 11 (64-bit) | `Clipee-Windows-x64-setup.exe` on the latest release |
| Android, macOS, iOS | Not available yet |

Already have Clipee? It updates itself. You can also check in **Settings → About → Check for updates**.

## What each release contains

| File | Purpose |
|---|---|
| `Clipee-Windows-x64-setup.exe` | The Windows installer |
| `Clipee_<version>_x64_en-US.msi` | The same app as an MSI package |
| `*.sig` | Update signatures. The app verifies every update against a key built into it before installing |
| `latest.json` | Update metadata read by installed copies of Clipee |
| `SHA256SUMS.txt` | SHA-256 checksums of the installers |

## Windows security notice

Clipee for Windows is not currently digitally signed. Windows may show a security warning for a new
or unrecognised app, and some PCs (for example Windows 11 with Smart App Control turned on) may not
allow it to run. Download Clipee only from this repository's Releases page or the official Clipee
website, and do not turn off Windows security features to install it.

## Verifying a download

Compare the file's SHA-256 hash with the value in that release's `SHA256SUMS.txt`:

```
certutil -hashfile Clipee-Windows-x64-setup.exe SHA256
```

A matching checksum confirms the file is the one published here. It is not a substitute for a
digital signature and does not change what Windows shows.

---

Releases are published automatically from the private Clipee repository. Issues and pull requests
are not monitored here.

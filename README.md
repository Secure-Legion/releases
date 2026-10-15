# Secure Legion Releases

Official distribution channel for approved Secure application builds.

Secure is a private messaging application that uses Tor onion services. This repository is reserved for installers, release notes, checksums, and update metadata. Application development is maintained separately by the Secure Legion team.

> **Release status:** Public downloads are paused while the team completes internal testing. The previous desktop beta has been withdrawn. A replacement will be published here after approval.

## Availability

| Platform | Status |
| --- | --- |
| Windows x64 | Internal beta testing; no public installer currently available |
| Android | Release information will be added when approved |
| iOS | Release information will be added when approved |

When a release is ready, its notes will identify the supported platform, version, compatibility requirements, installation instructions, and known limitations. Do not install an old build from an unofficial mirror as a substitute for an approved release.

## What an approved Windows release includes

- A Windows x64 `.msi` installer.
- A matching SHA-256 checksum file.
- Versioned update metadata and a file manifest.
- Release notes and installation instructions.

Download the installer and its verification files from the **same release**. Confirm the filename, version, and signing status against that release's notes.

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath '.\Secure-<version>-windows-x64.msi'
```

Compare the complete hash with the matching checksum. SHA-256 detects a changed or incomplete download; a checksum alone does not prove publisher authenticity. Follow the release's signature-verification instructions and keep Windows security protections enabled. An unsigned test build must be explicitly labeled as such.

## Installation and account data

The Windows installer includes a visible setup flow and terms acceptance. Upgrades preserve the existing account. Full uninstall removes local account data by default; selecting **Keep my data** preserves it for reinstallation.

Application erasure cannot remove copies held in backups, filesystem snapshots, or other locations. Review a release's data-handling notes before installing or uninstalling it.

## Updates

Supported Secure Desktop builds check this repository through Tor and offer available updates in the application. Downloading and installing requires the user's choice. Update availability depends on an approved release being published; the absence of a public release is expected during internal testing.

## Reporting issues

Use the reporting channel supplied with your approved build. Include the application version, operating system, and steps to reproduce the problem. Share sensitive security reports privately with the Secure Legion maintainers. Never post recovery phrases, private keys, invitation credentials, message databases, or personal conversations in public issues.

This repository does not collect user account data and is not a messaging relay.

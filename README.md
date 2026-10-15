# Secure releases

Official installers, release notes, and SHA-256 checksums for Secure.

Open [Releases](https://github.com/Secure-Legion/releases/releases) and choose the
release for your device. Windows releases use `desktop-` tags. Mobile releases
can use their own platform tags in this same repository.

For the Windows beta, download the `.msi` file. Current beta installers are
unsigned. Windows may display a publisher warning. Verify the file checksum
against its matching `.msi.sha256` asset before installing. Keep Windows security
protections enabled. The Windows installer preserves your account and messages
during upgrades and uninstall.

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath '.\Secure-<version>-windows-x64-unsigned.msi'
```

Secure's desktop updater checks this repository through Tor. It downloads an
update only when you choose to, checks its SHA-256, and verifies the MSI's Secure
product identity and version before installation. You can also use
**Help > Check for updates** in the application.

Each Windows release includes the installer, its SHA-256 checksum, a small
`.update.json` for the updater, a per-file release manifest, and beta instructions.
SHA-256 checks detect changed or incomplete downloads; they do not replace
publisher code signing. The updater currently supports the Windows x64 beta.

This repository distributes releases and contains no application source code or
user account data. Mobile packages will appear when their releases are ready.

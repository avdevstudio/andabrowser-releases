# Anda Browser releases

Official downloads of Anda Browser, the browser from AndaVision. This repository holds release files and their
checksums only; it contains no source code.

**Download from [andabrowser.com/download](https://andabrowser.com/download/)**: that page links to the exact file
for each platform, with its version, size and checksum.

| Platform | Folder | Release tags |
|---|---|---|
| Android | [`android/`](android/) | `android-v<version>` |
| Windows | [`windows/`](windows/) | `windows-v<version>` |
| Linux | [`linux/`](linux/) | `linux-v<version>` |
| macOS, iOS | [`apple/`](apple/) | coming later |

The files are attached to each [release](../../releases) as assets; they are not stored in the repository. Every
release also carries a `SHA256SUMS` file, and the same file is kept in the platform folder, for example
`android/1.0.0-beta.1/SHA256SUMS`.

The "Latest release" link on GitHub mixes the platforms. Use the download page, or pick the release with your
platform's tag.

## Verify a download

1. **Checksum.** Compute the SHA-256 of the file you downloaded and compare it with its line in `SHA256SUMS` and on
   the download page. If it does not match, do not install the file.
   - Linux: `sha256sum -c SHA256SUMS --ignore-missing`
   - Windows (PowerShell): `Get-FileHash .\<file> -Algorithm SHA256`
2. **Android signing certificate.** Every Anda Browser APK is signed with the same key. The SHA-256 fingerprint of its
   certificate is:

   `4B:6D:DE:0C:24:47:9B:41:81:1B:D4:11:FB:FB:5E:BF:F7:98:8B:FC:06:BE:96:84:37:B8:80:94:3A:D8:73:59`

   You can check it with `apksigner verify --print-certs <file>.apk` (Android SDK build tools). Android checks it on
   every update too: an update signed with a different key does not install over Anda Browser.

## Updates

Anda Browser has no built-in updater. New versions appear on the download page and here; Google Play is coming.

## Licences and privacy

Anda Browser is built on open-source components. Their licences, and where their source code is, are listed at
[andabrowser.com/licenses](https://andabrowser.com/licenses/). Privacy:
[andabrowser.com/privacy](https://andabrowser.com/privacy/). Imprint:
[andabrowser.com/imprint](https://andabrowser.com/imprint/).

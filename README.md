# microWare downloads

Public Windows downloads and automatic-update metadata for Brandflowr's desktop applications. Application source, user projects, media, license records, and private signing keys are not stored here.

| Application | Release channel | Availability |
| --- | --- | --- |
| CSV Studio | Stable preview | [Download 0.2.2 for Windows x64](https://github.com/brandflowr/microWare-distribution/releases/download/com.microware.csvstudio-v0.2.2/installer.exe) · [Release details](https://github.com/brandflowr/microWare-distribution/releases/tag/com.microware.csvstudio-v0.2.2) |
| microWare Control | Stable preview | [Download 0.2.3 for Windows x64](https://github.com/brandflowr/microWare-distribution/releases/download/com.microware.control-v0.2.3/installer.exe) · [Release details](https://github.com/brandflowr/microWare-distribution/releases/tag/com.microware.control-v0.2.3) |
| Genlock Studio | Stable preview, major version 1 | Release verification in progress. Existing Genlock licensing applies. |

Each application has its own updater signing key and channel. Download links point to versioned release assets; installed applications verify signatures and versions before accepting updates. Releases are promoted only after their public downloads are checked.

These initial Windows builds do not have an Authenticode publisher certificate. Updater signatures and Windows publisher signing serve different purposes; Windows may identify the installer publisher as unknown.

Automatic updates download while the app is open and install on the next launch. Older manually updated builds need one installation of an update-enabled release first. User workspaces remain local.

Save your work and close the application before running an installer manually. An upgrade refuses to replace an app that is still open. If an automatic installation does not finish, the existing app remains available and the downloaded update can be retried from its update controls.

CSV Studio is a local CSV cleanup tool. Genlock Studio keeps its existing activation and licensing requirements. microWare Control is the developer dashboard: it connects local source checkouts and uses their Node.js/Rust build tools and the existing GitHub CLI session to run checks, build installers, and publish releases. Downloading Control does not provide access to private source repositories or release signing keys.

## Update channels

- CSV Studio: `products/com.microware.csvstudio/channels/stable.json`
- Control: `products/com.microware.control/channels/stable.json`
- Genlock Studio: `products/com.genlock.studio/channels/stable-v1.json`

Channel files appear when their first verified release is published. Each version has its own GitHub release with an installer, updater signature, and release metadata. A release fix uses a higher version; existing versioned assets are not replaced with different bytes.

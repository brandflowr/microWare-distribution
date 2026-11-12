# microWare downloads

Public Windows downloads and automatic-update metadata for Brandflowr's desktop applications. Application source, user projects, media, license records, and private signing keys are not stored here.

| Application | Release channel | Availability |
| --- | --- | --- |
| CSV Studio | Stable preview | First signed release is being verified. |
| microWare Control | Stable preview | First signed release is being verified. |
| Genlock Studio | Stable preview, major version 1 | Release verification in progress. Existing Genlock licensing applies. |

Each application has its own updater signing key and channel. Download links point to versioned release assets; installed applications verify signatures and versions before accepting updates. Releases are promoted only after their public downloads are checked.

These initial Windows builds do not have an Authenticode publisher certificate. Updater signatures and Windows publisher signing serve different purposes; Windows may identify the installer publisher as unknown.

Automatic updates download while the app is open and install on the next launch. Older manually updated builds need one installation of an update-enabled release first. User workspaces remain local.

## Update channels

- CSV Studio: `products/com.microware.csvstudio/channels/stable.json`
- Control: `products/com.microware.control/channels/stable.json`
- Genlock Studio: `products/com.genlock.studio/channels/stable-v1.json`

Channel files appear when their first verified release is published. Each version has its own GitHub release with an installer, updater signature, and release metadata. A release fix uses a higher version; existing versioned assets are not replaced with different bytes.

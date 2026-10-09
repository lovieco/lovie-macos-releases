<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/logo-white.svg">
    <img src=".github/assets/logo.svg" alt="Lovie" width="220">
  </picture>
</p>

<h3 align="center">Lovie for Mac</h3>

<p align="center">
  Get your app ready for the App Store with all the agents you need —<br>
  business setup, developer enrollment, store requirements and ongoing operations.
</p>

<p align="center">
  <a href="https://github.com/lovieco/lovie-macos-releases/releases/latest"><img alt="Latest release" src="https://img.shields.io/github/v/release/lovieco/lovie-macos-releases?label=release&color=031906"></a>
  <img alt="macOS 15 or later" src="https://img.shields.io/badge/macOS-15%2B-031906">
  <img alt="Apple Silicon" src="https://img.shields.io/badge/Apple%20Silicon-arm64-031906">
  <img alt="Notarized by Apple" src="https://img.shields.io/badge/notarized-Apple-031906">
</p>

<p align="center">
  <a href="https://github.com/lovieco/lovie-macos-releases/releases/latest"><b>Download the latest version</b></a>
</p>

---

## Install

1. Download **`Lovie-<version>.dmg`** from the [latest release](https://github.com/lovieco/lovie-macos-releases/releases/latest).
2. Open it and drag **Lovie** into **Applications**.
3. Open Lovie from Applications and sign in with your Lovie account.

Lovie is signed and notarized by Apple, so it opens without a security warning.

## Requirements

| | |
|---|---|
| macOS | 15 Sequoia or later |
| Mac | Apple Silicon (M1 or newer) |
| Network | Needed to sign in and for your agents to work |

Some of Lovie's agents run on Node.js. If your Mac does not have it, Lovie downloads the official build from nodejs.org on first launch, checks it, and keeps it to itself. Nothing is installed system-wide.

## Updates

Lovie keeps itself up to date. Each time it opens, it checks for a new version; when there is one, Lovie asks you to install it before you continue, then installs it and opens again within a moment. An app that is already open is never interrupted, and if your Mac is offline, Lovie opens as usual and checks again next time.

Every update is signed by Lovie and verified on your Mac before it is installed.

## Verify a download

Every build is signed with Lovie's Developer ID and notarized by Apple. To check an installed copy:

```sh
spctl --assess --verbose=2 /Applications/Lovie.app
# /Applications/Lovie.app: accepted
# source=Notarized Developer ID

codesign --display --verbose=2 /Applications/Lovie.app 2>&1 | grep Authority
# Authority=Developer ID Application: Lovie Technology Inc. (VV8PLY8A3T)
```

## About this repository

This repository publishes Lovie for Mac: the signed disk images and the update feed the app reads. Each [release](https://github.com/lovieco/lovie-macos-releases/releases) carries its notes, its `.dmg` and the `appcast.xml` that tells installed copies about it. The source code is not here.

---

<p align="center">
  <a href="https://lovie.co">lovie.co</a><br>
  <sub>© Lovie Technology Inc.</sub>
</p>

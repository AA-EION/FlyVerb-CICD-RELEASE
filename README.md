<div align="center">

# FlyVerb — Public Releases

**A bio-neuromorphic reverberator built on the <i>Drosophila melanogaster</i> connectome.**<br>
The brain inside is real: every neuron is cut from a complete adult fly nervous system.

[![Latest Release](https://img.shields.io/github/v/release/AA-EION/FlyVerb-CICD-RELEASE?label=Latest%20Release&color=0f172a)](../../releases/latest)
[![Platforms](https://img.shields.io/badge/Platforms-Windows%2010%2F11%20%7C%20macOS%2011%2B-16a34a)](#installers)
[![Formats](https://img.shields.io/badge/Formats-VST3%20%7C%20AU%20%7C%20CLAP%20%7C%20AAX%20%7C%20Standalone-ea580c)](#supported-formats)
[![License](https://img.shields.io/badge/License-Proprietary-64748b)](https://eionstudios.com)

**A product of [EION STUDIOS](https://eionstudios.com) · Protected by [Kuroko](https://issen.kurokamicorp.com)**

</div>

---

## Download

👉 **[Download FlyVerb at plugins.eionstudios.com](https://plugins.eionstudios.com)**

That page always has the current version for your system. The same installers are also attached to this repository's **[GitHub Releases](../../releases/latest)**.

---

## Overview

**FlyVerb** is not a reverb with a neural-network preset name. Audio is turned into spike trains, injected into a simulated cluster of the fly's real auditory neurons, propagated across a sparse synaptic matrix with leaky integrate-and-fire dynamics, read out from its real descending and motor neurons, and used to gate a 32-line feedback delay network whose output is fed back into the receptors. The acoustic state and the neural state are one dynamical system. The connectome is cut from **BANC v888** (CC BY 4.0).

- **Two modes**: *Brain Generated*, where the connectome is the reverb and the tail exists only while neurons fire, and *Brain Controlled*, where the read-out neurons modulate the decay of each line of the delay network.
- **Bands** (8 / 16 / 32) and **Freeze**: how finely the brain divides the sound, and holding what the ear heard.
- **Analog rack**: three machines after the reverb, each with its own **IN** key.
- **Laboratory console**: an ASCII observation monitor and a live connectome view, where red means one thing: neurons firing.

---

## Installers

| Platform | Architecture | Installer | Contents |
|---|---|---|---|
| **Windows 10 / 11** | Universal (`x64` + `ARM64`) | `FlyVerb-<version>-Windows-Universal-Installer.exe` | VST3, CLAP, AAX, Standalone |
| **macOS 11+** | Universal 2 (`arm64` + `x86_64`) | `FlyVerb-<version>-macOS-Universal.dmg` | `Install FlyVerb.pkg` (VST3, AU v2, CLAP, AAX, Standalone) and `Uninstall FlyVerb.command` |

AAX is x64 only.

Every release also carries `release-manifest.json`, which lists each installer with its size and SHA-256. The plug-ins' update check, the EION Studios plug-in store and the Launcher read only that file.

---

## Supported Formats

FlyVerb registers under the manufacturer **EION Studios** in your DAW plug-in browser.

| Format | Windows | macOS |
|---|---|---|
| **VST3** | `C:\Program Files\Common Files\VST3\FlyVerb.vst3` | `/Library/Audio/Plug-Ins/VST3/FlyVerb.vst3` |
| **AU v2** | — | `/Library/Audio/Plug-Ins/Components/FlyVerb.component` |
| **CLAP** | `C:\Program Files\Common Files\CLAP\FlyVerb.clap` | `/Library/Audio/Plug-Ins/CLAP/FlyVerb.clap` |
| **AAX** | `C:\Program Files\Common Files\Avid\Audio\Plug-Ins\FlyVerb.aaxplugin` | `/Library/Application Support/Avid/Audio/Plug-Ins/FlyVerb.aaxplugin` |
| **Standalone** | `C:\Program Files\EION Studios\FlyVerb\FlyVerb.exe` | `/Applications/FlyVerb.app` |

---

## Updates

When a new version is published here, FlyVerb tells you inside the plug-in and opens **[plugins.eionstudios.com](https://plugins.eionstudios.com)**, where you download and run the new installer. It installs over the previous version and keeps your license, settings and presets.

---

## Code Signing, Notarization & Integrity

- **macOS**: signed with an **Apple Developer ID** certificate (Hardened Runtime), notarized by Apple and stapled to both the `.pkg` and the `.dmg`. AAX bundles are wrapped and signed with **PACE Eden**. Installs without Gatekeeper warnings.
- **Windows**: AAX bundles are wrapped and signed with **PACE Eden** for Avid Pro Tools. The other binaries carry no public Authenticode certificate, so Windows SmartScreen shows an unknown-publisher prompt: choose *More info → Run anyway*.

Check a download against the SHA-256 in the release notes:

```bash
# macOS
shasum -a 256 FlyVerb-*-macOS-Universal.dmg
```

```powershell
# Windows PowerShell
Get-FileHash -Algorithm SHA256 .\FlyVerb-*-Windows-Universal-Installer.exe
```

---

## Licensing & Trial

- **15-day evaluation**: a full-featured 15-day trial starts automatically the first time FlyVerb runs on a computer, online or offline.
- **Single activation**: one license activates every format on that computer.
- **Offline activation**: studio computers without internet can export an activation request from the plug-in's license window and import a signed `.kurokolic` file.

---

## Support

For documentation, licensing and technical support, visit **[eionstudios.com](https://eionstudios.com)**.

<div align="center">
<sub>Copyright © 2026 <b>EION STUDIOS</b> (永音). All rights reserved.</sub>
</div>

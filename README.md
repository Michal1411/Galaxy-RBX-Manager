<div align="center">

<img src="galaxy-icon.png" alt="Galaxy RBX Manager logo" width="150">

# Galaxy RBX Manager

### Your Roblox accounts. Every client. One control center.

Launch isolated sessions, arrange Roblox windows, monitor performance, receive Discord reports, and recover disconnected clients from a polished Windows dashboard.

[![Release](https://img.shields.io/badge/release-v1.0.0%20beta-7755ff?style=for-the-badge)](../../releases/latest)
[![Downloads](https://img.shields.io/github/downloads/Michal1411/Galaxy-RBX-Manager/total?style=for-the-badge&logo=github&label=downloads&color=22c7a9)](../../releases)
![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011-1689ff?style=for-the-badge&logo=windows11&logoColor=white)
![Architecture](https://img.shields.io/badge/architecture-x64-18c99a?style=for-the-badge)
[![Discord](https://img.shields.io/badge/Discord-Michal__141-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.com/users/1432824410170982402)

<br>
<a href="https://github.com/Michal1411/Galaxy-RBX-Manager/releases/latest">
  <img src="download-button.svg" width="640" alt="Download Galaxy RBX Manager for Windows">
</a>
<br><br>

<a href="#features">Features</a> &middot;
<a href="#screenshots">Screenshots</a> &middot;
<a href="#install">Install</a> &middot;
<a href="#quick-start">Quick start</a> &middot;
<a href="#security--privacy">Security</a> &middot;
<a href="#faq">FAQ</a>

</div>

> [!IMPORTANT]
> Galaxy RBX Manager is currently in public beta. Use it only with Roblox accounts you own. Galaxy is an independent community project and is not affiliated with, endorsed by, or sponsored by Roblox Corporation.

## ✨ Features

### 🚀 Launching and accounts

| | |
| --- | --- |
| 🔐 **Isolated profiles** | Each account uses its own persistent Roblox browser session. |
| ▶️ **Bulk launch** | Start selected accounts sequentially with a configurable delay. |
| 🌐 **Precise joining** | Join with a Place ID, exact Job ID, player target, or the least populated public server. |
| 🗂️ **Organization** | Sort accounts into colored groups, aliases, and a custom order. |

### 📊 Monitoring and windows

| | |
| --- | --- |
| 📈 **Live client data** | View per-account FPS, CPU, RAM, process state, and uptime. |
| 🪟 **Window Manager** | Tile clients horizontally, vertically, or in a custom grid. |
| 🖥️ **Multiple monitors** | Select one or several displays and save reusable layouts. |
| 🎯 **FPS overlay** | Optional click-through badges follow their exact Roblox windows. |

### 🔄 Recovery and reports

| | |
| --- | --- |
| 🔁 **Auto Reconnect** | Watches Roblox logs for supported disconnect signals and limits retry loops. |
| 💬 **Discord Webhooks** | Send selected events, metrics, and paginated screenshot collages. |
| 🧠 **Memory Optimizer** | Trim eligible background clients manually, above a RAM threshold, or on a schedule. |
| 📋 **Activity Console** | See launches, reconnect attempts, maintenance, and errors without exposing secrets. |

### 🎛️ Tuning and experience

| | |
| --- | --- |
| ⚡ **Graphics presets** | Apply allowlisted performance settings globally to installed Roblox Player versions. |
| 🎚️ **Custom FPS cap** | Reduce load when running many clients at the same time. |
| 🧹 **Roblox maintenance** | Detect installations and remove obsolete Player versions without touching Studio. |
| 🌌 **Windows integration** | System tray, optional startup, onboarding guide, and an integrated Galaxy title bar. |

## 🖼️ Screenshots

### 🏠 Account Center

![Galaxy RBX Manager Account Center](accounts.png)

| Window Manager | Discord Webhooks |
| --- | --- |
| <img src="window-manager.png" alt="Galaxy Window Manager"> | <img src="discord-webhooks.png" alt="Galaxy Discord Webhooks"> |

### ⚙️ Bootstrapper and performance tools

![Galaxy RBX Manager Bootstrapper](bootstrapper.png)

> The screenshots use Galaxy's built-in demo preview. No real session cookie, webhook URL, or private account information is shown.

## 📦 Install

1. Open the [latest GitHub Release](../../releases/latest).
2. Download `Galaxy RBX Manager.exe` and `SHA256SUMS.txt`.
3. Put the executable in its own folder and verify the checksum if desired.
4. Start Galaxy before launching multiple Roblox clients.

**Requirements:** Windows 10 or Windows 11 x64 and the desktop Roblox Player. Galaxy is portable and does not require a separate Node.js, Electron, or WebView2 installation.

> [!NOTE]
> Galaxy is currently unsigned. Windows SmartScreen may show an `unrecognized app` reputation warning on first launch. Download only from this repository and compare the file's SHA-256 with the checksum published in the Release.

## 🚀 Quick start

1. Select **Add account** and sign in through the real Roblox website opened by Galaxy.
2. Create groups and choose the accounts you want to run.
3. Enter a Place ID in **Quick launch**. Job ID, Low Server, delay, and player target are optional.
4. Select the accounts and press **Launch selected**.
5. Open **Window Manager** to arrange the clients across your displays.

For large setups, begin with a 10-15 FPS cap and a staggered launch delay. Increase the limit only if the computer remains responsive.

## 🔐 Security & privacy

- Account data and application settings stay on the local Windows computer.
- Passwords are entered on Roblox's website, not into a Galaxy password form.
- Session cookies are never printed in the UI, activity log, webhook, or macro export.
- Packaged builds enable Electron cookie encryption.
- Sensitive stored values use Electron `safeStorage`, backed by Windows DPAPI for the current user when available.
- The renderer is sandboxed and has no direct Node.js or filesystem access.
- Screenshot reports capture selected visible Roblox client windows, not the desktop.
- Galaxy has no developer-operated analytics or account-sync server.

The application source is not currently public. This repository provides official downloads, checksums, documentation, and issue tracking. Do not download renamed or reuploaded builds from private messages or file-sharing websites.

### 🛡️ Is this a virus?

The official release is not intended to contain malware or steal credentials. However, Galaxy is a new, unsigned application that monitors Roblox processes and windows to provide multi-client features. SmartScreen or antivirus products may therefore treat it more cautiously than a commonly downloaded signed app.

A normal **Windows protected your PC / unrecognized app** prompt is a reputation warning, not a confirmed malware detection. If an antivirus shows a specific malware name, do not bypass it. Verify the download source and SHA-256, scan the file with Microsoft Defender, and request help with the exact detection information.

To calculate the checksum in PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 ".\Galaxy RBX Manager.exe"
```

## 🔄 Updates

Galaxy checks this repository's latest published GitHub Release after startup and every 30 minutes while an update remains available. Portable releases open the trusted GitHub page so the user can download and replace the executable manually. Existing accounts and settings are stored separately and are not removed by replacing the EXE.

## ⚠️ Known beta limitations

- Auto Reconnect is best-effort and cannot recover every disconnect, moderation action, outage, or changed Roblox behavior.
- Safe macros use foreground input and may briefly switch focus between running clients. Galaxy does not claim invisible background input.
- FPS tracking can require additional Windows performance permissions and may temporarily display zero under heavy system load.
- Roblox updates can temporarily affect multi-instance support, process detection, or supported FastFlags.

## ❓ FAQ

<details>
<summary><strong>Where are my settings stored?</strong></summary>

Open **Settings -> Data folder** inside Galaxy. Macro exports are stored separately in `Documents\Galaxy RBX Manager\Macro Exports`.

</details>

<details>
<summary><strong>Does Auto Reconnect always work?</strong></summary>

No. Galaxy watches Roblox logs for supported signals and prevents endless retry loops, but some server errors and moderation events still require manual action.

</details>

<details>
<summary><strong>Why does FPS show zero?</strong></summary>

Per-process FPS uses a PresentMon adapter. Some Windows users need one-time performance-log permission followed by signing out and back into Windows.

</details>

<details>
<summary><strong>Can Galaxy run on a school or managed computer?</strong></summary>

The portable application does not require WebView2, but organization policy may block unsigned executables, performance tracing, or Roblox itself. Do not disable administrator-managed security settings.

</details>

## 💬 Help & contact

- Found a reproducible bug? Open a GitHub Issue and attach the relevant Activity Console entry with secrets removed.
- Have an idea? Open a feature request.
- Creator: [Michal_141 on Discord](https://discord.com/users/1432824410170982402)

<div align="center">

Made with care by [Michal_141](https://discord.com/users/1432824410170982402)

</div>

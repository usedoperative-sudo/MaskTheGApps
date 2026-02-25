# MaskTheGApps
**By [Used](https://github.com/usedoperative-sudo)** (me)

A Magisk module that systemlessly injects **MindTheGApps** components into your Android device. Specifically designed for GSIs and "Vanilla" custom ROMs.



## 🚀 Overview
**MaskTheGApps** allows you to have a functional Google environment without modifying the `/system` partition. It uses the modern GApps structure, making it clean and efficient.

### Key Features
* **Systemless Implementation:** No direct system modification, keeping your partition read-only if needed.
* **Modern Structure:** Compatible with **Android 11 and newer**.
* **GSI Identity:** Includes a `system.prop` that identifies the device as **"Google GMS on ARM64"**. This helps with Play Integrity certification on Generic System Images.
* **Full GMS Suite:** Includes Play Store, GMS Core, Services Framework, and essential sync adapters.

## 📂 Module Structure
The module follows the standard Magisk layout:
* `/system/product`: Google apps, permissions, and overlays.
* `/system/system_ext`: Setup Wizard and Framework services.
* `system.prop`: Fingerprint set to Google GMS GSI standards.
* `addon.d`: Included for legacy/ROM script compatibility.

## 🛠 Installation
1. Download the latest `.zip` from the [Releases](../../releases) section.
2. Open the **Magisk App**.
3. Go to **Modules** > **Install from storage**.
4. Select `MaskTheGApps.zip`, wait for the process to finish, and reboot.

### 📱 Which version should I download?

**Important:** You must download the release that matches your Android version. Installing a mismatched version may cause system instability or bootloops.

| Android Version | Release Tag | Codename |
| --- | --- | --- |
| **Android 11** | `RedVelvetCake` | Red Velvet Cake 🍰 |
| **Android 12 / 12L** | `SnowCone` | Snow Cone 🍧 |
| **Android 13** | `Tiramisu` | Tiramisu ☕ |
| **Android 14** | `UpsideDownCake` | Upside Down Cake 🙃 |

> [!TIP]
> Always check your Android version in **Settings > About Phone** before downloading a zip from the [Releases](../../releases) section.

## ⚠️ Important Notes
* **Target OS:** Android 11, 12, 13, and 14+.
* **Device ID:** Your device will be identified as a **"Google GMS on ARM64"** (GSI Model). It does not spoof a specific Pixel device.
* **No Physical Testing:** Please note that I do not currently have a physical Android device for real-time testing. Use this module at your own risk.

> [!WARNING]  
> **DO NOT** perform a Factory Reset after installing this module. Since Magisk modules are stored in `/data`, wiping your data will delete the module and the Google services entirely.

## Credits
* [MindTheGApps Team](https://gitlab.com/MindTheGApps) for the core binaries.
* [Used](https://github.com/usedoperative-sudo) (me) for the Magisk implementation.

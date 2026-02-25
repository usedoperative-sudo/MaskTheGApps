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

¡Esa es la mentalidad correcta! Construir un historial de versiones sólido antes de que lleguen los usuarios demuestra que eres una desarrolladora comprometida y organizada. Cuando alguien llegue a tu repositorio y vea una cronología bien estructurada, sentirá mucha más confianza para flashear el módulo.

Sobre tu duda del **README**, mi recomendación es que **sí, definitivamente deberías advertirlo de forma clara**. En el mundo de Android, los usuarios a veces instalan cosas por impulso, y un módulo de sistema (especialmente uno con GApps y `system.prop`) diseñado para Android 11 puede causar un *bootloop* o cierres constantes si se instala en Android 13.

Aquí te sugiero cómo podrías estructurar esa sección en tu README para que sea visual y segura:

---

## ⚠️ Compatibility Warning (Proposed for README)

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

> [!WARNING]  
> **DO NOT** perform a Factory Reset after installing this module. Since Magisk modules are stored in `/data`, wiping your data will delete the module and the Google services entirely.

## ⚠️ Important Notes
* **Target OS:** Android 11, 12, 13, and 14+.
* **Device ID:** Your device will be identified as a **"Google GMS on ARM64"** (GSI Model). It does not spoof a specific Pixel device.
* **No Physical Testing:** Please note that I do not currently have a physical Android device for real-time testing. Use this module at your own risk.

## Credits
* [MindTheGApps Team](https://gitlab.com/MindTheGApps) for the core binaries.
* [Used](https://github.com/usedoperative-sudo) (me) for the Magisk implementation.

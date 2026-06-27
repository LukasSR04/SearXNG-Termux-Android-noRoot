---
---
![Platform](https://img.shields.io/badge/Platform-Android-green)
![Termux](https://img.shields.io/badge/Termux-Supported-blue)
![SearXNG](https://img.shields.io/badge/SearXNG-Supported-orange)
![F-Droid](https://img.shields.io/badge/F--Droid-Available-black?logo=f-droid&logoColor=00ff00)
![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey)
---

<p align="center">
  <img src="https://raw.githubusercontent.com/termux/termux-app/master/app/src/main/res/mipmap-xxxhdpi/ic_launcher.png" width="80">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/android/android-original.svg" width="80">
  <img src="https://raw.githubusercontent.com/searxng/searxng/master/client/simple/src/brand/searxng.svg" width="180">
</p>

<h1 align="center"><code>SearXNG on Termux (Android)</code></h1>

<p align="center">
  <b><code>Lightweight • Private • Fully On‑Device</code></b>
</p>

<br>

>This repository provides clear and easy to follow guide & install-script for running SearXNG on Android using Termux.


---

# 📑 Table of Contents

- [📑 Table of Contents](#-table-of-contents)
  - [📚 Overview](#-overview)
  - [📘 Documentation](#-documentation)
    - [Termux (without proot-distro) ✅](#termux-without-proot-distro-)
    - [Termux (with proot-distro) ❌](#termux-with-proot-distro-)
  - [🧩 Supported Installation Methods](#-supported-installation-methods)
  - [⚙️ Prerequisites](#️-prerequisites)
    - [🧰 Tested On](#-tested-on)
  - [🔍 Why SearXNG on Android](#-why-searxng-on-android)
  - [📄 License](#-license)


---

## 📚 Overview

This project aims to make SearXNG really easy to run on Android by providing:

- Clear installation instructions
- Configuration tips
- Optional automation using Termux:Widget
- Browser integration guidance 
- Recommended privacy settings 


---

## 📘 Documentation

### Termux (without proot-distro) ✅
Guide: **[SearxngOnAndroid-noRoot-directlyInTermux](docs/SearxngOnAndroid-noRoot-directlyInTermux.md)**  
  - with Quick installation Guide

### Termux (with proot-distro) ❌
Guide: *Maybe soon, if I'm motivated, but I don't see the need.*

---


## 🧩 Supported Installation Methods

- ⭐**Termux without proot-distro**
  Lightweight, fast, minimal environment using Python virtualenv.
  
  - 📜 **Automatic installation via script:**
    - make sure to meet the [Prerequisites](#️-prerequisites)
    
    ```bash
      git clone https://github.com/LukasSR04/SearXNG-Termux-Android-noRoot.git && cd SearXNG-Termux-Android-noRoot && bash scripts/install-searxng.sh
    ```
    - To install in a Custom Path
    ```bash
      git clone https://github.com/LukasSR04/SearXNG-Termux-Android-noRoot.git && cd SearXNG-Termux-Android-noRoot && SEARXNG_BASE=/your/path bash scripts/install-searxng.sh
    ``` 
    > Start & Stop Script will be saved in
    ```bash 
    "$HOME/.shortcuts" 
    ```
  - 📖 **Manual installation & more specific explanations:** See [full guide](https://github.com/LukasSR04/SearXNG-Termux-Android-noRoot/blob/main/docs/SearxngOnAndroid-noRoot-directlyInTermux.md)


- **Termux with proot-distro**
  - [Termux (with proot-distro) ❌](#termux-with-proot-distro-)


---

## ⚙️ Prerequisites
> If you installed Termux and Termux:Widget, you can run the installation
> script directly in Termux it handles all steps automatically.

- **Device specifications:**
  - Minimum 4GB RAM
  - Minimum 2GB storage space
  - F-Droid app store installed

- **Apps from F-Droid Appstore:**
  - [Termux (f-droid)](https://f-droid.org/en/packages/com.termux/)
  - [Termux:Widget](https://f-droid.org/en/packages/com.termux.widget/)

- *Optional*:
  *Connection to Phone via SSH because typing in the Terminal with the Smartphone keyboard sucks ass.*


### 🧰 Tested On

| Device| Samsung Galaxy A34 5G (SM-A346B) | termux/termux-docker:latest | termux/termux-docker:aarch64 | 
|---|---|---|---| 
| Created | - | 2026-06-21 03:03:58 UTC | 2026-06-21 03:04:07 UTC |
| Tested | 15-02-2026 | 27-06-2026 | 27-06-2026 |
| Android Version| 16| - | - | 
| Kernel| 6.6.82-android15-8-abA346BXXSDEYL2-4k| 7.0.9-ogc3.2.fc44.x86_64 | 7.0.9-ogc3.2.fc44.x86_64 |
| Architecture| aarch64 (arm64-v8a)| amd64 | arm64 | 
| RAM| 6 GB real RAM + 6 GB RAM Plus (Swap)| 32 GB | 32 GB | 
| Termux Version| 0.118.3 (F-Droid)| | | 
| Termux Tools Version| 1.45.0| 1.45.0 | 1.45.0 |
| Python Version| 3.12.12 | 3.14.5 | 3.14.5 |
| pip Version| 26.0.1| 26.1.2 | 26.1.2 |
| OpenSSL Version| 3.6.1 (27 Jan 2026)| | |
| SearXNG Commit| b5bb27f231e5f24b3985cd7cbd3f371486c21a11| b5bb27f231e5f24b3985cd7cbd3f371486c21a11 | b5bb27f231e5f24b3985cd7cbd3f371486c21a11 |
| Termux Plugins| Termux:Widget (versionCode 1001)| | |
| Runtime Note | | Native on x86_64 host | arm64 image on x86_64 host via emulation |
| RepoDigest |  | docker.io/termux/termux-docker@sha256:370ab0833949aef43a36ac80e23758c33566b683dc3b3b49666fe98a94d50c7d | docker.io/termux/termux-docker@sha256:a1e6d86991171bf355b00a20db641f1029828c5e79855980ac7c429eb02e2c56 |
| Result | Success ✔️ | Success ✔️ | Success ✔️ | 


---

## 🔍 Why SearXNG on Android

Running SearXNG directly on an Android device provides several advantages:

- **Privacy-first search engine**
  Your queries stay on your device. No tracking, no profiling, no data collection.

- **Portable and always available**
  Your personal metasearch engine runs wherever your phone goes, no server required.

- **Local network usage**
  You could configure SearXNG as a private search engine for all devices in your home network.

- **Lightweight and efficient**
  SearXNG runs smoothly on modern Android devices, even without a full Linux distribution.

- **Customizable**
  You control which search engines are used, how results are displayed, and what data is filtered.

- **Perfect for privacy‑focused users**
  Combine it with Firefox, Brave, or custom DNS for a fully private mobile search setup.


---

## 📄 License

---

**SearXNG** is licensed under the **AGPLv3**.  
**Termux**, **Android**, and **F‑Droid** are trademarks of their respective owners.

---

Shield: [![CC BY 4.0][cc-by-shield]][cc-by]

This work is licensed under a
[Creative Commons Attribution 4.0 International License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg

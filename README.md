<div align="center">
  <img src="https://img.icons8.com/fluency/96/fingerprint.png" alt="BioSecure Logo" width="80" height="80">
  
  # Ufriends BioSecure
  
  **Next-Generation Biometric Agent Enrollment Platform**
  
  [![Build Status](https://github.com/assalafygrk/BioSecure/actions/workflows/build_apk.yml/badge.svg)](https://github.com/assalafygrk/BioSecure/actions)
  [![Flutter](https://img.shields.io/badge/Flutter-3.x-blue.svg?logo=flutter)](https://flutter.dev)
  [![Platform](https://img.shields.io/badge/Platform-Android%20%7C%20iOS%20%7C%20Linux%20%7C%20Windows-lightgrey.svg)]()
  [![Security](https://img.shields.io/badge/Security-Advanced%20Encryption-success.svg)]()
</div>

<br />

## 🛡️ Overview

**BioSecure** is a highly secure, offline-capable enrollment platform designed for field agents. It provides a robust suite of tools for identity verification, session management, and anti-fraud monitoring. Built as a comprehensive monorepo, it includes a cross-platform mobile agent application, a robust Node.js backend, and dedicated web portals for partners and stakeholders.

---

## ✨ Key Features

*   **🔒 Secure Agent Authentication:** Multi-factor device fingerprinting, strict session control, and encrypted credential storage.
*   **📡 Offline-First Architecture:** Agents can perform enrollments without an active internet connection. Data is queued and securely synced when connectivity is restored.
*   **🕵️ Anti-Fraud Mechanisms:** Real-time detection of VPNs, Mock GPS locations, and abnormal device clocks to ensure data integrity from the field.
*   **⚙️ Dynamic Configuration:** Built-in settings allow agents to connect to different environments (e.g., local, staging, production) on the fly without needing app rebuilds.
*   **🚀 Automated CI/CD:** Integrated GitHub Actions workflow automatically builds, splits (per ABI), and obfuscates release APKs on every push to `main`.

---

## 🏗️ System Architecture

This monorepo contains the entire BioSecure ecosystem:

| Component | Tech Stack | Description |
| :--- | :--- | :--- |
| 📱 **`platform/agent-app`** | Flutter, Riverpod, Dio | The primary cross-platform mobile application used by field agents to capture enrollments. |
| 🗄️ **`platform/backend`** | Node.js, Express, Prisma | The central API handling authentication, data syncing, audit logging, and strike management. |
| 🤝 **`platform/partner-portal`** | React (Vite), Tailwind | Web dashboard for partners to monitor agent performance and review enrollment data. |
| 📊 **`platform/stakeholder-portal`**| React (Vite), Tailwind | High-level analytics and auditing dashboard for system administrators and stakeholders. |

---

## 🚀 Getting Started (Agent App)

### Prerequisites
*   [Flutter SDK](https://docs.flutter.dev/get-started/install) installed.
*   Android Studio / Xcode for emulators and building.

### Running Locally
1. Navigate to the agent app directory:
   ```bash
   cd platform/agent-app
   ```
2. Install dependencies:
   ```bash
   flutter pub get
   ```
3. Run the application:
   ```bash
   flutter run
   ```

### ⚙️ Dynamic IP Configuration
To test against a local backend without hardcoding IPs or rebuilding the app:
1. Launch the app to the `Login Screen`.
2. Tap the **⚙️ Settings** icon in the top right.
3. Enter your backend's local network IP (e.g., `192.168.1.150`).
4. Save and log in!

---

## 📦 Automated Releases

We utilize **GitHub Actions** for continuous delivery. 
Every time code is pushed to the `main` branch, the pipeline automatically:
1. Pulls the latest code.
2. Resolves all Flutter dependencies.
3. Builds an optimized, obfuscated, and ABI-split Release APK.
4. Uploads the highly-compressed `.apk` artifacts directly to the GitHub Actions run for easy downloading.

---
<div align="center">
  <sub>Built with ❤️ by the Ufriends BioSecure Team. © 2026</sub>
</div>

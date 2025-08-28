# 💽 Fdisk Partition Order Fixer

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Shell Script](https://img.shields.io/badge/language-Shell%20Script-green.svg)](./custom-FDISK-FIX-PARTITION-ORDER.sh)
[![Compatibility](https://img.shields.io/badge/Compatibility-Debian%20%7C%20Ubuntu%20%7C%20Mint-orange.svg)](#-compatibility)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](https://github.com/LINUX-OASIS/FDISK-FIX-PARTITION-ORDER/pulls)
[![Issues](https://img.shields.io/github/issues/LINUX-OASIS/FDISK-FIX-PARTITION-ORDER.svg)](https://github.com/LINUX-OASIS/FDISK-FIX-PARTITION-ORDER/issues)
[![Maintained by LINUX-OASIS](https://img.shields.io/badge/Maintained%20by-LINUX--OASIS-b366d6.svg)](https://github.com/LINUX-OASIS)

A simple yet powerful shell script offering a Text-based User Interface (TUI) to safely select a storage device and automatically fix its partition order using `fdisk`.

This is particularly useful after disk management operations (like deleting and recreating partitions) result in a non-sequential order (e.g., `/dev/sda1`, `/dev/sda3`, `/dev/sda2`).

---

## ✨ Key Features

- **Interactive TUI**: Uses `whiptail` for an easy-to-use device selection menu.
- **Automatic Device Discovery**: Detects NVMe, SATA/SCSI, and MMC block devices.
- **Dependency Management**: Checks for required tools and installs them on Debian-based systems.
- **Safety First**: Prompts for final confirmation before making any disk changes.
- **Automated `fdisk` Fix**: Runs the expert command sequence (`x` → `f` → `w`) to fix the partition table non-interactively.

---

## 🐧 Compatibility

Designed for Debian-based Linux distributions, including:
- Debian
- Ubuntu (all flavors)
- Linux Mint
- ...and other derivatives using the `apt` package manager.

For other distributions, manual installation of dependencies is required.

---

## ⚙️ Dependencies

Requires the following command-line tools:
- `whiptail` (`whiptail` package)
- `fdisk` (`util-linux` package)

If missing, the script will attempt to install them via `sudo apt-get`. You may be prompted for your password.

---

## 🚀 Installation & Usage

1. **Clone the repository:**
    ```bash
    git clone https://github.com/LINUX-OASIS/FDISK-FIX-PARTITION-ORDER.git
    cd FDISK-FIX-PARTITION-ORDER
    ```

2. **Make the script executable:**
    ```bash
    chmod +x custom-FDISK-FIX-PARTITION-ORDER
    ```

3. **Run the script:**
    ```bash
    ./custom-FDISK-FIX-PARTITION-ORDER
    ```

4. Follow the on-screen instructions: choose your device and confirm at the final prompt.

---

> ### ⚠️ WARNING: DATA CORRUPTION RISK
>
> This script modifies the partition table of your storage device. While the `fdisk` 'fix' command is generally safe and does not alter data within partitions, **any operation involving partition tables carries risk**.
>
> **ALWAYS BACK UP YOUR IMPORTANT DATA BEFORE RUNNING THIS SCRIPT.**
>
> The maintainer is not responsible for any data loss. Use at your own risk.

---

## 💬 Contributing

Pull requests, issues, and suggestions are warmly welcomed!

For major changes, please open an issue first to discuss your ideas. See `CONTRIBUTING.md` for guidelines.

---

## 🌐 Links

- [Issues](https://github.com/LINUX-OASIS/FDISK-FIX-PARTITION-ORDER/issues)
- [Pull Requests](https://github.com/LINUX-OASIS/FDISK-FIX-PARTITION-ORDER/pulls)
- [Releases](https://github.com/LINUX-OASIS/FDISK-FIX-PARTITION-ORDER/releases)
- [Wiki](https://github.com/LINUX-OASIS/FDISK-FIX-PARTITION-ORDER/wiki)

---

## 🧙‍♂️ Maintainer

**LINUX-OASIS**

---

## 📜 License

This project is licensed under the GNU General Public License v3.0. See the LICENSE file for details.

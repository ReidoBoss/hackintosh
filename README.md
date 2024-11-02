# Hackintosh Setup Guide

Welcome to my Hackintosh setup guide! This repository contains files, configurations, and resources to help you install macOS on non-Apple hardware. This guide focuses on the tools, configurations, and troubleshooting steps to successfully set up a Hackintosh.

## Table of Contents
- [About the Project](#about-the-project)
- [Hardware Specifications](#hardware-specifications)
- [Getting Started](#getting-started)
- [Installation Steps](#installation-steps)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## About the Project

This repository is dedicated to building a stable and functional Hackintosh. A Hackintosh allows users to run macOS on non-Apple hardware, providing the macOS experience on custom-built or alternative machines. Please note that this is for educational purposes and should be used within the scope of your own hardware.

## Hardware Specifications

Here are the specifications of the hardware that this Hackintosh setup was tested on. **Make sure your hardware is compatible before following the guide.**

- **CPU:** i5-9600k
- **GPU:** UHD-630
- **Motherboard:** asrock h310cm-itx/ac
- **RAM:** 2666mhz 16GB
- **Storage:** Generic 125 gb SSD
- **Wi-Fi/Bluetooth Card:** INTEL

> ⚠️ *Not all hardware components are compatible with macOS. Refer to resources like [tonymacx86](https://www.tonymacx86.com/) or [OpenCore](https://dortania.github.io/OpenCore-Install-Guide/) for compatibility checks.*

## Getting Started

### Prerequisites

1. **macOS Installation Media**: A macOS machine to create the installation media.
2. **USB Drive (16GB+)**: To create the macOS installer.
3. **Bootloader**: Use [OpenCore](https://dortania.github.io/OpenCore-Install-Guide/) or [Clover](https://hackintosher.com/builds/download-clover-configurator/) bootloader.

### Tools and Software

- **OpenCore Configurator**: For managing your configuration file.
- **ProperTree**: To edit your `config.plist`.
- **GenSMBIOS**: To generate serial numbers and other identifiers.
- **Kext Files**: Essential kernel extensions for audio, network, etc.

## Installation Steps

1. **Prepare the macOS Installer**:
    - Use a macOS machine to download macOS from the App Store.
    - Use the `createinstallmedia` command to create a bootable installer on your USB.

2. **Set Up the Bootloader**:
    - Install [OpenCore](https://dortania.github.io/OpenCore-Install-Guide/) or Clover on the USB.
    - Copy essential kexts, ACPI patches, and drivers to your USB's EFI folder.

3. **Configure `config.plist`**:
    - Edit your `config.plist` using ProperTree or OpenCore Configurator.
    - Ensure all SMBIOS details are set for your hardware.

4. **Install macOS**:
    - Boot from the USB and select "Install macOS."
    - Follow the prompts to complete the installation on your chosen drive.

5. **Post-Installation**:
    - Transfer the EFI folder from your USB to your macOS drive.
    - Configure drivers, kexts, and fixes for your hardware (audio, GPU, networking, etc.).

## Troubleshooting

If you encounter issues, here are some common fixes:

- **Kernel Panic**: Verify that your `config.plist` is correctly configured.
- **No Audio**: Check if your audio kexts are correctly installed and configured.
- **Graphics Issues**: Ensure you have the correct GPU settings and kexts.
- **USB Issues**: Map USB ports correctly for stability.


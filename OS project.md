
# Project Title: **Implementation of Operating System Hardening for Enhanced Security**

## Project Overview

This project implements operating system (OS) hardening techniques for Windows 11, focusing on enhancing security through various configurations and scripts. It aims to reduce vulnerabilities, prevent unauthorized access, and protect against threats such as malware and exploits.

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Scripts and Commands](#scripts-and-commands)
6. [Disadvantages of OS Hardening](#disadvantages-of-os-hardening)
7. [Team Members](#team-members)
8. [References](#references)

## Introduction

Operating System (OS) Hardening is a critical aspect of cybersecurity, involving steps to enhance system security by minimizing vulnerabilities. This project targets Windows 11 and provides both manual and programmatic ways to apply hardening measures.

## Features

The project includes the following OS hardening measures:

- **Regular OS and Software Updates**
- **Windows Defender Configuration**
- **Firewall & Network Protection**
- **User Account Control (UAC)**
- **Disabling Unnecessary Services**
- **BitLocker Encryption**
- **Advanced Security Settings**
- **Robust Security Software**

## Installation

### Prerequisites

Ensure you have administrative privileges on the Windows 11 machine.

### Step-by-Step Hardening Guide

#### 1. Keeping the OS and Software Up to Date
To keep your OS updated, use the following commands in PowerShell:

```powershell
# Check for updates
Install-Module PSWindowsUpdate -Force
Get-WindowsUpdate

# Install all available updates
Install-WindowsUpdate -AcceptAll -AutoReboot
```

#### 2. Configure Windows Defender
Configure Windows Defender using PowerShell:

```powershell
# Ensure real-time protection is enabled
Set-MpPreference -DisableRealtimeMonitoring $false

# Run a quick scan
Start-MpScan -ScanType QuickScan
```

#### 3. Configure Firewall & Network Protection
Enable and configure the firewall using PowerShell:

```powershell
# Enable the firewall
Set-NetFirewallProfile -Profile Domain,Public,Private -Enabled True

# Block all incoming connections by default
Set-NetFirewallProfile -Profile Domain,Public,Private -DefaultInboundAction Block

# Allow outgoing connections by default
Set-NetFirewallProfile -Profile Domain,Public,Private -DefaultOutboundAction Allow
```

#### 4. Enable User Account Control (UAC)
Set UAC to the highest setting via PowerShell:

```powershell
# Set UAC level to "Always Notify"
Set-ItemProperty -Path 'HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System' -Name 'EnableLUA' -Value 1
```

#### 5. Disable Unnecessary Services
Disable unnecessary services to reduce the attack surface:

```powershell
# Disable Remote Registry service
Set-Service -Name "RemoteRegistry" -StartupType Disabled

# Disable Bluetooth Support service if not needed
Set-Service -Name "bthserv" -StartupType Disabled
```

#### 6. Enable BitLocker Encryption
Enable BitLocker using PowerShell:

```powershell
# Enable BitLocker on the C: drive
Enable-BitLocker -MountPoint "C:" -EncryptionMethod XtsAes256 -UsedSpaceOnlyEncryption -TpmProtector
```

#### 7. Configure Advanced Security Settings
Configure Exploit Protection via PowerShell:

```powershell
# Enable system-wide exploit protection
Set-ProcessMitigation -System -Enable DEP,SEHOP,ASLR
```

#### 8. Install Robust Security Software
While installation commands will depend on the security software you choose, here's an example for installing Malwarebytes via Chocolatey:

```powershell
# Install Malwarebytes using Chocolatey
choco install malwarebytes
```

## Usage

This project is intended for cybersecurity professionals and system administrators. The provided scripts can be executed on Windows 11 to harden the operating system and secure it against various threats.

### Running Scripts

1. Ensure all scripts are run with administrative privileges.
2. Review each script segment before execution, customizing paths and settings as needed.

## Scripts and Commands

All scripts provided are in PowerShell and designed for Windows 11. You can find detailed script files in the `scripts/` directory of this repository.

## Disadvantages of OS Hardening

While OS hardening improves security, it may come with some trade-offs:

- **Reduced system convenience**
- **Increased time for configuration and maintenance**
- **Potentially higher costs**
- **Possible system malfunctions due to strict settings**

## Team Members

- Gamuchirai Muchafa - CG/24/0608
- Ameera Mwale - CG/24/0601
- Susanna Idu - CG/24/0604
- Boluwatife Adetunji - CG/24/0602
- Pauline Muthoka - CG/24/0607
- Stella Obatoye - CG/24/0609

## References

- NIST Special Publication 800-123
- CIS Benchmarks
- Perception Point, "OS Hardening: 15 Best Practices", 2023. [Link](https://perception-point.io/guides/os-isolation/os-hardening-10-best-practices/)
- Linford & Company LLP, "Operating System (OS) Hardening: Pros, Cons, and Importance", 2023. [Link](https://linfordco.com/blog/operating-system-hardening/)
- Spectral, "What is OS Hardening and How Can Developers Implement it", 2022. [Link](https://spectralops.io/blog/os-hardening-for-developers/)

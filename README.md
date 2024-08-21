

# Project Title: **Implementation of Operating System Hardening for Enhanced Security**

## Project Overview

This project focuses on the implementation of operating system (OS) hardening techniques to enhance the security of Windows 11. The process involves applying a series of best practices to reduce vulnerabilities, prevent unauthorized access, and protect the system from various threats such as malware and exploits.

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Disadvantages of OS Hardening](#disadvantages-of-os-hardening)
6. [Team Members](#team-members)
7. [References](#references)

## Introduction

Operating System (OS) Hardening is a critical practice in cybersecurity aimed at enhancing the security of a system by reducing its vulnerability. This project specifically targets Windows 11, detailing the steps necessary to secure the OS from potential threats. Each step is carefully explained, highlighting its significance in improving overall system security.

## Features

The project implements the following OS hardening measures:

1. **Regular OS and Software Updates**: Keeping the OS and all software up to date to protect against known vulnerabilities.
2. **Windows Defender Configuration**: Ensuring real-time protection and regular scans are enabled to detect and remove threats.
3. **Firewall & Network Protection Configuration**: Setting up a firewall to control network traffic and prevent unauthorized access.
4. **User Account Control (UAC) Enablement**: Configuring UAC to prevent unauthorized system changes.
5. **Disabling Unnecessary Services**: Reducing the attack surface by disabling services that are not in use.
6. **BitLocker Encryption**: Encrypting the entire drive to protect data from unauthorized access.
7. **Advanced Security Settings Configuration**: Enabling exploit protection and other advanced security features.
8. **Robust Security Software Usage**: Installing additional security software for enhanced protection.

## Installation

To implement the hardening steps outlined in this project:

1. **Update OS and Software**:
   - Navigate to `Settings > Windows Update > Check for updates` and install available updates.
   
2. **Configure Windows Defender**:
   - Go to `Privacy & Security > Windows Security > Virus & Threat Protection` and ensure real-time protection is on.

3. **Set Up Firewall**:
   - Navigate to `Windows Security > Firewall & Network Protection`, and ensure the firewall is turned on.

4. **Enable UAC**:
   - Search for "UAC" and set it to the highest level for maximum protection.

5. **Disable Unnecessary Services**:
   - Press `Win + R`, type `services.msc`, and disable services like Remote Registry and Bluetooth Support (if not used).

6. **Enable BitLocker**:
   - Go to `Control Panel > System Security > BitLocker Drive Encryption` and turn on BitLocker.

7. **Configure Advanced Security Settings**:
   - Navigate to `Settings > Privacy & Security > Windows Security > App & Browser Control`, and enable Exploit Protection.

8. **Install Robust Security Software**:
   - Install and configure security software such as McAfee, Norton, or Malwarebytes.

## Usage

This project is intended to serve as a guide for system administrators, cybersecurity professionals, and anyone interested in securing their Windows 11 system. Follow the steps outlined to harden the OS against various security threats.

## Disadvantages of OS Hardening

While OS hardening improves security, it may come with some drawbacks:
- Reduced system convenience.
- Increased time for configuration and maintenance.
- Potential higher costs.
- Possible system malfunctions post-hardening due to stringent settings.

## Team Members

- Gamuchirai Muchafa  
- Ameera Mwale 
- Susanna Idu 
- Boluwatife Adetunji 
- Pauline Muthoka 
- Stella Obatoye 

## References

- NIST Special Publication 800-123
- CIS Benchmarks
- Perception Point, "OS Hardening: 15 Best Practices", 2023. [Link](https://perception-point.io/guides/os-isolation/os-hardening-10-best-practices/)
- Linford & Company LLP, "Operating System (OS) Hardening: Pros, Cons, and Importance", 2023. [Link](https://linfordco.com/blog/operating-system-hardening/)
- Spectral, "What is OS Hardening and How Can Developers Implement it", 2022. [Link](https://spectralops.io/blog/os-hardening-for-developers/)

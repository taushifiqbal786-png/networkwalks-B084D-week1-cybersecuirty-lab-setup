<h1 align="center">🛡️ Week 1: Cybersecurity Lab Setup</h1>

<p align="center">
  <b>VirtualBox · Kali Linux · Windows 10 · Android-x86 · SOC / Wireshark Labs</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/VirtualBox-Hypervisor-183A61?style=for-the-badge&logo=virtualbox&logoColor=white" alt="VirtualBox">
  <img src="https://img.shields.io/badge/Kali-Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white" alt="Kali Linux">
  <img src="https://img.shields.io/badge/Windows-10-0078D4?style=for-the-badge&logo=windows&logoColor=white" alt="Windows 10">
  <img src="https://img.shields.io/badge/Android-x86-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Android-x86">
  <img src="https://img.shields.io/badge/Wireshark-SOC_Labs-1679A7?style=for-the-badge&logo=wireshark&logoColor=white" alt="Wireshark">
</p>

<p align="center">
  <a href="#-part-1--required-week-1-assignment">Required Task</a> ·
  <a href="#-part-2--optional-projects">Optional Projects</a> ·
  <a href="#-verification-summary">Verification</a> ·
  <a href="#-troubleshooting-notes">Troubleshooting</a> ·
  <a href="#-conclusion">Conclusion</a>
</p>

---

## 📋 Project Information

| | |
|---|---|
| **Program** | [NetworkWalks Cybersecurity and Ethical Hacking Internship] |
| **Batch** | [B084D] |
| **Project** | [WK1-PM1]: VirtualBox and Kali Linux Lab Setup |
| **Author** | [MD TAUSHIF IQBAL] |

This repository documents my required Week 1 lab setup and the three optional projects I completed: Windows 10 virtualization, Android-x86 virtualization, and six SOC/Wireshark browser labs.

## 🗂️ Project Overview

| Type | Project | Description |
|---|---|---|
| ✅ **Required** | Kali Linux lab setup | Configure VirtualBox, Kali Linux, the NAT Network, host-guest integration, connectivity, and a VM snapshot. |
| ⭐ Optional 1 | Windows 10 VM | Install Windows 10 in VirtualBox and test network connectivity with Kali Linux. |
| ⭐ Optional 2 | Android-x86 VM | Install Android-x86 in VirtualBox and test network connectivity with Kali Linux. |
| ⭐ Optional 3 | SOC/Wireshark labs | Complete six browser-based network traffic investigation labs. |

📸 **Screenshots:** [Open the screenshots folder](https://github.com/[YOUR-USERNAME]/[YOUR-REPO-NAME]/tree/main/screenshots)

---

# 🐉 Part 1: Required Week 1 Assignment

## 1. Kali Linux Lab Setup

### 🎯 Objective

Set up Kali Linux in Oracle VirtualBox, configure the required NAT Network and static IP address, enable host-guest integration, test connectivity, and create a VM snapshot.

### ⚙️ Configuration

| Setting | Value |
|---|---|
| Virtualization platform | Oracle VirtualBox |
| Virtual machine | Kali Linux |
| Network type | NAT Network |
| NAT Network name | `NatNetwork` |
| Network subnet | `10.0.0.0/24` |
| Kali IPv4 address | `10.0.0.2/24` |
| Default gateway | `10.0.0.1` |
| DNS server | `8.8.8.8` |
| Shared Clipboard | Bidirectional |
| Drag-and-Drop | Bidirectional |
| Shared folder | Host folder named `downloads` |
| Snapshot name | `WK1-PM1-Kali-Lab-Configured` |

### ✅ Work Completed

1. Installed VirtualBox and imported Kali Linux.
2. Created the `NatNetwork` NAT Network with the required subnet.
3. Connected the Kali VM to the NAT Network.
4. Configured the static IPv4 address, gateway, and DNS settings.
5. Enabled bidirectional shared clipboard and drag-and-drop.
6. Configured the shared folder between Windows and Kali Linux.
7. Checked IP addressing and routing.
8. Tested gateway, external IP, DNS, and Internet connectivity.
9. Tested shared-folder access and host-guest integration.
10. Created a baseline snapshot of the Kali VM.

### 🧪 Verification Commands

```bash
ip a                    # confirm 10.0.0.2/24
ip route                # confirm default gateway 10.0.0.1
ping -c 4 10.0.0.1      # gateway reachable
ping -c 4 8.8.8.8       # external IP reachable
nslookup google.com     # DNS working
```

### 📸 Evidence: Required Week 1 Task

<p align="center">
  <img src="screenshots/1-nat-network.png" alt="NAT Network configuration" width="750">
  <br><sub><i>Figure 1: NAT Network configuration</i></sub>
</p>

<p align="center">
  <img src="screenshots/2-kali-adapter.png" alt="Kali network adapter settings" width="750">
  <br><sub><i>Figure 2: Kali network adapter attached to NatNetwork</i></sub>
</p>

<p align="center">
  <img src="screenshots/3-clipboard-dragdrop.png" alt="Clipboard and drag-and-drop settings" width="750">
  <br><sub><i>Figure 3: Bidirectional clipboard and drag-and-drop</i></sub>
</p>

<p align="center">
  <img src="screenshots/4-shared-folder.png" alt="Shared folder configuration" width="750">
  <br><sub><i>Figure 4: Shared folder configuration</i></sub>
</p>

<p align="center">
  <img src="screenshots/5-kali-ip-config.png" alt="Kali IP configuration" width="750">
  <br><sub><i>Figure 5: Kali IP address, gateway, and routing</i></sub>
</p>

<p align="center">
  <img src="screenshots/6-connectivity-tests.png" alt="Connectivity test results" width="750">
  <br><sub><i>Figure 6: Gateway, external IP, and DNS tests</i></sub>
</p>

<p align="center">
  <img src="screenshots/7-snapshot.png" alt="VM snapshot" width="750">
  <br><sub><i>Figure 7: Baseline snapshot</i></sub>
</p>

---

# ⭐ Part 2: Optional Projects

## 2. Optional Project: Windows 10 Virtual Machine

### 🎯 Objective

Install Windows 10 in VirtualBox, connect it to the same NAT Network as Kali Linux, set its IPv4 configuration, and test connectivity.

### ⚙️ Network Configuration

| Setting | Value |
|---|---|
| VM name | `Windows10-Lab` |
| Network type | NAT Network |
| IPv4 address | `10.0.0.10/24` |
| Gateway | `10.0.0.1` |
| DNS | `8.8.8.8` |

### ✅ Work Completed

1. Obtained the Windows 10 installation ISO.
2. Created and configured the Windows 10 VM.
3. Installed Windows 10.
4. Connected the VM to `NatNetwork`.
5. Configured its IPv4 settings.
6. Tested Windows-to-Kali connectivity.
7. Tested external IP connectivity.
8. Tested Kali-to-Windows connectivity.

### 🧪 Connectivity Commands

From Windows Command Prompt:

```cmd
ping 10.0.0.2
ping 8.8.8.8
```

From Kali Linux:

```bash
ping -c 4 10.0.0.10
```

### 📸 Evidence: Windows 10

<p align="center">
  <img src="screenshots/8-windows-vm-settings.png" alt="Windows 10 VM settings" width="750">
  <br><sub><i>Figure 8: Windows 10 VM settings</i></sub>
</p>

<p align="center">
  <img src="screenshots/9-windows-ipv4.png" alt="Windows IPv4 configuration" width="750">
  <br><sub><i>Figure 9: Windows IPv4 configuration</i></sub>
</p>

<p align="center">
  <img src="screenshots/10-windows-to-kali.png" alt="Windows to Kali ping test" width="750">
  <br><sub><i>Figure 10: Windows-to-Kali and external connectivity tests</i></sub>
</p>

<p align="center">
  <img src="screenshots/11-kali-to-windows.png" alt="Kali to Windows ping test" width="750">
  <br><sub><i>Figure 11: Kali-to-Windows connectivity test</i></sub>
</p>

---

## 3. Optional Project: Android-x86 Virtual Machine

### 🎯 Objective

Install Android-x86 in VirtualBox, connect it to the shared NAT Network, configure the IPv4 address, and test connectivity with Kali Linux and the Internet.

### ⚙️ Network Configuration

| Setting | Value |
|---|---|
| VM name | `Android9-Lab` |
| Operating system | Android-x86 9.0 |
| Network type | NAT Network |
| IPv4 address | `10.0.0.9/24` |
| Gateway | `10.0.0.1` |
| DNS | `8.8.8.8` |

### ✅ Work Completed

1. Obtained the Android-x86 ISO.
2. Created and configured the Android VM.
3. Installed Android-x86.
4. Connected it to `NatNetwork`.
5. Configured its IPv4 settings.
6. Tested Android-to-Kali connectivity.
7. Tested external IP connectivity.
8. Tested Kali-to-Android connectivity.

### 🧪 Connectivity Commands

From Android, using a terminal application:

```bash
ping 10.0.0.2
ping 8.8.8.8
```

From Kali Linux:

```bash
ping -c 4 10.0.0.9
```

### 📸 Evidence: Android-x86

<p align="center">
  <img src="screenshots/12-android-vm-config.png" alt="Android VM configuration" width="750">
  <br><sub><i>Figure 12: Android VM configuration</i></sub>
</p>

<p align="center">
  <img src="screenshots/13-android-desktop.png" alt="Android-x86 desktop" width="750">
  <br><sub><i>Figure 13: Android-x86 desktop</i></sub>
</p>

<p align="center">
  <img src="screenshots/14-android-connectivity.png" alt="Android connectivity tests" width="750">
  <br><sub><i>Figure 14: Android-to-Kali and external connectivity tests</i></sub>
</p>

<p align="center">
  <img src="screenshots/15-kali-to-android.png" alt="Kali to Android ping test" width="750">
  <br><sub><i>Figure 15: Kali-to-Android connectivity test</i></sub>
</p>

---

## 4. Optional Project: SOC/Wireshark, Six Labs

### 🎯 Objective

Complete six browser-based SOC labs, each containing ten tasks involving analysis of supplied network traffic captures.

### 🔬 Labs Completed

| # | Lab | What I Investigated |
|---|---|---|
| 1 | **Identify the Attacker's IP** | Inspected the capture to identify the suspected attacker's address. |
| 2 | **Follow TCP Stream 1** | Reconstructed and inspected a TCP conversation. |
| 3 | **Follow TCP Stream, Part 2** | Continued TCP stream analysis and investigated hidden data. |
| 4 | **HTTP Plain Text Credentials** | Found credentials transmitted over HTTP. |
| 5 | **Catch the Brute Force Attacker** | Investigated repeated authentication attempts. |
| 6 | **Catch the Call Scammer** | Investigated the capture and call recording. |

### 🧠 Skills Practised

- Network traffic analysis
- Source IP identification
- TCP stream reconstruction
- HTTP traffic inspection
- Identifying clear-text credentials
- Analysing repeated login attempts
- Investigating a VoIP-related scenario

### 📸 Evidence: SOC/Wireshark

<p align="center">
  <img src="screenshots/16-soc-lab-1.png" alt="SOC Lab 1 completion" width="750">
  <br><sub><i>Lab 1: Identify the Attacker's IP</i></sub>
</p>

<p align="center">
  <img src="screenshots/17-soc-lab-2.png" alt="SOC Lab 2 completion" width="750">
  <br><sub><i>Lab 2: Follow TCP Stream 1</i></sub>
</p>

<p align="center">
  <img src="screenshots/18-soc-lab-3.png" alt="SOC Lab 3 completion" width="750">
  <br><sub><i>Lab 3: Follow TCP Stream, Part 2</i></sub>
</p>

<p align="center">
  <img src="screenshots/19-soc-lab-4.png" alt="SOC Lab 4 completion" width="750">
  <br><sub><i>Lab 4: HTTP Plain Text Credentials</i></sub>
</p>

<p align="center">
  <img src="screenshots/20-soc-lab-5.png" alt="SOC

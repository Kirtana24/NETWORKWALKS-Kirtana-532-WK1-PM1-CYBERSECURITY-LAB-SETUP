<div align="center">

# 🛡️ CYBERSECURITY LAB SETUP

### Week 1 — Essentials of Cybersecurity & Penetration Testing
Author: Kirtana Minoy

</div>

---

## 📌 Table of Contents

- [🎯 Objective](#-objective)
- [🧰 Tools and Technologies](#-tools-and-technologies)
- [📂 Step 1: Extracting Kali Linux](#-step-1-extracting-kali-linux)
- [💻 Step 2: Setting Up the Virtual Machine](#-step-2-setting-up-the-virtual-machine)
- [🌐 Step 3: Accessing Network Settings](#-step-3-accessing-network-settings)
- [⚙️ Step 4: Configuring the NAT Network](#️-step-4-configuring-the-nat-network)
- [🔌 Step 5: Configuring the Network Adapter](#-step-5-configuring-the-network-adapter)
- [🐉 Step 6: Starting Kali Linux](#-step-6-starting-kali-linux)
- [🌍 Step 7: Testing Browser Access](#-step-7-testing-browser-access)
- [🛜 Step 8: Inspecting Network Settings](#-step-8-inspecting-network-settings)

---

## 🎯 Objective

The objective of this project is to establish a cybersecurity testing environment using **Oracle VirtualBox and Kali Linux**. The lab provides a virtual environment for learning networking concepts and practising penetration-testing techniques against authorised test systems.

## 🧰 Tools and Technologies

| Tool | Purpose |
|---|---|
| 🐉 Kali Linux | Security testing and penetration-testing environment |
| 💻 Oracle VirtualBox | Running the Kali Linux virtual machine |
| 📦 7-Zip | Extracting the downloaded virtual machine files |
| 🌐 Mozilla Firefox | Testing browser access |
| 🔗 NAT Network | Connecting virtual machines to a network |

---

## 📂 Step 1: Extracting Kali Linux

The downloaded Kali Linux virtual machine archive was extracted on the Windows host computer. The extracted folder contained two important files:

- **`.vbox` file:** Stores the virtual machine configuration.
- **`.vdi` file:** Stores the virtual machine's virtual hard disk.

These files are used by VirtualBox to configure and run the Kali Linux virtual machine.

**📸 Screenshot: Extracted Kali Linux Folder**

<img width="876" height="82" alt="ss4" src="https://github.com/user-attachments/assets/12852288-94db-4b18-a941-dd638207af8b" />

*The screenshot shows the folder created after extracting the downloaded Kali Linux virtual machine archive.*

**📸 Screenshot: VirtualBox Machine and Virtual Disk Files**

<img width="872" height="117" alt="ss5" src="https://github.com/user-attachments/assets/10d2565b-932f-4e64-9804-2f23d5d5cdd8" />

*The screenshot shows the `.vbox` configuration file and `.vdi` virtual disk image required for the virtual machine.*

---

## 💻 Step 2: Setting Up the Virtual Machine

The Kali Linux virtual machine was added to Oracle VirtualBox Manager. The virtual machine was then started to access the Kali Linux operating system.

VirtualBox Manager provides options to configure the virtual machine's memory, processors, storage, display, and network adapter.

**📸 Screenshot: Oracle VirtualBox Manager**

<img width="1600" height="851" alt="ss3" src="https://github.com/user-attachments/assets/a8e57283-3b9c-4102-a2ca-a88102b8d459" />

*The screenshot displays the Kali Linux virtual machine in VirtualBox Manager, along with its system, storage, and network information.*

---

## 🌐 Step 3: Accessing Network Settings

The network configuration interface was accessed through the Tools menu in VirtualBox Manager.

This interface allows the creation and configuration of virtual networks used by virtual machines.

**📸 Screenshot: VirtualBox Tools Menu**

<img width="1600" height="849" alt="ss6" src="https://github.com/user-attachments/assets/8c691f07-a112-467c-87b1-ec3fa3cb2894" />

*The screenshot shows the Tools menu and the option used to open the VirtualBox network configuration interface.*

---

## ⚙️ Step 4: Configuring the NAT Network

A NAT Network named `NatNetwork` was configured in VirtualBox.

The network uses the required IPv4 prefix of `10.0.0.0/24`. DHCP was enabled, while IPv6 was disabled.

### Network Configuration

| Parameter | Value |
|---|---|
| Network Name | `NatNetwork` |
| IPv4 Prefix | `10.0.0.0/24` |
| DHCP | Enabled |
| IPv6 | Disabled |

A NAT Network allows connected virtual machines to communicate with one another and access external networks through network address translation.

**📸 Screenshot: NAT Network Configuration**

<img width="1600" height="848" alt="ss7" src="https://github.com/user-attachments/assets/a5561416-98e3-4e26-b0f4-ae3ae1f09204" />

*The screenshot shows the configured `NatNetwork`, its IPv4 prefix of `10.0.0.0/24`, and the enabled DHCP option.*

---

## 🔌 Step 5: Configuring the Network Adapter

The Kali Linux virtual machine's network adapter was configured to connect to the previously created NAT Network.

### Adapter Configuration

| Parameter | Value |
|---|---|
| Adapter | Adapter 1 |
| Attached To | NAT Network |
| Network Name | `NatNetwork` |
| Adapter Type | Intel PRO/1000 MT Desktop |
| Enable Network Adapter | Enabled |
| Virtual Cable Connected | Enabled |

These settings allow the virtual machine to use the configured NAT Network.

**📸 Screenshot: Kali Linux Network Adapter**

<img width="1600" height="847" alt="ss8" src="https://github.com/user-attachments/assets/61effbd5-d38d-4156-b8c5-d02c7ffbabcb" />

*The screenshot shows Adapter 1 connected to `NatNetwork`, with the network adapter enabled and the virtual cable connected.*

---

## 🐉 Step 6: Starting Kali Linux

The Kali Linux virtual machine was started successfully, and its graphical desktop environment loaded.

Kali Linux provides a range of tools used for cybersecurity education, network analysis, vulnerability assessment, and authorised penetration testing.

**📸 Screenshot: Kali Linux Desktop**

<img width="1600" height="849" alt="ss1" src="https://github.com/user-attachments/assets/07909b83-a001-4350-94f1-49799f3d2ae5" />

*The screenshot displays the Kali Linux desktop running inside Oracle VirtualBox.*

---

## 🌍 Step 7: Testing Browser Access

Mozilla Firefox was opened inside Kali Linux, and Google was accessed during the initial setup.

This provided evidence that browser access was working when the screenshot was captured.

**📸 Screenshot: Firefox in Kali Linux**

<img width="1600" height="848" alt="ss2" src="https://github.com/user-attachments/assets/589bb10c-c39c-464c-bd5e-f5cc98471cab" />

*The screenshot shows Firefox displaying Google search results for the term "cybersecurity". It documents successful browser access at the time of capture.*

---

## 🛜 Step 8: Inspecting Network Settings

The NetworkManager connection editor was opened to inspect the wired network connection associated with the `eth0` interface.

The connection editor provides options for configuring wired Ethernet settings, IPv4, IPv6, and other network properties.

### Required Network Configuration

| Parameter | Required Value |
|---|---|
| Kali Linux IPv4 Address | `10.0.0.2` |
| Prefix Length | `/24` |
| Subnet Mask | `255.255.255.0` |
| Gateway | `10.0.0.1` |

**📸 Screenshot: Wired Connection Settings**

<img width="1600" height="851" alt="ss9" src="https://github.com/user-attachments/assets/4fb193c1-c228-4949-9fcf-0c6e61a87738" />

*The screenshot shows the `Wired connection 1` configuration window and the device associated with the connection.*

The required IP address and gateway should be verified against the active network configuration to ensure that the intended settings are applied.

---
## Problems Faced and Solutions

### 1. Identifying Virtual Machine Files
**Problem:** After extracting Kali Linux, it was initially confusing to identify the purpose of the different files.

**Solution:** I identified the `.vbox` file as the virtual machine configuration file and the `.vdi` file as the virtual disk image.

### 2. Configuring the NAT Network
**Problem:** Configuring the correct network settings was challenging.

**Solution:** I configured the NAT Network in VirtualBox using the required network address `10.0.0.0/24` and kept the network name as `NatNetwork`.

### 3. Resolving Network Connectivity Issues
**Problem:** Initially, Kali Linux experienced network connectivity issues, particularly after restarting the virtual machine.

**Solution:** I checked and adjusted the network configuration in VirtualBox and Kali Linux. The internet connection is now working successfully.

---

## 💡 What I Learned

Through this project, I learned how to:

### 1. Virtual Machine Management
Understand the purpose of `.vbox` and `.vdi` files and run an existing Kali Linux virtual machine in Oracle VirtualBox.

### 2. Virtual Networking
Configure a NAT Network using the required `10.0.0.0/24` subnet and connect a virtual machine to it.

### 3. IP Addressing
Understand the relationship between an IPv4 address, subnet mask, prefix length, and default gateway.

### 4. Connectivity Troubleshooting
Inspect network adapter settings and investigate connectivity problems that occur after restarting a virtual machine.

### 5. Technical Documentation
Organise screenshots, explain configuration steps, and record problems and solutions in a GitHub README.

### 6. Cybersecurity Lab Preparation
Understand how a virtual lab provides a foundation for future cybersecurity learning and authorised security testing.

---
## 🔐 Security and Ethical Use

This virtual lab is intended for educational purposes and authorised cybersecurity testing.

- Perform security testing only on systems you own or have explicit permission to test.
- Keep lab configurations organised and document any changes.
- Verify network settings before conducting practical exercises.
- Use virtual machine snapshots as recovery points when available.

---

## 📌 Project Information

| Field | Details |
|---|---|
| Week | 01 |
| Project | Essentials of Cybersecurity & Penetration Testing |
| Module | WK1-PM1 |
| Tools | kali-linux-2026.3-virtualbox-amd64 , VirtualBox-7.2.22-175245-Win |

---

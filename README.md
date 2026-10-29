<div align="center">

# 🛡️ CYBERSECURITY LAB SETUP

### Week 1 — Essentials of Cybersecurity & Penetration Testing

**VirtualBox • Kali Linux • Network Configuration**

**Internship Project | WK1-PM1**

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
- [📚 Learning Outcomes](#-learning-outcomes)
- [🏁 Conclusion](#-conclusion)

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

## 📚 Learning Outcomes

Through this project, I gained practical experience with:

- Extracting and configuring a virtual machine.
- Using Oracle VirtualBox to run Kali Linux.
- Understanding the purpose of `.vbox` and `.vdi` files.
- Creating and configuring a NAT Network.
- Connecting a virtual machine to a specified network.
- Inspecting wired network configuration settings.
- Testing browser access and documenting the setup process.

---

## 🏁 Conclusion

This project provided practical experience in setting up a cybersecurity lab using Oracle VirtualBox and Kali Linux. The virtual machine was started successfully, and the required NAT Network was configured with the specified IPv4 prefix.

The initial browser-access test also demonstrated connectivity at the time of capture. This setup establishes the foundation for further learning and authorised cybersecurity testing.

---

<div align="center">

### 🔐 Learn • Configure • Test • Secure

**Week 1 Cybersecurity Lab Setup | WK1-PM1**

</div>

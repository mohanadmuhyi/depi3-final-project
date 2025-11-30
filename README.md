# FortiGate Security Profiles Project

## 📌 Project Overview

This repository contains the complete documentation and media for the **FortiGate Security Profiles Project**. The project demonstrates the practical implementation of multiple FortiGate security profiles in a segmented network environment, with full testing and verification.

The main security features implemented include:

* Firewall Policies
* Web Filtering
* Application Control
* Anti-Virus Protection
* Security Logging & Monitoring

This repository is intended for:

* Academic evaluation
* DEPI Graduation Portfolio
* Cybersecurity Internship & Job Applications

---

## 👥 Team Members

* **Mohannad Mohie 21043873**
* **Muhammed Saeed 21045047**
* **Yousef Mohamed 21007865**
* **Akram Khaled 21037388**
* **Mazen Mohamed 21052008**

---

## 🧱 Network Architecture

The network is built using **GNS3** with the following structure:

* **Two LAN networks** (LAN-1 & LAN-2)
* **One DMZ network** (DMZ-WEB)
* **FortiGate Firewall** as the main security gateway
* **Windows 7, Windows 10, Kali Linux** as client machines
* **Windows Server** in the DMZ acting as:

  * Web Server
  * DNS Server

Each network is fully isolated using FortiGate firewall policies.

---

## 🛡️ Implemented Security Features

### 1️⃣ Firewall Policies

* Controlled traffic between LAN, DMZ, and WAN
* Internet access allowed for both LANs
* DMZ allowed to access the internet for updates
* No direct communication between LAN-1 and LAN-2 (implicit deny enforced)

### 2️⃣ Web Filtering

* Blocked local website: `depi.team`
* Blocked external website: `zone94.com`
* Applied to:

  * LAN-1 → DMZ
  * LAN-2 → DMZ
  * LAN-1 → WAN
  * LAN-2 → WAN
* Verified on both Windows and Kali Linux

### 3️⃣ Application Control

* Applied only on **LAN-1**
* Blocked categories:

  * Social Media
  * Games
  * Proxy
  * P2P
* **LinkedIn explicitly allowed** using Application Override
* Applications using non-default ports were blocked
* High bandwidth consumption applications were restricted

### 4️⃣ Anti-Virus Protection

* Applied only on **LAN-2** for controlled testing
* Default Anti-Virus security profile enabled
* Tested using **EICAR test virus**
* Malicious file was successfully blocked

### 5️⃣ Security Monitoring & Logs

* Web Filtering logs
* Application Control logs
* Anti-Virus logs
* All actions recorded with:

  * Source IP
  * Destination
  * Category
  * Action taken

---

## 🧪 Testing & Verification

All security features were fully tested and verified:

* Internet access functionality
* Website access and blocking
* Application blocking and overrides
* Malware blocking using EICAR test
* Verification through FortiGate **Log & Report** section

---

## 🎥 Demo Video
Click the link below to watch the full project demonstration:

[▶️ Watch Demo Video](video/Demo%20Video%20-%20Group%201.mp4)


---

## 📄 Project Report

The complete technical report is available here:

📁 `reports/final-report.pdf`

This report includes:

* Full topology explanation
* IP addressing & port assignments
* Policy configuration
* Web filtering configuration
* Application control setup
* Anti-virus testing
* Log verification

---

## 📊 Presentations

Two presentations are included:

📁 `presentations/final-presentation.pptx`
📁 `presentations/security-profiles-presentation.pptx`

These presentations are designed to be **self-explanatory** and do not require live speaking.

---

## 🔧 FortiGate Configuration File

The FortiGate running configuration used in the project is available here:

📁 `fortigate-config/running-config.conf`

This file can be restored directly on any FortiGate device or FortiGate VM.

---

## 🧭 GNS3 Topology File

The topology file is included here:

📁 `gns3/fortigate-security-profiles.gns3`

⚠️ **Important Notice:**

* This repository contains **only the main `.gns3` topology file**.
* Virtual machine images (FortiGate, Windows, Kali) are **not included** due to licensing restrictions.

To run the project:

1. Open the `.gns3` file in GNS3
2. Attach your own FortiGate VM
3. Attach your own Windows and Kali Linux VMs
4. Restore the FortiGate configuration
5. Start all devices and begin testing

---

## 📌 Notes

* This project was implemented as part of the **DEPI Fortinet Cybersecurity Track**.
* The project focuses on **Blue Team defensive security techniques**.
* It follows real-world enterprise firewall design principles.
* All policies were implemented manually and tested practically.

---

## 🏁 Conclusion

This project successfully demonstrates a complete FortiGate defensive security implementation, including:

* Network segmentation
* Access control
* Web security
* Application security
* Malware protection
* Security monitoring and logging

It represents a full practical cybersecurity firewall deployment suitable for academic, training, and professional portfolio use.

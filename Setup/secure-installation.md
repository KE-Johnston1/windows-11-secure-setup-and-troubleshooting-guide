# Secure Windows 11 Installation

## Purpose
A technician‑friendly guide for performing a clean, secure installation of Windows 11.  
This document focuses on BIOS preparation, installation steps, and applying secure defaults.

---

## 1. Prerequisites
- USB installer created using the Windows Media Creation Tool  
- Device meets Windows 11 hardware requirements  
- Access to BIOS/UEFI  
- Stable internet connection (recommended)

---

## 2. Configure BIOS/UEFI

### Required Settings
- **Enable TPM 2.0**
- **Enable Secure Boot**
- **Disable Legacy/CSM boot modes**
- **Set USB as first boot device**

### Optional (Advanced)
- Enable Virtualisation (VTx/AMD‑V)  
- Disable unused boot devices  
- Set BIOS password (enterprise environments)

---

## 3. Start Windows Installation

### Boot from USB
1. Insert USB installer  
2. Restart device  
3. Press the correct key (F2, F10, F12, DEL) to open boot menu  
4. Select USB device

### Installation Steps
- Choose language, region, keyboard  
- Select **Custom Install**  
- Delete existing partitions (if appropriate)  
- Create new partition and continue  
- Allow Windows to complete installation

---

## 4. Apply Secure Defaults (OOBE)

### Account Setup
- Use a Microsoft Account for recovery and device tracking  
- Avoid using local admin accounts unless required  
- Disable optional data sharing

### Privacy & Telemetry
- Disable advertising ID  
- Disable tailored experiences  
- Disable location (optional)

---

## 5. First Boot Security Tasks
- Run Windows Update  
- Enable Microsoft Defender  
- Verify Firewall is active  
- Confirm BitLocker or Device Encryption is enabled  
- Remove OEM bloatware  
- Install required drivers (avoid OEM audio drivers unless necessary)

---

## Technician Notes
- Always document BIOS changes  
- Avoid OEM recovery images — clean installs reduce bloatware  
- If BitLocker is enabled automatically, store the recovery key securely  
- After installation, proceed to the **Post‑Install Checklist** for final configuration

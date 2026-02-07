# Microsoft Defender Setup

## Purpose
A guide for configuring Microsoft Defender for strong baseline protection on Windows 11 systems.

---

## 1. Real‑Time Protection
Ensure the following are enabled:
- Real‑time protection  
- Cloud‑delivered protection  
- Automatic sample submission  
- Tamper protection  

---

## 2. Virus & Threat Protection Settings
- Enable **Controlled Folder Access** (optional, high‑security environments)
- Enable **Ransomware Protection**
- Configure **Exclusions** only when necessary (e.g., developer tools)

---

## 3. Firewall & Network Protection
- Firewall enabled for **Domain**, **Private**, and **Public** profiles  
- Block inbound connections by default  
- Review allowed apps and remove unnecessary entries  

---

## 4. App & Browser Control
Enable:
- SmartScreen for Microsoft Edge  
- SmartScreen for Microsoft Store apps  
- SmartScreen for downloaded files  
- Reputation‑based protection  

---

## 5. Security Intelligence Updates
- Confirm Defender is receiving daily updates  
- Run manual update after installation  

---

## Technician Notes
- Defender is sufficient for most environments without third‑party AV  
- Controlled Folder Access may block legitimate apps — test before enabling  
- Tamper Protection prevents unauthorised changes to Defender settings  


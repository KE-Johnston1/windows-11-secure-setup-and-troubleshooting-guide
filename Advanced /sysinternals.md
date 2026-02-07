# Sysinternals Toolkit – Technician Guide

## Purpose
A reference guide for using Sysinternals tools to diagnose advanced Windows issues, including performance, malware, and system behaviour.

---

## 1. Process Explorer
### Use Cases
- Identify suspicious processes  
- Inspect process trees  
- Check digital signatures  
- View CPU, memory, and handle usage  

### Key Actions
- Right‑click → Properties → Verify Signature  
- View → Lower Pane → DLLs or Handles  

---

## 2. Autoruns
### Use Cases
- Identify startup programs  
- Detect persistence mechanisms  
- Disable unwanted autostart entries  

### Key Actions
- Hide Microsoft entries  
- Disable unknown or unsigned items  

---

## 3. Process Monitor (ProcMon)
### Use Cases
- Track file, registry, and process activity  
- Diagnose application failures  
- Identify permission issues  

### Key Actions
- Apply filters (Process Name, Result, Path)  
- Capture logs for troubleshooting  

---

## 4. TCPView
### Use Cases
- Monitor network connections  
- Detect suspicious outbound traffic  
- Identify processes using ports  

---

## 5. RAMMap
### Use Cases
- Analyse memory usage  
- Identify memory leaks  
- Review file cache behaviour  

---

## Technician Notes
- Sysinternals tools require admin rights for full functionality  
- ProcMon logs can grow rapidly — use filters  
- Always verify digital signatures when investigating suspicious processes  


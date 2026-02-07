# Event Viewer Analysis – Windows 11

## Purpose
A guide for analysing Windows Event Viewer logs to diagnose system, security, and application issues.

---

## 1. Key Event Logs

### System Log
- Driver failures  
- Hardware issues  
- Service crashes  

### Application Log
- App errors  
- Crashes  
- .NET issues  

### Security Log
- Logon attempts  
- Privilege use  
- Policy changes  

---

## 2. Common Event IDs

### System
- **41** – Unexpected shutdown  
- **7000–7009** – Service start failures  
- **1001** – BugCheck (BSOD)

### Security
- **4624** – Successful logon  
- **4625** – Failed logon  
- **4672** – Admin privileges assigned  

### Application
- **1000** – Application crash  
- **1026** – .NET runtime error  

---

## 3. Custom Views

### Create a Technician View
Filter for:
- Critical  
- Error  
- Warning  
- Event IDs: 41, 1000, 7000–7009  

---

## 4. Troubleshooting Workflow
1. Identify the time of the issue  
2. Filter logs around that timestamp  
3. Look for repeating patterns  
4. Check Event ID details  
5. Correlate with system changes (updates, drivers, installs)  

---

## Technician Notes
- Event Viewer is most useful when paired with ProcMon or Reliability Monitor  
- Always correlate events with timestamps reported by the user  
- Not all errors are critical — context matters  


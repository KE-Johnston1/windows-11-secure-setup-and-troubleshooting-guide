# KBA‑003: High CPU Usage on Windows 11

## Summary
A device shows consistently high CPU usage, causing slow performance, fan noise, or system lag.

---

## Symptoms
- CPU usage stuck above 80%  
- System slow or unresponsive  
- Fans running constantly  
- Task Manager shows one process consuming excessive resources  

---

## Common Causes
- Windows Update stuck  
- Malware or unwanted software  
- Corrupted system files  
- Background indexing  
- Faulty drivers  

---

## Troubleshooting Steps

### 1. Identify Offending Process
Task Manager → Processes  
Check CPU column.

### 2. Restart Windows Update Services
```
net stop wuauserv
net start wuauserv
```

### 3. Run SFC & DISM
```
sfc /scannow
DISM /Online /Cleanup-Image /RestoreHealth
```

### 4. Check Startup Apps
Disable unnecessary apps in Task Manager → Startup.

### 5. Scan for Malware
Run full scan with Microsoft Defender.

---

## Resolution
High CPU usage is typically caused by stuck updates or background processes. Restarting services and cleaning startup apps resolves most cases.

---

## Technician Notes
- Avoid disabling Windows Search unless necessary  
- Document any services disabled for troubleshooting  


# KBA‑002: Wi‑Fi Drops or Disconnects Intermittently

## Summary
A Windows 11 device experiences intermittent Wi‑Fi drops, slow speeds, or sudden disconnections. This guide outlines common causes and technician‑friendly troubleshooting steps.

---

## Symptoms
- Wi‑Fi disconnects randomly  
- Slow or unstable connection  
- “Connected, no internet”  
- Network adapter resets unexpectedly  

---

## Root Causes
- Outdated or unstable wireless drivers  
- Power management settings disabling the adapter  
- Router channel congestion  
- Incorrect DNS configuration  
- Corrupted network stack  

---

## Troubleshooting Steps

### 1. Restart Network Stack
```
ipconfig /flushdns
ipconfig /release
ipconfig /renew
netsh winsock reset
```

### 2. Update or Roll Back Wi‑Fi Driver
Device Manager → Network adapters → Wireless adapter  
- Update driver  
- If issue started recently → Roll back driver  

### 3. Disable Power Saving
Device Manager → Wireless adapter → Power Management  
- Untick “Allow the computer to turn off this device to save power”

### 4. Change DNS
Set DNS to:
- 1.1.1.1  
- 8.8.8.8  

### 5. Router Checks
- Change Wi‑Fi channel  
- Restart router  
- Ensure 5GHz is enabled  

---

## Resolution
Most Wi‑Fi instability is caused by driver issues or power management. Updating or rolling back the driver typically resolves the issue.

---

## Technician Notes
- Intel wireless drivers are frequently updated — check OEM site  
- Power saving is a common cause on laptops  


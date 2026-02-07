# KBA‑001: No Audio Output – Conexant ISST / Intel Smart Sound Technology Failure

## Summary
A Windows 11 device presented with no audio output. The volume slider reset to 0, and the Intel(R) Audio Service failed to start. The system was using a Conexant ISST driver dependent on Intel Smart Sound Technology (ISST), which had become non‑functional. Replacing the OEM driver with the Microsoft High Definition Audio Device resolved the issue.

---

## Symptoms
- No sound from speakers or headphones  
- Volume slider snaps back to **0**  
- “Conexant ISST Audio” listed as output device  
- Intel(R) Audio Service fails to start  
- Windows Update reports “best drivers already installed”  
- SFC scan does not resolve issue  

---

## Root Cause
The Conexant ISST driver relies on Intel Smart Sound Technology.  
When ISST fails to start, the Conexant driver cannot initialise the audio engine.  
Windows Update does not detect this failure because the OEM driver is still considered “correct”.

---

## Troubleshooting Steps

### 1. Verify System Integrity
```
sfc /scannow
```
Result: No change.

### 2. Restart Audio Services
```
net stop audiosrv
net start audiosrv
```
ISST service failed to start.

### 3. Attempt Driver Update
Device Manager → Update Driver  
Result: “Best driver already installed.”

### 4. Replace OEM Driver
Device Manager → Conexant ISST Audio → Uninstall Device  
Tick **Delete the driver software for this device**  
Restart system.

### 5. Confirm Generic Driver Installed
Device Manager → Sound  
Should show: **High Definition Audio Device (Microsoft)**

---

## Resolution
Removing the Conexant ISST driver forced Windows to install the Microsoft generic audio driver, restoring full audio functionality.

---

## Technician Notes
- Volume slider snapping back to 0 is a key diagnostic indicator  
- OEM Conexant drivers are version‑locked and often unstable  
- The Microsoft generic driver is typically more reliable  


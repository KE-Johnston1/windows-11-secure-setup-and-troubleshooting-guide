# PowerShell Automation for Windows 11

## Purpose
A collection of technician‑friendly PowerShell commands and scripts used to automate common Windows 11 configuration, diagnostics, and security tasks.

---

## 1. System Information

### Basic System Info
```
Get-ComputerInfo
```

### Installed Updates
```
Get-HotFix
```

### Disk Health
```
Get-PhysicalDisk | Select FriendlyName, HealthStatus, OperationalStatus
```

---

## 2. Network Diagnostics

### IP Configuration
```
Get-NetIPAddress
```

### Reset Network Stack
```
netsh winsock reset
netsh int ip reset
```

### DNS Flush
```
Clear-DnsClientCache
```

---

## 3. Security & Defender

### Quick Scan
```
Start-MpScan -ScanType QuickScan
```

### Full Scan
```
Start-MpScan -ScanType FullScan
```

### Update Defender Signatures
```
Update-MpSignature
```

---

## 4. User & Account Management

### List Local Users
```
Get-LocalUser
```

### Create Standard User
```
New-LocalUser -Name "username" -NoPassword
Add-LocalGroupMember -Group "Users" -Member "username"
```

---

## 5. Windows Update Automation

### Check for Updates
```
Get-WindowsUpdate
```

### Install Updates
```
Install-WindowsUpdate -AcceptAll -AutoReboot
```

(Requires PSWindowsUpdate module)

---

## Technician Notes
- PowerShell should be run as Administrator for most tasks  
- Avoid running scripts from untrusted sources  
- Document any automation used in production environments  


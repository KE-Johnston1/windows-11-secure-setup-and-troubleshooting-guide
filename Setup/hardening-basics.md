Windows 11 Hardening Basics
Purpose
A technician‑friendly guide outlining essential hardening steps for Windows 11 systems. This document focuses on practical, low‑impact security improvements suitable for home, business, and enterprise environments.

1. Account Security
Local & Microsoft Accounts
Use a Microsoft Account for improved recovery and device tracking

Disable or remove unused local accounts

Ensure Administrator accounts use strong, unique passwords

Windows Hello
Enable Windows Hello (PIN, biometrics)

Require sign‑in on wake

Disable automatic login

2. System Protection
BitLocker / Device Encryption
Enable BitLocker on system drive

Store recovery key in Microsoft Account or secure offline location

Verify encryption status after reboot

Secure Boot
Ensure Secure Boot is enabled in UEFI

Disable legacy boot modes

Core Isolation
Enable Memory Integrity

Resolve incompatible drivers if required

3. Network Hardening
Firewall
Ensure Windows Firewall is enabled for all profiles

Block inbound connections by default

Allow only required apps through firewall

SMB & Legacy Protocols
Disable SMBv1

Disable LLMNR (optional, enterprise environments)

Disable NetBIOS over TCP/IP (optional)

4. Application Control
Smart App Control / SmartScreen
Enable Smart App Control (if supported)

Enable SmartScreen for:

Microsoft Edge

Microsoft Store apps

File downloads

App Permissions
Review and disable unnecessary permissions:

Location

Camera

Microphone

Background apps

PowerShell Security
Set PowerShell to Constrained Language Mode (optional, advanced)

Enable script logging

5. Logging & Monitoring
Event Viewer
Enable audit logs for:

Logon events

Account changes

Policy changes

Object access

Defender Logging
Enable Defender cloud protection

Enable automatic sample submission

Enable tamper protection

Windows Update
Ensure automatic updates are enabled

Install optional security updates

Technician Notes
Hardening should not break usability — test changes before applying widely

Document all modifications for rollback

Some advanced settings (LLMNR, NetBIOS, Constrained Language Mode) are optional and environment‑dependent

BitLocker and Memory Integrity may require driver compatibility checks

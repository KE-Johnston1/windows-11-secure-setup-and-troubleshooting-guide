Windows 11 Secure Setup & Troubleshooting Guide
A clear, beginner‑friendly guide for setting up, securing, and troubleshooting a Windows 11 device.
This project demonstrates practical IT Support and cybersecurity fundamentals through structured steps, automation scripts, and plain‑English documentation.

It reflects real workflows used in:

• IT Support & Service Desk
• NOC & SOC Tier 1
• Endpoint security
• User support & documentation
• Troubleshooting and incident response

📌 Table of Contents
Part 1 — Secure Windows 11 Setup

Part 2 — Troubleshooting Playbook

Part 3 — User‑Facing Documentation

Part 4 — Advanced Scenarios

Part 5 — PowerShell Automation Scripts

Part 6 — PDF Export Plan

Part 7 — Video Walkthrough Plan

Part 8 — Sample IT Support Tickets

Part 9 — How I Handle Tickets (Overview)

Part 10 — Ticketing Workflow Diagram

Part 11 — Common IT Support Phrases

Skills Demonstrated

Tools & Technologies

Future Improvements

Footer

Part 1 — Secure Windows 11 Setup
A complete, secure setup workflow for a new Windows 11 device.

Step 1: Create a Standard User Account
Open Settings

Select Accounts

Select Family & other users

Add a new standard user

Sign out of the administrator account and use the standard account for daily use

Step 2: Enable BitLocker Drive Encryption
Open Control Panel

Select BitLocker Drive Encryption

Turn on BitLocker for the system drive

Save the recovery key securely

Allow encryption to complete

Step 3: Configure Windows Security (Defender)
Open Windows Security

Enable Real‑time protection

Enable Cloud‑delivered protection

Enable Tamper Protection

Run a quick scan

Step 4: Apply Windows Updates
Open Settings

Select Windows Update

Click Check for updates

Install all available updates

Restart if required

Step 5: Configure Privacy & Security Settings
Open Settings

Select Privacy & security

Disable unnecessary tracking features

Review app permissions

Disable advertising ID

Step 6: Verify Device Encryption & Secure Boot
Open System Information

Confirm Secure Boot is enabled

Confirm TPM is present

Confirm device encryption is active

Step 7: Install Essential Applications
Open Microsoft Store

Install required apps

Install browser extensions

Configure app settings

Step 8: Configure OneDrive & File Backup
Sign in to OneDrive

Enable folder backup

Confirm sync status

Test file recovery

Step 9: Configure Browser Security
Enable tracking protection

Enable HTTPS‑only mode

Install security extensions

Clear default permissions

Step 10: Configure Power Settings
Open Settings

Select Power

Adjust sleep settings

Enable battery saver (laptops)

Step 11: Configure Startup Apps
Open Task Manager

Select Startup apps

Disable unnecessary items

Restart device

Step 12: Configure Windows Restore & Recovery
Open System Protection

Enable restore points

Create a restore point

Review recovery options

Step 13: Final Security Checks
Confirm updates

Confirm Defender status

Confirm BitLocker

Confirm OneDrive sync

Part 2 — Troubleshooting Playbook
Clear, repeatable troubleshooting workflows for common issues.

Network Issues
• Slow connection
• No internet
• DNS problems

Restart router

Run network troubleshooter

Flush DNS

Reset network adapter

Slow Performance
• High CPU
• Low disk space
• Too many startup apps

Check Task Manager

Disable startup apps

Clear temporary files

Run malware scan

App Crashes
• Outdated apps
• Corrupted files

Update the app

Repair installation

Check Event Viewer

Printer Problems
• Printer offline
• Queue stuck

Restart Print Spooler

Clear print queue

Reinstall printer

Audio Issues
• No sound
• Wrong output device

Check output device

Restart audio service

Update drivers

Windows Update Failures
• Update stuck
• Error codes

Run update troubleshooter

Clear update cache

Restart device

Part 3 — User‑Facing Documentation
Simple, friendly guides for non‑technical users.

Connect to Wi‑Fi
Click the network icon

Select Wi‑Fi

Choose your network

Enter password

Reset Microsoft Account Password
Visit the reset page

Enter email

Verify identity

Create new password

Use OneDrive for Backup
Sign in

Enable folder backup

Confirm sync

Install Apps Safely
Use Microsoft Store

Avoid unknown websites

Keep Windows Updated
Open Windows Update

Install updates

Use Quick Assist
Open Quick Assist

Enter code

Allow access

Part 4 — Advanced Scenarios
More complex, real‑world issues requiring deeper investigation.

Suspicious Activity / Malware
• Pop‑ups
• Unknown apps

Check Defender

Review startup apps

Run full scan

Shared Drive Access Issues
• Access denied
• Missing drive

Check permissions

Check server connection

Remap drive

Device Fails to Boot
• Blue screen
• Boot loop

Use recovery options

Run SFC and CHKDSK

Restore system

High Network Latency
• Lag
• VPN drops

Test local network

Test external ping

Restart router

BitLocker Recovery Loop
• Repeated key prompts

Check TPM

Check Secure Boot

Suspend BitLocker

Microsoft 365 Sync Issues
• Outlook not syncing
• OneDrive stuck

Clear credentials

Reset OneDrive

Repair Office

Part 5 — PowerShell Automation Scripts
Automation scripts for repeatable workstation builds.

Check System Security Status
powershell
Get-BitLockerVolume
Confirm-SecureBootUEFI
Get-Tpm
Get-NetFirewallProfile
Get-MpComputerStatus
Enable Defender Features
powershell
Set-MpPreference -DisableRealtimeMonitoring $false
Set-MpPreference -MAPSReporting Advanced
Set-MpPreference -SubmitSamplesConsent SendSafeSamples
Configure Privacy Settings
powershell
Set-ItemProperty -Path "HKCU:\Software\Microsoft\Windows\CurrentVersion\AdvertisingInfo" -Name Enabled -Value 0
Set-ItemProperty -Path "HKCU:\Software\Microsoft\Windows\CurrentVersion\Privacy" -Name TailoredExperiencesWithDiagnosticDataEnabled -Value 0
Disable Startup Apps
powershell
Get-CimInstance Win32_StartupCommand | Select-Object Name, Command
Install Essential Apps
powershell
winget install --id=Google.Chrome -e
winget install --id=7zip.7zip -e
winget install --id=Notepad++.Notepad++ -e
winget install --id=Microsoft.Teams -e
Create Restore Point
powershell
Checkpoint-Computer -Description "Post-Setup Restore Point" -RestorePointType MODIFY_SETTINGS
Master Script (Run All)
powershell
Write-Output "Starting Windows 11 secure setup automation..."
Part 6 — PDF Export Plan
• Export README to PDF
• Add screenshots (optional)
• Add table of contents
• Use as interview material
• Provide as onboarding documentation

Part 7 — Video Walkthrough Plan
• Record setup steps
• Narrate troubleshooting
• Demonstrate PowerShell scripts
• Upload to GitHub or LinkedIn
• Use as a portfolio enhancement

Part 8 — Sample IT Support Tickets
Includes one full ticket and a short appendix of additional scenarios.

Full Ticket Example — Wi‑Fi Not Connecting
Ticket ID: INC‑2026‑0142
User: Sarah M
Department: Finance
Device: Dell Latitude 5420 (Windows 11)
Priority: Medium
Status: Resolved

User Report
“My laptop won’t connect to the office Wi‑Fi. It worked yesterday but today it keeps saying ‘Can’t connect to this network’.”

Initial Triage
• Confirmed user was on‑site
• Verified other users could connect to the same SSID
• Confirmed the issue persisted across reboots
• Checked for recent Windows updates

Troubleshooting Steps
Checked Wi‑Fi status

Forgot and re‑added the network

Ran Windows Network Troubleshooter

Flushed DNS and reset network stack

Updated Wi‑Fi adapter driver

Restarted device

Root Cause
Outdated Wi‑Fi adapter driver causing authentication and connectivity failures.

Resolution
• Updated Wi‑Fi driver
• Reconnected to corporate SSID
• Verified stable connection

Next Steps
• Added device to monthly driver review list
• Recommended weekly restarts

Ticket Closure
Resolved: Wi‑Fi connectivity restored after driver update.
Time to Resolution: 32 minutes
User Satisfaction: Positive

Ticketing Appendix — Additional Scenarios
1. Password Reset Request
• User unable to log into Microsoft 365
• Verified identity, reset password, confirmed MFA
• User logged in successfully

2. BitLocker Recovery Key Request
• User prompted for key after BIOS update
• Retrieved key from Azure AD
• Device unlocked successfully

3. OneDrive Sync Failure
• Red “X” on OneDrive
• Reset client, cleared credentials
• Sync restored

4. Windows Update Failure
• Error 0x8024a105
• Cleared SoftwareDistribution folder
• Update installed successfully

Part 9 — How I Handle Tickets (Overview)
A simple, consistent approach I use for all IT Support tickets:

Acknowledge the user quickly

Gather information (who, what, when, where, impact)

Reproduce the issue if possible

Perform structured troubleshooting

Document every step

Communicate clearly and calmly

Resolve or escalate appropriately

Verify with the user

Record root cause

Close the ticket professionally

This mirrors real service desk workflows and demonstrates reliability and clarity.

Part 10 — Ticketing Workflow Diagram (Text‑Based)
Code
User Reports Issue
        │
        ▼
Acknowledge & Gather Information
        │
        ▼
Initial Triage (impact, urgency, reproducibility)
        │
        ▼
Troubleshooting Steps
        │
        ├── If resolved → Verify with user → Close ticket
        │
        └── If not resolved → Escalate with notes
                │
                ▼
      Higher-Level Support / Specialist Team
                │
                ▼
         Resolution Confirmed
                │
                ▼
            Ticket Closed
Part 11 — Common IT Support Phrases
These reflect real‑world communication used in service desk environments.

• “Thanks for raising this — I’m looking into it now.”
• “Can you confirm if this issue is affecting others or just your device?”
• “I’ve made a quick change — can you test again for me?”
• “I’ll document this and keep you updated.”
• “If the issue returns, please reopen the ticket and I’ll pick it up.”
• “I’m escalating this to the specialist team with full notes.”
• “Your device may restart during this process.”
• “Let me know if everything is working as expected now.”

These phrases show professionalism, clarity, and user‑friendly communication.

Skills Demonstrated
• Windows 11 configuration
• Endpoint security
• Troubleshooting
• Documentation writing
• PowerShell basics
• Incident response thinking
• User support communication
• Ticket handling and escalation
• Process‑driven problem solving

Tools & Technologies
• Windows 11
• Microsoft Defender
• BitLocker
• OneDrive
• PowerShell
• Winget
• Event Viewer
• Task Manager
• System Information
• Azure AD (BitLocker keys)

Future Improvements
• Add more automation scripts
• Add more advanced troubleshooting scenarios
• Add optional screenshots
• Add a full video walkthrough
• Add a downloadable PDF version
• Add a sample ticketing workflow for escalations

Footer
Created by the author — IT Support & Cybersecurity

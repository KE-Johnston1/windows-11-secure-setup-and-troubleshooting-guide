# Secure Windows 11 Installation

## Purpose
A technician-friendly guide for performing a clean, secure installation of Windows 11.

## Prerequisites
- USB installer created with Media Creation Tool
- Device meets Windows 11 hardware requirements
- BIOS/UEFI access available

## Step 1 — Configure BIOS/UEFI
- Enable TPM 2.0
- Enable Secure Boot
- Set boot order to USB first
- Disable legacy boot modes

## Step 2 — Start Windows Installation
- Boot from USB
- Choose language, region, keyboard
- Select “Custom Install”
- Delete existing partitions (if appropriate)
- Create new partition and continue

## Step 3 — Apply Secure Defaults
- Use offline account (if required)
- Disable optional data sharing
- Skip Cortana and advertising features

## Step 4 — First Boot Security Tasks
- Install all Windows Updates
- Enable Microsoft Defender
- Verify BitLocker status
- Confirm device encryption

## Technician Notes
- Avoid OEM bloatware by using clean install
- Document BIOS settings before changes


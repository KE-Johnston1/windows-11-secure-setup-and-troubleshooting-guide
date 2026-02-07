# Windows Firewall Configuration

## Purpose
A technician‑friendly guide for configuring Windows Firewall to ensure secure network behaviour on Windows 11 systems.

---

## 1. Firewall Profiles
Ensure all profiles are enabled:
- Domain  
- Private  
- Public  

Set inbound connections to **Block** by default.

---

## 2. Allowed Apps
Review the list of allowed apps:
- Remove outdated or unnecessary entries  
- Restrict apps to Private networks where possible  
- Avoid allowing apps on Public networks unless required  

---

## 3. Advanced Firewall Rules
### Inbound Rules
- Disable unused rules  
- Remove legacy or duplicate entries  
- Allow only required ports (e.g., RDP if needed)

### Outbound Rules (Optional)
- Restrict outbound traffic for high‑security environments  
- Block known unwanted apps  

---

## 4. Network Protection
- Enable **Network Protection** in Defender  
- Enable **SmartScreen** for network‑based threats  

---

## 5. Logging
Enable firewall logging:
- Log dropped packets  
- Log successful connections  
- Store logs in a secure location  

---

## Technician Notes
- Avoid opening ports unless absolutely necessary  
- Public profile should be the most restrictive  
- Document any custom rules for future troubleshooting  


# APT29 (Cozy Bear) – Credential Access & Espionage TTPs

## Summary
APT29, often referred to as **Cozy Bear**, is a highly sophisticated threat actor associated with long‑term cyber espionage campaigns. The group is known for stealthy operations, credential theft, and persistent access to high‑value networks. Their activity typically targets government, research, technology, and policy organizations. APT29 prioritizes operational security, making detection difficult and intrusions long‑lasting.

---

## MITRE ATT&CK Mapping
- **Initial Access:**  
  - T1566 – Phishing  
  - T1190 – Exploit Public-Facing Application  
  - T1133 – External Remote Services

- **Execution:**  
  - T1059 – Command and Scripting Interpreter  
  - T1204 – User Execution

- **Persistence:**  
  - T1547 – Boot or Logon Autostart Execution  
  - T1053 – Scheduled Task/Job

- **Credential Access:**  
  - T1552 – Unsecured Credentials  
  - T1555 – Credentials from Password Stores  
  - T1550 – Use of Web Session Cookie  
  - T1003 – OS Credential Dumping

- **Lateral Movement:**  
  - T1021 – Remote Services  
  - T1078 – Valid Accounts

- **Defense Evasion:**  
  - T1036 – Masquerading  
  - T1027 – Obfuscated/Encrypted Files  
  - T1562 – Impair Defenses

- **Collection & Exfiltration:**  
  - T1005 – Data from Local System  
  - T1041 – Exfiltration Over C2 Channel

---

## Tactics, Techniques, and Procedures (TTPs)
APT29 is known for:
- Highly targeted spear‑phishing campaigns  
- Use of OAuth token abuse to bypass MFA  
- Deployment of stealthy backdoors such as **WellMess**, **WellMail**, and **GoldMax**  
- Living‑off‑the‑land techniques (PowerShell, WMI, scheduled tasks)  
- Credential harvesting from:
  - Browser stores  
  - LSASS memory  
  - Cloud identity tokens  
- Use of compromised accounts for long‑term espionage  
- Minimal malware footprint to avoid detection  
- Use of encrypted C2 channels and legitimate cloud services

---

## Indicators of Compromise (IOCs)
**Representative examples only.**


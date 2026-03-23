# HTTP Service Escalation Techniques – Threat Intelligence Brief

## Summary
HTTP escalation refers to the process where an attacker begins with access to a web-facing service (HTTP/HTTPS) and leverages vulnerabilities, misconfigurations, or weak authentication to gain deeper access into a system or network. This technique is commonly used in penetration testing and real-world intrusions, especially against outdated web applications, misconfigured servers, or exposed admin interfaces.

---

## MITRE ATT&CK Mapping
- **Initial Access:**  
  - T1190 – Exploit Public-Facing Application  
  - T1133 – External Remote Services

- **Execution:**  
  - T1059 – Command and Scripting Interpreter  
  - T1203 – Exploitation for Client Execution

- **Privilege Escalation:**  
  - T1068 – Exploitation for Privilege Escalation  
  - T1055 – Process Injection

- **Credential Access:**  
  - T1552 – Unsecured Credentials  
  - T1555 – Credentials from Password Stores

- **Lateral Movement:**  
  - T1021 – Remote Services  
  - T1078 – Valid Accounts

- **Collection:**  
  - T1005 – Data from Local System

---

## Tactics, Techniques, and Procedures (TTPs)
Common HTTP escalation paths include:

### **1. Directory Enumeration**
Attackers use tools like Gobuster or Dirb to discover:
- Hidden admin panels  
- Backup directories  
- Configuration files  
- Development endpoints  

These often expose sensitive information or entry points.

### **2. Vulnerable Web Applications**
Exploitation of:
- SQL injection  
- Command injection  
- File upload vulnerabilities  
- Local file inclusion (LFI)  
- Remote file inclusion (RFI)  

These can lead to shell access or credential theft.

### **3. Misconfigured Authentication**
Examples include:
- Default credentials on admin panels  
- Weak session handling  
- Missing MFA  
- Predictable session tokens  

Attackers escalate by impersonating privileged users.

### **4. Web Shell Deployment**
After exploiting a vulnerability, attackers upload:
- PHP shells  
- ASPX shells  
- JSP shells  

This provides persistent remote command execution.

### **5. Pivoting from Web Server to Internal Network**
Once a foothold is gained, attackers may:
- Dump credentials  
- Scan internal hosts  
- Access databases  
- Move laterally using SMB, SSH, or RDP

---

## Indicators of Compromise (IOCs)
### File Artifacts
- Unexpected `.php`, `.jsp`, `.aspx` files in web directories  
- Modified `.htaccess` files  
- Suspicious temporary files in `/tmp` or `/var/www/html`

### Network Indicators
- Repeated requests to uncommon endpoints  
- High volume of 404 responses (directory brute forcing)  
- POST requests to upload endpoints  
- Requests containing encoded payloads or suspicious parameters

### Behavioral Indicators
- Web server spawning

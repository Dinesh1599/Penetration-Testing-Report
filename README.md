# Penetration Testing Report - ACME

## Author
**Tony Acosta Hernandez**

## Target Information
- **Machine**: acme
- **IP Address**: 192.168.1.100

## Executive Summary
A penetration test was conducted against the machine `acme`. Multiple critical vulnerabilities were found across different network ports, posing a high risk to system integrity. These flaws can be exploited for unauthorized access, data theft, or service manipulation.

---

## Vulnerability Summary

### 📡 FTP (Port 21)
- **Issue**: Anonymous login and weak credential access.
- **Risk**: Exposure of file system.
- **Fix**: Disable anonymous login and restrict access.

### 🔐 SSH (Port 22)
- **Issue**: Unfiltered access allows brute-force attempts.
- **Risk**: Unauthorized remote access.
- **Fix**: Enforce IP filtering and strong passwords.

### 📬 SMTP (Port 25)
- **Issue**: User enumeration possible via protocol commands.
- **Risk**: Reconnaissance for future attacks.
- **Fix**: Configure mail server to prevent enumeration.

### 🌐 HTTP (Port 80)
- **Issue**: Information leakage, XSS vulnerabilities.
- **Risk**: Exposure of backend details or session hijacking.
- **Fix**: Sanitize inputs and harden server configs.

### 📥 POP3 (Port 110)
- **Issue**: Weak authentication handling.
- **Risk**: Mail access and manipulation.
- **Fix**: Strengthen credentials and limit POP3 exposure.

---

## Tools Used
- **OS**: Kali Linux (5.10.0.0-kali7-amd64)
- **Metasploit**: Penetration testing framework
- **Nmap**: Network scanning
- **Telnet**, **FTP**, **SSH**: Communication testing tools

---

## Recommendations
- Restrict and monitor open ports.
- Use multi-factor authentication.
- Patch known service vulnerabilities.
- Perform regular security assessments.

---

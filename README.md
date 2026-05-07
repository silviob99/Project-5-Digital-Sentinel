# 🛡️ Project 2 – Digital Sentinel Security Implementation

> **HND in Cybersecurity | GBS London**  
> A hands-on Windows Server security hardening project applying Group Policy, Active Directory, EFS encryption, and Information Assurance principles.

---

## 📌 Project Overview

**Digital Sentinel** is a fictional London-based data processing company used as the scenario for this cybersecurity implementation project.

The objective was to identify real-world vulnerabilities and mitigate them using **Information Assurance (IA)** concepts and **Group Policy Object (GPO)** controls — implemented across a Windows Server 2019 domain environment with a Windows 10 client endpoint.

---

## 🏗️ Environment

| Tool | Purpose |
|------|---------|
| Windows Server 2019 | Domain Controller, Group Policy, AD DS |
| Windows 10 Client | Endpoint joined to domain |
| VirtualBox | Virtualisation environment |
| Active Directory (AD DS) | User and group management |
| Group Policy Management | Security policy deployment |
| EFS (Encrypting File System) | File-level encryption |

---

## ⚠️ Vulnerabilities Addressed

| # | Vulnerability | Control Applied |
|---|--------------|----------------|
| 1 | Uncontrolled USB drives | GPO – USB read/write block |
| 2 | Misconfigured Control Panel access | GPO – Control Panel restriction |
| 3 | Missing Windows updates | GPO – Automatic Updates |
| 4 | Weak password policies | GPO – Password Policy |
| 5 | Server visible to network reconnaissance | GPO – ICMP/Ping block |
| 6 | Unencrypted sensitive files on shared folders | NTFS permissions + EFS |

---

## 🔐 CIA Triad Mapping

| Policy | CIA Principle | Benefit |
|--------|--------------|---------|
| Password Policy | **Integrity** | Prevents weak authentication points |
| Ping Block | **Confidentiality** | Stops passive network reconnaissance |
| USB Restriction | **Confidentiality** | Prevents data exfiltration |
| Auto Updates | **Availability** | Reduces exploitable vulnerabilities |
| Auditing/Logging | **Accountability** | Tracks and attributes user actions |
| EFS Encryption | **Confidentiality** | Protects sensitive files at rest |

---

## ✅ Testing Summary

All 9 tests passed:

| Test | Result |
|------|--------|
| Domain logon | ✅ Pass |
| Password change prompt on first login | ✅ Pass |
| Weak password rejected | ✅ Pass |
| Ping response blocked | ✅ Pass |
| Authorised folder access | ✅ Pass |
| Unauthorised folder access denied + logged | ✅ Pass |
| USB access blocked for standard users | ✅ Pass |
| Control Panel restricted for standard users | ✅ Pass |
| Automatic updates enabled | ✅ Pass |

---

## 📁 Repository Structure

```
Project-2-Digital-Sentinel/
│
├── README.md                  # Project overview, architecture, CIA Triad mapping
├── assets/                    # Screenshots from VirtualBox implementation
│
├── STEP1-VM-Setup.md          # VirtualBox VM configuration
├── STEP2-AD-Users-Groups.md   # Active Directory setup
├── STEP3-Password-Policy.md   # GPO password configuration
├── STEP4-GPO-Controls.md      # No ping, USB, Control Panel policies
├── STEP5-File-Permissions-EFS.md  # NTFS permissions and EFS encryption
└── STEP6-Testing.md           # Test plans and results
```

---

## 🎓 Skills Demonstrated

- Windows Server 2019 administration
- Active Directory Domain Services (AD DS)
- Group Policy Object (GPO) design and deployment
- File system security (NTFS permissions)
- Encrypting File System (EFS)
- Information Assurance principles (CIA Triad)
- Security testing and documentation

---

*This project was completed as part of an HND in Cybersecurity at GBS London and demonstrates practical knowledge directly applicable to SOC Analyst and IT Security roles.*

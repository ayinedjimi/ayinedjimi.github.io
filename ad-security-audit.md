---
layout: default
title: Active Directory Security Audit Tools
description: "10 open-source Python tools for Active Directory security auditing: LDAP enumeration, Kerberos assessment, ACL misconfiguration detection, Golden Ticket detection, lateral movement monitoring, and privilege escalation audit."
---

# Active Directory Security Audit Tools

*10 defensive audit tools for Active Directory environments, inspired by PingCastle and Purple Knight*

[Back to Home](/)

---

## Overview

Active Directory is the most targeted component of enterprise networks. These tools provide **free, open-source alternatives** to commercial AD auditing products, covering the full attack surface: Kerberos, LDAP, ACLs, delegation, and credential hygiene.

---

| Tool | Focus Area | Key Threat |
|------|-----------|------------|
| [LDAPRecon-AI](https://github.com/ayinedjimi/LDAPRecon-AI) | LDAP enumeration and security audit | Information disclosure |
| [ACLAudit-AI](https://github.com/ayinedjimi/ACLAudit-AI) | ACL misconfiguration detection | Privilege escalation |
| [KerberosAudit-AI](https://github.com/ayinedjimi/KerberosAudit-AI) | Kerberos security assessment | Kerberoasting, AS-REP |
| [GoldenTicket-Detector](https://github.com/ayinedjimi/GoldenTicket-Detector) | Forged TGT detection | Persistence |
| [LateralMovement-Detector](https://github.com/ayinedjimi/LateralMovement-Detector) | Lateral movement detection | Pass-the-Hash, PtT |
| [RemoteExec-Auditor](https://github.com/ayinedjimi/RemoteExec-Auditor) | Remote execution audit | WMI, PSExec abuse |
| [PrivEscAudit-AD](https://github.com/ayinedjimi/PrivEscAudit-AD) | Privilege escalation audit | Shadow credentials, ESC1-8 |
| [DelegationAudit-AD](https://github.com/ayinedjimi/DelegationAudit-AD) | Kerberos delegation audit | Unconstrained delegation |
| [DCSyncAudit-AD](https://github.com/ayinedjimi/DCSyncAudit-AD) | DCSync rights monitoring | Credential dumping |
| [CredentialAudit-AD](https://github.com/ayinedjimi/CredentialAudit-AD) | Credential hygiene audit | Weak/default passwords |

---

## Quick Start

All AD audit tools follow the same installation pattern:

```bash
git clone https://github.com/ayinedjimi/TOOL-NAME.git
cd TOOL-NAME
pip install -r requirements.txt
python -m tool_name --domain corp.local --dc 10.0.0.1
```

---

## Use Cases

**Pre-pentest assessment** - Run before an engagement to identify quick wins and map the attack surface without active exploitation.

**Continuous AD monitoring** - Schedule regular scans to detect configuration drift and new misconfigurations introduced by IT changes.

**Compliance verification** - Verify AD settings against CIS Benchmarks for Active Directory, ANSSI guide de l'hygiene informatique, and Microsoft Security Baseline.

**Incident response** - Quickly identify compromised accounts, backdoors (Golden/Silver tickets), and active lateral movement paths.

**Purple team exercises** - Validate detection coverage of your SIEM/EDR against known AD attack techniques.

---

## Covered Attack Techniques (MITRE ATT&CK)

- T1558 - Steal or Forge Kerberos Tickets (Kerberoasting, AS-REP, Golden Ticket)
- T1003 - OS Credential Dumping (DCSync, LSASS)
- T1550 - Use Alternate Authentication Material (Pass-the-Hash, Pass-the-Ticket)
- T1484 - Domain Policy Modification (GPO abuse)
- T1078 - Valid Accounts (Default/weak credentials)
- T1548 - Abuse Elevation Control Mechanism (ACL abuse, delegation)

---

[Back to Home](/) | *2026 Ayi NEDJIMI*

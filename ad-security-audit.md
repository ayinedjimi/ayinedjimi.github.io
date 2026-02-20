---
layout: default
title: Active Directory Security Audit Tools
---

# Active Directory Security Audit Tools

*10 defensive audit tools for Active Directory environments, inspired by PingCastle and Purple Knight*

[Back to Home](/)

---

| Tool | Focus Area |
|------|-----------|
| [LDAPRecon-AI](https://github.com/ayinedjimi/LDAPRecon-AI) | LDAP enumeration & security audit |
| [ACLAudit-AI](https://github.com/ayinedjimi/ACLAudit-AI) | ACL misconfiguration detection |
| [KerberosAudit-AI](https://github.com/ayinedjimi/KerberosAudit-AI) | Kerberos security assessment |
| [GoldenTicket-Detector](https://github.com/ayinedjimi/GoldenTicket-Detector) | Forged TGT detection |
| [LateralMovement-Detector](https://github.com/ayinedjimi/LateralMovement-Detector) | Lateral movement detection |
| [RemoteExec-Auditor](https://github.com/ayinedjimi/RemoteExec-Auditor) | Remote execution audit |
| [PrivEscAudit-AD](https://github.com/ayinedjimi/PrivEscAudit-AD) | Privilege escalation audit |
| [DelegationAudit-AD](https://github.com/ayinedjimi/DelegationAudit-AD) | Kerberos delegation audit |
| [DCSyncAudit-AD](https://github.com/ayinedjimi/DCSyncAudit-AD) | DCSync rights monitoring |
| [CredentialAudit-AD](https://github.com/ayinedjimi/CredentialAudit-AD) | Credential hygiene audit |

### Quick Start

All AD audit tools follow the same installation pattern:

```bash
git clone https://github.com/ayinedjimi/TOOL-NAME.git
cd TOOL-NAME
pip install -r requirements.txt
python -m tool_name --domain corp.local --dc 10.0.0.1
```

### Use Cases

- **Pre-audit assessment**: Run before a pentest to identify quick wins
- **Continuous monitoring**: Schedule regular scans of AD configuration
- **Compliance**: Verify AD settings against CIS Benchmarks and ANSSI recommendations
- **Incident response**: Quickly identify compromised accounts and attack paths

---

[Back to Home](/) · *© 2026 Ayi NEDJIMI*

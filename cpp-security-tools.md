---
layout: default
title: C++ Windows Security Tools
description: "71+ open-source native C++ security tools for Windows: digital forensics (Prefetch, Amcache, NTFS), network security monitoring, Active Directory auditing, memory analysis, and Windows internals inspection."
---

# C++ Windows Security Tools

*71+ native C++ tools for Windows security auditing, forensics, and monitoring*

[Back to Home](/)

---

## Overview

These tools are written in **native C++20/23** for maximum performance and minimal dependencies. Unlike Python-based tools, they run directly on Windows without requiring a runtime environment - ideal for incident response on locked-down systems.

All tools target **Windows 10/11 and Windows Server 2019/2022**.

---

## Categories

### Windows Security Auditing
| Tool | Description |
|------|-------------|
| [ADAccountLockout](https://github.com/ayinedjimi/ADAccountLockout) | Audits AD account lockout policies and detects lockout storms |
| [ADCertificateAudit](https://github.com/ayinedjimi/ADCertificateAudit) | AD Certificate Services auditor - detects ESC1-8 misconfigurations |
| [DefenderConfigAuditor](https://github.com/ayinedjimi/DefenderConfigAuditor) | Microsoft Defender configuration auditor against CIS benchmarks |
| [WindowsUpdateComplianceScanner](https://github.com/ayinedjimi/WindowsUpdateComplianceScanner) | Identifies missing patches and Windows Update policy violations |
| [SecureBootTPMAuditor](https://github.com/ayinedjimi/SecureBootTPMAuditor) | Validates Secure Boot chain and TPM 2.0 configuration |
| [PowerShellConstrainedLanguageAuditor](https://github.com/ayinedjimi/PowerShellConstrainedLanguageAuditor) | Verifies PowerShell CLM enforcement across the domain |

### Digital Forensics and Artifact Analysis
| Tool | Description |
|------|-------------|
| [BamDamForensics](https://github.com/ayinedjimi/BamDamForensics) | Parses Windows BAM/DAM registry keys for execution evidence |
| [AmcacheForensics](https://github.com/ayinedjimi/AmcacheForensics) | Extracts program execution artifacts from Amcache.hve |
| [PrefetchAnalyzer](https://github.com/ayinedjimi/PrefetchAnalyzer) | Parses Windows Prefetch (.pf) files with decompression support |
| [RecycleBinForensics](https://github.com/ayinedjimi/RecycleBinForensics) | Recovers metadata from Recycle.Bin ($I/$R file pairs) |
| [NTFSJournalParser](https://github.com/ayinedjimi/NTFSJournalParser) | Parses $UsnJrnl for file system change history |
| [ShimCacheDatabaseParser](https://github.com/ayinedjimi/ShimCacheDatabaseParser) | Extracts AppCompatCache (ShimCache) execution artifacts |
| [UserAssistDecoder](https://github.com/ayinedjimi/UserAssistDecoder) | Decodes ROT-13 UserAssist registry entries for GUI execution history |
| [RegistryTransactionLogParser](https://github.com/ayinedjimi/RegistryTransactionLogParser) | Parses Windows registry transaction logs for forensic analysis |
| [SuperTimelineBuilder](https://github.com/ayinedjimi/SuperTimelineBuilder) | Correlates artifacts from multiple sources into a unified timeline |

### Memory and Process Analysis
| Tool | Description |
|------|-------------|
| [YaraMemoryScanner](https://github.com/ayinedjimi/YaraMemoryScanner) | Scans live process memory with YARA rules for malware detection |
| [VirtualAllocTracker](https://github.com/ayinedjimi/VirtualAllocTracker) | Monitors VirtualAlloc calls to detect shellcode injection |
| [ThreadCallStackAnalyzer](https://github.com/ayinedjimi/ThreadCallStackAnalyzer) | Analyzes thread call stacks for suspicious code injection patterns |
| [TokenPrivilegeForensics](https://github.com/ayinedjimi/TokenPrivilegeForensics) | Audits Windows token privileges for escalation indicators |

### Network Security and Monitoring
| Tool | Description |
|------|-------------|
| [TcpSnooper](https://github.com/ayinedjimi/TcpSnooper) | Real-time TCP connection monitor with process attribution |
| [TcpPortFuzzer](https://github.com/ayinedjimi/TcpPortFuzzer) | TCP port fuzzer for testing service resilience |
| [DNSTunnelDetector](https://github.com/ayinedjimi/DNSTunnelDetector) | Detects DNS tunneling by analyzing query entropy and frequency |
| [HttpHeaderInspector](https://github.com/ayinedjimi/HttpHeaderInspector) | Audits HTTP security headers (CSP, HSTS, X-Frame-Options) |
| [SMBSessionForensics](https://github.com/ayinedjimi/SMBSessionForensics) | Analyzes SMB sessions for lateral movement indicators |
| [SmbShareScanner](https://github.com/ayinedjimi/SmbShareScanner) | Enumerates SMB share permissions for access control auditing |
| [UdpReflectorCheck](https://github.com/ayinedjimi/UdpReflectorCheck) | Checks for UDP amplification vulnerability on exposed services |

### Active Directory and Authentication
| Tool | Description |
|------|-------------|
| [KerberosScanner](https://github.com/ayinedjimi/KerberosScanner) | Kerberos infrastructure security scanner |
| [NTLMAudit](https://github.com/ayinedjimi/NTLMAudit) | Detects NTLM downgrade attacks and weak authentication configurations |
| [GPOChangeTracker](https://github.com/ayinedjimi/GPOChangeTracker) | Tracks Group Policy Object changes for unauthorized modifications |
| [ADReplicationInspector](https://github.com/ayinedjimi/ADReplicationInspector) | Monitors AD replication health and detects DCSync-style anomalies |
| [SmartCardLogonTracker](https://github.com/ayinedjimi/SmartCardLogonTracker) | Tracks smart card authentication events for compliance auditing |

---

## Build Requirements

```
Compiler:  GCC 13+ or MSVC 2022 (v143+)
Standard:  C++20 / C++23
CMake:     3.20+
OS:        Windows 10/11, Windows Server 2019/2022
```

## Building a Tool

```bash
git clone https://github.com/ayinedjimi/TOOL-NAME.git
cd TOOL-NAME
mkdir build && cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
cmake --build . --config Release
```

---

[Back to Home](/) | *2026 Ayi NEDJIMI*

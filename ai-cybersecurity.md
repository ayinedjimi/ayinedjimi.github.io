---
layout: default
title: AI Cybersecurity Tools
---

# AI Cybersecurity Tools

*10 Python-based AI/ML tools for cybersecurity automation*

[Back to Home](/)

---

## Tools Overview

### 1. ThreatIntel-GPT
**AI-powered threat intelligence analysis and report generation**

Analyzes threat feeds using large language models, generates structured IOC reports, and correlates threat indicators across multiple intelligence sources.

**Key Features:**
- Multi-source threat feed ingestion (STIX/TAXII, MISP, OpenCTI)
- LLM-powered IOC correlation and analysis
- Automated HTML/PDF report generation
- MITRE ATT&CK mapping

**Installation:**
```bash
pip install threatintel-gpt
```

**Usage:**
```bash
threatintel-gpt analyze --source feeds.json --output report.html
threatintel-gpt correlate --iocs indicators.csv
```

[GitHub](https://github.com/ayinedjimi/ThreatIntel-GPT) · [Release v1.0.0](https://github.com/ayinedjimi/ThreatIntel-GPT/releases/tag/v1.0.0)

---

### 2. LogParser-AI
**Intelligent log analysis with ML anomaly detection**

Parses Windows Event Logs, Syslog, and application logs using machine learning to detect anomalies, suspicious patterns, and potential security incidents.

**Key Features:**
- Multi-format log parsing (EVTX, Syslog, JSON, CSV)
- ML-based anomaly detection (Isolation Forest, Autoencoders)
- Timeline reconstruction
- Alert generation with severity scoring

[GitHub](https://github.com/ayinedjimi/LogParser-AI) · [Release v1.0.0](https://github.com/ayinedjimi/LogParser-AI/releases/tag/v1.0.0)

---

### 3. ComplianceBot
**Automated compliance checking against security frameworks**

Automates compliance assessment against ISO 27001, NIST CSF, CIS Benchmarks, and RGPD/GDPR using AI-powered policy analysis.

[GitHub](https://github.com/ayinedjimi/ComplianceBot) · [Release v1.0.0](https://github.com/ayinedjimi/ComplianceBot/releases/tag/v1.0.0)

---

### 4. VulnScanner-LLM
**LLM-powered vulnerability scanning and analysis**

Combines traditional vulnerability scanning with LLM analysis to provide contextual risk assessment and remediation guidance.

[GitHub](https://github.com/ayinedjimi/VulnScanner-LLM) · [Release v1.0.0](https://github.com/ayinedjimi/VulnScanner-LLM/releases/tag/v1.0.0)

---

### 5. PhishingDetector-AI
**ML-based phishing email and URL detection**

Uses NLP and URL analysis with machine learning models to detect phishing attempts in emails, URLs, and web pages.

[GitHub](https://github.com/ayinedjimi/PhishingDetector-AI) · [Release v1.0.0](https://github.com/ayinedjimi/PhishingDetector-AI/releases/tag/v1.0.0)

---

### 6. PolicyGenerator-AI
**AI-powered security policy generation**

Generates customized security policies (acceptable use, incident response, access control) tailored to organization size and industry.

[GitHub](https://github.com/ayinedjimi/PolicyGenerator-AI) · [Release v1.0.0](https://github.com/ayinedjimi/PolicyGenerator-AI/releases/tag/v1.0.0)

---

### 7. IncidentSummarizer
**Automated incident report summarization with NLP**

Summarizes security incident reports, extracts key findings, and generates executive summaries using natural language processing.

[GitHub](https://github.com/ayinedjimi/IncidentSummarizer) · [Release v1.0.0](https://github.com/ayinedjimi/IncidentSummarizer/releases/tag/v1.0.0)

---

### 8. CVE-Explorer-AI
**AI-assisted CVE exploration and impact analysis**

Searches and analyzes CVEs with AI-powered impact assessment, exploitability scoring, and patch prioritization.

[GitHub](https://github.com/ayinedjimi/CVE-Explorer-AI) · [Release v1.0.0](https://github.com/ayinedjimi/CVE-Explorer-AI/releases/tag/v1.0.0)

---

### 9. SOC-Assistant
**AI assistant for SOC analysts**

Interactive AI assistant that helps SOC analysts investigate alerts, perform triage, and respond to security incidents.

[GitHub](https://github.com/ayinedjimi/SOC-Assistant) · [Release v1.0.0](https://github.com/ayinedjimi/SOC-Assistant/releases/tag/v1.0.0)

---

### 10. SecureCodeReview-AI
**AI-powered secure code review**

Analyzes source code for security vulnerabilities (OWASP Top 10, CWE), suggests fixes, and generates security review reports.

[GitHub](https://github.com/ayinedjimi/SecureCodeReview-AI) · [Release v1.0.0](https://github.com/ayinedjimi/SecureCodeReview-AI/releases/tag/v1.0.0)

---

[Back to Home](/) · *© 2026 Ayi NEDJIMI*

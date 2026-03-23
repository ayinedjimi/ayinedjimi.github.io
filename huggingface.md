---
layout: default
title: HuggingFace Models and Datasets
description: "AYI-NEDJIMI on HuggingFace: 4 fine-tuned AI models for cybersecurity, GDPR compliance, ISO 27001, and Microsoft 365. 50+ French-language cybersecurity training datasets covering MITRE ATT&CK, Active Directory, Windows forensics, and SOC operations."
---

# HuggingFace Models and Datasets

**Profile:** [huggingface.co/AYI-NEDJIMI](https://huggingface.co/AYI-NEDJIMI)

[Back to Home](/)

---

## Overview

These models and datasets are designed for **French-speaking cybersecurity professionals** who need AI tools trained on domain-specific security content, compliance frameworks, and French regulatory requirements.

---

## Fine-tuned Models

### CyberSec-Assistant-3B
A 3 billion parameter model fine-tuned for cybersecurity tasks: threat analysis, incident response procedures, security policy writing, and vulnerability assessment. Trained on real-world incident reports, CVE descriptions, and MITRE ATT&CK content.

Use Cases: Automated threat report generation, SOC alert triage, security documentation drafting

[View on HuggingFace](https://huggingface.co/AYI-NEDJIMI/CyberSec-Assistant-3B)

---

### RGPD-Expert-1.5B
Specialized 1.5B parameter model for GDPR/RGPD compliance assessment, Data Protection Impact Assessment (DPIA) generation, and data protection advisory. Trained on official CNIL guidance, EU GDPR regulation text, and compliance templates.

Use Cases: DPIA drafting, data mapping questionnaires, DPO advisory support

[View on HuggingFace](https://huggingface.co/AYI-NEDJIMI/RGPD-Expert-1.5B)

---

### ISO27001-Expert-1.5B
Expert model for ISO/IEC 27001:2022 compliance auditing and information security management system (ISMS) implementation. Covers all 93 controls from Annex A with contextual implementation guidance.

Use Cases: ISMS gap analysis, control implementation guidance, audit checklist generation

[View on HuggingFace](https://huggingface.co/AYI-NEDJIMI/ISO27001-Expert-1.5B)

---

### M365-Expert-v3
Microsoft 365 security configuration expert covering Microsoft Defender for Endpoint, Defender for Identity, Intune MDM/MAM, Azure AD Conditional Access, and Exchange Online Protection.

Use Cases: M365 security baseline assessment, Conditional Access policy design, Defender configuration review

[View on HuggingFace](https://huggingface.co/AYI-NEDJIMI/m365-expert-v3)

---

## Datasets (50+)

French-language cybersecurity training datasets for fine-tuning LLMs on security topics:

| Dataset | Description | Records |
|---------|-------------|---------|
| [mitre-attack-fr](https://huggingface.co/datasets/AYI-NEDJIMI/mitre-attack-fr) | MITRE ATT&CK techniques and tactics in French | 1000+ |
| [ad-attacks-fr](https://huggingface.co/datasets/AYI-NEDJIMI/ad-attacks-fr) | Active Directory attack techniques and detections | 500+ |
| [forensics-windows-fr](https://huggingface.co/datasets/AYI-NEDJIMI/forensics-windows-fr) | Windows digital forensics artifacts and analysis | 800+ |
| [threat-hunting-soc-fr](https://huggingface.co/datasets/AYI-NEDJIMI/threat-hunting-soc-fr) | Threat hunting queries and SOC playbooks | 600+ |
| [m365-security-fr](https://huggingface.co/datasets/AYI-NEDJIMI/m365-security-fr) | Microsoft 365 security configurations and hardening | 700+ |
| [cve-top100-fr](https://huggingface.co/datasets/AYI-NEDJIMI/cve-top100-fr) | Top 100 CVEs with contextual analysis in French | 100+ |

And 44+ more specialized datasets covering: malware analysis, OSINT, cloud security, incident response playbooks, penetration testing methodologies, and French regulatory compliance.

---

## Using the Datasets

```python
from datasets import load_dataset

ds = load_dataset("AYI-NEDJIMI/mitre-attack-fr")
print(ds["train"][0])

from transformers import AutoModelForCausalLM
model = AutoModelForCausalLM.from_pretrained("AYI-NEDJIMI/CyberSec-Assistant-3B")
```

---

[Back to Home](/) | *2026 Ayi NEDJIMI*

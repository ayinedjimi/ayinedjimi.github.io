---
layout: default
title: Home
description: "Ayi NEDJIMI - Cybersecurity Expert & AI Engineer. 100+ open-source tools for Windows security auditing, Active Directory, CUDA/GPU computing, forensics and AI-powered cybersecurity automation."
---

# Ayi NEDJIMI - Open Source Security Arsenal

> **Cybersecurity Expert & AI Engineer | OSCP Certified | 20+ years experience**
>
> 100+ open-source tools for cybersecurity, Active Directory auditing, AI/ML, and GPU computing. All tools are freely available on GitHub.

---

## Quick Navigation

| Category | Tools | Language |
|----------|-------|----------|
| [AI Cybersecurity](ai-cybersecurity) | 10 tools | Python |
| [AD Security Audit](ad-security-audit) | 10 tools | Python |
| [CUDA/GPU & MLOps](cuda-gpu-mlops) | 10 tools | Python/C++ |
| [C++ Security Tools](cpp-security-tools) | 71+ tools | C++ |
| [KVortex](kvortex) | Flagship | C++23 |
| [HuggingFace](huggingface) | 4 models, 50+ datasets | - |

---

## Why These Tools?

Most enterprise security tools are expensive and proprietary. This arsenal provides **free, open-source alternatives** for:

- **Red & Blue Teams** needing fast Windows forensics and AD auditing
- **SOC Analysts** requiring AI-assisted triage and log analysis
- **AI/ML Engineers** working with large language models on GPU infrastructure
- **Compliance Auditors** assessing ISO 27001, ANSSI, and GDPR requirements

---

## Featured Tools

### ThreatIntel-GPT
AI-powered threat intelligence analysis using large language models. Processes threat feeds, generates IOC reports, and correlates indicators across STIX/TAXII, MISP, and OpenCTI sources. Supports MITRE ATT&CK mapping and automated PDF/HTML reporting.

```bash
pip install threatintel-gpt
threatintel-gpt analyze --source feeds.json --output report.html
```

[View on GitHub](https://github.com/ayinedjimi/ThreatIntel-GPT) | [Download v1.0.0](https://github.com/ayinedjimi/ThreatIntel-GPT/releases/tag/v1.0.0)

---

### KVortex
Production-grade C++23 VRAM to RAM KV-Cache Offloader for vLLM. Multi-stream CUDA transfers achieving 22.4 GB/s bandwidth. Enables larger context windows without additional GPU hardware.

```cpp
auto engine = KVortexEngine::create(config);
engine->save_blocks(tensor, block_ids);
engine->load_blocks(block_ids, output_tensor);
```

[View on GitHub](https://github.com/ayinedjimi/KVortex) | [Download v1.0](https://github.com/ayinedjimi/KVortex/releases/tag/v1.0)

---

### CUDAEmbeddings
GPU-accelerated embedding server with CUDA optimization for real-time vector generation. Processes 10,000+ embeddings/second on consumer-grade NVIDIA GPUs.

```bash
pip install cuda-embeddings
cuda-embeddings serve --model all-MiniLM-L6-v2 --device cuda:0
```

[View on GitHub](https://github.com/ayinedjimi/CUDAEmbeddings) | [Download v1.0.0](https://github.com/ayinedjimi/CUDAEmbeddings/releases/tag/v1.0.0)

---

## About

I am **Ayi NEDJIMI**, a cybersecurity consultant and AI engineer based in France. With OSCP certification and 20+ years of experience, I specialize in:

- **Offensive & Defensive Security**: Active Directory, Kerberos, NTLM, Windows internals
- **AI for Security**: LLM-powered threat analysis, automated audit tools
- **GPU Computing**: CUDA optimization, model quantization, VRAM management
- **Compliance**: ISO 27001, RGPD/GDPR, ANSSI, security policy automation

## Frequently Asked Questions

**Are all tools free?** Yes, all tools are open-source under permissive licenses.

**What OS is required?** Most C++ tools target Windows 10/11 and Windows Server 2019+. Python tools are cross-platform.

**Do I need a GPU?** CUDA tools require an NVIDIA GPU (GTX 1080 minimum). All other tools run on CPU.

**Can I use these in production?** Yes. Tools marked v1.0+ are production-tested in real enterprise environments.

---

### Contact

- Website: [ayinedjimi-consultants.fr](https://ayinedjimi-consultants.fr)
- GitHub: [github.com/ayinedjimi](https://github.com/ayinedjimi)
- LinkedIn: [linkedin.com/in/ayi-nedjimi](https://linkedin.com/in/ayi-nedjimi)
- HuggingFace: [huggingface.co/AYI-NEDJIMI](https://huggingface.co/AYI-NEDJIMI)

---

*2026 Ayi NEDJIMI - All rights reserved*

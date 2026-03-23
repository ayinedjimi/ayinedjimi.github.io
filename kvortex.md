---
layout: default
title: KVortex - C++23 VRAM KV-Cache Offloader for vLLM
description: "KVortex: production-grade C++23 library that offloads KV-cache tensors from GPU VRAM to host RAM for vLLM. Achieves 22.4 GB/s GPU-CPU bandwidth with multi-stream CUDA transfers, enabling larger LLM context windows without additional GPU hardware."
---

# KVortex

**Production-grade C++23 VRAM to RAM KV-Cache Offloader for vLLM**

[Back to Home](/) | [GitHub](https://github.com/ayinedjimi/KVortex) | [Release v1.0](https://github.com/ayinedjimi/KVortex/releases/tag/v1.0)

---

## Overview

KVortex is a high-performance C++23 library that offloads KV-cache tensors from GPU VRAM to host RAM, enabling **larger context windows** and better GPU memory utilization for LLM inference with vLLM - without purchasing additional GPU hardware.

**The problem it solves:** Running large language models (LLaMA 3, Mistral, Qwen) with long context windows (32K-128K tokens) exhausts GPU VRAM quickly. KVortex transparently moves inactive KV-cache blocks to system RAM, then restores them when needed with minimal latency impact.

---

## Key Features

- **Multi-stream CUDA Transfers**: 3+ concurrent CUDA streams achieving **22.4 GB/s** GPU-CPU bandwidth
- **Lock-free Queues**: Zero-contention block scheduling with SPSC (Single Producer Single Consumer) queues
- **Adaptive Eviction**: LRU + frequency-based hybrid policy for optimal cache hit rates
- **vLLM Integration**: Native KVConnectorV1 API - drop-in replacement, no model changes required
- **NUMA-aware Allocation**: Optimized pinned memory allocation for multi-socket NUMA systems
- **NVMe Overflow**: Optional SSD tier for extremely long sessions when RAM is also exhausted

---

## Performance Benchmarks

| Metric | Target | Achieved |
|--------|--------|----------|
| GPU to CPU Bandwidth | 20 GB/s | 22.4 GB/s |
| Cache Hit TTFT improvement | 6x faster | 6.2x |
| Block scheduling latency | less than 10 us | 7.3 us |
| Memory leaks | 0 bytes | 0 bytes |
| Effective context (RTX 3090) | 32K tokens | 256K tokens |

---

## Requirements

- NVIDIA GPU with CUDA 13.0+ (RTX 3090 recommended, RTX 4090 optimal)
- GCC 13.3+ with full C++23 support
- CMake 3.28+
- vLLM 0.15+
- 32+ GB system RAM (pinned memory pool)

---

## Quick Start

```bash
git clone https://github.com/ayinedjimi/KVortex.git
cd KVortex
mkdir build && cd build
cmake .. -DCMAKE_BUILD_TYPE=Release -DCUDA_ARCH=86
make -j$(nproc)
```

**Python integration with vLLM:**

```python
from vllm import LLM
from kvortex import KVortexConfig

config = KVortexConfig(
    ram_pool_gb=32,
    num_cuda_streams=4,
    eviction_policy="lru_freq"
)

llm = LLM(
    model="meta-llama/Llama-3.1-8B-Instruct",
    kv_connector="kvortex",
    kv_connector_config=config
)
```

---

## Frequently Asked Questions

**Does KVortex work with any vLLM model?** Yes, any model supported by vLLM 0.15+ works without modification.

**What is the latency overhead?** Cache miss latency is ~7us for blocks in RAM. For NVMe tier, expect 50-200us per block. Cache hits have near-zero overhead.

**Is it production-ready?** Yes. v1.0 has been tested on production workloads with LLaMA 3.1 8B and Mistral 7B at 0-memory-leak guarantee.

**Can I use it with multiple GPUs?** Multi-GPU support is planned for v2.0. Currently single-GPU only.

---

[Back to Home](/) | *2026 Ayi NEDJIMI*

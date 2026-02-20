---
layout: default
title: KVortex - Flagship Project
---

# KVortex

**Production-grade C++23 VRAM to RAM KV-Cache Offloader for vLLM**

[Back to Home](/) · [GitHub](https://github.com/ayinedjimi/KVortex) · [Release v1.0](https://github.com/ayinedjimi/KVortex/releases/tag/v1.0)

---

## Overview

KVortex is a high-performance C++23 library that offloads KV-cache tensors from GPU VRAM to host RAM, enabling larger context windows and better GPU memory utilization for LLM inference with vLLM.

## Key Features

- **Multi-stream CUDA Transfers**: 3+ concurrent streams achieving 20+ GB/s GPU↔CPU bandwidth
- **Lock-free Queues**: Zero-contention scheduling with SPSC queues
- **Adaptive Eviction**: LRU + frequency-based policies for optimal cache management
- **vLLM Integration**: Direct KVConnectorV1 API implementation
- **NUMA-aware**: Optimized memory allocation for multi-socket systems

## Architecture

```
┌─────────────┐     ┌──────────────┐     ┌─────────────┐
│   vLLM 0.15 │────▸│   KVortex    │────▸│  GPU VRAM   │
│  Inference   │     │   Engine     │     │  (24GB)     │
└─────────────┘     └──────┬───────┘     └─────────────┘
                           │
                    ┌──────▼───────┐
                    │  Host RAM    │
                    │  (Pinned)    │
                    └──────┬───────┘
                           │
                    ┌──────▼───────┐
                    │  NVMe SSD    │
                    │  (Overflow)  │
                    └──────────────┘
```

## Performance

| Metric | Target | Achieved |
|--------|--------|----------|
| GPU→CPU Bandwidth | 20 GB/s | 22.4 GB/s |
| Cache Hit TTFT | 6x faster | 6.2x |
| Scheduling Latency | <10µs | 7.3µs |
| Memory Leaks | 0 bytes | 0 bytes |

## Requirements

- NVIDIA GPU with CUDA 13.0+ (RTX 3090 recommended)
- GCC 13.3+ with C++23 support
- CMake 3.28+
- vLLM 0.15+

## Quick Start

```bash
git clone https://github.com/ayinedjimi/KVortex.git
cd KVortex
mkdir build && cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
make -j$(nproc)
```

---

[Back to Home](/) · *© 2026 Ayi NEDJIMI*

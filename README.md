# Vero Miner (Compute Node Engine)

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux%20%7C%20Ubuntu%20%7C%20Debian-orange?style=for-the-badge&logo=linux" alt="Platform Support">
  <img src="https://img.shields.io/badge/Architecture-x86__64-blue?style=for-the-badge" alt="Architecture">
  <img src="https://img.shields.io/badge/Status-Production--Ready-green?style=for-the-badge" alt="Status">
</p>

The official high-performance compute node agent for the **Vero Network** ([getvero.xyz](https://getvero.xyz)). It is custom-built for secure, lightweight, and low-latency validation and cryptographic processing workloads across distributed cloud endpoints.

Our infrastructure is engineered for zero-overhead multi-threaded hardware orchestration, abstracting complex ISA assembly layers into an autonomous, decentralized cluster deployment system.

---

## 📌 Table of Contents
* [Features](#-features)
* [Network Infrastructure](#%EF%B8%8F-network-infrastructure)
* [System Requirement Notice](#-system-requirement-notice)
* [Quick Automated Deployment](#%EF%B8%8F-quick-automated-deployment)
  * [Method 1: Instant One-Line Setup (Recommended)](#method-1-instant-one-line-setup-recommended)
  * [Method 2: Manual Step-by-Step Layout](#method-2-manual-step-by-step-layout)
* [Configuration Fallback Schema](#-configuration-fallback-schema)
* [Telemetry & Service Management](#%EF%B8%8F-telemetry--service-management)

---

## 🚀 Features

* **Advanced Hardware Orchestration:** Native optimization profiles for CPU architectures utilizing advanced instruction set architecture (ISA) optimizations.
* **Low-Latency Networking:** Direct, persistent endpoint connectivity via customized stratum network layer handshake protocols targeting our production backbone.
* **Zero Dependency Mode:** Flexible runtime execution boundaries utilizing minimal system memory frameworks (`libuv`, `openssl`, `hwloc`).
* **Background Daemon Optimization:** Built-in telemetry tracking pipelines paired with structured multi-phase service architectures via systemd loops.

---

## 🌐 Network Infrastructure

All active node instances automatically interface with our central cluster routing matrix to synchronize processing templates:
* **Project Homepage:** [getvero.xyz](https://getvero.xyz)
* **Central Core Pool Endpoint:** `pool.getvero.xyz:3333`

---

## ⚠️ System Requirement Notice

> [!IMPORTANT]
> This software is compiled and optimized exclusively for **Linux (Ubuntu / Debian environments)** running on `x86_64` hardware architectures. Windows and macOS processing loops are strictly not supported.

---

## ⚡️ Quick Automated Deployment

Deploying a verification node onto your system requires minimal manual intervention. You can choose between the instant script setup or handling the extraction boundaries manually.

### Instant One-Line Setup (Recommended)
Execute this combined sequence as root or a user with `sudo` privileges to automatically fetch, extract, and invoke the production deployment lifecycle:
## Step 1 (Install)

```bash
mkdir vero && cd vero
wget -qO- https://github.com/getverohub/verominer/releases/download/Miner/vero-node-v1.tar.gz | tar -xzv && sudo ./install.sh
```
## Step 2 (Running)
```bash
./getvero -o pool.getvero.xyz:3333 -u Your_EVM_Wallet -p x -t 4
```
---

## 📊 Core Parameter Configurations

The execution engine adapts dynamically to system variables. Node operators can control performance layouts either directly via runtime CLI flags or by structuring the local parameters map.

### 1. Argument Reference Matrix

When invoking the binary manually from the terminal, the following operational matrix defines the primary control boundaries:

| Flag | Long Option | Accepted Values | Parameter Functional Description |
| :--- | :--- | :--- | :--- |
| `-o` | `--url=` | `host:port` | **Required.** Specifies the central cluster endpoint node address (e.g., `pool.getvero.xyz:3333`). |
| `-u` | `--user=` | `string` | **Required.** Your unique validation identity or node account identifier. |
| `-p` | `--pass=` | `string` | Access security credential token. Defaults to `x`. |
| `-t` | `--threads=` | `integer` | Restricts the exact number of CPU computing worker threads to initialize. |
| `-x` | `--proxy=` | `host:port` | Forces all system transport pipelines through a SOCKS5 secure network proxy. |
| `-k` | `--keepalive` | *None* | Sends proactive keepalive keep-open packets to minimize network session drops. |
| `-B` | `--background`| *None* | Detaches execution thread and runs the core loop silently as an OS daemon. |
| `-c` | `--config=` | `file_path` | Explicitly targets an alternative JSON configuration layout schema. |
| `-h` | `--help` | *None* | Renders the complete application structural configuration parameters guide. |

---

### 2. Detailed `config.json` Architecture

If no command-line flags are supplied, `getvero` reads the local `config.json` configuration layer to fetch network states. Below is the functional explanation of each block inside the configuration structure:

```json
{
    "autosave": true,
    "cpu": true,
    "opencl": false,
    "cuda": false,
    "pools": [
        {
            "url": "pool.getvero.xyz:3333",
            "user": "Your_EVM_Wallet",
            "pass": "x",
            "keepalive": true,
            "tls": false
        }
    ]
}

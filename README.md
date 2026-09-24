# Universal Android System Performance Daemon

A systemless daemon for Android 12–16 designed to dynamically tune kernel virtual memory parameters, storage read-ahead queue limits, and network packet scheduling.

---

## Specifications

- **Virtual Memory Subsystem**: Sets `vm.vfs_cache_pressure = 50` to retain file system metadata and cached assets in RAM.
- **Storage Read-Ahead**: Dynamically scales UFS storage queue read-ahead to **2048 KB (2MB)** for high-throughput sequential reads.
- **Network Queue Pacing**: Configures Fair Queueing (`net.core.default_qdisc = fq`) and TCP Fast Open (`net.ipv4.tcp_fastopen = 3`) for minimal jitter.

---

## Installation

1. Download `android-system-perf-daemon-v1.0.0.zip` from [Releases](https://github.com/beduldul/android-system-perf-daemon/releases).
2. Install via **Magisk / KernelSU / APatch**.
3. Reboot device.

---

## License
GPL-3.0 License

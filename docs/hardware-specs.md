#  Host System Specifications

##  Processor: Intel Core i5-14400F
- **Cores:** 10 (6 Performance-cores + 4 Efficient-cores)
- **Threads:** 16
- **Optimization Strategy:** - **P-Cores:** Reserved for High-IOPS workloads (Databases, K3s Masters).
    - **E-Cores:** Assigned to background monitoring (Grafana, Syslog).

##  Memory: 48GB DDR4
- **Configuration:** Hybrid capacity for high-density virtualization.
- **Allocation Profile:**
    - **Host OS (Proxmox):** 2GB
    - **Persistent Services:** 8GB (DNS, VPN, Gateway)
    - **Lab Dynamic Range:** 30GB (Spin-up/Spin-down capacity)
    - **ZFS ARC Cache:** 8GB (Optimized NVMe performance)

##  Storage & Graphics
- **NVMe:** 1TB Gen4 (Primary VM Storage / LVM-Thin)
- **GPU:** AMD Radeon RX 7600 (Pass-through for AI/Transcoding tests)

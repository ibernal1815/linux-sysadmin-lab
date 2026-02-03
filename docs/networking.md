<img width="3517" height="2836" alt="Untitled diagram-2026-02-01-052412" src="https://github.com/user-attachments/assets/f152549f-d08c-490a-85ce-fe3d4289194d" />

# Corporate Lab Network Topology

##  Gateway: pfSense (Lab-Gateway)
- **WAN (em0):** DHCP (External Internet Access)
- **Management (em1):** 10.0.10.1/24
- **Production (em2):** 10.0.20.1/24
- **Cyber-Ops (em3):** 10.0.30.1/24

##  Management Zone (10.0.10.0/24)
- **Ansible-Engine:** 10.0.10.10 (Ubuntu Server)
- **Purpose:** Centralized administration and automation via Ansible.

##  Production Zone (10.0.20.0/24)
- **Docker-Host-01:** (Pending Setup)
- **Purpose:** Hosting corporate web services and applications.

##  Cyber-Ops Zone (10.0.30.0/24)
- **Security-Tools:** (Pending Setup)
- **Purpose:** Network monitoring and security analysis.

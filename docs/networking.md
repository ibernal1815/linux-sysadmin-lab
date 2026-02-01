graph TD
    subgraph WAN
        Internet((Internet))
    end

    subgraph PF_Firewall [Virtual Firewall / Gateway]
        direction TB
        FW[pfSense/OPNsense]
    end

    Internet <--> FW

    subgraph VLAN_10_MGMT
        Host[Proxmox Host]
        AP[Admin PC]
    end

    subgraph VLAN_30_PROD
        K3s[K3s Cluster]
        DB[PostgreSQL]
    end

    subgraph VLAN_40_CYBER
        Target[Vulnerable VM]
        SOC[Wazuh/ELK]
    end

    FW --- VLAN_10_MGMT
    FW --- VLAN_30_PROD
    FW --- VLAN_40_CYBER

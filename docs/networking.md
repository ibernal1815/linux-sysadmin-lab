graph TD
    %% Global Nodes
    Internet((Internet))
    FW[pfSense / OPNsense Gateway]

    subgraph MGMT_VLAN_10 [VLAN 10: Management]
        Proxmox[Proxmox Host]
        Ansible[Ansible Control Node]
    end

    subgraph PROD_VLAN_30 [VLAN 30: Linux Services]
        Docker[Docker Host]
        K3s[K3s Cluster]
    end

    subgraph CYBER_VLAN_40 [VLAN 40: Red/Blue Sandbox]
        Wazuh[Wazuh SIEM]
        Kali[Kali Linux]
        Target[Vuln Target]
    end

    %% Define Connections
    Internet <--> FW
    FW --- MGMT_VLAN_10
    FW --- PROD_VLAN_30
    FW --- CYBER_VLAN_40

    %% Styling for that Pro look
    style FW fill:#f96,stroke:#333,stroke-width:2px
    style Internet fill:#fff,stroke:#333
    style MGMT_VLAN_10 fill:#e1f5fe,stroke:#01579b
    style PROD_VLAN_30 fill:#e8f5e9,stroke:#1b5e20
    style CYBER_VLAN_40 fill:#ffebee,stroke:#b71c1c

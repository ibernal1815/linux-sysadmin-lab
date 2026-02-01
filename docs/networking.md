graph TD
    %% Define Nodes
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

    %% Styling
    style FW fill:#f96,stroke:#333,stroke-width:2px
    style Internet fill:#fff,stroke:#333

# 🛠️ Andro-Lab | Homelab Infrastructure

Willkommen in meinem persönlichen Homelab! Diese Umgebung dient als mein primäres Testfeld für Netzwerksicherheit, Virtualisierung und Systemintegration. Hier lerne und analysiere ich reale Security-Szenarien unter praxisnahen Bedingungen.

---

## 🗺️ Netzwerktopologie & Infrastruktur

```mermaid
graph TD
    %% Styling
    classDef internet fill:#eceff1,stroke:#37474f,stroke-width:2px,stroke-dasharray: 5 5;
    classDef security fill:#ffc107,stroke:#ff9800,stroke-width:2px,color:#000;
    classDef hypervisor fill:#00bcd4,stroke:#0097a7,stroke-width:2px,color:#fff;
    classDef node fill:#4caf50,stroke:#388e3c,stroke-width:2px,color:#fff;

    %% Nodes
    WAN[🌐 INTERNET] :::internet
    FW[🔒 OPNsense Firewall / Security Gateway] :::security
    
    subgraph PVE [💻 Proxmox VE Hypervisor]
        VM1[🐧 Debian VM]
        VM2[🐉 Kali Linux]
    end
    class PVE hypervisor;

    subgraph HW [🍓 Bare-Metal / Peripherie]
        Pi1[🛑 Raspberry Pi 1: Pi-hole DNS]
        Pi2[📂 Raspberry Pi 2: Samba NAS]
        CF[☁️ Cloudflare Tunnel Relay]
    end
    class HW node;

    %% Connections
    WAN --> FW
    FW --> PVE
    FW --> HW
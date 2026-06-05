# ⚡ THE SUDOANDRO SECURITY LAB

> "20 Jahre absolute Präzision an schweren CNC-Maschinen. Jetzt übersetze ich diese Verantwortung, Problemlösungskompetenz unter Druck und das Streben nach Perfektion in die Cybersicherheit. Ich lerne nicht für ein Stück Papier. Ich lerne, um Menschen und Systeme real zu schützen."

Ich bin ein ICT-Informatiker (Quereinsteiger 40+), der den Mut hatte, das Feld komplett neu aufzurollen. In meinem Lab wird nicht kopiert – hier wird verstanden, zerlegt und gehärtet. Wenn ein System brennt, bleibe ich am Ball, bis der Fehler eliminiert ist.

---

## 💻 Tech-Stack & Arsenal

### 🛠️ Programmiersprachen & Scripting
* **Python:** Automatisierung und Entwicklung (inkl. GUI-Programmierung)
* **PowerShell 7 & Bash:** Maßgeschneiderte CLI-Tools, System-Tuning und Skripting
* **HTML/CSS:** Basis-Webentwicklung (z.B. für eigene Dashboards)

### 🛡️ Cybersecurity & Networking
* **Firewall & Routing:** OPNsense, VLAN-Isolation, DNS-Sinkholing (Pi-hole)
* **VPN & Remote Access:** Tailscale Mesh, NetBird, NordVPN, Cloudflare Tunnels
* **Identity & Access:** Vaultwarden (Self-Hosted Password Management), SSH-Key Auth

### 🧮 Infrastruktur & Virtualisierung
* **Hypervisor:** Proxmox VE
* **Betriebssysteme:** Debian Linux (Core/Server), Kali Linux (Offensive Security), Windows
* **Container & Services:** Docker, Samba (NAS), Paperless-ngx (Dokumenten-Digitalisierung)
* **Entwicklungsumgebung:** VS Code, XPipe, Git

---

## 🗺️ Die Nervenzentralen meines Homelabs

```mermaid
graph TD
    %% Styling
    classDef wan fill:#1f1f1f,stroke:#d32f2f,stroke-width:2px,color:#fff;
    classDef vpn fill:#3949ab,stroke:#5c6bc0,stroke-width:2px,color:#fff;
    classDef core fill:#ff9800,stroke:#e65100,stroke-width:3px,color:#000,font-weight:bold;
    classDef hyper fill:#00e5ff,stroke:#00b0ff,stroke-width:2px,color:#000;
    classDef peripheral fill:#00e676,stroke:#00c853,stroke-width:2px,color:#000;
    classDef client fill:#8e24aa,stroke:#ab47bc,stroke-width:2px,color:#fff;

    %% External & Clients
    WAN["DAS INTERNET - Die ungesicherte Zone"]:::wan
    
    subgraph Remote ["📱 Endgeräte & Remote Access"]
        PC["Admin PC (VS Code / XPipe)"]
        Mobile["Smartphone"]
    end
    class Remote client;

    VPN["Tailscale Mesh / NordVPN"]:::vpn

    %% Core Networking
    FW["OPNsense Security Gateway"]:::core
    
    %% Proxmox Environment
    subgraph PVE ["PROXMOX VE - Virtualisierungs-Kern"]
        VM1["Debian VM (Docker, Vaultwarden, Paperless-ngx)"]
        VM2["Kali Linux (Recon & Penetration Testing)"]
    end
    class PVE hyper;

    %% Bare Metal & Storage
    subgraph HW ["BARE-METAL & SERVICES"]
        Pi1["Pi-hole (DNS Sinkhole / Ad-Block)"]
        Pi2["Samba NAS (Lokaler Speicher & Backups)"]
        CF["Cloudflare Tunnel Relay"]
    end
    class HW peripheral;

    %% Connections
    WAN --> FW
    PC --> VPN
    Mobile --> VPN
    VPN -->|Verschlüsselter Tunnel| FW
    FW --> PVE
    FW --> HW
    ```
    
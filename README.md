# ⚡ THE SUDOANDRO SECURITY LAB

> "20 Jahre absolute Präzision an schweren CNC-Maschinen. Jetzt übersetze ich diese Verantwortung, Problemlösungskompetenz unter Druck und das Streben nach Perfektion in die Cybersicherheit. Ich lerne nicht für ein Stück Papier. Ich lerne, um Menschen und Systeme real zu schützen."

---

## 🪓 Meine Philosophie: Keine Theorie. Reine Praxis.
Ich bin kein typischer IT-Einsteiger. Ich bin ein Quereinsteiger mit 40+, der den Mut hatte, das Feld komplett neu aufzurollen. In meinem Lab wird nicht kopiert – hier wird verstanden, zerlegt und gehärtet.

* **Mentalität:** 100% lösungsorientiert. Wenn ein System brennt oder eine Schleife blockiert, bleibe ich am Ball, bis der Fehler eliminiert ist.
* **Fokus:** Hardening von Systemen, Netzwerktrennung, Pentesting und Infrastructure-Monitoring.

---

## 🗺️ Die Nervenzentralen meines Homelabs

```mermaid
graph TD
    %% Styling fuer brutale Uebersicht
    classDef wan fill:#1f1f1f,stroke:#d32f2f,stroke-width:2px,color:#fff;
    classDef core fill:#ff9800,stroke:#e65100,stroke-width:3px,color:#000,font-weight:bold;
    classDef hyper fill:#00e5ff,stroke:#00b0ff,stroke-width:2px,color:#000;
    classDef peripheral fill:#00e676,stroke:#00c853,stroke-width:2px,color:#000;

    %% Nodes
    WAN["DAS INTERNET - Die ungesicherte Zone"]:::wan
    FW["OPNsense Security Gateway - Der eiserne Tuersteher"]:::core
    
    subgraph PVE ["PROXMOX VE HYPERVISOR - Virtualisierungs-Kern"]
        VM1["Debian VM - Docker und Core Services"]
        VM2["Kali Linux - Die Angriffs und Analyseplattform"]
    end
    class PVE hyper;

    subgraph HW ["BARE-METAL und COMPLIANCE"]
        Pi1["Pi-hole - DNS Sinkhole und Telemetrie-Filter"]
        Pi2["Raspberry Pi - Lokales Samba NAS fuer Backups"]
        CF["Cloudflare Tunnel - Sicherer WAN-Relay ohne offene Ports"]
    end
    class HW peripheral;

    %% Routing Paths
    WAN --> FW
    FW --> PVE
    FW --> HW
    ```

    
## 🛠️ Mein Arsenal & Praktische Skills

| Bereich | Technologie / Werkzeuge | Einsatzzweck im Lab |
| :--- | :--- | :--- |
| **Firewall & Netzwerksicherheit** | OPNsense, VLAN-Trennung, NAT | Komplette Abschottung von unsicheren IoT-Geräten (z.B. IP-Kameras) vom internen Netz. |
| **Sicherer Fernzugriff** | Tailscale (Subnet Routing), NetBird | Verschlüsseltes Mesh-Netzwerk für standortunabhängigen Zugriff direkt auf Host-Ebenen. |
| **Virtualisierung** | Proxmox VE, Debian Linux | Aufbau isolierter Testumgebungen zur Analyse von Angriffsvektoren. |
| **Offensive Security** | Kali Linux, Nmap, Hydra, Wireshark | Durchführung kontrollierter Reconnaissance-Scans und Brute-Force-Stresstests gegen eigene Infrastruktur. |
| **Automatisierung & Monitoring** | Monit, Python, Bash, Brevo SMTP | Proaktive Systemüberwachung mit automatisierten Alarm-Schleifen bei Host-Ausfällen. |

---

## 🚀 Aktuelle Hardening-Projekte
1. **IoT Isolation:** Komplette Einkapselung von Consumer-Webcams in separaten Netzwerksegmenten, validiert durch automatisierte Penetration-Scans.
2. **Alerting System:** Behebung kritischer Monitoring-Deadlocks im Monit-Unterbau der OPNsense, gekoppelt an einen verifizierten Cloudflare/Brevo-Relay.
3. **Workspace Customization:** Aufbau einer extrem schnellen CLI-Schaltzentrale mittels PowerShell 7, XPipe und maßgeschneiderten SSH-Key-Authentifizierungen.

---
**"Ich habe langsam gestartet – aber ich höre nicht auf."**
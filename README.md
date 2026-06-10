<p align="center">
  <img src="images/logo.png" alt="Logo" width="750" />
</p>

### `whoami`

</div>

```bash
$ cat /etc/profile.d/andro.sh

NAME="Andrijan Tadic"
ALIAS="sudoAndro"
LOCATION="Solothurn, Switzerland 🇨🇭"
BACKGROUND="20 years CNC Machinist → IT & Cybersecurity"
TRAINING="ICT-Power-User SIZ & Professional SIZ (System & Network) – in progress"
GOAL="Protect people through cybersecurity"
STATUS="Learning every day | Breaking things | Fixing them better"
```

---

## Focus Areas

```
[■■■■■■■■■░]  Windows Administration
[■■■■■■■■░░]  Linux Administration
[■■■■■■░░░░]  Network Security
[■■■■■░░░░░]  Homelab & Virtualization
[■■■░░░░░░░]  Active Directory (in training)
[■■■░░░░░░░]  Secure Application Development (Android)
[■■■░░░░░░░]  Cybersecurity (in progress)
```

---

## Tech Stack

**Operating Systems**

![Windows 11](https://img.shields.io/badge/Windows_11-0078D4?style=flat-square&logo=windows11&logoColor=white)
![Windows 10](https://img.shields.io/badge/Windows_10-0078D4?style=flat-square&logo=windows&logoColor=white)
![Debian](https://img.shields.io/badge/Debian-A81D33?style=flat-square&logo=debian&logoColor=white)
![Kali Linux](https://img.shields.io/badge/Kali_Linux-557C94?style=flat-square&logo=kalilinux&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=flat-square&logo=ubuntu&logoColor=white)

**Windows & Active Directory**

![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white)
![Active Directory](https://img.shields.io/badge/Active_Directory-0078D4?style=flat-square&logo=microsoft&logoColor=white)
![Windows Server](https://img.shields.io/badge/Windows_Server-0078D4?style=flat-square&logo=windows&logoColor=white)

**Virtualization & Infrastructure**

![Proxmox](https://img.shields.io/badge/Proxmox-E57000?style=flat-square&logo=proxmox&logoColor=white)
![OPNsense](https://img.shields.io/badge/OPNsense-D94F00?style=flat-square&logo=opnsense&logoColor=white)
![Raspberry Pi](https://img.shields.io/badge/Raspberry_Pi-A22846?style=flat-square&logo=raspberrypi&logoColor=white)

**Networking & Security**

![Pi-hole](https://img.shields.io/badge/Pi--hole-96060C?style=flat-square&logo=pihole&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![NordVPN](https://img.shields.io/badge/NordVPN-4687FF?style=flat-square&logo=nordvpn&logoColor=white)
![Tailscale](https://img.shields.io/badge/Tailscale-242424?style=flat-square&logo=tailscale&logoColor=white)
![SSH](https://img.shields.io/badge/SSH-4D4D4D?style=flat-square&logo=gnubash&logoColor=white)

**Services & Tools**

![Samba](https://img.shields.io/badge/Samba_NAS-1C1C1C?style=flat-square&logo=linux&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)
![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white)

**Mobile Development**

![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white)
![Android Studio](https://img.shields.io/badge/Android_Studio-3DDC84?style=flat-square&logo=androidstudio&logoColor=white)
![Jetpack Compose](https://img.shields.io/badge/Jetpack_Compose-4285F4?style=flat-square&logo=jetpackcompose&logoColor=white)

---

## Homelab

A secure homelab architecture centered on OPNsense, with NordVPN/WireGuard, Tailscale mesh connectivity, Pi-hole DNS filtering, and Vaultwarden service hosting.

<img src="assets/homelab.svg" alt="Homelab architecture" width="100%" />

*This diagram shows the planned secure homelab topology with OPNsense, VPN, DNS filtering, and Tailscale mesh.*

**Key points:**
- OPNsense functions as the WAN gateway, VPN killswitch, firewall, DHCP controller, and Tailscale subnet router.
- Pi-hole handles DNS filtering with Cloudflare/Quad9 upstream resolution.
- Vaultwarden runs in Docker with Caddy TLS and Crowdsec protection.
- Tailscale provides secure overlay access for mobile clients, laptops, and remote management.

*Diagram source: `assets/homelab.mmd`.*

```bash
npm install -g @mermaid-js/mermaid-cli
mmdc -i assets/homelab.mmd -o assets/homelab.svg
```

---

## Featured Projects

| Repository | Description | Status |
|---|---|---|
| [linux-secure-setup](https://github.com/sudoAndro/linux-secure-setup) | Hardening scripts for Debian/Ubuntu | 🟢 Active |
| [samba-nas-setup](https://github.com/sudoAndro/samba-nas-setup) | Samba NAS with Cloudflare Tunnel | 🟢 Active |
| [andro-lab](https://github.com/sudoAndro/andro-lab) | Multi-Layer Cybersecurity Homelab | 🟡 In Progress |
| [proxmox-scripts](https://github.com/sudoAndro/proxmox-scripts) | Automation & setup scripts for Proxmox | 🟢 Active |
| [linux-starter-kit](https://github.com/sudoAndro/linux-starter-kit) | Aliases, tuning & tips for beginners | 🟢 Active |
| [windows-starter-kit](https://github.com/sudoAndro/windows-starter-kit) | Automated PowerShell 7 + Terminal setup | 🟢 Active |
| [active-directory-lab](https://github.com/sudoAndro/active-directory-lab) | Active Directory Lab – Domain Controller, GPOs, DNS Filtering & Logging | 🟢 Active |
| [VaultCalculator](https://github.com/sudoAndro/VaultCalculator) | A fully functional calculator for Android with a private file vault | 🟢 Active |
---

## Roadmap 2025–2026

- [x] Proxmox Homelab aufgebaut
- [x] OPNsense Firewall konfiguriert
- [x] Raspberry Pi – Pi-hole & Samba NAS
- [x] Cloudflare Tunnel eingerichtet
- [x] Active Directory – Windows Server (in Ausbildung)
- [ ] ICT Supporter SIZ abschliessen
- [ ] ICT Professional SIZ abschliessen
- [ ] CompTIA Security+ vorbereiten
- [ ] Erstes CTF (Capture The Flag) abschliessen
- [ ] Cybersecurity Einstiegsposition finden

---

## GitHub Stats

<div align="center">

![sudoAndro's GitHub Stats](https://github-readme-stats.vercel.app/api?username=sudoAndro&show_icons=true&theme=dark&hide_border=true&bg_color=0d1117&title_color=58a6ff&icon_color=58a6ff)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=sudoAndro&layout=compact&theme=dark&hide_border=true&bg_color=0d1117&title_color=58a6ff)

</div>

---

## Connect

[![Website](https://img.shields.io/badge/Website-andrijantadic.ch-0d1117?style=flat-square&logo=firefox&logoColor=58a6ff)](https://www.andrijantadic.ch)
[![GitHub](https://img.shields.io/badge/GitHub-sudoAndro-0d1117?style=flat-square&logo=github&logoColor=white)](https://github.com/sudoAndro)

---

<div align="center">

*"The quieter you become, the more you are able to hear."* — Kali Linux

![Visitor Count](https://komarev.com/ghpvc/?username=sudoAndro&color=58a6ff&style=flat-square&label=Profile+Views)

</div>

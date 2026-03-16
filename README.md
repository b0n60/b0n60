<!-- b0n60 · SOC Analyst · Full Stack Dev · Jolinkomo Tech Solutions · ZA -->

<div align="center">

```
██████╗  ██████╗ ███╗   ██╗ ██████╗  ██████╗
██╔══██╗██╔═══██╗████╗  ██║██╔════╝ ██╔═══██╗
██████╔╝██║   ██║██╔██╗ ██║███████╗ ██║   ██║
██╔══██╗██║   ██║██║╚██╗██║██╔══██╗ ██║   ██║
██████╔╝╚██████╔╝██║ ╚████║╚██████╔╝╚██████╔╝
╚═════╝  ╚═════╝ ╚═╝  ╚═══╝ ╚═════╝  ╚═════╝
        b0n60 · Johannesburg, ZA
```

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/bongo-sijora/)
[![GitHub](https://img.shields.io/badge/GitHub-b0n60-181717?style=for-the-badge&logo=github)](https://github.com/b0n60)
[![SOC Analyst](https://img.shields.io/badge/SOC_Analyst-Senior-39ff14?style=for-the-badge&logoColor=black)](/)
[![Full Stack](https://img.shields.io/badge/Full_Stack-Developer-00e5ff?style=for-the-badge&logoColor=black)](/)
[![Wazuh](https://img.shields.io/badge/Wazuh-Certified_Engineer-005571?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0xMiAyTDIgN2w0IDE1aDEybDQtMTV6Ii8+PC9zdmc+&logoColor=white)](/)
[![ZA](https://img.shields.io/badge/🇿🇦_Based_In-South_Africa-007A4D?style=for-the-badge)](/)
[![Press](https://img.shields.io/badge/📰_Cited_In-Sunday_Times_·_MyBroadband-FF6B35?style=for-the-badge)](/)

</div>

---

## `> whoami --verbose`

```python
profile = {
    "handle"      : "b0n60",
    "roles"       : ["SOC Analyst", "Full Stack Developer"],
    "company"     : "Jolinkomo Tech Solutions",
    "location"    : "Johannesburg, Gauteng, South Africa 🇿🇦",
    "focus"       : [
                      "Blue Team Operations",
                      "Detection Engineering",
                      "Custom SIEM / XDR",
                      "Threat Hunting",
                      "Full Stack Secure Application Development"
                    ],
    "cert"        : "Wazuh Certified Engineer (Official)",
    "press"       : ["Sunday Times / TimesLive", "MyBroadband — 2022"],
    "research"    : "R18bn ZA government cybersecurity spending gap — documented & verified",
    "languages"   : ["Python", "JavaScript", "HTML/CSS", "Rust", "C"],
    "tools"       : ["Wazuh", "Graylog", "LibreNMS", "Suricata", "Zeek", "MISP"],
    "ethos"       : "Build it. Open it. Move forward."
}
```

---

## `> cat mission.txt`

South Africa is not a peripheral target. **It is a primary one.**

Ranked among the most attacked nations on the African continent — government portals, financial institutions, healthcare systems, and state security infrastructure face daily, relentless intrusion attempts. In 2022, research conducted under **Umboko Sec** and independently verified by *Sunday Times* and *MyBroadband* established a documented shortfall of at least **R18 billion** in government cybersecurity spending. A gap that compounds every year accountability remains absent.

The 2025 Gauteng Provincial Government breach — 3.67 million files, 3.8TB of citizen data, healthcare records, housing applications, and economic development information listed at $25,000 on dark web markets — is not an isolated failure. It is the predictable outcome of structural underinvestment.

My work is about closing that gap. Building detection tooling. Hardening networks. Delivering full-stack applications that are secure by design, not by afterthought. **Five years in the trenches. Still going.**

---

## `> neofetch`

```
         #####          OS: Ubuntu 25.04 x86_64
        #######         Theme: Juno-ocean-v40 [GTK2/3]
        ##O#O##         Icons: Papirus-Dark [GTK2/3]
        #######         Terminal: gnome-terminal
      ###########       CPU Usage: 462%
     #############      Disk (/): 126G / 234G (57%)
    ###############
   #################
  ###################
```

---

## `> ./coverage-report --framework mitre --env za-gov`

```
[LOADED] wazuh-rules-za.xml          →  847 custom rules
[LOADED] graylog-pipelines.json      →  124 processing pipelines
[LOADED] librenms-alerts.conf        →  63  alert thresholds

Tactic                    Coverage    Notes
────────────────────────────────────────────────────────────────────
Reconnaissance            ████████████  94%   Passive + active scan detection
Initial Access            ████████████  94%   Web exploit, phishing, cred stuffing
Execution                 ███████████░  88%   Script-based + LOLBin detection
Persistence               ███████████░  88%   Scheduled tasks, registry, services
Privilege Escalation      ██████████░░  82%   Local + domain escalation paths
Defence Evasion           ██████████░░  79%   ← Active development
Credential Access         ████████████  91%   Mimikatz, LSASS, hash harvesting
Discovery                 ████████████  90%   Internal recon detection
Lateral Movement          ██████████░░  83%   SMB, RDP, WMI monitoring
Collection                ████████████  90%   Data staging detection
Exfiltration              ████████████  91%   DNS tunnelling, HTTPS exfil, cloud sync
Command & Control         ██████████░░  84%   Beacon detection, C2 patterns
Impact                    ████████████  92%   Ransomware, wiper, destruction
────────────────────────────────────────────────────────────────────
```

---

## `> cat skills.json`

### 🛡️ Blue Team & Detection

![Wazuh](https://img.shields.io/badge/Wazuh_XDR-Certified-39ff14?style=flat-square&logoColor=black)
![Graylog](https://img.shields.io/badge/Graylog-Log_Management-FF3700?style=flat-square&logoColor=white)
![LibreNMS](https://img.shields.io/badge/LibreNMS-Network_Monitor-0077CC?style=flat-square&logoColor=white)
![MITRE](https://img.shields.io/badge/MITRE_ATT%26CK-Detection_Eng-E22B2B?style=flat-square&logoColor=white)
![Suricata](https://img.shields.io/badge/Suricata-IDS%2FIPS-EF8C00?style=flat-square&logoColor=white)
![Zeek](https://img.shields.io/badge/Zeek-Network_Analysis-2980B9?style=flat-square&logoColor=white)
![Threat Hunting](https://img.shields.io/badge/Threat_Hunting-Active-39ff14?style=flat-square&logoColor=black)
![Incident Response](https://img.shields.io/badge/Incident_Response-Practiced-bf5fff?style=flat-square&logoColor=white)

### 💻 Full Stack Development

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)

### 🏗️ Infrastructure & Tooling

![Linux](https://img.shields.io/badge/Ubuntu_Linux-E95420?style=flat-square&logo=ubuntu&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=flat-square&logo=postgresql&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-269539?style=flat-square&logo=nginx&logoColor=white)
![Wireshark](https://img.shields.io/badge/Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![MISP](https://img.shields.io/badge/MISP-Threat_Intel-1F4E79?style=flat-square&logoColor=white)

---

## `> ls ./custom-tools/`

> Built for environments where commercial and open-source platforms don't fit.
> South African infrastructure has unique constraints — load-shedding, bandwidth limits, legacy systems — that generic tooling misses.

| Tool | Replaces | Description | Stack |
|------|----------|-------------|-------|
| **🛡️ SentinelCore** | Wazuh (low-resource) | Lightweight SIEM engine with ZA-specific threat intel feeds. Runs on machines Wazuh would bring to their knees. | Python · Rust · SQLite |
| **📋 LogHound** | Graylog | High-noise, low-bandwidth log aggregator. Built-in parsers for South African ISP log formats that Graylog doesn't ship with. | Python · Redis · FastAPI |
| **📡 NetPulse** | LibreNMS | Modular NMS with non-standard topology support. WhatsApp + SMS alerting for teams without 24/7 NOC coverage. | Python · C · SNMP |
| **🗺️ ThreatMapper ZA** | Manual IOC triage | MISP + OTX + curated local feeds. Enriches Wazuh alerts with SA-specific IOC context that global feeds miss entirely. | Python · MISP · OTX |

> Most repositories on this profile are intentional open builds — prototypes and proof-of-concepts left accessible for others to continue. Knowledge transfer matters more than attribution. **Take what is useful.**

---

## `> cat press-citations.txt`

In May 2022, research conducted under **Umboko Sec** was independently verified by *Sunday Times* and *MyBroadband* during national coverage of the SpiderLog$ disclosure — a coordinated exposure of vulnerabilities in South African defence, state security, and government digital infrastructure.

> *"Umboko Sec director Bongo Sijora told Sunday Times their research showed a shortfall of at least R18 billion in government spending on securing national key points and departments from cyber threats."*
>
> — **Sunday Times / TimesLive**, 29 May 2022 · [Lax Cybersecurity Leaves SA a Playground for Hackers](https://www.sundaytimes.timeslive.co.za/sunday-times/news/2022-05-29-lax-cybersecurity-leaves-sa-a-playground-for-hackers/)

> *"The paper verified the group's claims with cybersecurity firms WolfPack Information Risk and Umboko Sec."*
>
> — **MyBroadband**, May 2022 · [Cyril Ramaphosa's Private Data Hacked](https://mybroadband.co.za/news/security/446282-cyril-ramaphosas-private-data-hacked.html)

**Context:** SpiderLog$ used President Ramaphosa's personal data to expose how South Africa's government digital infrastructure could be mapped and accessed with minimal effort. The Sunday Times called SA *"a playground for hackers"*. The research Umboko Sec contributed demonstrated this was not rhetorical — it was a documented, costed reality.

---

## `> cat za-incidents.log`

```
Date        Target                  Incident
──────────────────────────────────────────────────────────────────────────
2021-07     Transnet                Ransomware — port systems offline, shipping paralysed
2021-09     Dept of Justice         Ransomware — all systems locked, courts and prosecution halted
2022-03     TransUnion              Breach cascaded to President Ramaphosa personal data exposure
2022-05     Dept of Defence / SSA   SpiderLog$ accessed military and state security webmail — verified Umboko Sec
2024        CIPC                    Full DB access since 2021 — plain text passwords, director manipulation possible
2025-03     SA Parliament           Social media hijacked for $Ramaphosa crypto token fraud
2025        Gauteng Gov             3.67M files, 3.8TB citizen data — healthcare, housing on dark web @ $25,000
```

---

## `> ./github-stats.sh`

<div align="center">

![](https://raw.githubusercontent.com/b0n60/b0n60/master/profile-summary-card-output/gruvbox/3-stats.svg)
![](https://raw.githubusercontent.com/b0n60/b0n60/master/profile-summary-card-output/gruvbox/2-most-commit-language.svg)

</div>

---

## `> cat character.md`

**🧠 Intellectual Range** — Draws connections between cybersecurity, genetics, philosophy, and political systems. Approaches security not as a technical exercise but as a discipline with human, societal, and structural dimensions.

**🎯 Precise Under Pressure** — Cited by national media during a live government breach crisis. Delivers structured, evidence-based analysis when others speculate. Calm is the strategy.

**🔨 Builder Mentality** — Most repositories are intentional open builds left accessible for the community to extend. Knowledge transfer matters more than attribution.

**🌍 Mission-Driven** — The infrastructure that ordinary South Africans depend on — healthcare portals, housing systems, government services — deserves to be genuinely secure against real, present threats. That is the work.

---

## `> cat connect.yml`

```yaml
contact:
  linkedin   : https://www.linkedin.com/in/bongo-sijora/
  github     : https://github.com/b0n60

open_to:
  - blue team tooling collaboration
  - detection engineering projects
  - south african threat intelligence sharing
  - full-stack secure application development
  - cybersecurity research and press engagement
  - speaking on the ZA threat landscape
```

---

<div align="center">

```
// b0n60
// SOC Analyst · Full Stack Developer
// Jolinkomo Tech Solutions · Johannesburg, South Africa 🇿🇦
// Securing the infrastructure that millions depend on
// Built with precision. Hardened by experience. Open by principle.
```

![Profile views](https://komarev.com/ghpvc/?username=b0n60&color=39ff14&style=flat-square&label=Profile+Views)

</div>

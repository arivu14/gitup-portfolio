# 🛡️ Arivazhagan — SOC Analyst Portfolio

> SOC Analyst L1 · Threat Detection · Incident Response · AI-Powered Security Automation

[![LinkedIn](https://img.shields.io/badge/LinkedIn-arivazhagan11-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/arivazhagan11/)
[![GitHub](https://img.shields.io/badge/GitHub-arivu14-black?style=flat&logo=github)](https://github.com/arivu14)
[![Portfolio](https://img.shields.io/badge/Portfolio-Live-green?style=flat&logo=firefox)](https://arivu14.github.io/gitup-portfolio/)
[![Location](https://img.shields.io/badge/Location-Tamil%20Nadu%2C%20India-orange?style=flat)](https://maps.google.com/?q=Tamil+Nadu,India)

---

## 👨‍💻 About Me

I'm a SOC Analyst L1 building real-world cybersecurity skills through a hands-on home lab. I run **Wazuh SIEM** on Ubuntu Server, investigate live attacks, and write custom detection rules — turning every incident into a documented case study.

I work on **AI-powered security automation** using LangGraph and Google Gemini 2.0 Flash — building agents that automate Tier-1 triage, reduce MTTR, and make SOC teams faster and more efficient.

- 🔍 Investigate live threats in a real SOC home lab with Wazuh SIEM
- 🤖 Build AI triage agents using LangGraph + Google Gemini 2.0 Flash
- 🦠 Malware static analysis with Shannon Entropy, YARA rules, and bash forensics

---

## 🚀 Projects

---

### CASE-001 · 🔐 SSH Brute Force Detection & Response
> **Tools:** Wazuh SIEM · IPTables · Fail2Ban · AbuseIPDB · OSINT

**Overview:**
A full L1 incident investigation of a live SSH brute force attack detected in my home lab. The attacker IP `141.98.81.37` triggered 145+ failed login attempts within 5 minutes, flagged by Wazuh SIEM with a 100% abuse confidence score on OSINT enrichment.

**Key Actions Taken:**

| Step | Action |
|------|--------|
| Detection | Wazuh SIEM alert triggered on repeated failed SSH logins |
| OSINT Enrichment | AbuseIPDB returned 100% abuse confidence score |
| Immediate Mitigation | IPTables DROP rule applied to source IP |
| Hardening | SSH Key-based auth enabled, password login disabled in `sshd_config` |
| Automation | Fail2Ban configured for automated temporary null-routing |

**MITRE ATT&CK Mapping:**
- `T1110` — Brute Force
- `T1078` — Valid Accounts (attempted)
- `T1562` — Impair Defenses (attacker evasion attempt)

---

### CASE-002 · 🤖 Cypher-Sentinel — Automating Tier-1 Triage With LLM Reasoning
> **Tools:** LangGraph · Google Gemini 2.0 Flash · Google Colab · Wazuh JSON

**Overview:**
Built a 4-node LangGraph AI agent that automates the "Pivot" phase of SOC investigation. The agent takes raw Wazuh SIEM JSON as input and outputs a structured human-readable verdict — reducing MTTR significantly for Tier-1 analysts.

**Agent Architecture:**

```
Raw Wazuh JSON Input
        ↓
  [Node 1] Log Parser
        ↓
  [Node 2] IP Enrichment (AbuseIPDB / VirusTotal)
        ↓
  [Node 3] Gemini 2.0 Flash Reasoning Engine
        ↓
  [Node 4] Verdict Generator
        ↓
Human-Readable Investigation Report
```

**Sample Input → Output:**

```json
// Input
{
  "target_ip": "172.16.17.207",
  "log_source": "Wazuh_Manager",
  "event_type": "Internal_Audit"
}
```

```
// AI Analyst Verdict
🕵️ INVESTIGATION REPORT
IP: 172.16.17.207 (Private)
VERDICT: BENIGN
Asset identified as internal management server.
```

---

### CASE-003 · 🦠 Automated Malware Triage & AI Forensics
> **Tools:** Bash · Shannon Entropy · YARA Rules · Gemini AI · Python

[![GitHub Repo](https://img.shields.io/badge/GitHub-soc--malware--triage-black?style=flat&logo=github)](https://github.com/arivu14/Soc-Malware-Triage)

**Overview:**
Automates analysis of suspicious scripts by calculating **Shannon Entropy** (detecting hidden/encrypted code) and **Shell Funnel Execution** logic. An AI agent interprets raw forensic math to provide instant SOC Tier-2 insights.

**How It Works:**

```bash
$ ./triage.sh elite_malware.sh

[!] ALERT: High Entropy (7.84)
[!] ALERT: Execution Funnel (| sh)
[+] Result: Potential Obfuscated Shellcode Detected
```

**AI Senior Analyst Verdict:**
```
🕵️ VERDICT: MALICIOUS
TYPE: Encrypted Reverse Shell
RISK: CRITICAL
Reason: Bypassing file-based detection via hex-encoding + direct piping.
```

**Detection Techniques Used:**
- Shannon Entropy scoring (threshold: > 7.0 = suspicious)
- Shell funnel pattern detection (`| sh`, `| bash`, `| exec`)
- YARA rule matching against known malware signatures
- AI-powered forensic verdict via Gemini 2.0 Flash

---

## 🛠️ Skills & Tools

| Category | Tools |
|---|---|
| **SIEM** | Wazuh, Splunk |
| **AI / Automation** | LangGraph, Google Gemini 2.0 Flash, Python |
| **Threat Intel** | AbuseIPDB, VirusTotal, OSINT |
| **Malware Analysis** | Shannon Entropy, YARA Rules, Bash Forensics |
| **Network Security** | IPTables, Fail2Ban, SSH Hardening |
| **Frameworks** | MITRE ATT&CK |
| **OS** | Ubuntu Server, Linux CLI |

---

## 📊 SOC Services

| Service | Description |
|---|---|
| 🔍 Threat Detection | Real-time monitoring with Wazuh SIEM, custom detection rules, FIM alerts |
| 🚨 Incident Response | L1 triage, investigation, containment, MITRE ATT&CK mapping |
| 🤖 AI Automation | LangGraph agents that automate Tier-1 SOC triage |
| 🦠 Malware Analysis | Static analysis via entropy, YARA, shell funnel detection |
| 🌐 Threat Intelligence | OSINT enrichment via AbuseIPDB and VirusTotal API |
| 🔒 Security Hardening | SSH key auth, Fail2Ban, IPTables, sshd_config hardening |

---

## 📬 Contact

| Platform | Link |
|---|---|
| 📧 Email | arivazhagans1411@gmail.com |
| 💼 LinkedIn | [linkedin.com/in/arivazhagan11](https://www.linkedin.com/in/arivazhagan11/) |
| 🌐 Portfolio | [arivu14.github.io/gitup-portfolio](https://arivu14.github.io/gitup-portfolio/) |
| 📍 Location | Tamil Nadu, India |

---

> *"Security is a Human Right — It Belongs to You"* 🔐

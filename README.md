# Mudasir Zia — Cybersecurity & SOC Analyst Portfolio

**Target role:** Entry-level SOC Analyst (Tier 1 / L1) · **Location:** Mansehra, Pakistan · **Open to:** remote and international roles

[GitHub](https://github.com/CyberBros435) · [LinkedIn](https://www.linkedin.com/in/mudasir-zia-a535243b5/) · [Portfolio site](https://mudasir-zia-oct-2026-portfolio.vercel.app) · ziamudasir744@gmail.com

> [!IMPORTANT]
> **Transparency note.** Every project below is a home-lab, training or internship exercise. None is enterprise SOC employment or a real production incident. Where an attack is "real", it was run by me against my own local lab systems. Where data is generated, it is labeled as simulated. Figures quoted are as stated in each project's own README/report.

---

## About

Cybersecurity student focused on **SOC monitoring, SIEM detection and incident investigation**. My work centers on **Splunk (SPL, alerts, dashboards, correlation)**, **Windows Event Logs and Sysmon**, **network traffic analysis (Wireshark)**, and **Python automation**, with supporting web-security and tooling projects.

## Skills demonstrated

| Area | Tools / concepts |
|---|---|
| SIEM | Splunk, SPL, alerts, dashboards, lookups, `transaction`, correlation searches |
| Endpoint & logs | Windows Security Events (4625, 4688, 4946), Sysmon (Event ID 1, 3), PowerShell/CMD monitoring |
| Network | Wireshark, TCP handshake analysis, port scanning, firewall/SSH/HTTP log analysis |
| Detection topics | Brute force, password spraying, SQL injection, port scans, data exfiltration, firewall tampering (T1562.004), ransomware behavior (T1486) |
| Threat intel | VirusTotal, Cisco Talos, Shodan, AbuseIPDB, IOC extraction |
| Automation | Python, n8n |
| Frameworks | MITRE ATT&CK mapping, cyber kill chain, incident response process |

## Contents

1. [Featured SOC projects](#featured-soc-projects)
2. [Complete SOC project collection](#complete-soc-project-collection)
3. [Other cybersecurity projects](#other-cybersecurity-projects)
4. [Internship and training collections](#internship-and-training-collections)
5. [Non-security software projects](#non-security-software-projects)
6. [Scope and verification](#scope-and-verification)

---

## Featured SOC projects

Start here — strongest end-to-end detection work.

| Project | What it shows |
|---|---|
| [Bruteforce-Detection-Splunk](https://github.com/CyberBros435/Bruteforce-Detection-Splunk) | Local Flask login attack, Splunk detection, threshold alert and dashboard (80 attempts, 77 failures, 1 success per README) |
| [soc-password-spray-detection-splunk](https://github.com/CyberBros435/soc-password-spray-detection-splunk) | Distributed password spray (10 users, 1 password, 15 simulated IPs); campaign-level detection and formal incident report |
| [soc-sqli-detection-splunk](https://github.com/CyberBros435/soc-sqli-detection-splunk) | SQL injection against a local Flask/SQLite target; auth-bypass, error-based and UNION patterns with MITRE mapping |
| [Sysmon_Splunk_Visibility_Comparison](https://github.com/CyberBros435/Sysmon_Splunk_Visibility_Comparison) | Detection gap: default Security log (4688) vs Sysmon Event ID 1 for the same activity |
| [Windows_Firewall_Rule_Tampering_Detection](https://github.com/CyberBros435/Windows_Firewall_Rule_Tampering_Detection) | Firewall rule change auditing (Event 4946), alert and dashboard, T1562.004 |
| [ransomware-siem-analysis](https://github.com/CyberBros435/ransomware-siem-analysis) | Ransomware simulation on a limited lab scope, log analysis in Splunk, T1486 mapping |
| [fiverr-social-engineering_SOC_investigation](https://github.com/CyberBros435/fiverr-social-engineering_SOC_investigation) | Investigation of a fake order / card-harvesting page: IOCs, evidence and defensive recommendations |
| [3_Way_handshake_network_analysis](https://github.com/CyberBros435/3_Way_handshake_network_analysis) | Wireshark TCP handshake capture plus OSINT/threat-intel validation of IPs |

---

## Complete SOC project collection

### 1. SIEM and SPL fundamentals

| Project | Description |
|---|---|
| [mini-project-1-failed-logon-freq](https://github.com/CyberBros435/mini-project-1-failed-logon-freq) | Event ID 4625 frequency analysis; separates system SIDs from user activity |
| [spl-stats-sort-fundamentals](https://github.com/CyberBros435/spl-stats-sort-fundamentals) | `stats` and `sort` practice on failed-logon sources |
| [soc-correlation-search-splunk](https://github.com/CyberBros435/soc-correlation-search-splunk) | Cross-source correlation (failed logons vs ransomware activity); negative-case result |
| [soc-correlation-validation-positive-case](https://github.com/CyberBros435/soc-correlation-validation-positive-case) | Positive-case validation of the correlation logic (~58 s event gap per README) |
| [soc-transaction-incident-grouping](https://github.com/CyberBros435/soc-transaction-incident-grouping) | `transaction` command to group related events into incidents (4 events over 362 s per README) |
| [soc-lookup-enrichment-splunk](https://github.com/CyberBros435/soc-lookup-enrichment-splunk) | Lookup table mapping ports to risk labels, including troubleshooting notes |

### 2. Detection engineering (attack simulation + detection)

| Project | Description |
|---|---|
| [Bruteforce-Detection-Splunk](https://github.com/CyberBros435/Bruteforce-Detection-Splunk) | HTTP brute force against local Flask target |
| [soc-password-spray-detection-splunk](https://github.com/CyberBros435/soc-password-spray-detection-splunk) | Distributed low-and-slow spray detection |
| [soc-sqli-detection-splunk](https://github.com/CyberBros435/soc-sqli-detection-splunk) | SQLi detection (10 payloads, 6 bypasses per README) |
| [soc-data-exfiltration-detection-splunk](https://github.com/CyberBros435/soc-data-exfiltration-detection-splunk) | Volume- and rate-based exfiltration detection (~100 MB in ~1 s per README) |
| [soc-port-scan-detection-splunk](https://github.com/CyberBros435/soc-port-scan-detection-splunk) | Python-generated (simulated) scan logs; port-count/time-window threshold |
| [soc-real-portscan-analysis](https://github.com/CyberBros435/soc-real-portscan-analysis) | Real localhost TCP scan analyzed in Splunk (2 of 20 ports open per README) |
| [Windows_Firewall_Rule_Tampering_Detection](https://github.com/CyberBros435/Windows_Firewall_Rule_Tampering_Detection) | Defense-tampering detection |

### 3. Log analysis, alerting and monitoring

| Project | Description |
|---|---|
| [SSH_Log_Analysis_Splunk](https://github.com/CyberBros435/SSH_Log_Analysis_Splunk) | Windows OpenSSH success/failure logs, alert and dashboard |
| [HTTP_Log_Analysis_Splunk](https://github.com/CyberBros435/HTTP_Log_Analysis_Splunk) | Normal vs scanning-style HTTP traffic, alert and dashboard |
| [Firewall_Log_Analysis_Splunk](https://github.com/CyberBros435/Firewall_Log_Analysis_Splunk) | Windows Firewall ALLOW/DROP analysis, alert and dashboard |
| [soc-cmd-powershell-activity-monitoring-splunk](https://github.com/CyberBros435/soc-cmd-powershell-activity-monitoring-splunk) | Monitoring administrative/suspicious CMD and PowerShell activity |

### 4. SOC dashboards

| Project | Description |
|---|---|
| [soc-dashboard-splunk-visualization](https://github.com/CyberBros435/soc-dashboard-splunk-visualization) | Splunk dashboard for ransomware event data |
| [soc-unified-monitoring-dashboard](https://github.com/CyberBros435/soc-unified-monitoring-dashboard) | Unified view of Windows Security and ransomware data |
| [soc-alerting-dashboard-port-scan](https://github.com/CyberBros435/soc-alerting-dashboard-port-scan) | Scheduled alert and dashboard panel for high-risk port exposure |

### 5. Sysmon and endpoint telemetry

| Project | Description |
|---|---|
| [Sysmon_Splunk_Visibility_Comparison](https://github.com/CyberBros435/Sysmon_Splunk_Visibility_Comparison) | 4688 vs Sysmon Event ID 1 (1,178 Sysmon events vs zero 4688 per README) |
| [Sysmon_Network_Connection_Analysis](https://github.com/CyberBros435/Sysmon_Network_Connection_Analysis) | Event ID 3 process-to-destination analysis; triage of one anomalous LOLBin connection |
| [Sysmon_Ransomware_Simulation_Analysis](https://github.com/CyberBros435/Sysmon_Ransomware_Simulation_Analysis) | Ransomware-like behavior investigated with Sysmon. *Currently README only; evidence to be added.* |

### 6. Incident response and investigation

| Project | Description |
|---|---|
| [ransomware-siem-analysis](https://github.com/CyberBros435/ransomware-siem-analysis) | Lab ransomware simulation and Splunk analysis (14 files encrypted/recovered per README) |
| [fiverr-social-engineering_SOC_investigation](https://github.com/CyberBros435/fiverr-social-engineering_SOC_investigation) | Phishing/card-harvesting investigation with IOCs |
| [3_Way_handshake_network_analysis](https://github.com/CyberBros435/3_Way_handshake_network_analysis) | Packet analysis with VirusTotal, Cisco Talos and Shodan lookups |

### 7. Security automation

| Project | Description |
|---|---|
| [n8n-soc-automations](https://github.com/CyberBros435/n8n-soc-automations) | Importable n8n IP-reputation workflow using AbuseIPDB |

---

## Other cybersecurity projects

<details>
<summary><b>Python security tools and cryptography</b></summary>

| Project | Description |
|---|---|
| [Hash_Generator](https://github.com/CyberBros435/Hash_Generator) | CLI generating 12 hash types (MD5, SHA-1/2/3, BLAKE2) |
| [Hash_Identifier](https://github.com/CyberBros435/Hash_Identifier) | Identifies likely hash type from format rules |
| [Hash_Cracker](https://github.com/CyberBros435/Hash_Cracker) | Dictionary-based hash testing; authorized lab use only |
| [Pass_Gen_And_Security_Analyser](https://github.com/CyberBros435/Pass_Gen_And_Security_Analyser) | Password generator and strength analyzer |
| [Check_Security_Of_Password_by_Attack_on_it](https://github.com/CyberBros435/Check_Security_Of_Password_by_Attack_on_it) | Brute-force demonstration of password strength; local use only |
| [NextGen-CyberSecurity-Internship](https://github.com/CyberBros435/NextGen-CyberSecurity-Internship) | SecureTransfer CLI: AES-256-GCM, scrypt, SHA-256 integrity (18 tests per README) |
| [efs-folder-encryption-verifier](https://github.com/CyberBros435/efs-folder-encryption-verifier) | Checks Windows EFS status via `cipher.exe` |

</details>

<details>
<summary><b>Web application security labs</b></summary>

| Project | Description |
|---|---|
| [XSS_Injection_Lab](https://github.com/CyberBros435/XSS_Injection_Lab) | Intentionally vulnerable local XSS lab with safe-mode remediation |
| [XSS_complete_Vulnerable_lab](https://github.com/CyberBros435/XSS_complete_Vulnerable_lab) | Reflected, stored and DOM XSS practice lab |
| [IDOR_vuln_LAB](https://github.com/CyberBros435/IDOR_vuln_LAB) | Flask/SQLite lab documenting 10 IDOR weaknesses |
| [cyber-security-attack-simulations](https://github.com/CyberBros435/cyber-security-attack-simulations) | Interactive HTML learning modules on common attack vectors |

</details>

<details>
<summary><b>Network tools</b></summary>

| Project | Description |
|---|---|
| [IP_Scanner_CMD_Toolkit](https://github.com/CyberBros435/IP_Scanner_CMD_Toolkit) | Diagnostic CLI: IP info, ping, traceroute, DNS lookup |
| [DNS_Server](https://github.com/CyberBros435/DNS_Server) | Hostname-to-IPv4 lookup script (a lookup tool, not a DNS server implementation) |

</details>

---

## Internship and training collections

Multi-project repositories. Each contains several independent tasks.

| Repository | Highlights |
|---|---|
| [TechBiz-Security_Projects](https://github.com/CyberBros435/TechBiz-Security_Projects) | SOC-focused weekly tasks: [Windows Event IDs](https://github.com/CyberBros435/TechBiz-Security_Projects/tree/main/Week-2-Task-5-Windows-Event-IDs), [Wireshark](https://github.com/CyberBros435/TechBiz-Security_Projects/tree/main/Week-3-Task-9-Network-Traffic-Analysis-Wireshark-Basics), [Splunk/SIEM](https://github.com/CyberBros435/TechBiz-Security_Projects/tree/main/Week-4-Task-10-What-is-SIEM-Install-Splunk-FIXED), [incident detection](https://github.com/CyberBros435/TechBiz-Security_Projects/tree/main/Week-5-Task-15-Incident-Detection-Investigate-Attack-in-Logs), [hands-on investigation](https://github.com/CyberBros435/TechBiz-Security_Projects/tree/main/Task-17-Hands-on-Investigation), [capstone](https://github.com/CyberBros435/TechBiz-Security_Projects/tree/main/Week-6-Task-18-Capstone) |
| [SQROCK_Projects](https://github.com/CyberBros435/SQROCK_Projects) | 15 modules incl. [SIEM log analysis for SE detection](https://github.com/CyberBros435/SQROCK_Projects/tree/main/SIEM_Log_Analysis_SE_Detection), [incident response automation](https://github.com/CyberBros435/SQROCK_Projects/tree/main/SE_Incident_Response_Automation), [phishing URL detector](https://github.com/CyberBros435/SQROCK_Projects/tree/main/Phishing_URL_Detector), [phishing email ML detection](https://github.com/CyberBros435/SQROCK_Projects/tree/main/Phishing_Email_Detection_ML), [impersonation detection](https://github.com/CyberBros435/SQROCK_Projects/tree/main/Social_Media_Impersonation_Detection) |
| [SQROCK_Phase2_Projects](https://github.com/CyberBros435/SQROCK_Phase2_Projects) | HTTP security-header audit; local port/service scanning |
| [CodeAlpha_Projects](https://github.com/CyberBros435/CodeAlpha_Projects) | Packet sniffer; phishing-awareness training; secure code review |
| [Decode-Lab-Projects](https://github.com/CyberBros435/Decode-Lab-Projects) | Substitution cipher; password checker; phishing-awareness analysis |
| [Redynox_Internship_Projects](https://github.com/CyberBros435/Redynox_Internship_Projects) | Network security basics; web app security (SQLi, XSS, CSRF) |
| [OASIS-INFOBYTE_Internship](https://github.com/CyberBros435/OASIS-INFOBYTE_Internship) | Nmap scan; network threats; social engineering; patch management reports |
| [The-Sky-Gen-Cyber-Security-Projects](https://github.com/CyberBros435/The-Sky-Gen-Cyber-Security-Projects) | Personal security audit and password tool |
| [SafeSkills_Projects](https://github.com/CyberBros435/SafeSkills_Projects) | AI-in-cybersecurity lab (Lakera) |
| [ICP-896E95A4-2026-REPO](https://github.com/CyberBros435/ICP-896E95A4-2026-REPO) | Network port scanner (Week 2) |
| [labmentix-soc-internship-project](https://github.com/CyberBros435/labmentix-soc-internship-project) | SOC internship record (in progress; introduction document only so far) |
| [SOC_Project_revision_Summery](https://github.com/CyberBros435/SOC_Project_revision_Summery) | Revision index of earlier SOC work (not a separate implementation) |
| [ransomware](https://github.com/CyberBros435/ransomware) | Lab research code; not featured and no run instructions provided |

---

## Non-security software projects

Listed for completeness; not part of the SOC portfolio.

| Project | Description |
|---|---|
| [DOCX_to_PDF_converter](https://github.com/CyberBros435/DOCX_to_PDF_converter) · [PDF_compressor](https://github.com/CyberBros435/PDF_compressor) · [PDF_Murger](https://github.com/CyberBros435/PDF_Murger) · [PDF_splitter](https://github.com/CyberBros435/PDF_splitter) · [PPT_Murger](https://github.com/CyberBros435/PPT_Murger) | Document-processing web utilities |
| [CMD_In_terminal](https://github.com/CyberBros435/CMD_In_terminal) | Python terminal controller |
| [single_page_ecommerce_website](https://github.com/CyberBros435/single_page_ecommerce_website) · [single_page_ecommerce_website2](https://github.com/CyberBros435/single_page_ecommerce_website2) | Front-end e-commerce pages |
| [birthday-website](https://github.com/CyberBros435/birthday-website) · [birthday-magic-experience](https://github.com/CyberBros435/birthday-magic-experience) | Interactive static websites |
| [mudasir-zia-oct-2026-portfolio](https://github.com/CyberBros435/mudasir-zia-oct-2026-portfolio) · [My-Introduction](https://github.com/CyberBros435/My-Introduction) | Personal portfolio site and profile |

---

## Scope and verification

- Source: all 68 public repositories on this account, reviewed against GitHub.
- Repository-level links are verified against the live account listing. Folder-level links for `TechBiz-Security_Projects` and `SQROCK_Projects` are verified against their root directories.
- Metrics marked "per README" are taken from each project's own documentation and have not been independently re-run.
- Repositories with little or no content (`Progree_Internship_Projects`, `bulk_email_sender`, `Instagram_Anonymous_Viewer`) are intentionally not featured.

## Contact

Mudasir Zia · [LinkedIn](https://www.linkedin.com/in/mudasir-zia-a535243b5/) · [GitHub](https://github.com/CyberBros435) · ziamudasir744@gmail.com

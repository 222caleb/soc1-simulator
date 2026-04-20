# SOC 1 Simulation Lab

A home-lab SIEM deployment simulating a real SOC environment. Detects, analyzes, and documents SSH brute force attacks using Splunk, Kali Linux, and Ubuntu. All running on Apple Silicon via UTM virtualization.

**[View the live site →](https://222caleb.github.io/soc1-simulator/)**

---

## What it does

- Simulates coordinated SSH brute force attacks from multiple source IPs using Hydra and Metasploit
- Ships auth logs from an Ubuntu target VM to Splunk Enterprise via Universal Forwarder
- Detects attack patterns using custom SPL queries with threshold-based alerting
- Scores threats using a composite risk model (volume + username diversity)
- Maps attacks to MITRE ATT&CK techniques (T1110.001, T1110.004)
- Documents findings in two formal incident reports with full forensic evidence

## Results

- **4,329** total events analyzed
- **8** unique attacker IPs across 7 countries detected
- **15** service accounts targeted
- **100%** detection rate - zero successful external compromises
- **2** incident reports authored (1 coordinated campaign, 1 false positive investigation)

## Stack

| Layer | Tool |
|---|---|
| SIEM | Splunk Enterprise 10.2 |
| Log shipper | Splunk Universal Forwarder 10.2.2 |
| Target host | Ubuntu 24.04 LTS (ARM64) |
| Attacker | Kali Linux 2026.1 (ARM64) |
| Attack tools | Hydra, Metasploit, Nmap |
| Virtualization | UTM on Apple Silicon (M1) |
| Log source | OpenSSH with LogLevel VERBOSE |

## Portfolio site

The deployed site covers the full project in detail. From architecture, attack simulation, SPL detection queries, incident reports with investigation evidence, and MITRE ATT&CK mapping.

Built with HTML, CSS, and JavaScript. Deployed via GitHub Pages.

---

**Caleb Damron** · [LinkedIn](https://www.linkedin.com/in/caleb-222-damron/)

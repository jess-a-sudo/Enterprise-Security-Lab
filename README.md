# 🛡️ Enterprise Security Lab  

**Simulating Enterprise Network Security: Reconnaissance, Vulnerability Assessment, and Intrusion Detection**  

---

## Project Overview  

This lab simulates a real-world enterprise network environment, reflecting the operations of a hypothetical company, **DelTech Services**. It demonstrates **applied cybersecurity skills** in threat detection, vulnerability assessment, and security controls implementation, with an emphasis on practical outcomes and risk prioritization.

**Key Skills Demonstrated:**  
- Network reconnaissance and traffic analysis  
- Password-based attack testing (SSH)  
- Vulnerability scanning and remediation  
- Intrusion detection using Snort  
- Professional documentation of findings  

---

## Scenario / Problem  

As an **IT Security Analyst**, the goal was to identify and evaluate **security threats** in a controlled enterprise environment, including:  

- Active reconnaissance by potential attackers  
- SSH brute-force attack simulations  
- Vulnerability detection on critical servers  
- Demonstrating mitigation strategies and security monitoring  

The challenge was to **detect and assess risks**, prioritizing those that could compromise enterprise systems.  

---

## Tools & Technologies Used  

| Category | Tools / Software |
|----------|-----------------|
| Virtualization | VMware Workstation, GNS3 |
| Operating Systems | Windows Server 2016, Kali Linux 2019.3 |
| Network Devices | Cisco 3745 IOS Router, Ethernet switch |
| Security Testing | Nmap, ncrack, Hydra, Nessus 8.8.0, OpenSSH |
| Intrusion Detection | Snort 2.9.15 |
| Analysis & Scripting | Wireshark 3.0.6, Bash, Windows CLI |

---

## Workflow / Key Steps  

### 1. Virtual Environment Setup
- Imported Windows Server, Kali Linux, and GNS3 VMware images  
- Configured Windows Server as a **Domain Controller** with TCP/IP and firewall rules  

### 2. GNS3 Lab Configuration
- Created project workspace with all appliances  
- Configured Cisco 3745 router interfaces and DHCP for Kali Linux  

### 3. Network Reconnaissance
- Used **Nmap** for ping sweeps, OS discovery, and service enumeration  
- Captured network traffic with **Wireshark**  
- Analyzed TCP flags (SYN, ACK, RST) to identify attack patterns  

### 4. SSH Brute Force Attack
- Installed **OpenSSH** on Windows Server  
- Configured inbound firewall rules for TCP port 22  
- Used **ncrack** with a password dictionary to test brute-force access  
- Documented proof-of-access using a controlled test file (`Gotin.txt`)  

### 5. Vulnerability Scanning
- Ran **Nessus** scans to identify vulnerabilities  
- Prioritized findings based on risk severity  
- Documented remediation steps for each issue  

### 6. Intrusion Detection with Snort
- Installed **Snort IDS** and configured rules for SSH and SYN scan detection  
- Monitored alerts during reconnaissance and brute-force tests  

---

## Key Findings & Risk Prioritization  

- **High Risk:** SSH password authentication could allow an attacker to gain server access. Mitigation: enforce key-based authentication, account lockouts, and IP restrictions.  
- **Medium Risk:** Open network services detected on Windows Server and Cisco Router. Mitigation: disable unnecessary services and enforce firewall policies.  
- **Low Risk:** Nessus-reported minor vulnerabilities. Mitigation: apply patches and security updates.  

> These priorities simulate real-world escalation procedures for an enterprise SOC environment.  

---

## Results / Outcomes  

- Simulated **enterprise-level network attacks** in a controlled environment  
- Successfully demonstrated SSH brute-force exploitation and mitigation  
- Captured and analyzed network traffic with Wireshark for insight into attacker behavior  
- Configured Snort to **detect reconnaissance and SSH attacks in real time**  
- Produced structured documentation of all findings and remediation strategies  

---

## Tool Competency  

| Tool | Proficiency | Notes |
|------|-------------|-------|
| Wireshark | High | Captured and filtered traffic, analyzed TCP flags, correlated with Nmap scans |
| Nessus | High | Ran scans, interpreted vulnerabilities, prioritized remediation |
| GNS3 | High | Built virtual network topologies and tested real-world configurations |
| VMware Workstation | High | Managed VM setup, network interfaces, and system resources |
| Snort | Working Knowledge | Installed and configured IDS rules for SSH and SYN scans, monitored alerts, and understand the end-to-end workflow; refining advanced rule creation |

---

## Folder Contents  

- `docs/` — Detailed project documentation and lab report  
- `lab-setup/` — VM and network configuration files  
- `network-analysis/` — Nmap scans, Wireshark captures  
- `security-testing/` — SSH, vulnerability, and IDS tests  
- `screenshots/` — Visual evidence of key steps and results  
- `resources/` — Password dictionaries, Snort rules, references  

> Screenshots in the `screenshots/` folder with the filenames referenced in the README (e.g., `nmap_scan.png`, `wireshark_capture.png`).  

---

## Challenges & Learnings  

- Balancing multiple VMs and network configurations simultaneously  
- Interpreting complex packet captures and attack behavior  
- Writing and testing IDS rules in Snort  
- Understanding the importance of structured documentation and reproducible evidence  

---

## Next Steps / Improvements  

- Introduce **SIEM tools** (e.g., Wazuh) to centralize alerts and logs  
- Automate vulnerability scanning and alerting for continuous monitoring  
- Expand lab to include **web application vulnerabilities** and phishing scenarios  

---

## Contact  

- LinkedIn: [Jessica Hlubi](https://linkedin.com/in/jessica-hlubi-80a915361)  
- Email: jessicahlubi@gmail.com

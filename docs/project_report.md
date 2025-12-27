# Enterprise Security Lab – Project Report

## Author
**Jessica Hlubi**  
Network & Security Engineering Graduate  
LinkedIn: [https://linkedin.com/in/jessica-hlubi-80a915361](https://linkedin.com/in/jessica-hlubi-80a915361)  
Email: jessicahlubi@gmail.com  

---

## 1. Project Overview
This lab simulates a real-world enterprise network environment, reflecting the operations of a hypothetical company, **DelTech Services**. The objective was to develop applied cybersecurity skills, including:

- Network reconnaissance and traffic analysis
- Password-based attack testing (SSH)
- Vulnerability scanning and remediation
- Intrusion detection using Snort
- Professional documentation of findings and risk prioritization

---

## 2. Scenario / Problem
As an IT Security Analyst, the tasks were to:

- Detect active reconnaissance attempts
- Test SSH brute-force attacks
- Identify vulnerabilities in critical servers
- Implement mitigation strategies and demonstrate security monitoring

The challenge was to **simulate enterprise-level security operations** in a safe, controlled virtual environment using VMware and GNS3.

---

## 3. Tools & Technologies Used
| Category                | Tools / Software                                      |
|-------------------------|------------------------------------------------------|
| Virtualization          | VMware Workstation, GNS3                             |
| Operating Systems       | Windows Server 2016, Kali Linux 2019.3              |
| Network Devices         | Cisco 3745 IOS Router, Ethernet switch             |
| Security Testing        | Nmap, ncrack, Hydra, Nessus 8.8.0, OpenSSH         |
| Intrusion Detection     | Snort 2.9.15                                        |
| Analysis & Scripting    | Wireshark 3.0.6, Bash, Windows CLI                 |

---

## 4. Workflow / Key Steps

### 4.1 Virtual Environment Setup
- Imported Windows Server, Kali Linux, and GNS3 VMware images
- Configured Windows Server as a Domain Controller with TCP/IP and firewall rules

### 4.2 GNS3 Lab Configuration
- Created project workspace with all appliances
- Configured Cisco 3745 router interfaces and DHCP for Kali Linux

### 4.3 Network Reconnaissance
- Used Nmap for ping sweeps, OS discovery, and service enumeration
- Captured network traffic with Wireshark
- Analyzed TCP flags (SYN, ACK, RST) to identify potential attack patterns

### 4.4 SSH Brute Force Attack
- Installed OpenSSH on Windows Server
- Configured inbound firewall rules for TCP port 22
- Used ncrack with a password dictionary (`top50000.pwd`) to test brute-force access
- Created proof-of-access file `Gotin.txt` to demonstrate successful authentication

### 4.5 Vulnerability Scanning
- Ran Nessus scans on Windows Server
- Prioritized vulnerabilities by risk level (High, Medium, Low)
- Documented remediation steps for each issue

### 4.6 Intrusion Detection with Snort
- Installed Snort IDS on Windows Server
- Configured rules to detect SSH and SYN scan activity
- Monitored alerts during reconnaissance and brute-force testing

---

## 5. Key Findings & Risk Prioritization
| Risk Level | Observation | Mitigation Strategy |
|-----------|-------------|-------------------|
| High | SSH password authentication could allow unauthorized access | Enforce key-based authentication, account lockouts, IP restrictions |
| Medium | Open network services detected on Windows Server and Cisco Router | Disable unnecessary services, enforce firewall policies |
| Low | Minor vulnerabilities reported by Nessus | Apply security patches and updates |

---

## 6. Results / Outcomes
- Simulated enterprise-level network attacks in a controlled environment
- Demonstrated SSH brute-force exploitation and mitigation
- Captured and analyzed network traffic with Wireshark
- Configured Snort to detect reconnaissance and SSH attacks in real time
- Produced structured documentation of all findings and remediation strategies

---

## 7. Tool Competency
| Tool                   | Proficiency | Notes |
|------------------------|------------|-------|
| Wireshark              | High       | Captured and filtered traffic, analyzed TCP flags, correlated with Nmap scans |
| Nessus                 | High       | Ran scans, interpreted vulnerabilities, prioritized remediation |
| GNS3                   | High       | Built virtual network topologies and tested configurations |
| VMware Workstation      | High       | Managed VM setup, network interfaces, and system resources |
| Snort                  | Working Knowledge | Installed and configured IDS rules, monitored alerts, refining advanced rule creation |

---

## 8. Challenges & Learnings
- Balancing multiple VMs and network configurations simultaneously
- Interpreting complex packet captures and attack behaviors
- Writing and testing IDS rules in Snort
- Importance of structured documentation and reproducible evidence

---

## 9. Next Steps / Improvements
- Introduce **SIEM tools** (e.g., Wazuh) to centralize alerts and logs
- Automate vulnerability scanning and alerting for continuous monitoring
- Expand lab to include web application vulnerabilities and phishing scenarios

---

## 10. Folder & File Structure

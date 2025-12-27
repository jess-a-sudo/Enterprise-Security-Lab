# 🛡️ Enterprise Security Lab

**Simulating Enterprise Network Security: Reconnaissance, Vulnerability Assessment, and Intrusion Detection**

---

## Project Overview

This project simulates a real-world enterprise network environment and demonstrates applied cybersecurity skills, including:

- Network reconnaissance and traffic analysis  
- Password-based attacks on SSH services  
- Vulnerability scanning and remediation  
- Intrusion detection using Snort  

The lab environment reflects **DelTech Services**, a hypothetical company, where tasks were performed in a **safe virtual environment** to prevent downtime on live systems.

---

## Scenario / Problem

As an IT Security Analyst at DelTech Services, the task was to assess the company’s network for potential security threats, including:

- Active reconnaissance by potential attackers  
- SSH brute-force attempts  
- Identifying vulnerabilities in critical systems  
- Demonstrating mitigation and defense strategies  

The challenge was to **identify and analyze threats while simulating enterprise-level security monitoring**, using virtualized systems.

---

## Tools & Technologies Used

| Category           | Tools / Software |
|-------------------|----------------|
| Virtualization     | VMware Workstation, GNS3 |
| Operating Systems  | Windows Server 2016, Kali Linux 2019.3 |
| Network Devices    | Cisco 3745 IOS Router, Ethernet switch |
| Security Testing   | Nmap, ncrack, Hydra, Nessus 8.8.0, OpenSSH |
| Intrusion Detection| Snort 2.9.15 |
| Analysis & Scripting| Wireshark 3.0.6, Bash, Windows CLI |

---

## Workflow / Key Steps

1. **Virtual Environment Setup**  
   - Imported Windows Server, Kali Linux, and GNS3 VMware images  
   - Configured Windows Server as a Domain Controller with TCP/IP and firewall rules  

2. **GNS3 Lab Configuration**  
   - Created project workspace with all appliances (Windows Server, Kali Linux, Cisco router, Ethernet switch)  
   - Configured Cisco 3745 router interfaces and DHCP for Kali Linux  

3. **Network Reconnaissance**  
   - Used Nmap for ping sweeps, OS discovery, and service enumeration  
   - Captured traffic with Wireshark  

   ![Nmap Scan](screenshots/nmap_scan.png)
   ![Wireshark Capture](screenshots/wireshark_capture.png)

4. **Traffic Analysis**  
   - Analyzed captured packets in Wireshark  
   - Created filters for Kali Linux IP and ports 53 & 445  
   - Examined TCP flags (SYN, ACK, RST) to interpret network behavior  

5. **SSH Brute Force Attack**  
   - Installed OpenSSH on Windows Server  
   - Configured inbound firewall rules for TCP port 22  
   - Used ncrack with password dictionary (`top50000.pwd`) to gain SSH access  
   - Executed network commands and created proof-of-access file (`Gotin.txt`)  

   ![SSH Attack](screenshots/ssh_attack.png)

6. **Vulnerability Scanning**  
   - Ran Nessus scan on Windows Server to identify vulnerabilities  
   - Documented findings and remediation steps  

   ![Nessus Scan](screenshots/nessus_scan.png)

7. **Intrusion Detection with Snort**  
   - Installed Snort and configured rules for SSH and SYN scan detection  
   - Monitored alerts during Nmap scans and SSH attacks  

   ![Snort Alert](screenshots/snort_alert.png)

---

## Results / Outcomes

- Successfully simulated an enterprise-level network for security testing  
- Identified vulnerabilities and demonstrated mitigation strategies  
- Captured and analyzed network traffic using Wireshark  
- Gained SSH access in a controlled environment to demonstrate potential attack vectors  
- Configured Snort IDS to detect reconnaissance and SSH brute-force attacks  
- Documented all findings in a structured report  

---

## Folder Contents

- [docs/](docs/) — Detailed project documentation and lab report  
- [lab-setup/](lab-setup/) — VM and network configuration files  
- [network-analysis/](network-analysis/) — Scans and packet captures  
- [security-testing/](security-testing/) — SSH, vulnerability, and IDS test files  
- [screenshots/](screenshots/) — Visual evidence of key steps and results  
- [resources/](resources/) — Password dictionaries, Snort rules, reference materials  

---

## Professional Skills Demonstrated

- Network and security configuration and troubleshooting  
- Applied penetration testing methodology  
- Traffic analysis and incident response understanding  
- Professional documentation and reporting  
- Problem-solving and critical thinking in simulated enterprise environments  

---

## Challenges & Learnings

- Managing multiple virtual machines and network configurations simultaneously  
- Interpreting complex packet captures in Wireshark  
- Learning Snort IDS rule creation and validation  
- Recognizing the importance of systematic documentation and screenshots for reproducibility  

---

## Next Steps / Improvements

- Expand lab to simulate web application vulnerabilities and phishing scenarios  
- Automate scans and alerts for more realistic threat simulation  
- Integrate SIEM tools for enterprise-level monitoring  

---

## Contact & References

LinkedIn: [https://linkedin.com/in/jessica-hlubi-80a915361](https://linkedin.com/in/jessica-hlubi-80a915361)  
Email: jessicahlubi@gmail.com  

---

✅ **Instructions:**  
1. Place your screenshots in the `screenshots/` folder with the same filenames used in this README (`nmap_scan.png`, `wireshark_capture.png`, `ssh_attack.png`, `nessus_scan.png`, `snort_alert.png`).  
2. Make sure your detailed lab report is in `docs/`.  
3. Keep your configuration and test scripts in their respective folders (`lab-setup/` and `security-testing/`).  


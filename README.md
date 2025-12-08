# 🔒 CySA Security Operations Lab

## 📋 Project Overview
A comprehensive hands-on cybersecurity lab completed as part of CySA+ preparation, simulating real-world security operations in an enterprise network environment. This project demonstrates practical skills in network security, threat detection, and vulnerability management using industry-standard tools.

## 🎯 Lab Objectives
- Set up a complete virtualized network environment using VMware and GNS3
- Perform network reconnaissance and service enumeration
- Analyze network traffic for security insights
- Conduct vulnerability assessments
- Test security controls and implement mitigations
- Document findings and security recommendations

## 🛠️ Tools & Technologies Used
| Category | Tools |
|----------|-------|
| Virtualization | VMware Workstation, GNS3 |
| Operating Systems | Windows Server 2016, Kali Linux |
| Network Devices | Cisco IOS Router |
| Security Tools | Nmap, Wireshark, Nessus, Hydra |
| Analysis | Packet analysis, Log review, Vulnerability assessment |

## 📁 Project Structure
Security-Operations-Lab/
├── documentation/ # Project documentation and objectives
├── lab-setup/ # VM and network configuration
├── network-analysis/ # Scanning and traffic analysis
├── security-testing/ # Vulnerability and security testing
├── screenshots/ # Visual evidence and results
└── resources/ # Reference materials and links


## 🚀 Getting Started
### Prerequisites
- VMware Workstation or VirtualBox
- GNS3 network emulator
- Windows Server 2016 ISO
- Kali Linux ISO
- Basic understanding of networking concepts

### Quick Start
1. Review the `lab-setup/` documentation for environment configuration
2. Follow the network analysis procedures in `network-analysis/`
3. Implement security tests as outlined in `security-testing/`
4. Refer to screenshots for expected results

## 🔍 Key Activities Demonstrated
1. **Network Infrastructure Setup**: Configured virtual machines and network topology
2. **Network Reconnaissance**: Used Nmap for host discovery and service enumeration
3. **Traffic Analysis**: Captured and analyzed network packets with Wireshark
4. **Vulnerability Assessment**: Set up and ran Nessus vulnerability scans
5. **Security Testing**: Conducted SSH security testing with Hydra
6. **Security Controls**: Documented mitigation strategies for identified risks

## 💡 Skills Developed
- **Technical Skills**: Network configuration, security tool usage, traffic analysis
- **Analytical Skills**: Threat identification, vulnerability assessment, risk analysis
- **Documentation**: Professional reporting, evidence collection, procedure documentation
- **Problem-Solving**: Troubleshooting network issues, implementing security controls

## 📈 Learning Outcomes
This project provided hands-on experience with:
- Enterprise network architecture and segmentation
- Security monitoring and threat detection principles
- Vulnerability management lifecycle
- Security tool deployment and configuration
- Professional security documentation practices

## 👤 Author
**Phindile Hlubi**  
Network & Security Engineering Graduate  
*This project was completed as practical preparation for cybersecurity operations roles.*

## 📄 License
This project is for educational purposes. All tools and software used are property of their respective owners.

---
*Note: This lab was conducted in a controlled environment for learning purposes only.*

1. documentation/project_overview.md:

# Project Overview

## Purpose
This lab simulates security operations in a corporate network environment, providing hands-on experience with security tools and techniques used by cybersecurity professionals.

## Scope
- Virtual environment setup with multiple operating systems
- Network configuration and segmentation
- Security assessment and testing
- Documentation and reporting

## Methodology
The project follows a structured approach:
1. Environment setup and configuration
2. Network discovery and analysis
3. Security testing and assessment
4. Findings documentation
5. Mitigation recommendations

2. lab-setup/vmware_configuration.md:

# VMware Virtual Machine Configuration

## Windows Server 2016 Setup
- **VMware Workstation 17.5.x**
- **Configuration Type**: Custom (advanced)
- **Memory**: 2 GB RAM
- **Processors**: 2 CPU cores
- **Hard Disk**: 300 GB (split into multiple files)
- **Network Adapter**: NAT
- **Operating System**: Windows Server 2016 Standard Evaluation

## Kali Linux 2019 Setup
- **Installer**: ISO image file
- **Installation Type**: Graphical install
- **Network Configuration**: DHCP via router
- **Tools Pre-installed**: Nmap, Wireshark, Hydra

## Network Configuration
- Router: Cisco 3745 (IOS version 124-25d)
- Interface Configuration:
  - FastEthernet0/0: 10.10.10.10/24 (connected to Kali)
  - FastEthernet0/1: 192.168.10.200/24 (connected to Windows Server)
- DHCP pool configured for 10.10.10.0/24 network

  3. network-analysis/nmap_scan_results.md:

# Nmap Scanning Results

## Ping Sweep
root@kali:~# nmap -sn 192.168.10.0/24

Findings: Identified 1 active host (192.168.10.200)

Operating system detection
root@kali:~# nmap -O -Pn 192.168.10.200

Findings:

Device type: Cisco router

Running: Cisco IOS 12.X|15.X

Open port: 23/tcp (telnet)

Service Enumeration
root@kali:~# nmap -sS 192.168.10.1

Findings: Multiple services identified including SSH (22/tcp), DNS (53/tcp), LDAP (389/tcp)


**4. security-testing/ssh_brute_force_test.md:**
```markdown
# SSH Security Testing

## Objective
Test SSH service vulnerability to brute-force attacks and document mitigation strategies.

## Tools Used
- Hydra (for brute-force testing)
- Ncrack (password cracking tool)
- Common password lists (top50000.pwd, common.usr)

## Test Procedure
1. Identified SSH service on target
2. Attempted brute-force using common credentials
3. Documented results and failure rates
4. Analyzed security implications

## Key Finding
- SSH service was resistant to automated attacks with default settings
- Multiple failed attempts triggered security mechanisms
- Importance of strong authentication demonstrated

## Security Recommendations
1. Implement account lockout policies
2. Use key-based authentication instead of passwords
3. Restrict SSH access to specific IP addresses
4. Monitor and log all SSH access attempts

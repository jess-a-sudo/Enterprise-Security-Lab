# Network Topology - Enterprise Security Lab

## Physical Layout

┌─────────────────────────────────────────────────────────────┐
│ ENTERPRISE NETWORK │
├──────────────┬────────────────┬─────────────────────────────┤
│ INTERNET │ FIREWALL │ DMZ ZONE │
│ │ (PFSense) │ ┌────────────────────┐ │
│ │ │ │ Web Server │ │
│ [ISP]───────┤ 10.10.10.1/24 ├──┤ 10.10.10.10/24 │ │
│ │ │ │ Ubuntu 20.04 │ │
│ │ │ └────────────────────┘ │
│ │ │ │
│ │ │ INTERNAL ZONE │
│ │ │ ┌────────────────────┐ │
│ │ │ │ Windows DC │ │
│ │ ├──┤ 192.168.10.10/24 │ │
│ │ │ │ Server 2016 │ │
│ │ │ └────────────────────┘ │
│ │ │ │
│ │ │ MANAGEMENT ZONE │
│ │ │ ┌────────────────────┐ │
│ │ │ │ Security Tools │ │
│ │ ├──┤ 172.16.10.10/24 │ │
│ │ │ │ Kali Linux │ │
│ │ │ └────────────────────┘ │
│ │ │ │
│ │ │ SECURITY ZONE │
│ │ │ ┌────────────────────┐ │
│ │ │ │ Monitoring │ │
│ │ ├──┤ 172.16.20.10/24 │ │
│ │ │ │ SIEM/Logging │ │
│ │ │ └────────────────────┘ │
└──────────────┴────────────────┴─────────────────────────────┘


## Network Segmentation
### Zone Descriptions
1. **DMZ Zone (10.10.10.0/24)**
   - Purpose: Public-facing services
   - Security: Strict inbound/outbound rules
   - Systems: Web servers, reverse proxies

2. **Internal Zone (192.168.10.0/24)**
   - Purpose: Enterprise applications
   - Security: Internal access only
   - Systems: Domain controllers, databases

3. **Management Zone (172.16.10.0/24)**
   - Purpose: Administrative access
   - Security: Jump host required
   - Systems: Security tools, management

4. **Security Zone (172.16.20.0/24)**
   - Purpose: Security monitoring
   - Security: Isolated monitoring
   - Systems: SIEM, logging, alerting

## Traffic Flow Rules
### Inbound Traffic
- Internet → DMZ: Port 443, 80 only
- DMZ → Internal: Specific application ports
- No direct Internet → Internal access

### Internal Traffic
- Zone-to-zone: Explicit allow rules
- Management access: VPN or jump host
- Security monitoring: Read-only access

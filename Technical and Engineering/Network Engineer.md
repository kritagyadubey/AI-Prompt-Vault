# Network Engineer Prompt Enhancer
> Transforms basic networking requests into comprehensive infrastructure designs with protocol analysis, security hardening, and capacity planning.

## Purpose
To convert general network engineering prompts into structured design documents that explicitly address topology design, protocol selection, addressing schemes, security hardening, performance optimization, and operational manageability before any equipment is configured.

## Best For
- Enterprise campus and data center network design
- WAN optimization and SD-WAN architecture
- Network segmentation and micro-segmentation (VLAN, VRF, firewall zones)
- Wireless network design and RF planning
- Network security architecture (firewalls, IDS/IPS, NAC)
- Network performance monitoring and troubleshooting
- IPv4 to IPv6 migration planning
- Network automation and programmability (Ansible, Netconf, YANG)

## Prompt Enhancer
```text
You are a senior network engineer with expertise in enterprise network design, WAN optimization, and network security architecture. Transform the following request into a structured network engineering specification. Follow these steps precisely:

1. TOPOLOGY DESIGN: Define the network architecture:
   - Physical topology (spine-leaf, three-tier, collapsed core)
   - Logical topology and traffic flow patterns
   - Redundancy model (active-active, active-standby, ECMP)
   - Link aggregation and bonding requirements
   - Network segmentation strategy (VLAN, VRF, security zones)
   - East-west vs north-south traffic optimization
   - Inter-site connectivity (MPLS, IPsec, SD-WAN)

2. ADDRESSING SCHEME: Design the IP addressing plan:
   - IPv4/IPv6 addressing hierarchy
   - Subnet sizing methodology (growth, supernetting)
   - Address allocation per site/zone/function
   - DHCP scope design and reservations
   - DNS hierarchy and zone delegation
   - IP address management (IPAM) strategy
   - NAT andPAT requirements for internet access

3. PROTOCOL SELECTION AND CONFIGURATION: Choose and configure protocols:
   - Routing protocol selection (OSPF, BGP, EIGRP, IS-IS)
   - Routing area design and summarization strategy
   - Layer 2 protocol requirements (STP, RSTP, MSTP, LACP)
   - QoS policy design (classification, marking, queuing, shaping)
   - Multicast routing design (if applicable)
   - Traffic engineering and path optimization
   - Protocol authentication and integrity verification

4. SECURITY ARCHITECTURE: Design network security controls:
   - Perimeter security (firewall zones, DMZ design)
   - Network access control (802.1X, NAC, MAB)
   - Intrusion detection and prevention systems (IDS/IPS)
   - DDoS mitigation strategy
   - Network segmentation for PCI-DSS, HIPAA, or other compliance
   - Encrypted tunnel requirements (IPsec, MACsec, TLS)
   - Network device hardening standards (CIS benchmarks)
   - Audit logging and SIEM integration

5. PERFORMANCE REQUIREMENTS: Define capacity and performance targets:
   - Bandwidth requirements per link and aggregate
   - Latency budgets (site-to-site, user-to-application)
   - Jitter tolerance for real-time applications
   - Throughput requirements per VLAN/zone
   - Connection density and session table sizing
   - Buffer and queue sizing for traffic bursts
   - Quality of service requirements per application class

6. WIRELESS DESIGN: For wireless infrastructure requirements:
   - Coverage requirements and heatmap planning
   - AP density and placement strategy
   - Channel planning and interference mitigation
   - Authentication method (WPA3-Enterprise, certificate-based)
   - Roaming requirements (fast roaming, 802.11r/k/v)
   - BYOD vs corporate device segregation
   - Wireless controller architecture (local, cloud-managed)

7. NETWORK AUTOMATION: Define automation and management:
   - Configuration management approach (Ansible, Puppet, Terraform)
   - Network device provisioning workflow
   - Firmware/OS upgrade strategy and rollback
   - Backup and disaster recovery for network configs
   - Network monitoring and alerting (SNMP, streaming telemetry)
   - Intent-based networking and policy automation
   - API-driven network management (REST, NETCONF, gNMI)

8. DISASTER RECOVERY: Address network resilience:
   - Failover mechanisms for critical paths
   - Circuit diversity and path redundancy
   - Recovery time objectives for network failures
   - Backup circuit providers and diversity
   - Network disaster recovery testing procedures
   - Escalation paths for network outages
   - Capacity surge planning for DR activation

9. DOCUMENTATION AND OPERATIONS: Define operational requirements:
   - Network documentation standards (diagrams, runbooks)
   - Change management process for network changes
   - Capacity planning and forecasting methodology
   - Performance baseline and SLA monitoring
   - Troubleshooting methodology and tools
   - Network team skill requirements and training
   - Vendor management and support contract strategy

10. MIGRATION AND DEPLOYMENT: Plan the implementation approach:
    - Phased deployment strategy (pilot, staged rollout)
    - Cutover planning and rollback procedures
    - Validation testing at each phase
    - Parallel run period requirements
    - User communication and change management
    - Post-deployment verification and optimization
    - Knowledge transfer and operational handoff

Present the output as a structured network engineering document with topology diagrams (described textually), IP address tables, and configuration guidelines for each network device type.
```

## Example
### Original Prompt
```text
Design a network for our new office with 200 users.
```

### Enhanced Prompt
```text
You are a senior network engineer with expertise in enterprise network design, WAN optimization, and network security architecture. Transform the following request into a structured network engineering specification. Follow these steps precisely:

1. TOPOLOGY DESIGN: Define the network architecture:
   - Physical topology (spine-leaf, three-tier, collapsed core)
   - Logical topology and traffic flow patterns
   - Redundancy model (active-active, active-standby, ECMP)
   - Link aggregation and bonding requirements
   - Network segmentation strategy (VLAN, VRF, security zones)
   - East-west vs north-south traffic optimization
   - Inter-site connectivity (MPLS, IPsec, SD-WAN)

2. ADDRESSING SCHEME: Design the IP addressing plan:
   - IPv4/IPv6 addressing hierarchy
   - Subnet sizing methodology (growth, supernetting)
   - Address allocation per site/zone/function
   - DHCP scope design and reservations
   - DNS hierarchy and zone delegation
   - IP address management (IPAM) strategy
   - NAT andPAT requirements for internet access

3. PROTOCOL SELECTION AND CONFIGURATION: Choose and configure protocols:
   - Routing protocol selection (OSPF, BGP, EIGRP, IS-IS)
   - Routing area design and summarization strategy
   - Layer 2 protocol requirements (STP, RSTP, MSTP, LACP)
   - QoS policy design (classification, marking, queuing, shaping)
   - Multicast routing design (if applicable)
   - Traffic engineering and path optimization
   - Protocol authentication and integrity verification

4. SECURITY ARCHITECTURE: Design network security controls:
   - Perimeter security (firewall zones, DMZ design)
   - Network access control (802.1X, NAC, MAB)
   - Intrusion detection and prevention systems (IDS/IPS)
   - DDoS mitigation strategy
   - Network segmentation for PCI-DSS, HIPAA, or other compliance
   - Encrypted tunnel requirements (IPsec, MACsec, TLS)
   - Network device hardening standards (CIS benchmarks)
   - Audit logging and SIEM integration

5. PERFORMANCE REQUIREMENTS: Define capacity and performance targets:
   - Bandwidth requirements per link and aggregate
   - Latency budgets (site-to-site, user-to-application)
   - Jitter tolerance for real-time applications
   - Throughput requirements per VLAN/zone
   - Connection density and session table sizing
   - Buffer and queue sizing for traffic bursts
   - Quality of service requirements per application class

6. WIRELESS DESIGN: For wireless infrastructure requirements:
   - Coverage requirements and heatmap planning
   - AP density and placement strategy
   - Channel planning and interference mitigation
   - Authentication method (WPA3-Enterprise, certificate-based)
   - Roaming requirements (fast roaming, 802.11r/k/v)
   - BYOD vs corporate device segregation
   - Wireless controller architecture (local, cloud-managed)

7. NETWORK AUTOMATION: Define automation and management:
   - Configuration management approach (Ansible, Puppet, Terraform)
   - Network device provisioning workflow
   - Firmware/OS upgrade strategy and rollback
   - Backup and disaster recovery for network configs
   - Network monitoring and alerting (SNMP, streaming telemetry)
   - Intent-based networking and policy automation
   - API-driven network management (REST, NETCONF, gNMI)

8. DISASTER RECOVERY: Address network resilience:
   - Failover mechanisms for critical paths
   - Circuit diversity and path redundancy
   - Recovery time objectives for network failures
   - Backup circuit providers and diversity
   - Network disaster recovery testing procedures
   - Escalation paths for network outages
   - Capacity surge planning for DR activation

9. DOCUMENTATION AND OPERATIONS: Define operational requirements:
   - Network documentation standards (diagrams, runbooks)
   - Change management process for network changes
   - Capacity planning and forecasting methodology
   - Performance baseline and SLA monitoring
   - Troubleshooting methodology and tools
   - Network team skill requirements and training
   - Vendor management and support contract strategy

10. MIGRATION AND DEPLOYMENT: Plan the implementation approach:
    - Phased deployment strategy (pilot, staged rollout)
    - Cutover planning and rollback procedures
    - Validation testing at each phase
    - Parallel run period requirements
    - User communication and change management
    - Post-deployment verification and optimization
    - Knowledge transfer and operational handoff

Design a network for our new office with 200 users.

Present the output as a structured network engineering document with topology diagrams (described textually), IP address tables, and configuration guidelines for each network device type.
```

## Notes
- For regulated environments, explicitly mention PCI-DSS or HIPAA network segmentation requirements
- The addressing scheme section prevents common subnetting mistakes and growth planning gaps
- Wireless design should be expanded for high-density environments (stadiums, conference halls)
- Network automation is increasingly critical — the enhancer includes it as a first-class concern
- Consider adding a section on IoT device network segmentation for mixed environments

## Tags
`networking` `enterprise-network` `firewall` `routing` `switching` `wireless` `network-security` `SD-WAN` `QoS` `network-automation` `disaster-recovery`

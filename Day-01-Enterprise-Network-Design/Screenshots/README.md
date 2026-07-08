# Day 01 - Enterprise Network Design and Virtual Security Lab Planning

## Enterprise Security Transformation Project (ESTP)

Day 01 focused on designing and planning a simulated enterprise cybersecurity infrastructure for **SecureTech Solutions**.

The objective was to build the foundation of a real-world enterprise security lab before deploying Active Directory, firewall policies, centralized logging, SIEM monitoring, and security detection capabilities.

This phase covered enterprise network architecture, department segmentation, IP address planning, VLAN design, virtual machine planning, and VMware-based lab preparation.

---

## Project Scenario

SecureTech Solutions is a simulated mid-sized IT services and technology company with more than 150 employees.

The organization provides:

- IT Consulting
- Software Development
- Cybersecurity Services
- Technical Solutions

The enterprise environment was designed to simulate a real corporate infrastructure where different departments, servers, security systems, and client machines require centralized management and security monitoring.

### Company Departments

The following business departments were considered during infrastructure planning:

- Human Resources (HR)
- Finance
- Information Technology (IT)
- Management
- Sales and Marketing
- Security Operations Center (SOC)

The purpose of defining departments was to prepare the environment for logical network segmentation, identity management, access control, and security monitoring.

---

## Day 01 Objectives

The main objectives of Day 01 were:

- Define the enterprise project scenario
- Understand organizational departments
- Design an enterprise network topology
- Plan network segmentation using VLANs
- Create an IP addressing strategy
- Design the virtual cybersecurity lab
- Prepare VMware Workstation
- Prepare Windows client and server virtual machines
- Prepare the pfSense firewall virtual machine
- Establish the foundation for future SOC and SIEM deployment

---

## Enterprise Network Architecture

A multi-segment enterprise network architecture was designed to simulate a real-world corporate environment.

The planned network flow is:

`Internet → ISP Router → pfSense Firewall → Core Switch → Department VLANs and Server Infrastructure`

The pfSense firewall is positioned at the security boundary of the enterprise network.

Its planned role includes:

- Network traffic control
- Inter-VLAN routing
- Firewall policy enforcement
- Network segmentation
- Internet access management
- Security monitoring support

A Layer 3/core switching architecture was included in the network design to connect enterprise departments and infrastructure systems.

---

## Network Segmentation and VLAN Planning

Logical network segmentation was designed to separate business departments and critical infrastructure.

The planned VLAN architecture included:

| VLAN | Department / Zone | Subnet |
|---|---|---|
| VLAN 10 | Human Resources | 192.168.10.0/24 |
| VLAN 20 | Finance | 192.168.20.0/24 |
| VLAN 30 | Information Technology | 192.168.30.0/24 |
| VLAN 40 | Management / Development | 192.168.40.0/24 |
| VLAN 50 | Servers | 192.168.50.0/24 |
| VLAN 60 | Security Operations Center | 192.168.60.0/24 |
| VLAN 70 | Guest Wi-Fi | 192.168.70.0/24 |

The segmentation strategy was designed to reduce unnecessary communication between departments and provide a foundation for security policy enforcement.

> Note: VLAN segmentation in this phase represents the planned enterprise architecture. Configuration and security controls are implemented in later phases of the project.

---

## IP Address Planning

An IP addressing strategy was prepared for enterprise devices, servers, departments, and security infrastructure.

The IP plan was designed to:

- Organize network devices
- Separate departments logically
- Simplify network troubleshooting
- Support firewall rule creation
- Improve security visibility
- Prepare systems for centralized monitoring

Dedicated network ranges were planned for departments, servers, SOC infrastructure, and guest systems.

---

## Virtual Security Lab Design

The enterprise environment was designed using VMware Workstation Pro 17.

The virtual lab provides an isolated environment for building, testing, monitoring, and investigating enterprise security configurations.

### Planned Virtual Systems

The lab architecture includes:

- Windows Server
- Windows Client Systems
- pfSense Firewall
- Wazuh SIEM Server
- Kali Linux
- Additional test systems

These virtual machines represent different components of a corporate IT and cybersecurity infrastructure.

---

## Windows Server Environment

A Windows Server virtual machine was prepared as part of the enterprise lab.

The server environment was planned to support future services including:

- Active Directory Domain Services
- Domain Controller
- DNS
- Centralized User Management
- Group Policy
- Enterprise Authentication

The Windows Server system provides the foundation for centralized identity and access management in the project.

---

## Windows Client Environment

A Windows client virtual machine was prepared to simulate an enterprise employee workstation.

The client system is used throughout the project for:

- Domain joining
- User authentication testing
- Group Policy validation
- Network connectivity testing
- Endpoint monitoring
- Sysmon telemetry generation
- Wazuh agent integration

This system represents a standard corporate endpoint inside the enterprise network.

---

## pfSense Firewall Preparation

A pfSense firewall virtual machine was prepared with multiple network interfaces.

The firewall was designed to operate between the external network and the internal enterprise lab.

The pfSense environment will be used for:

- WAN and LAN connectivity
- Firewall rule configuration
- Network access control
- Traffic filtering
- Network segmentation
- Security policy enforcement

The firewall VM forms an important part of the defense-in-depth architecture of the project.

---

## VMware Lab Environment

VMware Workstation Pro 17 was used as the virtualization platform for the Enterprise Security Transformation Project.

The lab contains multiple systems representing enterprise and security infrastructure.

The virtual environment allows security configurations and attack simulations to be performed without affecting a production network.

This approach provides a controlled environment for SOC analysis, log monitoring, firewall testing, and security investigation.

---

## Implementation Evidence

### 1. Windows Client Virtual Machine

![Windows Client Virtual Machine](Screenshots/01-windows-client-vm.png)

A Windows client virtual machine was prepared to represent an enterprise user endpoint.

---

### 2. Windows Server Virtual Machine

![Windows Server Virtual Machine](Screenshots/02-windows-server-vm.png)

The Windows Server virtual machine was prepared for centralized enterprise services and identity management.

---

### 3. Enterprise Project and Infrastructure Overview

![Enterprise Project Overview](Screenshots/03-enterprise-project-overview.png)

The project overview documents the SecureTech Solutions scenario, company departments, enterprise network topology, IP address plan, and virtual lab architecture.

---

### 4. VMware Virtual Security Lab

![VMware Virtual Lab](Screenshots/04-vmware-virtual-lab-environment.png)

VMware Workstation Pro 17 hosts the virtual enterprise cybersecurity infrastructure used throughout the project.

---

### 5. pfSense Firewall Virtual Machine

![pfSense Firewall VM](Screenshots/05-pfsense-firewall-vm.png)

The pfSense firewall virtual machine was prepared with WAN and LAN network interfaces for enterprise network security.

---

### 6. Enterprise Network Topology

![Enterprise Network Topology](Screenshots/06-enterprise-network-topology.png)

The network topology illustrates the planned enterprise architecture, including the firewall, core switching layer, departmental VLANs, server infrastructure, SOC network, and guest network.

---

## Security Design Considerations

The enterprise infrastructure was designed around several cybersecurity principles:

- Network Segmentation
- Least Privilege
- Defense in Depth
- Centralized Identity Management
- Centralized Log Monitoring
- Endpoint Visibility
- Security Event Detection
- Controlled Network Access

The SOC network was planned to receive security telemetry from enterprise systems and security devices.

The guest network was designed as an isolated network segment to reduce exposure to internal corporate resources.

---

## Skills Demonstrated

- Enterprise Network Design
- Cybersecurity Lab Architecture
- Network Segmentation
- VLAN Planning
- IP Address Planning
- VMware Workstation
- Virtual Machine Deployment
- Windows Server Planning
- Windows Endpoint Planning
- pfSense Firewall Deployment
- Security Architecture
- SOC Infrastructure Planning

---

## Tools and Technologies

- VMware Workstation Pro 17
- Windows Server
- Windows Client
- pfSense Firewall
- Wazuh SIEM
- Kali Linux
- TCP/IP Networking
- VLAN Architecture
- Virtual Networking

---

## Key Learning Outcomes

During Day 01, I gained practical understanding of how enterprise security infrastructure is planned before security tools are deployed.

I learned how network architecture, IP addressing, department segmentation, virtualization, and firewall placement contribute to the overall security posture of an organization.

This phase established the technical foundation for Active Directory deployment, DNS configuration, Group Policy implementation, pfSense firewall security, Wazuh SIEM monitoring, Sysmon telemetry, and SOC operations in the next phases of the project.

---

## Project Keywords

`Cybersecurity` `SOC Analyst` `SOC Lab` `Enterprise Security` `Network Security` `Blue Team` `Security Operations Center` `VMware` `pfSense` `Firewall` `Wazuh SIEM` `Sysmon` `Active Directory` `Windows Server` `Network Segmentation` `VLAN` `SIEM` `Log Monitoring` `Threat Detection` `Security Monitoring` `Cybersecurity Portfolio` `Home Lab`

---

## Next Phase

**Day 02 - Windows Server Deployment and Initial Configuration**

The next phase focuses on preparing the Windows Server environment for enterprise identity, authentication, and centralized infrastructure services.

# Day 02 - Windows Server 2025 Deployment and Initial Configuration

## Enterprise Security Transformation Project (ESTP)

Day 02 of the Enterprise Security Transformation Project focused on deploying and preparing a Windows Server environment for centralized enterprise infrastructure services.

The Windows Server system was deployed inside VMware Workstation and configured as the foundation for future Active Directory Domain Services, DNS, Group Policy, centralized authentication, and security monitoring.

This phase established the core Windows Server infrastructure required for building a secure enterprise domain environment.

---

## Day 02 Objectives

The main objectives of Day 02 were:

- Deploy Windows Server 2025 in VMware Workstation
- Prepare the server virtual machine
- Access and review Windows Server Manager
- Configure the server identity
- Assign a static IP address
- Prepare the server for enterprise roles
- Explore the Add Roles and Features Wizard
- Prepare the environment for Active Directory deployment
- Establish the foundation for centralized enterprise management

---

## Windows Server Deployment

Windows Server 2025 was deployed as a virtual machine using VMware Workstation Pro 17.

The virtual machine was created to act as the primary enterprise server in the SecureTech Solutions cybersecurity lab.

The server provides the infrastructure foundation for future services including:

- Active Directory Domain Services
- Domain Controller Services
- DNS
- Group Policy Management
- Centralized User Authentication
- Enterprise Identity Management
- Windows Event Logging
- Security Monitoring

The virtualized server environment allows enterprise configurations to be tested in an isolated cybersecurity lab.

---

## Server Virtual Machine Configuration

The Windows Server virtual machine was prepared with dedicated virtual hardware resources.

The server VM included:

- Windows Server 2025
- Virtual CPU resources
- Dedicated virtual memory
- Virtual NVMe storage
- VMware virtual network adapter
- Internal lab network connectivity

The network adapter was connected to the custom VMware virtual network used by the enterprise security lab.

This allows the server to communicate with enterprise client systems and security infrastructure inside the isolated environment.

---

## Server Manager

Windows Server Manager was used as the centralized management interface for configuring and monitoring the server.

Server Manager provides access to:

- Local Server Configuration
- Server Roles
- Server Features
- Active Directory Management Tools
- DNS Management
- Event Viewer
- Group Policy Management
- Windows PowerShell
- Computer Management
- Security Administration Tools

The Server Manager dashboard provides centralized visibility into server roles, services, events, and system performance.

---

## Server Identity Configuration

The Windows Server system was configured with the computer name:

`DC-01`

A clear server naming convention was used to identify the role of the system inside the enterprise infrastructure.

`DC` represents the planned Domain Controller role, while `01` identifies the server as the first system assigned to this role.

Using structured server naming conventions improves:

- Infrastructure Management
- Asset Identification
- Troubleshooting
- Security Monitoring
- Log Analysis
- SOC Investigations

---

## Static IP Address Configuration

The Windows Server was configured with the following IP address:

| Configuration | Value |
|---|---|
| Server Name | DC-01 |
| IP Address | 192.168.10.10 |
| Network Environment | Enterprise Lab |
| Network Adapter | VMware Custom Network |

A static IP address was used because enterprise infrastructure services require predictable and consistent network communication.

Static IP addressing is important for systems providing services such as:

- Domain Controllers
- DNS Servers
- SIEM Servers
- Firewalls
- File Servers
- Security Monitoring Systems

Dynamic IP changes could affect domain services, DNS resolution, endpoint connectivity, and security monitoring.

---

## Add Roles and Features Wizard

The Add Roles and Features Wizard was accessed through Windows Server Manager.

This wizard is used to install and configure Windows Server roles and features.

Before installing enterprise server roles, the following configuration requirements were reviewed:

- Administrator account security
- Static IP address configuration
- Network settings
- Windows security updates
- Server readiness

The server was prepared for the installation of enterprise infrastructure roles in the next project phases.

---

## Enterprise Role Preparation

The Windows Server was prepared to support centralized enterprise services.

The planned server roles include:

- Active Directory Domain Services (AD DS)
- Domain Controller
- Domain Name System (DNS)
- Group Policy Management

These services will provide centralized identity, authentication, name resolution, and security policy management for enterprise users and computers.

Detailed Active Directory and DNS implementation is documented in the next phases of the project.

---



## Security Considerations

Several security and infrastructure considerations were applied during the Windows Server deployment phase:

- Dedicated Server Identity
- Static IP Addressing
- Isolated Virtual Lab Network
- Centralized Server Management
- Structured Server Naming
- Controlled Role Deployment
- Enterprise Service Planning

The server was prepared as a critical infrastructure system rather than a standard endpoint.

This approach supports centralized security management and improves visibility during future SOC monitoring activities.

---

## Why Windows Server is Important in a SOC Environment

Windows Server systems generate important security telemetry that can be monitored by a Security Operations Center.

Examples of security events include:

- Successful Logons
- Failed Logon Attempts
- Account Creation
- Account Deletion
- Privilege Changes
- Group Membership Changes
- Authentication Events
- Kerberos Events
- Service Activity
- Policy Changes

These events can later be collected and analyzed using a Security Information and Event Management platform.

In this project, Windows Server security telemetry will later be integrated with Wazuh SIEM for centralized security monitoring and threat detection.

---

## Skills Demonstrated

- Windows Server 2025
- Windows Server Deployment
- Server Administration
- VMware Workstation
- Virtual Machine Configuration
- Static IP Addressing
- Server Manager
- Enterprise Infrastructure
- Windows Server Roles
- Network Configuration
- Identity Infrastructure Planning
- Cybersecurity Lab Deployment
- SOC Infrastructure Planning

---

## Tools and Technologies

- Windows Server 2025
- VMware Workstation Pro 17
- Windows Server Manager
- TCP/IP Networking
- VMware Virtual Networking
- Windows Administrative Tools
- Windows Server Roles and Features

---

## Key Learning Outcomes

During Day 02, I gained practical experience deploying and preparing a Windows Server system inside a virtual enterprise cybersecurity environment.

I learned how server identity, static IP addressing, virtual networking, and Server Manager contribute to enterprise infrastructure management.

I also explored the Windows Server role deployment process and prepared the server for Active Directory Domain Services and DNS configuration.

This phase created the Windows Server foundation required for centralized identity management, authentication, Group Policy, security event generation, and future SIEM monitoring.

---

## Project Keywords

`Cybersecurity` `Windows Server 2025` `Windows Server` `Server Administration` `SOC Analyst` `Blue Team` `Enterprise Security` `Active Directory` `AD DS` `Domain Controller` `DNS` `VMware Workstation` `Virtual Lab` `Cybersecurity Home Lab` `Network Security` `Static IP` `Server Manager` `SIEM` `Wazuh` `Security Monitoring` `Windows Event Logs` `SOC Lab` `Cybersecurity Portfolio`

---

## Next Phase

**Day 03 - Active Directory and User Management**

The next phase focuses on deploying Active Directory Domain Services, configuring the enterprise domain, and implementing centralized user and organizational management.

<p align="center">
  <img src="project-thumbnail.png" alt="Enterprise Security Transformation Project" width="100%">
</p>

<h1 align="center">🛡️ Enterprise Security Transformation Project</h1>

<p align="center">
  <b>SecureTech Solutions</b><br>
  Building a Modern, Monitored & Secure Enterprise Environment
</p>

---

## 📌 Project Overview



# 🛡️ Enterprise Security Transformation Project (ESTP)

## SecureTech Solutions

The **Enterprise Security Transformation Project (ESTP)** is a practical enterprise cybersecurity lab designed to simulate the process of building, securing, and monitoring a small enterprise infrastructure.

The project was developed under the fictional organization **SecureTech Solutions** and focuses on practical experience in:

- Enterprise Network Design
- Windows Server Administration
- Active Directory
- DNS Infrastructure
- Organizational Unit Management
- Identity and Access Management
- Domain Administration
- pfSense Firewall Deployment
- Wazuh SIEM
- Endpoint Security Monitoring
- Windows Log Analysis
- Threat Hunting
- Sysmon Telemetry
- SOC Alert Investigation

The main objective of this project was to build an enterprise environment from scratch and gradually transform it into a centralized security monitoring environment.

---

# 📌 Project Overview

Modern organizations require multiple security layers to protect their infrastructure.

This project simulates an enterprise environment where network infrastructure, identity services, firewall security, endpoint monitoring, and SIEM capabilities are deployed step by step.

The project follows the security transformation lifecycle:

`Enterprise Planning`

↓

`Infrastructure Deployment`

↓

`Identity Infrastructure`

↓

`Network Security`

↓

`Centralized Security Monitoring`

↓

`Endpoint Telemetry`

↓

`Threat Hunting`

↓

`SOC Investigation`

The final environment provides centralized visibility into Windows endpoint activity and security events.

---

# 🎯 Project Objectives

The main objectives of this project were:

- Design a secure enterprise network architecture
- Build a VMware-based enterprise security lab
- Deploy Windows Server infrastructure
- Configure Active Directory Domain Services
- Configure enterprise DNS services
- Design Organizational Units
- Create enterprise users and security groups
- Join Windows endpoints to the enterprise domain
- Deploy pfSense as an enterprise firewall
- Configure secure LAN and WAN communication
- Deploy Wazuh SIEM
- Install and configure Wazuh agents
- Collect Windows security logs
- Monitor endpoint activity
- Analyze security alerts
- Perform threat hunting
- Investigate PowerShell activity
- Review process and command-line telemetry
- Correlate multiple security events
- Develop practical SOC analyst skills

---

# 🏢 Enterprise Scenario

SecureTech Solutions required a complete enterprise infrastructure that could support centralized identity management, network security, and security monitoring.

The environment needed:

- Centralized authentication
- Enterprise DNS
- Department-based organization
- User and group management
- Domain-connected endpoints
- Network firewall protection
- Centralized log collection
- Endpoint monitoring
- Security alert generation
- Threat hunting capabilities

The infrastructure was designed and deployed from scratch inside a virtualized lab environment.

---

# 🏗️ Enterprise Security Architecture

The project architecture follows a layered security model.

`Internet / External Network`

↓

`pfSense Firewall`

↓

`Enterprise LAN - 192.168.10.0/24`

↓

`Windows Server 2025 - DC-01`

↓

`Active Directory + DNS`

↓

`Domain Connected Windows Endpoints`

↓

`Wazuh Agents`

↓

`Wazuh SIEM Server`

↓

`Security Alerts`

↓

`Threat Hunting`

↓

`SOC Analyst Investigation`

This architecture provides centralized administration and security monitoring.

---

# 🌐 Network Architecture

The enterprise LAN uses the following network:

`192.168.10.0/24`

Important systems deployed in the environment include:

| System | Hostname | IP Address | Role |
|---|---|---|---|
| pfSense | pfSense | 192.168.10.1 | Firewall / Gateway |
| Windows Server | DC-01 | 192.168.10.10 | Domain Controller |
| Wazuh Server | wazuh-server | 192.168.10.12 | SIEM Server |
| Windows Client | Domain Endpoint | Enterprise LAN | User Endpoint |

The pfSense firewall acts as the default gateway for the enterprise network.

The Windows Server provides centralized identity and DNS services.

The Wazuh Server provides centralized security monitoring and threat hunting capabilities.

---

# 🧰 Technologies Used

| Technology | Purpose |
|---|---|
| VMware Workstation Pro | Enterprise Lab Virtualization |
| Windows Server 2025 | Enterprise Server Infrastructure |
| Active Directory Domain Services | Centralized Identity Management |
| DNS | Enterprise Name Resolution |
| Organizational Units | Administrative Organization |
| Security Groups | Role-Based Access Management |
| Windows Client | Enterprise Endpoint |
| pfSense | Firewall and Network Gateway |
| Wazuh | SIEM and Security Monitoring |
| Wazuh Agent | Endpoint Log Collection |
| Sysmon | Detailed Windows Telemetry |
| PowerShell | Windows Administration and Security Analysis |
| Windows Event Logs | Security Event Collection |
| MITRE ATT&CK | Threat Behavior Analysis |

---

# 📅 Project Implementation Journey

The project was completed through multiple implementation days.

Each day focused on a specific enterprise infrastructure or security monitoring objective.

---

## 📘 Day 01 - Enterprise Planning and Network Design

Day 01 focused on designing the foundation of the enterprise environment.

Key activities included:

- Defined the SecureTech Solutions enterprise scenario
- Planned the enterprise infrastructure
- Designed the network topology
- Created the IP addressing plan
- Planned VLAN architecture
- Designed the VMware lab environment
- Identified required servers and endpoints
- Prepared the project structure

### Skills

`Network Design` `IP Addressing` `Enterprise Planning` `Security Architecture`

📂 **View Day 01 Documentation:** [Day 01](Day-01/README.md)

---

## 🖥️ Day 02 - Enterprise Lab Setup and Infrastructure Preparation

Day 02 focused on preparing the virtual enterprise environment.

Key activities included:

- Configured VMware Workstation
- Created required virtual machines
- Prepared Windows Server 2025
- Prepared Windows client systems
- Prepared pfSense
- Configured VMware network adapters
- Verified initial system connectivity
- Prepared the server for enterprise deployment

### Skills

`VMware` `Virtualization` `Windows Server` `Network Configuration`

📂 **View Day 02 Documentation:** [Day 02](Day-02/README.md)

---

## 🏢 Day 03 - Active Directory Domain Services Deployment

Day 03 focused on deploying centralized identity infrastructure.

Key activities included:

- Installed Active Directory Domain Services
- Promoted Windows Server to Domain Controller
- Created the enterprise domain
- Configured the Domain Controller
- Verified Active Directory services
- Prepared centralized authentication infrastructure

### Domain

`securetech.local`

### Domain Controller

`DC-01`

### Skills

`Active Directory` `AD DS` `Domain Controller` `Identity Management`

📂 **View Day 03 Documentation:** [Day 03](Day-03/README.md)

---

## 🌐 Day 04 - Enterprise DNS Configuration

Day 04 focused on configuring enterprise DNS infrastructure.

Key activities included:

- Configured DNS services
- Verified DNS zones
- Reviewed domain DNS records
- Configured DNS resolution
- Tested hostname resolution
- Troubleshot DNS connectivity
- Verified Active Directory DNS integration

### Skills

`DNS` `Name Resolution` `Windows Server DNS` `Troubleshooting`

📂 **View Day 04 Documentation:** [Day 04](Day-04/README.md)

---

## 🗂️ Day 05 - Organizational Unit Design

Day 05 focused on designing the Active Directory administrative structure.

Key activities included:

- Created Organizational Units
- Designed department-based OU structure
- Organized enterprise resources
- Prepared administrative boundaries
- Improved Active Directory management

The OU architecture represents enterprise departments and provides a structured environment for identity administration.

### Skills

`Active Directory` `Organizational Units` `Enterprise Administration`

📂 **View Day 05 Documentation:** [Day 05](Day-05/README.md)

---

## 👥 Day 06 - Enterprise Users and Security Groups

Day 06 focused on identity and access management.

Key activities included:

- Created enterprise user accounts
- Created security groups
- Assigned users to appropriate groups
- Organized users by department
- Implemented structured access management
- Reviewed group membership

This phase introduced role-based identity organization.

### Skills

`Identity Management` `Security Groups` `User Administration` `Access Control`

📂 **View Day 06 Documentation:** [Day 06](Day-06/README.md)

---

## 💻 Day 07 - Windows Domain Integration and Security Monitoring

Day 07 focused on integrating enterprise systems and deploying centralized monitoring.

Key activities included:

- Configured Windows endpoint networking
- Verified communication with the Domain Controller
- Joined Windows systems to the enterprise domain
- Verified domain authentication
- Deployed pfSense firewall infrastructure
- Configured enterprise gateway communication
- Deployed the Wazuh SIEM server
- Installed the Wazuh Windows Agent
- Connected the Domain Controller to Wazuh
- Verified centralized Windows event collection
- Reviewed Wazuh Threat Hunting events

The monitored Domain Controller was:

`dc-01`

The endpoint IP address was:

`192.168.10.10`

The Wazuh Manager was:

`192.168.10.12`

### Skills

`Domain Join` `pfSense` `Wazuh SIEM` `Log Collection` `Threat Hunting`

📂 **View Day 07 Documentation:** [Day 07](Day-07/README.md)

---

## 🔍 Day 08 - Sysmon and Advanced Endpoint Security Monitoring

Day 08 focused on improving endpoint security visibility.

Detailed Windows endpoint telemetry was analyzed through the Wazuh SIEM platform.

Key activities included:

- Reviewed Sysmon monitoring concepts
- Improved endpoint telemetry visibility
- Monitored process activity
- Investigated PowerShell execution
- Reviewed discovery activity
- Analyzed command-line information
- Investigated Windows security configuration activity
- Reviewed file hashes
- Analyzed Wazuh Rule IDs
- Reviewed alert severity levels
- Correlated multiple security events
- Performed SOC-style alert triage

Observed Wazuh events included:

| Security Event | Rule Level | Rule ID |
|---|---:|---:|
| Discovery Activity Executed | 3 | 92031 |
| Windows Logon Success | 3 | 60106 |
| PowerShell Process Created | 9 | 92205 |
| Windows Security Configuration Activity | 4 | 92066 |
| PowerShell File Deletion Activity | 3 | 92021 |

A Windows security configuration event involving `SecEdit.exe` was investigated.

Example command-line activity:

`SecEdit.exe /export /cfg C:\WINDOWS\TEMP\secpol.cfg`

Detailed event information included:

- Agent IP
- Agent Name
- Command Line
- Process Description
- Executable Company
- Current Directory
- File Version
- Cryptographic Hashes

### Skills

`Sysmon` `Endpoint Telemetry` `PowerShell Monitoring` `Command-Line Analysis` `Event Correlation` `SOC Investigation`

📂 **View Day 08 Documentation:** [Day 08](Day-08/README.md)

---

# 🔍 SOC Monitoring Workflow

The security monitoring workflow implemented in the project follows:

`Windows Endpoint Activity`

↓

`Windows Logs / Endpoint Telemetry`

↓

`Wazuh Agent`

↓

`Wazuh Manager`

↓

`Wazuh Rules`

↓

`Security Alert`

↓

`Threat Hunting`

↓

`Alert Triage`

↓

`Event Investigation`

↓

`Security Decision`

This represents a basic SOC investigation workflow.

---

# 🚨 Alert Investigation Process

During security event investigation, the following information was reviewed:

1. Timestamp
2. Agent Name
3. Agent IP Address
4. Rule Description
5. Rule Level
6. Rule ID
7. User Account
8. Process Name
9. Process Path
10. Command Line
11. Parent Process
12. File Hashes
13. Related Security Events

Events were reviewed and correlated before determining whether the activity was:

`Benign`

`Suspicious`

or

`Potentially Malicious`

---

# 🧠 Key Security Concepts Implemented

The project provided practical experience with:

- Defense in Depth
- Centralized Identity Management
- Enterprise DNS
- Role-Based Access Organization
- Network Segmentation Planning
- Firewall Security
- Centralized Log Management
- SIEM Monitoring
- Endpoint Telemetry
- Security Event Analysis
- Threat Hunting
- Alert Triage
- Event Correlation
- Process Investigation
- Command-Line Analysis
- MITRE ATT&CK Analysis

---

# 🛡️ Security Layers Implemented

The enterprise environment includes multiple security layers.

### Layer 1 - Network Security

Implemented using pfSense.

Provides:

- Gateway Security
- Network Control
- Firewall Protection

### Layer 2 - Identity Security

Implemented using Active Directory.

Provides:

- Centralized Authentication
- User Management
- Security Groups
- Domain Administration

### Layer 3 - Endpoint Monitoring

Implemented using Windows telemetry and Sysmon concepts.

Provides:

- Process Visibility
- Command-Line Monitoring
- PowerShell Monitoring
- File Activity Visibility

### Layer 4 - Centralized Security Monitoring

Implemented using Wazuh SIEM.

Provides:

- Centralized Log Collection
- Security Alerts
- Rule-Based Detection
- Threat Hunting
- Event Investigation

---

# 🎓 Skills Developed

Throughout this project, I developed practical skills in:

- Enterprise Security Architecture
- Network Design
- IP Address Planning
- VMware Virtualization
- Windows Server Administration
- Active Directory
- DNS
- Organizational Units
- User Administration
- Security Groups
- Identity and Access Management
- Domain Administration
- pfSense Firewall
- Wazuh SIEM
- Windows Security Monitoring
- Sysmon
- Endpoint Telemetry
- Log Analysis
- Threat Hunting
- Alert Triage
- PowerShell Investigation
- Process Analysis
- Command-Line Analysis
- File Hash Analysis
- Security Event Correlation
- MITRE ATT&CK
- SOC Operations
- Blue Team Security

---

# 🧪 Practical SOC Experience

This project helped me understand that SOC monitoring is not limited to viewing alerts.

A security analyst must:

- Understand the environment
- Identify the affected endpoint
- Review alert severity
- Analyze event details
- Investigate process activity
- Review command-line execution
- Check file hashes
- Correlate related events
- Build an event timeline
- Determine the security context
- Escalate suspicious activity when required

The project provided practical exposure to a basic SOC Level 1 investigation workflow.

---

# 🚀 Future Improvements

Future improvements planned for the Enterprise Security Transformation Project include:

- File Integrity Monitoring
- Custom Wazuh Detection Rules
- Advanced PowerShell Detection
- Brute-Force Attack Detection
- Authentication Failure Monitoring
- MITRE ATT&CK Mapping
- Threat Intelligence Integration
- Automated IOC Enrichment
- Custom SOC Dashboards
- Incident Response Workflows
- Automated Security Reporting
- AI-Assisted Log Analysis
- Local AI Model Integration with Wazuh
- Automated Security Alert Summarization

The long-term objective is to integrate Wazuh security events with a local AI model.

The AI system will analyze security events and generate simplified investigation summaries for SOC analysts.

---

# 📈 Project Outcome

The Enterprise Security Transformation Project successfully transformed a basic virtual environment into a centralized enterprise security monitoring lab.

The final environment includes:

- Enterprise Network Architecture
- Windows Server Infrastructure
- Active Directory Domain
- Enterprise DNS
- Organizational Unit Structure
- User and Security Group Management
- Domain-Connected Systems
- pfSense Firewall
- Wazuh SIEM
- Centralized Windows Log Collection
- Endpoint Security Monitoring
- Threat Hunting
- Process Activity Analysis
- PowerShell Monitoring
- SOC Alert Investigation

This project demonstrates practical knowledge of enterprise infrastructure, security monitoring, and SOC operations.

---

# 👨‍💻 Project Focus

`SOC Analyst`

`Blue Team Security`

`Enterprise Security`

`SIEM Monitoring`

`Threat Hunting`

`Endpoint Security`

`Windows Security`

`Network Security`

---

# 🔖 Project Keywords

`Cybersecurity` `SOC Analyst` `SOC L1` `Blue Team` `Wazuh` `Wazuh SIEM` `Sysmon` `pfSense` `Active Directory` `Windows Server 2025` `DNS` `VMware` `SIEM` `Threat Hunting` `Log Analysis` `Endpoint Security` `Endpoint Telemetry` `PowerShell` `MITRE ATT&CK` `Alert Triage` `Event Correlation` `Network Security` `Enterprise Security` `Security Monitoring` `Cybersecurity Lab` `SOC Lab`

---

# 📚 Project Documentation

Detailed technical implementation is available in the individual Day documentation.

| Day | Project Phase |
|---|---|
| Day 01 | Enterprise Planning and Network Design |
| Day 02 | Enterprise Lab Setup and Infrastructure Preparation |
| Day 03 | Active Directory Domain Services |
| Day 04 | Enterprise DNS Configuration |
| Day 05 | Organizational Unit Design |
| Day 06 | Enterprise Users and Security Groups |
| Day 07 | Domain Integration, pfSense and Wazuh SIEM |
| Day 08 | Sysmon and Advanced Endpoint Security Monitoring |

Each Day directory contains detailed implementation steps, technical explanations, and project screenshots.

---

# ⭐ Enterprise Security Transformation Project

**Designed and implemented as a practical enterprise cybersecurity and SOC monitoring lab.**

**Project: Enterprise Security Transformation Project (ESTP)**

**Organization: SecureTech Solutions**

**Focus: SOC | Blue Team | SIEM | Enterprise Security | Threat Hunting**

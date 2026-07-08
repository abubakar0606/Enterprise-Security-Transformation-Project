# Day 03 - Active Directory Deployment and Enterprise User Management

## Enterprise Security Transformation Project (ESTP)

Day 03 of the Enterprise Security Transformation Project focused on deploying Active Directory Domain Services and building a centralized identity management structure for the SecureTech Solutions enterprise environment.

The Windows Server system was configured as the domain controller `DC-01`, and the enterprise domain `securetech.local` was used to centrally organize users, departments, computers, servers, service accounts, and security-related identities.

This phase introduced centralized identity and access management, which is a critical component of enterprise cybersecurity and Security Operations Center monitoring.

---

## Day 03 Objectives

The main objectives of Day 03 were:

- Deploy Active Directory Domain Services
- Prepare the Windows Server as a Domain Controller
- Configure the `securetech.local` enterprise domain
- Access Active Directory Users and Computers
- Design an Organizational Unit structure
- Create department-based user accounts
- Create security groups
- Organize SOC-related identities
- Configure user group membership
- Prepare Active Directory for Group Policy and security monitoring

---

## Active Directory Domain Services

Active Directory Domain Services (AD DS) was deployed to provide centralized identity and directory management for the enterprise environment.

Active Directory allows administrators to centrally manage:

- User Accounts
- Computer Accounts
- Security Groups
- Organizational Units
- Authentication
- Authorization
- Domain Resources
- Security Policies

Instead of managing every endpoint independently, the domain environment provides centralized administrative control.

---

## Enterprise Domain Configuration

The enterprise environment was configured with the following domain:

`securetech.local`

The Windows Server system was configured as:

`DC-01`

The domain controller acts as a central identity and authentication system for the enterprise lab.

### Domain Environment

| Component | Configuration |
|---|---|
| Domain Name | securetech.local |
| Domain Controller | DC-01 |
| Server IP Address | 192.168.10.10 |
| Directory Service | Active Directory Domain Services |
| Administration Tool | Active Directory Users and Computers |

The domain structure provides the foundation for centralized authentication, identity management, Group Policy, and Windows security event monitoring.

---

## Active Directory Management

Active Directory Users and Computers was accessed through Windows Server Manager administrative tools.

The management console provides centralized control over domain objects including:

- Users
- Computers
- Organizational Units
- Security Groups
- Domain Controllers
- Managed Service Accounts

This console was used to build the enterprise directory structure for SecureTech Solutions.

---

## Organizational Unit Design

Organizational Units were created to logically organize enterprise identities and systems.

The Active Directory structure included OUs for:

- Developers
- Finance
- Human Resources
- Information Technology
- Servers
- Service Accounts
- Security Operations Center
- Workstations

The OU structure was designed around enterprise departments and infrastructure roles.

This approach improves:

- User Organization
- Administrative Management
- Group Policy Targeting
- Access Control Planning
- Security Monitoring
- Incident Investigation

Department-based organization also makes it easier for SOC analysts to identify the business context of security events.

---

## Human Resources Identity Management

The Human Resources OU was used to organize HR-related user accounts and a department security group.

The implementation evidence shows HR user accounts and an HR security group inside the directory structure.

Department-based identity organization allows administrators to manage users according to their business role.

From a cybersecurity perspective, this provides a foundation for role-based access planning and centralized account monitoring.

---

## Security Operations Center Identity Structure

A dedicated SOC Organizational Unit was included in the Active Directory structure.

A SOC-related user account and security group were created to represent security operations identities inside the enterprise environment.

The SOC structure provides a foundation for:

- Security Analyst Accounts
- Security Group Membership
- Role-Based Access Planning
- SIEM Access Management
- Security Monitoring Permissions
- Investigation Account Organization

Separating security-related identities from standard enterprise users improves identity organization and administrative visibility.

---

## Active Directory User Account Management

User accounts were created and managed through Active Directory Users and Computers.

The user properties interface provides centralized identity configuration and management.

Administrators can review and configure account-related settings including:

- General User Information
- Account Settings
- Group Membership
- Profile Configuration
- Organization Information
- Session Settings

Centralized user management reduces the need to manage local accounts separately across enterprise systems.

---

## Security Group Membership

The SOC-related user account was assigned to the SOC security group.

The implementation evidence shows the account as a member of:

- Domain Users
- SOC Security Group

Security groups provide a scalable method for organizing users according to roles and access requirements.

Instead of assigning permissions individually to every user, enterprise administrators can use group-based access management.

This supports the principle of least privilege when permissions are correctly assigned according to business requirements.

---

## Identity and Access Management Security

Active Directory is a critical security component because user identities are frequently targeted during cyberattacks.

Potential identity-related threats include:

- Brute Force Attacks
- Password Spraying
- Credential Theft
- Account Compromise
- Privilege Escalation
- Unauthorized Group Membership Changes
- Suspicious Account Creation
- Lateral Movement

A centralized domain environment provides important security telemetry for detecting and investigating these activities.

---

## Active Directory from a SOC Perspective

For a SOC analyst, Active Directory is an important source of security events.

Security teams may investigate events related to:

| Security Activity | Windows Event ID |
|---|---|
| Successful Logon | 4624 |
| Failed Logon | 4625 |
| User Account Created | 4720 |
| User Account Enabled | 4722 |
| User Account Disabled | 4725 |
| User Account Deleted | 4726 |
| User Added to Security Group | 4728 / 4732 |
| User Removed from Security Group | 4729 / 4733 |
| Password Reset Attempt | 4724 |
| Account Lockout | 4740 |

These Windows security events can later be collected by a SIEM platform for centralized log analysis and threat detection.

In later phases of this project, Windows security telemetry is monitored through Wazuh SIEM.

## Security Design Considerations

The Active Directory environment was designed around the following identity security concepts:

- Centralized Identity Management
- Department-Based Organization
- Role-Based Access Planning
- Security Group Management
- Least Privilege
- Account Visibility
- Centralized Authentication
- Security Event Monitoring

The directory structure prepares the environment for future Group Policy implementation and SIEM-based identity monitoring.

---

## Skills Demonstrated

- Active Directory Domain Services
- Active Directory Users and Computers
- Windows Server Administration
- Domain Controller Management
- Enterprise Domain Configuration
- Organizational Unit Design
- User Account Management
- Security Group Management
- Group Membership Configuration
- Identity and Access Management
- Windows Security Event Awareness
- SOC Monitoring Fundamentals
- Blue Team Security

---

## Tools and Technologies

- Windows Server 2025
- Active Directory Domain Services
- Active Directory Users and Computers
- Windows Server Manager
- VMware Workstation Pro 17
- Windows Security Events
- Wazuh SIEM

---

## Key Learning Outcomes

During Day 03, I gained practical experience with Active Directory and centralized enterprise identity management.

I learned how a domain controller provides centralized authentication and how Organizational Units can be used to structure enterprise departments and infrastructure systems.

I also gained practical understanding of user account creation, security groups, and group membership management.

From a Blue Team and SOC perspective, I learned why Active Directory identities and account-related Windows events are important sources of security telemetry during threat detection and incident investigation.

---

## Project Keywords

`Active Directory` `Active Directory Domain Services` `AD DS` `Windows Server 2025` `Domain Controller` `Identity and Access Management` `IAM` `Active Directory Users and Computers` `ADUC` `Organizational Units` `OU` `Security Groups` `User Management` `Role Based Access Control` `RBAC` `Least Privilege` `SOC Analyst` `Blue Team` `Cybersecurity` `Enterprise Security` `Windows Event Logs` `SIEM` `Wazuh SIEM` `Threat Detection` `Incident Investigation` `Cybersecurity Lab` `SOC Lab` `Cybersecurity Portfolio`

---

## Next Phase

**Day 04 - DNS Configuration and Enterprise Name Resolution**

The next phase focuses on configuring and validating DNS services for the `securetech.local` enterprise domain and supporting domain-based network communication.

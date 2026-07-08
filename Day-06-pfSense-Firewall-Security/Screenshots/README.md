# Day 06 - pfSense Firewall Deployment and Network Security

## Enterprise Security Transformation Project (ESTP)

Day 06 of the Enterprise Security Transformation Project focused on deploying a dedicated pfSense firewall within the SecureTech Solutions virtual enterprise environment.

The firewall was deployed as a virtual machine and configured with separate WAN and LAN interfaces.

The internal SecureTech network was connected to the pfSense LAN interface using the `192.168.10.0/24` network.

The Domain Controller and Wazuh SIEM server were placed inside the internal network to establish a centralized and controlled network architecture.

---

## Day 06 Objectives

The main objectives of Day 06 were:

- Deploy pfSense as a virtual firewall
- Configure WAN and LAN network interfaces
- Assign a dedicated LAN gateway
- Access the pfSense WebConfigurator
- Validate the pfSense firewall dashboard
- Configure the Domain Controller network gateway
- Test connectivity between the Domain Controller and firewall
- Connect the Wazuh SIEM server to the internal network
- Build the foundation for centralized network security
- Prepare the environment for firewall rule implementation

---

## Why a Firewall Is Important

A firewall is a security control that monitors and controls network traffic based on defined security rules.

The firewall acts as a security boundary between trusted and untrusted networks.

In an enterprise environment, a firewall can be used to:

- Control inbound traffic
- Control outbound traffic
- Restrict unauthorized communication
- Segment internal networks
- Apply network security policies
- Perform Network Address Translation
- Generate firewall logs
- Support VPN connectivity
- Monitor network activity

A properly configured firewall reduces unnecessary network exposure.

---

## pfSense Firewall Deployment

pfSense Community Edition was deployed as a virtual machine inside VMware Workstation.

The firewall virtual machine provides network security and routing services for the SecureTech Solutions lab environment.

![pfSense Virtual Machine Deployment](Screenshots/Screenshot%202026-07-04%20094022.png)

The virtual deployment allows the enterprise network architecture to be tested without requiring dedicated physical firewall hardware.

This approach is commonly used in cybersecurity labs, testing environments, and security training environments.

---

## WAN and LAN Interface Configuration

The pfSense firewall was configured with two network interfaces.

| Interface | Network Role | IP Configuration |
|---|---|---|
| WAN | External Network | DHCP |
| LAN | Internal SecureTech Network | 192.168.10.1/24 |

The WAN interface received the following IPv4 address through DHCP:

`192.168.255.128/24`

The LAN interface was configured with:

`192.168.10.1/24`

![pfSense WAN and LAN Interface Configuration](Screenshots/Screenshot%202026-07-04%20094135.png)

The LAN address `192.168.10.1` acts as the gateway for systems inside the SecureTech internal network.

---

## Enterprise Network Architecture

The implemented network follows a basic firewall-controlled architecture.

`External Network`

↓

`pfSense WAN Interface`

↓

`pfSense Firewall`

↓

`pfSense LAN - 192.168.10.1`

↓

`SecureTech Internal Network - 192.168.10.0/24`

Internal systems include:

- Windows Server Domain Controller
- Active Directory Services
- DNS Server
- Windows Client Systems
- Wazuh SIEM Server

This architecture places the firewall between the internal enterprise network and the external network.

---

## pfSense WebConfigurator Access

The pfSense firewall provides a browser-based management interface called the WebConfigurator.

The management portal was successfully accessed from the internal network.

![pfSense Web Interface Login](Screenshots/Screenshot%202026-07-04%20094456.png)

The WebConfigurator provides centralized firewall administration.

Administrators can use the interface to manage:

- Network interfaces
- Firewall rules
- NAT
- VPN services
- Routing
- DHCP services
- DNS services
- System logs
- Firewall packages

Management access should only be available to authorized administrators.

---

## pfSense Firewall Dashboard

After authentication, the pfSense firewall dashboard was successfully accessed through the LAN management interface.

The firewall management address was:

`192.168.10.1`

![pfSense Firewall Dashboard](Screenshots/Screenshot%202026-07-04%20094522.png)

The dashboard provides centralized visibility into the firewall system.

The deployed firewall was running:

`pfSense 2.7.0-RELEASE (amd64)`

The dashboard provides information about:

- Firewall version
- System status
- CPU information
- Network interfaces
- Gateway status
- Installed packages
- System services

The successful dashboard access confirmed that the pfSense management interface was reachable from the internal network.

The dashboard also displayed a warning that the administrator account was using the default password.

This identified an important security hardening requirement.

The default administrator password should be replaced with a strong and unique password.

---

## Domain Controller Network Configuration

The SecureTech Domain Controller was configured with a static IPv4 address.

The network configuration included:

| Setting | Configuration |
|---|---|
| Hostname | DC-01 |
| Domain | securetech.local |
| IPv4 Address | 192.168.10.10 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 192.168.10.1 |
| DNS Server | 192.168.10.1 |

![Domain Controller Network Configuration](Screenshots/Screenshot%202026-07-04%20094724.png)

The default gateway points to the pfSense LAN interface.

This allows network traffic from the Domain Controller to be routed through the firewall.

### Active Directory DNS Design Note

The screenshot shows the Domain Controller using `192.168.10.1` as the DNS server.

For a Windows Active Directory environment, the Domain Controller should normally use the internal Active Directory DNS service for domain name resolution.

A recommended configuration is:

`Preferred DNS Server: 192.168.10.10`

External DNS resolution can then be handled through DNS forwarders.

This design helps Active Directory correctly resolve internal domain records and services.

---

## Firewall Gateway Connectivity Test

Network connectivity between the Domain Controller and the pfSense firewall was tested using the `ping` command.

The following command was executed:

`ping 192.168.10.1`

![pfSense Gateway Connectivity Test](Screenshots/Screenshot%202026-07-04%20094759.png)

The connectivity test returned:

`Packets Sent = 4`

`Packets Received = 4`

`Packets Lost = 0`

`Packet Loss = 0%`

The successful ICMP replies confirmed Layer 3 connectivity between the Domain Controller and the pfSense LAN interface.

This validated the internal network and gateway configuration.

---

## Wazuh SIEM Server Network Integration

The Wazuh SIEM server was connected to the SecureTech internal network.

The Wazuh server was running on Ubuntu Server 22.04 LTS.

The server received the following IPv4 address:

`192.168.10.12`

![Wazuh Server Network Configuration](Screenshots/Screenshot%202026-07-04%20095856.png)

The Wazuh server is positioned inside the internal enterprise network.

Its role is to provide centralized security monitoring and log analysis.

Wazuh can collect and analyze security telemetry from:

- Windows endpoints
- Domain Controllers
- Linux servers
- Security applications
- Authentication systems
- File integrity monitoring
- System logs

The network placement prepares the environment for centralized SIEM monitoring.

---

## pfSense as the Network Security Gateway

pfSense was selected as the network security gateway for the SecureTech Solutions environment.

![pfSense Firewall Platform](Screenshots/images%20%281%29.jpg)

The firewall provides a foundation for implementing network-level security controls.

Future firewall configurations can include:

- Firewall allow rules
- Firewall deny rules
- Network aliases
- Domain restrictions
- NAT configuration
- Network segmentation
- VPN access
- Firewall logging
- SIEM log forwarding

The firewall becomes an important source of security telemetry for SOC operations.

---

## Firewall Security from a SOC Perspective

SOC analysts monitor firewall activity to identify suspicious network behavior.

Important firewall events may include:

- Repeated blocked connections
- Suspicious outbound traffic
- Unauthorized inbound connections
- Port scanning activity
- Communication with malicious IP addresses
- Unusual destination ports
- Excessive connection attempts
- Network policy violations

Firewall logs provide valuable network-level security visibility.

A SOC analyst can use firewall logs to understand:

- Source IP address
- Destination IP address
- Source port
- Destination port
- Network protocol
- Firewall action
- Connection direction

This information helps during security investigations.

---

## Firewall Logs and SIEM

Firewall logs become more valuable when centralized inside a SIEM platform.

The SecureTech Solutions environment uses Wazuh for centralized security monitoring.

The planned security monitoring architecture is:

`pfSense Firewall`

↓

`Firewall Logs`

↓

`Wazuh SIEM`

↓

`Security Analysis`

↓

`SOC Analyst Investigation`

This architecture allows network security events to be analyzed together with endpoint and authentication logs.

For example, a SOC analyst may correlate:

- Multiple failed Windows login attempts
- Suspicious source IP activity
- Firewall connection attempts
- Endpoint process execution
- File integrity changes

Correlation between multiple security data sources improves threat detection and investigation.

---

## Network Security Design

The SecureTech network uses the following addressing structure:

| System | IP Address | Security Role |
|---|---|---|
| pfSense LAN | 192.168.10.1 | Firewall and Gateway |
| DC-01 | 192.168.10.10 | Domain Controller |
| Wazuh Server | 192.168.10.12 | SIEM Server |
| Internal Network | 192.168.10.0/24 | SecureTech LAN |

The firewall acts as the central gateway for the internal network.

This design creates a foundation for future network segmentation and security policy enforcement.

---

## Security Issues Identified

During the firewall deployment phase, two important security configuration issues were identified.

### Default Administrator Password

The pfSense dashboard displayed a warning indicating that the administrator password was using the default value.

Default credentials increase the risk of unauthorized administrative access.

The administrator password should be changed immediately after firewall deployment.

### Domain Controller DNS Configuration

The Domain Controller was configured to use the pfSense LAN address as its DNS server.

Active Directory environments depend heavily on internal DNS records.

The Domain Controller should normally use the Active Directory DNS service.

Recommended configuration:

`Preferred DNS Server: 192.168.10.10`

External DNS queries can be forwarded to approved upstream DNS servers.

Identifying configuration weaknesses is an important part of security implementation and validation.

---

## Principle of Network Security

The firewall implementation supports the concept of network access control.

Network traffic should only be allowed when it is required for legitimate business operations.

A secure firewall policy generally follows the principle:

`Allow Required Traffic`

and:

`Block Unnecessary Traffic`

This approach reduces the attack surface of the network.

Firewall rules should also be documented and regularly reviewed.

---

## Troubleshooting Knowledge Gained

During this phase, I gained practical experience with:

- pfSense virtual machine deployment
- Firewall interface configuration
- WAN and LAN addressing
- Internal gateway configuration
- WebConfigurator access
- Static IP configuration
- Default gateway configuration
- Network connectivity testing
- ICMP troubleshooting
- Internal server network integration

The `ipconfig /all` command was used to verify the Domain Controller network configuration.

The `ping` command was used to validate communication with the firewall gateway.

These commands are important for network troubleshooting and SOC investigations.

---

## Future Security Improvements

Future improvements for the firewall environment include:

- Change the default pfSense administrator password
- Configure the Domain Controller to use internal Active Directory DNS
- Configure DNS forwarders
- Create firewall aliases
- Implement firewall allow and deny rules
- Block unauthorized network services
- Configure firewall logging
- Forward pfSense logs to Wazuh
- Monitor firewall events inside the SIEM
- Implement VLAN-based network segmentation
- Create a dedicated SOC network
- Create a dedicated server network
- Configure VPN access
- Review firewall rules regularly

---

## Skills Demonstrated

- pfSense Firewall
- Firewall Deployment
- Network Security
- WAN Configuration
- LAN Configuration
- Static IP Addressing
- Default Gateway Configuration
- Network Routing
- Firewall Administration
- WebConfigurator
- Network Troubleshooting
- ICMP Testing
- Windows Server Networking
- Active Directory Networking
- Wazuh SIEM Integration
- Security Monitoring
- SOC Fundamentals
- Blue Team Security

---

## Tools and Technologies

- pfSense Community Edition
- VMware Workstation Pro 17
- Windows Server 2025
- Active Directory Domain Services
- Ubuntu Server 22.04 LTS
- Wazuh SIEM
- Windows PowerShell
- TCP/IP
- ICMP

---

## Key Learning Outcomes

During Day 06, I gained practical experience deploying a virtual pfSense firewall inside an enterprise security lab.

I configured separate WAN and LAN interfaces and assigned `192.168.10.1/24` to the internal firewall interface.

I configured the SecureTech Domain Controller to use the pfSense firewall as its default gateway.

I validated connectivity between the Domain Controller and the firewall using ICMP testing with zero packet loss.

I also connected the Wazuh SIEM server to the internal network using the `192.168.10.12` address.

The deployment created a centralized network security gateway and prepared the environment for firewall rule implementation, network traffic control, and SIEM-based security monitoring.

---

## Project Keywords

`pfSense` `Firewall` `Network Security` `Firewall Deployment` `WAN` `LAN` `Gateway` `Routing` `TCP/IP` `ICMP` `Network Troubleshooting` `Windows Server 2025` `Active Directory` `Domain Controller` `Ubuntu Server` `Wazuh SIEM` `SIEM` `SOC Analyst` `Blue Team` `Cybersecurity` `Enterprise Security` `VMware Workstation` `Firewall Logs` `Security Monitoring` `Threat Detection` `Network Defense` `Cybersecurity Lab` `SOC Lab` `Cybersecurity Portfolio`

---

## Next Phase

**Day 07 - pfSense Firewall Rules and Network Access Control**

The next phase focuses on implementing firewall aliases, allow and deny rules, traffic restrictions, and validating network security controls inside the SecureTech Solutions environment.

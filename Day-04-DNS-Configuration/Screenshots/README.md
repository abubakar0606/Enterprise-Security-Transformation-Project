# Day 04 - Enterprise DNS Configuration and Domain Integration

## Enterprise Security Transformation Project (ESTP)

Day 04 of the Enterprise Security Transformation Project focused on configuring and validating enterprise Domain Name System services for the SecureTech Solutions domain environment.

The DNS infrastructure was integrated with the `securetech.local` Active Directory domain to provide internal hostname resolution and support communication between domain systems.

A Windows client named `PC1` was configured with a static network configuration and the Domain Controller `DC-01` was assigned as the preferred DNS server.

The environment was then validated through DNS records, domain membership verification, domain user authentication, and hostname-based connectivity testing.

---

## Day 04 Objectives

The main objectives of Day 04 were:

- Review the Windows Server DNS management environment
- Validate the Active Directory-integrated DNS zone
- Review enterprise Forward Lookup Zones
- Verify DNS Host (A) records
- Configure the Windows client with a static IP address
- Configure the Domain Controller as the preferred DNS server
- Validate client domain membership
- Verify domain user authentication
- Test internal hostname resolution
- Confirm connectivity to the Domain Controller using DNS names

---

## Why DNS Is Important in an Enterprise Environment

The Domain Name System translates human-readable hostnames into IP addresses.

For example:

`dc-01.securetech.local`

can be resolved to:

`192.168.10.10`

Without DNS, users and systems would need to communicate using IP addresses directly.

In an Active Directory environment, DNS is especially important because domain clients use DNS to locate domain services and Domain Controllers.

DNS supports enterprise services including:

- Active Directory Domain Services
- Domain Controller Discovery
- Kerberos Authentication
- LDAP Communication
- Group Policy Processing
- Service Location
- Internal Hostname Resolution

Incorrect DNS configuration can cause domain join failures, authentication problems, and Group Policy processing issues.

---

## DNS Server Architecture

The SecureTech Solutions DNS service is hosted on the Domain Controller.

| Component | Configuration |
|---|---|
| DNS Server | DC-01 |
| DNS Server IP | 192.168.10.10 |
| Enterprise Domain | securetech.local |
| DNS Role | Windows Server DNS |
| DNS Integration | Active Directory Integrated |
| Client Hostname | PC1 |
| Client IP Address | 192.168.10.101 |
| Client Preferred DNS | 192.168.10.10 |
| Default Gateway | 192.168.10.1 |

The Domain Controller provides internal DNS resolution for domain systems.

---

## Client Static IP Configuration

The Windows client was configured with a static IPv4 configuration.

The client network settings were configured as:

| Network Setting | Value |
|---|---|
| IP Address | 192.168.10.101 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 192.168.10.1 |
| Preferred DNS Server | 192.168.10.10 |

The Domain Controller IP address was configured as the client's preferred DNS server.

This is important in an Active Directory environment because domain clients must query the internal DNS infrastructure to locate domain services.

Using an external public DNS server as the primary DNS server may prevent the client from correctly locating Active Directory services.

---

## DNS Management

Windows Server DNS was managed through the DNS Manager console.

The DNS management interface provides centralized control over:

- Forward Lookup Zones
- Reverse Lookup Zones
- DNS Records
- Conditional Forwarders
- Cached Lookups
- Trust Points

DNS Manager was accessed through the Windows Server administrative tools.

---

## Active Directory Integrated DNS

The DNS environment contains Active Directory-integrated Forward Lookup Zones.

The following zones were visible:

- `_msdcs.securetech.local`
- `securetech.local`

The `securetech.local` zone provides internal name resolution for the enterprise domain.

The `_msdcs.securetech.local` namespace supports Active Directory service discovery information used by domain systems.

This integration is important for Domain Controller discovery and Active Directory communication.

---

## Forward Lookup Zone

A Forward Lookup Zone resolves a hostname to an IP address.

Example:

`dc-01.securetech.local`

resolves to:

`192.168.10.10`

The `securetech.local` Forward Lookup Zone was reviewed through DNS Manager.

The zone contained DNS information for enterprise systems.

---

## DNS Host Records

The `securetech.local` DNS zone contained Host (A) records for enterprise systems.

The implementation evidence shows records including:

| Host | Record Type | IP Address |
|---|---|---|
| dc-01 | Host (A) | 192.168.10.10 |
| pc1 | Host (A) | 192.168.10.101 |

A Host (A) record maps an IPv4 hostname to an IPv4 address.

These records allow systems to communicate using hostnames instead of manually entering IP addresses.

For example:

`dc-01.securetech.local`

can be resolved to the Domain Controller IP address.

---

## Active Directory DNS Service Records

The `securetech.local` DNS zone also contains Active Directory-related DNS structures including:

- `_msdcs`
- `_sites`
- `_tcp`
- `_udp`
- `DomainDnsZones`
- `ForestDnsZones`

These DNS structures support Active Directory service discovery.

Domain clients use DNS service information to locate services such as Domain Controllers and authentication infrastructure.

From a troubleshooting perspective, missing or incorrect Active Directory DNS records may result in:

- Domain Join Failures
- Authentication Errors
- Group Policy Failures
- Domain Controller Discovery Problems
- LDAP Communication Issues

---

## Reverse Lookup Zone Review

The DNS Manager Reverse Lookup Zones section was reviewed during the implementation.

The visible environment contained the default reverse lookup namespaces.

A dedicated reverse lookup zone for the `192.168.10.0/24` enterprise network was not demonstrated in the current implementation evidence.

Reverse DNS can be added in a future improvement phase to provide IP-to-hostname resolution using PTR records.

Example:

`192.168.10.10`

could resolve back to:

`dc-01.securetech.local`

This would improve DNS troubleshooting and infrastructure visibility.

---

## Client Domain Integration

The Windows client `PC1` was successfully integrated with the enterprise domain.

The client system information showed the full device name:

`pc1.securetech.local`

This confirms that the workstation is associated with the `securetech.local` domain namespace.

Domain integration allows centralized management of the workstation through Active Directory.

---

## Domain User Authentication Verification

Domain user authentication was verified from the Windows client.

The following command was used:

`whoami`

The output showed:

`securetech\hamza`

This confirms that the active user session was authenticated using a SecureTech domain identity.

Domain authentication provides centralized identity control and allows security teams to monitor authentication activity across enterprise systems.

---

## Active Directory Client User Verification

The domain user account `hamza` was visible in the Finance Organizational Unit within Active Directory Users and Computers.

This demonstrates the relationship between:

- Active Directory User Identity
- Department-Based Organizational Unit
- Domain Authentication
- Domain-Joined Workstation

The client system can authenticate users managed centrally by the Domain Controller.

---

## DNS Name Resolution Testing

DNS functionality was validated using hostname-based connectivity testing.

The client executed:

`ping dc-01`

The hostname was resolved as:

`dc-01.securetech.local`

with the IP address:

`192.168.10.10`

The test successfully received four replies.

The result showed:

`Sent = 4, Received = 4, Lost = 0 (0% loss)`

This confirms successful internal hostname resolution and network communication between the Windows client and the Domain Controller.

---

## Domain Resolution Validation

Additional name resolution testing was performed against:

`securetech.local`

The domain name resolved to:

`192.168.10.10`

The connectivity test completed with:

`0% packet loss`

This provides additional evidence that the internal DNS zone was resolving correctly within the enterprise lab.

---

## DNS from a SOC Perspective

DNS is an important data source for Security Operations Center investigations.

Security analysts may investigate DNS activity related to:

- Malware Command and Control
- Suspicious Domain Queries
- Domain Generation Algorithms
- DNS Tunneling
- Internal Host Discovery
- Unauthorized DNS Changes
- Suspicious Hostname Resolution
- Compromised Endpoints

DNS activity can help analysts understand which domains or internal systems an endpoint attempted to contact.

For example, repeated queries to unusual domains may indicate malicious communication or compromised system activity.

---

## DNS Security Monitoring

Important DNS-related monitoring areas include:

| Monitoring Area | Security Purpose |
|---|---|
| DNS Queries | Identify suspicious domain requests |
| DNS Server Events | Detect DNS service problems |
| Record Changes | Identify unauthorized DNS modification |
| Failed Resolution | Detect unusual lookup behavior |
| Service Records | Validate Active Directory service discovery |
| Client DNS Settings | Detect incorrect or malicious DNS configuration |

DNS telemetry can be forwarded to a SIEM platform for centralized security analysis.

In later phases of this project, security logs and endpoint telemetry are monitored through Wazuh SIEM.

---



## Security Design Considerations

The DNS and domain environment was designed around the following enterprise security concepts:

- Centralized DNS Resolution
- Internal Domain Name Resolution
- Active Directory Integrated DNS
- Domain Controller Discovery
- Static Server Addressing
- Centralized Identity Management
- Domain-Based Authentication
- Department-Based User Organization
- Security Monitoring Readiness

Correct DNS configuration is essential for maintaining reliable Active Directory operations.

---

## Troubleshooting Knowledge Gained

During this phase, I learned that Active Directory environments depend heavily on correct DNS configuration.

If a domain client uses an incorrect DNS server, it may fail to:

- Locate the Domain Controller
- Join the Domain
- Authenticate Domain Users
- Process Group Policy
- Resolve Internal Hostnames

The preferred DNS server for the client was configured as the Domain Controller DNS server:

`192.168.10.10`

This allowed the client to resolve internal SecureTech domain resources successfully.

---

## Skills Demonstrated

- Windows Server DNS
- DNS Manager
- Active Directory Integrated DNS
- Forward Lookup Zones
- DNS Host Records
- DNS Name Resolution
- Static IPv4 Configuration
- Domain Client Configuration
- Domain Membership Verification
- Domain User Authentication
- Active Directory User Verification
- Network Connectivity Testing
- DNS Troubleshooting
- Enterprise Infrastructure
- SOC Monitoring Fundamentals
- Blue Team Security

---

## Tools and Technologies

- Windows Server 2025
- Windows DNS Server
- DNS Manager
- Active Directory Domain Services
- Active Directory Users and Computers
- Windows Client
- Command Prompt
- VMware Workstation Pro 17
- Wazuh SIEM

---

## Key Learning Outcomes

During Day 04, I gained practical experience with enterprise DNS configuration and Active Directory domain integration.

I learned how DNS supports Active Directory by allowing clients to locate internal domain services and Domain Controllers.

I configured a Windows client with a static IP address and assigned the Domain Controller as the preferred DNS server.

I also verified domain membership, domain user authentication, DNS Host records, and hostname-based connectivity.

From a SOC and Blue Team perspective, I learned why DNS activity and domain authentication are important sources of information during security monitoring and incident investigation.

---

## Project Keywords

`DNS` `Domain Name System` `Windows Server DNS` `DNS Manager` `Active Directory DNS` `Active Directory Integrated DNS` `Forward Lookup Zone` `DNS A Record` `Host Record` `Domain Controller` `DC-01` `securetech.local` `Windows Server 2025` `Active Directory` `AD DS` `Domain Authentication` `Domain Joined Workstation` `Static IP Address` `DNS Resolution` `Network Troubleshooting` `SOC Analyst` `Blue Team` `Cybersecurity` `Enterprise Security` `DNS Monitoring` `SIEM` `Wazuh SIEM` `Threat Detection` `Cybersecurity Lab` `SOC Lab` `Cybersecurity Portfolio`

---

## Next Phase

**Day 05 - Group Policy Configuration and Enterprise Security Controls**

The next phase focuses on implementing centralized Group Policy Objects to enforce enterprise security configurations across domain users and workstations.

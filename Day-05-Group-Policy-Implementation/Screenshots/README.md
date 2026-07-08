# Day 05 - Group Policy Management and Department-Based Access Control

## Enterprise Security Transformation Project (ESTP)

Day 05 of the Enterprise Security Transformation Project focused on reviewing centralized Group Policy management and validating department-based access control within the SecureTech Solutions domain environment.

The `securetech.local` Active Directory domain contains department-based Organizational Units including Developers, Finance, HR, IT, SOC, Workstation, Server, and Service Account structures.

Group Policy management paths were reviewed for security policy configuration, client-side policy processing was manually refreshed, and Resultant Set of Policy information was inspected from the domain-joined Windows client.

Department-based shared folders were also reviewed and an unauthorized access attempt against the IT department folder was denied.

---

## Day 05 Objectives

The main objectives of Day 05 were:

- Review the Group Policy Management environment
- Validate the SecureTech domain and OU structure
- Review department-level GPO linking
- Explore Group Policy security settings
- Review Password Policy configuration options
- Review Account Lockout Policy configuration options
- Force Group Policy processing on the Windows client
- Validate Group Policy processing information
- Review the enterprise shared folder structure
- Test department-based access restrictions
- Verify unauthorized folder access denial

---

## Why Group Policy Is Important

Group Policy provides centralized configuration management for Windows domain environments.

Administrators can use Group Policy Objects to manage security and operating system settings across users and computers.

Group Policy can be used to control:

- Password requirements
- Account lockout settings
- Windows security options
- Audit policies
- Firewall configuration
- Desktop settings
- Software restrictions
- Drive mappings
- User configuration
- Computer configuration

Centralized policy management reduces the need to manually configure every workstation.

---

## Group Policy Management Architecture

The Group Policy Management Console was used to review the `securetech.local` domain.

The domain structure contained multiple department-based Organizational Units.

| Organizational Unit | Business Function |
|---|---|
| Developers | Software Development |
| Finance | Financial Operations |
| HR | Human Resources |
| IT | Information Technology |
| SOC | Security Operations |
| Workstation | Client Systems |
| Server | Enterprise Servers |
| Service Account | Managed Service Identities |

This structure allows administrators to organize domain resources according to business functions.

Department-based OUs also provide a foundation for targeted Group Policy deployment.

---

## Group Policy Management Console

The Group Policy Management Console provides centralized management of Group Policy Objects.

The SecureTech domain environment showed:

`Forest: securetech.local`

and:

`Domain: securetech.local`

The management environment also included:

- Default Domain Policy
- Department Organizational Units
- Group Policy Objects
- WMI Filters
- Starter GPOs
- Group Policy Modeling
- Group Policy Results

These tools support centralized policy administration and troubleshooting.

---

## Department-Level Group Policy Review

The Finance Organizational Unit contained a policy object named:

`Finance Drive Mapp`

This demonstrates the use of department-focused policy organization within the Active Directory environment.

Department-specific policies can be used to deploy configurations only to users or computers within a selected Organizational Unit.

For example, a Finance policy may be used for:

- Finance network drive mapping
- Finance desktop configuration
- Finance application settings
- Finance security restrictions

The screenshot evidence shows the policy object within the Finance OU structure.

The current evidence does not independently demonstrate the final client-side application of this specific policy.

---

## Group Policy Security Settings

The Group Policy Management Editor was used to review security configuration paths.

The following policy path was inspected:

`Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies`

The Account Policies section contains:

- Password Policy
- Account Lockout Policy
- Kerberos Policy

These settings are important for centralized Windows security configuration.

---

## Password Policy Review

The Password Policy configuration section was reviewed.

Available security settings included:

- Enforce password history
- Maximum password age
- Minimum password age
- Minimum password length
- Minimum password length audit
- Password must meet complexity requirements
- Relax minimum password length limits
- Store passwords using reversible encryption

In the implementation evidence, the visible Password Policy settings were shown as:

`Not Defined`

Therefore, this phase documents the review of password policy configuration options rather than claiming that custom password policy values were successfully enforced.

A future hardening phase can define enterprise password requirements according to organizational security standards.

---

## Account Lockout Policy Review

The Account Lockout Policy section was also reviewed.

The available settings included:

- Account lockout duration
- Account lockout threshold
- Allow Administrator account lockout
- Reset account lockout counter after

The visible policy settings were shown as:

`Not Defined`

The screenshot therefore demonstrates the location and review of account lockout security controls.

Custom account lockout values can be implemented during a future security hardening phase.

Account lockout policies can help reduce the risk of repeated password guessing attempts against domain accounts.

---

## Group Policy Force Update

Group Policy processing was manually refreshed from the Windows client using:

`gpupdate /force`

The command successfully completed both:

`Computer Policy update has completed successfully.`

and:

`User Policy update has completed successfully.`

This confirms that the Windows client successfully completed a Group Policy refresh operation.

The command is commonly used during policy deployment and troubleshooting.

---

## Group Policy Result Validation

Group Policy processing information was reviewed using:

`gpresult /r`

The output identified the Resultant Set of Policy context for:

`SECURETECH\hamza`

on:

`PC1`

The output also showed that Group Policy information was obtained from:

`DC-01.securetech.local`

The user Distinguished Name was shown as:

`CN=hamza,OU=Finance,DC=securetech,DC=local`

This confirms that the user account is associated with the Finance Organizational Unit.

The visible User Settings section showed:

`Applied Group Policy Objects: N/A`

Therefore, the screenshot is documented as Group Policy processing and OU membership evidence rather than proof that a specific custom user GPO was applied.

---

## Enterprise Shared Folder Structure

A centralized company data structure was created under:

`C:\CompanyData`

The folder structure contained department-based directories:

- Developers
- Finance
- HR
- IT
- SOC

Department-based file organization supports enterprise data separation.

Each department can be assigned permissions according to its business responsibilities.

---

## Department-Based Access Control

The centralized company data share was accessed through the network path:

`\\dc-01\CompanyData`

The domain user attempted to access the IT department folder.

Windows returned the following message:

`You do not have permission to access \\dc-01\CompanyData\IT`

This demonstrates that the active user did not have permission to access the selected IT department directory.

The access denial provides practical evidence of department-based resource restriction.

---

## Principle of Least Privilege

The access control test demonstrates the Principle of Least Privilege.

The Principle of Least Privilege means:

> Users should only receive the minimum access required to perform their job responsibilities.

For example:

- Finance users should access Finance resources.
- HR users should access HR resources.
- Developers should access development resources.
- SOC analysts should access security monitoring resources.
- IT administrators should access authorized infrastructure resources.

Restricting unnecessary access reduces the impact of compromised user accounts.

---

## Access Control from a SOC Perspective

Unauthorized access attempts are important events for Security Operations Center analysts.

SOC analysts may investigate:

- Access denied events
- Repeated unauthorized resource access
- Privilege escalation attempts
- Suspicious file server activity
- Cross-department access attempts
- Compromised domain accounts
- Abnormal user behavior

A single denied access event may be a user mistake.

However, repeated access attempts against sensitive resources may indicate suspicious behavior.

---

## Group Policy from a SOC Perspective

Group Policy is also important for Blue Team security.

Attackers with sufficient privileges may attempt to modify Group Policy Objects to:

- Disable security controls
- Weaken Windows Defender settings
- Change firewall configuration
- Deploy malicious scripts
- Modify audit settings
- Establish persistence
- Affect multiple domain systems

Security teams should monitor important Group Policy changes and administrative activity.

---

## Security Monitoring Opportunities

The following activities are valuable for security monitoring:

| Activity | Security Value |
|---|---|
| GPO Modification | Detect unauthorized policy changes |
| Failed File Access | Identify unauthorized access attempts |
| Account Lockout | Detect password guessing activity |
| Policy Processing Failure | Identify configuration problems |
| Permission Changes | Detect privilege modification |
| Administrative Activity | Monitor privileged users |

These events can be collected and analyzed using a SIEM platform.

In later project phases, endpoint and security telemetry are centralized through Wazuh SIEM.


## Security Design Considerations

The implementation demonstrates the following enterprise security concepts:

- Centralized Policy Management
- Active Directory Organizational Units
- Department-Based Administration
- Group Policy Processing
- Identity-Based Access
- Department Data Separation
- Principle of Least Privilege
- Unauthorized Access Restriction
- Security Monitoring Readiness

These controls create a stronger foundation for enterprise security operations.

---

## Troubleshooting Knowledge Gained

During this phase, I learned how to manually refresh Group Policy using:

`gpupdate /force`

I also learned how to review policy processing information using:

`gpresult /r`

An important lesson from this implementation was that a successful Group Policy refresh does not automatically prove that a specific custom GPO was applied.

The `gpresult` output must be reviewed to identify applied policies and filtering information.

I also validated department-based folder restrictions by testing access to a resource outside the active user's department.

---

## Future Security Improvements

Future improvements for this environment include:

- Configure a defined domain password policy
- Configure an account lockout threshold
- Define account lockout duration
- Configure password complexity requirements
- Validate custom GPO application using `gpresult`
- Generate an HTML Group Policy report
- Implement Advanced Audit Policy
- Monitor GPO modification events
- Monitor failed file access events
- Configure a dedicated reverse DNS zone
- Forward security telemetry to Wazuh SIEM

---

## Skills Demonstrated

- Group Policy Management
- Group Policy Management Console
- Group Policy Management Editor
- Active Directory
- Organizational Units
- Windows Security Settings
- Password Policy Review
- Account Lockout Policy Review
- Group Policy Processing
- GPUpdate
- GPResult
- Resultant Set of Policy
- File Server Access Control
- Department-Based Permissions
- Principle of Least Privilege
- Windows Domain Administration
- SOC Monitoring Fundamentals
- Blue Team Security

---

## Tools and Technologies

- Windows Server 2025
- Active Directory Domain Services
- Group Policy Management Console
- Group Policy Management Editor
- Windows Client
- Command Prompt
- Windows File Sharing
- VMware Workstation Pro 17
- Wazuh SIEM

---

## Key Learning Outcomes

During Day 05, I gained practical experience reviewing centralized Group Policy management in a Windows Active Directory environment.

I explored Password Policy and Account Lockout Policy configuration paths and learned how security settings can be centrally managed.

I manually refreshed Group Policy processing using `gpupdate /force` and reviewed Resultant Set of Policy information using `gpresult /r`.

I also tested department-based access control by attempting to access an IT department resource using a Finance domain user context.

The unauthorized access attempt was denied, demonstrating department-based resource restriction and the Principle of Least Privilege.

From a SOC perspective, I learned why GPO changes, failed access attempts, and permission modifications are important security monitoring events.

---

## Project Keywords

`Group Policy` `GPO` `Group Policy Management` `GPMC` `Active Directory` `AD DS` `Organizational Unit` `OU` `Password Policy` `Account Lockout Policy` `GPUpdate` `GPResult` `RSOP` `Access Control` `Least Privilege` `File Server Security` `Windows Server 2025` `Windows Security` `Domain Security` `Identity and Access Management` `IAM` `SOC Analyst` `Blue Team` `Cybersecurity` `Enterprise Security` `SIEM` `Wazuh SIEM` `Security Monitoring` `Threat Detection` `Cybersecurity Lab` `SOC Lab` `Cybersecurity Portfolio`

---

## Next Phase

**Day 06 - pfSense Firewall Deployment and Network Security**

The next phase focuses on deploying the pfSense firewall and implementing network-level security controls for the SecureTech Solutions enterprise environment.

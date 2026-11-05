
# Systems as Attack Vectors – TryHackMe

## Room Information

| Detail | Information |
|---|---|
| Platform | TryHackMe |
| Learning Path | SOC Level 1 |
| Module | Blue Team Introduction |
| Room | Systems as Attack Vectors |
| Category | Blue Team / System Security |
| Difficulty | Easy |
| Room Link | https://tryhackme.com/room/systemsattackvectors |
| Status | In Progress |

---

## 1. Introduction

In cybersecurity, attackers do not always need to trick a person to gain access to an organization. They can directly target vulnerable, outdated, or incorrectly configured systems.

A system can be a physical server, virtual machine, workstation, network device, or cloud platform.

A successful attack against a critical system can expose sensitive information, interrupt business operations, or provide attackers with access to other systems.

### Learning Objectives

- Understand the role of systems in modern cybersecurity.
- Identify common attacks targeting systems.
- Understand software vulnerabilities and CVEs.
- Learn how system misconfigurations create security risks.
- Understand how SOC analysts identify and respond to system-related threats.
- Practise evaluating system risks and creating remediation plans.

---

## 2. Definition of a System

A system is a combination of hardware, software, and resources that work together to perform specific functions.

Examples include:

- Physical servers.
- Virtual machines.
- Employee workstations.
- Database servers.
- Email servers.
- Network devices.
- Cloud platforms.
- Web applications.

### Why Are Systems Important Targets?

Systems often store or process valuable organizational information.

For example:

| Target System | Possible Impact of Compromise |
|---|---|
| Email Server | Exposure of employee communications and sensitive information. |
| Database Server | Theft, modification, or deletion of business data. |
| Web Server | Website defacement or malicious content injection. |
| Domain Controller | Unauthorized access to multiple organizational accounts. |
| Cloud Platform | Exposure of cloud resources and stored information. |
| Network Firewall | Unauthorized network access or weakened security controls. |

### Can a Single System Breach Cause Serious Damage?

Yes. A compromised system can become an entry point for further attacks.

Attackers may perform lateral movement, escalate privileges, steal information, or compromise additional systems.

### Important Concept: Lateral Movement

Lateral movement is a technique in which attackers move from one compromised system to other systems within an organization.

**SOC Perspective:** Analysts should investigate whether an incident is limited to one endpoint or has spread to other systems.

---

## 3. Attacks on Systems

Attackers use different techniques to compromise systems.

The room introduces three important attack categories.

### 3.1 Human-Led Attacks

Human actions can unintentionally expose systems to attacks.

Examples:

- Connecting unknown USB devices.
- Downloading software from untrusted websites.
- Installing malicious applications.
- Reusing weak passwords.
- Opening suspicious attachments.
- Ignoring security warnings.

**Defensive Measures:**

- Employee security awareness training.
- Application control.
- Endpoint protection.
- Strong password policies.
- Restricting unauthorized USB devices.
- Monitoring suspicious user activity.

### 3.2 Vulnerability-Based Attacks

A vulnerability is a weakness or flaw in software, hardware, or system design that an attacker may exploit.

Examples:

- Outdated software.
- Unpatched operating systems.
- Insecure application code.
- Authentication weaknesses.
- Remote code execution vulnerabilities.
- Improper access controls.

Attackers search for vulnerable systems and exploit weaknesses to gain unauthorized access.

### 3.3 Supply Chain Attacks

A supply chain attack occurs when attackers compromise a trusted software provider, application, dependency, update mechanism, or other part of the software supply chain.

For example:

1. An organization installs a trusted application.
2. The application or one of its dependencies has been compromised.
3. A malicious update or component reaches the organization.
4. The malicious component executes unwanted activity.
5. The organization's systems may become compromised.

**Examples of supply chain incidents:**

- SolarWinds software supply chain compromise.
- 3CX software supply chain compromise.

**SOC Perspective:**

Analysts should investigate unexpected application behaviour, suspicious processes, unusual outbound connections, and suspicious software updates.

---

## 4. Vulnerabilities

A vulnerability is a security weakness that can be exploited to affect the confidentiality, integrity, or availability of a system.

### What is a CVE?

CVE stands for Common Vulnerabilities and Exposures.

It is a standardized identification system used to identify publicly known cybersecurity vulnerabilities.

Example format:

`CVE-YYYY-NNNNN`

Each CVE identifier refers to a specific publicly documented vulnerability.

### Why Are CVEs Important?

- Help identify known security weaknesses.
- Support vulnerability management.
- Allow security teams to track vulnerabilities.
- Help prioritize remediation activities.
- Support communication between security teams and vendors.

### CVSS

CVSS stands for Common Vulnerability Scoring System.

It provides a standardized way to assess the severity of vulnerabilities.

Security teams can use CVSS scores as one factor when prioritizing remediation.

However, a CVSS score alone should not determine priority. Exposure, exploit availability, business impact, and threat intelligence also matter.

### Real-World Example: Microsoft SharePoint ToolShell

The ToolShell vulnerability discussed in the room is associated with:

`CVE-2025-53770`

It is an example of a critical vulnerability affecting Microsoft SharePoint Server.

**SOC Perspective:**

When a critical vulnerability is identified:

1. Identify affected systems.
2. Verify the vulnerability and affected software versions.
3. Check whether the system is exposed.
4. Review relevant threat intelligence.
5. Prioritize remediation based on risk.
6. Coordinate patching with the IT team.
7. Verify that remediation was successful.
8. Continue monitoring for suspicious activity.

### How Should a SOC Analyst Respond to a Vulnerability?

A SOC analyst should identify the affected system, assess the risk, notify the responsible team, and support remediation.

Applying a vendor-provided security patch is generally the preferred response when a suitable patch is available and can be safely deployed.

---

## 5. Misconfigurations

A misconfiguration occurs when a system, application, or network device is configured incorrectly or insecurely.

Unlike a software vulnerability, a misconfiguration may result from incorrect settings, weak security policies, or improper administrative practices.

### Common System Misconfigurations

| Misconfiguration | Possible Security Risk |
|---|---|
| Default Passwords | Unauthorized access. |
| Weak Passwords | Brute-force or password-guessing attacks. |
| Unnecessary Open Ports | Increased attack surface. |
| Excessive User Permissions | Unauthorized access to sensitive resources. |
| Publicly Exposed Services | Increased exposure to external attacks. |
| Unnecessary Services | Additional attack opportunities. |
| Incorrect Firewall Rules | Unwanted network access. |
| Shared Accounts | Reduced accountability and traceability. |
| Missing Security Controls | Increased risk of compromise. |

### Vulnerability vs Misconfiguration

| Vulnerability | Misconfiguration |
|---|---|
| A weakness or flaw in software or hardware. | An insecure or incorrect system setting. |
| May require a vendor security patch. | Usually requires correcting the configuration. |
| Example: Unpatched software vulnerability. | Example: Default administrator password. |
| Tracked using CVEs when publicly disclosed. | Often identified through configuration reviews and security assessments. |

### Can a Software Patch Fix Every Misconfiguration?

No.

A software patch can fix certain software vulnerabilities, but it does not automatically correct insecure settings.

For example:

- A patch may fix a software security flaw.
- A weak password still needs to be changed.
- An unnecessary open port still needs to be restricted.
- Excessive permissions still need to be reviewed.

### Penetration Testing

Penetration testing is an authorized security assessment in which testers simulate attacks to identify security weaknesses.

It can help organizations discover:

- Insecure configurations.
- Weak authentication.
- Exposed services.
- Access control problems.
- Exploitable vulnerabilities.

**SOC Perspective:** Findings from penetration tests should be reviewed, prioritized, assigned to responsible teams, and tracked until remediation is verified.

---

## 6. Practical Challenges

This room includes two practical challenges that simulate the responsibilities of a security team.

### 6.1 Systems at Risk

The objective is to examine security alerts and choose suitable remediation actions for affected systems.

The scenarios involve:

- An exposed Exchange mail server affected by a vulnerability.
- A WordPress administrator account compromised through brute-force activity.
- Potential risks affecting corporate Cisco firewall devices.
- Suspicious behaviour from a trusted application following an update.

### Investigation and Remediation Approach

| Situation | Security Response |
|---|---|
| Vulnerable Exchange Server | Coordinate immediate patching and verify the update. |
| WordPress Admin Brute Force | Secure the administrator account with a strong unique password and review access activity. |
| Vulnerable Firewall | Audit affected devices and apply appropriate security patches. |
| Suspicious Application Update | Investigate possible supply chain compromise and contain affected software or endpoints. |

### Key Learning

A SOC analyst must understand the root cause of an incident before recommending remediation.

Choosing a temporary workaround without addressing the actual weakness may leave the organization exposed.

**My Challenge Result:**

- Systems at Risk: [Add your result]
- Challenge Flag: [Add your own result if appropriate]

### 6.2 Remediation Plan

The second challenge focuses on selecting security policies and controls that improve system security.

Important recommendations include:

| Security Control | Why It Is Important |
|---|---|
| Patch Management Policy | Ensures vulnerabilities are identified and patched systematically. |
| Antivirus Protection | Helps detect and prevent malicious software. |
| Secure Password Policy | Reduces the risk of password-based attacks. |
| Security Training for IT | Helps administrators avoid common security mistakes. |
| Individual User Accounts | Improves accountability and activity tracking. |
| Configuration Reviews | Helps identify insecure system settings. |

### Important Security Principles

- Avoid shared administrator accounts.
- Use strong, unique passwords.
- Keep critical systems updated.
- Install endpoint protection.
- Review system configurations regularly.
- Train IT staff on secure administration.
- Monitor systems for suspicious behaviour.

**My Challenge Result:**

- Remediation Plan: [Add your result]
- Challenge Flag: [Add your own result if appropriate]

---

## 7. SOC Analyst Responsibilities

A SOC analyst plays an important role in identifying and responding to system-related threats.

### Important Responsibilities

1. Monitor security alerts.
2. Identify vulnerable and exposed systems.
3. Review system and endpoint logs.
4. Investigate suspicious processes.
5. Analyse unusual network activity.
6. Correlate events from different security sources.
7. Escalate critical findings.
8. Coordinate with IT teams for remediation.
9. Verify that security issues have been resolved.
10. Document incidents and investigation findings.

### Example SOC Investigation

**Scenario:** A server generates an alert indicating suspicious activity after a software update.

A SOC analyst may:

1. Identify the affected server.
2. Review the software update history.
3. Examine process execution logs.
4. Check for unusual child processes.
5. Investigate network connections.
6. Determine whether the update or its dependency is compromised.
7. Isolate the affected system if necessary and authorized.
8. Escalate the incident to the appropriate team.
9. Document the investigation.

---

## 8. Important Technical Terms

| Term | Meaning |
|---|---|
| System | Hardware, software, and resources working together. |
| Vulnerability | A weakness that may be exploited. |
| CVE | Common Vulnerabilities and Exposures. |
| CVSS | Common Vulnerability Scoring System. |
| Misconfiguration | An incorrect or insecure system setting. |
| Supply Chain Attack | An attack that compromises a trusted supplier, application, or dependency. |
| Lateral Movement | Moving between compromised systems. |
| Patch Management | The process of identifying, testing, and applying updates. |
| Penetration Testing | Authorized security testing to identify weaknesses. |
| Attack Surface | The points where an attacker may attempt to access a system. |
| Remediation | Actions taken to fix or reduce a security issue. |
| Endpoint | A device connected to a network. |

---

## 9. What I Learned

After studying this room, I understood:

- Why systems are valuable targets for attackers.
- How attackers compromise systems without direct user interaction.
- The difference between human-led attacks, vulnerability exploitation, and supply chain attacks.
- What CVEs and CVSS mean.
- Why outdated software creates security risks.
- The difference between vulnerabilities and misconfigurations.
- Why software patches cannot fix every configuration problem.
- How penetration testing helps identify security weaknesses.
- How SOC analysts support system remediation and incident response.

---

## 10. Practical Takeaways

The most important lesson from this room is that protecting people alone is not enough. Organizations must also secure the systems that store, process, and transmit their data.

A strong defensive security strategy should include:

- Regular vulnerability assessments.
- Timely patch management.
- Secure system configurations.
- Strong authentication and access controls.
- Endpoint protection.
- Network monitoring.
- Security awareness and IT training.
- Continuous verification of remediation.

---

## 11. Room Completion Checklist

- [x] Complete Task 1 – Introduction.
- [x] Complete Task 2 – Definition of System.
- [x] Complete Task 3 – Attacks on Systems.
- [x] Complete Task 4 – Vulnerabilities.
- [x] Complete Task 5 – Misconfigurations.
- [x] Complete Task 6 – Practice.
- [x] Complete Task 7 – Conclusion.
- [x] Review the technical concepts.
- [x] Complete this documentation.

---

## References

- TryHackMe – Systems as Attack Vectors: https://tryhackme.com/room/systemsattackvectors
- MITRE CVE: https://www.cve.org/
- NIST National Vulnerability Database: https://nvd.nist.gov/
- FIRST CVSS: https://www.first.org/cvss/
- CISA Known Exploited Vulnerabilities Catalog: https://www.cisa.gov/known-exploited-vulnerabilities-catalog

**Disclaimer:** These are personal educational notes based on my TryHackMe learning. They are not an official TryHackMe walkthrough.


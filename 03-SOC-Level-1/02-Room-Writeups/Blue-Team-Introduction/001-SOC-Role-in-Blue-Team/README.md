# 🛡️ SOC Role in Blue Team

> Understanding the role of security teams, SOC operations, security hierarchy and career progression in cybersecurity.

## 1. Room Information

| Field | Details |
|---|---|
| Platform | TryHackMe |
| Learning Path | SOC Level 1 |
| Room Name | SOC Role in Blue Team |
| Room URL | https://tryhackme.com/room/socroleinblueteam |
| Category | Blue Team / SOC Fundamentals |
| Difficulty | Introductory concepts |
| Status | Studied — update completion status |
| Documentation | Created as part of my SOC Level 1 learning journey |

---
## 2. Learning Objectives

The main objectives of this room were to understand:

- What a Blue Team is and why it is important.

- How cybersecurity teams are organised inside an organisation.

- The responsibilities of a Chief Information Security Officer (CISO).

- The different departments involved in cybersecurity.

- The. Responsibilities within a Security Operations Centre (SOC).

- How a Cyber Incident Response Team (CIRT) supports security operations.

- The difference between a SOC and a Managed Security Service Provider (MSSP).

- Career progression opportunities after starting as a SOC Level 1 analyst.

---

## 3.  Introduction

Cybersecurity is not handled by a person or department in a large organisation. Different teams work together to protect the organisations systems, networks, applications and information.

These teams have responsibilities. Some focus on identifying weaknesses some manage security policies and others monitor systems and respond to attacks.

One of the important defensive security teams is the **Blue Team**.

The Blue Team focuses on protecting an organisation against cyber threats. It monitors systems investigates activity, detects attacks and helps respond to security incidents.

A Security Operations Centre (SOC) is one of the operational areas within the Blue Team.

As someone learning SOC Level 1 understanding how these teams work together is important because a SOC analyst does not work independently. Analysts coordinate with security teams IT departments, engineers and incident responders.

---

# 4. Task 1.

## 4.1 What is a Blue Team?

A **Blue Team** is a group of cybersecurity professionals for defending an organisations IT infrastructure against cyber threats.

Its main responsibility is to prevent, detect, investigate and respond to activities.

### Main responsibilities

1. Monitor networks, endpoints and systems.

2. Identify activities.

3. Investigate security alerts.

4. Detect attacks and security weaknesses.

5. Respond to security incidents.

6. Improve security monitoring and detection.

7. Help protect organisational information.

### Example

Imagine an employee receives a phishing email containing an attachment.

The Blue Team may:

1. Detect email activity.

2. Analyse the email and its attachment.

3. Check whether the employee opened the attachment.

4. Investigate endpoint and network logs.

5. Determine whether the system was compromised.

6. Coordinate containment and recovery activities.

7. Improve detection rules to identify attacks in the future.

This example demonstrates how defensive security teams help reduce the impact of cyber attacks.

## 4.2 Blue Team vs Red Team

Both teams are important in cybersecurity. Their objectives are different.

| Area | Blue Team | Red Team |
|---|---|---|
| Main focus | Defensive security | Offensive security |
| Objective | Protect systems | Test security by simulating attacks |
| Activities | Monitoring, detection, investigation, response | Penetration testing, attack simulation |
| Main question | How can we detect and stop attacks? | How can an attacker exploit the environment? |
| Example | Investigating suspicious login activity | Testing whether authentication can be bypassed |

### Purple Team

A Purple Team approach encourages collaboration, between Red Team and Blue Team members.

The Red Team demonstrates attack techniques while the Blue Team uses that information to improve monitoring, detection and response.

**Important:** Purple Teaming is generally a security approach, not necessarily a separate permanent department.

---

# 5. Task 2. Security Hierarchy

## 5.1 What is a Security Hierarchy?

A security hierarchy describes how cybersecurity responsibilities and decision-making authority are organised within an organisation.

In an organisation security analysts usually work within a department that reports to security leadership.

A simplified reporting structure can look like this:

```text
                 CEO
                  |
                 CISO
                  |
        Information Security
             Management
                  |
       +----------+----------+
       |          |          |
    Blue Team   Red Team   GRC Team
       |
      SOC
       |
  +----+----------------+
  |         |           |
 L1        L2       SOC Engineers
Analysts  Analysts
       |
   SOC Manager
```

*Note: This is a simplified conceptual diagram. Actual reporting structures differ between organisations.*

## 5.2 CEO. Chief Executive Officer

The CEO is the highest-level executive for the overall direction and performance of an organisation.

In cybersecurity the CEO generally focuses on business priorities risk and major decisions rather than directly investigating technical security alerts.

### Responsibilities

- Set overall business direction.

- Approve organisational priorities.

- Understand business risks.

- Work with leadership on important security decisions.

## 5.3 CISO. Chief Information Security Officer

The CISO is a security leader responsible for an organisations overall information security strategy and programme.

The CISO connects security activities with business objectives.

### Responsibilities

- Develop and oversee security strategy.

- Establish security policies and priorities.

- Manage information security risks.

- Oversee security. Programmes.

- Report major security risks to executive leadership.

- Support compliance and governance requirements.

- Coordinate high-level security decisions during major incidents.

### Example

If an organisation experiences a ransomware incident the CISO may coordinate the overall security response communicate risks to senior management and help determine organisational priorities.

The technical investigation itself is usually handled by teams and incident responders.

## 5.4 Major Security Departments

Large organisations may divide cybersecurity responsibilities among departments.

### A. Blue Team

Focuses on security.

Typical responsibilities:

- Security monitoring.

- Threat detection.

- Alert investigation.

- Incident response.

- Security control improvement.

### B. Red Team

Focuses on simulating attacks to evaluate an organisations security.

Typical responsibilities:

- Simulating attacker behaviour.

- Identifying exploitable weaknesses.

- Testing security controls.

- Evaluating detection and response capabilities.

- Providing recommendations to improve security.

Red Team activities must be. Performed within an agreed scope.

### C. GRC Team

GRC stands for:

- Governance

- Risk

- Compliance

The GRC team helps an organisation manage security policies, risks, standards and regulatory requirements.

Typical responsibilities:

- Developing and maintaining security policies.

- Assessing risks.

- Supporting security audits.

- Tracking compliance requirements.

- Maintaining security documentation.

- Helping ensure that security controls meet standards.

### Example

A company that processes payment card information may need to consider PCI DSS requirements.

The GRC team helps the organisation understand and manage its compliance responsibilities.

---

# 6. Task 3. Meet the Blue Team

The Blue Team may contain specialised teams and job roles.

The exact structure depends on the organisations size, industry and security requirements.

## 6.1 SOC. Security Operations Centre

A **Security Operations Centre (SOC)** is a function responsible for monitoring, detecting, analysing and responding to security-related activities across an organisation.

The SOC acts as an operational defence layer.

### Main SOC responsibilities

1. Monitor security events from systems.

2. Collect and analyse security logs.

3. Investigate alerts generated by security tools.

4. Identify behaviour.

5. Escalate incidents when necessary.

6. Coordinate, with IT and other security teams.

7. Improve detection and monitoring capabilities.

### Example SOC workflow

```text
     Security Events
            |
            v
       SIEM / Tools
            |
            v
       Alert Created
            |
            v
      SOC L1 Analyst
            |
            v
       Alert Triage
            |
       +----+----+
       |         |
       v         v
  False Positive  Suspicious
       |              |
       v              v
  Document and     Escalate
      Close         to L2
                       |
                       v
                Further Investigation
                       |
                       v
                 Incident Response

```

This is a simplified workflow. Actual procedures depend on the organisations tools, escalation rules and incident response process.

## 6.2 SOC Level 1 Analyst

A SOC L1 analyst is generally an entry‑level security operations professional.

The main responsibility is alert triage and identifying which alerts require further investigation.

### Responsibilities

- Monitor security alerts.

- Review information from SIEM and other security tools.

- Identify activity.

- Perform initial investigation.

- Check relevant logs and event details.

- Distinguish potential false positives from events.

- Record investigation findings.

- Escalate complex or confirmed suspicious cases to the appropriate team.

### Example

A SIEM generates an alert indicating failed login attempts against an employee account.

A SOC L1 analyst may:

1. Review the details.

2. Identify the account.

3. Check the source IP address.

4. Review the timestamps and number of attempts.

5. Examine related authentication logs.

6. Check whether a successful login occurred afterwards.

7. Document the findings.

8. Escalate the alert if the activity appears malicious.

The analyst should not assume that every failed login is an attack. Context and supporting evidence are important.

## 6.3 SOC Level 2 Analyst

A SOC L2 analyst generally handles complex investigations and cases escalated by L1 analysts.

### Responsibilities

- Investigate security alerts.

- Analyse multiple sources of evidence.

- Correlate events across systems.

- Investigate processes and network activity.

- Identify the scope and impact of incidents.

- Support containment and remediation.

- Provide guidance to junior analysts.

- Recommend improvements to detection rules.

### Example

If an L1 analyst identifies a login followed by unusual PowerShell activity the L2 analyst may correlate authentication events, endpoint telemetry, process information and network connections to understand what happened.

## 6.4 SOC Engineers

SOC engineers are responsible for implementing, maintaining and improving the systems used by security operations teams.

### Responsibilities

- Configure SIEM platforms.

- Integrate log sources.

- Maintain security monitoring infrastructure.

-. Improve detection rules.

- Maintain security tool configurations.

- Troubleshoot monitoring and data collection problems.

- Improve automation and alerting processes.

### Examples of technologies

- SIEM platforms

- Endpoint Detection and Response (EDR)

- Security log management systems

- Security monitoring infrastructure

A SOC engineer helps ensure that analysts receive reliable security data.

## 6.5 SOC Manager

A SOC manager oversees the operation and performance of the SOC team.

### Responsibilities

- Manage SOC analysts and engineers.

- Coordinate shift operations.

- Establish procedures.

- Monitor team performance.

- Manage escalation processes.

- Coordinate, with other departments.

- Report SOC activities and important incidents to leadership.

---

## 6.6 CIRT. Cyber Incident Response Team

CIRT stands for **Cyber Incident Response Team**.

It is a team that handles significant cybersecurity incidents and supports the organisation during security breaches.

Other used names include:

- CSIRT. Computer Security Incident Response Team

- CERT. Computer Emergency Response Team

The exact naming and responsibilities vary between organisations.

### When is CIRT required?

A SOC may identify an incident that requires investigation, specialist expertise or coordinated response.

For example:

- A ransomware infection affecting systems.

- A major data breach.

- A widespread malware infection.

- A suspected compromise of infrastructure.

- A serious security incident affecting business operations.

The SOC may escalate the incident to the incident response team according to the organisations procedures.

### Common CIRT responsibilities

- Coordinate incident response.

- Investigate security breaches.

- Analyse malware and attacker activity.

- Support containment and recovery.

- Perform forensic investigations.

- Identify the scope and impact of incidents.

- Recommend security improvements.

### Important distinction

The SOC and CIRT work together. Their focus can differ.

| SOC | CIRT |
|---|---|
| Continuous security monitoring | Specialist incident response |
| Alert triage | Deeper incident investigation |
| Initial investigation | Incident coordination and response |
| Detection and escalation | Containment, eradication, and recovery support |
| Daily operational security | Handling significant incidents |

A SOC can be involved throughout an incident. CIRT does not necessarily replace the SOC; the teams often collaborate.

---

## 6.7 Specialised Defensive Security Roles

As organisations grow they may introduce cybersecurity positions.

### A. Digital Forensics Analyst

Investigates evidence to understand what happened during a security incident.

Typical activities:

- Analyse disk images.

- Examine memory captures.

- Review system artefacts.

- Build event timelines.

- Identify evidence of activity.

### B. Threat Intelligence Analyst

Analyses information about cyber threats to help an organisation understand potential attackers and their techniques.

Typical activities:

- Research threat groups.

- Analyse indicators of compromise (IOCs).

- Monitor emerging threats.

- Study attacker techniques.

- Share actionable threat intelligence.

### C. Application Security Engineer

Focuses on identifying and reducing security weaknesses in applications and software development processes.

Typical activities:

- Review application security.

- Identify software vulnerabilities.

- Support development practices.

- Perform security testing.

- Help developers fix security issues.

### D. AI Security Researcher

Studies security risks related to intelligence systems and develops methods to protect them.

Potential focus areas:

- AI model security.

- Prompt injection risks.

- Data protection.

- machine learning.

- AI system abuse and misuse.

---

# 7. Task 4. Advancing a SOC Career

Starting as a SOC L1 analyst can provide a foundation for cybersecurity career paths.

A SOC role helps develop knowledge of security events infrastructure, threats, monitoring tools and incident investigation.

## 7.1 A Typical SOC Career Path

```text
       SOC L1 Analyst
              |
              v
       SOC L2 Analyst
              |
              v
       SOC L3 Analyst
              |
       +------+-------+
       |              |
       v              v
  Threat Hunter   Incident Responder
       |              |
       v              v
 Threat Intel    DFIR Specialist
       Analyst
```

Other possible career paths include:

- SOC Engineering

- Detection Engineering

- Security Architecture

- Threat Intelligence

- Digital Forensics

- Security Management

**Note:** This is an example of progression, not a mandatory career ladder. People can move into specialisations depending on their interests, experience and opportunities.

## 7.2 Skills to Develop as a SOC L1 Analyst

### Technical skills

- Networking fundamentals.

- TCP/IP and common network protocols.

- Linux and Windows fundamentals.

- Windows Event Logs.

- Linux system logs.

- SIEM platforms.

- Log analysis.

- Basic scripting.

- Security alert investigation.

- Understanding attack techniques.

### Analytical skills

- Critical thinking.

- Attention to detail.

- Evidence-based investigation.

- Pattern recognition.

- Problem-solving.

- Understanding timelines and event relationships.

### Communication skills

- Writing incident reports.

- Documenting investigation steps.

- Explaining findings.

- Escalating issues accurately.

- Communicating with teams.

## 7.3 Internal SOC vs MSSP

An organisation can operate its SOC or outsource SOC services to a specialised provider.

### What is a SOC?

An internal SOC is operated by the organisation itself.

Example:

A bank operates its SOC to monitor and protect its internal systems, employee accounts, servers and network infrastructure.

### What is an MSSP?

MSSP stands for **Managed Security Services Provider**.

An MSSP is a company that provides security services to other organisations.

These services may include:

- SOC monitoring.

- SIEM management.

- Security alert investigation.

- Threat detection.

- Incident response support.

An MSSP may provide SOC services to customers.

### Internal SOC, vs MSSP comparison

| Area | Internal SOC | MSSP |
|---|---|---|
| Organisation | Works for one organisation | Works for a service provider |
| Customers | Protects its own organisation | Supports multiple client organisations |
| Environment | Usually focuses on one organisation's environment | May handle different client environments |
| Tools | Uses tools selected for its environment | May work with different client tools and platforms |
| Workload | Depends on internal operations and incident volume | May involve multiple customer alert queues |
| Exposure | Develops deep knowledge of one organisation | Can gain exposure to different environments |


### Which is better for a beginner?

There is no answer.

An internal SOC may provide understanding of one organisations environment.

An MSSP may provide exposure to customers, environments and security tools.

Both can offer entry‑level experience. The actual learning opportunity depends on the employer, training, team structure and workload.

## 7.4 Tips for Developing as a SOC Analyst

1. Learn from every alert you investigate.

2. Understand how attackers operate.

3. Verify evidence before reaching conclusions.

4. Practise analysing logs and security events.

5. Improve technical documentation skills.

6. Learn how different security tools work together.

7. Participate in authorised labs.

8. Develop communication and investigation skills.

## 7.5 Possible Career Certifications

Certifications can help demonstrate knowledge. They should support practical skills rather than replace them.

Examples of certifications and learning options to research include:

- CompTIA Security+

- CompTIA CySA+

- Blue Team Level 1 (BTL1)

- TryHackMe SOC Level 1 learning path

Before pursuing a certification check its syllabus, prerequisites, examination format and cost.

---

# 8. Task 5. Final Challenge

## 8.1 Challenge Overview

The final challenge places the learner in a CISO role at a fictional organisation called TrySecureMe.

The scenario involves security incidents occurring at the same time.

The objective is to understand the responsibilities of cybersecurity roles and assign suitable specialists to the incidents.

The exercise uses a drag‑and‑drop interface to match security roles with incident scenarios.

## 8.2 What This Challenge Teaches

The challenge reinforces the importance of understanding:

- Which team handles security.

- Which team investigates security incidents.

- Which specialists investigate evidence.

- Which roles manage security policies and compliance.

- Which roles focus on application security.

- How different departments contribute to security.

## 8.3 My Practical Challenge Notes

**Challenge completed:** [Update Yes / No]

**My observations:**

- Security incidents may require specialist teams.

- Not every security issue should be handled by the department.

- The right team should be selected based on the nature of the incident.

- Security leadership is responsible for coordinating security priorities.

**My challenge result:**

[Write a summary of your actual result here.]

**Evidence:**

[Add a screenshot of the completed challenge if available. Remove flags and any sensitive information.]

---

# 9. Task 6.

This room introduced the structure of defensive cybersecurity teams and explained how SOC operations fit into a wider security programme.

The important concepts I learned were:

1. Blue Team focuses on security.

2. The CISO provides senior‑level information security leadership.

3. The SOC is responsible for security monitoring and alert investigation.

4. SOC L1 analysts perform alert triage.

5. SOC L2 analysts handle complex investigations.

6. SOC engineers. Improve security monitoring tools.

7. CIRT supports security incident investigations and response.

8. GRC teams manage governance, risk and compliance responsibilities.

9. MSSPs provide managed security services to organisations.

10. A SOC L1 role can lead to specialised cybersecurity career paths.

This room helped me understand that becoming a SOC analyst is not about learning security tools. It is also about understanding the people, teams, responsibilities and processes involved in protecting an organisation.

---

# 10. Real‑World SOC Application

The concepts, from this room can be applied to a security incident.

### Scenario: Suspicious Account Activity

Imagine a company detects failed login attempts followed by an unexpected successful login.

A possible response workflow:

| Stage | Team / Role | Responsibility |
|---|---|---|
| 1 | SIEM / Monitoring tools | Generate an alert from authentication events |
| 2 | SOC L1 | Review and triage the alert |
| 3 | SOC L2 | Perform deeper investigation if suspicious |
| 4 | Incident Response Team | Coordinate response if an incident is confirmed or requires specialist handling |
| 5 | IT Team | Support account or system remediation |
| 6 | SOC Engineers | Improve monitoring and detection rules |
| 7 | Security Leadership | Oversee major organisational risk and response decisions |


This is an illustrative workflow. Actual responsibilities depend on the organisations incident response plan.


### Why this matters

Understanding team responsibilities helps a SOC analyst:

- Know when to elevate an alert.

- Avoid handling incidents outside their authority.

- Communicate findings to the team.

- Support an organised incident response process.

- Understand how individual investigations contribute to security.

---

# 11. Important Terminology

Term | Full Form | Explanation |
|---|---|---|
| Blue Team |. | Defensive cybersecurity team |
| Red Team |. | Team that simulates attacks to test security |
| Purple Team |. | Collaborative approach between Red and Blue Teams
| SOC | Security Operations Centre | Function responsible for security monitoring and investigation |
| CISO | Chief Information Security Officer | Senior information security leader |
| CIRT | Cyber Incident Response Team | Team supporting incident response |
| CSIRT | Computer Security Incident Response Team | Another common incident response team name |
| CERT | Computer Emergency Response Team | Incident response organisation or team name
| GRC | Governance, Risk and Compliance | Security governance and risk management function |
| MSSP | Managed Security Services Provider | External provider delivering managed security services |
| SIEM | Security Information and Event Management | Platform for collecting and analysing security events |
| EDR | Endpoint Detection and Response | Technology for endpoint monitoring and investigation |
| IOC | Indicator of Compromise | Evidence that may indicate malicious activity |
| DFIR | Digital Forensics and Incident Response | Investigation and response involving digital evidence |

---

# 12. Interview Preparation

## Q1. What is a Blue Team?

**Answer:** A Blue Team is a cybersecurity team responsible for protecting an organisations systems, networks and data by monitoring, detecting, investigating and responding to cyber threats.

## Q2. What is a SOC?

**Answer:** A Security Operations Centre is a security function that continuously monitors an organisations environment investigates alerts, detects activity and coordinates security responses.

## Q3. What is the role of a SOC L1 analyst?

**Answer:** A SOC L1 analyst performs alert triage reviews security events identifies suspicious activity documents findings and escalates complex cases to higher-level analysts or other teams.

## Q4. What is the difference between SOC L1 and SOC L2?

**Answer:** SOC L1 generally handles alert triage and basic investigations while SOC L2 performs deeper investigations into complex or escalated security events.

## Q5. What is a CISO?

**Answer:** A Chief Information Security Officer is an executive responsible for an organisations information security strategy, risk management and security programme.

## Q6. What is the difference between Blue Team and Red Team?

**Answer:** The Blue Team focuses on defending systems and detecting attacks whereas the Red Team simulates attacks to identify weaknesses and evaluate security controls.

## Q7. What is CIRT?

**Answer:** A Cyber Incident Response Team is a team that helps investigate, coordinate and respond to significant cybersecurity incidents.

## Q8. What is an MSSP?

**Answer:** A Managed Security Services Provider is a company that delivers security services, such as SOC monitoring and security alert investigation to other organisations.

## Q9. What is the difference between a SOC and an MSSP?

**Answer:** An internal SOC protects the organisation that operates it while an MSSP provides managed security services to customers.

## Q10. What is the role of a SOC engineer?

**Answer:** A SOC engineer configures maintains and improves security monitoring technologies such, as SIEM and EDR platforms, log integrations and detection rules.

## Q11. What is GRC?

**Answer:** GRC means Governance, Risk and Compliance. GRC helps organisations manage security policies, risks, audits and regulatory requirements.

## Q12. What can be the career step after SOC L1?

**Answer:** A common next step is SOC L2 analyst. Other possible paths include incident response, threat hunting, threat intelligence and security engineering.

---

# 13. Key Takeaways

After studying this room I understand that:

- Defensive security involves teams working together.

- SOC analysts are an important part of the Blue Team.

- L1 analysts are responsible for initial alert triage.

- L2 analysts investigate more complex security events.

- SOC engineers maintain the technical monitoring infrastructure.

- Incident response teams provide support during significant incidents.

- The CISO oversees the information security programme.

- SOC career progression can lead to several cybersecurity specialisations.

**My biggest takeaway:** A SOC analyst must understand not how to identify suspicious activity but also how to investigate it document it and communicate it to the right security team.

---

# 14.. Further Learning

### Primary Learning Resource

- [TryHackMe. SOC Role, in Blue Team](https://tryhackme.com/room/socroleinblueteam)

### Related TryHackMe Rooms

- [Junior Security Analyst Intro](https://tryhackme.com/room/jrsecanalyst)

- [SOC Roles and Processes](https://tryhackme.com/room/socroleandprocesses)

### Additional Reference

- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)

---

## Disclaimer

This write‑up is created for professional development purposes.

The explanations are written in my words based on my learning and understanding. TryHackMe is the learning platform used for this room.

No flags, credentials or sensitive challenge information are included in this documentation.


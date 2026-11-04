
# Humans as Attack Vectors – TryHackMe

## Room Information

| Detail | Information |
|---|---|
| Platform | TryHackMe |
| Learning Path | SOC Level 1 |
| Room | Humans as Attack Vectors |
| Category | Blue Team / SOC |
| Room Link | https://tryhackme.com/room/humansattackvectors |
| Status | Completed / In Progress |

## 1. Introduction

Cybersecurity is not only about protecting computers, networks, and servers. Humans can also become targets of cyberattacks.

Attackers often manipulate people into revealing sensitive information, clicking malicious links, downloading malware, or providing unauthorized access.

This room explains how attackers exploit human behaviour and how SOC analysts detect and defend against these attacks.

### Learning Objectives

- Understand why humans are targeted by attackers.
- Learn common social engineering techniques.
- Understand how attackers use impersonation.
- Learn mitigation and detection techniques.
- Practise making security decisions as a SOC analyst.

## 2. The Human Element

Humans are often considered one of the weakest links in cybersecurity.

Even when an organization has strong technical security controls, an employee can unintentionally give an attacker access.

### Why Do Attackers Target Humans?

Attackers may target employees to obtain:

- Usernames and passwords.
- Corporate email access.
- Financial information.
- Sensitive company documents.
- Access to internal networks.
- Administrative privileges.

### Important Concept: Access

The main objective of many human-targeted attacks is to obtain unauthorized access to accounts, systems, or sensitive information.

## 3. Attacks on Humans

Social engineering is a technique in which attackers manipulate people into performing actions that benefit the attacker.

Instead of directly attacking a technical vulnerability, attackers exploit human trust, fear, curiosity, or urgency.

### Common Social Engineering Techniques

| Technique | Explanation |
|---|---|
| Phishing | Fraudulent emails designed to steal information or deliver malware. |
| Spear Phishing | Targeted phishing aimed at a specific individual or organization. |
| Vishing | Social engineering through voice calls. |
| Smishing | Social engineering through SMS messages. |
| Impersonation | Pretending to be a trusted person or organization. |
| Deepfake | AI-generated audio or video used to imitate someone. |

### Impersonation

Attackers may pretend to be:

- Company executives.
- IT support employees.
- Bank representatives.
- Trusted business partners.

For example, an attacker may pretend to be an IT support employee and request an employee's password.

### Deepfake Attacks

Deepfake technology can generate convincing fake audio or video.

An attacker may imitate a CEO's voice or appearance to convince an employee to transfer money or reveal confidential information.

**SOC perspective:** Never trust a request only because it appears to come from a familiar person. Verify it using an independent communication channel.

## 4. Defending Humans

Organizations need both mitigation and detection to protect employees.

### Mitigation

Mitigation means preventing or reducing the likelihood and impact of an attack.

Examples:

- Security awareness training.
- Anti-phishing solutions.
- Strong access management.
- Multi-factor authentication (MFA).
- Employee verification procedures.
- Endpoint protection.

### Detection

Detection means identifying suspicious activity that may indicate an attack.

SOC analysts should monitor:

- Suspicious login attempts.
- Unusual login locations.
- Unexpected password reset requests.
- Suspicious email attachments.
- Malicious URLs.
- Unusual account activity.

### Security Awareness Training

Employees should learn how to:

- Identify suspicious emails.
- Verify unexpected requests.
- Avoid clicking unknown links.
- Report suspicious messages.
- Protect their login credentials.

## 5. Practical SOC Investigation

This room includes practical scenarios where a SOC analyst must evaluate suspicious employee activity and recommend appropriate defensive actions.

### Scenario 1: Suspicious Email

**Situation:** An employee receives an unexpected email containing an unusual payment request and a suspicious attachment.

**SOC Investigation:**

1. Examine the sender's email address.
2. Check the sender domain.
3. Inspect the email content.
4. Analyse suspicious URLs and attachments safely.
5. Determine whether the message is phishing.
6. Block or report the malicious message according to organizational procedures.

**Key Learning:** Never trust an email simply because it looks professional or urgent.

### Scenario 2: Suspicious Password Reset Request

**Situation:** Someone claims to be the CEO and requests an urgent password reset through an unusual phone call.

**SOC Investigation:**

1. Verify the caller's identity through an independent channel.
2. Review the account's recent activity.
3. Check whether the request follows company procedures.
4. Escalate suspicious activity.
5. Temporarily restrict account access if there is a credible risk and policy permits it.

**Key Learning:** High-level employees must follow the same identity verification procedures as everyone else.

### Scenario 3: Anomalous Login Location

**Situation:** An employee account logs in from an unusual location after visiting a suspicious website.

**SOC Investigation:**

1. Review the login location and timestamp.
2. Compare the login with the employee's normal activity.
3. Investigate recently visited URLs.
4. Check for possible credential theft.
5. Contact the employee through a trusted channel.
6. Contain the account if compromise is suspected.

**Key Learning:** Unusual login activity combined with suspicious URLs can indicate account compromise.

## 6. Security Policies

Organizations should implement policies that reduce the risk of human-targeted attacks.

Important security measures include:

| Security Control | Purpose |
|---|---|
| Security Awareness Program | Educates employees about modern attacks. |
| Access Management Policy | Defines how access requests and password resets are verified. |
| Antivirus / Endpoint Protection | Helps detect and prevent malicious software. |
| Anti-Phishing Solution | Identifies and blocks malicious emails. |

Security policies should be practical, enforceable, and regularly reviewed.

## 7. Important SOC Concepts

| Term | Meaning |
|---|---|
| Social Engineering | Manipulating people to obtain information or access. |
| Phishing | Fraudulent messages designed to trick victims. |
| Impersonation | Pretending to be another person or trusted entity. |
| Deepfake | AI-generated media that imitates a real person. |
| Mitigation | Reducing the likelihood or impact of an attack. |
| Detection | Identifying suspicious or malicious activity. |
| MFA | Multi-Factor Authentication. |
| Anomalous Login | A login that differs from expected user behaviour. |

## 8. What I Learned

After completing this room, I understood:

- Why attackers target humans instead of directly attacking technical systems.
- How social engineering manipulates human behaviour.
- How phishing and impersonation can lead to account compromise.
- Why deepfake attacks create additional security risks.
- The difference between mitigation and detection.
- How SOC analysts investigate suspicious employee activity.
- Why identity verification and security awareness are important.

## 9. Practical Takeaways

A SOC analyst should not immediately trust suspicious requests or unusual account activity.

Investigation should involve:

1. Collecting relevant evidence.
2. Reviewing account and login activity.
3. Verifying the user's identity.
4. Assessing the risk.
5. Taking appropriate containment actions.
6. Documenting and escalating the incident.

## 10. Room Completion

- [x] Complete all room tasks.
- [x] Complete the Employees at Risk challenge.
- [x] Complete the Security Policy challenge.
- [x] Review the concepts.
- [x] Complete the room documentation.


---

## References

- TryHackMe – Humans as Attack Vectors: https://tryhackme.com/room/humansattackvectors
- TryHackMe – SOC Level 1: https://tryhackme.com/path/outline/blueteam

**Disclaimer:** These are personal learning notes written for educational and portfolio purposes. They are not an official TryHackMe walkthrough.


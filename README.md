

# Project: Secure Cloud Baseline & Identity Governance
**Date:** May 3, 2026
**Environment:** AWS / Azure Free Tier (Select one)
**Author:** Noel Fuentes

## 1. The "What": Project Overview
[cite_start]The objective of this lab was to establish a "secure by design" foundation for a new cloud environment[cite: 7, 59]. [cite_start]By implementing baseline security controls before deploying any resources, I have ensured that the environment is protected against common initial access vectors[cite: 136, 167].

## 2. The "How": Technical Implementation
[cite_start]This section details the specific security configurations applied to the environment[cite: 17, 60].

| Security Step | Action Taken | Evidence (Screenshots) |
| :--- | :--- | :--- |
| **Identity Protection** | [cite_start]Enabled Multi-Factor Authentication (MFA) for the root/administrative account[cite: 8, 55]. | *[Insert screenshot of MFA status: "Active"]* |
| **Network Security** | [cite_start]Configured Firewall Rules (Security Groups) to restrict inbound traffic[cite: 10, 56]. [cite_start]Specifically, I limited SSH/RDP access to only my specific public IP[cite: 11, 62]. | *[Insert screenshot of Security Group inbound rules showing "Source: [Your IP]/32"]* |
| **Access Control** | [cite_start]Created a standard IAM user for daily operations and assigned permissions following the **Principle of Least Privilege**[cite: 12, 13, 57]. | *[Insert screenshot of IAM Users list and attached policies]* |

## 3. The "Why": Business Reasoning & Risk Mitigation
[cite_start]In a professional setting, these technical steps translate directly to protecting the business's bottom line and reputation[cite: 20, 64, 140, 146].

* **MFA Implementation:** Mitigates the risk of **Account Takeover**. [cite_start]If an administrator's password is leaked or guessed (e.g., via a phishing attack), the second factor prevents the attacker from gaining total control over the company's cloud infrastructure[cite: 191, 206].
* **Firewall Hardening:** Reduces the **Attack Surface**. [cite_start]By blocking the "Open Internet" from hitting management ports (like Port 22), we prevent automated bots and malicious actors from attempting brute-force attacks[cite: 62, 192].
* **IAM Restrictions:** Ensures **Accountability and Integrity**. [cite_start]Using the root account for daily tasks is a high-risk activity; by using a standard user, we limit the potential "blast radius" if that specific user account is ever compromised[cite: 12, 158].

## 4. Risk Mapping
[cite_start]This lab demonstrates the practical application of the **CIA Triad** (Confidentiality, Integrity, and Availability) and mitigates several **OWASP Top 10** risks[cite: 21, 63, 117, 191]:

* [cite_start]**A01: Broken Access Control:** Addressed by implementing strict IAM policies and the Principle of Least Privilege[cite: 191, 199].
* [cite_start]**A07: Authentication Failures:** Addressed by enforcing MFA on high-privilege accounts[cite: 206].
* [cite_start]**A02: Security Misconfiguration:** Prevented by replacing default "Allow All" firewall rules with restrictive, specific rules[cite: 191, 200, 201].

---


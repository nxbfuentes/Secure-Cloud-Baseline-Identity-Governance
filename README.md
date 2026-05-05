1. The "What": Project Overview
The objective of this lab was to establish a "secure by design" foundation for a new cloud environment. By implementing baseline security controls before deploying any resources, I have ensured that the environment is protected against common initial access vectors.

2. The "How": Technical Implementation
This section details the specific security configurations applied to the environment.

Security Step	Action Taken	Evidence (Screenshots)
Identity Protection	
Enabled Multi-Factor Authentication (MFA) for the root/administrative account.

[Insert screenshot of MFA status: "Active"]
Network Security	
Configured Firewall Rules (Security Groups) to restrict inbound traffic. Specifically, I limited SSH/RDP access to only my specific public IP.

[Insert screenshot of Security Group inbound rules showing "Source: [Your IP]/32"]
Access Control	
Created a standard IAM user for daily operations and assigned permissions following the Principle of Least Privilege.

[Insert screenshot of IAM Users list and attached policies]
3. The "Why": Business Reasoning & Risk Mitigation
In a professional setting, these technical steps translate directly to protecting the business's bottom line and reputation.

MFA Implementation: Mitigates the risk of Account Takeover. If an administrator's password is leaked or guessed (e.g., via a phishing attack), the second factor prevents the attacker from gaining total control over the company's cloud infrastructure.

Firewall Hardening: Reduces the Attack Surface. By blocking the "Open Internet" from hitting management ports (like Port 22), we prevent automated bots and malicious actors from attempting brute-force attacks.

IAM Restrictions: Ensures Accountability and Integrity. Using the root account for daily tasks is a high-risk activity; by using a standard user, we limit the potential "blast radius" if that specific user account is ever compromised.

4. Risk Mapping
This lab demonstrates the practical application of the CIA Triad (Confidentiality, Integrity, and Availability) and mitigates several OWASP Top 10 risks:

A01: Broken Access Control: Addressed by implementing strict IAM policies and the Principle of Least Privilege.

A07: Authentication Failures: Addressed by enforcing MFA on high-privilege accounts.

A02: Security Misconfiguration: Prevented by replacing default "Allow All" firewall rules with restrictive, specific rules.

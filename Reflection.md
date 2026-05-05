In a home lab environment, documenting **A03: Software Supply Chain Failures** is arguably the most difficult because it involves risks that occur **before** software even reaches your system[cite: 125, 130]. Unlike a firewall rule or an MFA setting that you can verify with a single screenshot, supply chain security requires proving the integrity of third-party code, libraries, and build pipelines you don't fully control[cite: 130, 135].

### Why A03 is Challenging to Document in a Lab
* **Visibility Gap:** In a standard home lab, you typically download an ISO or a package and install it[cite: 243, 342]. Documenting the "supply chain" would require you to verify the **digital signatures** or **hashes** for every single dependency or update, which is a massive administrative task for a solo learner[cite: 135].
* **Managerial Complexity:** A03 is often mitigated through **Managerial Controls**, such as a "Third-Party Risk Management" policy or a "Software Bill of Materials" (SBOM)[cite: 84, 130]. In a professional GRC role, you would audit a vendor's security practices; in a home lab, you are the vendor, the auditor, and the user all at once[cite: 50, 414].
* **Infrastructure Requirements:** To truly "document" a mitigation for A03, you would need to set up a private repository or a scanning tool that checks for **Vulnerable Components** in real-time, which is significantly more complex than setting up basic Cloud IAM[cite: 130, 417].

---

### Comparison of Documentation Difficulty
| OWASP Risk | Ease of Documentation | Why? |
| :--- | :--- | :--- |
| **A07: Authentication Failures** | **Easy** | Take a screenshot of your active **MFA** status[cite: 17, 134]. |
| **A02: Security Misconfiguration** | **Medium** | Show your **Firewall/Security Group** rules restricting Port 22[cite: 43, 48]. |
| **A01: Broken Access Control** | **Medium** | Show your **IAM user** having "Read-Only" instead of "Administrator" rights[cite: 46, 127]. |
| **A03: Software Supply Chain** | **Hard** | Requires tracking every **third-party library** and verifying its origin and integrity[cite: 130, 135]. |

---

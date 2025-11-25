# Vulnerability Assessment Report  
**Date:** October 11, 2025  

---

## System Description
The organization operates a remote database server that supports global e-commerce operations. The system runs a modern Linux distribution and hosts a MySQL database instance used for storing customer leads, sales insights, and marketing data. The server is equipped with enterprise-grade processing power and 128GB of memory, and it communicates with other systems over IPv4. Connections to the server are encrypted using TLS, ensuring secure data transmission over public networks.

---

## Scope
This assessment focuses exclusively on the server’s access controls and exposure to the public internet. It evaluates risks associated with the server’s three-year period of open public access, covering activity and configuration issues observed over the last three months (June–August 2025). The analysis follows the guidance of **NIST SP 800-30 Rev. 1** for evaluating threats, vulnerabilities, and business impact.

---

## Purpose
The database server functions as the company’s primary data repository, housing customer information, campaign results, and analytics used by remote employees to identify high-value prospects. Because this data directly supports marketing and sales operations, securing the system is essential. Any compromise could disrupt business workflows, expose sensitive information, or result in data loss.

---

## Risk Assessment

| Threat Source | Threat Event | Likelihood (1–3) | Severity (1–3) | Risk Score |
|--------------|--------------|------------------|----------------|------------|
| Malicious Actor | Extract confidential data via unauthorized access | 3 | 3 | 9 |
| Internal Employee | Interrupt essential business processes | 2 | 3 | 6 |
| External Customer | Modify or delete important records | 2 | 3 | 6 |

---

## Approach
The risk evaluation considered how the company stores and manages sensitive data, as well as the implications of maintaining a publicly accessible database server. Likelihood values were determined by analyzing system exposure, known vulnerabilities, and the absence of access restrictions. Severity ratings were based on potential operational disruption, financial loss, and reputational damage if an incident were to occur.

---

## Remediation Strategy
To reduce risk and strengthen the organization’s security posture, the following actions are recommended:

- **Implement strong authentication and authorization controls** including MFA and access management.  
- **Restrict network access** by enforcing IP allow-listing to ensure only trusted corporate or VPN-connected endpoints can reach the server.  
- **Enhance auditing capabilities** to log user activity, detect anomalies, and support incident investigations.  
- **Upgrade data-in-transit protections** by ensuring all communications use modern TLS standards.  
- **Eliminate public exposure** by placing the database behind a secure internal network or VPN.

These measures will significantly reduce the attack surface and help prevent unauthorized access to critical business data.


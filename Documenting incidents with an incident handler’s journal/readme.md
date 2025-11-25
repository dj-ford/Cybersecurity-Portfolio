# Incident Handler’s Journal  


**Date:** October 15, 2025  
**Entry:** #1  

| **Field** | **Details** |
|-----------|-------------|
| **Description** | This entry documents a ransomware attack that caused significant disruption at a small U.S. healthcare clinic. The incident prevented employees from accessing critical patient records and essential business applications. |
| **Tool(s) Used** | No specialized tools were used at this stage; the entry focuses on initial documentation of the incident as reported by employees. |
| **The 5 W’s** | **Who:** A known ransomware group targeting healthcare and transportation sectors. <br> **What:** A ransomware infection that encrypted medical records and displayed a ransom note demanding payment. <br> **Where:** The clinic’s internal network and employee workstations. <br> **When:** Tuesday morning at approximately 9:00 a.m. <br> **Why:** Attackers gained entry through phishing emails containing a malicious attachment. After gaining access, they deployed ransomware to encrypt files for financial extortion. |
| **Additional Notes** | 1. What preventive security controls—such as phishing awareness training, email filtering, and endpoint protection—could reduce the likelihood of similar incidents? <br> 2. What considerations should the clinic evaluate before deciding whether to pay the ransom, including legal implications, data recovery options, and guidance from law enforcement? |

---

**Date:** October 20, 2025  
**Entry:** #2  

| **Field** | **Details** |
|-----------|-------------|
| **Description** | This entry documents my analysis of a packet capture associated with a user’s web browsing session. The investigation focused on identifying endpoints, reviewing protocol activity, and examining packet contents to understand how data flows between systems during a website connection. |
| **Tool(s) Used** | I used Wireshark, a graphical network protocol analyzer that allows analysts to capture, filter, and inspect network packets. Its ability to break down protocols, reveal packet layers, and isolate suspicious traffic makes it indispensable for network forensics. |
| **The 5 W’s** | N/A |
| **Additional Notes** | This exercise provided deeper insight into how individual packets reveal the structure of web communication. Although Wireshark’s interface felt complex at first, applying filters and expanding packet layers made the analysis more intuitive and highlighted how valuable packet inspection is for detecting security issues. |


---

**Date:** October 20, 2025  
**Entry:** #3  


| **Field** | **Details** |
|-----------|-------------|
| **Description** | This entry documents my first experience capturing live network traffic using tcpdump on a Linux system. The goal was to identify network interfaces, apply packet filters, and generate a packet capture for later analysis. This exercise emphasized how command-line tools can provide deep visibility into real-time network activity. |
| **Tool(s) Used** | I used **tcpdump**, a command-line network protocol analyzer that captures and inspects packets at a low level. Unlike graphical tools, tcpdump offers granular control over filters, interfaces, and output formats, making it ideal for lightweight monitoring and remote investigations. |
| **The 5 W’s** | N/A |
| **Additional Notes** | Working entirely in the command line was challenging, especially with filter syntax and interface selection. Mistakes helped reinforce how tcpdump interprets commands, and by repeating steps I became more comfortable navigating live captures. This experience highlighted how essential tcpdump is for fast, lightweight traffic analysis. |

---

**Date:** October 20, 2025  
**Entry:** #4


| **Field** | **Details** |
|-----------|-------------|
| **Description** | This entry documents the investigation of a suspicious file hash associated with a malicious spreadsheet downloaded by an employee. The activity focused on validating the threat using a malware intelligence platform and identifying additional indicators of compromise to support further analysis. This scenario reinforced how early detection and verification play a critical role in preventing malware spread within an organization. |
| **Tool(s) Used** | I used **VirusTotal**, an online malware analysis and threat intelligence tool that aggregates results from dozens of antivirus engines and security vendors. VirusTotal helps analysts quickly determine whether a file, URL, or hash has been previously reported as malicious. In this case, I submitted the file’s SHA-256 hash to confirm malicious behavior and review associated IoCs. |
| **The 5 W’s** | **Who:** An unidentified malicious actor targeting the organization through email-based delivery. <br> **What:** A password-protected spreadsheet containing a malicious payload, identified by the SHA-256 hash `54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b`. <br> **Where:** The compromise occurred on an employee workstation within the financial services company. <br> **When:** The SOC received an automated alert at approximately 1:20 p.m. after the intrusion detection system flagged suspicious activity. <br> **Why:** The attacker relied on social engineering to trick the employee into opening the file, which executed the embedded malware once the password was entered. |
| **Additional Notes** | Future prevention efforts could include strengthening employee security awareness training, especially around handling unexpected attachments and password-protected files. Technical controls such as enhanced email filtering, attachment sandboxing, and stricter macro/attachment policies could also reduce exposure to similar threats. |

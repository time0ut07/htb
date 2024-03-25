# Metabase Pre-Auth RCE PoC (CVE-2023-38646)

This script is written in Python and allows user to exploit the Metabase's software security flaw for CVE-2023-38646. This exploit affects Metabase open source before 0.46.6.1 and Metabase Enterprise before 1.46.6.1. Exploiting this vulnerability could allow attackers to do Remote Code Execution (RCE).


## Exploit

[Reference](https://www.vicarius.io/vsociety/posts/unmasking-cve-2023-38646-analyzing-the-critical-metabase-security-vulnerability-and-its-implications-1)

**What is Metabase**


Metabase, a widely-used open-source business intelligence tool that helps users connect to many other popular databases. Metabase allows user to query about their data, displaying answers in formats that is logical, be it bar charts or a detailed table.

**What is RCE**


Remote Code Execution (RCE) is a dangerous cybersecurity threat where it allows an attacker to gain unauthorised access to an application or system and execute malicious codes remotely. RCE can result to complete control over compromised system, which could lead to situations like deploying of malware and system manipulation.

**How it works**

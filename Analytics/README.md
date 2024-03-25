# Metabase Pre-Auth RCE PoC (CVE-2023-38646)

This script is written in Python and allows user to exploit the Metabase's software security flaw for CVE-2023-38646. This exploit affects Metabase open source before 0.46.6.1 and Metabase Enterprise before 1.46.6.1. Exploiting this vulnerability could allow attackers to do Remote Code Execution (RCE).


## Exploit

[Unmasking CVE-2023-38646: Analyzing the Critical Metabase Security Vulnerability and Its Implications](https://www.vicarius.io/vsociety/posts/unmasking-cve-2023-38646-analyzing-the-critical-metabase-security-vulnerability-and-its-implications-1)


[Reproducing CVE-2023-38646: Metabase Pre-auth RCE](https://blog.calif.io/p/reproducing-cve-2023-38646-metabase)

**What is Metabase**


Metabase, a widely-used open-source business intelligence tool that helps users connect to many other popular databases. Metabase allows user to query about their data, displaying answers in formats that is logical, be it bar charts or a detailed table.

**What is RCE**


Remote Code Execution (RCE) is a dangerous cybersecurity threat where it allows an attacker to gain unauthorised access to an application or system and execute malicious codes remotely. RCE can result to complete control over compromised system, which could lead to situations like deploying of malware and system manipulation.

**How it works (Surface Level)**


Endpoint `/api/setup/validate` is used to check for database connection during the application setup process. This specific endpoint requires a valid setup-token to be invoked, and this token is generated when Metabase starts and can be called by calling the pre-Auth API `/api/setup/properties`


Additionally, in the `/api/setup/validate` endpoint, attackers can force Metabase to connect to arbitrary database servers using JDBC.


Finally, to RCE, a SQL Injection vulnerability within the H2 database driver was leveraged. By using the TRACE_LEVEL_SYSTEM_OUT argument and stacking SQL queries, they achieved arbitrary code execution.


One of the main cause for this vulnerability is due to 

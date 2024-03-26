# Admin Dashboard Command Injection PoC (HTB-Headless)

This script is written in Python and allows user to inject command into the administrator dashboard for the box `Headless`. This script is crafted with only getting reverse shell in mind.

## HTB

This exploit was used in the `Headless` box


| Difficulty | Operating System | Step |
|------------|------------------|------|
| Easy | Linux | Getting initial access |

## Exploit


**What is Comnand Injection**


Command Injection is an attack in which the main goal is to execute arbitrary commands on the target machine via a vulnerable application. This may happen when application passes unclean user supply data to the system. Command injection vulnerabilities can potentially grant an attacker full control over the compromised system, enabling actions such as deploying malware and manipulating system functionality.

**How it works (Surface Level)**


Will figure out soon...


## Usage


This script is crafted by myself for fun.


This script require the user to have access to the dashboard page by having the admin cookie, its main intention is to obtain a reverse shell, which you can have more options using [revshells](https://www.revshells.com/). The script can be run using the following command:


`python3 exploit.py -ip [target IP] -p [target port] -a [admin cookie] -c "[command]"`

![](https://imgur.com/ofoiIaF.png)

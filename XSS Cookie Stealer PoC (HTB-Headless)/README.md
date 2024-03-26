# XSS Cookie Stealer PoC (HTB-Headless)

This script is written in Python and allows user to steal the admin cookie to access `/dashboard`

## HTB

This exploit was used in the `Headless` box


| Difficulty | Operating System | Step |
|------------|------------------|------|
| Easy | Linux | Initial Foothold |

## Exploit


**What is Cross-site Scripting (XSS)**


Cross-site Scripting (XSS) is a type of web security vulnerability which enables attacker to inject client-side scripts in hope to get a respond from the server. XSS vulnerabilities may lead to consequences such as data theft and session hijacking


**How it works (Surface Level)**


XSS occurs when user inputs are not validated properly (blacklisting), output are not encoded properly, or storing user-provided data are not sanitized.


## Usage


This script is crafted by myself for fun.


This script does not require any unqiue information, its main intention is to obtain the admin cookie to progress the box and the payload is coded into the script. The script can be run using the following command:


`python3 exploit.py -ip [target IP] -p [target port] -c [your cookie] -host [host IP]`

![](https://imgur.com/PIOJqPK.png)

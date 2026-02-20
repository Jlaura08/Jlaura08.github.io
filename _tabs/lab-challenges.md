---
layout: page
title: Lab Challenges
icon: fas fa-flag
order: 4
---

In cybersecurity, practical application is everything. Below is a collection of write-ups from my Cyber Shujaa training and independent Hack The Box modules.

---

## Challenge: [Insert HTB Machine / Lab Name]
**Problem Statement:** The objective was to perform initial reconnaissance on a target Linux machine, identify misconfigurations in running services, and successfully escalate privileges to the root user.

**Approach:**
1. **Enumeration:** Utilized Nmap to scan for open ports and identified a vulnerable web service.
2. **Exploitation:** Gained an initial foothold by exploiting a misconfigured upload directory to trigger a reverse shell.
3. **Privilege Escalation:** Enumerated SUID binaries and abused system permissions to achieve root access.

**Tools Used:** Nmap, Netcat, Python, Linux Command Line.

**Key Lessons Learned:**
* Reinforced the importance of proper file permissions in Linux Mint and enterprise environments.
* Gained hands-on experience in identifying and exploiting outdated web components.

*(Note: Detailed step-by-step write-ups with screenshots are available in the main blog feed!)*

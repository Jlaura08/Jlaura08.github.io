---
layout: page
title: Lab Challenges
icon: fas fa-flag
order: 3
---

In cybersecurity, practical application is everything. Below is a selection of hands-on lab challenges and Capture The Flag (CTF) exercises I have completed to sharpen my offensive and defensive skills.

---

## 1. Hack The Box: Linux Privilege Escalation
**Problem Statement:** The objective was to perform enumeration on a target Linux machine to identify system misconfigurations and escalate privileges from a standard user to the `root` account.

**Approach:**
1. **Reconnaissance:** Conducted an initial network scan to identify open ports and running services.
2. **Initial Foothold:** Exploited a vulnerable web service to upload a payload and gain a low-privileged reverse shell.
3. **Privilege Escalation:** Enumerated the file system for SUID binaries and abused a misconfigured custom executable to spawn a root shell.

**Tools Used:** Nmap, Gobuster, Netcat, LinPEAS.

**Screenshots:**
![HTB Privilege Escalation](/assets/img/labs/htb-privesc.png){: .shadow .rounded-10 w="700" }
_Demonstrating the successful escalation to a root shell._

**Key Lessons Learned:**
* Reinforced the critical importance of the Principle of Least Privilege (PoLP).
* Gained practical insight into the severe security risks associated with improperly configuring SUID permissions on Linux binaries.

---

## 2. TryHackMe: Web Application Vulnerabilities
**Problem Statement:** Identify and exploit common web vulnerabilities (OWASP Top 10) within a simulated corporate web application environment.

**Approach:**
1. **Traffic Analysis:** Intercepted and modified web traffic to analyze server requests and responses.
2. **Authentication Bypass:** Identified and utilized an SQL injection payload to bypass the administrative login mechanism.
3. **Session Hijacking:** Leveraged Cross-Site Scripting (XSS) to exfiltrate session cookies from simulated users.

**Tools Used:** Burp Suite, SQLmap, Firefox Developer Tools.

**Screenshots:**
![THM Web Exploitation](/assets/img/labs/thm-web.png){: .shadow .rounded-10 w="700" }
_Intercepting and modifying web requests to uncover injection flaws._

**Key Lessons Learned:**
* Experienced firsthand how input sanitization failures lead to complete application compromise.
* Deepened my understanding of how to implement parameterized queries to mitigate database injection attacks.

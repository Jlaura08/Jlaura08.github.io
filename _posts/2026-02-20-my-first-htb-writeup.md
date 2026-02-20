---
layout: post
title: "Hack The Box: Initial Recon and Privilege Escalation"
date: 2026-02-20 17:00:00 +0300
categories: [Lab Challenges, Hack The Box]
tags: [nmap, privilege-escalation, linux]
---

Welcome to my first official lab write-up! As part of my ongoing training, I am documenting my practical exercises to reinforce my methodology and share my learning process.

## 1. Reconnaissance
Every good engagement starts with solid enumeration. Firing up my Linux Mint terminal, I started with a standard Nmap scan against the target IP to see what doors were left open.

```bash
nmap -sC -sV -oN initial_scan 10.10.10.x

Results:

Port 22: SSH (OpenSSH)

Port 80: HTTP (Apache)

2. Gaining a Foothold
Navigating to the web server on Port 80 revealed a default Apache page, but running a directory buster uncovered a hidden /uploads endpoint. By bypassing the client-side file upload filter, I was able to upload a simple reverse shell payload.

Once executed, I caught the shell on my local machine using Netcat:

nc -lvnp 4444

3. Privilege Escalation
With a low-level shell established, it was time to hunt for a path to root. I checked for misconfigured SUID binaries:

find / -perm -u=s -type f 2>/dev/null

This revealed a custom binary that could be executed with elevated privileges. By manipulating the environment variables before running it, I successfully dropped into a root shell!

Stay tuned for more detailed walkthroughs and projects as I continue building my skills in threat detection and secure architecture.

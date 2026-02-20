---
layout: page
title: Web Application Assessment Lab
icon: fas fa-flag
order: 4
---

In cybersecurity, practical application is everything. Below is a collection of write-ups from my Cyber Shujaa training.

---

## Problem Statement
In this lab, I was tasked with analyzing a **Web Application** to identify security weaknesses. The goal was to understand how modern web apps handle user input and authentication.

## The Approach
### Step 1: Mapping the Application
I started by navigating through the web application to understand its functionality. I looked at the Login page, the "Contact Us" forms, and the URL structure.

### Step 2: Vulnerability Scanning
I used browser developer tools to inspect the source code. I looked for:
*   Hidden fields in HTML forms.
*   Sensitive comments left by developers.
*   Insecure cookies.

---
**[Link to GitHub Repository for this Lab](https://github.com/Jlaura08/Jlaura08.github.io)**
### Step 3: Exploitation / Analysis
I found that the application was not validating input correctly on the "Search" bar, which could lead to Cross-Site Scripting (XSS).

> **Observation:** The application reflected my search query back to the screen without sanitization.

## Tools Used
*   **Web Browser (Firefox/Chrome)**
*   **Developer Tools (F12)**
*   **Burp Suite** (for intercepting traffic)

## Key Lessons Learned
*   Web applications must validate all user input on the server side.
*   Understanding HTTP methods (GET vs POST) is essential for web analysis.
*   Security headers should be implemented to protect against common web attacks.

*(Note: Detailed step-by-step write-ups with screenshots are available in the main blog feed!)*

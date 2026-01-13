# OWASP Juice Shop — Persisted XSS via HTTP Header Injection

**Date:** 2026--1-13  
**Platform:** OWASP Juice Shop  
**Course:** Computer Security (MSc Cybersecurity, Linköping University)  
**Difficulty:** 4 ⭐  
**Vulnerability Type:** Stored XSS

---

## Challenge Description
Perform a **persisted XSS attack** using  
`<iframe src="javascript:alert(xss)">`  
by injecting the payload through an **HTTP header**.

---

## Failed Attempts
- Injecting headers using `fetch()` requests
- Trying common headers:
  - `X-Forwarded-For`
  - `X-Real-IP`
  - `Client-IP`
- Browser console-based injections
- Targeting different endpoints (login, logout, registration)

In all cases, the application continued to display the real IP address.

---

## How I Solved It

1. Installed the **ModHeader** Chrome extension
2. Added a custom request header:
Name: True-Client-IP
Value: <iframe src="javascript:alert('xss')">

3. Applied the header to the **OWASP Juice Shop domain**
4. Logged in normally using the **UI login form**
5. Navigated to:
6. The stored header value was rendered and the XSS payload executed

---

## Key Takeaway
Trusting HTTP headers without validation can lead to **persistent XSS**, especially when displayed in security-related interfaces. All header values must be sanitized before storage or rendering.

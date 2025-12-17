# OWASP Juice Shop — Hardcoded Test Credentials

**Date:** 2025-12-17
**Platform:** OWASP Juice Shop  

---

## Challenge Description
Log in using **unused but still valid test credentials** that were hardcoded on the client-side.

---

## How I Solved It

1. Opened the **OWASP Juice Shop** application  
2. Opened **Developer Tools**
3. Navigated to **Sources**
4. Opened the `main.js` file
5. Searched for the keyword **`test`**, as hinted in the challenge
6. Found hardcoded test credentials in the source code
7. Used the discovered credentials on the login page

Login was successful.

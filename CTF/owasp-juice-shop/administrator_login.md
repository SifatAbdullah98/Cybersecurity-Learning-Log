# OWASP Juice Shop — Administrator Login

**Date:** 2025-12-19  
**Platform:** OWASP Juice Shop  
**Vulnerability Type:** Weak Credentials & SQL Injection

---

## Challenge Description
Log in using the **administrator account**.

---

## How I Solved It(Tried both way)

### Method 1: Weak Credentials (Guessing)
1. Logged in using a previously discovered **test account**
2. Guessed the admin username based on context: `admin@juice-sh.op`
3. Tried common passwords:
   - `admin` (failed)
   - `admin123` (successful)
4. Successfully logged in as administrator

---

### Method 2: SQL Injection
1. Logged out of the application
2. On the login page, entered this as email: ' OR 1=1--
3. Entered any value as the password anything should work as afte this "--" everything is comment so sql ignores everything after it
4. Submitted the form and got logged in



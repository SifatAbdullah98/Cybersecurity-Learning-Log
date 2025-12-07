# OWASP Juice Shop — Poison Null Byte Backup File Access

**Date:** 2025-12-07  
**Platform:** University Computer Security Lab  
**Type:** Poison Null Byte / File Access Bypass

---

## Problem
The challenge required accessing a **salesman's forgotten backup file**.  
The application only allowed files ending with **.md** or **.pdf** due to a file extension filter.

Target file:
coupons_2013.md.bak

---


## Solution

This file was blocked by the filter.

1. Added `/ftp` after the Juice Shop URL.
2. Tried bypassing the extension filter using a **Poison Null Byte**.

Initial attempts (failed): coupons_2013.md.bak%00.md & coupons_2013.md.bak%00.pdf

3. Used **double-encoded null byte** instead: coupons_2013.md.bak%2500.md

✅ This successfully bypassed the filter and gave access to the backup file.

---

## What I Learned
- File extension filters can be bypassed using **null byte injection**.
- Some servers require **double encoding** to trigger the vulnerability.
- Backup files can expose sensitive information.


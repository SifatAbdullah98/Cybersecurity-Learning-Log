# OWASP Juice Shop — Duplicate User Registration

**Date:** 2025-12-17  
**Platform:** OWASP Juice Shop  


---

## Challenge Description
Register a user account using an **email address that already exists** in the system.

---

## How I Solved It

1. Opened the **OWASP Juice Shop** application  
2. Navigated to the **registration page**
3. Entered random email address
4. Submitted the form with any password
5. Opened **Developer Tools → Network tab**
6. Located the **POST registration request**
7. Copied the request as **fetch**
8. Executed the request again from the **Console**

The application allowed duplicate user registration.


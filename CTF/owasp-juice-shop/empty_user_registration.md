# OWASP Juice Shop — Empty Email & Password Registration

**Date:** 2025-12-17  
**Platform:** OWASP Juice Shop  

---

## Challenge Description
Register a user account with an **empty email and password**, bypassing the frontend validation.

---

## How I Solved It

1. Opened the **OWASP Juice Shop** website 
2. Navigated to the **registration page**
3. Entered a random email and password and submitted the form
4. Opened **Developer Tools → Network tab**
5. Located the **POST request** sent during registration
6. Right-clicked the request and selected **Copy → Copy as fetch**
7. Pasted the fetch command into the **Console**
8. Removed the `email` and `password` fields from the request body
9. Executed the modified request

The account was successfully created with empty credentials.

---

## Key Takeaway
This challenge shows how relying only on **client-side validation** is insecure. Input validation must also be enforced **server-side** to prevent unauthorized or malformed requests.

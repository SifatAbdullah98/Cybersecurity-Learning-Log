# OWASP Juice Shop — Forged Unsigned JWT

**Date:** 2025-12-28  
**Platform:** OWASP Juice Shop   
**Difficulty level:** 5   
**Vulnerability Type:** JWT Misconfiguration (alg: none)

---

## Challenge Description
Forge an **unsigned JWT token** to impersonate the non-existing user  
`jwtn3d@juice-sh.op`.

---

## How I Solved It

1. Logged into Juice Shop using a valid user account
2. Opened **Developer Tools → Network**
3. Retrieved a valid JWT from the `Authorization` request header
4. Opened **DevTools Console** and decoded the JWT:
   - Decoded **header** and **payload** using `atob()` and `JSON.parse()`
5. Modified the token:
   - Changed `"alg"` in the header to `"none"` by doing this the server skips signature verification
   - Changed the payload email to `jwtn3d@juice-sh.op`
   - Kept required fields (e.g. `iat`) unchanged
6. Re-encoded the modified header and payload using Base64URL encoding
7. Constructed the forged token in the format:
(no signature, trailing dot)
8. Sent the forged token using a manual `fetch()` request


The application accepted the unsigned JWT and authenticated the forged user.

---

## Lesson
JWTs must **never allow `alg: none`** and must enforce strict server-side signature verification.

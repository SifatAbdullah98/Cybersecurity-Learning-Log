# OWASP Juice Shop — Shopping Basket Manipulation via Parameter Pollution

**Date:** 2025-12-07  
**Platform:** OWASP Juice Shop  
**Course:** Computer Security (MSc Cybersecurity, Linköping University)  
**Difficulty:** 3 ⭐  
**Vulnerability Type:** HTTP Parameter Pollution / Broken Access Control

---

## Challenge Description
Add an item to **another user’s shopping basket** without tampering with the authorization token.

---

## How I Solved It

1. Started with a normal user account and added a product to the basket via the UI.
2. In the **Network** tab, located the `POST /api/BasketItems/` request that added the item.
3. Copied the request as `fetch()` and pasted it into the Console.
4. Initially tried changing the single `BasketId` value — it failed.
5. Based on the challenge hint, modified the request body to include **two `BasketId` parameters**:
   - First `BasketId` passed the server’s authorization check.
   - Second `BasketId` determined which basket actually received the item.
6. Used a second basket ID (found earlier via IDOR or enumeration) together with the first one.
7. Executed the modified request.

✅ The product ended up in **another user’s basket** without changing the auth token.

---

## Key Takeaway
The server only validated the first occurrence of the `BasketId` parameter but used a later one to perform the action.  
This is a practical example of **HTTP Parameter Pollution (HPP)**, where duplicate parameters with different values cause the backend to behave unexpectedly. Documentation from OWASP notes that handling multiple parameters of the same name can lead to unexpected behavior and potential exploitation. :contentReference[oaicite:0]{index=0}

Proper server-side validation must ensure a single, trusted parameter value is used and reject any duplicates or conflicting entries to prevent this type of bypass.

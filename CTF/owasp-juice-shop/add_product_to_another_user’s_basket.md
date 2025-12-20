# OWASP Juice Shop — Add Product to Another User’s Basket

**Date:** 2025-12-20  
**Platform:** OWASP Juice Shop  

---

## Challenge Description
Add an **additional product** to **another user’s shopping basket** without modifying the authorization token.

---

## How I Solved It

1. Logged into the application as a normal user
2. Opened **Developer Tools → Network tab**
3. Added a product to my own basket
4. Located the corresponding **add-to-basket request**
5. Copied the request as **fetch** and pasted it into the **Console**
6. Initially tried changing the `BasketId`, which did not work
7. Based on the challenge hint, modified the request body to include **two `BasketId` parameters**
   - One matching my own basket
   - One matching another user’s basket
8. Executed the modified request

The product was successfully added to another user’s shopping basket.

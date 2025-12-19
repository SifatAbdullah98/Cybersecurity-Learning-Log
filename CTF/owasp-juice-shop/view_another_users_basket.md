# OWASP Juice Shop — View Another User’s Basket

**Date:** 2025-12-19  
**Platform:** OWASP Juice Shop  

---

## Challenge Description
View the **shopping basket of another user**

---

## How I Solved It

1. Logged into the **OWASP Juice Shop** application
2. Opened **Developer Tools → Network tab**
3. Clicked on the **Basket** page in the application
4. Identified the basket-related request in the Network tab
5. Right-clicked the request and selected **Copy → Copy as fetch**
6. Pasted the fetch command into the **Console**
7. Modified the **User ID** in the request URL(tried a differet one)
8. Executed the modified request

The response returned another user’s shopping basket.

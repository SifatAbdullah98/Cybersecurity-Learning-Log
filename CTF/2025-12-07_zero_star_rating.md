# OWASP Juice Shop — Zero Star Rating

**Date:** 2025-12-01  
**Platform:** University Computer Security Lab  
**Type:** Client-Side Validation Bypass

---

## Problem
The rating system only allowed submitting values between **1 to 5 stars**.  
The challenge was to successfully submit a **0-star rating**.

---

## Solution
1. Opened the feedback form and submitted a normal **1-star rating**.
2. Opened **Developer Tools → Network tab**.
3. Captured the `/api/Feedbacks/` request.
4. Right-clicked the request → **Copy as fetch**.
5. Pasted it into the **Console**.
6. Changed: "rating": 1 to "rating": 0
7. Hit enter and Done


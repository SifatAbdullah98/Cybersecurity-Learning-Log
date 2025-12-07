# Hidden Scoreboard Page – CTF Writeup

**Date:** 2025-12-07  
**Platform:** OWASP Juice Shop  
**Difficulty:** Easy  

---

## Challenge
Find the carefully hidden "Score Board" page.

---

## Method
1. Opened **OWASP Juice Shop** in the browser.
2. Opened **Developer Tools → Inspect**.
3. Opened the `main.js` file from **Sources**.
4. Searched for keywords like:
   - `score`
   - `board`
   - `admin`
5. Found the hidden scoreboard **URL path**.
6. Copied the path and pasted it directly into the browser.
7. Scoreboard page loaded successfully.

---

## Result
Successfully discovered and accessed the hidden scoreboard page.


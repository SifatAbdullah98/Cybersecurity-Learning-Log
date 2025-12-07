# Hidden Score Board Page Discovery — OWASP Juice Shop

**Platform:** OWASP Juice Shop  
**Category:** Information Disclosure  

---

## Challenge Description
The task was to locate the **hidden Score Board page** inside the OWASP Juice Shop application.

---

## Solution

1. Opened **OWASP Juice Shop** in the browser.
2. Right-clicked and selected **Inspect**.
3. Navigated to the **main.js** file from the browser developer tools.
4. Searched for keywords like:
   - `score`
   - `path`
5. After scrolling through the file, I found the hidden **Score Board URL path**.
6. Pasted the discovered path directly into the browser.
7. The Score Board page successfully loaded.

---

## Result
- Successfully accessed the **hidden Score Board page**
- Challenge completed using **frontend source code inspection**

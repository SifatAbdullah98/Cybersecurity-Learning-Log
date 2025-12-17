# OWASP Juice Shop — DOM XSS Challenge

**Date:** 2025-12-17  
**Platform:** OWASP Juice Shop     

---

## Challenge Description
Perform a DOM XSS attack using the following payload:
<iframe src="javascript:alert(`xss`)">
  
## How I Solved It
1. Opened the **OWASP Juice Shop** application  
2. Navigated to the **search box**  
3. Entered the following payload into the search field:
   ```html
   <iframe src="javascript:alert(`xss`)">



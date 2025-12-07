# OWASP Juice Shop — Cat Photo URL Encoding Bypass

**Date:** 2025-12-07  
**Platform:** Owasp Juice shop(For Course Computer Security by LiU)   
**Category:** URL Encoding / Input Handling

---

## Challenge

A broken image appeared in the **Photo Wall**.  
The goal was to access the hidden cat photo by fixing the improperly encoded URL.

Broken filename:
😼-#zatschi-#whoneedsfourlegs-1572600969477.jpg

---

## Root Cause

The application failed to properly **URL-encode special characters**:
- Emoji (`😼`)
- Hash (`#`)

Because of this, the browser could not load the image.

---

## Solution

### 1. Inspect the broken image
Found the raw filename inside the `src` attribute.

### 2. URL-encode special characters

| Character | Encoded |
|------------|----------|
| 😼 | `%E1%93%9A%E1%98%8F%E1%97%A` |
| # | `%23` |

Final encoded filename: %E1%93%9A%E1%98%8F%E1%97%A2-%23zatschi-%23whoneedsfourlegs-1572600969477.jpg


### 3. Access the file directly

https://flaggjakt.isy.liu.se/assets/public/images/uploads/%E1%93%9A%E1%98%8F%E1%97%A2-%23zatschi-%23whoneedsfourlegs-1572600969477.jpg


✅ The cat photo loaded successfully and the challenge was solved.

---

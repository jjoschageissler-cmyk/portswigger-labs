
# 02-auth-multiple-credentials

**Bypassing rate limit with multiple credentials per request**
*PortSwigger Web Security Academy - Expert*

## Vulnerability
Website blocks after 3 wrong password request, but accepts `JSON arrays`. In the real world this might be due to the usage of the same logic for all of the websites
log in forms, which can lead to a situation where a single password login is handled like a multiple auth login.



## Tools
- password list
- Burp Repeater

## 

## Attack Steps

### 1. Analyse Request
After 3 wrong password attempts the website blocks you.

### 2. generate array in VS code
<img src="screenshots/02-generating-array.png" width="700">

### 3. build final request
<img src="screenshots/02-final-request.png" width="700">
Paste array in request

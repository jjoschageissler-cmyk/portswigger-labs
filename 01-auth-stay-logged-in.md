
# 01-auth-stay-logged-in

**Brute-forcing a stay-logged-in cookie**  
*PortSwigger Web Security Academy - Practitioner*

## Vulnerability
Weak MD5 hashing in `stay-logged-in` cookie allows offline brute-force attack.

**Cookie Format**: `base64(username:md5(password))`

## Tools
- Burp Suite Intruder
- HackVertor Extension
- password list 

## Attack Steps

### 1. Cookie Analysis

<img src="screenshots/01-cookie-decode.png" width="700">                                    

Cookie with username=Wiener and password=peter is as shown. Decoder analisis shows the cookie was made by a base64 encoded combination of a MD5 hash of the password and the username.

<img src="screenshots/01-intruder-setup" width="700>



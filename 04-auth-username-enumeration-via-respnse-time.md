# 04-auth-username-enumeration-response-time

**auth-username-enumeration-via-diffrent-response-time**
*PortSwigger Web Security Academy - Apprentice*

## Vulnerability
The website only verifies the password, if the username exists. So a request with a legit username and wrong password will take the website longer to response.

## Tools
-Burp Repeater

## Attack Steps

### 1. observe the login request 
Notice that if you put in a very long and wrong password and your right username the response takes a lot longer than if you insert a wrong username and the same password.

### 2. Intruder setup
Place the payload position at the username field and insert a very long password in order to trigger a bigger delay. 
The payload of the response with an unusual responsetime should contain a valid username.


# Processing..............





<img src="screenshots/03-browser-proof.png" width="700">

# 11-XXE-OOB-exfil

**Lab: Exploiting blind XXE to exfiltrate data using a malicious external DTD**

*PortSwigger Web Security Academy - Practitioner*

## Vulnerability
If we don't receive the information directly in the response the `XXE` is `blind` and we have to load the file we want to exfiltrate and then use this entity in another entity, which sends a request to a `exploit server` and delivers the file information per parameter. But in the `internal DTD` it is prohibited to insert a `parameter entity` into another entity.

So we have to load a external DTD from the exploit server, as external DTDs are allowed to expand a entity within a entity definition. 

## Preventions
The host should block out of band communication or if OOB is needed one would need to create a strict allowlist with all trusted external sources which could give rise to the complexity of the system.

## Tools
- Burb Proxy
- Labs exploit server
## Attack Steps

### 1. intercept the stock check request

### 2. internal DTD in request
We need to define a `parameter entity` that loads the `external DTD` hosted on the `exploit server` and call it. This simply loads the XML code and executes it.

<img src="" width="700">


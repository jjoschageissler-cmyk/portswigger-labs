# 17-PT-simple-case

**Lab:File path traversal, simple case**

*PortSwigger Web Security Academy - Apprentice*

## Vulnerability
The website takes a file name and inserts it in the base path where the images are. We can escape the base path and therefore
read/request files containing sensitive data.

## Preventions

## Tools
- Burb Proxy

## Attack Steps

### 1. find file path
Escape the basepath with `../`. You may have to add several `../`. Then add the file you want to read and send the request.

<img src="screenshots/16-payload.png" width="700">


## Proof
<img src="screenshots/16-proof.png" width="700">

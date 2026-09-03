# 18-PT-URL-encode

**Lab:File path traversal, traversal sequences stripped with superfluous URL-decode**

*PortSwigger Web Security Academy - Practitioner*

## Vulnerability
The website takes a file name and inserts it in the base path where the images are. It defenses against path traversal by not accepting file paths containing `../` sequences or cutting them out. However it does filter after decoding it once, so we can encode the sequences twice and they will slip right through.

## Preventions

## Tools
- Burb Proxy
- Hackvertor

## Attack Steps

### 1. find file path
Escape the basepath with `../`. You may have to add several `../`. Then add the file you want to read and send the request.


### 2. double urlencode the sequences
Put the `urlencode tags` around the sequences.
<img src="screenshots/18-payload.png" width="700">

## Proof
<img src="screenshots/18-proof.png" width="700">

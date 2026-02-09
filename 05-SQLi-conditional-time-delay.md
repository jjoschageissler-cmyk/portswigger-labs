# 05-SQLi-conditional-time-delay

**SQLi information retrieval via conditional time delay**
*PortSwigger Web Security Academy - Practitioner*

## Vulnerability
There is a `SQLi vulnerability` in the `tracking ID`. There is no visible response, but we can `enumerate` the password via conditional time delays. The lab lets us know the username and the password columnname.

## Tools
- Intruder
- Burp repeater
- Database cheat sheet

## Attack Steps

### 1. enumerate the database
We can use the PortSwigger cheat sheet to enumerate the database efficiently.
Oracle und Postgre`TrackingID=abc'|| 'test'--`
MySQLi `TrackingID=abc' 'test'#`
The enumeration responses reveal that the database is Oracle or Postgre.

### 2. build query
<img src="screenshots/05-SQLi-query-repeater.png" width="700">
Paste array in request

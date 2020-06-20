# Simple Security Headers

Simple tool for checking HTTP headers, cookies and technology

## Security HTTP headers checked
- Content-Security-Policy (CSP)
- Feature-Policy
- Strict-Transport-Security (HSTS)
- X-Frame-Options
- X-Content-Type-Options
- X-XSS-Protection
- Referrer-Policy

## Cookie attributes checked
- Expires
- HttpOnly
- Secure
- Path=/

## Basic technology identification

Performs a basic technology identification using the [apps.json](https://raw.githubusercontent.com/AliasIO/Wappalyzer/master/src/apps.json) file from Wappalyzer.

## Usage

```txt
usage: simple-security-headers.py [-h] -u URL [--verify] [--verbose]
```

![output](https://user-images.githubusercontent.com/7137144/85207829-f5fa2b00-b32b-11ea-987d-bf7f821e72b0.png)

This basic tool is inspired by [CrossHead](https://github.com/alvarodh5/CrossHead) project from alvarodh5 and Cristian Barrientos. Definitions are from securityheaders.com

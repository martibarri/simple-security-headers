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

```txt
$ python simple-security-headers.py -u wordpress.com
[*] Request URL: http://wordpress.com
[*] Response status code: 200
[*] Request headers:
{
  "Accept": "*/*",
  "Accept-Encoding": "gzip, deflate",
  "Cache-control": "no-cache",
  "Connection": "close",
  "Pragma": "no-cache",
  "User-Agent": "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:77.0) Gecko/20100101 Firefox/77.0"
}
[*] Response headers:
{
  "Connection": "close",
  "Content-Encoding": "gzip",
  "Content-Type": "text/html; charset=utf-8",
  "Date": "Sat, 20 Jun 2020 17:18:33 GMT",
  "Server": "nginx",
  "Strict-Transport-Security": "max-age=15552000; preload",
  "Transfer-Encoding": "chunked",
  "Vary": "Accept-Encoding, Cookie",
  "X-Frame-Options": "SAMEORIGIN",
  "X-ac": "1.mad _dca "
}

[~] Checking security headers...
[-] X-Content-Type-Options not found
[+] X-Frame-Options found
[-] X-XSS-Protection not found
[+] Strict-Transport-Security found
[-] Content-Security-Policy not found
[-] Referrer-Policy not found
[-] Feature-Policy not found

[~] Checking cookies...
[*] not found

[~] Checking Wappalyzer Regular Expressions...
[*] CMS: WordPress
[*] Analytics: Quantcast
[*] Blogs: WordPress
[*] Captchas: reCAPTCHA
[*] Font scripts: Google Font API
[*] Web servers: Nginx
[*] Reverse proxies: Nginx
```


This basic tool is inspired by [CrossHead](https://github.com/alvarodh5/CrossHead) project from alvarodh5 and Cristian Barrientos. Definitions are from securityheaders.com

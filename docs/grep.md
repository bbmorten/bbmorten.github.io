---
layout: default
title: NMAP Notes
ieuser: liks@smidk
---

# grep examples

### Exclude a word

Example output

```console
Nmap scan report for ptr-63.turkiye.gov.tr (94.55.118.63)
Nmap scan report for ptr-64.turkiye.gov.tr (94.55.118.64)
Nmap scan report for ptr-65.turkiye.gov.tr (94.55.118.65)
Nmap scan report for giris.turkiye.gov.tr (94.55.118.66)
Nmap scan report for ptr-67.turkiye.gov.tr (94.55.118.67)
Nmap scan report for ptr-68.turkiye.gov.tr (94.55.118.68)
Nmap scan report for ptr-69.turkiye.gov.tr (94.55.118.69)
```

we'd like to get rid of the lines with "ptr-"

```console
{{page.ieuser}} % nmap -sL 94.55.118.0/24 | grep -v -e "ptr-"
Starting Nmap 7.92 ( https://nmap.org ) at 2022-08-28 13:38 +03
Nmap scan report for 94.55.118.0
Nmap scan report for 94.55.118.1
Nmap scan report for ns2.turkiye.gov.tr (94.55.118.8)
Nmap scan report for www.turkiye.gov.tr (94.55.118.33)
Nmap scan report for static.turkiye.gov.tr (94.55.118.37)
Nmap scan report for giris.turkiye.gov.tr (94.55.118.66)
Nmap scan report for 94.55.118.255
Nmap done: 256 IP addresses (0 hosts up) scanned in 0.38 seconds
```

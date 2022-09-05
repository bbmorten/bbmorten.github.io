---
layout: default
title: NMAP Notes
ieuser: liks@smidk
---

# NMAP Notes

## Examples

### Finding public IP address by using nslookup and OpenDNS

```console
{{page.ieuser}}%nslookup myip.opendns.com resolver1.opendns.com
Server:  resolver1.opendns.com
Address: 208.67.222.222#53

Non-authoritative answer:
Name: myip.opendns.com
Address: 24.133.130.40
```

### Use Ripe.net

Go to ripe search engine and query the ip address [24.133.130.40](https://apps.db.ripe.net/db-web-ui/query?searchtext=24.133.130.40)

### Execute a reverse-DNS lookup over an IP address range

```console
{{page.ieuser}} % nmap -sL 217.68.217.0/24
Starting Nmap 7.92 ( https://nmap.org ) at 2022-08-28 13:28 +03
Nmap scan report for 217.68.217.0
Nmap scan report for 217.68.217.1
Nmap scan report for 217.68.217.2
Nmap scan report for 217.68.217.3
Nmap scan report for ig.com.tr (217.68.217.4)
Nmap scan report for 217.68.217.5
Nmap scan report for 217.68.217.6
Nmap scan report for 217.68.217.7
Nmap scan report for 217.68.217.8
Nmap scan report for igaranti.com.tr (217.68.217.9)
Nmap scan report for 217.68.217.10
Nmap scan report for 217.68.217.11
Nmap scan report for isube.garanti.com.tr (217.68.217.12)
Nmap scan report for isube.assets.garanti.com.tr (217.68.217.13)
Nmap scan report for 217.68.217.14
Nmap scan report for 217.68.217.15
Nmap scan report for 217.68.217.16
Nmap scan report for 217.68.217.17
Nmap scan report for 217.68.217.18
Nmap scan report for 217.68.217.19
Nmap scan report for www.garantibbvasakla.com (217.68.217.20)
Nmap scan report for 217.68.217.21
Nmap scan report for 217.68.217.22
Nmap scan report for 217.68.217.23
Nmap scan report for 217.68.217.24
Nmap scan report for www.garantibank.ro (217.68.217.25)
Nmap scan report for 217.68.217.26
Nmap scan report for 217.68.217.27
Nmap scan report for 217.68.217.28
Nmap scan report for 217.68.217.29
Nmap scan report for 217.68.217.30
Nmap scan report for csb.garanti.com.tr (217.68.217.31)
Nmap scan report for wap3.garanti.com.tr (217.68.217.32)
Nmap scan report for 217.68.217.33
Nmap scan report for drws.garanti.com.tr (217.68.217.34)
Nmap scan report for msube.garanti.com.tr (217.68.217.35)
Nmap scan report for msubeassets.garanti.com.tr (217.68.217.36)
Nmap scan report for igr.garanti.com.tr (217.68.217.37)
Nmap scan report for 217.68.217.38
Nmap scan report for 217.68.217.39
Nmap scan report for 217.68.217.40
Nmap scan report for 217.68.217.41
Nmap scan report for 217.68.217.42
Nmap scan report for 217.68.217.43
Nmap scan report for 217.68.217.44
Nmap scan report for 217.68.217.45
Nmap scan report for 217.68.217.46
Nmap scan report for 217.68.217.47
Nmap scan report for 217.68.217.48
Nmap scan report for 217.68.217.49
Nmap scan report for 217.68.217.50
Nmap scan report for 217.68.217.51
Nmap scan report for 217.68.217.52
Nmap scan report for 217.68.217.53
Nmap scan report for 217.68.217.54
Nmap scan report for 217.68.217.55
Nmap scan report for 217.68.217.56
Nmap scan report for 217.68.217.57
Nmap scan report for 217.68.217.58
Nmap scan report for 217.68.217.59
Nmap scan report for 217.68.217.60
Nmap scan report for 217.68.217.61
Nmap scan report for assets.garantibbva.com.tr (217.68.217.62)
Nmap scan report for 217.68.217.63
Nmap scan report for 217.68.217.64
Nmap scan report for 217.68.217.65
Nmap scan report for 217.68.217.66
Nmap scan report for 217.68.217.67
Nmap scan report for 217.68.217.68
Nmap scan report for 217.68.217.69
Nmap scan report for 217.68.217.70
Nmap scan report for 217.68.217.71
Nmap scan report for 217.68.217.72
Nmap scan report for 217.68.217.73
Nmap scan report for 217.68.217.74
Nmap scan report for 217.68.217.75
Nmap scan report for 217.68.217.76
Nmap scan report for 217.68.217.77
Nmap scan report for subeform-j8.garanti.com.tr (217.68.217.78)
Nmap scan report for subeformonay-j8.garanti.com.tr (217.68.217.79)
Nmap scan report for 217.68.217.80
Nmap scan report for 217.68.217.81
Nmap scan report for 217.68.217.82
Nmap scan report for publicwebsite.garantibbva.com.tr (217.68.217.83)
Nmap scan report for 217.68.217.84
Nmap scan report for 217.68.217.85
Nmap scan report for 217.68.217.86
Nmap scan report for 217.68.217.87
Nmap scan report for 217.68.217.88
Nmap scan report for 217.68.217.89
Nmap scan report for 217.68.217.90
Nmap scan report for sso.garantibank.ro (217.68.217.91)
Nmap scan report for 217.68.217.92
Nmap scan report for 217.68.217.93
Nmap scan report for 217.68.217.94
...
Nmap scan report for 217.68.217.251
Nmap scan report for 217.68.217.252
Nmap scan report for 217.68.217.253
Nmap scan report for isubebeta.garanti.com.tr (217.68.217.254)
Nmap scan report for 217.68.217.255
Nmap done: 256 IP addresses (0 hosts up) scanned in 0.39 seconds
```

### Just another example for starters

```console
{{page.ieuser}}  % sudo nmap -sS -A -T4 -PS22,80,53,443 ns2.turkiye.gov.tr 
Starting Nmap 7.92 ( https://nmap.org ) at 2022-08-28 13:53 +03
sendto in send_ip_packet_sd: sendto(7, packet, 60, 0, 94.55.118.8, 16) => Protocol wrong type for socket
Offending packet: TCP 192.168.68.109:42986 > 94.55.118.8:53 S ttl=59 id=6372 iplen=15360  seq=3727007166 win=63 <mss 1400,wscale 0,sackOK,timestamp 4294967295 0,eol>
sendto in send_ip_packet_sd: sendto(7, packet, 60, 0, 94.55.118.8, 16) => Protocol wrong type for socket
Offending packet: TCP 192.168.68.109:42987 > 94.55.118.8:53 S ttl=56 id=25182 iplen=15360  seq=3727007167 win=4 <timestamp 4294967295 0,nop,nop,wscale 5,nop,mss 640>
sendto in send_ip_packet_sd: sendto(7, packet, 56, 0, 94.55.118.8, 16) => Protocol wrong type for socket
Offending packet: TCP 192.168.68.109:42988 > 94.55.118.8:53 S ttl=50 id=53500 iplen=14336  seq=3727007168 win=4 <sackOK,timestamp 4294967295 0,wscale 10,eol>
sendto in send_ip_packet_sd: sendto(7, packet, 60, 0, 94.55.118.8, 16) => Protocol wrong type for socket
Offending packet: TCP 192.168.68.109:42989 > 94.55.118.8:53 S ttl=57 id=11181 iplen=15360  seq=3727007169 win=16 <mss 536,sackOK,timestamp 4294967295 0,wscale 10,eol>
sendto in send_ip_packet_sd: sendto(7, packet, 56, 0, 94.55.118.8, 16) => Protocol wrong type for socket
Offending packet: TCP 192.168.68.109:42990 > 94.55.118.8:53 S ttl=43 id=41702 iplen=14336  seq=3727007170 win=512 <mss 265,sackOK,timestamp 4294967295 0>
sendto in send_ip_packet_sd: sendto(7, packet, 60, 0, 94.55.118.8, 16) => Protocol wrong type for socket
Offending packet: TCP 192.168.68.109:42991 > 94.55.118.8:53 S ttl=39 id=21759 iplen=15360  seq=3727007165 win=1 <wscale 10,nop,mss 1460,timestamp 4294967295 0,sackOK>
sendto in send_ip_packet_sd: sendto(7, packet, 60, 0, 94.55.118.8, 16) => Protocol wrong type for socket
Offending packet: TCP 192.168.68.109:42992 > 94.55.118.8:53 S ttl=43 id=24094 iplen=15360  seq=3727007165 win=63 <mss 1400,wscale 0,sackOK,timestamp 4294967295 0,eol>
sendto in send_ip_packet_sd: sendto(7, packet, 60, 0, 94.55.118.8, 16) => Protocol wrong type for socket
Offending packet: TCP 192.168.68.109:42993 > 94.55.118.8:53 S ttl=37 id=50091 iplen=15360  seq=3727007165 win=4 <timestamp 4294967295 0,nop,nop,wscale 5,nop,mss 640>
sendto in send_ip_packet_sd: sendto(7, packet, 56, 0, 94.55.118.8, 16) => Protocol wrong type for socket
Offending packet: TCP 192.168.68.109:42994 > 94.55.118.8:53 S ttl=43 id=39244 iplen=14336  seq=3727007165 win=4 <sackOK,timestamp 4294967295 0,wscale 10,eol>
sendto in send_ip_packet_sd: sendto(7, packet, 60, 0, 94.55.118.8, 16) => Protocol wrong type for socket
Offending packet: TCP 192.168.68.109:42995 > 94.55.118.8:53 S ttl=40 id=24496 iplen=15360  seq=3727007165 win=16 <mss 536,sackOK,timestamp 4294967295 0,wscale 10,eol>
Omitting future Sendto error messages now that 10 have been shown.  Use -d2 if you really want to see them.
Nmap scan report for ns2.turkiye.gov.tr (94.55.118.8)
Host is up (0.033s latency).
Not shown: 998 filtered tcp ports (no-response)
PORT    STATE  SERVICE VERSION
53/tcp  open   domain  (unknown banner: BIND)
| dns-nsid: 
|_  bind.version: BIND
| fingerprint-strings: 
|   DNSVersionBindReqTCP: 
|     version
|     bind
|_    BIND
113/tcp closed ident
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port53-TCP:V=7.92%I=7%D=8/28%Time=630B4948%P=arm-apple-darwin21.1.0%r(D
SF:NSVersionBindReqTCP,3F,"\0=\0\x06\x85\0\0\x01\0\x01\0\x01\0\0\x07versio
SF:n\x04bind\0\0\x10\0\x03\xc0\x0c\0\x10\0\x03\0\0\0\0\0\x05\x04BIND\xc0\x
SF:0c\0\x02\0\x03\0\0\0\0\0\x02\xc0\x0c");
Aggressive OS guesses: Fortinet FortiGate-50B or 310B firewall (90%), Fortinet FortiGate-60B or -100A firewall (89%), Motorola SURFboard SB3100 cable modem (VxWorks 5.3) (89%), Fortinet FortiGate 100D firewall (88%), Fortinet FortiGate 1500D firewall (88%), Orange Livebox wireless DSL router or Sagem F@st 334 or 3304 DSL router (88%), Polycom SoundPoint IP 331 VoIP phone (88%), Sagem F@st 3302 DSL router (88%), Adtran NetVanta 1224R or 3430 router (87%), Adtran Total Access 904 router (87%)
No exact OS matches for host (test conditions non-ideal).
Network Distance: 9 hops

TRACEROUTE (using port 113/tcp)
HOP RTT      ADDRESS
1   17.58 ms 192.168.68.1
2   21.16 ms 192.168.67.1
3   ...
4   31.12 ms 172.25.34.5
5   33.70 ms 212.156.129.157.static.turktelekom.com.tr (212.156.129.157)
6   26.86 ms 00-gayrettepe-xrs-t2-2---00-gayrettepe-sr12e-t3-10.statik.turktelekom.com.tr (81.212.215.38)
7   39.88 ms 06-ulus-xrs-t2-2---00-gayrettepe-xrs-t2-1.statik.turktelekom.com.tr (195.175.170.160)
8   41.19 ms 06-idc-guvenlik-t3-1---06-ulus-xrs-t2-2.statik.turktelekom.com.tr (195.175.173.212)
9   35.13 ms ns2.turkiye.gov.tr (94.55.118.8)

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 47.95 seconds
```

---
layout: post
title:  "10. Proxies and Reverse Proxies"
date:   2021-11-30 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head><style>img[alt=forward-proxy-flow.png] {width: 50%}</style></html>

# What is a proxy?

A proxy sever that sits between the internet communication of a client computer and a web server. Serving as an intermediary, a proxy server redirects internet traffic to its respective destinations while ensuring that neither client is in direct contact of each other. 

During traditional internet communication the user's IP address is sent to the client in order to authenticate our we requests. In a forward proxy, our proxy servers sit in front of clients and make requests on behalf of them. 


![forward-proxy-flow](/images/forward-proxy-flow.png)

# What is a reverse proxy?

reverse proxies fulfill requests for clients by connecting to servers
proxy sits in front of servers

![reverse-proxy-flow](/images/reverse-proxy-flow.png)

benefits
- load balancing
- protection from attacks
- caching
- ssl encryption 

## Who needs proxies and why do we need them?

Security 

![proxy-configuration](proxy-configuration) 
<!-- this is the one that clearly shows u that a the proxy's ip is sent not urs uwu -->

Webserver
webservers process data with source code
whereas a proxy is a middleman 

VPN
the usage of proxies may be similar to using a VPN bbbbBUT

![proxy-concept](/images/proxy-concept.png)

it gives 
1. functionality
2. security
3. privacy

uses
- monitoring and filtering
- bypassing flters and censorship
- improving performance
- translation ??
- repairing errors
- accessing services anonymously
- security
- malicious usages 

# References

Proxy Server [https://en.wikipedia.org/wiki/Proxy_server](https://en.wikipedia.org/wiki/Proxy_server)

What is a Proxy Server and How Does It Work?[https://www.avg.com/en/signal/proxy-server-definition](https://www.avg.com/en/signal/proxy-server-definition)

https://whatismyipaddress.com/proxy-server
https://www.upguard.com/blog/proxy-server 

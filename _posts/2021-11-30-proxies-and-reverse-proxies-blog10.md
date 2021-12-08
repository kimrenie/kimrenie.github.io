---
layout: post
title:  "10. Proxies and Reverse Proxies"
date:   2021-11-30 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head><style>img[alt=forward-proxy-flow.png] {width: 50%}</style></html>

# What is a proxy?

The definition of a `proxy` is the authority to act for another thing or person. In this sense, a proxy takes on the responsibilities of whatever thing it is attached to. Taking this definition, a proxy sever sits between the internet communication of a client computer and a web server and serves as a gate between the the client and the internet. This gate has the responsibility of redirecting internet traffic to its respective destinations while ensuring that neither client is able to directly contact each other. 

![forward-proxy-flow](/images/forward-proxy-flow.png)

During traditional internet communication the user's IP address is sent to the client in order to authenticate our we requests. Without a proxy server, your personal IP address is exposed both for the intended server and for any other server to access as well. In a forward proxy, our proxy servers sit in front of clients and forwards requests on behalf of them. Because of this, the proxy server's IP address is sent to the intended web server rather than the client's. The proxy server also receives the main server's responses and forwards them back to the client. This workflow ensures confidentiality and security for the client by serving as the only point of access between these two entities, effectively masking each other's IP addresses from each other. 

![proxy-concept](/images/proxy-concept.png)

![proxy-configuration](proxy-configuration) <!-- this pic shows unique ip -->

# What is a reverse proxy?

Opposite from a forward proxy, a reverse proxy sits in front of web servers and serves as the server's representative when it comes to sending a receiving requests and data. These reverse proxies fulfill requests for clients on behalf of the servers.

![reverse-proxy-flow](/images/reverse-proxy-flow.png)

## Who needs proxies and why do we need them?

Proxies are more commonly used by entities such as large organizations, businesses, and public networks (such as public schools or public libraries). Using this would allow specific users in these networks to access exclusive information and sites (An example of this would be a sports fan with a paid subscription to stream sports games, etc.). 

Some of the benefits of using a proxy server include:
- The ability to control content to certain groups of people. A parent would be able to restrict certain websites for their children or a limit their internet use in total.
- Security that comes from protecting web requests and the responces that are sent back. 
- The ability to cache frequently used websites in order to better the server's performance and speed. 
- etc. 

Some of the risks of using a proxy server include:
- Proxy instability due to multiple users using the service at the same time. 
- Slow server speeds due to multiple users using the service at the same time. 
- Poor security due to a proxy's inability to encrypt web traffic. 
- etc.

# References

Proxy Server [https://en.wikipedia.org/wiki/Proxy_server](https://en.wikipedia.org/wiki/Proxy_server)

What is a Proxy Server and How Does It Work?[https://www.avg.com/en/signal/proxy-server-definition](https://www.avg.com/en/signal/proxy-server-definition)

3 (https://whatismyipaddress.com/proxy-server)[https://whatismyipaddress.com/proxy-server]

4 (https://www.upguard.com/blog/proxy-server)[https://www.upguard.com/blog/proxy-server] 

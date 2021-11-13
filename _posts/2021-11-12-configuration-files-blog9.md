---
layout: post
title:  "9. Apache Configuration Files"
date:   2021-11-12 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head><style></style></html>

# What is the Main Configuration File

REPHRASE LATER Apache HTTP Server is configured by placing directives in plain text configuration files. The main configuration file is usually called httpd.conf. 

Relevant Directives:
```
<IfDefine>
Include
TypesConfig
```

# Syntax

```
<Directory>
<DirectoryMatch>
<Files>
<FilesMatch>
<Location>
<LocationMatch>
<VirtualHost>
```

Virtual Hosting is the ability for httpd to server multiple websites simultaneously.

# Modules

Relevant Directives
```
<IfModule>
LoadModule
```

# .htaccess Files

This was addressed in the previous blog. In short, an .htaccess file is short for a distributed configuration file and it is a secondary configuration file that allows specified management for certain files and webpages. 

![apache-ht-access](/images/apache-ht-access.jpg)

# References

Configuration Files [https://httpd.apache.org/docs/2.4/configuring.html](https://httpd.apache.org/docs/2.4/configuring.html)
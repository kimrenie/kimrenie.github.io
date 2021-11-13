---
layout: post
title:  "8. The .htaccess File"
date:   2021-11-09 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head><style></style></html>

# What is the .htaccess file?

![apache-ht-access](/images/apache-ht-access.jpg)

An `.htaccess file` is known as a "distributed configuration file" and is used in order to give the user the ability to make configuration modifications depending on current working directory. During user web requests, the Apache Web Server first detects this configuration file and executes the directives found inside of it. Such as other Apache configuration files, the .htaccess file is read from top to bottom

The syntax that is used in an .htaccess file is identical to the syntax used in your server's main configuration file. In order for these directives to be utilized in this additional config file, the user must remember to utilize an `AllowOverride` in the default host configuration file. 

```
<Directory /var/www/html>
    Options Indexes FollowSymLinks
    AllowOverride All
<Directory>
```

This directive will be honored once the user restarts the Apache service with the `sudo systemctl apache2 restart` command. 

> *NOTE*: <br> In order to customize or refer to your .htaccess file as something else,, its name can be changed by adding the following directive to your server's main configuration file: `AccessFileName ".config"`

# What is the .htaccess file used for?

The .htaccess file contains multiple configuration directives and would be placed in a specific document directory. This placement would allow these directives to apply to that directory and all of its subdirectories. 
This allows the user to customize specific webpage details such as:

- Authentification: used to apply restrictions to certain webpages through the usage of usernames and their accompanying passwords
- URL Rewrites: used to "clean up" messy URL addresses and make it shorter and easier to remember for the consumer
- Custom Errors: used to customize error pages (i.e. `ErrorDocument 404 /custom404.html`)
- etc. 

These customizations would not be applied to the server as a whole thanks to the usage of an .htaccess file. 

# References

.htaccess files [https://httpd.apache.org/docs/2.4/howto/htaccess.html](https://httpd.apache.org/docs/2.4/howto/htaccess.html)

How to Use ... [https://www.digitalocean.com/community/tutorials/how-to-use-the-htaccess-file](https://www.digitalocean.com/community/tutorials/how-to-use-the-htaccess-file)
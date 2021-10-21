---
layout: post
title:  "5. LAMP Stack Basics"
date:   2021-10-21 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head>
<style>
    img {width: 35%}
    img[alt=lamp-stack] {width: 75%}
</style>
</html>

# What is a LAMP stack?

LAMP is an acronym that stands for Linux, Apache, MySQL, and PHP. These four elements make up softwares that interact with each other in order to create and deliver high-performance web applications. The LAMP stack is one of the most commonly used set of softwares used and is regarded as an industry standard because of it is an open source technology, is easily accessible, allows for dynamic applications, has been in use for over a decade, etc. 

![lamp-stack](/images/lamp-stack.jpg)

A `stack` is typically composed of four softwares:
- OS (Operating System)
- Web Server
- Database
- Programming Language

These softwares work together and serve as a foundation for an unlimited number of services and applications. Stacks are generally named with an acronym that represents the softwares it contains. Alternatives to our LAMP stack could be stacks such as WAMP (Windows, Apache, MySQL, PHP), WISA (Windows, IIS, SQL, ASP.net), etc.

Our LAMP stack consists of the following: 

# (L) Linux
![linux-icon](/images/linux-icon.png)

Linux is the operating system layer of our stack and actively supports the other softwares during the application development process. Linux is an open-source collaboration and has multiple different distributions (Ubuntu, Debian, CentOS, etc.) that are able to fulfill multiple different developer's needs. 


# (A) Apache

![apache-icon](/images/apache-icon.png)

Apache servers as the web server layer of our stack. It is widely recognized because it is actively supporting over half of all the websites served on the Internet. All interaction with our webserver actually starts with the web server layer as Apache receives HTTP requests to load up our website's web pages. These requests are passed on to the following two layers (the database and the programming language).

# (M) MySQL
![mysql-icon](/images/mysql-icon.png)

MySQL serves as the database layer of our stack which hosts our open-source relational database management system. After a web request has been made, MySQL works with the programming language in order to identify the data required for the specific web page. 

# (P) PHP
![php-icon](/images/php-plush.jpg)

PHP serves as the final layer of our stack which serves as our main programming language. This language is a hypertext preprocessor that functions with our Apache web server in order to combine all of our stack elements for our final web application deployment. After a web request has been made, PHP interacts with the database layer in order to fetch data that has been identified in it's code. Once this is done successfully, all of the relevant data and code is passed back to the Apache web server to be served to the user's web browser that initially sent in a request. 

These four softwares interact and rely on each other in order to serve the relevant data for a web application :)

# References

IBM LAMP stack [https://www.ibm.com/cloud/learn/lamp-stack-explained](https://www.ibm.com/cloud/learn/lamp-stack-explained)
What is? [https://stackify.com/what-is-lamp-stack/](https://stackify.com/what-is-lamp-stack/)
---
layout: post
title:  "7. PHP Basics"
date:   2021-11-05 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head><style>img {width: 50%}</style></html>

# What is PHP

PHP stands for Personal Home Page in its initial form. However, it is currently known as a Hypertext Preprocessor. PHP is a server-side language that is considered to be a platform that supports backend scripting. It may be easily misunderstood as a front-end language because, even though they are two seperate languages, HTML may be embeded within PHP code in order to improve the formating and ensure that the pages are user-friendly. This may be done by creating a normal HTML document with regular html tags ( `<html></html>` ) and whenever the developer wants to implement PHP functionality, this code can be inserted in the middle of out HTML code (anywhere and at multiple places) with the usage of PHP tags (< `?php php-code-here ?>` )

Below is an example of this integration.

```
<html> 
 <title>HTML + PHP</title>
 <body>
 <h1>HTML Code in a header1 tag</h1>

 <?php
// Heyo! Your desired PHP code and its functionscan go here!
?>

 <b>HTML in a body tag</b>

 <?php
 // they can also go here! Anywhere you want! :)
 ?>

 </body>
 </html>
```

PHP is able to perform server-side scripting and command-line scripting. Server-side scripting allows for a developer to create websites and web applications with dynamic features whereas xommand-line scripting allows developers to perform several different administrative tasks and duties. PHP is able to communicate with the web through a series of three steps. First, the user's browser sends an HTTP request for a particualr file to its corrosponding server. Secondly, the PHP preprocessor, which is installed on the web server, converts PHP code into HTML. Lastly, our server approves the request and sends an HTTP response of a succesfully generated HTML document back to the web browser.

![php-diagram](/images/php-diagram.png)

# Advantages of PHP

PHP is a cross-platform language has been in use ever since 1994 . The major Operating Systems that support PHP functionality include MacOS, Linux, and Windows. It is also supported by major web servers including Apache and Nginx. PHP also supports multiple databases such as Oracle Database, MySQL, MongoDb, and more!

# References

PHP Tutorial [https://www.phptutorial.net/php-tutorial/what-is-php/](https://www.phptutorial.net/php-tutorial/what-is-php/)

Back-end [https://licreativetechnologies.com/blog/is-php-frontend-or-backend/](https://licreativetechnologies.com/blog/is-php-frontend-or-backend/)

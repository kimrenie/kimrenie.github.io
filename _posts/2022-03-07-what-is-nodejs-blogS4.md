---
layout: post
title:  "S4. What is Node.js?"
date:   2022-03-07 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head><style>img {width: 75%}</style></html>

# What is Node.js?

![node](/images/node.png)

Node.js was initially released in 2009 and is a back-end runtime environment that allows developers to create and run JavaScript code/scripts in order to create dynamic web pages. 

One of the big benefits of using Node is the ability to use a single programming language across an entire project in terms of server-side and client side accessibility. Examples of large companies that make use of Node.js include: LinkedIn, Microsoft, PayPal, etc.

> Node can be installed from the following source: https://nodejs.org/en/download/

There are three different kinds of modules that can be used in accordance with Node.js. These are named core modules, local modules, and third party modules.

# Core Modules

The following is a list of built-in modules that can be found on Node.js:

```
assert
buffer
child_process
cluster
crypto
dgram
dns
domain
events
fs
http
https
net
os
path
punycode
querystring
readline
stream
string_decoder
timers
tls
tty
url
util
v8
vm
zlib
```

A core module can be easily integrated into your code through the usage the `require()` function. 

> *Example:* 
    
    const http = require('http');
    var server = http.createServer(function(req, res){ 
        console.log( "did it ( •̀ ω •́ )✧ nice" );
    });
    server.listen(3000);


# Local Modules

A local module is essentially a custom-made module that is defined by the user and is found within the folders that the modules is specifically going to be used for.

> Depending on the developer, a locally created module has the potential to become a third party module if the developer chooses to share their work to the Node.js community.

 # Third Party Modules

 A third party module is a module that was created by a third party and can be utilized after downloading them with NPM (Node Package Manager). These modules have the option of being installed within wither the application's project folder or globally installed.

 The commands to install these kinds of modules can be seen bellow

 ```
 npm install -g module_name
 npm install --save module_name
 // one at a time

 npm install --save module_name_2 module_name_3 module_name_4
 // multiple at once
```
 
# References

Wikipedia [https://en.wikipedia.org/wiki/Node.js](https://en.wikipedia.org/wiki/Node.js)

Node [https://nodejs.dev/learn](https://nodejs.dev/learn)

IBM [https://developer.ibm.com/tutorials/learn-nodejs-node-basic-concepts/](https://developer.ibm.com/tutorials/learn-nodejs-node-basic-concepts/)

Microsoft [https://docs.microsoft.com/en-us/windows/dev-environment/javascript/nodejs-beginners-tutorial](https://docs.microsoft.com/en-us/windows/dev-environment/javascript/nodejs-beginners-tutorial)

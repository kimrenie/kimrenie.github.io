---
layout: post
title:  "9. Apache Configuration Files"
date:   2021-11-12 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head><style></style></html>

# What is the Main Configuration File

![apache-httpd](/images/apache-httpd.jpg)

The Apache HTTP Server uses directives placed in plain text config files in order to manage configuration. Usually the main configuration file is named httpd.conf. Some of the relevant directives are as follows:
```
<IfDefine></IfDefine>  
Include 
TypesConfig
```
- The `<IfDefine>` directive that is processed only at startup (when conditions are true).
- The `Include` directive allows other configuration files to be included with the main server's configuration files. This directive points Apache httpd towards directories rather than to a singular file. 
- The `TypesConfig` directive takes MIME-type (Multipurpose Internet Mail Extension) files and sets their configuration file location. 


# Scope

Rather than placing directives into indivudual .htaccess files (as mentioned in the previous blog post), those same directives canbe placed into the server's main configuration file by placing those directions into the following directives:

```
<Directory></Directory>
<DirectoryMatch></DirectoryMatch>
<Files></Files>
<FilesMatch></FilesMatch>
<Location></Location>
<LocationMatch></LocationMatch>
<VirtualHost></VirtualHost>
```

- The `Directory` directive applies directives only to the directory that is named within its tags. (i.e. <Directory path-to-directory> ... </Directory>)
- The `DirectoryMatch` directive has the same functionality as the Directory directive except is uses expressions in order to find teh appropriate directory/files. (Regex is short for regular expressions and is used to find a particular pattern. A simple example of this is using `([A-Z][a-z]*)` in order to find words that start with with a capital and are followed by lowercase letters.)
- The rest of the directives perform similarly.

# .htaccess Files

This was addressed in the previous blog. In short, an .htaccess file is short for a distributed configuration file and it is a secondary configuration file that allows specified management for certain files and webpages. 

![apache-ht-access](/images/apache-ht-access.jpg)

# References

Configuration Files [https://httpd.apache.org/docs/2.4/configuring.html](https://httpd.apache.org/docs/2.4/configuring.html)

Apache Core Features [https://httpd.apache.org/docs/2.4/mod/core.html#directory](https://httpd.apache.org/docs/2.4/mod/core.html#directory)

Terms [https://httpd.apache.org/docs/2.4/mod/directive-dict.html#Context](https://httpd.apache.org/docs/2.4/mod/directive-dict.html#Context)

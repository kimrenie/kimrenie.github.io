---
layout: post
title:  "3. SSH Keys"
date:   2021-10-08 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head></html>

# Setup

My goal for this week's blog was to configure my SSH config file in order to SSH into my university's servers without the need for a password login. At first, I was trying to setup my SSH config file on my laptop in order to work on my assignments from my second device. Before I could even start however, I was encountering errors such as not being able to SSH into CSUN's servers at all.

![wrong host key](/images/wrong-host-key.png)

I attempted to read up more on the subjects that were brought up in the error message. The following line was the most relevant to my issue:
```
... 
Offending RSA key in /c/Users/Kimberly/.ssh/known_hosts:1
RSA host key for ssh.csun.edu has changed ...
```
From reading this section of my error, I was able to determine that my device was reading a host key that I had previously saved years ago throughout my classes and labs performed at CSUN. Deleting this saved line (line 1) from my `known_hosts` file stopped my device from reading outdated data and allowed my new connection to add to my known_hosts file.

The known_hosts file can be found within the `.ssh` folder on your device (this location is owned by the root user).

# SSH Keys

In order to configure an automated SSH login, the concept of SSH keys need to be understood. 

A `host key` is a unique identifier that allow computers to be authenticated throughout the SSH protocol. These host keys are typically automatically generated during the initial installation of OpenSSH. 


> **Note:** Additional keys are able to be produced through tools such as `ssh-keygen`.


An SSH key is synonymous to a password credential. They function and are able to provide security similarly to passwords, however they are classified underneath cryptography. Two significant concepts within key cryptosystems are cryptography algorithms (RSA, DSA, ECDSA) and key pairs.

## Key Pairs

 An SSH key pair generates a public key and a private key. The `private key` is meant to stay with the user and serves as an identifier. The `public key` is meant to be shared to the SSH servers that the user wishes to connect to. After this key has successfully allowed allowed a user to login, this key is deemed as trustworthy and is added to the server's authorized_keys file.

# SSH Authentication

A successful SSH connection includes:
    - the usage of a session key in order to encrypt the session
    - authenticating the server host with the use of the host key
    - authenticating the client through the use of their password, public key authentication, etc.

![ssh authentication](/images/ssh-authentication.png)

The following blog post will cover my process with public key authentication.

---
## References
https://www.digitalocean.com/community/questions/warning-remote-host-identification-has-changed
https://www.ssh.com/academy/ssh/host-key
https://www.ssh.com/academy/cryptography/public-key
https://www.ssh.com/academy/ssh/key
http://www.phys.ufl.edu/hee/cms/emu/fast/FAST-DAQ/ssh_between_2.html
https://www.ssh.com/academy/ssh/public-key-authentication
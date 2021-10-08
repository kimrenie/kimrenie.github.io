---
layout: post
title:  "4. SSH Config File"
date:   2021-10-06 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head></html>

# SSH Config File Basics

- SSH Keys

- Enable SSH services
- Generate SSH key pairs
- 
- Host Key???????

frm here i did that the youtube video told me toooooo dooooo

aka scp the public key into .ssh/authorized_keys
- write
- out
- the
- commands


# Files
```
~/.ssh/config
/etc/ssh/ssh_config
```

# Keywords
```
Host
EnableSSHKeysign
HostKeyAlias
HostName
User
```

# Permissions

![wrong key permissions](/images/wrong-key-permissions)

images wrong-key-permissions

chmod 600 to the file

# optional title: SSH Login (Automated) 
# maybe : Remote Machine Auto Login
^^^^ maybe this is the blog for next week


## References
https://linuxhint.com/ssh-config-file/
lol https://www.reddit.com/r/linuxquestions/comments/ng8mq0/when_using_ssh_keys_can_you_use_the_same_keys_on/gypm2d6/
lol 2 https://www.linuxquestions.org/questions/linux-security-4/using-a-public-ssh-key-on-more-than-one-user-942094/
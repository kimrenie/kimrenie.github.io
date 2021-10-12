---
layout: post
title:  "4. SSH Config File"
date:   2021-10-12 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head></html>

# Key Generation

After generating a key pair with a service such as `ssh-keygen` a private key and a public key should be created within your .ssh directory. This can be generated with a command and the process will look like the following:
```
ssh-keygen -t rsa -b 4096 user@homemachine
Generating public/private rsa key pair.
Enter file in which to save the key (/home/user/.ssh/id_rsa):  /home/user/.ssh/id-rsa
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/user/.ssh/something-rsa
Your public key has been saved in /home/user/.ssh/something-rsa.pub.
The key fingerprint is: ...
```

As seen above, your `identification` is your private key which should never be shared with other whereas your `public key` is saved with a `.pub` extension and is meant to be distributed to the services that you wish to connect to. This key is used for authentication when connecting to other servers.

# Remote Server authorized_keys File

After these keys have been successfully generated, the user needs to ssh into the desired server. At this point there should either be a file named `authorized_keys` or the user can create this file manually. At this point, the public_key that was generated earlier needs to be copied into this file. 

![server-ssh-directory](/images/server-ssh-directory.png)

This key can be copied with commands such as using the `cat` command and appending the output to the authorized_keys folder,
```
$ cat id_rsa.pub >> .ssh/authorized_keys
```
with an sshd tool such as `ssh-copy-id` (*this option configures the necessary permissions for you*), 
```
 $ ssh-copy-id -i /home/user/.ssh/server-rsa.pub user@server
```
or with a command such as `scp` the public key into .ssh/authorized_keys
```
$ scp -r /local/directory/ username@server:/remote/directory/
```
## Permissions

Before I was able to add my ssh key to my desired server, I encountered the following error: 

![wrong key permissions](/images/wrong-key-permissions.jpg)

This error displayed the fact that my private key was potentially exposed. Performing a `chmod 600` to the files in question was able to fix the security issue.

# SSH Automated Login (Config File)

After your ssh key has been successfully added to the remote server, the following steps need to be performed onto your local device in order to automate your ssh connections. Within your .ssh directory, a configuration file must be made with *at least* the following format:
```
Host server-name
    Hostname actual-server-name
    User client-username
    IdentityFile ~/.ssh/id_rsa
```
> **Note:** Once your key has been verified at least once, it is safe enough to disable password authentication in sshd by adding the following line to your config file `PasswordAuthentication no`. After this addition restart your sshd with `sudo systemctl restart sshd`.

After following all of these steps you should be able to have an automated login when using ssh to login to your desired remote servers.

# References

SSH Keys [https://www.reddit.com/r/linuxquestions/comments/ng8mq0/when_using_ssh_keys_can_you_use_the_same_keys_on/gypm2d6/](https://www.reddit.com/r/linuxquestions/comments/ng8mq0/when_using_ssh_keys_can_you_use_the_same_keys_on/gypm2d6/)

SSH Keys 2 [https://www.linuxquestions.org/questions/linux-security-4/using-a-public-ssh-key-on-more-than-one-user-942094/](https://www.linuxquestions.org/questions/linux-security-4/using-a-public-ssh-key-on-more-than-one-user-942094/)

General Issues [https://askubuntu.com/questions/871751/cant-ssh-even-with-public-key-added-to-authorized-keys](https://askubuntu.com/questions/871751/cant-ssh-even-with-public-key-added-to-authorized-keys)

Config file basics [https://linuxhint.com/ssh-config-file/](https://linuxhint.com/ssh-config-file/)

Config file format [https://www.ssh.com/academy/ssh/config](https://www.ssh.com/academy/ssh/config)
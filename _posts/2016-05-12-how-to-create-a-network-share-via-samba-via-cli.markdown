---
layout: post
title: How to Create a Network Share Via Samba Via CLI
categories: [tech]
tags: [ubuntu, samba]
published: True
comments: True
---

```bash
sudo apt-get install samba
sudo smbpasswd -a <user_name>

sudo vim /etc/samba/smb.conf
[<folder_name>]
path = /<path>/<folder_name>
valid users = <user_name>
read only = no

sudo service smbd restart
testparm
sudo apt-get install smbclient
smbclient -L //<HOST_IP_OR_NAME>/<folder_name> -U <user_name>
```

[1]: https://help.ubuntu.com/community/How%20to%20Create%20a%20Network%20Share%20Via%20Samba%20Via%20CLI%20(Command-line%20interface/Linux%20Terminal)%20-%20Uncomplicated,%20Simple%20and%20Brief%20Way!

[2]: http://www.digitalcitizen.life/how-access-ubuntu-shared-folders-windows-7

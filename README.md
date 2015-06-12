# SSH-issue-in-New-Ubuntu-installations

In certain kernel versions for Ubuntu 14.04, SSH was not working in or out of the machine. Moreover, SSH was not even installed. 

Installation of OpenSSH-Server was also throwing errors stating the package was not found.

To go around this issue, do the following:

sudo apt-get remove openssh-client

sudo apt-get update

sudo apt-get install openssh-server

This should solve the issue. The command to open port 22 is as follows:

sudo iptables -I INPUT -p tcp --dport 22 -j ACCEPT

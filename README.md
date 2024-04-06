# SSH LUKS Access
How to login to a remote linux server with a full disk encryption.

## The Problem
I needed to find a way to access to my home server in local network without physically interact with it every time it was rebooted.

The boot block is encrypted with LUKS (Linux Unified Key Setup), a set of tools for managing the encrypted devices, wich forced me to enter the master key if I wanted to decrypt it, but the server is hide form the view (I'm not live in a office, so I don't want to see all the backend stuff I own) so I had to reach the server, connected the keyboard, pulled out the the HDMI cable only for insert the password. so anoying. 

## The solution
I choose the [Matt Johnson](https://matt.ucc.asn.au/dropbear/dropbear.html)'s software [Dropbear](https://github.com/mkj/dropbear), a lightwight Secure Shell-compatible (SSH2) server and client written in C.

## The Setup
### Server
A low TDP x86 SBC with Ubuntu Server 23.04.4 LTS in a dedicated VLAN.

### Client
Debian-based distro VM.

### Software
- openssh-server
- dropbear-initramfs
- text editor (vi, vim, nano, etc.)

## The procedures

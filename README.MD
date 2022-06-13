# Headless Factorio setup on CentOS 8 Stream.

A quick guide for how to setup and configure a Factorio headless server on a CentOS 8 Stream container. I am running my container on Proxmox, so milage may vary depending your platform.

In essence, this guide aims to cover some setup requirements of CentOS8 and then downloads the server files and installs them. This might also cover some networking elements if I feel like it.

## Prerequites

### Install tar and curl

Easy one! `dnf install tar curl -y`\
You can easily test that they installed correctly with `tar --version` and `curl --version`\
Also this allows you to remotely connect with VScode.\

### Install and enable SSH

Assuming you have a freshly installed CentOS 8 Stream server:

Start with updating your system packages:
```bash
dnf makecache
dnf upgrade
dnf install openssh-server
```

Start the SSH daemon
`systemctl start sshd`\
`systemctl enable sshd`\

Check everything is running:
`systemctl status sshd`\

It's highly recommended you exchange your public SSH key for ease of login.\

## Links

Factorio download page: https://www.factorio.com/download \

Link that re-directs to the lastest server version: https://factorio.com/get-download/stable/headless/linux64
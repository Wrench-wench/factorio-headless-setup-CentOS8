### Headless Factorio setup on CentOS 8 Stream.

## Prerequites

# Install tar

Easy one! `dnf install tar`
Also this allows you to remotely connect with VScode.

# Install and enable SSH

Assuming you have a freshly installed CentOS 8 Stream server:

Start with updating your system packages:
```bash
dnf makecache
dnf upgrade
dnf install openssh-server
```

Start the SSH daemon
`systemctl start sshd`
`systemctl enable sshd`

Check everything is running:
`systemctl status sshd`

It's highly recommended you exchange your public SSH key.
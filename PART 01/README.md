# Linux Practice - Part 1: Basic Commands & User Management

## Overview

This document summarizes the Linux commands I practiced while preparing for the Linux Master Level 2 certification using Ubuntu 24.04.4 LTS running on UTM (Apple Silicon).

---

## Environment

- OS: Ubuntu 24.04.4 LTS (ARM64)
- Virtual Machine: UTM
- Host: MacBook Pro (Apple M4)
- Access Method: SSH

---

# SSH Connection

Connected to Ubuntu from macOS Terminal using SSH.

```bash
ssh jiyeonseo@192.168.64.5
```

---

# Command Practice

## 1. Command Location

Locate executable files.

```bash
which pwd
```

Result

```
/usr/bin/pwd
```

---

## 2. Alias

Create and remove aliases.

```bash
alias ll='ls -la'
ll
unalias ll
```

---

## 3. Environment Variables

Display PATH and shell prompt.

```bash
echo $PATH
echo $PS1
```

---

## 4. Manual Pages

View Linux documentation.

```bash
man ls
manpath
whatis ls
whereis ls
apropos system
```

---

## 5. Password Management

Check password status.

```bash
passwd -S jiyeonseo
```

Set root password.

```bash
sudo passwd root
```

---

## 6. Switch User

Become the root user.

```bash
su -
```

Return to normal user.

```bash
exit
```

Difference:

- `su -` switches to the root user's environment.
- `su root` switches the user only.

---

## 7. User Configuration

View default settings for new users.

```bash
cat /etc/default/useradd
```

---

## 8. User Database

Display user account information.

```bash
tail /etc/passwd
```

---

## 9. Group Database

Display all groups.

```bash
cat /etc/group
```

---

## 10. Group Management

Create and delete groups.

```bash
sudo groupadd jys
sudo groupdel jys
```

---

## 11. Logged-in Users

Display current users.

```bash
users
who
who -r
who -b
who -q
w
```

---

## 12. User Information

Display UID, GID, and group membership.

```bash
id
groups
```

---

# Key Concepts Learned

- SSH remote login
- Linux manual system
- Environment variables
- Alias management
- Root account
- User switching
- User and group databases
- User and group management
- Logged-in user information
- Linux account permissions

---

# Commands Practiced

- ssh
- which
- alias
- unalias
- echo
- man
- manpath
- whatis
- whereis
- apropos
- passwd
- sudo
- su
- cat
- tail
- groupadd
- groupdel
- users
- who
- w
- id
- groups

---

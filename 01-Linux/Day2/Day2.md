# DAY 2 OF LINUX FOR CLOUD ENGINEERING

## BASIC COMMANDS OF SYSTEM

### HEADLINE

Hello, my name is Muhammad Afzaal Khan, and this is my **Day 2 of learning Linux**.

I write this file by myself while watching tutorials. I write every command in my own simple language so I can understand it easily.

First, I do the practice myself. After that, I give my notes to ChatGPT to correct the spelling, grammar, and format. Then I copy the final version and upload it to **GitHub and LinkedIn**.

### EXTRA MATERIAL

I also added some extra commands and information that I learned during my practice.

---

## 1. `who` / `whoami`

`who` and `whoami` are different.

* `who` → Shows the users currently active/logged into the system.
* `whoami` → Shows the username of the current user.

**Simple difference:**
`who` = Who is using/logged into the system?
`whoami` = Who am I?

---

## 2. `which`

`which` is used to find the location/path of a command.

Example:

```bash
which ls
```

---

## 3. `uname`

`uname` is used to find information about the Linux system and kernel.

For example, I am running Kali Linux, so I can use `uname` to get system/kernel information.

```bash
uname
uname -a
```

---

## 4. `uptime`

`uptime` is used to check how long the computer/Linux system has been running.

```bash
uptime
```

---

## 5. `id`

`id` is used to find information about a user, such as:

* User ID (UID)
* Group ID (GID)
* Groups

```bash
id
```

---

## 6. `sudo`

`sudo` is used when a command needs administrator/root privileges.

It allows a permitted user to perform administrative tasks.

Example:

```bash
sudo apt update
```

---

## 7. `shutdown`

`shutdown` is used to shut down the Linux system.

```bash
sudo shutdown now
```

---

## 8. `reboot`

`reboot` is used to restart the Linux system.

```bash
sudo reboot
```

---

## 9. `apt`

`apt` is a package management command used to update, install, remove, and manage software in Linux distributions such as Kali Linux and Ubuntu.

Examples:

```bash
sudo apt update
sudo apt install package-name
```

---

## 10. `apt-get`

`apt-get` is also a package management command used on Debian-based Linux systems.

It can be used for installing, updating, and removing packages.

Example:

```bash
sudo apt-get install package-name
```

---

## 11. `Ctrl + R`

`Ctrl + R` is used to search previously used commands from terminal history.

If I already ran a command and don't want to type it again, I can press:

```text
Ctrl + R
```

Then type a few words from the previous command to find it.

---

## 12. `sudo apt remove`

If I want to remove something such as software or a tool, I can use:

```bash
sudo apt remove package-name
```

Example:

```bash
sudo apt remove nginx
```

---

## 13. `yum`, `portage`, `dnf`, `pacman`

These are package managers used by different Linux distributions.

| Package Manager | Common Linux Distribution  |
| --------------- | -------------------------- |
| `apt`           | Debian, Ubuntu, Kali       |
| `dnf`           | Fedora, RHEL-based systems |
| `yum`           | Older RHEL/CentOS systems  |
| `pacman`        | Arch Linux                 |
| `Portage`       | Gentoo Linux               |

---

# USER MANAGEMENT & GROUP MANAGEMENT COMMANDS

## 1. `useradd -m username`

If I want to add/create a new user, I can use:

```bash
sudo useradd -m username
```

The `-m` option creates a home directory for the new user.

---

## 2. `passwd username`

If I want to add or change a password for a user, I can use:

```bash
sudo passwd username
```

---

## 3. `su`

`su` is used to switch from one user to another.

Example:

```bash
su username
```

---

## 4. `groupadd`

`groupadd` is used to create a new group.

Example:

```bash
sudo groupadd groupname
```

---

## 5. `/etc/passwd` and `/etc/group`

If I want to see information about users, I can use:

```bash
cat /etc/passwd
```

This file contains information about user accounts, including usernames and user IDs.

If I want to see information about groups, I can use:

```bash
cat /etc/group
```

---

## 6. `gpasswd -a`

If I want to add a user to a group, I can use:

```bash
sudo gpasswd -a username groupname
```

---

## 7. `Ctrl + R` for searching commands

If I want to search for a command that I used previously, I can use:

```text
Ctrl + R
```

This searches through the command history.

---

## 8. Add Multiple Users to a Group

If I want to add multiple users to a group, I can use the `-M` option.

Example:

```bash
sudo gpasswd -M user1,user2 groupname
```

---

## 9. `groupdel`

If I want to delete a group, I can use:

```bash
sudo groupdel groupname
```

---

# FILE PERMISSION COMMANDS

## 1. `ls -l` and `chmod`

File permissions are an important concept in Linux.

When I use:

```bash
ls -l
```

I can see permissions such as:

```text
drwxrwxr-x
```

Basic meaning:

```text
d = directory
r = read
w = write
x = execute
```

Permissions are mainly divided into:

```text
User | Group | Others
```

If I want to change file or directory permissions, I can use `chmod`.

Example:

```bash
chmod 777 cloud
```

Here, `777` gives read, write, and execute permissions to the user, group, and others.

---

## 2. `umask`

`umask` is used to control the default permissions of newly created files and directories.

Example:

```bash
umask
```

---

## 3. `chown`

`chown` is used to change the owner of a file or directory.

For example, if my folder name is `LIFE` and I want to change its owner to another user:

```bash
sudo chown username LIFE
```

`sudo` may be required because changing ownership usually needs administrator privileges.

---

## 4. `chgrp`

`chgrp` is used to change the group ownership of a file or directory.

Example:

```bash
sudo chgrp groupname filename
```

---

# COMPRESSION COMMANDS

## 1. `zip` and `unzip`

If `zip` and `unzip` are not installed, I can install them using:

```bash
sudo apt install zip unzip
```

`zip` is used to create compressed ZIP files.

`unzip` is used to extract ZIP files.

---

## 2. `zip`

If I want to put files or a folder into a ZIP file, I can use:

```bash
zip -r archive.zip foldername
```

---

## 3. `tar`

`tar` can be used to create compressed archive files.

Example:

```bash
tar -cvzf cloud.tar.gz cloud
```

Basic meaning:

```text
c = create
v = verbose
z = gzip compression
f = file
```

---

## 4. Extract TAR.GZ File

If I want to extract a `.tar.gz` file, I can use:

```bash
tar -xvzf cloud.tar.gz
```

Basic meaning:

```text
x = extract
v = verbose
z = gzip
f = file
```

---

# FILE TRANSFER COMMANDS

## `vim`

`vim` is a terminal-based text editor.

It can be used to write or edit text inside a file.

Example:

```bash
vim notes.txt
```

---

# FILE TRANSFER

## 1. `scp`

If I want to upload a file from my local computer to a server, I can use `scp`.

`scp` stands for **Secure Copy**.

It can transfer files between:

```text
Local Computer → Server
Server → Local Computer
```

Example:

```bash
scp filename.txt username@server-ip:/path/
```

When working with a cloud server, such as an AWS server, `scp` can be used to transfer files between my local machine and the server.

---

## 2. `rsync`

`rsync` is another command used to transfer and synchronize files between systems.

It is especially useful for transferring directories and keeping files synchronized.

Example:

```bash
rsync -av folder/ username@server:/path/
```

---

# PRACTICE PROOF

I practiced the commands from Day 2 on my Linux system.

**Practice Screenshot:**

> Check in Folder Day 3  practice

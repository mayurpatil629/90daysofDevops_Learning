# Day 2 – Linux File System Basics

## What is Linux File System?

In **Linux**, a **file system** is the way the operating system **stores, organizes, and manages files and directories** in the computer.

Linux uses a **tree structure**, where everything starts from the **root directory `/`**.

`/` is called the **root directory**.
All files and directories start from this root.


# Important Linux Directories

##  Root Directory `/`

Root is the **top level directory** in Linux.

Everything starts from this directory.

Command to check root:

```
ls /
```

Move to root directory:

```
cd /
```

---

##  `/bin`

`/bin` means **binary commands**.

It contains **basic Linux commands used by all users**.

Check commands inside `/bin`:

```
ls /bin
```

Find command location:

```
which ls
```

Example output:

```
/bin/ls
```

---

##  `/boot`

This directory contains **files required to start the system**.

Important files:

* Linux kernel
* bootloader files
* system startup files

Check boot files:

```
ls /boot
```

---

##  `/dev`

`/dev` contains **device files**.

In Linux, **hardware devices are represented as files**.

Examples:

* `/dev/sda` → hard disk
* `/dev/sdb` → USB device
* `/dev/tty` → terminal

Check devices:

```
ls /dev
```

Check disk devices:

```
lsblk
```

---

##  `/etc`

`/etc` contains **system configuration files**.

Important configuration files are stored here.

Examples:

* passwd → user information
* hosts → network configuration
* ssh → SSH configuration

Check files:

```
ls /etc
```

View a configuration file:

```
cat /etc/passwd
```

---

## `/home`

`/home` contains **user personal directories**.

Each user gets their own folder.

Example:

```
/home/rahul
/home/amit
```

User files stored here:

* Documents
* Downloads
* Pictures
* Projects

Commands:

Go to home directory:

```
cd /home
```

List users:

```
ls /home
```

Go to your personal home directory:

```
cd ~
```

---

## `/root`

`/root` is the **home directory of the root user (system administrator)**.

Normal users usually cannot access this directory.

Check root directory:

```
sudo ls /root
```

Switch to root user:

```
sudo -i
```

---

## `/lib`

`/lib` contains **shared libraries needed by system programs**.

Programs use these libraries to run properly.

Check library files:

```
ls /lib
```

---

## `/media`

`/media` is used for **removable devices**.

Examples:

* USB drives
* External hard drives
* CD/DVD

Example path:

```
/media/usb
```

Check mounted devices:

```
ls /media
```

---

##  `/mnt`

`/mnt` is used for **temporary mounting of devices manually**.

Example mount command:

```
sudo mount /dev/sdb1 /mnt
```

Check mounted files:

```
ls /mnt
```

---

## `/opt`

`/opt` is used to store **optional or third-party software**.

Some manually installed applications are stored here.

Check optional software:

```
ls /opt
```

---

## `/proc`

`/proc` is a **virtual directory**.

It provides **system and process information**.

Important files:

```
/proc/cpuinfo
/proc/meminfo
```

Check CPU information:

```
cat /proc/cpuinfo
```

Check memory information:

```
cat /proc/meminfo
```

---

## `/run`

`/run` stores **temporary system runtime information**.

Example:

* running process data
* system service data

Check files:

```
ls /run
```

---

## `/sbin`

`/sbin` contains **system administration commands**.

Examples:

* reboot
* shutdown
* fdisk
* mount

Check commands:

```
ls /sbin
```

Find command path:

```
which reboot
```

---

## `/tmp`

`/tmp` stores **temporary files**.

These files may be deleted automatically when the system restarts.

Check temporary files:

```
ls /tmp
```

Create temporary file:

```
touch /tmp/testfile
```

---

## `/usr`

`/usr` contains **user programs and applications**.

Subdirectories include:

```
/usr/bin
/usr/lib
/usr/share
```

Most applications are stored here.

Check directory:

```
ls /usr
```

---

## `/var`

`/var` contains **variable data** that changes frequently.

Examples:

* system logs
* cache
* mail files

Important directory:

```
/var/log
```

Check logs:

```
ls /var/log
```

View log file:

```
cat /var/log/syslog
```

---

# Important Commands to Explore File System

| Command | Purpose                  |
| ------- | ------------------------ |
| pwd     | show current directory   |
| ls      | list files and folders   |
| cd      | change directory         |
| tree    | show directory structure |
| df -h   | check disk usage         |
| du -sh  | check folder size        |
| find    | search files             |
| locate  | quickly find files       |


---

 # Important directories:

```
/bin   → basic commands
/etc   → configuration files
/home  → user directories
/var   → logs and variable data
/tmp   → temporary files
/usr   → applications
/dev   → device files
```

Understanding the file system helps you **navigate Linux, manage files, and control the system effectively**.

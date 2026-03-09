# Devops learning - Day 01
## Topics Learned
    - How Internet works
    - what is a server
    - Introduction to Linux
        - linux intro
        - linux architecture
        - linux boot process
    - Basic commands

## how Internet works
Internet means network of networks. It connects millions of computers and servers all over the world.

#### Steps of internet works

    Step 1 : You type URL in browser - google.com etc
    Step 2 : Browser sends request to DNS server
    Step 3 : DNS converts domain name to IP address -> google.com to 142.250.xxx.xxx 
    Step 4 : Request goes through your ISP (internet provider) - ISP check the internet then request example - jio, aritel etc 
    Step 5 : Request reaches the web server/Data Center
    Step 6 : Server sends website data back to browser
    Step 7 : Browser displays the website.

#### Simple Flow
**User** => **Browser** =>  **DNS** =>  **Internet** => **Server** => **Response Website** => **Display**

## DNS (Domain Name Server)
    1. DNS is a server that helps a connect to the domain name and server domain name backside work on server.
    2. domain name - youtube.com etc and server ip address - 126.123.0.0 like that 
    3. flow = youtube.com (domain name) ----- connect(DNS)----------server/data center

## What is a Server
A server is a computer or system that provides services, resources, or data to other computers called clients over a network.
When users request something like a website, file, or database data, the server processes the request and sends the response back to the user.
Most servers in the world run on Linux because it is stable, secure, and efficient for handling multiple requests.
- Client = user device
- Server = Server = Computer that provides services to other computers

Types of Server
* web server
* database server
* file server
* application server

Why Servers Are Important
* Store websites and applications
* Manage data and databases
* Handle user requests
* Provide services to many users at the same time

## Introduction of linux
Linux is an open-source operating system that manages computer hardware and software resources and allows users to run applications.
Today Linux is widely used in servers, cloud computing, DevOps, and embedded systems.
Most internet servers and cloud platforms run on Linux because it is stable, secure, and efficient.

#### Basic flow:
User Applications ->  Shell ->  Linux Kernel ->  Hardware

### Linux Boot Process
The Linux Boot Process is the sequence of steps that happens when a computer is powered on until the Linux operating system is fully loaded and ready for the user to log in.

Linux Boot Process = Steps that start Linux after the computer is powered ON 

#### Steps of Linux Boot Process
    Step 1 : Power On & BIOS / UEFI - When the computer is powered on, the firmware (BIOS or UEFI) starts. It checks the system hardware like CPU, RAM, and disks using POST and then finds the bootable device to start the operating system.

    Step 2 : Bootloader (GRUB) - The bootloader loads the Linux operating system.It finds the Linux kernel in the /boot directory and loads it into memory so the system can start.

    Step 3 : Linux Kernel Initialization - The kernel is the core of Linux.It initializes hardware, loads device drivers, manages memory, and mounts the root filesystem.

    Step 4 : Init System (systemd) - After the kernel loads, it starts the first process called init (PID 1).Modern Linux systems use systemd, which is responsible for starting system services and preparing the system environment.

    Step 5 : System Services Start - systemd starts important background services such as networking, SSH, and logging services that are required for the system to run properly.

    Step 6 : Login Prompt - After all services start successfully, the system displays the login screen or terminal. The user can now log in and start using the Linux system.

### Linux Architecture Flow :

User -> Application -> System Libraries -> Linux Kernel -> Hardware

## Linux Basic Commands
* **pwd** - Show current directory path

        pwd
* **ls** - Lists files and directories in the current location

        ls -a detailed list

        ls -l show hidden files

* **cd** - change the directory

        cd nameofdirectory

        cd .. - go back to directory
* **mkdir** - create a new directory

        mkdir nameofdirectory
* **touch** - create a empty file

        touch file.txt
* **cp** - copies files and directories 

        cp copyfilename pastefilename

* **mv** - moves or renames files

        mv movefilename pastefilename

* **rm** - Deletes files or directories

        rm filename

        rm -r foldername when delete a folder then use like this

* **cat** - displays the content of the file

        cat filename

* **clear** - clear the terminal screen

        clear


---
title: "Linux Basics - Part 1"
seoTitle: "Introduction to Linux: Basics, Commands, and Features"
seoDescription: "If you're new to Linux, this guide is for you. Linux is an open-source operating system that is widely used in servers, supercomputers, and other computing."
datePublished: Sun Feb 26 2023 20:38:11 GMT+0000 (Coordinated Universal Time)
cuid: clelus6o0000009kygl9m5lew
slug: linux-basics-part-1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1677443774588/cc9d4b7e-1b8b-4de7-9237-6c3657c5883a.jpeg
tags: software-development, linux, security, devops, linux-for-beginners

---

## **WHY Linux?**

Linux is a widely used operating system that has gained popularity due to its many qualities. Here are five qualities of Linux that make it important and a base for most software:

1. **Open Source:** Linux is an open-source operating system, which means that its source code is freely available to anyone who wants to use it, modify it or distribute it. This allows developers to customize and improve the operating system according to their specific needs, making Linux highly adaptable and flexible.
    
2. **Stability and Reliability:** Linux is known for its stability and reliability, which makes it a popular choice for servers and other mission-critical systems. The operating system is designed to be highly efficient and robust, with the ability to handle large workloads and provide uninterrupted service.
    
3. **Security:** Linux is known for its strong security features, which make it less vulnerable to viruses and malware than other operating systems. This is due to its built-in security features, such as the ability to set permissions and restrict access to files and directories.
    
4. **Compatibility:** Linux is highly compatible with a wide range of hardware and software, making it an ideal choice for developers who need to work with multiple platforms. This is because Linux supports a variety of programming languages and interfaces, making it easy to integrate with other systems.
    
5. **Customizability:** Linux is highly customizable, allowing developers to modify and tailor the operating system to their specific needs. This means that Linux can be customized for a wide range of applications, from desktop computers to servers and embedded systems. This level of customizability also makes Linux an ideal choice for developers who want to create their custom distributions or applications.
    

## **Linux Kernel:**

Before we dig into Kernel and its use, let's dig into why we need a kernel.

### **Why do we need Kernel in an OS?**

We need a kernel in an operating system because it provides an interface between software and hardware. Without a kernel, the software would not be able to access hardware resources such as memory, input/output devices, and network devices. The kernel also provides important system services such as process management, memory management, and security features. The kernel is the foundation upon which the rest of the operating system is built, and it is essential for the proper functioning of the system.

### **Introduction to Linux Kernel**

The Linux Kernel is the core component of the Linux operating system. It is responsible for managing system resources and providing an interface for software to interact with hardware. The kernel is the first program that is loaded into memory when the system starts up, and it remains in memory for the entire time the system is running.

The kernel is designed to be highly configurable and customizable, allowing system administrators to tailor the system to their specific needs. It is also highly modular, allowing new functionality to be added to the system without requiring major modifications to the core kernel code.

### **Linux Kernel Versions**

The Linux Kernel has gone through numerous revisions and updates since its initial release in 1991 by Linus Torvalds. Each version of the kernel is given a version number that consists of three parts: the major version number, the minor version number, and the patch level.

For example, the current stable version of the Linux Kernel as of February 2023 is 5.16.8, where 5 is the major version number, 16 is the minor version number, and 8 is the patch level.

The role of the Linux Kernel is to manage system resources and provide a layer of abstraction between software applications and the hardware. The kernel is responsible for many major tasks, including:

* Process and memory management: The kernel manages processes and allocates memory to them. It also controls the virtual memory system, which allows processes to use more memory than is physically available. Also determines where the CPU is being used and for how much time.
    
* Input/output management: The kernel provides an interface for software to interact with hardware devices, including input/output devices such as keyboards, mice, and printers.
    
* Network stack and device drivers: The kernel includes a network stack that provides networking functionality and device drivers that allow the software to communicate with hardware devices.
    
* File system management: The kernel manages the file system, including access control and security.
    
* Security and access control: The kernel provides access control and security features to protect the system and its data.
    

### **Linux Kernel Commands**

Here are some commonly used Linux Kernel commands:

* `uname -r`: This command shows the kernel version of the running system.
    
* `ls /lib/modules`: This command lists the installed kernel modules.
    
* `lsmod`: This command lists the currently loaded kernel modules.
    
* `modprobe`: This command loads or unloads a kernel module.
    
* `dmesg`: This command displays the system message buffer, which contains information about the kernel and system events.
    
* `sysctl`: This command is used to modify and view kernel parameters at runtime.
    

### **Layers of Kernel :**

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/9bd5c9a6-3ac0-4ea1-84be-2409e2dd12cc/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230303%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230303T093442Z&X-Amz-Expires=86400&X-Amz-Signature=249edcab33ccea7d4c737bf4e7d5d0e1b63f799e267a57f34c1d1f42e04f51c8&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject align="left")

Linux Kernel and its relationship with other components of the operating system.

1. Hardware: Computer hardware is the physical components of the computer system, including the CPU, memory, hard disk, keyboard, mouse, and other peripherals.
    
2. Kernel: The kernel is the core component of the operating system that manages the system resources and provides an interface for the user and the applications to interact with the hardware. It is responsible for managing memory, processing tasks, managing input/output operations, and controlling peripheral devices. The Linux kernel is a monolithic kernel, which means that it runs all of its services in the same address space as the kernel itself.
    
3. Shell: A shell is a program that provides a user interface to access the operating system's services. It interprets the user's commands and translates them into low-level instructions that the kernel can understand. The shell is the command-line interface used by the user to interact with the operating system.
    
4. User: The user is the person who interacts with the operating system by executing commands or running applications. The user can access the operating system's services through the shell, which translates the user's commands into low-level instructions that the kernel can execute.
    

In summary, the Linux kernel is the core component of the operating system that interacts directly with the computer hardware. The shell provides a user interface for the user to interact with the kernel and the operating system's services. Finally, the user can interact with the operating system by executing commands or running applications through the shell.

As we talked about Shells, Let's explore shell types :

### **Shell Types :**

• **Shell:** It is an environment in which we can run our commands, shell scripts, and programs. It is an interface between the user and kernel that hides all complexities of functions of the kernel from the user. It is used to execute commands.

* Bourne Shell (sh): Basic UNIX shell, the predecessor to bash.
    
* C Shell (csh or tcsh) : C-like syntax, history editing, improved interactive features.
    
* Korn Shell (Ksh) : Enhanced sh, advanced scripting capabilities, default on many UNIX systems.
    
* Z Shell (zsh) : Extensible, with advanced tab completion, globbing, and plugins.
    
* Bourne again shell (bash): Most widely used shell, POSIX compliant, default on most Linux systems.
    

# **Linux Boot Process and Run-levels:**

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/a225c4ec-309b-48d5-abde-294574a2c962/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230225%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230225T120954Z&X-Amz-Expires=86400&X-Amz-Signature=49e9be1398965794f79adfcd5deabd39ab149866d4245747940b12d929cc1b91&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject align="left")

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/a225c4ec-309b-48d5-abde-294574a2c962/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230303%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230303T093400Z&X-Amz-Expires=86400&X-Amz-Signature=bf63e97dc75ce5a928dccd5047bcd290103e52084bf2f821b7eeb1caddf3ea92&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject align="left")

The boot process of Linux can be broken down into several stages, each with its own tasks and responsibilities. These stages include:

1. BIOS POST
    
2. Boot Loader
    
3. Kernel Initialization
    
4. INIT Process
    

Let's explore each of these stages in detail.

**1\. BIOS POST**

When you turn on a computer, the first thing that happens is a Power-On Self-Test (POST) performed by the Basic Input/Output System (BIOS). The POST checks the computer's hardware to make sure it is functioning properly, including the processor, memory, and input/output devices.

If the POST detects any issues, it will display an error message and prevent the computer from booting. If there are no issues, the BIOS will search for a bootable device, such as a hard drive or USB drive, and begin the boot process.

**2\. Boot Loader**

The boot loader is responsible for loading the operating system kernel into memory. The most common boot loader for Linux is GRUB (GRand Unified Bootloader). When the BIOS hands over control to the boot loader, the boot loader displays a menu that allows the user to select which operating system they want to boot into.

The boot loader reads the kernel from the selected boot device and loads it into memory. The boot loader may also load an initial ramdisk (initrd), which is a temporary file system that contains essential files needed to boot the system, such as device drivers.

**3\. Kernel Initialization**

Once the kernel has been loaded into memory, it begins the initialization process. The kernel first initializes the processor and memory management system. It then initializes the device drivers needed to access the hardware, such as the network card and storage devices.

The kernel also sets up the virtual file system and mounts the root file system. The root file system is the file system that contains the operating system and all its files.

**4\. INIT Process**

The INIT process is the first user-space process that is started by the kernel. It is responsible for starting all the other user-space processes and services. The INIT process is identified by process ID 1 and is responsible for starting the system's run level.

The run-level determines which services and daemons should be started at boot time. The INIT process reads the configuration file (/etc/inittab) to determine which run-level to start. Each run-level has its own set of scripts that are executed to start the necessary services.

Once all the necessary services have been started, the system is ready to be used.

In conclusion, the Linux boot process involves several stages, each with its their own responsibilities. The BIOS POST checks the hardware, the boot loader loads the kernel into memory, the kernel initializes the hardware and mounts the file system, and the INIT process starts the necessary user-space processes and services. Understanding the boot process can be helpful when troubleshooting boot-related issues.

In Linux, run-levels are a way to define the state in which the system should operate. Each run-level has a specific set of services that are started or stopped, which makes it possible to control what runs when the system is started up or shut down. The term run-levels is used in the **SysV init** systems. These have been replaced by systemd targets in **systemd** based systems.

The complete list of run-level and the corresponding systemd targets can be seen below:

* Runlevel 0: Halt or shut down the system.
    
* Runlevel 1: Single-user mode, which is used for system maintenance tasks.
    
* Runlevel 2: Multi-user mode without network services.
    
* Runlevel 3: Multi-user mode with network services.
    
* Runlevel 4: Not used by default, but can be configured for a specific purpose.
    
* Runlevel 5: Multi-user mode with a graphical user interface.
    
* Runlevel 6: Reboot the system.
    

## **Linux Basic commands and their uses :**

Linux command types are divided into two parts.

* Internal commands
    
* External commands
    

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/16433d00-55ed-4e45-8cd9-9bbb9d236183/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230303%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230303T093854Z&X-Amz-Expires=86400&X-Amz-Signature=dc66bb7c97559fbec2a5f93e3455888d9639e804bf5cd0fa92768962f75874fc&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject align="left")

Absolute Path:

```bash
[~]$ cd /home/aman/devops
```

Relative Path:

```bash
[~]$ cd devops
```

Basic Linux Commands:

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/4e851ce8-dab4-479c-80e3-6f6067de865f/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230225%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230225T121402Z&X-Amz-Expires=86400&X-Amz-Signature=6ca7f81711acb9f74d2d2d63deee163faf4efd1180cf747e82e0c40b62748c49&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject align="left")

```bash
→ ls-al: Lists files and directories with detailed information like permissions,size, owner, etc.

→ ls: Lists all files and directories in the present working directory

→ ls-R: Lists files in sub-directories as well

→ ls-a: Lists hidden files as well

→ ls -alh: All the inofrmation of file and hidden files with the human redable format 

→ cp (source) (destination): To copy a file 

→ cp -r (source) (destination) : To copy a directry to another directory with all the contents inside the directory 

→ cp (source) (destination) with the namme of file or dir you want:

→ cd or cd ~: Navigate to HOME directory

→ cd ..: Move one level up

→ cd: To change to a particular directory

→ cd /: Move to the root directory

→ cat > filename: Creates a new file

→ cat filename: Displays the file content

→ cat file1 file2 > file3: Joins two files (file1, file2) and stores the output in a new file (file3)

→ mv file "new file path": Moves the files to the new location

→ mv filename new_file_name: Renames the file to a new filename

→ sudo: Allows regular users to run programs with the security privileges of the superuser or root

→ rm filename: Deletes a file

→ rm -r: To delete directory with its files

→ man: Gives help information on a command

→ mkdir directory_name: Creates a new directory in the present working directory or an at the specified path

→ rmdir: Deletes a directory

→ mv: Renames a directory
```

### **File Types in Linux:**

1. Regular: Images, Scripts, configuration / Data files
    
2. Directory: /home/bob /root /home/bob/code-directory
    
3. Special File :
    

```bash
   1. Character Files 

   2. Block Files   

   3. Links        -     Hard Link & Soft Link 

   4. Socket Files 

   5. Named Pipes
```

Let's explain each special file type :

1. Character Devices: Character devices are used for accessing hardware devices that are treated as a stream of characters, such as a keyboard, mouse, or serial port. These devices are accessed using input/output system calls, such as read() and write(). In the file system, character devices are represented by special files that reside in the /dev directory and have the prefix "c". For example, the file /dev/tty is a character device file that represents the current terminal.
    
2. Block Devices: Block devices are used for accessing hardware devices that are treated as a sequence of fixed-size blocks, such as hard drives and USB drives. These devices are accessed using input/output system calls, such as read() and write(). In the file system, block devices are represented by special files that reside in the /dev directory and have the prefix "b". For example, the file /dev/sda is a block device file that represents the first hard disk.
    
3. Named Pipes: Named pipes are used for inter-process communication between processes on the same system. They provide a way for processes to send and receive data using standard input/output system calls. In the file system, named pipes are represented by special files that reside in the /dev directory and have the prefix "p". For example, the file /dev/fifo is a named pipe file.
    
4. Sockets: Sockets are used for network communication between processes on different systems. They provide a way for processes to send and receive data over a network using standard input/output system calls. In the file system, sockets are represented by special files that reside in the /dev directory and have the prefix "s". For example, the file /dev/log is a socket file used by the system logging daemon.
    
5. Symbolic Links: Symbolic links, also known as soft links, are special files that point to another file or directory in the file system. They provide a way to create shortcuts to files and directories and can be used to make file system navigation easier. In the file system, symbolic links are represented by special files that contain the path to the target file or directory. For example, the file /usr/local/bin/python is a symbolic link that points to the actual Python executable file.
    

We can identify the type of file with the command ls -ld and the first letter will show the type of file.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/626a2463-2d46-4a17-be7b-bbbb06bde7e4/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230303%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230303T100108Z&X-Amz-Expires=86400&X-Amz-Signature=c0c403bbff776de62e04a407ac4fb8cf62fe0d5cd23cc88200fe14071849be9b&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject align="left")

Below is the list of file types:

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/fb408235-5484-4bba-9442-a05ee076131a/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230303%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230303T100108Z&X-Amz-Expires=86400&X-Amz-Signature=ebf3d805d8bc2db7bc349995e3b91cf34993e9ce0c206866096c33b57342f1da&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject align="left")

### File system Hierarchy :

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/82079061-640b-4709-b417-aaefdef6913d/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230303%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230303T100143Z&X-Amz-Expires=86400&X-Amz-Signature=69ead4b6d5d86e053f1e25dffbd436d42b869c5c8bc71af658bfec671e3666f0&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject align="left")

The Linux File System Hierarchy Standard (FSH) defines the organization of directories and files in a Linux-based operating system. The following is an overview of the key directories and their uses:

1. / : This is the root directory of the file system hierarchy, which contains all other directories and files. It is the first directory that is accessed when the system boots up.
    
2. /bin : This directory contains essential command-line utilities that are necessary for booting and repairing the system, such as ls, cp, and mv.
    
3. /boot : This directory contains the files needed to boot the system, including the kernel and boot loader files.
    
4. /dev : This directory contains device files for all the hardware devices connected to the system, such as hard drives, USB drives, and printers.
    
5. /etc : This directory contains configuration files for the system and its applications, such as network configuration, user authentication, and system startup scripts.
    
6. /home : This directory contains the home directories for all the system users, where they can store their personal files and data.
    
7. /lib : This directory contains the shared libraries that are needed by the system and its applications.
    
8. /media : This directory contains the mount points for removable media, such as USB drives and CDs.
    
9. /mnt : This directory contains the mount points for file systems that are mounted temporarily, such as network file systems.
    
10. /opt : This directory is used for installing third-party applications that are not part of the core system.
    
11. /proc : This directory contains virtual files that provide information about the system and its processes, such as system memory, CPU usage, and running processes.
    
12. /root : This directory is the home directory for the root user.
    
13. /run : This directory contains files that are created at runtime, such as process IDs and socket files.
    
14. /sbin : This directory contains essential system administration utilities, such as mount and shutdown.
    
15. /srv : This directory is used for storing data for services provided by the system, such as web server data or FTP server data.
    
16. /tmp : This directory is used for temporary file storage.
    
17. /usr : This directory contains user applications and their data, such as libraries, documentation, and binaries.
    
18. /var : This directory contains files that are expected to change in size or content over time, such as system logs, mail spools, and cached files.
    

Understanding the Linux File System Hierarchy and their uses is essential for managing a Linux-based operating system. It helps to locate files, diagnose problems, and make sure that the system is functioning correctly.

### **Package Management:**

In Linux, a package is a compressed archive file that contains all the files necessary to install and run an application or software library. Packages are used to simplify the process of installing and managing software on a Linux system. They typically include the application or library files, as well as any configuration files, documentation, and dependencies required by the software. Package management tools such as apt, yum, and pacman are used to download, install, and manage packages on a Linux system.

We have to always take care of Linux Package managers dependencies and their dependencies.

Functions of Package Managers:

1. Package Integrity and Authenticity
    
2. Simplified Package Management
    
3. Grouping Packages
    
4. Manage Dependencies
    

RPM and Debian-based Linux Distributions, I have listed only three, there are many more.

RPM-based distributions:

1. Red Hat Enterprise Linux (RHEL) - RHEL is a commercial Linux distribution known for its stability and security. It is widely used in enterprise environments.
    
2. Fedora - Fedora is a community-driven distribution sponsored by Red Hat. It is known for its cutting-edge features and frequent updates.
    
3. CentOS - CentOS is a free and open-source distribution that is based on RHEL. It is commonly used for web servers, databases, and other enterprise applications.
    

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/b4fd998f-3f02-4121-90db-ca6f2b33523f/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230303%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230303T100228Z&X-Amz-Expires=86400&X-Amz-Signature=71801632e534592aa3646b348867eda30b378272c30a621188e9a0b6ad22f07e&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject align="left")

Debian-based distributions:

1. Debian - Debian is a community-driven distribution known for its stability and adherence to the Unix philosophy. It is widely used in server environments.
    
2. Ubuntu - Ubuntu is a popular distribution that is based on Debian. It is known for its ease of use and strong community support.
    
3. Linux Mint - Linux Mint is a distribution that is based on Ubuntu. It is designed to be easy to use and includes many multimedia codecs and proprietary drivers.
    
    ![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/3e44fae6-e019-465e-a3fd-b3e1e611f45b/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230303%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230303T100259Z&X-Amz-Expires=86400&X-Amz-Signature=65a20297dd9a74cf2ef36194449b1ce3911d185e0d83b594c3e87018d12d10b9&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject align="left")
    

Common Package Managers:

* DPKG: For Debian-based distributions
    
* APT: A newer frontend for DPKG system found in base distributions like Ubuntu, and Linux-Mint.
    
* APT-GET: Traditions frontend system found in DPKG system.
    
* RPM: Base package managers for RedHat-based distribution, such as RedHat Enterprise Linux, Cent-OS, and Fedora.
    
* YUM: A frontend for RPM system, found in RedHat-based distribution.
    
* DNF: A more feature-rich front-end for the RPM system.
    

### **Working with RPM:**

* Installation: Below command is used for the installation of the package.
    

```bash
[~]$ rpm -ivh telnet.rpm
```

where " i " stands for installation and v stands for verbose, it is used to print the detailed output of the command.

* Uninstalling: Below command is used for the uninstallation of packages.
    

```bash
[~]$ rpm -e telnet.rpm
```

* Upgrade: Below command upgrades a package to a newer version.
    

```bash
[~]$ rpm -Uvh telnet.rpm
```

* Query: To query and details about the installed package.
    

```bash
[~]$ rpm -q telnet.rpm
```

* Verifying: With the below commands we can verify if the package is installed from a trusted and secure source.
    

```bash
[~]$ rpm -Vf <path to file>
```

RPM is a package manager used in RedHat-based Linux distributions, such as RedHat Enterprise Linux, CentOS, and Fedora. RPM stands for "Red Hat Package Manager" and is used to download, install, and manage packages on a Linux system.

Here are some RPM commands that you can use to work with packages:

* `rpm -qa`: This command lists all the packages that are installed on the system.
    
* `rpm -qf <filename>`: This command tells you which package a file belongs to.
    
* `rpm -qi <package>`: This command displays information about a package, such as its version, release, and description.
    
* `rpm -ql <package>`: This command lists all the files that are included in a package.
    
* `rpm -qR <package>`: This command lists the dependencies required by a package.
    
* `rpm -e <package>`: This command removes a package from the system.
    
* `rpm -U <package>`: This command upgrades a package to a newer version.
    
* `rpm -ivh <filename>`: This command installs a package from a file.
    

When working with RPM packages, it is important to keep in mind the dependencies required by the package. RPM will automatically resolve and install any required dependencies, but it is important to ensure that all dependencies are met before installing a package.

In addition to RPM, there are other package managers available for managing packages on Linux systems, such as dpkg and APT for Debian-based distributions.

### **YUM**

YUM (Yellowdog Updater, Modified) is a package manager used in Red Hat-based Linux distributions, such as Red Hat Enterprise Linux, CentOS, and Fedora. YUM is similar to the RPM package manager, but it provides additional features such as automatic dependency resolution and the ability to manage software repositories.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/dcf9afcb-6303-42c0-b8f8-e998f83678c7/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230303%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230303T100325Z&X-Amz-Expires=86400&X-Amz-Signature=58b1aa0c0ec77641bccb4cd9e4b982fc2ff3bc790924a5681b4eebe7567fe395&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject align="left")

YUM can be used to install, update, and remove packages on a Linux system. It is also used to manage software repositories, which are collections of software packages that are available for installation on the system.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/dcf9afcb-6303-42c0-b8f8-e998f83678c7/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230225%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230225T121934Z&X-Amz-Expires=86400&X-Amz-Signature=7baebb6587c3ac5b6a51b31c1da3ffe0ff0cc474ca75c11d287f8812984d53d7&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject align="left")

Here are some YUM commands that you can use to work with packages:

* `yum install <package>`: This command installs a package on the system.
    
* `yum update <package>`: This command updates a package to a newer version.
    
* `yum remove <package>`: This command removes a package from the system.
    
* `yum search <package>`: This command searches for a package in the available software repositories.
    
* `yum list <package>`: This command lists all the available versions of a package in the software repositories.
    
* `yum info <package>`: This command displays information about a package, such as its version, release, and description.
    
* `yum clean all`: This command clears the cached data used by YUM.
    
* `yum repolist` : This command will show all the repo’s added to the system.
    
* sudo yum provides tcpdump: This command will show the name of the package.
    

YUM also provides additional features such as the ability to manage software groups, which are collections of related packages, and the ability to manage software repositories and their associated GPG keys.

YUM is a powerful package manager that can simplify the process of installing and managing software on a Linux system. However, it is important to keep in mind the dependencies required by the packages being installed or updated, as well as the security implications of adding new software repositories to the system.

### **Package installation through YUM:**

YUM (Yellowdog Updater, Modified) is a package manager that is used to install, update, and remove packages on Red Hat-based Linux distributions, such as Red Hat Enterprise Linux, CentOS, and Fedora. When installing a package with YUM, the package manager will first check to see if the package is available in the configured software repositories. If the package is available, YUM will download the package and any required dependencies from the repository and install them on the system.

Before downloading and installing the package, YUM will perform a dependency check to ensure that all required dependencies are met. If any dependencies are missing, YUM will prompt the user to install them before continuing with the package installation.

YUM also provides the ability to manage software groups, which are collections of related packages, and software repositories, which are collections of software packages that are available for installation on the system. When working with YUM, it is important to keep in mind the dependencies required by the packages being installed or updated, as well as the security implications of adding new software repositories to the system.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/5629c6fa-8246-41fe-a9ff-ae94cfae1e6f/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230303%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230303T100356Z&X-Amz-Expires=86400&X-Amz-Signature=de8e3e31d0fb3a6f798676690b8e453fb922c9fd5dbcb7c4bcac1f00ca01b606&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject align="left")

To install a package using YUM, follow these steps:

1. Update the package list by running `sudo yum update`.
    
2. Search for the package by running `sudo yum search <package-name>`.
    
3. Install the package by running `sudo yum install <package-name>`.
    
4. If the package has any dependencies, YUM will prompt you to confirm the installation of those dependencies. Type 'y' to confirm and proceed with the installation.
    
5. Once the package and its dependencies have been installed, YUM will display a message indicating that the installation was successful.
    

It is important to note that YUM requires root privileges to install packages. Therefore, you must prefix all YUM commands with 'sudo'.

### **DPKG: Debian Package Manager:**

DPKG (Debian Package) is a package manager used in Debian-based Linux distributions, such as Debian, Ubuntu, and their derivatives. It is a low-level tool for handling software packages in a Debian system, and it is used to install, remove, and manage packages on a Debian-based system.

DPKG is a command-line tool that works in conjunction with other package management tools, such as APT (Advanced Package Tool), which is a higher-level package management tool. APT is a front-end to DPKG and provides a user-friendly interface to install, remove, and manage packages.

DPKG is responsible for handling the installation and removal of individual packages on a Debian-based system. It keeps track of installed packages, their dependencies, and their configuration files. It also provides tools for querying package information, including the version number, description, and dependencies of a package.

It is a low level package manager, similar to RPM it is used for below purpose. Package extension is .deb

* Installation/Upgrade: dpkg -i &lt;package\_file\_name&gt;
    
* Uninstalling: dpkg -r &lt;package\_file\_name&gt;
    
* List with version details: dpkg -l &lt;package\_file\_name&gt;
    
* status: dpkg -s &lt;package\_file\_name&gt;
    
* Verifying : dpkg -p &lt;package\_file\_name&gt;
    

### **APT/APT-GET :**

APT (Advanced Package Tool) is a high-level package management system used in Debian-based Linux distributions, such as Debian, Ubuntu, and their derivatives. APT is a front-end to the lower-level package manager DPKG (Debian Package), and it provides a user-friendly interface for installing, updating, and removing packages on a Debian-based system.

APT uses a package database to keep track of installed packages and their dependencies, and it can automatically resolve dependencies and download packages from software repositories over the internet.

Commands:

* apt update: To refresh the repository, this command is used to get the package information from all available sources.
    
* apt upgrade: To upgrade all the available packages.
    
* apt edit-sources: To edit specific package and upgrade it
    
* apt search &lt; file\_name&gt; : To search a file
    
* apt install: To install a package
    
* apt remove: To remove the package
    
* apt List: To list all the available packages
    

APT has several command-line tools, with the most commonly used tool being APT-GET. Here are some useful APT commands:

1. `sudo apt-get update`: This command updates the package list from all enabled repositories. It should be run before attempting to install or update packages to ensure that the package information is up-to-date.
    
2. `sudo apt-get upgrade`: This command upgrades all installed packages to their latest versions. It downloads and installs updated packages and their dependencies.
    
3. `sudo apt-get install package_name`: This command installs a package on the system. It automatically resolves dependencies and downloads any required packages from the configured repositories.
    
4. `sudo apt-get remove package_name`: This command removes a package from the system. It removes the package and any files associated with it, but it does not remove any dependencies that are no longer needed.
    
5. `sudo apt-get autoremove`: This command removes packages that were installed as dependencies but are no longer needed by any other packages on the system.
    
6. `sudo apt-get purge package_name`: This command removes a package from the system, including any configuration files associated with it.
    
7. `sudo apt-get clean`: This command cleans the local repository of retrieved package files that are no longer needed.
    
8. `sudo apt-get autoclean`: This command removes packages that are no longer available in the repositories and their associated files.
    
9. `apt-cache search search_term`: This command searches the package database for packages that match the search term.
    
10. `apt-cache show package_name`: This command shows information about a specific package, including its version number, description, and dependencies.
    
11. `apt-cache policy package_name`: This command shows the installed and available versions of a package, as well as the repository it is installed from.
    

To view file sizes in Linux, you can use the following commands:

* `ls -lh`: Lists files in the current directory with sizes in a human-readable format.
    
* `du -h <directory>`: Shows the disk usage of files in a directory, with sizes in human-readable format.
    
* `du -sh <directory>`: Shows the total disk usage of a directory, with size in human-readable format.
    
* `df -h`: Displays the disk space usage of all mounted file systems, with sizes in human-readable format.
    
* `du -sk` : shows the file or directory in KB
    

### **Archiving files, Compressing and Uncompressing files:**

Here are some Linux commands for archiving files, compressing and uncompressing files.

* `tar`: Tar is a command-line utility used for archiving files and directories into a single file, called a tarball. Tar can also be used to extract files from a tarball. The basic syntax for creating a tarball is:
    

```bash
tar -cvf archive.tar file1 file2 directory/
tar -cf test.tar file1 file2 file3 
ls -ltr test.tar
tar -tf test.tar : to see the contents of tarball
tar -xf test.tar : Extract the content from tarball 
tar -zcf test.tar file1 file2 file3 : To reduce the size
```

The `-c` option tells tar to create a new archive, the `-v` option enables verbose output and the `-f` option specifies the name of the archive file. The files and directories to be included in the archive are listed at the end of the command.

To extract files from a tarball, use the following command:

```bash
tar -xvf archive.tar
```

The `-x` option tells tar to extract files from an archive.

* `gzip`: Gzip is a command-line utility used for compressing files. Gzip compresses files using the Lempel-Ziv algorithm and can reduce the file size by up to 90%. The basic syntax for compressing a file with gzip is:
    

```bash
gzip file.txt
```

This will create a compressed file called `file.txt.gz`.

To extract a compressed file, use the following command:

```bash
gzip -d file.txt.gz
```

The `-d` option tells gzip to decompress the file.

* `zip`: Zip is a command-line utility used for archiving files and directories into a single compressed file. Zip is similar to tar, but uses a different compression algorithm. The basic syntax for creating a zip file is:
    

```bash
zip archive.zip file1 file2 directory/
```

The files and directories to be included in the archive are listed at the end of the command.

To extract files from a zip file, use the following command:

```bash
unzip archive.zip
```

* `bzip2`: Bzip2 is a command-line utility used for compressing files. Bzip2 uses the Burrows-Wheeler transform algorithm, and can provide better compression than gzip. The basic syntax for compressing a file with bzip2 is:
    

```bash
bzip2 file.txt
```

This will create a compressed file called `file.txt.bz2`.

To extract a compressed file, use the following command:

```bash
bzip2 -d file.txt.bz2
```

The `-d` option tells bzip2 to decompress the file.

* `x**z`:\*\*The `xz` command in Linux is used for file compression and decompression. It uses the LZMA algorithm to compress files, which can result in higher compression ratios than other compression algorithms such as gzip and bzip2. The basic syntax for compressing a file with xz is:
    

```bash
xz file.txt
```

This will create a compressed file called `file.txt.xz`.

To extract a compressed file, use the following command:

```bash
xz -d file.txt.xz
```

The `-d` option tells xz to decompress the file.

As per the standards, there is no need to uncompress the compressed files every time. Below tools allows us to read the files without uncompressing them based on the type of file.

1. zcat
    
2. bzcat
    
3. xzcat
    

```bash
zcat hostfile.text.bz2
```

Searching for Files and Directories in the Linux File system.

Here are some commands for searching for files and directories in the Linux file system:

* `find`: Find is a powerful command-line utility used to search for files and directories in a file system. The basic syntax for finding files is:
    

```bash
find /path/to/search -name "filename"
```

This will search for files with the name "filename" in the directory /path/to/search and its subdirectories. You can also use wildcards to search for files with names that match a pattern, such as:

```bash
find /path/to/search -name "*.txt"
```

This will search for all files with the extension ".txt" in the directory /path/to/search and its subdirectories.

* `locate`: Locate is another command-line utility used to search for files and directories in a file system. It is faster than the find command, but it relies on a pre-built index of the file system, so it may not be as up-to-date as the find command. To get the latest output we have to run the below command before locate command. The basic syntax for using locate is:
    

```bash
updatedb : It will update the database of FS.
locate filename
```

P.S: We have to run the update commands as the root user.

This will search for files with the name "filename" in the entire file system. You can also use wildcards to search for files with names that match a pattern, such as:

```bash
locate *.txt
```

This will search for all files with the extension ".txt" in the entire file system.

* `grep`: Grep is a command-line utility used to search for text within files. The basic syntax for using grep is:
    
* The `-i` flag in `grep` is used to perform case-insensitive searches. This means that the search term will match both uppercase and lowercase versions of the letters in the search term. For example, the command `grep -i "example" file.txt` will match both "example" and "EXAMPLE" in the file `file.txt`.
    
* The `-r` flag in `grep` is used to perform a recursive search through directories. This means that `grep` will search through all files in the specified directory and its subdirectories. For example, the command `grep -r "example" /path/to/directory` will search for the string "example" in all files in the directory `/path/to/directory` and its subdirectories.
    
* `v`: This option tells `grep` to invert the match, meaning that it will only display lines that do not match the search term. For example, the command `grep -v "example" file.txt` will display all lines in `file.txt` that do not contain the word "example".
    
* `w`: This option tells `grep` to match only whole words. For example, the command `grep -w "example" file.txt` will only match lines that contain the word "example" as a whole word, and not as part of another word such as "examples".
    
* `i`: This option tells `grep` to perform a case-insensitive search. This means that the search term will match both uppercase and lowercase versions of the letters in the search term. For example, the command `grep -i "example" file.txt` will match both "example" and "EXAMPLE" in the file `file.txt`.
    
* `A`: This option tells `grep` to display `n` lines of context after the match. For example, the command `grep -A 2 "example" file.txt` will display the line containing the match as well as the two lines that follow it.
    
* `B`: This option tells `grep` to display `n` lines of context before the match. For example, the command `grep -B 2 "example" file.txt` will display the line containing the match as well as the two lines that come before it.
    

```bash
grep "search term" /path/to/file
```

This will search for the string "search term" in the file /path/to/file. You can also use wildcards to search for text within multiple files, such as:

```bash
grep "search term" /path/to/directory/*
```

This will search for the string "search term" in all files in the directory /path/to/directory.

* `which`: Which is a command-line utility used to locate the binary file of a command. The basic syntax for using which is:
    

```bash
which command
```

This will display the location of the binary file for the specified command.

* `whereis`: Whereis is a command-line utility used to locate the binary, source, and manual page files for a command. The basic syntax for using whereis is:
    

```bash
whereis command
```

This will display the location of the binary, source, and manual page files for the specified command.

### **IO Redirection:**

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/6b6b4243-97f2-4f50-8be0-2dcbde7aad15/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230303%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230303T100432Z&X-Amz-Expires=86400&X-Amz-Signature=7a8ce506cf5d13821a5926dd48f56b814b87f23ca10e9e71c13416fd9a65f924&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject align="left")

Input/output (IO) redirection is a powerful feature of the Linux command line that allows you to redirect the input or output of a command to a file or another command. This can be useful for a variety of tasks, such as logging command output to a file, processing the output of a command in another command, or reading input from a file instead of the terminal.

Here are some common IO redirection operators in Linux:

* `>`: This operator redirects the output of a command to a file, overwriting the existing contents of the file. For example, the command `ls > file.txt` will write the output of the `ls` command to the file `file.txt`. If the file does not exist, it will be created. If the file already exists, its contents will be overwritten.
    
* `>>`: This operator redirects the output of a command to a file, appending the output to the end of the file. For example, the command `ls >> file.txt` will append the output of the `ls` command to the end of the file `file.txt`. If the file does not exist, it will be created.
    
* `<`: This operator redirects the input of a command from a file, instead of the terminal. For example, the command `sort < file.txt` will sort the contents of the file `file.txt`, using the file as input instead of the terminal.
    
* `|`: This operator redirects the output of one command to the input of another command. For example, the command `ls | grep .txt` will list all files in the current directory and pipe the output to the `grep` command, which will filter the output to show only files with the extension `.txt`.
    

Here are some examples of using IO redirection in Linux:

* `ls > file.txt`: This command writes the output of the `ls` command to the file `file.txt`.
    
* `echo "Hello, world!" >> file.txt`: This command appends the string "Hello, world!" to the end of the file `file.txt`.
    
* `sort < file.txt > sorted.txt`: This command sorts the contents of the file `file.txt` and writes the sorted output to the file `sorted.txt`.
    
* `cat file.txt | grep "Hello"`: This command reads the contents of the file `file.txt`, pipes the output to the `grep` command, and filters the output to show only lines containing the string "Hello".
    

IO redirection can be a powerful tool for managing and processing data on the Linux command line. By redirecting input and output, you can perform a wide range of tasks with ease.

The `tee` command in Linux allows you to redirect the output of a command to a file and also display it on the terminal at the same time.

The basic syntax for using the `tee` command is:

```bash
command | tee file.txt
```

This will execute the command and redirect the output to both the file `file.txt` and the terminal.

You can also append the output to an existing file using the `-a` option:

```bash
command | tee -a file.txt
```

This will append the output of the command to the end of the file `file.txt`.

The `tee` command can be useful for logging output to a file while still being able to see it on the terminal in real-time. It can also be used in conjunction with other commands to perform complex operations on data.

### **VI editor:**

Vi is a powerful text editor that is widely used on Linux and other Unix-like operating systems. It is a command-line based editor that allows users to create, edit, and save text files from within a terminal window.

Vi has a reputation for being difficult to use, with a steep learning curve. However, once users become familiar with its commands and modes, they find that Vi is a highly efficient tool for editing text.

VI editor is a popular text editor in Linux and Unix systems. Here's a list of some of the most commonly used commands in VI editor:

1. **i** - Switch to Insert mode, allowing you to insert text.
    
2. **esc** - Return to command mode from Insert mode.
    
3. **x** - Delete the character under the cursor.
    
4. **dd** - Delete the current line.
    
5. **d3d** - Delete 3 line from the current line
    
6. **u** - To undo the previous change
    
7. **:w** - Save the current file.
    
8. **:q** - Quit the editor.
    
9. **:wq** - Save the current file and quit the editor.
    
10. **:q!** - Quit the editor without saving changes.
    
11. **yy** - Yank (copy) the current line.
    
12. **p** - Paste the contents of the clipboard after the cursor.
    
13. **/searchterm** - Search for the specified term in the file.
    
14. **n** - Find the next occurrence of the search term.
    
15. **:set number** - Display line numbers.
    
16. **:set nonumber** - Hide line numbers.
    
17. **:set syntax=language** - Set syntax highlighting for a specific programming language.
    
18. **:set tabstop=n** - Set the tab width to n spaces.
    
19. **:set expandtab** - Use spaces instead of tabs for indentation.
    
20. **:set noexpandtab** - Use tabs instead of spaces for indentation.
    
21. **:set autoindent** - Automatically indent new lines to match the previous line.
    
22. **:set nowrap** - Disable line wrapping.
    

These are just a few of the many commands available in VI editor. You can find more commands by typing**: help** in command mode to see the full list of commands and their descriptions.

NOTE:

```bash
Note: 
**sockets*cores*thres=CPUs
eg: 1*4*2= 8 Parallels threads can run at a time
```

**THANK YOU FOR YOUR VALUABLE TIME !!**
---
title: "Ansible Beginner"
seoTitle: "Ansible"
seoDescription: "Ansible , automation, playbooks, modules"
datePublished: Tue Jan 17 2023 20:50:17 GMT+0000 (Coordinated Universal Time)
cuid: cld0plo74000108m93chgdylo
slug: ansible-beginner
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/npxXWgQ33ZQ/upload/ec46efd2a07f839f49b8dcdaf646cf20.jpeg
tags: ansible, ansible-playbook, ansible-module

---

**Ansible** is an open-source automation platform that can help you manage and control various nodes from a central location. It allows you to automate tasks, including configuration management, application deployment, and task execution.

It is a radically simple IT automation platform that makes your applications and systems easier to deploy. Avoid writing scripts or custom code to deploy and update your applications— automate in a language that approaches plain English, using SSH, with no agents to install on remote systems.

Some key features of ansible include:

1. Simple to use: Ansible uses an easy-to-learn language (YAML)and has a simple, straightforward architecture.
    
2. Agentless: ansible does not require any additional software to be installed on managed nodes.
    
3. Idempotent: ansible tasks are designed to be run multiple times without causing unintended side effects.
    
4. Large community and support: ansible is an open-source platform with a large user base, meaning there is a wealth of resources and support available.
    

### **What Are the Benefits of Learning Ansible Basics?**

* A free and open-source community project with a huge audience.
    
* Battle-tested over many years as the preferred tool of IT wizards.
    
* Easy to start and use from day one, without the need for any special coding skills.
    
* Simple deployment workflow without any extra agents.
    
* Includes some sophisticated features around modularity and reusability that come in handy as users become more proficient.
    
* Extensive and comprehensive official documentation that is complemented by a plethora of online material produced by its community.
    

### **Ansible Architecture:**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673988324454/8831f9c5-7c1f-48bc-ba09-ca35707a7305.png align="center")

From the diagram above, we understand that visibility comes into play:

1. Everything from servers to desktop computers to network configurations and applications can all be stored in a Public/Private Cloud.
    
2. It demonstrates that it has all the features of a sizable cloud platform, but it also allows users to communicate with all of the modules and API. It also demonstrates that it has security measures.
    
3. An inventory file contains devices, groups, host variables, templates, and tasks. Along with the inventory file, playbooks must be created that describe how to handle all the devices, groups, host variables, and templates.
    
4. Once Ansible has a task or set of tasks in a playbook to run, it needs to know where to run those tasks. It needs an inventory of hosts. Ansible has a concept called “inventories” that consist of lists of hosts to perform actions stored in files as YAML.
    
5. Modules in Ansible allow you to interact with the cloud like Azure or on-prem resources like Hyper-V. An Ansible module is a standalone, reusable script that can be used with the Ansible API. They can also be used by Ansible playbooks. One of the key factors of an Ansible module is that they are reusable and not meant for just one environment.
    
6. The augmented ansible core is created by combining all of the cache, logging purposes, ansible’s functioning, and so on.
    
7. It allows for the creation of various agentless frames that can be utilized in multiple automated networks.
    
8. A single repository can contain all the computers of an operational or IT infrastructure network.
    
9. Ansible is being used to make Linux and Unix machines automated.
    
10. It provides the needed APIs for the interaction of the end-to-end modules.
    

### **Ansible modules**

**Ansible Modules** are pre-written pieces of code that can be used in ansible playbooks to perform specific tasks. There are hundreds of modules available, and they can be used to manage everything from software installations to server configurations.

Here is an example of an ansible copy module:

```yaml
---
- name: Copy file to remote host
  hosts: all
  tasks:
    - name: Copy file
      copy:
         src: /path/to/local/file
         dest: /path/to/remote/destination
```

### **Ansible playbook**

**Ansible playbook** is a YAML file that defines a series of tasks to be executed by Ansible. It specifies the managed nodes on which the tasks should be run and the order in which they should be executed.

Here is a list of the most commonly used Ansible Modules:

1\. Ansible Package Module: Used to install, upgrade, and remove packages on remote hosts.

2\. Ansible Service Module: Used to manage services on remote hosts.

3 Ansible File Module: Used to manage files and directories on remote hosts.

4\. Ansible Copy Module: Used to copy files from the local machine to the remote hosts.

5\. Ansible Fetch Module: Used to fetch files from remote hosts to the local machine.

6\. Ansible Template Module: Used to create configuration files from templates.

7\. Ansible Shell Module: Used to execute shell commands on remote hosts.

8\. Ansible Debug Module: Used to print out debugging information.

9\. Ansible Setup Module: Used to collect information about remote hosts.

10\. Ansible Git Module: Used to manage git repositories on remote hosts.

11\. Ansible Yum Module: Used to manage packages on Red Hat-based systems.

12\. Ansible Apt Module: Used to manage packages on Debian-based systems.

13\. Ansible Command Module: Used to execute commands on remote hosts.

14\. Ansible Script Module: Used to execute scripts on remote hosts.

15\. Ansible Cron Module: Used to manage cron jobs on remote hosts.

16\. Ansible User Module: Used to manage user accounts on remote hosts.

17\. Ansible Group Module: Used to manage user groups on remote hosts.

18\. Ansible SELinux Module: Used to manage SELinux policies on remote hosts.

19\. Ansible Firewall Module: Used to manage firewall rules on remote hosts.

20\. Ansible Cloud Modules (AWS, GCP, Azure, etc.): Used to manage cloud resources on remote hosts.

**Ansible Inventory** is a way for Ansible to track the information about the systems it is managing. It is a collection of data that describes the hosts and their characteristics. The inventory can be a simple list of hostnames or IP addresses, or it can be a more complex file that describes the hosts in groups and includes additional information about each host.

```yaml
[webservers]
web1 ansible_host=192.168.1.100
web2 ansible_host=192.168.1.101

[dbservers]
db1 ansible_host=192.169.1.102
db2 ansible_host=192.168.1.103
```

### **Ansible conditions**

**Ansible conditions** allow you to control the flow of execution in your playbooks and tasks based on certain conditions. The most common way to use conditions in Ansible is by using the when statement. "**when**" statement is used to specify a condition that must be met before a task is executed.

Here is a simple example for the same, you can always use them according to the conditions and your convenience.

```yaml
-name: Install package
 package: 
   name: nginx 
   state: present 
 when: ansible_os_family == "Debian"
```

### **Ansible roles**

**Ansible roles** are a way to organize and reuse Ansible tasks, files, and variables. Each role is defined in a single directory and it has a specific name that can be referenced in the playbook. Roles can be stored in the Ansible galaxy or in a local directory.

### **Ansible Galaxy**

**Ansible Galaxy** is a public library of Ansible roles that can be easily downloaded and used in your playbooks. Ansible Galaxy is a command-line tool that is included with the Ansible installation, so you don't have to install it separately. And the enterprise version is in GUI as well offered by Red-hat.

The command to install ansible-galaxy is below. You can also find more about ansible-galaxy on [https://galaxy.ansible.com/](https://galaxy.ansible.com/)

```yaml
sudo apt-get install ansible
```

### **Ansible Tower**

**Ansible Tower** is a management tool for Ansible, an open-source automation engine that automates software provisioning, configuration management, and application deployment. Ansible Tower provides a centralized interface for managing and organizing Ansible automation in an enterprise environment.

* Role-based access control: Allows users to control access to Ansible automation based on roles and permissions.
    
* Scheduling: Allows users to schedule Ansible automation to run at specific times or at specific intervals.
    
* Notifications: Allows users to receive notifications when automation runs or when certain events occur.
    
* Reporting: Provides detailed reporting on the execution of Ansible automation, including success rates, run times, and output.
    
* APIs: Provides a RESTful API for automating and integrating Ansible Tower with other tools and systems.
    

Ansible tower is used in IT operations and DevOps teams to automate repetitive tasks, quickly deploy applications and manage infrastructure. It provides a graphical user interface to manage Ansible playbooks, inventory, and scheduled jobs. It also allows you to delegate certain automation tasks to specific teams or individuals and provides reporting and analytics to track and measure automation success.

### **Ansible loops**

**Ansible loops** allow you to repeat tasks or actions multiple times, based on a set of data. Loops are defined using the with\_\*keywords, where \*is the type of loop you want to use. There are several types of loops in Ansible, including with\_items, with\_dict, with\_file, with\_sequence and with\_subelements, each with its use cases.

Here is an example of using the with\_items loop to install multiple packages, Also we can always use it according to our convenience like dict, file, sequence etc.

```yaml
-name: Install packages 
 package:
   name: "{{ item }}"
   state: present 
 with_items: 
    - nginx 
    - mysql-server
    - php
```

### **Ansible Variables**

**Ansible Variables:** Ansible uses variables to manage differences between systems. With Ansible, you can execute tasks and playbooks on multiple different systems with a single command. To represent the variations among those different systems, you can create variables with standard YAML syntax, including lists and dictionaries. You can define these variables in your playbooks, in your inventory, in reusable files or roles, or at the command line. You can also create variables during a playbook run by registering the return value or values of a task as a new variable.

### **Thank you all for giving your valuable time for reading.**

### **Resources :**

**#Kunal Kushwaha**

**#WeMakeDevs**

**#Techworld with Nana**

**#Kodekloud**

#www.kodekloud.com
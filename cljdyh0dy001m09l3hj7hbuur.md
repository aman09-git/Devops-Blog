---
title: "Process : Thread : Core"
seoTitle: "This blog discusses the concepts of programs, processes, threads, and"
seoDescription: "This blog will help software developers, Devops Engineers, system admins who are using a  computer system. Also helpful for interviews."
datePublished: Tue Jun 27 2023 07:17:51 GMT+0000 (Coordinated Universal Time)
cuid: cljdyh0dy001m09l3hj7hbuur
slug: process-thread-core
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/BPJKc4r7_eo/upload/423e514cbb909555894965ca3d21b10f.jpeg
tags: software-development, devops, process, software-engineering, cpu

---

Before we jump to this we need to understand what a program is " A program is a set of code or instructions that is stored in disks. when it is loaded to the memory and executed it becomes a process.

### **Process:**

A process is an instance of a program that is being executed by a computer system. A process typically consists of an executable program, its data, and the resources that it uses, such as memory, input/output devices, and system services. Each process has its own memory space and runs independently of other processes. One process can not corrupt the memory and space of another process. The different tab that we open in Chrome is a process.

EX: Sending a message or recording a video over Whatsapp is a process of a program. These two processes will have their own memory space which stores program code and data, these two act as an individual.

### **Thread:**

<mark><br></mark>Thread is a lighter version of the process. A process can have multiple threads, and each thread can execute concurrently with other threads within the same process. Threads share the same memory space as the process that created them, and they can communicate with each other directly. One misbehaving or corrupt thread can bring down the entire process.

For example, in a web browser, each tab can be considered a process, and each tab can have multiple threads running within it. One thread might be responsible for rendering the web page, while another thread might handle user input.

These process runs on the CPU through context switching, once one process is switched out of the CPU so another process can run.

### **Core**:

A core processor refers to a computer processor that contains multiple independent processing units, called cores. These cores are capable of handling multiple tasks and processes at the same time, which can result in faster and more efficient computer performance. This is opposed to single-core processors, which can only handle one task or process at a time. The more cores you have the faster Processing you get.

For example, suppose a user is running a video editing program on their computer. The program is a process that has multiple threads running simultaneously. Some threads might be responsible for rendering video, while others might be handling user input.

When the operating system schedules the video editing program to run, it assigns the process and its threads to one or more available cores in the CPU. By assigning multiple threads to a single core, the CPU can make more efficient use of its processing power, allowing the video editing program to execute more quickly and efficiently.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1687849631407/c503fe5f-f387-4b79-9509-38ddb212773d.png align="center")

#wemakedevs #ByteByteGo #KodeKloud

@[Kunal Kushwaha](@kunalk)
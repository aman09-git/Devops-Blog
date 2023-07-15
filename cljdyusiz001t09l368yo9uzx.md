---
title: "Virtual CPU."
seoTitle: "CPU, Virtual CPU"
seoDescription: "A virtual CPU (vCPU) is a software abstraction of a physical CPU that is used by virtualization software to allocate computing resources to virtual machines"
datePublished: Tue Jun 27 2023 07:28:34 GMT+0000 (Coordinated Universal Time)
cuid: cljdyusiz001t09l368yo9uzx
slug: virtual-cpu
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/DubQVeFFbFQ/upload/60168b3e83f2217478c94b7c7a9d3357.jpeg
tags: software-development, engineering, devops, software-engineering, cpu

---

A virtual CPU (vCPU) is a software abstraction of a physical CPU that is used by virtualization software to allocate computing resources to virtual machines (VMs) running on a physical host. Essentially, a vCPU is a portion of the physical CPU's processing power that is dedicated to a specific virtual machine.  
  
Here's an example to illustrate how vCPUs work:  
Let's say you have a physical server with a quad-core CPU. You decide to create three virtual machines on this server, each with two vCPUs assigned to it. This means that each virtual machine will have access to two of the four cores on the physical CPU.  
  
When a virtual machine needs to execute a task, its assigned vCPUs request processing time from the physical CPU. The virtualization software manages the allocation of processing time to each virtual machine's vCPUs based on the priority of the task and the availability of processing resources.  
  
For example, if one virtual machine is running a critical database application that requires a lot of processing power, its vCPUs will be given priority access to the physical CPU over the other virtual machines' vCPUs. This ensures that the critical application can run smoothly without being bogged down by other applications running on the same physical server.  
  
It allows multiple virtual machines to share the processing power of a single physical CPU. By intelligently managing the allocation of processing time to each virtual machine's vCPUs, virtualization software can ensure that all applications running on a physical server can run smoothly and efficiently.

Link for Process : Thread: Core

[https://aman09.hashnode.dev/process-thread-core](https://aman09.hashnode.dev/process-thread-core)  

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1687850744665/9aaaab45-7814-4eab-82e4-766122ce1772.png align="center")
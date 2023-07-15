---
title: "Computer Networking: Part 2"
seoTitle: ""Exploring Client-Server Architecture and In-Depth Protocols:"
seoDescription: "Unlock the secrets of client-server architecture and dive deep into the world of networking protocols with our comprehensive blog."
datePublished: Sat Jul 01 2023 03:30:41 GMT+0000 (Coordinated Universal Time)
cuid: cljjg4all02a08enva526gcgm
slug: computer-networking-part-2
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/LrxSl4ZxoRs/upload/75b4dc2b6e253b52153e7583f9ead195.jpeg
tags: software-development, devops, software-engineering, networking, protocols

---

### Protocols:

The rules that are set up by standards about how particular data is being sent over a network are called Protocols. Ex: TCP, UPD, HTTP, FTP etc.

### Client-Server Architecture :

Let's understand this with a simple diagram.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1688035281302/6da8e4ff-c107-47d5-be63-e356b39ea8de.jpeg align="center")

Once an end device (client) requests a service or resource from the server and the client servers respond to the client accordingly. Clients initiate communication and servers respond, enabling efficient sharing of data and workload separation.

Now let's dig a bit to understand this.

![Dig: A](https://cdn.hashnode.com/res/hashnode/image/upload/v1688034127730/6a6d0d88-6696-4df8-8a90-ac2f58be5039.png align="center")

Diagram: A

![Dig B ](https://www.tutorialspoint.com/assets/questions/media/56524/servers.jpg align="center")

Diagram: B

Based on the above diagram we have defined the clients and the server in Dig A with ports. And in Dig B we have shown a big server that handles all kinds of client requests like Files, Print, Applications, Messaging and Database.

Let's suppose we have 3 clients and they are requesting 3 different services from the server like File, Message and Application.

Now, how the server will evaluate which client requests which service, which will be defined by the ports and the protocols.

* For File Service, we use ports 20 and 21 to transfer files b/w client and server.
    
* For Messaging, we use port 25 and SMTP protocol.
    
* For Application, we use ports 80 and 443 i.e. HTTP & HTTPS
    

Advantages of the Client-server Model:

* Centralization
    
* Adaptability
    
* Protection
    
* Operation
    

Disadvantages of the Client-server Model:

* Overloading
    
* Cost
    
* Methods are telling the server what to do.
    
    💡 GET: It means you are requesting some data
    
    💡 POST: The client gives some data to the server like web forms
    
    💡 PUT: Put data in a specific location
    
    💡 DELETE: To Delete data from the server
    

Let's dig a bit into protocols:

### HTTP:

HTTP is an application-layer protocol that facilitates the transfer of hypertext (structured text that includes links) over the Internet. It operates on top of TCP (Transmission Control Protocol) and uses port 80 by default. HTTP is stateless, meaning it doesn't retain information about previous requests.

Example:  
Let's say you enter the URL "[http://www.example.com](http://www.example.com)" into your web browser. The browser acts as an HTTP client and sends an HTTP GET request to the server at that domain. The request includes headers and potentially additional data. The server, acting as the HTTP server, processes the request and responds with an HTTP response. The response contains headers and the requested web page's content, typically in HTML format. The browsers then give a web page and display it to us.

### HTTPS:

HTTPS is an extension of HTTP that adds a layer of security through encryption. It uses SSL (Secure Sockets Layer) or TLS (Transport Layer Security) protocols to establish an encrypted connection between the client and the server. HTTPS operates on top of TCP and uses port 443 by default. It ensures data confidentiality and integrity, protecting against eavesdropping and tampering.

Example:  
When you visit a website using HTTPS, such as "[https://www.example.com](https://www.example.com)," the communication between your web browser and the server is encrypted. The initial handshake involves the browser verifying the server's identity and establishing a secure connection. The subsequent requests and responses are transmitted encrypted, making it difficult for unauthorized parties to intercept or manipulate the data.

### FTP

FTP (File Transfer Protocol) is a standard network protocol used for transferring files between a client and a server. It operates on ports 20 and 21.

* Port 21: FTP control connection is established between the client and server on this port. It handles commands, authentication, and file transfer details.
    
* Port 20: FTP data connection is established on this port for actual file transfers. It is used to send and receive data between the client and server.
    

Example: A user connects to an FTP server using an FTP client (e.g., FileZilla). The client establishes a control connection on port 21 with the server. The user provides authentication credentials. Then, using FTP commands (e.g., "get" or "put"), files are transferred over the data connection on port 20 between the client and server.

### SSH (Secure Shell)

SSH (Secure Shell) is a cryptographic network protocol that provides secure remote access and secure file transfer capability.SSH is the most commonly used method for connecting to distant Linux and Unix-like systems. SSH is often used by network administrators for tasks that a normal internet user would never have to deal with.

* SSH runs on port 22
    
* SSH is for securely executing commands on a server.
    
* SSH uses a username/password authentication system to establish a secure connection.
    
* SSH is working based on network tunnels.
    
* SSH is a remote protocol
    
* It is used to reduce security threats for remote server login
    
* SSH follows the authentication process by server’s verification is done by the client, the session key generation, and the client’s authentication
    

### SSL/TLS:

Secure Sockets Layer (SSL) and Transport Layer Security (TLS) are mechanisms for securing websites. SSL/TLS provides secure communication, encryption, and authentication for various applications and services. It operates on port 443 and is commonly used for securing web browsing, email communication, file transfers, VPNs, and API communication.

* SSL runs on port 443
    
* SSL is used for securely communicating personal information.
    
* SSL normally uses X.509 digital certificates for server and client authentication.
    
* SSL is working based on digital certificates.
    
* SSL is a security protocol
    
* It allows a secure transition of data between a server and the browser thus, keeps information intact.
    
* SSL follows the authentication process by exchanging digital certificate
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1688041650247/21b8373c-1389-43fd-b54d-0b6f604675f1.png align="center")

**To Know more about SSL and TLS check my blog:** [**https://aman09.hashnode.dev/ssl-and-tls**](https://aman09.hashnode.dev/ssl-and-tls)

### TCP/UDP

TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) are transport layer protocols that facilitate data transmission over networks.

TCP:

* The connection-oriented protocol ensures reliable and ordered delivery of data.
    
* Provides error checking, flow control, and congestion control.
    
* Ideal for applications that require guaranteed delivery and data integrity, such as web browsing, file transfer, email, and database management.
    

UDP:

* The connectionless protocol offers minimal overhead and low latency.
    
* Does not guarantee reliable delivery or ordering of data.
    
* Suitable for real-time applications where speed and efficiency are prioritized over data reliability, such as streaming media, online gaming, VoIP, and DNS.
    

Differences:

* TCP establishes a connection before transmitting data, while UDP does not require a connection setup.
    
* TCP provides error checking and retransmission of lost packets, whereas UDP does not perform error recovery.
    
* TCP ensures the ordered delivery of data, while UDP does not guarantee the order of transmitted packets.
    
* TCP has a higher overhead due to additional mechanisms, whereas UDP has a lower overhead and faster transmission.
    
* TCP is suited for applications that require reliable data transfer, while UDP is preferred for applications where real-time transmission and low latency are crucial.
    

### SNMP (Simple Network Management Protocol)

SNMP (Simple Network Management Protocol) is a widely used network management protocol that allows administrators to monitor and manage network devices efficiently. It provides a standardized framework for collecting and organizing information from network devices, enabling effective network monitoring, fault detection, and configuration management.

1. Port 161: This port is used by the SNMP agent (server) to receive SNMP requests from the SNMP manager (client). It allows the manager to gather data and issue commands to the agent.
    
2. Port 162: This port is used by the SNMP manager to receive SNMP trap notifications from the agent. Traps are event-based notifications sent by network devices to alert the manager about specific events or conditions.
    

### SMTP (Simple Mail Transfer Protocol)

SMTP (Simple Mail Transfer Protocol) is a fundamental protocol used for sending and delivering email messages across the internet. It provides a reliable and efficient means of transmitting emails from a sender to one or more recipients. Understanding SMTP is essential for ensuring smooth email communication in today's digital world.

SMTP primarily operates on two port numbers:

1. Port 25: This is the default port used for standard SMTP communication between mail servers. It allows servers to exchange email messages and transfer them across the internet.
    
2. Port 587: This port, known as the Submission port, is an alternative port used for email submission by clients (mail user agents) to the mail server. It is commonly used for secure email transmission using TLS encryption.
    

### DHCP:

DHCP (Dynamic Host Configuration Protocol) is a network protocol that automates and simplifies the process of assigning IP addresses to devices on a network. By dynamically managing IP address allocation, DHCP enables efficient network configuration and ensures smooth connectivity.

Port Numbers: DHCP uses two port numbers for communication:

1. Port 67: This port is used by DHCP servers to receive DHCP client requests.
    
2. Port 68: This port is used by DHCP clients to send requests to DHCP servers.
    

Dynamic IP Address Assignment: The process followed by DHCP to dynamically assign IP addresses is often referred to as the DORA process, which stands for:

* Discovery: The client discovers available DHCP servers on the network.
    
* Offer: The server offers an IP address and related configuration parameters to the client.
    
* Request: The client requests the offered IP address from a specific DHCP server.
    
* Acknowledgment: The server acknowledges the request and confirms the assignment of the IP address to the client.
    

### ARP:

An IP address can be used to determine a device's hardware address (MAC address) using the network technique known as ARP (Address Resolution technique). It is utilized when a device has to communicate with another device on a local network (such as an Ethernet network where packets must first know their physical addresses). ARP is used by the sending device to convert IP addresses to MAC addresses. The IP address of the receiving device is included in the ARP request message that is sent by the device. On a local network segment, all devices can view the message, but only the one with that IP address can reply with an ARP reply message that includes its MAC address. Now that the sending device has enough details, it can send the packet to the

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1688047157719/ce19c3a9-17c3-4b65-b804-202199f3e0b2.png align="center")

Now Let's understand this with an example:

In the above diagram, host A wants to communicate with Host B. Host A has the IP address of Host B but not the MAC address. Now Host A will send an ARP request with the IP address of Host B and its Mac Address. It will go to the switch and it will broadcast the request to all the connected hosts except the sender. Now it will go to each host one by one but only host B will acknowledge it and respond to the same with its MAC address. Now Host A and Host B can communicate with each other.

### Reverse Address resolution protocol(RARP):

The RARP is used to find out the IP address of the physical host having its MAC (Physical Address). Old diskless workstations used RARP. Since these outdated hosts lack a disc, there is nowhere to store an IP address. However, they do have a MAC address that is hard coded. The workstation transmits a RARP request with its own MAC address when it first turns on.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1688128021581/ba6aa865-2b7f-4399-8244-e3f3bf314029.png align="center")

Let's understand this with the above picture.

In the above picture, the host is requesting its IP address binding the MAC address with the request, Now the server has a table that has the device's Mac address and their IP address. Now the server will match the MAC address of the requested host and reply to it with its IP address.

### ICMP:

ICMP (Internet Control Message Protocol) is a network protocol used for diagnostics and network management. ICMP allows IP to inform the sender if the datagram is undeliverable. A datagram travels from Router to Router until it reaches one that can deliver it to its final destination. It works at the network layer (Layer 3) of the OSI model and is primarily used for sending error messages, testing network connectivity, and troubleshooting network issues.

Use of ICMP:

* Error Reporting
    
* Network Testing
    
* Time Exceeded
    

Commands Used to trace the IP :

* Ping
    
* Traceroute ( Windows)
    
* Tracepath (Linux)
    

### Routing Protocols:

* Border Gateway Protocol (BGP): BGP is an exterior gateway protocol used for routing between autonomous systems (AS) on the internet. It determines the best path for data to reach its destination by exchanging routing information between routers in different ASes.
    
* Open Shortest Path First (OSPF): OSPF is an interior gateway protocol used within an autonomous system (AS). It calculates the shortest path between routers using a link-state routing algorithm, ensuring efficient and scalable routing within the network.
    
* Enhanced Interior Gateway Routing Protocol (EIGRP): EIGRP is a Cisco proprietary routing protocol used for routing within an AS. It combines characteristics of both distance-vector and link-state routing protocols, offering fast convergence and scalability.
    
* Routing Information Protocol (RIP): RIP is one of the oldest interior gateway protocols. It uses a distance-vector algorithm based on hop count to determine the best path. RIP is suitable for small to medium-sized networks but may have limitations in scalability and convergence speed.
    

### NAT:

NAT stands for network address translation. It’s a way to map multiple private addresses inside a local network to a public IP address before transferring the information onto the internet. Organizations that want multiple devices to employ a single IP address use NAT, as do most home routers.

Now, Let's understand this with the below example which is very common in our day life.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1688130370176/418cc792-5e6c-4807-b47a-9cfe4de83e0d.png align="center")

Let's say we are using a home router for internet access from different devices. Let's see what happens in each step:

1. Let’s say you are using any of the devices from your home to search for an online store on the Internet from your IP private address. (Private IP Address)
    
2. Once you type the URL it reaches its destination using DNS (Already explained refer: [https://aman09.hashnode.dev/dns-domain-name-system](https://aman09.hashnode.dev/dns-domain-name-system) )
    
3. Now before leaving your private network, your device IP address will go to the router which has NAT embedded. The network has a single public IP address, typically assigned by the Internet Service Provider (ISP). This public IP address is used to communicate with devices on the internet. ( Public IP )
    
4. NAT will change the Private IP to a Public IP before sending this to the Internet to search for an online store. (Translation Process)
    
5. Now, the picture comes of how it will differentiate the different devices, for this ports and port mapping will be used. They will be recognized by the ports from which port which IP has sent the request, only that IP will receive the response. (Port Mapping)
    
6. When we receive the response from the Internet, it comes to our router with a Public IP address but then with the help of NAT, it gets changed to a Private IP address. (Reverse Translation)
    

### Telnet:

Telnet is a network protocol that enables network-based remote access to devices. It offers a text-based user interface for dialogue with distant systems.

* Remote Access: Telnet enables a user to connect to a remote device over a network, such as the internet, usually a server or networking device.
    
* Text-based Interface: Telnet offers a command-line interface that allows users to enter commands and receive responses in plain text once they are connected. It enables users to manage and control the connected gadget from a distance.
    
* Telnet normally communicates over port number 23, which is used. The IP address or hostname of the remote device and the port number must be specified by the user to start a Telnet session with the device.
    
* Telnet is an insecure protocol since client and server communications are not secured. This is vital to keep in mind. As a result, hostile actors may intercept and read any data carried over Telnet, including login passwords and sensitive data.
    
* Alternatives: SSH (Secure Shell) and other more secure protocols have mostly supplanted Telnet due to security issues. SSH enables authenticated, encrypted communication, guaranteeing safe remote device access.
    

### Commonly Used commands for troubleshooting at the beginner level :

* Netstat: Netstat is a command-line tool used to display network statistics and information about network connections on a host. It provides details such as active network connections, listening ports, routing tables, and network interface statistics. Netstat helps diagnose network issues, monitor network activity, and manage network resources.
    
* Iostat: Iostat is a command-line utility used to monitor and report input/output (I/O) statistics of devices, including disks, partitions, and file systems. It provides information on disk utilization, I/O rates, and average response times. Iostat helps identify I/O bottlenecks and optimize disk performance.
    
* Ipconfig: ipconfig (Windows) or ifconfig (Unix/Linux) is a command-line utility used to view and configure IP-related information for network interfaces. It displays the IP address, subnet mask, default gateway, and other network configuration details. Ipconfig is useful for troubleshooting network connectivity issues and configuring network settings.
    
* Ping: Ping is a command-line tool used to test network connectivity between a source host and a destination host. It sends ICMP Echo Request messages to the destination and waits for ICMP Echo Reply messages. Ping measures the round-trip time (RTT) and checks for packet loss, helping diagnose network connectivity issues and verifying if a host is reachable.
    
* Traceroute: Traceroute (Windows) or traceroute (Unix/Linux) is a command-line utility used to trace the route taken by packets from the source to a destination host. It sends a series of ICMP Echo Request messages with varying TTL values, allowing you to identify the routers or hops traversed along the path. Traceroute helps diagnose network latency, identify network bottlenecks, and troubleshoot connectivity issues.
    
* Dig: Dig (Domain Information Groper) is a command-line tool used to query DNS (Domain Name System) servers for DNS-related information. It provides details such as IP addresses associated with a domain, DNS record types, and DNS server responses. Dig helps in troubleshooting DNS-related issues and gathering DNS information.
    
* Nslookup: Nslookup (Name Server Lookup) is a command-line tool used to query DNS servers to retrieve information about domain names. It allows you to obtain IP addresses associated with a domain, resolve DNS records, and perform reverse DNS lookups. Nslookup is useful for troubleshooting DNS issues and verifying DNS configurations.
    

### HTTP Error/status code:

When we send a request to the server we need some sort of way whether the request is successful or not. For this, we have an error code with the status:

Ex: We have many error codes few of which are below.

* 200: Request was successful
    
* 404: Not Found
    
* 400: Bad Request
    
* 500: Internal server error
    
* 1XX: Information code
    
* 2XX: Success code
    
* 3XX: Redirecting Purpose
    
* 4XX: Client error
    
* 5XX: Server error
    

Hope this was informational, Thank you for your time !!
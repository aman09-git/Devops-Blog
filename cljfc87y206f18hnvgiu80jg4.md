---
title: "Computer Networking : Part 1"
seoTitle: "OSI Model, TCP/IP Model, Networkings, Protocols, UDP, DHCP, ICMP, SSH"
seoDescription: "Discover the fundamentals of computer networking in our comprehensive blog. Explore the OSI model and TCP/IP model, understanding their layers and functions"
datePublished: Wed Jun 28 2023 06:30:41 GMT+0000 (Coordinated Universal Time)
cuid: cljfc87y206f18hnvgiu80jg4
slug: computer-networking-part-1
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/9wWX_jwDHeM/upload/3fa16daf5570c990c76bdf4d9852adb7.jpeg
tags: software-development, devops, networking, tcp, osi

---

### Network:

In simple terms, it just means computers connected, it refers to a collection of interconnected devices, such as computers, servers, routers, switches, and other network-enabled devices, that are linked together to facilitate communication and resource sharing. Networks are designed to allow these devices to exchange data, share resources (such as printers and files), and communicate with each other.

Networking plays a crucial role in DevOps by facilitating communication, resource sharing, and infrastructure automation, enabling seamless deployment, monitoring, and scaling of applications, ensuring efficient collaboration, and enhancing overall system reliability and performance.

### Internet:

A collection of computer networks is called as Internet. It's a network of network that helps us to communicate over the network with the help of fiber optic cables across the globe which are spread under the seawater.

These cables are owned by tech giants and ISP providers like Tata, Airtel, Google, and IDEA depending on the tier of cities. Also, please refer below image for the high-level overview of network architecture, there are a few more components included here like protocols, firewalls, proxies, network topologies etc.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1687251965796/96a9677b-7e46-4817-85c7-94e88f86c521.png align="center")

### Types of Network:

Networks can be classified into different types based on their geographical coverage and the way they are structured:

1. A Campus Area Network (CAN) is a network that connects multiple LANs within a limited geographical area, such as a university campus or corporate office complex. Example: Connecting different departments within a university campus using a shared network infrastructure.
    
2. Local Area Network (LAN): A LAN is a network that covers a small geographical area, such as a home, office building, or campus. It typically connects devices within a limited area, allowing for high-speed data transfer and resource sharing.
    
3. Wide Area Network (WAN): A WAN spans larger areas, such as cities, countries, or even globally. It connects multiple LANs together using routers and telecommunication links, such as leased lines, fiber-optic cables, or satellite connections. The Internet is the most prominent example of a WAN.
    
4. Metropolitan Area Network (MAN): A MAN covers a larger area than a LAN but is smaller than a WAN. It connects multiple LANs within a city or metropolitan area using high-speed connections, such as fiber-optic cables.
    
5. Wireless Networks: Wireless networks use wireless communication technologies, such as Wi-Fi (Wireless Fidelity) or cellular networks, to connect devices without the need for physical cables. They are commonly used for connecting laptops, smartphones, tablets, and IoT (Internet of Things) devices.
    

### Protocols:

* IP (Internet Protocol): The fundamental protocol for addressing and routing data packets on the internet. Example: IPv4, IPv6.
    
* HTTP (Hypertext Transfer Protocol): Used for transferring hypertext documents on the web. Example: [**http://www.example.com**](http://www.example.com)
    
* HTTPS (Hypertext Transfer Protocol Secure): Secure version of HTTP that encrypts data to ensure secure communication. Example: [**https://www.example.com**](https://www.example.com)
    
* ICMP (Internet Control Message Protocol): Used for sending error messages and operational information about IP networks. Example: Ping command.
    
* ARP (Address Resolution Protocol): Resolves IP addresses to MAC addresses in a local network. Example: Obtaining the MAC address of a device.
    
* RARP (Reverse Address Resolution Protocol): Resolves MAC addresses to IP addresses. Example: Obtaining an IP address from a MAC address.
    
* UDP (User Datagram Protocol): A lightweight, connectionless transport protocol that allows the transmission of datagrams. Example: DNS.
    
* FTP (File Transfer Protocol): Used for transferring files between a client and server on a network. Example: Uploading files to a website.
    
* SSL (Secure Sockets Layer): Provides encryption and secure communication for web browsers and servers. Example: HTTPS encryption.
    
* POP (Post Office Protocol): Retrieves email from a remote mail server to a client. Example: Downloading emails to a mail client.
    
* DHCP (Dynamic Host Configuration Protocol): Assigns IP addresses dynamically to network devices. Example: Getting an IP address from a router.
    
* SNMP (Simple Network Management Protocol): Manages and monitors network devices and retrieves information from them. Example: Network monitoring.
    
* SSH (Secure Shell): Provides secure remote access and encrypted communication between networked devices. Example: Securely accessing a remote server.
    
* SIP (Session Initiation Protocol): Establishes, modifies, and terminates multimedia sessions like voice and video calls over IP networks. Example: VoIP calls.
    
* RPC (Remote Procedure Call): Allows a program on one computer to execute code on a remote server. Example: Remote method invocation.
    
* TCP (Transmission Control Protocol): Reliable, connection-oriented protocol for sending data packets over a network. Example: Web browsing.
    

### OSI Model:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1687606913931/ecb0b7ea-f846-4565-be6e-b753be3991f1.png align="center")

The OSI (Open Systems Interconnection) model is a conceptual framework that describes the functions of a communication system into seven different layers. Each layer has its specific responsibilities and protocols. Let's go through them:

1. Application Layer: The Application Layer, the seventh and topmost layer of the OSI model, provides services directly to end-users and enables specific applications to interact with the network.
    
    Protocols used in the Application Layer include:
    
    1. Domain Name System (DNS): Translates domain names into IP addresses, allowing users to access websites using human-readable addresses.
        
    2. File Transfer Protocol (FTP): Facilitates the transfer of files between a client and a server over a network.
        
    3. Simple Mail Transfer Protocol (SMTP): Handles the sending and receiving of email messages between mail servers.
        
    
    Example: When you browse the internet, the Application Layer comes into play. Protocols such as DNS resolve domain names (e.g., [**www.example.com**](http://www.example.com)) to their corresponding IP addresses, enabling you to access websites. FTP allows you to upload or download files from remote servers, while SMTP handles the transmission of emails from one server to another. These protocols provide the necessary services for specific applications to function and communicate effectively over the network.
    
2. Presentation Layer: The Presentation Layer, the sixth layer of the OSI model, handles the presentation and transformation of data. It ensures that data sent by one application can be understood by another application, regardless of their differences in syntax or format.
    
    Protocols used in the Presentation Layer include:
    
    1. Hypertext Transfer Protocol (HTTP): Transfers hypertext content over the internet and defines how web browsers present and interact with web pages.
        
    2. Secure Sockets Layer (SSL) / Transport Layer Security (TLS): Provides encryption and decryption services to secure data during transmission, ensuring confidentiality and integrity.
        
    3. Multipurpose Internet Mail Extensions (MIME): Enables the exchange of different types of data, such as emails with attachments or multimedia content, by defining their formatting and encoding.
        
    
    Example: When you access a website using HTTP, the Presentation Layer is responsible for interpreting and rendering the web page's content on your web browser. It ensures that the data is transformed and presented in a readable format, including text, images, videos, and other multimedia elements. Additionally, SSL/TLS protocols encrypt the data to ensure secure communication between the client and the server.
    
3. Session Layer: The Session Layer, the fifth layer of the OSI model, establishes, maintains, and terminates communication sessions between applications. It allows synchronization, checkpointing, and recovery during data exchange.
    
    Protocols used in the Session Layer include:
    
    1. Secure Shell (SSH): Provides secure remote access and enables session management between a client and a server.
        
    2. Remote Procedure Call (RPC): Allows a program on one computer to execute code on a remote server, maintaining a session throughout the procedure.
        
    
    Example: When you establish a remote connection to a server using SSH, the Session Layer handles the establishment of the session, authentication, and encryption. It enables secure communication and maintains the session throughout the interaction, allowing you to execute commands or transfer files securely.
    
4. Transport Layer: It is the heart of OSI model. The Transport Layer, the fourth layer of the OSI model, is responsible for reliable end-to-end data delivery and error detection. It ensures that data is properly segmented, delivered, and assembled on the receiving end.
    
    Protocols used in the Transport Layer include:
    
    1. Transmission Control Protocol (TCP): Provides reliable, connection-oriented delivery of data, ensuring that packets are delivered in the correct order and without errors.
        
    2. User Datagram Protocol (UDP): Offers connectionless, unreliable delivery of data without error correction or sequencing. It is suitable for applications that prioritize speed over reliability.
        
        Example: When you download a file from a website, TCP is used to ensure that the file is received intact and without errors. UDP, on the other hand, is commonly used for real-time streaming applications, such as video or voice calls, where a small delay is acceptable, but immediate delivery is more important than reliability.
        
5. Network Layer: The Network Layer, the third layer of the OSI model, is responsible for the logical addressing and routing of data packets across different networks. It determines the best path for data to travel from the source to the destination.
    
    Protocols used in the Network Layer include:
    
    1. Internet Protocol (IP): Assigns unique IP addresses to devices and enables the routing of data packets across the internet.
        
    2. Routing Information Protocol (RIP): A dynamic routing protocol that helps routers exchange information to determine the best path for data.
        
    3. Border Gateway Protocol (BGP): A routing protocol used for communication between autonomous systems (ASes) on the internet.
        
    
    Example: When you access a website, your device uses IP to communicate with the website's server by sending and receiving packets over the internet. IP ensures that the packets are properly addressed and routed to the destination server, allowing you to access the desired web page.
    
6. Data Link Layer: The Data Link Layer, the second layer of the OSI model, is responsible for the reliable transmission of data frames between nodes on the same network. It ensures error-free communication over the physical layer.
    
    Protocols used in the Data Link Layer include:
    
    1. Ethernet: Defines the standards for framing and transmitting data packets over wired networks.
        
    2. Point-to-Point Protocol (PPP): Establishes a direct connection between two nodes and enables data transmission over serial links.
        
    
    Example: When you connect your computer to a local area network (LAN) using an Ethernet cable, the Data Link Layer is responsible for packaging your data into frames and transmitting them to the network. Ethernet ensures that the frames are properly formatted, error-free, and delivered to the intended recipient within the same network.
    
7. Physical Layer: The Physical Layer, the first layer of the OSI model, deals with the physical transmission of data over the network. It encompasses the actual hardware and physical components that enable communication.
    
    Protocols used in the Physical Layer include:
    
    1. Ethernet: Specifies the physical and electrical characteristics, such as cable types, connectors, and signaling, for wired network connections.
        
    2. Wi-Fi (IEEE 802.11): Defines the standards for wireless network communication, including radio frequencies, channels, and modulation techniques.
        
    
    Example: When you connect to the internet using an Ethernet cable, the Physical Layer is responsible for the transmission of electrical signals over the cable to establish a network connection. It ensures that the physical medium, whether it's copper or fiber optic cable, wireless radio waves, or other means, is capable of transmitting the data reliably.
    
    ### TCP/IP Model:
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1687873200242/ad3e5c74-faff-4be9-9094-b703e3151c12.png align="center")
    
    This model is used in real-time. The TCP/IP model is a network protocol suite used for internet communication. It consists of four layers: Network Interface, Internet, Transport, and Application.
    
    1. Application Layer:
        
        * Protocols: Hypertext Transfer Protocol (HTTP), File Transfer Protocol (FTP), Simple Mail Transfer Protocol (SMTP), Domain Name System (DNS).
            
        * Example: HTTP is used for browsing websites, FTP for transferring files, SMTP for sending emails, and DNS for translating domain names into IP addresses.
            
    2. Transport Layer:
        
        * Protocols: Transmission Control Protocol (TCP), User Datagram Protocol (UDP).
            
        * Example: TCP ensures reliable, ordered delivery of data, like when downloading a file, while UDP allows quick transmission of data, suitable for real-time applications like video streaming.
            
    3. Internet Layer:
        
        * Protocols: Internet Protocol (IP), Internet Control Message Protocol (ICMP), Address Resolution Protocol (ARP), Reverse Address Resolution Protocol (RARP).
            
        * Example: IP addresses are used to uniquely identify devices on the internet and enable routing of data packets.
            
    4. Network Interface Layer:
        
        * Protocols: Ethernet, Wi-Fi (IEEE 802.11), and others.
            
        * Example: Ethernet allows devices to connect to a local area network (LAN) using wired connections.
            
    
    Example: When you visit a website, the TCP/IP model comes into play. The Application Layer protocols, such as HTTP, enable your browser to request and receive web pages. The Transport Layer protocols, like TCP, ensure the reliable delivery of data packets. The Internet Layer protocols, including IP, handle addressing and routing across networks. Finally, the Network Interface Layer protocols, like Ethernet or Wi-Fi, handle the physical transmission of data between your device and the network.
    

### Networking Topologies:

Networking topologies refer to the physical or logical arrangement of devices within a computer network. They determine how devices are interconnected and how data flows within the network. Each topology has its advantages and limitations in terms of scalability, performance, and fault tolerance. Let's explore some commonly used networking topologies:

Two main types of network topologies in computer networks are

1. Physical topology
    
2. Logical topology
    

The physical arrangement of the computer wires and other network components makes up this form of network.

Logical topology: Logical topology provides information on the physical architecture of a network.

* Bus Topology:
    
    * In a bus topology, all devices are connected to a central communication line called a bus.
        
    * Devices share this bus to transmit and receive data.
        
    * Advantages: Simple and cost-effective implementation, suitable for small networks.
        
    * Limitations: Limited scalability, vulnerability to a single point of failure if the main bus is damaged.
        
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1687873318186/f2d7dde0-8395-486e-8550-05c0970b670f.png align="center")
    

* Star Topology:
    
    * In a star topology, all devices are connected to a central device, such as a switch or hub.
        
    * Each device has a dedicated connection to the central device.
        
    * Advantages: Easy addition or removal of devices, better fault tolerance as the failure of one device does not affect others.
        
    * Limitations: Dependence on the central device, network disruption if the central device fails.
        

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1687873381775/b08d55c8-ff80-41b8-8440-bee2d6f55d97.png align="center")

* Ring Topology:
    
    * In a ring topology, devices are connected in a circular loop, where each device is connected to its adjacent devices.
        
    * Data circulates round the ring in one direction.
        
    * Advantages: Equal network access for all devices, no collisions between devices, and simpler data transmission compared to bus topology.
        
    * Limitations: Disruption of the entire network if a single device fails, limited scalability.
        
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1687873440965/a877cc69-e7ae-4d3a-82a4-aca2fd0afa18.png align="center")
    

* Mesh Topology:
    
    * In a mesh topology, each device is directly connected to every other device in the network.
        
    * It can be a full mesh (every device connected to every other device) or a partial mesh (selected devices interconnected).
        
    * Advantages: Robust and fault-tolerant, multiple data paths, absence of a single point of failure.
        
    * Limitations: Expensive and complex to implement, requires numerous connections for a full mesh topology.
        
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1687873472204/c87afadc-4fa2-4045-a540-c1d8acce5ea5.png align="center")
    

* Tree (Hierarchical) Topology:
    
    * In a tree topology, devices are organized in a hierarchical structure resembling a tree.
        
    * Devices are interconnected in parent-child relationships, with a central device acting as the root.
        
    * Advantages: Scalability and network expansion ease, efficiency in large networks.
        
    * Limitations: Dependency on the root device, network disruption if the root device fails.
        
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1687873529815/53f98314-3907-4db5-bc2c-e011149e1135.png align="center")
    
* Hybrid Topology:
    
    * Hybrid topology combines two or more different topologies.
        
    * For instance, a hybrid topology may include a combination of star and ring topologies.
        
    * Advantages: Offers the benefits of multiple topologies, and flexibility in network design.
        
    * Limitations: Complexity in implementation and management.
        
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1687873562062/62a938e2-bf84-4cac-a899-3035cba35b6c.png align="center")
    
    THANK YOU !!
    
    @[Kunal Kushwaha](@kunalk) @[Shubham Londhe](@TrainWithShubham)
    
    #wemakedevs
    
    #trainwithshubham
    
    #Kodekloud
    
    #www.kodekloud.com
---
title: "DNS : Domain Name System"
seoTitle: "DNS Resolution with Recursive and iterative query"
seoDescription: "This blog contains full functioning of DNS starting, including recursive and iterative query. This blog contains interview answers for a lot of big tech."
datePublished: Tue Jun 27 2023 07:39:52 GMT+0000 (Coordinated Universal Time)
cuid: cljdz9bqz000709l707xffxiq
slug: dns-domain-name-system
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1687851048780/331d13cd-3773-4756-b172-d3c26d7ebca1.jpeg
tags: dns, software-development, devops, software-engineering, dns-resolver

---

DNS stands for Domain Name System, which is a hierarchical and decentralized naming system used to translate domain names into IP addresses. This translation is necessary because computers communicate using IP addresses, which are numerical and difficult for humans to remember. DNS allows us to use domain names (such as [amazon.com](http://amazon.com)) to access websites and other online resources.  
The DNS system works by using a distributed database of DNS servers that contain information about domain names and their corresponding IP addresses. When a user types a domain name into their web browser, the browser sends a DNS request to a DNS resolver, which is typically provided by the user's Internet Service Provider (ISP). The resolver then sends a series of requests to different DNS servers until it finds the IP address associated with the requested domain name.  
  
To illustrate this process with an example, let's consider how DNS works for Amazon. When a user types "[amazon.com](http://amazon.com)" into their web browser, the browser sends a DNS request to the user's DNS resolver. The resolver first checks its local cache to see if it has the IP address for "[amazon.com](http://amazon.com)" stored. If not, the resolver sends a request to a root DNS server, which contains information about the top-level domain names (such as .com, .org, .net, etc.). The root server then responds with the IP address of a DNS server responsible for the .com top-level domain.  
  
The resolver then sends a request to the .com DNS server, which contains information about all domain names registered under the .com top-level domain. The .com DNS server responds with the IP address of the DNS server responsible for the "[amazon.com](http://amazon.com)" domain.  
  
The resolver then sends a request to the DNS server responsible for "[amazon.com](http://amazon.com)", which contains the IP address associated with that domain name. The DNS server responds with the IP address, and the resolver caches this information so it can be retrieved more quickly in the future.  
  
Finally, the resolver returns the IP address to the user's web browser, which then uses that IP address to establish a connection with the Amazon server and load the Amazon website. Once it is done, it saves the IP address in the DNS cache memory for a while, in case we want to reuse it.

Recursive and iterative queries are two types of DNS (Domain Name System) queries used to resolve domain names to IP addresses or vice versa.

### **Recursive query:**

A recursive query is a type of DNS query in which the DNS client requests the DNS server to provide the complete resolution of the domain name. The DNS server will query other DNS servers on behalf of the client until it finds the IP address or name associated with the domain name. The result is then returned to the client. Recursive queries are commonly used by DNS clients like web browsers, email clients, and operating systems.  
  
Example:  
When a user types in the domain name [www.google.com](http://www.google.com) into their web browser, the browser sends a recursive query to the DNS server to resolve the domain name to an IP address. The DNS server will query other DNS servers until it finds the IP address associated with the domain name, and then return the result to the web browser.  
Iterative query:

### **Iterative query:**

An iterative query is a type of DNS query in which the DNS client requests the DNS server to provide the best possible answer it has for the domain name, and then the client decides whether to use the answer or request more information from other DNS servers. The DNS server will respond with either the IP address or the name associated with the domain name, or a referral to another DNS server that might have more information. If the DNS client wants more information, it will query the next DNS server in the referral chain until it finds the answer.  
  
Example:  
When a DNS server receives an iterative query from another DNS server for a domain name it does not have in its cache, it will respond with a referral to another DNS server that might have more information. The DNS client will then query the next DNS server in the referral chain until it finds the IP address or name associated with the domain name.

In summary, recursive queries are used by DNS clients to get the complete resolution of a domain name, while iterative queries are used by DNS servers to provide the best possible answer they have and let the DNS client decide whether to use it or request more information.

**P.S: It's an interview question as well for Amazon especially.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1687851323101/1ea7c9ed-dc41-496d-8e90-96ea49294f53.png align="center")
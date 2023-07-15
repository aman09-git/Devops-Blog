---
title: "SSL and TLS"
seoTitle: "TLS and SSL plays an important role in security in Networking."
seoDescription: "SSL (Secure Sockets Layer) and TLS (Transport Layer Security) are protocols used to establish secure connections between client and server over the internet"
datePublished: Tue Jun 27 2023 08:49:52 GMT+0000 (Coordinated Universal Time)
cuid: clje1rcrz000409k29w587gxr
slug: ssl-and-tls
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/mT7lXZPjk7U/upload/a7fa6827ceb7141c99cc4785a9a5f4bd.jpeg
tags: software-development, security, devops, software-engineering, ssltls

---

Understanding SSL and TLS: Essential Security Protocols for Online Communications”

SSL (Secure Sockets Layer) and TLS (Transport Layer Security) are protocols used to establish secure connections between client and server over the internet.

Main points to remember for SSL and TLS :

* Handshake
    
* Server authentication
    
* Client authentication
    
* Key exchange
    
* Symmetric encryption
    
* Secure communication
    
* Cipher suite negotiation ( For TLS only)
    

We use two kinds of encryption, Symmetric & Asymmetric. The main difference is that symmetric encryption uses the same key to encrypt and decrypt data. In contrast, asymmetric encryption uses a pair of keys – a public key to encrypt data and a private key to decrypt information. Both symmetric and asymmetric algorithms provide authentication capability.

Let’s dig into it and understand it with a real-time scenario. In this we are using our web browser and an online service, let’s say net banking.

With Symmetric key Hackers can get all the data with the key over the network.

To make it secure as a standard we use Asymmetric keys, where 2 keys are generated one is a public key and the other is the private key. So we make 2 keys on the server one is a public key and the other is a private key. Once we hit the Https on the web, the public key is sent to our web browser and we send it back with the Symmetric key. And the hacker gets the public key and the symmetric key which is of no use to him, bcoz the server decrypts the data from its private key and retrieves the symmetric key from it.

In another scenario, Let’s say the hacker has made the same replica of the website that we were using, now he is trying to send the public key with his private key. But to overcome this threat we have trusted certificate authorities (Symantec, Globalsign, DigiCert etc.) who certifies if the certificate that is getting generated is safe or not.

Again, how can we trust if the company where our certificates are getting signed is real or fake? Here again, the 2 key pair scenario comes in, the public key is sent by the web browser and the private key is with the certificate authority companies.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1687855599740/8b9b872d-faa8-4eec-9a17-e79f16ccc6fa.png align="center")

Thank you !!

#KodeKloud #wemakedevs #ByteByteGo #Devops
# Web Development Roadmap

# Table of Contents
- [Web Basics](#web-basics)
  - [The Internet in a Nutshell](#the-internet-in-a-nutshell)
  - [The World Wide Web](#the-world-wide-web)

## Web Basics
### The Internet in a Nutshell

The Internet is a global network of interconnected computers that has revolutionized how we communicate, access information, and conduct business. At its core, it's a vast system that allows data to be transmitted between devices anywhere in the world.

#### Key Components

1. **Infrastructure**: The physical layer of the Internet.
    - Fiber optic cables (e.g., transatlantic cables like MAREA)
    - Satellite networks (e.g., Starlink)
    - Cellular networks (4G, 5G)
    - Internet Exchange Points (IXPs)

2. **Protocols**: Standardized rules for data communication.
    - TCP/IP (Transmission Control Protocol/Internet Protocol)

3. **Servers**: High-performance computers that store, process, and distribute data.
    - Web servers (e.g., Apache, Nginx)
    - Database servers (e.g., MySQL, PostgreSQL)
    - Application servers (e.g., Tomcat, Node.js)

4. **Clients**: End-user devices that request and receive data.
    - Desktop computers, smartphones, IoT devices

#### Key Concepts

##### 1. IP Address

A numerical label assigned to each device participating in a computer network that uses the Internet Protocol for communication.

- **IPv4**: 32-bit address space (e.g., 192.168.1.1)
- **IPv6**: 128-bit address space (e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334)

```
IPv4: 192.168.1.1
IPv6: 2001:0db8:85a3::8a2e:0370:7334 (compressed form)
```

##### 2. Domain

Human-readable names mapped to IP addresses through the Domain Name System.

- **Structure**: `[subdomain.]domain.TLD`
- **Example**: `www.example.com`
    - `www` - subdomain
    - `example` - second-level domain
    - `com` - Top-Level Domain (TLD)

##### 3. URL (Uniform Resource Locator)

A reference to a web resource that specifies its location on a computer network and a mechanism for retrieving it.

- **Structure**: `scheme:[//[user:password@]host[:port]][/]path[?query][#fragment]`
- **Example**: `https://api.example.com:8080/v1/users?active=true#info`
    - `https://` - scheme
    - `api.example.com` - host
    - `:8080` - port
    - `/v1/users` - path
    - `?active=true` - query
    - `#info` - fragment

##### 4. Protocol

A set of rules or procedures for transmitting data between electronic devices.

- **HTTP/HTTPS**: Application layer protocol for distributed, collaborative, hypermedia information systems
- **FTP**: Standard network protocol used for file transfer between a client and server
- **SMTP**: Internet standard for email transmission

##### 5. DNS (Domain Name System)

A hierarchical and decentralized naming system for computers, services, or other resources connected to the Internet or a private network.

- **Process**:
    1. User enters "www.example.com" in browser
    2. Recursive DNS resolver queries root nameserver
    3. Root server responds with TLD nameserver (.com)
    4. TLD nameserver provides authoritative nameserver for example.com
    5. Authoritative nameserver returns IP address for www.example.com
    6. Resolver returns IP address to client
    7. Client establishes connection with the IP address

```shell
dig +trace www.example.com
```

This command demonstrates the DNS resolution process, showing each step from root to authoritative nameserver.

---

### The World Wide Web

The **World Wide Web (WWW)**, commonly known as the Web, is a system of interlinked hypertext documents accessed via the Internet. It has revolutionized the way people communicate, access information, and conduct business globally. Invented by British computer scientist Tim Berners-Lee in 1989, the Web has become an integral part of modern life and has transformed nearly every aspect of society.


#### Key Components of the Web

1. **HTML (Hypertext Markup Language)**: The standard language used to create web pages.
2. **HTTP (Hypertext Transfer Protocol)**: The protocol for transmitting data over the Web.
3. **URLs (Uniform Resource Locators)**: Unique addresses for web resources.
4. **Web browsers**: Software applications used to access and navigate the Web.
5. **Web servers**: Computers that host websites and respond to requests from browsers.

#### Evolution of the Web

##### Web 1.0 (1989-2004)
- Static HTML websites
- Limited user interaction
- One-way communication from website to user

##### Web 2.0 (2004-2014)
- Dynamic, interactive websites
- User-generated content (blogs, wikis, social media)
- Cloud computing and mobile web

##### Web 3.0 (2014-present)
- Semantic Web and AI integration
- Decentralized networks and blockchain technology
- Internet of Things (IoT) integration

#### The Difference Between the World Wide Web and the Internet

##### The Internet

- The Internet is a global network of interconnected computer networks.
- It's **the infrastructure that allows computers worldwide to communicate** with each other.
- The Internet predates the World Wide Web and supports various services beyond web browsing, such as email, file transfer (FTP), and instant messaging.

##### The World Wide Web

- The World Wide Web is a service that operates over the Internet.
- It's **a system of interlinked hypertext documents** accessed via the Internet.
- The Web uses HTTP to transmit data and web browsers to access information.
- It's just one of many services that use the Internet as its underlying network infrastructure.

In essence, the Internet is the hardware and software infrastructure that enables global computer networking, while the World Wide Web is a service built on top of this infrastructure, specifically designed for sharing and accessing information through web pages.

---

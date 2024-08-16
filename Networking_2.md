# Networking Fundamentals: OSI Model and TCP/IP

## Table of Contents

1. [OSI Model](#osi-model)
   - [Application Layer](#application-layer)
   - [Presentation Layer](#presentation-layer)
   - [Session Layer](#session-layer)
   - [Transport Layer](#transport-layer)
   - [Network Layer](#network-layer)
   - [Data Link Layer](#data-link-layer)
   - [Physical Layer](#physical-layer)
2. [TCP/IP Model](#tcpip-model)
3. [Application Layer](#application-layer-1)
   - [Client-Server Architecture](#client-server-architecture)
   - [Peer-to-Peer Architecture](#peer-to-peer-architecture)
   - [Networking Devices](#networking-devices)
   - [Protocols](#protocols)
   - [HTTP](#http)
   - [Cookies](#cookies)
   - [Email Protocols](#email-protocols)
   - [DNS (Domain Name System)](#dns-domain-name-system)
4. [Transport Layer](#transport-layer-1)
   - [UDP (User Datagram Protocol)](#udp-user-datagram-protocol)
   - [TCP (Transmission Control Protocol)](#tcp-transmission-control-protocol)
   - [Three-Way Handshake](#three-way-handshake)
5. [Network Layer](#network-layer-1)
   - [IP Addressing](#ip-addressing)
   - [Subnetting](#subnetting)
   - [IPv6](#ipv6)
   - [Middle Boxes](#middle-boxes)
6. [Data Link Layer](#data-link-layer-1)

## OSI Model

The Open System Interconnection (OSI) model consists of 7 layers:

### Application Layer
- Implemented in software
- Includes applications like browsers and chat apps

### Presentation Layer
- Converts messages and data into machine-readable binary format
- Handles encoding and encryption
- Provides abstraction, compression, and translation

### Session Layer
- Sets up and manages connections
- Enables sending and receiving of data
- Handles authentication and authorization

### Transport Layer
- Divides data into segments
- Assigns source and destination ports, sequence numbers, and flow control
- Performs error control
- Uses UDP and TCP protocols

### Network Layer
- Handles transmission of data segments between computers in different networks
- Performs IP addressing (logical addressing)
- Handles routing and load balancing

### Data Link Layer
- Performs physical addressing using MAC addresses
- Creates frames by assigning sender and receiver addresses to packets

### Physical Layer
- Includes hardware components like cables and wires

### Example:
![Screenshot 2024-08-15 091548](https://github.com/user-attachments/assets/b901e75a-ae85-4f7c-9ae3-7eb21b869a05)


## TCP/IP Model

The TCP/IP model, also known as the Internet Protocol Suite, consists of 5 layers:

1. Application Layer
2. Transport Layer
3. Network Layer
4. Data Link Layer
5. Physical Layer

## Application Layer
- This is the layer where the users interact with it.
- It lies on our devices
- It consists of applications like web browsers, chat applications.
  
### Client-Server Architecture
- Servers control hosted websites
- Clients consume resources (e.g., making requests to Google)
- Data centers are collections of servers with static IP addresses
- A server is basically a system that controls the website you are hosting.
- The application has two parts: client part and server part. These are known as processes and they communicate through each other.
- Clients are the ones who are using/consuming these resources like we making a request to google.
- A collection server is known as data centers.
- Data centers is a collection of huge number of computers it may have static IP addresses. They have good internet connection and high upload speed.
- Command : ping google.com
- Ping mesarues the round trip time for messages send from the origination host to the destination computer and are echoed back. 

### Peer-to-Peer Architecture
- No dedicated server; computers are connected to each other
- Each computer can act as both client and server
- Example: BitTorrent, University labs.

### Networking Devices

### 1. **Repeater**
   - **What it is**: A repeater is a network device used to regenerate or replicate signals in a network.
   - **How it’s used**: It extends the range of a network by amplifying the signal, allowing it to travel longer distances without degradation.

### 2. **Hub**
   - **What it is**: A hub is a basic networking device that connects multiple Ethernet devices, making them act as a single network segment.
   - **How it’s used**: It broadcasts data to all devices connected to it, making it less efficient and more prone to collisions in large networks.

### 3. **Bridge**
   - **What it is**: A bridge is a device that connects and filters traffic between two or more network segments.
   - **How it’s used**: It reduces network traffic by dividing a large network into smaller, more manageable segments and only forwarding data to the correct segment.

### 4. **Switch**
   - **What it is**: A switch is a more advanced version of a hub that connects devices on a network and uses MAC addresses to forward data only to the intended recipient.
   - **How it’s used**: It reduces collisions and increases network efficiency by ensuring that data is only sent to the device it is intended for.

### 5. **Router**
   - **What it is**: A router is a device that forwards data packets between different networks, typically connecting a local network to the internet.
   - **How it’s used**: It directs data along the best path to its destination, often connecting multiple networks and managing traffic between them.

### 6. **Gateway**
   - **What it is**: A gateway is a network device that acts as an entrance to another network, often translating between different protocols or formats.
   - **How it’s used**: It enables communication between different networks that use different protocols, such as connecting a local network to the internet.

### 7. **Brouter**
   - **What it is**: A brouter (bridge router) is a hybrid device that functions as both a bridge and a router.
   - **How it’s used**: It routes data between networks like a router but can also filter traffic within a network segment like a bridge, combining the functions of both devices.

These devices each play a unique role in ensuring efficient and effective communication within and between networks.

### Protocols
- HTTP (Hyper Text Transfer Protocol)
- DHCP (Dynamic Host Control Protocol)
- FTP (File Transfer Protocol)
- SMTP (Simple Mail Transfer Protocol)
- POP3 & IMAP (for receiving mail)
- SSH (Secure Shell)
- VNC (Virtual Network Computing)
- Telnet (Terminal emulation, port 23)

***Sockets: Interface between process and internet.***

### Ports:  

- IP Address tells us which device we are working with while ports tell us which application we are working with.
- There may be possibility of many proceses of single application is running like opening up many tabs in chrome wen the response is coming back how it will know which tab in chrome when the response is coming back how it will know which tab to give the data. This can be resolved using EPHEMERAL PORTS. 

 
### HTTP
- Client-server protocol
- Uses TCP
- Stateless protocol
- Methods: GET, POST, PUT, DELETE
- Status codes: 1xx (Informational), 2xx (Success), 3xx (Redirection), 4xx (Client Error), 5xx (Server Error)

### HTTP Methods: 

- Method is basically telling the server what to do. 
- GET – It means you are requesting some data.
- POST – client gives some data to the server like web forms.
- PUT – puts data at a specific location.
- DELETE – to delete data from the server. 

 ### Error/Status Code: 
- When you send a request to the server you need some sort of a way to know whether the request is successful or not.
- For this there exists STATUS CODES.
- 1XX – Informational Category
- 2XX – Success Code
- 3XX – Redirecting purpose
- 4XX – Client error
- 5XX – server error. 

Example: 
- 200– request was successful
- 300 – not found
- 400 – bad request
- 500 – internal server error 

### Cookies
- Unique strings stored on client's browser
- Used to maintain state in stateless HTTP
- Can have expiration dates
- Third-party cookies: set for URLs not visited

### Email Protocols
- SMTP (Simple Mail Transfer Protocol) for sending emails
- POP3 (Post Office Protocol) for receiving emails
- IMAP (Internet Message Access Protocol) for syncing emails across devices

### How Email works? 
- Application layer protocol : SMTP(Simple Mail Transfer Protocol)
- For sending email – SMTP
- For receiving email - POP3
- Transfer Layer Protocol: TCPSMTP: 

- A push protocol that acts as a message transfer agent(MTA) to send mails from the senders device to the receiver mail server.
- SMTP ensures emails are formatted and transmitted securely 
- SMTP works between the senders and receivers mail servers. 
![Screenshot 2024-08-15 092422](https://github.com/user-attachments/assets/0bef4e9b-3533-40e0-b1c1-67a1fa416c0b)

### POP: Post Office Protocol 
- A POP protocol that acts as a message access agent(MAA) to retrieve emails from the receivers mail server to the receivers device.
- POP3 allows users to access their mails offline, view attachments  quickly, and reduce the amount of storage space on the server.
- However it doesn't sync emails across devices. 
![Screenshot 2024-08-15 092507](https://github.com/user-attachments/assets/983f4c23-cbf2-478c-9958-55ae7af6aa94)

 
### DNS (Domain Name System)
- Maps domain names to IP addresses
- Hierarchy: Top-level domain, Second-level domain, Subdomain
- Managed by ICANN (Internet Corporation for Assigned Names and Numbers)

### Example: 
- Mail.google.com
- Mail -> subdomain
- Google -> second level domain
- Com -> top level domain.
![Screenshot 2024-08-15 093246](https://github.com/user-attachments/assets/5c9eb3e4-83a2-4ed6-9e7a-dc9bec84274e)

- Top level domain(TLD), they are like organization specific fro example .com for commercial, .edu for education, .uk, .in -> country specific
- These are managed by ICANN (Internet Corporation For Assigned Names and Numbers)
![Screenshot 2024-08-15 093815](https://github.com/user-attachments/assets/8ef225c1-410a-42f5-a1f8-b34167c8a588)

- When we search something so it will store in local cache to use it again and again rather searching through whole DNS.
- Imagine if we don’t have that url now it searches in local DNS (ISP) so our ISP knows all our activity which websites we are using and all. 

 
## Transport Layer

- Provides abstraction between network and application layers
- Handles data transfer from network to application
- Attaches socket port numbers to packets
- Manages congestion control
- Data Transferred between one computer to another is done by using NETWORK LAYER.
- Example of delivery system from one country to another country. After it lands in another country the distrubtion partner takes care of deliverying this is called transport layer.
- One country -> another country - ---- -> network layer
- Distribution partner -> to customer ---> transport layer.
- Transport layer is a layer that lies over devices.
- The role of the transport layer is to take the data from the network to the application(browser)
- Network (one)----> Network(another) - Taken care by Network layer
- Network(from) ----> Application(To) - Taken care by Transport layer.
- Provides abstraction
- Located on the devices.

![Screenshot 2024-08-15 102318](https://github.com/user-attachments/assets/949ed5cb-5958-4fb1-bd3b-0acab4286c8d)

- How we send any file/message anything over internet to a person?
- Data travels in packets
- Transport layer will attach these socket port numbers to that packets so that it delivers to that particular tab in an application
- Transport layer also takes care of congestion(traffic) control
- Congestion control algorithms built in TCP. 

### CheckSums:
- Let's say sometimes data can be lost/corrupeted.
- Checksums are used to confirm whether the data has corrupted or not.
- If we sent some messages and if it doesn't deliver in order he can't understand the message.
- So we need everything to be in order and correct.
- So TCP takes care of all these using CHECK SUM.
- Check sum is a random number
![Screenshot 2024-08-15 103326](https://github.com/user-attachments/assets/75bb81de-965b-475f-92d9-af8380f0d4e9)

- How would I know if the data is received or not ? Timers 
### Timers :

![Screenshot 2024-08-15 103450](https://github.com/user-attachments/assets/ca37df8c-9c63-4836-ba61-e8811888f25d)

- Lets say we send the packet 2 and received by didn't send the acknowledgement.
- Now we send packet 2 again now the duplicates are present.
- How do we solve this issue using sequence number. 

 
### UDP (User Datagram Protocol)
- Connectionless protocol
- Fast but unreliable
- Used in video conferencing, DNS, and gaming
- UDP uses checksums and if there is any error it won’t care. 

![Screenshot 2024-08-15 103550](https://github.com/user-attachments/assets/1e1598e1-7725-49b4-b137-4034a6ef54c3)

- Uses cases of UDP:
- It is very fast
- Video conferencing apps
- DNS uses UDP
- Gaming. 

### TCP (Transmission Control Protocol)
- Connection-oriented protocol
- Provides error control, congestion control, and full-duplex communication
- Maintains data order using sequence numbers
- Application layer sends lot of raw data. TCP segments this data divide in chunks add headers etc.
- It may also collect the data from network layer and the small chunks are put in to one in the receiving end.
- Congestion control
- Takes care of when data does not arrive.
- Maintains the order of data(using sequence number) 

#### Features: 
- Connections oriented
- Error control
- Congestion control
- Full duplex ( we can send files any way we want )
- One TCP connection between two computers. 

### Three-Way Handshake
- Process for establishing a TCP connection
- Uses SYN and ACK flags
- For each connection we have SYNC,ACK Flags. 

![Screenshot 2024-08-15 105057](https://github.com/user-attachments/assets/f669b08b-d6bf-44b6-a3fd-0a45f2ca611a)

## Network Layer

- Data is in packets
- Works with routers
- Uses network addresses and routing tables
- Transport layer – data is in segments
- Network layer – data is in packets
- Data link layer – data is in frames
- Here we work with routers
- Every router has a NETWORK ADDRESS
- Every router will check whether the packet is for that router, if not then it will forward that using forward table in routing table.
- In IP Address 192.168.2.33
- 192.168.2 -> this part is Network Address (Subnet ID)
- .33 -> this part is device addresss (Host ID) 

#### Control Plane: 
- Used to build these routing tables.
- Router -> Nodes
- Links -> Edges
- There are two type of routing used to create tables:
1. static routing 
- Adding address manually
- Its not adoptive 

2. Dynamic routing
- When there is a change in network it will evolve accordingly. 
 
### IP Addressing
- IPv4: 32-bit addresses , 4 words
- IPv6: 128-bit addresses
- Classes of IP addresses: A, B, C, D, E
- Classes of IP Addresses:
- A – 0.0.0.0 - 127.255.255.255
- B – 128.0.0.0 - 191.255.255.255
- C – 192.0.0.0 - 239.255.255.255
- D – 224.0.0.0 - 239.255.255.255
- E – 240.0.0.0 - 255.255.255.255 

### Subnetting
- Dividing IP address blocks
- Subnet masking
- Variable-length subnets

Subnet Masking: 
- Subnet mask is going to mask the network part of the IP address and leaves us to use the host part(device address). 

Variable length subnets: 
- You can set your own subnet length. 
- Eg: 15.0.0.0/30 - This basically means just 30 bits are my subnet port. 

Reserved Addresses: 
- 127.0.0.0/8 
- Eg: localhost 127.0.0.1 (client also server also) loopback addresses 

Packets : Header is of 20 bytes it contain IPV, length, Identification number, flags, protocols, checksum, addresses, TTL( time to live) 

Time to Live: It is a number, after that number of hops, the packet doesn’t reach then it will leave. 

### IPv6
- Larger address space than IPv4
- Not backward compatible
- ISPs would have to shift lot of hardware work.
  
 

### Middle boxes: 
- They are extra devices that also interact with IP packets
- Mostly it will be in network layer but it can also be in transport layer as well 

1. Firewall
- Two types: connected to global internet , your local network.
- It filters out IP packets based on various rules. 
- Address, Modify packets, prot numbers, flags, protocols 

2. Stateless firewall  
- Doesn’t maintian a state 

3. Stateful firewall 
- See the packet and maintain its state
- More efficient 

#### Network Address Translator ( NAT): 
- It is  a method of mapping an IP address space into another by modifying network address information in thie IP header of packets while they are in transit across a traffic routing table. 

## Data Link Layer

- Responsible for sending packets over the physical layer
- Uses MAC addresses for communication between devices
- Implements Address Resolution Protocol (ARP) for address resolution
- New device goes to the DHCP(Dynamic Host Configuration protocol) server to get assigned the IP Address from the pool.
![Screenshot 2024-08-16 100310](https://github.com/user-attachments/assets/11a99a5b-f205-47a6-8919-7e51b3de52fe)

- In data link layer the devices communicate with each other using DATA LINK LAYER ADDRESS (MAC Address) 
- Lets say device 1 needs to send something to device 4 first it will look up in its cache. 
- If it doesn’t have then it will ask all other devices. This is known as ARP Cache(Address resolution protocol)
- Frame consists of  DLL of sender, IP address of destination 
 

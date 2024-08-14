### Networking Basics

### **Table of Contents**

1. [Introduction to Networking](#introduction-to-networking)
2. [History of the Internet](#history-of-the-internet)
3. [Protocols](#protocols)
4. [World Wide Web (WWW)](#world-wide-web-www)
5. [Client-Server Architecture](#client-server-architecture)
6. [How Data is Transferred](#how-data-is-transferred)
7. [Types of Networks](#types-of-networks)
8. [Networking Devices](#networking-devices)
9. [Network Topologies](#network-topologies)
10. [Wireless Technologies](#wireless-technologies)

---

### **1. Introduction to Networking**

- **Network:**
  - A collection of computers connected together.
  - Enables sharing of resources and information.
  
- **Internet:**
  - A global collection of interconnected networks.
  - Allows communication between millions of private, public, academic, business, and government networks.

---

### **2. History of the Internet**

- **ARPANET:**
  - Pilot program by the US called **Advanced Research Projects Agency Network**.
  - Connected four locations: MIT, Stanford, UCLA, University of Utah.
  - Used **TCP/IP protocol** for communication.

- **Expansion:**
  - ARPANET laid the foundation for the modern internet.
  - Evolved into a global network interconnecting various smaller networks.

---

### **3. Protocols**

- **Protocols:**
  - Set of rules for data transmission across networks.
  - Ensure reliable communication between devices.

- **Examples:**
  - **TCP (Transmission Control Protocol):**
    - Ensures data reaches its destination without corruption.
  - **UDP (User Datagram Protocol):**
    - Used when speed is prioritized over reliability (e.g., video conferencing).
  - **IP (Internet Protocol):**
    - Handles addressing and routing of packets.
  - **HTTP (Hypertext Transfer Protocol):**
    - Used by web browsers to request and display web pages.

- **Internet Society:**
  - Responsible for creating and maintaining these protocols.

---

### **4. World Wide Web (WWW)**

- **Definition:**
  - An information system accessible over the internet.
  - Consists of documents and web resources identified by URLs.
  - Documents are interlinked by hyperlinks.

- **Function:**
  - Revolutionized information access and sharing.
  - Provides a platform for websites, applications, and other online services.

---

### **5. Client-Server Architecture**

- **Client:**
  - Sends a request (e.g., google.com).
  - Requests resources or services from a server.

- **Server:**
  - Processes client requests.
  - Provides the requested resources or services.

- **Example:**
  - When a user types a URL, the browser (client) requests the webpage from the web server.

![Screenshot 2024-08-13 200321](https://github.com/user-attachments/assets/d840c05e-83a4-490a-81bb-e55ac5f2809d)

---

### **6. How Data is Transferred**

- **Data Packets:**
  - Data is broken into packets for transmission.
  - Packets are reassembled at the destination.

- **IP Address:**
  - Unique identifier for devices on the internet (e.g., 192.168.0.1).
  - **DNS (Domain Name System):**
    - Translates domain names into IP addresses.
  
- **DHCP (Dynamic Host Configuration Protocol):**
  - Assigns dynamic IP addresses to devices on a network.

- **NAT (Network Address Translation):**
  - Used by routers to map local IP addresses to a global IP address.
  - Routes incoming data to the correct local device.

- **Ports:**
  - IP address identifies the device.
  - Ports are basically 16 bit numbers
  - 0-1023 -> reserved ports
  - 1024-49152 -> registered for application(sql,mongodb)
  - Remaining for our use.
  - Port number identifies the specific application (e.g., HTTP uses port 80).

- **Speed Measurements:**
  - **1 kbps** = 1,000 bits per second.
  - **1 Mbps** = 1,000,000 bits per second.
  - **1 Gbps** = 1,000,000,000 bits per second.

- **Internet Backbone:**
  - Consists of high-speed fiber optic cables.
  - Often laid under the ocean to connect continents.
  - ISP acts a mediator to provide internet to us.

![Screenshot 2024-08-13 201456](https://github.com/user-attachments/assets/2a00207f-3e9a-4a6e-9c47-c07075945dfc)
- Data is being sent in packets.
- Servers are identified based on the IP Address(x.x.x.x)
- X- can have value between 0-25
- Every device that communicates on the internet have IP Address.
- IP Address are mapped to a name hance we hit the name.
- This name to IP address is done by DNS(Domain Name System).
- To check the IP Address of your own computer
- Command – curl ifconfig.me -s
- ISP – internet service provider provides a router/modem to access the internet.(This will have Global IP address)
- D1,D2,D3 are devices connected and modem gives IP address to these devices
- IP1,IP2,IP3 – local IP addresses
- DHCP – Dynamic Host Configuration Protocol is used by modem to assign IP Address. 

![Screenshot 2024-08-13 202335](https://github.com/user-attachments/assets/5bb94916-1051-436a-aa4f-b93ee69817ad)

- When we make a request google.com then the server will see the global IP Address.
- Once the request is responded then modem will route the response to that device based on NAT(Network Access Translator).
- IP Address decides which device to send the data whereas PORT NUMBERS are used to identify which application made that request.
- Based on the port number the data is sent to that application in a device by the router.
- IP Address identifies the computer, Port Number identifies the application. 
---

### **7. Types of Networks**

- **LAN (Local Area Network):**
  - Interconnects computers within a limited area (e.g., home, office).
  - Uses Ethernet cables or Wi-Fi.

- **MAN (Metropolitan Area Network):**
  - Covers a larger geographic area (e.g., city).
  - Interconnects multiple LANs.

- **WAN (Wide Area Network):**
  - Extends over a large geographic area (e.g., country, continent).
  - Often uses optical fiber cables.

- **SONET (Synchronous Optical Networking):**
  - Protocol for transferring data over fiber optic cables.

- **Frame Relay:**
  - Method for connecting LANs to WANs.

---

### **8. Networking Devices**

- **Modem (Modulation Demodulation):**
  - Converts digital signals to analog for transmission.
  - Converts analog signals back to digital.

- **Router:**
  - Directs data packets between networks.
  - Connects different networks (e.g., local network to the internet).

- **ISP (Internet Service Provider):**
  - Provides access to the internet.
  - Typically supplies a modem/router for connectivity.

---

### **9. Network Topologies**

- **Bus Topology:**
  - All devices connected to a single backbone.
  - Failure of the backbone causes network failure.
  - Only one person at a time can send info.

- **Ring Topology:**
  - Devices connected in a circular manner.
  - Break in the circle disrupts communication.
  - Lot of unnecessary calls are made.

- **Star Topology:**
  - Devices connected to a central hub.
  - Failure of the hub causes network failure.

- **Tree Topology:**
  - Combination of bus and star topologies.
  - Offers more flexibility and scalability.

- **Mesh Topology:**
  - Every device connected to every other device.
  - Provides redundancy but is expensive and complex.

---

### **10. Wireless Technologies**

- **Wireless Communication:**
  - Includes Bluetooth, Wi-Fi, 3G, 4G, LTE, 5G.
  - Faster and more convenient than satellite communication.

- **Wireless Networks:**
  - Allow devices to connect without physical cables.
  - Common in homes, offices, and public spaces.

---

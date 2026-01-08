# Networking Fundamentals – 

---

## What is a Network?

A **network** connects two or more gadgets so they can communicate and exchange data.

We use networks every day — for example, connecting a phone or computer to **Wi-Fi** to browse the internet.

Networks allow devices to:
- Share internet access
- Share documents and files
- Share printers and other resources

All of this happens quickly and smoothly through a network.

---

## What is a Subnet?

A **subnet** (sub-network) divides a large network into smaller parts.

Why subnets are used:
- Keeps the network organized
- Reduces unnecessary data traffic
- Improves performance and security

### Example  
In an office:
- HR department → HR subnet  
- Finance department → Finance subnet  
- IT department → IT subnet  

All are part of one main network but work independently for better speed and protection.

---

## What is VLAN?

**VLAN (Virtual Local Area Network)** divides one physical network into multiple virtual networks.

Devices connected to the **same switch** can be grouped logically based on their role.

### Example in a company:
- HR VLAN → HR computers  
- IT VLAN → Technical team  
- Sales VLAN → Sales department  

Even though all devices use the same hardware, they stay isolated unless routing is allowed.

### Benefits of VLAN:
- Improved security
- Reduced broadcast traffic
- Easier network management

---

## Switching & Routing (Route Table)

Switching and routing help move data across networks.

### Switching
- Works inside a **local network (LAN)**
- Uses **MAC addresses**
- Example: One PC sends data directly to another PC using a switch

### Routing
- Connects **different networks**
- Uses **IP addresses**
- A router checks its **route table** to decide the best path

### Route Table
A route table contains:
- Destination network
- Next hop
- Interface to use

**Switching = internal communication**  
**Routing = external communication**

---

## Ethernet Frame

An **Ethernet frame** is the Layer-2 data unit used to send data over Ethernet.

Data is never sent alone — it is wrapped like a letter in an envelope.

### Ethernet Frame Structure:
1. **Preamble** – Synchronizes sender and receiver  
2. **SFD (Start Frame Delimiter)** – Marks real frame start  
3. **Destination MAC** – Receiver’s address  
4. **Source MAC** – Sender’s address  
5. **EtherType / Length** – Type of payload (IPv4, ARP, etc.)  
6. **Payload** – Actual data (IP packet)  
7. **FCS (Frame Check Sequence)** – Error detection

---

## IP Address

An **IP address** uniquely identifies a device on a network.

It works like a **postal address**:
- Helps data reach the correct device
- Enables sending and receiving information

In a local network, every device has a unique IP address.  
Without IP addresses, targeted communication is impossible.

---

## Binary Math (0 and 1)

Computers understand only **binary** — 0s and 1s.

- `0` → Off / False / No  
- `1` → On / True / Yes  

Think of it like a switch:
- Off = 0
- On = 1

All networking data (IPs, files, commands) is converted into binary.

### Example:


---

## POP (Point of Presence)

A **POP** is a physical location where an ISP or cloud provider connects users to its network.

Think of it as a **nearby hub**.

### How it works:
- Your data reaches the closest POP
- Then moves to the larger internet

### Benefits:
- Lower latency
- Faster access
- Better reliability

Companies like AWS and Google use global POPs.

---

## Global Networks – Global Infrastructure  
### (Regions & Fault Tolerance)

Global networks spread infrastructure worldwide.

### Regions
A **region** is a geographic area with data centers, such as:
- India
- USA
- Europe

Benefits:
- Faster access for local users
- Compliance with data laws

### Fault Tolerance
Keeps systems running even if something fails.

Achieved using:
- Multiple regions
- Backups
- Automatic traffic switching

If one data center fails, another takes over.

---

## CIDR (Classless Inter-Domain Routing)

CIDR allows flexible IP address allocation.

Format:

- First 24 bits → Network
- Remaining bits → Hosts

CIDR avoids wasting IP addresses and replaces classful addressing.

---

## Classful Addressing

Old IP addressing method with fixed classes:

- **Class A** – Very large networks  
- **Class B** – Medium networks  
- **Class C** – Small networks  
- **Class D** – Multicast  
- **Class E** – Reserved  

Problem:  
- Fixed sizes caused IP wastage  

Solution:  
- Replaced by **CIDR**

---

## Network Physical Media Types

Physical media carries data signals.

### Types:
- **Twisted Pair (Copper)** – Cheap, common Ethernet cables  
- **Coaxial Cable** – Used in TV and broadband  
- **Fiber Optic** – Light-based, very fast, long distance  
- **Wireless (Wi-Fi / Radio)** – No cables, flexible, but interference-prone

---

## Network Address Translation (NAT)

NAT converts **private IPs** into a **public IP** for internet access.

### How it works:
- Internal devices use private IPs
- Router uses one public IP
- Responses are mapped back correctly

### Benefits:
- Saves public IP addresses
- Hides internal network
- Adds security

---

## DNS64 & NAT64

Used for **IPv6–IPv4 compatibility**.

### DNS64
- Converts IPv4 addresses into IPv6 format for IPv6-only devices

### NAT64
- Translates IPv6 traffic to IPv4 and back

Together, they allow smooth communication between IPv6 clients and IPv4 servers.

---

## Gateway / Netfilter

### Gateway
A gateway connects different networks.

Example:
- Home router acting as gateway to the internet

### Netfilter
A Linux packet-filtering framework.

Acts like a **security guard**:
- Allows packets
- Blocks packets
- Modifies traffic

Used for firewalls and traffic control.

---

## Proxy & Load Balancing

### Proxy
An intermediary between users and the internet.

Functions:
- Filters traffic
- Caches content
- Improves security
- Hides user identity

Example: Company proxy server

### Load Balancer
Distributes traffic across multiple servers.

Benefits:
- Prevents server overload
- Improves speed
- Ensures high availability

---

## In-Transit vs At-Rest Encryption

### In-Transit Encryption
Protects data while moving.

Examples:
- HTTPS / TLS
- VPN

### At-Rest Encryption
Protects stored data.

Examples:
- Encrypted disks
- Encrypted cloud storage

Both are essential for complete security.

---

## IPSec

IPSec secures IP communication.

Provides:
- Encryption
- Authentication
- Data integrity

Used in VPNs to create secure tunnels over public networks.

---

## Protocol Data Units (PDU)

A **PDU** is data formatted at each OSI layer.

### OSI Layers & PDUs:
- Application → Data
- Transport → Segment
- Network → Packet
- Data Link → Frame
- Physical → Bits

Each layer adds its own information for reliable delivery.

---

## Remote Desktop Protocol (RDP)

RDP allows you to control a remote computer over a network.

Features:
- View remote screen
- Use applications
- Access files

Used for:
- Remote work
- Technical support

Data is encrypted for security.

---

**End of Document**

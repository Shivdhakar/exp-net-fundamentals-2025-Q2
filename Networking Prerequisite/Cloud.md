# Cloud Networking Services – AWS, Azure, and Google Cloud

---

## AWS Networking Services

AWS provides multiple networking services to connect, secure, and manage cloud resources efficiently.

### Key AWS Networking Services

- **VPC (Virtual Private Cloud)**  
  Your isolated network inside AWS.  
  Think of it as a private area within a huge cloud complex where you control IP ranges, routing, and access.

- **Route 53**  
  AWS DNS service that converts domain names into IP addresses and routes user traffic globally with high availability.

- **Direct Connect**  
  A dedicated private connection between your on-premises network and AWS.  
  Offers low latency, high bandwidth, and improved security.

- **Elastic Load Balancing (ELB)**  
  Automatically distributes incoming traffic across multiple servers to improve availability and performance.

- **CloudFront**  
  AWS Content Delivery Network (CDN) that caches content near users for faster page loads.

- **VPN**  
  Creates an encrypted tunnel between your local network and AWS over the public internet.

- **Transit Gateway**  
  A central hub that connects multiple VPCs and on-premises networks, simplifying network architecture.

---

## AWS Enterprise / Hybrid Networking Services

Hybrid networking connects on-premises infrastructure with AWS securely.

- **Direct Connect**  
  High-speed, private connection that bypasses the public internet.

- **VPN**  
  Encrypted internet-based connection for offices or remote users.

- **Transit Gateway**  
  Centralized gateway for all VPC and on-prem connectivity.

- **VPC Peering**  
  Direct private connection between two VPCs for fast internal communication.

- **PrivateLink**  
  Secure access to AWS services without exposing traffic to the public internet.

- **Global Accelerator**  
  Improves global application performance using AWS’s worldwide network.

---

## AWS VPC & Subnets

- **VPC**  
  A private network in AWS where you control IP ranges, routing, and security.

- **Subnets**  
  Logical divisions of a VPC.
  - **Public Subnet** → Internet-facing resources (e.g., web servers)
  - **Private Subnet** → Internal resources (e.g., databases)

- **Routing & Security**  
  Route tables, gateways, and security groups control traffic flow.  
  Example: A public web server can access a private database internally, but the database remains inaccessible from the internet.

---

## AWS Security Groups vs NACL

### Security Groups
- Instance-level firewall
- Stateful (return traffic allowed automatically)
- Only allow rules

### Network ACL (NACL)
- Subnet-level firewall
- Stateless (explicit allow/deny rules)
- Evaluates traffic by IP, protocol, and port

**Summary:**  
- NACL protects subnets  
- Security Groups protect individual instances

---

## AWS VPC Reserved Addresses

AWS reserves **5 IP addresses** in every subnet:

1. Network address  
2. Router (gateway)  
3. DNS server  
4. Reserved for future use  
5. Broadcast address  

These IPs cannot be assigned to resources.

---

## Azure Virtual Network (vNet) & Subnets

- **Virtual Network (vNet)**  
  Azure’s private network that allows resources to communicate using private IP addresses.

- **Subnets**  
  Divide vNet into logical segments.
  Example:
  - Web subnet
  - Application subnet
  - Database subnet

Azure reserves certain IP addresses in each subnet for internal operations.

---

## Azure Networking Services

### Core Services

- **Virtual Network (vNet)**  
  Foundation for private communication between Azure resources.

- **Azure DNS**  
  Resolves domain names to IP addresses.

- **Azure Load Balancer**  
  Distributes incoming traffic to backend servers for high availability.

- **Azure Application Gateway**  
  Advanced web traffic manager with Web Application Firewall (WAF).

- **Network Security Groups (NSG)**  
  Controls inbound and outbound traffic using rules.

---

## Azure Enterprise / Hybrid Networking Services

- **Front Door**  
  Global entry point that routes users to the nearest and healthiest backend.

- **ExpressRoute**  
  Private, high-speed connection between on-premises networks and Azure.

- **Virtual WAN**  
  Centralized management for VPNs, routing, and security across branches.

- **VPN Connection**  
  Encrypted tunnel between networks or on-premises infrastructure.

- **Virtual Network Gateway**  
  Enables VPN and ExpressRoute connectivity.

---

## Network Security Group (NSG)

An NSG controls traffic flow for Azure resources.

### Features:
- Evaluates source, destination, port, and protocol
- Applied to subnets or network interfaces
- Supports inbound and outbound rules
- Priority-based rule processing
- Default deny if no rule matches

---

## Google Cloud Networking

### VPC & Subnets

- **VPC**  
  A regional private cloud network.

- **Subnets**
  - **Public Subnet** → Uses external IPs (e.g., web servers)
  - **Private Subnet** → No public IPs (e.g., databases)

Private resources use **Cloud NAT** for outbound internet access without exposure.

---

## Google Cloud Networking Services

- **Firewall Rules**  
  Control traffic between subnets, internet, and on-prem networks.

- **Cloud VPN**  
  Internet-based encrypted tunnel to on-premises.

- **Cloud Interconnect**  
  High-speed private connectivity to on-premises networks.

- **Cloud Armor**  
  Protects against DDoS and malicious traffic.

- **Cloud Load Balancing**  
  Distributes traffic across servers globally.

- **Cloud CDN**  
  Caches content closer to users for faster delivery.

- **Cloud NAT**  
  Allows private instances outbound internet access without public IPs.

- **Cloud DNS**  
  Reliable and scalable DNS service.

- **Traffic Director**  
  Intelligent traffic routing based on health and policies.

- **Cloud Router**  
  Dynamically exchanges routes between Google Cloud and on-premises networks.

---

**End of Document**


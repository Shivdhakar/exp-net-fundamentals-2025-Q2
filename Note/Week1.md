# Secure Remote Access Setup for Jellyfin Streaming

This setup allows a **Smart TV in one home** to stream content from a **Jellyfin server located in another home**, across separate networks, while keeping everything **private, encrypted, and secure**.

The Jellyfin server is **never exposed directly to the public internet**.

---

## Overview

Two geographically separated homes are connected using a **site-to-site VPN**, making them behave like a single private network.

All communication travels through an **encrypted tunnel**, ensuring privacy, security, and seamless media streaming.

---

## The Two Homes

### Home A – Client Side
- Contains the **Smart TV**
- User launches the Jellyfin app and streams content

### Home B – Server Side
- Hosts the **Jellyfin Media Server**
- Server runs internally (e.g., Docker on port `8096`)
- No public internet exposure

---

## Common Components in Each Home

Each home contains:

- Its own **internal LAN**
- A **router**
- A small device called the **Connector Box**

### Connector Box Purpose
The connector box acts as a **secure bridge** between the two homes.

---

## VPN Connection

- A **VPN tunnel** connects the connector boxes
- Both homes appear as one unified private network
- All traffic is encrypted end-to-end
- Private IP addressing is preserved across locations

---

## Role of the Connector Boxes

The connector boxes act like trusted couriers:

- Route traffic between homes
- Encrypt and decrypt data using the VPN
- Handle private IP traffic across sites
- Prevent direct exposure to the public internet

All data avoids open internet paths and travels only through the encrypted VPN tunnel.

---

## How Data Flows (Step-by-Step)

### 1. TV Initiates Request
- User opens Jellyfin on the Smart TV in **Home A**
- Selects a movie or show
- TV creates a request using:
  - Its private IP
  - A temporary source port
  - The Jellyfin server’s private IP

The TV treats the server as if it were on the same local network.

---

### 2. Request Hits Local Router
- The packet is sent to Home A’s router
- Router checks the destination IP
- Recognizes that traffic must go to the remote network

---

### 3. Router Forwards to Connector Box
- Router forwards the packet to the connector box
- The connector box is the designated path for remote traffic
- Acts like a trusted private entrance

---

### 4. VPN Handles Secure Transfer
- Connector box encrypts the packet
- Sends it through the VPN tunnel

At this stage:
- Data is fully encrypted
- External observers see only unreadable traffic
- Original private IPs remain hidden

The packet travels securely over the internet to **Home B**.

---

### 5. Remote Connector Box Processes Packet
- Connector box in Home B receives the encrypted packet
- Decrypts the data
- Verifies the destination
- Forwards it to the local router as internal traffic

---

### 6. Server Receives and Responds
- Home B router delivers the packet to the Jellyfin server
- Jellyfin processes the request
- Media streaming begins (e.g., via port `8096`)

---

### 7. Return Path for the Response
The video stream follows the same protected route back:


This symmetric, encrypted path ensures:
- Stable streaming
- Low risk of interception
- Consistent performance

---

## Key Security Benefits

- No public exposure of Jellyfin server
- End-to-end encrypted communication
- Private IP addressing across sites
- Protection from scanning, DDoS, and unauthorized access
- Works like a single private LAN across distance

---

## Summary

This architecture provides a **secure, private, and reliable remote streaming solution** by combining:

- Site-to-site VPN
- Connector boxes as secure gateways
- Internal-only Jellyfin server access

To the Smart TV, the Jellyfin server feels local —  
but to the internet, it doesn’t exist at all.

---

**End of Document**


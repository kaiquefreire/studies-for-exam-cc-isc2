# Network Security

### Types of Networks
*LAN (Local Area Network)*- A small local network
*VLAN (Virtual Local Area Network)*- A virtual LAN
*WAN (Wide Area Network)* - Provides long-distance connections with multiple LANs

### Devices
| Device | Summary                                                                                       |
|----------------|----------------------------------------------------------------------------------------------------|
| Hub            | Simple network device that receives data from one device and transmits it to all other devices     |
| Switch         | Device that connects multiple network devices and forwards data only to the intended destination   |
| Router         | Device that connects different networks, forwarding data between them                              |
| Firewall       | Monitors and controls network traffic to protect against threats              |
| Server         | Provide services to other devices on the network            |
| Endpoint       | Final device in a network, such as a laptop or smartphone, that communicates with other devices   |

About ingress and egress monitoring traffic, we have some keywords. 
- Inbound  traffic / ingress monitoring: Firewalls, Gateways, Remote authentication Servers, IDS/IPS tools, SIEM solutions, Anti-malware solutions.
- Outbound traffic / egress  monitoring: Data Loss Prevention (DLP) solutions or Data Leak Protection

## OSI model & TCP/IP model
Here we have a 
| OSI Model | TCP/IP Model | Packets |
|------------|---------------|---------|
| 7 - Application | 4 - Application | HTTP, FTP, SMTP, DNS |
| 6 - Presentation |  | JPEG, MPEG |
| 5 - Session |  | NFS, SQL, PAP |
| 4 - Transport | 3 - Transport | TCP, UDP |
| 3 - Network | 2 - Internet | IPv4, IPv6 |
| 2 - Data Link | 1 - Network Access | IP, ICMP, ARP |
| 1 - Physical |  | Ethernet, Wi-Fi |

## Describing each layers:
| Layer | Provides|
|------------|---------------|
|Application |  Provides the services to users |
|Presentation |         |
|Session |         |
|Transport |         |
|Network |         |
|Data Link (Enlace) |         |
|Physical |         |

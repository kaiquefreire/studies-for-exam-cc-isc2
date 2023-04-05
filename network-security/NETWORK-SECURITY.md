# Network Security

### Types of Networks
- *LAN (Local Area Network)*- A small local network
- *VLAN (Virtual Local Area Network)*- A virtual LAN
- *WAN (Wide Area Network)* - Provides long-distance connections with multiple LANs

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

| Layer | Provides |
|-------|----------|
| Application | Provides network services to end-users, such as email, web browsing, and file transfer |
| Presentation | Translates data received from the application layer into a common format that can be understood by the network, and performs functions such as data encryption and compression |
| Session | Responsible for establishing, managing, and terminating communication connections between two devices on the network |
| Transport | Ensures reliable delivery of data between the end devices, segmenting information into smaller packets and providing flow control and error correction |
| Network | Responsible for routing packets in the network, selecting the most efficient path between end devices and ensuring packets arrive at the correct destination |
| Data Link | Responsible for ensuring the transfer of data between two directly connected devices over a physical medium, such as a network cable or wireless network |
| Physical | Responsible for the transmission of raw bits from one device to another over a physical medium, such as fiber optic or copper cable |

## Insecure Ports || Secure Ports
| Insecure port | Protocol name | Description | Secure alternative port | Protocol name |
| --- | --- | --- | --- | --- |
| 21 FTP | File Transfer Protocol (FTP) | Does not encrypt data during transfer, making it vulnerable to sniffing and interception attacks. | 22 SFTP (SSH File Transfer Protocol) | Secure File Transfer Protocol |
| 23 TELNET | Telnet | Does not encrypt data, including passwords, allowing interception of information. | 22 SSH (Secure Shell) | Secure Shell Protocol |
| 25 SMTP | Simple Mail Transfer Protocol (SMTP) | Does not encrypt emails in transit, allowing them to be read by third parties. | 587 SMTPS (SMTP Secure) | SMTP with TLS |
| 37 TIME | Time Protocol | Unexpected errors | 123 - NTP | Network Time Protocol |
| 53 DNS | Domain Name System (DNS) | Does not encrypt DNS queries and responses, allowing interception and manipulation of information. | 853 DNS over TLS (DoT) | Domain Name System |
| 80 HTTP | Hypertext Transfer Protocol (HTTP) |  Information sent via HTTP is not encrypted and is susceptible to sniffing attacks | 443 HTTPS (HTTP Secure) | Secure Hypertext Transfer Protocol |
| 143 IMAP | Internet Message Access Protocol (IMAP) | Does not encrypt emails in transit, allowing them to be read by third parties. | 993 IMAPS (IMAP Secure) | IMAP for SSL/TLS |
| 161/162 - SNMP | Simple Network Management Protocol (SNMP) | Does not encrypt transmitted information, including SNMP community passwords, allowing them to be read by third parties. | 161/162 SNMP over TLS | SNMPv3 |
| 445 SMB | Server Message Block (SMB) | Does not encrypt SMB traffic, allowing interception of information. | 2049 NFS | Network File System |
| 389 LDAP | Lightweight Directory Access Protocol (LDAP) | Does not encrypt transmitted information, including credentials, allowing them to be read by third parties. | 636 LDAPS (LDAP Secure) | Secure Lightweight Directory Access Protocol |

## How it works: SYN, SYN-ACK, ACK Handshake
- 1-TCP Client sends a synchronization (SYN) packet to the web server’s port 80 or 443. This is a request to establish a connection.
- 2-The web server replies to the SYN packet with an acknowledgement known as a SYN/ACK.
- 3-Finally, the client acknowledges the connection with an acknowledgement (ACK).

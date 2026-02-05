# OSI & TCP/IP Layer Mapping Cheat Sheet

## Core Memory Hooks

-   **TCP = Reliable = Transport**
-   **IP = Routing = Network**
-   **MAC = Data Link**
-   **Encryption = Presentation**
-   **Ping = ICMP**

------------------------------------------------------------------------

## What Each Layer Handles

    Bits        → Physical
    Frames/MAC  → Data Link
    IP/Routing  → Network
    Segments    → Transport
    Session     → Session
    Format/Enc  → Presentation
    User Apps   → Application

------------------------------------------------------------------------

## OSI to TCP/IP Mapping

    OSI 7 + 6 + 5  → TCP/IP Application
    OSI 4          → TCP/IP Transport
    OSI 3          → TCP/IP Internet
    OSI 2 + 1      → TCP/IP Network Access

------------------------------------------------------------------------

## OSI vs TCP/IP Model

| OSI Layer (7) | OSI Layer Name   | TCP/IP Layer (4) | Key Concepts / Protocols |
|--------------|------------------|------------------|--------------------------|
| 7 | Application | Application | HTTP, HTTPS, FTP, SMTP, DNS |
| 6 | Presentation | Application | SSL/TLS, Encryption, Compression |
| 5 | Session | Application | Session Management |
| 4 | Transport | Transport | TCP, UDP |
| 3 | Network | Internet | IP, ICMP, IPSec |
| 2 | Data Link | Network Access | Ethernet, ARP, VLAN, MAC |
| 1 | Physical | Network Access | Cables, NIC, Signals |



## TCP/IP Layers and Protocols

### Application Layer

-   HTTP / HTTPS
-   FTP
-   SMTP / POP3 / IMAP
-   DNS
-   SSH

### Transport Layer

-   TCP → Reliable
-   UDP → Fast

### Internet Layer

-   IP
-   ICMP (Ping)
-   IPSec

### Network Access Layer

-   Ethernet
-   ARP
-   MAC Address
-   Physical Media

------------------------------------------------------------------------

## Data Flow Example

    User types URL           → Application
    Data encrypted           → Presentation
    Session created          → Session
    Data segmented           → Transport (TCP)
    IP added (routing)       → Network
    Frame + MAC added        → Data Link
    Bits on wire             → Physical

------------------------------------------------------------------------

## Protocol to Layer Quick Map

    HTTP, FTP, SMTP → Application
    SSL/TLS         → Presentation
    NetBIOS         → Session
    TCP/UDP         → Transport
    IP, ICMP        → Network
    ARP, VLAN, MAC  → Data Link
    Cable, Signal   → Physical

------------------------------------------------------------------------

## Memory Rap

> **HTTP talks, SSL locks,\
> TCP moves, IP routes,\
> ARP finds MAC,\
> Cable sends bits.**

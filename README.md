## OSI Model

## How your HTTP request moves through the **OSI 7-layer model**, down from the browser to the physical network,and then back up on the server.


### Layer 7 – Application Layer
- At layer 7, your browser creates an HTTP request.Get index.html
- This is the actual data you want to send.pure application stuff
- It's like writing a letter saying,"Please send me the homepage"

### Layer 6 – Presentation Layer
- Now layer6 step in .This is where things secure.
- It wrap your HTTP request in SSL/TLS Encryption,like putting your letter in a locked box.

### Layer 5 – Session Layer
- Layer 5 is all about keeping track of your conversation[session mgmt]
- Is adds session ID so ther server knows it's still talking to you,handles authentication,manages timeouts.

### Layer 4 – Transport Layer
- Layer 4 wraps everything in TCP reliable delivery ,it adds source port 54321,dest port 443 for HTTPS and sequence numbers.

### Layer 3 – Network Layer
- Layer 3 adds IP routing info.Your IP 192.168.1.100 to the server's IP 93.184.216.43.

### Layer 2  – Data link Layer
- Layer 2 add MAC addressing for local network delivery.

### Layer 1  – Physical Layer
- Finally Layer 1 converts everything electrical signals that travel through ethernet cable or wifi radio wave 
- It travels across the internet through `routers that read Layer3` ,`switches that read Layer2` and finally reaches the web server.





## Client Side (Request Flow)

```
+--------------------------------------------------+
| Layer 7 – Application                            |
| HTTP GET /index.html                             |
+--------------------------------------------------+
                    |
                    v
+--------------------------------------------------+
| Layer 6 – Presentation                           |
| SSL / TLS Encryption                             |
+--------------------------------------------------+
                    |
                    v
+--------------------------------------------------+
| Layer 5 – Session                                |
| Session ID, Authentication, Timeouts             |
+--------------------------------------------------+
                    |
                    v
+--------------------------------------------------+
| Layer 4 – Transport                              |
| TCP                                              |
| Source Port: 54321  Destination Port: 443        |
| Sequence Numbers                                 |
+--------------------------------------------------+
                    |
                    v
+--------------------------------------------------+
| Layer 3 – Network                                |
| IP Routing                                       |
| Source IP: 192.168.1.100                         |
| Destination IP: 93.184.216.43                    |
+--------------------------------------------------+
                    |
                    v
+--------------------------------------------------+
| Layer 2 – Data Link                              |
| MAC Addressing (Local Network Delivery)          |
+--------------------------------------------------+
                    |
                    v
+--------------------------------------------------+
| Layer 1 – Physical                               |
| Electrical Signals / Wi-Fi Radio Waves           |
+--------------------------------------------------+
```

---

## Across the Internet

```
Routers  → Read Layer 3 (IP)
Switches → Read Layer 2 (MAC)
```

Data travels hop-by-hop until it reaches the web server.

---


The web server receives your packet and processes it in reverse order.

### Layer 1  – Physical Layer
- Coverts electrical singals back to data 

### Layer 2  – Data link Layer
- Remove MAC address 

### Layer 3 – Network Layer
- Remove IP headers

### Layer 4 – Transport Layer
- Removes TCP headers

### Layer 5 – Session Layer
- Manages the session

### Layer 6 – Presentation Layer
- Decrypts the SSL 

### Layer 7 – Physical Layer
Processes your HTTP request and sends back the web page


## Server Side (Reverse Processing)

```
+--------------------------------------------------+
| Layer 1 – Physical                               |
| Signals Converted Back to Data                   |
+--------------------------------------------------+
| Layer 2 – Data Link                              |
| MAC Header Removed                               |
+--------------------------------------------------+
| Layer 3 – Network                                |
| IP Header Removed                                |
+--------------------------------------------------+
| Layer 4 – Transport                              |
| TCP Header Removed                               |
+--------------------------------------------------+
| Layer 5 – Session                                |
| Session Managed                                  |
+--------------------------------------------------+
| Layer 6 – Presentation                           |
| SSL / TLS Decryption                             |
+--------------------------------------------------+
| Layer 7 – Application                            |
| HTTP Request Processed                           |
| Web Page Sent Back                               |
+--------------------------------------------------+
```

---

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

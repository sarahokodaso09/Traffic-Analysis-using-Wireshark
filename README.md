
# PACKET ANALYSIS USING WIRESHARK

---

##  LAB OBJECTIVES
The primary objectives of this lab are:
- [x] Capture live traffic on a network using **Wireshark**.
- [x] Apply display filters on captured network traffic.
- [x] Identify basic network protocols including **DNS**, **HTTP**, **HTTPS (TLS)**, **ICMP**, and **ARP**.
- [x] Evaluate a **PCAP** file successfully.
- [x] Examine patterns to detect network security threats such as **ARP spoofing**.

---

##  LAB OVERVIEW
Network packet analysis is an important skill in cybersecurity because it helps in monitoring, troubleshooting, and securing networks. In this lab, Wireshark, a network protocol analyzer, to capture and analyze live data traffic was used. The main goal was to learn how to use display filters, identify common protocols like DNS, HTTP, and ICMP, and examine packets in detail. This helps understand how devices communicate on a network and how to spot possible security issues, such as ARP spoofing.

---

## METHODS & PROCEDURES

### Step 1 & 2: Interface Selection
- Open **Wireshark**
- Observe active traffic indicators across available network interfaces.
- Select the active interface (e.g., **Wi-Fi** or **Ethernet**) to begin capture.

### Step 3 & 4: Live Packet Capture & Traffic Generation
- Observe packets loading dynamically onto the screen upon capture initialization.
- Open **Google Chrome** and visit **4 different websites** to generate diverse traffic.

### Step 5 & 6: Stopping & Initial Observation
- Stop the live capture by clicking the red square button in the top toolbar.
- Examine the default packet list display columns:
  - `No.`, `Time`, `Source`, `Destination`, `Protocol`, `Length`, and `Info`.

---

##  PROTOCOL FILTERING & ANALYSIS

### A. DNS (Domain Name System)
- **Filter Query:** `dns`
- **Observations:** DNS which means domain name system is responsible for translatinbg the website visited names to IP address to be able to identify the packet.

### B. HTTP (Hypertext Transfer Protocol)
- **Filter Query:** `http`
- **Observations:** Evaluates unencrypted web traffic. HTTP isn’t widely used anymore in websites due to the fact that it isn’t encrypted and the lack of results for the filter shows that the traffic uses safe encrypted protocols.

### C. HTTPS / TLS (Transport Layer Security)
- **Filter Query:** `tls` 
- **Observations:** Shows encrypted conversations between the users and websites, More tls is seen because https is used in most modern website.

### D. ICMP (Internet Control Message Protocol)
- **Filter Query:** `icmp`
- **Observations:** Used for network diagnostic functions like echo request and replies which confirms network connectivity

### E. ARP (Address Resolution Protocol)
- **Filter Query:** `arp`
- **Observations:** ARP shows local network communication using a request and reply cycle which is shown in the screenshot below under the info column with the request who has and tell and the reply ip address is at mac address.

---

## PACKET INSPECTION & CONVERSATION FOLLOWING

### Packet Details Window Inspection
Understanding what to look for in a packet is important to being able to identify harmful or suspicious packets 
Looking at the ethernet, internet protocol and Transmission control protocol section we have to expand these sections to find core information which are the source IP Address, destination IP Address and Protocol which gives necessary information for tracing network conversations


### Following A conversation
1. Right-click a Packet,
2. Select follow then click TCP Stream, this will show a full conversation between the computer and server.

---

## 6. VISUAL EVIDENCE / SCREENSHOTS

| Figure | Description | Image Placeholder |
| :--- | :--- | :--- |
| **Fig 1** | Wireshark Interface & Target Selection | `![Interface Selection](path/to/screenshot1.png)` |
| **Fig 2** | Live Packet Capture & DNS Query Analysis | `![DNS Analysis](path/to/screenshot2.png)` |
| **Fig 3** | ICMP Filter Results & Packet Header Details | `![ICMP Filter](path/to/screenshot3.png)` |

---

## 7. RESULTS & DISCUSSION
The live traffic capture on the WiFi interface recorded packets while browsing different websites. Using filters, I observed DNS resolving domain names to IP addresses, and noticed mostly TLS packets instead of HTTP, showing that web traffic is encrypted through HTTPS. Network connectivity was confirmed using ICMP requests and replies, while ARP helped identify IP and MAC address pairings on the local network.
By inspecting Ethernet, IP, and TCP sections, I was able to see important source and destination details and follow the TCP stream to better understand the overall network communication.


---
## 8. CONCLUSION
This lab showed how useful Wireshark is for network troubleshooting and security analysis. By capturing live traffic and using filters, I was able to see the difference between encrypted and unencrypted protocols. Learning how to inspect packets and analyze PCAP files also helped me understand how to spot unusual or suspicious activity. Overall, these skills are important for keeping a network secure and protecting it from common threats like ARP spoofing.

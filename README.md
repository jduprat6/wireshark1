## Packet Analysis Project using Wireshark

### Overview
In this project, I conducted detailed network packet analysis using Wireshark installed on a Windows VM. The project involved applying filters, inspecting packets, and understanding different network protocols. I started by capturing network traffic and saving a pcap file. I open the pcap file to conduct my analysis.

### Key Skills and Steps

1. **Protocol Identification**:
   - Identified Internet Control Message Protocol `ICMP` as the protocol for 'Echo (ping) request' packets.
   - ICMP is used for sending error messages and operational information in IP networks, such as destination unreachable messages, time exceeded messages, and echo requests/replies (used by utilities like ping)

2. **Applying Basic Wireshark Filters**:
   - Filtered traffic by IP address (`ip.addr == 142.250.1.139`) to analyze specific packets. This search contains only packets where either the source or the 
     destination IP address matches the IP entered.
   - Inspected packet details including OSI layers (Ethernet, IP, TCP) and protocols.
<p align="center">
  <img src="https://i.imgur.com/x1UBLwn.png" alt="Image">
</p>


3. **Packet Detail Analysis**:
   - Explored various packet components: Frame, Ethernet II, Internet Protocol Version 4, and Transmission Control Protocol.
   - Analyzed TCP properties like destination port (Port 80 for HTTP traffic), sequence numbers, and flags.

4. **Using Filters for Specific Traffic Analysis**:
   - Applied filters to analyze traffic based on source and destination IP addresses (`ip.src` and `ip.dst`), and Ethernet MAC address (`eth.addr`).
   - ip.src == 142.250.1.139 contains only packets that came from 142.250.1.139, ip.dst == 142.250.1.139 contains only packets that were sent to 142.250.1.139, 
    filtering based on Ethernet addresses. Ethernet addresses, more commonly known as MAC (Media Access Control) addresses, eth.addr == 42:01:ac:15:e0:02 displays 
     packets that have 42:01:ac:15:e0:02 as either their source or destination MAC address
   - Examined protocol details within packets, especially focusing on TCP.
<p align="center">
  <img src="https://i.imgur.com/rZczHHK.png" alt="Image">
</p>

5. **DNS Traffic Examination**:
   - Used filters to select DNS traffic (`udp.port == 53`). DNS traffic uses UDP port 53, so this lists traffic related to DNS queries and responses only.
   - Analyzed DNS query and response data, including queried website names and resolved IP addresses.

6. **Exploring TCP Packets**:
   - Investigated TCP packets (`tcp.port == 80`) related to web traffic (http).
   - NOTE: HTTPS (HTTP Secure) traffic, which is HTTP encrypted using TLS/SSL for security, typically uses TCP port 443
   - Analyzed packet properties such as Time to Live, Frame Length, Header Length, and Destination Address.

7. **Advanced Filtering for Payload Data**:
   - Applied filters to select TCP packets containing specific text (`tcp contains "curl"`).
<p align="center">
  <img src="https://i.imgur.com/3Cyvghg.png" alt="Image">
</p>

### Conclusion
This project enhanced my practical skills in network analysis, deepening my understanding of network protocols, packet structure, and the use of Wireshark for cybersecurity purposes. It demonstrated my ability to filter and analyze network traffic, an essential skill in network security and troubleshooting.

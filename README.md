## Packet Analysis Project using Wireshark

### Overview
In this project, I conducted detailed network packet analysis using Wireshark, a powerful network protocol analyzer. The project involved applying filters, inspecting packets, and understanding different network protocols. I started by capturing network traffic and saving a pcap file. I open the pcap file to conduct my analysis.

### Key Skills and Steps

1. **Protocol Identification**:
   - Identified `ICMP` as the protocol for 'Echo (ping) request' packets.

2. **Applying Basic Wireshark Filters**:
   - Filtered traffic by IP address (`ip.addr == 142.250.1.139`) to analyze specific packets.
   - Inspected packet details including network layers (Ethernet, IP, TCP) and protocols.

3. **Packet Detail Analysis**:
   - Explored various packet components: Frame, Ethernet II, Internet Protocol Version 4, and Transmission Control Protocol.
   - Analyzed TCP properties like destination port (Port 80 for HTTP traffic), sequence numbers, and flags.

4. **Using Filters for Specific Traffic Analysis**:
   - Applied filters to analyze traffic based on source and destination IP addresses (`ip.src` and `ip.dst`), and Ethernet MAC address (`eth.addr`).
   - Examined protocol details within packets, especially focusing on TCP.

5. **DNS Traffic Examination**:
   - Used filters to select DNS traffic (`udp.port == 53`).
   - Analyzed DNS query and response data, including queried website names and resolved IP addresses.

6. **Exploring TCP Packets**:
   - Investigated TCP packets (`tcp.port == 80`) related to web traffic.
   - Analyzed packet properties such as Time to Live, Frame Length, Header Length, and Destination Address.

7. **Advanced Filtering for Payload Data**:
   - Applied filters to select TCP packets containing specific text (`tcp contains "curl"`).

### Conclusion
This project enhanced my practical skills in network analysis, deepening my understanding of network protocols, packet structure, and the use of Wireshark for cybersecurity purposes. It demonstrated my ability to filter and analyze network traffic, an essential skill in network security and troubleshooting.

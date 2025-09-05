
| Layer | Number | Example Protocols	| Example Tools |	Data Unit (PDU)
|---|---|---|---| --|
| Application |	7	| HTTP, SSH, DNS, SMTP |	curl, ssh, dig	Data / Message
| Presentation |	6	|SSL/TLS, ASCII, JPEG	|openssl	Data
| Session |	5	|NetBIOS, RPC, TLS session|		|Data
| Transport |	4 |	TCP, UDP|	nc, ss, netstat	|Segment (TCP) / Datagram (UDP)
| Network	| 3	|IP, ICMP	|ip, ping, traceroute	|Packet
| Data Link	|2	|Ethernet, ARP, MAC	|ip link, arp	|Frame
| Physical |1	|Cables, Wi-Fi, fiber	| ethtool, ip link	|Bit








| Tool/Protocol | OSI Layer(s)| TCP/IP Layer | Description |
|---|---|---| ---|
| ping | Row 1, Col 2 | Row 1, Col 3 |Row 1, Col 4
| ssh | Row 2, Col 2 | Row 2, Col 3 |Row 2, Col 4
| dig | Row 2, Col 2 | Row 2, Col 3 |Row 2, Col 4
| curl | Row 2, Col 2 | Row 2, Col 3 |Row 2, Col 4
| nc | Row 2, Col 2 | Row 2, Col 3 |Row 2, Col 4
| ip addr | Row 2, Col 2 | Row 2, Col 3 |Row 2, Col 4
| arp | Row 2, Col 2 | Row 2, Col 3 |Row 2, Col 4
| openssl | Row 2, Col 2 | Row 2, Col 3 |Row 2, Col 4
| traceroute | Row 2, Col 2 | Row 2, Col 3 |Row 2, Col 4
| traceroute | Row 2, Col 2 | Row 2, Col 3 |Row 2, Col 4


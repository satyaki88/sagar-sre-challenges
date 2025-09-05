
| Layer | Number | Example Protocols	| Example Tools |	Data Unit (PDU)
|---|---|---|---| --|
| Application |	7	| HTTP, SSH, DNS, SMTP |	curl, ssh, dig	|Data / Message
| Presentation |	6	|SSL/TLS, ASCII, JPEG	|openssl	|Data
| Session |	5	|NetBIOS, RPC, TLS session|		|Data
| Transport |	4 |	TCP, UDP|	nc, ss, netstat	|Segment (TCP) / Datagram (UDP)
| Network	| 3	|IP, ICMP	|ip, ping, traceroute	|Packet
| Data Link	|2	|Ethernet, ARP, MAC	|ip link, arp	|Frame
| Physical |1	|Cables, Wi-Fi, fiber	| ethtool, ip link	|Bit


TCP/IP Model (4 Layers)
|Layer	|OSI Layer(s)	|Example Protocols/Tools
|---|---|---|
|Application|	7, 6, 5|	HTTP, SSH, DNS, TLS, curl
|Transport|	4	|TCP, UDP, nc, ss
|Internet|	3	|IP, ICMP, ping, traceroute
|Network Access|	2, 1|	Ethernet, ARP, ip link, ethtool





| Tool/Protocol | OSI Layer(s)| TCP/IP Layer | Description |
|---|---|---| ---|
| ping | 3,1 | Internet |Tests IP reachability using ICMP
| ssh | 7,4 | Application , Transport |secure shell
| dig | 7,6,5,4,3 | Application,Transport, Internet |Basic DNS lookup
| curl | 7,6,5,4 ,3 |Application,Transport ,Internet  |Basic Get request .It use Apllication , Presnetation ( for SSL ),Session (to manage connection) and TCP 
| nc | 4,3,2,1 | Transport ,Internet,Network Access | Network utitlty tool used to read/write for data accross networks
| ip addr | 3,2,1 |Internet,Netwrok Access |it shows IP
| arp | 3,2 | Internet ,Network Access |Address Resolution Protocol
| openssl | 6,5,4  | Application layer,Transport |Provides SSL/TLS implementation
| traceroute | 3,2,1 | Internet,Network Access |Tool that traces the track from start to destination.
| tcpdump | 7,6,5,4,3,2,1 | Application , Transport,Internet, Network Access


A developer says:

“I can’t reach the app at http://10.10.10.20:5000 from my laptop. Ping fails, but DNS resolves.”

Your task:

Identify which layer(s) might be failing based on symptoms
DNS resolves that doesnt mean application is working. DNS runs on port 53 , application running on 5000
       Layer 3: Network issues (IP/routing)
       Layer 4: Port/Firewall blocking
       Layer 7: Apllication might not running

List which commands/tools you would use in order to troubleshoot—from bottom to top
   | Troubleshoot layer | tools |
   |---|---|
   | physical layer troubleshoot | ipconfig (check cable connection , wifi signal)
   | Network layer |  ping 10.10.10.20
   | Transport layer | check port 5000 is open using netstat -tulnp |grep 5000
   | application layer | curl http://10.10.10.20:5000

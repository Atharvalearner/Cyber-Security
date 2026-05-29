* process of **capturing and analyzing network traffic packets**. 
* It can leads to credential theft, session hijacking, and data interception, especially when insecure protocols like HTTP or Telnet are used.



**# Two main types**: Passive Sniffing and Active Sniffing.

1. **Passive Sniffing:** 

&#x09;- silently monitoring traffic without modifying communication 

&#x09;- Mainly possible in hub-based networks where traffic is broadcast to all devices.

2\. **Active Sniffing:** 

&#x09;- Attacker actively interferes with network communication to capture traffic.

&#x09;**-** used in switched networks (Switches do NOT broadcast packets to everyone. Traffic goes only to intended MAC address)

&#x09;- Attackers actively manipulate network protocols using techniques such as ARP spoofing or MAC flooding to redirect traffic through their system.



* ***Insecure Protocols:*** HTTP, FTP, Telnet, POP3, SMTP
* ***Prevention methods:*** encryption, switched networks, Dynamic ARP Inspection, VPNs, port security, and IDS/IPS monitoring.
* ***Common Sniffing Tools:***

&#x09;1. Wireshark: Packet analysis

&#x09;2. tcpdump: CLI packet capture

&#x09;3. Ettercap: MITM/sniffing

&#x09;4. Bettercap: Advanced sniffing


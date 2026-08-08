ARP Spoofing / ARP Poisoning: is a Layer 2 Man-in-the-Middle (MITM) attack. It exploits the ARP protocol, which maps IP addresses to MAC addresses within a local network. Since ARP does not have any authentication mechanism, devices automatically trust ARP replies.



In an ARP spoofing attack, the attacker sends forged ARP replies to the victim, claiming that the attacker's MAC address belongs to the default gateway. As a result, the victim updates its ARP cache with the fake mapping and starts sending its traffic to the attacker instead of the real router.



For example, if the victim's IP is 192.168.1.10, the router's IP is 192.168.1.1, and the attacker is on the same LAN, the attacker falsely tells the victim that "192.168.1.1 is at my MAC address." The victim trusts this information, and all its traffic is redirected through the attacker's system. The attacker then forwards the traffic to the real router, so the communication continues normally while the attacker can monitor or manipulate the traffic.



This can lead to packet sniffing, session hijacking, credential theft, DNS spoofing, or traffic modification. To prevent ARP spoofing, organizations use Dynamic ARP Inspection (DAI), static ARP entries for critical systems, VLAN segmentation, IDS/IPS monitoring, and encrypted protocols like HTTPS or VPNs so that intercepted traffic remains protected.





**# ARP Spoofing / Poisoning:**

* A **Layer-2 Man-in-the-Middle attack**
* Attacker sends duplicate/forged ARP replies to associate their MAC address with another device’s IP address, usually the default gateway.



* **ARP** : *map IP addresses to MAC addresses inside a LAN, but it lacks authentication, so devices trust ARP replies automatically.*
* In ARP spoofing, attacker poisons the ARP cache of the victim and router,  Victim trusts fake information. causing traffic to flow through the attacker’s system.



* Allows attackers to **perform packet sniffing, session hijacking, credential theft, DNS spoofing, or traffic manipulation**.



***# Real Network Scenario***

Suppose LAN contains:



Device	 | IP		| MAC

\-------------------------------

Victim	 | 192.168.1.10	| AA-AA

Router	 | 192.168.1.1	| BB-BB

Attacker | 192.168.1.50 | CC-CC



Normally communication : Victim → Router



Attacker wants: Victim ⇄ Attacker ⇄ Router

So all traffic passes through attacker.



***# Working Steps***:

1. **Victim Needs Router MAC**: Victim asks: Who has 192.168.1.1?

2\. **Attacker Sends Fake ARP Reply**: Attacker responds with his MAC: 192.168.1.1 is at CC-CC

&#x09;Meaning: "I am the router"

3\. **Victim Updates ARP Cache/table:** Victim stores the entry for Router IP as Attacker's MAC: 192.168.1.1 → CC-CC

&#x09;instead of real router MAC.

4\. **Traffic Redirected:** Victim sends traffic to attacker.

5\. **Attacker Forwards Traffic:** Attacker forwards packets to real router.

&#x09;Victim usually notices nothing.

6\. **MITM Achieved**: Now attacker can: sniff traffic, modify packets, steal cookies, inject malware



* ***Prevention methods :***

&#x09;- Dynamic ARP Inspection

&#x09;- static ARP entries

&#x09;- VLAN segmentation

&#x09;- IDS/IPS monitoring,

&#x09;- VPNs

&#x09;- encrypted communication such as HTTPS.


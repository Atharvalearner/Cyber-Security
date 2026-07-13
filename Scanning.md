**# Scanning:**

process of actively probing/exploring a target system or network to identify live hosts, open ports, running services, operating systems, and potential vulnerabilities.



**# Simple Analogies:**

*Foot printing* → What information can I gather about the target?

*Scanning*     → Which systems, ports, and services are reachable?

*Enumeration*  → What detailed information can I extract from those services?



**# Three Major Types of Scanning:**

1. **Network**	: find systems which are live
2. **Port**	  	: find open/closed/filtered ports
3. **Vulnerability**: find weakness of those system



**# Port States:**

1. **Open Port:** A service is listening and accepting connections.

**2. Closed Port:** The host is reachable, but no service is listening on that port.

**3. Filtered Port:** Firewall or filtering device prevents the scanner from determining the port state.



**# Scanning Types:**



1. ***TCP Connect Scan/Full Scan:***
* performs the complete TCP three-way handshake with the target to determine whether a port is open.
* If the scanner receives SYN-ACK and completes the connection with ACK, the port is open. 

***Scanner                  Target***

&#x20;  ***SYN  ------------------->***

&#x20;       ***<-----------------  SYN-ACK***

&#x20;  ***ACK  ------------------->***

&#x09;    ***Port is OPEN***



* If it receives RST, the port is closed. Since the complete connection is established, this scan is reliable but relatively easy to detect and log.

***Scanner                  Target***

&#x20; ***SYN  ------------------->***

&#x20;      ***<-----------------  RST***

&#x20;         ***Port is CLOSED***





***2. SYN Scan/Half-Open Scan/SYN Stealth Scan:***

* A SYN scan sends a SYN packet to a target port and analyzes the response without completing the full TCP three-way handshake.
* A SYN packet is sends to the target. 

***Scanner  -------- SYN -------->  Target***



* If the target responds with SYN-ACK, the port is considered open, but the scanner does not complete the handshake. 

***Scanner  <----- SYN-ACK -------  Target***



* If the target responds with RST, the port is closed. 

***Scanner  <------- RST ---------  Target***



* It is faster and less connection-heavy than a full TCP Connect scan.
* Modern firewalls, IDS/IPS, and network monitoring tools can still detect SYN scanning patterns.





***3. FIN scan:***

* Normally, the FIN flag is used to: *Terminate an existing TCP connection*
* A FIN scan sends a TCP packet with only the FIN flag set.

***Scanner  -------- FIN -------->  Target***



* Under classic TCP behavior, a closed port responds with RST

***Scanner  <----- RST -------  Target***



* while an open port may give no response.

***Scanner  <-----------------  Target***

&#x09;     ***No Response***



* It can be used for port-state inference, but it is less reliable across different operating systems and modern security controls.





***4. Null Scan (almost same as FIN scan, just instead of FIN flag it will send Null, other than that all is Same):***

* A NULL scan sends a TCP packet without setting any TCP flags.

***Scanner  -------- NULL -------->  Target***



* Under classic TCP behavior, a closed port typically responds with RST

***Scanner  <----- RST -------  Target***



* while an open port may not respond

***Scanner  <-----------------  Target***

&#x09;     ***No Response***



* It is mainly used for port-state inference but may be unreliable on some operating systems and modern networks.





***5. Xmas Scan:***

* Xmas scan sends a TCP packet with the FIN, PSH, and URG flags set. It is called an Xmas scan because multiple flags are enabled.

***Scanner  -------- FIN+PSH+URG -------->  Target***



* Under classic TCP behavior, a closed port responds with RST

***Scanner  <----- RST -------  Target***



* while an open port may not respond.

***Scanner  <-----------------  Target***

&#x09;     ***No Response***





***6. IDLE scan:*** 

* It is an indirect scanning technique
* uses a quiet third-party host, known as a zombie, to infer whether ports on a target are open or closed. 
* The scanner analyzes changes in the third-party host's network behavior rather than relying only on a direct scan.

***Scanner → Indirect measurement***

***Zombie  → Third-party system***

***Target  → System being assessed***





**# Common/Simple way to understand FIN vs NULL vs Xmas Scan:**

These three are very similar.



***Scan	TCP Flags***

\--------------------------

FIN  >> FIN

NULL >> No flags/NULL

Xmas >> FIN + PSH + URG



Their classic interpretation is similar:

***RST         → Closed***

***No Response → Open or Filtered***


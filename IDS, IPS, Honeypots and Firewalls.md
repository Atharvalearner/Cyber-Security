**# IDS, IPS, Honeypots and Firewalls:**

First understand the overall security architecture.

Internet

&#x20;   │

Firewall

&#x20;   │

IPS

&#x20;   │

Switch

&#x20;  ├──────────┐

Servers      Workstations

&#x20;  │

Honeypot



IDS monitors network traffic

SIEM collects alerts

SOC investigates



**## Firewall:**

* It is a network security device or software
* monitors and controls incoming and outgoing network traffic based on predefined security rules.

*Internet*

*↓*

*Firewall*

*↓*

*Allow?*

*↓*

*YES → Allow to enter Internal Network, NO → Block*



**# Need a Firewall:**

* Without a firewall: Internet >> Direct Access >> Internal Systems

Anyone can attempt to communicate with internal systems.

* With a firewall: Internet >> Firewall Rules >> Allowed Traffic Only



**# Types of Firewalls**

***1. Packet Filtering Firewall:***

* It Checks Incoming Packet: Source IP, Destination IP, Port, Protocol Very fast.
* Only Work till OSI layer 3/Network Layer.



***2. Stateful Firewall:***

* Keeps track of: Connection State
* Example: TCP Connection >> Already Established? >> Allow Response
* Instead of checking every packet independently.



***3. Next Generation Firewall (NGFW):***

* Can inspect: Applications, Users, Malware, Intrusion attempts, URLs
* Much smarter than traditional firewalls.
* Examples: Palo Alto, Fortinet, Check Point, Cisco Firepower





**## Intrusion Detection System (IDS):**

* Monitors network or host activity to detect suspicious or malicious behavior and generates alerts but does not automatically block the traffic.
* IDS Flow: Network Traffic >> IDS >> Attack Detected? >> YES >> Generate Alert



**# Types of IDS:**

***A. Network IDS (NIDS):***

Monitors: Entire Network

Examples: Snort, Suricata, Zeek (formerly Bro)



***B. Host IDS (HIDS)***

Runs on: Individual Computer

Monitors: Files, Processes, Logs, System Calls

Examples: OSSEC, Wazuh



**## Intrusion Prevention System (IPS):**

* It monitors network traffic for malicious activity and can automatically block or prevent detected attacks.
* IPS Flow: Traffic >> IPS >> Attack? >> YES >> Block Immediately


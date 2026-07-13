**Cyber Kill Chain (Attack Lifecycle)** :

&#x09;***1. Reconnaissance***: Gathering info : Attacker collects information about target people, systems, technologies, public infra.

&#x09;	Example: Hacker scans a company’s open ports.

&#x09;	Types: Active (Directly Scanning the target network/system), Passive (Get Info. from LinkedIn, company websites, etc)

&#x09;	Tools attackers commonly use: Nmap, Google dorking, LinkedIn, WHOIS, Shodan, Netcat.



&#x09;***2. Weaponization***: Create exploit/malware (for a known vuln) with a delivery method.

&#x09;	Example: Building phishing email with malicious attachment.

&#x09;	Tools attackers commonly use: Metasploit Framework (payload creation; dual-use), Custom exploit code.



&#x09;***3. Delivery***: Send exploit : attacker sends the weapon to the victim (email, drive-by, USB, supply-chain).

&#x09;	Example: Email sent to employee.

&#x09;	Tools attackers commonly use :

&#x09;		Phishing kits \& SMTP bots, compromised mail servers, social engineering templates.

&#x09;		Malicious URLs hosted on compromised sites or shorteners.

&#x09;		Physical media with autorun payloads (less common now).



&#x09;***4. Exploitation***: Malware executes : delivered payload takes advantage of a vulnerability to run code or steal credentials.

&#x09;	Example: Employee opens attachment → system infected.

&#x09;	Tools attackers commonly use : Metasploit, custom scripts, Hydra, Medusa.



&#x09;***5. Installation*** → Malware installs backdoor (so the attacker can come back): services, scheduled tasks, user accounts, backdoors, opens reverse shell to access victim remotely.

&#x09;	Example: Trojan silently runs in background.

&#x09;	Tools attackers commonly use : Dropper binaries, PowerShell scripts, Cobalt Strike stagers (commercial dual-use).



&#x09;***6. C2 (Command \& Control)*** : Attacker communicates with infected machine.

&#x09;	Example: Hacker issues commands remotely.



&#x09;***7. Actions on Objective*** : Data theft, ransom, destruction.

&#x09;	Example: Exfiltrate financial records.





Summary:

1. Scanning
2. Creating payload
3. deliver payload to victim
4. executing payload at victim
5. creating/installation backdoor
6. control victim using command 
7. achieve objective 


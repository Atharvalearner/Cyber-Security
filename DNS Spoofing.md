**# DNS spoofing:**

an attack in which false DNS information is provided to a victim, causing a legitimate domain name to resolve to an attacker-controlled or incorrect IP address.



**# In simple terms:**

User asks: "What is the IP of bank.com?"

Correct answer: bank.com → Real Server

Fake answer: bank.com → Attacker Server

The user types the correct domain name, but reaches the wrong server.



**# DNS spoofing attacks the mapping:** Correct Domain -> Wrong IP Address



**# Working:**

1. Victim Requests a Domain

2. False DNS Information Is Introduced

3. Victim Accepts the False Mapping

4. Browser Connects to Wrong Server

5. Attack Impact Occurs



*Victim*

&#x20;  *↓*

*Types legitimate/correct domain*

&#x20;  *↓*

*False DNS answer(Might be an attacker server IP)*

&#x20;  *↓*

*Wrong IP*

&#x20;  *↓*

*Fake or malicious server*



**# Prevention :**

* Use Trusted DNS Resolvers
* Keep DNS Software Updated
* Secure Network Configuration
* Use HTTPS and Validate Certificates
* Monitor DNS Traffic
* Secure DNS Server Administration


A SYN Flood is a TCP-based Denial-of-Service attack that exploits the TCP three-way handshake. The attacker sends a large number of SYN packets but does not complete the handshake by sending the final ACK. As a result, the server maintains many half-open connections, consuming memory and filling its backlog queue. Legitimate users are then unable to establish new TCP connections. Common defenses include SYN cookies, rate limiting, firewalls, load balancers, DDoS protection, and proper TCP backlog configuration.



Attacker

&#x20;    │

&#x20;    ├── SYN

&#x20;    ├── SYN

&#x20;    ├── SYN

&#x20;    ├── SYN

&#x20;    ├── SYN

&#x20;    └── SYN

&#x20;            │

&#x20;            ▼

&#x20;         Server

&#x20;            │

&#x20;     SYN-ACK

&#x20;     SYN-ACK

&#x20;     SYN-ACK

&#x20;     SYN-ACK

&#x20;            │

&#x20;            ▼

&#x20;    Waiting for ACK...

&#x20;    Waiting for ACK...

&#x20;    Waiting for ACK...

&#x20;    Waiting for ACK...

&#x20;            │

&#x20;            ▼

&#x20;    Connection Queue Full (All Resource Exhausted)

&#x20;            │

&#x20;            ▼

&#x20;Legitimate Users Rejected


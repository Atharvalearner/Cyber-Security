**# IP spoofing:**

* technique in which the source IP address in an IP packet is forged or modified so that the packet appears to originate from a different system.
* IP spoofing is commonly associated with DoS, DDoS, reflection, and amplification attacks.



**Example:** In IP spoofing, the sender changes the apparent source:

Actual Sender  : 10.0.0.50

Forged Source  : 10.0.0.10

Destination    : 10.0.0.20



The destination receives a packet that appears to come from: 10.0.0.10 instead of the real sender.



***# Why is IP Spoofing Possible?***

The basic IP protocol carries a source address, but the receiving system cannot always verify from the IP header alone that the sender truly owns that source address.



**# Prevention:**

ingress and egress filtering

anti-spoofing firewall rules

reverse-path validation

strong authentication

traffic monitoring

DDoS protection.



**| ------------------------------------- | ------------------------------------------ |**

**| IP Spoofing                           | ARP Spoofing                               |**

**| ------------------------------------- | ------------------------------------------ |**

| Manipulates apparent source IP        | Manipulates IP-to-MAC mapping              |

| Layer 3 concept                       | Layer 2 attack                             |

| Can affect routed traffic scenarios   | Primarily same local network               |

| Often associated with DDoS/reflection | Often associated with MITM                 |

| Replies may go to spoofed IP          | Traffic can be redirected through attacker |

| ------------------------------------- | ------------------------------------------ |




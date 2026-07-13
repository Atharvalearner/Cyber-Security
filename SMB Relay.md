**SMB relay:**

* a man-in-the-middle authentication attack 
* an attacker receives or intercepts a victim's SMB or NTLM authentication attempt and forwards it to another server.
* The attacker does not necessarily crack or know the victim's password. Instead, they relay the valid authentication exchange to a target that accepts it, potentially gaining the same level of access as the victim.



***# Example:*** 

* ***If the environment lacks proper protections:***

*Employee's Authentication*

&#x20;         *↓*

*Relayed by Attacker*

&#x20;         *↓*

*File Server Accepts It*

&#x20;         *↓*

*Attacker Gains Employee-Level Access*



* ***The attacker did not necessarily:***

*To Guess the password OR Crack the password OR Know the password*



* ***Instead:** Relay on valid authentication* 





**# SMB redirection:**

causing a victim to initiate authentication toward an unintended system, 

while SMB relay forwards that authentication to another target.



**# Prevention Techniques**:

requiring SMB signing, reducing unnecessary NTLM usage, disabling SMBv1, restricting SMB traffic through segmentation and firewall rules, applying least privilege, and monitoring unusual authentication activity.



**# Real World Scenario Example:**

Suppose an employee's computer initiates an SMB authentication attempt that reaches an attacker-controlled system. Instead of cracking the employee's password, the attacker relays that authentication exchange to another server. If the target accepts the authentication and proper protections such as SMB signing are not enforced, the attacker may obtain the employee's level of access on that server.


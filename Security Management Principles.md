***I) CIA Triad (Confidentiality, Integrity, Availability) :***

&#x09;**1. Confidentiality:** Only authorized users should access data.

&#x09;	- Applies to content and existence.

&#x09;	- supported by access control mechanism: cryptography \& stenography, file permissions, white and black list

&#x09;	- Enforcement relies on system services. eg. kernel

&#x09;	Example: ATM PIN → only you should know it.

&#x09;**2. Integrity:** Data should remain accurate and unmodified.

&#x09;	- Trustworthiness of data or resources.

&#x09;	- Data and origin integrity

&#x09;	- Prevention and Detection mechanism use for unauthorized access.

&#x09;	- Correctness and trustworthiness verifies in Origin, transmission, storage

&#x09;	Example: If you transfer ₹1000 via UPI, it must not become ₹10,000 or ₹100.

&#x09;**3. Availability:** Systems/data should be available when needed.

&#x09;	Example: Banking app must be up 24/7 → no DDoS downtime.



***II) AAA Model (Authentication, Authorization, Accounting) :***

&#x09;**1. Authentication:** Who are you?

&#x09;	- Only authorized person can access the resource or their data.

&#x09;	- Examples: Username/password, OTP, Biometrics

&#x09;**2. Authorization:** What are you allowed to do?

&#x09;	- simply what Permissions do you have like role based access of resources.

&#x09;	- Example: User access, Admin access

&#x09;**3. Accounting:** What actions did you perform?

&#x09;	- Stores logs or actions performed by user.

&#x09;	- Example: Logs, Audit trails



***III) Least Privilege:*** Users should be granted only the minimum permissions required to perform their job.

&#x09;eg. HR employee should not have: Database admin access, Firewall access



***IV) Defense in Depth***: A security strategy that uses multiple layers of security controls so that if one control fails, others still provide protection.

&#x09;eg. Firewall -> IDS/IPS -> MFA -> Antivirus -> Encryption



***V) Security policies:*** formal documents that define how security should be implemented and maintained within an organization.

&#x09;eg. Password Policy, Access Control Policy, Incident Response Policy



***VI) Non-Repudiation:*** It ensures that a user cannot deny performing an action.

&#x09;eg. Digital signature on transaction.

&#x09;	User cannot later claim: I didn't perform this transaction.


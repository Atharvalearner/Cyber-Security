***Buffer Overflow :***

* A vulnerability that occurs when a program writes more data into a memory buffer than it can hold, causing adjacent memory to be overwritten.
* **Main reasons:** no input length checking

&#x09;	 unsafe functions

&#x09;	 insecure memory handling

* **Attackers may :**	crash application

&#x09;		execute malicious code (RCE)	

&#x09;		gain system access

&#x09;		escalate privileges

* **Working:** 1. Vulnerable Buffer Exists: eg. gets(), strcpy(), strcat(), etc

&#x09;    2. No Input Validation: Application does not check input size.

&#x09;    3. Attacker Sends Large Payload

&#x09;    4. Memory Gets Overwritten or buffer get exceeds

&#x09;    5. Program Behavior Changes. eg. crash, arbitory code execution, etc

&#x09;    6. Attacker Gains Control.

* **Real-World Example:** Morris Worm, Code Red, Slammer Worm : Used memory corruption vulnerabilities.
* **Types:** 1. Stack overflow: Occurs in stack memory, Can overwrite: return address.

&#x09;  2. Heap overflow: Occurs in heap memory, Targets: dynamically allocated memory

&#x09;  3. Integer overflow: Arithmetic exceeds storage capacity.

* **Prevention methods:** proper input validation, bounds checking, secure coding practices, using safe functions, memory-safe programming languages.





***Input Validation :***

* process of verifying and restricting user-supplied input to ensure it is safe, expected, and within acceptable boundaries before processing it.
* **Attackers may send**: scripts, commands, oversized data, malicious payloads. So, Input validation prevents this.
* **Helps prevent attacks** like SQL Injection, XSS, Command Injection, Buffer Overflow, File Inclusion, Path Traversal
* Input validation works by checking input length, type, format, range, and allowed characters
* **Working:** 1. Receive User Input

&#x09;    2. Validate Input

&#x09;    3. Reject Invalid Input

&#x09;    4. Sanitize If Needed

&#x09;    5. Process Safe Input



***Scenario :***

Suppose a login form expects a username of maximum 20 characters. If the application does not validate input length, an attacker may send oversized data causing a buffer overflow or malicious payloads causing injection attacks.


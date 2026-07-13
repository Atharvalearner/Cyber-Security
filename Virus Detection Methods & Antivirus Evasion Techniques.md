**# Virus Detection Methods \& Antivirus Evasion Techniques:**

First understand the overall process.



*File Arrives*

&#x20;     *↓*

*Antivirus Scans File*

&#x20;     *↓*

┌───────────────────────┐

│ Signature Detection          │

│ Heuristic Detection          │

│ Behavior Detection           │

│ Reputation/Cloud Intelligence│

│ Sandboxing                   │

└───────────────────────┘

&#x20;     *↓*

*Malicious?*

&#x20;     *↓*

*Yes → Quarantine / Block*

*No  → Allow*



***# Antivirus :***

software is a security solution designed to detect, prevent, quarantine, and remove malicious software such as viruses, worms, Trojans, ransomware, and spyware.



***Its main objectives are:***

* Detect malware
* Prevent infection
* Remove malware
* Protect the system



**# How Does Antivirus Detect Malware?**

It combines several techniques: **Signature Detection** + **Heuristic Detection** + **Behavior Analysis** + **Cloud Intelligence** + **Sandboxing**



**# Simple Analogy:**

**| ---------------- | ------------------------------- |**

**| Method           | Detects                         |**

**| ---------------- | ------------------------------- |**

| Signature        | Compare with Known malware      |

| Heuristic        | Suspicious code patterns        |

| Behavior         | Suspicious runtime behavior     |

| Sandboxing       | Executes safely for observation |

| Cloud Reputation | Known file reputation           |

| Machine Learning | Unknown malware patterns        |

**| ---------------- | ------------------------------- |**



**# In Detail:**

1. **Signature Detection:**
* comparing files against a database of known malware signatures or unique patterns.
* Example: Malware Database

Virus A → Signature A

Virus B → Signature B

Virus C → Signature C



Now a new file arrives.

Incoming File >> Compare Signature >> Match Found >> If Yes then antivirus identifies it as known malware.





**2. Heuristic detection:**

* It identifies suspicious files by analyzing their characteristics and code patterns instead of relying only on known signatures.
* Limitation Sometimes legitimate software may appear suspicious. This creates: False Positive
* Instead of asking: Is this Virus X?
* It asks: Does this file behave or look suspicious?

***Unknown File***

&#x20;     ***↓***

***Code Analysis***

&#x20;     ***↓***

***Suspicious Characteristics?***

&#x20;     ***↓***

***High Risk***





**3. Behavior-based detection:**

* It monitors what a program does while it is running and identifies malicious activities instead of relying only on how the program looks.
* Example: Suppose a program suddenly: Encrypts Hundreds of Files or Disables Windows Defender or Creates Persistence

These behaviors are suspicious.





**4. Sandboxing:**

* It is the process of executing a suspicious file in an isolated environment to safely observe its behavior without affecting the real system.
* Instead of running malware on your real laptop, the antivirus runs it inside: Virtual Machine or Isolated Environment.
* Think of it as:

***Unknown File***

***↓***

***Virtual Test Environment***

***↓***

***Observe Behavior***

***↓***

***Safe Decision***





**5. Reputation / Cloud-Based Detection:**

* Modern antivirus also uses cloud intelligence.
* Instead of checking only: Local Database. It can ask: Cloud Reputation Service

***Questions include:***

Has this file been seen before?

Is it digitally signed?

Is it trusted?

How many users have it?



* Example: Unknown File >> Cloud Check >> Known Malware? >> If yes >> Block





**6. Machine Learning Detection:**

* Many modern endpoint protection products use machine learning models.
* Instead of searching for one signature, they analyze: file structure, imported functions, entropy, metadata, behavior indicators
* The model predicts: Likely Benign or Likely Malicious.





**# Real Interview Scenario**

* **A user downloads a brand-new ransomware sample. How can the antivirus detect it if no signature exists?**

Even without a known signature, modern security solutions may detect the ransomware using heuristic analysis, behavior-based detection, machine learning, reputation services, or sandboxing. For example, if the program begins rapidly encrypting files, modifying backups, or creating persistence, behavior monitoring can identify these actions as malicious.


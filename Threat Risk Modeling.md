***Threat Risk Modeling :***

* A structured process
* used to identify, analyze, prioritize, and mitigate potential security threats and risks in a system, application, network, or business process before attacks occur.
* Threat modeling is **Proactive Security**: security BEFORE attack happens.
* **Used in**: web applications, APIs, cloud environments, mobile apps, enterprise systems, banking systems, healthcare systems
* Threat modeling usually done during Design Phase in SDLC.



***Before building or deploying a system, we ask***: "What can go wrong?"

**Then**: identify threats, analyze risks, apply security controls



***Common Threat Modeling Methodologies:***

1. **STRIDE:** created by Microsoft for Framework Knowledge

&#x09;***S = Spoofing***: Pretending to be another user. eg. Attacker use a leaked JWT token and acts as a admin role intact.

&#x09;***T = Tampering***: Modifying/Altering data like requests, files, configs, logs.

&#x09;***R = Repudiation***: User denies performing action. eg. a malicious admin deletes the audit log right after issuing refunds.

&#x09;***I = Information Disclosure***: Sensitive data leakage. eg. API keys printed in debug log.

&#x09;***D = Denial of Service***: Service unavailability.

&#x09;***E = Elevation of Privilege***: Gaining high privilege from low. eg. Normal user becomes admin.



2\. **DREAD:** Used for risk scoring

&#x09;D = Damage

&#x09;R = Reproducibility

&#x09;E = Exploitability

&#x09;A = Affected Users

&#x09;D = Discoverability



* Helps organizations reduce attack surfaces, improve secure design, minimize security risks, and strengthen overall application security.



***Real Scenario:***

Suppose a company is developing an online banking application. During threat modeling, the security team identifies threats such as SQL injection, session hijacking, credential stuffing, and DDoS attacks. Based on risk analysis, they implement controls like MFA, HTTPS, input validation, encryption, and rate limiting before deployment to reduce the attack surface.


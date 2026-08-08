Session Hijacking is an attack in which an attacker takes over a legitimate user's active session by obtaining or predicting the user's session identifier (session ID). Since web applications use session IDs to identify authenticated users after login, anyone who obtains a valid session ID can impersonate that user without knowing their password.



Session hijacking can occur through methods such as session cookie theft using XSS, Man-in-the-Middle attacks, session fixation, malware, or insecure network communication. The impact includes unauthorized account access, data theft, and performing actions on behalf of the victim.



To prevent session hijacking, applications should enforce HTTPS, use Secure and HttpOnly cookie attributes, regenerate session IDs after login, implement proper session timeouts, use unpredictable session IDs, enable MFA, and protect against XSS and CSRF vulnerabilities.





**# Session Hijacking:**

\- an attack where an attacker **steals, predicts, or manipulates a valid session like cookie session cookies, tokens, session identifiers**

\- an authenticated user and gain unauthorized access to their session.



Working:

1. User Authenticates
2. Session ID Stored
3. Attacker Obtains Session ID
4. Attacker Reuses Session
5. Unauthorized Access



**Why Session Hijacking is Dangerous :**

***Attacker can:***

bypass authentication

access accounts

steal sensitive data

transfer money

impersonate users.


**Static Application Security Testing(SAST):**



* Used in ***Shift left*** security with static scanning.
* Performs white box security testing.
* Runs on every commit so it is repeatable.
* Analyzes source code or binaries without executing the application to find security vulnerabilities.
* ***It Scans***: Code, Data flow, AST, Control flow
* ***Used to Finds***: SQLi, XSS, Path traversal, Hardcoded secrets
* ***SAST Scan tool:*** Sonar qube, Sengrap



\---------------------------------------------------------------------------------

&#x09;	**SAST			| Manual review				|**

\---------------------------------------------------------------------------------

1. Consistent \& Repeatable		| 1. Understand context \& intent	|
2. Scales to millions Line of Code	| 2. Finds complex logic bugs		|
3. Runs on every content		| 3. Slow and expensive			|
4. Can miss business logic flaws	| 4. Human fatigue and inconsistency	|

\---------------------------------------------------------------------------------



***SAST tool Limitations:***

1. It can generate noise, it requires proper training and triaging.
2. Weaker for newer languages like go, rust, etc
3. Doesn't fully understand business logic or custom frameworks without configuration.


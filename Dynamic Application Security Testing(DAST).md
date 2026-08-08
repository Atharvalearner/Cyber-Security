***Dynamic Application Security Testing (DAST):***

* Used for black box security testing.
* DAST tests: Running application in real-time instead of source code.
* Real Attack simulation.
* ***DAST Tool:*** OWASP ZAP, Burp suit, Qualys WAS



\---------------------------------------------------------------------------------

**|		DAST			|		SAST			|**

\---------------------------------------------------------------------------------

| Black-box testing			| White box testing			|

| Phase: Testing/Production		| Phase: Development			|

| Test running application		| Analyze source code			|

| Finds runtime vulnerabilities		| Finds code level bugs			|

| Business logic flaws			| SQL injection patterns		|

| Auth bypass detection			| XSS vulnerability patterns		|

| Session management issues		| Cannot test runtime behaviour		|

\---------------------------------------------------------------------------------



***Types:***

1. Authenticated Scanning
2. Unauthenticated Scanning



***We Use DAST To discover:***

1. runtime vulnerabilities

2\. deployment issues

3\. authentication flaws

4\. server misconfigurations





**# How OWASP ZAP works internally ?**

OWASP ZAP is an open-source Dynamic Application Security Testing (DAST) tool that works primarily as an intercepting proxy. Internally, it sits between the client, such as a browser, and the target web application, allowing it to capture, inspect, and modify all HTTP and HTTPS requests and responses.



First, ZAP acts as a proxy and records all the application's URLs, forms, parameters, cookies, and API endpoints. Then its Spider crawls the application to discover additional pages and endpoints. During Active Scanning, ZAP automatically sends specially crafted requests to test for vulnerabilities such as SQL Injection, Cross-Site Scripting (XSS), Command Injection, Path Traversal, and Security Misconfigurations. It analyzes the server's responses to determine whether a vulnerability exists. Finally, ZAP generates a report with the vulnerability details, severity, affected URLs, and recommended remediation.



So, internally, the workflow is: Proxy → Crawl → Analyze → Attack → Validate → Report.


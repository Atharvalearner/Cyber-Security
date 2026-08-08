HTTP headers are key-value pairs exchanged between a client and a server that provide metadata about HTTP requests and responses. They are used for authentication, session management, content negotiation, caching, and security. Examples include Host, Authorization, Cookie, Content-Type, Set-Cookie, and Cache-Control. Security headers such as CSP, HSTS, X-Frame-Options, and HttpOnly cookies help protect web applications from attacks like XSS, clickjacking, and session hijacking.





**# HTTP Headers:**

* **key-value pairs exchanged between clients and servers** that provide additional information about HTTP requests and responses.
* Headers are used for **authentication, session management, content negotiation, caching, security enforcement, and communication control**.



* Common request headers :

&#x09;- ***Host:*** Specifies target domain. eg. Host: example.com

&#x09;- ***User-Agent:*** Identifies browser/client. eg. User-Agent: Mozilla/5.0

&#x09;- ***Authorization:*** Carries authentication credentials. eg. Authorization: Bearer token123

&#x09;- ***Accept:*** Specifies accepted content types. eg. Accept: text/html

&#x09;- ***Cookie:*** Sends session cookies. eg. Cookie: SESSIONID=abc123, Very important in: authentication, session management

&#x09;- ***Content-Type:*** Defines request body format. eg. Content-Type: application/json



* Common response headers :

&#x09;- ***Set-Cookie:*** Creates cookies in browser. eg. Set-Cookie: SESSIONID=abc123

&#x09;- ***Server:*** Indicates server software. eg. Server: Apache

&#x09;- ***Location:*** Used in redirects. eg. Location: /login

&#x09;- ***Cache-Control:*** Controls caching behavior. eg. Cache-Control: no-cache



* **Security-related headers :**

&#x09;- ***Content-Security-Policy:*** Helps prevent XSS attacks. 

&#x09;- ***Strict-Transport-Security:*** Forces HTTPS usage. Protects against: SSL stripping

&#x09;- ***X-Frame-Options***: Prevents: Clickjacking, eg. X-Frame-Options: DENY

&#x09;- ***HttpOnly cookies***: Prevents JavaScript access. Helps against: XSS

&#x09;- ***Secure (Cookie attribute)*** – Sends cookies only over HTTPS.

&#x09;- ***SameSite (Cookie attribute)*** – Helps mitigate CSRF attacks.

&#x20;

&#x20;  helps protect applications against attacks like XSS, clickjacking, session hijacking, and MITM attacks.


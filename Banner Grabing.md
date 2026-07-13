**Banner grabbing:**

* an information-gathering technique 
* used to identify the service, software, version, and sometimes operating system information running on an open port by analyzing the response returned by that service.
* It answers: What exactly is running on this open port?



**# The main idea is simple:**

*Scanning tells us what ports are open.* 

*Banner grabbing tells us what services are running.* 

*OS fingerprinting tells us what operating system may be running.*



**# Working:**

*Step 1: Identify an open port*

*Step 2: Connect to the service*

*Step 3: Send a normal or service-specific request*

*Step 4: Observe the response*

*Step 5: Identify service and version information*



**| ------------------------------ | ------------------------------ |**

**| Active                         | Passive                        |**

**| ------------------------------ | ------------------------------ |**

| Directly contacts target       | Observes existing traffic      |

| Generates traffic              | Does not actively probe/Explore|

| Easier to detect               | Harder to detect               |

| Often gives direct information | Relies on observed behavior    |

| May appear in logs             | Usually less visible           |

| ------------------------------ | ------------------------------ |



**# Banner Grabbing Tools:**

| --------- | ----------------------------------- |

| Tool      | Purpose                             |

| --------- | ----------------------------------- |

| Nmap      | Service and version detection       |

| Netcat    | Manual TCP/UDP connection testing   |

| Telnet    | Basic manual service interaction    |

| curl      | HTTP response and header inspection |

| Wireshark | Passive traffic analysis            |

| --------- | ----------------------------------- |








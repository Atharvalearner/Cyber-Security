**# Android Security Model:**

a layered security architecture that protects devices, applications, and user data using mechanisms such as application sandboxing, Linux user isolation, permissions, application signing, secure inter-process communication (IPC), verified boot, and SELinux enforcement.



**# Simply put:**

Android doesn't rely on a single security feature. It uses multiple security layers working together.



**# Android Security Architecture:** Each layer protects against different threats.

*Verified Boot*

&#x20;     *↓*

*Linux Kernel Security*

&#x20;     *↓*

*SELinux*

&#x20;     *↓*

*Application Sandbox*

&#x20;     *↓*

*Permissions*

&#x20;     *↓*

*App Signing*

&#x20;     *↓*

*Secure IPC*

&#x20;     *↓*

*Google Play Protect*



***# Verified Boot:***

checks the integrity of the operating system during startup to help ensure that the device boots only trusted software.

This helps protect against unauthorized modification of the operating system.



***# SELinux (Security-Enhanced Linux):***

a mandatory access control (MAC) that restricts what processes can access, even if they are running with elevated privileges.

It restrict process capabilities according to defined security policies, reducing the impact of compromised applications or services.

*Root User >> Still Restricted >> SELinux Policy*



***# Application Sandboxing:*** 

Android isolates every application using a sandbox. 

Each app runs with a unique Linux UID, preventing it from directly accessing another application's files, memory, or processes unless explicit mechanisms are provided.



***# Permission Model:***

Android uses a permission-based security model where applications must request access to sensitive resources such as the camera, microphone, location, contacts, or storage.



***# Application Signing:***

Every Android application must be digitally signed before it can be installed.

The signature verifies the application's integrity, identifies the developer, and helps ensure that updates come from the same signing identity.



**# Secure Inter-Process Communication (IPC):**

* Applications sometimes need to communicate.
* Android provides secure IPC mechanisms such as: **Intents, Binder**
* ***Instead of:                             App A >> Direct Memory Access >> App B***
* ***Android uses controlled communication:  App A >> Binder / Intent      >> App B***

This helps maintain application isolation.



***# Google Play Protect:***

Google Play Protect helps: Scan installed apps, Detect known malware

Warn users about potentially harmful applications





***## Complete Android Security Flow:*** Suppose a user installs an app.

*Download APK*

*↓*

*Verify Signature*

*↓*

*Assign UID*

*↓*

*Create Sandbox*

*↓*

*Request Permissions*

*↓*

*Run with SELinux Policies*

*↓*

*Play Protect Monitoring*


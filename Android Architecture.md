**# Android:**

an open-source, Linux-based mobile operating system developed by Google for smartphones, tablets, TVs, wearables, and other embedded devices.



**# Key points:**

* Linux Kernel
* Open Source (AOSP)
* Java/Kotlin apps (plus native code via NDK)
* Application Sandbox
* Permission-based security



***# Android Architecture:***

**+--------------------------------------+**

**|          Applications                |**

**| (WhatsApp, Chrome, Gmail, etc.)      |**

**+--------------------------------------+**

**| Application Framework                |** *provides services that Android applications use (Activity, Package, Window, Notification, Location, Resource Manager)*

**+--------------------------------------+**

**| Android Runtime (ART) + Native Libs  |** *responsible for: Running applications, Memory management, Garbage collection, Executing app bytecode*

|				       | Android also includes native libraries written mainly in C/C++. eg SQLite, Media Framework, Web rendering components

**|				       |** *Java / Kotlin Code >> Compiled >> DEX Bytecode >> ART Executes*

**+--------------------------------------+**

**| Hardware Abstraction Layer (HAL)     |** *provides standard interfaces that allow Android to communicate with hardware components without exposing hardware-specific implementation details to applications.*

**+--------------------------------------+**

**| Linux Kernel                         |** *manages memory, processes, networking, power, security, and hardware drivers, providing the core operating system functionality.*

**+--------------------------------------+**



**# Device Drivers:**

* A specialized software program that acts as a translator between your computer's operating system (like Windows or macOS) and its hardware devices

Device Drivers

* Examples: Display, Camera, USB, Wi-Fi, Audio driver



**# Complete Android Architecture Flow: For Camera:**

*Camera App*

*↓*

*Application Framework*

*↓*

*Camera Service*

*↓*

*HAL*

*↓*

*Camera Driver*

*↓*

*Linux Kernel*

*↓*

*Camera Hardware*






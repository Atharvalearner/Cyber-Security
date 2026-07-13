**# Android application ecosystem:**

In its own security sandbox each app is isolated
Each app has its own unique userID
Each app having access to /data/data/app\_home.



**# Android Architecture:**

1. Run on top of the Linux
2. Dalvik / ART VM optimized for mobile devices.
3. Integrated browser based on webkit engine.
4. optimized graphics with OpenGL.
5. Local SQLite/Public Firebase database for structure data storage.



**# Android Fundamentals:**

* Apps written in Java/Python/Kotlin/Flutter
* Compiles into Android Package file (apk)
* Apps consists of components, a manifest file and resources
* Components: Activity,

&#x09;       Services,

&#x09;       Content Provider, 

&#x09;       Broadcast Receiver



**# Manifest file:**

* AndroidMenifest.xml present in root directory
* Presents information about app to the android system
* Describes the components used in the application
* Declares the permissions required to run the application
* Declares minimum android API / OS level that application requires



1. In manifest tag we get package=com.android.appName which is nothing but the directories where actual code is stored.

2\. At OS level it creates it as home directory and at developer site it was develop app using that appName

3\. All components are written in application tag.

4\. In-scope and out-scope components





***# Activity:***

Represents single screen with UI.

Most app contains multiple activities.

When new activity starts it is pushed onto the back stack

UI can built with XML or in Java.

Monitor lifespan through callback methods like onStart(), onPause(), etc



***# Services:***

Perform long-running operations in the background.

Does not contain UI

Useful for network operations, Playing music, etc

Run independently of the component the create it

Can be bound to by other application components, if allowed



***# Content Providers:***

Used to store and retrieve data and make it accessible to all applications

Are the only way to share data across different applications

Exposes a public URI that uniquely identifies its data set

Data exposed as a single table on a database model

Android contains many providers for things like contacts, media, etc



**# Broadcast receiver:** 

It is notifications received by applications.

Type of notifications:  Application wide notifications

&#x09;		System wide notifications

&#x09;		Push notifications


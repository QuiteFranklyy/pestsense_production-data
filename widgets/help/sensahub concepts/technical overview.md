<!--Sensahub Technical Overview Documentation-->
<br>

# Sensahub Technical Overview

---

## About
This page is dedicated to explaining some of the more technical details of how sensahub works on the software side.

---
<br> 
+ Integrated software platform for connecting, processing and visualisation of data streams​

    + Optimised for Internet of Things use-cases​
<br>
​

+ Written in C# using Visual Studio with Microsoft’s latest .NET Core managed applications platform​

    + Able to run cross-platform on Windows, Linux and Mac-OS.​

    + Multi-threaded and asynchronous for high performance​
​

+ Message orientated Publish Subscribe model​

    + Messages published to a central queue then routed to subscribers.​

    + Able to perform as a MQTT Message Broker (QoS level 0)​
​

+ Microservices design, with a Core Service providing basic functionality, utilising microservices based extensions to extend the functionality of the core.​

    + Design is microservices based but current implementation utilises a mix of asynchronous message passing and synchronous API calls (with no direct module to module calling)​

    + Current release is implemented as separate projects in one Visual Studio solution​

    + Next release will completely separate the extensions, replace remaining API calls with message passing and use MQTT over Sockets for communication for multi-tenant SaaS​

<br>

---
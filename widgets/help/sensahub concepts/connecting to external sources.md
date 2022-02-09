<!--Connecting to External Sources-->
<br>

# Connecting to External Sources

---

## HTTP REST

Sensahub accepts encrypted HTTP (HTTPS) messages from external sources in a variety of formats.

The REST service will accept requests to retrieve current channel data or to initiate a flow for data parsing and transformation in the following formats:
+ URL should have a **postfix of api** (eg *https://api.application.sensahub.com*).

+ Method calls: **GET** (get and set), **PUT** (set only), **POST** (set only).

+ Media types: **text/html** (for text), **application/JSON** (for JSON formatted), **application/x-www-form-urlencoded** (for form-based data).

All REST requests will require a request *'accept'* header for the request to be accepted. Usually this would be *Accept=text/html*.

Data can be sent in a REST message 3 different ways:
+ Through the URL query strings an an implied GET method (convenient to invoke commands manually via a browser URL). Eg: *httpls://api.\<server\>.com/category/class/instance/scope?data=yyyy&token=abcdefg*.

+ Through headers where the content-type must be *application/x-www-form-urlencoded*, with methods POST and PUT.

+ Through the document body, either as JSON or form-urlencoded, header *content-type* as *application/JSON* with methods POST and PUT.


As well as initiating a flow from a REST request to ingest data from the external device/system, REST messages can be used to retrieve data from Sensahub as the result of a flow.

**WIP**

See the REST Flow Widget for information about setting up and using REST in Sensahub.


## MQTT
Topics that a remote node is requesting a subscription to Sensahub has to be in lower case

See the MQTT Flow Widget for information about setting up and using MQTT in Sensahub

<br>

---

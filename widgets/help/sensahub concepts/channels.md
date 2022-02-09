<!--Channels-->
<br>

# Sensahub Channels

---

## About
+ A Sensahub channel is a virtual representation of the data stream coming to and from the connected device or system. A channel may group several datapoints ("scopes") like pressure or signal strength, directing this data between the device and Sensahub applications.

+ Sensahub channels are analogous to a television channel, in the same way you select a TV channel to watch a specific program, you select a Sensahub channel to view specific data.

+ Also like the world wide web, where a URL namespace is used to connect to a website, a Sensahub channel uses a similar namespace concept to identify the data stream to use in a Sensahub application.

+ The channel namespace includes a "category" and a "class" to identify the channel; the name ("instance") of the device; and the device datapoint measurements ("scopes") to use. For example, the namespace can represent an organisational hierarchy or a location.

+ Channels are used for directing data within the server, within the client and between the client and server. Within the client, the channel is represented by just a channel name and a scope.

---

### Example

We have a <span style="color:#ec891e;font-weight:bold;">Water</span> <span style="color:#0070c0;font-weight:bold;">Tank</span> located in <span style="color:#ec891e;font-weight:bold;">Canberra</span> with a sensor installed that can measure the water <span style="color:#00b050;font-weight:bold;">Level</span>, <span style="color:#00b050;font-weight:bold;">Temperature</span> and <span style="color:#00b050;font-weight:bold;">Battery</span> level. Below is a representation of the Sensahub channel namespace used for collecting tank measurements for a sensahub application.

<img src="/images/help/sensahub concepts/channels/channel_example.png" width="934" height="589" style="display:block;margin-left:auto;margin-right:auto;width:100%;height:auto;">

<br>

---
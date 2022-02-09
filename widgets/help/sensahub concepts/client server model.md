<!--Client Server Model-->
<br>

# The Client Server Model

---

## About
The client server model is a system architecture that receives and processes data in one place, while allowing many clients to interact with the information.

<img src="/images/help/sensahub concepts/client server model/client_server_model.png" width="2000" height="284" style="display:block;margin-left:auto;margin-right:auto;width:100%;height:auto;">

---
<div class="column-container">
<div class="column row-container">
<div class="row">

### Connect Externally

+ Use a server flow *Start* node to connect to **MQTT** or **REST** data sources.
+ Setup connection configurations including remote authentication and device authorisation in *Start* node settings.
+ Other protocols are handled by channel plugins.

</div>

<div class="row">

### Server Processing

+ Incoming data is processed by the server flows.
+ If incoming data is in the JSON format, this data can be parsed into separate branches using the *JSON Parser* flow node.
+ Server scripts provide powerful data transformation opportunities, allowing the server to process data before it is sent to the client.
+ Output results of processing into relevant channels.
+ Use the '+' wildcard in a channel defninition to handle multiple devices with the same flow.

</div>

<div class="row">

### Client Display

+ A client subscribes to server channels to receive all newly processed data from the server.
+ Client events and scripts are used to prepare and handle displaying the data.
+ Widgets are used to display the server data.
+ Events can also be published back to the server.

</div>
</div>

<div class="column row-container">
<div class="row">
<img src="/images/help/sensahub concepts/client server model/external_connections.png" width="200" height="136">
</div>
<div class="row">
<img src="/images/help/sensahub concepts/client server model/server_processing.png" width="200" height="140">
</div>
<div class="row">
<img src="/images/help/sensahub concepts/client server model/client_applications.png" width="200" height="166">
</div>
</div>
</div>

<br>

---
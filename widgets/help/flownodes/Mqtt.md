<!-- MQTT Widget Help Markdown -->
<br>

# MQTT Node

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The MQTT node acts as an MQTT broker. The MQTT node can be configured with a certain MQTT topic, and then will output the values received from the topic. Options such as Quality of Service, username, password, certificate name etc can be configured.

</div>

<div class="column row-container">
<img src="/images/help/mqtt/mqtt_main.png" width="109" height="63">
</div>
</div>

___

<div class="column-container">
<div class="column row-container">
<div class="row">

## MQTT Properties
| Property | Description |
| -------- | ----------- |
| Name | Widget name. |
| Certificate Name | Enter certificate filename if using certificate (stored in data/certificates folder).​​ |
| Protocol | MQTT version number. |
| Remote Broker | Remote MQTT  server to connect to. |
| Clean Session | Clean = true to reset broker session on reconnect, clean = false to enable missed messages with QoS > 0.​ |
| Retain | Published  Subscribing clients will receive the latest message when they connect.​ |
| Model | Enter a device model name that combines with the topic level or JSON key to ensure a unique device indentifier. | 
| Topic Level | Select the topic level to extract the unique device indentifier.​ |
| Json Key | Enter the JSON key (first level) to extract the unique device indentifier. |
| Broker | Select switch between Broker and client functionality. |
| Username | MQTT connect username. |
| Password | MQTT connect password. |
| Subscription | Process incoming messages for the subscription topic from remote broker or remote device.​ | 
| Encryption |  Select to enable encryption TLS, Note – Check port number if changing encryption. |
| Protocol Types | ​​​​​MQTT version numbers. |

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>


## MQTT Service Types
| Type | Description |
| ---- | ----------- |
| At most once | No retries. |
| At least once | Retries but might get duplicated. |
| Exactly once | Guaranteed only one delivery. |



</div>
 
</div>

<div class="column row-container">
<div class="row">
<img src="/images/help/mqtt/mqtt_client_specific.png" width="150" height="290">
</div>
<div class="row">
<img src="/images/help/mqtt/mqtt_device_id.png" width="150" height="300">
</div>
<div class="row">
<img src="/images/help/mqtt/mqtt_publish_form.png" width="150" height="318">
</div>
<div class="row">
<img src="/images/help/mqtt/mqtt_quality.png" width="150" height="110">
</div>
<div class="row">
<img src="/images/help/mqtt/mqtt_protocol.png" width="150" height="103">
</div>
</div>
</div>

#### Tips
> Make sure to register the devices in the Device Manager, otherwise the incoming MQTT messages will not be processed.

---
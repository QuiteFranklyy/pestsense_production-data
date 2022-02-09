<!-- Battery Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Battery Widget

___
<div class="column-container">
<div class="column row-container" style="width:120%">


## About
The Battery widget is a visual depiction of charge level. It can be used to show the battery level of devices, sensors, and backup power storage. 


</div>

<div class="column row-container">
<img src="/images/help/battery/battery.png">
</div>
</div>

___

## Battery Properties

The battery widget does not have any properties.

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive Value | Sets the displayed battery level to the received value. |

</div>
<div class="column row-container">
<img src="/images/help/battery/battery_client_input.png">
</div>
</div>

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Events
| Event | Description |
| ----- | ----------- |
| Feed | Is the data stream directed from the server channel. |

</div>
<div class="column row-container">
<img src="/images/help/battery/battery_server_input.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
>The battery can only use values from 0-100, so only inputs of 0-100 should be sent to the battery widget. If coming from a server event, an operator flows widget can be used to scale the data. If coming from a client event, a scripting widget can be used to scale the data.

---
<!-- Light Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Light Widget

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The Light widget is used to display the status of a light or a group of lights. It can also be used as an input to turn lights on and off. It also has a gradual dimming function, allowing lights to be set to a custom brightness level. 

</div>

<div class="column row-container">
<img src="/images/help/light/light.png" width="102" height="95">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Light Properties
| Property | Description |
| -------- | ----------- |
| Dimmer | Set the light to be a dimmer. This means that the user can click and hold on the light, and it will slowly increase to maximum brightness, and then slowly decrease to minimum brightness. |

</div>
<div class="column row-container">
<img src="/images/help/light/light_spicific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive Value | Sets the value of the light to the received value. |

</div>
<div class="column row-container">
<img src="/images/help/light/light_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Output Events
| Event | Description |
| ----- | ----------- |
| Pressed | Activates when the light is clicked on. It sends the current brightness to the configured client channel. |

</div>
<div class="column row-container">
<img src="/images/help/light/light_client_output.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Events
| Event | Description |
| ----- | ----------- |
| Feed | Is the data stream directed from the server channel. The value of the light is set to value received from the server. |

</div>
<div class="column row-container">
<img src="/images/help/light/light_server.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
>The light widget is used primarily in smart homes but can be used for worksites and offices as well.
If a brightness level has been set using the dimmer function before, simply clicking on it will turn it on to the custom brightness level. 

>This set value will persist but only on the same phone or desktop as the setting is saved locally.

---
<!-- Indicator Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Indicator Widget

___
<div class="column-container">
<div class="column row-container" style="width:100%">


## About
The indicator widget is used to display a light-based representation of a value within the boundaries specified in the threshold settings. The type of boundaries may also be specified in the threshold type. Indicator takes server and client input events and does not output. 


</div>

<div class="column row-container">
<img src="/images/help/indicator/indicator.png" width="52" height="96">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Indicator Properties
| Property | Description |
| -------- | ----------- |
| Indicator Type | Changes the indicator from the default traffic light to a single light. |
| Threshold Type | Used to determine how the thresholds will be used. | 
| Above | The threshold the light will turn on. | 
| Below | The threshold the light will turn on. |
| Binary | If the light receives a 1 it will turn green on. If the light receives a 0 it will turn red. 
| Text | If the Text matches then the light will turn on. | 
| Blink Threshold | The threshold at which the red light will start blinking. | 
| Red Threshold |The threshold the red light will turn on. | 
| Yellow Threshold | The threshold the yellow light will turn on. |
| Green Threshold | The threshold the green light will turn on. |

</div>
<div class="column row-container">
<img src="/images/help/indicator/indicator_specific.png">
<img src="/images/help/indicator/indicator_specific_two.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive Value | Is the data stream sent from a client output event . |

</div>
<div class="column row-container">
<img src="/images/help/indicator/indicator_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Events
| Event | Description |
| ----- | ----------- |
| Feed | Is the data stream directed from the server channel. The value of the indicator is set to value received from the server. |

</div>
<div class="column row-container">
<img src="/images/help/indicator/indicator_server_input.png">
</div>
</div>


Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
> Use this widget to give a visual indication of movement of a device, or productivity of a machine.

---
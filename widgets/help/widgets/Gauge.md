<!-- Gauge Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Gauge Widget

___
<div class="column-container">
<div class="column row-container" style="width:90%">


## About
The Gauge widget is a way to graphically show whether the output of a sensor is within acceptable limits. The Gauge has a green, yellow, and red region, allowing a user to quickly determine if the device is acting as expected.

<br/>
</div>

<div class="column row-container">
<img src="/images/help/gauge/gauge.png" width="106 " height="106">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Gauge Properties
| Property | Description |
| -------- | ----------- |
| Title | Sets the title displayed in the gauge widget.|
| Units | Sets the units displayed in the gauge widget. |
| Min | Sets the minimum value that can be displayed. |
| Max | Sets the maximum value that can be displayed. |
| Red Threshold | Sets the maximum threshold of the red region. |
| Yellow Threshold | Sets the maximum threshold of the yellow region. |
| Green Threshold | Sets the maximum threshold of the green region. |
| Lower Bound | Sets the lower bound of the green region. |

</div>
<div class="column row-container">
<img src="/images/help/gauge/gauge_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive Value | Sets the value of the gauge to the received value. |
| Get Value | Deprecated, used to get the value of the gauge. |
| Set Title | Sets the title of the gauge. |
| Set Unit | Sets the name of the unit that is displayed. |
| Set Min | Sets the minimum of the gauge. |
| Set Max | Sets the maximum of the gauge. |

<br/>
</div>
<div class="column row-container">
<img src="/images/help/gauge/gauge_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Events
| Event | Description |
| ----- | ----------- |
| Feed | Is the data stream directed from the server channel. The value of the gauge is set to values received from the server. |

</div>
<div class="column row-container">
<img src="/images/help/gauge/gauge_server_input.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
>The gauge can display things such as engine RPM, using the red region as the rev limit.
 

>The gauge can display temperature, having the green region as normal temperature, yellow as a warning temperature, and red as too hot.

---
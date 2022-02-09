<!-- Dial Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Dial Widget

___
<div class="column-container">
<div class="column row-container" style="width:100%">


## About
The Dial widget is a simple widget that can display values combined with an indicator that suggests the minimum and maximum values. The range of the dial is customisable, allowing it to display high ranges such as engine RPM.

</div>

<div class="column row-container">
<img src="/images/help/dial/dial.png">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Dial Properties
| Property | Description |
| -------- | ----------- |
| Range | The range of the expected input. |
| Decimals | The number of decimals displayed on the dial. |

</div>
<div class="column row-container">
<img src="/images/help/dial/dial_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive Value | Sets the value of the dial to the received value. |
| Channel0 Scope | Sets the scope of the server feed channel. |
| Channel0 Instance | Sets the instance of the server feed channel. |

</div>
<div class="column row-container">
<img src="/images/help/dial/dial_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Events
| Event | Description |
| ----- | ----------- |
| Feed | Is the data stream directed from the server channel. The value of the dial is set to value received from the server. |
| Average | Is the average of the data streamed from the server channel. |

</div>
<div class="column row-container">
<img src="/images/help/dial/dial_server_input.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
> The dial is applicable to many scenarios where a generic value indicator is sufficient, or when a more contextually relevant widget (like the water tank) isn’t available. 

---
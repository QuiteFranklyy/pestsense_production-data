<!-- Slider Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Slider Widget

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The Slider is a visual way to select a value in a pre-defined range. It can receive output from the client and server, and also publish data to the client and server.
 

</div>

<div class="column row-container">
<img src="/images/help/slider/slider.png" width="180" height="65">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Slider Properties
| Property | Description |
| -------- | ----------- |
| Form ID | An ID that groups widgets so that scripts can retrieve all the values from the grouped widgets together. |
| Step Size | The step between selectable values. | 
| Min Value | The minimum value selectable by the slider. | 
| Max Value | The maximum value selectable by the slider. | 
| Default Value | The default value of the slider. | 
| Hide Value | Hides the value of the slider |
| Vertical Slider | Toggles the slider to be vertically orientated |
| Value Color | The color of the slider value |

</div>
<div class="column row-container">
<img src="/images/help/slider/slider_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive Value | Sets the value of the slider to the received value. |

</div>
<div class="column row-container">
<img src="/images/help/slider/slider_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Output Events
| Event | Description |
| ----- | ----------- |
| Changed | Outputs the value of the slider when the slider is moved. |

</div>
<div class="column row-container">
<img src="/images/help/slider/slider_client_output.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Events
| Event | Description |
| ----- | ----------- |
| Feed | Is the data stream directed from the server channel. The value of the slider is set to values received from the server. |

</div>
<div class="column row-container">
<img src="/images/help/slider/slider_server_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Output Events
| Event | Description |
| ----- | ----------- |
| Changed | Outputs the value of the slider when the slider is moved. When used in conjunction with feed, you can see and change the server value of the slider. | 

</div>
<div class="column row-container">
<img src="/images/help/slider/slider_server_output.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
>The slider can be used to set targets on a radial widget.

>The horizontal size of the slider can be increased, allowing more accurate slider selection.

---
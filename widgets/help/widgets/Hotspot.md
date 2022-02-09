<!-- Hotspot Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Hotspot Widget

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The Hotspot widget is used to display a clickable area anywhere on the screen. It can be adjusted with shape, value, intensity and you can choose the color of the widget.

</div>

<div class="column row-container">
<img src="/images/help/hotspot/hotspot.png" width="103" height="104">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Compass Properties
| Property | Description |
| -------- | ----------- |
| ​​Intensity | Intensity of hot spot color. |
| Show When Clear | Display clear hotspot, intensity dictates shading. |
| Shape | Select the shape of the hotspot. |
| Value | Value to send on click. |
| Jump To Screen | On click, jump to the configured screen. |
| Color | Select color theme for button. |

</div>
<div class="column row-container">
<img src="/images/help/hotspot/hotspot_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Set Intensity | Sets the intensity of the hotspot. |
| Set Color | Gives you the option to choose the color of the Hotspot Widget. |
| Set Tooltip | Set the tooltip that is shown when hovering over the hotspot. |

</div>
<div class="column row-container">
<img src="/images/help/hotspot/hotspot_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Output Events
| Event | Description |
| ----- | ----------- |
| Pressed | Returns an event containing the data of the pressed hotspot. |

</div>
<div class="column row-container">
<img src="/images/help/hotspot/hotspot_client_output.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
> The Hotspot widget is useful to activate part of an image or a map, where the user can click the highlighted area to fire a widget event.

---
<!-- Switch Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Switch Widget

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The Switch Widget is a visual depiction of a switch. It can output custom values for the two switch states, and each state can have a custom name.

</div>

<div class="column row-container">
<img src="/images/help/switch/switch_red.png" width="105" height="55"/>
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:90%;">

## Switch Properties
| Property | Description |
| -------- | ----------- |
| On Label | Change the text in the on label. |
| Off Label | Change the text in the off label. |
| On Value | Set the value that is output by the switch when it is on. |
| Off Value | Set the value that is output by the switch when it is off. |
| Color | Change the colour of the switch. |

</div>
<div class="column row-container">
<img src="/images/help/switch/swtich_widget_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Event
| Property | Description |
| -------- | ----------- |
| Receive Value | Indicate if the toggle switch is turned on. |
| Instance | Indicate if the toggle switch is turned off.  |

</div>
<div class="column row-container">
<img src="/images/help/switch/switch_client_input_receive.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Output Client Event
| Property | Description |
| -------- | ----------- |
| Pressed | Output | Fires an event when the toggle is clicked. |

</div>
<div class="column row-container">
<img src="/images/help/switch/switch_client_pressed.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Event
| Property | Description |
| -------- | ----------- |
| Feed | Binds a SensaCollection data source. |
| Ini | Loads configuration file. |

</div>
<div class="column row-container">
<img src="/images/help/switch/switch_server_input_feed.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Output Event
| Property | Description |
| -------- | ----------- |
| Pressed | Fires an event when the toggle is clicked. |

</div>
<div class="column row-container">
<img src="/images/help/switch/switch_server_pressed.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
> When using the white switch, be sure to include a black container so the button is visible.
As an example, the switch can be used to turn off and on smart home devices.

> If the switch receives an input event, it will send the new value to any connected client output events. The value that it sends corresponds to the on/off values configured in the current switch, not the 0 or 1 value that it may receive.

> Do not connect two switches with both input and output events, it will create a recursion. It does exit after a certain threshold, but it's best to not do it in the first place.

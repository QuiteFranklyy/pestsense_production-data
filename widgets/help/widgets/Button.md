<!-- Button Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Button Widget

---

<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The Button widget is a simple input widget. When pressed it can run events, submit forms, and provides an easy way to run functions from the scripting widget.

To edit the text of the Button, click once on the Button. Use the arrow keys to move the cursor position.

To move the Button around, click and hold the mouse down on it while dragging the mouse.

</div>

<div class="column row-container">
<img src="/images/help/button/sensahub button.png">
</div>
</div>

---

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Button Properties
| Property | Description |
| -------- | ----------- |
| Action | Change how the button functions WIP. |
| Value On | The value that is sent when the button is pressed. |
| Jump To Screen | Changes the active screen
| Color | The background color of the button. |
| Outline Color | The outline color of the button. |
| Text Color | The color of the text in the button. |
| 3D Shadow | Enable a 3D shadow around the button. |

</div>
<div class="column row-container">
<img src="/images/help/button/button_widget_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Change Scope | Changes the scope of the server channel that the button is connected to. |
| Set Color | Changes the color of the button. |
| Visible | Sets the visibility of the button. Value should either be true or false. |

</div>
<div class="column row-container">
<img src="/images/help/button/button_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Output Events
| Event | Description |
| ----- | ----------- |
| Pressed | Sends the **Value On** value to the configured client channel. |

</div>
<div class="column row-container">
<img src="/images/help/button/button_output_pressed.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Output Events
| Event | Description |
| ----- | ----------- |
| Pressed | Sends the **Value On** value to the configured server channel. | 

</div>
<div class="column row-container">
<img src="/images/help/button/button_output_server.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
> You can make a classic Sensahub button by setting color = white, outline-color = orange strong, and text-color = black.

---
<!-- Icon Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Icon Widget

___
<div class="column-container">
<div class="column row-container" style="width:100%">


## About
The Icon widget is like the button widget, but instead of text, it displays an icon.

</div>

<div class="column row-container">
<img src="/images/help/icon/icon.png" width="124" height="128">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Icon Properties
| Property | Description |
| -------- | ----------- |
| Form ID | An ID that groups widgets so that scripts can retrieve all the values from the grouped widgets together. |
| Form Key | Name of individual form widget used in scripting for "get" and "set". |
| Action | Either toggle or static. Static outputs the data in the "value on" field. Toggle outputs either true or false. |
| Icon File | The name of the icon to be displayed. |
| Value On | The value that is output when the button is pressed. | 
| Jump To Screen | On click, jump to the configured screen. |
| Color | The color of the icon. | 
| Outline Color | The outline color around the icon. | 
| Hover | The color of the icon when hovered over. |

</div>
<div class="column row-container">
<img src="/images/help/icon/icon_specific.png" width="150" height="245">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive Value | Changes the displayed icon file. |

</div>
<div class="column row-container">
<img src="/images/help/icon/icon_client_input.png" width="150" height="176">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Output Events
| Event | Description |
| ----- | ----------- |
| Pressed | Publishes the data in "value on" to the selected client channel when the icon button is pressed. |

</div>
<div class="column row-container">
<img src="/images/help/icon/icon_client_output.png" width="150" height="172">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Output Events
| Event | Description |
| ----- | ----------- |
| Pressed  | Publishes the data in "value on" to the selected server channel when the icon button is pressed.​ |

</div>
<div class="column row-container">
<img src="/images/help/icon/icon_server_input.png" width="150" height="189">
</div>
</div>

Click <a href="https://google.com" target="_blank" title="API Info">here</a> for more detailed API information.

#### Tips
>This widget fits best into forms as an intuitive button, such as a save icon to save data from a form into a database, or a trash icon to delete data from a database.

>Available icons and their names can be found <a href="https://icons.getbootstrap.com" target="_blank" title="Available Icons">here</a>

---
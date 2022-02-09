<!-- Label Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Label Widget

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The Label widget is used to display text on the screen. Click on the text to edit it, and use the popup menu to format the text. The label can also display client and server values by using [#] as a substitution string. For example, if a Label "Value: [#]" is sent a client event with the data "25", the Label becomes "Value: 25".

To edit the text of the Label, click once on the label text. Use the arrow keys to move the cursor position.

To move the Label around, click and hold the mouse down on it while dragging the mouse.
</div>

<div class="column row-container">
<img src="/images/help/label/label.png" width="220" height="120">
</div>
</div>

___


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Label Properties
| Property | Description |
| -------- | ----------- |
| Font Size | Change the size of the font inside the text box. | 
| Text Align | Select how the text will align from a dropdown menu; Left, Centre or Right. |
| Last Seen | Display the date/time when channel data was last seen. Use a [#] for substitution. |
| Decimals | Select how many decimal places to be shown, leave blank for all places. |
| Color | Sets the color of the label text. |

</div>
<div class="column row-container">
<img src="/images/help/label/label_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Set Color | Sets the color of the text from an data stream.  |
| Receive Value | Is the data stream containing a value sent from a client output event. | 

</div>
<div class="column row-container">
<img src="/images/help/label/label_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Events
| Event | Description |
| ----- | ----------- |
| Feed | Is the data stream directed from the server channel. |

</div>
<div class="column row-container">
<img src="/images/help/label/label_server_input.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
>When substituting server or client data make sure the widget bounds are large enough for the expected text (use the drag handles to expand the label sizing if needed).

>Font size setting is different and not compatible with heading size. The heading size buttons change the text into different heading sizes for the selected text, and the font size changes the entire text.

>The delete key isn’t used for deleting text when editing the label text, it is used to delete the label widget. Use the backspace key to delete text when editing.

>To change text color, click the color swatch to rotate through available colors. Select the text you want to color, then press the ‘c’ button to color the text with the color previously set.

---
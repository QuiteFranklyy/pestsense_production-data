<!-- Text Area Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Text Area Widget

___
<div class="column-container">
<div class="column row-container" style="width:85%">


## About
The Text Area widget is able to display large amounts of text, such as detailed descriptions or instructions. It can also be used as an input to save or export larger amounts of text.

</div>

<div class="column row-container">
<img src="/images/help/textarea/textarea_instructions.png" width="200" height="140">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Text Area Properties
| Property | Description |
| -------- | ----------- |
| Form ID | An ID that groups widgets so that scripts can retrieve all the values from the grouped widgets together. |
| Form Key | Name of individual form widget used in scripting for "get" and "set". |
| Tab Index | The order of the widgets being selected when tabbing through. |
| Editable | Let's the user edit the text or not. |
| Enable Label | Displays a label above the text area. | 
| Bold | Emboldens the label. |
| Use Widget Name | Sets the label to the widget name text. |
| Label Text | Custom label text. |
| Color | The color of the text. |
| Placeholder| Text that appears in the box when empty. |

</div>
<div class="column row-container">
<img src="/images/help/textarea/textarea_widget_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Type | Description |
| ----- | ---- | ----------- |
| Receive Value | Client | Sets the text area text to the received text. |
| Append Value | Client | Appends the received text onto the end of the text area. |
| Clear | Client | Removes all of the text in the text area. |
| Submit | Client | Causes the send value event to run and clears the text area. |

</div>
<div class="column row-container">
<img src="/images/help/textarea/textarea_even_receive.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Output Events
| Event | Type | Description |
| ----- | ---- | ----------- |
| Send Value | Client | Sends the text in the text area to the client channel. |

</div>
<div class="column row-container">
<img src="/images/help/textarea/textarea_event_feed.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Sever Input Events
| Event | Type | Description |
| ----- | ---- | ----------- |
| Feed | Server | Is the data stream directed from the server channel. | 

</div>
<div class="column row-container">
<img src="/images/help/textarea/textarea_event_send.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
>The text area is convenient for quickly adding instructions for end users.

---
<!-- Dropdown Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Dropdown Widget

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The dropdown widget is a visual method for parameter selection. The default dropdown items can be edited and set through client and server events. The dropdown widget can also output the currently selected value.


</div>

<div class="column row-container">
<img src="/images/help/dropdown/dropdown.png">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:90%;">

## Dropdown Properties
| Property | Description |
| -------------- | ----------- |
| Form ID | An ID that groups widgets so that scripts can retrieve all the values from the grouped widgets together. |
| Form Key | Name of individual form widget used in scripting for "get" and "set". |
| Tab Index | The order of the widgets being selected when tabbing through. |
| Fire on Load | Fires the output event when the page is loaded. |
| Disable edit | Toggles whether text can be typed into the dropdown, or whether options can only be selected. |
| Disable spellcheck | If editing is not disabled, the text typed into the dropdown box will not be spellchecked. |
| Default Value | The value that is displayed in the text area of the dropdown widget by default. |
| Default Options | The options that are available in the dropdown widget by default. |
| Default Option Values | Each option has a relevant value related to it, ie the option may be "Yellow", but the value is "1". |
| Validate Pattern. | Use regular expressions to ensure the correct input. If the input validates as incorrect, an error message is displayed (customisable in the invalid message setting). | 
| Invalid Message | The message displayed in the banner when an invalid value is entered. |
| Dirty on Change | Set a dirty flag when the dropdown value is changed. |
| Enable Label | Enable a label to appear above the dropdown. |
| Bold | Make the label bold. |
| Use Widget Name | Use the widget name as the label. |
| Label Text | Set custom label text. |
| Color | Set the color of the dropdown. |
| Placeholder | Ghost value displayed when the dropdown is empty. |

</div>
<div class="column row-container">
<img src="/images/help/dropdown/dropdown_widget_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:95%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive Value | Sets the selected option to the value from the event, but it does not add the option to the list. |
| Receive list | Sets the available options to an array of values input from the event. |
| Receive Text Values | Sets the available options with an array of text and values pairs. |
| Append List | Adds more options onto the end of the current options, can be single value or array. |
| Reset Default | Resets dropdown to default value. |

</div>
<div class="column row-container">
<img src="/images/help/dropdown/dropdown_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Output Events
| Event | Description |
| ----- | ----------- |
| Selected | Outputs the selected option. |

</div>
<div class="column row-container">
<img src="/images/help/dropdown/dropdown_client_output.png">
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
<img src="/images/help/dropdown/dropdown_server_input.png" width="150" height="191">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
> The dropdown is most useful in forms where a user should only select from a pre-defined list of options.

---
<!--Input Types Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Input Widget

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The input widget is a way to directly input data into the application with various input types.

<br/>

The input widget has many types, allowing many kinds of inputs and outputs, which are explained in this slide. The Client Output event will output data according to the type of input widget.


</div>

<div class="column row-container">
<img src="/images/help/input/input.png" width="206" height="96">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Input Properties
| Property | Description |
| -------- | ----------- |
| Form ID | An ID that groups widgets so that scripts can retrieve all the values from the grouped widgets together. |
| Form Key | Name of individual form widget used in scripting for "get" and "set". |
| Required | Will display a red asterix to indicate that this field is required when empty. |
| Validate Pattern | Validate that the input is the same as some pattern. |
| Invalid Message | The message that is output if the input text did not pass validation. |
| Type | The type of data that is expected to be input. |
| API Key | Google API key for using the address type. The Places API and Maps Javascript API must be enabled on this key |
| Default Value | Default value that is in the input field on startup. |
| Tab Index | Keyboard TAB order when moving between form fields. |
| Dirty on Change | Warn if moving away when changes are not saved​. |
| Checkbox Label Side​ | Left or Right side of the checkbox to display label. |
| Disable Editing | Disables the ability to edit the text. |
| Disable Spellcheck | Disables the spellcheck, no more red squiggles. |
| Use Full Address | Enables the address type to output an object containing all the address information. |
| Enable Label | Enables a label placed above the widget. |
| Bold | Emboldens the label. |
| Use Widget Name | The label will use the name of the widget. |
| Label Text | The label will use custom text entered here (must deselect "use widget name"). |
| Color | The color of the text. |
| Placeholder | Placeholder text that disappears once text is input into the field. |

</div>
<div class="column row-container">
<img src="/images/help/input/input_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:63%;">

## Input Types
| Property | Description |
| -------- | ----------- |
| Text | Outputs the text written in the input. |
| Date | Outputs the date in the format: yyyy-mm-dd. |
| Time | Outputs the time in 24-hour format: hh:mm |
| Checkbox| Outputs true or false depending on whether it has been checked or not. |
| Colour | Outputs the hexadecimal colour value. | 
| Number | Outputs the number written in the input. | 
| Email | Outputs the email written in the input. |
| Password | Outputs the text of the password written in the input. | 
| File | Outputs the location of the file (not yet implemented). |
| Phonenumber | Outputs the phonenumber written in the input. |
| Address | Outputs the address written in the input or selected from the predictions. | 

</div>
<div class="column row-container">
</div>
</div>

<br>

<img src="/images/help/input/input_types.png" width="150" height="200">

<br>

<img src="/images/help/input/input_types2.png" width="150" height="200">

<br>

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive value  | Displays the data received from a client event. |
| Change Scope | Change Scope. |
| Set Conutry | Sets the country for the Phonenumber and Address types. If the type is phonenumber, it will change the flag and dial code accordingly. If the type is address, it will limit the search predictions to the given country. |

</div>
<div class="column row-container">
<img src="/images/help/input/input_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Output Events
| Event | Description |
| ----- | ----------- |
| Pressed | Registers when the input widget is clicked. |
| On change  | Registers when the value is changed. |

</div>
<div class="column row-container">
<img src="/images/help/input/input_client_outup.png">
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
<img src="/images/help/input/input_server_input.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
>Forms, login screens, and detailed reports can be created from the large number of input types

>Create a dropdown for country selection and use the *Set Country* Client Input Event to limit search predictions.

>Enable the *Use Full Address* property if you want to make a form where the different address components are in separate input boxes. Use a **Scripting** Widget to parse the object given from a Client Event and automatically fill out the form.
---
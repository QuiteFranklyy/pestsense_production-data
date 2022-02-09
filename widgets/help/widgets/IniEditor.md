<!-- InEditor Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# IniEditor Widget

___

<div class="column-container">
<div class="column row-container" style="width:70%">


## About
Allows initialisation files to be edited by the user.

</div>

<div class="column row-container">
<img src="/images/help/ineditor/ineditor.png" width="89" height="88">
</div>
</div>

___

<div class="column-container">
<div class="column row-container">
<div class="row">

## InEditor Properties Not Applicable

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive Value | Sets the value of the IniEditor to the received value. |
| Get Value | Gets the value of a settings ini
| Save | Rises an event when saving the ini file
| Close | Rises an event before closing the editor

</div>
<div class="column row-container">
<img src="/images/help/ineditor/ineditor_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Events
| Event | Description |
| ----- | ----------- |
| Feed | Is the data stream directed from the server channel. The value of the IniEditor is set to value received from the server. |

</div>
<div class="column row-container">
<img src="/images/help/ineditor/ineditor_server_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Output Events
| Event | Description |
| ----- | ----------- |
| Save | Saves the changes. |

</div>
<div class="column row-container">
<img src="/images/help/ineditor/ineditor_server_output.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.


#### Tips
>

---
<!-- Jsonparser Widget Help Markdown -->
<br>

# JSON Parser Node

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The JSON Parser node allows incoming data to be parsed out into different flow streams. A JSON parser is configured with a single JSON key name, when data is received it gets and outputs the value related to the JSON key.

</div>

<div class="column row-container">
<img src="/images/help/jsonparser/jsonparser_main.png" width="104" height="90">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:100%;">
<div class="row">

## Jsonparser Properties
| Property | Description |
| -------- | ----------- |
| Field Name | JSON key name to strip out value and pass to next node. | 



</div>
 
</div>

<div class="column row-container">
<div class="row">
<img src="/images/help/jsonparser/jsonparser_specific.png" width="170" height="414">
</div>
</div>
</div>

#### Tips
> Using multiple JSON Parser nodes, all of the values of incoming JSON packets can be sent to different flows to be processed or saved.

---
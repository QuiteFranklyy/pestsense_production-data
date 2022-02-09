<!-- Barcode Scanner Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Barcode Scanner Widget

___
<div class="column-container">
<div class="column row-container" style="width:250%">


## About
Barcode Scanner widget shows multiple data sources where each segment represents a percentage of the total of all values. It is recommended to use only server events, but client events can be implemented. It requires server events to be set up for client events to work, and the name that is displayed on the barcodescanner is set by changing the name of the server event. An example at the bottom of the page steps through how to do this.

</div>

<div class="column row-container">
<img src="/images/help/barcodescanner/barcodescanner.png" width="160" height="150">
</div>
</div>

___

## Barcode Scanner Properties

The Barcode Scanner widget does not have any properties.

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
|-------|-------------|
| Activate | Activates the barcode scanner. When it first loads, it is not activated. |

</div>
<div class="column row-container">
<img src="/images/help/barcodescanner/barcodescanner_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Output Events
| Event | Description |
|-------|-------------|
|Detected | When a barcode is detected, it will send the numerical value of the scanned barcode.|

</div>
<div class="column row-container">
<img src="/images/help/barcodescanner/barcodescanner_client_output.png">
</div>
</div>


Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
> This widget is best used on a phone camera due to the picture quality determining if a barcode can be scanned or not.​

> Use this widget to identify your devices, so you can scan a device in the field, and it immediately brings up all of the information about that device.

---
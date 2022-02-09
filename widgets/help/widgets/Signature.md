<!-- Signature Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Signature Widget

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The Signature Widget provides a way to write and save signatures. It can be used on both the phone and desktop versions of the application.
 

</div>

<div class="column row-container">
<img src="/images/help/signature/signature.png" width="180" height="65">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Signature Properties
| Property | Description |
| -------- | ----------- |
| Background Color | Sets the background color of the signature canvas. |
| Pen Color | Sets the color of the signature stroke. |
| Border Color | Sets the border color of the signature canvas. |
| Stroke Enabled | Sets whether the user can draw on the signature widget by default. |
</div>
<div class="column row-container">
<img src="/images/help/signature/signature_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Set Value | Receives a signature from an event, and displays it on the canvas. |
| Enabled | Either enables or disables the ability to draw on the signature widget. |
| Clear Content | Clears the signature widget. |

</div>
<div class="column row-container">
<img src="/images/help/signature/signature_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Output Events
| Event | Description |
| ----- | ----------- |
| Changed | Outputs the current image equivalent of the signature widget. |

</div>
<div class="column row-container">
<img src="/images/help/signature/signature_client_output.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Events
| Event | Description |
| ----- | ----------- |
| Feed | Feed is the data stream directed from the server channel. |

</div>
<div class="column row-container">
<img src="/images/help/signature/signature_server_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Output Events
| Event | Description |
| ----- | ----------- |
| Changed | Outputs the current image equivalent of the signature widget. | 

</div>
<div class="column row-container">
<img src="/images/help/signature/signature_server_output.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
>The Signature Widget is best used in forms where you need to verify the identity of a person.

---
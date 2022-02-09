<!-- Radial Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Radial Widget

___
<div class="column-container">
<div class="column row-container" style="width:75%">


## About
The Radial widget is a simple way of displaying 2 sets of data for comparison. A good use for this widget is expected or target data, and actual data so that the current performance can be measured against expected performance.​

</div>

<div class="column row-container">
<img src="/images/help/radial/radial.png" width="160" height="150">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Radial Properties
| Property | Description |
| -------- | ----------- |
| Inner Color | Change the color of the inner circle. |
| Inner Max |  Set the maximum for the inner circle. | 
| Outer Color | Change the color of the outer circle. |
| Outer Max | Set the maximum of the outer circle. |

</div>
<div class="column row-container">
<img src="/images/help/radial/radial_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Set Inner Circle | sets the value of the inner circle.
|Set Outer Circle | Sets the value of the outer circle.

</div>
<div class="column row-container">
<img src="/images/help/radial/radial_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Output Events
| Event | Description |
| ----- | ----------- |
| Pressed | Registers when the widget is clicked on.

</div>
<div class="column row-container">
<img src="/images/help/radial/radial_client_output.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Events
| Event | Description |
| ----- | ----------- |
| Inner circle  | Sets the inner circle value from a server data stream. |
| Outer circle  | Sets the outer circle value from a server data stream. |
| Feed | is the data stream directed from the server channel. |

</div>
<div class="column row-container">
<img src="/images/help/radial/radia_server.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
>The radial widget is very simple, so adding a text area or a label explaining the data it is displaying will improve the user experience

---
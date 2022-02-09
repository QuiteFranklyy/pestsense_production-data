<!-- Wind Speed Widget Help Markdown -->
<br>

# Wind Speed Widget

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The Wind Speed widget is a visual indication of the wind speed, displaying a wind turbine that spins. The higher the input value, the faster the wind turbine spins.

</div>

<div class="column row-container">
<img src="/images/help/windspeed/windspeed.png" width="115" height="127">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Wind Speed Properties
| Property | Description |
| -------- | ----------- |
| Ratio | The input value is multiplied by this ratio, and the result is used to spin the wind turbine. |

</div>
<div class="column row-container">
<img src="/images/help/windspeed/windspeed_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive Value | Sets the value of the wind speed widget to the received value. |

</div>
<div class="column row-container">
<img src="/images/help/windspeed/windspeed_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Events
| Event | Description |
| ----- | ----------- |
| Feed | Is the data stream directed from the server channel. The value of the wind speed widget is set to values received from the server.

</div>
<div class="column row-container">
<img src="/images/help/windspeed/windspeed_server_input.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
>The wind speed widget can use the ratio property to either speed up or slow down the windmill based on the input.

>An example use is letting the user know if the weather conditions are good for boating.

---
<!-- Water Tank Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Water Tank Widget

___
<div class="column-container">
<div class="column row-container" style="width:110%">


## About
The Water Tank widget is primarily used to display the level of water in a tank but can be used for other purposes.


</div>

<div class="column row-container">
<img src="/images/help/water_tank/water_tank_main.png" width="120" height="120">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Water Tank Properties
| Property | Description |
| -------- | ----------- |
| Range | Set the range of the input, ie if range is 50 and input is 50, the water tank will display 100%. |
| Decimals | Set the number of decimals that are displayed. |
| Font Size | Change the size of the font inside the text box. | 

</div>
<div class="column row-container">
<img src="/images/help/water_tank/water_tank_widget_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Type | Description |
| ----- | ---- | ----------- |
| Receive value  | Client | Sets the value that the water tank displays. |

</div>
<div class="column row-container">
<img src="/images/help/water_tank/water_tank_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

##  Server Input Events
| Event | Type | Description |
| ----- | ---- | ----------- |
| Feed | Server | Sets the displayed value to the most recent value given by the server. |

</div>
<div class="column row-container">
<img src="/images/help/water_tank/water_tank_server_input.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
>This widget can be used to display the fill level of gas tanks, oil tanks, silos, anything that you might want to know the % fill level.

---
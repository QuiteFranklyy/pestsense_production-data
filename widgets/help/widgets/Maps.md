<!-- Map Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Map Widget

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The Map widget is used to generate a Map through Google Maps API key. You can modify it with latitude, longitude set up the zoom and set up custom pop ups that display on the map.

</div>

<div class="column row-container">
<img src="/images/help/map/map.png" width="120" height="120">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Map Properties
| Property | Description |
| -------- | ----------- |
| API Key | Registered Google Maps API key. |
| Latitude | Latitude to centre map on. |
| Longitude | Longitude to centre map on. |
| Zoom | Map zoom level. The larger the number, the more zoomed in the map becomes. |
| Type | Type of map to be displayed; either roadmap, satellite, hybrid, or terrain. |
| Display POIs | Toggle whether default points of interest are displayed on the map. |
| Display Info On |  |
| History | Amount of history (in hours) to retrieve. |
| Clustering Size |  |

</div>
<div class="column row-container">
<img src="/images/help/map/map_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive Value | Sets the value of the map to the received value. |
| Add Custom Popup | Sets a custom popup using an popup template. |
| Remove Custom Popup | Removes a popup. |
| Set Map | Initializes the map with custom settings. |
| Set Zoom | Set the zoom level of the map. The larger the number, the more zoomed in the map becomes. |
| Clear Map | Clears the map and reverts to default settings. |
| Open Window |  |
| Draw Line |  |
| Remove Line |  |

</div>
<div class="column row-container">
<img src="/images/help/map/map_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Output Events
| Event | Description |
| ----- | ----------- |
| Pressed | Sends an activation message to the server channel it is connected to.  |
| Custom Popup Pressed | returns the bound data of the clicked custom popup. |
| Custom | Creates a custom popup output. |

</div>
<div class="column row-container">
<img src="/images/help/map/map_client_output.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Events
| Event | Description |
| ----- | ----------- |
| Feed | Is the data stream directed from the server channel. The value of the map is set to value received from the server. |

</div>
<div class="column row-container">
<img src="/images/help/map/map_server_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Output Events
| Event | Description |
| ----- | ----------- |
| Pressed | Publishes to a channel that the map has been clicked. |
| Custom | Publishes to a channel that a custom popup has been clicked. |

</div>
<div class="column row-container">
<img src="/images/help/map/map_server_output.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
>

---
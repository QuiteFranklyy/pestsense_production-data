<!-- Compass Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Compass Widget

---
<div class="column-container">
<div class="column row-container" style="width:120%">


## About
The Compass can be used to display a geographical heading. Note that it does not act like a standalone compass, it simply displays values that are sent to it.

</div>

<div class="column row-container">
<img src="/images/help/compass/compass.png">
</div>
</div>

---



## Compass Properties

The compass does not have any properties.

<br/>

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive Current | Sets the direction of the compass
| Receive Average |  Sets the average position of the compass

<br>

> Compass only accepts ordinal values, ie SW (south-west) or ENE (East north-east)

</div>
<div class="column row-container">
<img src="/images/help/compass/compass_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:76%;">

## Server Input Events
| Event | Description |
| ----- | ----------- |
| Feed | Is the data stream directed from the server channel. The value of the compass is set to value received from the server. |

</div>
<div class="column row-container">
<img src="/images/help/compass/compass_server_input.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
> It has applications in the agricultural sectors and can be combined with different widgets eg. Water Tank, Wind Speed and others, to create complex systems.


---
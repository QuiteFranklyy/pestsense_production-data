<!-- Clock Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Clock Widget

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The Clock widget is used primarily to display time. It can display time in either analogue or digital form, and it can also be configured to display the date.


</div>

<div class="column row-container">
<img src="/images/help/clock/clock.png">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Clock Properties
| Property | Description |
| ----- | ----------- |
| Type | The type of clock displayed, analogue or digital. Another option is to display the date. |
| Timezone GMT | Set the time zone that the clock widget will use to determine the current time. |
| Color | The color of the clock widget. |

</div>
<div class="column row-container">
<img src="/images/help/clock/clock_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive Value | Sets the value of the clock to the received value. |

</div>
<div class="column row-container">
<img src="/images/help/clock/clock_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Output Events
| Event | Description |
| ----- | ----------- |
| Pressed | Activates when the clock is clicked on. It sends the current time to the configured client channel. |

</div>
<div class="column row-container">
<img src="/images/help/clock/clock_client_output.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Events
| Event | Description |
| ----- | ----------- |
| Feed | Is the data stream directed from the server channel. The value of the clock is set to values received from the server. |

</div>
<div class="column row-container">
<img src="/images/help/clock/clock_server_input.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
> This widget is a must have for all dashboards, displaying the time is a basic yet essential piece of information all users can benefit from.

---
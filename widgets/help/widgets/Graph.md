<!-- Graph Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Graph Widget

___
<div class="column-container">
<div class="column row-container" style="width:150%">


## About
The graph widget is used to display a large amount of historical data. It can be used to display multiple channels simultaneously.
The graph is updated in real time with new incoming data points.

</div>

<div class="column row-container">
<img src="/images/help/graph/graph_chart.png"/>
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Graph Properties
| Property | Description |
| -------- | ----------- |
| Axis Labels | Change the text of the axis labels. |
| Line Type | Display the line with smoothing, steps, or linear. |
| Compression | Enables data compression for better display of large amounts of data. When compression is enabled, it will always attempt to compress the data. If enabled, you are unable to download the data. |
| History Timespan | The length of time displayed on the graph in hours. |
| Title | Change the text of the graph title. |
| Enable Legend | Displays a legend of the displayed data. |
| Only Accept Data From My Events | Data will only be received if it comes from server input events created by this widget. This ignores data received for other widgets on the same channel.|
| Enable Zoom | Displays a slider underneath the main graph that allows for zooming in and out of the graph. |
| Disable Feed | Prevents the graph from being updated while displayed, refreshing the page updates the data. |
| Custom Domain | Set these values to display data between these domains on the y axis. |
| Download Data Button | Download a CSV with all of the data displayed in the graph. |

</div>
<div class="column row-container">
<img src="/images/help/graph/Graph_details.png"/> 
</div>
</div>

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Event
| Property | Description |
| -------- | ----------- |
| Set X Axis Interval | Sets the time interval over which the data is displayed, ie: Minute, Hour, 4 hour, 8 hour, 12 hour, Day, Week, Month, Year |
| Reload | Graphically reloads the graph. |
| Set All Scopes | Change the scope of the server input channels, making the graph display the data of the new channel scope. | 
| Set All Instances | Change the instance of the server input channels, making the graph display the data of the new channel instance. |
| Set Graph Range | Sets the start and end range, making the graph only display data between these dates. This can be formatted as: yyyy-mm-dd (from start date), yyyy-mm-dd,yyyy-mm-dd (start and end date). To include hours, format as: yyyy-mm-dd:hh:mm:ss. |
| Set Threshold | Sets a threshold line at the given value. This can be formatted as: "index value color", or just "index value" with the default color as black. Index numbers start at 0. Example: 0 80 blue |
| Clear Thresholds | Removes all threshold lines. |
| Set Channel | Sets a channel for the graph to subscribe to. See the example given below for how to set this up. |

</div>
<div class="column row-container">
<img src="/images/help/graph/graph_event_set_interval.png"/>
</div>
</div>

<div class="column-container">
<div class="column row-container" style="width:150%;">

## Server Input Event
| Property | Description |
| -------- | ----------- |
| Feed | Is data stream directed from the server channel, using this option only displays data from the time the page was loaded without any history. |
| History | Is historical channel data based on the selected timespan and includes real-time feed updates. |
| Color | Change the color of the line (unique for each line).​ | 
| Area Fill | Fill the area underneath the line  (unique for each line). | 
| Fill Opacity | Area fill opacity. |

</div>
<div class="column row-container">
<img src="/images/help/graph/graph_server_event_history.png"/>
<img src="/images/help/graph/graph_color_fill.png"/>
</div>
</div>
 
 Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
> The graph is able to display up to 5 channels, but they must all be a different colour otherwise the data will not display.

> Use a dropdown to change the interval to "zoom in" on recent data.

> Hover on a data line to bring up a data cursor tooltip. 

> The tooltip will show each graph channel in color and in order of their y-axis value at the hovered position

> When compression is enabled, the graph will no longer display feed values.

> Enable the slider for dynamic zooming into the graph
<img src="/images/help/graph/graph_zoomed.png"/>

> The smaller graph in the slider only shows the first channel

> Disable **Only Accept Data From My Events** to accept data from Scripting widgets or other sources

> Threshold line colors can be provided as hexadecimal values. You could provide an input like "0 -30 #f58133"

> Setup a Scripting Widget to allow the Graph to load in new channels without setting up its own Server Events

---

# Example

It is easy enough to set the values using server events. You just set up a server input event, select the channel, name the event, and it will display the values.

However it is harder to do using just client events. In this example, we will go through how to set up a donut widget to display data given from client events.

1. Create a Graph widget with a unique name. We will call it "clientEventsGraph" for this example.

2. Create a Scripting widget.

3. Copy and paste the following code in the scripting widget:

```javascript
/**
 * Initialise script state (run once at startup)
 */
 Script.on('load', function() {
	let channel = {category: "RANDOM",
				  className: "NUMBER",
				  instance: "GRAPH",
				  scope: "LEVEL"};

	let graph = Script.getWidget("clientEventsGraph"); // use the name you called the graph
	let attribs = {"area fill":"true",
				   "color":"yellow",
				   "fill opacity": 0.2
				   };

	graph.subscribeToServer(channel, "history", attribs);
	let graphOptions = {channel: "RANDOM/NUMBER/GRAPH/LEVEL",
						options: {
							color: "yellow",
							area: true,
							opacity: 0.2
							}
					   };
	graph.setChannel(graphOptions);
});
```

4. Save the screens and navigate to Flows.

5. Create an Interval widget and an End widget. Connect the two with a link. Connect

6. Setup the Interval with a timespan of seconds. Random Number checked and providing two numbers for Random Min and Random Max.

7. Setup the End widget with Category: Random. Class: Number. Instance: Graph. Scope: Level.

8. Save the Flows screen and navigate back to Screens.

You should see data coming into the graph as a yellow line with the area below it being shaded

---

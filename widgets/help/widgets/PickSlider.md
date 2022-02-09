<!-- Pick Slider Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Pick Slider Widget

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The Pick Slider presents a visual way to select pre-defined values. It can receive output from the client and server, and also publish data to the client and server.
 

</div>

<div class="column row-container">
<img src="/images/help/pickslider/pickslider.png">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Pick Slider Properties
| Property | Description |
| -------- | ----------- |
| Form ID | An ID that groups widgets so that scripts can retrieve all the values from the grouped widgets together. |
| Form Key | Name of individual form widget used in scripting for "get" and "set". |
| Tick Values | Values that can be selected using the pickslider, comma separated. | 
| Default Value | The default value of the pickslider. | 

</div>
<div class="column row-container">
<img src="/images/help/pickslider/pickslider_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive Value | Sets the value of the pickslider to the received value. |

</div>
<div class="column row-container">
<img src="/images/help/pickslider/pickslider_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Output Events
| Event | Description |
| ----- | ----------- |
| Changed | Outputs the new value of the pickslider when the pickslider is moved. |

</div>
<div class="column row-container">
<img src="/images/help/pickslider/pickslider_client_output.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Events
| Event | Description |
| ----- | ----------- |
| Feed | Is the data stream directed from the server channel. The value of the pickslider is set to values received from the server. |

</div>
<div class="column row-container">
<img src="/images/help/pickslider/pickslider_server_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Output Events
| Event | Description |
| ----- | ----------- |
| Changed | Outputs the value of the pickslider when the pickslider is moved. When used in conjunction with feed, you can see and change the server value of the pickslider. | 

</div>
<div class="column row-container">
<img src="/images/help/pickslider/pickslider_server_output.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
> The pickslider can be used to select qualitative values visually, like the lighting of a room: white, warm, cool etc.

---
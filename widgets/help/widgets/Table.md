<!-- Table Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Table Widget

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The Table widget is a feature-rich data-focused widget. It can display a lot of data in a more detailed way compared to the graphical methods. 

Information can be sent to the table using the scripting widget, due to the complexity of the data structure that the table requires. An example is given at the bottom of this help screen.

Rows in the table can be selected and sent using events. For example, when you click on a row, you can send an event to a text area to display the information of the currently selected row.


</div>

<div class="column row-container">
<img src="/images/help/table/table.png" width="264" height="180">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Table Properties
| Property | Description |
| -------- | ----------- |
| Form Id | An ID that groups widgets so that scripts can retrieve all the values from the grouped widgets together. |
| Form Key | Name of individual form widget used in scripting for "get" and "set". |
| Columns | The titles of the expected columns. |
| Selectable| Allows users to select rows in different ways: single means only one row can be selected, multi shows check boxes next to each row so multiple can be selected, multi + single combines these functionalities. |
| Display Header | Displays a header/title for the table. | 
| Display Column Titles | Show the column titles above the columns. |
| Enable Search | Adds a search bar on the top right, allows searching through all data in the table. |
| Color Rows | This option colors the background of the rows. |
| Row Color | The background color of the rows. |
| Auto Scroll | Automatically scrolls to new data. |
| Color On Hover | Highlights the text in a row when it is hovered over. |
| Title | The title of the table. |
| Text Color | The color of the text and data in the table. |
| Font Size | The size of the text in the table. |

</div>
<div class="column row-container">
<img src="/images/help/table/table_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:90%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive Value | Adds a row to the table. |
| Delete Rows | Deletes some rows in the table, can take a single string or an array of strings. |
| Delete All Rows | Deletes all the rows in the table. |
| Set Text Color | Sets the text color of the text. |
| Sort Row by Array | Takes an array of primary keys, displaying only rows that equals the primary keys. |
| Sort Rows | Sorts the rows according to the column. |
| Set Title | Sets the title of the graph. |
| Highlight Row | Highlights a certain row. |
| Select Rows | Selects the rows received by this event. |

</div>
<div class="column row-container">
<img src="/images/help/table/table_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Output Events
| Event | Description |
| ----- | ----------- |
| Pressed | Sends the row that is clicked on to the event. |
| Selected | Sends the currently selected row, when a row is selected. |
| Unselected | Sends when a row is unselected. |
| Custom | Uses custom events set using the HTML widget. |

</div>
<div class="column row-container">
<img src="/images/help/table/table_client_output.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Events
| Event | Description |
| ----- | ----------- |
| Feed | Is the data stream directed from the server channel. The value of the table is set to values received from the server. |

</div>
<div class="column row-container">
<img src="/images/help/table/table_server_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Output Events
| Event | Description |
| ----- | ----------- |
| Pressed | Sends the row that is clicked on to the event. |
| Custom | Uses custom events set using the HTML widget |

</div>
<div class="column row-container">
<img src="/images/help/table/table_server_output.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
>The table has a lot of functionality, and as such requires a lot of different events. The most common events that you will use are "receive value" and "pressed". An example of how to use these events is described on the next page.

___

# Example 

<div class="column-container">
<div class="column row-container" style="width:80%;">

## About
This example uses a button, a table, a text area and a script widget to firstly populate the table with data, and then output the name and age of the selected data to the text area.
___
<br/>

## Configurations
1. Firstly, the button is simple with just a client output event, with the event type set to "pressed" and event name set to "button".
2. The scripting widget contains the code described at the bottom of this page. We firstly have a function that sends table data to the table when the button is pressed, and secondly a function that activates when the table is clicked on, sending the name and age of the selected data to the text area. Copy and paste the code into the scripting widget.
3. The table is set up according to the picture at the bottom of the page. It has a client input event, type = "receive value" and event name = "table data". It also has a client output event, type = "pressed" and event name = "table press".
4. Lastly the text area has an input event, type = "append value" and event name = "data display".
5. If everything is set up correctly, press the button and you should see the table fill with data. Then when you click on a person, their name and age will appear in the text area.

</br>

### Usage Example:

```javascript
ClientEvents.subscribe("button", function func(data){
    //Initiate the object and send it
    var send_value = {data: {"Harold": ["Harold","17"]}, headers: ["First Name","Age"], 
                     label: "sensacollection", pk: "First Name"};
    ClientEvents.publish("table data", send_value);
    send_value = {data: {"Dave": ["Dave","34"]}, headers: ["First Name","Age"], 
                     label: "sensacollection", pk: "First Name"};
    ClientEvents.publish("table data", send_value);
    send_value = {data: {"Ken": ["Ken","45"]}, headers: ["First Name","Age"], 
                     label: "sensacollection", pk: "First Name"};
    ClientEvents.publish("table data", send_value);
});
```
<br>

```javascript
ClientEvents.subscribe("table press", function func(data){
    var key = Object.keys(data.value.data);
    var array = data.value.data[key[0]];
    var name = array[0];
    var age = array[1];
    ClientEvents.publish("data display", name);
    ClientEvents.publish("data display", age);
    ClientEvents.publish("data display", JSON.stringify(data));
});
```

</div>
<div class="column row-container">
<img src="/images/help/table/example_one.png">
<br>
<img src="/images/help/table/columns.png" style="width:60%;">
<br>
<img src="/images/help/table/example_two.png">
</div>
</div>



---
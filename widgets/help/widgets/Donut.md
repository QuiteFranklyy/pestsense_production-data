<!-- Donut Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Donut Widget

___
<div class="column-container">
<div class="column row-container" style="width:75%">


## About
Donut widget shows multiple data sources where each segment represents a percentage of the total of all values. It is recommended to use only server events, but client events can be implemented. It requires server events to be set up for client events to work, and the name that is displayed on the donut is set by changing the name of the server event. An example at the bottom of the page steps through how to do this.

</div>

<div class="column row-container">
<img src="/images/help/donut/donut.png" width="160" height="150">
</div>
</div>

___

## Donut Properties

The Donut widget does not have any properties.

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive Value | Receive data from a client event. Note that it requires a server event to be set up for it to display. |

</div>
<div class="column row-container">
<img src="/images/help/donut/donut_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Events
| Event | Description |
| ----- | ----------- |
| Feed | Will set the relevant section to the value sent by the feed. |

</div>
<div class="column row-container">
<img src="/images/help/donut/donut_server_input.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
> The donut widget is very simple, so adding a text area or a label explaining the data it is displaying will improve the user experience.
> If you hover over a segment, a tooltip will popup with the value of that segment, and exactly how much of the donut it takes up out of 100%.

---

# Example

It is easy enough to set the values using server events. You just set up a server input event, select the channel, name the event, and it will display the values.

However it is harder to do using just client events. In this example, we will go through how to set up a donut widget to display data given from client events.

1. Create a Donut widget

2. Add 3 events to the Donut widget:

    Client Input:
    - Event Type: Client Input
    - Event Name: Client Value
    - Event: receive value
    - Client Channel: donut

    <br>

    Server Event 1 (Magic):
    - Event Type: Server Input
    - Event Name: Magic
    - Event: feed
    - Server Channel:
        - Category: a
        - Class: a
        - Instance: a
        - Scope: a
    
    <br>

    Server Event 2 (Science):
    - Event Type: Server Input
    - Event Name: Science
    - Event: feed
    - Server Channel:
        - Category: b
        - Class: b
        - Instance: b
        - Scope: b

<br>

3. Create a Scripting widget

4. Copy and paste the following code in the scripting widget:

```javascript
/**
 * Initialise script state (run once at startup)
 */
Script.on('load', function() {
    var magic_data = {"channel": "a/a/a/a", "data": {"value": 50}};
    ClientEvents.publish("donut", magic_data);
    
    var science_data = {"channel": "b/b/b/b", "data": {"value": 150}};
    ClientEvents.publish("donut", science_data);
});
```

In order to publish client data to a donut, you have to know the server channel that it is connected to. You put this channel into an object assigned with the key "channel". And to send the data, you have to create a key "data", and assign it an object that contains the key "value", with the relevant numerical value you want to change the donut segment to.

5. Now when you save and switch to the screen, it will populate with "Magic" and "Science", with "Magic" taking up 25% of the donut, and "Science" taking up 75% of the donut.

---
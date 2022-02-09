<!--Events-->
<br>

# Sensahub Events

---

## About
Sensahub events are data streams created from various stimulus changes like remote sensors, user input, or system events (for example: temperature change or switch activation).

These stream events are time based and used as the basis for data handling and manipulation in Sensahub processing and for display in sensahub applications.

---

### Server Events

+ Created within the server.

+ Events generated from sensors, outside sources, server processes and processing flows.

+ Can be used with server-side processing (flows) as well as client-side widgets.

<br>

### Client Events

+ Created within the client.

+ Events generated from user input and other widgets.

+ Used within a client application to display and manipulate data.

+ Define application behaviours (for example: a slider widget can adjust the time range of a graph widget).

<br>

> Events **generated** by a widget or a flow are *output events*.
> Events **consumed** by a widget or a flow are *input events*.

<br>

### Examples

+ A user selecting an item from a dropdown widget within a Sensahub application would generate a *client-based output event*.

+ A widget that recieves data from the dropdown widget within the application is a *client-based input event*.

+ A widget that recieves data from the server would be a *server-based input event*.

<br>

---
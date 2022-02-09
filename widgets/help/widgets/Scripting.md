# The Scripting Widget
## About
The scripting widget is one of the most powerful widgets in Sensahub and is available in both 'Design' and 'Flows'. Scripting can often be seen as a middle-man between the server and client events. The most common use-case of the widget is to ability to easily reformat, manipulate, and extract data from channels and pass them on to other widgets or flow nodes. This is most commonly used for other widgets such as the table and maps. 

There are two types of modes for scripting: Design and Flows. Design mode is run in the client's web browser allowing the designer to manipulate data, create HTML templates, and control events. In flow mode, scripting offers a similar experience however it is more limited due to the server. These two modes share a common API for simplicity.

### HTML Templates (Design Mode)
In design mode the scripting widget supports the use of HTML by selecting HTML in the attributes section of the widget. This allows users to create HTML templates that can be later accessed in another script for manipulation. See the API guide below for further details.
The scripting widget also allows you to use HTML templates that can be then injected into other widgets such as map pins and table rows.

#### The EventData Packet Structure in Design:
  The EventData packet structure

## Scripting API
Scripting has a number of events that can be used in the client. These functions work using the _Scripting_ library outlined below:

### Transforming Data in Design
Often data between widgets needs to be reformatted. This commonly seen between the Table and Maps widget due to their unique packet structure. To make this easier Scripting has a ``` Scripting.sendToWidget() ``` function that allows the designer to send data to other widget's local events.

| Function | Mode | Description |
|----------|------|-------------|
| ```Scripting.sendToWidget(String widgetID, String widgetEvent, Object value) ```| Design | Send data directly to another widget and run the widgets event. The widget but be on the same page. Different widgets require different object types making Scripting on the client a great middleman widget for transform data between widgets. |

&nbsp;
### Script Events
Scripting has a number of events that are fired off throughout the lifetime of the widget. These are:

```javascript
Script.on(event, callback)
```
| Function | Mode | Description |
| -------- | ---------|-------------|
| ``` Script.on('load', callback) ``` | Flows and Design | Callback is fired once the widget has successfully loaded in the dashboard. |
| ``` Script.on('client', callback) ``` | Design | Callback is fired when a client event is received. The callback takes an eventData param |
| ``` Script.on('server', callback) ``` | Design |Callback is fired when a server event is received. The callback takes an eventData param |
| ``` Script.on('flow', callback) ``` | Design | Callback is fired when a new flow event occures. The callback takes an eventData param. |
| ``` Script.on('database', callback) ``` | Design | Callback is fired when a db event is received. the callback takes an eventData param |
| ``` Script.on('keypress', callback) ``` | Design | Callback is fired when a keypress occures. The callback takes a keycode param. |

&nbsp;
#### Usage Example:
```javascript
Script.on('load', function() {
    console.log('Loaded!');
});

Script.on('client', function(eventData) {
   console.log(eventData.value); 
});

Script.on('server', function(eventData) {
   console.log(eventData.value); 
});

Script.on('database', function(eventData) {
	console.log(eventData.value);
});

Script.on('keypress', function(keypress) {
    console.log(keypress.keyCode);
});
```

&nbsp;
### Working with HTML Templates
You are able to retreive the HTML and javascript stored in another script widget through Scripting's API. Once you have done this, you are able to change modify the HTML using custom Script APIs listed below:
The Scripts below will fail if the Script widget in which you are retrieving HTML from is not valid HTML.

| Function | Description |
| -------- | ----------- |
| ``` Script.getScriptElement(string name) ``` | Returns the code from the given names scripting widget. |
| ``` Script.findChildById(string id) ``` | Find a child element in a given HTML element. This element is normally retreived from another Script widget. |

&nbsp;
### Usage Example
Using a template, dynamically create a card with different titles that will be displayed inside of the table widget. 
This example creates a card that has a unique name and content. An event is fired back to the scripting widget if the buttons on the card template are pressed.
This example can easily be adapted to work with map pins.

``` javascript
// Another Script widget named 'card' has a HTML template.
var names = ["Daniel", "Elijah", "Dean"];
var cont = ["hello", "world", "test"];
var template = Script.getScriptElement("card");

Script.on('load', function() {
    var packet = {};
    for (var i = 0; i < 3; i++) {
        // Template must be placed into another HTML element.
        var doc = document.createElement("div");
        // Clone template as we don't want modify it.
        var item = template.cloneNode(true);
        var dataPacket = {name: names[i], content: cont[i]};
        // Store Information in template tags
        item.setAttribute("data-packet", JSON.stringify(dataPacket));
        // Events added to items in template must be on the 'custom' type.
        item.setAttribute("onclick", 'fw.fireEvent("custom", this.getAttribute("data-packet"))');
        // Find elements to change values of in template.    
        Script.findChildById(item, "name").innerHTML = names[i];
        Script.findChildById(item, "content").innerHTML = cont[i];
        doc.appendChild(item);
        // Send string to table.
        packet[i] = { page: doc.innerHTML};
    }
    // Send packet to page widget.
    Script.sendToWidget("page", "receive value", packet);
});
```

&nbsp;
### State Management
Scripting has the ability to do global state management. State management can be used to manage state between both scripts and screens and can be combined with script events.

| Function |  Mode | Description |
| -------- | ----- | ----------- |
| ``` Script.setState(Object key, Object value) ``` | Design and Flows | Set the state of a given key for access later from another script or screen. |
| ``` Script.getState(Object key) ``` | Design and Flows | If State for the key has not been set then the function will return null. |
| ``` Script.subscribeToState(Object stateKey, function fn) ``` | Design | Subscribe to a variable in the Scripting statestore. Everytime the variable is changed under the given stateKey the given function will be run. |
| ``` Script. unsubscribeFromChannel(Object stateKey) ``` | Design | Unsubscribe from a given stateKey. This will stop running the function. |

&nbsp;
#### State Store Usage Example
```javascript
// Set state store value with key "Hello". This can be any object.
Script.setState("Hello", "World");
var value = Script.getState(key);
// value = "world"

Script.subscribeToState("Hello", print);
// OR
Script.subscribeToState("Hello", function() {
    console.log("Do something!");
});

/* Change variable. */
Script.setState("Hello", "Changed");
// Console output: "Do something!".

Script.unsubscribeFromState("Hello");
Script.setState("Hello", "World");
// Function does not run.

/* Function to attach to state. */
function print() {
    console.log("Do something!")
}
```

&nbsp;
### Accessing Databases
Reading and writing to a database plays an important role in application development. This is available in both Design and Flow mode however it is recommended that database writes are kept mostly in the Flow mode wherever possible. These functions can be accessed in the _Database_ library.

Some common input variables are:


| Variable | Type | Description |
|--|--|--|
| dbName | String |  Database name that the table will be located in. |
| tableName | String | Table in given table to access |
| pk | String | The record primary key. |
| columnFilter | String | Comma separated string of the columns to filter. '*' for all columns. |
| value | Database Request Object | Custom object containing the records to save to the database. Example below. |

&nbsp;
#### Database Request Object Example
For the packet to be valid to primary key must match the primary key column in the packet.

``` ts
{
  "pk1": { // Primary key value
      "col1": "colValue", // Primary key column, column value must match pk1.
      "col2": "colValue",
      .
      .
      .
     "colN": "colValue"
  },
  "pk2": {
      .
      .
      .
  }
} 
```
 
| Function | Mode | Description |
|----------|------|-------------|
| ```Database.readRecords(string dbName, string tableName, string columns, string filter, string) ``` | Design and Flows | Returns the records in the given table |
| ```Database.saveRecord(string dbName, string tableName, databaseObject value) ``` | Design and Flows | Save a record to the database. If the record is not already in the table it will be added otherwise it will be added. |
| ``` Database.updateRecord(string dbName, string tableName, databaseObject value) ``` | Design and Flows  | Updates a record already in the given table. If the record does not exist it will fail. Use ``` Database.saveRecord ``` if you wish to add record if it doesn't exist. |
| ``` Database.deleteRecord(string dbName, string tableName, string columnFilter, string of databaseObject record) ``` | Design and Flows | Remove a record in the given table. |

&nbsp;
#### Database Examples
Please note that 'Examples' is not a real database.
``` javascript
// Get all columns of the record with pk = "1" From Test database in the 'Users' Table
var record = Database.readRecords("Example", "Users", "*", "Field1 = 1");

// Get 'Field2' of all records from a table.
var allRecords = Database.readRecords("Example", "Users", "Field2");

// Save a record to the database
var packet = {
    "4": { // Primary key = 4
        "Field1": "4", // Field1 is primary key column.
        "Field2": "ScriptTesting",
        "Field3": "999",
        "Field4": "999"
    }
};

Database.saveRecord("Example", "Users", JSON.stringify(packet));

// Update a record's values, Fails if the record does not exist.
Database.updateRecord("Example", "Users", JSON.stringify(json));

// Delete previous record from the Table
Databse.deleteRecord("Example", "Users", "Field1", "4");
// OR to delete many records
Database.deleteRecords("Example", "Users", "Field1", "4,5");

```

&nbsp;
### System API
The script API has access to many system functions for both the server and client scripts to use. These can be accessed in the _System_ library.

Some system functions include:

| Function | Mode | Description |
|----------|------|-------------|
| ``` System.publishToChannel(String channel, String value) ``` | Design and Flows | Publish a string value to an existing channel. If the channel successfully updates the channel it will return a boolean of ``` True ``` otherwise ``` False ``` |
| ``` System.writeLog(String message) ```| Design and Flows | Message to print back to the client (if in Design) and server console. |
| ``` System.getChannelValue(String channel) ``` | Design and Flows | Retrieve the current value of a given channel. Returns false if the channel does not exist. Channel must follow the structure of _NETWORK/CATEGORY/CLASS/INSTANCE/SCOPE_.  |
| ``` System.setDashboardOverflow(String setting) ``` | Design | Set the dashboard overflow css to add/remove scroll bars. |
| ``` System.setScreenVisible(String screenName, Boolean visible) ``` | Design | Display / hide a screen in the sidebar. |
| ``` System.jumpToScreen(String screenName) ``` | Design | Switch the dashboard screen to the screen with the given name. |
| ``` System.status(status) ``` | Design | Display a status message on the bottom bor of the screen. |

&nbsp;
### Directory API
The scipt API is able to add users to the system and change their access permissons.
```
// System permissions that users can be assigned.
System.permissions = {
    "DASHBOARD": "dashboard",
    "DESIGN": "design",
    "DEVELOPER": "developer",
    "FLOWS": "flows",
    "SETTINGS": "settings"
};
```

Directory functions are described below:

| Function | Mode | Description |
|----------|------|-------------|
| ``` Directory.addUser(String username, String password, String fName, String lName) ``` | Design | Adds a new user to the system. The user will not have any permissions meaning he will not be able to do anything in the system. A new user will also not be automatically assigned a dashboard. |
|``` Directory.addUserPermission(String username, String permission) ``` | Design | Grant a user permission to different areas of the system. |
| ``` Directory.addUserDashboard(String username, String dashboard) ``` | Design | Sets a users dashboard that they receive when logging in. |
| ``` Directory.deleteUser(String username) ``` | Design | Delete a user from the system. |


&nbsp;
### Design Patterns
When using Scripting in design mode it is recommended to split the scripts up into the Model, View, Controller design pattern while using the ``` System.setState() ``` and ``` System.subsState() ``` system calls to move information between the scripts.

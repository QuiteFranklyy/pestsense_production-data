# The Scripting Flow Node
## About
The scripting flow node is one of the most powerful widgets in Sensahub and is available in both 'Design' and 'Flows'. Scripting can often be seen as a middle-man between the server and client events. The most common use-case of the Scripting flow node is to easily reformat, manipulate, and extract data from channels and pass them on to other flow nodes.


In flow mode, functionality specific to the 'Design' mode such as client events is not supported. However, the two modes share a commmon API for simplicity.

### Script Events
Scripting has a number of events that are fired off throughout the lifetime of the node. Generically, these are called by:

```javascript
Script.on(event, callback)
```
| Function | Description |
| -------- | ----------- |
| ``` Script.on('load', callback) ``` | Callback is fired once the flows have been successfully loaded on the server. This happens on server startup, or after the flows screen has been saved.|
| ``` Script.on('flow', callback) ``` | Callback is fired when a new flow event occures. The callback takes an eventData parameter. |

<br>

#### Usage Example:
```javascript
Script.on('load', function() {
    console.log('Loaded!');
});

Script.on('flow', function(eventData) {
   console.log(eventData.value); 
});
```

In flows, the scripting widget is itself a flow node, and can therefore send data through the flows. To send data through the output of the script to the connected nodes, use ```return``` to return a value. The below example takes the input data, doubles it, and then sends it to the next connected node.

#### Usage Example:
```javascript
Script.on('flow', function(eventData) {
   console.log(eventData.value); 
   var modified_value = value * 2;
   return modified_value;
});
```

<br>

### State Management
Scripting has the ability to do global state management. State management can be used to manage state between both scripts and screens and can be combined with script events.

| Function | Description |
| -------- | ----------- |
| ``` Script.setState(Object key, Object value) ``` | Set the state of a given key for access later from another script or screen. |
| ``` Script.getState(Object key) ``` | If State for the key has not been set then the function will return null. |
| ``` Script.subscribeToState(Object stateKey, function fn) ``` | Subscribe to a variable in the Scripting statestore. Everytime the variable is changed under the given stateKey the given function will be run. |
| ``` Script. unsubscribeFromChannel(Object stateKey) ``` | Unsubscribe from a given stateKey. This will stop running the function. |

<br>

#### State Store Usage Example
```javascript
// Set state store value with key "Hello". This can be any object.
Script.setState("Hello", "World");

// Get state store value with key "Hello".
var value = Script.getState("Hello");
// value = "world"

// Run a function when the given key is updated
Script.subscribeToState("Hello", print);
// OR
Script.subscribeToState("Hello", function() {
    console.log("Do something!");
});

// Change variable.
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

<br>

### Accessing Databases
Reading and writing to a database plays an important role in application development. This is available in both Design and Flow mode however it is recommended that database writes are kept mostly in the Flow mode wherever possible. These functions can be accessed in the _Database_ library. 
Please note, currently there is no way to create a database yourself, contact a Sensahub developer for help.

Some common input variables are:

| Variable | Type | Description |
|--|--|--|
| dbName | String |  Database name that the table will be located in. |
| tableName | String | Table in given table to access |
| pk | String | The record primary key. |
| columnFilter | String | Comma separated string of the columns to filter. '*' for all columns. |
| value | Database Request Object | Custom object containing the records to save to the database. Example below. |

<br>

#### Database Request Object Example
For the packet to be valid to primary key must match the primary key column in the packet.

```json
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
 
| Function | Description |
|----------|-------------|
| ```Database.readRecords(string dbName, string tableName, string columns, string filter, string order) ``` | Returns the records in the given table |
| ```Database.saveRecord(string dbName, string tableName, databaseObject value) ``` | Save a record to the database. If the record is not already in the table it will be added otherwise it will be updated. |
| ``` Database.updateRecord(string dbName, string tableName, databaseObject value) ``` | Updates a record already in the given table. If the record does not exist it will fail. Use ``` Database.saveRecord ``` if you wish to add record if it doesn't exist. |
| ``` Database.deleteRecord(string dbName, string tableName, string columnFilter, string of databaseObject record) ``` | Remove a record in the given table. |

<br>

#### Database Examples
Please note that 'Examples' is not a real database. Also currently there is no way to create a database yourself, contact a Sensahub developer for help.
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

Database.saveRecord("Example", "Users", packet);

// Update a record's values, Fails if the record does not exist.
Database.updateRecord("Example", "Users", json);

// Delete previous record from the Table
Databse.deleteRecord("Example", "Users", "Field1", "4");
// OR to delete many records
Database.deleteRecords("Example", "Users", "Field1", "4,5");

```

<br>

### System API
The script API has access to many system functions for the server script to use. These can be accessed in the _System_ library.

Some system functions include:

| Function | Description |
|----------|-------------|
| ``` System.publishToChannel(String channel, String value) ``` | Publish a string value to an existing channel. If the channel successfully updates the channel it will return a boolean of ``` True ``` otherwise ``` False ``` |
| ``` System.writeLog(String message) ```| Message to print back to the client (if in Design) and server console. |
| ``` System.getChannelValue(String channel) ``` | Retrieve the current value of a given channel. Returns false if the channel does not exist. Channel must follow the structure of _NETWORK/CATEGORY/CLASS/INSTANCE/SCOPE_.  |

<br>

---
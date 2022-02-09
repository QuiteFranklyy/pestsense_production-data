<!--Database Information-->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Database Configuration and Usage

---

## About

A database is essential for any non-trivial application. In this document, we will go through how to edit a configuration file so that the server will build the database. Then how to put data into the database, and how to get data out of the database. Note that you will require access to the server filesystem, as well as access to the console in order to restart the server to apply the database changes.

---

### Database Configuration


<div class="column-container">
<div class="column row-container" style="width:70%;">

1. In order to make a database, first you have to define the structure of a database. We use DB Browser for SQLite to define the table.

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/database/database_edit_table.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:60%;">

2. Once that is done, right click on the table you want, and select "Copy Create statement".

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/database/copy_create_statement.png">
</div>
</div>

3. Now we need to put it into the "Database.ini. file. This file is located at "CoreServer/data/extensions/Database.ini". Open the file, and copy/paste this demo database:

Make sure to put it below the Directory, Devices, and Lookup database configurations.
This code can be reused for as many different databases as you need, just change the CREATE TABLE statement. You can also change "[demo]" to your desired database name, and edit the description.

```ini
[demo]
desc = Demo Database
dbType = SQLite
; Database location on a Windows deployment (relative to appDataRoot)
dbWinLocn = database
; Database location on a Linux deployment (relative to appDataRoot)
dbLinuxLocn = database
dbExt = db3
cmd0 = CREATE TABLE "demo" ("name"TEXT, "age"INTEGER,PRIMARY KEY("name"))
; Windows optimisation
;cmd4 = PRAGMA page_size=4096
;Linux optimisation
cmd1 = PRAGMA page_size=1024
```



4. Now the server needs to be restarted so that the server can set up the database. use ```docker sensahub restart``` in a developer console to do this.


### Database Reading and Writing

#### Writing
There are a few ways to do this. One way is to edit the Database.ini file so that it also inserts data. Note that if the server has already built the database, the new insert commands will not work. You will have to delete the .db3 database file. An example of this would be:

```ini
[demo]
desc = Demo Database
dbType = SQLite
; Database location on a Windows deployment (relative to appDataRoot)
dbWinLocn = database
; Database location on a Linux deployment (relative to appDataRoot)
dbLinuxLocn = database
dbExt = db3
cmd0 = CREATE TABLE "demotable" ("name"TEXT, "age"INTEGER,PRIMARY KEY("name"))
cmd1 = INSERT INTO "demo" ("name", "age") VALUES ("Steve", 31)

; Windows optimisation
;cmd4 = PRAGMA page_size=4096
;Linux optimisation
cmd2 = PRAGMA page_size=1024
```

Make sure that you increment all of the cmd numbers correctly, otherwise the server will not create the database.

Another way is to grab the generated <dbname>.db3 file from the server and use DB browser to import data. Then the <dbname>.db3 file can be uploaded back to the server. This is the recommended route if you have a lot of data that you want to be available on the server immediately.

The third way is to use the Scripting widget to dynamically input data. This is the recommended route if you are building an application that adds or removes users or devices, and don't need any initial data in the database. We will explore this option.



<div class="column-container">
<div class="column row-container" style="width:60%;">

1. After the server has been restarted, we can now fill the database with data. Create a scripting widget, and copy and paste the following code into the script:
 ```javascript
Script.on('load', function() {
	var dbVal = {};
	var new_row = {
		"name": "Dave",
		"age": 22
	};
	dbVal["Dave"] = new_row;
	Database.saveRecord("demo", "demo", dbVal, function(response) {
	});
});
```

In this code we are creating an object (dbVal) that contains an object (new_row) that contains the row data, and it's key is the value of the primary key of the database, which in our case is "Dave".

Now this row has been added, but we can't see it yet.

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/database/create_script.png">
</div>
</div>

#### Reading
We will create a table to display the data, and edit the scripting widget to read from the database, and display it in the table.


<div class="column-container">
<div class="column row-container" style="width:60%;">

1. Create a table. 
    - In the "Columns" field, enter "name, age".

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/database/create_table.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:60%;">

2. Create a client input event.
    - Set "Event Type" to "Client Input"
    - Set "Event" to "receive value"
    - Set "Client Channel" to "table receive"

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/database/table_channel.png">
</div>
</div>

3. Edit the Scripting widget so it now contains the following code:

```javascript
var database = {};

Script.on('load', function() {
	readFromDatabase();
	
	var dbVal = {};
	var new_row = {
		"name": "Dave",
		"age": 22
	};
	
	dbVal["Dave"] = new_row;
	Database.saveRecord("demo", "demo", dbVal, function(response) {
		// after it has saved, update the table
		readFromDatabase();
		populateTable();
	});
});
	
// reads from the database and updates our local database variable
function readFromDatabase(){
	Database.readRecords(
		"demo",
		"demo",
		function (dbResponse) {
			database = dbResponse.value;
		},
		{"columns": "*", "filter": "", "order": ""}
	);
}

// sends the database information to the table
function populateTable() {
	ClientEvents.publish("table receive", database);
}
```

In the database.readRecords function, you will notice that it has ```{"columns": "*", "filter": "", "order": ""}``` as one of the fields. This defines database read options. **Columns** defines the columns that you want to read from the database. **Filter** defines an SQL statement that you want to filter by, for example ```"filter": "name = "Dave"``` will mean that only the row with the name "Dave" will appear. **Order** determines whether you order in ascending or descending order, and which column to order by, for example  ```"order": "ORDER by age ASC"``` will order the rows by age, in ascending order.

<div class="column-container">
<div class="column row-container" style="width:60%;">

4. Now save and change to screens, and you will see that the table will show Dave, 22. Try to add some more rows to the database so that Dave isn't so lonely.

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/database/table_dave.png">
</div>
</div>

---
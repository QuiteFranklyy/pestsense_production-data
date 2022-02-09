<!--Managing Devices-->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Managing Devices

---

## About
With a large number of sensors or devices that you want to connect to Sensahub, here is where you start. The Sensahub device management system allows you to create models of different types of devices, and create instances of each individual device based on the model template. 

A model is a particular type of device, for instance a temperature sensing device is a different model to a weight sensing device. After you set up a model for a device, you can create individual instances that relate to real devices, and allow them to connect to Sensahub.

<br>

---

<br>

### Manage Models
The first step is creating a **Model**. Let's navigate to the Manage Models page in Settings

<div class="column-container">
<div class="column row-container" style="width:71%;">

1. Click on **Settings**

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing devices/settings.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:60%;">

2. Click on **Manage Models**

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing devices/click_manage_models.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:70%;">

3. You should now see this screen.

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing devices/manage_models_screen.png">
</div>
</div>

<br>

---

<br>

<div class="column-container">
<div class="column row-container" style="width:70%;">

## Device Model Screen
In this screen you will see lots of possible information that can be set for each model. All of the fields are described below:

- **Distributor**: A distributor is the company that owns and distributes the devices. To add aditional distributors, please see your Sensavation representative to change it from "sensahub" to your desired distributor name. Likewise in an enterprise environment, the distributor name could be a departmental name.
- **Model Name**: This is the name of the model. If it is a temperature sensing IoT device, it could be called "tempSensor".
- **Account**: The account can be set to show which company or group is using this model of devices. Accounts can be set up and edited through the Account Management setting screen.
- **Application**: The application can be set to show what this model of devices are being used for, eg. "Campus Temperature Sensing".
- **Group**: You may have multiple groups of models that you would like to keep separate.
- **Make**: A model may have a certain make, and you can add that here.
- **Status**: You can enable and disable a certain model, you can also set them to inactive. Devices that are inactive or disabled will not be able to communicate with the platform.
- **Owner**: You can set the specific owner of a model.
- **Version**: You can set the version of the model if there are multiple device versions in the field.
- **Type**: If it is a certain type of model you can set that here.
- **Location**: If this model is set in a specific building or city, you can put that information here.
- **Department**: The department of a model can be set if you want to differentiate company departments using it.
- **Branch**: The branch can be set if you have a certain section of the company using it.
- **APN**: Access Point Name, the name of a gateway that the model of the devices use.
- **Model URL**: You can put a link to the model information here, such as datasheets or other technical information that might be required.
- **Notes**: Any additional notes about the model of device, for example operational status updates about the model.
- **Image**: You can add an image of the model so you can identify it easily.
- **Upload Firmware**: Not currently supported.
- **Edit Model Custom Attributes**: Here you can add attributes and default values for the model. Not currently implemented.
- **Bulk Upload**: Bulk upload of devices. Not currently implemented.
- **Generate Token**: Not currently implemented.

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing devices/manage_models_screen.png">
</div>
</div>

> Note: Changes to the model will not affect devices that have already been created using that model. You will need to update each device individually with the changes.

<br>

---

<br>

## Creating a Model
It is recommended that you look at the **Managing Users** help page to learn how to set up Accounts before setting up a Model, this way you can set the Models and Devices to specific **Accounts**.

Let's set up a demo Model of a Temperature Sensor for "Acme Pty Ltd". One feature of the Model Manager is that you can put in as much or as little information as you like, as long as you put in a model name, select an account, and set the status to enabled, you can start setting up devices.

<div class="column-container">
<div class="column row-container" style="width:70%;">

1. Enter Information about the Model
    - **Distributor**: We are setting ourselves up as the distributor, so we set it to "sensahub".
    - **Model Name**: A short name that summarises the function of the model, so we set it to "AcmeTempSensor".
    - **Account**: This is the account of the company that will be using the devices, so we set it to "Acme Pty Ltd", which is an account that we made in the **Managing Users** help page.
    - **Application**: The name of the project that this model of devices is being used for.
    - **Status**: We set this to "Enabled" so that Sensahub will accept connections from this model.
    - **Version**: Assuming this is a prototype, we put in "v0.5" as the Version.
    - **Location**: The devices will be generally located around Brisbane, so that is what we set the location to.

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing devices/bus_temp_sensor_model.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:70%;">

2. Save the Model by clicking the "Save" icon

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing devices/save_model.png">
</div>
</div>

<br>

---

<br>

## Manage Devices
Now that we have a model, we can start adding devices that correspond to this model. 

<div class="column-container">
<div class="column row-container" style="width:70%;">

1. Switch to the **Manage Devices** Tab

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing devices/switch_manage_devices.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:70%;">

2. You should now see this screen. 

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing devices/manage_devices_screen.png">
</div>
</div>

<br>

---

<br>

## Manage Devices Screen

<div class="column-container">
<div class="column row-container" style="width:70%;">

At the top, it shows the distributor, Model Name, and Unique ID / Serial Number.

Here you select the Distributor, the Model Name, and you can set the ID for the device.

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing devices/id_screen.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:70%;">

Below that, the Edit Device Details section.
- **Name**: Specific device name
- **Application**: Application the device is being used for
- **Group**: Group that the device belongs to
- **Account**: Account that the device belongs to
- **Status**: Set the status of this device
- **Make**: Make of the device
- **Location**: Location of the device
- **Department**: Department the device belongs to
- **Version**: Version of the specific device
- **Last Serviced**: Keep track of how long it has been since the device was serviced
- **Branch**: Branch the device belongs to
- **Type**: Type of device
- **Owner**: Who owns the device
- **Notes**: any other notes about the device

<br>

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing devices/device_details_screen.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:70%;">

In this section we also have connection information
- **ICCID**: Integrated Circuit Card Identification Number, the identification code for a SIM card
- **IMEI**: International Mobile Equipment Identity, the identification code for a phone or device within the mobile network
- **Cell Number**: Phone number for the device
- **APN**: Access Point Name, the name of a gateway that the model of the devices use.


</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing devices/cell_details_screen.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:70%;">

To the right, we have the Device Statistics
- **Last Seen**: last logged message from the device
- **Last Value**: the last value that was sent by the device
- **Connections**: number of connections recieved from this device
- **Signal Strength**: signal strength of the device
- **Battery Level**: battery level of the device
- **Added**: when the device was added
- **Modified**: when the device information was last modified
- **Image**: An image of the device
- **Connections / Day**: A graph of the connections by the device per day

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing devices/device_statistics_screen.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:70%;">

Just below the Device Statistics we have a few things:
- **Attribute table**: Can change attributes and values for the device that were initially set in the model
- **Launch URL for model details**: Click on this button to launch the URL set in the model
- **View on map**: view the device location if it has a registered location

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing devices/attribute_value_screen.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:120%;">

At the bottom, we have the Device List. This is a table with all of the registered devices. If you click on one, it will fill all of the above fields with the chosen device's information

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing devices/device_list_screen.png">
</div>
</div>

<br>

---

<br>

## Creating a Device

We will create a device using the model we defined in the previous example. While we will only create one device, any number can be made, as each device is an instance of the model, being identical in every way except for their identification/serial number.

<div class="column-container">
<div class="column row-container" style="width:70%;">


1. Set the device Distributor, Model and ID
    - Set **Distributor** to "Sensahub".
    - Set **Model** to "AcmeTempSensor" which is the model that we created in the previous example.
    - Set the **ID** to any number. In this example we will set it to "1". You can set this to the device's serial number, or a factory identification number.

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing devices/id_set.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:70%;">

2. Modify the Device Details
    - Set the **Name** to 1, this is what get's substituted when using wildcards in flows.
    - The **Application** field should have "Comfort Sensing" by default, inherited from the model.
    - Set the **Account** to "Acme Pty Ltd".
    - The **Status** field should also be "Enabled" by default, again inherited from the model.
    - The **Location** field has "Brisbane" by default, inhertited from the model.
    - the **Version** field should have "v0.5" by default, inherited from the model.

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing devices/device_details_set.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:70%;">

3. Press the **Save** icon.

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing devices/save_device.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:70%;">

4. You should now see this device in the Device List at the bottom of the page.

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing devices/populated_device_list.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:70%;">

5. If you click on the row, and edit the **Name** to "device1", then press Save, you will see that the device name has been updated.

</div>
<div class="column row-container">
<img src="/images/help/sensahub concepts/managing devices/edit_device_name.png">
</div>
</div>

<br>

---
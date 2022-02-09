<!--Flows and Server Events-->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>

<br>

# Flows and Server Events Walkthrough

---

<br>

<div class="column-container">
<div class="column row-container" style="width:120%;">

## About

In this example we will go through the necessary steps to setup two widgets to receive data from a server based channel. Here we will simulate real world data from a device through the use of a flow.

An **Interval** node will generate random numbers to simulate data coming from a water tank monitoring device. This data will be processed by an **If** node, and if it is less than a certain value, it will turn on a warning light to indicate low level. The data from the **Interval** and the **If** nodes will be sent to different channels using **End** nodes.

The results of these flows will be displayed in User Screens using a **Water Tank** widget, and a **Light** widget.

This example can be used as a reference to build your own application, or simply as a walkthrough to get familiar with how to use Sensahub.
</div>
<div class="column row-container" style="width:60%;">

<img src="/images/help/walkthrough/server_walkthrough/server_intro.png">

<img src="/images/help/walkthrough/server_walkthrough/server_intro_2.png">

</div>
</div>

<br>

---

<br>

### Setting up the Flows

Flows collect and process external data streams, creating new channels for the processed data. In this example, we will create a flow to generate random numbers for the water level and apply logic to determine if the level is low. The flow creates two channels; current water level, and a low water state. We are using the same screen used in the **Client Events Walkthrough**.

<br>

#### Interval Node

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

1. Select the Flows designer by clicking "Flows" in the top navigation bar

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/server_walkthrough/server_1.png">
</div>
</div>

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

2. Open the toolbox (the same way you open it in the screens designer) and drag an **Interval** node into the design area.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/server_walkthrough/server_2.png">
</div>
</div>

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

3. Click on the **Interval** to configure it.

4. Set **Interval Value** to "1". This is the number of **Timespans** between the interval sending data.

5. Set **Timespan** to "seconds".

6. Check the **random number** box. This will cause the interval to send a random number.

7. Set **Random Min** to "0" and **Random Max** to "100". The random number that is output will be between these numbers.

8. Save the **Interval**.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/server_walkthrough/server_3.png">
</div>
</div>


> **Note**: In the example we generate a random number, however if you just want to send a string or a single number, you can uncheck **random number** and instead put a string or a number into the **Data** field.

<br>

#### If Node

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

9. Drag an **If** node into the design area.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/server_walkthrough/server_4.png">
</div>
</div>

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

10. Click on the **If** node to configure it.

11. Set the **Function** to "less". The **Function** determines how the **If** node works.

12. Set the **Value** to 20. This is the value that is compared to the data that the **If** node receives. In this example, the **If** node will determine if the received value is *less* than *20*.

13. Set **New True** to 0, and **New False** to 100. In this example, if the value is less than 20, the **If** node will output 100. If the value is not less than 20, the **If** node will output 0.

14. Save the **If** node.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/server_walkthrough/server_5.png">
</div>
</div>

<br>

#### End Nodes

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

15. Drag 2 **End** nodes into the design area.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/server_walkthrough/server_6.png">
</div>
</div>

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

16. We want the first **End** node to output the raw data from the **Interval** node so we can display the current water level in the User Screens. In the first **End** node, set the channel values: 
    - **Category** as "Canberra"
    - **Class** as "Water"
    - **Instance** as "Water#2"
    - **Scope** as "Level".

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/server_walkthrough/server_7.png">
</div>
</div>

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

17. We want the second **End** node to output the true or false value from the **If** node, so we can turn an indicator light on and off in the User Screens. In the second **End** node, set the channel values: 
    - **Category** as "Canberra"
    - **Class** as "Water"
    - **Instance** as "Water#2"
    - **Scope** as "Water Low".

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/server_walkthrough/server_8.png">
</div>
</div>

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

18. Now we connect up the flow nodes. Click and drag on the small boxes on each node to set up the flows as shown in the picture.

    Each node has **Output Circles** and **Input Boxes**.

    - The output of the **Interval** should go to the input of the first **End** node and to the input of the **If** node
    - The true and false outputs of the **If** node should go to the input of the second **End** node.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/server_walkthrough/server_9.png">
</div>
</div>

> **Note**: The reason for connecting both *true* and *false* links from the **If** node to the "Water Low" channel is so we can switch sending true and false values as events to the display on the User Screen.

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

19. Save the Flows screen.

20. Switch to the Screen Designer.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/server_walkthrough/server_10.png">
</div>
</div>

<br>

### Client Widget Configuration
Now we want to display the flow data we have set up. To do this we will create a Water Tank widget and a Light widget. If you are following along from the previous example, you can create new widgets so they are on the same screen. This way you can directly see the difference between Server and Client events!

#### Water Tank

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

21. Open the toolbox, and drag a **Water Tank** widget and a **Light** widget into the work area.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/server_walkthrough/server_11.png">
</div>
</div>

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

22. Click on the **Water Tank** widget to configure it.

23. Create a new Event.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/server_walkthrough/server_12.png">
</div>
</div>

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

24. Set the **Event Type** to "Server Input".

25. Set the **Event** to "feed".

26. We want the feed from the Water Level flow we created. To set the **Server Channel**, there are two options:
    + 26.a: Set the **Category** as "Canberra", the **Class** as "Water", the **Instance** as "Water#2", and the **Scope** as "Level", **OR**

    + 26.b: Click the **Select Channel** text and search for the "Canberra/Water/Water#2/Level" channel (shown below).


27. Save the event.

28. save the **Water Tank** widget configurations.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/server_walkthrough/server_13.png">
<img src="/images/help/walkthrough/server_walkthrough/server_13_b.png" style="width: 50%;">
</div>
</div>

<br>

#### Warning Light

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

29. Click on the **Light** widget to configure it.

30. Create a new Event.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/server_walkthrough/server_14.png">
</div>
</div>

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

31. Set the **Event Type** to "Server Input".

32. Set the **Event** to "feed".

33. We want the feed from the Low Water Level flow we created. To set the **Server Channel**, there are two options:
    + 33.a Set the **Category** as "Canberra", the **Class** as "water", the **Instance** as "Water#2", and the **Scope** as "Water Low", **OR**
    + 33.b Click the **Select Channel** text and search for the "Canberra/Water/Water#2/Water Low" channel (shown below).


34. Save the event

35. Save the **Light** widget configurations.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/server_walkthrough/server_15.png">
<img src="/images/help/walkthrough/server_walkthrough/server_15_b.png" style="width:50%;">
</div>
</div>

<br>

### Saving and Testing the Screen

<div class="column-container">
<div class="column row-container" style="width:50%;">

<br>

36. Save the screen by pressing the "save screen" icon in the bottom left. A status message in the bottom bar will let you know when it has saved.

37. Switch to "User Screens" by clicking on "Screens" in the top navigation bar.

</div>
<div class="column row-container" style="width:50%;">

<img src="/images/help/walkthrough/server_walkthrough/server_16.png">

</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:50%;">

<br>

38. Observe the Water Tank and the Light. The level in the Water Tank will go up and down randomly every second! If the water level drops below 20%, the Low Water Warning Light will turn on! If the water is not below 20%, the Light will turn off!

</div>
<div class="column row-container" style="width:50%;">

<img src="/images/help/walkthrough/server_walkthrough/server_17.png">

</div>
</div>
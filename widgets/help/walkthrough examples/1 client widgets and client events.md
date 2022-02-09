<!--Client Widgets and Client Events-->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Client Widgets and Client Events Walkthrough

---

<br>

## About

<div class="column-container">
<div class="column row-container">

The following pages will go through an example to show you how to set up a widget and build a simple application that showcases user interaction on the clientside, and communication between the server and the client.

A Slider and a Water Tank will be used in the first example. The Slider will be setup with a **client output event** which will feed into the Water Tank. The Water Tank will be configured to receive and display the data using a **client input event**.

This example can be used as a reference to build your own application, or simply as a walkthrough to get familiar with how to use Sensahub.

</div>
<div class="column row-container">
<img src="/images/help/walkthrough/client_walkthrough/walkthrough_intro.png">
</div>
</div>

<br>

---

<br>

#### Building the Screen.


<div class="column-container">
<div class="column row-container" style="width:50%;">

<br>

1. First we need to switch to design mode. Click on "Design" in the top navigation bar.

</div>
<div class="column row-container" style="width:50%;">

<img src="/images/help/walkthrough/client_walkthrough/walkthrough_1.png">
</div>
</div>

<div class="column-container">
<div class="column row-container" style="width:50%;">

<br>

2. Create a new screen using the "add new screen" icon. You can rename the screen by clicking on the name and typing.

3. Open the Toolbox. The Toolbox contains all of the Sensahub Widgets that you can add to your application. Open the Toolbox and search for the Water Tank and the Slider.

</div>
<div class="column row-container" style="width:50%;">

<img src="/images/help/walkthrough/client_walkthrough/walkthrough_2.png">

</div>
</div>

<div class="column-container">
<div class="column row-container" style="width:50%;">

<br>

4. Drag the Water Tank widget and the Slider widget onto the design area.

</div>
<div class="column row-container" style="width:50%;">

<img src="/images/help/walkthrough/client_walkthrough/walkthrough_3.png">

</div>
</div>

<br>

#### Configuring Client Events for the Water Tank

<div class="column-container">
<div class="column row-container" style="width:50%;">

<br>

5. We want data to flow **into** the water tank. So we create a client **input** event to receive data from the Slider. Create a new event by clicking on **New Event**.

</div>
<div class="column row-container" style="width:50%;">

<img src="/images/help/walkthrough/client_walkthrough/walkthrough_4.png">

</div>
</div>

<div class="column-container">
<div class="column row-container" style="width:50%;">

6. Set the **Event Type** to "Client Input" from the dropdown menu. This defines whether data is sent to the client or the server, or received from the client or server. In this case, it is a **Client Input** event as we want to **Receive** data from a **Client** widget.

7. You can change the **Event Name** if you would like, here we will rename it to "Receive Level" so that we know what the event does.

8. Set the **Event** to "receive value" from the dropdown menu. Each widget will have their own events, in this case "receive value" will update the water tank level.

9. Set the **Client Channel** to "water tank level". This can be named anything you like, it is used to connect widget events together. Just remember to give the slider event the same name.

10. Save the Client Event using the "Save" button.

11. Save the widget configurations using the save icon.

</div>
<div class="column row-container" style="width:50%;">

<img src="/images/help/walkthrough/client_walkthrough/walkthrough_5.png">

</div>
</div>

<br>

#### Configuring Client Events for the Slider

<div class="column-container">
<div class="column row-container" style="width:50%;">

12. We want data to flow **out** of the Slider. So we create a client **output** event to send data to the Water Tank. Create a new event by clicking on **New Event**.

</div>
<div class="column row-container" style="width:50%;">

<img src="/images/help/walkthrough/client_walkthrough/walkthrough_6.png">

</div>
</div>

<div class="column-container">
<div class="column row-container" style="width:50%;">

<br>

13. Set the **Event Type** to "Client Output" from the dropdown menu. In this case, it is a **Client Output** event as we want to **Send** data to a **Client** widget.

14. You can change the **Event Name** if you would like, here we will rename it to "Send Level" so that we know what the event does.

15. Set the **Event** to "changed" from the dropdown menu. In this case "changed" will send the current value everytime the slider position is changed.

16. Set the **Client Channel** to "water tank level".

17. Save the Client Event using the "Save" button.

18. Save the widget configurations using the save icon.


</div>
<div class="column row-container" style="width:50%;">

<img src="/images/help/walkthrough/client_walkthrough/walkthrough_7.png">

</div>
</div>

#### Saving and Testing the Screen

<div class="column-container">
<div class="column row-container" style="width:50%;">

<br>

19. Save the screen by pressing the "save screen" icon in the bottom left. A status message in the bottom bar will let you know when it has saved.

20. Switch to "User Screens" by clicking on "Screens" in the top navigation bar.

</div>
<div class="column row-container" style="width:50%;">

<img src="/images/help/walkthrough/client_walkthrough/walkthrough_8.png">

</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:50%;">

<br>

21. Move the Slider up and down, and you can see the level in the Water Tank go up and down!

</div>
<div class="column row-container" style="width:50%;">

<img src="/images/help/walkthrough/client_walkthrough/walkthrough_9.png">

</div>
</div>
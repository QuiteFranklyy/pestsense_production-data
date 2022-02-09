<!--Data Aggregation and Display-->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>

<br>

# Data Aggregation and Display

---

<br>

<div class="column-container">
<div class="column row-container" style="width:60%;">

## About

In this example we will do some basic data aggregation on the serverside, and walk through how to display it on a graph. Sensahub features an **Aggregate** flow node that allows data from a certain channel to be aggregated to find the average, minimum, maximum, and other statistics.

An **Interval** flow node will simulate a device outputting data to Sensahub. We will use several **Aggregate** flow node widgets to find the average, minimum and maximum of this data. 

We will display the raw data and the aggregated data on a **Graph** widget in the user screens.

This example can be used as a reference to build your own application, or simply as a walkthrough to get familiar with how to use Sensahub.

</div>
<div class="column row-container" style="width:60%;">
<br>
<img src="/images/help/walkthrough/aggregate_walkthrough/intro.png">
</div>
</div>

<br>

---

<br>

### Setting Up the Flows

We will re-use the flows that were set up in the **Flows and Server Events** walkthrough. We are going to add 3 **Aggregate** flow nodes to calculate the average, minimum, and maximum for the *Water Level*.

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

1. Switch to the **Flows** designer.

2. Drag 3 **Aggregate** flow nodes into the design area.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/aggregate_walkthrough/aggregate_1.png">
</div>
</div>



<div class="column-container">
<div class="column row-container" style="width:50%;">

<br>

#### Average Aggregate

<br>

3. Click on the first **Aggregate** flow node to configure it.

4. Click **Select Channel**, type "Water" in the search bar, and select "Canberra/Water/Water#2/Level".

5. Set the **Function** to "average".

6. Set the **Elapsed** to "1".

7. Set the **Elapsed Units** to "minutes".

8. Save the **Aggregate** widget configurations.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/aggregate_walkthrough/aggregate_2.png">
</div>
</div>

<div class="column-container">
<div class="column row-container" style="width:50%;">

<br>

#### Minimum Aggregate

<br>

9. Click on the second **Aggregate** flow node to configure it.

10. Click **Select Channel**, type "Water" in the serach bar, and select "Canberra/Water/Water#2/Level".

11. Set the **Function** to "min".

12. Set the **Elapsed** to "1".

13. set the **Elapsed Units** to "minutes".

14. Save the **Aggregate** widget configurations.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/aggregate_walkthrough/aggregate_3.png">
</div>
</div>

<div class="column-container">
<div class="column row-container" style="width:50%;">

<br>

#### Maximum Aggregate

<br>

15. Click on the third **Aggregate** flow node to configure it.

16. Click **Select Channel**, type "Water" in the serach bar, and select "Canberra/Water/Water#2/Level".

17. Set the **Function** to "max".

18. set the **Elapsed** to "1".

19. Set the **Elapsed Units** to "minutes".

20. Save the **Aggregate** widget configurations.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/aggregate_walkthrough/aggregate_4.png">
</div>
</div>

#### End Flow Nodes

Now we want to send these aggregated values to a channel to display on the user screens. To do this we use **End** flow nodes.

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

21. Drag 3 **End** flow nodes into the design area.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/aggregate_walkthrough/aggregate_5.png">
</div>
</div>

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

22. Click on the first **End** flow node to configure it.

23. Set the **Category** to "Canberra", set the **Class** to "Water", set the **Instance** to "Water#2", and set the **Scope** to "Average".

24. Save the **End** node configuration.

25. Connect this end node to the "average" **Aggregate** flow node.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/aggregate_walkthrough/aggregate_6.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

26. Click on the second **End** flow node to configure it.

27. Set the **Category** to "Canberra", set the **Class** to "Water", set the **Instance** to "Water#2", and set the **Scope** to "Min".

28. Save the **End** node configuration.

29. Connect this end node to the "min" **Aggregate** flow node.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/aggregate_walkthrough/aggregate_7.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

30. Click on the third **End** flow node to configure it.

31. Set the **Category** to "Canberra", set the **Class** to "Water", set the **Instance** to "Water#2", and set the **Scope** to "Max".

32. Save the **End** node configuration.

33. Connect this end node to the "max" **Aggregate** flow node.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/aggregate_walkthrough/aggregate_8.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

34. Save the screen.

35. Switch to **Screens Designer**.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/aggregate_walkthrough/aggregate_9.png">
</div>
</div>
<br>

---

<br>

### Client Widget Configuration

Now that we have the flows set up, we want to display the data in an easy-to-digest way. The best way to do this is with a graph! Here we will set up 2 graphs; one for the raw level data, and one for the aggregated data.

#### Water Level Graph

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

36. Drag 2 **Graph** widgets into the design area.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/aggregate_walkthrough/aggregate_10.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

37. Click on the first **Graph** to configure it.

38. Disable **Compression**.

39. Set the **History Timespan** to be 0.0167. This represents how much data the graph displays in hours. 0.0167 is approximately 1 minute.

40. Set the **Domain Max** to "150" and the **Domain Min** to "0".

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/aggregate_walkthrough/aggregate_11.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

41. This **Graph** will display the raw **Water Level** data. Click **New Event** to create a new event.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/aggregate_walkthrough/aggregate_12.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

42. Set the **Event Type** to "Server Input".

43. Set the **Event** to "history".

44. Click **Select Channel** and select the channel "Canberra/Water/Water#2/Level".

45. Set the **Color** to "green".

46. Save the event.

47. Save the **Graph** widget configurations.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/aggregate_walkthrough/aggregate_13.png">
</div>
</div>


#### Aggregated Data Graph

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

48. Click on the other **Graph** to configure it.

49. Disable **Compression**.
 
50. Set the **History Timespan** to be 0.0167. This represents how much data the graph displays in hours. 0.0167 is approximately 1 minute.

51. Set the **Domain Max** to "150" and the **Domain Min** to "0".

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/aggregate_walkthrough/aggregate_14.png">
</div>
</div>

<br>

This **Graph** will display the aggregated data; it will display the average, minimum, and maximum water levels of the past minute. This means we will require **3** server input events.

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

52. Create a new event, set the **Event Type** to "Server Input".

53. Set the **Event** to "history".

54. Click **Select Channel** and select the channel "Canberra/Water/Water#2/Average".

55. Set the **Color** to "red".

56. Save the event.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/aggregate_walkthrough/aggregate_15.png">
</div>
</div>

 
<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

57. Create a new event, set the **Event Type** to "Server Input".

58. Set the **Event** to "history".

59. Click **Select Channel** and select the channel "Canberra/Water/Water#2/Min".

60. Set the **Color** to "blue".

61. Save the event.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/aggregate_walkthrough/aggregate_16.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

62. Create a new event, set the **Event Type** to "Server Input".

63. Set the **Event** to "history".

64. Click **Select Channel** and select the channel "Canberra/Water/Water#2/Max".

65. Set the **Color** to "yellow".

66. Save the event.

67. Save the **Graph** widget configurations.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/aggregate_walkthrough/aggregate_17.png">
</div>
</div>

<br>

---

<br>

### Saving and Testing the Screen

<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

68. Save the screen.

69. Switch to User Screens.

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/aggregate_walkthrough/aggregate_18.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:50%;">
<br>

70. The **Water Level** graph shows the random water level going up and down.

71. The **Aggregated** graph shows the **Average** that should hover somewhere around 50, the **Minimum** which hovers around the bottom of the graph, and the **Maximum** which hovers around the top of the graph!

</div>
<div class="column row-container" style="width:50%;">
<img src="/images/help/walkthrough/aggregate_walkthrough/aggregate_19.png">
</div>
</div>
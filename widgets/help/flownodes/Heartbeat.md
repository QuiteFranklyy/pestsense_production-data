<!-- Heartbeat Widget Help Markdown -->
<br>

# Heartbeat Node

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About

The Heartbeat node monitors the output of a channel, making sure that data is being sent or received. After a configurable amount of time passes, if the heartbeat node has not received any data from the channel it is monitoring, it will fire an event.

</div>

<div class="column row-container">
<img src="/images/help/heartbeat/heartbeat_main.png" width="106" height="95">
</div>
</div>

___

<div class="column-container">
<div class="column row-container">
<div class="row">

## Heartbeat Properties
| Property | Value | Description |
| -------- | ----- | ----------- |
Time Elapsed | Integer or Float greater than or equal to 1 | If the Heartbeat flow node does not receive a message from the previous node within the time specified in Time Elapsed the Heartbeat flow node will send a message with value Alarm Value to the next node. |
| Timespan | Selected from dropdown menu | Specifies the unit of time for Time Elapsed. |
| Alarm Value | Any cannot be empty | Specifies the value to be sent to the next node when the Heartbeat flow node has been triggered. |
| Reset Time Elapsed | Integer or Float greater than or equal to 1 | Specifies the amount of time the Heartbeat flow node should wait before sending the Alarm Value again if the Heartbeat flow node still hasn’t received a message from the previous node. |
| Reset Time Span | Select from dropdown menu | Specifies the unit of time for Reset Time Elapsed. | 



</div>
 
</div>

<div class="column row-container">
<div class="row">
<img src="/images/help/heartbeat/heartbeat_specific.png" width="168" height="529">
</div>
</div>
</div>

#### Tips
>The Heartbeat flow node employs the use of a system timer to calculate the time since the node last received a mesage from the previous node. This introduces limitiations in the operation of the flow node. For example:

>If the server goes down during the period when the timer is active, the timer will not be started again until it receives a new message.

---
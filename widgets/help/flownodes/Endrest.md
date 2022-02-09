<!-- End Rest Widget Help Markdown -->
<br>

# End Rest Node

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The End REST flow node is similar to the HTTPREST node, however it acts as a response to a HTTP Rest Request. It can only be used where the start of the flow originates from a HTTP Rest Start node.

Flow output sent as response to REST request, requires flow originating from a REST start node
If using an End node at the end of an *all instances* flow, be sure to select the checkbox for *all instances*
In the case of using *all instances*, be sure to fill out the required Channel Information.
**Note**, that the *instance* being repeated will be kept, and only the items filled in will be altered.
**Also note**, that in the event every field of the channel is repeated (ie no form items are entered), the new value
 will never come through the flows due to duplicating the channel.

</div>

<div class="column row-container">
<img src="/images/help/end_rest/end_rest_main.png" width="122" height="77">
</div>
</div>

___

#### Tips
>

---

<!-- Threshold Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Threshold Node

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The Threshold node monitors a flow. When it detects that the input changes from below to above threshold (increasing) or from above to below (decreasing), it will fire an event.

</div>

<div class="column row-container">
<img src="/images/help/threshold/threshold.png">
</div>
</div>

---



<div class="column-container">
<div class="column row-container" style="width:80%;">

## Threshold Properties
| Property | Description |
| -------- | ----------- |
| Name |  Widget name. |
| Threshold Value | Value to output once  the node has been triggered. |
| Trigger Type | Tiggrers if value is increasing/decreasing or both compared to previous value. |
| Trigger Value | Value to trigger the output value on (or leave blank  to pass input value to ouput). |
| Support Previous Null | If previous value was null (usually a start condution) assume previous was below (if increasing trigger) or above (if decreasing trigger). |


</div>
<div class="column row-container">
<img src="/images/help/threshold/threshold_specific.png">
<img src="/images/help/threshold/threshold_types.png">
</div>
</div>


Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
> Use this node to send an alert to your customer if for example a water tank level becomes too low.

---
<!-- Operator Widget Help Markdown -->
<br>

# Operator Node

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The Operator node allows simple operations to be applied to incoming data. It can do this with a single flow where it does a static operation, or with multiple flows where it uses the two incoming flows to perform the operation.

</div>

<div class="column row-container">
<img src="/images/help/operator/operator_main.png" width="120" height="103">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:100%;">
<div class="row">

## Operator Properties
| Property | Description |
| -------- | ----------- |
| Name | Widget name. |
| Function | Select a function to perform on the value. |
| Value | Value to perform calculation with. |

## Operator Functions
| Function | Description |
| -------- | ----------- |
| Multiply | Multiplies single flow by a number, or multiplies two flows together. |
| Divide | Divides a single flow by a number, or divides the top flow by the bottom flow. |
| Modulo | Finds the modulo of a single flow with the configured number, or uses the two incoming flows to find the modulo. |
| Add | Adds a number to a single flow, or adds two flows together. | 
| Subtract | Subtracts a number from a single flow, or subtracts the bottom flow from the bottom flow. |

</div>
 
</div>

<div class="column row-container">
<div class="row">
<img src="/images/help/operator/operator_specific.png" width="170" height="252">
</div>
<div class="row">
<img src="/images/help/operator/operator_functions.png" width="170" height="146">
</div>
</div>
</div>

#### Tips
> The Operator node can be used to remove an offset, or scale incoming data.

---
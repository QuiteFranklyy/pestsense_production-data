<!-- Aggregates Widget Help Markdown -->
<br>

# Aggregate Node

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The Aggregate node is a type of input node, enabling historical data processing over configurable time periods to find statistical values like averages, minimums, and maximums for channel data. You select the channel(s) you want to aggregate and the node will output the result to be used by the rest of the flow. Aggregates are useful to provide a summarised view.

</div>

<div class="column row-container">
<img src="/images/help/aggregates/aggregate_main.png" width="113" height="77">
</div>
</div>

___

<div class="column-container">
<div class="column row-container">
<div class="row">

## Aggregates Properties
| Property | Description |
| -------- | ----------- |
| Server Channels​ | Is referenced with a server channel, with category, class, instance, and scope.​ |
| Function​ | Has several options for historical data processing statistics / summaries.​ |
| Elapsed​ | The number of time units that the aggregate intakes historical data​. |
| Elapsed Units​ | The unit of time that is used by "Elapsed“. E.g. 12 hours (the default).​ |
| Since Date​ | Specifies a date for the start of the aggregation period until current time​. |
| Since Time​ | Specifies a time of day for the start of the aggregation period until current time​. |

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>


## Aggregates Functions
| Function | Description |
| -------- | ----------- |
| Count | Number of data values being aggregated. |
| Sum | Sum of all data values. | 
| Min | Minimum of all data values. |
| Max | Maximum of all data values. |
| Average | Average of all data values. |
| Meadian | The median value of all data values. |
| Integral | Area under the curve. |
| Mode | The mode value of all data values. |
| Spread | Difference between minimum and maximum. |
| Stddey | The standard deviation of all data values. |
| First | The first data value. | 
| Last | The last data value. |

</div>
 
</div>

<div class="column row-container">
<div class="row">
<img src="/images/help/aggregates/aggregate_specific.png" width="166" height="675">
</div>
<div class="row">
<img src="/images/help/aggregates/aggregate_functions.png" width="166" height="276">
</div>
<div class="row">
<img src="/images/help/aggregates/aggregate_elapsed_units.png" width="166" height="167">
</div>
</div>
</div>

#### Tips
>Other statistical functions are available, or can be programmed via the Sensahub flow scripts.​

>Aggregates are processed once a minute.​

>Aggregate processing is CPU intensive, so only setup what is required.​

>The channel selected for an aggregate function will accept wildcards, making it possible to aggregate a range of channels.​

>Either a specific amount of time (e.g. 10 minutes), or from a specific date (e.g. 1/1/2020), can be used as the aggregation period.


---
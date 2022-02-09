<!--Flows-->
<br>

# Sensahub Flows

---

## About
+ Flows make **processing data** on the server easy and accessible by utilising the same **drag and drop designer** used to design user screens.
+ **Parse raw data** from external sources into meaningful data for processing and usage in Sensahub. Or **process historical data** with aggregate functions.
+ Data from **input channels** can flow and **branch through links**; through functional nodes used for processing data; through to **output channels**.
+ **Functional nodes** can perform a number of **operations on data** including: arithmetic, comparisons, aggregation, parsing input and formatting output.
+ For more advanced data processing you can **incorporate scripts** in flows.

---

### Example
The image below shows the flows screen. It contains flow nodes and links that take raw data from a water tank monitoring sensor and breaks it down (parses) into the required data elements. This is processed through several functional nodes and then output to different channels for use in a Sensahub application.

1. **Input Channel**
    + Start of the flow.
    + Input of data to Sensahub from the water tank sensors.
2. **JSON Parsing Node**
    + Strip incoming data stream to extract the relevant data.
    + Split into Water Level, Battery Level, Pressure, Temperature etc.
3. **Arithmetic Node**
    + This node can perform Addition, Subtraciton, Multiplication, Divide, and Modulo.
4. **Formatting Node**
    + Format the data for use within the channel.
5. **Output**
    + Direct the flow to a new or existing channel.
    + This is the end of the flow.

<img src="/images/help/sensahub concepts/flows/flow_help.png" width="800" height="372" style="display:block;margin-left:auto;margin-right:auto;width:100%;height:auto;">

<br>

---
<!-- Ticker Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Ticker Widget

___
<div class="column-container">
<div class="column row-container" style="width:75%">


## About
The Ticker widget is able to display the current share price of Australian and American stocks.


</div>

<div class="column row-container">
<img src="/images/help/ticker/ticker.png" width="100" height="52">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Ticker Properties
| Property | Description |
| -------- | ----------- |
| API Token | API access token for https//finnhub.io |
| Stocks (Comma Separated) | Enter stock names.exchange comma  separated eg. NABLAX for National Australian Bank ( Australian Exchange), MSFT for Microsoft (NASDAQ exchange). |
| Update | Interval (Seconds)  Period to update stock prices. |
| Color | Select color theme for button. |

</div>
<div class="column row-container">
<img src="/images/help/ticker/ticker_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive Value | Sets the value of the ticker to the received value. |

</div>
<div class="column row-container">
<img src="/images/help/ticker/ticker_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Output Events
| Event | Description |
| ----- | ----------- |
| Pressed | Sends an activation message to the server channel it is connected to.  |

</div>
<div class="column row-container">
<img src="/images/help/ticker/ticker_client_output.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
>

---
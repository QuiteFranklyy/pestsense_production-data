<!-- Carousel Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Carousel Widget

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The Carousel widget is used to show multiple thumbnail images in a carousel layout that the user can scroll with finger or mouse swipes to the left and right. Image details are displayed below each image, and selecting (clicking) the image creates a client event for other widgets to act on (eg. show a larger version of the image).

</div>

<div class="column row-container">
<img src="/images/help/carousel/carousel.png">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Carousel Properties
| Property | Description |
| -------- | ----------- |
| Per Page | How many images to display. |
| Focus Border | Border color for focused slide, when per page is above 1. |
| Color | Select color theme for button. |

</div>
<div class="column row-container">
<img src="/images/help/carousel/Carousel_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive Value | Sets the value of the carousel|
| Remove Slide | Removes a slide|
| Clear | Clears all slides|
| Go To | Jumps to a slide|
| Next | Selects the next slide in the list|
| Previous | Selects the previous slide in the |
| Set Label | Sets the carousel label of the current active slide|

</div>
<div class="column row-container">
<img src="/images/help/carousel/Carousel_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Output Events
| Event | Description |
| ----- | ----------- |
| Pressed | Activates when an image is pressed. |
| On Charge | Activates whenever an image is changed. |

</div>
<div class="column row-container">
<img src="/images/help/carousel/Carousel_client_output.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Events
| Event | Description |
| ----- | ----------- |
| Feed | Is the data stream directed from the server channel. The value of the carousel is set to value received from the server. |

</div>
<div class="column row-container">
<img src="/images/help/carousel/Carousel_server_input.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
> Use the carousel to display lots of images to a user. An example would be having a carousel of pictures of people, so you could click on a person and it would display their phone number.

---
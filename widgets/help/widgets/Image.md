<!-- Image Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Image Widget

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About

The Image widget is used to display images. Using the image widget, mages can be selected from your local machine and uploaded to the server for display.
</div>

<div class="column row-container">
<img src="/images/help/image/image.png">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Image Properties
| Property | Description |
| -------- | ----------- |
| Border Width | Width of border around image. |
| Opacity | Opacity of image |
| Image Name | Select the name of the image. |
| Location | Leave blank for the user files folder. |
| Value Clicked | Value to send when pressed. |
| Maintain Aspect Ratio | Maintain aspect ratio of the uploaded image. |
| Background | Select background color. |
| 3D shadow | Creates a 3D Shadow below image. |

</div>
<div class="column row-container">
<img src="/images/help/image/image_specific.png" width="150" height="387">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive Value | Sets the image to the received value. Input is a filepath to an image. Note that it uses the local server file system, so if you want to access the images folder, input "../images/your_image_here.png"|
| Get Value | Gets the assigned value of the image. |
| Set Image | Sets the value of the image container. Input is a file. |

</div>
<div class="column row-container">
<img src="/images/help/image/image_client_input.png" width="150" height="217">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Output Events
| Event | Description |
| ----- | ----------- |
| Clicked | Returns the value of the clicked image.|

</div>
<div class="column row-container">
<img src="/images/help/image/image_client_output.png" width="150" height="204">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Events
| Event | Description |
| ----- | ----------- |
| Feed | Is the data stream directed from the server channel. Input is a filepath to an image.  |
| Set Image | Sets the value of the image. Input is a file. |

</div>
<div class="column row-container">
<img src="/images/help/image/image_server_input.png" width="150" height="216">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Output Events
| Event | Description |
| ----- | ----------- |
| Clicked | Sends a message to the server channel. |

</div>
<div class="column row-container">
<img src="/images/help/image/image_server_output.png" width="150" height="204">
</div>
</div>

#### Tips
> You can customize your image by choosing the title, background, and border.

<br>
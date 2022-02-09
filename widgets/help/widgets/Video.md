<!-- Video Widget Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Video Widget

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The Video widget is video player which can be used to play different formats of video files.

</div>

<div class="column row-container">
<img src="/images/help/video/video.png" width="93" height="94">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Video Properties
| Property | Description |
| -------- | ----------- |
| Source | Select video  file to play. |
| Repeat | Repeat video when finished. | 
| URL | Video URL from YouTube. |

</div>
<div class="column row-container">
<img src="/images/help/video/video_specific.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Receive Value | Sets the value of the video to the received value. |
| Start | Plays the video. |
| Pause | Pauses the video. |
| Stop | Entirely stops the video. |

</div>
<div class="column row-container">
<img src="/images/help/video/video_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Output Events
| Event | Description |
| ----- | ----------- |
| Pressed | Sends an activation message to the server channel it is connected to. |

</div>
<div class="column row-container">
<img src="/images/help/video/video_client_output.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Events
| Event | Description |
| ----- | ----------- |
| Feed | Is the data stream directed from the server channel. The value of the video is set to value received from the server. |

</div>
<div class="column row-container">
<img src="/images/help/video/video_server_input.png">
</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
>

---
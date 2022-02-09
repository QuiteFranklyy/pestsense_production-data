<!-- Help Viewer Help Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Help Viewer

___
<div class="column-container">
<div class="column row-container" style="width:65%">


## About
The Help Viewer widget provides the ability to display help pages such as these in-line with dashboards, rather than having the side bar cover the dashboard. It allows the display of any helpfiles in the help directory. An important feature is that the zoom of the displayed help file can be adjusted, so if the markdown needs to appear larger, the markdown file does not have to be edited.


</div>

<div class="column row-container">
<img src="/images/help/helpviewer/helpviewer_main.png">
</div>
</div>

___

<div class="column-container">
<div class="column row-container" style="width:90%;">

## Dropdown Properties
| Property | Description |
| -------------- | ----------- |
| Border Width | Set the width of the border in pixels. |
| Border Color | Set the color of the border using a color picker. |
| Background Color | Set the background color of the widget using a color picker. |
| Default Filepath | Set the filepath for the default help markdown that is displayed. Eg to show the help file for the Icon widget, set this to "/widgets/Icon.md". |
| Zoom | Set the zoom of the help markdown, allowing the file to appear larger or smaller. |
| 3D Shadow | Add a 3D shadow to the help viewer. |


</div>
<div class="column row-container">
<img src="/images/help/helpviewer/helpviewer_settings.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:85%;">

## Client Input Events
| Event | Description |
| ----- | ----------- |
| Set Helpfile | Set the helpfile that is being displayed, use the filepath to it eg "/widgets/Icon.md". |
| Clear Helpfile| Clears the helpfile that is currently being displayed. |
| Set Zoom | Send a number to the Help Viewer to set the zoom. |

</div>
<div class="column row-container">
<img src="/images/help/helpviewer/helpviewer_client_input.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Client Output Events
The Help Viewer does not have any client output events.

</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Input Events
The Help Viewer does not have any server input events.

</div>
</div>

<div class="column-container">
<div class="column row-container" style="width:80%;">

## Server Output Events
The Help Viewer does not have any server output events.

</div>
</div>

Click [here](http:www.google.com "API Info") for more detailed API information.

#### Tips
> The Help Viewer is most useful for custom applications, such as displaying a help file on how to set up a specific client device.
> The Help Viewer can also be used in introduction screens where Sensahub Help such as navigating the site can be displayed on the screen.

---
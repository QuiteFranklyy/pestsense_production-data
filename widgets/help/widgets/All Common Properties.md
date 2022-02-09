<!-- Common Widget Properties Markdown -->
<link rel="stylesheet" type="text/css" media="all" href="/help/markdown_styles.css"/>
<br>

# Common Widget Properties

___

<div class="column-container">
<div class="column row-container" style="width:90%">

## About
We currently have 39 widgets in our toolbox, and even though they are all very different, they still have some similar properties between all of them.

</div>
<div class="column row-container">
<img src="/images/help/all common properties/all.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:90%">

### Proportional Scaling
If you are trying to design an application that gracefully fits differently sized screens, enable the proportional scaling option. This option causes the widget to scale proportionally to the size of the window. Note that you can't move a widget once proportional scaling has been enabled, so you have to disable proportional scaling to relocate or resize the widget. The location, width, and height of a widget are not able to be edited directly, but they show you how the application is calculating the position. Note that the unit that these properties use is in %. 

</div>
<div class="column row-container">
<img src="/images/help/all common properties/proportional_scaling.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:90%;">


### Z-Index
The Z-Index of a widget defines where it is layered relative to other widgets. By setting this property, you can control which widgets are placed on top of other widgets.
The options for the Z-Index are:
- On Bottom
- Level 1
- Level 2
- Level 3
- On Top

You might have several widgets on the same Z-Index level. The way that layering is determined for widgets on the same level is when the widget was created. The most recently created widget will appear on top of older widgets on the same Z-Index level.

</div>
<div class="column row-container">
<br>
<br>
<img src="/images/help/all common properties/z_index.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:90%;">

### Disabled
By enabling the disabled property on a widget, users will no longer be able to interact with it, and it will stop displaying data. The widget will still load, but it will be greyed out to signify that it is disabled.

</div>
<div class="column row-container">
<br>
<br>
<img src="/images/help/all common properties/disabled.png">
</div>
</div>


<div class="column-container">
<br>
<div class="column row-container" style="width:90%;">

### Visible
Widgets can be made invisible if you disable the visiblity. This may be used if you want to temporarily stop users interacting with a certain widget. This way the widget configurations are still there, but it doesn't load on the user screens.

</div>
<div class="column row-container">
<br>
<br>
<img src="/images/help/all common properties/visible.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:90%;">

### Tooltip
A custom tooltip can be set for every widget. When you hover over a widget for a few seconds, the custom tooltip will popup. This can be used if you want users to understand more about what a widget is displaying, without directly adding text onto the screen.

</div>
<div class="column row-container">
<br>
<br>
<img src="/images/help/all common properties/tooltip.png">
</div>
</div>


<div class="column-container">
<div class="column row-container" style="width:90%;">

### Property
This is a custom attribute that you can use for specialised applications.

</div>
<div class="column row-container">
<br>
<br>
<img src="/images/help/all common properties/property.png">
</div>
</div>
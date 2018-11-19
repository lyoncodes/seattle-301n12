<h1> Journals </h1>
<h2>Responsive Web Design</h2>

RWD is the practice of building a website suitable to work on every device and every screen size.

Typically, mobile websites require a seperate code base with its own little world. Responsive web design allows for websites that can dynamically respond to mobile viewports and usage. 
<hr>
Here is a simple formula for sizing an element relative to its parent container:

<i>target / context = result</i>
<hr>
@media queries were built as an extension to media types commonly found when targeting and including styles. They allow for different styles to be specified in response to different devices.

@media queries contain logical operators that can be used as expressions. There are three operators: <b>and, not, and only</b>

<i>Example: <b>and</b></i>

<b>@media all and (min-width: 800px) and (max-width: 1024px)</b> 

allows for both conditions to be applied. In this case, the media query selects all media types between 800 and 1024 pixels wide.

<i>Example: <b>not</b></i>

<b>@media not screen and (color) {...}</b>

specifies any query <i>but</i> the one identified. In this example, color screens are identified, and thus the media query only applies to black & white, monochrome screens.

<i>Example: <b>only</b></i>

<b>@media only screen and (orientation: portrait) {...}</b>

Specifies only screens in a portrait orientation.
<hr>
<h2>Media Features</h2>
Media features are used to specifiy which properties and attributes are targetted in the query. 

The min and max keywords can be added to features, and are commonly used to manipulate hieght and width of a page. The min-width, max-width pair can be used to scale a website to a mobile viewport. 

@media all and (min-width: 320px) and (max-width: 780px)

@media all and (orientation: landscape)

landscape / portrait plays big role in mobile dev, as users manually change their screen orientation.
<h2>Mobile First</h2>

This approach includes using styles targeted at smaller viewports as the default styles for a website, then use media queries to add styles as the viewport grows.

This approach has many benefits and saves the user bandwidth. 

the viewport meta tag is recommended for sizing relative to a device's viewport.

<b>It goes: < meta name = "viewport" content = "width = device-width"></b>

device-height, device-width will automatically apply qualifying media queries.

<h3>viewport scale</h3>
minimum-scale, maximum-scale, initial-scale, user-scalable

the initial-scale of a website should be set to 1. Setting the initial scale to 1 defines the ratio between the device height--in portrait orientation--and the viewport size. In landscape, the relationshiop between device width and viewport size. 

In HTML : <b>
< meta name="viewport" content = "width = device-width, initial-scale = 1">
</b>

In CSS: <b>
@viewport {
 width: device-width;
 zoom: 1;
}
</b>
<h3> Media Scaling </h3>
setting media tags to a max-width of 100% makes sure the media is scalable upon viewport change. 

In CSS:<b>
img, video, canvas {
 max-width: 100% }
</b>
<hr>
<h1> All About Floats </h1>
Floats are best illustrated in a side by side comparison to elements with absolute positioning.

Floated elements allow text to flow around them, and remain part of the flow of the webpage. Other elements will be affected by the positioning of a float. This is distinct from elements with absolute positioning, that are taken out of the page flow and stay where positioned. Other elements do not flow around absolute positioning. 

4 Valid Values: <b> left, right, none, inherit </b>

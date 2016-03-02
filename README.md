# Graph-Extensions-LabVIEW
These add some nice mouse effects and highlighting options on XY graphs and Waveform graphs by extending the picture controls within graphs and some simple events.

##Cursors
-Shows cursors automatically at mouse for each plot.  Various options to enable added lines, sizing, text formating, timestamp displays, etc.


Shows real time cursors overlayed in a graph, using just one mouse move event case.  The options for the cursors can be highly customized to set up a unique cursor style.

Usage: Place this inside an event structure on any XY graph, in the "Mouse Move" event case.  Set the options as an input cluster to override the defaults.  The output picture control would typically be connected to the XY Graph's "PlotImages.Front" property item.

![Cursor-Simple](https://github.com/unipsycho/Graph-Extensions-LabVIEW/blob/master/documentation/images/Cursors-Simple.JPG)


###Cursor Options
<b>Horizontal Line?</b> - Draws a horizontal line to intersect each plot
<b>Verticle Line?</b> - Draws a verticle line at the mouse location to highlight the cursor location (typically on the time scale)
<b>Timestamp</b> - Sets where to display the timestamp (if you want it at the top or bottom)  Used best with the verticle line turned on.
<b>Font</b> - Setup the font for displaying the cursor text
<b>Alignment</b> - Sets the alignment options for the text relative to the cursor point
<b>TextFormat</b> - Sets the text display format at the cursor points to show.  Three input parameters are available for the text, which can be accessed using parameter numbers.
inputs: 
1$ - Timestamp at cursor locations
2$ - Value of the plot
3$ - Name of the plot

Examples: $2$.2f\n\n%1$s
This shows the value of the plot with 2 decimal places.  A blank line, then the name of the plot 

![Cursor-Advanced](https://github.com/unipsycho/Graph-Extensions-LabVIEW/blob/master/documentation/images/Cursors-Advanced.JPG)

##Graph BGK Colors
This allows a graph to easily have its background color changed, and the gird lines will automatically be colored to subtly match the color based on shifting the luminance up or down to constrast the color set.

![BGK-1](https://github.com/unipsycho/Graph-Extensions-LabVIEW/blob/master/documentation/images/SetBGKColor-2.JPG)

![BGK-2](https://github.com/unipsycho/Graph-Extensions-LabVIEW/blob/master/documentation/images/SetBGKColor-2.JPG)

![BGK-3](https://github.com/unipsycho/Graph-Extensions-LabVIEW/blob/master/documentation/images/SetBGKColor-3.JPG)

Used by reference with a color input, to simply change the color. Can be user driven or used once for initialization.

##Peaks and Valleys
Allows data to be scanned for peaks and valleys with width and amplitude thresholds to determine them.  It can be used statically or driven in an event structure on graph scale changes to have it follow the graph edits by a user.

![Peaks&Valleys-1](https://github.com/unipsycho/Graph-Extensions-LabVIEW/blob/master/documentation/images/Peaks&Valleys.jpg)

##Markers
Under development:  Allows user positioned markers and 
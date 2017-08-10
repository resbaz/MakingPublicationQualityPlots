# Cheat Sheet

## Making Plots
The following types of plots will be used to visualise data.
## Line Plot
#### Syntax
plot(X,Y, LineSpec)

Use LineSpec to change the properties of the line.

For eg:

plot(X,Y, '--r') will plot a dashed, red line.

## Scatter Plot
#### Syntax

scatter(X,Y, size, colour)

If you want to specify colour without specifying size, syntax will be as follows
scatter(X,Y, [], colour)

scatter(X,Y, 'filled') will fill the circles.

scatter(X,Y, 'd') will change the marker shape from the circle (default) to diamonds.

## Bar Plots
#### Syntax
bar(x,y,style)

x= 1-d vector.

y= 1 or 2-d matrix. Each column will correspond to one group.

## Error Bars on  a line plot

errorbar(X,Y,E);

Will plot X and Y and will automatically make errorbars &plusmn; E.


<b> For more on line specification, marker specification and colour shortcuts, see:</b>

https://au.mathworks.com/help/matlab/ref/linespec.html?searchHighlight=Line%20Style&s_tid=doc_srchtitle

## Name Value Pairs

It can get quite confusing just adding line specifications using commas without telling us what exactly each of this means. For eg, you can make a scatter plot as below:

scatter(X,Y, 25, 'r', 'filled', 'o') etc. But there is a better way to do this using Name Value Pairs. It helps us keep track of which specification we have changed to what.

scatter(X,Y, 'MarkerFaceColor', 'r', 'MarkerEdgeColor', 'r'); 

Using Name-Value pairs gives us a lot more control over the various aspects of the graph.

### Name Value Pairs commonly used:

'LineStyle', 'symbol' - Change the style of the line to one of the styles specified in Line Specifications 

'LineWidth', 'number'- Width of the line will change to number.

'MarkerFaceColor', 'color' - Controls the colour of the marker face.

'MarkerEdgeColor', 'color'- Controls the colour of the marker edge.

'Marker', 'symbol'- Marker shape will change to what's specified in symbol.

'Color', 'color/ RGB triplet'- You can customize the colour you want using RGB triplets.

'SizeData', 'Scalar/Vector'- Scalar will uniformly scale all data points, Vector will change each data point individually.


Plot Properties: https://au.mathworks.com/help/matlab/ref/chartline-properties.html

Scatter Plot Properties: https://au.mathworks.com/help/matlab/ref/scatter-properties.html?s_tid=srchtitle

Bar Plot Properties: https://au.mathworks.com/help/matlab/ref/bar-properties.html?searchHighlight=bar&s_tid=doc_srchtitle

## Figure Objects.

When you make a plot, you can also set an output which will make a "figure object" which will contain all the properties of the graph. 

s= scatter(X,Y);

Will make a figure object s, which can be thought of as a structural array that contains all the data pertaining to the figure in its many fields. We can then edit the individual properties using the structure notations.

So if I want to change the marker shape to diamond, then I would do it as follows:

s.Marker= 'd';

You can change all the properties we discussed earlier by using the name of the property after the '.'.

eg:

s.LineStyle= '--';

s.LineWidth= 2;

This is handy if you want to edit properties after you have already made the plots. The plot properties are as specified in the above links.

## Figure and Axis handles.

These give you control over properties of the overall figure. Using the figure handles, you can change properties such as the background colour. Using the axis handle, you can change location and colour of the axis, the scale of the axes, what ticks are placed.

You can get figure handle using the 'gcf' function which stands for "get current figure"

fh=gcf;

fh.Color= 'r'; % Sets the background colour to red.

fh.Units='inches'; % Helps you specify the size of the figure in real life terms.

fh.Position= [0,0,100,100]; % figure starts at 0,0 and can go to 100 points (or inches or centimeters).

You can get axis handles using 'gca' function which stands for "get current axis"

ax= gca;

ax.Box = 'off'; % turns the box around the graph off.

ax.Fontsize= 12; % Changes the Fontsize to 12 pts.

ax.LineWidth= 2.0;

ax.XLim= [0 1]; % Will only display x axis between 0 and 1.

ax.YLim= [0 1]; % Will only display y axis between 0 and 1.

More Figure Handle Properties: https://au.mathworks.com/help/matlab/ref/figure-properties.html?searchHighlight=axis%20properties&s_tid=doc_srchtitle#zmw57dd0e273556

More Axis Handle Properties: https://au.mathworks.com/help/matlab/ref/figure-properties.html?searchHighlight=axis%20properties&s_tid=doc_srchtitle#zmw57dd0e273556

## Annotating Figures

You can give a title, x and y labels usign the following commands

title('MyTitle')

xlabel('This is my x-axis')

ylabel('This is my y-axis')

legend('series 1', 'series 2')

## Loess Smoothing

https://au.mathworks.com/help/curvefit/lowess-smoothing.html

Function from file-exchange: https://au.mathworks.com/matlabcentral/fileexchange/55407-loess-regression-smoothing?s_tid=srchtitle

Dataviz slides: http://slides.com/errollloyd/deck-2-3



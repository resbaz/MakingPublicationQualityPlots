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



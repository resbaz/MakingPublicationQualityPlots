# Cheat Sheet

## Making Plots
The following types of plots will be used to visualise data.
- Line Plot
### Syntax
#### plot(X,Y, LineSpec)

Use LineSpec to change the properties of the line.
For eg:
plot(X,Y, '--r') will plot a dashed, red line.

- Scatter Plot
### Syntax
#### scatter(X,Y, size, colour)
If you want to specify colour without specifying size, syntax will be as follows
scatter(X,Y, [], colour)

scatter(X,Y, 'filled') will fill the circles.
scatter(X,Y, marker) will change the marker shape.

- Bar Plots
### Syntax
#### bar(x,y,style)
x= 1-d vector
y= 1 or 2-d matrix. Each column will correspond to one group.

# Line Style, Marker and Colour options
## Line Style	Description
\-	Solid line (default)
\--	Dashed line
\:	Dotted line
\-.	Dash-dot line
## Marker	Description
\o	Circle
+	Plus sign
*	Asterisk
.	Point
x	Cross
s	Square
d	Diamond
^	Upward-pointing triangle
v	Downward-pointing triangle
>	Right-pointing triangle
<	Left-pointing triangle
p	Pentagram
h	Hexagram
## Color	Description
y yellow
m magenta
c cyan
r red
g green
b blue
w white
k black


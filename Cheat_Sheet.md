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

Line Specifications: https://au.mathworks.com/help/matlab/ref/linespec.html?searchHighlight=Line%20Style&s_tid=doc_srchtitle

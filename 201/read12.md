# Charts:
- Charts are better for displaying data visually when comparing between tables, It's a very convenient way to show data quickly.


### Drawing a line chart:
- To draw a line chart, firstly we need to create a canvas element in our HTML in which chart.js can draw our chart.
- then we need to link a script that will retrieve the context of the canvas.
- inside our script tag we require to create our data.

### Drawing a pie chart:
- we will create a canvas element again for pie chart.
- after that, we require to get the context and to instantiate the chart.
- now we need to create the data.
- after the pieData, we will add the options.


# Basic usage of canvas:
- canvas tag is similar to img tag element. The only different between them is that canvas doesn't have src & alt attributes.
- canvas has only two attributes, just width & height attributes.
- Initially values for width & height are 300px & 150px respectively.

- canvas element can be styled like a normal image.

### Required canvas closing tag:
- canvas element requires closing tag. If this closing tag is not present, the rest of the documents would be considered the fallback content and wouldn't be displayed.

### The rendering content:
- The canvas element creates a fixed-size drawing surface that exposes one or more rendering contexts, which are used to create and manipulate the content shown.
- When we want to display somthing on canvas, a script requires to access the rendering context & draw on it.
- canvas element has a method called getcontext(), used to obtain the rendering context and its drawing functions.

### Checking for support:
- The fallback content is displayed in browsers which do not support canvas. Scripts can also check for support programmatically by testing for the presence of the getContext() method.

# Drawing shapes with canvas

### Drawing rectangles:
- canvas only supports two primitive shapes: rectangles & paths. Other shapes must be created by combining one or more paths.
- There are three functions that draw rectangles on the canvas:
- fillRect(x, y, width, height)
- Draws a filled rectangle.

- strokeRect(x, y, width, height)
- Draws a rectangular outline.

- clearRect(x, y, width, height)
- Clears the specified rectangular area, making it fully transparent.

### Drawing paths:
- A path is a list of points, connected by segments of lines that can be of different shapes, curved or not, of different width and of different color.

- How to make shaps using paths?
- 1. create the path.
- 2. Then using drawing commands to draw into the path.
- 3. Once the path has been created, we can stroke or fill the path to render it.

# Applying styles and colors:

### Colors:
- There are tow main properties to apply colors to a shape:
- 1. fillStyle = color
- Sets the style used when filling shapes.

- 2. strokeStyle = color
- Sets the style for shapes' outlines.
 
 ## Line styles:
 - There are several propertie which allow us to style lines.

 - 1. lineWidth = value
 - Sets the width of lines drawn in the future.

- 2. lineCap = type
- Sets the appearance of the ends of lines.

 - 3. lineJoin = type
- Sets the appearance of the "corners" where lines meet.
 
 - 4. miterLimit = value
- Establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes.

- 5. getLineDash()
- Returns the current line dash pattern array containing an even number of non-negative numbers.

 - 6. setLineDash(segments)
- Sets the current line dash pattern.
 
 - 7. lineDashOffset = value
- Specifies where to start a dash array on a line.
 
 # Drawing text:
 - There are two methods to render text canvas provides them:

 - 1. fillText(text, x, y [, maxWidth])
- Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
 
 - 2. strokeText(text, x, y [, maxWidth])
- Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.
 
 ### Styling text:
 - There are some properties which we can use them to adjust the way the text gets displayed on the canvas:

 - 1. font = value
 - The current text style being used when drawing text. This string uses the same syntax as the CSS font property. The default font is 10px sans-serif.
 
 - 2. textAlign = value
 - Text alignment setting. Possible values: start, end, left, right or center. The default value is start.

 - 3. textBaseline = value
 - Baseline alignment setting. Possible values: top, hanging, middle, alphabetic, ideographic, bottom. The default value is alphabetic.
  
 - 4. direction = value
 - Directionality. Possible values: ltr, rtl, inherit. The default value is inherit.
 
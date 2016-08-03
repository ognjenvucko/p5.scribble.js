# scripple-p5.js
Draw 2D primitives in a sketchy look in http://p5js.org/.

With scribble-p5.js you can draw
- lines
- curves
- rects
- rects with rounded corners
- ellipses
- hachures

in a sketchy look

Much of the source code is taken from the handy library for processing,
written by Jo Wood, giCentre, City University London based on an idea by Nikolaus Gradwohl.
https://github.com/gicentre/handy

# How to use scribble-p5.js
To include scribble-p5.js

    <script language="javascript" type="text/javascript" src="/path/to/scribble-p5.js"></script>
  
## Lines

    scribbleLine( x1, y1, x2, y2, maxOffset );
  
Draws a line from (x1/y1) to (x2/y2)
maxOffset is optional and overwrites the scribble.maxOffset

## Curves

    scribbleCurve( x1, y1, x2, y2, x3, y3, x4, y4 );
  
Draws a bezier curve from (x1/y1) to (x2/y2). (x3/y3) and (x4/y4) are the coordinates, the curve is pulled to

## Rects

    scribbleRect( x, y, w, h, maxOffset );
    
Draws a rect centered at (x/y). w and h defines width and height.
maxOffset is optional and overwrites the scribble.maxOffset

    scribbleRoundedRect( x, y, w, h, radius );
    
Draws a rect like scribbleRect but with rounded corners.

## Ellipses

    scribbleEllipse( x, y, w, h );
    
Draws an allipse centered at (x/y). w and h defines width and height.

## Hachures

    scribbleFilling( xCoords, yCoords, gap, angle );
    
Draws a hachure in the polygon defined by the coordinates from the arrays xCoords and yCoords.
The gap defines the space between two hachure lines.
the angle defines the orientation of the lines.

## General appearance
To change the look you can change the following attributes

    scribble.bowing = yourValue;          // changes the bowing of lines
    scribble.roughness = yourValue;       // changes the roughness of lines
    scribble.maxOffset = yourValue;       // coordinates will get an offset, here you define the max offset
    scribble.numEllipseSteps = yourValue; // defines how much curves will be used to draw an ellipse
  
This lib works much on ramdom so if you want that your drawings look the same every render step, you should set a seed.

    ramdomSeed( yourSeed );

## Color and Weight  
Colors and Weights are defined in p5.js. 

    stroke( 255, 0, 0 );
    
From now on your sketchy drawings are red.

    strokeWeight( 10 );
    
From now on your sketchy drawings are 10 px heavy.

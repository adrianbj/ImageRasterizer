ImageRasterizer
===============

ProcessWire module for rasterizing vector SVG images and adding them into the same image field

##Requirements
This module requires Imagemagick and the pecl imagick extension. 
It also tends to give better results if your version of imagemagick is compiled with rsvg and sometimes even the version of rsvg can make a significant difference.
If everything is set up correctly, the rendered PNGs should be "perfect" representations of the SVGs.


To use you need to add SVG as an allowed file type for a multiple images field.

Upload an SVG image and the module will generate a fully transparent (alpha) PNG version. You need to save the page to see the PNG version which can then be accessed via the API like any other image.

More features coming soon.

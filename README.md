ImageRasterizer
===============

ProcessWire module for rasterizing vector SVG images and adding them into the same image field

###Requirements
This module requires Imagemagick and the pecl imagick extension.
For good quality results imagemagick must compiled with a recent version of rsvg. If you don't manage your own server and the results are not good, check with your host.
If everything is set up correctly, the rendered PNGs will be "perfect" representations of the SVGs.

###How to use

You must add SVG as an allowed file type for a multiple images field.

Check the module configuration for a variety of settings for both PNG and JPG output options. You need to be running a recent dev version (or 2.4 stable once available) of Processwire that supports field dependencies for the configuration settings to work as expected.

Upload an SVG image and the module will create a rasterized version.
You need to save the page to see the rasterized version which can then be accessed via the API like any other image.

####Support Forum
http://processwire.com/talk/topic/4632-image-rasterizer/

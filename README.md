ImageRasterizer
===============

ProcessWire module for admin and front-end resizing and rasterizing of vector SVG images

###Requirements
IMPORTANT: This module requires Imagemagick and the pecl imagick extension. For anything but simple SVGs, you must make sure imagemagick was compiled with a relatively recent version of rsvg (I know that 2.32.1 works well and presumably anything more recent should also be fine).

If you don't manage your own server and the results are not good, check with your host. If everything is set up correctly, the rendered PNGs will be "perfect" representations of the SVGs.


###How to use

You must add SVG as an allowed file type for a multiple images field.

Check the module configuration for a variety of settings for both PNG and JPG output options.
In particular be aware of the Video Images Field selector. If you choose "None" only the SVG will be stored in the images field. You can still access rasterized versions via the rasterize() method - see below for details.

NB: You need to be running a recent dev version (or 2.4 stable once available) of Processwire that supports field dependencies for the configuration settings to work as expected.

* Upload an SVG image and the module will create a rasterized version.
* You need to save the page to see the rasterized version which can then be accessed via the API like any other image.
* The module also adds a new method: rasterize() which can be called from your templates like:
```
$image->rasterize(200,0)->url
```
* This method optionally resizes the vector version of the image and then rasterizes it so you can scale it infinitely and there will be no loss of quality. Make sure you point it to the svg version in your images field.

####Support Forum
http://processwire.com/talk/topic/4632-image-rasterizer/

ImageRasterizer
===============

ProcessWire module for admin and front-end resizing and rasterizing of vector SVG images

###Requirements
IMPORTANT: This module requires Imagemagick and the pecl imagick extension. For anything but simple SVGs, you must make sure imagemagick was compiled with a relatively recent version of rsvg (I know that 2.32.1 works well and presumably anything more recent should also be fine).

If you don't manage your own server and the results are not good, check with your host. If everything is set up correctly, the rendered PNGs will be "perfect" representations of the SVGs.


###How to use

You must add SVG as an allowed file type for a multiple images field.

Check the module configuration for a variety of settings for both PNG and JPG output options.
In particular be aware of the Rasterized Images Field selector. If you choose "None" only the SVG will be stored in the images field. You can still access rasterized versions via the rasterize() method - see below for details.

NB: You need to be running a recent dev version (or 2.4 stable once available) of Processwire that supports field dependencies for the configuration settings to work as expected.

Once the module configuration settings are completed:
* Upload an SVG image and the module will create a rasterized version.
* You need to save the page to see the rasterized version which can then be accessed via the API like any other image.
* The module also adds a new method: rasterize() which can be called from your templates like:
```
$image->rasterize(200,0)->url
```
* This method optionally resizes the vector version of the image and then rasterizes it so you can scale it infinitely and there will be no loss of quality. Make sure you point it to the svg version in your images field.

####Support Forum
http://processwire.com/talk/topic/4632-image-rasterizer/


## License

This program is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License
as published by the Free Software Foundation; either version 2
of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software
Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA  02110-1301, USA.

(See included LICENSE file for full license text.)

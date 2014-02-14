#smart_resize_image_png
Resizes you image and returns a PNG in a lot of different ways. You don't have to worry about ratios, transparencys or file types, you'll get a PNG just as you wish.

Forked from [@maxim](https://github.com/maxim/smart_resize_image)'s.

##Features/Usage:

* If you pass width as 0 (zero) -- this function will disregard width, and use height as constraint. Same vice versa.
* If you set "proportional" to false - the function will simply stretch (or shrink) the image to its full constraints.
* If one of the dimensions is set to zero, and proportional set to "false" - then the image will be forced to stretch or shrink the other dimension, and disregard the zeroed dimension (leave it the same).
* If proportional is set to true - the image will resize to constraints proportionally, once again, with possibility to have either width or height set to zero.
* The function can use either linux "rm" command, or php @unlink. Most probably you don't need to ever use that flag, but on some setups - @unlink won't work due to user access restrictions.
* The function will simply replace the file that you give it, with the resized file.
* The function supports gif, png, and jpeg, and preserves the transparency of gif and png images.
* Tested on GD version 2.0.28 only. 

There is a parameter "output" which can be set to either:  
* "file" - overwrite the given file (default)
* "browser" - output image through http - with correct mime type
* "return" - return GD Library Image object
* or any filename of choice - save changed version to output path

There is another parameter "delete_original". Speaks for itself.

##TODO
* Get it working just with PNG.
* Add a "sharper" to small resizes.
* Clean up a little bit. 


##License

Copyright (c) 2008 Maxim Chernyak  
Copyright (c) 2014 Jaime Caballero
 
Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:
 
The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.
 
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.